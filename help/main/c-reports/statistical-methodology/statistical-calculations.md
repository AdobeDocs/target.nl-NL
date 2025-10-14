---
keywords: rapporten;statistische methodologie;statistische berekeningen;statistieken;gemiddelde;omrekeningskoers;inkomsten per bezoeker;rpv;betrouwbaarheidsinterval;lift;welkomsttest;offlineberekeningen
description: Meer informatie over de statistische berekeningen die worden gebruikt in handmatige [!UICONTROL A/B Test] -activiteiten in  [!DNL Adobe Target] .
title: Hoe kan ik meer leren over de statistische berekeningen die worden gebruikt in [!UICONTROL A/B Test] -activiteiten?
feature: Reports
exl-id: 5f7377b9-0567-4b6f-8968-4696b2088d0a
source-git-commit: 18f8ccd3edfda635c3f47bd67ff0b7a516748fa8
workflow-type: tm+mt
source-wordcount: '1143'
ht-degree: 0%

---

# Statistische berekeningen voor A/Bn-tests

In dit artikel worden de gedetailleerde statistische berekeningen beschreven die in handmatige A/Bn-tests in [!DNL Adobe Target] worden gebruikt. Definities worden opgegeven voor [!UICONTROL Conversion Rate] , [!UICONTROL Confidence Interval of Conversion Rate] , [!UICONTROL Lift] , [!UICONTROL Confidence Interval for Lift] en [!UICONTROL Confidence] .

>[!NOTE]
>
>De informatie in dit artikel vervangt de *Berekeningen van Adobe Target voor het Testen A/B* pdf- dossier dat eerder voor download op deze plaats beschikbaar was.

![&#x200B; rapport dat van het Doel [!UICONTROL Conversion Rate] toont, [!UICONTROL Average Lift and Confidence Interval], en [!UICONTROL Confidence] van een activiteit van de Test A/B.](/help/main/c-reports/statistical-methodology/img/target_report.png)

## Gemiddelde prestaties

In de volgende sectie worden de berekeningen beschreven die in de vorige illustratie zijn gebruikt.

### Omzetsnelheid en inkomsten per bezoeker (RPV)-campagnes

De volgende afbeelding toont [!UICONTROL Conversion Rate] , [!UICONTROL Confidence Interval of Conversion Rate] en het aantal [!UICONTROL Conversions] in een [!DNL Target] -rapport. De eerste regel toont bijvoorbeeld dat voor Experience A: de waarde [!UICONTROL Conversion Rate] 25,81% is, waarbij een [!UICONTROL Confidence Interval] van ±7,7% en 32 conversies zijn opgenomen. Aangezien 124 bezoekers de ervaring hebben gezien, komt dit overeen met 32/124 = 25,81%.

<p style="text-align:center;"><img width="25%" src="img/conv_rate.png"></p>

De omzettingspercentage of **gemiddelde**, *ν <sub></sub>*, voor elke ervaring *ν* in een experiment wordt bepaald als verhouding van de som metrisch aan het aantal eenheden die aan metrisch, *worden toegewezen N <sub> ν</sub>*:

<p style="text-align:center;"><img width="125px" src="img/mean_definition.png"></p>

Hier,

* *Y <sub> ν</sub>* is de waarde van metrisch voor elke eenheid *i*, die aan een bepaalde ervaring *ν* is toegewezen.

* De som over eenheden *i* hangt van de keus van tellingsmethodologie af.

   * Als *[!UICONTROL Visitors]* wordt gebruikt als de telmethode, is elke eenheid een unieke bezoeker die wordt gedefinieerd als een unieke deelnemer aan de activiteit gedurende de levensduur van de activiteit.
   * Als *[!UICONTROL Visits]* wordt gebruikt als de telmethode, is elke eenheid een uniek bezoek dat wordt gedefinieerd als een unieke deelnemer aan een ervaring tijdens een [!DNL Target] -sessie (met een unieke `sessionId` ). Wanneer `sessionId` verandert, of de bezoeker de omzettingsstap bereikt, wordt een nieuw bezoek geteld.
   * Als *[!UICONTROL Activity Impressions]* wordt gebruikt als de telmethode, is elke eenheid een unieke indruk die wordt gedefinieerd als elke keer dat een bezoeker een pagina van de activiteit laadt.

## [!UICONTROL Confidence Interval of Mean]/[!UICONTROL Conversion Rate]

Het betrouwbaarheidsinterval van de omrekeningskoers wordt intuïtief gedefinieerd als een bereik van mogelijke omrekeningskoersen dat consistent is met de onderliggende gegevens.

Wanneer het runnen van experimenten, is de omzettingspercentage voor een bepaalde ervaring een *schatting* van de &quot;ware&quot;omzettingspercentage. [!DNL Target] gebruikt een betrouwbaarheidsinterval om de onzekerheid in deze schatting te kwantificeren. [!DNL Target] geeft altijd een 95%-betrouwbaarheidsinterval weer, wat betekent dat uiteindelijk 95% van de berekende betrouwbaarheidsintervallen de werkelijke conversiesnelheid van de ervaring bevat.

Er wordt ook een &quot;Vertrouwensnummer&quot; gerapporteerd naast de huidige leidende of winnende ervaring. Dit cijfer wordt alleen gerapporteerd als de [!UICONTROL Confidence] -ervaring van de regelaar ten minste 60% bereikt. Als er twee ervaringen in de activiteit aanwezig zijn, geeft dit aantal het betrouwbaarheidsniveau aan dat de ervaring beter presteert dan de andere ervaring. Als de activiteit meer dan twee ervaringen bevat, geeft dit aantal het betrouwbaarheidsniveau aan dat de ervaring beter presteert dan de gedefinieerde ervaring bij &quot;Besturing&quot;. Als de &quot;Controle&quot;ervaring het winnen is, wordt geen &quot;Vertrouwen&quot;cijfer gemeld.

Een 95% betrouwbaarheidsinterval van omzettingspercentage *wordt <sub> ν</sub>* bepaald als waaier van waarden:

<p style="text-align:center;"><img width="30%" src="img/confidence_interval.png"></p>

Wanneer de standaardfout voor het gemiddelde wordt gedefinieerd als

<p style="text-align:center;"><img width="75px" src="img/se_conv_continuous.png"></p>

Wanneer een onpartijdige schatting van de standaardafwijking van het monster wordt gebruikt:

<p style="text-align:center;"><img width="200px" src="img/stdev_definition.png"></p>

Wanneer de campagne een campagne van het omzettingspercentage is (d.w.z., is de omzettings metrisch binair), vermindert de standaardfout tot:

<p style="text-align:center;"><img width="150px" src="img/se_conv.png"></p>

## Optillen

De volgende afbeelding toont [!UICONTROL Lift] en [!UICONTROL Confidence Interval of Lift] in een [!DNL Target] -rapport. Het getal vertegenwoordigt het gemiddelde van het bereik van de liftgrenzen en de pijl geeft aan of de lift positief of negatief is. De pijl wordt grijs weergegeven totdat het vertrouwen 95% bereikt. Als het vertrouwen de drempel bereikt, is de pijl groen of rood op basis van een positieve of negatieve lift.

<p style="text-align:center;"><img width="35%" src="img/lift.png"></p>

De lift tussen een ervaring *ν*, en de controleervaring *ν <sub> 0</sub>* is de relatieve &quot;delta&quot;in omzettingspercentages, die zoals worden bepaald

<p style="text-align:center;"><img width="15%" src="img/lift_definition.png"></p>

Indien de afzonderlijke omrekeningskoersen overeenkomen met de hierboven omschreven waarden. Eenvoudiger,

```
Lift(Experience N) = (Performance_Experience_N - Performance_Control)/ Performance_Control
```

Als de omzettingspercentage van de controleervaring *ν <sub> 0</sub>* 0 is, is er geen lift.

## [!DNL Confidence Interval of Lift]

De grafiek van het kavel in de [!UICONTROL Average Lift and Confidence Interval] kolom vertegenwoordigt de gemiddelde waarde en 95% [!UICONTROL Confidence Interval of Lift]. Het veld is grijs wanneer het betrouwbaarheidsinterval van een bepaalde ervaring met niet-besturing overlapt met het betrouwbaarheidsinterval van de controleervaring. Het kader is groen of rood wanneer het bereik van het betrouwbaarheidsinterval van een bepaalde ervaring boven of onder het betrouwbaarheidsinterval van de ervaring ligt.

De standaardfout van de lift tussen een ervaring *ν*, en de controleervaring *ν <sub> 0</sub>* wordt bepaald als:

<p style="text-align:center;"><img width="35%" src="img/se_lift.png" alt="metrisch gemiddelde"></p>

Vervolgens is het 95% betrouwbaarheidsinterval van de lift:

<p style="text-align:center;"><img width="40%" src="img/lift_CI.png"></p>

Deze berekening gebruikt de &quot;Delta&quot;methode, en wordt beschreven [&#x200B; meer in detail in dit document &#x200B;](/help/main/assets/confidence_interval_lift.pdf)

## [!UICONTROL Confidence]

In de laatste kolom ziet u het vertrouwen in een [!DNL Target] -rapport. Het vertrouwen van een ervaring is een kans (uitgedrukt als een percentage) om een resultaat te verkrijgen dat even extreem is als het resultaat dat wordt waargenomen, gezien de nulhypothese waar is. In termen van p-waarden, is het getoonde vertrouwen *1 - p-waarde*. Intuïtief betekent een hoger vertrouwen dat het minder waarschijnlijk is dat de controle- en niet-controleervaring gelijke omrekeningskoersen hebben.

In [!DNL Target], wordt een twee-staart **lelzen t-test** uitgevoerd tussen de testervaring en de controleervaring om te testen als de middelen van test en controleervaringen het zelfde zijn. Omdat we meestal niet weten of de grootte en variaties van de monsters van twee groepen hetzelfde zijn voordat we het experiment uitvoeren. [!DNL Target] geeft u ook de mogelijkheid om ongelijke percentages van het verkeer naar elke ervaring te sturen. Daarom gaan we er niet van uit dat de variantie voor elke ervaring gelijk is. Welch&#39;s t-test wordt dus gekozen in plaats van de t-test van Student.

Om de t-test van Welch uit te voeren, beginnen we eerst de t-statistiek en de vrijheidsgraden te berekenen en vervolgens een t-test met twee trappen uit te voeren om de p-waarde te genereren. Tot slot berekenen we het vertrouwen op basis van p-waarde.

*t* - statistiek wordt bepaald om het verschil van de middelen van om het even welke twee onafhankelijke willekeurige variabelen te zijn, *ν* en *ν <sub> 0</sub>*, die door de standaardfout van het verschil wordt verdeeld:

<p style="text-align:center;"><img width="100px" src="img/t_value.png"></p>

Waar *μ <sub> v</sub>* en *μ <sub> v0</sub>* de middelen van *ν* en *ν <sub> 0</sub>* respectievelijk, en de standaardfout van het verschil tussen *wordt /12 <sub> en</sub>* /v0 *door gegeven:<sub></sub>*

<p style="text-align:center;"><img width="150px" src="img/standard_error_diff.png"></p>

Waar *σ <sup> 2 </sup><sub> v</sub>* en *σ <sup> 2 </sup><sub> v <sub> 0</sub></sub>* zijn de varianties van twee ervaringen *ν* en *ν <sub> 0</sub>* respectievelijk, en *N <sub> v</sub>* en *N <sub> 8&rbrace; v <sub> 0</sub></sub>* is steekproefgrootte voor *ν* en *ν <sub> 0</sub>* respectievelijk.

Voor de T-test van Welch wordt de vrijheidsgraad als volgt berekend:

<p style="text-align:center;"><img width="180px" src="img/degree_of_freedom.png"></p>

En graad van vrijheid voor *ν* en *ν <sub> 0</sub>* worden bepaald als:

<p style="text-align:center;"><img width="100px" src="img/df_v.png"></p>

<p style="text-align:center;"><img width="100px" src="img/df_v0.png"></p>

Dan kan de p-waarde van het gebied in de staarten van *worden gegevens verwerkt t* - distributie:

<p style="text-align:center;"><img width="20%" src="img/p_value.png"></p>

Tot slot wordt het in [!DNL Target] gerapporteerde vertrouwen gedefinieerd als:

<p style="text-align:center;"><img width="20%" src="img/confidence.png"></p>

## Berekeningen offline uitvoeren

Het [&#x200B; gedownloade rapport CSV &#x200B;](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md) omvat slechts ruwe gegevens en omvat geen berekende metriek, zoals opbrengst per bezoeker, lift, of vertrouwen dat voor tests A/B wordt gebruikt.

Om deze statistische hoeveelheden gegevens te verwerken, download het [!DNL Target] [&#x200B; Volledige dossier van Excel van de Rekenmachine van het Vertrouwen &#x200B;](/help/main/assets/complete_confidence_calculator.xlsx) om de waarde van de activiteit in te voeren.
