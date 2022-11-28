---
keywords: omgevingsgegevens;sessiegegevens;geo-gegevens;geografische gegevens;apparaatgegevens;mobiele gegevens;kenmerken;profielkenmerken;verpersoonlijkingsalgoritmen;machinaal leeralgoritmen;machinaal leeralgoritmen
description: Meer informatie over de Adobe [!DNL Target] verzamelt en gebruikt om zijn machine-leert algoritmen te bouwen.
title: Welke Gegevens worden verzameld om machine-Lerende Algoritmen te bouwen?
feature: Automated Personalization
exl-id: 7114a6d6-4779-471e-9b91-646aa49e102a
source-git-commit: 6a2071e08b60db90021239a14a1167f79a3ed879
workflow-type: tm+mt
source-wordcount: '2015'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Gegevens gebruikt door [!DNL Target] computerleeralgoritmen

[!DNL Adobe Target] verzamelt en gebruikt automatisch een verscheidenheid van gegevens om zijn verpersoonlijkingsalgoritmen in te bouwen [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten. Wanneer een bezoeker een AP- of AT-activiteit betreedt, wordt een momentopname van informatie doorgegeven aan een set van &quot;trainingsrecords&quot; (de bezoekersgegevens waarop de verpersoonlijkingsalgoritmen zullen leren).

Meer informatie over de [!DNL Target] verpersoonlijkingsalgoritmen, zie [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

## Standaard [!DNL Adobe Target] kenmerkcategorieën

In de volgende tabel worden de gegevens weergegeven die zijn verzameld door [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] activiteiten standaard, zonder enige configuratie van [!DNL Target] of andere [!DNL Adobe] en de naamgevingsconventie die wordt gebruikt om deze kenmerken aan te geven in [Persoonlijkheidsrapporten](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). U kunt de invoergegevensset op elk gewenst moment uitbreiden. Ga voor meer informatie over het uploaden van aanvullende gegevens naar [Gegevens uploaden voor de [!DNL Target] verpersoonlijkingsalgoritmen](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

| Gegevenscategorie | Systeemvoorvoegsel | Beschrijving | Naam weergeven in [!UICONTROL Insights] rapporten |
| --- | --- | --- | --- |
| Omgevingsparameters | ENV | Informatie over de omgeving van een gebruiker, zoals het besturingssysteem, de browser en het tijdstip van de dag/dag van de week. | Browser - [Kenmerknaam]<br>Besturingssysteem - [Waarde] |
| Geografie | GEO | Informatie over de geografie van een gebruiker, die via IP raadpleging wordt verkregen. | Geo - [geo, kenmerk] |
| Mobiel apparaat | MOB | Informatie over het mobiele apparaat van een gebruiker. | Apparaat - [apparaatkenmerk]<br>Mobiel - [mobile, kenmerk] |
| Doelrapporterende segmenten | SEG | In [!DNL Target] rapportage. | Rapporterend segment -[Segmentnaam] |
| Sessiegedrag | SES | Informatie over gebruikersgedrag, zoals het aantal weergegeven pagina&#39;s. | Bezoekerprofiel - [Kenmerknaam] |

## Aangepaste Adobe Target-kenmerkcategorieën

In de volgende tabel worden de door de klant verschafte gegevens weergegeven die zijn verzameld door [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] activiteiten. Deze gegevens worden alleen verzameld als u ze opgeeft. De specifieke attributennamen en de steekproefwaarden zullen voor uw systeemconfiguratie bijzonder zijn.

| Gegevenscategorie | Systeemvoorvoegsel | Beschrijving | Naam weergeven in [!UICONTROL Insights] rapporten |
| --- | --- | --- | --- |
| Paginaparameters | VAK | Aangepaste paginaparameters (&quot;mbox parameters&quot;) die in de aanroep aan worden doorgegeven [!DNL Target]. | Aangepast, mappenparameter - [parameternaam] |
| [!DNL Target] profiel | PRO | Aangepaste profielkenmerken die rechtstreeks zijn geüpload naar de [!DNL Target] profiel via API of paginaparameter en [!DNL Target] profielscripts. | Aangepast - Bezoekersprofiel - [kenmerknaam] |
| Klantkenmerken | CRS | Klantkenmerken geüpload naar de [!DNL Target] profiel via de [Adobe Experience Cloud Customer Attributes Service](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html){target=_blank}. | Aangepast - Bezoekersprofiel - [kenmerknaam] |
| URL-parameters | URL | URL en eventuele URL-parameters voor de momenteel weergegeven pagina. | Aangepast - URL-parameter - [URL-parameter] |
| URL verwijzen | REF | Verwijzen naar URL- en URL-parameters voor de verwijzende URL. | Aangepast - [Verwijzen naar URL-parameter] - [Parameterwaarde] |
| Adobe Experience Cloud, gedeeld publiek | AAM | Alle soorten publiek die worden gedeeld met [!DNL Target] van andere [!DNL Adobe Experience Cloud] oplossingen (bijvoorbeeld [!DNL Adobe Audience Manager] en [!DNL Adobe Analytics]via de [[!DNL Experience Cloud Audience Library]](https://experienceleague.adobe.com/docs/core-services/interface/services/audiences/audience-library.html){target=_blank}). | Aangepast, Experience Cloud-publiek - [Auditienaam] |
| Adobe Experience Platform CDP-publiek in realtime | UPS | AEP CDP-publiek in realtime gedeeld met [!DNL Target] via Doelen. |  |
| Adobe Experience Platform CDP-kenmerken in realtime | AEP | AEP CDP-kenmerken in realtime die worden gedeeld met [!DNL Target] via Doelen. Deze functie staat momenteel in bètaversie. |  |

## Functies blokkeren [!DNL Target] computerleeralgoritmen

Functies kunnen worden geblokkeerd [!DNL Target] computerleeralgoritmen, die voorkomen dat ze worden gebruikt in om het even welk [!UICONTROL Auto-Target] of [!UICONTROL Automated Personalization] model of activiteit.

Zie voor meer informatie [Modellen-API (Voegend op lijst van gewenste personen) - overzicht](https://developer.adobe.com/target/before-administer/models-api/){target=_blank} in het dialoogvenster *Adobe Target Developer Guide*.

## Apparaat- en mobiele gegevens {#device-mobile}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden | Systeemnaam |
| --- | --- | --- | --- |
| Mobiel - apparaat - merk | Het merk van het mobiele apparaat dat de bezoeker gebruikte om tot de activiteit toegang te hebben. | Apple | MOB_targeting.mobile.vendor |
| Mobiel - apparaat - eReader | Geeft aan of het apparaat een eReader is. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.ereader |
| Mobiel - apparaat - spelconsole | Geeft aan of het apparaat een spelconsole is. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.gamesConsole |
| Mobiel - apparaat - Mediaspeler | Geeft aan of het apparaat een mediaspeler is. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.mediaPlayer |
| Mobiel - apparaat - mobiele telefoon | Geeft aan of het apparaat een mobiele telefoon is. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.mobilePhone |
| Mobiel - apparaat - modelnaam | De modelnaam van het mobiele apparaat dat de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | iPhone XS | MOB_targeting.mobile.model |
| Apparaat - Vak boven instellen | Geeft aan of het apparaat een set-top box is. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.setTopBox |
| Mobiel - apparaat - tablet | Geeft aan of het apparaat een tablet is. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.tablet |
| Mobiel - Pixeldichtheid (ppi) | De pixeldichtheid van het mobiele apparaat die de bezoeker gebruikt heeft om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. | MOB_targeting.mobile.displayPi |
| Mobiel - OS X (Android, Windows, enz.) | Geeft aan of de gebruiker een OSX (of Android, Windows, enz.) heeft gebruikt apparaat voor toegang tot de activiteit. | 0 is Onwaar, 1 is Waar | MOB_targeting.mobile.os[OS]<br>Bijvoorbeeld MOB_targeting.mobile.osOSx, MOB_targeting.mobile.osWindows, MOB_targeting.mobile.osAndroid, MOB_targeting.mobile.osLinux |
| Mobiel - schermhoogte (px) | De schermhoogte van het mobiele apparaat (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit. | 1, 2, 3, enz. | MOB_targeting.mobile.displayHeight |
| Mobiel - schermbreedte (px) | De schermbreedte (in pixels) van het mobiele apparaat die de bezoeker heeft gebruikt om de activiteit te openen. | 1, 2, 3, enz. | MOB_targeting.mobile.displayWidth |

## Milieugegevens {#env}

|Kenmerknaam|Kenmerkbeschrijving|Voorbeeldwaarden|Systeemnaam| | — | — | — | — | |Browser - Dag van de Week|De dag van de week waarop de bezoeker de activiteit opende.|0 tot en met 6.<br>(0 is zondag)|ENV_DagOfWeek| |Browser - Uur van Dag|Het uur van de dag waarop de bezoeker de activiteit heeft geopend.|0 tot en met 23<br>(0 is middernacht)|ENV_UserHour| |Browser - Uur van Week|Het uur van de week waarin de bezoeker de activiteit opende.|0 tot en met 168<br>(Zondag middernacht is 0)|ENV_WeekHour| |Browser - Taalinstelling|De taal die in de browser van de bezoeker is opgegeven en die wordt gebruikt om toegang te krijgen tot de activiteit.|Engels<br>Duits|ENV_Taal| |Browser - Tijd van Dag|De browsertijd van dag waarop de bezoeker de activiteit heeft geopend.|0, 6, 12, 18<br>(0 is nacht, 6 is ochtend,<br>12 is middag, 18 is avond)|ENV_LocalTimePeriod| |Browser - Tijdzone|De tijdzone van de bezoeker terwijl het toegang tot van de activiteit.|Pacific Time<br>Oosterse tijd<br>GMT|ENV_BrowserTimezoneOffsetMinutes| |Browser - Type|Het type browser dat de bezoeker tijdens de toegang tot de activiteit heeft gebruikt.|Chroom<br>Firefox<br>Internet Explorer<br>Safari<br>Overige|ENV_Browser| |Browser - Weekdag/Weekend|De werkstatus toen de bezoeker de activiteit (weekend, werkuren, of weekdagvrije tijd) betreedde.|Zaterdag en zondag is weekend<br>Maandag-vrijdag 0900 tot 1800 is de arbeidstijd<br>Maandag - vrijdag na 1800 tot 900 is vrije tijd op weekdagen|ENV_UserHourType| |Browser - Vensterhoogte (px)|De vensterhoogte van de browser (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit.|1, 2, 3, enz.|ENV_BrowserHeight| |Browser - Vensterbreedte (px)|De breedte van het browservenster (in pixels) die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit.|1, 2, 3, enz.|ENV_BrowserWidth| |Apparaat - Schermhoogte (px)|De schermhoogte van het apparaat die de bezoeker heeft gebruikt om toegang te krijgen tot de activiteit.|1, 2, 3, enz.|ENV_ScreenHeight| |Apparaat - Schermbreedte (px)|De schermbreedte van het apparaat die de bezoeker heeft gebruikt om de activiteit te openen.|1, 2, 3, enz.|ENV_ScreenWidth| |Besturingssysteem|Het besturingssysteem op het apparaat van de bezoeker dat wordt gebruikt om toegang te krijgen tot de activiteit.|Mac OS<br>Windows<br>Linux<br>Zoekvak<br>Onbekend besturingssysteem|ENV_Besturingssysteem| |Besturingssysteem - Versie|De versie van het besturingssysteem die de bezoeker gebruikte om toegang te krijgen tot de activiteit.|Windows 10<br>Mac OS 10|ENV_OperatingSystemVersion| |Verkeersbronnen - Verwijzen naar URL van bestemmingspagina|De eerste pagina die de bezoeker heeft gezien toen hij uw site opende.|`https://www.adobe.com/ecloud.html`|ENV_Referrer|

## Geografische gegevens {#geo}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden | Systeemnaam |
| --- | --- | --- | --- |
| Geo - Plaats | De stad waar de bezoeker de activiteit heeft geopend. | San Francisco | Geo_City |
| Geo - Land | Het land waar de bezoeker de activiteit heeft geopend. | Duitsland | Geo_Land |
| Geo - DMA | Het toegewezen marketinggebied (DMA) waar de bezoeker toegang toe had tot de activiteit. | Charlottesville | Geo_DMA |
| Geo - breedtegraad | De breedtegraad waartoe de bezoeker de activiteit heeft benaderd. | 47,269<br>Afgerond tot 3 decimalen (nauwkeurigheid ongeveer 100 meter) | GEO_Latitude |
| Geo - Lengte | De lengtegraad waartoe de bezoeker de activiteit heeft benaderd. | -122,269<br>Afgerond tot 3 decimalen (nauwkeurigheid ongeveer 100 meter) | GEO_Lengtegraad |
| Geo - Staat/regio | De staat of het gebied waarvan de bezoeker de activiteit betreedde. | Utah<br>New South Wales | GEO_State<br>GEO_Regio |
| Geo - Postcode | De postcode waarvan de bezoeker de activiteit betreedde. | 84004 | GEO_ZipCode |
| Mobiel - vervoerder | De mobiele drager die de bezoeker gebruikte toen het toegang tot van de activiteit. | Vodafon<br>T-Mobile | GEO_mobileCarrier |
| Netwerk - Verbindingssnelheid | De snelheid van de netwerkverbinding van het apparaat toen de bezoeker de activiteit opende. | Breedband<br>Kabel<br>DSL<br>Mobiel<br>Draadloos<br>Satelliet | GEO_ConnectionSpeed |
| Netwerk - domeinnaam | De naam van het netwerkdomein waartoe de bezoeker toegang heeft gehad. | `nnt.net` | GEO_DomainName |
| Netwerk - ISP | Het netwerk waarvan de bezoeker de activiteit betreedde. | nnt communications corporation | GEO_ISPName |

## Sessiegegevens {#session}

| Kenmerknaam | Beschrijving van kenmerk | Samplewaarden | Systeemnaam |
| --- | --- | --- | --- |
| Bezoekersprofiel - Waarde van LiveTime-order voor activiteit | Hiermee geeft u de som op van alle bestelwaarden voor alle bezoeken/sessies aan een bepaalde activiteit. | Dubbel | SES_CUMULATIVE_ORDER_VALUE |
| Bezoekersprofiel - Levensduur activiteit op de site | Geeft de totale tijd aan die de bezoeker aan de site heeft doorgebracht, exclusief de huidige sessie, en wordt bijgewerkt wanneer de sessie verloopt. | Dubbele milliseconden | SES_TOTAL_TIME |
| Bezoekersprofiel -Gemiddelde paginaweergaven per bezoek tijdens activiteit | Hiermee geeft u het gemiddelde aantal paginaweergaven per sessie op, exclusief de huidige sessie. | Dubbel | SES_REQUESTS_PER_SESSION |
| Bezoekersprofiel - Gemiddelde tijd per bezoek | Hiermee geeft u de gemiddelde tijd per bezoek/sessie op. De huidige sessie is hier niet in opgenomen. | Dubbele milliseconden | SES_TIME_PER_SESSION |
| Bezoekersprofiel - Eerste bezoek | Geeft de tijd aan van het eerste bezoek waarmee de gebruiker interactie heeft gehad [!DNL Target]. | Dubbele milliseconden | SES_PROFILE_CREATION_TIME |
| Bezoekersprofiel - Uren sinds laatste bezoek | Geeft de uren aan sinds het laatste bezoek aan deze specifieke activiteit. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. | SES_HOURS_SINCE_LAST_VISIT |
| Bezoekersprofiel - Impressies van locatie/inhoud | Hiermee wordt het aantal indrukkingen opgegeven voor een bepaalde locatie/inhoudscombinatie in een bepaalde activiteit. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. | SES_CUMULATIVE_ACTION_[LOCATION_ID]_[CONTENT_ID] |
| Bezoekersprofiel - Laatste [!DNL Target] Interactie | Hiermee wordt de tijd van de laatste interactie opgegeven met [!DNL Target]. Interactie vindt plaats op elke [!DNL Target] verzoek omdat de huidige implementatie van [!DNL Target] werkt het profiel bij elke aanvraag. | Dubbele milliseconden | SES_PROFILE_UPDATE_TIME |
| Bezoekersprofiel - Pagina&#39;s weergegeven voor activiteit | Hiermee geeft u het aantal weergaven van de totale pagina (afbeeldingen) op, inclusief het huidige bezoek/de huidige sessie totdat de bezoeker de activiteit start. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. | SES_TOTAL_PAGE_VIEWS |
| Bezoekersprofiel - Paginaweergaven in huidig bezoek | Hiermee geeft u het aantal paginaweergaven op in de huidige bezoek/sessie totdat de bezoeker de activiteit start. Meer in het bijzonder het aantal indrukken. Dit zijn geen echte paginaweergaven, maar het aantal keren dat de aanvraag Target heeft bereikt. Doel kan geen onderscheid maken tussen time-outs of andere redenen waarom de gebruiker de inhoud niet heeft ontvangen of weergegeven. | Dubbel (alleen geheel getal positief) | SES_SESSION_POSITION |
| Bezoekersprofiel - Begin van huidig bezoek | Hiermee geeft u de tijd op waarop het huidige bezoek/de huidige sessie met Target is gestart. Het bezoek aan Target kan worden gestart zonder een activiteit in te voeren. Al dat wordt vereist is een vraag aan om het even welk [!DNL Target] verzoek. Een bezoeker kan enige tijd duren voordat de activiteit wordt betreden en de opname wordt gemaakt. | Dubbele milliseconden | SES_SESSION_START |
| Bezoekersprofiel - Begin van het meest recente bezoek | Geeft de tijd aan waarop het laatste bezoek of de laatste sessie moet worden uitgevoerd [!DNL Target] begonnen. Dit kenmerk wordt bijgewerkt wanneer de sessie verloopt.<br>Als dit de eerste sessie voor de bezoeker is, resulteert dit in `LAST_SESSION_START = 0.` | Dubbele milliseconden | SES_LAST_SESSION_START |
| Bezoekersprofiel - Tijd sinds meest recente bezoek bij eerste intrede van activiteit | Geeft de duur aan tussen de vorige sessie en de tijd waarop de gebruiker de activiteit invoert en de momentopname wordt uitgevoerd. | Dubbele milliseconden | SES_RECENCY |
| Bezoekersprofiel - Bezoek de tijd voordat u de activiteit betreedt | Hiermee wordt het verschil opgegeven tussen de laatste interactie met [!DNL Target] en wanneer het huidige bezoek is begonnen. Dit kenmerk kan worden beschouwd als een bezoek-/sessieduur totdat de gebruiker de activiteit invoert en de momentopname wordt uitgevoerd.<br>Negatieve waarden treden op wanneer de sessie start en de laatste updatetijd door dezelfde persoon wordt geactiveerd [!DNL Target] vraag. Negatieve waarden moeten worden beschouwd als 0 (nul). | Dubbele milliseconden | SES_SESSION_TIME |
| Bezoekersprofiel - Totaal aantal bezoeken | Geeft het totale aantal bezoeken/sessies aan. Omvat niet het huidige bezoek/de zitting. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. | SES_TOTAL_SESSIONS |
| Bezoekersprofiel - Totaal aantal bezoeken aan activiteit | Geeft het aantal bezoeken aan een bepaalde activiteit aan. Als er geen vorig bezoek is, keert 0 (nul) terug. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. | SES_PREVIOUS_VISIT_COUNT |
| Bezoekersprofiel - Totaal aantal bezoeken aan activiteit met conversie | Hiermee geeft u het aantal bezoeken/sessies voor een bepaalde activiteit op wanneer er ten minste één conversie heeft plaatsgevonden tijdens het bezoek. | Dubbel | SES_CUMULATIVE_SUCCESSES |
| Bezoekersprofiel - Bezoek aan activiteit zonder conversie | Aantal bezoeken/sessies zonder conversies naar een bepaalde activiteit. Deze waarde wordt na conversie weer op nul ingesteld, of -1 als er geen conversie heeft plaatsgevonden. | Dubbel (alleen geheel getal als positief getal) 1, 2, 3, enz. | SES_SUCCESS_RECENCY |
