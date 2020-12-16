---
keywords: integration;roles;user permissions;admin console
description: Informatie over het verlenen van toegang tot alle werkruimten met de gewenste rol in Adobe Target voor bestaande Adobe I/O-integratie
title: Adobe I/O-integratie toegang verlenen tot werkruimten en rollen toewijzen in Adobe Target
feature: user management
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---


# ![PREMIUMGrant Adobe I/O integrations access to workspaces and assign rollen ](/help/assets/premium.png) 

[!UICONTROL Enterprise Permissions] staat  [!DNL Target] klanten toe om één enkele organisatie te gebruiken, maar het te verdelen in werkruimten voor hun verschillende teams of werkschema&#39;s.

>[!NOTE]
>
>Eigenschappen en de functionaliteit van Toestemmingen is beschikbaar als deel van [de Oplossing van de Premium ](/help/c-intro/intro.md#premium) van het Doel. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.

De functie [!UICONTROL Enterprise Permissions] vereenvoudigt het effectief schalen van optimalisatieprogramma&#39;s in verschillende teams. Hoewel de functie beschikbaar was in de gebruikersinterface van [!DNL Target], ontbrak de Admin API&#39;s tot eerder in 2019 de corresponderende ondersteuning. In [!DNL Target] Februari 2019 versie, heeft Adobe Admin APIs bijgewerkt zodat u de integratierekening kunt gebruiken om tot alle werkruimten toegang te hebben die in uw organisatie worden gecreeerd. Dus, terwijl vroeger, Admin APIs tot enkel de standaardwerkruimte beperkt was, verleende de update van februari 2019 toegang tot alle werkruimten met [!UICONTROL Approver] toegang.

Met de [!DNL Target] release van september 2019 biedt [!DNL Target] [!UICONTROL Enterprise Permissions] klanten de volgende toegangsbesturingselementen:

* U kunt de werkruimten kiezen waarop de integratie kan worden toegepast
* U kunt een rol op de integratie van Adobe I/O toepassen: [!UICONTROL Approver], [!UICONTROL Editor] of [!UICONTROL Observer].

Deze update biedt ondersteuning voor de volgende gebruiksgevallen:

* Verleen de integratietoegang van Adobe I/O tot alle werkruimten met de [!UICONTROL Observer] rol voor rapporteringsdoeleinden zonder rechten om middelen tot stand te brengen of uit te geven.
* Verleen de integratie van Adobe I/O de toegang tot uitgezochte werkruimten met de aangewezen rol om een centraal team toe te staan om API-gedreven veranderingen in slechts een paar werkruimten aan te brengen.
* Laat elk team dat eigenaar is van zijn werkruimte zijn eigen integratie hebben wanneer het team klaar is om API&#39;s te verkennen en de rol dienovereenkomstig te kiezen.
* Mengen en afstemmen van bovenstaande scenario&#39;s.

**Actie vereist**: De klanten die momenteel APIs voor verrichtingen CRUD op middelen (activiteiten, publiek, aanbiedingen, en rapportering) over alle werkruimten leveraging moeten hun bestaande de integratietoegang van Adobe I/O tot alle werkruimten met de gewenste rol volgens hun gebruikscase verlenen. U kunt dit doen door elke [!DNL Target] [!UICONTROL Product Profile] in [!DNL Adobe Admin Console] te selecteren en de integratie(s) in &lt;a3 toe te voegen/> tabel. [!UICONTROL Integration] Vóór de release van september werkten alle integratie met behulp van [!UICONTROL Approver]-toegang, ongeacht de keuze uit de vervolgkeuzelijst [!UICONTROL Product Role]. U kunt nu de gewenste rol kiezen.

>[!NOTE]
>
>Als deze actie niet wordt uitgevoerd, na [!DNL Target] Versie van september 2019, zullen de toegangscontroles activeren en u zult toegang tot enkel de standaardwerkruimte waarnemen als dat is hoe u momenteel opstelling bent. Er is geen negatieve reactie op het vooraf opzetten van integraties. Hoe eerder u deze wijziging aanbrengt, des te beter. Afhankelijk van het aantal werkruimten in uw organisatie, vergt dit proces slechts een paar klikken om een bestaande integratie in werkruimten met de gewenste rol toe te voegen.

**Adobe I/O-integratie toegang verlenen tot werkruimten en rollen toewijzen:**

1. Open **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Klik op het tabblad **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![Product kiezen in Adobe Admin Console](/help/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Selecteer de gewenste werkruimte (Productprofiel).

   ![Selecteer het productprofiel](/help/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klik op het tabblad **[!UICONTROL Integrations]**.

   ![Tabblad Integratie](/help/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Voorwaardelijk) om een nieuwe integratie toe te voegen, klik **[!UICONTROL Add Integration]**, selecteer de gewenste integratie, dan klik **[!UICONTROL Save]**.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Product Role]** de gewenste rol voor die werkruimte:

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |
