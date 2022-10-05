---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: c5445903e7bbab210d0e72200c54ab07975c21c5
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target] Standard/Premium 22.10.1 (gefaseerde release 5-7 oktober 2022)

Deze release is beschikbaar volgens het volgende schema:

* **5 oktober**: Regio Azië-Stille Oceaan (APAC)
* **6 oktober**: Amerikaanse regio
* **7 oktober**: Europa, Midden-Oosten en Afrika (EMEA)

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) fragmenten ervaren | Tot de updates voor de functie voor fragmenten met AEM ervaring behoren:<ul><li>De mogelijkheid om te filteren AEM ervaringsfragmenten op type (HTML of JSON) in de [!UICONTROL Offers] lijst. (TGT-43121)</li><li>Probleem verholpen waarbij klanten JSON konden invoegen. [!UICONTROL Experience Fragment] biedt aan wanneer het gebruiken van VEC, dat niet wordt gesteund. JSON-aanbiedingen kunnen alleen worden ingevoegd wanneer u de [!UICONTROL Form-Based Experience] composer. (TGT-43846)</li></ul>Zie AEM voor meer informatie [ervaringsfragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nieuw [!UICONTROL Visual Experience Composer] extensie voor Google Chrome | Een nieuwe [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) extensie voor Chrome is beschikbaar in de Chrome Web Store.<br>Vanaf januari 2023 wordt de huidige [!DNL Target] De extensie VEC Helper werkt niet meer in Google Chrome omdat Google extensies niet toestaat met Manifest V2. Download de nieuwe extensie om uw websites visueel te blijven ontwerpen in [!DNL Target] vanaf het nieuwe jaar.<br>De volgende koppelingen tonen de twee extensies in de Chrome Web Store:<ul><li>[Nieuwe extensie](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Oude extensie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Zie voor meer informatie [De extensie Visuele bewerkingshulp](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Geoptimaliseerde A4T-meetwaarden voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]<br>(Exacte releasedatum die moet worden bepaald.) | Houd rekening met de volgende wijzigingen:<ul><li>Extra ondersteuning voor binaire en maximalisatiemetriek in [!UICONTROL Analytics for Target] A4T-rapportage voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten</li><li>Behoud van gedrag voor bestaande activiteiten tot 20 februari 2023. Na deze datum zullen de activiteiten worden stopgezet om de migratie van bestaande activiteiten naar nieuw gedrag af te dwingen</li><li>Vanaf 20 februari 2023, ondersteuning voor `averagetimespentonsite`, `bouncerate`, en `entries` maatstaven in [!DNL Target] de activiteiten zullen worden afgekeurd .</li></ul> |

* Probleem verholpen waardoor de publieksregelgegevens niet correct konden worden weergegeven in het dialoogvenster [!UICONTROL Audiences Refinements] informatievenster. (TGT-43917)
* De prestaties van de [!DNL Target] UI bij het laden van publiek dat de [aanbevolen limiet voor doelgroepregels](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* Probleem verholpen waarbij sommige componenten niet correct werden weergegeven in het dialoogvenster [!UICONTROL Modifications] op het [!UICONTROL Experiences] pagina wanneer het creëren van of het uitgeven van activiteiten in VEC na omschakeling van [!UICONTROL Compose] tot [!UICONTROL Browse] in. (TGT-43300)
* Probleem verholpen waardoor sommige klanten niet konden archiveren [!UICONTROL A/B Test] activiteiten die [!UICONTROL Auto-Target]. (TGT-40978)
* De mogelijkheid toegevoegd om automatisch één aanbieding te gebruiken op meerdere locaties binnen één rapportagegroep. (TGT-40689)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie voor meer informatie [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Zie voor meer informatie [Opmerkingen bij de release van vorige releases](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie voor meer informatie [Opmerkingen bij de release Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie [Opmerkingen bij de doelversie - Prerelease](/help/main/r-release-notes/target-release-notes.md) pagina. |
