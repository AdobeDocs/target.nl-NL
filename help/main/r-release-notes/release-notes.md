---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: a03975f8f14db3cb8be0850130aab8d34c4c7fc0
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## Doelversie van Platform (13 april 2022)

Deze release bevat de volgende update:

* Probleem opgelost om ervoor te zorgen dat het laatste octet van IP-adressen behoorlijk wordt verduisterd wanneer deze worden vastgelegd met profielscripts. (TNT-44076)

## [!DNL Target Standard/Premium] 22.3.1 (gespreide afgifte, nog te bepalen datum)

Deze release bevat de volgende wijzigingen en verbeteringen:

* Probleem verholpen waarbij tijdens het bewerken van profielscripts het oorspronkelijke, onbewerkte script werd hersteld nadat het script was bewerkt, geactiveerd en vervolgens gedeactiveerd. Het profielscript blijft nu in de bewerkte status staan. (TGT-43249)
* Probleem verholpen dat het volgende foutbericht veroorzaakte in het dialoogvenster [!DNL Target] UI bij het verplaatsen van een publiek dat wordt gebruikt in een activiteit met de status &quot;concept&quot;: &quot;We kunnen je aanvraag niet voltooien. Neem contact op met de klantenservice van Adobe als het probleem zich blijft voordoen.&quot; (TGT-43212)
* Het probleem dat de oorzaak was van de [!UICONTROL Include] en [!UICONTROL Exclude] opties die bij het bewerken van een activiteit moeten worden uitgeschakeld voor een gecombineerd publiek. (TGT-43422)
* Probleem verholpen waardoor sommige klanten de lijst met beschikbare soorten publiek niet konden zien tijdens het bewerken van een activiteit. (TGT-43404)
* Probleem verholpen waardoor sommige klanten een IP-adres niet konden verwijderen van &quot;[!UICONTROL IPs to exclude from [!DNL Target] reporting data]&quot; lijst in [!UICONTROL Administration] > [!UICONTROL Reporting]. (TGT-43384)
* Probleem verholpen waarbij het gebruik van negatieve getallen in publiekscriterium werd voorkomen waarmee werd gecontroleerd of een variabele &quot;groter dan&quot;, &quot;groter dan of gelijk aan&quot;, &quot;kleiner dan&quot; of &quot;kleiner dan of gelijk aan&quot; is. (TGT-43367)
* Probleem verholpen waardoor klanten de [!UICONTROL Audience Details] kaart bij het maken van een gecombineerd publiek. (TGT-43303)
* Het probleem dat de oorzaak was van de [!DNL Target] UI of new [!UICONTROL Audiences] UI aan prematuurtijd uit voor sommige klanten. (TGT-42590 &amp; TGT-43273)

## [!DNL Target] Release van Platform (30 maart)

Deze release bevat de volgende verbeteringen:

* De metriek van het klik-spoor zal analytische lading in levering API verzoeken voor activiteiten omvatten die Analytics als rapporteringsbron (A4T) en procesgebeurtenissen op cliënt-kant gebruiken. (TNT-43073)

## [!DNL Target Standard] Vernieuwen van soorten publiek (28 maart)

Deze release bevat de volgende update:

* De nieuwe [!UICONTROL Audiences] De interface wordt voor iedereen ingeschakeld [!DNL Target Standard] klanten.

## Oplossingen voor technische oplossingen voor doelklanten/Premium (22 maart 2022)

Deze onderhoudrelease bevat de volgende verbeteringen:

* Toegevoegde functionaliteit die moet worden geretourneerd [!DNL Analytics] ladingsgegevens voor `prefetch` weergaven en `pageLoad` klik op Metriek wanneer u de [!UICONTROL Delivery API] met activiteiten die [!UICONTROL Analytics as the reporting source] (A4T). (TNT-43198)
* Bijgewerkt de beide het filtreren lijst van gebruikersagent om een browser type toe te staan dat algemeen in Japan wordt gebruikt. (TNT-43867)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

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
