---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release van Adobe Target (huidige) '
feature: Release Notes
translation-type: tm+mt
source-git-commit: 2dce7bbe94f20ad6f6732dfc3abceb69058a1f75
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 0%

---


# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke doelstandaard- en doelpremiumversie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd. We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen.
>
>* **Adobe Experience Platform Web SDK**: Met dit  [!UICONTROL Adobe Experience Platform Web SDK] programma kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in de  [!DNL Experience Cloud] (inclusief  [!DNL Target]). Als u ervoor kiest om naar [!DNL Adobe Experience Platform Web SDK] te migreren, zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Web SDK Guide*.
   >
   >
* **at.js**: De JavaScript-bibliotheek at.js biedt veel voordelen ten opzichte van mbox.js. Het bestand at.js verbetert onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert de beveiliging en biedt betere implementatieopties voor toepassingen op één pagina. Als u verkiest om aan at.js te migreren, zie [How At.js werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) en [Adobe Target Skill Builder: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Hoewel mbox.js momenteel wordt ondersteund (tot 31 maart 2021), hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Door alle klanten naar [!UICONTROL Adobe Experience Platform Web SDK] of at.js te verplaatsen, zullen onze technici en ondersteunend personeel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## Target Standard/Premium 21.1.1 (19 januari 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

* Er is een waarschuwing toegevoegd bij het selecteren van een [!DNL Adobe Analytics]-meting bij gebruik van [!UICONTROL Analytics as the reporting source] (A4T) in een [!UICONTROL Auto-Target]-activiteit. [!UICONTROL Auto-Target] modellen zijn geoptimaliseerd om met binaire (op omzetting-gebaseerde) metriek te werken. Het selecteren van ononderbroken metrisch, zoals opbrengst, zou suboptimale resultaten kunnen hebben en de [!UICONTROL Personalization Insights] rapporten zouden niet nauwkeurig kunnen zijn. (TGT-38926)
* Er is een statuspictogram toegevoegd in het [!UICONTROL Auto-Target Summary]-rapport voor [!UICONTROL Auto-Target]-activiteiten die gebruikmaken van A4T. Het groene controlepictogram naast elke ervaring in het rapport geeft aan dat er een gepersonaliseerd model voor machinaal leren is gegenereerd voor die ervaring. Het klokpictogram wijst erop dat niet genoeg verkeer is gediend om het model te bouwen. (TGT-38925)
* De [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] rapporteren voor [!UICONTROL Auto-Target] activiteiten die A4T en [!DNL Analytics] omzettingsmetriek gebruiken worden geproduceerd en kijken het zelfde als wanneer het gebruiken van [!DNL Target] als rapporteringsbron. (TGT-38931)
* Een omgevingsfilteroptie toegevoegd aan de lijst [!UICONTROL Recommendations] [!UICONTROL Collections]. (TGT-38353)
* Probleem verholpen waarbij het onjuiste aantal producten in verzamelingen [!UICONTROL Recommendations] werd weergegeven. (TGT-39162)
* Filter [!UICONTROL Last Updated] toegevoegd aan [!UICONTROL Recommendations] [!UICONTROL Catalog Search]. (TGT-38340)
* Probleem verholpen in [!UICONTROL Recommendations] dat ertoe leidde dat de pagina [!UICONTROL Create Sequence] vastliep nadat de verticale branche was gewijzigd. (TGT-38160)
* Probleem verholpen waardoor de activiteit niet kon worden opgeslagen als Device Co-op was ingeschakeld en de gebruiker van [!DNL Target] als rapportbron veranderde in [!DNL Analytics] (A4T). (TGT-38163)
* Probleem verholpen waardoor gebruikers een publiek niet konden verwijderen uit een aanbieding in een activiteit [!UICONTROL Automated Personalization] (AP). (TGT-39058)
* Probleem verholpen waarbij het onjuiste tijdframe (begin- en einddatum) voor sommige klanten werd weergegeven in [!UICONTROL Audience Info]-kaarten. (TGT-39150)
* Probleem verholpen waardoor sommige klanten de lijst met activiteiten in [!UICONTROL Default Workspace] niet konden zien. (TGT-38526)

## om 2.4.0 uur (14 januari 2021)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossingen:

* Voegt ondersteuning voor Unified Profile/platform-id toe aan de levering-API van de klant.
* Oplossing voor een ongeldige inspuiting van stijllabels.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Voorlopige-releasegegevens {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdatelijst | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
