---
keywords: gegevensvariaties;analyses;verschillen;variantie;a4t;analytische gegevens voor doel;analytische gegevens als bron van de rapportage;discrepanties;discrepantie
description: Leer over de verwachte gegevensvariaties tussen Adobe Target en Analytics wanneer het gebruiken van Analytics voor Doel (A4T) niet, die gegevensvariantie algeheel elimineert.
title: Wat is de verwachte Variantie van Gegevens tussen Analytics en A4T?
feature: Analyses voor doel (A4T)
translation-type: tm+mt
source-git-commit: 4abf975095c5e29eea42d67119a426a3922d8d79
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---


# Verwachte gegevensvariaties tussen Adobe Target en Adobe Analytics bij gebruik en niet bij gebruik van A4T

Informatie over verwachte gegevensvariaties tussen [!DNL Target] en Adobe [!DNL Analytics] wanneer *het gebruik van* en *niet* het gebruiken van Analytics als Rapporterende Bron (A4T). A4T verlaagt de gegevensvariantie aanzienlijk.

## Verwachte gegevensvariantie bij gebruik van A4T {#expected-using-a4t}

Met A4T, zowel gebruiken de Analytics als het Doel het melden van activiteiten de gegevens van de Analyse uitsluitend, zodat is er weinig verschil tussen de oplossingen in de activiteitenverslagen van het Doel. In sommige omstandigheden vergelijken klanten de gegevens van Target echter met de gegevens van Analytics buiten het bereik van de integratie A4T en ervaren ze dus de hieronder beschreven variantiekwesties.

Hier volgen enkele scenario&#39;s waarin u de verwachte gegevensvariatie kunt ervaren:

* A4T maakt het mogelijk dat een doelhit (boven aan pagina) optreedt, maar er vindt geen treffer voor Analytics (onder aan pagina) plaats. Stel dat een bezoeker de pagina laadt, maar de browser sluit voordat de analytische aanroep wordt geactiveerd. In deze gevallen sluit A4T de Target hit uit van de gegevens. Als u toestaat dat Target-hits (ook boven aan de pagina) worden geteld als analyseresultaten wanneer er geen daadwerkelijke analytische aanroep is, ontstaan er inconsistenties met de gegevensset in Analytics (bezoekersinflatie, enzovoort).

   Als een omleidingstest in Doel wordt opgezet om verkeer 50/50 (of 25/25/25, etc.) te verdelen, zou het gebruikersgedrag niet gelijkmatig kunnen worden verdeeld. Als u een ongelijkmatige splitsing ziet, betekent dit simpelweg dat één groep gebruikers er niet in is geslaagd een analytische aanroep op de bestemmingspagina uit te voeren meer dan de andere groepen wel hebben gedaan. Als de analytische aanroep voor één groep niet werd uitgevoerd, werd de Target-hit voor die gebruiker uitgesloten, waardoor de ongelijkheid ontstond.

   Adobe hoopt dit probleem in de toekomst aan te pakken terwijl Adobe-teams werken aan A4T op de Adobe Experience Platform. De teams van Adobe bepalen hoe te om deze verschillende gebeurtenissen te behandelen die op verschillende tijden op de pagina voorkomen.

   >[!NOTE]
   >
   >Een bekende kwestie weggaat die een beperkt aantal klanten veroorzaakt die omleidingen met A4T gebruiken om een hoger percentage van unstitched hit tarieven te zien. Zie [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Verwachte gegevensvariantie wanneer *geen* A4T {#expected-not-using-a4t} wordt gebruikt

Variaties van 15-20% zijn normaal, zelfs bij vergelijkbare gegevenssets. Systemen die verschillend tellen kunnen resulteren in veel hogere gegevensvariaties, tot wel 35-50%. Soms kunnen variaties zelfs hoger zijn.

Hoewel de werkelijke gegevens aanzienlijk kunnen variëren, zijn trends doorgaans consistent. Zolang de verschillen en trends consistent blijven, blijven de gegevens waardevol en nuttig. Als de verschillen en trends inconsistent zijn, kan dat betekenen dat er iets verkeerd wordt opgezet. Neem in dit geval contact op met uw accountvertegenwoordiger voor hulp.

[!DNL Analytics] gebruikt een systeem dat op bezoeken en transacties wordt gebaseerd, maar op bezoekers-gebaseerde metriek  [!DNL Target] gebruikt. Wanneer een bezoeker een pagina opent, telt het als een bezoek in [!DNL Analytics], maar [!DNL Target] telt niet het bezoek tot de voorwaarden in de activiteit worden geplaatst vervuld.

Rapporten in [!DNL Target] tonen prestaties die op de geselecteerde omzettingsdoos worden gebaseerd wanneer het bepalen van de activiteit. Deze conversiemaboxgegevens worden echter niet verzonden naar [!DNL Analytics], dat zijn eigen conversievariabelen heeft zoals gedefinieerd door uw [!DNL Analytics]-coderingsimplementatie. Waar u identieke gegevens verwacht (bijvoorbeeld als de bestelling van een detailhandelaar bevestigt dat de pagina zowel een conversiembox als een [!DNL Analytics] aankoopgebeurtenis bevat), kunnen de gegevens verschillen door de plaatsing van deze labels. Over het algemeen zijn de trends in de verslagen van beide producten vergelijkbaar.

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
* Eén enkel vak op meerdere pagina&#39;s, waarbij bezoekers op elk van deze pagina&#39;s worden geteld
* Activiteitsprioriteiten kunnen sommige bezoekers bevatten en andere op een pagina uitsluiten
* Bezoekers die eenmaal zijn geconverteerd, kunnen opnieuw worden geteld wanneer ze de activiteit opnieuw betreden
* [!DNL Analytics] telt alle omzettingen voor alle bezoeken en bezoekers, maar  [!DNL Target] telt alleen omzettingen voor die bezoeken en bezoekers die in de activiteit zijn opgenomen