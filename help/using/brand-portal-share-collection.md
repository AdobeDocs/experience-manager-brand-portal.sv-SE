---
title: Dela en samling
description: Läs om hur Experience Manager Assets Brand Portal-administratörer kan dela och ta bort delning av en samling eller en smart samling med behöriga användare. Redigerare kan bara visa och dela samlingar som de skapat, delat med dem och gemensamma samlingar.
contentOwner: Vishabh Gupta
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
exl-id: 29b877f6-4200-4299-9b8d-81d88f4e8221
source-git-commit: 32a67abf466dd3bf635b851b02377ed23591915e
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# Dela samlingar {#share-collections}

En samling representerar en grupp relaterade resurser som lagras tillsammans i Adobe Experience Manager Assets Brand Portal. Användarna kan skapa smarta samlingar genom att [använda sökning eller ansiktssökning för att filtrera bort relaterade resurser](brand-portal-searching.md) och lagra dem tillsammans för enkel åtkomst och dela dem ytterligare med andra Brand Portal-användare.

<!--The administrators can share and unshare a collection with the authorized Brand Portal users. Editors and viewers can view and share the collections created by them, shared with them, and public collections.-->

Samlingar delas som länkar via e-post. Alla som har tillgång till länken för delning kan öppna samlingen. Delade e-postmeddelanden kan dock vidarebefordras till alla. Dessutom är [delade länkar](https://experienceleague.adobe.com/sv/docs/experience-manager-brand-portal/using/share/brand-portal-link-share) temporära och tillgängliga endast under en begränsad tid. Alternativt kan användare bjudas in som permanenta medlemmar i samlingar. Det finns följande typer av användare för samlingarna:

* **Administratörer** kan dela eller ta bort delning av en samling med behöriga Brand Portal-användare. De kan bjuda in andra användare till en viss samling och definiera deras roll i samlingen. Dessutom kan administratörer skapa offentliga samlingar.

* **Redigerare** kan skapa och dela samlingar. De kan bjuda in andra användare till en viss samling och definiera deras roll i samlingen. Dessutom kan de dela samlingar, om de har bjudits in till samlingen som redigerare eller ägare.

* **Visare** kan bara skapa privata samlingar. De kan inte dela en samling även när de har bjudits in som ägare.

>[!NOTE]
>
>Redigerare kan inte ändra en offentlig samling till en icke-offentlig samling och har därför inte kryssrutan **[!UICONTROL Public Collection]** tillgänglig i dialogrutan **[!UICONTROL Collection Settings]**.

## Dela en samling {#share-collection}

Så här delar du en samling med behöriga Brand Portal-användare:

1. Logga in på din Brand Portal-klient. Som standard öppnas vyn **[!UICONTROL Files]** som innehåller alla publicerade resurser och mappar.

1. Klicka på **[!UICONTROL Collections]** i snabbnavigeringen högst upp.

1. Gör något av följande från konsolen **[!UICONTROL Collections]**:

   * Håll pekaren över den samling som du vill dela. Klicka på ikonen **[!UICONTROL Settings]** i miniatyrbilderna för snabbåtgärder som är tillgängliga för samlingen.

     ![](assets/settings-icon.png)

   * Markera den samling som du vill dela. Klicka på **[!UICONTROL Settings]** i verktygsfältet överst.

     ![](assets/collection-console.png)

1. I dialogrutan **[!UICONTROL Collection Settings]** väljer du de användare som du vill dela samlingen med och väljer rollen som användaren ska matcha sin globala roll. Tilldela till exempel redigerarrollen till en global redigerare, visningsprogramrollen till ett globalt visningsprogram.

   Du kan även göra samlingen tillgänglig för alla användare oavsett deras gruppmedlemskap och roll genom att markera kryssrutan **[!UICONTROL Public Collection]**.

   >[!NOTE]
   >
   >Användare som inte är administratörer kan dock hindras från att skapa offentliga samlingar, så att du slipper ha flera offentliga samlingar så att systemutrymmet kan sparas. Organisationer kan inaktivera **[!UICONTROL Allow public collections creation]**-konfigurationen från **[!UICONTROL General]**-inställningarna som är tillgängliga på panelen Administrationsverktyg.

   ![](assets/collection_sharingadduser.png)

   Redigerarna kan inte ändra en offentlig samling till en icke-offentlig samling och har därför ingen kryssruta av typen **[!UICONTROL Public Collection]** i dialogrutan **[!UICONTROL Collection Settings]**.

   ![](assets/collection-setting-editor.png)

1. Klicka på knappen **[!UICONTROL Add]** för att lägga till användaren och klicka sedan på **[!UICONTROL Save]**. Samlingen delas med användarna.

   >[!NOTE]
   >
   >En användares roll styr åtkomsten till resurser och mappar i en samling. Om en användare inte har åtkomst till resurser delas en tom samling med användaren. Dessutom styr en användares roll vilka åtgärder som är tillgängliga för samlingar.

## Ta bort delning av en samling {#unshare-a-collection}

Så här tar du bort delningen av en tidigare delad samling:

1. Välj den samling du vill ta bort delningen från konsolen **[!UICONTROL Collections]**.

   Klicka på **[!UICONTROL Settings]** i verktygsfältet överst.

   ![](assets/collection_settings.png)

1. I dialogrutan **[!UICONTROL Collection Settings]**, under avsnittet **[!UICONTROL Members]**, klickar du på symbolen **[!UICONTROL x]** bredvid användare för att ta bort dem från listan över användare som har åtkomst till samlingen.

   ![](assets/unshare_collection.png)

1. Ett varningsmeddelande visas. Klicka på **[!UICONTROL Confirm]** om du vill ta bort delningen av samlingen.

1. Klicka på **[!UICONTROL Save]** för att tillämpa ändringarna.

   När användaren har tagits bort från den delade listan tas den odelade samlingen bort från användarens **[!UICONTROL Collections]**-konsol.

<!--
1. Click the overlay icon on the left, and choose **[!UICONTROL Navigation]**.

   ![](assets/contenttree-1.png)

1. From the siderail on the left, click **[!UICONTROL Collections]**.

   ![](assets/access_collections.png)

1. From the **[!UICONTROL Collections]** console, do one of the following:

    * Hover the pointer over the collection you want to share. From the quick action thumbnails available for the collection, click the **[!UICONTROL Settings]** icon.

   ![](assets/settings_thumbnail.png)

    * Select the collection you want to share. From the toolbar at the top, click **[!UICONTROL Settings]**.
    
   ![](assets/collection-sharing.png)

1. In the [!UICONTROL Collection Settings] dialog box, select the users or groups with whom you want to share the collection and select the role for a user or a group to match their global role. For example, assign the Editor role to a global editor, the Viewer role to a global viewer.

   Alternatively, to make the collection available to all users irrespective of their group membership and role, make it public by selecting the **[!UICONTROL Public Collection]** check-box.

   >[!NOTE]
   >
   >However, non-admin users can be restricted from creating public collections, to avoid having numerous public collections so that system space can be saved. Organizations can disable the **[!UICONTROL Allow public collections creation]** configuration from [!UICONTROL General] settings available in admin tools panel.

   ![](assets/collection_sharingadduser.png)

   Editors cannot change a public collection to a non-public collection and, therefore, do not have **[!UICONTROL Public Collection]** check-box available in **[!UICONTROL Collection Settings]** dialog.

   ![](assets/collection-setting-editor.png)

1. Select **[!UICONTROL Add]**, and then **[!UICONTROL Save]**. The collection is shared with the chosen users.

   >[!NOTE]
   >
   >A user's role governs access to the assets and folders inside a collection. If a user does not have access to assets, an empty collection is shared with the user. Also, a user's role governs the actions available for collections.

## Unshare a collection {#unshare-a-collection}

To unshare a previously shared collection, do the following:

1. From the **[!UICONTROL Collections]** console, select the collection you want to unshare.

   In the toolbar, click **[!UICONTROL Settings]**.

   ![](assets/collection_settings.png)

1. On the **[!UICONTROL Collection Settings]** dialog box, under **[!UICONTROL Members]**, click the **[!UICONTROL x]** symbol next to users or groups to remove them from the list of users you shared the collection with.

   ![](assets/unshare_collection.png)

1. In the warning message box, click **[!UICONTROL Confirm]** to confirm unshare.

   Click **[!UICONTROL Save]**.

1. Log in to Brand Portal with the credentials of the user you removed from the shared list. The collection is removed from the **[!UICONTROL Collections]** console.
-->
