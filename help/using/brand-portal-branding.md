---
title: Anpassa skrivbordsunderlägg, sidhuvud och e-postmeddelanden
seo-title: Customize wallpaper, header, and email message
description: Brand Portal-administratörer kan göra begränsade anpassningar av gränssnittet som visas för användarna. Du kan välja en viss bakgrundsbild (skrivbordsunderlägg) för inloggningssidan för Brand Portal. Du kan också lägga till en huvudbild och anpassa e-postmeddelanden om resursdelning så att de matchar kundens varumärke.
seo-description: Brand Portal administrators can make limited customizations to the interface displayed to users. You can choose a specific background image (wallpaper) for the Brand Portal login page. You can also add a header image and customize asset sharing emails to match the customer’s brand.
uuid: e078d0b9-18b5-467a-ae90-7f0b9fd0d414
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: administration
discoiquuid: 7b573a4f-2d4e-48d6-b259-436d0cfbdce9
role: Admin
exl-id: 9f5c2a6a-8844-4ca4-b0d9-8f50b6164219
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Anpassa skrivbordsunderlägg, sidhuvud och e-postmeddelanden {#customize-wallpaper-header-and-email-message}

Brand Portal-administratörer kan göra begränsade anpassningar av gränssnittet som visas för användarna. Du kan välja en viss bakgrundsbild (skrivbordsunderlägg) för inloggningssidan för Brand Portal. Du kan också lägga till en huvudbild och anpassa e-postmeddelanden om resursdelning så att de matchar kundens varumärke.

## Anpassa skrivbordsunderlägg för inloggningsskärmen {#customize-the-login-screen-wallpaper}

Om det inte finns någon anpassad bakgrundsbild visas ett standardskrivbordsunderlägg på inloggningssidan.

1. Klicka på Experience Manager-logotypen i verktygsfältet överst för att öppna administrationsverktygen.

   ![](assets/aemlogo.png)

1. Klicka på **[!UICONTROL Branding]** på panelen Administrationsverktyg.


   ![](assets/admin-tools-panel-10.png)

1. **[!UICONTROL Wallpaper]** är markerat som standard i den vänstra listen på sidan **[!UICONTROL Configure Branding]**. Standardbakgrundsbilden som visas på inloggningssidan visas.

   ![](assets/default_wallpaper.png)

1. Om du vill lägga till en ny bakgrundsbild klickar du på ikonen **[!UICONTROL Choose Image]** i verktygsfältet högst upp.

   ![](assets/choose_wallpaperimage.png)

   Gör något av följande:

   * Klicka på **[!UICONTROL Upload]** om du vill överföra en bild från datorn. Navigera till önskad bild och överför den.
   * Om du vill använda en befintlig Brand Portal-bild klickar du på **[!UICONTROL Select from existing]**. Välj en bild med resursväljaren.

   ![](assets/asset-picker.png)

1. Ange en rubriktext och beskrivning för bakgrundsbilden. Om du vill spara ändringarna klickar du på **[!UICONTROL Save]** i verktygsfältet högst upp.

1. Klicka på ikonen **[!UICONTROL Preview]** i verktygsfältet högst upp för att generera en förhandsvisning av Brand Portal-gränssnittet med bilden.

   ![](assets/chlimage_1.png)

   ![](assets/custom-wallpaper-preview.png)

1. Gör följande på sidan **[!UICONTROL Configure Branding > Wallpaper]** om du vill aktivera eller inaktivera standardskrivbordsunderlägget:

   * Om du vill visa standardbilden för skrivbordsunderlägg på Brand Portal inloggningssida klickar du på **[!UICONTROL Deactivate Wallpaper]** i verktygsfältet högst upp. Ett meddelande bekräftar att den anpassade bilden är inaktiverad.

   ![](assets/chlimage_1-1.png)

   * Om du vill återställa den anpassade bilden på inloggningssidan för Brand Portal klickar du på **[!UICONTROL Activate Wallpaper]** i verktygsfältet. Ett meddelande bekräftar att bilden har återställts.

   ![](assets/chlimage_1-2.png)

   * Klicka på **[!UICONTROL Save]** om du vill spara ändringarna.

## Anpassa rubriken {#customize-the-header}

Sidhuvudet visas på olika Brand Portal-sidor när du har loggat in på Brand Portal.

1. Klicka på Experience Manager-logotypen i verktygsfältet överst för att öppna administrationsverktygen.

   ![](assets/aemlogo.png)

1. Klicka på **[!UICONTROL Branding]** på panelen Administrationsverktyg.

   ![](assets/admin-tools-panel-11.png)

1. Om du vill anpassa sidhuvudet för Brand Portal-gränssnittet väljer du **[!UICONTROL Header Image]** i den vänstra listen på sidan **[!UICONTROL Configure Branding]**. Standardbilden för sidhuvud visas.

   ![](assets/default-header.png)

1. Om du vill överföra en rubrikbild klickar du på ikonen **[!UICONTROL Choose Image]** och väljer **[!UICONTROL Upload]**.

   Om du vill använda en befintlig Brand Portal-bild väljer du **[!UICONTROL Select from existing]**.

   ![](assets/choose_wallpaperimage-1.png)

   Välj en bild med resursväljaren.

   ![](assets/asset-picker-header.png)

1. Om du vill ta med en URL-adress i rubrikbilden anger du den i rutan **[!UICONTROL Image URL]**. Du kan ange externa eller interna URL-adresser. Interna länkar kan också vara relativa länkar, till exempel
   [!UICONTROL `/mediaportal.html/content/dam/mac/tenant_id/tags`].
Den här länken dirigerar användare till mappen taggar.
Om du vill spara ändringarna klickar du på **[!UICONTROL Save]** i verktygsfältet högst upp.

   ![](assets/configure_brandingheaderimageurl.png)

1. Klicka på ikonen **[!UICONTROL Preview]** i verktygsfältet högst upp för att generera en förhandsvisning av Brand Portal-gränssnittet med rubrikbilden.

   ![](assets/chlimage_1-3.png)
   ![](assets/custom_header_preview.png)

1. Gör följande på sidan **[!UICONTROL Configure Branding > Header Image]** om du vill aktivera eller inaktivera rubrikbilden:

   * Om du vill förhindra att en rubrikbild visas på Brand Portal-sidor klickar du på **[!UICONTROL Deactivate Header]** i verktygsfältet högst upp. Ett meddelande bekräftar att bilden är inaktiverad.

   ![](assets/chlimage_1-4.png)

   * Om du vill att rubrikbilden ska visas igen på Brand Portal-sidor klickar du på **[!UICONTROL Activate Header]** i verktygsfältet högst upp. Ett meddelande bekräftar att bilden är aktiverad.

   ![](assets/chlimage_1-5.png)

   * Klicka på **[!UICONTROL Save]** om du vill spara ändringarna.

## Anpassa e-postmeddelanden {#customize-the-email-messaging}

När resurser delas som en länk får användarna ett e-postmeddelande med länken. Administratörer kan anpassa meddelandena, det vill säga logotyp, beskrivning och sidfot, för dessa e-postmeddelanden.

1. Klicka på Experience Manager-logotypen i verktygsfältet överst för att öppna administrationsverktygen.

   ![](assets/aemlogo.png)

1. Klicka på **[!UICONTROL Branding]** på panelen Administrationsverktyg.

   ![](assets/admin-tools-panel-12.png)

1. När resurser delas som länkar eller hämtas via e-post, och när **[!UICONTROL collections]** delas, skickas e-postmeddelanden till användarna. Om du vill anpassa e-postmeddelandet väljer du **[!UICONTROL Email Message]** från den vänstra listen på sidan **[!UICONTROL Configure Branding]**.

   ![](assets/configure-branding-page-email.png)

1. Om du vill lägga till en logotyp i utgående e-postmeddelanden klickar du på **[!UICONTROL Upload]** i verktygsfältet högst upp.

1. I avsnittet **[!UICONTROL Description]** anger du sidhuvud och sidfot för e-post. Om du vill spara ändringarna klickar du på **[!UICONTROL Save]** i verktygsfältet högst upp.

   >[!NOTE]
   >
   >Om du inte använder den rekommenderade storleken för logotypen, eller om sidhuvuds- och sidfotstexten överskrider det rekommenderade antalet ord, kan innehållet i e-postmeddelandet bli förvrängt.
