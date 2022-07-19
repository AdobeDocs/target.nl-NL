---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: a5d2c07105b1d0fac6115fe507537be6a36799e9
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 19 juli 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target Standard/Premium] 22.7.1 (20 juli 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | --- |
| Verbeterde nauwkeurigheid van de publieksevaluatie en latentie voor eindgebruikers via IPv6-ondersteuning | De geo-plaatsen van bezoekers worden nu bepaald door IPv6 adressen, als beschikbaar, in tegenstelling tot slechts IPv4 adressen. De levering APIs steunt ook IPv6 inputparameters. Het filteren en toestaan-lijst steunen zowel IPv4 als IPv6 adressen. Deze IPv6-ondersteuning in deze release betekent dat bezoekers nauwkeuriger worden opgenomen in het publiek (kwalificeer nauwkeuriger voor activiteiten of worden opgenomen in filtercriteria). Het verbetert ook gegevenslatentie, aangezien de cliënten IPv6 rechtstreeks zullen leiden, vermijdend de overheadkosten van de gateway IPv6-aan-IPv4. |
| A4T Verbetering voor taakverwerking op de client | Met integratie op de server-side van A4T, als Adobe Target een verzoek als afkomstig van beide identificeert, stuurt het niet de nuttige lading naar Analytics, en er is geen mod_stats gebeurtenis in geregistreerd in [!DNL Target] logboeken. Voorafgaand aan deze versie, zouden de cliënt-zijintegratie A4T de lading aan door:sturen [!DNL Analytics], zelfs wanneer het als beide verkeer was geïdentificeerd. Deze inconsistentie tussen server en cliënt-kant zou tot discrepanties leiden, aangezien A4T rapporten voor laatstgenoemde het beide verkeer omvatten. Bovendien was het beide verkeer niet noodzakelijk geïdentificeerd of gemarkeerd, wat betekent dat het niet mogelijk was het beide verkeer uit de rest van het verkeer te doorbreken of te verwijderen. En zelfs als een klant voor beide verkeer op zich rekenschap zou geven, zou het niet noodzakelijk de reeks verkeer aanpassen die [!DNL Target] die als zowel verkeer zijn geïdentificeerd en uitgesloten, wat leidt tot gesplitste discrepanties of andere problemen. Met deze versie, is het cliënt-zijregistreren A4T verbeterd zodat het gedrag met betrekking tot de A4T lading het zelfde als met server-kant A4T is: Bezoekers die als bots zijn geïdentificeerd, worden uitgesloten van [!DNL Target] tellen/rapporteren, voor zowel server-kant als cliënt-zijimplementaties. |


## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
