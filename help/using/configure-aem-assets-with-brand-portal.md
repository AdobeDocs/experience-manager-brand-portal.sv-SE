---
title: Konfigurera Experience Manager Assets med Brand Portal
seo-title: Configure Experience Manager Assets with Brand Portal
description: Få insikt i hur du konfigurerar Experience Manager Assets med Brand Portal.
seo-description: Get an insight into configuring Experience Manager Assets with Brand Portal.
uuid: null
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: null
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: 454b05c05359a2068cc29124f826d5bd25a1bad1
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 1%

---

# Konfigurera Experience Manager Assets med Brand Portal {#configure-integration}

Om du konfigurerar Adobe Experience Manager Assets med Brand Portal kan Brand Portal-användare publicera mediefiler, distribuera resurser och bidra med resurser. Med det kan Experience Manager Assets-användare publicera och distribuera mediefiler med Brand Portal-användare. Brand Portal-användare kan komma åt de delade resurserna och bidra genom att överföra nya resurser till resursavgiftsmapparna och publicera dem tillbaka till Experience Manager Assets.

Konfigurering av Experience Manager Assets med Brand Portal stöds i:

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets (lokal och hanterad tjänst) 6.5 och senare

Experience Manager Assets as a Cloud Service konfigureras automatiskt med Brand Portal genom att Brand Portal aktiveras från Cloud Manager. Aktiveringsarbetsflödet skapar de nödvändiga konfigurationerna i bakänden och aktiverar Brand Portal i samma IMS-organisation som i Experience Manager Assets as a Cloud Service-instansen.

Experience Manager Assets (lokal och hanterad tjänst) konfigureras manuellt med Brand Portal med Adobe Developer Console, som anskaffar en IMS-token (Adobe Identity Management Services) för godkännande av Brand Portal-klienten.

>[!NOTE]
>
>***För Experience Manager Assets 6.5 och senare***
>
>Tidigare konfigurerades Brand Portal i det klassiska gränssnittet via äldre OAuth Gateway, som använder JSON Web token-utbyte för att erhålla en IMS-token för auktorisering.
>
>Konfiguration via äldre OAuth stöds inte längre från 6 april 2020 och har ändrats till att konfigureras via Adobe Developer Console.


>[!TIP]
>
>***Endast för befintliga kunder (lokal och hanterad tjänst)***
>
>Äldre OAuth Gateway-konfiguration fortsätter att fungera för befintliga kunder.
>
>Om du får problem med äldre OAuth Gateway-konfiguration tar du bort den befintliga konfigurationen och skapar en ny konfiguration via Adobe Developer Console.

Hur du konfigurerar AEM Assets med Brand Portal varierar beroende på vilken version du har av AEM, om du konfigurerar för första gången eller om du uppgraderar de befintliga konfigurationerna:

| **AEM version** | **Ny konfiguration** | **Uppgraderingskonfiguration** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Aktivera Brand Portal](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) | - |
| **AEM 6.5 (6.5.4.0 och senare)** | [Skapa konfiguration](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html) | [Uppgraderingskonfiguration](https://experienceleague.adobe.com/docs/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
