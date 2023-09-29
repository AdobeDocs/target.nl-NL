---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;oplossingen;foutoplossingen;updates
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van  [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van [!DNL Adobe Target].
short-description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 2e15709ac2a34a96dbc632c71f400c2575d74cf4
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 6%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target] Standard/Premium 23.9.4 (2-4 oktober 2023)

Deze release is beschikbaar volgens het volgende schema voor gefaseerde installatie:

* **2 oktober** Betreft: Europa, Midden-Oosten en Afrika (EMEA)
* **3 oktober**: Amerikaanse regio
* **4 oktober**: regio Azië-Stille Oceaan (APAC)

Deze versie bevat de volgende verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| [!UICONTROL Activities] UI vernieuwen<P>en<P>[!UICONTROL Feeds] UI vernieuwen | Als onderdeel van het [!DNL Adobe Target] de voortdurende inspanning van het team om de gebruiker-ervaring voor te verbeteren [!DNL Target] gebruikers, deze versie vernieuwt de [!UICONTROL Activities] en [!DNL Recommendations] [!UICONTROL Feeds] pagina&#39;s in het dialoogvenster [!DNL Target] UI. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen.<P>Zie voor meer informatie [Activiteiten](/help/main/c-activities/activities.md) en [Feeds](/help/main/c-recommendations/c-products/feeds.md). |
| [!DNL Recommendations] implementatiepatroon | De *Recommendations-implementatiepatroon met behulp van at.js* artikelen helpen u uw [!DNL Adobe Target Recommendations] implementatie bij gebruik van de JavaScript-bibliotheek at.js.<P>Zie voor algemene informatie over doelpatronen [Overzicht van implementatiepatronen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/pattern-overview.html){target=_blank} in de *Adobe Target Developer Guide*.<P>Het nieuwe Recommendations-implementatiepatroon bestaat uit de volgende artikelen:<ul><li>[Recommendations-implementatiepatroon met behulp van at.js-overzicht](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/recs-implementation-pattern-atjs.html){target=_blank}</li><ul><li>[SDK&#39;s initialiseren](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/initialize-sdk.html){target=_blank}</li><li>[Gegevensverzameling configureren](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/data-collection.html){target=_blank}</li><li>[Renderervaringen](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/render-experiences.html?lang=en){target=_blank}</li><li>[Waarschuwen [!DNL Target]](https://experienceleague.adobe.com/docs/target-dev/developer/implementation-patterns/atjs/notify-target.html?lang=en){target=_blank}</li></ul></ul> |

* Toegevoegd [!UICONTROL Visual Experience Composer] (VEC) Verbeteringen voor dynamische kaders. (TGT-44064)
* Het probleem dat de geselecteerde datum veroorzaakte in het dialoogvenster `getViewInAnalyticsId` verzoek om niet correct bij te werken. Met deze correctie kunt u de [!DNL Analytics] koppeling in rapportage wanneer het datumbereik en de instellingen van het metriekrapport zijn gewijzigd. (TGT-46246)

## [!DNL Target] Standard/Premium 23.9.3 (18 september 2023)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Verbeterde het [!UICONTROL Visual Experience Composer] (VEC) ter ondersteuning van Lightning Web Components (Light DOM). (TGT-45422)
* Probleem opgelost waarbij VEC-handelingen in de onjuiste volgorde werden toegepast. In sommige gevallen paste VEC sommige wijzigingen asynchroon toe en het toevoegen van extra aanpassingen aan een element veroorzaakte fouten als dat element na een [!UICONTROL Insert] handeling. Hiermee corrigeert u ook de VEC-URL die nu wordt bijgewerkt wanneer u op ankerkoppelingen klikt. (TGT-45983)
* Probleem opgelost met VEC [!UICONTROL Overlay] -functie, die nu elementen in DOM&#39;s met schaduw ondersteunt. (TGT-45202 &amp; TGT-45262)
* Probleem verholpen bij het openen van een toepassingspagina voor één pagina (SPA) in de VEC en vervolgens naar [!UICONTROL Browse] De modus voor de pijlen Vorige en Volgende functioneren niet correct. (TGT-45956)
* Probleem verholpen waardoor sommige webpagina&#39;s niet in de VEC konden worden geladen. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (12-14 september 2023)

Deze release is beschikbaar volgens het volgende schema voor gefaseerde installatie:

* **12 september**: Amerikaanse regio
* **13 september**: regio Azië-Stille Oceaan (APAC)
* **14 september** Betreft: Europa, Midden-Oosten en Afrika (EMEA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* De [!DNL Analytics] API voor de nieuwe [!DNL Analytics] API versie 2.0. (TGT-45345)
* Opgeloste problemen met gevolgen [!UICONTROL Automated Personalization] (AP) activiteiten voor sommige klanten, met inbegrip van het tijdig synchroniseren van de activiteit op [!DNL Target] back-end maken en de verwachte ervaring bieden met voorvertoningskoppelingen. (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (6-11 september 2023)

Deze release is beschikbaar volgens het volgende schema voor gefaseerde installatie:

* **6 september**: Amerikaanse regio
* **7 september** Betreft: Europa, Midden-Oosten en Afrika (EMEA)
* **11 september**: regio Azië-Stille Oceaan (APAC)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen waarbij inconsistente rapportgegevens in het dialoogvenster [!DNL Target] UI en de [!DNL Adobe Analytics] UI voor [!UICONTROL Auto-Allocate] activiteiten die [!UICONTROL Analytics for Target] (A4T) als bron van rapportage. (TGT-46112)
* De time-out voor aanroepen van PUTTEN naar de API voor doellevering is verhoogd tot 15 seconden om time-outfouten te voorkomen. (TGT-46091)
* Probleem verholpen waardoor de URL niet constant kon worden bijgewerkt wanneer er door een website van de toepassing Eén pagina (SPA) werd gebladerd. (TGT-45417)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details at.js-versie](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [Opmerkingen bij de release van vorige releases](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium. |
| [Aanvullende informatie over Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [Adobe Prioriteit productupdate](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen. |
| [Opmerkingen bij de doelversie - Prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
