---
title: Publish-förinställningar, schema och ansikten för Brand Portal
seo-title: Publish presets, schema, and facets to Brand Portal
description: Lär dig hur du publicerar förinställningar, scheman och ansikten till Brand Portal.
seo-description: Learn how to publish presets, schema, and facets to Brand Portal.
uuid: c836d9bb-074a-4113-9c91-b2bf7658b88d
topic-tags: publish
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: bc305abc-9373-4d33-9179-0a5f3904b352
exl-id: 9b585606-6538-459b-87a9-2e68df0087b3
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 0%

---

# Publish-förinställningar, schema och ansikten för Brand Portal {#publish-presets-schema-and-facets-to-brand-portal}

Artikeln tar bort publicering av bildförinställningar, metadataram och anpassade sökfaktorer från AEM Author-instans till Brand Portal. Med publiceringsfunktionen kan organisationer återanvända bildförinställningar, metadatamatcheman och sökfaktorer som skapats/ändrats AEM Author-instansen, vilket minskar behovet av dubbelarbete.

>[!NOTE]
>
>Möjligheten att publicera bildförinställningar, metadataram och sökfaktorer från AEM Author-instans till Brand Portal finns AEM 6.2 SP1-CFP7 och AEM 6.3 SP 1-CFP 1 (6.3.1.1) och framåt.

## Publish bildförinställningar till Brand Portal {#publish-image-presets-to-brand-portal}

Bildförinställningar är en uppsättning kommandon för storleksändring och formatering som används på bilden när bilden levereras. Du kan skapa och ändra bildförinställningar på Brand Portal. Om AEM Author-instansen körs i läget för dynamiska medier kan användarna skapa förinställningar på AEM Author och publicera dem på AEM Assets Brand Portal, och undvika att återskapa samma förinställningar på Brand Portal.\
När förinställningen har skapats visas den som en dynamisk återgivning på resursdetaljåtergivningsfältet och i dialogrutan för hämtning.

>[!NOTE]
>
>Om AEM Author-instansen inte körs i **[!UICONTROL Dynamic Media Mode]** (kunden har inte köpt Dynamic Media), skapas inte **[!UICONTROL Pyramid TIFF]**-återgivningen av resurserna vid överföringen. Bildförinställningar eller dynamiska återgivningar fungerar på **[!UICONTROL Pyramid TIFF]** för en resurs, så om **[!UICONTROL Pyramid TIFF]** inte är tillgänglig på AEM Author-instansen är den inte heller tillgänglig på Brand Portal. Därför finns det inga dynamiska återgivningar i återgivningsfältet på sidan med resursinformation och i dialogrutan för hämtning.

Så här publicerar du bildförinställningar till Brand Portal:

1. I AEM Author-instansen trycker/klickar du på den AEM logotypen för att komma åt den globala navigeringskonsolen och trycker/ klickar på verktygsikonen och navigerar till **[!UICONTROL Assets > Image Presets]**.
1. Välj bildförinställningen eller flera bildförinställningar i listan med bildförinställningar och klicka/tryck på **[!UICONTROL Publish to Brand Portal]**.

![](assets/publishpreset.png)

>[!NOTE]
>
>När användare klickar på **[!UICONTROL Publish to Brand Portal]** köas bildförinställningarna för publicering. Användarna uppmanas att övervaka loggen för replikeringsagenterna för att bekräfta om publiceringen lyckades.

Så här avpublicerar du en bildförinställning från Brand Portal:

1. I AEM Author-instansen trycker/klickar du på den AEM logotypen för att komma åt den globala navigeringskonsolen, trycker/klickar på ikonen **[!UICONTROL Tools]** och navigerar till **[!UICONTROL Assets > Image Presets]**.
1. Välj en bildförinställning och välj **[!UICONTROL Remove from Brand Portal]** bland de tillgängliga alternativen högst upp.

## Publish metadatamatchema för Brand Portal  {#publish-metadata-schema-to-brand-portal}

Metadata-schemat beskriver layouten och egenskaperna som visas på egenskapssidan för resurser/samlingar.

![](assets/metadata-schema-editor.png) ![](assets/asset-properties-1.png)

Om användare har redigerat standardschemat på AEM Author-instansen och är villiga att använda samma schema som standardschemat på Brand Portal, kan de helt enkelt publicera metadatamappningsformulären till Brand Portal. I ett sådant fall åsidosätts standardschemat på Brand Portal av standardscheman som publiceras AEM författarinstansen.

Om användare har skapat ett anpassat schema AEM författarinstansen kan de publicera det anpassade schemat till Brand Portal i stället för att återskapa samma anpassade schema där. Användarna kan sedan använda det här anpassade schemat för alla mappar/samlingar i Brand Portal.

>[!NOTE]
>
>Standardscheman kan inte publiceras till Brand Portal om de är låsta vid AEM (d.v.s. de är oredigerade).

![](assets/default-schema-form.png)

>[!NOTE]
>
>Om en mapp har ett schema som används på AEM Author-instans måste samma schema också finnas på Brand Portal för att upprätthålla konsekvensen på sidan med resursegenskaper på AEM Author och Brand Portal.

Så här publicerar du ett metadataschema från AEM Author-instans till Brand Portal:

1. I AEM Author, tryck/klicka på den AEM logotypen för att komma åt den globala navigeringskonsolen och tryck/klicka på verktygsikonen och navigera till **[!UICONTROL Assets > Metadata Schemas]**.
1. Välj ett metadataschema och välj **[!UICONTROL Publish to Brand Portal]** bland de tillgängliga alternativen högst upp.

>[!NOTE]
>
>När användare klickar på **[!UICONTROL Publish to Brand Portal]** köas metadatamodeller för publicering. Användarna uppmanas att övervaka loggen för replikeringsagenterna för att bekräfta om publiceringen lyckades.

Så här avpublicerar du ett metadataschema från Brand Portal:

1. I AEM Author, tryck/klicka på den AEM logotypen för att komma åt den globala navigeringskonsolen och tryck/klicka på verktygsikonen och navigera till **[!UICONTROL Assets > Metadata Schemas]**.
1. Välj ett metadataschema och välj **[!UICONTROL Remove from Brand Portal]** bland de tillgängliga alternativen högst upp.

## Publish sökfack till Brand Portal {#publish-search-facets-to-brand-portal}

Sökformulär kan användas för [fasetterad sökning](../using/brand-portal-search-facets.md) för användare på Brand Portal. Sökfacets ger större granularitet åt sökningar i Brand Portal. Alla [predikat som läggs till](https://experienceleague.adobe.com/docs/experience-manager-65/assets/administer/search-facets.html) i sökformuläret är tillgängliga för användare som sökfaktorer i sökfilter.

![](assets/property-predicate-removed.png)
![](assets/search-form.png)

Om du vill använda det anpassade sökformuläret **[!UICONTROL Assets Admin Search Rail]** från AEM Author-instansen kan du publicera det anpassade sökformuläret från AEM Author-instansen till Brand Portal i stället för att återskapa samma formulär på Brand Portal.

>[!NOTE]
>
>Låst sökformulär **[!UICONTROL Assets Admin Search Rail]** på AEM Assets kan inte publiceras till Brand Portal om det inte redigeras. När sökformuläret har redigerats och publicerats i Brand Portal åsidosätts det av Brand Portal.

Så här publicerar du den redigerade sökaspekten från AEM Author-instansen till Brand Portal:

1. Tryck/klicka på AEM logotyp och gå sedan till **[!UICONTROL Tools > General > Search Forms]**.
1. Markera det redigerade sökformuläret och välj **[!UICONTROL Publish to Brand Portal]**.

   >[!NOTE]
   >
   >När användare klickar på **[!UICONTROL Publish to Brand Portal]** står sökfunktionerna i kö för publicering. Användarna uppmanas att övervaka loggen för replikeringsagenterna för att bekräfta om publiceringen lyckades.

Så här avpublicerar du sökformulär från Brand Portal:

1. I AEM Author, tryck/klicka på den AEM logotypen för att komma åt den globala navigeringskonsolen och tryck/klicka på verktygsikonen och navigera till **[!UICONTROL General > Search Forms]**.
1. Markera sökformuläret och välj **[!UICONTROL Remove from Brand Portal]** bland de tillgängliga alternativen överst.

>[!NOTE]
>
>Åtgärden **[!UICONTROL Unpublish from Brand Portal]** lämnar standardsökformuläret på Brand Portal och återställer inte det sökformulär som användes före publiceringen.

### Begränsningar {#limitations}

1. Ett fåtal sökpredikat kan inte användas för sökfilter på Brand Portal. När de här sökpredikaten publiceras som en del av sökformuläret från AEM Author-instansen till Brand Portal, filtreras de bort. Användarna ser därför färre antal predikt i det publicerade formuläret på Brand Portal. Se [sökpredikat som kan tillämpas på filter i Brand Portal](../using/brand-portal-search-facets.md#list-of-search-predicates).

1. Om en användare använder en anpassad sökväg för att läsa alternativ på AEM författarinstans för [!UICONTROL Options Predicate] fungerar den inte på Brand Portal. Dessa ytterligare sökvägar och alternativ publiceras inte till Brand Portal med sökformuläret. I så fall kan användare välja alternativet **[!UICONTROL Manual]** i **[!UICONTROL Add Options]** inom **[!UICONTROL Options Predicate]** för att lägga till dessa alternativ manuellt på Brand Portal.

![](assets/options-predicate-manual.png)
