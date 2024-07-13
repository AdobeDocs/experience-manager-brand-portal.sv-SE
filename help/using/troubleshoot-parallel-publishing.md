---
title: Felsöka problem vid parallell publicering till Brand Portal
seo-title: Troubleshoot issues in parallel publishing to Brand Portal
description: Felsöka parallell publicering.
seo-description: Troubleshoot parallel publishing.
uuid: 51e45cca-8c96-4c69-84ef-2ef34f3bcde2
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: brand-portal
discoiquuid: a4801024-b509-4c51-afd8-e337417e658b
role: Admin
exl-id: 631beabc-b145-49ba-a8e4-f301497be6da
source-git-commit: 72cd0ebbf05067287d94e1dc4e1b68f5fb6c2888
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---

# Felsöka problem vid parallell publicering till Brand Portal {#troubleshoot-issues-in-parallel-publishing-to-brand-portal}

Brand Portal är konfigurerat med Experience Manager Assets för att ha godkänt varumärkesresurser som sömlöst importerats (eller publicerats) från Experience Manager Assets författarinstans. När [konfigurerats](../using/configure-aem-assets-with-brand-portal.md) använder Experience Manager Author en replikeringsagent för att replikera de markerade resurserna till Brand Portal molntjänst för godkänd användning av Brand Portal-användare. Flera replikeringsagenter används Experience Manager 6.2 SP1-CFP5, Experience Manager CFP 6.3.0.2 och senare för att möjliggöra parallell publicering med hög hastighet.

>[!NOTE]
>
>Adobe rekommenderar uppgradering till Experience Manager 6.4.1.0 för att säkerställa att Experience Manager Assets Brand Portal konfigureras med Experience Manager Assets. En begränsning i Experience Manager 6.4 ger ett fel när Experience Manager Assets konfigureras med Brand Portal och replikeringen misslyckas.

När molntjänsten konfigureras för Brand Portal under **[!UICONTROL /etc/cloudservice]** genereras alla nödvändiga användare och token automatiskt och sparas i databasen. Molntjänstkonfigurationen skapas. Tjänstanvändare som krävs för replikerings- och replikeringsagenter för att replikera innehåll skapas också. Den skapar fyra replikeringsagenter. När du publicerar ett stort antal resurser från Experience Manager till Brand Portal står resurserna i kö och distribueras mellan replikeringsagenterna via Round Robin.

Publiceringen kan misslyckas ibland på grund av stora snedställningsjobb, ökat nätverk och **[!UICONTROL Disk I/O]** på Experience Manager Author-instansen eller långsammare prestanda för Experience Manager Author-instansen. Därför bör du testa anslutningen till replikeringsagenterna innan du börjar publicera.

![](assets/test-connection.png)

## Felsöka fel vid förstagångspublicering: verifiera din publiceringskonfiguration {#troubleshoot-failures-in-first-time-publishing-validating-your-publish-configuration}

Så här validerar du dina publiceringskonfigurationer:

1. Kontrollera felloggarna
1. Kontrollera om replikeringsagenten har skapats
1. Testanslutning

**Slutloggar när Cloud Service skapas**

Kontrollera slutloggar. Kontrollera om replikeringsagenten har skapats eller inte. Om det inte går att skapa replikeringsagenten kan du redigera molntjänsten genom att göra mindre ändringar i molntjänsten. Validera och kontrollera igen om replikeringsagenten har skapats eller inte. Om inte kan du redigera tjänsten igen.

Om molntjänsten inte konfigureras korrekt upprepade gånger ska du rapportera en dagis-biljett.

**Testa anslutningen med replikeringsagenter**

Visa logg, om fel påträffas i replikeringsloggen:

1. Kontakta kundsupport.

1. Försök rensa [upp](../using/troubleshoot-parallel-publishing.md#clean-up-existing-config) igen och skapa publiceringskonfigurationen igen.

<!--
Comment Type: remark
Last Modified By: Mini Gulati (mgulati)
Last Modified Date: 2018-06-21T22:56:21.256-0400
<p>?? check and compare public key. At times public key is different</p>
<p>?? another thing to check in /useradmin</p>
-->

## Rensa befintliga publiceringskonfigurationer för Brand Portal {#clean-up-existing-config}

Oftast när publiceringen inte fungerar kan orsaken vara att den användare som publicerar (till exempel: `mac-<tenantid>-replication` inte har den senaste privata nyckeln, och publiceringen misslyckas därför med felet&quot;401 obehörig&quot; och inga andra fel rapporteras i replikeringsagentloggarna. Du kanske vill undvika felsökning och skapa en konfiguration i stället. För att den nya konfigurationen ska fungera på rätt sätt bör du rensa följande från författarinställningarna i Experience Manager:

1. Gå till `localhost:4502/crx/de/` (eftersom du kör författarinstans på localhost:4502:)\
   i. delete `/etc/replication/agents.author/mp_replication`
ii. ta bort `/etc/cloudservices/mediaportal/<config_name>`

1. Gå till localhost:4502/useradmin:\
   i. sök efter användare `mac-<tenantid>replication`
ii. ta bort den här användaren

Nu är systemet städat. Nu kan du försöka skapa en molntjänstkonfiguration och fortfarande använda det befintliga JWT-programmet. Du behöver inte skapa något program, utan istället uppdatera den offentliga nyckeln från den nya molnkonfigurationen.

>[!NOTE]
>
>Ändra inte några autogenererade inställningar.


## Problem med klientsynlighet för JWT-program för utvecklaranslutning {#developer-connection-jwt-application-tenant-visibility-issue}

Om den `https://legacy-oauth.cloud.adobe.io/` finns visas alla organ (klientorganisationer) som de aktuella användarna har systemadministratör för. Om du inte hittar organisationsnamnet här eller om du inte kan skapa ett program för en nödvändig klient här, kontrollerar du om du har tillräcklig behörighet (systemadministratör).

Det finns ett känt fel i det här användargränssnittet som innebär att för alla innehavare visas endast de tio viktigaste programmen. När du skapar programmet ska du stanna kvar på den sidan och skapa ett bokmärke för webbadressen. Du behöver inte gå till programmets listsida och hitta det program du har skapat. Du kan trycka på den här bokmärkesadressen direkt och uppdatera/ta bort programmet vid behov.

JWT-programmet kanske inte visas korrekt. Du bör därför anteckna/bokmärka URL-adressen när du skapar ett JWT-program.

## Konfigurationen som körs slutar fungera {#running-configuration-stops-working}

<!--
Comment Type: draft

<p>If the running configuration stops working, either of the following two possibilities
<g class="gr_ gr_15 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar multiReplace" data-gr-id="15" id="15" style="font-size: 12px;">
are
</g> there:</p>
<p>1.
<g class="gr_ gr_14 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="14" id="14">
Connection
</g> has failed, or</p>
<p>2. Publish has failed with permission to dam-replication-service denied, while connection has passed </p>
<p>If the connection has failed [1], the
<g class="gr_ gr_10 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling ins-del multiReplace" data-gr-id="10" id="10">
fail safe
</g> way to fix it is to <a href="../using/troubleshoot-parallel-publishing.md#main-pars-header-1664955658">clean up</a> the existing Brand Portal publish configuration and recreate a publish configuration. </p>
<p>However, if the
<g class="gr_ gr_18 gr-alert gr_spell gr_inline_cards gr_run_anim ContextualSpelling" data-gr-id="18" id="18">
publish
</g> has failed with
<g class="gr_ gr_16 gr-alert gr_gramm gr_inline_cards gr_run_anim Grammar only-ins doubleReplace replaceWithoutSep" data-gr-id="16" id="16">
permission
</g> denied to dam-replication-service, raise a support ticket.</p>
-->

Om en replikeringsagent (som publicerade till Brand Portal bara fint) slutar bearbeta publiceringsjobb bör du kontrollera replikeringsloggarna. Experience Manager har automatiskt gjort ett nytt försök, så om en viss resurspublicering misslyckas görs ett nytt försök automatiskt. Om det uppstår något tillfälligt problem, t.ex. ett nätverksfel, kan det lyckas under ett nytt försök.

Om det finns kontinuerliga publiceringsfel och kön är blockerad bör du kontrollera **[!UICONTROL test connection]** och försöka lösa de fel som rapporteras.

Beroende på felen rekommenderar vi att du loggar en supportanmälan så att Brand Portal tekniker kan hjälpa dig att lösa problem.

## Konfigurationstoken för Brand Portal IMS har upphört att gälla {#token-expired}

Om Brand Portal-miljön avbryts plötsligt finns det en risk för att IMS-konfigurationerna inte fungerar som de ska. Systemet visar en felfri IMS-konfiguration och visar ett felmeddelande (liknande följande) om att din åtkomsttoken har upphört att gälla.

`com.adobe.granite.auth.oauth.AccessTokenProvider failed to get access token from authorization server status: 400 response: Unknown macro: {"error"}`

Du bör spara och stänga IMS-konfigurationen manuellt och kontrollera hälsostatusen igen för att lösa problemet. Om konfigurationerna inte fungerar tar du bort de befintliga konfigurationerna och skapar en ny.


## Konfigurera replikeringsagenter för att undvika timeoutfel i anslutningen {#connection-timeout}

Publiceringsjobbet misslyckas vanligtvis med ett timeout-fel om det finns flera väntande begäranden i replikeringskön. Kontrollera att replikeringsagenterna är konfigurerade för att undvika timeout för att lösa problemet.

Så här konfigurerar du replikeringsagenterna:

1. Logga in på din AEM Assets-författarinstans.
1. Navigera till **[!UICONTROL Deployment]** > **[!UICONTROL Replication]** från panelen **Verktyg**.
1. Klicka på **[!UICONTROL Agents on author]** på sidan Replikering. Du kan se de fyra replikeringsagenterna för din Brand Portal-klient.
1. Klicka på replikeringsagentens URL och klicka på **[!UICONTROL Edit]**.
1. Klicka på fliken **[!UICONTROL Extended]** i Agentinställningar.
1. Markera kryssrutan **[!UICONTROL Close Connection]**.
1. Upprepa steg 4 till 7 för att konfigurera alla fyra replikeringsagenterna.
1. Starta om servern.
