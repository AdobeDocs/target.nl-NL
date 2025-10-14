---
keywords: inhoud;elementen;inhoud beheren;aanbiedingen;elementen beheren;selectiemodus openen;selectiemodus
description: Ontdek hoe u code- en afbeeldingsaanbiedingen efficiënt kunt beheren met de [!UICONTROL Offers] -bibliotheek.
title: Hoe kan ik code- en afbeeldingsaanbiedingen beheren?
feature: Experiences and Offers
exl-id: d8c24656-64d6-4a4b-a5f2-bcde57180007
source-git-commit: f034aba7fe4f54b937dee0846140af140052694c
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---

# Aanbiedingen

Ontdek hoe u code- en afbeeldingsaanbiedingen efficiënt kunt beheren met de [!UICONTROL Offers] -bibliotheek in [!DNL Adobe Target] .

Als u de [!UICONTROL Offers] -bibliotheek wilt weergeven, klikt u op het tabblad **[!UICONTROL Offers]** boven aan de gebruikersinterface van [!DNL Target] .

![&#x200B; pagina van Aanbiedingen &#x200B;](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

De [!UICONTROL Offers] -bibliotheek bevat aanbiedingen die zijn ingesteld via [!DNL Target Standard/Premium] , [!DNL Target Classic] , [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) en API&#39;s. Aanbiedingen die zijn gemaakt in [!DNL Target Classic] of andere oplossingen, kunnen worden bewerkt in [!DNL Target Standard/Premium] .

De [!UICONTROL Offers] -bibliotheek biedt een overzicht van alle code en afbeeldingsaanbiedingen en biedt u de mogelijkheid verschillende handelingen uit te voeren:

| Element | Beschrijving |
|--- |--- |
| Linkernavigatieregel | Schakel tussen het weergeven van [!UICONTROL Code Offers] of [!UICONTROL Image Offers] . |
| [!UICONTROL Show Folders] / [!UICONTROL Hide Folders]<P>![&#x200B; toon Filters/verberg Filters pictogram &#x200B;](/help/main/assets/icons/RailLeft.svg) | Klik op het pictogram **[!UICONTROL Show Folders]** of **[!UICONTROL Hide Folders]** om te schakelen tussen het weergeven van de mappenstructuur voor aanbiedingen of het niet weergeven van de mappenstructuur.<P>Voor meer informatie, zie [&#x200B; aanbiedingsomslagen &#x200B;](/help/main/c-experiences/c-manage-content/create-content-folder.md) creëren. |
| [!UICONTROL Show filters] pictogram<P>![&#x200B; toon Filters pictogram &#x200B;](/help/main/assets/icons/Filter.svg) | Klik op het pictogram **[!UICONTROL Show filters]** om aanbiedingen te filteren op [!UICONTROL Type] , [!UICONTROL Source] en [!UICONTROL AEM Type] .<P>Voor meer informatie, zie [&#x200B; filters op de lijst van Aanbiedingen &#x200B;](#filters) hieronder toepassen. |
| Zoeken in velden | Gebruik de velden **[!UICONTROL Search in]** om snel een aanbieding te vinden of om het aantal aanbiedingen dat wordt weergegeven in de [!UICONTROL Offers] -bibliotheek te verminderen. U kunt zoeken op [!UICONTROL Offer Name] , [!UICONTROL AEM Paths] of [!UICONTROL AEM Tags] . Zoekopties zijn sessiedoneel. |
| [!UICONTROL Create Folder] | Klik op **[!UICONTROL Create Folder]** om mappen in de [!UICONTROL Offer] -bibliotheek te maken voor de opslag van codeaanbiedingen, afbeeldingsaanbiedingen en andere mappen om een submapstructuur te maken.<P>Voor meer informatie, zie [&#x200B; aanbiedingsomslagen &#x200B;](/help/main/c-experiences/c-manage-content/create-content-folder.md) creëren. |
| [!UICONTROL [!UICONTROL Create Offer]] | Klik op **[!UICONTROL Create Offer]** om een aanbieding te maken.<P>Zie voor meer informatie over het maken van de verschillende soorten aanbiedingen: <ul><li>HTML-voorstel</li><li>[&#x200B; Aanbieding JSON &#x200B;](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[&#x200B; Redirect Aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[&#x200B; Verre Aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Selectievakjes voor bulkbewerkingen<P>![&#x200B; het pictogram van Verrichtingen van het Bulk &#x200B;](/help/main/assets/icons/Rectangle.svg) | Klik op de selectievakjes [!UICONTROL Bulk Operations] om bulkbewerkingen uit te voeren op alle aanbiedingen of op geselecteerde aanbiedingen.<P>Voor een lijst van acties die (afhankelijk van uw toestemmingen en de aanbiedingsstatus) beschikbaar zijn, zie [&#x200B; snelle acties &#x200B;](#quick-actions) hieronder uitvoeren. |
| [!UICONTROL Name] | De naam van elke aanbieding.<P>Klik het **[!UICONTROL Quick Info]** pictogram ( ![&#x200B; Snelle pictogram van Info &#x200B;](/help/main/assets/icons/InfoOutline.svg)) naast elke aanbiedingsnaam om meer informatie over die aanbieding in een pop-up kaart, met inbegrip van aanbiedingsidentiteitskaart, type, datum te bekijken de aanbieding het laatst werd gewijzigd en door wie, en meer.<p>Klik het **[!UICONTROL More Actions]** pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) naast elke aanbiedingsnaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren. De volgende handelingen zijn beschikbaar (afhankelijk van uw machtigingen en de status van het aanbod): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] en [!UICONTROL Move] . Voor meer informatie over elke actie, zie [&#x200B; snelle acties &#x200B;](#quick-actions) hieronder uitvoeren.<P>Klik op de tabelkop om de lijst alfabetisch te sorteren in oplopende of aflopende volgorde op naam. |
| [!UICONTROL Type] | Het aanbiedingstype: [!UICONTROL HTML Offers], [[!UICONTROL Redirect Offers]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offers]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) en [[!UICONTROL JSON Offers]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Toont waar de aanbieding is gemaakt: [!DNL Adobe Target], [!DNL Adobe Target Classic] en [!DNL Adobe Experience Manager] . |
| [!UICONTROL Last updated] | Geeft de datum en tijd weer waarop de aanbieding voor het laatst is gewijzigd en door wie.<P>Klik op de tabelkop om de lijst op datum in oplopende of aflopende volgorde te sorteren. |

## Filters toepassen op de bibliotheek met aanbiedingen {#filters}

Klik het **[!UICONTROL Show filters]** pictogram ( ![&#x200B; toon het pictogram van Filters op de pagina van Aanbiedingen &#x200B;](/help/main/assets/icons/Filter.svg)) aan filteraanbiedingen door [!UICONTROL Type], [!UICONTROL Source], en [!UICONTROL AEM Type].

Met het pictogram **[!UICONTROL Show filters]** kunt u aanbiedingen filteren op de volgende categorieën:

* **[!UICONTROL Type]** : [!UICONTROL HTML Offer] , [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md) , [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) en [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md) .

* **[!UICONTROL Source]** : [!DNL Adobe Target] , [!DNL Adobe Target Classic] en [!DNL Adobe Experience Manager] .

* **Type van AEM**: [&#x200B; de Fragmenten van de Inhoud &#x200B;](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) en [&#x200B; de Fragmenten van de Ervaring &#x200B;](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Voor meer informatie over de verschillende fragmenttypes, zie [&#x200B; de Fragmenten van de Ervaring van AEM en het overzicht van de Fragmenten van de Inhoud &#x200B;](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

Filters zijn sessiepermanent.

## Snelle handelingen uitvoeren {#quick-actions}

U kunt de volgende snelle acties uitvoeren door op het juiste pictogram te klikken:

### Snelle informatie

Klik het **[!UICONTROL Quick Info]** pictogram ( ![&#x200B; Snelle pictogram van Info &#x200B;](/help/main/assets/icons/InfoOutline.svg)) naast elke aanbiedingsnaam om meer informatie over die aanbieding in een pop-up kaart, met inbegrip van aanbiedingsidentiteitskaart, type, datum te bekijken de aanbieding het laatst werd gewijzigd en door wie, en meer. Welke opties beschikbaar zijn, is afhankelijk van het aanbiedingstype: [!UICONTROL HTML Offer], [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) .

### Meer handelingen

De beschikbare acties voor [!UICONTROL Code Offers] en voor [!UICONTROL Image Offers] verschillen enigszins. De volgende secties bevatten meer informatie:

#### [!UICONTROL Code Offer] opties

Klik het **[!UICONTROL More actions]** pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) naast elke aanbiedingsnaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren.

De volgende acties zijn beschikbaar (afhankelijk van uw machtigingen en de status van het aanbod):

* [!UICONTROL Edit]
* [!UICONTROL Copy]
* [!UICONTROL Delete]
* [!UICONTROL Move] (Als u bijvoorbeeld een of meer items naar een map wilt verplaatsen, klikt u op **[!UICONTROL Move]** naast het gewenste item, klikt u op de gewenste map en vervolgens op **[!UICONTROL Move]** .)

Afhankelijk van uw machtigingen worden mogelijk niet alle pictogrammen voor opties weergegeven. Een gebruiker met [!UICONTROL Observer] -machtigingen heeft bijvoorbeeld niet de rechten om de optie [!UICONTROL Copy] te gebruiken.

Voor gedetailleerde informatie over de taken kunt u op aanbiedingen en omslagen uitvoeren, zie [&#x200B; Werk met inhoud in de bibliotheek van Activa &#x200B;](/help/main/c-experiences/c-manage-content/assets-working.md).

#### [!UICONTROL Image Offer] opties

Voer aanvullende taken uit door de muisaanwijzer boven de gewenste afbeeldingsaanbieding of -map op het tabblad [!UICONTROL Image Offers] te houden en vervolgens op het gewenste pictogram te klikken.

U kunt onder andere de volgende opties kiezen:

* [!UICONTROL Select]
* [!UICONTROL Download]
* [!UICONTROL View Properties]
* [!UICONTROL More Actions]
* [!UICONTROL Edit]
* [!UICONTROL Annotate]
* [!UICONTROL Copy]

Voor gedetailleerde informatie over de taken kunt u op aanbiedingen en omslagen uitvoeren, zie [&#x200B; Werk met inhoud in de bibliotheek van Activa &#x200B;](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>De aanbiedingen van het beeld maken geen deel uit van het [&#x200B; model van de Toestemmingen van de Gebruiker van de Onderneming &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

## Definities van aanbiedingen weergeven {#section_6B059DD121434E6292CAB393507D010E}

Om de details van de aanbiedingsdefinitie op een pop-up kaart in de [!UICONTROL Offers] bibliotheek te bekijken zonder de aanbieding te openen, klik het ( ![&#x200B; Snelle pictogram van Info &#x200B;](/help/main/assets/icons/InfoOutline.svg)).

De volgende informatie is beschikbaar:

* [!UICONTROL Name]
* [!UICONTROL Offer ID]
* [!UICONTROL Type]
* [!UICONTROL Last Modified]

Klik op de koppeling [!UICONTROL View Full Details] om de kenmerken en activiteiten van de aanbieding te bekijken die verwijzen naar een codeaanbieding in de definitie-pop-upkaart van elke aanbieding. Deze functionaliteit is niet van toepassing op afbeeldingsaanbiedingen. Op deze manier voorkomt u dat andere activiteiten worden beïnvloed tijdens het bewerken van aanbiedingen. Deze informatie bevat gegevens voor [!UICONTROL Live Activities] en [!UICONTROL Inactive Activities] .
