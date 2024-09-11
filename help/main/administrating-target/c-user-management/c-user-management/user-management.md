---
keywords: gebruiker toevoegen;gebruiker beheren;gebruikersmachtigingen
description: Leer hoe te om  [!DNL Adobe Admin Console]  te gebruiken om gebruikers en hun toestemmingen en rechten in  [!DNL Adobe Target Standard] te beheren.
title: Hoe voeg ik Gebruikers toe en beheer Toestemmingen voor a  [!DNL Target Standard]  Rekening?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: 8560fa828fac91170fd295c9ef9a9b0e6ce1651c
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 0%

---

# Gebruikers

Voeg gebruikers toe en beheer hun machtigingen in de [!DNL Adobe Admin Console] voor een [!DNL Target Standard] -account.

>[!NOTE]
>
>[!UICONTROL Properties] en [!UICONTROL Permissions] is beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Deze zijn niet beschikbaar in [!DNL Target] Standard zonder een [!DNL Target] Premium-licentie.
>
>Als u wilt weten of uw organisatie een [!UICONTROL Standard] - of [!UICONTROL Premium] -licentie heeft, klikt u op de koppeling [!UICONTROL Administration] boven aan de gebruikersinterface van [!DNL Target] .
>
>* **[!DNL Target][!UICONTROL Standard] Klanten**: als u het tabblad [!UICONTROL Users] ([!UICONTROL Administration > Users]) ziet (en niet het tabblad **[!UICONTROL Properties]** ), heeft uw organisatie een licentie [!DNL Target] [!UICONTROL Standard] . [!DNL Target] [!UICONTROL Standard] -klanten moeten de instructies in dit artikel opvolgen om gebruikers toe te voegen en machtigingen toe te wijzen in [!DNL Adobe Admin Console] .
>
>* **[!DNL Target]Premium-klanten** : als u de tab [!UICONTROL Users] en de tab [!UICONTROL Properties] ([!UICONTROL Administration > Properties] ) ziet, heeft uw organisatie een [!DNL Target] Premium-licentie. [!DNL Target] de klanten van de Premie zouden de instructies in [ de gebruikerstoestemmingen van de Onderneming ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) moeten volgen en [ ondernemingstoestemmingen ](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) vormen om gebruikers toe te voegen en toestemmingen in [!DNL Adobe Admin Console] toe te wijzen.
>
>Voor gedetailleerde informatie over hoe te om gebruikers en toestemmingen te beheren, zie [ producten en profielen ](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) in de *Gids van de Gebruiker van de Onderneming &amp; van Teams* leiden.

Wanneer u aan de slag gaat met [!DNL Adobe Target] , worden id&#39;s (eindigend op Adobe.com) al ingevuld in uw [!DNL Adobe Experience Cloud] -account. Deze id&#39;s zijn bestemd voor leden van [!DNL Adobe] -teams, zodat zij u kunnen helpen met uw nieuwe account en met uw gebruik van [!DNL Adobe Target] , als u hulp nodig hebt. Neem op de gebruikelijke manier contact op met uw Adobe teams om hulp te krijgen.

Nieuwe gebruikers worden pas op de [!UICONTROL Users] -pagina weergegeven wanneer ze zich met hun [!DNL Adobe Experience Cloud] -account hebben aangemeld en zich vervolgens aanmelden bij [!DNL Target] .

Standaard beginnen alle [!DNL Target] -gebruikers met [!UICONTROL Observer] -machtigingen.

Admin-gebruikers worden geïdentificeerd in de lijst [!UICONTROL Users] . Neem contact op met een van de gebruikers van de systeembeheerder als u uw toegangsniveau wilt wijzigen.

## Gebruikersgegevens weergeven vanuit [!DNL Target]

U kunt een lijst van uw huidige gebruikers in [!DNL Target] UI, met inbegrip van hun rollen per werkruimte en e-mailadressen bekijken.

Als u de pagina [!UICONTROL Users] wilt weergeven, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Users]** .

![ lijst van de Gebruiker van binnen Doel ](/help/main/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Als u bestaande gebruikers wilt beheren of nieuwe gebruikers wilt toevoegen, moet u de instructie [!UICONTROL Adobe Admin Console] gebruiken, zoals hieronder wordt uitgelegd.

## Toegang krijgen tot de [!DNL Adobe Admin Console] {#access}

Voor taken uitgevoerd in [!DNL Adobe Admin Console], heb toegang tot de console door deze stappen te volgen:

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]** .

   of

   Ga naar [ https://adminconsole.adobe.com/enterprise/ ](https://adminconsole.adobe.com/enterprise/), dan login gebruikend uw Adobe ID, als u niet reeds het programma hebt geopend.

1. (Voorwaardelijk) Als u toegang hebt tot [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klikt u op de gebruikersavatar in de rechterhoek of op de bovenste navigatiebalk en selecteert u de gewenste organisatie.

## Gebruikers toevoegen {#add-users}

Al gebruikersbeheer moet in [!DNL Adobe Admin Console for Enterprise] worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter gemigreerd van [!DNL Target] naar [!DNL Admin Console for Enterprise] .

1. [ in de Admin Console ](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), klik **[!UICONTROL Users]** > **[!UICONTROL Users]** om nieuwe gebruikers tot stand te brengen of bestaande gebruikers uit te geven.
1. Volg de instructies in [ leiden Gebruikers en Groepen in het Experience Cloud ](https://helpx.adobe.com/enterprise/help/users.html) in de *Gids van de Gebruiker van de Onderneming*.

## Gebruikersgroepen maken {#user-groups}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives enzovoort, en vervolgens rechten toewijzen voor meerdere [!DNL Adobe] -producten en -werkruimten. Het toewijzen van een nieuw teamlid aan alle juiste rechten voor verschillende [!DNL Adobe] -producten kan net zo eenvoudig zijn als het toevoegen van deze rechten aan een specifieke gebruikersgroep.

1. [ in de Admin Console ](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), klik **[!UICONTROL Users]** > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen tot stand te brengen of bestaande groepen uit te geven.
1. Volg de instructies in [ leiden Gebruikers en Groepen in het Experience Cloud ](https://helpx.adobe.com/enterprise/help/users.html) in de *Gids van de Gebruiker van de Onderneming*.

## Rollen en machtigingen opgeven {#roles-permissions}

Alleen systeembeheerders kunnen gebruikersrollen instellen in [!DNL Target] . Een [!UICONTROL Standard] -fiatteur kan een waarnemer bijvoorbeeld niet wijzigen in een fiatteur zonder ook over [!DNL Experience Cloud] beheerdersrechten te beschikken.

Systeembeheerders moeten gebruikers aan het systeem toevoegen. Gebruikers worden niet automatisch toegevoegd. Ze worden uitgenodigd per e-mail van [!DNL Experience Cloud] en moeten hun e-mailadres bevestigen voordat hun accounts worden geregistreerd.

>[!NOTE]
>
>Als u activiteiten wilt weergeven in [!DNL Target] , moeten gebruikers rechtstreeks worden toegewezen aan een werkruimte met ten minste de rol [!UICONTROL Observer] . Toewijzing via alleen gebruikersgroepen is onvoldoende. Het wordt over het algemeen aanbevolen gebruikers toegang te verlenen tot de standaardwerkruimte.

1. [ in de Admin Console ](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), klik **[!UICONTROL Products]**, dan selecteer de naam van het gewenste product.

   ![ Producten tabel ](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de gewenste werkruimte (bijvoorbeeld Standaard Workspace).

   ![ Standaard Workspace ](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   Op het tabblad [!UICONTROL Users] worden alle gebruikers in die werkruimte weergegeven.

   ![ configuratiegebruikers ](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste machtigingenrol ([!UICONTROL Approver], [!UICONTROL Editor], [!UICONTROL Observer] of [!UICONTROL Publisher]) door de vervolgkeuzelijst voor elke gebruiker in de kolom [!UICONTROL Product Role] te gebruiken.

   ![ drop-down lijst van de Rol van het Product ](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | [!UICONTROL Approver] | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | [!UICONTROL Editor] | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | [!UICONTROL Observer] | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | [!UICONTROL Publisher] | Lijkt op de rol [!UICONTROL Observer] (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De [!UICONTROL Publisher] -rol heeft echter de extra machtiging om activiteiten te activeren. |

Voor meer informatie, zie [ de Toestemmingen en Rollen van het Product in de Admin Console ](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de *Gids van de Gebruiker van de Onderneming* leiden.

## De video van de opleiding: Hoe te om de Werkruimten van Adobe Target ![ badge van de Leerprogramma te vormen ](/help/main/assets/tutorial.png)

Leerdoelstellingen:

* Toegang tot de Adobe Admin Console vanuit de Adobe Target-interface (drie manieren)
* Een werkruimte configureren in de Adobe Admin Console
   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten
* Standaardwerkruimten begrijpen

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] [!UICONTROL Administration] menu (voorheen [!UICONTROL Setup] ) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct; nochtans, zouden de opties in lichtjes verschillende plaatsen kunnen zijn. Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
