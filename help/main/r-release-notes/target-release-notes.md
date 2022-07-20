---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: d54f3c4c75031788316a94acf3d14a8db2a17366
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 20 juli 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] platformrelease (20 juli 2022)

Deze versie bevat de volgende functies, verbeteringen en oplossingen:

| Functie | Beschrijving |
| --- | --- |
| Verbeterde nauwkeurigheid van de publieksevaluatie en verminderde latentie van de eindgebruiker door IPv6 steun (TNT-43364, TNT-44692) | De geo-plaatsen van bezoekers worden nu bepaald door IPv6 adressen, als beschikbaar, in tegenstelling tot slechts IPv4 adressen. De levering APIs steunt ook IPv6 inputparameters. Het filteren en toestaan-lijst steunen zowel IPv4 als IPv6 adressen. De IPv6-ondersteuning in deze release betekent dat bezoekers nauwkeuriger worden opgenomen in het publiek (kwalificeer nauwkeuriger voor activiteiten of worden opgenomen in filtercriteria). Het verbetert ook gegevenslatentie, aangezien de cliënten IPv6 rechtstreeks zullen leiden, vermijdend de overheadkosten van de gateway IPv6-aan-IPv4. |
| Vast probleem met de afhandeling van betalingen aan de client-side A4T (TNT-44926) | Met integratie op de server-side van A4T, als Adobe Target een verzoek als afkomstig van beide identificeert, stuurt het niet de nuttige lading naar Analytics, en er is geen mod_stats gebeurtenis in geregistreerd in [!DNL Target] logboeken. &lt;!— Voorafgaand aan deze versie, zouden de A4T cliënt-zijintegratie de lading aan door:sturen [!DNL Analytics], zelfs wanneer het als beide verkeer was geïdentificeerd. Deze inconsistentie tussen server en cliënt-kant zou tot discrepanties leiden, aangezien A4T rapporten voor laatstgenoemde het beide verkeer omvatten. Bovendien was het beide verkeer niet noodzakelijk geïdentificeerd of gemarkeerd, wat betekent dat het niet mogelijk was het beide verkeer uit de rest van het verkeer te doorbreken of te verwijderen. En zelfs als een klant voor beide verkeer op zich rekenschap zou geven, zou het niet noodzakelijk de reeks verkeer aanpassen die [!DNL Target] die als zowel verkeer zijn geïdentificeerd en uitgesloten, wat leidt tot gesplitste discrepanties of andere problemen. —> Met deze release is het logboekbestand van de A4T-client verbeterd, zodat het gedrag met betrekking tot de A4T-payload hetzelfde is als bij de A4T-server: Bezoekers die als bots zijn geïdentificeerd, worden uitgesloten van [!DNL Target] tellen/rapporteren. (Let op: het probleem in kwestie was beperkt tot implementaties die gebruik maakten van client-side payload handling; server-kant niet beïnvloed. Met deze release is het gedrag nu consistent voor zowel server-side als client-side payload-afhandeling.) |


## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
