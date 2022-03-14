---
keywords: gegevensvariaties;analyses;verschillen;variantie;a4t;analytische gegevens voor doel;analytische gegevens als bron van de rapportage;discrepanties;discrepantie
description: Meer informatie over de verwachte gegevensvariaties tussen Adobe [!DNL Target] en Analytics wanneer u Analytics niet gebruikt voor [!DNL Target] (A4T), waardoor gegevensvariatie volledig wordt verwijderd.
title: What Is the Expected Data Variance between Analytics and A4T?
feature: Analytics for Target (A4T)
exl-id: 9e63f309-8ec1-4ed5-a1f9-6c3098a7b8f6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Verwachte gegevensvariaties tussen Adobe [!DNL Target] en Adobe Analytics bij gebruik en niet bij gebruik van A4T

Informatie over verwachte gegevensvariaties tussen [!DNL Target] en Adobe [!DNL Analytics] wanneer *gebruiken* en *niet* het gebruiken van Analytics als Rapporterende Bron (A4T). A4T verlaagt de gegevensvariantie aanzienlijk.

## Verwachte gegevensvariantie bij gebruik van A4T {#expected-using-a4t}

Met A4T, zowel gebruiken de Analytics als het Doel het melden van activiteiten de gegevens van de Analyse uitsluitend, zodat is er weinig verschil tussen de oplossingen in de activiteitenverslagen van het Doel. In some circumstances, however, customers compare Target data to Analytics data outside the scope of the A4T integration and, thus, experience the variance issues described below.

Hier volgen enkele scenario&#39;s waarin u de verwachte gegevensvariatie kunt ervaren:

* A4T allows for the possibility that a Target hit (top of page) occurs, but no Analytics hit (bottom of page) occurs. Stel dat een bezoeker de pagina laadt, maar de browser sluit voordat de analytische aanroep wordt geactiveerd. In deze gevallen sluit A4T de Target hit uit van de gegevens. Als u toestaat dat Target-hits (ook boven aan de pagina) worden geteld als analyseresultaten wanneer er geen daadwerkelijke analytische aanroep is, ontstaan er inconsistenties met de gegevensset in Analytics (bezoekersinflatie, enzovoort).

   Als een omleidingstest in Doel wordt opgezet om verkeer 50/50 (of 25/25/25, etc.) te verdelen, zou het gebruikersgedrag niet gelijkmatig kunnen worden verdeeld. Als u een ongelijkmatige splitsing ziet, betekent dit simpelweg dat één groep gebruikers er niet in is geslaagd een analytische aanroep op de bestemmingspagina uit te voeren meer dan de andere groepen wel hebben gedaan. Als de analytische aanroep voor één groep niet werd uitgevoerd, werd de Target-hit voor die gebruiker uitgesloten, waardoor de ongelijkheid ontstond.

   Adobe hoopt dit probleem in de toekomst aan te pakken terwijl Adobe-teams werken aan A4T op de Adobe Experience Platform. De teams van Adobe bepalen hoe te om deze verschillende gebeurtenissen te behandelen die op verschillende tijden op de pagina voorkomen.

   >[!NOTE]
   >
   >Een bekende kwestie weggaat die een beperkt aantal klanten veroorzaakt die omleidingen met A4T gebruiken om een hoger percentage van unstitched hit tarieven te zien. Zie [Bekende problemen en opgeloste problemen](/help/main/r-release-notes/known-issues-resolved-issues.md#redirect).

## Verwachte gegevensvariantie wanneer *niet gebruiken* A4T {#expected-not-using-a4t}

Variaties van 15-20% zijn normaal, zelfs bij vergelijkbare gegevenssets. Systemen die verschillend tellen kunnen resulteren in veel hogere gegevensvariaties, tot wel 35-50%. Soms kunnen variaties zelfs hoger zijn.

Hoewel de werkelijke gegevens aanzienlijk kunnen variëren, zijn trends doorgaans consistent. Zolang de verschillen en trends consistent blijven, blijven de gegevens waardevol en nuttig. Als de verschillen en trends inconsistent zijn, kan dat betekenen dat er iets verkeerd wordt opgezet. Neem in dit geval contact op met uw accountvertegenwoordiger voor hulp.

[!DNL Analytics] gebruikt een systeem dat is gebaseerd op bezoeken en transacties, maar [!DNL Target] gebruikt op bezoekers gebaseerde meetgegevens. Wanneer een bezoeker een pagina opent, telt deze als een bezoek in [!DNL Analytics], maar [!DNL Target] telt het bezoek niet mee totdat aan de voorwaarden van de activiteit is voldaan.

Reports in [!DNL Target] show performance based on the conversion mbox selected when defining the activity. Deze gegevens van het conversiemabox worden echter niet verzonden naar [!DNL Analytics], dat zijn eigen omzettingsvariabelen heeft zoals die door uw [!DNL Analytics] tagging-implementatie. Where you expect identical data (for example, if a retailer&#39;s order confirm that page contains both a conversion mbox and an [!DNL Analytics] purchase event), data can differ due to the placement of these tags. In general, trends in the two products&#39; reports are similar.

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
* [!DNL Analytics] telt alle omzettingen voor alle bezoeken en bezoekers , maar [!DNL Target] tellingen uitsluitend conversies voor bezoeken en bezoekers die deel uitmaken van de activiteit
