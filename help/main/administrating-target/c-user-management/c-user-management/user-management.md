---
keywords: gebruiker toevoegen;gebruiker beheren;gebruikersmachtigingen
description: Leer hoe u de [!DNL Adobe Admin Console] om gebruikers en hun rechten en rechten te beheren in [!DNL Adobe Target Standard].
title: Hoe voeg ik Gebruikers toe en beheer toestemmingen voor [!DNL Target Standard] Account?
feature: Administration & Configuration
role: Admin
exl-id: 535c28c7-179d-4edc-b140-880b9dfe1d59
source-git-commit: d40c25f75103327e749ad864b17df926cb323be0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Gebruikers

Gebruikers toevoegen en hun machtigingen beheren in het dialoogvenster [!DNL Adobe Admin Console] voor een [!DNL Target Standard] account.

>[!NOTE]
>
>[!UICONTROL Properties] en [!UICONTROL Permissions] is beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Ze zijn niet beschikbaar in [!DNL Target] Standaard zonder een [!DNL Target] Premium-licentie.
>
>U kunt zien of uw organisatie een [!UICONTROL Standard] of [!UICONTROL Premium] door op de [!UICONTROL Administration] koppeling boven aan [!DNL Target] UI.
>
>* **[!DNL Target][!UICONTROL Standard] Klanten**: Als u de [!UICONTROL Users] tab ([!UICONTROL Administration > Users]) (en niet de **[!UICONTROL Properties]** tab), heeft uw organisatie een [!DNL Target] [!UICONTROL Standard] licentie. [!DNL Target] [!UICONTROL Standard] klanten moeten de instructies in dit artikel opvolgen om gebruikers toe te voegen en machtigingen toe te wijzen in het dialoogvenster [!DNL Adobe Admin Console].
>
>* **[!DNL Target]Premium-klanten**: Als u de [!UICONTROL Users] en de [!UICONTROL Properties] tab ([!UICONTROL Administration > Properties]), heeft uw organisatie een [!DNL Target] Premium-licentie. [!DNL Target] Premiumklanten moeten de instructies in [Machtigingen voor Enterprise-gebruikers](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) en [Bedrijfsmachtigingen configureren](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) om gebruikers toe te voegen en toestemmingen toe te wijzen in [!DNL Adobe Admin Console].
>
>Voor gedetailleerde informatie over hoe te om gebruikers en toestemmingen te beheren, zie [Producten en profielen beheren](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html) in de *Gebruikershandleiding voor ondernemingen en teams*.

Wanneer u aan de slag gaat met [!DNL Adobe Target], vindt u id&#39;s (eindigend in Adobe.com) die vooraf zijn ingevuld in uw [!DNL Adobe Experience Cloud] account. Deze id&#39;s gelden voor leden van [!DNL Adobe] -teams zodat zij u kunnen helpen met uw nieuwe account en met uw gebruik van [!DNL Adobe Target], als u hulp nodig hebt. Neem op de gebruikelijke manier contact op met uw Adobe teams om hulp te krijgen.

Er worden geen nieuwe gebruikers weergegeven in de lijst [!UICONTROL Users] pagina tot zij login gebruikend hun [!DNL Adobe Experience Cloud] account en meld u vervolgens aan [!DNL Target].

Standaard alles [!DNL Target] gebruikers beginnen met [!UICONTROL Observer] machtigingen.

Admin-gebruikers worden geïdentificeerd in de [!UICONTROL Users] lijst. Neem contact op met een van de gebruikers van de systeembeheerder als u uw toegangsniveau wilt wijzigen.

## Gebruikersgegevens weergeven vanuit [!DNL Target]

U kunt een lijst met uw huidige gebruikers weergeven in het dialoogvenster [!DNL Target] UI, inclusief de rollen per werkruimte en e-mailadressen.

Als u het dialoogvenster [!UICONTROL Users] pagina, klikt u **[!UICONTROL Administration]** > **[!UICONTROL Users]**.

![Gebruikerslijst vanuit doel](/help/main/administrating-target/c-user-management/c-user-management/assets/user-list-target.png)

>[!NOTE]
>
>Als u een bestaande gebruiker wilt beheren of nieuwe gebruikers wilt toevoegen, moet u de opdracht [!UICONTROL Adobe Admin Console], zoals hieronder uiteengezet.

## Toegang krijgen tot de [!DNL Adobe Admin Console] {#access}

Voor taken die worden uitgevoerd in het dialoogvenster [!DNL Adobe Admin Console], toegang tot de console door deze stappen te volgen:

1. Van binnen [!DNL Target], klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Users]** > **[!UICONTROL Users Management]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/)Meld u vervolgens aan met uw Adobe ID als u zich nog niet hebt aangemeld.

1. (Voorwaardelijk) Als u toegang hebt tot de [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klik de gebruikersavatar in de juiste hoek of de hoogste navigatiebar, dan selecteer de gewenste organisatie.

## Gebruikers toevoegen {#add-users}

Alle gebruikersbeheer moet worden uitgevoerd in het dialoogvenster [!DNL Adobe Admin Console for Enterprise]. Alle bestaande gebruikers in [!DNL Target] wordt gemigreerd van [!DNL Target] aan de [!DNL Admin Console for Enterprise].

1. [In de Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), klikt u op **[!UICONTROL Users]** > **[!UICONTROL Users]** om nieuwe gebruikers te maken of om bestaande gebruikers te bewerken.
1. Volg de instructies in [Gebruikers en groepen beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de *Handleiding voor bedrijven*.

## Gebruikersgroepen maken {#user-groups}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Managers, enzovoort, en vervolgens rechten toewijzen voor meerdere [!DNL Adobe] producten en werkruimten. Het toewijzen van een nieuw teamlid alle aangewezen voorrechten over verschillende [!DNL Adobe] producten kunnen net zo eenvoudig zijn als het toevoegen ervan aan een specifieke gebruikersgroep.

1. [In de Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), klikt u op **[!UICONTROL Users]** > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of om bestaande groepen te bewerken.
1. Volg de instructies in [Gebruikers en groepen beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de *Handleiding voor bedrijven*.

## Rollen en machtigingen opgeven {#roles-permissions}

Alleen systeembeheerders kunnen gebruikersrollen instellen in [!DNL Target]. Bijvoorbeeld een [!UICONTROL Standard] een fiatteur kan een waarnemer niet in een fiatteur veranderen zonder dat hij [!DNL Experience Cloud] Beheerdersrechten.

Systeembeheerders moeten gebruikers aan het systeem toevoegen. Gebruikers worden niet automatisch toegevoegd. Ze worden per e-mail uitgenodigd vanuit de [!DNL Experience Cloud] en moeten hun e-mailadres bevestigen voordat hun account wordt geregistreerd.

1. [In de Admin Console](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#section_79796E0227D048F59BAE0AB02E544EBE), klikt u op **[!UICONTROL Products]** en selecteert u vervolgens de naam van het gewenste product.

   ![Tabblad Producten](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de gewenste werkruimte (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

   De [!UICONTROL Users] worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste machtigingenrol ([!UICONTROL Approver], [!UICONTROL Editor], [!UICONTROL Observer] of [!UICONTROL Publisher]) door de vervolgkeuzelijst te gebruiken voor elke gebruiker in de [!UICONTROL Product Role] kolom.

   ![Vervolgkeuzelijst Productrol](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | [!UICONTROL Approver] | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | [!UICONTROL Editor] | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | [!UICONTROL Observer] | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | [!UICONTROL Publisher] | Vergelijkbaar met de [!UICONTROL Observer] rol (kan activiteiten bekijken, maar kan niet hen creëren of uitgeven). De [!UICONTROL Publisher] de rol heeft de extra toestemming om activiteiten te activeren. |

Zie voor meer informatie [Productmachtigingen en -rollen beheren in de Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de *Handleiding voor bedrijven*.

## Trainingsvideo: Adobe Target Workspaces configureren ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Leerdoelstellingen:

* Toegang tot de Adobe Admin Console vanuit de Adobe Target-interface (drie manieren)
* Een werkruimte configureren in de Adobe Admin Console
   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten
* Standaardwerkruimten begrijpen

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct; nochtans, zouden de opties in lichtjes verschillende plaatsen kunnen zijn. Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/19463/)
