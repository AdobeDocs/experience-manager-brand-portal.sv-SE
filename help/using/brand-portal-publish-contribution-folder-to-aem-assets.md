---
title: Ladda upp material och publicera Contribute-mappen från Brand Portal till Experience Manager Assets
description: Få insikt i hur du överför nya resurser och publicerar bidragsmappen från Brand Portal till Experience Manager Assets.
content-type: reference
contentOwner: Vishabh Gupta
topic-tags: brand-portal
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: 7dcf445d-97ed-4fa5-959c-c4c48e325766
source-git-commit: 10f89ded6febb1a024cbe181fa48a290d90223f0
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 0%

---

# Publish-mapp för bidrag till Experience Manager Assets {#using-asset-souring-in-bp}

Brand Portal-användare med lämplig behörighet kan överföra flera resurser, eller mappar som innehåller flera resurser, till bidragsmappen. Brand Portal-användare kan dock bara överföra resurser till mappen **NEW**. Mappen **DELAD** är avsedd för distribution av baslinjeresurser (referensinnehåll) som används av Brand Portal-användare när nya resurser skapas för bidrag.

Brand Portal-användare som har behörighet att komma åt mappen för bidrag kan utföra följande åtgärder:

* [Hämta resurskrav](#download-asset-requirements)
* [Överför nya resurser till mappen för bidrag](#uplad-new-assets-to-contribution-folder)
* [Publish-mapp för bidrag till Experience Manager Assets](#publish-contribution-folder-to-aem)

## Hämta resurskrav {#download-asset-requirements}

Brand Portal-användare får automatiskt e-post och pulsmeddelanden när en Experience Manager Assets-användare delar en avgiftsmapp. Med det här arbetsflödet kan de hämta det korta (resurskrav) dokumentet och baslinjeresurserna (referensinnehåll) från mappen **SHARED** för att förstå resurskraven.

Brand Portal-användare utför följande åtgärder för att ladda ned mediefiler:

* **Ladda ned i korthet** - Ladda ned översikten (tillgångskravsdokument) som är bifogad till mappen för bidrag. Den innehåller tillgångsrelaterad information som typ av resurser, syfte, format som stöds, maximal storlek för mediefiler med mera.
* **Hämta baslinjeresurser** - Hämta baslinjeresurser som kan användas för att förstå vilka typer av resurser som krävs. Brand Portal-användare kan använda dessa resurser som referens för att skapa nya resurser som kan bidra.

Brand Portal Dashboard visar alla befintliga mappar som är tillåtna för Brand Portal-användaren tillsammans med den nyligen delade bidragsmappen. I det här exemplet har Brand Portal-användaren bara åtkomst till den nyligen skapade mappen för bidrag. Ingen annan befintlig mapp delas med användaren.

**Så här hämtar du resurskrav:**

1. Logga in på din Brand Portal-instans.
1. Välj en mapp för bidrag från Brand Portal Dashboard.
1. Klicka på **[!UICONTROL Properties]**. Fönstret Egenskap som innehåller informationen om bidragsmappen öppnas.

   ![](assets/properties.png)

   ![](assets/download-asset-requirement2.png)

1. Klicka på alternativet **[!UICONTROL Download Brief]** om du vill hämta tillgångskravsdokumentet på den lokala datorn.

   ![](assets/download.png)

1. Gå tillbaka till Brand Portal Dashboard.
1. Klicka på mappen för bidrag för att öppna den. Du kan se två undermappar: **[!UICONTROL SHARED]** och **[!UICONTROL NEW]** i bidragsmappen. Mappen SHARED innehåller alla baslinjeresurser (referensinnehåll) som delas av administratörerna.
1. Du kan hämta mappen **[!UICONTROL SHARED]** som innehåller alla baslinjeresurser på den lokala datorn.
Du kan också öppna mappen **[!UICONTROL SHARED]** och klicka på ikonen **Hämta** för att hämta enskilda filer/mappar.

   ![](assets/download.png)

   ![](assets/download-asset-requirement5.png)

Gå igenom översikten (tillgångskravsdokument) och hänvisa till bastillgångarna för att förstå tillgångskraven. Nu kan du skapa nya resurser för bidrag och överföra dem till mappen för bidrag.

## Överför resurser till mappen för bidrag {#upload-new-assets-to-contribution-folder}

Efter att ha gått igenom resurskraven kan Brand Portal-användare skapa nya resurser för bidrag och överföra dem till mappen NEW i mappen för bidrag. En användare kan överföra flera resurser till en resursavgiftsmapp. Det går dock bara att skapa en mapp åt gången.

>[!NOTE]
>
>Brand Portal-användare kan överföra resurser (högst två gigabyte per filstorlek) till mappen NEW.
>
>Den maximala överföringsgränsen för alla Brand Portal-klientorganisationer är tio gigabyte, som kumulativt tillämpas på alla bidragsmappar.
>
>Resurserna som överförs till Brand Portal bearbetas inte för återgivningar och innehåller inte förhandsgranskningar.

>[!NOTE]
>
>Adobe rekommenderar att du frigör överföringsutrymmet efter att du har publicerat avgiftsbelagda mappar till Experience Manager Assets så att de är tillgängliga för övriga Brand Portal-användare.
>
>Om du behöver utöka din Brand Portal-klientorganisations överföringsgräns mer än **10** GB kontaktar du kundsupport och anger kraven.


**Så här överför du nya resurser:**

1. Logga in på din Brand Portal-instans.
På Brand Portal-kontrollpanelen visas alla befintliga mappar som är tillåtna för Brand Portal-användaren tillsammans med den nyligen delade bidragsmappen.

1. Markera mappen för bidrag och klicka för att öppna den. Mappen för bidrag innehåller två undermappar - **[!UICONTROL SHARED]** och **[!UICONTROL NEW]**.

1. Klicka på mappen **[!UICONTROL NEW]**.

   ![](assets/upload-new-assets4.png)

1. Klicka på **[!UICONTROL Create]** > **[!UICONTROL Files]** om du vill överföra enskilda filer eller mappar (.zip) som innehåller flera resurser.

   ![](assets/upload-new-assets5.png)

1. Bläddra och överför resurser (filer eller mappar) till mappen **[!UICONTROL NEW]**.

   ![](assets/upload-asset4.png)

När du har överfört alla resurser eller mappar till mappen NEW publicerar du mappen för bidrag till Experience Manager Assets.


## Publish-mapp för bidrag till Experience Manager Assets {#publish-contribution-folder-to-aem}

Brand Portal-användare kan publicera bidragsmappen till Experience Manager Assets utan att ha tillgång till författarinstansen i Experience Manager.

Se till att du har gått igenom resurskraven och överfört de nyskapade resurserna i mappen **NEW** i mappen för bidrag.

**Så här publicerar du en bidragsmapp:**

1. Logga in på din Brand Portal-instans.

1. Välj en mapp för bidrag från Brand Portal Dashboard.
1. Klicka på **[!UICONTROL Publish to AEM]**.

   ![](assets/export.png)

   ![](assets/publish-contribution-folder-to-aem1.png)

Ett e-post-/pulsmeddelande skickas till Brand Portal-användare och -administratörer i olika stadier av publiceringsarbetsflödet:

1. **Köad** - Ett meddelande skickas till Brand Portal-användare och Brand Portal-administratörer när ett publiceringsarbetsflöde utlöses i Brand Portal.

1. **Fullständigt** - Ett meddelande skickas till Brand Portal-användare och Brand Portal-administratörer när bidragsmappen har publicerats till Experience Manager Assets.

När de nyskapade resurserna har publicerats till Experience Manager Assets kan Brand Portal-användare ta bort dem från mappen NEW. Brand Portal-administratören kan dock ta bort resurserna från både NYTT och Delat.

När målet att skapa bidragsmappen är uppfyllt kan Brand Portal-administratören ta bort bidragsmappen och frigöra överföringsutrymmet för andra användare.

## Status för publiceringsjobb {#publishing-job-status}

Administratörer kan använda två rapporter för att visa status för resursavgiftsmappar som publicerats från Brand Portal till Experience Manager Assets.

* I Brand Portal går du till **[!UICONTROL Tools]** > **[!UICONTROL Asset Contribution Status]**. Den här rapporten visar statusen för alla publiceringsjobb i olika faser av publiceringsarbetsflödet.

  ![](assets/contribution-folder-status-v2.png)

* I Experience Manager Assets (lokal eller hanterad tjänst) går du till **[!UICONTROL Assets]** > **[!UICONTROL Jobs]**. Den här rapporten visar det slutliga tillståndet (Slutfört eller Fel) för alla publiceringsjobb.

  ![](assets/publishing-status.png)

* I Experience Manager Assets as a Cloud Service går du till **[!UICONTROL Assets]** > **[!UICONTROL Jobs]**.

  Du kan också navigera direkt till **[!UICONTROL Jobs]** från den globala navigeringen.

  Den här rapporten visar det slutliga läget (Slutfört eller Fel) för alla publiceringsjobb, inklusive import av resurser från Brand Portal till Experience Manager Assets as a Cloud Service.

  ![](assets/cloud-service-job-status.png)

<!--
>[!NOTE]
>
>Currently, no report is generated in AEM Assets as a Cloud Service for the Asset Sourcing workflow. 
-->

## Automatisk borttagning av resurser som publicerats till Experience Manager Assets från Contribute-mappen {#automatically-delete-published-assets-from-contribution-folder}

Brand Portal kör nu automatiska jobb var tolfte timme för att skanna alla Contribute-mappar och ta bort alla resurser som publicerats till AEM. Därför behöver du inte ta bort resurserna i Contribute-mappen manuellt för att mappstorleken ska hållas under [tröskelvärdet](#upload-new-assets-to-contribution-folder). Du kan också övervaka status för de borttagningsjobb som har körts automatiskt under de senaste sju dagarna. Rapporten för ett jobb innehåller följande information:

* Jobbstarttid
* Jobbsluttid
* Jobbstatus
* Totalt antal tillgångar som ingår i ett jobb
* Totalt antal resurser som tagits bort i ett jobb
* Totalt lagringsutrymme som gjorts tillgängligt som ett resultat av jobbkörningen

  ![Borttagningsrapport](assets/deletion-reports.png)

Du kan även gå vidare och visa information om varje resurs som ingår i ett borttagningsjobb. I rapporten finns information om exempelvis objektets titel, storlek, författare, borttagningsstatus och borttagningstid.

![Detaljerad borttagningsrapport](assets/deletion-reports-detailed.png)

>[!NOTE]
>
> * Kunder kan begära att Adobe kundsupport inaktiverar och återaktiverar den automatiska borttagningsjobbfunktionen eller ändrar hur ofta den ska köras.
> * Den här funktionen är tillgänglig i Experience Manager 6.5.13.0 och senare versioner.

### Visa och hämta borttagningsrapporter {#view-delete-jobs}

Så här visar och hämtar du rapporter för ett borttagningsjobb:

1. I Brand Portal går du till alternativet **[!UICONTROL Tools]**>**[!UICONTROL Asset Contribution Status]**>**[!UICONTROL Deletion Reports]**.

1. Välj ett jobb och klicka på **[!UICONTROL View]** för att visa rapporten.

   Visa information om varje resurs som ingår i ett borttagningsjobb. I rapporten finns information om exempelvis objektets titel, storlek, författare, borttagningsstatus och borttagningstid. Klicka på **[!UICONTROL Download]** om du vill hämta rapporten för jobbet i CSV-format.

   Borttagningsstatusen för en resurs i rapporten kan ha följande värden:

   * **Borttagen** - Resursen har tagits bort från Contribute-mappen.

   * **Hittades inte** - Brand Portal kunde inte hitta resursen i Contribute-mappen. Resursen har redan tagits bort från mappen manuellt.

   * **Överhoppad** - Brand Portal ignorerade borttagningen av resurser eftersom det finns en ny version tillgänglig för resursen i Contribute-mappen, som ännu inte har publicerats i Experience Manager.

   * **Misslyckades** - Brand Portal kunde inte ta bort resursen. Det finns tre nya försök att ta bort en resurs med borttagningsstatus `Failed`. Om resursen inte kan tas bort från det tredje försöket måste du ta bort resursen manuellt.

### Ta bort en rapport

I Brand Portal kan du också markera en eller flera rapporter och ta bort dem manuellt.

Ta bort en rapport:

1. Navigera till alternativet **[!UICONTROL Tools]**>**[!UICONTROL Asset Contribution Status]**>**[!UICONTROL Deletion Reports]**.

1. Markera en eller flera rapporter och klicka på **[!UICONTROL Delete]**.


