---
keywords: Doel;AP-rapporten;geautomatiseerde verpersoonlijkingsrapporten;automatisch doel;automatisch doel;automatisch doel-rapport;automatisch doel-rapport;automatisch doelrapport;verpersoonlijking;veelgestelde vragen;belangrijke kenmerken
description: Leer hoe u de [!UICONTROL Important Attributes] rapport dat de hoogste attributen toont die het verpersoonlijkingsmodel en hun relatieve belang beïnvloedden.
title: Wat is het Belangrijke Rapport van Attributen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: c1069ca7-e221-4865-a82e-6cff5b4c0055
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1758'
ht-degree: 0%

---

# Rapport Belangrijke kenmerken

Informatie over de [!UICONTROL Important Attributes] rapport, één van de twee gespecialiseerde rapporten beschikbaar aan gebruikers van [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u [!UICONTROL Personalization Insights] rapporten:
>
>* AP- en AT-activiteiten zijn beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Ze zijn niet inbegrepen bij [!DNL Target Standard] zonder [!DNL Target Premium] licentie.
>
>* [!UICONTROL Personalization Insights] rapporten zijn beschikbaar slechts voor AP en bij activiteiten die een doel van de omzetoptimalisering gebruiken. Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.
>
>* [!UICONTROL Personalization Insights] rapporten zijn alleen beschikbaar als de [!UICONTROL Primary Goal] is geselecteerd in het dialoogvenster [!UICONTROL Report Metric] vervolgkeuzelijst.
>
>* [!UICONTROL Personalization Insights] de rapporten worden gesteund in [standaardomgeving](/help/main/administrating-target/hosts.md) alleen.
>
>* [!UICONTROL Personalization Insights] rapporten worden alleen gegenereerd voor activiteiten in het [!UICONTROL Live] en ten minste 15 dagen in werking zijn gesteld en verkeer ontvangen.


In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden.

## Toegang krijgen tot [!UICONTROL Important Attributes] verslag {#section_8E8F997AAAF44A1B9EE06EB6FB652801}

1. Klikken **[!UICONTROL Activities]** en klik vervolgens op de gewenste knop [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteit uit de lijst.

   Als u vele activiteiten hebt, kunt u de lijst filtreren door opties van te selecteren [!UICONTROL Type], [!UICONTROL Status], [!UICONTROL Reporting Source], [!UICONTROL Experience Composer], [!UICONTROL Metrics Type], en [!UICONTROL Activity Source] vervolgkeuzelijsten.

1. Klik op **[!UICONTROL Reports]**.

   De [Automated Personalization-overzicht](/help/main/c-reports/personalization-reports/reports-ap.md) of [Overzicht autom. doel](/help/main/c-reports/personalization-reports/auto-target-summary-report.md) rapportvertoningen, die informatie over de prestaties van uw activiteiten verstrekken, die door het eerste het schermpictogram wordt vertegenwoordigd. De twee extra pictogrammen vertegenwoordigen de twee [!UICONTROL Personalization Insights] rapporten: [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes].

   ![Samenvattingsrapport voor Automated Personalization-activiteit](/help/main/c-reports/assets/summary-report-ap.png)

   Let op: [!UICONTROL Auto-Target] heeft een extra grafiekpictogram voor de grafische weergave van het dialoogvenster [!UICONTROL Summary] verslag.

   ![Samenvattingsrapport voor Auto-Target-activiteit](/help/main/c-reports/assets/personalization_insights.png)

   >[!IMPORTANT]
   >
   >De [!UICONTROL Important Attributes] -rapport is pas beschikbaar 15 dagen nadat je je activiteit hebt geactiveerd. Tijdens deze eerste periode hebt u geen toegang tot dit rapport of kunt u op de knop [!UICONTROL Important Attributes] pictogram. Als er 15 dagen zijn verstreken en er voldoende gepersonaliseerd verkeer in uw activiteit is, kan de [!UICONTROL Important Attributes] -rapport is beschikbaar.

1. Na 15 dagen vanaf het activeren van de activiteit klikt u op de knop **[!UICONTROL Important Attributes]** pictogram.

   ![Het pictogram Belangrijke kenmerken in een Adobe Target-rapport](/help/main/c-reports/assets/model_attribute_ranking.png)

1. Selecteer het gewenste datumbereik.

   In tegenstelling tot [!UICONTROL Summary] verslag (prestatierapportage), [!UICONTROL Personalization Insights], met inbegrip van [!UICONTROL Important Attributes], is alleen beschikbaar voor vaste datumbereiken: 15 dagen, 30 dagen en 60 dagen.

   Deze vaste datumbereiken staan [!UICONTROL Personalization Insights] om een groot genoeg bereik aan gegevens te gebruiken om de kans te verkleinen dat u inzichten afleidt van een kortstondig patroon in uw activiteit. De twee besluiten u voor uw datumwaaier kunt maken zijn de &quot;Datum van het Eind&quot;en &quot;Duur.&quot; U zult merken dat het &quot;Begin&quot;grijs uit is. De begindatum wordt automatisch gewijzigd op basis van uw selecties voor de einddatum en -duur.

   ![Kalender in een Adobe Target-rapport](/help/main/c-reports/assets/personalization_insights_calendar_1.png)

   U hebt toegang tot de beschikbare vaste datumbereiken via de [!UICONTROL Choose Duration] vervolgkeuzelijst.

   ![Kies Duur in een rapport](/help/main/c-reports/assets/personalization_insights_calendar_2.png)

1. Controleer de [!UICONTROL Important Attributes] rapportgegevens.

   ![Rapport Belangrijke kenmerken in Adobe Target](/help/main/c-reports/assets/model_attribute_ranking_report.png)

1. (Optioneel) [Het rapport downloaden in CSV-indeling](/help/main/c-reports/c-report-settings/report-settings.md#section_77E65C50BAAF4AB79242DB3A8778ADEF) voor analyse in Excel en andere hulpmiddelen.

   >[!NOTE]
   >
   >Het gebruikersinterfacerapport voor persoonlijke gegevens bevat geselecteerde gegevens. De CSV-download voor het rapport Belangrijke kenmerken bevat aanvullende gegevens. De belangrijke download van het Attributenrapport omvat de volledige lijst van top 100 attributen, terwijl het UI rapport top 10 slechts omvat. Als u naar een specifiek attribuut op het rapport zoekt maar het niet daar is, betekent dat niet dat het attribuut niet de activiteit beïnvloedde, het maakte enkel niet de lijst voor top 100 attributen.

## Het rapport Belangrijke kenmerken interpreteren

De volgende lijst verklaart hoe te om het rapport te interpreteren en beschrijft zijn elementen:

| Element | Details |
|--- |--- |
| Staafgrafiek | Met de gekleurde staafgrafiek boven aan het scherm kunt u deze relatieve belangrijkscores visualiseren en kunt u de punten toewijzen aan de kleur van de punt naast elk van de respectieve kenmerken in de tabel. U kunt de muisaanwijzer ook boven een specifieke kleur in het staafdiagram plaatsen om het kenmerk dat het vertegenwoordigt te zien.  De belangrijke scores over de top 100 attributen voegen aan 100% toe. Voor meer informatie over hoe te om meer attributen toe te voegen die de verpersoonlijkingsmodellen van het Doel kunnen gebruiken, zie [Gegevens uploaden voor de Persoonlijke Algoritmen van het Doel](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md). |
| Modelkenmerkdiagram | De rangschikking van modelkenmerken bevat de tien bovenste kenmerken die het belangrijkst waren voor de manier waarop het personalisatiemodel van Target besloot welke inhoud elke bezoeker moet worden weergegeven. De belangrijke score toont, met betrekking tot de hoogste 100 attributen, hoe belangrijk een specifiek attribuut aan de verpersoonlijkingsmodellen van Target in deze activiteit was. |

## Belangrijke veelgestelde vragen over kenmerken {#section_740910A52FA646B4AC9452F98C2F5719}

Raadpleeg de volgende veelgestelde vragen voor antwoorden op veelgestelde vragen over het gebruik van de [!UICONTROL Important Attributes] verslag.

### Persoonlijke inzichten zijn nog niet beschikbaar voor mijn activiteiten. Waarom is dat?

Er zijn verschillende redenen waarom de [!UICONTROL Personalization Insights] rapporten zijn mogelijk nog niet beschikbaar voor uw activiteiten:

* Er is geen 15 dagen verstreken sinds u de activiteit hebt geactiveerd. De geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen zullen niet tot minstens 15 dagen beschikbaar zijn nadat u uw activiteit hebt begonnen. Tijdens deze eerste periode kunt u deze rapporten niet openen of op de pictogrammen Geautomatiseerde segmenten en Belangrijke kenmerken klikken.
* Uw activiteit heeft niet voldoende verkeer tijdens het gespecificeerde tijdkader gehad. Na 15 dagen zijn verstreken, ervan uitgaande dat [voldoende gepersonaliseerd verkeer](/help/main/c-activities/auto-target/auto-target-to-optimize.md#section_BA4D83BE40F14A96BE7CBC7C7CF2A8FB) in uw activiteit om de verpersoonlijkingsmodellen te bouwen, zullen de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen beschikbaar zijn.
* Uw activiteit heeft een opbrengstoptimalisatiedoel. Op dit moment [!UICONTROL Personalization Insights] is alleen beschikbaar voor optimalisatieactiviteiten voor conversie. In een toekomstige release zullen we ondersteuning toevoegen voor activiteiten die gericht zijn op het optimaliseren van de inkomsten.

### Wat is een kenmerk?

Een attribuut is informatie over een bezoeker of zijn of haar specifiek bezoek dat door de verpersoonlijkingsalgoritmen wordt gebruikt om te leren hoe te om verkeer te personaliseren. Een kenmerk kan bijvoorbeeld het browsertype, de locatie, het tijdstip van het bezoek zijn, enzovoort.

Meer informatie over welke kenmerken [!DNL Target] gebruik in zijn verpersoonlijkingsmodellen, zie [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md). Voor meer informatie over hoe te om nieuwe attributen in Doel te uploaden om in de verpersoonlijkingsmodellen van Target te gebruiken, zie [Methoden om gegevens op te halen in doel](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}.

### Ik zie een of meer kenmerken die ik niet wil gebruiken voor training. Kan ik deze kenmerken verwijderen uit het trainingsmodel? {#models-api}

De [!UICONTROL Models API], ook wel de Lijst van gewezen personen-API genoemd, stelt gebruikers in staat de lijst met kenmerken (ook wel functies genoemd) die worden gebruikt in modellen voor machinaal leren, weer te geven en te beheren voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten. Als u een of meer kenmerken wilt uitsluiten van gebruik door de modellen voor AP- of AT-activiteiten, kunt u de Modellen API gebruiken om die kenmerken toe te voegen aan de &quot;lijst van gewezen personen&quot;.

Zie voor meer informatie [Modellen-API-overzicht](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api.html){target=_blank} in the *Adobe Target Developer Guide*. To use the API to block attributes, see [Models API](https://experienceleague.adobe.com/docs/target-dev/developer/api/models-api/models-api-overview.html){target=_blank}.

### Is de informatie in [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] hetzelfde als bij het downloaden van CSV?

Nr, bevat het UI rapport uitgezochte informatie. De CSV-download bevat aanvullende gegevens. De geautomatiseerde het rapportdownload van de Inzichten van het Segment omvat extra Geautomatiseerde Segmenten voorbij de hoogste segmenten inbegrepen in UI, samen met hoe die segmenten tegen uw aanbiedingen of ervaringen uitvoerden. Het rapport Belangrijke kenmerken bevat de bovenste 100 bezoekerskenmerken en hun relatieve belang, terwijl de gebruikersinterface alleen de bovenste 10 bezoekerskenmerken bevat.

### Kan ik inzichten van de Personalisatie voor een waaier van de douanedatum zien?

Verslaglegging over persoonlijke inzichten (beide [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes]) is alleen beschikbaar voor vaste datumbereiken: 15 dagen, 30 dagen, 45 dagen, 60 dagen en 90 dagen. Deze vaste datumbereiken staan [!UICONTROL Personalization Insights] om een groot genoeg bereik aan gegevens te gebruiken om de kans te verkleinen dat u inzichten afleidt van een kortstondig patroon in uw activiteit. U kunt deze tijdsduur voor om het even welke einddatum selecteren (waar deze genoeg gegevens in de activiteit zijn om aan de duur te voldoen).

### Hoe wordt [!UICONTROL Personalization Insights] gemaakt?

[!UICONTROL Personalization Insights] wordt gecreeerd gebruikend een Adobe octrooi-hangende techniek genoemd MAGIX (ModelAgnostic globally Interpretable Verklaringen). Meer informatie over MAGIX vindt u in het gepubliceerde document van het onderzoeksteam van Adobe op het tabblad [arXiv.org-website](https://arxiv.org/abs/1706.07160).

### zijn [!UICONTROL Personalization Insights] beschikbaar voor op opbrengst-gebaseerde modelleringsdoelstellingen/primair doel?

Op dit moment [!UICONTROL Personalization Insights] is alleen beschikbaar voor optimalisatieactiviteiten voor conversie. In een toekomstige release zullen we ondersteuning toevoegen voor activiteiten die gericht zijn op het optimaliseren van de inkomsten.

### Wat is de score van het attributenbelang in het Belangrijke rapport van Attributen?

De belangrijke score in het gedeelte &quot;Belangrijkste eigenschappen van kenmerk&quot; van het rapport geeft input in welke variabelen het algoritme dat werd gebruikt om te leren het belangrijkst was toen het bepaalde hoe te om alle bezoekers in de segmenten te verdelen het identificeerde. Er wordt een percentagescore toegewezen aan de bovenste 100 kenmerken die door het model worden gebruikt.

### Waarom ontvangen sommige aanbiedingen/ervaringen met een lagere omrekeningskoers een grotere hoeveelheid verkeer dan andere aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment?

Er zijn verscheidene potentiële redenen waarom u meer bezoeken aan een laag-omzetaanbod/ervaring binnen een geautomatiseerd segment zou kunnen zien, die omvatten:

* Een klein aantal meningen voor sommige of alle aanbiedingen/ervaringen voor een bepaald geautomatiseerd segment.
* Ondermaatse activiteiten waarbij bepaalde aanbiedingen of ervaringen geen modellen hebben.
* Minder volume-activiteiten waarin modellen eerder werden gebouwd voor sommige aanbiedingen/ervaringen dan andere. Stel dat op dag 22 een aanvullend model is gemaakt en u kijkt naar gegevens van dag 10-24.
* Gerichte regels voor een specifieke aanbieding die de bezoekers kunnen zien welke aanbiedingen/ervaringen er zijn.
* Er zijn geen betrouwbaarheidsintervallen in de rapportage van inzichten. Nochtans, als de omrekeningskoersen dicht genoeg zijn, zou het model verkeer kunnen dienen zodat het in de punthoeveelheid hoger is, maar zij zijn niet &quot;statistisch verschillend&quot;aantallen.

Het kan nuttig zijn te weten hoe het model werkt dat verkeer dient. Elke persoon wordt gediend op basis van zijn of haar totale profiel. In de rapporten van Insights wordt dit gedrag echter veralgemeend, zodat het beter door een mens kan worden geïnterpreteerd. Dientengevolge, sluiten de segmenten elkaar niet uit. Dit kan ertoe leiden dat afzonderlijke segmenten dit type gedrag weergeven omdat dezelfde persoon in meerdere segmenten kan worden weergegeven.

### Wat zijn verschillende manieren waarop ik de informatie in de Inzichten van de Personalisatie kan gebruiken?

* Nieuw doelpubliek ontdekken: Als u een bepaald geautomatiseerd segment ziet dat bijzonder goed presteert, zou u kunnen overwegen om een publiek tot stand te brengen zodat kunt u dat segment in andere rapporten opnieuw gebruiken.
* Test uw hypothesen van welk type bezoekers zullen antwoorden op welke van uw ervaringen.
* Afleiden inzicht in welke inhoud werkte voor wat soort bezoekers: Welke aanbiedingen waren verantwoordelijk voor het optillen van de bezoekers.
* Ondermaatse inhoud identificeren.
* Begrijp welke attributen het meest kritiek aan hoe het model leerde.
* Zie welke eigenschappen in de verpersoonlijkingsmodellen worden gebruikt en hoe belangrijk zij zijn.
* Identificeer kansen voor extra gegevenspunten u in Doel kunt overgaan om uw verpersoonlijking verder te informeren.

## Bekende problemen

De volgende kwestie wordt momenteel onderzocht door de [!DNL Target] technisch team.

* [!DNL Adobe Experience Platform] segmentnamen worden niet weergegeven in het dialoogvenster [!UICONTROL Important Attributes] verslag voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten. (TOP-3813)
