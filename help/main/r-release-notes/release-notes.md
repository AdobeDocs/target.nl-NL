---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;oplossingen;foutoplossingen;updates
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van  [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van [!DNL Adobe Target].
short-description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: b06cc6f4a8e7d1617dd5d3a8226e2b77474cfe77
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 8%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target] Standard/Premium 23.5.2 (31 mei 2023)

Deze versie bevat de volgende verbeteringen en oplossingen:

| Functie | Details |
|--- |--- |
| Real-Time CDP-profielkenmerken die worden gedeeld met [!DNL Target] | [!UICONTROL Real-Time CDP Profile Attributes] kan worden gedeeld met [!DNL Target] voor gebruik in HTML- en JSON-aanbiedingen.<P>Zie voor meer informatie [Real-Time CDP-profielkenmerken delen met [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes). |

* Probleem verholpen waarbij een lege pagina werd weergegeven terwijl een API-autorisatietoken voor profielen werd gegenereerd. (TGT-45387 &amp; TGT-45423)
* Probleem verholpen waarbij een afbeelding niet kon worden weergegeven in het dialoogvenster [!UICONTROL Create Design] als de afbeeldingsnaam 18030 GB tekens bevat. (TGT-44614)
* Probleem verholpen waarbij tekst/HTML ten onrechte werd beschermd tegen sommige GB 18030-symbooltekens. (TGT-44600)
* Probleem verholpen waarbij rapporten werden gegenereerd voor [!UICONTROL Auto Personalization] activiteiten om tijdens de analyse te bevriezen. (TGT-44820)
* Probleem verholpen waardoor het zoeken naar een activiteit op de [!UICONTROL Activity] pagina als de naam van de activiteit een vierkant haakje bevat ( [ of ] ). (TGT-44777)
* Probleem verholpen waardoor een activiteit niet kon worden gesynchroniseerd als het doel van de activiteit speciale tekens bevat. (TGT-44982)
* Probleem opgelost waarbij geen activiteiten werden weergegeven in het dialoogvenster [!DNL Target] UI voor de Standaardwerkruimte voor bepaalde klanten. (TGT-45286)
* De werking van de markering Duplicaten niet toestaan is bijgewerkt. Markten voor uitgesloten herhalingsaanbiedingen worden bijgewerkt om herhalende aanbiedingen toe te staan als deze de standaardinhoudsaanbieding zijn (voor API&#39;s v3, v4) en om dubbele opties toe te staan als de opties verwijzen naar de standaardinhoudsaanbieding en geen sjablonen hebben gedefinieerd. (TNT-46617)
* Probleem verholpen waarbij een queryparameter werd toegevoegd aan een URL waardoor de pagina niet kon worden geladen in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC). (TGT-44873)
* Verschillende lokalisatieoplossingen in de hele [!DNL Target] UI.

## [!DNL Target] Standard/Premium 23.5.1 (23-25 mei 2023)

Deze release is beschikbaar volgens het volgende schema:

23 mei: Europa, Midden-Oosten en Afrika (EMEA) 24 mei: Regio Azië-Stille Oceaan (APAC) 25 mei: Amerikaanse regio

Deze release bevat de volgende nieuwe verbeteringen en oplossingen:

* Probleem verholpen waardoor bepaalde klanten geen publiek konden maken met bezoekersprofielen met de operatoren &quot;groter dan&quot; of &quot;kleiner dan&quot;. (TGT-45271)
* Verschillende lokalisatieoplossingen in de hele [!DNL Target] UI.
* De interface van het Doel is op verschillende plaatsen bijgewerkt voor een komende UI (de veranderingen zijn achter een eigenschapvlag tot de updates worden vrijgegeven).

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [Opmerkingen bij de release van vorige releases](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium. |
| [Aanvullende informatie over Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| [Adobe Priority-productupdate](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen. |
| [Opmerkingen bij de doelversie - Prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
