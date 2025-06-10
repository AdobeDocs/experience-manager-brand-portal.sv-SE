---
title: Konfigurera Experience Manager Assets med Brand Portal
description: Få insikt i hur du konfigurerar Experience Manager Assets med Brand Portal.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
role: Admin
exl-id: 261c0e84-6b3d-459c-b6b9-a9af106d6943
source-git-commit: f4add370fd3242f5506e5cc4d921362e2b14141a
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---

# Konfigurera Experience Manager Assets med Brand Portal {#configure-integration}

Om du konfigurerar Adobe Experience Manager Assets med Brand Portal kan Brand Portal-användare publicera mediefiler, distribuera resurser och bidra med resurser. Med det kan Experience Manager Assets-användare publicera och distribuera material med Brand Portal-användare. Brand Portal-användare kan komma åt de delade resurserna och bidra genom att överföra nya resurser till resursavgiftsmapparna och publicera dem tillbaka till Experience Manager Assets.

Konfigurering av Experience Manager Assets med Brand Portal stöds i:

* Experience Manager Assets as a Cloud Service
* Experience Manager Assets (lokal och hanterad tjänst) 6.5 och senare

Experience Manager Assets as a Cloud Service konfigureras automatiskt med Brand Portal genom att Brand Portal aktiveras från Cloud Manager. Aktiveringsarbetsflödet skapar de nödvändiga konfigurationerna i bakänden och aktiverar Brand Portal i samma IMS-organisation som i Experience Manager Assets as a Cloud Service-instansen.

Experience Manager Assets (lokal och hanterad tjänst) konfigureras manuellt med Brand Portal med Adobe Developer Console, som anskaffar en Adobe Identity Management Services-token (IMS) för godkännande av Brand Portal-klienten.

>[!NOTE]
>
>***För Experience Manager Assets 6.5 och senare***
>
>Tidigare konfigurerade det klassiska gränssnittet Brand Portal med den äldre OAuth-gatewayen, som använder JSON Web Token-växeln (JWT) för att erhålla en IMS-token för auktorisering.
>
>Konfiguration via äldre OAuth stöds inte längre från och med 6 april 2020 och har ändrats till att konfigureras via Adobe Developer Console.


>[!TIP]
>
>***Endast för befintliga kunder (lokal och hanterad tjänst)***
>
>Äldre OAuth Gateway-konfiguration fortsätter att fungera för befintliga kunder.
>
>Om du får problem med den äldre OAuth Gateway-konfigurationen tar du bort den befintliga konfigurationen och skapar en ny konfiguration med Adobe Developer Console.

Hur du konfigurerar AEM Assets med Brand Portal varierar beroende på vilken version av AEM du har, om du konfigurerar för första gången eller om du uppgraderar de befintliga konfigurationerna:

| **AEM-version** | **Ny konfiguration** | **Uppgraderingskonfiguration** |
|---|---|---|
| **AEM Assets as a Cloud Service** | [Aktivera Brand Portal](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) | - |
| **AEM 6.5 (6.5.4.0 och senare)** | [Skapa konfiguration](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) | [Uppgraderingskonfiguration](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal#upgrade-integration-65) |
