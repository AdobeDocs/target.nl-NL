---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;oplossingen;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de huidige release van [!DNL Adobe Target].
short-description: Learn about the new features, enhancements, and fixes included in the current release of [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 207095a1db483abcc59f7806a67e559ee8694397
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 2%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target] Standard/Premium 22.15.1 (8 en 9 maart 2023)

Deze release is beschikbaar volgens het volgende schema:

* **8 maart**: Amerikaanse regio
* **9 maart**: Europa, Midden-Oosten en Afrika (EMEA)
* **9 maart**: Regio Azië-Stille Oceaan (APAC)

>[!NOTE]
>
>Vanwege problemen die sindsdien zijn verholpen, zijn de &quot;Geoptimaliseerde A4T metriek voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]De functie &quot; die op 8 en 9 maart is uitgebracht, is tijdelijk verwijderd. Na verdere interne tests wordt de functie in de komende weken opnieuw vrijgegeven.

Deze versie bevat de volgende oplossingen:

* Updates voor het ontwerpen van aangepaste webcomponenten met de [!UICONTROL Visual Experience Composer] (VEC):

   * De Vaste de elementenselectie van de Schaduw DOM in VEC door het auteursproces te verbeteren zodat is er geen afhankelijkheid van [!DNL Target] implementatietype bij het ontwerpen van de schaduwhoofdmap. Het selecteren van Schaduw-DOM-elementen in de VEC werkt nu voor elke website.
   * Probleem opgelost waarbij het laden van HTML-elementen met #Shadow DOM in de VEC werd voorkomen. (TGT-35801)
   * VEC-problemen met SPA websites opgelost met ShadowDOM. (TGT-43169)
   * Probleem verholpen met de optimalisatiedoelstelling: &quot;clicked an element&quot; dat de CSS-kiezer niet correct identificeerde in ShadowDOM.

>[!NOTE]
>
>Zorg ervoor dat u een [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js) met een versie groter dan 2.8.

**Bekend probleem**: Klikken en volgen op een schaduwbasiselement bij gebruik [!DNL Adobe Experience Platform Web SDK] werkt niet correct. (TNT-47012)

## at.js versie 2.10.2 (7 maart 2023)

* Het probleem dat de oorzaak was van de `trackEvent` om altijd een fout te retourneren.

Voor informatie over alle versies at.js, zie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

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
