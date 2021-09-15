---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en bibliotheken JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5a5b39db9b9b4ffd95573d643dcff52fe562c0c2
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard]- en [!DNL Target Premium]-versie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, [!DNL Adobe Experience Platform Web SDK], at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## [!DNL Target Standard/Premium] 21.9.1 (14 september 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

* Problemen verholpen waardoor klanten zich niet konden aanmelden bij [!UICONTROL Visual Experience Composer] (VEC) vanwege nieuw beveiligingsbeleid voor cookies van derden in sommige webbrowsers. Dit probleem is besproken in &quot;Pagina&#39;s die niet worden geladen in Visual Experience Composer (VEC) of Enhanced Experience Composer (EEC) bij gebruik van Google Chrome versie 80+&quot; in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* Probleem verholpen waarbij aanbiedingsnamen in de VEC het pad van de aanbieding weergeven in plaats van de vriendelijke naam van de aanbieding. (TGT-41300)
* De namen van de ervaring worden nu weerspiegeld in [!DNL Analysis Workspace] voor activiteiten A4T (TGT-38674)
* Probleem verholpen in [!DNL Recommendations] waarbij wijzigingen in de entiteit-id bij een promotie in een gedupliceerde activiteit ten onrechte werden toegepast op de oorspronkelijke activiteit. (TGT-41482)
* Probleem verholpen waardoor de knop &quot;Criteria bewerken&quot; niet correct kon worden weergegeven op de pagina [!UICONTROL Experiences] voor [!DNL Recommendations]-activiteiten in de VEC. (TGT-39512)
* Probleem verholpen waarbij synchronisatie van activiteiten tijdens het dupliceren en kopiëren naar een testwerkruimte werd voorkomen. (TGT-40686)
* Probleem verholpen waarbij wijzigingen in een kiezer met [ervaringsfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md) tijdens het gebruik van &quot;[!UICONTROL Insert After]&quot; in de VEC werden voorkomen. (TGT-41802)
* Probleem verholpen waarbij lege JSON-inhoud in een aanbieding niet naar de achtergrond kon worden verzonden. [!DNL Target] verzendt nu het JSON-object, ook al is het leeg. (TGT-41555)
* Probleem verholpen waarbij rapportage [!DNL Analytics] werd geopend in plaats van [!DNL Analysis Workspace] wanneer klanten tijdens het weergeven van een rapport op &quot;[!UICONTROL View in Analytics]&quot; hadden geklikt. (TGT-41867)
* Er is extra verduidelijking toegevoegd aan het weergegeven UI-bericht wanneer een klant [!DNL Analytics] probeert te selecteren als rapportagebron (A4T) voor een [!UICONTROL Automated Personalization]-activiteit. In het bericht staat dat &quot;[!DNL Target] de enige ondersteunde bron is voor [!UICONTROL Automated Personalization]-activiteiten.&quot; (TGT-41954)
* Er is extra verduidelijking toegevoegd aan het foutbericht wanneer klanten proberen hosts te scheiden met &quot;newline&quot; in plaats van met komma&#39;s. (TGT-40671)
* Probleem verholpen waarbij de datums &quot;[!UICONTROL Last Updated]&quot; van sommige activiteiten verschilden van de Engelse gebruikersinterface voor Spaanse en Japanse klanten (wanneer de gebruikersinterface wordt weergegeven in het Spaans en Japans). (TGT-38980)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
