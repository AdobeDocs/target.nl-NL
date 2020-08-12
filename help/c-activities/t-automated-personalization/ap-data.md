---
keywords: environmental data;session data;geo data;geographical data;device data;mobile data;attributes;profile attributes
description: Adobe Target verzamelt en gebruikt automatisch een verscheidenheid aan gegevens om zijn verpersoonlijkingsalgoritmen in de activiteiten van Automated Personalization (AP) en Auto-Target (AT) te bouwen. Wanneer een bezoeker de AP of activiteit van AT ingaat, wordt een momentopname van informatie overgegaan tot een reeks "opleidingsverslagen"(de bezoekersgegevens die de verpersoonlijkingsalgoritmen zullen leren).
title: Gegevensverzameling voor Adobe Target-verpersoonlijkingsalgoritmen
feature: null
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1755'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -gegevensverzameling voor de &#39;Target personalization&#39;-algoritmen{#data-collection-for-the-target-personalization-algorithms}

Het doel verzamelt en gebruikt automatisch een verscheidenheid van gegevens om zijn verpersoonlijkingsalgoritmen in de activiteiten van Automated Personalization (AP) en Auto-Target (AT) te bouwen. Wanneer een bezoeker de AP of activiteit van AT ingaat, wordt een momentopname van informatie overgegaan tot een reeks &quot;opleidingsverslagen&quot;(de bezoekersgegevens die de verpersoonlijkingsalgoritmen zullen leren).

Meer over de de verpersoonlijkingsalgoritmen van het Doel leren, zie [Willekeurig Bosalgoritme](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

In de volgende tabel worden standaard de gegevens weergegeven die door Automated Personalization en Auto-Target zijn verzameld, zonder dat de markeerstift iets hoeft te doen. Daarnaast ziet u ook de naamgevingsconventie die wordt gebruikt om deze kenmerken aan te geven in [Persoonlijke inzichten](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). U kunt de invoergegevensset op elk gewenst moment uitbreiden. Voor meer over hoe te om extra gegevens te uploaden, zie het [Uploaden van Gegevens voor de Algoritmen](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6)van de Aanpassing van het Doel.

| Gegevenstype | Beschrijving | Naamgevingsconventie voor gegevenstypen | Voorbeeldkenmerken |
| --- | --- | --- | --- |
| [Apparaat- en mobiele gegevens](#device-mobile) | Apparaat en mobiele specifieke informatie.<br>Zie &quot;Apparaat en mobiele gegevens&quot; hieronder. | `Device - [device attribute]`<br>`Mobile - [mobile attribute]` | Schermgrootte mobiel apparaat<br>OSMobile |
| [Milieugegevens](#env) | Informatie over het besturingssysteem van de bezoeker en hoe en wanneer de bezoeker toegang heeft tot de activiteit. | `Browser - / Operating System] - [Attribute Name]` | Browser - Type |
| Experience Cloud-segment | Soorten publiek gemaakt in Audience Manager of Analytics en gedeeld door de Experience Cloud | `Custom - Experience Cloud Audience - [Audience Name]` | Aangepaste gegevens |
| [Geografische gegevens](#geo) | Informatie over de locatie van de bezoeker.<br>Zie &quot;Geografische gegevens&quot; hieronder. | `Geo - [geo attribute]` | <br><br>CityCountryRegion/<br>StateZip<br><br><br>CodeLatitudeLongitudeISP of Mobile Carrier |
| Profielkenmerken | Profielscripts of -kenmerken die rechtstreeks via de update-API naar het doelprofiel zijn geüpload | `Custom - Visitor Profile - [attribute name]` | Aangepaste gegevens |
| URL-parameters verwijzen | In het algemeen is de verwijzende URL de URL die naar een bepaalde pagina verwees die de vraag van het Doel in werking stelde.<br>Deze variabele kan worden beïnvloed door de gebruikersactiviteit op uw site en de technische implementatie van uw site. | `Custom - [Referring URL Parameter] - [Parameter value]` | Aangepaste gegevens |
| Rapporterende segmenten | Om het even welke segmenten opstelling in activiteitenopstelling. | `Reporting Segment -[Segment Name]` | Aangepaste gegevens |
| [Sessiegegevens](#session) | Informatie over het gedrag van de bezoeker tijdens de sessie bij het openen van de activiteit. | `Visitor Profile - [Attribute Name]` | Bezoekersprofiel - Begin van het meest recente bezoek |
| URL-parameters | Doel inspecteert de URL om de URL-parameters te extraheren. | `Custom - URL Parameter - [URL Parameter]` | Aangepaste gegevens |

De volgende secties bevatten gedetailleerde informatie over de verschillende gegevenstypen, waaronder kenmerknamen, beschrijvingen en samplewaarden.

## Apparaat en mobiele gegevens {#device-mobile}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden |
| --- | --- | --- |
| Mobiel - apparaat - merk | Het merk van het mobiele apparaat dat de bezoeker gebruikte om tot de activiteit toegang te hebben. | Apple |
| Mobiel - apparaat - eReader | Geeft aan of het apparaat een eReader is. | 0 is Onwaar, 1 is Waar |
| Mobiel - apparaat - spelconsole | Geeft aan of het apparaat een spelconsole is. | 0 is Onwaar, 1 is Waar |
| Mobiel - apparaat - Mediaspeler | Geeft aan of het apparaat een mediaspeler is. | 0 is Onwaar, 1 is Waar |
| Mobiel - apparaat - mobiele telefoon | Geeft aan of het apparaat een mobiele telefoon is. | 0 is Onwaar, 1 is Waar |
| Mobiel - apparaat - modelnaam | De modelnaam van het mobiele apparaat dat de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | iPhone XS |
| Apparaat - Vak boven instellen | Geeft aan of het apparaat een set-top box is. | 0 is Onwaar, 1 is Waar |
| Mobiel - apparaat - tablet | Geeft aan of het apparaat een tablet is. | 0 is Onwaar, 1 is Waar |
| Mobiel - Pixeldichtheid (ppi) | De pixeldichtheid van het mobiele apparaat die de bezoeker gebruikt heeft om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Mobiel - OS X (Android, Windows, enz.) | Geeft aan of de gebruiker een OSX (of Android, Windows, enz.) heeft gebruikt apparaat voor toegang tot de activiteit. | 0 is Onwaar, 1 is Waar |
| Mobiel - schermhoogte (px) | De schermhoogte van het mobiele apparaat (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Mobiel - schermbreedte (px) | De schermbreedte (in pixels) van het mobiele apparaat die de bezoeker heeft gebruikt om de activiteit te openen. | 1, 2, 3, enz. |

## Milieugegevens {#env}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden |
| --- | --- | --- |
| Browser - Dag van Week | De dag van de week waarop de bezoeker de activiteit opende. | 0 tot en met 6.<br>(0 is zondag) |
| Browser - Uur van Dag | Het uur van de dag waarop de bezoeker de activiteit heeft geopend. | 0 tot en met 23<br>(0 is middernacht) |
| Browser - Uur van week | Het uur van de week waarin de bezoeker de activiteit opende. | 0 tot en met 168<br>(zondag middernacht is 0) |
| Browser - Taalinstelling | De taal die in de browser van de bezoeker wordt opgegeven en die wordt gebruikt om toegang te krijgen tot de activiteit. | <br>EngelsDuits |
| Browser - Schermhoogte (px) | De browserschermhoogte van het apparaat (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Browser - Tijd van Dag | De tijd van de dag van de browser waarop de bezoeker de activiteit heeft geopend. | 0, 6, 12, 18<br>(0 is nacht, 6 is ochtend,<br>12 is middag, 18 is avond) |
| Browser - Tijdzone | De tijdzone van de bezoeker terwijl de toegang tot van de activiteit. | Pacific<br>TimeEastern<br>TimeGMT |
| Browser - Type | Het type browser dat de bezoeker heeft gebruikt tijdens het openen van de activiteit. | <br><br>ChromeFirefoxInternet<br><br>ExplorerSafariOther |
| Browser - Weekdag/Weekend | De werkstatus toen de bezoeker de activiteit opende (weekend, werkuren, of vrije tijd van weekdagen). | Zaterdag en zondag is<br>weekendMaandag-Vrijdag 0900 tot 1800 is de<br>arbeidstijdMaandag-Vrijdag na 1800 tot 0900 is vrije tijd van weekdag |
| Browser - Vensterhoogte (px) | De vensterhoogte van de browser (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Browser - Vensterbreedte (px) | De breedte van het browservenster (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Apparaat - schermhoogte | De schermhoogte van het apparaat die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Apparaat - Schermbreedte | De schermbreedte van het apparaat die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. |
| Besturingssysteem | Het besturingssysteem op het apparaat van de bezoeker dat wordt gebruikt om toegang te krijgen tot de activiteit. | Mac<br><br><br>OSWindowsLinuxSearch<br>BotUnknown OS |
| Besturingssysteem - versie | De versie van het besturingssysteem die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | Windows 10<br>Mac OS 10 |
| Verkeersbronnen - Verwijzen naar URL van bestemmingspagina | De eerste pagina die de bezoeker heeft gezien bij het openen van uw site. | `https://www.adobe.com/ecloud.html` |

## Geografische gegevens {#geo}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden |
| --- | --- | --- |
| Geo - Plaats | De stad waar de bezoeker de activiteit heeft geopend. | San Francisco |
| Geo - Land | Het land waar de bezoeker de activiteit heeft geopend. | Duitsland |
| Geo - DMA | Het toegewezen marketinggebied (DMA) waar de bezoeker toegang toe had tot de activiteit. | Charlottesville |
| Geo - breedtegraad | De breedtegraad waartoe de bezoeker de activiteit heeft benaderd. | 47,269<br>Afgerond tot 3 decimalen (nauwkeurigheid ongeveer 100 m) |
| Geo - Lengte | De lengtegraad waartoe de bezoeker de activiteit heeft benaderd. | -122,269<br>Afgerond tot 3 decimalen (nauwkeurigheid ongeveer 100 m) |
| Geo - Staat/regio | De staat of het gebied waarvan de bezoeker de activiteit betreedde. | <br>UtahNew South Wales |
| Geo - Postcode | De postcode waarvan de bezoeker de activiteit betreedde. | 84004 |
| Mobiel - vervoerder | De mobiele drager die de bezoeker gebruikte toen het toegang tot van de activiteit. | <br>VodafoneT-Mobile |
| Netwerk - Verbindingssnelheid | De snelheid van de netwerkverbinding van het apparaat toen de bezoeker de activiteit opende. | <br><br><br><br><br>BroadbandCableDSLMobileWirelessSatellite |
| Netwerk - domeinnaam | De naam van het netwerkdomein waartoe de bezoeker toegang heeft gehad. | `nnt.net` |
| Netwerk - ISP | Het netwerk waarvan de bezoeker de activiteit betreedde. | nnt communications corporation |

## Sessiegegevens {#session}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden |
| --- | --- | --- |
| Bezoekersprofiel - Waarde van LiveTime-order voor activiteit | Hiermee geeft u de som op van alle bestelwaarden voor alle bezoeken/sessies aan een bepaalde activiteit. | Dubbel |
| Bezoekersprofiel - Levensduur activiteit op de site | Geeft de totale tijd aan die de bezoeker aan de site heeft doorgebracht, exclusief de huidige sessie, en wordt bijgewerkt wanneer de sessie verloopt. | Dubbele milliseconden |
| Bezoekersprofiel -Gemiddelde paginaweergaven per bezoek tijdens activiteit | Hiermee geeft u het gemiddelde aantal paginaweergaven per sessie op, exclusief de huidige sessie. | Dubbel |
| Bezoekersprofiel - Gemiddelde tijd per bezoek | Hiermee geeft u de gemiddelde tijd per bezoek/sessie op. De huidige sessie is hier niet in opgenomen. | Dubbele milliseconden |
| Bezoekersprofiel - Eerste bezoek | Hiermee geeft u de tijd op van het eerste bezoek dat de gebruiker met Target heeft uitgevoerd. | Dubbele milliseconden |
| Bezoekersprofiel - Uren sinds laatste bezoek | Geeft de uren aan sinds het laatste bezoek aan deze specifieke activiteit. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. |
| Bezoekersprofiel - Impressies van locatie/inhoud | Hiermee wordt het aantal indrukkingen opgegeven voor een bepaalde locatie/inhoudscombinatie in een bepaalde activiteit. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. |
| Bezoekersprofiel - Laatste doelinteractie | Geeft de tijd van de laatste interactie met Doel aan. Er vindt interactie plaats bij elk [!DNL Target] verzoek, omdat het profiel bij elke aanvraag door de huidige implementatie wordt [!DNL Target] bijgewerkt. | Dubbele milliseconden |
| Bezoekersprofiel - Pagina&#39;s weergegeven voor activiteit | Hiermee geeft u het aantal weergaven van de totale pagina (afbeeldingen) op, inclusief het huidige bezoek/de huidige sessie totdat de bezoeker de activiteit start. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. |
| Bezoekersprofiel - Paginaweergaven in huidig bezoek | Hiermee geeft u het aantal paginaweergaven op in de huidige bezoek/sessie totdat de bezoeker de activiteit start. Meer in het bijzonder het aantal indrukken. Dit zijn geen echte paginaweergaven, maar het aantal keren dat de aanvraag Target heeft bereikt. Doel kan geen onderscheid maken tussen time-outs of andere redenen waarom de gebruiker de inhoud niet heeft ontvangen of weergegeven. | Dubbel (alleen geheel getal positief) |
| Bezoekersprofiel - Begin van huidig bezoek | Hiermee geeft u de tijd op waarop het huidige bezoek/de huidige sessie met Target is gestart. Het bezoek aan Target kan worden gestart zonder een activiteit in te voeren. Alles wat vereist is, is een aanroep naar elk [!DNL Target] verzoek. Een bezoeker kan enige tijd duren voordat de activiteit wordt betreden en de opname wordt gemaakt. | Dubbele milliseconden |
| Bezoekersprofiel - Begin van het meest recente bezoek | Geeft de tijd aan waarop het laatste bezoek/de laatste sessie met Target is gestart. Dit kenmerk wordt bijgewerkt wanneer de sessie verloopt.<br>Als dit de eerste sessie voor de bezoeker is, resulteert dit in `LAST_SESSION_START = 0.` | Dubbele milliseconden |
| Bezoekersprofiel - Tijd sinds meest recente bezoek bij eerste intrede van activiteit | Geeft de duur aan tussen de vorige sessie en de tijd waarop de gebruiker de activiteit invoert en de momentopname wordt uitgevoerd. | Dubbele milliseconden |
| Bezoekersprofiel - Bezoek de tijd voordat u de activiteit betreedt | Geeft het verschil aan tussen de laatste interactie met Target en wanneer het huidige bezoek is gestart. Dit kenmerk kan worden beschouwd als een bezoek-/sessieduur totdat de gebruiker de activiteit invoert en de momentopname wordt uitgevoerd.<br>Negatieve waarden treden op wanneer het sessiebegin en de laatste updatetijd door dezelfde [!DNL Target] aanroep worden geactiveerd. Negatieve waarden moeten worden beschouwd als 0 (nul). | Dubbele milliseconden |
| Bezoekersprofiel - Totaal aantal bezoeken | Geeft het totale aantal bezoeken/sessies aan. Omvat niet het huidige bezoek/de zitting. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. |
| Bezoekersprofiel - Totaal aantal bezoeken aan activiteit | Geeft het aantal bezoeken aan een bepaalde activiteit aan. Als er geen vorig bezoek is, keert 0 (nul) terug. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. |
| Bezoekersprofiel - Totaal aantal bezoeken aan activiteit met conversie | Hiermee geeft u het aantal bezoeken/sessies voor een bepaalde activiteit op wanneer er ten minste één conversie heeft plaatsgevonden tijdens het bezoek. | Dubbel |
| Bezoekersprofiel - Bezoek aan activiteit zonder conversie | Aantal bezoeken/sessies zonder conversies naar een bepaalde activiteit. Deze waarde wordt na conversie weer op nul ingesteld, of -1 als er geen conversie heeft plaatsgevonden. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. |
