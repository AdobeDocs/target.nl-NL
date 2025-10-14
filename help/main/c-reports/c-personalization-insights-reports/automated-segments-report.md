---
keywords: Doel;AP-rapporten;geautomatiseerde verpersoonlijkingsrapporten;automatisch doel;automatisch doel;automatisch doel;automatisch doelrapport;automatisch doelrapport;verpersoonlijking;inzichten;geautomatiseerde segmenten;vk;vaak gestelde vragen
description: Leer hoe de verschillende segmenten die door Adobe  [!DNL Target]  worden bepaald verpersoonlijkingsmodellen aan aanbiedingen/ervaringen in de activiteit antwoorden door het Geautomatiseerde rapport van Segmenten te bekijken.
title: Wat is het Geautomatiseerde Rapport van Segmenten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Reports
exl-id: d21517b7-770b-4618-9899-7ac4948c2a8b
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '2066'
ht-degree: 0%

---

# [!UICONTROL Automated Segments] -rapport

Informatie over het [!UICONTROL Automated Segments] -rapport, een van de twee gespecialiseerde rapporten die beschikbaar zijn voor gebruikers van [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] (AT)-activiteiten.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u [!UICONTROL Personalization Insights] -rapporten gebruikt:
>
>* AP- en AT-activiteiten zijn beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. Ze worden niet zonder [!DNL Target Standard] -licentie opgenomen in [!DNL Target Premium] .
>
>* [!UICONTROL Personalization Insights] -rapporten zijn alleen beschikbaar voor AP- en AT-activiteiten die een doel voor conversie-optimalisatie gebruiken. Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.
>
>* [!UICONTROL Personalization Insights] -rapporten zijn alleen beschikbaar als [!UICONTROL Primary Goal] is geselecteerd in de vervolgkeuzelijst [!UICONTROL Report Metric] .
>
>* [!UICONTROL Personalization Insights] de rapporten worden gesteund in het [&#x200B; standaardmilieu &#x200B;](/help/main/administrating-target/hosts.md) slechts.
>
>* [!UICONTROL Personalization Insights] -rapporten worden alleen gegenereerd voor activiteiten die de status [!UICONTROL Live] hebben en die gedurende ten minste 15 dagen zijn geactiveerd en verzonden.

Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd.

## Heb toegang tot het Geautomatiseerde rapport van Segmenten {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klik **[!UICONTROL Activities]**, dan klik de gewenste [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) of [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteit van de lijst.

   Als u vele activiteiten hebt, klik het pictogram van de Filter ( ![&#x200B; pictogram van de Filter &#x200B;](/help/main/assets/icons/Filter.svg)) om de lijst te filtreren door opties van [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] drop-down lijsten te selecteren.

1. Klik op **[!UICONTROL Reports]**.

   Het [&#x200B; Samenvatting van Automated Personalization &#x200B;](/help/main/c-reports/personalization-reports/reports-ap.md) of [&#x200B; auto-Doel Summiere &#x200B;](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) rapportvertoningen, die informatie over de prestaties van uw activiteiten verstrekt, die door het eerste het schermpictogram worden vertegenwoordigd. De twee extra pictogrammen vertegenwoordigen de twee [!UICONTROL Personalization Insights] rapporten: **[!UICONTROL Automated Segments]** ( ![&#x200B; Geautomatiseerde het rapport van Segmenten &#x200B;](/help/main/assets/icons/AutomatedSegment.svg)) en **[!UICONTROL Important Attributes]** ( ![&#x200B; Belangrijk pictogram van Attributen &#x200B;](/help/main/assets/icons/ViewList.svg)). Auto-Target heeft een extra grafiekpictogram voor de grafische mening van het [!UICONTROL Summary] rapport.

   >[!IMPORTANT]
   >
   >Het [!UICONTROL Automated Segments] -rapport is pas beschikbaar 15 dagen nadat u uw activiteit hebt geactiveerd. Tijdens deze eerste periode hebt u geen toegang tot dit rapport of kunt u op het pictogram [!UICONTROL Automated Segments] klikken. Nadat er 15 dagen zijn verstreken, is het [!UICONTROL Automated Segments] -rapport beschikbaar, ervan uitgaande dat er voldoende gepersonaliseerd verkeer in uw activiteit is.

1. Na 15 dagen vanaf het activeren van de activiteit kunt u op het pictogram **[!UICONTROL Automated Segments]** klikken.

1. Selecteer het gewenste datumbereik.

   In tegenstelling tot het [!UICONTROL Summary] -rapport (prestatierapportage) is [!UICONTROL Personalization Insights] , inclusief [!UICONTROL Automated Segments] , alleen beschikbaar voor vaste datumbereiken: 15 dagen, 30 dagen en 60 dagen. Met deze vaste datumbereiken kan [!UICONTROL Personalization Insights] een groot genoeg gegevensbereik gebruiken om de kans te verkleinen dat u inzichten afleidt van een kortstondig patroon in uw activiteit. De twee besluiten u voor uw datumwaaier kunt maken zijn de &quot;Datum van het Eind&quot;en &quot;Duur.&quot; U zult merken dat het &quot;Begin&quot;grijs uit is. De begindatum wordt automatisch gewijzigd op basis van uw selecties voor de einddatum en -duur.

   U hebt toegang tot de beschikbare vaste datumbereiken via de vervolgkeuzelijst [!UICONTROL Preset Date Range] .

1. Controleer de rapportgegevens van [!UICONTROL Automated Segments] .

1. (Facultatief) klik **[!UICONTROL Download]** ( ![&#x200B; pictogram van de Download &#x200B;](/help/main/assets/icons/Download.svg) ) pictogram aan [&#x200B; download het rapport in formaat CSV &#x200B;](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) voor analyse in Excel en andere hulpmiddelen.

   >[!NOTE]
   >
   >Het gebruikersinterfacerapport van Personalization Insights bevat geselecteerde gegevens. De download CSV voor het Geautomatiseerde rapport van Segmenten bevat extra details. De geautomatiseerde het rapportdownload van Segmenten omvat extra Geautomatiseerde Segmenten voorbij de hoogste segmenten inbegrepen in UI, samen met hoe die segmenten tegen uw aanbiedingen of ervaringen uitvoerden.

## Het rapport Geautomatiseerde segmenten interpreteren

De volgende lijst verklaart hoe te om het rapport te interpreteren en beschrijft zijn elementen:

| Element | Details |
|--- |--- |
| Linkerzijpaneel | Het linkerpaneel maakt een lijst van de 20 grootste &quot;geautomatiseerde segmenten&quot;die door de verpersoonlijkingsmodellen van Target voor deze activiteit worden geïdentificeerd. Een &quot;geautomatiseerd segment&quot;is als een publiek, maar het wordt bepaald door de verpersoonlijkingsmodellen van Target in plaats van door de telleraar. Elk geautomatiseerd segment bestaat uit specifieke waarden (of waardebereiken) van specifieke kenmerken.<br> de geautomatiseerde segmenten kunnen overlappen. Geautomatiseerde segmenten kunnen worden gedefinieerd door één, twee, drie of vier kenmerken. Zie de voorbeelden hieronder voor meer informatie.<br> om meer over de verpersoonlijkingsmodellen van het Doel te leren, zie [&#x200B; Willekeurig Bosalgoritme &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md). Meer over de verpersoonlijkingsmodellen van het attribuutDoel gebruiken om de geautomatiseerde segmenten tot stand te brengen, zie {de Inzameling van 0} Gegevens voor de Algoritmen van Personalization van het Doel [.](/help/main/c-activities/t-automated-personalization/ap-data.md) |
| Grafiek midden | De middelste grafieken tonen hoe de inhoud van uw activiteit voor het benadrukte geautomatiseerde segment wordt uitgevoerd. Als u op verschillende segmenten in het linkerdeelvenster klikt, worden de middelste grafieken bijgewerkt. |
| Cirkeldiagrammen | De schijfgrafieken bij de bovenkant van het centrumpaneel tonen de grootte van het geautomatiseerde segment, evenals het totale aantal gepersonaliseerde bezoeken in de activiteit (bijvoorbeeld, verkeer aan deze activiteit die door het verpersoonlijkingsmodel werd gediend. Het omvat geen controleverkeer of verkeer dat door het algemene windenermodel wordt gediend). De omvang van het segment is uitsluitend gebaseerd op individuele bezoeken.<br>![&#x200B; Schijfgrafiek &#x200B;](/help/main/c-reports/assets/pie.png) |
| Streepjesgrafiek met twee assen | Het staafdiagram met twee assen bevat informatie over bezoeken en conversie door de aanbieding of ervaring voor dat specifieke geautomatiseerde segment. |
| Roze balk | De roze balk vertegenwoordigt de conversiesnelheid en gebruikt de onderste as van de grafiek. U kunt de muisaanwijzer op de balk plaatsen voor meer informatie |
| Blauwe balk | De blauwe balk geeft het aantal bezoeken aan en gebruikt de bovenste as van de grafiek. U kunt de muisaanwijzer op de balk plaatsen voor meer informatie. |
| Grijze stippellijn | De grijze stippellijn geeft de conversiesnelheid weer voor alle persoonlijke bezoeken in de activiteit, voor alle aanbiedingen/ervaringen en geautomatiseerde segmenten. |

**Geautomatiseerd Voorbeeld van het Segment 1**

Dit geautomatiseerde segment wordt gedefinieerd op basis van slechts één kenmerk. Bezoekers die in dit geautomatiseerde segment zijn opgenomen, zagen deze AP-activiteit op een weekdag buiten de gebruikelijke werkuren of in een weekend.

![&#x200B; Geautomatiseerde het rapportvoorbeeld van Segmenten 1 &#x200B;](/help/main/c-reports/assets/automated_segment_example_1.png)

**Geautomatiseerd Voorbeeld 2 van het Segment**

Dit geautomatiseerde segment wordt gedefinieerd op basis van twee kenmerken. Bezoekers die in dit geautomatiseerde segment waren opgenomen en die deze AP-activiteit zagen, hadden tijdens hun huidige bezoek minder dan drie pagina&#39;s en waren geografisch gevestigd in de Latitude 42.57 en 47.29 (ongeveer tussen New Hampshire/Oregon en Washington/Maine voor een in de VS gevestigd bedrijf).

![&#x200B; Geautomatiseerde het rapportvoorbeeld van Segmenten 2 &#x200B;](/help/main/c-reports/assets/automated_segment_example_2.png)

## Veelgestelde vragen over geautomatiseerde segmenten {#section_740910A52FA646B4AC9452F98C2F5719}

**de rapporten van de Inzichten van Personalization zijn nog niet beschikbaar voor mijn activiteit. Waarom is dat?**

Er zijn verschillende redenen waarom de [!UICONTROL Personalization Insights] -rapporten nog niet beschikbaar zijn voor uw activiteiten:

* Er zijn geen 15 dagen verstreken sinds u de activiteit hebt geactiveerd. De geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen zullen niet tot minstens 15 dagen beschikbaar zijn nadat u uw activiteit hebt begonnen. Tijdens deze eerste periode kunt u deze rapporten niet openen of op de pictogrammen Geautomatiseerde segmenten en Belangrijke kenmerken klikken.
* Uw activiteit heeft niet voldoende verkeer tijdens het gespecificeerde tijdkader gehad. Na 15 dagen zijn overgegaan, veronderstellend is er voldoende gepersonaliseerd verkeer in uw activiteit om de verpersoonlijkingsmodellen te bouwen, zullen de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen beschikbaar zijn.
* Uw activiteit heeft een opbrengstoptimalisatiedoel. [!UICONTROL Personalization Insights] is momenteel alleen beschikbaar voor doelactiviteiten voor conversie. Adobe voegt in een toekomstige release ondersteuning toe voor activiteiten die gericht zijn op het optimaliseren van inkomsten.

**wat is een attribuut?**

Een attribuut is informatie over een bezoeker of zijn of haar specifiek bezoek dat door de verpersoonlijkingsalgoritmen wordt gebruikt om te leren hoe te om verkeer te personaliseren. Een kenmerk kan bijvoorbeeld het browsertype, de locatie, het tijdstip van het bezoek zijn, enzovoort.

Voor meer informatie over welke attributen [!DNL Target] gebruikt in zijn verpersoonlijkingsmodellen, zie [&#x200B; Inzameling van Gegevens voor de Algoritmen van Personalization van het Doel &#x200B;](/help/main/c-activities/t-automated-personalization/ap-data.md). Voor meer informatie over hoe te om nieuwe attributen in Doel te uploaden om in de verpersoonlijkingsmodellen van het Doel te gebruiken, zie [&#x200B; Methoden om Gegevens in Doel &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=nl-NL){target=_blank} te krijgen.

**wat is een geautomatiseerd segment?**

Een &quot;geautomatiseerd segment&quot;is als een publiek, maar het wordt bepaald door de verpersoonlijkingsmodellen van Target in plaats van door de telleraar.

Een geautomatiseerd segment bestaat uit specifieke waarden (of waardebereiken) van specifieke kenmerken. Zie Stap 5 hierboven, bijvoorbeeld geautomatiseerde segmenten. Segmenten kunnen elkaar overlappen.

Meer over het willekeurige bosverpersoonlijkingsalgoritme leren, dat de basis voor de verpersoonlijkingsmodellen van het Doel is, zie [&#x200B; Willekeurig Bosalgoritme &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md).

**wat beslist de orde van de geautomatiseerde segmenten?**

Voor elk segment wordt een score berekend op basis van de grootte van het segment en het verschil tussen de score en de inhoud in uw activiteit. De combinatie van deze input bepaalt de orde van de geautomatiseerde segmenten dusdanig dat de grotere segmenten met grotere verschillen in hoe zij op de verschillende inhoud antwoordden dichter aan de bovenkant van de segmentlijst zullen lijken.

**waarom zijn slechts enkele van mijn aanbiedingen/ervaringen die in het Geautomatiseerde rapport van Segmenten verschijnen?**

AP- en AT-activiteiten bouwen één model per aanbieding (in het geval van AP) en één model per ervaring (in het geval van AT). Deze activiteiten beginnen gepersonaliseerd verkeer te dienen en uw [!UICONTROL Personalization Insights] te creëren met slechts twee gebouwde modellen. Als u niet al uw aanbiedingen/ervaringen in [!UICONTROL Personalization Insights] ziet, is het waarschijnlijk dat u geen modellen hebt die voor die specifieke aanbiedingen/ervaringen zijn gebouwd. U kunt het rapport [!UICONTROL Summary] van uw activiteit controleren en zien of is er een klokpictogram naast die aanbieding/ervaring. Dit pictogram geeft aan dat er nog geen modellen zijn gebouwd voor die aanbieding/ervaring.

**waarom zijn sommige aanbiedingen/ervaringen met een lagere omzettingspercentage die een grotere hoeveelheid verkeer in vergelijking met andere aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment ontvangen?**

Er zijn verscheidene potentiële redenen waarom u meer bezoeken aan een laag-omzettingsaanbieding of ervaring binnen een geautomatiseerd segment zou kunnen zien, die omvatten:

* Een klein aantal meningen voor sommige of alle aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment.
* Ondermaatse activiteiten waarbij bepaalde aanbiedingen/ervaringen geen modellen hebben, of modellen die eerder zijn ontwikkeld voor sommige aanbiedingen/ervaringen dan andere.
* Gerichte regels voor een specifieke aanbieding die de bezoekers de grenzen van hun aanbiedingen/ervaringen beperken.

**is de informatie in [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] het zelfde als in de download CSV?**

Nr, bevat het UI rapport uitgezochte informatie. De CSV-download bevat aanvullende gegevens. De geautomatiseerde het rapportdownload van de Inzichten van het Segment omvat extra Geautomatiseerde Segmenten voorbij de hoogste segmenten inbegrepen in UI, samen met hoe die segmenten tegen uw aanbiedingen of ervaringen uitvoerden. Het rapport Belangrijke kenmerken bevat de bovenste 100 bezoekerskenmerken en hun relatieve belang, terwijl de gebruikersinterface alleen de bovenste 10 bezoekerskenmerken bevat.

**kan ik [!UICONTROL Personalization Insights] voor een waaier van de douanedatum zien?**

Personalization Insights-rapportage (zowel [!UICONTROL Automated Segments] als [!UICONTROL Important Attributes] ) is alleen beschikbaar voor vaste datumbereiken: 15 dagen, 30 dagen en 60 dagen. Met deze vaste datumbereiken kan [!UICONTROL Personalization Insights] een groot genoeg gegevensbereik gebruiken om de kans te verkleinen dat u inzichten afleidt van een kortstondig patroon in uw activiteit. U kunt deze tijdsduur voor om het even welke einddatum selecteren (waar deze genoeg gegevens in de activiteit zijn om aan de duur te voldoen).

**hoe wordt [!UICONTROL Personalization Insights] gecreeerd?**

[!UICONTROL Personalization Insights] wordt gemaakt met behulp van een Adobe-techniek waarvoor een patent is aangevraagd, MAGIX (Model Agnostic Global Interpretable Explanations). U kunt meer over MAGIX in het gepubliceerde document van het onderzoeksteam van Adobe op de [&#x200B; arXiv.org &#x200B;](https://arxiv.org/abs/1706.07160) leren.

**waarom past de totale gegevens van het bezoekersverkeer in het [!UICONTROL Automated Segments] rapport niet mijn AP of bij Samenvatting/Prestaties rapport aan?**

De [!UICONTROL Personalization Insights] -rapporten bevatten alleen bezoekers die een stuk inhoud hebben gezien dat door de personalisatiemodellen van Target is geselecteerd (dat wil zeggen dat er geen rekening wordt gehouden met verkeer of verkeer dat door het algemene winnersmodel wordt bediend). Dit verkeerstype wordt genoemd &quot;gepersonaliseerd&quot;verkeer. Het summiere prestatiesrapport in AP/AT omvat controle tegenover &quot;gericht&quot;verkeer. Het gerichte verkeer omvat gepersonaliseerd verkeer, evenals verkeer dat gebruikend het algemene windenermodel en wat willekeurig bediende verkeer werd gediend dat werd gebruikt om verder te leren.

**zijn de geautomatiseerde segmenten wederzijds exclusief?**

Nee, er is overlapping tussen de geautomatiseerde segmenten.

**is [!UICONTROL Personalization Insights] beschikbaar voor op opbrengst-gebaseerde modelleringsdoelstellingen/primair doel?**

Op dit moment is [!UICONTROL Personalization Insights] alleen beschikbaar voor doelactiviteiten voor het optimaliseren van conversies. Adobe voegt in een toekomstige release ondersteuning toe voor activiteiten die gericht zijn op het optimaliseren van inkomsten.

**wat zijn verschillende manieren ik hefboomwerking de informatie in de Inzichten van Personalization kan?**

* Nieuw publiek ontdekken om te richten: Als u een bepaald geautomatiseerd segment ziet dat goed presteert, zou u kunnen overwegen om een publiek tot stand te brengen zodat kunt u dat segment in andere rapporten opnieuw gebruiken.
* Test uw hypothesen van welk type bezoekers reageren op welke van uw ervaringen.
* Afleiden insight naar de inhoud die werkte voor wat voor soort bezoekers: welke aanbiedingen waren verantwoordelijk voor het optillen van de bezoekers.
* Ondermaatse inhoud identificeren.
* Begrijp welke attributen het meest kritiek aan hoe het model leerde.
* Zie welke eigenschappen in de verpersoonlijkingsmodellen worden gebruikt en hoe belangrijk zij zijn.
* Identificeer kansen voor extra gegevenspunten u in Doel kunt overgaan om uw verpersoonlijking verder te informeren.

**is er om het even welke logica aan de orde die de attributen in een segmentkaart verschijnen?**

Neen, de volgorde van de kaarten is alleen gebaseerd op een hierboven beschreven rangorde. De volgorde van de kenmerken binnen een kaart is niet gebaseerd op logica.
