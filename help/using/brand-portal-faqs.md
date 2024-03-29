---
title: Vanliga frågor
seo-title: null
description: Få insikt i de vanliga frågorna om Adobe Experience Manager Assets Brand Portal.
seo-description: null
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1496'
ht-degree: 0%

---

# Vanliga frågor {#frequently-asked-questions}

Vanliga frågor och svar om Brand Portal fokuserar på frågor och problem som slutanvändarna kan råka ut för när de arbetar med den senaste versionen av Experience Manager Assets Brand Portal 6.4.6 eller tidigare versioner.


## Brand Portal 6.4.6 - frågor och svar  {#faqs-bp646}

**Frågor. Den befintliga gamla OAuth-slutpunkten (`https://legacy-oauth.cloud.adobe.io/login`) fungerar inte. Vad kan vara den möjliga orsaken?**

**Ans.** Äldre OAuth-konfiguration är föråldrad. Du måste uppgradera Experience Manager Assets-författarinstanser till det senaste Service Pack-paketet och konfigurera det via Adobe Developer Console. Se [Konfigurera Experience Manager Assets med Brand Portal](configure-aem-assets-with-brand-portal.md) för mer information. För att äldre OAuth-konfiguration ska fungera tills du uppgraderar måste du dock uppdatera den äldre OAuth-slutpunkten till `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

<!--
**Ques. I have created a collection using the asset link shared by the administrator. But I am unable to create a share link for my collection. Do I need special permissions to do this?**

**Ans.** The functionality is by design, the viewer users are not permitted to share link for collections as they have limited privileges due to which they cannot add users to create a share link. It is a known issue that the share link for collections is currently visible to the viewer users. This issue will be fixed in the upcoming release, the option to share link for the collections will not be available to the viewer users.    
-->

**Frågor. Jag kan inte publicera resurserna i mappen för bidrag från Brand Portal till Experience Manager Assets efter att ha uppgraderat till Adobe Developer Console. Min författarinstans finns på Experience Manager Assets 6.5.4. Vad kan vara den möjliga orsaken?**

**Ans.** Ja, det finns ett känt fel när du publicerar material i mappen för bidrag till Experience Manager Assets 6.5.4 via Adobe Developer Console.

Problemet har åtgärdats i Experience Manager Assets 6.5.5. Du kan uppgradera din Experience Manager Assets-instans till den senaste Service Pack-versionen och [uppgradera dina konfigurationer](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) på Adobe Developer Console.

<!--
Broken link of download hotfix, comment out this section until we have the latest URL.

For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your AEM author instance.
-->

**Frågor. Jag ser inte innehållet i bidragsmappen som publicerats från Brand Portal i Experience Manager Assets. Vad kan vara den möjliga orsaken?**

**Ans.** Kontakta Experience Manager Assets-administratören för att verifiera konfigurationerna och se till att din Brand Portal-klient bara är konfigurerad med en Experience Manager Assets-författarinstans.

Detta kan inträffa när du har konfigurerat en Brand Portal-klient för flera instanser av Experience Manager Assets-författare. Administratören konfigurerar till exempel samma Brand Portal-klient på Experience Manager Assets författarinstans i staging- och produktionsmiljön. I det här fallet utlöses resurspubliceringen i Brand Portal men Experience Manager Assets författarinstans kunde inte importera resurskoden som replikeringsagenten inte får den begärande token.


**Frågor. Jag kan inte publicera material från Experience Manager Assets till Brand Portal. Replikeringsloggen anger att anslutningen gjorde timeout. Finns det en snabbkorrigering?**

**Ans.** Publiceringen misslyckas vanligtvis med ett timeout-fel om det finns flera väntande begäranden i replikeringskön. Kontrollera att replikeringsagenterna är konfigurerade för att undvika timeout för att lösa problemet.

Utför följande steg för att konfigurera replikeringsagenten:

1. Logga in på din Experience Manager Assets-författarinstans.
1. Från **verktyg** panel, navigera till **[!UICONTROL Deployment]** > **[!UICONTROL Replication]**.
1. Klicka på **[!UICONTROL Agents on author]**. Du kan se de fyra replikeringsagenterna för din Brand Portal-klient.
1. Klicka på replikeringsagentens URL för att öppna agentinformationen.
1. Klicka **[!UICONTROL Edit]** om du vill ändra inställningarna för replikeringsagenten.
1. Klicka på knappen **[!UICONTROL Extended]** -fliken.
1. Välj **[!UICONTROL Close Connection]** kryssruta.
1. Upprepa steg 4 till 7 för att konfigurera alla fyra replikeringsagenterna.
1. Starta om servern och bekräfta anslutningen.


## Brand Portal 6.4.5 - frågor och svar  {#faqs-bp645}

**Frågor. Vilken är den största förändringen i Brand Portal 6.4.5?**

**Ans.** Experience Manager Assets Brand Portal 6.4.5 är en funktionsversion som gör att Brand Portal-användare kan överföra innehåll från Brand Portal-instansen och publicera Contribute-mappen till Experience Manager Assets utan att behöva ha administratörsbehörighet.
Mer information finns i [Resurshantering i Brand Portal](brand-portal-asset-sourcing.md).



**Frågor. Kommer jag att förlora åtkomsten till befintliga resurser, funktioner eller konfigurationer som jag har skapat?**

**Ans.** Alla befintliga funktioner och konfigurationer förblir intakta. Slutanvändarna påverkas inte och innehållet förblir intakt.



**Frågor. När ska jag byta till den nya versionen av Brand Portal?**

**Ans.** Brand Portal 6.4.5 lanserades i oktober 2019. Och nästa version av Brand Portal förväntas släppas tredje kvartalet 2020.
För uppdateringar och versionsändringar rekommenderar vi att du spårar [Versionsinformation](brand-portal-release-notes.md) och [Nyheter i Brand Portal](whats-new.md).



**Frågor. Kommer mina användare att påverkas?**

**Ans.** Brand Portal 6.4.5 finns endast i Brand Portal, så slutanvändarna påverkas inte.



**Frågor. Måste jag som Brand Portal-användare vidta någon åtgärd?**

**Ans.** Brand Portal 6.4.5 har en ny funktion som heter Asset Sourcing. Administratören måste konfigurera funktionen Resurser i Experience Manager Assets för att aktivera funktionen för Brand Portal-användare. Mer information finns i [Aktivera resurskälla](brand-portal-asset-sourcing.md).



**Frågor. Vem kan skapa en Contribute-mapp?**

**Ans.** Alla Experience Manager Assets-användare som har behörighet att skapa en ny mapp i Experience Manager Assets kan skapa **Bidrag** mapp. Skapa en **Bidrag** mapp, skapa en ny mapp av typen **Resursbidrag**.
Den här mappen delas med de aktiva Brand Portal-användarna för att de ska kunna bidra.



**Frågor. Vad innehåller en Contribute-mapp?**

**Ans.** **Bidrag** mappen innehåller två undermappar **NYHET** och **DELAD**. Till att börja med är mappen NEW tom och mappen SHARED innehåller referensinnehållet (återanvändbara resurser) för Brand Portal-användare.
Brand Portal-användare har åtkomst till **Bidrag** och ladda upp innehåll i **NYHET** mapp.



**Frågor.  Kan jag ändra namnet på en befintlig Contribute-mapp?**

**Ans.** **Nej** kan du inte ändra namnet på en befintlig **Bidrag** mapp.



**Frågor. Vad är tillgångskrav utan bidrag?**

**Ans.** The **Kort** dokumentet som är kopplat till **Bidrag** och referensinnehållet (återanvändbara resurser) som överförts i **DELAD** kan Brand Portal-användaren förstå behovet av bidrag och förväntningar som medverkande och kallas gemensamt för tillgångskrav.



**Frågor. Kan jag överföra resurser till en tillåten mapp?**

**Ans.** Inte alla tillåtna mappar. En Brand Portal-användare kan bara överföra innehåll till **Bidrag** som delas av Experience Manager Assets- eller Brand Portal-administratören.



**Frågor. Hur får jag åtkomst till en Contribute-mapp?**

**Ans.** Du kan komma åt en **Bidrag** endast om den har delats med dig. Du får ett meddelande via e-post/puls när en Contribute-mapp delas med dig. Du kan antingen komma åt Contribute-mappen via länken som delas i e-postmeddelandet eller logga in på din Brand Portal-instans och navigera till klockikonen för att få meddelanden om att komma åt Contribute-mappen.

>[!NOTE]
>
>Om du inte är en befintlig Brand Portal-användare ber du Experience Manager Assets-administratören att skapa din användare i Admin Console och lägga till din profil i användarkonfigurationsfilen i Brand Portal användarlista.

**Frågor. Vilket format har CSV-filen för användarimport?**

**Ans.** Formatet är samma som det som stöds av Admin Console för massanvändarimport. E-post, förnamn och efternamn är obligatoriska.



**Frågor. Vad fyller i listan med användare (Brand Portal-medverkande) i listrutan Tillgångsmedverkande användare?**

**Ans.** Användarna i listrutan fylls i från Brand Portal-användarkonfigurationsfilen (.csv) som har överförts till Experience Manager Assets.



**Frågor. Var kan jag se status för import- och publiceringsjobb?**

**Ans.** I Experience Manager Assets ser du status för en import i **async** jobbsida. I Brand Portal kan du se status för ett publiceringsjobb i **[!UICONTROL Tools > Asset Contribution status]**.



**Frågor. Vilken frekvens har ett importjobb som periodvis körs i Experience Manager?**

**Ans.** I Experience Manager Assets avsöks var femte minut.



**Frågor. Finns det någon begränsning för hur många gånger en mapp kan publiceras från Brand Portal till Experience Manager Assets?**

**Ans.** Nej, alla resurser i **NYHET** -mappen publiceras på Experience Manager Assets oavsett om de publicerades tidigare eller inte. Varje gång **Bidrag** -mappen publiceras från Brand Portal till Experience Manager Assets, den åsidosätter innehållet i **NYHET** mapp.



**Frågor. Hur överför jag nya resurser i en Contribute-mapp?**

**Ans.** Mer information finns i den detaljerade dokumentationen [Överför resurser till Contribute-mappen](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Frågor. Kan jag inte se miniatyrbilder/förhandsvisningar av de mediefiler som en Brand Portal-användare har överfört till den NYA mappen?**

**Ans.** Det är utformat, eftersom det inte finns något arbetsflöde i Brand Portal.



**Frågor. Vad händer om en mapp publiceras från Experience Manager Assets till Brand Portal som är i full gång?**

**Ans.** I Experience Manager Assets bevaras loggar för varje gång en mapp publiceras till Brand Portal. Vid publiceringen placeras alla resurser som inte publiceras till Brand Portal i en replikeringskö. Alla resurser som läggs till i mappen efter att publiceringsjobbet har utlösts publiceras inte till Brand Portal. När Experience Manager Assets-användaren publicerar mappen igen publiceras endast resurser som inte publicerades tidigare (som finns i replikeringskön) till Brand Portal.
Detta gäller för alla mappar som publiceras från Experience Manager Assets till Brand Portal och för delade mappar i en Contribute-mapp.

**Frågor. Vem kontaktar jag med frågor?**

**Ans.** Kontakta kontohanteraren för Adobe eller kundsupporten.

>[!NOTE]
>
>Releasedatan är preliminärt och kan komma att ändras. Kontakta kontohanteraren eller kundsupporten för Adobe för att få det uppdaterade releaseschemat.


## Produktåtkomst och support (begränsade platser) {#product-access-and-support-restricted-sites}

Dessa webbplatser är bara tillgängliga för kunder. Om du är kund och behöver åtkomst kontaktar du din kontoansvarige på Adobe.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
