---
keywords: content;assets;manage content;offers;manage assets;enter selection mode;selection mode
description: Hoe kan ik code- en afbeeldingsaanbiedingen beheren?
title: Aanbiedingen
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 70547a05155aa2909b0e66a1f26b0fd2cc730dd9
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# Aanbiedingen

Gebruik de [!UICONTROL Offers] bibliotheek in [!DNL Adobe Target] om uw codeaanbieding en beeldaanbiedingsinhoud te beheren.

1. Klik **[!UICONTROL Offers]** om de bibliotheek te openen.

   De bibliotheek bevat de aanbiedingen die zijn ingesteld via [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) en API&#39;s. Aanbiedingen die zijn gemaakt in [!DNL Target Classic] of andere oplossingen kunnen worden bewerkt in [!DNL Target Standard/Premium].

   De pagina [!UICONTROL Offers] heeft twee tabbladen aan de rechterkant: [!UICONTROL Code Offers] en [!UICONTROL Image Offers] die u voorstellen door type laten bekijken.

   ![Pagina met aanbiedingen met de tabbladen Codevoorstellen en Afbeeldingsaanbiedingen](/help/c-experiences/c-manage-content/assets/offers-page.png)

1. (Optioneel) Klik op de vervolgkeuzelijst **[!UICONTROL Type]** om aanbiedingen op type te filteren (HTML-aanbieding, [Gespecialiseerde fragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md), [Aanbieding omleiden](/help/c-experiences/c-manage-content/offer-redirect.md), [Externe aanbieding](/help/c-experiences/c-manage-content/about-remote-offers.md), [JSON-aanbiedingen](/help/c-experiences/c-manage-content/create-json-offer.md) en [Mappen](/help/c-experiences/c-manage-content/create-content-folder.md)).

   ![](assets/offers_filter.png)

1. (Optioneel) Klik op de vervolgkeuzelijst **[!UICONTROL Source]** om aanbiedingen te filteren op bron (Adobe Target, Adobe Target Classic en Adobe Experience Manager).

1. (Optioneel) Voer aanvullende taken uit door de muisaanwijzer boven de gewenste aanbieding of map op het tabblad [!UICONTROL Code Offers] te houden en vervolgens op het gewenste pictogram te klikken.

   ![Opties voor codeaanbiedingen](assets/offer-picker-large.png)

   De volgende opties zijn beschikbaar:

   * Weergave (zie [Definities van aanbiedingen weergeven](#section_6B059DD121434E6292CAB393507D010E) hieronder voor meer informatie.)
   * Bewerken
   * Kopiëren
   * Verplaats (als u bijvoorbeeld een of meer items naar een map wilt verplaatsen, klikt u op het pictogram **[!UICONTROL Move]** voor het gewenste item, klikt u op de gewenste map en vervolgens op **[!UICONTROL Drop]**.)
   * Verwijderen

   Afhankelijk van uw machtigingen worden mogelijk niet alle pictogrammen voor opties weergegeven. Bijvoorbeeld, heeft een gebruiker met [!UICONTROL Observer] toestemmingen niet de rechten om de [!UICONTROL Copy] optie te gebruiken.

1. (Optioneel) Voer aanvullende taken uit door de muisaanwijzer boven de gewenste afbeeldingsaanbieding of map op het tabblad [!UICONTROL Image Offers] te houden en vervolgens op het gewenste pictogram te klikken.

   ![Opties voor afbeeldingsaanbiedingen](/help/c-experiences/c-manage-content/assets/image-offers-icons.png)

   De volgende opties zijn beschikbaar:

   * Selecteren
   * Downloaden
   * Eigenschappen weergeven
   * Bewerken
   * Annoteren
   * Kopiëren

## Definities {#section_6B059DD121434E6292CAB393507D010E} weergeven

U kunt definitiedetails van aanbiedingen op een pop-up kaart in [!UICONTROL Offers] bibliotheek bekijken zonder de aanbieding te openen.

De volgende aanbiedingsdefinitiekaart voor een HTML-aanbieding wordt bijvoorbeeld geopend door de muisaanwijzer op een aanbieding in de lijst [!UICONTROL Content] te plaatsen en vervolgens op het informatiepictogram te klikken:

![](assets/offer-card-html.png)

De volgende informatie is beschikbaar:

* Naam
* Bron
* Type
* Aanbieding-id
* Pad aanbod
* Laatst gewijzigd

Klik op het tabblad [!UICONTROL Offer Usage] om de activiteiten weer te geven die verwijzen naar een codeaanbieding in de definitie-pop-upkaart van elke aanbieding. Deze functionaliteit is niet van toepassing op afbeeldingsaanbiedingen. Op deze manier voorkomt u dat andere activiteiten worden beïnvloed tijdens het bewerken van aanbiedingen. De informatie omvat [!UICONTROL Live Activities] en [!UICONTROL Inactive Activities].

![](assets/offer-card-usage.png)

De volgende aanbieding definitiekaart voor een Voorstelling van de Omleiding:

![](assets/offer-card-redirect.png)

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

![](assets/offer-card-remote.png)

De volgende informatie is beschikbaar:

* Naam
* Bron
* Type
* Aanbieding-id
* Pad aanbod
* Laatst gewijzigd
* Type URL omleiden
* Absolute of relatieve URL

## Trainingsvideo: De inhoudopslagplaats ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het beheer van aanbiedingen.

* Verbinding tussen de [Experience Cloud-elementenbibliotheek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) en de doelinhoudsbibliotheek
* Aangepaste HTML-aanbiedingen
* Aangepaste HTML-aanbieding in de Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)