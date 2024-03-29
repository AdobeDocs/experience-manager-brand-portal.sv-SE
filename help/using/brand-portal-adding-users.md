---
title: Hantera användare, grupper och användarroller
seo-title: Manage users, groups, and user roles
description: Administratörer kan använda Adobe Admin Console för att skapa Brand Portal-användare och produktprofiler och hantera sina roller med Brand Portal användargränssnitt. Det här privilegiet är inte tillgängligt för granskare och redigerare.
seo-description: Administrators can use Adobe Admin Console to create Brand Portal users and product profiles, and manage their roles using the Brand Portal user interface. This privilege is not available to Viewers and Editors.
uuid: 0dc1867c-6d1b-4d0d-a25e-0df207c269b8
content-type: reference
topic-tags: administration
products: SG_EXPERIENCEMANAGER/Brand_Portal
discoiquuid: ba468e80-d077-4af6-b782-238fc557e22b
role: Admin
exl-id: 35b1fd75-f9e4-4145-80bd-84de091f8b2b
source-git-commit: 955cd8afe939ff47e9f08f312505e230e2f38495
workflow-type: tm+mt
source-wordcount: '2011'
ht-degree: 0%

---

# Hantera användare, grupper och användarroller {#manage-users-groups-and-user-roles}

Administratörer kan använda Adobe Admin Console för att skapa Experience Manager Assets Brand Portal-användare och -produktprofiler och hantera sina roller med Brand Portal användargränssnitt. Det här privilegiet är inte tillgängligt för granskare och redigerare.

I [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview)kan du visa alla produkter som är kopplade till din organisation. En produkt kan vara en valfri Experience Cloud-lösning, som Adobe Analytics, Adobe Target eller Experience Manager Assets Brand Portal. Du måste välja AEM Brand Portal och skapa produktprofiler.

<!--
Comment Type: draft

<note type="note">
<p>Product Profiles (formerly known as product configurations*). </p>
<p>* The nomenclature has changed from product configurations to product profiles in the new Adobe Admin Console.</p>
</note>
-->
![](assets/create-user-group.png)

Dessa produktprofiler synkroniseras med Brand Portal användargränssnitt var 8:e timme och visas som grupper i Brand Portal. När du har lagt till användare och skapat produktprofiler, och lagt till användare i produktprofilerna, kan du tilldela roller till användare och grupper i Brand Portal.

>[!NOTE]
>
>Skapa grupper i Brand Portal från Adobe [!UICONTROL Admin Console], använda **[!UICONTROL Products > Product Profiles]**, i stället för **[!UICONTROL User page > User Groups]**. Produktprofiler i Adobe [!UICONTROL Admin Console] används för att skapa grupper i Brand Portal.

## Lägg till en användare {#add-a-user}

Om du är produktadministratör använder du Adobe [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) för att skapa användare och tilldela dem till produktprofiler (*kallades tidigare produktkonfigurationer*) som visas som grupper i Brand Portal. Du kan använda grupper för att utföra gruppåtgärder som rollhantering och resursdelning.

>[!NOTE]
>
>Nya användare som inte har tillgång till Brand Portal kan begära åtkomst från inloggningsskärmen i Brand Portal. Mer information finns i [Begär åtkomst till Brand Portal](../using/brand-portal.md#request-access-to-brand-portal). När du har fått meddelanden om åtkomstbegäran i meddelandefältet klickar du på meddelandet och sedan på **[!UICONTROL Grant Access]**. Du kan även följa länken i det e-postmeddelande om åtkomstbegäran som har tagits emot. Därefter lägger du till en användare via [Adobe [!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview)följer steg 4-7 i proceduren nedan.

>[!NOTE]
>
>Du kan logga in på [Adobe [!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direkt eller från Brand Portal. Om du loggar in direkt följer du steg 4-7 i proceduren nedan för att lägga till en användare.

1. Klicka på Adobe-logotypen AEM verktygsfältet överst för att öppna administrationsverktygen.

   ![AEM logotyp](assets/aemlogo.png)

1. På panelen Administrationsverktyg klickar du på **[!UICONTROL Users]**.

   ![Panelen Administratörsverktyg](assets/admin-tools-panel-5.png)

1. I [!UICONTROL User Roles] klickar du på **[!UICONTROL Management]** tabbtangenten och sedan klicka **[!UICONTROL Launch Admin Console]**.

   ![Användarroller att starta Admin Console](assets/launch_admin_console.png)

1. Gör något av följande i Admin Console för att skapa en ny användare:

   * Klicka på i verktygsfältet högst upp **[!UICONTROL Overview]**. I [!UICONTROL Overview] sida, klicka **[!UICONTROL Assign Users]** från Brand Portal produktkort.

   ![Översikt över Admin Console](assets/admin_console_overviewadduser.png)

   * Klicka på i verktygsfältet högst upp **[!UICONTROL Users]**. I [!UICONTROL Users] sida, [!UICONTROL Users] till vänster är markerat som standard. Klicka på **[!UICONTROL Add User]**.

   ![Admin Console Lägg till användare](assets/admin_console_adduseruserpage.png)

1. I dialogrutan Lägg till användare skriver du e-post-ID:t för den användare som du vill lägga till eller väljer användaren i listan med förslag som visas när du skriver.

   ![Lägg till användare i Brand Portal](assets/add_user_to_aem_bp.png)

1. Tilldela användaren minst en produktprofil (tidigare produktkonfigurationer) så att användaren kan komma åt Brand Portal. Välj lämplig produktprofil på menyn **[!UICONTROL Please select a profile for this product]** fält.
1. Klicka på **[!UICONTROL Save]**. Ett välkomstmeddelande skickas till den nya användaren. Den inbjudna användaren kan klicka på länken i välkomstmeddelandet för att få åtkomst till Brand Portal. Användaren kan logga in med e-post-ID ([!UICONTROL Adobe ID], [!UICONTROL Enterprise ID], eller [!UICONTROL Fedrated ID]) som konfigurerats i Admin Console. Mer information finns i [Första gången du loggar in](../using/brand-portal-onboarding.md).

   >[!NOTE]
   >
   >Om en användare inte kan logga in på Brand Portal bör organisationens administratör besöka Adobe [!UICONTROL Admin Console] och kontrollera om användaren finns och har lagts till i minst en produktprofil.

   Mer information om hur du tilldelar administratörsbehörighet till användaren finns i [Ge användarna administratörsbehörighet](../using/brand-portal-adding-users.md#provideadministratorprivilegestousers).

## Lägg till en produktprofil {#add-a-product-profile}

Produktprofiler (kallades tidigare produktkonfigurationer) i [!UICONTROL Admin Console] används för att skapa grupper i Brand Portal så att du kan utföra gruppåtgärder som rollhantering och resursdelning i Brand Portal. **Brand Portal** är standardproduktprofilen tillgänglig, kan du skapa fler produktprofiler och lägga till användare i de nya produktprofilerna.

>[!NOTE]
>
>Du kan logga in på [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direkt eller från Brand Portal. Om du loggar in på [!UICONTROL Admin Console] följer du steg 4-7 nedan för att lägga till en produktprofil.

1. Klicka på Adobe-logotypen AEM verktygsfältet överst för att öppna administrationsverktygen.

   ![AEM](assets/aemlogo.png)

1. På panelen Administrationsverktyg klickar du på **[!UICONTROL Users]**.

   ![Panelen Administratörsverktyg](assets/admin-tools-panel-6.png)

1. I [!UICONTROL User Roles] klickar du på **[!UICONTROL Management]** tabbtangenten och sedan klicka **[!UICONTROL Launch Admin Console]**.

   ![Starta Admin Console](assets/launch_admin_console.png)

1. Klicka på i verktygsfältet högst upp **[!UICONTROL Products]**.
1. I [!UICONTROL Products] sida, [!UICONTROL Product Profiles] är markerat som standard. Klicka på **[!UICONTROL New Profile]**.

   ![Lägg till ny produktprofil](assets/admin_console_addproductprofile.png)

1. I [!UICONTROL Create a New Profile] ska du ange profilnamn, visningsnamn, profilbeskrivning och välja om du vill meddela användare via e-post när de läggs till i eller tas bort från profilen.

   ![Skapa produktprofil](assets/admin_console_addaproductprofilecreatenewprofile.png)

1. Klicka på **[!UICONTROL Done]**. Produktkonfigurationsgruppen, till exempel **[!UICONTROL Sales group]**, läggs till i Brand Portal.

   ![Produktprofiler](assets/admin_console_productprofileadded.png)

## Lägga till användare i en produktprofil {#add-users-to-a-product-profile}

Om du vill lägga till användare i en Brand Portal-grupp lägger du till dem i motsvarande produktprofil (tidigare produktkonfigurationer) i [!UICONTROL Admin Console]. Du kan lägga till användare individuellt eller gruppvis.

>[!NOTE]
>
>Du kan logga in på [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direkt eller från Brand Portal. Om du loggar in direkt på Admin Console följer du steg 4-7 i proceduren nedan för att lägga till användare i en produktprofil.

1. Klicka på Experience Manager-logotypen i verktygsfältet överst för att öppna administrationsverktygen.

   ![AEM](assets/aemlogo.png)

1. På panelen Administrationsverktyg klickar du på **[!UICONTROL Users]**.

   ![Panelen Administratörsverktyg](assets/admin-tools-panel-7.png)

1. I [!UICONTROL User Roles] klickar du på **[!UICONTROL Management]** tabbtangenten och sedan klicka **[!UICONTROL Launch Admin Console]**.

   ![Starta [!DNL Admin Console]](assets/launch_admin_console.png)

1. Klicka på i verktygsfältet högst upp **[!UICONTROL Products]**.
1. I [!UICONTROL Products] sida, [!UICONTROL Product Profiles] är markerat som standard. Öppna produktprofilen som du vill lägga till en användare i, till exempel [!UICONTROL Sales group].

   ![Produktprofiler](assets/admin_console_productprofileadded.png)

1. Så här lägger du till enskilda användare i produktprofilen:

   * Klicka på **[!UICONTROL Add User]**.

   ![Grupp att mappa produktprofil i Brand Portal](assets/admin_console_productprofilesalesgroup.png)

   * I [!UICONTROL Add User to Sales group] skriver du e-post-ID:t för användaren som du vill lägga till eller väljer användaren i listan med förslag som visas när du skriver.

   ![Lägga till användare i en grupp](assets/admin_console_addusertosalesgroup.png)

   * Klicka på **[!UICONTROL Save]**.



1. Så här lägger du till massanvändare i produktprofilen:

   * Välj **[!UICONTROL ellipsis (...) > Add users by CSV]**.

   ![Lägga till flera användare samtidigt](assets/admin_console_addbulkusers.png)

   * I **[!UICONTROL Add Users by CSV]** hämtar du en CSV-mall eller drar och släpper en CSV-fil.

   ![Lägga till användare via csv](assets/admin_console_addbulkuserscsv.png)

   * Klicka på **[!UICONTROL Upload]**.
   Om du har lagt till användare i standardproduktprofilen, dvs. Brand Portal, skickas ett välkomstmeddelande till e-post-ID:t för de användare som du har lagt till. De inbjudna användarna kan komma åt Brand Portal genom att klicka på länken i välkomstmeddelandet och logga in med en [!UICONTROL Adobe ID]. Mer information finns i [Första gången du loggar in](../using/brand-portal-onboarding.md).

   Användare som läggs till i en anpassad eller ny produktprofil får inga e-postmeddelanden.

## Ge användarna administratörsbehörighet {#provide-administrator-privileges-to-users}

Du kan ge systemadministratören eller produktadministratörsbehörighet till en Brand Portal-användare. Ge inte andra administrativa rättigheter i [!UICONTROL Admin Console], t.ex. administratör av produktprofiler, administratör av användargrupper och supportadministratör. Mer information om de här rollerna finns i [Administrativa roller](https://helpx.adobe.com/enterprise/using/admin-roles.html).

>[!NOTE]
>
>Du kan logga in på [[!UICONTROL Admin Console]](https://adminconsole.adobe.com/enterprise/overview) direkt eller från Brand Portal. Om du loggar in på [!UICONTROL Admin Console] följer du steg 4-8 nedan för att lägga till en användare i en produktprofil.

1. Klicka på Adobe-logotypen AEM verktygsfältet överst för att öppna administrationsverktygen.

   ![AEMLogo](assets/aemlogo.png)

1. På panelen Administrationsverktyg klickar du på **[!UICONTROL Users]**.

   ![Panelen Administratörsverktyg](assets/admin-tools-panel-8.png)

1. I [!UICONTROL User Roles] klickar du på **[!UICONTROL Management]** tabbtangenten och sedan klicka **[!UICONTROL Launch Admin Console]**.

   ![Starta Admin Console](assets/launch_admin_console.png)

1. Klicka på i verktygsfältet högst upp **[!UICONTROL Users]**.
1. I [!UICONTROL Users] sida, [!UICONTROL Users] till vänster är markerat som standard. Klicka på användarnamnet för den användare som du vill ge administratörsbehörighet till.

   ![Lägg till användare i Admin Console](assets/admin_console_adduseruserpage.png)

1. På sidan för användarprofiler hittar du **[!UICONTROL Administrative Rights]** längst ned och välj **[!UICONTROL ellipsis (...) > Edit admin rights]**.
   ![Administratörsrättigheter i Admin Console](assets/admin_console_editadminrights.png)

1. I [!UICONTROL Edit Admin] väljer du Systemadministratör eller Produktadministratör.

   ![Redigera administratörsrättigheter i Admin Console](assets/admin_console_editadminrightsselection.png)

   >[!NOTE]
   >
   >Brand Portal har endast stöd för systemadministratörs- och produktadministratörsroller.
   >
   >Adobe rekommenderar att du undviker att använda systemadministratörsrollen eftersom den ger administratörsbehörighet för hela organisationen för alla produkter i en organisation. En systemadministratör för en organisation som inkluderar tre molnprodukter för marknadsföring har till exempel hela uppsättningen behörigheter för alla tre produkterna. Endast en systemadministratör kan konfigurera Experience Manager Assets så att resurser kan publiceras från Experience Manager Assets till Brand Portal. Mer information finns i [Konfigurera Experience Manager Assets med Brand Portal](../using/configure-aem-assets-with-brand-portal.md).
   >
   >Produktadministratörsrollen ger däremot administratörsbehörighet för en viss produkt. Om du vill använda en mer detaljerad åtkomstkontroll i Brand Portal använder du produktadministratörsrollen och väljer produkten som Brand Portal.

   >[!NOTE]
   >
   >Brand Portal stöder inte administratörsbehörighet för produktprofiler (tidigare konfigurationsadministratör). Undvik att tilldela en användare administratörsrättigheter för produktprofiler.

1. Granska valet av administratörstyp och klicka på **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Om du vill återkalla administratörsbehörighet för en användare gör du lämpliga ändringar i **[!UICONTROL Edit Admin]** sida och klicka sedan på **[!UICONTROL Save]**.


## Hantera användarroller {#manage-user-roles}

En administratör kan ändra roller för användare i Brand Portal.

Förutom administratörsrollen har Brand Portal stöd för följande roller:

* [!UICONTROL Viewer]: Användare med den här rollen kan visa filer och mappar som en administratör delar med sig. Visningsprogram kan även söka efter och hämta resurser. Visningsprogram kan dock inte dela innehåll (filer, mappar, [!UICONTROL collections]) med andra användare.
* [!UICONTROL Editor]: Användare med den här rollen har alla behörigheter som finns för ett visningsprogram. Dessutom kan redigerare dela innehåll (mappar, [!UICONTROL collections], länkar) med andra användare.

1. Klicka på Adobe-logotypen AEM verktygsfältet överst för att öppna administrationsverktygen.

   ![AEMLogo](assets/aemlogo.png)

1. På panelen Administrationsverktyg klickar du på **[!UICONTROL Users]**.

   ![Panelen Administratörsverktyg](assets/admin-tools-panel-9.png)

1. I [!UICONTROL User Roles] sidan, [!UICONTROL Users] -fliken är markerad som standard. För den användare vars roll du vill ändra väljer du **[!UICONTROL Editor]** eller **[!UICONTROL Viewer]** från **[!UICONTROL Role]** nedrullningsbar meny.

   ![Ändra användarroller](assets/modify_user_role.png)

   Om du vill ändra rollen för flera användare samtidigt, markerar du användarna och väljer rätt roll i dialogrutan **[!UICONTROL Role]** nedrullningsbar meny.

   >[!NOTE]
   >
   >The [!UICONTROL Role] listan för administratörsanvändare är inaktiverad. Du kan inte välja dessa användare för att ändra deras roller.


   >[!NOTE]
   >
   >Användarrollen är också inaktiverad om användaren är medlem i gruppen Redigerare. Om du vill återkalla redigeringsbehörighet för användaren tar du antingen bort användaren från gruppen Redigeraren eller ändrar rollen för hela gruppen till Visningsprogram.


1. Klicka på **[!UICONTROL Save]**. Rollen ändras för motsvarande användare. Om du har valt flera användare ändras rollerna för alla användare samtidigt.

   >[!NOTE]
   >
   >Ändringar i användarbehörigheter återspeglas i **[!UICONTROL User Roles]** visas först när användarna har loggat in på Brand Portal igen.

## Hantera grupproller och behörigheter {#manage-group-roles-and-privileges}

En administratör kan associera specifika behörigheter med en [grupp](../using/brand-portal-adding-users.md#main-pars-title-278567577) av användare i Brand Portal. The **[!UICONTROL Groups]** på **[!UICONTROL User Roles]** kan administratörer göra följande:

* Tilldela roller till användargrupper
* Begränsa användargrupper så att de hämtar originalåtergivningar av bildfiler (.jpeg, .tiff, .png, .bmp, .gif, .pjpeg, x-portable-anymap, x-portable-bitmap, x-portable-graymap, x-portable-pixmap, x-rgb, x-bitmap, x-pixmap, x-icon, image/image photoshop, image/x-photoshop, .psd, image/vnd.adobe.photoshop) from Brand Portal.

>[!NOTE]
>
>För de resurser som delas som länken gäller behörigheten att komma åt de ursprungliga återgivningarna av bildfiler baserat på behörigheten för den användare som delar resurserna.

Så här ändrar du rollen och åtkomsträttigheten till de ursprungliga återgivningarna för specifika gruppmedlemmar:

1. På **[!UICONTROL User Roles]** sida, navigera till **[!UICONTROL Groups]** -fliken.
1. Markera de grupper som du vill ändra roller för.
1. Välj lämplig roll från **[!UICONTROL Role]** nedrullningsbar lista.

   Om du vill att medlemmarna i en grupp ska kunna få tillgång till de ursprungliga återgivningarna av bildfiler (.jpeg, .tiff, .png, .bmp, .gif, .pjpeg, x-portable-anymap, x-portable-bitmap, x-portable-graymap, x-portable-pixmap, x-rgb, x-bitmap, x-pixmap ikon, image/photoshop, image/x-photoshop, .psd, image/vnd.adobe.photoshop) som de hämtar från portalen eller via en delad länk, **[!UICONTROL Access to  Original]** för den gruppen. Som standard **[!UICONTROL Access to Original]** är markerat för alla användare. Om du vill förhindra att en användargrupp får åtkomst till de ursprungliga återgivningarna avmarkerar du det alternativ som motsvarar den gruppen.

   ![Användargruppsroller](assets/access-original-rend.png)

   >[!NOTE]
   >
   >Om en användare läggs till i flera grupper och en av dessa grupper har begränsningar, gäller begränsningarna den användaren.
   >
   >Begränsningar för åtkomst till ursprungliga återgivningar av bildfiler gäller inte för administratörer även om de är medlemmar i begränsade grupper.


1. Klicka på **[!UICONTROL Save]**. Rollen ändras för motsvarande grupper.

   >[!NOTE]
   >
   >Associationen användare-till-grupp, eller gruppmedlemskapet för en användare, synkroniseras med Brand Portal var 8:e timme. Ändringar i användar- eller grupproller börjar gälla efter att nästa synkroniseringsjobb har körts.
