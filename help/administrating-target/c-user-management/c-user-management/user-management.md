---
keywords: add user;manage user;user permissions
description: Voeg gebruikers toe aan Adobe Target en beheer hun machtigingen in de Adobe Admin Console.
title: Gebruikers
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 1c5fd1062da5f90f24720fc3deb67f7f3b05aee9
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# Gebruikers{#users}

Voeg gebruikers toe en beheer hun toestemmingen in [!DNL Adobe Admin Console].

>[!NOTE]
>
>[!UICONTROL Properties] en  [!UICONTROL Permissions] functionaliteit is beschikbaar als onderdeel van de  [!DNL Target] Premium-oplossing. Ze zijn niet beschikbaar in [!DNL Target] Standard zonder een [!DNL Target] Premium-licentie.
>U kunt zien of uw organisatie een Standard- of Premium-licentie heeft door op de koppeling [!UICONTROL Administration] boven aan de interface [!DNL Target] te klikken.
>
>* **[!DNL Target]Standaardklanten**: Als u het  [!UICONTROL Users] tabblad ([!UICONTROL Administration > Users]) ziet (en niet het  **[!UICONTROL Properties]** tabblad), heeft uw organisatie een  [!DNL Target] standaardlicentie. [!DNL Target] Standaardklanten moeten de instructies in dit artikel volgen om gebruikers toe te voegen en machtigingen in het  [!DNL Adobe Admin Console]artikel toe te wijzen.
   >
   >
* **[!DNL Target]Premium-klanten**: Als u het  [!UICONTROL Users] tabblad en het  [!UICONTROL Properties] tabblad ([!UICONTROL Administration > Properties]) ziet, heeft uw organisatie een  [!DNL Target] Premium-licentie. [!DNL Target] Premiumklanten moeten de instructies in  [Enterprise-gebruikersmachtigingen ](/help/administrating-target/c-user-management/property-channel/property-channel.md) opvolgen en bedrijfsmachtigingen  [configureren ](/help/administrating-target/c-user-management/property-channel/properties-overview.md) om gebruikers toe te voegen en machtigingen in de  [!DNL Adobe Admin Console]account toe te wijzen.
>
>
Zie [Producten en profielen beheren](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) in de *Gebruikershandleiding voor bedrijven en teams* voor gedetailleerde informatie over het beheren van gebruikers en machtigingen.

Wanneer u aan de slag gaat met [!DNL Adobe Target], worden id&#39;s (eindigend op Adobe.com) vooraf ingevuld in uw [!DNL Adobe Experience Cloud]-account. Deze id&#39;s zijn bedoeld voor leden van teams van [!DNL Adobe], zodat zij u kunnen helpen met uw nieuwe account en met uw gebruik van [!DNL Adobe Target], indien u hulp nodig hebt. Neem op de gebruikelijke manier contact op met uw Adobe-teams om hulp te krijgen.

De nieuwe gebruiker wordt pas op de [!UICONTROL Users]-pagina weergegeven wanneer de gebruiker zich aanmeldt met zijn of haar [!DNL Adobe Experience Cloud]-account en zich vervolgens aanmeldt bij [!DNL Target Standard/Premium].

Standaard beginnen alle [!DNL Target] gebruikers met waarnemersmachtigingen.

Admin-gebruikers worden in de lijst [!UICONTROL Users] vermeld. Neem contact op met een van de gebruikers van de systeembeheerder als u uw toegangsniveau wilt wijzigen.

## Gebruikersgegevens weergeven vanuit Doel

U kunt een lijst van uw huidige gebruikers in uw milieu van het Doel, met inbegrip van hun rollen per werkruimte en e-mailadressen direct van binnen Doel bekijken.

Als u de pagina Gebruikers wilt weergeven, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Users]**.

![Gebruikerslijst vanuit doel](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Als u bestaande gebruikers wilt beheren of nieuwe gebruikers wilt toevoegen, moet u [!UICONTROL Adobe Admin Console] gebruiken, zoals hieronder wordt uitgelegd.

## Toegang tot de Adobe Admin Console {#access}

Voor taken die in Adobe Admin Console worden uitgevoerd, opent u de console door de volgende stappen uit te voeren:

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) en meld u vervolgens aan met uw Adobe ID als u zich nog niet hebt aangemeld.

1. (Voorwaardelijk) als u toegang tot [!DNL Admin Console for Enterprise] voor meer dan één organisatie hebt, klik de gebruikersavatar in de juiste hoek of de hoogste navigatiebar, dan selecteer de gewenste organisatie.

## Gebruikers {#add-users} toevoegen

Al gebruikersbeheer moet in [!DNL Adobe Admin Console for Enterprise] worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter gemigreerd van [!DNL Target] naar [!DNL Admin Console for Enterprise].

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) op  **[!UICONTROL Users]** >  **[!UICONTROL Users]** om nieuwe gebruikers te maken of bestaande gebruikers te bewerken.
1. Volg de instructies in [Gebruikers en groepen beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in *Handleiding voor gebruikers in de onderneming*.

## Gebruikersgroepen {#user-groups} maken

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid alle aangewezen voorrechten over verschillende producten van de Adobe kan zo gemakkelijk zijn zoals het toevoegen van hen aan een specifieke gebruikersgroep.

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) op  **[!UICONTROL Users]** >  **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of bestaande groepen te bewerken.
1. Volg de instructies in [Gebruikers en groepen beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in *Handleiding voor gebruikers in de onderneming*.

## Rollen en machtigingen opgeven {#roles-permissions}

Alleen systeembeheerders kunnen gebruikersrollen instellen in [!DNL Target]. Een gebruiker met een standaardfiatteur kan een waarnemer bijvoorbeeld niet wijzigen in een fiatteur zonder ook over [!DNL Experience Cloud] beheerdersrechten te beschikken.

Gebruikers van systeembeheerders moeten gebruikers aan het systeem toevoegen. Gebruikers worden niet automatisch toegevoegd. Ze worden uitgenodigd per e-mail van [!DNL Experience Cloud] en moeten hun e-mailadres bevestigen voordat hun accounts worden geregistreerd.

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE) op  **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![Tabblad Producten](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de gewenste werkruimte (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Op het tabblad [!UICONTROL Users] worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste toestemmingenrol (Approver, Redacteur, of Waarnemer) door de drop-down lijst voor elke gebruiker in [!UICONTROL Product Role] kolom te gebruiken.

   ![Vervolgkeuzelijst Productrol](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

Zie [Productmachtigingen en -rollen beheren in de Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de *Handleiding voor bedrijven* voor meer informatie.

## Trainingsvideo: Hoe te om de Werkruimten van het Doel ![badge van het Leerprogramma](/help/assets/tutorial.png) te vormen

Leerdoelstellingen:

* Toegang tot de Adobe Admin Console vanuit de Adobe Target-interface (drie manieren)
* Een werkruimte configureren in de Adobe Admin Console
   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten
* Standaardwerkruimten begrijpen

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
