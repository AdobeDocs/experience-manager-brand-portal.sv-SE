---
title: Dela mappar
seo-title: Share folders
description: Brand Portal stöder inte tillgångsintag, vilket innebär att resurser måste publiceras till Brand Portal från en förkonfigurerad Experience Manager Assets Author-instans. Publicerade resurser är inte tillgängliga för icke-adminanvändare av Brand Portal, såvida de inte konfigureras under konfigurationen av replikering med instansen Experience Manager, och måste delas med dem.
seo-description: Brand Portal does not support asset ingestion so assets must be published to Brand Portal from a pre-configured Experience Manager Assets Author instance. Published assets are not accessible to non-admin users of Brand Portal, unless configured while configuring replication with Experience Manager instance, and need to be shared with them.
uuid: 340d0a49-b708-4f0e-9fb8-99c824942f34
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: 2332c16f-40be-4673-8cc6-2360d5b74116
exl-id: d28cf927-60e8-437e-9cba-92f7e19020e7
source-git-commit: 4caa4263bd74b51af7504295161c421524e51f0c
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---

# Dela mappar i Brand Portal {#share-folders}

Assets måste publiceras till Brand Portal från en förkonfigurerad Experience Manager Author-instans eftersom Brand Portal inte stöder tillgångsintag.

## Arbetsflöde för mappdelning i Brand Portal {#folder-sharing-workflow-in-brand-portal}

Nedan beskrivs arbetsflödet för mappdelning och användaråtkomst:

* Som standard visas alla mappar som publiceras från Experience Manager Assets till Brand Portal endast för Brand Portal Administrator, såvida de inte är markerade som public när replikeringen konfigureras.
* Administratören använder konsolen **[!UICONTROL Folder Properties]** för att dela en mapp med selektiva användare eller grupper. Endast de användare eller grupper som mappen delas med kan se mappen när de har loggat in på Brand Portal. Mappen visas inte för andra användare.
* Administratören kan även välja att göra en mapp offentlig genom kryssrutan **[!UICONTROL Public Folder]** i konsolen **[!UICONTROL Folder Properties]**. En gemensam mapp visas för alla användare.

* Oberoende av användarroller och behörigheter kan användare som loggar in på Brand Portal se alla gemensamma mappar och de mappar som delas direkt med dem eller med en grupp som de tillhör. Privata mappar, eller mappar som delas med andra användare, visas inte för alla användare.

### Dela mappar med användargrupper på Brand Portal {#sharing-folders-with-user-groups-on-brand-portal}

Åtkomsträttigheter för resurser i en mapp är beroende av åtkomsträttigheterna för den överordnade mappen, oavsett inställningarna för de underordnade mapparna. Det här beteendet styrs av [ACL:er](https://experienceleague.adobe.com/docs/experience-manager-65/administering/security/security.html) i AEM, eftersom underordnade mappar ärver ACL:er från sina överordnade mappar. Om till exempel en mapp A innehåller mappen B som innehåller mappen C, har en eller flera användargrupper som har behörighet till mappen A även samma åtkomstbehörighet till mappen B och mappen C. Mapp B är underordnad mappen till A ärver åtkomstkontrollistan och mapp C är underordnad mappen till B ärver åtkomstkontrollistan.

På samma sätt har användargrupper (eller användare) som bara har behörighet att komma åt mappen B samma åtkomstbehörighet i mappen C men inte i mappen A. Därför bör organisationer ordna sitt innehåll så att de flesta exponerade resurserna placeras i mappen med underordnade och så att åtkomsten från underordnade till rotmappen kan begränsas.

### Publicering av offentlig mapp {#public-folder-publish}

Såvida inte alternativet **[!UICONTROL Public Folder Publish]** är markerat när du konfigurerar Brand Portal-replikering har icke-adminanvändare (som redigerare och visningsprogram) inte åtkomst till resurser som publicerats från AEM Assets till Brand Portal.

![](assets/assetbpreplication.png)

Om alternativet **[!UICONTROL Public Folder Publish]** är inaktiverat måste administratörer dela dessa resurser med icke-adminanvändare som använder delningsfunktioner.

>[!NOTE]
>
>Alternativet för att aktivera **[!UICONTROL Public Folder Publish]** finns i AEM 6.3.2.1 och senare.

## Åtkomst till delade mappar {#access-to-shared-folders}

I följande matris beskrivs åtkomsträttigheter och rättigheter att dela/ta bort delning av resurser för olika användarroller:

|               | Åtkomst till alla mappar som publicerats från AEM Assets till Brand Portal | Åtkomst till delade mappar | Dela/ta bort mapprättigheter |
|---------------|-----------|-----------|------------|
| Administratör | Ja | Ja | Ja |
| Redigerare | Nej* | Ja, endast om det delas med dem eller med den grupp de tillhör | Ja, endast för de mappar som delas med dem eller med den grupp som de tillhör |
| Visningsprogram | Nej* | Ja, endast om det delas med dem eller med den grupp de tillhör | Nej |
| Gästanvändare | Nej* | Ja, endast om det delas med dem eller med den grupp de tillhör | Nej |

>[!NOTE]
>
>Som standard är alternativet **[!UICONTROL Public Folder Publish]** inaktiverat när replikering av Brand Portal konfigureras med AEM författare. Om alternativet är aktiverat är de mappar som publiceras till Brand Portal tillgängliga för alla användare (även icke-adminanvändare) som standard.

### Åtkomst till delade mappar som inte är administratörsanvändare {#non-admin-user-access-to-shared-folders}

Användare som inte är administratörer har bara åtkomst till de mappar som delas med dem på Brand Portal. Hur de här mapparna visas på portalen när de loggar in beror dock på inställningarna för konfigurationen **[!UICONTROL Enable Folder Hierarchy]**.

**Om konfigurationen är inaktiverad**

Användare som inte är administratörer ser alla mappar som delas med dem på landningssidan när de loggar in på Brand Portal.

![](assets/disabled-folder-hierarchy1-1.png)

**Om konfigurationen är aktiverad**

Användare som inte är administratörer kan se mappträdet (från rotmappen) och de delade mapparna i sina respektive överordnade mappar när de loggar in på Brand Portal.

De här överordnade mapparna är de virtuella mapparna och inga åtgärder kan utföras på dem. Du känner igen dessa virtuella mappar med en låsikon.

Inga åtgärder visas när du hovrar eller markerar dem i **[!UICONTROL Card View]**, till skillnad från delade mappar. Knappen **[!UICONTROL Overview]** visas när du väljer en virtuell mapp i **[!UICONTROL Column View]** och **[!UICONTROL List View]**.

>[!NOTE]
>
>Observera att standardminiatyrbilden för de virtuella mapparna är miniatyrbilden för den första delade mappen.

![](assets/enabled-hierarchy1-1.png) ![](assets/hierarchy1-nonadmin-1.png) ![](assets/hierarchy-nonadmin-1.png) ![](assets/hierarchy2-nonadmin-1.png)

## Dela mappar {#how-to-share-folders}

Så här delar du en mapp med användare på Brand Portal:

1. Klicka på övertäckningsikonen till vänster och välj **[!UICONTROL Navigation]**.

   ![](assets/selectorrail.png)

1. Välj **[!UICONTROL Files]** i sidofältet till vänster.

   ![](assets/access_files.png)

1. I Brand Portal-gränssnittet väljer du den mapp du vill dela.

   ![](assets/share-folders.png)

1. Välj **[!UICONTROL Share]** i verktygsfältet högst upp.

   ![](assets/share_icon.png)

   Konsolen [!UICONTROL Folder Properties] visas.

   ![](assets/folder_properties.png)

1. I konsolen **[!UICONTROL Folder Properties]** anger du mapptiteln i fältet **[!UICONTROL Folder Title]** om du inte vill att standardnamnet ska visas för användarna.
1. I listan **[!UICONTROL Add User]** markerar du de användare eller grupper som du vill dela mappen med och klickar på **[!UICONTROL Add]**.
Om du bara vill dela mappen med gästanvändare och inga andra användare väljer du **[!UICONTROL Anonymous Users]** i listrutan **[!UICONTROL Members]**.

   ![](assets/only-anonymous.png)

   >[!NOTE]
   >
   >Om du vill göra mappen tillgänglig för alla användare oavsett deras gruppmedlemskap och roll markerar du kryssrutan **[!UICONTROL Public Folder]**.

1. Om det behövs klickar du på **[!UICONTROL Change Thumbnail]** för att ändra miniatyrbilden för mappen.
1. Klicka på **[!UICONTROL Save]**.

1. Om du vill komma åt den delade mappen loggar du in på Brand Portal med inloggningsuppgifterna för den användare som du delade mappen med. Granska den delade mappen i gränssnittet.

## Dela inte mappar {#unshare-the-folders}

Så här tar du bort delningen av en tidigare delad mapp:

1. I Brand Portal-gränssnittet väljer du den mapp du vill ta bort delningen av.

   ![](assets/share-folders-1.png)

1. Klicka på **[!UICONTROL Share]** i verktygsfältet överst.
1. Klicka på symbolen **[!UICONTROL x]** bredvid en användare i **[!UICONTROL Folder Properties]**-konsolen under **[!UICONTROL Members]** för att ta bort dem från listan över användare som du delade mappen med.

   ![](assets/folder_propertiesunshare.png)

1. Klicka på **[!UICONTROL Confirm]** i varningsmeddelanderutan för att bekräfta att du inte vill dela.
Klicka på **[!UICONTROL Save]**.

1. Logga in på Brand Portal med inloggningsuppgifterna för den användare du tog bort från den delade listan. Mappen är inte längre tillgänglig i Brand Portal-gränssnittet för användaren.
