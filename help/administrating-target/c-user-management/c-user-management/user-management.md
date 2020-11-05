---
keywords: add user;manage user;user permissions
description: U kunt gebruikers toevoegen en hun machtigingen beheren in de Adobe Admin Console.
title: Gebruikers
feature: user management
subtopic: Getting Started
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---


# Gebruikers{#users}

U kunt gebruikers toevoegen en hun toestemmingen in [!DNL Adobe Admin Console]beheren.

>[!NOTE]
>
>[!UICONTROL Properties] en [!UICONTROL Permissions] functionaliteit is beschikbaar als onderdeel van de [!DNL Target] Premium-oplossing. Ze zijn niet beschikbaar in [!DNL Target] Standard zonder een [!DNL Target] Premium-licentie.
>U kunt zien of uw organisatie een Standard- of Premium-licentie heeft door op de [!UICONTROL Administration] koppeling boven aan de [!DNL Target] gebruikersinterface te klikken.
>
>* **[!DNL Target]Standaardklanten**: Als u het [!UICONTROL Users] tabblad ([!UICONTROL Administration > Users]) ziet (en niet het **[!UICONTROL Properties]** tabblad), heeft uw organisatie een [!DNL Target] standaardlicentie. [!DNL Target] Standaardklanten moeten de instructies in dit artikel volgen om gebruikers toe te voegen en machtigingen in het [!DNL Adobe Admin Console]artikel toe te wijzen.
   >
   >
* **[!DNL Target]Premium-klanten**: Als u het [!UICONTROL Users] tabblad en het [!UICONTROL Properties] tabblad ([!UICONTROL Administration > Properties]) ziet, heeft uw organisatie een [!DNL Target] Premium-licentie. [!DNL Target] Premiumklanten moeten de instructies in de gebruikersrechten [van de](/help/administrating-target/c-user-management/property-channel/property-channel.md) Enterprise opvolgen en bedrijfsmachtigingen [](/help/administrating-target/c-user-management/property-channel/properties-overview.md) configureren om gebruikers toe te voegen en machtigingen in de [!DNL Adobe Admin Console]Enterprise toe te wijzen.
>
>
Zie [Producten en profielen](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) beheren in de gebruikershandleiding voor *bedrijven en teams voor gedetailleerde informatie over het beheren van gebruikers en machtigingen*.

Wanneer u begint met [!DNL Adobe Target], worden id&#39;s (eindigend op Adobe.com) vooraf ingevuld in uw [!DNL Adobe Experience Cloud] account. Deze id&#39;s zijn bestemd voor leden van [!DNL Adobe] teams, zodat zij u kunnen helpen met uw nieuwe account en met uw gebruik van [!DNL Adobe Target], mocht u hulp nodig hebben. Neem op de gebruikelijke manier contact op met uw Adobe-teams om hulp te krijgen.

De nieuwe gebruiker wordt pas op de [!UICONTROL Users] pagina weergegeven wanneer de gebruiker zich met zijn of haar [!DNL Adobe Experience Cloud] account heeft aangemeld en zich vervolgens aanmeldt bij [!DNL Target Standard/Premium].

Standaard beginnen alle [!DNL Target] gebruikers met waarnemersmachtigingen.

De gebruikers van Admin worden geïdentificeerd in de [!UICONTROL Users] lijst. Neem contact op met een van de gebruikers van de systeembeheerder als u uw toegangsniveau wilt wijzigen.

## Gebruikersgegevens weergeven vanuit Doel

U kunt een lijst van uw huidige gebruikers in uw milieu van het Doel, met inbegrip van hun rollen per werkruimte en e-mailadressen direct van binnen Doel bekijken.

Klik op **[!UICONTROL Administration]** > **[!UICONTROL Users]**.

![Gebruikerslijst vanuit doel](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Als u bestaande gebruikers wilt beheren of nieuwe gebruikers wilt toevoegen, moet u de toepassing gebruiken, [!UICONTROL Adobe Admin Console]zoals hieronder wordt uitgelegd.

## Toegang tot de Adobe Admin Console {#access}

Voor taken die in Adobe Admin Console worden uitgevoerd, opent u de console door de volgende stappen uit te voeren:

1. From within [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/)en meld u vervolgens aan met uw Adobe ID als u zich nog niet hebt aangemeld.

1. (Voorwaardelijk) Als u toegang hebt tot de sjabloon [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klikt u op de gebruikersavatar in de rechterhoek of op de bovenste navigatiebalk en selecteert u de gewenste organisatie.

## Gebruikers toevoegen {#add-users}

Al gebruikersbeheer moet in de [!DNL Adobe Admin Console for Enterprise]worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter van [!DNL Target] naar [!DNL Admin Console for Enterprise].

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Users]** > **[!UICONTROL Users]** om nieuwe gebruikers te maken of bestaande gebruikers te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de gebruikershandleiding *van de* onderneming.

## Gebruikersgroepen maken {#user-groups}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid alle aangewezen voorrechten over verschillende producten van de Adobe kan zo gemakkelijk zijn zoals het toevoegen van hen aan een specifieke gebruikersgroep.

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Users]** > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of bestaande groepen te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de gebruikershandleiding *van de* onderneming.

## Rollen en machtigingen opgeven {#roles-permissions}

Alleen systeembeheerders kunnen gebruikersrollen instellen in [!DNL Target]. Een standaardfiatteur kan een waarnemer bijvoorbeeld niet wijzigen in een fiatteur zonder ook over [!DNL Experience Cloud] beheerdersrechten te beschikken.

Gebruikers van systeembeheerders moeten gebruikers aan het systeem toevoegen. Gebruikers worden niet automatisch toegevoegd. Ze worden uitgenodigd via e-mail van de website [!DNL Experience Cloud] en moeten hun e-mailadres bevestigen voordat hun accounts worden geregistreerd.

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![Tabblad Producten](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de gewenste werkruimte (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Op het [!UICONTROL Users] tabblad worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste toestemmingenrol (Approver, Redacteur, of Waarnemer) door de drop-down lijst voor elke gebruiker in de [!UICONTROL Product Role] kolom te gebruiken.

   ![Vervolgkeuzelijst Productrol](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

Zie [Productmachtigingen en -rollen beheren in de Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de gebruikershandleiding *van de* onderneming voor meer informatie.

## Trainingsvideo: Hoe te om het ![Leerprogramma van de Werkruimten van het Doel te vormen](/help/assets/tutorial.png)

Leerdoelstellingen:

* Toegang tot de Adobe Admin Console vanuit de Adobe Target-interface (drie manieren)
* Een werkruimte configureren in de Adobe Admin Console
   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten
* Standaardwerkruimten begrijpen

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] menu (voorheen [!UICONTROL Administration] [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
