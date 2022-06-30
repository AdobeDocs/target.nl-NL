---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: fa6324606b32f265084615fd1c13ce6c49921b48
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target Standard/Premium] 22.6.2 (30 juni 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | ---  |
| Meldingen in producten | Verkrijg de volgende relevante in-product berichten:<ul><li>**Activiteiten**: Meldingen voor alle soorten activiteiten wanneer een activiteit handmatig wordt goedgekeurd of gedeactiveerd of wanneer de begin- of einddatum wordt bereikt. Het bericht bevat de naam van de activiteit met een koppeling naar de overzichtspagina van de activiteit.</li><li>**Profielscripts** Meldingen wanneer een profielscript handmatig of door Doel is geactiveerd of gedeactiveerd.</li><li>**Recommendations feeds**: Meldingen wanneer een Recommendations-feed handmatig of via Target is geactiveerd of gedeactiveerd. Meldingen worden ook verzonden wanneer een Recommendations-feed mislukt.</li></ul> Standaard worden meldingen ontvangen door productbeheerders, uitgevers en fiatteurs. Meldingen kunnen worden geconfigureerd in de voorkeuren voor Experience Cloud.<br>Zie voor meer informatie [Meldingen en aankondigingen](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Adobe Target Developer Guide* | De *Adobe Target Developer Guide* consolideert alles [!DNL Target] ontwikkelaarsinhoud in één handige handleiding. De gids bevat informatie over de implementatie [!DNL Target] en [!DNL Recommendations], [!DNL Target] SDK&#39;s, en [!DNL Target] API&#39;s.<br>Zie voor meer informatie [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}. |

* Gebruikers met de [!UICONTROL Editor] rol kan het publiek in live activiteiten niet meer bewerken. (TGT-43582)
* Een waarschuwingsbericht wordt weergegeven als een klant een publiek probeert op te slaan met een uitroepteken ( ! ) als het eerste teken van de naam van het publiek (bijvoorbeeld !Londen). (TGT-43643)
* Probleem verholpen waarbij definitiedetails voor bepaalde klanten werden veroorzaakt om aan te geven dat een beëindigde activiteit nog steeds actief is. (TGT-43527)

## [!DNL Target Standard/Premium] 22.6.1 (gefaseerde release: (7-9 juni 2022)

Deze release is beschikbaar volgens het volgende schema:

* **7 juni**: Regio Azië-Stille Oceaan (APAC)
* **8 juni**: Amerikaanse regio
* **9 juni**: Europa, Midden-Oosten en Afrika (EMEA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Er is een verbetering voor de nieuwe [!UICONTROL Audiences] pagina om een inconsistente staat tussen het oude gegevensbestand te verhinderen waar het publiek in het verleden en de nieuwe architectuur werd opgeslagen die de informatie direct van het achtereind terugwint. (TGT-43552)
* Probleem verholpen waardoor sommige klanten geen gecombineerd publiek konden opslaan dat was veroorzaakt door het maken van &quot;lege&quot; containers in de doelgebruikersinterface. (TGT-43588)

## Doelplatformversie (25 mei 2022)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Toegevoegd [Clienttips van gebruikersagent](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} ondersteuning.
* Probleem verholpen waarbij periodiek time-outs werden veroorzaakt tijdens het renderen [!UICONTROL Offer Decisions] in [!UICONTROL Experience Targeting] (XT) activiteiten. (TNT-44611)

## at.js versie 2.9.0 (27 mei 2022)

* Toegevoegd [Clienttips van gebruikersagent](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank} ondersteuning.
* Probleem verholpen waarbij meerdere mbox-aanvragen op dezelfde pagina verschillende beeld-id&#39;s hebben.

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
