---
title: Söka efter resurser i Brand Portal
description: Med Brand Portal sökfunktion kan du snabbt söka efter relevanta resurser med Omnissearch, och med sökfiltren kan du begränsa sökningen ytterligare. Spara dina sökningar som smarta samlingar för framtiden.
contentOwner: bdhar
content-type: reference
products: SG_EXPERIENCEMANAGER/Brand_Portal
topic-tags: SearchandPromote
exl-id: 7297bbe5-df8c-4d0b-8204-218a9fdc2292
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# Söka efter resurser i Brand Portal {#search-assets-on-brand-portal}

Med Brand Portal sökfunktion kan du snabbt söka efter relevanta resurser med hjälp av Omnissearch, och ansiktssökning som använder filter för att ytterligare begränsa sökningen. Du kan söka efter resurser på fil- eller mappnivå och spara sökresultaten som smarta samlingar.

>[!NOTE]
>
>Brand Portal stöder inte sökning i Samlingar med Omnissearch.
>
>Du kan dock använda [sökfilter för att hämta listan över relevanta samlingar](#search-collection).

## Söka efter resurser med Omnissearch {#search-assets-using-omnisearch}

Så här söker du efter resurser på Brand Portal:

1. Klicka på ikonen **[!UICONTROL Search]** i verktygsfältet eller tryck på tangenten **[!UICONTROL /]** (snedstreck) för att starta Omnissearch.

   ![](assets/omnisearchicon-1.png)

1. Skriv ett nyckelord för de resurser du vill söka efter i sökrutan.

   ![](assets/omnisearch.png)

   >[!NOTE]
   >
   >* Minst tre tecken krävs i Omnissearch för att sökförslagen ska visas.
   >* När du söker efter `mountain biking` returneras alla resurser i sökresultatet som har både `mountain` och `biking` tillgängliga i metadatafälten. Till exempel `mountain` i fältet `Title` och `biking` i fältet `Description`. Båda termerna måste vara tillgängliga i metadatafälten för att kunna visas i sökresultaten. Omnissearch returnerar emellertid resursen i sökresultaten även om bara en av de två termerna är tillgänglig i metadatafältet för smarta taggar. Anta till exempel att en resurs har `mountain` som en smart tagg men saknar `biking` i något annat metadatafält. Sedan söker du efter `mountain biking`. Omnissearch returnerar fortfarande resursen i sökresultaten. Det här arbetsflödet ser till att resurser med relevanta taggar inte missas.

1. Välj bland de relaterade förslag som visas i listrutan för att snabbt få tillgång till relevanta resurser.

   ![](assets/assets-search-result.png)

   *Resurssökning med Omnissearch*

Om du vill veta mer om sökbeteenden med smarta taggade resurser går du till [Mer information om sökresultat och sökbeteenden](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/search-assets).

## Söka med ansikten på panelen Filter {#search-using-facets-in-filters-panel}

Sökfaktorer på panelen Filter ger en mer detaljerad sökupplevelse och gör sökfunktionen mer effektiv. Sökfacets använder flera dimensioner (predikatfärger) som gör att du kan utföra komplexa sökningar. Du kan enkelt gå ned till önskad detaljnivå för en mer fokuserad sökning.

Om du till exempel söker efter en bild kan du välja om du vill ha en bitmapp eller en vektorbild. Du kan begränsa sökomfånget ytterligare genom att ange bildens MIME-typ i sökgränssnittet för filtyp. På samma sätt kan du ange formatet, t.ex. PDF eller MS® Word, när du söker efter dokument.

![Panelen Filter i Brand Portal](assets/file-type-search.png "Panelen Filter i Brand Portal")

Panelen **[!UICONTROL Filters]** innehåller några standardaspekter, till exempel - **[!UICONTROL Path Browser]**, **[!UICONTROL File Type]**, **[!UICONTROL File Size]**, **[!UICONTROL Status]** och **[!UICONTROL Orientation]**.
Du kan dock [lägga till anpassade sökfaktorer](../using/brand-portal-search-facets.md) eller ta bort specifika från panelen **[!UICONTROL Filters]**. Redigera bara predikten i det underliggande sökformuläret. Se listan med tillgängliga och användbara [sökpredikatorer i Brand Portal](../using/brand-portal-search-facets.md#list-of-search-predicates).

Om du vill använda filter på sökningen använder du de tillgängliga [sökfunktionerna](../using/brand-portal-search-facets.md):

1. Klicka på övertäckningsikonen och välj **[!UICONTROL Filter]**.

   ![](assets/selectorrail.png)

1. Välj lämpliga alternativ på panelen **[!UICONTROL Filters]** till vänster för att använda de relevanta filtren.
Använd till exempel följande standardfilter:

   * **[!UICONTROL Path Browser]** om du vill söka efter resurser i en viss katalog. Standardsöksökvägen för predikatet för sökvägsläsaren är `/content/dam/mac/<tenant-id>/`, som kan konfigureras genom att redigera standardsökformuläret.

   >[!NOTE]
   >
   >För icke-adminanvändare visar [!UICONTROL Path Browser] på panelen [!UICONTROL Filter] endast innehållsstrukturen för de mappar (och deras överordnade mappar) som delas med dem.\
   >Om du vill administrera användare kan du navigera till valfri mapp i Brand Portal med hjälp av Path Browser.

   * **[!UICONTROL File Type]** för att ange typ (bild, dokument, multimedia, arkiv) av resursfilen som du söker efter. Du kan dessutom begränsa omfattningen av sökningen, till exempel ange MIME-typen (TIFF, Bitmapp, GIMP-bilder) för bilden eller formatet (PDF eller MS® Word) för dokumenten.
   * **[!UICONTROL File Size]** om du vill söka efter resurser baserat på deras storlek. Du kan ange de nedre och övre gränserna för storleksintervallet för att begränsa sökningen och ange vilken måttenhet som ska sökas igenom.
   * **[!UICONTROL Status]** om du vill söka efter resurser baserat på tillgångsstatus, till exempel Godkänd, Ändringar Begärd, Avvisad, Väntande) och Förfallotid.
   * **[!UICONTROL Average Rating]** om du vill söka efter resurser baserat på resursernas klassificering.
   * **[!UICONTROL Orientation]** om du vill söka efter resurser baserat på orienteringen (vågrät, lodrät, kvadratisk) för resurserna.
   * **[!UICONTROL Style]** om du vill söka efter resurser baserat på resursernas stil (färgad, monokrom).
   * **[!UICONTROL Video Format]** om du vill söka efter videoresurser baserat på deras format (DVI, Flash, MPEG4, MPEG, OGG Theora, QuickTime, Windows Media, WebM).

   Du kan använda [anpassade sökfunktioner](../using/brand-portal-search-facets.md) på panelen Filter genom att redigera det underliggande sökformuläret.

   * **[!UICONTROL Property Predicate]** om det används i sökformuläret kan du söka efter resurser som matchar en metadataegenskap som predikatet är mappat till.\
     Om egenskapspredikatet till exempel är mappat till `jcr:content/metadata/dc:title` kan du söka efter resurser baserat på deras titel.\
     [!UICONTROL Property Predicate] stöder textsökningar för:

     **Partiella fraser**
Om du vill tillåta resurssökning med partiella fraser i Property Predicate markerar du kryssrutan **[!UICONTROL Partial Search]** i sökformuläret. Med den här metoden kan du söka efter de önskade resurserna även om du inte anger exakt vilka ord eller fraser som används i metadata för resursen.

     >[!NOTE]
     >
     > Brand Portal har stöd för följande fält för partiell sökning:
     >
     >* `jcr:content/metadata/dc:title`
     >* `jcr:content/jcr:title`
     >* `jcr:content/metadata/dc:format`

     Du kan:
      * Ange ett ord som förekommer i din sökfras i ansiktet på panelen Filter. Om du till exempel söker efter termen **klättb** (och egenskapspredikatet mappas till egenskapen `dc:title`) returneras alla resurser med ordet **klättb** i rubrikfrasen.
      * Ange en del av ordet som förekommer i den sökta frasen tillsammans med ett jokertecken (&#42;) för att fylla i luckorna.
Om du till exempel söker efter:
         * **klättb&#42;** returnerar alla resurser som har ord som börjar med tecknen &quot;klättra&quot; i titelfrasen.
         * **&#42;klättb** returnerar alla resurser med ord som slutar med tecknen &quot;klättra&quot; i titelfrasen.
         * **&#42;klättb&#42;** returnerar alla resurser som har ord som innehåller tecknen &quot;klättra&quot; i titelfrasen.

     **Ej skiftlägeskänslig text**
Du kan tillåta icke-skiftlägeskänslig sökning i Egenskapspredikat. Aktivera bara kryssrutan **[!UICONTROL Ignore Case]** i sökformuläret. Som standard är textsökningen i Egenskapsförutsägelse skiftlägeskänslig.

   >[!NOTE]
   >
   >När du markerar kryssrutan **[!UICONTROL Partial Search]** markeras **[!UICONTROL Ignore Case]** som standard.

   ![](assets/wildcard-prop-1.png)

   Sökresultaten visas enligt de filter som används, tillsammans med antalet sökresultat.

   ![](assets/omnisearch-with-filters.png)

   Resultat av resurssökning med antal sökresultat.

1. Du kan enkelt navigera till ett objekt från sökresultatet och gå tillbaka till samma sökresultat med bakåtknappen i webbläsaren utan att behöva köra sökfrågan igen.

## Spara dina sökningar som en smart samling {#save-your-searches-as-smart-collection}

Du kan spara sökinställningarna som en smart samling om du snabbt vill kunna upprepa samma sökning utan att behöva göra om samma inställningar senare. Du kan dock inte använda sökfilter i en samling.

Så här sparar du sökinställningarna som en smart samling:

1. Klicka på **[!UICONTROL Save Smart Collection]** och ange ett namn för den smarta samlingen.

   Om du vill göra den smarta samlingen tillgänglig för alla användare väljer du **[!UICONTROL Public]**. Ett meddelande bekräftar att den smarta samlingen skapades och lades till i listan över dina sparade sökningar.

   >[!NOTE]
   >
   >Du kan hindra användare som inte är administratörer från att göra smarta samlingar offentliga för att undvika att ha ett stort antal publika smarta samlingar som skapats av användare som inte är administratörer i organisationens Brand Portal. Organisationer kan inaktivera **[!UICONTROL Allow public smart collections creation]**-konfigurationen från de **[!UICONTROL General]**-inställningar som är tillgängliga på panelen Administrationsverktyg.

   ![](assets/save_smartcollectionui.png)

1. Om du vill spara den smarta samlingen med ett annat namn och markera eller avmarkera kryssrutan **[!UICONTROL Public]** klickar du på **[!UICONTROL Edit Smart Collection]**.

   ![](assets/edit_smartcollection.png)

1. I dialogrutan **[!UICONTROL Edit Smart Collection]** väljer du **[!UICONTROL Save As]** och anger ett namn för den smarta samlingen. Klicka på **[!UICONTROL Save]**.

   ![](assets/saveas_smartsearch.png)


## Sök i samling {#search-collection}

Omnissearch stöds inte för samlingar. Du kan dock använda sökfilter för att lista de relevanta samlingarna inifrån [!UICONTROL Collections]-gränssnittet.

I gränssnittet [!UICONTROL Collections] klickar du på övertäckningsikonen för att öppna filterpanelen i den vänstra listen. Använd ett eller flera sökfilter från tillgängliga filter (`modified date`, `access type` och `tags`). Här visas den mest relevanta uppsättningen samlingar baserat på de använda filtren.

![](assets/collection-search.png)
