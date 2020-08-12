---
keywords: data variances;analytics;differences;variance;a4t;analytics for target;analytics as the reporting source;discrepancies;discrepancy
description: Informatie over verwachte gegevensvariaties tussen Target en Adobe Analytics bij het niet gebruiken van Analytics als Rapporterende Bron (A4T), die gegevensvariatie volledig elimineert.
title: Gegevensvariaties verwacht bij gebruik van A4T
feature: null
topic: Advanced
uuid: 61bef460-8613-4251-b1b2-b6226ec86d9b
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# Verwachte gegevensvariaties tussen Doel en Analytics bij gebruik en niet bij gebruik van A4T{#expected-data-variances-when-not-using-a-t}

Informatie over verwachte gegevensvariaties tussen [!DNL Target] en Adobe [!DNL Analytics] wanneer *het gebruiken* van en *niet* het gebruiken van Analytics als Rapporterende Bron (A4T). A4T verlaagt de gegevensvariantie aanzienlijk.

## Verwachte gegevensvariantie bij gebruik van A4T {#expected-using-a4t}

Met A4T, zowel gebruiken de Analytics als het Doel het melden van activiteiten de gegevens van de Analyse uitsluitend, zodat is er weinig verschil tussen de oplossingen in de activiteitenverslagen van het Doel. In sommige omstandigheden, echter, zouden de klanten de gegevens van het Doel met de gegevens van Analytics buiten het werkingsgebied van de integratie A4T kunnen vergelijken en, zo, ervaren de variance hieronder beschreven kwesties.

Hier zijn een paar scenario&#39;s waarin u verwachte gegevensvariantie zou kunnen ervaren:

* A4T maakt het mogelijk dat een doelhit (boven aan pagina) optreedt, maar er vindt geen treffer voor Analytics (onder aan pagina) plaats. Een voorbeeld hiervan is als de gebruiker de pagina laadt, maar de browser sluit voordat de analytische aanroep wordt geactiveerd. In deze gevallen sluit A4T de Target hit uit van onze gegevens. De reden hiervoor is dat het toestaan van Target-hits (opnieuw boven aan de pagina) om te tellen als analyseresultaten zonder een daadwerkelijke analytische aanroep tot inconsistenties zou leiden met de gegevensset in Analytics (bezoekersinflatie, enz.).

   Als een omleidingstest in Target wordt opgezet om verkeer 50/50 (of 25/25/25/25 enz.) te verdelen, zou het gebruikersgedrag niet gelijkmatig kunnen worden verdeeld. Als u een ongelijke splitsing ziet, betekent dit gewoon dat één groep gebruikers een analytische aanroep op de bestemmingspagina niet meer heeft uitgevoerd dan de andere groep(en). Als de analytische aanroep voor één groep niet werd uitgevoerd, werd de Target-hit voor die gebruiker uitgesloten, waardoor de ongelijkheid ontstond.

   Dit is iets wat we in de toekomst willen aanpakken als we werken aan een A4T op de Adobe Experience Platform. Onze teams werken door hoe u deze verschillende gebeurtenissen het beste kunt afhandelen op verschillende tijdstippen op de pagina.

   >[!NOTE]
   >
   >Een bekende kwestie weggaat die een beperkt aantal klanten veroorzaakt die omleidingen met A4T gebruiken om een hoger percentage van unstitched hit tarieven te zien. Bekende [problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#redirect)bekijken.

* Stel dat u een activiteit voor automatisch toewijzen maakt die open staat voor alle bezoekers van een bepaalde pagina. Omdat de auto-Wijs activiteiten geen A4T steunen, worden alle activiteitengegevens verzameld door [!DNL Target]. U zou kunnen verwachten dat de bezoekers aan de activiteit in de [!DNL Target] rapportering de bezoekers aan die pagina in de [!DNL Analytics] rapportering voor de zelfde datumwaaier zouden moeten aanpassen. Dit is een scenario waarin de hieronder beschreven variantie wordt verwacht.

   Voor een volledige lijst van activiteitentypes die A4T steunen, zie de [Gesteunde Types](../../c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA)van Activiteit.

## Verwachte gegevensvariantie wanneer *geen A4T wordt gebruikt* {#expected-not-using-a4t}

Variaties van 15-20% zijn normaal, zelfs bij vergelijkbare gegevenssets. Systemen die verschillend tellen kunnen resulteren in veel hogere gegevensvariaties, tot wel 35-50%. In sommige gevallen kunnen verschillen zelfs nog groter zijn.

Hoewel de werkelijke gegevens aanzienlijk kunnen variëren, zijn trends doorgaans consistent. Zolang de verschillen en trends consistent blijven, blijven de gegevens waardevol en nuttig. Als de verschillen en trends inconsistent zijn, kan dat betekenen dat er iets verkeerd wordt opgezet. Neem in dit geval contact op met uw accountvertegenwoordiger voor hulp.

[!DNL Analytics] gebruikt een systeem dat op bezoeken en transacties wordt gebaseerd, maar op bezoekers-gebaseerde metriek [!DNL Target] gebruikt. Dat betekent dat wanneer een bezoeker een pagina opent, het als een bezoek in telt [!DNL Analytics], maar [!DNL Target] niet het bezoek telt totdat aan de voorwaarden van de activiteit is voldaan.

Rapporten in [!DNL Target] tonen prestaties die op de omzettingsdoos worden gebaseerd die bij het bepalen van de activiteit wordt geselecteerd, maar deze omzettingsgegevens worden niet verzonden naar [!DNL Analytics], die zijn eigen omzettingsvariabelen zoals die door uw [!DNL Analytics] het etiketteren implementatie worden bepaald heeft. In gevallen waarin identieke gegevens kunnen worden verwacht (bijvoorbeeld als de orderbevestigingspagina van een detailhandelaar zowel een conversiembox als een [!DNL Analytics] aankoopgebeurtenis bevat), kunnen de gegevens verschillen als gevolg van de plaatsing van deze tags. Over het algemeen zouden de trends in de verslagen van beide producten op dezelfde wijze moeten zijn.

De verwachte gegevensvariaties kunnen door zowel technische als bedrijfsvariaties worden veroorzaakt.

### Voorbeelden van technische variaties {#section_C3B50ED2E2F9416FAC91437CF1A87369}

Het volgende kan gegevensvariaties veroorzaken op basis van technische verschillen:

* [!DNL Target] bezoekers moeten cookies en JavaScript toestaan
* cookies van de eerste en derde partij worden op verschillende wijze verwerkt; als gevolg hiervan komen de gegevens van deze cookietypen niet overeen
* Relatieve locatie van tags op pagina&#39;s en &#39;lekkage&#39; veroorzaakt door bezoekers die de pagina verlaten voordat deze volledig wordt geladen
* Overwegingen voor tijdzones
* Verschillen in de meeteenheden

### Voorbeelden van bedrijfsvariaties {#section_2E1EB5E15BB64A1A80E4CDB1A5062AEE}

Het volgende kan gegevensvariaties veroorzaken die op bedrijfsverschillen worden gebaseerd:

* Verschillen tussen meetgegevens bezoekers en bezoekers
* Bij gerichte activiteiten zijn sommige bezoekers uitgesloten
* Er kan één box op meerdere pagina&#39;s worden geplaatst, waarbij bezoekers op elk van deze pagina&#39;s worden geteld
* Activiteitsprioriteiten kunnen sommige bezoekers bevatten en andere op een pagina uitsluiten
* Bezoekers die eenmaal zijn geconverteerd, kunnen opnieuw worden geteld wanneer ze de activiteit opnieuw betreden
* [!DNL Analytics] telt alle omzettingen voor alle bezoeken en bezoekers, maar [!DNL Target] telt alleen omzettingen voor die bezoeken en bezoekers die deel uitmaken van de activiteit