---
keywords: integratie;rollen;gebruikersmachtigingen;beheerconsole
description: Leer hoe u bestaande Adobe I/O-integraties toegang geeft tot alle werkruimten met de gewenste rol in Adobe Target.
title: Hoe verstrek ik de Toegang van Adobe I/O tot Werkruimten en wijs Rollen toe?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Administration & Configuration
role: Admin
exl-id: 62f6399f-c590-470c-ac3b-e0c84db63112
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Toegang tot werkruimten voor Adobe I/O-integratie verlenen en rollen toewijzen

[!UICONTROL Enterprise Permissions] toestaat [!DNL Target] klanten om één enkele organisatie te gebruiken, maar het te verdelen in werkruimten voor hun verschillende teams of werkschema&#39;s.

>[!NOTE]
>
>Eigenschappen en machtigingen zijn beschikbaar als onderdeel van de [Doelpremie](/help/main/c-intro/intro.md#premium) oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder [!DNL Target Premium] licentie.

De [!UICONTROL Enterprise Permissions] Deze functie vergemakkelijkt het effectief schalen van optimalisatieprogramma&#39;s in verschillende teams. Hoewel de functie beschikbaar was in het dialoogvenster [!DNL Target] UI, ontbraken de Admin APIs de overeenkomstige steun tot vroeger in 2019. In de [!DNL Target] Release van februari 2019, heeft Adobe de Admin APIs bijgewerkt zodat u de integratierekening kunt gebruiken om tot alle werkruimten toegang te hebben die in uw organisatie worden gecreeerd. Dus, terwijl eerder, Admin APIs tot enkel de standaardwerkruimte beperkt waren, verleende de update van februari 2019 toegang tot alle werkruimten met [!UICONTROL Approver] toegang.

Met de [!DNL Target] release september 2019, [!DNL Target] [!UICONTROL Enterprise Permissions] voorziet klanten van de volgende toegangscontroles:

* U kunt de werkruimten kiezen waarop de integratie kan worden toegepast
* U kunt een rol op de integratie van Adobe I/O toepassen: [!UICONTROL Approver], [!UICONTROL Editor], of [!UICONTROL Observer].

Deze update biedt ondersteuning voor de volgende gebruiksgevallen:

* Verleen de integratietoegang van de Adobe I/O tot alle werkruimten met de [!UICONTROL Observer] rol voor rapportagedoeleinden zonder rechten om bronnen te maken of te bewerken.
* Verleen de Adobe I/O integratie de toegang tot uitgezochte werkruimten met de aangewezen rol om een centraal team toe te staan om API-gedreven veranderingen in slechts een paar werkruimten aan te brengen.
* Laat elk team dat eigenaar is van zijn werkruimte, zijn eigen integratie hebben wanneer het team klaar is om API&#39;s te verkennen en de rol dienovereenkomstig te kiezen.
* Mengen en afstemmen van bovenstaande scenario&#39;s.

**Actie vereist**: De klanten die momenteel APIs voor verrichtingen CRUD op middelen (activiteiten, publiek, aanbiedingen, en rapportering) over alle werkruimten gebruiken moeten hun bestaande de integratietoegang van Adobe I/O tot alle werkruimten met de gewenste rol zoals per hun gebruikscase verlenen. U kunt dit doen door elk te selecteren [!DNL Target] [!UICONTROL Product Profile] in de [!DNL Adobe Admin Console] en de integratie(s) in de [!UICONTROL Integration] tab. Vóór de release van september werden alle integraties uitgevoerd met [!UICONTROL Approver] toegang, ongeacht de keuze van de [!UICONTROL Product Role] vervolgkeuzelijst. U kunt nu de gewenste rol kiezen.

>[!NOTE]
>
>Als deze actie niet wordt uitgevoerd, na [!DNL Target] De versie van september 2019, zullen de toegangscontroles activeren en u zult toegang tot enkel de standaardwerkruimte waarnemen als dat is hoe u momenteel opstelling bent. Er is geen negatieve reactie op het vooraf opzetten van integraties. Hoe eerder u deze wijziging aanbrengt, des te beter. Afhankelijk van het aantal werkruimten in uw organisatie, vergt dit proces slechts een paar klikken om een bestaande integratie in werkruimten met de gewenste rol toe te voegen.

**Om Adobe I/O integraties toegang tot werkruimten te verlenen en rollen toe te wijzen:**

1. Open de **[Adobe Admin Console](https://adminconsole.adobe.com)**.

1. Klik op de knop **[!UICONTROL Products]** selecteert u vervolgens de naam van het gewenste product.

   ![Product kiezen in Adobe Admin Console](/help/main/administrating-target/c-user-management/property-channel/assets/io-choose-product.png)

1. Selecteer de gewenste werkruimte (Productprofiel).

   ![Selecteer het productprofiel](/help/main/administrating-target/c-user-management/property-channel/assets/io-select-product-profile.png)

1. Klik op de knop **[!UICONTROL Integrations]** tab.

   ![Tabblad Integratie](/help/main/administrating-target/c-user-management/property-channel/assets/integrations-tab.png)

1. (Voorwaardelijk) Als u een nieuwe integratie wilt toevoegen, klikt u op **[!UICONTROL Add Integration]** selecteert u de gewenste integratie en klikt u vervolgens op **[!UICONTROL Save]**.

1. Van de **[!UICONTROL Product Role]** selecteert u de gewenste rol voor die werkruimte in de vervolgkeuzelijst:

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |
