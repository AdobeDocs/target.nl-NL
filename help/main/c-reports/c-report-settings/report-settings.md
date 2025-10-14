---
keywords: Doel;rapporten;rapportinstellingen;voorinstelling;doel voorinstelling;metrisch;publiek;datumbereik;instellingen;download;tabelweergave;grafiekweergave;gemiddelde lift;lift gebonden;betrouwbaarheidsinterval;vertrouwen;locatie-bijdrage;lopende gemiddelde;telmethode
description: Leer hoe te om rapportmontages in Adobe Target, met inbegrip van metriek, publiek, datumwaaiers, en meer te vormen.
title: Hoe vorm ik de Montages van het Rapport?
feature: Reports
exl-id: 337579d1-c678-43b6-9e80-b5abe159c2d3
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '1778'
ht-degree: 0%

---

# Rapportinstellingen

Informatie die u helpt bij het instellen van de elementen die u wilt opnemen in uw rapport in [!DNL Adobe Target] . Rapportinstellingen kunnen voor later gebruik worden opgeslagen.

Een rapport weergeven:

1. Klik op **[!UICONTROL Activities]** en klik vervolgens op de gewenste activiteit in de lijst.
1. Klik op de tab **[!UICONTROL Reports]** .

   ![&#x200B; UI van het Rapport &#x200B;](/help/main/c-reports/c-report-settings/assets/report-ui-refresh.png)

## Doelvoorinstelling {#section_51F67341465045BEB4F1A2FB638A8EB1}

U kunt maximaal tien verschillende voorinstellingen van het rapport van een afzonderlijke activiteit opslaan nadat u het naar wens hebt geconfigureerd (metriek, datumbereiken, publiek, geavanceerde instellingen, enzovoort). Alle [!DNL Target] -gebruikers kunnen de verschillende voorinstellingen weergeven, bewerken en verwijderen, ongeacht wie deze heeft gemaakt.

U kunt het rapport van een individuele activiteit ook vormen zoals gewenst en dan die configuratie opslaan als uw gebrek/favoriete voorinstelling. Dit is de mening die toont wanneer u het rapport van die activiteit vooruitgaat.

### Een voorinstelling of standaardvoorinstelling maken

1. Configureer het activiteitenrapport naar wens.

   De beschikbare instellingen, zoals metriek, datumbereiken, publiek, geavanceerde instellingen, enzovoort, worden hieronder uitgelegd.

1. Naast **[!UICONTROL Target Preset]**, klik het **[!UICONTROL More Options]** ( ![&#x200B; Meer pictogram van Opties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)) pictogram > **[!UICONTROL Save as New]**.

   Het dialoogvenster [!UICONTROL Create Preset] wordt weergegeven.

   ![&#x200B; Nieuwe Vooraf ingestelde dialoogdoos &#x200B;](/help/main/c-reports/c-report-settings/assets/report_preset_dialog-new.png)

1. Controleer de informatie in de secties **[!UICONTROL Filters]** om ervoor te zorgen dat het rapport wordt gevormd zoals gewenst, dan specificeer **[!UICONTROL Preset Name]** (tot 50 karakters).
1. (Voorwaardelijk) Als u dit uw standaard/favoriete rapportmening wilt zijn, glijd **[!UICONTROL Set as default preset]** knevel aan On positie.
1. Klik op **[!UICONTROL Create]**.

### Een andere voorinstelling selecteren

Selecteer de gewenste voorinstelling in de vervolgkeuzelijst **[!UICONTROL Target Preset]** .

### Een voorinstelling bewerken

1. Selecteer de voorinstelling die u wilt bewerken.
1. Geef de configuratie van het rapport zoals gewenst uit (metriek, datumwaaiers, publiek, geavanceerde montages, etc.).

   Nadat u op [!UICONTROL Save] hebt geklikt nadat u de configuratie van het rapport hebt bewerkt, wordt een sterretje ( &#42; ) weergegeven achter de naam van de voorinstelling om aan te geven dat de voorinstelling is gewijzigd.

1. Klik **[!UICONTROL More Options]** ( ![&#x200B; Meer pictogram van Opties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)) pictogram > **[!UICONTROL Save as New]** om een nieuwe vooraf ingesteld tot stand te brengen.

### Een voorinstelling verwijderen

1. Selecteer de voorinstelling die u wilt verwijderen.
1. Klik **[!UICONTROL More Options]** ( ![&#x200B; Meer pictogram van Opties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)) pictogram > **[!UICONTROL Delete]**.

1. Klik nogmaals op **[!UICONTROL Delete]** om uw verwijdering te bevestigen (verwijderde voorinstellingen kunnen niet worden hersteld).

### Foutafhandeling voorinstelling

Waarschuwingen en berichten in rapporten geven aan of een voorinstelling ongeldig wordt. Met de waarschuwing of het bericht kunt u een ander publiek, metrische groep, hostgroep of ervaring kiezen om een geldige voorinstelling te maken.

In de volgende lijst worden enkele situaties beschreven die ertoe kunnen leiden dat een voorinstelling ongeldig wordt:

* Er is een rapportagepubliek verwijderd uit de activiteit, maar er wordt naar verwezen in de definitie van de voorinstelling.
* Er is een (of meer) metrische waarde verwijderd, maar er wordt naar verwezen in de definitie van de voorinstelling. U kunt bijvoorbeeld een of meer metriek verwijderen uit de activiteit en vervolgens nieuwe metriek toevoegen.
* Een (of meer) hostgroep (omgeving) bestaat niet, maar wordt vermeld in de definitie van de voorinstelling.
* Een (of meer) ervaring is verwijderd nadat de voorinstelling is gemaakt, maar er wordt naar verwezen in de definitie van de voorinstelling.
* Een voorinstelling is semantisch ongeldig omdat de vermelde entiteiten nog bestaan, maar zijn bijgewerkt op een manier die de definitie van de voorinstelling semantisch is gewijzigd. Stel dat u in eerste instantie een voorinstelling maakt met de naam &#39;Revenue on Chrome&#39;. U werkt later de activiteit bij om metrische omzettingen in plaats van Inkomsten te meten. Door deze update van de activiteitendefinitie wordt de definitie van de voorinstelling semantisch ongeldig.

## [!UICONTROL Report Metric] {#section_894ABD7148244806B7CE556EBBA2AD62}

Klik de **[!UICONTROL Report Metric]** drop-down lijst om een verschillend [&#x200B; metrisch succes &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) of veelvoudige metriek te selecteren om in de grafiek en de grafiek te tonen.

Door gebrek, wordt primaire metrisch bepaald in de opstelling van succesmetriek wanneer u de activiteit creeert. Als u de opstelling verandert en de activiteit opnieuw opslaat, wordt primaire metrisch voor het melden bijgewerkt.

Voor meer informatie over het selecteren van veelvoudige metriek aan mening in rapporten, zie [&#x200B; Veelvoudige Metriek van de Mening in een Rapport &#x200B;](/help/main/c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7).

## [!UICONTROL Audience] {#section_70926EB4618945D9AFF2B0564FF3717B}

Klik op de vervolgkeuzelijst **[!UICONTROL Audience]** om het weergegeven publiek voor het rapport te wijzigen.

Voor meer informatie, zie [&#x200B; Soorten publiek &#x200B;](/help/main/c-target/target.md#concept_A782F8481A5041EBA75103CB26376522).

## [!UICONTROL Preset Date Range]

Klik op de vervolgkeuzelijst **[!UICONTROL Preset Date Range]** om een keuze te maken uit vooraf ingestelde datumbereiken.

Selecteer nieuwe **[!UICONTROL Start]** en **[!UICONTROL End]** datums voor het rapport. U kunt ook de bereiken **[!UICONTROL Start of Activity]** en **[!UICONTROL Start of activity - End of Activity]** gebruiken.

Vooraf gedefinieerde datumbereiken zijn onder andere: Laatste 7 dagen, Laatste 15 dagen of Laatste 30 dagen. Deze vooraf gedefinieerde datumbereiken zijn rolbereiken. Als de begindatum kleiner is dan het aantal gekozen dagen, wordt in de kalender het bereik weergegeven vanaf de begindatum, maar rolt deze zodra de begindatum ouder wordt dan het aantal dagen dat wordt gekozen als de activiteitsperiode toeneemt.

Rapporten hebben de volgende datumbeperkingen:

* De begindatum van het verslag moet binnen de laatste twee jaar liggen.
* De groepsrapporten van de aanbieding zijn beperkt tot 99 dagen vanaf de huidige dag.
* Uurmeldingen zijn beperkt tot 15 dagen.

## Datumbereik {#section_A410A768403C4E01891F95CB357E63ED}

In het vak [!UICONTROL Date Range] wordt het huidige datumbereik van het rapport weergegeven. Klik het **[!UICONTROL Calendar]** ( ![&#x200B; pictogram van de Kalender &#x200B;](/help/main/assets/icons/Calendar.svg)) pictogram om een kalender te tonen die u de de datumwaaier van het rapport laat veranderen.

## Instellingen {#section_D99CE462107D45CABE0960F820E1E972}

Om rapportmontages te vormen:

1. Klik het **[!UICONTROL Report Settings]** ( ![&#x200B; pictogram van de Montages van het Rapport &#x200B;](/help/main/assets/icons/Setting.svg)), breng gewenste veranderingen (zoals hieronder verklaard) aan.
1. Klik op **[!UICONTROL Save]** als u klaar bent.

Afhankelijk van het geselecteerde type activiteit, variëren de opties:

### Telmethode

Selecteer de gewenste methode:

* Bezoekers
* Bezoeken
* Activiteitenindrukkingen

### Besturing

Selecteer de besturingservaring die u wilt gebruiken bij het berekenen en vergelijken van lift.

### Omgeving {#environment}

Selecteer de omgeving (hostgroep) die u voor het rapport wilt gebruiken. Voor meer informatie, zie [&#x200B; Gastheren &#x200B;](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

>[!NOTE]
>
>Als uw organisatie [&#x200B; Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=nl-NL){target=_blank} (AEP) gebruikt om metrieke gegevens naar [!DNL Target] te verzenden, zou het milieu in AEP DataStream het milieu in uw [!DNL Target] rapportmontages moeten aanpassen.

### Rapportgegevens opnieuw instellen

Klik op [!UICONTROL Reset Report Data]. Rapportgegevens opnieuw instellen om oude gegevens te verwijderen. Huidige bezoekers blijven in de activiteit.  Deze optie is alleen beschikbaar voor gebruikers met [!UICONTROL Approver] -machtigingen.

>[!IMPORTANT]
>
>Dit is een permanente actie en kan niet ongedaan worden gemaakt.

Extreme waarden uitsluiten

De schakeloptie [!UICONTROL Exclude Extreme Values] is alleen van toepassing op activiteiten met metrische typen Inkomsten en Betrokkenheid. Voor meer informatie, zie [&#x200B; Excluding Extreme Orders &#x200B;](/help/main/c-reports/c-report-settings/excluding-extreme-orders.md#task_2AE7743FFCDD466DAEEB720BE5F33DAA).

## Downloaden {#section_77E65C50BAAF4AB79242DB3A8778ADEF}

Klik het **[!UICONTROL Download]** ( ![&#x200B; pictogram van de Download &#x200B;](/help/main/assets/icons/Download.svg) ) pictogram om rapportgegevens in een [!DNL .csv] formaat voor het snel invoeren in Excel, Toegang, of andere programma&#39;s van de gegevensanalyse te downloaden.

Voor meer informatie, zie [&#x200B; het Downloaden Gegevens in een Csv- Dossier &#x200B;](/help/main/c-reports/c-report-settings/downloading-data-in-csv-file.md).

## Vernieuwen {#section_E203729F2F314DF3856D2EE67C60B370}

Klik **[!UICONTROL Refresh]** ( ![&#x200B; verfrissen pictogram &#x200B;](/help/main/assets/icons/Refresh.svg)) pictogram om de lijst en de grafiekmening van een rapport te verfrissen zonder de volledige pagina, zijn configuratie, of zijn datumwaaier te verfrissen.

## Meer opties {#section_AB1B5C695D7045A0A0AC0E2698D2E7DE}

Klik het **[!UICONTROL More Options]** pictogram ( ![&#x200B; Meer pictogram van Opties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)) om tot de [!UICONTROL Save as New] en [!UICONTROL Delete] opties toegang te hebben.

## Weergaveopties

U kunt het rapport in diverse formaten, afhankelijk van het activiteitstype bekijken. Selecteer de gewenste optie.

* **Mening van de Lijst**: Klik het **[!UICONTROL Table View]** ( ![&#x200B; pictogram van de Mening van de Lijst &#x200B;](/help/main/assets/icons/Table.svg)) pictogram om het rapport als lijst te bekijken.
* **de Mening van de Grafiek**: Klik **[!UICONTROL Graph View]** ( ![&#x200B; pictogram van de Mening van de Grafiek &#x200B;](/help/main/assets/icons/GraphTrend.svg)) om het rapport als grafiek te bekijken.
* **Geautomatiseerde Segmenten**: (Beschikbaar slechts voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten.) Klik ** [!UICONTROL Automated Segments] ( ![&#x200B; Geautomatiseerde het pictogram van Segmenten &#x200B;](/help/main/assets/icons/AutomatedSegment.svg)) pictogram om het [&#x200B; Geautomatiseerde segmentrapport &#x200B;](/help/main/c-reports/c-personalization-insights-reports/automated-segments-report.md) te bekijken.
* **Belangrijke Attributen**: (Beschikbaar slechts voor [!DNL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten.) Klik het **[!UICONTROL Important Attributes]** ( ![&#x200B; Belangrijke pictogram van Attributen &#x200B;](/help/main/assets/icons/ViewList.svg)) pictogram om het [&#x200B; Belangrijke rapport van Attributen &#x200B;](/help/main/c-reports/c-personalization-insights-reports/important-attributes-report.md) te bekijken.

## Gemiddelde optillen, Lift Bounds en het Interval van het Vertrouwen {#section_0D87615B1D3344B3858BA494EEBC16FB}

De rapporten omvatten verscheidene gegevenspunten en visualisatievertegenwoordiging die de liftgrenzen en het betrouwbaarheidsniveau verbonden aan uw activiteit begrijpen. Hierdoor kunt u nauwkeuriger bepalen wie de winnaar is.

Voor meer informatie, zie [&#x200B; Statistische berekeningen in tests A/Bn &#x200B;](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

Overweeg het volgende:

* Deze optie is alleen beschikbaar wanneer u rapporten bekijkt in [!UICONTROL Table View] .
* Deze eigenschap is niet beschikbaar voor activiteiten die [&#x200B; Analytics als rapporteringsbron (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) gebruiken.

## Locatiebijdrage {#section_5832F126AC114AE1ABFFF4D9B904393B}

Klik het [[!UICONTROL Location Contribution]](/help/main/c-reports/multivariate-test-reports/location-contribution-report.md) ( ![&#x200B; pictogram van de Bijdrage van de Plaats &#x200B;](/help/main/assets/icons/LocationContribution.svg) ) om het rapport te schakelen om bijdrage door plaats voor Multivariate de activiteiten van de Test (MVT) te tonen.

## Ervaringen {#section_3A450DE1FA7E43F0AAB73165EC3D1C34}

Deze optie is alleen beschikbaar wanneer u het rapport weergeeft in [!UICONTROL Graph View] .

Schakel ervaringen aan de linkerkant van het diagram in of uit om de bijbehorende ervaringen uit het diagram weer te geven of te verbergen.

## Doorlopende gemiddelde {#section_59066693158C4433B87D07402C2BC6CD}

Deze optie is alleen beschikbaar wanneer u het rapport weergeeft in [!UICONTROL Graph View] .

&quot;Doorlopend gemiddelde&quot; geeft de cumulatieve omrekening weer (van het begin van het rapportagevenster tot de datum die in de grafiek wordt weergegeven) gedeeld door de cumulatieve bezoekers.

Selecteer de gewenste grafiekweergave:

* Doorlopende gemiddelde
* Gemiddelde optillen uitvoeren
* Dagelijks
* Dagelijks optillen

De naam van deze vervolgkeuzelijst is afhankelijk van de geselecteerde weergave, maar het is een van de bovenstaande weergaven.

## Telmethode {#section_01B0ED5665C74AE1AE97259800190C3E}

Deze optie is alleen beschikbaar wanneer u het rapport weergeeft in [!UICONTROL Graph View] .

U kunt de telmethode voor grafieken kiezen in rapporten. Dit wordt niet ondersteund voor [!UICONTROL Automated Personalization] (AP)-activiteiten.

Als u de optie [!UICONTROL Counting Methodology] wilt openen en een rapport wilt weergeven in de grafiekmodus, klikt u op de vervolgkeuzelijst **[!UICONTROL My Primary Goal]** en selecteert u vervolgens de telmethode.

De methode voor tellen is dezelfde als de methode die u in het dialoogvenster [!UICONTROL Settings] hebt geselecteerd, zoals hierboven beschreven.

De grafiek wordt standaard in de modus [!UICONTROL Daily] getekend.

U kunt de modus wijzigen door te klikken op de vervolgkeuzelijst [!UICONTROL Daily] en vervolgens een cumulatieve optie te selecteren.

>[!NOTE]
>
>De naam van deze vervolgkeuzelijst is afhankelijk van de geselecteerde modus.

Er zijn vier modi voor [!UICONTROL Auto-Target] -activiteiten: [!UICONTROL Daily Control] , [!UICONTROL Daily Targeted] , [!UICONTROL Cumulative Control] en [!UICONTROL Cumulative Targeted] .

De standaardvolgorde waarin de grafiek wordt uitgezet is als volgt:

* **[!UICONTROL A/B Test] (met inbegrip van [!UICONTROL Auto-Allocate] en [!UICONTROL Automated Personalization])**: Orde van ervarings verwezenlijking, in dalende orde.
* **[!UICONTROL Experience Targeting] (XT)**: Orde van ervaringen in de activiteit.
* **[!UICONTROL Multivariate Test] (MVT)**: Alfabetisch door ervaringsnaam.
* **[!UICONTROL Recommendations]**: volgorde waarin u ervaringen hebt gemaakt, in aflopende volgorde.

Houd rekening met het volgende terwijl u met de opties voor [!UICONTROL Counting Methodology] werkt:

* Voor [[!UICONTROL Auto-Target] activiteiten &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md), is er geen optie om &quot;Bezoekers&quot;als tellingsmethodologie te selecteren. [!UICONTROL Auto-Target] is het enige type activiteit dat u niet kunt tekenen door bezoekers.
* Voor activiteiten die [&#x200B; Analytics als rapporteringsbron (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) gebruiken, kunt u Bezoeker, Bezoek, of Indrukking niet cumulatief plotten.

## Werken met grafieken met meer dan 16 ervaringen in de activiteit

Als een activiteit minder dan 16 ervaringen heeft, wordt elke ervaring uitgezet in een verschillende kleur in de grafiek.

Als een activiteit meer dan 16 ervaringen heeft, tonen de gekleurde lijnen voor de eerste 16 ervaringen in de grafiek. De resterende ervaringen worden grijs weergegeven in het deelvenster Ervaring aan de linkerkant en er worden geen overeenkomende plotlijnen weergegeven in de grafiek. De lijnen voor slechts 16 ervaringen kunnen op elk ogenblik worden getoond.

Als u de muis boven een van de grijze ervaringen houdt, wordt er tijdelijk een nieuwe grijze plotlijn weergegeven die overeenkomt met die ervaring. Als u de plotlijn van een grijswaardenervaring in een kleur wilt weergeven, deselecteert u een ervaring die in kleur wordt weergegeven door op de naam ervan te klikken en vervolgens de gewenste grijswaardenervaring te selecteren door op de naam ervan te klikken.

De grafiek toont de lijnen voor de eerste 16 ervaringen (sommige overlappen, zodat lijkt het dat er minder dan 16 lijnen zijn). De gekleurde stip in het deelvenster Ervaring aan de linkerkant naast elke ervaringsnaam geeft aan dat de plotlijn van de ervaring in de overeenkomstige kleur wordt weergegeven.

Als u omlaag schuift in het deelvenster Ervaring, ziet u dat de namen voor de 17e tot 26e ervaring grijs worden weergegeven, zoals in de volgende afbeelding wordt getoond:

Als u de muis boven een van de grijze ervaringen houdt, wordt er tijdelijk een nieuwe grijze plotlijn weergegeven die overeenkomt met die ervaring.

Stel dat u de plotlijn voor Ervaring R wilt tonen en u niet de lijn voor Ervaring P wilt zien. U kunt op P&#39;s naam beleven klikken om deze te deselecteren en vervolgens op R&#39;s naam beleven klikken om deze te selecteren, zoals hieronder wordt weergegeven:
