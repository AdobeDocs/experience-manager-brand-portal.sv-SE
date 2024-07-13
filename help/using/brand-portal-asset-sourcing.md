---
title: Resurshantering i Brand Portal
seo-title: Asset Sourcing in Brand Portal
description: Få insikt i den nya resurskällfunktionen i Adobe Experience Manager Assets Brand Portal.
seo-description: Get an insight into the asset sourcing feature released in the Adobe Experience Manager Assets Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
sub-product: assets
topics: collaboration, content-velocity, sharing
doc-type: feature-video
activity: use
audience: author, marketer
version: 6.5
kt: 3838
exl-id: 2c132a7a-ed10-4856-8378-67939167ea60
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---

# Översikt över resurskälla {#overview-asset-sourcing-in-bp}

Med **Resurshantering** kan Experience Manager Assets-användare (administratörer/icke-admin-användare) skapa nya mappar med en extra **Resursbidrag** -egenskap, vilket garanterar att den nya mappen som skapas är öppen för resursöverföring av Brand Portal-användare. Detta utlöser automatiskt ett arbetsflöde som skapar ytterligare två undermappar, som kallas **DELAD** och **NY**, i den nya **Contribute** -mappen. Administratören definierar sedan behovet genom att ladda upp en översikt över de typer av resurser som ska läggas till i bidragsmappen, samt en uppsättning baslinjeresurser, till mappen **SHARED** för att säkerställa att BP-användarna har den referensinformation de behöver. Administratören kan sedan ge aktiva Brand Portal-användare åtkomst till mappen för bidrag innan den nyligen skapade **Contribute**-mappen publiceras på Brand Portal. När användaren är klar med att lägga till innehåll i mappen **NEW** kan de publicera bidragsmappen i Experience Manager-redigeringsmiljön. Observera att det kan ta några minuter att slutföra importen och återspegla det nya publicerade innehållet i Experience Manager Assets.

Dessutom ändras inte alla befintliga funktioner. Brand Portal-användare kan visa, söka efter och hämta resurser från bidragsmappen samt från andra tillåtna mappar. Administratörer kan dessutom dela mappen för bidrag ytterligare, ändra egenskaper och lägga till resurser i samlingar.

![Brand Portal Resurser](assets/asset-sourcing.png)

>[!VIDEO](https://video.tv.adobe.com/v/29365/?quality=12)

## Förutsättningar {#prerequisites}

* Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.5.2 eller senare.
* Kontrollera att din Experience Manager Assets-instans är konfigurerad med Brand Portal. Se [Konfigurera Experience Manager Assets med Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

<!--
* Ensure that your Brand Portal tenant is configured with one AEM Assets author instance.
-->

>[!NOTE]
>
>Funktionen Resurshantering är som standard aktiverad i Experience Manager Assets as a Cloud Service, Experience Manager Assets 6.5.9 och senare.
>
>De befintliga konfigurationerna fortsätter att fungera med de tidigare versionerna.

>[!NOTE]
>
>Det finns ett känt fel i Experience Manager Assets 6.5.4. Brand Portal-användare kan inte publicera resurser i mappen för bidrag till Experience Manager Assets när de uppgraderar till Adobe Developer Console.
>
>Problemet har åtgärdats i Experience Manager Assets 6.5.5. Du kan uppgradera din Experience Manager Assets-instans till den senaste Service Pack-versionen och [uppgradera dina konfigurationer](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) på Adobe Developer Console.

<!--

>For immediate fix on AEM 6.5.4, it is recommended to [download the hotfix](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq650/hotfix/cq-6.5.0-hotfix-33041) and install on your author instance.
-->

<!--
## Configure Asset Sourcing {#configure-asset-sourcing}

**Asset Sourcing** is configured from within the AEM Assets author instance. The administrators can enable the Asset Sourcing feature flag configuration from the **AEM Web Console Configuration** and upload the active Brand Portal users list in **AEM Assets**.

>[!NOTE]
>
>Asset Sourcing is by default enabled on AEM Assets as a Cloud Service. The AEM administrator can directly upload the active Brand Portal users to allow them access to the Asset Sourcing feature.

>[!NOTE]
>
>Before you begin with the configuration, ensure that your AEM Assets instance is configured with Brand Portal. See, [Configure AEM Assets with Brand Portal](../using/configure-aem-assets-with-brand-portal.md). 

The following video demonstrates, how to configure Asset Sourcing on your AEM Assets author instance:

>[!VIDEO](https://video.tv.adobe.com/v/29771)
-->

<!--
### Enable Asset Sourcing {#enable-asset-sourcing}

AEM administrators can enable the Asset Sourcing feature flag from within the AEM Web Console Configuration (a.k.a Configuration Manager).

>[!NOTE]
>
>This step is not applicable for AEM Assets as a Cloud Service.


**To enable Asset Sourcing:**
1. Log in to your AEM Assets author instance and open Configuration Manager. 
Default URL: http:// localhost:4502/system/console/configMgr.
1. Search using the keyword **Asset Sourcing** to locate **[!UICONTROL Asset Sourcing Feature Flag Config]**.
1. Click **[!UICONTROL Asset Sourcing Feature Flag Config]** to open the configuration window.
1. Select the **[!UICONTROL feature.flag.active.status]** check box.
1. Click **[!UICONTROL Save]**.

![](assets/enable-asset-sourcing.png)
-->


### Ladda upp Brand Portal-användarlista {#upload-bp-user-list}

Experience Manager Assets-administratörer kan överföra Brand Portal-användarkonfigurationsfilen (.csv) som innehåller den aktiva Brand Portal-användarlistan i Experience Manager Assets för att ge dem åtkomst till funktionen Resurser.

En mapp för bidrag kan bara delas med de aktiva Brand Portal-användare som är definierade i användarlistan. Administratören kan även lägga till nya användare i konfigurationsfilen och överföra den ändrade användarlistan.

>[!NOTE]
>
>Kontrollera att din Experience Manager Assets-instans är konfigurerad med Brand Portal. Se [Konfigurera Experience Manager Assets med Brand Portal](../using/configure-aem-assets-with-brand-portal.md).

>[!NOTE]
>
>CSV-filens format är detsamma som det som stöds i Admin Console för bulkanvändarimport. E-post, förnamn och efternamn är obligatoriska.

Administratörerna kan lägga till nya användare i Admin Console. Mer information finns i [Hantera användare](brand-portal-adding-users.md). När du har lagt till användare i Admin Console kan dessa användare läggas till i Brand Portal användarkonfigurationsfil och sedan tilldelas behörighet att komma åt mappen för bidrag.

**Så här överför du Brand Portal-användarlista:**

1. Logga in på din Experience Manager Assets-instans.
1. Navigera till **[!UICONTROL Assets]** > **[!UICONTROL Brand Portal Users]** från panelen **Verktyg**.

1. Fönstret Brand Portal Upload Contributors öppnas.
Bläddra från den lokala datorn och överför **konfigurationsfilen (.csv)** som innehåller den aktiva Brand Portal-användarlistan.
1. Klicka på **[!UICONTROL Save]**.

   ![](assets/upload-user-list2.png)


Administratörer kan ge åtkomst till specifika användare från den här användarlistan när de konfigurerar en mapp för bidrag. Endast de användare som är tilldelade till en bidragsmapp har tillgång till bidragsmappen och publicerar resurser från Brand Portal till Experience Manager Assets.

## Se även {#reference-articles}

* [Konfigurera och publicera avgiftsbelagda mappar i Brand Portal](brand-portal-publish-contribution-folder-to-brand-portal.md)

* [Publish-mapp för bidrag till Experience Manager Assets](brand-portal-publish-contribution-folder-to-aem-assets.md)
