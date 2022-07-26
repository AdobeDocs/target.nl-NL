---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5566393192b131b837fece1bb2a6781e2f953190
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## Models API-release (23 november 2022)

De nieuwe [!DNL Adobe Target] De model API, ook genoemd de Lijst van gewezen personen API, laat gebruikers de lijst van eigenschappen bekijken en beheren die in machine het leren modellen worden gebruikt voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten.

Zie voor meer informatie [Modellen API - Overzicht](https://developer.adobe.com/target/before-administer/models-api/){target=_blank} in het dialoogvenster *Adobe Target Developer Guide*.

## [!DNL Target] Standard/Premium 22.10.3 (gefaseerde release 25-27 oktober 2022)

Deze release is beschikbaar volgens het volgende schema:

* **25 oktober**: Europa, Midden-Oosten en Afrika (EMEA)
* **26 oktober**: Regio Azië-Stille Oceaan (APAC)
* **27 oktober**: Amerikaanse regio

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| Geoptimaliseerde A4T-meetwaarden voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]<br>(Beschikbaar om klanten te selecteren voor testen. In een toekomstige release beschikbaar voor alle klanten.) | Houd rekening met de volgende wijzigingen:<ul><li>Toegevoegde steun voor niet binaire en maximalisatiemetriek in [!UICONTROL Analytics for Target] A4T-rapportage voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten</li><li>Behoud van gedrag voor bestaande activiteiten tot februari 2023. Na deze datum zullen de activiteiten worden stopgezet om de migratie van bestaande activiteiten naar nieuw gedrag af te dwingen</li><li>Vanaf 20 februari 2023, ondersteuning voor `averagetimespentonsite`, `bouncerate`, en `entries` maatstaven in [!DNL Target] de activiteiten zullen worden afgekeurd .</li></ul> |

* Extra knopinfo in het dialoogvenster [!DNL Target] UI om klanten te helpen efficiënter navigeren de publieksbouwer en te leren hoe te om eigenschappen te gebruiken die onvertrouwd zouden kunnen zijn. (TGT-44139)
* Extra functionaliteit om te voorkomen dat klanten een activiteit bewerken die door [!DNL Target] omdat er niet-ondersteunde meetgegevens worden gebruikt. Een bericht in UI geeft klanten de opdracht om de activiteit te dupliceren en dan omzettings metrisch bij te werken.

   Met deze release `averagetimespentonsite`, `bouncerate`, en `entries` maatstaven in [!DNL Target] de activiteiten zullen worden vervangen voor nieuwe activiteiten . Bestaande activiteiten kunnen deze cijfers tot mei 2023 blijven gebruiken.

* Knopinfo toegevoegd in het dialoogvenster [!DNL Target] UI om klanten te helpen een optimalisatiecriteria te selecteren terwijl het creëren van of het uitgeven van een [!UICONTROL Auto-Target] activiteit die A4T gebruikt.

## [!DNL Target] Standard/Premium 22.10.1 (gefaseerde release 10-13 oktober 2022)

Deze release is beschikbaar volgens het volgende schema:

* **10 oktober**: Regio Azië-Stille Oceaan (APAC)
* **12 oktober**: Amerikaanse regio
* **13 oktober**: Europa, Midden-Oosten en Afrika (EMEA)

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) fragmenten ervaren | Tot de updates voor de functie voor fragmenten met AEM ervaring behoren:<ul><li>De mogelijkheid om te filteren AEM ervaringsfragmenten op type (HTML of JSON) in de [!UICONTROL Offers] lijst. (TGT-43121)</li><li>Probleem verholpen waarbij klanten JSON konden invoegen. [!UICONTROL Experience Fragment] biedt aan wanneer het gebruiken van VEC, dat niet wordt gesteund. JSON-aanbiedingen kunnen alleen worden ingevoegd wanneer u de [!UICONTROL Form-Based Experience] composer. (TGT-43846)</li></ul>Zie AEM voor meer informatie [ervaringsfragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nieuw [!UICONTROL Visual Experience Composer] extensie voor Google Chrome | Een nieuwe [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) extensie voor Chrome is beschikbaar in de Chrome Web Store.<br>Vanaf januari 2023 wordt de huidige [!DNL Target] De extensie VEC Helper werkt niet meer in Google Chrome omdat Google extensies niet toestaat met Manifest V2. Download de nieuwe extensie om uw websites visueel te blijven ontwerpen in [!DNL Target] vanaf het nieuwe jaar.<br>De volgende koppelingen tonen de twee extensies in de Chrome Web Store:<ul><li>[Nieuwe extensie](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Oude extensie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Zie voor meer informatie [De extensie Visuele bewerkingshulp](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Documentatie-updates | De belangrijkste documentatieupdates omvatten het volgende:<ul><li>Nieuw en bijgewerkt [Adobe Target Admin en Reporting API-documentatie](https://developer.adobe.com/target/administer/admin-api/){target=_blank} bevat uitgebreide dekking van API-eindpunten voor beheer en rapportage, waaronder eigenschappen, aanbiedingen, hosts, omgevingen, clients, doelgroepen, activiteiten en meer.<br>Zie dit en extra inhoud voor ontwikkelaars in de [[!DNL Adobe Target] [!UICONTROL Developer Guide]](https://developer.adobe.com/target/){target=_blank}.</li><li>[Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>In dit artikel worden de gedetailleerde statistische berekeningen beschreven die in de handmatige A/Bn-tests in [!DNL Adobe Target].<br>De informatie in dit artikel vervangt de *Adobe Target-berekeningen voor A/B-tests* pdf-bestand dat eerder beschikbaar was voor downloaden op deze site.</li></ul> |

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
