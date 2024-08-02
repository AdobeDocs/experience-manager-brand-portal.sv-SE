---
title: Dela resurser som en länk
description: Läs om hur Adobe Experience Manager Assets Brand Portal-administratörer kan dela länkar mellan olika resurser med auktoriserade interna användare och externa enheter, inklusive partners och leverantörer. Redigerare kan bara visa och dela resurser som delas med dem.
contentOwner: bdhar
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: f3573219-3c58-47ba-90db-62b003d8b9aa
exl-id: 9d254e95-a4fc-468d-ae1f-9690ddd3b4a1
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# Dela resurser som en länk {#share-assets-as-a-link}

Adobe Experience Manager Assets Brand Portal-administratörer kan dela länkar mellan olika resurser med auktoriserade interna användare och externa enheter, inklusive partners och leverantörer. Redigerare kan bara visa och dela resurser som delas med dem.

Att dela resurser via en länk är ett bekvämt sätt att göra dem tillgängliga för externa parter eftersom mottagarna inte behöver logga in på Brand Portal för att få tillgång till resurserna.

<!-- Link sharing access is restricted to editors and administrators. 
-->

Mer information finns i [Hantera användare, grupper och användarroller](../using/brand-portal-adding-users.md#manage-user-roles).


Så här delar du resurser som en länk:

1. Logga in på din Brand Portal-klient. Som standard öppnas vyn **[!UICONTROL Files]** som innehåller alla publicerade resurser och mappar.

1. Välj de resurser eller mappar som ska delas, eller navigera till vyn **[!UICONTROL Collections]** om du vill dela de samlingar du har skapat.

   ![select-multiple-assets](assets/select-assets-new.png)

1. Klicka på ikonen **[!UICONTROL Share Link]** i verktygsfältet högst upp.

   Dialogrutan **[!UICONTROL Link Sharing]** visas.

   ![](assets/link-sharing.png)

   * I rutan E-postadress skriver du e-post-ID för den användare som du vill dela länken med. Du kan dela länken med flera användare. Om användaren är medlem i din organisation väljer du användarens e-post-ID bland förslagen som visas i listrutan. Om användaren är extern skriver du det fullständiga e-post-ID:t och trycker på **[!UICONTROL Enter]**. E-post-ID:t läggs till i listan över användare.

     ![](assets/link-sharing-text.png)

   * I rutan **[!UICONTROL Subject]** anger du ett ämne för resursen som du vill dela.
   * Skriv ett meddelande i rutan **[!UICONTROL Message]** om det behövs.
   * I fältet **[!UICONTROL Expiration]** använder du datumväljaren för att ange ett förfallodatum och en förfallotid för länken. Som standard är förfallodatumet 7 dagar från det datum då du delar länken.
   * Aktivera kryssrutan **[!UICONTROL Allow download of the original file]** om du vill tillåta mottagarna att hämta den ursprungliga återgivningen.

   Resurserna som delas via länken går ut när det datum och den tid som anges i fältet **[!UICONTROL Expiration]** har passerats. Mer information om förfallna tillgångsbeteenden och rollbaserade aktivitetsändringar i Brand Portal finns i [Hantera digitala rättigheter för resurser](../using/manage-digital-rights-of-assets.md#asset-expiration).

   >[!NOTE]
   >
   >Länkens standardförfallotid är 7 dagar. Länken måste skickas med e-post till användarna med dialogrutan **[!UICONTROL Link Sharing]**. Kopiera inte länken och dela den inte separat.

1. Klicka på **[!UICONTROL Share]**. Ett meddelande bekräftar att länken delas med användarna. Användarna får ett e-postmeddelande med den delade länken.

   ![](assets/link-share-email.png)

   >[!NOTE]
   >
   >Administratörer kan anpassa e-postmeddelanden, som bland annat anpassar logotyp, beskrivning och sidfot med funktionen [Varumärkning](../using/brand-portal-branding.md) .

## Hämta resurser från delade länkar {#download-assets-from-shared-links}

Klicka på länken i e-postmeddelandet för att komma åt den delade resursen. Sidan AEM länkdelning öppnas.

Så här hämtar du de delade resurserna:

1. Klicka på resurserna eller mapparna och klicka sedan på ikonen **[!UICONTROL Download]** i verktygsfältet.

   ![](assets/download-share-link.png)

   >[!NOTE]
   >
   >För närvarande kan du bara generera en förhandsvisning och en miniatyrbild för vissa resurser, beroende på filformatet. Mer information om vilka filformat som stöds finns i [Stöd för förhandsgranskning och miniatyrbilder för resursformat](#preview-thumbnail-support).

1. Dialogrutan **[!UICONTROL Download]** visas.

   ![download-dialog](assets/download-dialog-box-new.png)

1. Som standard är inställningen **[!UICONTROL Fast Download]** aktiverad i **[!UICONTROL Download Settings]**. Därför visas en bekräftelseruta som gör att nedladdningen med IBM® Aspera Connect kan fortsätta.

   Klicka på **[!UICONTROL Allow]** om du vill fortsätta använda **[!UICONTROL Fast Download]**.

   Alla valda återgivningar hämtas i en ZIP-mapp som innehåller en separat mapp för varje resurs.

   >[!NOTE]
   >
   >En separat mapp skapas för varje resurs när resurserna hämtas från en delad länk.
   >
   >Om en mapp, en samling eller fler än 20 resurser har valts hoppas dialogrutan **[!UICONTROL Download]** över. Dessutom hämtas alla tillgängliga resursåtergivningar (utom dynamiska) i en zip-mapp med separata mappar för varje resurs.

   >[!NOTE]
   >
   >Om administratören inte har auktoriserat den användare som delade resurserna hämtas inte de ursprungliga återgivningarna via den delade länken. Se även [auktoriserad av administratören att ha åtkomst till de ursprungliga återgivningarna](../using/brand-portal-adding-users.md#manage-group-roles-and-privileges).


>[!NOTE]
>
>Brand Portal begränsar nedladdningen av mappar eller resurser som är större än 5 GB med hjälp av länkdelning.

<!--
1. The **[!UICONTROL Download]** dialog box appears.

   ![](assets/download-linkshare.png)

    * To speed up the download of asset files shared as the link, select **[!UICONTROL Enable download acceleration]** option and [follow the wizard](../using/accelerated-download.md#download-workflow-using-file-accelerator). To know more about the fast download of assets on Brand Portal refer [Guide to accelerate downloads from Brand Portal](../using/accelerated-download.md).
    
1. To download the renditions of assets in addition to the assets from the shared link, select **[!UICONTROL Rendition(s)]** option. When you do so, **[!UICONTROL Exclude System Renditions]** option appears that is selected by default. This prevents the download of out-of-the-box renditions along with approved assets or their custom renditions.

   However, to allow auto-generated renditions to download along with custom renditions, deselect the **[!UICONTROL Exclude System Renditions]** option.

   >[!NOTE]
   >
   >Original renditions are not downloaded using the shared link if the user who shared the assets as a link is not [authorized by the administrator to have access to the original renditions](../using/brand-portal-adding-users.md#manage-group-roles-and-privileges).

   ![](assets/download-linkshare-autoren.png)

1. Click **[!UICONTROL Download]**. The assets (and renditions if selected) are downloaded as a ZIP file to your local folder. However, no zip file is created if a single asset is downloaded without any of the renditions, thereby ensuring speedy download.

-->

## Stöd för förhandsgranskning och miniatyrbilder för resursformat {#preview-thumbnail-support}

I följande matris visas de resursformat som Brand Portal stöder miniatyrbilder och förhandsvisning för:

| Resursformat | Stöd för miniatyrbilder | Stöd för förhandsgranskning |
|--------------|-------------------|-----------------|
| PNG | ✓ | ✓ |
| GIF | ✓ | ✓ |
| TIFF | ✓ | ✕ |
| JPEG | ✓ | ✓ |
| BMP | ✓ | ✕ |
| PNM* | NA | NA |
| PGM* | NA | NA |
| PBM* | NA | NA |
| PPM* | NA | NA |
| PSD | ✓ | ✕ |
| EPS | NA | ✕ |
| DNG | ✓ | ✕ |
| PICT | ✓ | ✕ |
| PSB* | ✓ | ✕ |
| JPG | ✓ | ✓ |
| AI | ✓ | ✕ |
| DOC | ✕ | ✕ |
| DOCX | ✕ | ✕ |
| ODT* | ✕ | ✕ |
| PDF | ✓ | ✕ |
| HTML | ✕ | ✕ |
| RTF | ✕ | ✕ |
| TXT | ✓ | ✕ |
| XLS | ✕ | ✕ |
| XSX | ✕ | ✕ |
| ODS | ✕ | ✕ |
| PPT | ✓ | ✕ |
| PPTX | ✕ | ✕ |
| ODP | ✕ | ✕ |
| INDD | ✓ | ✕ |
| PS | ✕ | ✕ |
| QXP | ✕ | ✕ |
| EPUB | ✓ | ✕ |
| AAC | ✕ | ✕ |
| MIDI | ✕ | ✕ |
| 3GP | ✕ | ✕ |
| MP3 | ✕ | ✕ |
| MP4 | ✕ | ✕ |
| OGA | ✕ | ✕ |
| OGG | ✕ | ✕ |
| RA | ✕ | ✕ |
| WAV | ✕ | ✕ |
| WMA | ✕ | ✕ |
| DVI | ✕ | ✕ |
| FLV | ✕ | ✕ |
| M4V | ✕ | ✕ |
| MPG | ✕ | ✕ |
| OGV | ✕ | ✕ |
| MOV | ✕ | ✕ |
| WMV | ✕ | ✕ |
| SWF | ✕ | ✕ |
| TGZ | NA | ✕ |
| JAR | ✓ | ✕ |
| RAR | NA | ✕ |
| TAR | NA | ✕ |
| ZIP | ✓ | ✕ |

I följande förklaring förklaras symbolerna som används i matrisen:

| Symbol | Betydelse |
|---|---|
| ✓ | Det här filformatet stöder den här funktionen |
| ✕ | Det här filformatet stöder inte den här funktionen |
| NA | Den här funktionen gäller inte för det här filformatet |
| &#42; | Den här funktionen kräver tilläggsstöd för det här filformatet AEM författarinstansen men inte på Brand Portal efter att resurserna har publicerats i Brand Portal |

## Dela inte resurser som delas som en länk {#unshare-assets-shared-as-a-link}

Så här tar du bort delning av tidigare delade resurser som en länk:

1. När du loggar in på Brand Portal öppnas vyn **[!UICONTROL File]** som standard. Om du vill visa de resurser du har delat som länkar går du till vyn **[!UICONTROL Shared Links]**.

1. Granska de länkar som du har delat i den lista som visas.

   ![](assets/shared-links.png)

1. Om du vill ta bort delningen av en länk från listan markerar du den och klickar på ikonen **[!UICONTROL Unshare]** i verktygsfältet högst upp.

   ![](assets/unshare-asset.png)

   >[!NOTE]
   >
   >Visningen av delade länkar är användarspecifik. Den här funktionen visar inte alla länkar som delas av alla användare av en klientorganisation.

1. Klicka på **[!UICONTROL Continue]** i varningsmeddelanderutan för att bekräfta att du inte vill dela. Posten för länken tas bort från listan med delade länkar.
