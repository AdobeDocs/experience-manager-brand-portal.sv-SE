---
title: Publish-taggar till Brand Portal
seo-title: Publish tags to Brand Portal
description: Lär dig publicera taggar från Experience Manager Assets till Brand Portal.
seo-description: Learn how to publish tags from Experience Manager Assets to Brand Portal.
uuid: 4167367e-1af8-476b-97a5-730c43bd0816
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: 3c8e9251-195d-4c56-a9a9-27bc8b2a82a4
exl-id: 842656a6-1a2b-4b64-954d-1e663923a1a1
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---

# Publish-taggar till Brand Portal {#publish-tags-to-brand-portal}

Lär dig publicera taggar från Experience Manager Assets till Brand Portal.

Taggar är användbara när du vill ordna resurser och förbättra sökbarheten för resurser som de är kopplade till. Taggar kan ses som nyckelord eller etiketter (metadata) som bifogas med resurser, och gör att resurser snabbt kan hittas som ett resultat av en sökning. Om du vill veta hur du tilldelar taggar till resurser i Experience Manager Assets läser du [använd taggar för att ordna resurser](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/organize-assets.html).

Taggar (som är kopplade till resurser och samlingar i AEM) publiceras automatiskt till Brand Portal när resurser (och samlingar) med associerade taggar publiceras till Brand Portal. De publicerade taggarna är användbara när du vill göra det möjligt att söka efter associerade resurser.

>[!NOTE]
>
>Vi rekommenderar dock att du exklusivt publicerar taggar till Brand Portal innan du publicerar de resurser (och samlingar) som taggarna är kopplade till. Detta ger snabbare publicering av materialet (och samlingarna) till Brand Portal.

## Hantera taggar {#manage-tags}

Du kan använda de befintliga taggarna för att bifoga till en resurs eller skapa nya taggar AEM taggkonsolen (**[!UICONTROL Tools | Tagging | AEM Tags]**). I båda fallen måste du först publicera taggarna till Brand Portal och sedan associera dem med lämpliga resurser.

Så här skapar du taggar på AEM, publicerar taggar på Brand Portal och associerar taggarna med lämpliga resurser (eller samlingar):

1. **Skapa taggar**
Logga in på AEM Author instance med administratörsbehörighet och öppna **[!UICONTROL AEM Tags]** console från global navigering:

   1. Välj **[!UICONTROL Tools]**

   1. Välj **[!UICONTROL General]**

   1. Välj **[!UICONTROL Tagging]**

1. Välj **[!UICONTROL Create]** och välj sedan alternativet **[!UICONTROL Create Tag]**.
1. Ange:

   * **[!UICONTROL Title]**
     *(obligatoriskt)* En visningsrubrik för taggen.
   * **[!UICONTROL Name]**
     *(obligatoriskt)* Ett namn för taggen. Om inget anges skapas ett giltigt nodnamn från titeln. Se [TaggID](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/tagging/framework.html).
   * **Beskrivning**
     *(valfritt)* En beskrivning av taggen.
   * **Taggsökväg**
JCR-sökväg för taggen.

1. Välj **[!UICONTROL Submit]** för att skapa taggen.

   När du har skapat en tagg för AEM blir taggen tillgänglig för att bifogas till en resurs (med egenskapssektionen eller avsnittet Hantera taggar för den resursen).

1. **Publish taggen till Brand Portal**.

   Gå till **[!UICONTROL AEM Tags]**-konsolen ([!UICONTROL Tools | Tagging | AEM Tags]), markera önskad tagg och Publish till Brand Portal.

1. **Koppla taggen till en resurs (eller samling)**.

   Markera en resurs (eller samling) och bifoga den önskade taggen med egenskapssektionen eller avsnittet Hantera taggar för den resursen. Mer information om hur du tilldelar taggar till resurser i AEM Assets finns i [använd taggar för att ordna resurser](https://experienceleague.adobe.com/docs/experience-manager-65/assets/managing/organize-assets.html).

1. **Publish-resurser (eller samlingar) till Brand Portal**.\
   När du publicerar en resurs (eller samling) till Brand Portal är den bifogade taggen även tillgänglig i Brand Portal.

   Om du vill se den bifogade taggen för respektive resurs (eller samling) i Brand Portal loggar du in på Brand Portal och väljer resursen, under egenskapsavsnittet ser du den bifogade taggen.

## Search Promote {#search-promote}

Med AEM Assets Brand Portal kan du få specifika resurser att bli det bästa resultatet för sökningar som baseras på en nyckelordstagg.

Så här utökar du en resurs för ett söknyckelord:

1. Öppna sidan **[!UICONTROL Properties]** för en resurs på AEM författarinstans.
1. Gå till fliken **[!UICONTROL Advanced]**.
1. I **[!UICONTROL Search Promote]** i avsnittet **[!UICONTROL Elevate for search keywords]** väljer du **[!UICONTROL Add]** för att lägga till söknyckelord eller -taggar.

   ![](assets/search-promote.png)

1. Spara ändringarna.
1. Publish materialet till Brand Portal.
1. Logga in på Brand Portal. Visa fliken **[!UICONTROL Advanced]** i avsnittet **[!UICONTROL Properties]** för resursen.
Observera att nyckelordet **[!UICONTROL Search Promote]** också visas i egenskaperna för resursen.
