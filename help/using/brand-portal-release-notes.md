---
title: Versionsinformation
description: Få en inblick i funktioner, förbättringar, åtgärdade kritiska problem och kända fel i Adobe Experience Manager Assets Brand Portal 2024.02.0.
content-type: reference
contentOwner: Kirandeep Kour
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: e4e89080-9863-4857-8f3a-fcd516ef3271
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 1%

---

# Versionsinformation {#release-notes}

Få en inblick i de nya funktionerna, förbättringarna, de allvarliga problemen och de kända problemen i Adobe Experience Manager Assets Brand Portal 2024.02.0.

## Versionsinformation {#release-information}

| Produkt | Adobe Experience Manager Assets Brand Portal |
|---|---|
| Version | 2024.02.0 |
| Datum | Februari 2024 |

## Ökning {#overview}

Adobe Experience Manager (AEM) Assets Brand Portal hjälper er att enkelt skaffa, styra och på ett säkert sätt distribuera godkänt material till externa parter och interna användare på olika enheter. Det bidrar till att effektivisera delning av tillgångar, kortar time-to-market för tillgångar och minskar risken för bristande efterlevnad och obehörig åtkomst. Med Brand Portal kan man bläddra bland, söka, förhandsgranska, ladda ned och exportera material i företagsgodkända format - när som helst, var som helst.

## Nyheter i 2024.02.0 {#whats-new-in-2024.02.0}

### Allvarliga problem har åtgärdats {#critical-issues-fixed}

#### Felkorrigeringar {#bug-fixes}

Den här versionen innehåller följande felkorrigeringar:

* Det går inte att hämta digitala resurser som skyddas av DRM på den turkiska språkinställningen.
* Det går inte att öppna och hämta befintliga rapporter som innehåller resurser med flerradsrubrik.
* När du hämtar resurser med knappen [!UICONTROL Download] från åtgärdsfältet hämtas maximalt 1 000 resurser.
* Felaktigt namn på resurser av typen PSD när de visas i innehållsträdet.
* Alternativet [!UICONTROL Delete Rendition] på sidan med resursinformation fungerar inte.
* Feljusterad rubrik och storlek för resurser i hämtningsfönstret.
* När du skapar en rapport lokaliseras inte etiketter.
* Supportadministratörer kallades administratörer i Brand Portal.

## Tidigare versioner

### Oktober 2023-versionen {#oct-2023}

**Felkorrigeringar och förbättringar**
Den här versionen innehåller följande förbättringar:

* Prestandaförbättringar vid bläddring genom [!UICONTROL Collections].

* Förbättringar av sökresultat när en del av sökningen utförs med OmniSearch-fältet.

Den här versionen innehåller följande felkorrigeringar:

* Det går inte att spara [!UICONTROL Date]- och [!UICONTROL Options]-predikat till [!UICONTROL Smart Collection].

* Formatet [!UICONTROL Date and Time] är inkonsekvent när du arbetar på andra språk än engelska.

* Knappen [!UICONTROL Delete] saknas när du söker efter resurser.

* Om fältet [!UICONTROL Title] innehåller multibytesymboler i [!UICONTROL Link Share] kan rapporten inte hämtas.

* När du visar ett dokument av PDF-typ är etiketterna och verktygstipsen inte lokaliserade.

### Augustiversionen 2023 {#aug-2023}

**Felkorrigeringar och förbättringar**
Den här versionen innehåller följande förbättringar:

* Prestandaförbättringar vid inläsning av resurser på popup-fönstret [!UICONTROL Download].
* När du hämtar en resurs eller en återgivning av en resurs hämtas den nu i det ursprungliga filformatet i stället för i en zip-fil.

Den här versionen innehåller följande felkorrigeringar:

* De långa etiketterna eller taggarna visas inte korrekt för sökfilter.
* Det går inte att visa långa återgivningsnamn i dialogrutan Hämta.
* Det går inte att förhandsgranska videomaterial i kortvyn.

### Version från maj 2023 {#may-2023}

**Felkorrigeringar**
Den här versionen innehåller korrigeringar av följande allvarliga problem:

* Om ett fel inträffar när en resurs hämtas från en delad länk är etiketterna `Notice` och `Close` i felmeddelandet inte lokaliserade.
* Brand Portal visar **Request Header-fälten för stora**-fel vid åtkomst av sökfilter i rutan `Filter`.

**Kända fel**
Den här versionen innehåller följande kända fel:

* Delvis lokalisering i rapportinnehåll för tillgångskälla.
* Det går inte att redigera få fält i användarprofilen.

### Version från februari 2023 {#feb-2023}

**Felkorrigeringar**

Den här versionen innehåller korrigeringar av följande allvarliga problem:

* Profilbilden kan inte uppdateras på Brand Portal.
* Det går inte att ändra storlek på innehållsträdrutan. Om filnamnet är längre än innehållsträdets standardbredd kan du inte dra innehållsträdet både vågrätt och lodrätt. Därför går det inte att läsa längre filnamn.
* Sökresultaten är inkonsekventa för samma egenskapsprediat som används två gånger i sökformulären.
* Texten på de mellanliggande inloggningssidorna är inte lokaliserad för alla språk.

**Förbättringar**

Den här versionen innehåller följande förbättringar:

* Det finns nu ett nytt modernt visningsprogram för PDF för en förbättrad förhandsvisning av resurserna i PDF.
* Du kan nu välja att aktivera eller inaktivera meddelanden om resurskälla för administratörer. Navigera till [!UICONTROL General Settings] och aktivera eller inaktivera sedan [!UICONTROL `Notify Administrator of asset contribution`].

  ![Meddela administratören om resursbidrag](assets/notify-admin.png)

* En obehörig användare kan inte begära åtkomst till Brand Portal om åtkomstbegäran är inaktiverad.
* Endast de organisationer som har etablerats för Brand Portal visas i listan med profilväljare.

**Kända fel**

Den här versionen innehåller följande kända fel:

* Delvis lokalisering i rapportinnehåll för tillgångskälla.
* Det går inte att redigera få fält i användarprofilen.

### Oktober 2022-versionen {#oct-2022}

**Allvarliga fel har åtgärdats**

Den här versionen innehåller korrigeringar av följande allvarliga problem:

* Sakta svarstider vid kopiering av stora filer från Brand Portal till ett verktyg från tredje part.
* När du markerar kryssrutan för antal återgivningar inaktiveras kryssrutorna för att välja enskilda återgivningar.
* Sakta svarstid för sökning.

>[!IMPORTANT]
>
>Pulsmeddelanden i AEM Assets Brand Portal upphör den 1 december 2022. I stället för Pulse-meddelanden får du även fler e-postmeddelanden om följande händelser:
>
>* Dela resurser via länk
>* Begär åtkomstarbetsflöde
>* Delning av bidragsmapp
>* Initierar export till AEM
>* Exporten till AEM har slutförts
>

### Version från augusti 2022 {#aug-2022}

**Allvarliga fel har åtgärdats**

Den här versionen innehåller korrigeringar av följande allvarliga problem:

* När NUI inte kan bearbeta en resurs i Experience Manager visas en felaktig status för resursimportering i Brand Portal.
* När förhandsgranskningsåtgärden misslyckas finns det inget meddelande om att meddela felet.
* Det felaktiga värdet för egenskapen `totalUploadedSize` för varje tillgång är fast.
* När du klickar på **Hämta alla objekt** och det finns ett stort antal renderingar tillgängliga för en resurs hämtar Brand Portal en ogiltig ZIP-fil.
* Översättningen av vissa strängar trunkeras i Brand Portal användargränssnitt.

### Version från maj 2022 {#may-2022}

**Nya funktioner**

Brand Portal kör nu automatiska jobb var tolfte timme för att ta bort alla Brand Portal-resurser som publicerats till AEM. Därför behöver du inte ta bort resurserna i Contribute-mappen manuellt för att mappstorleken ska hållas under tröskelvärdet.

**Allvarliga fel har åtgärdats**

Den här versionen innehåller korrigeringar av följande allvarliga problem:

* När du hämtar en mapp eller en samling som innehåller resurser med färgtaggar hämtas även en XML-fil.
* När du hämtar en video som innehåller återgivningar skapar Brand Portal en ogiltig ZIP-fil.
* När du skapar förinställningar och resurser AEM författaren och sedan publicerar dem på Brand Portal kan du välja dynamiska återgivningar medan du hämtar resurserna. Du kan dock inte extrahera den hämtade ZIP-filen. Detta förhindrar åtkomst till det hämtade innehållet.
* Problem vid hämtning av videomaterial från vissa mappar som är tillgängliga på Brand Portal.
* När du delar Contribute-mappens URL med hjälp av ett e-postmeddelande stöter rollerna Viewer och Editor på problem när de får åtkomst till den överordnade mappen med hjälp av paketet.
* En publicerad rapport visar en felaktig jobbstarttid.

### Version från februari 2022 {#feb-2022}

**Nya funktioner**

* Tröskelvärdet för sessionstimeout för gästanvändare har reducerats från 2 timmar till 15 minuter.
* Det extra alternativet **[!UICONTROL View pages]** har tagits bort för flersidig PDF eftersom användaren nu kan visa PDF-sidorna från Adobe Document Cloud Viewer.
* Användarna kan inte söka i, navigera i eller öppna mappar. Användargränssnittet visar felmeddelandet: `Failed to load data`.
* Panelen **[!UICONTROL Renditions]** innehåller inte alla statiska återgivningar av resurserna som publiceras till Brand Portal.
* På panelen **[!UICONTROL Renditions]** visas de smarta beskärningsåtergivningarna för resursen, men användaren kan inte förhandsvisa eller hämta de smarta beskärningsåtergivningarna.
* I hämtningsdialogrutan visas smarta beskärningsåtergivningar för den valda resursen, men användaren kan inte hämta smarta beskärningsåtergivningar.
* En icke-admin-användare får bara den ursprungliga resursåtergivningen när en resurs hämtas. Återgivningarna för systemet och anpassade versioner hämtas inte.
* När du använder sökfilter för att hämta en resurs inaktiveras knappen `Download` i hämtningsdialogrutan och användaren kan inte hämta resursen.
* Om `Smart Tags` och (eller) `Color Tags` är aktiverade visas `json`-filerna som återgivningar i hämtningsdialogrutan och dessa `json`-filer hämtas till den arkiverade zip-mappen.
* De anonyma användarna kan inte hämta resurser via en delad länk eftersom länken dirigerar om till Brand Portal inloggningssida.
* Systemet återspeglar inte rätt värde för antalet aktiva samtidiga användare.

<!--
### New Features {#new-features}

This release includes the following new features:

* AEM Assets as a Cloud Service is now entitled to have a pre-configured Brand Portal instance. The Cloud Manager user can activate Brand Portal on the AEM Assets as a Cloud Service instance.

* Asset Sourcing feature is now available on AEM Assets as a Cloud Service. It allows the Brand Portal users to upload assets to the permitted contribution folders and publish the contribution folder from Brand Portal to AEM Assets as a Cloud Service instance. 

* An additional **[!UICONTROL Asset Download]** setting has been introduced under the **[!UICONTROL Download Settings]**. It creates a separate folder for each asset while downloading the folders, collections, or bulk download of assets. 
-->
<!-- 
* The **[!UICONTROL Download]** dialog is revamped in a list view with additional options to exclude the renditions which are not required, apply the same set of rules for similar asset types, and download the selected asset renditions.
-->

<!--
* The new **[!UICONTROL Download]** dialog now appears with all the renditions of the selected assets or folders containing assets in a list view, wherein the Brand Portal users can apply same set of renditions for similar asset types and download the selected asset renditions. 
-->

<!-- 
* Navigation to the **[!UICONTROL Files]**, **[!UICONTROL Collections]**, and **[!UICONTROL Shared Links]** is now possible from all the Brand Portal pages in one-click.  

* The **[!UICONTROL Renditions]** panel in the asset details page now allows the Brand Portal users to select the original asset and (or) specific asset renditions, and directly download them from the **[!UICONTROL Renditions]** panel without having to open the **[!UICONTROL Download]** dialog.
-->

<!--
Brand Portal users can exclude specific renditions which are not required and directly download the original asset and its renditions from the **[!UICONTROL Renditions]** panel on the asset details page. 
-->

<!-- 
* In addition to the existing **[!UICONTROL Download]** configurations, the Brand Portal administrators can also [configure permissions for different group of users]() to view and (or) download the original asset and its renditions from the asset details page. These configurations will define who can access and (or) download the asset renditions.
-->

<!--
### Enhancements {#enhancements}

Brand Portal 2021.08.0 is an internal release that introduces Business profiles for enterprise and teams customers to give organizations better control over their assets. 

This release includes the following enhancements:

* The users now have organization-specific entitlement on the new and migrated organizations. If a user is entitled to multiple organizations, the user has to select the organization at the time of login.

* The new users that are added in Admin Console must **Join Team** to get entitled to the organization. 

>[!NOTE]
>
>Business profiles are currently applicable for the new organizations that are created after August 16, 2021. 
>
>Until your organization is migrated, you can continue to use Adobe ID, Enterprise ID, or Federated ID types to access the organization.   
-->

<!-- 
* For folder download, a separate folder is created for each asset using share link irrespective of the **[!UICONTROL Download Settings]**. 
* The Brand Portal **[!UICONTROL Usage Report]** has been modified to reflect only the active Brand Portal users.
-->

<!--
* The threshold of session timeout for the guest users has been reduced from 2 hours to 15 minutes.
* The additional **[!UICONTROL View pages]** option has been removed for multi-page PDFs as the user can now view the PDF pages from the Adobe Document Cloud Viewer.

* The users are unable to search, navigate, or open folders. The user interface reflects the error message: `Failed to load data`. 
* The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal.
* The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
* The download dialog lists the smart crop renditions of the selected asset, however, the user cannot download the smart crop renditions. 
* A non-admin user is getting only the original asset rendition when downloading an asset. The system and custom renditions are not downloaded.  
* When applying search filter to download an asset, the `Download` button is disabled in the download dialog and does not allows the user to download the asset.
* If `Smart Tags` and (or) `Color Tags` are enabled, the download dialog lists the `json` files as renditions and downloads these `json` files in the archived zip folder.
* The anonymous users are unable to download assets using a shared link because the link redirects to the Brand Portal login page. 
* The system is not reflecting the correct value for the number of active concurrent users.
-->

<!--
### New features {#new-features}

Brand Portal now executes automatic jobs every twelve hours to delete all Brand Portal assets that are published to AEM. As a result, you do not need to delete the assets in the Contribution folder manually to keep the folder size below the threshold limit. See [What's new in Experience Manager Assets Brand Portal](whats-new.md).
-->

<!--
This release includes fixes to the following critical issues:

* When you download a folder or a collection that includes assets with color tags, an XML file gets downloaded as well.

* When you download a video that includes renditions, Brand Portal creates an invalid .ZIP file.

* When you create presets and assets on AEM author and publish them to Brand Portal and then select dynamic renditions while downloading the assets, you cannot extract the downloaded .ZIP file.

* Issues while downloading video assets from certain folders available on Brand Portal.

* When you share the Contribution folder's URL using an email, Viewer and Editor roles face issues while accessing its parent folder using the breadcrumb.

* Sourcing published report displays an incorrect job start time.
>
 
<!--
* Asset Sourcing email notifications are not delivered for some organizations. 

* Video files with extension `.mov` are not running on Brand Portal. 

* In the **[!UICONTROL Smart Collections]** dropdown list, only ten saved collections are visible. 
-->
<!--
* *_deleted tenants are listed as valid tenant which fails during the execution of TenantCustomizers/TenantUpdates where tenant id is returned as /etc/tenants/`<nodename>`.
-->

<!--
In case only the original assets are downloaded, the asset reflects its own extension and does not open until the extension is manually changed to zip. 
* The user interface of the collection folder does not respond on clicking the navigation arrow. 
* **[!UICONTROL Create]** button is visible in the **[!UICONTROL Column]** view even when the folders are empty.
* **[!UICONTROL Omni search]** fails with a 414 error message (Request-URI Too Long) if the dispatcher is bypassed while accessing the Brand Portal instance.
* An empty zip folder is downloaded if the asset contains a comma (`,`) in the file name.
* The viewer users get the option to add users to the collection they have created. 
* Inconsistent behavior is experienced when an asset (thumbnail or web rendition) is downloaded using share link.

See [what's new in Brand Portal 2021.02.0](whats-new.md).
-->

<!--
### Known Issues {#known-issues}

This release includes the following known issue:

* Search on the **[!UICONTROL Asset Reports]** shows processing on the product interface with no search result.
* The video DM encodes are not visible to the non-admin users on the asset details page.
* The alignment of the size of individual asset renditions and total download size is distorted in the Download dialog.
-->


<!--
* Download Settings configuration to configure asset download from Brand Portal. Fast download, custom renditions, and system renditions are the available configurations. 
-->

<!--
* Document Viewer has been introduced to enhance the PDF viewing experience. New options are available for viewing the PDF files in Brand Portal.

* Advances in the asset download process which improves the Brand Portal user experience while [downloading assets from Brand Portal](brand-portal-download-assets.md). Brand Portal administrators can configure **[!UICONTROL Fast Download]**, **[!UICONTROL Custom Renditions]**, and **[!UICONTROL System Renditions]** from the **[!UICONTROL Download]** settings. 

For details, see [what's new in Brand Portal 6.4.7](whats-new.md). 

### Critical Issues Fixed {#critical-issues-fixed-647}

This release includes fixes to the following critical issues:

* The viewer users are not permitted to share link for collections but the option to share is visible to them on the product interface.

* The **[!UICONTROL Download]** button on the options bar does not list all the licensed assets of the selected folder.

* The search takes longer to show the results for certain keywords.

* The **[!UICONTROL Agree]** and **[!UICONTROL Disagree]** check boxes does not appear on bulk selection of licensed and unlicensed assets during download.

* Filter-based search shows processing on the product interface with no search result. 

* The assets do not download from share link if the shared folder contains numerous and large assets.


### Known Issues {#known-issues-647}

This release includes the following known issues:

* If multiple assets are selected, license text does not appear on clicking Terms and Conditions on the license agreement page during download using share link.   

-->

## Språk {#languages}

Brand Portal användargränssnitt finns på följande språk:

* Engelska
* Tyska
* Franska
* Spanska
* Italienska
* Brasiliansk portugisiska
* Japanska
* Förenklad kinesiska
* Koreanska

## Certifierade plattformar {#certified-platforms}

Om du vill se vilka plattformar som är certifierade för den här Brand Portal-versionen ska du kontrollera kolumnen **Stöd för pekoptimerat användargränssnitt** i avsnittet **Webbläsare som stöds för redigeringsanvändargränssnittet** i [Tekniska krav](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/introduction/technical-requirements) .

## Länkar {#links}

* [Adobe Experience Manager produktsida på adobe.com](https://business.adobe.com/in/products/experience-manager/adobe-experience-manager.html)
* [Assets Brand Portal-dokumentation](https://experienceleague.adobe.com/en/docs/experience-manager-brand-portal/using/home)

## Produktåtkomst och support (begränsade platser) {#product-access-and-support-restricted-sites}

Dessa webbplatser är bara tillgängliga för kunder. Om du är kund och behöver åtkomst kontaktar du din kontoansvarige på Adobe.

<!--
* [https://daycare.day.com](https://daycare.day.com) 
-->

<!--
* [Customer Support]()
-->
