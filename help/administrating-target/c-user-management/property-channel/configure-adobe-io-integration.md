---
keywords: integration;roles;user permissions;admin console
description: Informatie over het verlenen van bestaande Adobe I/O integratietoegang tot alle werkruimten met de gewenste rol in Adobe Target
title: Toegang tot werkruimten verlenen voor Adobe I/O-integratie en rollen toewijzen in Adobe Target
feature: user management
subtopic: Getting Started
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) BIEDT I/O-integratietoegang tot werkruimten en wijst rollen toe

[!UICONTROL Enterprise Permissions] staat [!DNL Target] klanten toe om één enkele organisatie te gebruiken, maar het te verdelen in werkruimten voor hun verschillende teams of werkschema&#39;s.

>[!NOTE]
>
>De eigenschappen en de Toestemmingsfunctionaliteit zijn beschikbaar als deel van de [Oplossing van de Premie](/help/c-intro/intro.md#premium) van het Doel. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.

Met deze [!UICONTROL Enterprise Permissions] functie kunt u optimalisatieprogramma&#39;s in verschillende teams op effectieve wijze schalen. Hoewel de functie beschikbaar was in de [!DNL Target] gebruikersinterface, ontbrak de corresponderende ondersteuning tot eerder in 2019. In de release van [!DNL Target] februari 2019 heeft Adobe de Admin API&#39;s bijgewerkt zodat u met het integratieaccount toegang kunt krijgen tot alle werkruimten die in uw organisatie zijn gemaakt. Dus, terwijl vroeger, Admin APIs tot enkel de standaardwerkruimte beperkt was, verleende de update van februari 2019 toegang tot alle werkruimten met [!UICONTROL Approver] toegang.

Met de release van [!DNL Target] september 2019 [!DNL Target] biedt [!UICONTROL Enterprise Permissions] u klanten de volgende toegangscontroles:

* U kunt de werkruimten kiezen waarop de integratie kan worden toegepast
* U kunt een rol op de Adobe I/O integratie toepassen: [!UICONTROL Approver], [!UICONTROL Editor]of [!UICONTROL Observer].

Deze update biedt ondersteuning voor de volgende gebruiksgevallen:

* De Adobe I/O-integratie toegang verlenen tot alle werkruimten met de [!UICONTROL Observer] rol voor rapportagedoeleinden zonder rechten om bronnen te maken of te bewerken.
* Verleen de Adobe I/O integratie de toegang tot uitgezochte werkruimten met de aangewezen rol om een centraal team toe te staan om API-gedreven veranderingen in slechts een paar werkruimten aan te brengen.
* Laat elk team dat eigenaar is van zijn werkruimte, zijn eigen integratie hebben wanneer het team klaar is om API&#39;s te verkennen en de rol dienovereenkomstig te kiezen.
* Mengen en afstemmen van bovenstaande scenario&#39;s.

**Actie vereist**: De klanten die momenteel APIs voor verrichtingen CRUD op middelen (activiteiten, publiek, aanbiedingen, en rapportering) over alle werkruimten gebruiken moeten hun bestaande Adobe I/O integratietoegang tot alle werkruimten met de gewenste rol zoals per hun gebruikscase verlenen. U kunt dit doen door elk [!DNL Target] in [!UICONTROL Product Profile] de [!DNL Adobe Admin Console] en integratie(s) op het [!UICONTROL Integration] lusje te selecteren en toe te voegen. Vóór de release van september werkten alle integraties met behulp van [!UICONTROL Approver] toegang, ongeacht de keuze uit de [!UICONTROL Product Role] vervolgkeuzelijst. U kunt nu de gewenste rol kiezen.

>[!NOTE]
>
>Als deze actie niet wordt uitgevoerd, na de versie van [!DNL Target] september 2019, zullen de toegangscontroles activeren en u zult toegang tot enkel de standaardwerkruimte waarnemen als dat is hoe u momenteel opstelling bent. Er is geen negatieve reactie op het vooraf opzetten van integraties. Hoe eerder u deze wijziging aanbrengt, des te beter. Afhankelijk van het aantal werkruimten in uw organisatie, vergt dit proces slechts een paar klikken om een bestaande integratie in werkruimten met de gewenste rol toe te voegen.

**Om Adobe I/O integraties toegang tot werkruimten te verlenen en rollen toe te wijzen:**

1. Open de **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Klik op het **[!UICONTROL Products]** tabblad en selecteer vervolgens de naam van het gewenste product.

   ![Product kiezen in Adobe Admin Console](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Selecteer de gewenste werkruimte (Productprofiel).

   ![Selecteer het productprofiel](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klik op het **[!UICONTROL Integrations]** tabblad.

   ![Tabblad Integratie](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Voorwaardelijk) om een nieuwe integratie toe te voegen, klik **[!UICONTROL Add Integration]**, selecteer de gewenste integratie, dan klik **[!UICONTROL Save]**.

1. Selecteer in de **[!UICONTROL Product Role]** vervolgkeuzelijst de gewenste rol voor de desbetreffende werkruimte:

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |
