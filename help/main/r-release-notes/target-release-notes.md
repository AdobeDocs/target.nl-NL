---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c5445903e7bbab210d0e72200c54ab07975c21c5
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 4 oktober 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

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

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
