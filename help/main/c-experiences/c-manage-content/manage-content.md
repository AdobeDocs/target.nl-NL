---
keywords: inhoud;elementen;inhoud beheren;aanbiedingen;elementen beheren;selectiemodus openen;selectiemodus
description: Leer hoe u code- en afbeeldingsaanbiedingen kunt beheren met de bibliotheek Aanbiedingen in Adobe Target.
title: Hoe kan ik code- en afbeeldingsaanbiedingen beheren?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: f93e33e91fb7be9c0d1772a2014864b46c1dfe47
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Aanbiedingen

Gebruik de [!UICONTROL Offers] bibliotheek in [!DNL Adobe Target] om uw codeaanbieding en beeldaanbieding inhoud te beheren.

1. Klikken **[!UICONTROL Offers]** de bibliotheek openen.

   De bibliotheek bevat de aanbiedingen die zijn ingesteld via [!DNL Target Standard/Premium], [!DNL Target Classic], [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) en API&#39;s. Aanbiedingen gemaakt in [!DNL Target Classic] of andere oplossingen kunnen worden bewerkt in [!DNL Target Standard/Premium].

   De [!UICONTROL Offers] De pagina heeft twee tabbladen aan de rechterkant: [!UICONTROL Code Offers] en [!UICONTROL Image Offers] Hiermee kunt u voorstellen op type weergeven.

   ![Pagina met aanbiedingen met de tabbladen Codevoorstellen en Afbeeldingsaanbiedingen](/help/main/c-experiences/c-manage-content/assets/offers-page.png)

1. (Optioneel) Klik op de knop **[!UICONTROL Type]** vervolgkeuzelijst voor het filteren van aanbiedingen op type (HTML-aanbieding, [Ervaar fragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Omleidingsvoorstel](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Externe aanbieding](/help/main/c-experiences/c-manage-content/about-remote-offers.md), [JSON-aanbiedingen](/help/main/c-experiences/c-manage-content/create-json-offer.md), en [Mappen](/help/main/c-experiences/c-manage-content/create-content-folder.md)).

   ![aanbiedingen_filter, afbeelding](assets/offers_filter.png)

1. (Optioneel) Klik op de knop **[!UICONTROL Source]** vervolgkeuzelijst voor het filteren van aanbiedingen op bron (Adobe Target, Adobe Target Classic en Adobe Experience Manager).

1. (Optioneel) Voer aanvullende taken uit door de muis boven de gewenste aanbieding of map op de [!UICONTROL Code Offers] door op het gewenste pictogram te klikken.

   ![Opties voor codeaanbiedingen](assets/offer-picker-large.png)

   U kunt onder andere de volgende opties kiezen:

   * Weergeven (zie voor meer informatie [Definities van aanbiedingen weergeven](#section_6B059DD121434E6292CAB393507D010E) hieronder.)
   * Bewerken
   * Kopiëren
   * Verplaatsen (als u bijvoorbeeld een of meer items naar een map wilt verplaatsen, klikt u op de knop **[!UICONTROL Move]** pictogram voor het gewenste item, klik op de gewenste map en klik vervolgens op **[!UICONTROL Drop]**.)
   * Verwijderen

   Afhankelijk van uw machtigingen worden mogelijk niet alle pictogrammen voor opties weergegeven. Bijvoorbeeld een gebruiker met [!UICONTROL Observer] machtigingen hebben niet de rechten om de [!UICONTROL Copy] -optie.

   Voor gedetailleerde informatie over de taken die u kunt uitvoeren op aanbiedingen en omslagen, zie [Werken met inhoud in de elementenbibliotheek](/help/main/c-experiences/c-manage-content/assets-working.md).

1. (Optioneel) Voer aanvullende taken uit door de muis boven de gewenste afbeeldingsaanbieding of map op de [!UICONTROL Image Offers] door op het gewenste pictogram te klikken.

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

De volgende aanbiedingsdefinitiekaart voor een HTML-aanbieding wordt bijvoorbeeld geopend door op het informatiepictogram te klikken:

![aanbiedingskaart-html-afbeelding](assets/offer-card-html-new.png)

De volgende informatie is beschikbaar:

* Naam
* Aanbieding-id
* Type
* Laatst gewijzigd

Klik op de knop [!UICONTROL View Full Details] link naar de inhoud van de aanbieding en de activiteiten die verwijzen naar een codeaanbieding. Op deze manier voorkomt u dat andere activiteiten worden beïnvloed tijdens het bewerken van aanbiedingen. Informatie omvat [!UICONTROL Live Activities] en [!UICONTROL Inactive Activities].

De beschikbare informatie op elke kaart varieert afhankelijk van het type aanbieding: HTML-aanbieding, [Ervaar fragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md), [Omleidingsvoorstel](/help/main/c-experiences/c-manage-content/offer-redirect.md), [Externe aanbieding](/help/main/c-experiences/c-manage-content/about-remote-offers.md), of [JSON-aanbiedingen](/help/main/c-experiences/c-manage-content/create-json-offer.md).

De functionaliteit voor details van de aanbieding is niet van toepassing op afbeeldingsaanbiedingen.

<!--

## Training video: The Content Repository ![Overview badge](/help/main/assets/overview.png)

This video includes information about managing offers.

* Connection between the [Experience Cloud Asset Library](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) and the Target Content Library 
* Custom HTML Offers 
* Custom HTML Offer in the [!UICONTROL Visual Experience Composer]

>[!VIDEO](https://video.tv.adobe.com/v/17387)

-->
