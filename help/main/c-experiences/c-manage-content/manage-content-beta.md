---
keywords: inhoud;elementen;inhoud beheren;aanbiedingen;elementen beheren;selectiemodus openen;selectiemodus
description: Leer hoe u code- en afbeeldingsaanbiedingen kunt beheren met de bibliotheek met aanbiedingen.
title: Hoe kan ik code- en afbeeldingsaanbiedingen beheren?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn bètafuncties in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 5d14dfd700cb1cec0fa62f66da1400bc8d7fd109
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---

# Aanbiedingen

Gebruik de [!UICONTROL Offers] bibliotheek in [!DNL Adobe Target] om uw code en afbeelding te beheren, biedt u inhoud aan.

>[!NOTE]
>
>Dit artikel bevat informatie over updates van de [!DNL Target] gebruikersinterface die momenteel deel uitmaakt van een bètaprogramma. De [!DNL Adobe Target] team laat vaak nieuwe eigenschappen voor bepaalde klanten voor het testen en terugkoppelen doeleinden toe. Nadat de testperiode is voltooid, worden deze functies in de toekomst voor alle klanten ingeschakeld [!DNL Target Standard/Premium] releases en aankondigingen in de releaseopmerkingen.

Klik op de knop **[!UICONTROL Offers]** tabblad boven aan het dialoogvenster [!DNL Target] UI om de [!UICONTROL Offers] bibliotheek.

![Biedt bibliotheek aan in Adobe Target](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

De [!UICONTROL Offers] bibliotheek bevat aanbiedingen die zijn ingesteld via [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) en API&#39;s. Aanbiedingen gemaakt in [!DNL Target Classic] of andere oplossingen kunnen worden bewerkt in [!DNL Target Standard/Premium].

De bibliotheek van Aanbiedingen verstrekt een overzicht van alle code en beeldaanbiedingen en laat u diverse acties uitvoeren:

| Element | Beschrijving |
|--- |--- |
| Linkernavigatieregel | Schakelen tussen aanbiedingen [!UICONTROL Code Offers] of [!UICONTROL Image Offers]. |
| [!UICONTROL Show filters] pictogram<P>![Pictogram Filters tonen](/help/main/c-activities/assets/show-filters-icon.png) | Klik op de knop **[!UICONTROL Show filters]** pictogram om aanbiedingen te filteren op [!UICONTROL Type], [!UICONTROL Source], en [!UICONTROL AEM Type]<P>Zie voor meer informatie [Filters toepassen op de lijst met aanbiedingen](#filters) hieronder. |
| Zoeken in velden | Gebruik de **[!UICONTROL Search in]** velden om snel een voorstel te vinden of om het aantal aanbiedingen dat wordt weergegeven in het dialoogvenster [!UICONTROL Offers] bibliotheek. U kunt zoeken op [!UICONTROL Offer Name], [!UICONTROL AEM Paths], of [!UICONTROL AEM Tags]. |
| [!UICONTROL Create Folder] | Klik op Map maken om mappen te maken in het dialoogvenster [!UICONTROL Offer] bibliotheek om codeaanbiedingen, beeldaanbiedingen, evenals andere omslagen te houden om een subomslagstructuur tot stand te brengen. Zie voor meer informatie [Aanbiedingsmappen maken](/help/main/c-experiences/c-manage-content/create-content-folder.md). |
| [!UICONTROL [!UICONTROL Create Offer]] | Maak een voorstel. Zie voor meer informatie over het maken van de verschillende soorten aanbiedingen: <ul><li>HTML-aanbod</li><li>[JSON-aanbieding](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[Omleidingsvoorstel](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[Externe aanbieding](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Selectievakjes voor bulkbewerkingen | bulktransacties uitvoeren op alle activiteiten of op geselecteerde activiteiten.<P>Voor een lijst van acties die beschikbaar zijn (afhankelijk van uw toestemmingen en de aanbiedingsstatus), zie [Snelle handelingen uitvoeren](#quick-actions) hieronder. |
| [!UICONTROL Name] | De naam van elke aanbieding.<P>Klik op de knop **[!UICONTROL Quick Info]** naast elke aanbiedingsnaam om meer informatie over die aanbieding in een pop-upkaart te bekijken, zoals de aanbieding-id, het type, de datum waarop de aanbieding voor het laatst is gewijzigd en door wie en meer.<p>Klik op de knop **[!UICONTROL More actions]** het pictogram (de horizontale ellips) naast elke aanbiedingsnaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren. De volgende acties zijn beschikbaar (afhankelijk van uw machtigingen en de status van het aanbod): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], en [!UICONTROL Move]. Zie voor meer informatie over elke actie [Snelle handelingen uitvoeren](#quick-actions) hieronder.<P>Klik op de tabelkop om de lijst alfabetisch te sorteren in oplopende of aflopende volgorde op naam. |
| [!UICONTROL Type] | Het type aanbieding: HTML-aanbiedingen, [Omleidingsvoorstellen](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Externe aanbiedingen](/help/main/c-experiences/c-manage-content/about-remote-offers.md), en [JSON-aanbiedingen](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Toont waar het voorstel is gemaakt: [!DNL Adobe Target], [!DNL Adobe Target Classic], en [!DNL Adobe Experience Manager]. |

## Filters toepassen op de bibliotheek met aanbiedingen {#filters}

Klik op de knop **[!UICONTROL Show filters]** icon ( ![Filters weergeven op de pagina Aanbiedingen](/help/main/c-experiences/c-manage-content/assets/show-filters-icon.png) ) om aanbiedingen te filteren op [!UICONTROL Type], [!UICONTROL Source], en [!UICONTROL AEM Type].

![aanbiedingen_filter, afbeelding](assets/offers-filter-new.png)

De **[!UICONTROL Show filters]** Met dit pictogram kunt u aanbiedingen filteren op de volgende categorieën:

* **Type**: HTML-aanbieding, [JSON-aanbieding](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Omleidingsvoorstel](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Externe aanbieding](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

* **Bron**: [!DNL Adobe Target], [!DNL Adobe Target Classic], en [!DNL Adobe Experience Manager].

* **AEM**: [Inhoudsfragmenten](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) en [Ervaar fragmenten](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Zie voor meer informatie over de verschillende fragmenttypen [Overzicht van AEM Experience Fragments en Content Fragments](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Snelle handelingen uitvoeren {#quick-actions}

U kunt de volgende snelle acties uitvoeren door op het juiste pictogram te klikken:

### Snelle informatie

Klik op de knop **[!UICONTROL Quick Info]** naast elke aanbiedingsnaam om meer informatie over die aanbieding in een pop-upkaart te bekijken, zoals de aanbieding-id, het type, de datum waarop de aanbieding voor het laatst is gewijzigd en door wie en meer. Welke opties beschikbaar zijn, is afhankelijk van het type aanbieding: HTML-aanbieding, [JSON-aanbieding](/help/main/c-experiences/c-manage-content/create-json-offer.md), [Omleidingsvoorstel](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Externe aanbieding](/help/main/c-experiences/c-manage-content/about-remote-offers.md).

![](/help/main/c-experiences/c-manage-content/assets/quick-actions.png)

### Meer handelingen

De beschikbare acties voor Codevoorstellen en voor Afbeeldingsaanbiedingen verschillen enigszins. De volgende secties bevatten meer informatie:

#### [!UICONTROL Code Offer] opties

Klik op de knop **[!UICONTROL More actions]** het pictogram (de horizontale ellips) naast elke aanbiedingsnaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren. De volgende acties zijn beschikbaar (afhankelijk van uw machtigingen en de status van het aanbod): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete], en [!UICONTROL Move].

![De optie Meer handelingen in de bibliotheek met doelaanbiedingen](/help/main/c-experiences/c-manage-content/assets/more-actions.png)

* Bewerken
* Kopiëren
* Verwijderen
* Verplaatsen (als u bijvoorbeeld een of meer items naar een map wilt verplaatsen, klikt u op de knop **[!UICONTROL Move]** pictogram voor het gewenste item, klik op de gewenste map en klik vervolgens op **[!UICONTROL Drop]**.)

Afhankelijk van uw machtigingen worden mogelijk niet alle pictogrammen voor opties weergegeven. Bijvoorbeeld een gebruiker met [!UICONTROL Observer] machtigingen hebben niet de rechten om de [!UICONTROL Copy] -optie.

Voor gedetailleerde informatie over de taken die u kunt uitvoeren op aanbiedingen en omslagen, zie [Werken met inhoud in de elementenbibliotheek](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] opties

Voer aanvullende taken uit door de muisaanwijzer boven de gewenste afbeeldingsaanbieding of map op de [!UICONTROL Image Offers] door op het gewenste pictogram te klikken.

![Opties voor afbeeldingsaanbiedingen](/help/main/c-experiences/c-manage-content/assets/image-offers-icons.png)

U kunt onder andere de volgende opties kiezen:

* Selecteren
* Downloaden
* Eigenschappen weergeven
* Bewerken
* Annoteren
* Kopiëren

Voor gedetailleerde informatie over de taken die u kunt uitvoeren op aanbiedingen en omslagen, zie [Werken met inhoud in de elementenbibliotheek](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>Aanbiedingen voor afbeeldingen maken geen deel uit van de [Machtigingen voor zakelijke gebruikers](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) model.

## Definities van aanbiedingen weergeven {#section_6B059DD121434E6292CAB393507D010E}

U kunt definitiedetails van voorstellen op een pop-up kaart in bekijken [!UICONTROL Offers] bibliotheek zonder de aanbieding te openen.

De volgende aanbiedingsdefinitiekaart voor een HTML-aanbieding is bijvoorbeeld toegankelijk door de muis boven een aanbieding op de [!UICONTROL Content] en klik vervolgens op het informatiepictogram:

![aanbiedingskaart-html-afbeelding](assets/offer-card-html.png)

De volgende informatie is beschikbaar:

* Naam
* Bron
* Type
* Aanbieding-id
* Pad aanbod
* Laatst gewijzigd

Klik op de knop [!UICONTROL Offer Usage] om de activiteiten weer te geven die verwijzen naar een codeaanbieding in de definitie-pop-upkaart van elke aanbieding. Deze functionaliteit is niet van toepassing op afbeeldingsaanbiedingen. Op deze manier voorkomt u dat andere activiteiten worden beïnvloed tijdens het bewerken van aanbiedingen. Informatie omvat [!UICONTROL Live Activities] en [!UICONTROL Inactive Activities].

![afbeelding met handige kaart](assets/offer-card-usage.png)

De volgende aanbieding definitiekaart voor een Voorstelling van de Omleiding:

![aanbieding-kaart-omleiding afbeelding](assets/offer-card-redirect.png)

De volgende informatie is beschikbaar:

* Naam
* Bron
* Type
* Aanbieding-id
* Pad aanbod
* Laatst gewijzigd
* URL omleiden
* Alle URL-parameters opnemen (Aan of Uit)
* Identiteitskaart van de vergaderingszitting van de pas (aan of weg)

De volgende kaart van de aanbiedingsdefinitie voor een Verre aanbieding:

![extern image met creditcard](assets/offer-card-remote.png)

De volgende informatie is beschikbaar:

* Naam
* Bron
* Type
* Aanbieding-id
* Pad aanbod
* Laatst gewijzigd
* Type URL omleiden
* Absolute of relatieve URL

## Trainingsvideo: De opslagplaats voor inhoud ![Overzicht badge](/help/main/assets/overview.png)

Deze video bevat informatie over het beheer van aanbiedingen.

* Verbinding tussen de [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) en de doelinhoudsbibliotheek
* Aangepaste HTML-aanbiedingen
* Aanbod van de HTML van de douane in de Visuele Composer van de Ervaring

>[!VIDEO](https://video.tv.adobe.com/v/17387)
