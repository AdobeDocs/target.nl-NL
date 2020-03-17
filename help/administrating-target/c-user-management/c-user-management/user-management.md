---
keywords: add user;manage user;user permissions
description: U kunt gebruikers toevoegen en hun machtigingen beheren in de Adobe Admin Console.
title: Gebruikers
subtopic: Getting Started
topic: Standard
uuid: 9b311dd3-b8fa-483d-aedd-96761cfcd67e
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Gebruikers{#users}

U kunt gebruikers toevoegen en hun machtigingen beheren in de Adobe Admin Console.

>[!NOTE]
>
>[!UICONTROL Properties] en [!UICONTROL Permissions] functionaliteit is beschikbaar als onderdeel van de [!DNL Target] Premium-oplossing. Ze zijn niet beschikbaar in [!DNL Target] Standard zonder een [!DNL Target] Premium-licentie.
>U kunt zien of uw organisatie een Standard- of Premium-licentie heeft door op de [!UICONTROL Setup] koppeling boven aan de [!DNL Target] gebruikersinterface te klikken.
>
>**[!DNL Target]Standaardklanten **: Als u het[!UICONTROL Users]tabblad ([!UICONTROL Setup > Users]) ziet, heeft uw organisatie een[!DNL Target]standaardlicentie. [!DNL de Standaardklanten van het Doel zouden de instructies in dit artikel moeten volgen om gebruikers toe te voegen en toestemmingen in toe te wijzen[!DNL Adobe Admin Console].
>
>**[!DNL Target]Premium-klanten **: Als u het[!UICONTROL Properties]tabblad ([!UICONTROL Setup > Properties]) ziet, heeft uw organisatie een[!DNL Target]Premium-licentie.[!DNL Target]Premiumklanten moeten de instructies in de gebruikersrechten[van de](/help/administrating-target/c-user-management/property-channel/property-channel.md)Enterprise opvolgen en bedrijfsmachtigingen[](/help/administrating-target/c-user-management/property-channel/properties-overview.md)configureren om gebruikers toe te voegen en machtigingen in de[!DNL Adobe Admin Console]Enterprise toe te wijzen.

Zie Producten en profielen [](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) beheren in de gebruikershandleiding voor Enterprise &amp; Teams voor informatie over het beheren van gebruikers en machtigingen.

Wanneer u aan de slag gaat met [!DNL Adobe Target], worden de id&#39;s (eindigend op Adobe.com) vooraf ingevuld in uw [!DNL Adobe Experience Cloud] account. Deze id&#39;s zijn bestemd voor leden van Adobe-teams, zodat zij u kunnen helpen met uw nieuwe account en met uw gebruik van [!DNL Adobe Target], mocht u hulp nodig hebben. Als u hulp nodig hebt, kunt u op de gebruikelijke manier contact opnemen met uw Adobe-teams.

De nieuwe gebruiker wordt pas op de [!UICONTROL Users] pagina weergegeven wanneer de gebruiker zich aanmeldt met zijn of haar Adobe Experience Cloud-account en zich vervolgens aanmeldt bij [!DNL Target Standard/Premium] door op de [!DNL Target] kaart te klikken.

Standaard beginnen alle [!DNL Target] gebruikers met waarnemersmachtigingen.

Admin-gebruikers worden geïdentificeerd in de lijst Gebruikers. Neem contact op met een van de gebruikers van de systeembeheerder als u uw toegangsniveau wilt wijzigen.

## De Adobe Admin Console openen {#access}

Voor taken die worden uitgevoerd in de Adobe Admin Console, toegang tot de console door deze stappen te volgen:

1. Ga naar [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/) > Meld u aan met uw Adobe-id, als u zich nog niet hebt aangemeld.

   of

   Als u zich al hebt aangemeld bij de Experience Cloud, gaat u naar [https://www.experiencecloud.adobe.com](https://experiencecloud.adobe.com)en klikt u op het [!UICONTROL App] pictogram in de bovenste navigatiebalk > op **[!UICONTROL Admin]** de rechterkant.

1. (Voorwaardelijk) Als u toegang hebt tot de sjabloon [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klikt u op de gebruikersavatar in de rechterhoek of op de bovenste navigatiebalk en selecteert u de gewenste organisatie.

## Gebruikers toevoegen {#add-users}

Al gebruikersbeheer moet in de [!DNL Adobe Admin Console for Enterprise]worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter van [!DNL Target] naar [!DNL Admin Console for Enterprise].

1. [Klik in de beheerconsole](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Users]** > **[!UICONTROL Users]** om nieuwe gebruikers te maken of bestaande gebruikers te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de *Enterprise User Guide*.

## Gebruikersgroepen maken {#user-groups}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid aan alle juiste rechten voor verschillende Adobe-producten kan net zo eenvoudig zijn als het toevoegen van deze rechten aan een specifieke gebruikersgroep.

1. [Klik in de beheerconsole](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Users]** > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of bestaande groepen te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de *Enterprise User Guide*.

## Rollen en machtigingen opgeven {#roles-permissions}

Alleen systeembeheerders kunnen gebruikersrollen instellen in [!DNL Target]. Een gebruiker met een standaardfiatteur kan een waarnemer bijvoorbeeld niet wijzigen in een fiatteur zonder dat hij of zij ook beschikt over de rechten voor beheer van de cloud.

Gebruikers van systeembeheerders moeten gebruikers aan het systeem toevoegen. Gebruikers worden niet automatisch toegevoegd. Ze worden via e-mail uitgenodigd vanuit de Experience Cloud en moeten hun e-mailadres bevestigen voordat hun accounts worden geregistreerd.

1. [Klik in de beheerconsole](../../../administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE)op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![Tabblad Producten](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Klik op de gewenste werkruimte (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace.png)

   Op het [!UICONTROL Users] tabblad worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new.png)

1. Selecteer de gewenste toestemmingenrol (Approver, Redacteur, of Waarnemer) door de drop-down lijst voor elke gebruiker in de [!UICONTROL Product Role] kolom te gebruiken.

   ![Vervolgkeuzelijst Productrol](/help/administrating-target/c-user-management/c-user-management/assets/product-role.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |

Zie [Productmachtigingen en -rollen beheren in de beheerconsole](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de gebruikershandleiding *van de* onderneming voor meer informatie.

## Trainingsvideo: Hoe te om het ![Leerprogramma van de Werkruimten van het Doel te vormen](/help/assets/tutorial.png)

Leerdoelstellingen:

* Toegang tot de Adobe Admin Console van de interface van het Doel van Adobe (drie manieren)
* Een werkruimte configureren in de Adobe Admin Console
   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten
* Standaardwerkruimten begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
