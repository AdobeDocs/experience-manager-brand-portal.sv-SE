---
title: Dynamiskt videostöd i Brand Portal
description: Dynamiskt videostöd i Brand Portal
contentOwner: mgulati
products: SG_EXPERIENCEMANAGER/Brand_Portal
content-type: reference
topic-tags: download-install
exl-id: 08d6a0fb-061e-4bef-b8e2-bb8522e7482e
source-git-commit: ce9cf89dc3fdfe1f147096b42233aa3f599dcf43
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---

# Dynamiskt videostöd i Brand Portal {#dynamic-video-support-on-brand-portal}

Förgranska och spela upp videor på ett anpassat sätt på Brand Portal med stöd för dynamiska media. Hämta även dynamiska återgivningar från portalen och delade länkar.
Brand Portal kan

* Förhandsgranska videoklipp på sidan Resursinformation, i kortvyn och på sidan för förhandsgranskning av länkdelning.
* Spela upp videokodningar på sidan Resursinformation.
* Visa dynamiska återgivningar på fliken Återgivningar på sidan Resursinformation.
* Ladda ned videokoder och mappar med videoklipp.

>[!NOTE]
>
>Om du vill arbeta med videoklipp och publicera dem på Brand Portal kontrollerar du att din instans av Experience Manager Author är konfigurerad i läget Dynamic Media Hybrid eller Dynamic Media **[!DNL Scene7]**.

För att förhandsgranska, spela upp och ladda ned videor visar Brand Portal följande två konfigurationer för administratörer:

* [Dynamisk hybridkonfiguration för media](#configure-dm-hybrid-settings)
Om Experience Manager Author-instansen körs i läget Dynamic Media - hybrid.
* [Dynamiska media [!DNL Scene7] konfiguration](#configure-dm-scene7-settings)
Om Experience Manager Author-instansen körs i läget Dynamic Media - **[!DNL Scene7]** .
Ange någon av dessa konfigurationer baserat på de konfigurationer du anger i din Experience Manager Author-instans som Brand Portal-klienten replikeras med.

>[!NOTE]
>
>Dynamiska videor stöds inte på Brand Portal-klientorganisationer som har konfigurerats med Experience Manager Author som körs i körläge **[!UICONTROL Scene7 Connect]**.

## Hur spelas dynamiska videor upp? {#how-are-dynamic-videos-played}

![Videokodningar hämtas från molnet](assets/VideoEncodes.png)

Om dynamiska mediekonfigurationer ([hybridkonfigurationer](../using/dynamic-video-brand-portal.md#configure-dm-hybrid-settings) eller [[!DNL Scene7]](../using/dynamic-video-brand-portal.md#configure-dm-scene7-settings)) har konfigurerats på Brand Portal hämtas de dynamiska återgivningarna från **[!DNL Scene7]**-servern. Videokodningar förhandsvisas och spelas upp utan fördröjning och kvalitetsförvrängning.

Brand Portal-databasen lagrar inte videokodningar och hämtar dem från **[!DNL Scene7]**-servern. Kontrollera att de dynamiska mediekonfigurationerna i både Adobe Experience Manager Author Instance och Brand Portal är desamma.

>[!NOTE]
>
>Videovisningsprogram och visningsförinställningar stöds inte i Brand Portal. Videor förhandsvisas och spelas upp på standardvisningsprogrammen i Brand Portal.

## Förutsättningar {#prerequisites}

Om du vill arbeta med dynamiska videoklipp på Brand Portal måste du se till att:

* **Starta Experience Manager Author i läget Dynamic Media**

  Starta Experience Manager Author-instansen (som Brand Portal är konfigurerat med) antingen i [Dynamic Media - [!DNL Scene7] mode](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/config-dms7#enabling-dynamic-media-in-scene-mode) eller i [Dynamic Media - hybrid-läge](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/config-dynamic) eller

* **Konfigurera Dynamic Media Cloud Services på Experience Manager Author-instansen**

  Baserat på det dynamiska medieläge (Scene7-läge eller hybridläge) som Experience Manager Author körs i anger du antingen [Dynamic Media Cloud Services ([!DNL Scene7] mode)](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) eller [Dynamic Media Cloud Services (hybridläge)](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) på Experience Manager Author från **Tools** | **Molntjänster** | **Dynamiska media**.

* **Konfigurera dynamiska media på Brand Portal**

  Baserat på Dynamic Media Cloud-konfigurationer på Experience Manager Author konfigurerar du inställningarna för [Dynamic Media](#configure-dm-hybrid-settings) eller [[!DNL Scene7] inställningar](#configure-dm-scene7-settings) från Brand Portal administrationsverktyg.

  Kontrollera att [separata Brand Portal-klientorganisationer](#separate-tenants) används för Experience Manager Author-instanser som har konfigurerats i läget Dynamic Media - **[!UICONTROL Scene7]** och Dynamic Media - Hybrid. Om du använder funktionerna för Dynamic Media **[!UICONTROL S7]** och Dynamic Media Hybrid är detta särskilt viktigt.

* **Publicera mappar med videokodning tillämpad på Brand Portal**

  Använd [videokodning](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/video-profiles) och publicera mappen med multimedieresurser från Experience Manager Author-instansen till Brand Portal.

* **Tillåtslista IP-adresser i SPS om säker förhandsvisning är aktiverat**

  Om du använder Dynamic Media-**[!DNL Scene7]** (med [säker förhandsgranskning aktiverad](https://experienceleague.adobe.com/sv/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public) för ett företag) bör **[!DNL Scene7]** företagsadministratören [tillåtslista IP-adresserna för den offentliga utgången](https://experienceleague.adobe.com/sv/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service) för respektive region med hjälp av SPS-gränssnittet (**[!UICONTROL Scene7]** Publishing System).

  IP-adresserna för Egress är följande:

  | **Region** | **Utreses-IP** |
  |--- |--- |
  | NA | 130.248.160.68, 20.94.203.130 |
  | EMEA | 185.34.189.3, 51.132.146.75 |
  | APAC | 63.140.44.54 |

  Information om hur du tillåtslista någon av dessa utgående IP:n finns i [Förbered ditt konto för en säker testningstjänst](https://experienceleague.adobe.com/sv/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service).

## Bästa praxis

Kontrollera att dynamiskt videomaterial förhandsvisas, spelas upp och hämtas från Brand Portal (och delade länkar) på följande sätt:

### Separata innehavare för Dynamic Media - Scene7 och Dynamic Media - hybrid {#separate-tenants}

Om du använder både Dynamic Media - **[!DNL Scene7]**-läge och Dynamic Media - hybridläge ska du använda olika Brand Portal-klientorganisationer för Experience Manager Author-instanser som konfigurerats med Dynamic Media - **[!DNL Scene7]** och Dynamic Media - hybridläge.


![Författare och BP en till en mappning](assets/BPDynamicMedia.png)

### Samma konfigurationsinformation på Experience Manager Author-instansen och Brand Portal

Se till att konfigurationsinformationen är densamma i Brand Portal och **[!UICONTROL Experience Manager Cloud Configuration]**. Samma konfigurationsinformation omfattar följande:

* **[!UICONTROL Title]**
* **[!UICONTROL Registration ID]**
* **[!UICONTROL Video Service URL]** i **[!UICONTROL Dynamic Media - Hybrid mode]**
* **[!UICONTROL Title]**
* Autentiseringsuppgifter (**[!UICONTROL Email]** och lösenord)
* **[!UICONTROL Region]**
* **[!UICONTROL Company]** i Dynamic Media - **[!DNL Scene7]**-läge

### Tillåtslista IP-adresser för offentlig utgång för läget Dynamic Media Scene7

Om Dynamic Media **[!UICONTROL Scene7]** - med [säker förhandsgranskning aktiverad](https://experienceleague.adobe.com/sv/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public) - används för att skicka videoresurser till Brand Portal, skapar **[!UICONTROL Scene7]** en dedikerad bildserver för mellanlagringsmiljöer eller interna program. Alla förfrågningar till den här servern kontrollerar den ursprungliga IP-adressen. Om den inkommande begäran inte finns i den godkända listan över IP-adresser returneras ett felsvar.
Företagsadministratören **[!UICONTROL Scene7]** konfigurerar därför en godkänd lista över IP-adresser för företagets **[!UICONTROL Secure Testing]**-miljö via Flash-gränssnittet **[!UICONTROL SPS]** (Scene7 Publishing System). Se till att IP-adressen för utgångar för din respektive region (från följande) läggs till i den godkända listan.
Information om hur du tillåtslista någon av dessa utgående IP:n finns i [Förbered ditt konto för en säker testningstjänst](https://experienceleague.adobe.com/sv/docs/dynamic-media-classic/using/upload-publish/testing-assets-making-them-public#testing-the-secure-testing-service).
IP-adresserna för utgångar är följande:

| **Region** | **Utreses-IP** |
|--- |--- |
| NA | 130.248.160.68, 20.94.203.130 |
| EMEA | 51.132.146.75, 130.248.244.202, 130.248.244.203, 130.248.244.204, 130.248.244.210, 130.248.244.211, 130.248.244.212 |
| APAC | 63.140.44.54 |

## Konfigurera inställningar för Dynamic Media (Hybrid) {#configure-dm-hybrid-settings}

Om Experience Manager Author-instansen körs i dynamiskt medihybridläge använder du **[!UICONTROL Video]**-panelen i panelen Administrationsverktyg för att konfigurera Dynamic Media Gateway-inställningar.

>[!NOTE]
>
>[videokodningsprofilerna](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/video-profiles) publiceras inte till Brand Portal. De hämtas i stället från servern **[!UICONTROL Scene7]**. För att videokodningar ska kunna spelas upp i Brand Portal måste därför konfigurationsinformationen vara densamma som [Dynamic Media Cloud Services ([!DNL Scene7] mode)](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/config-dms7#configuring-dynamic-media-cloud-services) i Experience Manager Author-instansen.

Så här konfigurerar du dynamiska mediekonfigurationer för Brand Portal-klientorganisationer:

1. Välj Experience Manager logotyp så att du kan öppna administrationsverktygen från verktygsfältet längst upp i Brand Portal.
1. Välj **[!UICONTROL Video]**-rutan på panelen Administrationsverktyg.

   ![Dynamic Media Hybrid Config på Brand Portal](assets/DMHybrid-Video.png)

   **[!UICONTROL Edit Dynamic Media Configuration]** sida öppnas.

   ![Dynamisk hybridkonfiguration för media i Brand Portal](assets/edit-dynamic-media-config.png)

1. Ange **[!UICONTROL Registration ID]** och **[!UICONTROL Video Service URL]** (URL för DM-gateway). Se till att dessa uppgifter är desamma som de som finns i **[!UICONTROL Tools > Cloud Services]** i din Experience Manager Author-instans.
1. Välj **Spara** om du vill spara konfigurationen.

## Konfigurera inställningar för Dynamic Media Scene7 {#configure-dm-scene7-settings}

Om Experience Manager Author-instansen körs i läget Dynamic Media- **[!UICONTROL Scene7]** använder du **[!UICONTROL Dynamic Media Configuration]** i panelen Administrationsverktyg för att konfigurera serverinställningarna för **[!UICONTROL Scene7]**.

Så här konfigurerar du **[!UICONTROL Scene7]**-konfigurationer för dynamiska media på Brand Portal-klientorganisationer:

1. Välj Experience Manager logotyp så att du kan öppna administrationsverktygen från verktygsfältet längst upp i Brand Portal.

2. Välj **[!UICONTROL Dynamic Media Configuration]**-rutan på panelen Administrationsverktyg.

   ![DM [!UICONTROL Scene 7]-konfiguration på Brand Portal](assets/DMS7-Tile.png)

   **[!UICONTROL Edit Dynamic Media Configuration]** sida visas.

   ![Scene 7-konfiguration på Brand Portal](assets/S7Config.png)

3. Ange:

   * **[!UICONTROL Title]**
   * Autentiseringsuppgifter (**[!UICONTROL Email ID]** och **[!UICONTROL Password]**) för åtkomst till Scene7-servern
   * **[!UICONTROL Region]**

   Se till att dessa värden är desamma som de som finns i Experience Manager Author-instansen.

4. Välj **[!UICONTROL Connect to Dynamic Media]**.

5. Ange **[!UICONTROL Company name]** och **[!UICONTROL Save]** konfigurationen.

6. Välj **[!UICONTROL Reset]** om du vill ta bort ändringar, återställa lösenordet och återställa konfigurationen till standardtillståndet.

