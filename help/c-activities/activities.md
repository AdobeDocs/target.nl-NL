---
keywords: activities list;activities;activity;activity types;edit activity;activity actions;activity attribute;activity list filter;activity limitations;personalize;personalization
description: Met de activiteiten in Adobe Target kunt u inhoud aanpassen aan specifieke doelgroepen en pagina-ontwerpen testen
title: Met de activiteiten in Adobe Target kunt u inhoud aanpassen aan specifieke doelgroepen en pagina-ontwerpen testen.
feature: activities
topic: Standard
uuid: 89dca5b4-c23d-4dfa-8f13-f1b05c7ab22c
translation-type: tm+mt
source-git-commit: e18f18e6d6e0b8fc6eb5ada845e2fe5377d6c5d0
workflow-type: tm+mt
source-wordcount: '2069'
ht-degree: 1%

---


# Activiteiten{#activities}

Met de activiteiten in Adobe Target kunt u inhoud aanpassen aan specifieke doelgroepen en pagina-ontwerpen testen.

U kunt bijvoorbeeld een activiteit ontwerpen die twee verschillende landingspagina&#39;s test, een die informatie over dameszomerschoenen markeert, en een andere landingspagina die meer algemene zomerkleding markeert. De activiteit bepaalt de voorwaarden die controleren wanneer elk van deze landingspagina&#39;s verschijnt, en de metriek die bepalen welke pagina succesvoller is. De activiteit wordt gevormd om te beginnen en te beëindigen wanneer specifieke voorwaarden, zoals tussen specifieke data worden voldaan, of om te beginnen wanneer de activiteit wordt goedgekeurd en te beëindigen wanneer het wordt gedeactiveerd.

Wanneer het ontwerpen van een activiteit, zou u zorgvuldig moeten plannen. Bepaal wanneer de activiteit zal beginnen en hoe lang het zal duren. Geef vervolgens een lijst met uw aanbiedingen en wijs een doelgroep toe aan elk aanbod.

## Typen activiteiten

Doel bevat verschillende typen activiteit. In de volgende tabel vindt u een overzicht van elk type activiteit met koppelingen voor meer informatie. Om u te helpen het beste type activiteit voor uw doeleinden te kiezen, hebben wij ook de Gids [van de Activiteiten van de](/help/c-activities/target-activities-guide.md)Adobe Target gecreeerd.

| Type activiteit | Beschrijving |
|--- |--- |
| [A/B-test](/help/c-activities/t-test-ab/test-ab.md) | Bij het testen van A/B worden twee of meer versies van de inhoud van uw website vergeleken om te zien welke versie het beste uw omzettingen tijdens een vooraf gespecificeerde testperiode verbetert.<br>**Opmerking:** U kunt nu [aanbevelingen opnemen in de A/B-testactiviteiten](/help/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit is een [Target Premium-licentie](/help/c-intro/intro.md#premium)vereist. |
| [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Met Automatisch toewijzen wordt een winnaar geïdentificeerd aan de hand van twee of meer ervaringen en wordt automatisch meer verkeer toegewezen aan de winnaar, zodat de conversie toeneemt terwijl de test nog steeds wordt uitgevoerd en opgedaan.<br>**Opmerking:** U kunt nu [aanbevelingen opnemen in de activiteiten](/help/c-recommendations/recommendations-as-an-offer.md)voor automatisch toewijzen. Voor deze functionaliteit is een [Target Premium-licentie](/help/c-intro/intro.md#premium)vereist. |
| [Auto-](/help/c-activities/auto-target/auto-target-to-optimize.md)<br>![Target Premium](/help/assets/premium.png) | AutoTarget maakt gebruik van geavanceerd computerleren om meerdere ervaren die door markters worden gedefinieerd, te identificeren en biedt elke bezoeker de meest op maat gemaakte ervaring op basis van zijn individuele klantprofiel en het gedrag van eerdere bezoekers met vergelijkbare profielen, om inhoud en stationsomzettingen aan te passen.<br>**Opmerking:** U kunt nu [aanbevelingen opnemen in Auto-Target-activiteiten](/help/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit is een This-functionaliteit vereist dat u een [Target Premium-licentie](/help/c-intro/intro.md#premium)hebt. |
| [Analytische gegevens](/help/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) gebruiken (A4T) | U kunt een activiteit vormen om als rapporteringsbron te gebruiken [!DNL Adobe Analytics] . Voor dit type activiteit is het vereist dat u uw [!DNL Adobe Experience Cloud] account koppelt aan zowel [!DNL Analytics] als [!DNL Target]. |
| [Multivariatietest](/help/c-activities/c-multivariate-testing/multivariate-testing.md) | MVT (Multivariate Testing) vergelijkt combinaties van aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifieke doelgroep presteert, en identificeert welk element de meeste invloed op het succes van de activiteit heeft. |
| [Gericht op ervaring](/help/c-activities/t-experience-target/experience-target.md) | Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.<br>**Opmerking:** U kunt nu [aanbevelingen opnemen in de activiteiten](/help/c-recommendations/recommendations-as-an-offer.md)Experience Targeting. Voor deze functionaliteit is een [Target Premium-licentie](/help/c-intro/intro.md#premium)vereist. |
| [Geautomatiseerde](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>![personalizationTarget Premium](/help/assets/premium.png) | Automated Personalization (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende verschillen met elke bezoeker op basis van hun individuele klantprofiel met elkaar in overeenstemming te brengen, om inhoud en schijfconversies aan te passen. |
| [](/help/c-recommendations/recommendations.md)<br>![RecommendationsTarget Premium](/help/assets/premium.png) | Een aanbeveling bepaalt hoe een product aan een websitegebruiker wordt voorgesteld, afhankelijk van de activiteiten van die gebruiker op de plaats.<br>U kunt bijvoorbeeld mensen die een rugzak kopen aanmoedigen om wandelschoenen en wandelstokken te kopen. U kunt een aanbeveling maken die items toont die vaak samen worden aangeschaft met het algoritme &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. U kunt bezoekers ook aanmoedigen om meer tijd te besteden aan uw mediasite door dezelfde video aan te bevelen als de video die ze bekijken. Gebruik hiervoor het algoritme &quot;Personen die dit hebben bekeken&quot;.<br>**Opmerking:** U kunt nu aanbevelingen opnemen in de A/B-test (inclusief Automatische toewijzing en Auto-Target) en de Experience Targeting-activiteiten (XT). Zie [Recommendations als een voorstel](/help/c-recommendations/recommendations-as-an-offer.md). |

## Activiteitenlijst {#section_DE8E2DB30D534962A931EF8BB48240F5}

De [!UICONTROL Activities] lijst is de standaardweergave wanneer u opent [!DNL Target]. U kunt nieuwe activiteiten maken op deze pagina en bestaande activiteiten beheren.

U kunt de [!UICONTROL Activities] lijst ook weergeven door op het [!UICONTROL Activities] tabblad boven aan de [!DNL Target] gebruikersinterface te klikken.

![Activiteitenlijst](/help/c-activities/assets/activities-list.png)

De activiteitenlijst geeft een overzicht van alle activiteiten:

| Element | Beschrijving |
|--- |--- |
| Type | Het activiteitstype, zoals A/B of MVT. |
| Naam | De naam van de activiteit. |
| URL | De URL wordt weergegeven in lichtere tekst onder de naam.<br>De URL voor de activiteit identificeert waar de activiteit wordt getoond. Hierdoor kunt u snel een activiteit identificeren en bepalen of op een bepaalde pagina al een test wordt uitgevoerd.<br>Als een test op veelvoudige URLs loopt, toont een verbinding hoeveel meer URLs worden gebruikt. Klik op de koppeling om de volledige lijst met URL&#39;s voor die activiteit weer te geven.<br>U kunt zoeken op basis van URL. Gebruik de vervolgkeuzelijst naast het zoekvak en selecteer [!UICONTROL Search URL]. |
| Status | De status van de activiteit kan een van de volgende zijn:<ul><li>**Live**: De activiteit wordt momenteel uitgevoerd.</li><li>**Concept**: De activiteitenopstelling is begonnen maar de activiteit is nog niet klaar om te lopen.</li><li>**Gepland**: De activiteit is klaar om te worden geactiveerd wanneer de gespecificeerde begindatum en de tijd aankomen.</li><li>**Inactief**: De activiteit is gepauzeerd of gedeactiveerd.</li><li>**Synchroniseren**: De activiteit is opgeslagen en wordt gesynchroniseerd aan het de leveringsnetwerk van het Doel.</li><li>**Beëindigd**: De opgegeven einddatum en -tijd van de activiteit zijn bereikt en de activiteit wordt niet meer uitgevoerd.</li><li>**Gearchiveerd**: De activiteit is gearchiveerd. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.</li></ul>**Opmerking**: Wanneer u bepaalde acties uitvoert, zoals het activeren van een activiteit buiten de UI die API methodes gebruikt, kan de update tot tien minuten vergen om aan UI te verspreiden. |
| Bron | Toont waar de activiteit werd gecreeerd:<ul><li>Adobe Target</li><li>Adobe Target Classic</li><li>Adobe Experience Manager (AEM)</li><li>Adobe Mobile Services (AMS)</li></ul> |
| Eigenschap | Geeft de [eigenschap](/help/administrating-target/c-user-management/property-channel/property-channel.md) voor de activiteit weer. |
| Geschat bedrag aan inkomsten | Toont de voorspelde toename van inkomsten als 100% van het publiek de winnende ervaring ziet.<br>Berekend met de volgende formule:<br>`(<winning experience> - <control experience>)*<total number of visitors>`<br>Dit getal wordt afgerond tot op één decimaal, maximaal, als het versmalde formulier slechts één cijfer voor het decimaalteken heeft. Bijvoorbeeld: $1,6 M, $60 K, $900, $8,5 K, $205<br>KTDeze kolom toont &quot;—&quot;voor activiteiten die niet genoeg gegevens hebben om een winnaar te roepen of geen kostenraming hebben.<br>Zie [Schatting van Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie. |
| Laatst bijgewerkt | De datum waarop de activiteit voor het laatst is bijgewerkt en door wie. |

Plaats de muis boven een activiteit om de beschikbare handelingen weer te geven.

![Handelingen in de lijst met activiteiten](/help/c-activities/assets/activities_list_hover.png)

De volgende handelingen zijn beschikbaar (afhankelijk van uw machtigingen):

| Handeling | Beschrijving |
| --- | --- |
| Bewerken | Wijzig de activiteit. Elke activiteit kan worden bewerkt.<br>Zie Een activiteit [bewerken of opslaan als concept](/help/c-activities/edit-activity.md)voor meer informatie over de verschillende manieren waarop u activiteiten kunt bewerken. |
| Deactiveren | Stop een live of geplande activiteit. Een gedeactiveerde campagne kan opnieuw worden geactiveerd of worden<br>gearchiveerdAls u een activiteit deactiveert of archiveert en deze later opnieuw activeert, blijft een bezoeker na de reactivering deel uitmaken van die activiteit als deze zich in de activiteit bevond voordat deze werd gedeactiveerd of gearchiveerd. Alle conversiemetriek die tijdens de tijd tussen de twee gebeurtenissen is vastgelegd, worden niet aan die activiteit toegewezen. |
| Activeren | Een inactieve of kant-en-klare activiteit starten. |
| Archief | Verzend de activiteit naar het archief. Gearchiveerde activiteiten worden standaard niet meer weergegeven in de lijst Activiteiten. Wijzig het filter voor de activiteitenlijst om gearchiveerde activiteiten op te nemen om ze te zien. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.<br>Als u een activiteit deactiveert of archiveert en deze later opnieuw activeert, blijft een bezoeker deel uitmaken van die activiteit nadat de activiteit opnieuw is geactiveerd, als hij of zij zich daarin bevond voordat de activiteit werd gedeactiveerd of gearchiveerd. Alle conversiemetriek die tijdens de tijd tussen de twee gebeurtenissen is vastgelegd, worden niet aan die activiteit toegewezen. |
| Kopiëren | Kopieer een activiteit. Elke activiteit kan worden gekopieerd. Wanneer u een activiteit kopieert, wordt er een nieuwe activiteit met dezelfde naam gemaakt, die wordt toegevoegd met &quot;Copy&quot;. Een test met de naam &quot;Browser Offers&quot; wordt bijvoorbeeld gekopieerd naar &quot;Browser Offers Copy&quot;.<br>Visuele aanbiedingen worden gekopieerd met de activiteit. U kunt de voorstellen in de kopie veilig bewerken zonder dat dit invloed heeft op de oorspronkelijke activiteit. De enige uitzondering hierop vormen de opgeslagen aanbiedingen en afbeeldingen in de map Inhoud/Middelen. |
| Verwijderen | Een concept of activiteit verwijderen.<BR>**OPMERKING**: Verwijderde activiteiten kunnen niet worden hersteld. Gebruik de [!UICONTROL Archive] handeling, tenzij u er absoluut zeker van bent dat u deze activiteit nooit meer nodig hebt. U kunt de activiteit vervolgens desgewenst opnieuw activeren. |

Let op de volgende details over de activiteitenlijst:

* Gearchiveerde en beëindigde activiteiten worden niet in de [!UICONTROL Activities] lijst weergegeven. Als u deze activiteiten wilt weergeven, filtert u ze met de geavanceerde filterinstellingen op de linkerspoorstaaf.
* Zodra een oorspronkelijk in gemaakte activiteit [!DNL Target Classic] wordt gedeactiveerd of geschrapt, wordt het geschrapt van [!DNL Target Standard/Premium]. Verwijderde activiteiten die oorspronkelijk in zijn gemaakt, [!DNL Target Classic] worden niet verzonden naar de [!UICONTROL Archive] map in [!DNL Target Standard/Premium]. De functionaliteit voor gearchiveerde mappen is alleen van toepassing op activiteiten die zijn gemaakt in [!DNL Target Standard/Premium].
* Alle activiteitstypen behalve [!UICONTROL Automated Personalization] (AP) [!UICONTROL Auto-Allocate]en [!UICONTROL Auto-Target] geven u de keuze om [!DNL Target] of als gegevensbron te gebruiken [!DNL Adobe Analytics] . [!UICONTROL AP], [!UICONTROL Auto-Allocate]en [!UICONTROL Auto-Target] altijd ** [!DNL Target] gegevens gebruiken.
* De activiteiten zijn beschikbaar voor verschillende kanalen:

   * Websites en mobiele sites
   * Schermen en apparaten met internetverbinding, waaronder kiosken en geldautomaten
   * E-mail en andere verwervingskanalen of partnerplaatsen
   * Mobiele apps
   * Overal waar u gecodeerde inhoud kunt leveren

## Sorteren en filteren van de lijst Activiteiten {#section_41DAD479FFF740E2BB67BF4825955670}

Standaard wordt de lijst gesorteerd op de datum waarop de activiteit voor het laatst is gewijzigd, met de meest recente bovenaan. Nochtans, zijn er verscheidene het filtreren opties om u te helpen de lijst aanpassen om de activiteiten te tonen u wilt zien.

### Zoeken {#search-heading}

Gebruik het zoekveld om te zoeken naar activiteiten die voldoen aan uw zoekcriteria.

![Activiteiten zoeken](/help/c-activities/assets/activities_search_new.png)

Het zoekveld bevat een vervolgkeuzemenu waarmee u uw zoekopdracht kunt beperken door een van de volgende zoekfilters op te geven: [!UICONTROL Activity Name] en [!UICONTROL URL].

### Activiteitenlijstfilters

U kunt bepalen welke activiteiten in uw lijst Activiteiten verschijnen door lijstfilters te selecteren.

![Filteractiviteiten per type](/help/c-activities/assets/activities_filters_new.png)

U kunt filteren op de volgende opties. Als er in elke categorie niets is geselecteerd, is de standaardwaarde Alles.

| Filtercategorie | Filter |
|--- |--- |
| Type | A/B-test: [Handmatig](/help/c-activities/t-test-ab/test-ab.md), [automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)en [automatisch toewijzen](/help/c-activities/auto-target/auto-target-to-optimize.md).<br>[Geautomatiseerde](/help/c-activities/t-automated-personalization/automated-personalization.md)<br>[PersonalizationExperience](/help/c-activities/t-experience-target/experience-target.md)<br>[TargetingMultivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md)<br>[TestRecommendations](/help/c-recommendations/recommendations.md) |
| Status | <br><br><br><br><br><br>LiveDraftScheduledInactiveSyncingEndedArchived |
| Rapportagebron | <br>TargetAnalytics |
| Experience Composer | Op<br>VisualForm gebaseerd |
| Type statistieken | <br><br>ConversionRevenueEngagement |
| Activiteitsbron | Adobe<br>TargetAdobe Target<br>ClassicAdobe Experience<br>ManagerAdobe Mobile Services |

### Sorteren op activiteitskenmerk

Klik op een van de volgende koppen om te schakelen of de activiteiten in oplopende of aflopende volgorde worden weergegeven volgens de geselecteerde kop.

* Naam activiteit
* Type activiteit

![Activiteitenlijst oplopende volgorde](/help/c-activities/assets/activities_list_ascending.png)

## Tips en trucs {#section_F77F30A246A14B538D9363B7F3639F97}

Haal het meeste uit Adobe Target door meer te leren over verschillende functies en te zien waarom je ze een poging moet doen. De functie Tips en trucs biedt koppelingen naar video&#39;s, gebruiksscenario&#39;s, blogs, documentatie en nog veel meer.

De functie Tips en trucs wordt periodiek weergegeven op de pagina Activiteiten. Nadat u een tip hebt gelezen of gesloten, wordt deze pas weer weergegeven als de volgende tip beschikbaar is. U kunt desgewenst de weergave van alle tips uitschakelen door op het Help-pictogram > [!UICONTROL Disable Tip of the Day]te klikken.

![Tip van de dag uitschakelen](/help/c-activities/assets/tip-disable-new.png)

## Beperkingen {#section_049D4684403A4E07B998067EB8E9BE56}

Elke doelactiviteit heeft de volgende inhoudsbeperkingen:

| Item | Limiet |
|--- |--- |
| Unieke kiezers | 300 wanneer een kiezer in een andere ervaring wordt herhaald, wordt deze eenmaal meegeteld. Als het echter in dezelfde ervaring wordt herhaald, wordt het opnieuw geteld. |
| Aanbiedingen in elke ervaring | 350 |
| Klik op kiezers bijhouden in metriek | 50 |
| Mboxen in metriek | 50 |
| Soorten publiek en locaties | De combinatie van 50 soorten publiek en locaties (mbox) mag niet meer dan 50 zijn. |

De activiteit kan niet worden bewaard als u om het even welk van deze grenzen overschrijdt.

Als u het aantal van deze items in uw activiteit vergroot, neemt ook de tijd die nodig is om de activiteit in het hele doel te synchroniseren, toe.

Voor extra grenzen van de Visuele Composer van de Ervaring, zie de Beperkingen van de Samensteller van de [Visuele Ervaring](../c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributen geïmporteerd in Target voor activiteiten bijgewerkt buiten Target {#section_802B0D174E6A44E1A96F404CA81AAE44}

Als in gemaakte activiteiten van buiten [!DNL Target] worden bijgewerkt [!DNL Target] (bijvoorbeeld via Adobe I/O), worden de volgende activiteitskenmerken weer geïmporteerd in [!DNL Target]:

`thirdpartyId`

`startDate`

`endDate`

`status`

`priority`

`marketingCloudMetadata(remoteModifiedBy)`

Deze importtaak wordt uitgevoerd wanneer de activiteitenpagina wordt geopend, met een maximale vertraging van tien minuten. (kB-1526)

## Trainingsvideo&#39;s {#section_BE80D13A2E81460C885F902010E1AD87}

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Activiteitstypen (9:03) ![overzichtspagina](/help/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Managing Activity (5:55) ![Overview badge](/help/assets/overview.png)

In deze video wordt uitgelegd hoe u de lijst Activiteiten kunt gebruiken om activiteiten te beheren.

* De term *activiteit definiëren*
* Activiteiten zoeken in de lijst Activiteiten
* Activiteiten bewerken, deactiveren, kopiëren en verwijderen

>[!VIDEO](https://video.tv.adobe.com/v/18550)
