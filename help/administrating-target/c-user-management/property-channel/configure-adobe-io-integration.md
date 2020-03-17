---
keywords: integration;roles;user permissions;admin console
description: Informatie over het verlenen van bestaande Adobe I/O-integraties toegang tot alle werkruimten met de gewenste rol in Adobe Target
title: Adobe I/O-integratie toegang verlenen tot werkruimten en rollen toewijzen in Adobe Target
subtopic: Getting Started
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# ![PREMIUM](/help/assets/premium.png) verleent Adobe I/O-integratie toegang tot werkruimten en wijst rollen toe

[!UICONTROL Enterprise Permissions] staat [!DNL Target] klanten toe om één enkele organisatie te gebruiken, maar het te verdelen in werkruimten voor hun verschillende teams of werkschema&#39;s.

>[!NOTE]
>
>De eigenschappen en de Toestemmingsfunctionaliteit zijn beschikbaar als deel van de [Oplossing van de Premie](/help/c-intro/intro.md#premium) van het Doel. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.

Met deze [!UICONTROL Enterprise Permissions] functie kunt u optimalisatieprogramma&#39;s in verschillende teams op effectieve wijze schalen. Hoewel de functie beschikbaar was in de [!DNL Target] gebruikersinterface, ontbrak de corresponderende ondersteuning tot eerder in 2019. In de release van [!DNL Target] februari 2019 heeft Adobe de Admin API&#39;s bijgewerkt, zodat u met het integratieaccount toegang kunt krijgen tot alle werkruimten die in uw organisatie zijn gemaakt. Dus, terwijl vroeger, Admin APIs tot enkel de standaardwerkruimte beperkt was, verleende de update van februari 2019 toegang tot alle werkruimten met [!UICONTROL Approver] toegang.

Met de release van [!DNL Target] september 2019 [!DNL Target] biedt [!UICONTROL Enterprise Permissions] u klanten de volgende toegangscontroles:

* U kunt de werkruimten kiezen waarop de integratie kan worden toegepast
* U kunt een rol op de integratie van Adobe I/O toepassen: [!UICONTROL Approver], [!UICONTROL Editor], of [!UICONTROL Observer].

Deze update biedt ondersteuning voor de volgende gebruiksgevallen:

* De Adobe I/O-integratie toegang geven tot alle werkruimten met de [!UICONTROL Observer] rol voor rapportagedoeleinden zonder rechten om bronnen te maken of te bewerken.
* Geef de Adobe I/O-integratie de toegang tot geselecteerde werkruimten met de juiste rol, zodat een centraal team in slechts enkele werkruimten API-gestuurde wijzigingen kan aanbrengen.
* Laat elk team dat eigenaar is van zijn werkruimte, zijn eigen integratie hebben wanneer het team klaar is om API&#39;s te verkennen en de rol dienovereenkomstig te kiezen.
* Mengen en afstemmen van bovenstaande scenario&#39;s.

**Actie vereist**: Klanten die momenteel API&#39;s gebruiken voor CRUD-bewerkingen op bronnen (activiteiten, publiek, aanbiedingen en rapportage) in alle werkruimten, moeten hun bestaande Adobe I/O-integratie toegang geven tot alle werkruimten met de gewenste rol volgens hun gebruikscase. U kunt dit doen door elk [!DNL Target] in [!UICONTROL Product Profile] de [!DNL Adobe Admin Console] en integratie(s) op het [!UICONTROL Integration] lusje te selecteren en toe te voegen. Vóór de release van september werkten alle integraties met behulp van [!UICONTROL Approver] toegang, ongeacht de keuze uit de [!UICONTROL Product Role] vervolgkeuzelijst. U kunt nu de gewenste rol kiezen.

>[!NOTE]
>
>Als deze actie niet wordt uitgevoerd, na de versie van [!DNL Target] september 2019, zullen de toegangscontroles activeren en u zult toegang tot enkel de standaardwerkruimte waarnemen als dat is hoe u momenteel opstelling bent. Er is geen negatieve reactie op het vooraf opzetten van integraties. Hoe eerder u deze wijziging aanbrengt, des te beter. Afhankelijk van het aantal werkruimten in uw organisatie, vergt dit proces slechts een paar klikken om een bestaande integratie in werkruimten met de gewenste rol toe te voegen.

**Om Adobe I/O-integraties toegang te geven tot werkruimten en om rollen toe te wijzen:**

1. Open de **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Klik op het **[!UICONTROL Products]** tabblad en selecteer vervolgens de naam van het gewenste product.

   ![Product kiezen in Adobe Admin Console](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Selecteer de gewenste werkruimte (Productprofiel).

   ![Selecteer het productprofiel](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klik op het **[!UICONTROL Integrations]** tabblad.

   ![Tabblad Integratie](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Voorwaardelijk) om een nieuwe integratie toe te voegen, klik **[!UICONTROL Add Integration]**, selecteer de gewenste integratie, dan klik **[!UICONTROL Save]**.

1. Selecteer in de **[!UICONTROL Product Role]** vervolgkeuzelijst de gewenste rol voor de desbetreffende werkruimte:

   * [!UICONTROL Approver]
   * [!UICONTROL Editor]
   * [!UICONTROL Observer]
   ![De rol Productprofiel kiezen](/help/administrating-target/c-user-management/property-channel/assets/product-profile-role.png)
