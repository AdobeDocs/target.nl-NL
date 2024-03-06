---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;oplossingen;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
short-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 784f41a73941877135a5902f2331972ba9d0e880
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## Updates voor `Browser:iPad` en `Browser:iPhone` in [!UICONTROL Browser] attributen voor het publiek (30 april 2024)

| Updates | Details |
|--- |--- |
| [!UICONTROL Browser:iPad] en [!UICONTROL Browser:iPhone] bijgewerkt in [Browserkenmerken](/help/main/c-target/c-audiences/c-target-rules/browser.md) gebruikt bij het maken van soorten publiek. | [!DNL Adobe Target] laat u [doel op een van de verschillende categoriekenmerken](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), met inbegrip van bezoekers die een specifieke [browser- of browseropties](/help/main/c-target/c-audiences/c-target-rules/browser.md) wanneer ze uw pagina bezoeken.<P>Beginnen met de [!DNL Target] Standard/Premium 24.3.1 (4-6 maart 2024), ingebouwde doelgroepen, zoals `Browser:iPad` en `Browser:iPhone` wordt bijgewerkt om de juiste doelversie uit te voeren voor [!DNL iPad] en [!DNL iPhone] gebruiken `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` en `profile.mobile.isTablet`.<P>Deze update vereist geen actie aan de kant van de klanten.<p><B>Belangrijk</b>: Voor klanten om het juiste richten uit te voeren voor [!DNL iPad] en [!DNL iPhone] in profielscripts (en JavaScript-segmenten) moet de klant handmatig wijzigingen aanbrengen door **30 april 2024**. Voor voorbeelden van alternatieve instellingen die handmatig moeten worden gewijzigd, raadpleegt u [Updates voor [!DNL iPad] en [!DNL iPhone] in [!UICONTROL Browser] publiekskenmerken](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

## [!DNL Target] Standard/Premium 24.3.1 (4-6 maart 2024)

Deze release is gepland voor de volgende dagen:

* **4 maart** Betreft: Europa, Midden-Oosten en Afrika (EMEA)
* **5 maart**: regio Azië-Stille Oceaan (APAC)
* **6 maart**: Amerikaanse regio

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen met de logica die het aantal unieke kiezers in een activiteit berekent. (TGT-47878)
* Probleem verholpen dat ertoe heeft geleid [!UICONTROL Multivariate] (MVT) activiteiten geconfigureerd met [!UICONTROL Analytics for Target] (A4T) rapporteren om niet correct weer te geven. (TGT-47490)
* Verbeterde het waarschuwingsbericht dat in het melden wordt getoond wanneer een ervaring zonder verkeer als controleervaring wordt gebruikt. (TGT-47537)
* Er zijn veel oplossingen toegevoegd voor backend en lokalisatie.

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details at.js-versie](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [Opmerkingen bij de release van vorige releases](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium. |
| [Opmerkingen bij de release van Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [Adobe Prioriteit productupdate](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen. |
| [Opmerkingen bij de doelversie - Prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
