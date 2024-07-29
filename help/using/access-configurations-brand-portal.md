---
title: Administrera användaråtkomst på Brand Portal
description: Konfigurera gäståtkomst och åtkomst för nya användare på Brand Portal.
contentOwner: mgulati
topic-tags: administration
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 27a9cd26-9bb3-473b-b1ac-37f77975c912
source-git-commit: 1a3e51922fb658d9d05113b4b1f4d05a0b6555c0
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Administrera användaråtkomst på Brand Portal {#administer-user-access-on-brand-portal}

Adobe Experience Manager Assets Brand Portal 6.4.2 och senare ger administratörer behörighet att konfigurera gäståtkomst och göra det möjligt för användare att begära åtkomst till Brand Portal i sin organisation. Dessa konfigurationer har tillhandahållits som **[!UICONTROL Access Settings]** konfigurationer på administrationspanelen. Båda inställningarna är inaktiverade som standard.

![](assets/access-configs.png)

**A** - Konfiguration för att ge gäster åtkomst till Brand Portal via länken **[!UICONTROL `Guest Access?`]** på Brand Portal välkomstskärm. (Standard är inaktiverat)

**B** - Konfiguration som gör att användare kan begära åtkomst till Brand Portal via länken **[!UICONTROL `Need access?`]** på Brand Portal välkomstskärm. (Standard är inaktiverat)

## Tillåt gäståtkomst {#allow-guest-access}

Genom att tillåta gäståtkomst kan användarna få åtkomst till offentliga resurser utan att behöva logga in på Brand Portal.
Administratören måste utföra följande steg för att tillåta gäståtkomst:

1. Välj AEM logotyp för att komma åt administrationsverktygen i verktygsfältet högst upp.
1. Öppna sidan **[!UICONTROL Access Settings]** genom att välja **[!UICONTROL Access]** på panelen Administrationsverktyg.
1. Aktivera **[!UICONTROL Allow Guest Access]**-konfigurationen.
1. **[!UICONTROL Save]** ändringarna.
1. Logga ut för att ändringarna ska börja gälla.

![](assets/bp-welcome-screen.png)

## Tillåt användare att begära åtkomst {#allow-users-to-request-access}

Administratörer kan tillåta användare i organisationen att begära åtkomst till Brand Portal från välkomstskärmen. Administratörer måste dock aktivera konfigurationen för **[!UICONTROL Allow Users to Request Access]** så att länken för åtkomstbegäran visas på välkomstskärmen.

För att organisationsanvändare ska kunna begära åtkomst från Brand Portal måste administratörerna:

1. Välj AEM logotyp för att komma åt administrationsverktygen i verktygsfältet högst upp.
1. Öppna sidan **[!UICONTROL Access Settings]** genom att välja **[!UICONTROL Access]** på panelen Administrationsverktyg.
1. Aktivera **[!UICONTROL Allow Users to Request Access]**-konfigurationen.
1. **[!UICONTROL Save]** ändringarna.
1. Logga ut för att ändringarna ska börja gälla.
