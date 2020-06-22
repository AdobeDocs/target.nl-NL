---
keywords: add user;manage user;user permissions
description: U kunt gebruikers toevoegen en hun machtigingen beheren in de Adobe Admin Console.
title: Gebruikers
subtopic: Getting Started
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: f81e03cb4bc7cd2080f7c8a8473192858b4bbef8
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---


# Gebruikers{#users}

U kunt gebruikers toevoegen en hun toestemmingen in [!DNL Adobe Admin Console]beheren.

>[!NOTE]
>
>De informatie in dit onderwerp is bijgewerkt om u een sluimerpiek bij de veranderingen te geven UI die in Target Standard/Premium 20.6.1 versie (Juli 2020) komen. De meeste informatie die in dit onderwerp wordt voorgesteld is op huidige UI van toepassing; de opties kunnen zich echter op iets andere locaties bevinden .

>[!NOTE]
>
>[!UICONTROL Properties] en [!UICONTROL Permissions] functionaliteit is beschikbaar als onderdeel van de [!DNL Target] Premium-oplossing. Ze zijn niet beschikbaar in [!DNL Target] Standard zonder een [!DNL Target] Premium-licentie.
>U kunt zien of uw organisatie een Standard- of Premium-licentie heeft door op de [!UICONTROL Administration] koppeling boven aan de [!DNL Target] gebruikersinterface te klikken.
>
>* **[!DNL Target]Standaardklanten **: Als u het[!UICONTROL Users]tabblad ([!UICONTROL Administration > Users]) ziet (en niet het **[!UICONTROL Properties]**tabblad), heeft uw organisatie een[!DNL Target]standaardlicentie. [!DNL Target Standard-klanten moeten de instructies in dit artikel opvolgen om gebruikers toe te voegen en machtigingen in het[!DNL Adobe Admin Console]artikel toe te wijzen.
   >
   >
* **[!DNL Target]Premium-klanten **: Als u het[!UICONTROL Users]tabblad en het[!UICONTROL Properties]tabblad ([!UICONTROL Administration > Properties]) ziet, heeft uw organisatie een[!DNL Target]Premium-licentie.[!DNL Target]Premiumklanten moeten de instructies in de gebruikersrechten[van de](/help/administrating-target/c-user-management/property-channel/property-channel.md)Enterprise opvolgen en bedrijfsmachtigingen[](/help/administrating-target/c-user-management/property-channel/properties-overview.md)configureren om gebruikers toe te voegen en machtigingen in de[!DNL Adobe Admin Console]Enterprise toe te wijzen.
>
>
Zie [Producten en profielen](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) beheren in de gebruikershandleiding voor *bedrijven en teams voor gedetailleerde informatie over het beheren van gebruikers en machtigingen*.

Wanneer u aan de slag gaat met [!DNL Adobe Target], worden de id&#39;s (eindigend op Adobe.com) vooraf ingevuld in uw [!DNL Adobe Experience Cloud] account. Deze id&#39;s zijn bestemd voor leden van [!DNL Adobe] teams, zodat zij u kunnen helpen met uw nieuwe account en met uw gebruik van [!DNL Adobe Target], mocht u hulp nodig hebben. Als u hulp nodig hebt, kunt u op de gebruikelijke manier contact opnemen met uw Adobe-teams.

De nieuwe gebruiker wordt pas op de [!UICONTROL Users] pagina weergegeven wanneer de gebruiker zich met zijn of haar [!DNL Adobe Experience Cloud] account heeft aangemeld en zich vervolgens aanmeldt bij [!DNL Target Standard/Premium].

Standaard beginnen alle [!DNL Target] gebruikers met waarnemersmachtigingen.

De gebruikers van Admin worden geïdentificeerd in de [!UICONTROL Users] lijst. Neem contact op met een van de gebruikers van de systeembeheerder als u uw toegangsniveau wilt wijzigen.

## Gebruikersgegevens weergeven vanuit Target

U kunt een lijst weergeven van uw huidige gebruikers in uw Target-omgeving, inclusief hun rollen per werkruimte en e-mailadressen, rechtstreeks vanuit Target.

Klik op **[!UICONTROL Administration]** > **[!UICONTROL Users]**.

![Gebruikerslijst vanuit Target](/help/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Als u bestaande gebruikers wilt beheren of nieuwe gebruikers wilt toevoegen, moet u de toepassing gebruiken, [!UICONTROL Adobe Admin Console]zoals hieronder wordt uitgelegd.

## De Adobe-Admin Console openen {#access}

Voor taken die in de Admin Console van Adobe worden uitgevoerd, toegang tot de console door deze stappen te volgen:

1. From within [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/)en meld u vervolgens aan met uw Adobe ID als u zich nog niet hebt aangemeld.

1. (Voorwaardelijk) Als u toegang hebt tot de sjabloon [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klikt u op de gebruikersavatar in de rechterhoek of op de bovenste navigatiebalk en selecteert u de gewenste organisatie.

## Gebruikers toevoegen {#add-users}

Al gebruikersbeheer moet in de [!DNL Adobe Admin Console for Enterprise]worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter van [!DNL Target] naar [!DNL Admin Console for Enterprise].

1. [Klik in de Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Users]** > **[!UICONTROL Users]** om nieuwe gebruikers te maken of bestaande gebruikers te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de gebruikershandleiding *van de* onderneming.

## Gebruikersgroepen maken {#user-groups}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid aan alle juiste rechten voor verschillende Adobe-producten kan net zo eenvoudig zijn als het toevoegen van deze rechten aan een specifieke gebruikersgroep.

1. [Klik in de Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Users]** > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of bestaande groepen te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de gebruikershandleiding *van de* onderneming.

## Rollen en machtigingen opgeven {#roles-permissions}

Alleen systeembeheerders kunnen gebruikersrollen instellen in [!DNL Target]. Een standaardfiatteur kan een waarnemer bijvoorbeeld niet wijzigen in een fiatteur zonder ook over [!DNL Experience Cloud] beheerdersrechten te beschikken.

Gebruikers van systeembeheerders moeten gebruikers aan het systeem toevoegen. Gebruikers worden niet automatisch toegevoegd. Ze worden uitgenodigd via e-mail van de website [!DNL Experience Cloud] en moeten hun e-mailadres bevestigen voordat hun accounts worden geregistreerd.

1. [Klik in de Admin Console](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

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

## Trainingsvideo: Target Workspaces ![Tutorial badge configureren](/help/assets/tutorial.png)

Leerdoelstellingen:

* De Adobe Admin Console openen vanuit de Adobe Target-interface (drie manieren)
* Een werkruimte configureren in de Adobe-Admin Console
   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten
* Standaardwerkruimten begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
