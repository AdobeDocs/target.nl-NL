---
keywords: rapporten;statistische methodologie;statistische berekeningen;statistieken;gemiddelde;omrekeningskoers;inkomsten per bezoeker;rpv;betrouwbaarheidsinterval;lift;welkomsttest;offlineberekeningen
description: Meer informatie over de statistische berekeningen in de handleiding [!UICONTROL A/B Test] activiteiten in [!DNL Adobe Target].
title: Hoe kan ik leren over de statistische berekeningen die worden gebruikt in [!UICONTROL A/B Test] Activiteiten?
feature: Reports
exl-id: 5f7377b9-0567-4b6f-8968-4696b2088d0a
source-git-commit: f997b6a0ea9e0cebf7b414c029971d8520f8b95f
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# Statistische berekeningen voor A/Bn-tests

In dit artikel worden de gedetailleerde statistische berekeningen beschreven die in de handmatige A/Bn-tests in [!DNL Adobe Target]. Definities worden gegeven voor [!UICONTROL Conversion Rate], [!UICONTROL Confidence Interval of Conversion Rate], [!UICONTROL Lift], [!UICONTROL Confidence Interval for Lift], en [!UICONTROL Confidence].

>[!NOTE]
>
>De informatie in dit artikel vervangt de *Adobe Target-berekeningen voor A/B-tests* pdf-bestand dat eerder beschikbaar was voor downloaden op deze site.

![Het rapport van het doel dat toont [!UICONTROL Conversion Rate], [!UICONTROL Average Lift and Confidence Interval], en [!UICONTROL Confidence] van een A/B-testactiviteit.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## Gemiddelde prestaties

In de volgende sectie worden de berekeningen beschreven die in de vorige illustratie zijn gebruikt.

### Omzetsnelheid en inkomsten per bezoeker (RPV)-campagnes

In de volgende afbeelding ziet u [!UICONTROL Conversion Rate], [!UICONTROL Confidence Interval of Conversion Rate]en het aantal [!UICONTROL Conversions] in een [!DNL Target] verslag. De eerste regel toont bijvoorbeeld dat voor Experience A: de [!UICONTROL Conversion Rate] is 25,81% met a [!UICONTROL Confidence Interval] van ±7,7% en 32 omzettingen werden geregistreerd. Aangezien 124 bezoekers de ervaring hebben gezien, komt dit overeen met 32/124 = 25,81%.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

de omrekeningskoers of **gemiddelde**, *μ<sub>ν</sub>*, voor elke ervaring *ν* in een experiment wordt gedefinieerd als een verhouding tussen de som van de metrische waarden en het aantal eenheden dat aan die meting is toegewezen; *N<sub>ν</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

Hier,

* *Y<sub>ν</sub>* is de waarde van metrisch voor elke eenheid *i*, die is toegewezen aan een bepaalde ervaring *ν*.

* De som over eenheden *i* hangt af van de keuze van de telmethode.

   * Indien *[!UICONTROL Visitors]* wordt gebruikt als telmethode, is elke eenheid een unieke bezoeker die wordt gedefinieerd als een unieke deelnemer aan de activiteit gedurende de levensduur van de activiteit.
   * Indien *[!UICONTROL Visits]* wordt gebruikt als telmethode, is elke eenheid een uniek bezoek dat wordt gedefinieerd als een unieke deelnemer aan een ervaring tijdens een [!DNL Target] sessie (met een unieke `sessionId`). Wanneer de `sessionId` wanneer de bezoeker de conversiestap bereikt, wordt een nieuw bezoek geteld.
   * Indien *[!UICONTROL Activity Impressions]* wordt gebruikt als telmethode, is elke eenheid een unieke indruk die wordt gedefinieerd als elke keer dat een bezoeker een pagina van de activiteit laadt.

## [!UICONTROL Confidence Interval of Mean]/[!UICONTROL Conversion Rate]

Het betrouwbaarheidsinterval van de omrekeningskoers wordt intuïtief gedefinieerd als een bereik van mogelijke omrekeningskoersen dat consistent is met de onderliggende gegevens.

Bij het uitvoeren van experimenten is de conversiesnelheid voor een bepaalde ervaring een *schatten* van de &quot;werkelijke&quot; omrekeningskoers. Om de onzekerheid in deze raming te kwantificeren, [!DNL Target] gebruikt een betrouwbaarheidsinterval. [!DNL Target] er wordt altijd een betrouwbaarheidsinterval van 95% gerapporteerd, wat betekent dat uiteindelijk 95% van de berekende betrouwbaarheidsintervallen de werkelijke omrekeningskoers van de ervaring bevat.

Een 95% betrouwbaarheidsinterval van de omrekeningskoers *μ<sub>ν</sub>* wordt gedefinieerd als het waardebereik:

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

Wanneer de standaardfout voor het gemiddelde wordt gedefinieerd als

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

Wanneer een onpartijdige schatting van de standaardafwijking van het monster wordt gebruikt:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

Wanneer de campagne een campagne van het omzettingspercentage is (d.w.z., is de omzettings metrisch binair), vermindert de standaardfout tot:

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## Optillen

In de volgende afbeelding ziet u [!UICONTROL Lift] en [!UICONTROL Confidence Interval of Lift] in een [!DNL Target] Rapport. Het getal vertegenwoordigt het gemiddelde van het bereik van de liftgrenzen en de pijl geeft aan of de lift positief of negatief is. De pijl wordt grijs weergegeven totdat het vertrouwen 95% bereikt. Als het vertrouwen de drempel bereikt, is de pijl groen of rood op basis van een positieve of negatieve lift.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

De lift tussen een ervaring  *ν* en de controleervaring *ν<sub>0</sub>* is de relatieve &quot;delta&quot; in omrekeningskoersen, gedefinieerd als

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

Indien de afzonderlijke omrekeningskoersen overeenkomen met de hierboven omschreven waarden. Eenvoudiger,

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

Indien de omrekeningskoers van de controleervaring *ν<sub>0</sub>* 0 is, er is geen lift.

## [!DNL Confidence Interval of Lift]

De grafiek van het klokveld in de [!UICONTROL Average Lift and Confidence Interval] de kolom staat voor de gemiddelde waarde en 95% [!UICONTROL Confidence Interval of Lift]. Het veld is grijs wanneer het betrouwbaarheidsinterval van een bepaalde ervaring met niet-besturing overlapt met het betrouwbaarheidsinterval van de controleervaring. Het kader is groen of rood wanneer het bereik van het betrouwbaarheidsinterval van een bepaalde ervaring boven of onder het betrouwbaarheidsinterval van de ervaring ligt.

De standaardfout van de lift tussen een ervaring  *ν* en de controleervaring  *ν<sub>0</sub>* wordt gedefinieerd als:

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="metrisch gemiddelde"></p>

Vervolgens is het 95% betrouwbaarheidsinterval van de lift:

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

Deze berekening gebruikt de methode &quot;Delta&quot; en wordt beschreven [meer in detail in dit document](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL Confidence]

De laatste kolom toont het vertrouwen in een [!DNL Target] verslag. Het vertrouwen van een ervaring is een waarschijnlijkheid (uitgedrukt als percentage) om een minder extreem resultaat te behalen dan het resultaat dat wordt waargenomen, gezien de nulhypothese waar is. Wat p-waarden betreft, wordt het weergegeven vertrouwen *1 - p-waarde*. Intuïtief betekent een hoger vertrouwen dat het minder waarschijnlijk is dat de controle- en niet-controleervaring gelijke omrekeningskoersen hebben.

In [!DNL Target], met twee staarten **T-test van Welch** tussen de testervaring en de controleervaring wordt uitgevoerd om te testen of de test- en controleervaringen hetzelfde zijn. Omdat we meestal niet weten of de grootte en variaties van de monsters van twee groepen hetzelfde zijn voordat we het experiment uitvoeren, en [!DNL Target] staat u ook toe om ongelijke percentages van verkeer te hebben die naar elke ervaring worden verzonden, veronderstellen wij niet dat de variantie voor elke ervaring gelijk is. Welch&#39;s t-test wordt dus gekozen in plaats van de t-test van Student.

Om de t-test van Welch uit te voeren, beginnen we eerst de t-statistiek en de vrijheidsgraden te berekenen en vervolgens een t-test met twee trappen uit te voeren om de p-waarde te genereren. Tot slot berekenen we het vertrouwen op basis van p-waarde.

De *t*-statistiek wordt gedefinieerd als het verschil tussen de middelen van twee onafhankelijke willekeurige variabelen; *ν* en *ν<sub>0</sub>*, gedeeld door de standaardfout van het verschil:

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

Wanneer *μ<sub>v</sub>* en *μ<sub>v0</sub>* zijn de middelen *ν*  en *ν<sub>0</sub>* en de standaardfout van het verschil tussen *μ<sub>v</sub>* en *μ<sub>v0</sub>* worden gegeven door:

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

Wanneer *σ<sup>2</sup><sub>v</sub>* en *σ<sup>2</sup><sub>v<sub>0</sub></sub>* de verschillen tussen twee ervaringen *ν*  en *ν<sub>0</sub>* en *N<sub>v</sub>* en *N<sub>v<sub>0</sub></sub>* zijn voorbeeldgrootten voor *ν* en *ν<sub>0</sub>* respectievelijk.

Voor de T-test van Welch wordt de vrijheidsgraad als volgt berekend:

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

en de mate van vrijheid voor *ν*  en *ν<sub>0</sub>* worden gedefinieerd als:

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

Vervolgens kan de p-waarde worden berekend uit het gebied in de staarten van het *t*-distributie:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

Ten slotte werd het vertrouwen in [!DNL Target] wordt gedefinieerd als:

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## Berekeningen offline uitvoeren

De [gedownload CSV-rapport](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) omvat alleen onbewerkte gegevens en omvat geen berekende meetwaarden, zoals inkomsten per bezoeker, lift of betrouwbaarheid die voor A/B-tests worden gebruikt.

Als u deze statistische hoeveelheden wilt berekenen, downloadt u de [!DNL Target] [Complete betrouwbaarheidscalculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel-bestand om de waarde van de activiteit in te voeren.
