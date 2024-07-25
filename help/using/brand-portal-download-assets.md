---
title: Hämta resurser
description: Alla användare kan hämta tillgängliga resurser och mappar samtidigt, vilket säkerställer att godkända varumärkesresurser distribueras säkert för användning offline.
content-type: reference
contentOwner: Vishabh Gupta
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: download, download-install, download assets
exl-id: be264b1c-38d9-4075-b56a-113f34a2c6bf
source-git-commit: f483ac280a5e89ca25305eae09380d70ad661752
workflow-type: tm+mt
source-wordcount: '1823'
ht-degree: 0%

---

# Hämta resurser {#download-assets-from-bp}

Adobe Experience Manager Assets Brand Portal förbättrar nedladdningen genom att man samtidigt kan ladda ned material och mappar från Brand Portal. Den här metoden innebär att godkända varumärkesresurser kan distribueras säkert för användning offline. Läs vidare om du vill veta hur du hämtar resurser (godkända resurser) från Brand Portal och vad du kan förvänta dig av [hämtningsprestanda](#expected-download-performance).


>[!NOTE]
>
>I Brand Portal 2020.10.0 (och senare) är inställningen **[!UICONTROL Fast Download]** aktiverad som standard, vilket innebär att IBM® Aspera Connect används för att hämta resurserna snabbare. Installera IBM® Aspera Connect 3.9.9 (`https://www.ibm.com/docs/en/aspera-connect/3.9.9`) i webbläsartillägget innan du hämtar resurserna från Brand Portal. Se guiden [om du vill snabba upp hämtningar från Brand Portal](../using/accelerated-download.md).
>
>Om du inte vill använda IBM® Aspera Connect och fortsätta med den normala hämtningsprocessen kontaktar du Brand Portal-administratören för att inaktivera inställningen för **[!UICONTROL Fast Download]**.

## Konfigurera hämtning av resurser {#configure-download}

Brand Portal-administratörer kan konfigurera resurshämtning och användargruppinställningar för Brand Portal-användare. Detta gör att användarna kan komma åt och hämta resursrenderingar från Brand Portal gränssnitt.

>[!NOTE]
>
>Nedladdningsinställningarna i användargränssnittet ger en självbetjäning för Brand Portal-användare, så att de enkelt kan konfigurera och hämta resursrenderingar. Det begränsar inte hämtningen av resurser i programlagret, till exempel kan användarna fortfarande komma åt och hämta resursåtergivningar med den fullständiga URL-sökvägen.

Följande konfigurationer definierar hur du får åtkomst till och hämtar resursåtergivningarna från Brand Portal-gränssnittet:

* Aktivera hämtningsinställningar
* Konfigurera inställningar för användargrupp

### Aktivera hämtningsinställningar {#enable-download-settings}

Administratörerna kan aktivera **[!UICONTROL Download Settings]** för att definiera uppsättningen renderingar som är tillgängliga för Brand Portal-användare för hämtning.

De tillgängliga inställningarna är:

* **[!UICONTROL Fast Download]**

  Den snabbar upp nedladdningen av materialet med IBM® Aspera Connect. Inställningen **[!UICONTROL Fast Download]** är som standard aktiverad i **[!UICONTROL Download Settings]**.

* **[!UICONTROL Custom Renditions]**

  Aktiverar hämtning av anpassade och (eller) dynamiska återgivningar av resurserna.

  Alla resursåtergivningar som inte är den ursprungliga resursen och systemgenererade återgivningar kallas anpassade återgivningar. Den innehåller både statiska och dynamiska renderingar som är tillgängliga för resursen. Alla användare kan skapa en anpassad statisk återgivning i Experience Manager Assets, medan bara administratören kan skapa anpassade dynamiska återgivningar. Se [Använda bildförinställningar eller dynamiska återgivningar](../using/brand-portal-image-presets.md).

* **[!UICONTROL System Renditions]**

  Aktiverar hämtning av systemgenererade återgivningar av resurserna.

  Dessa resurser är miniatyrbilder som genereras automatiskt i Experience Manager Assets baserat på arbetsflödet&quot;DAM-uppdateringsresurs&quot;.

* **[!UICONTROL Asset Download]**

  Återgivningar hämtas i separata mappar för varje resurs. Den här inställningen gäller för mappar, samlingar och massnedladdningar av mer än 20 resurser.


Logga in på din Brand Portal-klient som administratör och gå till **[!UICONTROL Tools]** > **[!UICONTROL Download]**.

Administratörerna kan aktivera valfri kombination av inställningar som Brand Portal-användare kan använda för att komma åt och hämta resursrenderingar.

![](assets/download-settings-new.png)


>[!NOTE]
>
>Endast administratörer kan hämta utgångna resurser. Mer information om utgångna resurser finns i [Hantera digitala rättigheter för resurser](../using/manage-digital-rights-of-assets.md).

### Konfigurera inställningar för användargrupp {#configure-user-group-settings}

Förutom **[!UICONTROL Download Settings]** kan Brand Portal-administratörer ytterligare konfigurera inställningar för olika användargrupper så att de kan visa och (eller) hämta originalresurserna och deras återgivningar.

Logga in på din Brand Portal-klient som administratör och gå till **[!UICONTROL Tools]** > **[!UICONTROL Users]**. Gå till fliken **[!UICONTROL Groups]** på sidan **[!UICONTROL User Roles]** för att konfigurera inställningar för visning och (eller) hämtning för användargrupperna.

![view-download-permission](assets/download-permissions.png)

>[!NOTE]
>
>Om en användare läggs till i flera grupper och om en av grupperna har begränsningar, gäller begränsningarna användaren.

Beroende på konfigurationen förblir hämtningsarbetsflödet konstant för fristående resurser, flera resurser, mappar som innehåller resurser, licensierade eller olicensierade resurser och hämtning av resurser via delningslänken.

I följande matris definieras om en användare har åtkomst till återgivningarna beroende på [hämtningskonfigurationerna](#configure-download):

| **Hämtningsinställningar: Anpassade återgivningar** | **Hämtningsinställningar: Systemåtergivningar** | **Inställningar för användargrupp: Hämta original** | **Användargruppsinställningar: Hämta återgivningar** | **Resultat** |
|---|---|---|---|---|
| PÅ | PÅ | PÅ | PÅ | Visa och hämta alla återgivningar |
| PÅ | PÅ | AV | AV | Visa ursprunglig resurs |
| AV | AV | PÅ | PÅ | Visa och hämta originalresursen |
| PÅ | AV | PÅ | PÅ | Visa och hämta ursprungliga resurser och anpassade återgivningar |
| AV | PÅ | PÅ | PÅ | Visa och hämta ursprungliga resurs- och systemåtergivningar |
| PÅ | AV | AV | AV | Visa ursprunglig resurs |
| AV | PÅ | AV | AV | Visa ursprunglig resurs |
| AV | AV | AV | PÅ | Visa ursprunglig resurs |
| AV | AV | PÅ | AV | Visa och hämta originalresursen |
| AV | AV | AV | AV | Visa ursprunglig resurs |



## Hämta resurser {#download-assets}

Brand Portal-användare kan hämta flera resurser, mappar med resurser och samlingar från Brand Portal gränssnitt.

>[!NOTE]
>
>Kontakta Brand Portal-administratören om du inte har behörighet att komma åt eller hämta resursåtergivningarna.

Om användaren har åtkomst till återgivningar får användaren den förbättrade dialogrutan **[!UICONTROL Download]** med följande funktioner:

* Visa alla tillgängliga återgivningar av alla resurser i hämtningslistan.
* Undanta återgivningar av resurser som inte krävs för hämtning.
* Använd samma uppsättning renderingar för alla liknande resurstyper med ett klick.
* Använd olika uppsättningar återgivningar för olika resurstyper.
* Skapa en separat mapp för varje resurs.
* Hämta markerade resurser och deras återgivningar.

![download-dialog](assets/download-dialog-box.png)

>[!NOTE]
>
>Dialogrutan **[!UICONTROL Download]** visas bara om **[!UICONTROL Custom Renditions]** och (eller) **[!UICONTROL System Renditions]** är aktiverat i **[!UICONTROL Download Settings]**.


### Steg för att hämta resurser {#bulk-download}

Så här hämtar du resurser eller mappar som innehåller resurser från Brand Portal-gränssnittet:

1. Logga in på din Brand Portal-klient. Som standard öppnas vyn **[!UICONTROL Files]** som innehåller alla publicerade resurser och mappar.

   Gör något av följande:

   * Markera de resurser eller mappar som du vill hämta. Klicka på ikonen **[!UICONTROL Download]** i verktygsfältet högst upp.

     ![select-multiple-assets](assets/select-assets-new.png)

   * Om du vill hämta särskilda återgivningar av en resurs håller du pekaren över resursen och klickar på ikonen **[!UICONTROL Download]** som finns i miniatyrbilderna för snabbåtgärden.

     ![select-asset](assets/select-asset.png)


     >[!NOTE]
     >
     >Om du hämtar resurserna för första gången och inte har IBM® Aspera Connect installerat i webbläsaren uppmanas du att installera Aspera Download Accelerator (`https://www.ibm.com/docs/en/aspera-connect/3.9.9`).


     >[!NOTE]
     >
     >Om de hämtade resurserna även innehåller licensierade resurser omdirigeras du till sidan **[!UICONTROL Copyright Management]**. På den här sidan markerar du resurserna, klickar på **[!UICONTROL Agree]** och sedan på **[!UICONTROL Download]**. Om du inte håller med hämtas inte licensierade mediefiler.
     > 
     >Licensskyddade resurser har ett [licensavtal kopplat](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/drm) till sig, vilket görs genom att resursens [metadataegenskap ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/drm) ställs in i Experience Manager Assets.


     ![licensed-asset](assets/licensed-asset-new.png)

1. Dialogrutan **[!UICONTROL Download]** där alla markerade resurser visas.

   Klicka på en resurs för att visa tillgängliga återgivningar och markera kryssrutorna för de återgivningar som du vill hämta.

   Du kan välja eller exkludera återgivningar manuellt för enskilda resurser eller klicka på ikonen **Använd** för att välja samma uppsättning återgivningar som ska hämtas för liknande resurstyper (alla bildfiler i det här exemplet). I dialogrutan **[!UICONTROL Apply All]** klickar du på **[!UICONTROL Done]** för att tillämpa regeln på alla liknande resurser.

   ![apply-all](assets/apply.png)

   Du kan också ta bort en resurs från hämtningslistan (om det behövs) genom att klicka på ikonen **Ta bort** .

   ![ta bort](assets/remove.png)

   Markera kryssrutan **[!UICONTROL `Create separate folder for each asset`]** om du vill behålla mappstrukturen för Brand Portal när du hämtar resurser.

   Nedladdningsknappen visar antalet markerade objekt. När du är klar med att tillämpa reglerna klickar du på **[!UICONTROL Download items]**.

   ![download-dialog](assets/download-dialog-box-new.png)

1. Som standard är inställningen **[!UICONTROL Fast Download]** aktiverad i **[!UICONTROL Download Settings]**. Därför visas en bekräftelseruta som tillåter snabb hämtning med IBM® Aspera Connect.

   Klicka på **[!UICONTROL Allow]** om du vill fortsätta använda **[!UICONTROL Fast Download]**. Alla valda återgivningar hämtas i en zip-mapp med IBM® Aspera Connect.

   Om du inte vill använda IBM® Aspera Connect klickar du på **[!UICONTROL Deny]**. Om **[!UICONTROL Fast Download]** nekas eller misslyckas fyller systemet i ett felmeddelande. Klicka på knappen **[!UICONTROL Normal Download]** om du vill fortsätta hämta resurserna.

<!-- removed the known issue from step 2 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issue will be fixed in the upcoming release:
   >
   >The download dialog lists the smart crop renditions of the selected asset, however, the user cannot download the smart crop renditions.
-->

>[!NOTE]
>
>Om inställningen **[!UICONTROL Fast Download]** är inaktiverad av administratören hämtas de valda återgivningarna direkt till en ZIP-mapp utan att IBM® Aspera Connect används.

>[!NOTE]
>
>Om inställningen **[!UICONTROL Asset Download]** är aktiverad i **[!UICONTROL Download Settings]** hämtas resursåtergivningarna i en separat mapp för varje resurs i zip-mappen.
>  
>Om resurserna hämtas från en delad länk hämtas resursåtergivningarna i en separat mapp för varje resurs i zip-mappen.
>
>När du väljer en mapp, en samling eller fler än 20 resurser att hämta, ignoreras dialogrutan **[!UICONTROL Download]**. I stället hämtas alla tillgängliga resursåtergivningar, förutom dynamiska återgivningar, i en ZIP-mapp.

>[!NOTE]
>
>Brand Portal stöder konfigurering av Dynamic Media i både läget Hybrid och Scene7.
>
>(*Om Experience Manager Assets-författarinstansen körs i **Dynamic Media-hybridläge***)
>
>Aktivera dynamiska medier om du vill förhandsgranska eller hämta dynamiska återgivningar. Kontrollera att resursens Pyramid-återgivning finns i den Experience Manager Assets-författarinstans där resurserna publicerades. När en resurs publiceras från Experience Manager Assets till Brand Portal publiceras även dess Pyramid-återgivning.

Om [administratören inte har gett dig behörighet att komma åt de ursprungliga återgivningarna](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) kan du inte hämta de ursprungliga återgivningarna för de valda resurserna.

![no-access-message](assets/no-access-message.png)

<!-- This issue has been resolved, check with engineering.
>[!NOTE]
>
>Once you have downloaded the asset renditions, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.
-->

### Hämta resurser från sidan med resursinformation {#download-assets-from-asset-details-page}

Förutom hämtningsarbetsflödet finns det en annan metod för att hämta återgivningar för enskilda resurser direkt från sidan med resursinformation.

Användarna kan förhandsgranska olika resursåtergivningar, välja specifika återgivningar och direkt hämta resursåtergivningar från panelen **[!UICONTROL Renditions]** på sidan med resursinformation utan att behöva öppna dialogrutan **[!UICONTROL Download]**.


Så här hämtar du resursåtergivningar från sidan med resursinformation:

1. Logga in på din Brand Portal-klient och klicka på resursen för att öppna sidan med resursinformation.
1. Klicka på övertäckningsikonen till vänster och klicka sedan på **[!UICONTROL Renditions]**.

   ![återgivningsnavigering](assets/rendition-navigation.png)

1. På panelen **[!UICONTROL Renditions]** visas alla tillgängliga resursåtergivningar baserat på resursens [hämtningskonfigurationer](#configure-download).

   Markera de renderingar som du vill hämta och klicka på **[!UICONTROL Download items]**.

   ![renditions-panel](assets/renditions-panel.png)


1. Som standard är inställningen **[!UICONTROL Fast Download]** aktiverad i **[!UICONTROL Download Settings]**. Därför visas en bekräftelseruta som tillåter snabb hämtning med IBM® Aspera Connect.

   Klicka på **[!UICONTROL Allow]** om du vill fortsätta använda **[!UICONTROL Fast Download]**. Alla valda återgivningar hämtas i en zip-mapp med IBM® Aspera Connect.

   Om du nekar med hjälp av **[!UICONTROL Fast Download]** fyller systemet i ett felmeddelande. Klicka på knappen **[!UICONTROL Normal Download]** om du vill fortsätta hämta resurserna.

<!-- removed the known issue from step 3 as it is fixed in 2022.02.0 release.
   >[!CAUTION]
   >
   >(**Experience Manager Assets as a Cloud Service** only) The following known issues will be fixed in the upcoming release:
   >
   >The **[!UICONTROL Renditions]** panel does not list all the static renditions of the assets that are published to Brand Portal after December 16, 2021.
   >
   >The **[!UICONTROL Renditions]** panel lists the smart crop renditions of the asset, however, the user cannot preview or download the smart crop renditions.
-->

>[!NOTE]
>
>Om inställningen **[!UICONTROL Fast Download]** är inaktiverad av administratören hämtas de valda återgivningarna direkt till en ZIP-mapp utan att IBM® Aspera Connect används.


>[!NOTE]
>
>Assets som laddas ned separat visas i resurshämtningsrapporten. Om en mapp som innehåller resurser däremot hämtas visas inte mappen och resurserna i hämtningsrapporten för resurser.

<!--
>[!NOTE]
>
>Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

<!-- Backup of content before updating the new feature docs.
## Configure asset download {#configure-download}

The download configuration allows the Brand Portal administrators to define the set of renditions available to the Brand Portal users for downloading the assets. The administrator can configure the asset **[!UICONTROL Download]** settings from the Brand Portal interface. 

The available configurations are:

* **[!UICONTROL Fast Download]** 

  Enables high-speed download of the assets. To know more, see [guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).

* **[!UICONTROL Custom Renditions]** 
  
  Download custom and (or) dynamic renditions of the assets. 
  All the asset renditions other than the original asset and system-generated renditions are called as custom renditions. It includes static as well as dynamic renditions available for the asset. Any user can create a custom static rendition in AEM Assets, whereas, only the AEM administrator can create custom dynamic renditions. To know more, see [how to apply image presets or dynamic renditions](../using/brand-portal-image-presets.md)

* **[!UICONTROL System Renditions]** 

  Download system-generated renditions of the assets. These are the thumbnails which are automatically generated in AEM Assets based on the "DAM update asset" workflow. 

Log in to your Brand Portal tenant as an administrator and navigate to **[!UICONTROL Tools]** > **[!UICONTROL Download]**. By default, the **[!UICONTROL Fast Download]** configuration is enabled in the **[!UICONTROL Download Settings]**. 

The administrators can enable any combination to configure the asset download process.

![](assets/download-configuration.png)


Based on the configuration, the download workflow remains constant for stand-alone assets, multiple assets, folders containing assets, licensed or unlicensed assets, and downloading assets using share link. 


* If both **[!UICONTROL Custom Renditions]** and **[!UICONTROL System Renditions]** configurations are turned-off, the original renditions of the assets are downloaded without any additional dialog being presented to the users.    


* If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled, an additional **[!UICONTROL Download]** dialog box appears wherein you can choose whether to download the original asset along with its renditions, or download only specific renditions. 

>[!NOTE]
>
>Only the administrators can download the expired assets. For more information about expired assets, see [manage digital rights of assets](../using/manage-digital-rights-of-assets.md).

## Steps to download assets {#steps-to-download-assets}

Following are the steps to download assets or folders containing assets from Brand Portal:

1. From the Brand Portal interface, do one of the following:

   * Select the folders or assets you want to download. From the toolbar at the top, click the **[!UICONTROL Download]** icon.

     ![](assets/downloadassets-1.png)

   * To download a specific asset or folder, hover the pointer over the asset or folder and click the **[!UICONTROL Download]** icon available in the quick action thumbnails.

     ![](assets/downloadsingleasset-1.png)


     >[!NOTE]
     >
     >If you are downloading the assets for the first time and do not have IBM Aspera Connect installed in your browser, it will prompt you to install the Aspera download accelerator. 


     >[!NOTE]
     >
     >If the assets you are downloading also include licensed assets, you are redirected to the **[!UICONTROL Copyright Management]** page. In this page, select the assets, click **[!UICONTROL Agree]**, and then click **[!UICONTROL Download]**. If you choose to disagree, licensed assets are not downloaded. 
     > 
     >License-protected assets have [license agreement attached]() to them, which is done by setting asset's [metadata property]() in Experience Manager Assets.


     ![](assets/licensed-asset-download-1.png)

     
     >[!NOTE]
     >
     >Ensure to select all the required asset renditions while downloading them from the asset details page, and click **[!UICONTROL Download]**. The selected renditions are downloaded to your local machine.
     > 
     >Once you download, the **[!UICONTROL Download]** button is disabled to avoid creating duplicate copies of the downloaded renditions. To download more (missing or another copy of renditions), refresh the browser to re-enable the download button.

     If any of the **[!UICONTROL Custom Renditions]** or **[!UICONTROL System Renditions]** configuration is enabled in the **[!UICONTROL Download Settings]**, the **[!UICONTROL Download]** dialog appears with the **[!UICONTROL Asset(s)]** check box selected by default. If the **[!UICONTROL Fast Download]** configuration is enabled, the **[!UICONTROL Enable download acceleration]** check box is selected by default.

     ![](assets/download-dialog.png)

     >[!NOTE]
     >
     >If the downloading assets are image files, and you select only the **[!UICONTROL Asset(s)]** check box in the **[!UICONTROL Download]** dialog but are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708) then no image files are downloaded and a notification appears, stating that you have been restricted by the administrator to access original renditions.

     ![](assets/restrictaccess-note.png)

1. To download the renditions in addition to the original assets, select the **[!UICONTROL Rendition(s)]** check box. However, if you want to download the system-generated renditions along with the custom renditions, clear the **[!UICONTROL Exclude System Renditions]** check box.

   ![](assets/download-system-rendition.png)

   * To download only the renditions, clear the **[!UICONTROL Asset(s)]** check box.

     >[!NOTE]
     >
     >By default, only the assets are downloaded. However, original renditions of image files are not downloaded if you are not [authorized by the administrator to have access to the original renditions of image files](../using/brand-portal-adding-users.md#main-pars-procedure-202029708).

    * To share the selected assets with other users through a link, select the **[!UICONTROL Email]** check box. An email notification is sent to the users with the download link. To know how to download assets from shared links, see [downloading assets from shared links](../using/brand-portal-link-share.md#main-pars-header-1703469193).  

      ![](assets/download-link.png)

      >[!NOTE]
      >
      >The download link on email notification expires after 45 days.
      >
      >The administrators can customize email messages, that is, logo, description, and footer, using the [Branding](../using/brand-portal-branding.md) feature.


    * You can select a predefined image preset or create a custom dynamic rendition from the **[!UICONTROL Download]** dialog box. 

      To apply a [custom image preset to the asset and its renditions](../using/brand-portal-image-presets.md#applyimagepresetswhendownloadingimages), select the **[!UICONTROL Dynamic Rendition(s)]** check box. Specify the image preset properties (such as size, format, color space, resolution, and image modifier) to apply the custom image preset while downloading the asset and its renditions. To download only the dynamic renditions, clear the **[!UICONTROL Asset(s)]** check box.

      ![](assets/dynamic-rendition.png)

      >[!NOTE]
      >
      >Brand Portal supports configuring Dynamic Media in both - Hybird and Scene 7 mode. 
      >
      >(*If AEM author instance is running on **Dynamic Media Hybrid mode***)
      >
      >To preview or download dynamic renditions of an asset, ensure that the dynamic media is enabled and the asset's Pyramid tiff rendition exists at the AEM Assets author instance from where the assets have been published. When an asset is published to Brand Portal, its Pyramid tiff rendition is also published.
      
  
    * To preserve the Brand Portal folder hierarchy while downloading assets, select the **[!UICONTROL Create separate folder for each asset]** check box. By default, the Brand Portal folder hierarchy is ignored and all the assets are downloaded in one folder in your local system.

1. Click **[!UICONTROL Download]**.

   The assets (and renditions if selected) are downloaded as a zip file to your local folder. However, no zip file is created if a single asset is downloaded without any of the renditions. 

   If you are not [authorized by the administrator to have access to the original renditions](../using/brand-portal-adding-users.md#main-pars-procedure-202029708), the original renditions of the selected assets are not downloaded. 

   >[!NOTE]
   >
   >Assets that are individually downloaded are visible in the assets download report. However, if a folder containing assets is downloaded, the folder and assets are not displayed in the assets download report.
-->

## Förväntade hämtningsprestanda {#expected-download-performance}

Filhämtningen kan variera för användare på olika platser på klienten, beroende på faktorer som lokal Internetanslutning och serverfördröjning. Den förväntade hämtningsprestandan för 2-GB-filer som observeras på olika klientplatser är följande, med Brand Portal server på Oregon i USA:

| Klientplats | Latens mellan klient och server | Förväntad hämtningshastighet | Tidsåtgång för att hämta en 2 GB-fil |
|-------------------------|-----------------------------------|-------------------------|------------------------------------|
| Västra USA (N. Kalifornien) | 18 millisekunder | 7,68 MB/s | 4 minuter |
| Västra USA (Oregon) | 42 millisekunder | 3,84 MB/s | 9 minuter |
| Östra USA (N. Virginia) | 85 millisekunder | 1,61 MB/s | 21 minuter |
| APAC (Tokyo) | 124 millisekunder | 1,13 MB/s | 30 minuter |
| Noida | 275 millisekunder | 0,5 MB/s | 68 minuter |
| Sydney | 175 millisekunder | 0,49 MB/s | 69 minuter |
| London | 179 millisekunder | 0,32 MB/s | 106 minuter |
| Singapore | 196 millisekunder | 0,5 MB/s | 68 minuter |


>[!NOTE]
>
>Citerade data observeras under testförhållanden, som kan variera för användare på olika platser där olika fördröjningar och bandbredd kan förekomma.
