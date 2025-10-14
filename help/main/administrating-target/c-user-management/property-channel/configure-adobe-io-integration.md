---
keywords: integratie;rollen;gebruikersmachtigingen;beheerconsole
description: Leer hoe u bestaande Adobe I/O-integraties toegang geeft tot alle werkruimten met de gewenste rol in Adobe Target.
title: Hoe kan ik Adobe I/O toegang verlenen tot werkruimten en Rollen toewijzen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# Adobe I/O-integratie toegang verlenen tot werkruimten en rollen toewijzen

Met [!UICONTROL Enterprise Permissions] kunnen [!DNL Target] -klanten één organisatie gebruiken, maar deze delen in werkruimten voor hun verschillende teams of workflows.

>[!NOTE]
>
>De eigenschappen en de functionaliteit van Toestemmingen zijn beschikbaar als deel van de [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie.

Met de functie [!UICONTROL Enterprise Permissions] kunt u optimalisatieprogramma&#39;s in verschillende teams op effectieve wijze schalen. Hoewel de functie beschikbaar was in de gebruikersinterface van [!DNL Target] , hadden de API&#39;s voor beheerders tot eerder in 2019 geen ondersteuning. In de release van [!DNL Target] februari 2019 heeft Adobe de API&#39;s voor beheer bijgewerkt, zodat u met het integratieaccount toegang kunt krijgen tot alle werkruimten die in uw organisatie zijn gemaakt. Dus, terwijl eerdere versies, waren Admin APIs beperkt tot enkel de standaardwerkruimte, verleende de update van februari 2019 toegang tot alle werkruimten met [!UICONTROL Approver] toegang.

Met de release van [!DNL Target] september 2019 biedt [!DNL Target] [!UICONTROL Enterprise Permissions] klanten de volgende toegangsbesturingselementen:

* U kunt de werkruimten kiezen waarop de integratie kan worden toegepast
* U kunt een rol op de integratie van Adobe I/O toepassen: [!UICONTROL Approver], [!UICONTROL Editor], of [!UICONTROL Observer].

Deze update biedt ondersteuning voor de volgende gebruiksgevallen:

* Bied de Adobe I/O-integratietoegang tot alle werkruimten met de [!UICONTROL Observer] -rol voor rapportagedoeleinden zonder rechten om bronnen te maken of te bewerken.
* Verleen de integratie van Adobe I/O de toegang tot uitgezochte werkruimten met de aangewezen rol om een centraal team toe te staan om API-gedreven veranderingen in slechts een paar werkruimten aan te brengen.
* Laat elk team dat eigenaar is van zijn werkruimte zijn eigen integratie hebben wanneer het team klaar is om API&#39;s te verkennen en de rol dienovereenkomstig te kiezen.
* Voeg een van de bovenstaande scenario&#39;s samen en pas deze aan.

**Vereiste Actie**: Die klanten die momenteel APIs voor de verrichtingen van CRUD op middelen (activiteiten, publiek, aanbiedingen, en rapportering) over alle werkruimten leveraging moeten hun bestaande de integratietoegang van Adobe I/O tot alle werkruimten met de gewenste rol zoals per hun gebruikscase verlenen. U kunt dit doen door elke [!DNL Target] [!UICONTROL Product Profile] in de [!DNL Adobe Admin Console] te selecteren en de integratie(s) op het tabblad [!UICONTROL Integration] toe te voegen. Vóór de release van september werden alle integraties uitgevoerd met [!UICONTROL Approver] toegang, ongeacht de keuze uit de vervolgkeuzelijst [!UICONTROL Product Role] . U kunt nu de gewenste rol kiezen.

>[!NOTE]
>
>Als deze actie niet wordt uitgevoerd, na de release van [!DNL Target] september 2019, worden de toegangsbesturingselementen geactiveerd en ziet u alleen de toegang tot de standaardwerkruimte als dat is hoe u momenteel bent ingesteld. Er is geen negatieve reactie op het vooraf opzetten van integraties. Hoe eerder u deze wijziging aanbrengt, des te beter. Afhankelijk van het aantal werkruimten in uw organisatie, vergt dit proces slechts een paar klikken om een bestaande integratie in werkruimten met de gewenste rol toe te voegen.

**om de integraties van Adobe I/O toegang tot werkruimten te verlenen en rollen toe te wijzen:**

1. Open **[Adobe Admin Console &#x200B;](https://adminconsole.adobe.com)**.

1. Klik op het tabblad **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![&#x200B; kies product in Adobe Admin Console &#x200B;](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Selecteer de gewenste werkruimte (Productprofiel).

   ![&#x200B; selecteer het productprofiel &#x200B;](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klik op de tab **[!UICONTROL Integrations]** .

   ![&#x200B; het lusje van Integraties &#x200B;](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Voorwaardelijk) Als u een nieuwe integratie wilt toevoegen, klikt u op **[!UICONTROL Add Integration]** , selecteert u de gewenste integratie en klikt u op **[!UICONTROL Save]** .

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Product Role]** de gewenste rol voor de desbetreffende werkruimte:

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |
