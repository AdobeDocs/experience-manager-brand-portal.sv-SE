---
title: Hantera digitala rättigheter för resurser
seo-title: Hantera digitala rättigheter för resurser
description: Genom att licensiera resurser och ange förfallodatum för resurser och delade länkar kan du kontrollera användningen av dessa resurser och skydda dem.
seo-description: Genom att licensiera resurser och ange förfallodatum för resurser och delade länkar kan du kontrollera användningen av dessa resurser och skydda dem.
uuid: ce30e398-0109-41bf-a4d2-2fcca476f499
contentOwner: bdhar
topic-tags: download-install
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
discoiquuid: f77003ba-31fe-4a9e-96c8-dbc4c2eba79e
role: Admin
exl-id: 86c31891-0627-41ca-b571-8dac3a074d55
source-git-commit: 26b009fec800d9b437bde5838009c71b1b3b7ac6
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 0%

---

# Hantera digitala rättigheter för resurser {#manage-digital-rights-of-assets}

För att skydda ert varumärke är det viktigt att säkerställa säker distribution och användning av kreativa tillgångar och varumärkesmaterial. Detta kan framtvingas i hela organisationen och utanför genom att ett förfallodatum (och en förfallotid) kopplas till godkända mediefiler som publiceras från AEM till Brand Portal, eller genom att dessa mediefiler licensieras för villkorlig användning. I Brand Portal kan du också ange ett förfallodatum för länkar till resurser som delas från Brand Portal.

Läs vidare för att lära dig hur materialet skyddas på Brand Portal och förstå de tillhörande användningsbehörigheterna.

## Resursens förfallodatum {#asset-expiration}

Att mediefiler förfaller är ett effektivt sätt att kontrollera användningen av godkända mediefiler på Brand Portal i en hel organisation. Alla mediefiler som publiceras från AEM Assets till Brand Portal kan ha ett förfallodatum, vilket begränsar användningen av dessa mediefiler från olika användarroller.

### Användningsbehörigheter för resurser som gått ut {#usage-permissions-expired-assets}

I Brand Portal kan administratörer visa, ladda ned och lägga till material som gått ut i samlingar. Redigerare och visningsprogram kan bara visa och lägga till utgångna resurser i samlingar.

Administratörer kan publicera material som gått ut från AEM Assets till Brand Portal. Utgångna mediefiler kan dock inte delas via bläck från Brand Portal. Om du väljer en resurs som har gått ut i en mapp som innehåller både förfallna och icke-utgångna resurser är åtgärden **[!UICONTROL Share Link]** inte tillgänglig. Men om du väljer en mapp som innehåller resurser som har gått ut och som inte gått ut är åtgärderna [!UICONTROL Share] och **[!UICONTROL Share Link]** tillgängliga.

>[!NOTE]
>
>En mapp kan fortfarande delas som en länk, även om den innehåller resurser som har gått ut. I det här fallet listar länken inte resurser som har gått ut och bara resurser som inte har gått ut delas.

I följande tabell visas användningsbehörigheterna för utgångna resurser:

|  | **[!UICONTROL Link share]** | **[!UICONTROL Download]** | **[!UICONTROL Properties]** | **[!UICONTROL Add to collection]** | **[!UICONTROL Delete]** |
|---|---|---|---|---|---|
| **[!UICONTROL Administrator]** | Otillgänglig | Tillgänglig | Tillgänglig | Tillgänglig | Tillgänglig |
| **[!UICONTROL Editor]** | Otillgänglig | Otillgänglig | Tillgänglig | Tillgänglig | Otillgänglig |
| **[!UICONTROL Viewer]** | Otillgänglig | Otillgänglig | Tillgänglig | Tillgänglig | Otillgänglig |
| **[!UICONTROL Guest user]** | Otillgänglig | Otillgänglig | Tillgänglig | Tillgänglig | Otillgänglig |

>[!NOTE]
>
>Om visningsprogram och redigerare hämtar en mapp med resurser som har upphört att gälla och som inte har gått ut, hämtas endast de resurser som inte har gått ut. Om en mapp bara innehåller resurser som har gått ut hämtas en tom mapp.

### Utgångsstatus för tillgångar {#expiration-status-of-assets}

Du kan visa förfallostatusen för resurser i deras **[!UICONTROL Card View]**. En röd flagga på kortet anger att resursen har gått ut.

![](assets/expired_assets_cardview.png)

>[!NOTE]
>
>I list- och kolumnvyer visas inte tillgångarnas förfallostatus.

## Resurslänkens förfallodatum {#asset-link-expiration}

När du delar resurser via länkar kan administratörer och redigerare ange ett datum och en tid när de ska förfalla med fältet **[!UICONTROL Expiration]** i dialogrutan **[!UICONTROL Link Sharing]**. Länkens standardförfallodatum är sju dagar från det datum då länken delas.

![](assets/asset-link-sharing.png)

Det ser till att resurser som delas som länkar förfaller det datum och den tid som anges av Brand Portal administratörer och redigerare och inte längre kan visas och hämtas efter förfallodatumet. Eftersom resurser som delas via länkar också kan visas av externa användare som inte är en del av organisationen, kan du genom att ange förfallodatum se till att dina godkända resurser är skyddade och inte exponerade för okända enheter längre än en angiven tid.

Mer information om länkdelning finns i [Dela resurser som en länk](../using/brand-portal-link-share.md).

## Licensierade resurser {#licensed-assets}

För licensierade mediefiler krävs att ett licensavtal godkänns innan du laddar ned dem från Brand Portal. Det här avtalet för licensierade mediefiler levereras när du hämtar mediefilen direkt från Brand Portal eller via en delad länk. Licensskyddade resurser kan visas av alla användare, oavsett om de har gått ut eller inte. Hämtningen och användningen av licensierade mediefiler som upphört att gälla är dock begränsad. Om du vill veta mer om hur licensierade resurser och tillåtna aktiviteter som har upphört att gälla baserat på användarroller kan du läsa [användningsbehörigheter för utgångna resurser](../using/manage-digital-rights-of-assets.md#usage-permissions-expired-assets).

Licensskyddade resurser har [licensavtal som är kopplade](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) till sig, vilket görs genom att ställa in resursens [metadataegenskap](https://helpx.adobe.com/experience-manager/6-5/assets/using/drm.html#DigitalRightsManagementinAssets) i AEM Assets.

Om du väljer att hämta licensskyddade mediefiler omdirigeras du till sidan **[!UICONTROL Copyright Management]**.

![](assets/asset-copyright-mgmt.png)

Här måste du välja resursen för att hämta och godkänna det associerade licensavtalet. Om du inte godkänner licensavtalet är knappen **[!UICONTROL Download]** inte aktiverad.

![](assets/licensed-asset-download-2.png)

Om markeringen innehåller flera skyddade resurser markerar du en resurs i taget, godkänner licensavtalet och fortsätter att hämta resursen.

## Generera en rapport över förfallna resurser {#generate-report-about-expired-assets}

Administratörer kan generera och ladda ned en rapport med en lista över alla mediefiler som gått ut inom en viss tidsram. Den här rapporten innehåller detaljerad information - som storlek, typ, sökväg som anger resursens placering i resurshierarkin, när tillgången förföll och när den publicerades - om de förfallna tillgångarna. Kolumnerna i den här rapporten kan anpassas för att visa mer data baserat på användarkrav.

![](assets/assets-expired.png)

Mer information om rapportfunktionen finns i [Arbeta med rapporter](../using/brand-portal-reports.md#work-with-reports).
