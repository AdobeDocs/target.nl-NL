---
keywords: inhoud;elementen;inhoud beheren;aanbiedingen;elementen beheren;selectiemodus openen;selectiemodus
description: Ontdek hoe u code- en afbeeldingsaanbiedingen efficiënt kunt beheren met de [!UICONTROL Offers] -bibliotheek. Leer beste praktijken en tips om uw werkschema te stroomlijnen en uw projecten te verbeteren.
title: Hoe kan ik code- en afbeeldingsaanbiedingen beheren?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn de eigenschappen van Beta in  [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: f64aec3d-5f83-4bd1-8e64-df1779809812
source-git-commit: 74dbbb2f56e62c2c5595497c7ae1e264f9ffd9d4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Aanbiedingen

Ontdek hoe u code- en afbeeldingsaanbiedingen efficiënt kunt beheren met de [!UICONTROL Offers] -bibliotheek in [!DNL Adobe Target] .

>[!NOTE]
>
>Dit artikel bevat informatie over updates van de gebruikersinterface van [!DNL Target] die momenteel deel uitmaakt van een Beta-programma. Het team van [!DNL Adobe Target] laat vaak nieuwe eigenschappen voor bepaalde klanten voor het testen en terugkoppelen doeleinden toe. Nadat de testperiode is voltooid, worden deze functies in toekomstige versies van [!DNL Target Standard/Premium] voor alle klanten ingeschakeld en in releaseopmerkingen aangekondigd.

Als u de [!UICONTROL Offers] -bibliotheek wilt weergeven, klikt u op het tabblad **[!UICONTROL Offers]** boven aan de gebruikersinterface van [!DNL Target] .

![ pagina van Aanbiedingen ](/help/main/c-experiences/c-manage-content/assets/offers-page-new.png)

De [!UICONTROL Offers] -bibliotheek bevat aanbiedingen die zijn ingesteld via [!DNL Target Standard/Premium] , [!DNL Target Classic] , [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] (AMS) en API&#39;s. Aanbiedingen die zijn gemaakt in [!DNL Target Classic] of andere oplossingen, kunnen worden bewerkt in [!DNL Target Standard/Premium] .

De [!UICONTROL Offers] -bibliotheek biedt een overzicht van alle code en afbeeldingsaanbiedingen en biedt u de mogelijkheid verschillende handelingen uit te voeren:

| Element | Beschrijving |
|--- |--- |
| Linkernavigatieregel | Schakel tussen het weergeven van [!UICONTROL Code Offers] of [!UICONTROL Image Offers] . |
| [!UICONTROL Show filters] pictogram<P>![ toon Filters pictogram ](/help/main/assets/icons/Filter.svg) | Klik op het pictogram **[!UICONTROL Show filters]** om aanbiedingen te filteren op [!UICONTROL Type] , [!UICONTROL Source] en [!UICONTROL AEM Type] .<P>Voor meer informatie, zie [ filters op de lijst van Aanbiedingen ](#filters) hieronder toepassen. |
| Zoeken in velden | Gebruik de velden **[!UICONTROL Search in]** om snel een aanbieding te vinden of om het aantal aanbiedingen dat wordt weergegeven in de [!UICONTROL Offers] -bibliotheek te verminderen. U kunt zoeken op [!UICONTROL Offer Name] , [!UICONTROL AEM Paths] of [!UICONTROL AEM Tags] . |
| [!UICONTROL Create Folder] | Klik op **[!UICONTROL Create Folder]** om mappen in de [!UICONTROL Offer] -bibliotheek te maken voor de opslag van codeaanbiedingen, afbeeldingsaanbiedingen en andere mappen om een submapstructuur te maken.<P>Voor meer informatie, zie [ aanbiedingsomslagen ](/help/main/c-experiences/c-manage-content/create-content-folder.md) creëren. |
| [!UICONTROL [!UICONTROL Create Offer]] | Klik op **[!UICONTROL Create Offer]** om een aanbieding te maken.<P>Zie voor meer informatie over het maken van de verschillende soorten aanbiedingen: <ul><li>HTML-aanbod</li><li>[ Aanbieding JSON ](/help/main/c-experiences/c-manage-content/create-json-offer.md)</li><li>[ Redirect Aanbieding ](/help/main/c-experiences/c-manage-content/offer-redirect.md)</li><li>[ Verre Aanbieding ](/help/main/c-experiences/c-manage-content/about-remote-offers.md)</li></ul> |
| Selectievakjes voor bulkbewerkingen<P>![ het pictogram van Verrichtingen van het Bulk ](/help/main/assets/icons/Selection.svg) | Klik op de selectievakjes [!UICONTROL Bulk Operations] om bulkbewerkingen uit te voeren op alle activiteiten of op geselecteerde activiteiten.<P>Voor een lijst van acties die (afhankelijk van uw toestemmingen en de aanbiedingsstatus) beschikbaar zijn, zie [ snelle acties ](#quick-actions) hieronder uitvoeren. |
| [!UICONTROL Name] | De naam van elke aanbieding.<P>Klik het **[!UICONTROL Quick Info]** pictogram ( ![ Snelle pictogram van Info ](/help/main/assets/icons/InfoOutline.svg)) naast elke aanbiedingsnaam om meer informatie over die aanbieding in een pop-up kaart, met inbegrip van aanbiedingsidentiteitskaart, type, datum te bekijken de aanbieding, laatst gewijzigd en door wie, en meer.<p>Klik het **[!UICONTROL More Actions]** pictogram ( ![ Meer pictogram van Acties ](/help/main/assets/icons/MoreSmallList.svg)) naast elke aanbiedingsnaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren. De volgende handelingen zijn beschikbaar (afhankelijk van uw machtigingen en de status van het aanbod): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] en [!UICONTROL Move] . Voor meer informatie over elke actie, zie [ snelle acties ](#quick-actions) hieronder uitvoeren.<P>Klik op de tabelkop om de lijst alfabetisch te sorteren in oplopende of aflopende volgorde op naam. |
| [!UICONTROL Type] | Het aanbiedingstype: [!UICONTROL HTML Offers], [[!UICONTROL Redirect Offers]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offers]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) en [[!UICONTROL JSON Offers]](/help/main/c-experiences/c-manage-content/create-json-offer.md). |
| [!UICONTROL Source] | Toont waar de aanbieding is gemaakt: [!DNL Adobe Target], [!DNL Adobe Target Classic] en [!DNL Adobe Experience Manager] . |

## Filters toepassen op de bibliotheek met aanbiedingen {#filters}

Klik het **[!UICONTROL Show filters]** pictogram ( ![ toon het pictogram van Filters op de pagina van Aanbiedingen ](/help/main/assets/icons/Filter.svg)) aan filteraanbiedingen door [!UICONTROL Type], [!UICONTROL Source], en [!UICONTROL AEM Type].

Met het pictogram **[!UICONTROL Show filters]** kunt u aanbiedingen filteren op de volgende categorieën:

* **[!UICONTROL Type]** : [!UICONTROL HTML Offer] , [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md) , [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) en [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md) .

* **[!UICONTROL Source]** : [!DNL Adobe Target] , [!DNL Adobe Target Classic] en [!DNL Adobe Experience Manager] .

* **AEM Type**: [ de Fragmenten van de Inhoud ](/help/main/c-integrating-target-with-mac/aem/content-fragments-aem.md) en [ de Fragmenten van de Ervaring ](/help/main/c-integrating-target-with-mac/aem/experience-fragments-aem.md). Voor meer informatie over de verschillende fragmenttypes, zie [ AEM het Overzicht van de Fragmenten van de Ervaring en van de Fragmenten van de Inhoud ](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Snelle handelingen uitvoeren {#quick-actions}

U kunt de volgende snelle acties uitvoeren door op het juiste pictogram te klikken:

### Snelle informatie

Klik het **[!UICONTROL Quick Info]** pictogram ( ![ Snelle pictogram van Info ](/help/main/assets/icons/InfoOutline.svg)) naast elke aanbiedingsnaam om meer informatie over die aanbieding in een pop-up kaart, met inbegrip van aanbiedingsidentiteitskaart, type, datum te bekijken de aanbieding het laatst werd gewijzigd en door wie, en meer. Welke opties beschikbaar zijn, is afhankelijk van het aanbiedingstype: [!UICONTROL HTML Offer], [[!UICONTROL JSON Offer]](/help/main/c-experiences/c-manage-content/create-json-offer.md), [[!UICONTROL Redirect Offer]](/help/main/c-experiences/c-manage-content/offer-redirect.md), [[!UICONTROL Remote Offer]](/help/main/c-experiences/c-manage-content/about-remote-offers.md) .

### Meer handelingen

De beschikbare acties voor Codevoorstellen en voor Afbeeldingsaanbiedingen verschillen enigszins. De volgende secties bevatten meer informatie:

#### [!UICONTROL Code Offer] opties

Klik het **[!UICONTROL More actions]** pictogram ( ![ Meer pictogram van Acties ](/help/main/assets/icons/MoreSmallList.svg)) naast elke aanbiedingsnaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren.

De volgende handelingen zijn beschikbaar (afhankelijk van uw machtigingen en de status van het aanbod): [!UICONTROL Edit], [!UICONTROL Copy], [!UICONTROL Delete] en [!UICONTROL Move] .

* [!UICONTROL Edit]
* [!UICONTROL Copy]
* [!UICONTROL Delete]
* [!UICONTROL Move] (Als u bijvoorbeeld een of meer items naar een map wilt verplaatsen, klikt u op het pictogram **[!UICONTROL Move]** voor het gewenste item, klikt u op de gewenste map en vervolgens op **[!UICONTROL Drop]** .)

Afhankelijk van uw machtigingen worden mogelijk niet alle pictogrammen voor opties weergegeven. Een gebruiker met [!UICONTROL Observer] -machtigingen heeft bijvoorbeeld niet de rechten om de optie [!UICONTROL Copy] te gebruiken.

Voor gedetailleerde informatie over de taken kunt u op aanbiedingen en omslagen uitvoeren, zie [ Werk met inhoud in de bibliotheek van Activa ](/help/main/c-experiences/c-manage-content/assets-working.md).

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

Voor gedetailleerde informatie over de taken kunt u op aanbiedingen en omslagen uitvoeren, zie [ Werk met inhoud in de bibliotheek van Activa ](/help/main/c-experiences/c-manage-content/assets-working.md).

>[!NOTE]
>
>De aanbiedingen van het beeld maken geen deel uit van het ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) model van de Toestemmingen van de Gebruiker van de Onderneming [.

## Definities van aanbiedingen weergeven {#section_6B059DD121434E6292CAB393507D010E}

Om de details van de aanbiedingsdefinitie op een pop-up kaart in de [!UICONTROL Offers] bibliotheek te bekijken zonder de aanbieding te openen, klik het ( ![ Snelle pictogram van Info ](/help/main/assets/icons/InfoOutline.svg)).

De volgende informatie is beschikbaar:

* [!UICONTROL Name]
* [!UICONTROL Source]
* [!UICONTROL Offer ID]
* [!UICONTROL Type]
* [!UICONTROL Last Modified]
* [!UICONTROL Offer path]


Klik op de koppeling [!UICONTROL View Full Details] om de kenmerken en activiteiten van de aanbieding te bekijken die verwijzen naar een codeaanbieding in de definitie-pop-upkaart van elke aanbieding. Deze functionaliteit is niet van toepassing op afbeeldingsaanbiedingen. Op deze manier voorkomt u dat andere activiteiten worden beïnvloed tijdens het bewerken van aanbiedingen. Deze informatie bevat gegevens voor [!UICONTROL Live Activities] en [!UICONTROL Inactive Activities] .
