---
title: Administrera allmänna klientkonfigurationer
description: Konfigurera hämtningsacceleration, offentliga smarta samlingar, skapande av offentliga samlingar och gör det möjligt för administratörsanvändare att ta bort resurser på klientorganisationer.
contentOwner: mgulati
topic-tags: administration
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 5607be8e-0a7f-4692-b71b-5f66eb9ac5ee
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Administrera allmänna klientkonfigurationer {#administer-general-tenant-configurations}

Med Experience Manager Assets Brand Portal kan organisationer konfigurera följande funktioner för specifika innehavare:

* Borttagning av resurser av administratörer
* Skapande av offentlig samling av icke-adminanvändare
* Skapande av offentlig smart samling av icke-adminanvändare
* Den överordnade hierarkin för delade mappar är synlig för användare som inte är administratörer

Dessa konfigurationer har tillhandahållits som **[!UICONTROL General Settings]** konfigurationer på panelen Administrationsverktyg.

![](assets/general-config.png)

**A** - Konfiguration som gör att administratörer kan ta bort resurser från Brand Portal. (Standard är aktiverat)

**B** - Konfiguration för att låta icke-adminanvändare skapa offentliga samlingar. (Standard är aktiverat)

**C** - Konfiguration för att låta icke-adminanvändare skapa publika smarta samlingar. (Standard är aktiverat)

**D** - Konfiguration för att visa mapphierarkin (från roten) för delade mappar till icke-adminanvändare (redigerare, visningsprogram, gästanvändare). (Standard är inaktiverat)

## Aktivera eller inaktivera allmänna konfigurationer {#enable-disable-general-configurations}

Så här aktiverar eller inaktiverar du dessa konfigurationer:

1. Logga in med administratörsbehörighet.
1. Om du vill öppna administrationsverktygen i verktygsfältet högst upp väljer du Experience Manager-logotypen.
1. Öppna sidan **[!UICONTROL General Settings]** genom att välja **[!UICONTROL General]** på panelen Administrationsverktyg.
1. Använd respektive växlingsknapp för att aktivera eller inaktivera någon av de allmänna konfigurationerna.
1. **[!UICONTROL Save]** ändringarna.
1. Logga ut så att ändringarna kan börja gälla.

## Tillåt administratörsanvändare att ta bort resurser från Brand Portal {#allow-admin-users-to-delete-assets-from-brand-portal}

Med konfigurationen **[!UICONTROL Allow users to delete]** kan organisationer tillåta (eller begränsa) användare med administratörsbehörighet att ta bort resurser och mappar från Brand Portal.

## Tillåt att offentliga samlingar skapas av icke-administratörer {#allow-public-collections-creation-by-non-admins}

[[!UICONTROL Allow public collections creation]](../using/brand-portal-share-collection.md#main-pars-text-1915052376)-konfigurationen kontrollerar om icke-administratörer kan skapa offentliga samlingar på Brand Portal. Konfigurationen är aktiverad som standard. Genom att inaktivera konfigurationen kan organisationer förhindra att det finns många offentliga samlingar på portalen så att systemutrymmet kan sparas.

## Tillåt att icke-administratörer skapar offentliga smarta samlingar {#allow-public-smart-collections-creation-by-non-admins}

Konfigurationen för [[!UICONTROL Allow public smart collections creation]](../using/brand-portal-searching.md#main-pars-header-500620467) styr om icke-administratörer kan spara sina sökningar som smarta samlingar och göra dem offentliga för den klienten. Konfigurationen är aktiverad som standard. Genom att inaktivera konfigurationen kan organisationer förhindra att det finns ett stort antal publika smarta samlingar som skapats av icke-adminanvändare i organisationens Brand Portal.

<!-- 
## Allow download acceleration {#allow-download-acceleration}

[[!UICONTROL Allow download acceleration]](../using/accelerated-download.md) configuration lets the organizations to allow accelerated downloads of assets from Brand Portal and shared links, by integrating with IBM Aspera Connect that is an install-on-demand application. The application uses proprietary technology to remove TCP overheads.
-->

## Aktivera mapphierarki {#enable-folder-hierarchy}

Med konfigurationen [[!UICONTROL Enable Folder Hierarchy]](../using/brand-portal-sharing-folders.md#non-admin-user-access-to-shared-folders) kan administratörer styra hur icke-adminanvändare (redigerare, visningsprogram och gästanvändare) ser de delade mapparna efter inloggning.
