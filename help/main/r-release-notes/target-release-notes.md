---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: d0b6f81507cc5d5bc17d029c3d8f5b36c2c71a29
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 18 juli 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target Standard/Premium] 22.7.1 (20 juli 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | --- |
| Verbeterde nauwkeurigheid van de publieksevaluatie en latentie voor eindgebruikers via IPv6-ondersteuning | De geo-plaatsen van bezoekers worden nu bepaald door IPv6 adressen, als beschikbaar, in tegenstelling tot slechts IPv4 adressen. De levering APIs steunt ook IPv6 inputparameters. Het filteren en toestaan-lijst steunen zowel IPv4 als IPv6 adressen. Deze IPv6-ondersteuning in deze release betekent dat bezoekers nauwkeuriger worden opgenomen in het publiek (kwalificeer nauwkeuriger voor activiteiten of worden opgenomen in filtercriteria). Het verbetert ook gegevenslatentie, aangezien de cliënten IPv6 rechtstreeks zullen leiden, vermijdend de overheadkosten van de gateway IPv6-aan-IPv4. |
| A4T Verbetering voor taakverwerking op de client | Met integratie van de server-kant A4T, als Adobe Target een verzoek als afkomstig van beide identificeert, door:sturen het niet de nuttige lading aan Analytics, en er is geen mod_stats gebeurtenis in geregistreerd in de logboeken van het Doel. Voorafgaand aan deze versie, zouden de cliënt-zijintegratie A4T de lading aan Analytics door:sturen, zelfs wanneer het als allebei verkeer was geïdentificeerd. Deze inconsistentie tussen server en cliënt-kant zou tot discrepanties leiden, aangezien A4T rapporten voor laatstgenoemde het beide verkeer omvatten. Bovendien was het beide verkeer niet noodzakelijk geïdentificeerd of gemarkeerd, wat betekent dat het niet mogelijk was het beide verkeer uit de rest van het verkeer te doorbreken of te verwijderen. En zelfs als een klant beide verkeer op zich rekenschap zou geven, zou het niet noodzakelijk de reeks verkeer aanpassen die Target identificeerde en als zowel verkeer uitsloot, zodat tot gesplitste discrepanties of andere kwesties zou leiden. Met deze versie, is het cliënt-zijregistreren A4T verbeterd zodat het gedrag met betrekking tot de A4T lading het zelfde als met server-kant A4T is: Bezoekers die als bots worden geïdentificeerd, worden uitgesloten van het tellen/rapporteren van doelen, zowel voor server-side als voor client-side implementaties. |

## [!DNL Target Standard/Premium] 22.6.2 (30 juni 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | ---  |
| Meldingen in producten | Verkrijg de volgende relevante in-product berichten:<ul><li>**Activiteiten**: Meldingen voor alle soorten activiteiten wanneer een activiteit handmatig wordt goedgekeurd of gedeactiveerd of wanneer de begin- of einddatum wordt bereikt. Het bericht bevat de naam van de activiteit met een koppeling naar de overzichtspagina van de activiteit.</li><li>**Profielscripts** Meldingen wanneer een profielscript handmatig of door Doel is geactiveerd of gedeactiveerd.</li><li>**Recommendations feeds**: Meldingen wanneer een Recommendations-feed handmatig of via Target is geactiveerd of gedeactiveerd. Meldingen worden ook verzonden wanneer een Recommendations-feed mislukt.</li></ul> Standaard worden meldingen ontvangen door productbeheerders, uitgevers en fiatteurs. Meldingen kunnen worden geconfigureerd in de voorkeuren voor Experience Cloud.<br>Zie voor meer informatie [Meldingen en aankondigingen](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Adobe Target Developer Guide* | De *Adobe Target Developer Guide* consolideert alles [!DNL Target] ontwikkelaarsinhoud in één handige handleiding. De gids bevat informatie over de implementatie [!DNL Target] en [!DNL Recommendations], [!DNL Target] SDK&#39;s, en [!DNL Target] API&#39;s.<br>Zie voor meer informatie [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}. |

* Gebruikers met de [!UICONTROL Editor] rol kan het publiek in live activiteiten niet meer bewerken. (TGT-43582)
* Een waarschuwingsbericht wordt weergegeven als een klant een publiek probeert op te slaan met een uitroepteken ( ! ) als het eerste teken van de naam van het publiek (bijvoorbeeld !Londen). (TGT-43643)
* Probleem verholpen waarbij definitiedetails voor bepaalde klanten werden veroorzaakt om aan te geven dat een beëindigde activiteit nog steeds actief is. (TGT-43527)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
