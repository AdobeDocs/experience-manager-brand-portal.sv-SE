---
title: Dela en samling
seo-title: Share a collection
description: Administratörer för Experience Manager Assets Brand Portal kan dela och ta bort delning av en samling eller en smart samling med behöriga användare. Redigerare kan bara visa och dela samlingar som de skapat, delat med dem och gemensamma samlingar.
seo-description: Experience Manager Assets Brand Portal Administrators can share and unshare a collection or a smart collection with authorized users. Editors can view and share only the collections created by them, shared with them, and public collections.
uuid: 965f39cd-1378-42c1-a58a-01e1bf825aa3
contentOwner: Vishabh Gupta
content-type: reference
topic-tags: sharing
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: f053013e-5981-419f-927e-b5bb1d47eae2
exl-id: 29b877f6-4200-4299-9b8d-81d88f4e8221
source-git-commit: 26c16668224d22f133419c13ea5fe4e24335a22f
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Dela samlingar {#share-collections}

En samling representerar en grupp relaterade resurser som lagras tillsammans i Adobe Experience Manager Assets Brand Portal. Användarna kan skapa smarta samlingar med [använda sökning eller ansiktssökning för att filtrera bort relaterade resurser](brand-portal-searching.md) och lagra dem tillsammans så att de blir lätta att komma åt och dela dem med andra Brand Portal-användare.

<!--The administrators can share and unshare a collection with the authorized Brand Portal users. Editors and viewers can view and share the collections created by them, shared with them, and public collections.-->

Samlingar delas som länkar via e-post. Alla som har åtkomst till länken för delning kan öppna samlingen, medan delade e-postmeddelanden kan vidarebefordras till alla. Dessutom [delade länkar](https://experienceleague.adobe.com/docs/experience-manager-brand-portal/using/share/brand-portal-link-share.html?lang=en) är tillfälliga och endast tillgängliga under begränsad tid. Alternativt kan användare bjudas in som permanenta medlemmar i samlingar. Det finns följande typer av användare för samlingarna:

* **Administratörer** kan dela eller ta bort delning av en samling med behöriga Brand Portal-användare. De kan bjuda in andra användare till en viss samling och definiera deras roll för den samlingen. Dessutom kan administratörer skapa offentliga samlingar.

* **Redigerare** kan skapa och dela samlingar. De kan bjuda in andra användare till en viss samling och definiera deras roll för den samlingen. Dessutom kan de dela samlingar, om de har bjudits in till samlingen som redigerare eller ägare.

* **Tittare** kan bara skapa privata samlingar. De får inte dela en samling även när de har bjudits in som ägare.

>[!NOTE]
>
>Redigerare kan inte ändra en offentlig samling till en icke-offentlig samling och har därför inte **[!UICONTROL Public Collection]** kryssruta tillgänglig i **[!UICONTROL Collection Settings]** -dialogrutan.

## Dela en samling {#share-collection}

Så här delar du en samling med behöriga Brand Portal-användare:

1. Logga in på din Brand Portal-klient. Som standard är **[!UICONTROL Files]** öppnas som innehåller alla publicerade resurser och mappar.

1. Klicka på snabbnavigeringen högst upp **[!UICONTROL Collections]**.

1. Från **[!UICONTROL Collections]** gör du något av följande:

   * Håll pekaren över den samling som du vill dela. Klicka på miniatyrbilderna för snabbåtgärder som är tillgängliga för samlingen **[!UICONTROL Settings]** -ikon.

     ![](assets/settings-icon.png)

   * Markera den samling som du vill dela. Klicka på i verktygsfältet högst upp **[!UICONTROL Settings]**.

     ![](assets/collection-console.png)

1. I **[!UICONTROL Collection Settings]** väljer du de användare som du vill dela samlingen med och väljer den roll som användaren ska ha för att matcha den globala rollen. Tilldela till exempel redigerarrollen till en global redigerare, visningsprogramrollen till ett globalt visningsprogram.

   Du kan även göra samlingen tillgänglig för alla användare, oavsett deras gruppmedlemskap och roll, genom att välja **[!UICONTROL Public Collection]** kryssruta.

   >[!NOTE]
   >
   >Användare som inte är administratörer kan dock hindras från att skapa offentliga samlingar, så att du slipper ha flera offentliga samlingar så att systemutrymmet kan sparas. Organisationer kan inaktivera **[!UICONTROL Allow public collections creation]** konfiguration från **[!UICONTROL General]** inställningar som är tillgängliga på panelen Administrationsverktyg.

   ![](assets/collection_sharingadduser.png)

   Redigerarna kan inte ändra en offentlig samling till en icke-offentlig samling och har därför inte **[!UICONTROL Public Collection]** kryssruta tillgänglig i **[!UICONTROL Collection Settings]** -dialogrutan.

   ![](assets/collection-setting-editor.png)

1. Klicka på **[!UICONTROL Add]** för att lägga till användaren och klicka sedan på **[!UICONTROL Save]**. Samlingen delas med användarna.

   >[!NOTE]
   >
   >En användares roll styr åtkomsten till resurser och mappar i en samling. Om en användare inte har åtkomst till resurser delas en tom samling med användaren. Dessutom styr en användares roll vilka åtgärder som är tillgängliga för samlingar.

## Ta bort delning av en samling {#unshare-a-collection}

Så här tar du bort delningen av en tidigare delad samling:

1. Från **[!UICONTROL Collections]** väljer du den samling du vill ta bort delningen från.

   Klicka på i verktygsfältet högst upp **[!UICONTROL Settings]**.

   ![](assets/collection_settings.png)

1. I **[!UICONTROL Collection Settings]** dialogrutan, under **[!UICONTROL Members]** klickar du på **[!UICONTROL x]** -symbol bredvid användare för att ta bort dem från listan över användare som har åtkomst till samlingen.

   ![](assets/unshare_collection.png)

1. Ett varningsmeddelande visas. Klicka **[!UICONTROL Confirm]** för att ta bort delning av samlingen.

1. Klicka **[!UICONTROL Save]** för att tillämpa ändringarna.

   När användaren har tagits bort från den delade listan tas den odelade samlingen bort från användarens **[!UICONTROL Collections]** konsol.

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
