---
keywords: Doel;AP-rapporten;geautomatiseerde verpersoonlijkingsrapporten;automatisch doel;automatisch doel;automatisch doel;automatisch doelrapport;automatisch doelrapport;verpersoonlijking;inzichten;geautomatiseerde segmenten;vk;vaak gestelde vragen
description: Leer hoe verschillende segmenten die worden gedefinieerd door Adobe [!DNL Target] de verpersoonlijkingsmodellen antwoorden aan aanbiedingen/ervaringen in de activiteit door het Geautomatiseerde rapport van Segmenten te bekijken.
title: Wat is het Geautomatiseerde Rapport van Segmenten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '2054'
ht-degree: 0%

---

# [!UICONTROL Automated Segments] verslag

Informatie over de [!UICONTROL Automated Segments] rapport, één van de twee gespecialiseerde rapporten beschikbaar aan gebruikers van [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u rapporten over persoonlijke voorkeuren gebruikt:
>
>* AP- en AT-activiteiten zijn beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Ze zijn niet inbegrepen bij [!DNL Target Standard] zonder [!DNL Target Premium] licentie.
>
>* [!UICONTROL Personalization Insights] rapporten zijn beschikbaar slechts voor AP en bij activiteiten die een doel van de omzetoptimalisering gebruiken. Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.
>
>* [!UICONTROL Personalization Insights] rapporten zijn alleen beschikbaar als de [!UICONTROL Primary Goal] is geselecteerd uit het [!UICONTROL Report Metric] vervolgkeuzelijst.
>
>* [!UICONTROL Personalization Insights] de rapporten worden gesteund in [standaardomgeving](/help/main/administrating-target/hosts.md) alleen.
>
>* [!UICONTROL Personalization Insights] rapporten worden alleen gegenereerd voor activiteiten in het [!UICONTROL Live] en ten minste 15 dagen in werking zijn gesteld en verkeer ontvangen.


Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

## Heb toegang tot het Geautomatiseerde rapport van Segmenten {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klikken **[!UICONTROL Activities]** en klik vervolgens op de gewenste knop [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteit uit de lijst.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van te selecteren [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Property], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] vervolgkeuzelijsten.

1. Klik op **[!UICONTROL Reports]**.

   De [Automated Personalization-overzicht](/help/main/c-reports/personalization-reports/reports-ap.md) of [Overzicht autom. doel](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) rapportvertoningen, die informatie over de prestaties van uw activiteiten verstrekken, die door het eerste het schermpictogram wordt vertegenwoordigd. De twee extra pictogrammen vertegenwoordigen de twee rapporten van de Inzichten van de Personalisatie: Geautomatiseerde segmenten en belangrijke kenmerken. Auto-Target heeft een extra grafiekpictogram voor de grafische mening van [!UICONTROL Summary] verslag.

   ![Rapport over persoonlijke inzichten in Adobe Target](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >De [!UICONTROL Automated Segments] -rapport is pas beschikbaar 15 dagen nadat je je activiteit hebt geactiveerd. Tijdens deze eerste periode hebt u geen toegang tot dit rapport of kunt u op de knop [!UICONTROL Automated Segments] pictogram. Als er 15 dagen zijn verstreken en er voldoende gepersonaliseerd verkeer in uw activiteit is, kan de [!UICONTROL Automated Segments] verslag zal beschikbaar zijn.

1. Na 15 dagen vanaf het activeren van de activiteit kunt u op de knop **[!UICONTROL Automated Segments]** pictogram.

   ![Pictogram Automatisch segment](/help/main/c-reports/assets/icon-automated-sements.png)

1. Selecteer het gewenste datumbereik.

   In tegenstelling tot [!UICONTROL Summary] verslag (prestatierapportage), [!UICONTROL Personalization Insights], met inbegrip van [!UICONTROL Automated Segments], is alleen beschikbaar voor vaste datumbereiken: 15 dagen, 30 dagen en 60 dagen. Deze vaste datumbereiken staan [!UICONTROL Personalization Insights] om een groot genoeg bereik aan gegevens te gebruiken om de kans te verkleinen dat u inzichten afleidt van een kortstondig patroon in uw activiteit. De twee besluiten u voor uw datumwaaier kunt maken zijn de &quot;Datum van het Eind&quot;en &quot;Duur.&quot; U zult merken dat het &quot;Begin&quot;grijs uit is. De begindatum wordt automatisch gewijzigd op basis van uw selecties voor de einddatum en -duur.

   ![Kalender in Adobe Target-rapport](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   U hebt toegang tot de beschikbare vaste datumbereiken via de [!UICONTROL Choose Duration] vervolgkeuzelijst.

   ![Vervolgkeuzelijst Duur in Adobe Target](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Controleer de [!UICONTROL Automated Segments] rapportgegevens.

   ![Rapport Automated Segments](/help/main/c-reports/assets/automated_segments_report.png)

1. (Optioneel) [Het rapport downloaden in CSV-indeling](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) voor analyse in Excel en andere hulpmiddelen.

   >[!NOTE]
   >
   >Het gebruikersinterfacerapport voor persoonlijke gegevens bevat geselecteerde gegevens. De download CSV voor het Geautomatiseerde rapport van Segmenten bevat extra details. De geautomatiseerde het rapportdownload van Segmenten omvat extra Geautomatiseerde Segmenten voorbij de hoogste segmenten inbegrepen in UI, samen met hoe die segmenten tegen uw aanbiedingen of ervaringen uitvoerden.

## Het rapport Geautomatiseerde segmenten interpreteren

De volgende lijst verklaart hoe te om het rapport te interpreteren en beschrijft zijn elementen:

| Element | Details |
|--- |--- |
| Linkerzijpaneel | Het linkerpaneel maakt een lijst van de 20 grootste &quot;geautomatiseerde segmenten&quot;die door de verpersoonlijkingsmodellen van Target voor deze activiteit worden geïdentificeerd. Een &quot;geautomatiseerd segment&quot;is als een publiek, maar het wordt bepaald door de verpersoonlijkingsmodellen van Target in plaats van door de telleraar. Elk geautomatiseerd segment bestaat uit specifieke waarden (of waardebereiken) van specifieke kenmerken.<br>Geautomatiseerde segmenten kunnen elkaar overlappen. Geautomatiseerde segmenten kunnen worden gedefinieerd door één, twee, drie of vier kenmerken. Zie de voorbeelden hieronder voor meer informatie.<br>Voor meer informatie over de personalisatiemodellen van Target raadpleegt u [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). Voor meer informatie over de attributen die de verpersoonlijkingsmodellen van het Doel gebruiken om de geautomatiseerde segmenten tot stand te brengen, zie [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md). |
| Grafiek centreren | De middelste grafieken tonen hoe de inhoud van uw activiteit voor het benadrukte geautomatiseerde segment wordt uitgevoerd. Als u op verschillende segmenten in het linkerdeelvenster klikt, worden de middelste grafieken bijgewerkt. |
| Cirkeldiagrammen | De schijfgrafieken bij de bovenkant van het centrumpaneel tonen de grootte van het geautomatiseerde segment, evenals het totale aantal gepersonaliseerde bezoeken in de activiteit (bijvoorbeeld, verkeer aan deze activiteit die door het verpersoonlijkingsmodel werd gediend. Het omvat geen controleverkeer of verkeer dat door het algemene windenermodel wordt gediend). De omvang van het segment is uitsluitend gebaseerd op individuele bezoeken.<br>![Cirkeldiagram](/help/main/c-reports/assets/pie.png) |
| Streepjesgrafiek met twee assen | Het staafdiagram met twee assen bevat informatie over bezoeken en conversie door de aanbieding of ervaring voor dat specifieke geautomatiseerde segment. |
| Roze balk | De roze balk vertegenwoordigt de conversiesnelheid en gebruikt de onderste as van de grafiek. U kunt de muisaanwijzer op de balk plaatsen voor meer informatie |
| Blauwe balk | De blauwe balk geeft het aantal bezoeken aan en gebruikt de bovenste as van de grafiek. U kunt de muisaanwijzer op de balk plaatsen voor meer informatie. |
| Grijze stippellijn | De grijze stippellijn geeft de conversiesnelheid weer voor alle persoonlijke bezoeken in de activiteit, voor alle aanbiedingen/ervaringen en geautomatiseerde segmenten. |

**Voorbeeld 1 van geautomatiseerd segment**

Dit geautomatiseerde segment wordt gedefinieerd op basis van slechts één kenmerk. Bezoekers die in dit geautomatiseerde segment zijn opgenomen, zagen deze AP-activiteit op een weekdag buiten de gebruikelijke werkuren of in een weekend.

![Voorbeeld 1 van geautomatiseerd segmentrapport](/help/main/c-reports/assets/automated_segment_example_1.png)

**Voorbeeld 2 van geautomatiseerd segment**

Dit geautomatiseerde segment wordt gedefinieerd op basis van twee kenmerken. Bezoekers die in dit geautomatiseerde segment waren opgenomen en die deze AP-activiteit zagen, hadden tijdens hun huidige bezoek minder dan drie pagina&#39;s en waren geografisch gevestigd in de Latitude 42.57 en 47.29 (ongeveer tussen New Hampshire/Oregon en Washington/Maine voor een in de VS gevestigd bedrijf).

![Voorbeeld 2 van geautomatiseerd segmentrapport](/help/main/c-reports/assets/automated_segment_example_2.png)

## Veelgestelde vragen over geautomatiseerde segmenten {#section_740910A52FA646B4AC9452F98C2F5719}

**Persoonlijke inzichten zijn nog niet beschikbaar voor mijn activiteiten. Waarom is dat?**

Er zijn verschillende redenen waarom de [!UICONTROL Personalization Insights] rapporten zijn nog niet beschikbaar voor je activiteiten:

* Er zijn geen 15 dagen verstreken sinds u de activiteit hebt geactiveerd. De geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen zullen niet tot minstens 15 dagen beschikbaar zijn nadat u uw activiteit hebt begonnen. Tijdens deze eerste periode kunt u deze rapporten niet openen of op de pictogrammen Geautomatiseerde segmenten en Belangrijke kenmerken klikken.
* Uw activiteit heeft niet voldoende verkeer tijdens het gespecificeerde tijdkader gehad. Na 15 dagen zijn overgegaan, veronderstellend is er voldoende gepersonaliseerd verkeer in uw activiteit om de verpersoonlijkingsmodellen te bouwen, zullen de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen beschikbaar zijn.
* Uw activiteit heeft een opbrengstoptimalisatiedoel. Momenteel [!UICONTROL Personalization Insights] is alleen beschikbaar voor optimalisatieactiviteiten voor conversie. Adobe voegt in een toekomstige release ondersteuning toe voor activiteiten die gericht zijn op het optimaliseren van de inkomsten.

**Wat is een kenmerk?**

Een attribuut is informatie over een bezoeker of zijn of haar specifiek bezoek dat door de verpersoonlijkingsalgoritmen wordt gebruikt om te leren hoe te om verkeer te personaliseren. Een kenmerk kan bijvoorbeeld het browsertype, de locatie, het tijdstip van het bezoek zijn, enzovoort.

Meer informatie over welke kenmerken [!DNL Target] gebruik in zijn verpersoonlijkingsmodellen, zie [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md). Voor meer informatie over hoe te om nieuwe attributen in Doel te uploaden om in de verpersoonlijkingsmodellen van Target te gebruiken, zie [Methoden om gegevens op te halen in doel](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/){target=_blank}.

**Wat is een geautomatiseerd segment?**

Een &quot;geautomatiseerd segment&quot;is als een publiek, maar het wordt bepaald door de verpersoonlijkingsmodellen van Target in plaats van door de telleraar.

Een geautomatiseerd segment bestaat uit specifieke waarden (of waardebereiken) van specifieke kenmerken. Zie Stap 5 hierboven, bijvoorbeeld geautomatiseerde segmenten. Segmenten kunnen elkaar overlappen.

Meer over het willekeurige bosverpersoonlijkingsalgoritme leren, dat de basis voor de verpersoonlijkingsmodellen van het Doel is, zie [Random Forest Algorithm](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**Wat bepaalt de orde van de geautomatiseerde segmenten?**

Voor elk segment wordt een score berekend op basis van de grootte van het segment en het verschil tussen de score en de inhoud in uw activiteit. De combinatie van deze input bepaalt de orde van de geautomatiseerde segmenten dusdanig dat de grotere segmenten met grotere verschillen in hoe zij op de verschillende inhoud antwoordden dichter aan de bovenkant van de segmentlijst zullen lijken.

**Waarom worden slechts enkele van mijn aanbiedingen/ervaringen weergegeven in het rapport Automated Segments?**

AP- en AT-activiteiten bouwen één model per aanbieding (in het geval van AP) en één model per ervaring (in het geval van AT). Deze activiteiten beginnen het gepersonaliseerde verkeer te dienen en uw tot stand te brengen [!UICONTROL Personalization Insights] met slechts twee modellen. Als je niet al je aanbiedingen en ervaringen ziet in [!UICONTROL Personalization Insights], is het waarschijnlijk dat u geen modellen hebt die voor die specifieke aanbiedingen/ervaringen worden gebouwd. Je kunt je activiteiten controleren [!UICONTROL Summary] rapporteer en controleer of er een klokpictogram staat naast die aanbieding / ervaring. Dit pictogram geeft aan dat er nog geen modellen zijn gebouwd voor die aanbieding/ervaring.

**Waarom ontvangen sommige aanbiedingen/ervaringen met een lagere omrekeningskoers een grotere hoeveelheid verkeer dan andere aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment?**

Er zijn verscheidene potentiële redenen waarom u meer bezoeken aan een laag-omzettingsaanbieding of ervaring binnen een geautomatiseerd segment zou kunnen zien, die omvatten:

* Een klein aantal meningen voor sommige of alle aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment.
* Ondermaatse activiteiten waarbij bepaalde aanbiedingen/ervaringen geen modellen hebben, of modellen die eerder zijn ontwikkeld voor sommige aanbiedingen/ervaringen dan andere.
* Gerichte regels voor een specifieke aanbieding die de bezoekers de grenzen van hun aanbiedingen/ervaringen beperken.

**Is de informatie in [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] hetzelfde als bij het downloaden van CSV?**

Nr, bevat het UI rapport uitgezochte informatie. De CSV-download bevat aanvullende gegevens. De geautomatiseerde het rapportdownload van de Inzichten van het Segment omvat extra Geautomatiseerde Segmenten voorbij de hoogste segmenten inbegrepen in UI, samen met hoe die segmenten tegen uw aanbiedingen of ervaringen uitvoerden. Het rapport Belangrijke kenmerken bevat de bovenste 100 bezoekerskenmerken en hun relatieve belang, terwijl de gebruikersinterface alleen de bovenste 10 bezoekerskenmerken bevat.

**Kan ik zien [!UICONTROL Personalization Insights] voor een aangepast datumbereik?**

Verslaglegging over persoonlijke inzichten (beide [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes]) is alleen beschikbaar voor vaste datumbereiken: 15 dagen, 30 dagen en 60 dagen. Deze vaste datumbereiken staan [!UICONTROL Personalization Insights] om een groot genoeg bereik aan gegevens te gebruiken om de kans te verkleinen dat u inzichten afleidt van een kortstondig patroon in uw activiteit. U kunt deze tijdsduur voor om het even welke einddatum selecteren (waar deze genoeg gegevens in de activiteit zijn om aan de duur te voldoen).

**Hoe wordt [!UICONTROL Personalization Insights] gemaakt?**

[!UICONTROL Personalization Insights] wordt gecreeerd gebruikend een Adobe octrooi-hangende techniek genoemd MAGIX (ModelAgnostic globally Interpretable Verklaringen). Meer informatie over MAGIX vindt u in het gepubliceerde document van het onderzoeksteam van Adobe op het tabblad [arXiv.org-website](https://arxiv.org/abs/1706.07160).

**Waarom zijn de totale gegevens van het bezoekersverkeer in [!UICONTROL Automated Segments] het rapport komt niet overeen met mijn rapport AP of AT Summary/Performance?**

De [!UICONTROL Personalization Insights] De rapporten bevatten alleen bezoekers die een stuk inhoud zagen dat door de personalisatiemodellen van Target werd geselecteerd (d.w.z. het houdt geen rekening met verkeer of verkeer dat door het algemene winnersmodel wordt gediend). Dit verkeerstype wordt genoemd &quot;gepersonaliseerd&quot;verkeer. Het summiere prestatiesrapport in AP/AT omvat controle tegenover &quot;gericht&quot;verkeer. Het gerichte verkeer omvat gepersonaliseerd verkeer, evenals verkeer dat gebruikend het algemene windenermodel en wat willekeurig bediende verkeer werd gediend dat werd gebruikt om verder te leren.

**Sluit de geautomatiseerde segmenten elkaar uit?**

Nee, er is sprake van overlapping tussen de geautomatiseerde segmenten.

**Is [!UICONTROL Personalization Insights] beschikbaar voor op opbrengst-gebaseerde modelleringsdoelstellingen/primair doel?**

Op dit moment [!UICONTROL Personalization Insights] is alleen beschikbaar voor optimalisatieactiviteiten voor conversie. Adobe voegt in een toekomstige release ondersteuning toe voor activiteiten die gericht zijn op het optimaliseren van de inkomsten.

**Wat zijn verschillende manieren waarop ik de informatie in de Inzichten van de Personalisatie kan gebruiken?**

* Nieuw doelpubliek ontdekken: Als u een bepaald geautomatiseerd segment ziet dat goed presteert, zou u kunnen overwegen om een publiek tot stand te brengen zodat kunt u dat segment in andere rapporten opnieuw gebruiken.
* Test uw hypothesen van welk type bezoekers reageren op welke van uw ervaringen.
* Afleiden inzicht in welke inhoud werkte voor wat soort bezoekers: Welke aanbiedingen waren verantwoordelijk voor het optillen van de bezoekers.
* Ondermaatse inhoud identificeren.
* Begrijp welke attributen het meest kritiek aan hoe het model leerde.
* Zie welke eigenschappen in de verpersoonlijkingsmodellen worden gebruikt en hoe belangrijk zij zijn.
* Identificeer kansen voor extra gegevenspunten u in Doel kunt overgaan om uw verpersoonlijking verder te informeren.

**Is er logica aan de orde die de attributen in een segmentkaart verschijnen?**

Nee, de volgorde van de kaarten is alleen gebaseerd op een bovenstaande rangorde. De volgorde van de kenmerken binnen een kaart is niet gebaseerd op logica.
