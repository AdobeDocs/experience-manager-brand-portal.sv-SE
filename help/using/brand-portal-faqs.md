---
title: Vanliga frågor
description: Få insikt i de vanliga frågorna om Adobe Experience Manager Assets Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: frequently-asked-questions
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
exl-id: 4a8f7fbd-7485-421d-a8db-755324d2dbef
source-git-commit: 60104481e8f0b883fbf2cf25c1562e8376882e54
workflow-type: tm+mt
source-wordcount: '1485'
ht-degree: 0%

---

# Vanliga frågor {#frequently-asked-questions}

Vanliga frågor och svar om Brand Portal fokuserar på frågor och problem som slutanvändarna kan råka ut för när de arbetar med den senaste versionen av Experience Manager Assets Brand Portal 6.4.6 eller tidigare.


## Brand Portal 6.4.6 - frågor och svar {#faqs-bp646}

**Fråga: Den befintliga gamla OAuth-slutpunkten (`https://legacy-oauth.cloud.adobe.io/login`) fungerar inte. Vad kan vara den möjliga orsaken?**

**Svar:** Äldre OAuth-konfiguration är föråldrad. Uppgradera Experience Manager Assets-författarinstanser till det senaste Service Pack-paketet och konfigurera det via Adobe Developer Console. Mer information finns i [Konfigurera Experience Manager Assets med Brand Portal](configure-aem-assets-with-brand-portal.md). För att äldre OAuth-konfiguration ska fungera tills du uppgraderar måste du dock uppdatera den äldre OAuth-slutpunkten till `https://hypnosisprod.ethos11-prod-or1.ethos.adobe.net/`.

**Fråga: Jag kan inte publicera resurserna i mappen för bidrag från Brand Portal till Experience Manager Assets efter uppgradering till Adobe Developer Console. Min författarinstans finns på Experience Manager Assets 6.5.4. Vad kan vara den möjliga orsaken?**

**Svar:** Ja, det finns ett känt fel när du publicerar resurser i mappen för bidrag till Experience Manager Assets 6.5.4 via Adobe Developer Console.

Problemet har åtgärdats i Experience Manager Assets 6.5.5. Du kan uppgradera din Experience Manager Assets-instans till den senaste Service Pack-versionen och [uppgradera dina konfigurationer](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) på Adobe Developer Console.


**Fråga: Jag ser inte innehåll i mappen för bidrag som publiceras från Brand Portal i Experience Manager Assets. Vad kan vara den möjliga orsaken?**

**Svar:** Kontakta Experience Manager Assets-administratören för att verifiera konfigurationerna och se till att din Brand Portal-klient bara är konfigurerad med en Experience Manager Assets-författarinstans.

Detta kan inträffa när du har konfigurerat en Brand Portal-klient för flera instanser av Experience Manager Assets-författare. Administratören konfigurerar till exempel samma Brand Portal-klientorganisation för Experience Manager Assets-författarinstansen i en staging- och produktionsmiljö. I det här fallet utlöses resurspubliceringen i Brand Portal, men Experience Manager Assets-författarinstansen kan inte importera resursen eftersom replikeringsagenten inte tar emot den begärande token.


**Fråga: Jag kan inte publicera resurser från Experience Manager Assets till Brand Portal. Replikeringsloggen anger att anslutningen gjorde timeout. Finns det en snabbkorrigering?**

**Svar:** Publiceringen misslyckas vanligtvis med ett timeout-fel om det finns flera väntande begäranden i replikeringskön. Kontrollera att replikeringsagenterna är konfigurerade för att undvika timeout för att lösa problemet.

Utför följande steg för att konfigurera replikeringsagenten:

1. Logga in på din Experience Manager Assets-författarinstans.
1. Navigera till **[!UICONTROL Deployment]** > **[!UICONTROL Replication]** från panelen **Verktyg**.
1. Klicka på **[!UICONTROL `Agents on author`]** på sidan Replikering. Du kan se de fyra replikeringsagenterna för din Brand Portal-klient.
1. Klicka på replikeringsagentens URL för att öppna agentinformationen.
1. Klicka på **[!UICONTROL Edit]** om du vill redigera inställningarna för replikeringsagenten.
1. Klicka på fliken **[!UICONTROL Extended]** i agentinställningarna.
1. Markera kryssrutan **[!UICONTROL Close Connection]**.
1. Upprepa steg 4 till 7 för att konfigurera alla fyra replikeringsagenterna.
1. Starta om servern och bekräfta anslutningen.


## Brand Portal 6.4.5 - frågor och svar {#faqs-bp645}

**Fråga: Vilken är den största förändringen i Brand Portal 6.4.5?**

**Svar:** Med Experience Manager Assets Brand Portal 6.4.5 kan användare överföra innehåll och publicera Contribute-mappen direkt från Brand Portal, utan att behöva administratörsbehörighet. Mer information finns i [Resurser i Brand Portal](brand-portal-asset-sourcing.md).



**Fråga: Har jag förlorat åtkomsten till befintliga resurser, funktioner eller konfigurationer som jag har skapat?**

**Svar:** Alla befintliga funktioner och konfigurationer förblir intakta. Slutanvändarna påverkas inte och innehållet förblir intakt.



**Fråga: När ska jag byta till den nya versionen av Brand Portal?**

**Svar:** Brand Portal 6.4.5 släpptes till produktion i oktober 2019. Och nästa version av Brand Portal förväntas bli klar i mars 2020.
För uppdateringar och versionsändringar rekommenderar Adobe att du spårar [versionsinformationen](brand-portal-release-notes.md) och [Nyheter i Brand Portal](whats-new.md).



**Fråga: Påverkar mina användare?**

**Svar:** Brand Portal 6.4.5-utgåvan finns endast i Brand Portal, så slutanvändarna påverkas inte.



**Fråga: Behöver jag någon åtgärd från min sida som Brand Portal-användare?**

**Svar:** Brand Portal 6.4.5 har en ny funktion som heter Resurser. Administratören måste konfigurera funktionen Resurser i Experience Manager Assets för att aktivera funktionen för Brand Portal-användare. Mer information finns i [Aktivera resurskälla](brand-portal-asset-sourcing.md).



**Fråga: Vem kan skapa en Contribute-mapp?**

**Svar:** Alla Experience Manager Assets-användare som har behörighet att skapa en mapp i Experience Manager Assets kan skapa en **Contribute**-mapp. Om du vill skapa en **Contribute**-mapp skapar du en mapp av typen **Resursbidrag**.
Den här mappen delas med de aktiva Brand Portal-användarna för att de ska kunna bidra.



**Fråga: Vad innehåller en Contribute-mapp?**

**Svar:** **Contribute**-mappen innehåller två undermappar **NEW** och **SHARED**. Till att börja med är mappen NEW tom och mappen SHARED innehåller referensinnehållet (återanvändbara resurser) för Brand Portal-användare.
Brand Portal-användarna kommer åt mappen **Contribute** och överför innehåll i mappen **NEW** .



**Fråga: Kan jag ändra namnet på en befintlig Contribute-mapp?**

**Svar:** **Nej**, du kan inte ändra namnet på en befintlig **Contribute**-mapp.



**Fråga: Vad är tillgångskrav med ett bidrag?**

**Svar:** Dokumentet **Brief** i mappen **Contribute** och referensinnehållet i mappen **SHARED** hjälper Brand Portal-användare att förstå bidragsbehoven och förväntningarna. Tillsammans kallas de tillgångskrav.

**Fråga: Kan jag överföra resurser till en tillåten mapp?**

**Svara:** Alla tillåtna mappar är inte tillåtna. En Brand Portal-användare kan bara överföra innehåll till mappen **Contribute** som delas av Experience Manager Assets- eller Brand Portal-administratörer.



**Fråga: Hur får jag åtkomst till en Contribute-mapp?**

**Svar:** Du kan bara komma åt en **Contribute**-mapp om den har delats med dig. Du får ett meddelande via e-post/puls varje gång en Contribute-mapp delas med dig. Du kommer åt Contribute-mappen via länken som delas i e-postmeddelandet. Du kan också logga in på din Brand Portal-instans och navigera till klockikonen för att få meddelanden om att få åtkomst till Contribute-mappen.

>[!NOTE]
>
>Om du inte är Brand Portal-användare ber du Experience Manager Assets-administratören att skapa din användare i Admin Console. Lägg sedan till din profil i användarkonfigurationsfilen i Brand Portal användarlista.


**Fråga: Vilket format har CSV-filen för användarimport?**

**Svar:** Formatet matchar det som Admin Console stöder för massanvändarimport. E-post, förnamn och efternamn är obligatoriska.



**Fråga: Vad fyller i listan med användare (Brand Portal-medarbetare) i listrutan Tillgångsbidragsanvändare?**

**Svar:** Användarna i listrutan fylls i från Brand Portal-användarkonfigurationsfilen (.csv) som har överförts till Experience Manager Assets.



**Fråga: Var kan jag se status för import- och publiceringsjobb?**

**Svar:** I Experience Manager Assets kan du se status för en import på jobbsidan för **async**. I Brand Portal kan du se status för ett publiceringsjobb i **[!UICONTROL Tools > Asset Contribution status]**.



**Fråga: Vilken frekvens har ett importjobb som regelbundet körs i Experience Manager?**

**Svar:** I Experience Manager Assets avsöks var femte minut.



**Fråga: Finns det ett tröskelvärde för hur många gånger en mapp kan publiceras från Brand Portal till Experience Manager Assets?**

**Svar:** Nej, alla resurser i mappen **NEW** publiceras till Experience Manager Assets oavsett om de publicerades tidigare eller inte. Varje gång en **Contribution**-mapp publiceras från Brand Portal till Experience Manager Assets ersätts innehållet i mappen **NEW** .



**Fråga: Hur överför jag nya resurser i en Contribute-mapp?**

**Svar:** Mer information finns i den detaljerade dokumentationen för [Överföra resurser till Contribute-mappen](brand-portal-publish-contribution-folder-to-brand-portal.md).



**Fråga: Jag kan inte se miniatyrbilder eller förhandsvisningar för resurserna som överförts till mappen NEW.**

**Svar:** Det är utformat eftersom det inte finns något arbetsflöde i Brand Portal.



**Fråga: Vad händer om en mapp publiceras från Experience Manager Assets till Brand Portal som är i full gång?**

**Svar:** I Experience Manager Assets bevaras loggar för varje gång en mapp publiceras till Brand Portal. Vid publiceringen läggs alla resurser som inte publiceras till i Brand Portal till i en replikeringskö. Alla resurser som läggs till i mappen efter att publiceringsjobbet har utlösts publiceras inte till Brand Portal. När en Experience Manager Assets-användare publicerar mappen igen publiceras endast de resurser som inte publicerades tidigare (som finns i replikeringskön) till Brand Portal. Den här processen gäller för alla mappar som publiceras från Experience Manager Assets till Brand Portal och för delade mappar i en Contribute-mapp.

**Fråga: Vem ska jag kontakta med frågor?**

**Svar:** Kontakta kontohanteraren eller kundsupporten för Adobe.

>[!NOTE]
>
>Versionsschemat är preliminärt och kan komma att ändras. Kontakta kontohanteraren eller kundsupporten för Adobe för att få det uppdaterade releaseschemat.


## Produktåtkomst och support (begränsade platser) {#product-access-and-support-restricted-sites}

Dessa webbplatser är bara tillgängliga för kunder. Om du är kund och behöver åtkomst kontaktar du kontohanteraren för Adobe.

<!--
* [](https://daycare.day.com) [Product Access](https://login.marketing.adobe.com)

* [Adobe Customer Support]()
-->
