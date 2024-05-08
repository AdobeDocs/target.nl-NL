---
keywords: activiteitenlijst;activiteiten;activiteit;activiteitstypen;activiteit bewerken;activiteit;activiteit, acties;activiteitskenmerk;activiteitlijstfilter;activiteitsbeperkingen;personaliseren;personalisatie
description: Meer informatie over activiteiten in [!DNL Target] Hiermee kunt u de inhoud aanpassen aan specifieke doelgroepen en kunt u paginaontwerpen testen.
title: Hoe kan ik inhoud personaliseren en pagina-ontwerpen testen met [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: be63fa4c89f229e3f4566cb400e1268d2cdf08d2
workflow-type: tm+mt
source-wordcount: '2290'
ht-degree: 0%

---

# Activiteiten

Activiteiten in [!DNL Adobe Target] Hiermee kunt u de inhoud aanpassen aan specifieke doelgroepen en kunt u paginaontwerpen testen.

U kunt bijvoorbeeld een activiteit ontwerpen die twee verschillende landingspagina&#39;s test, een die informatie over dameszomerschoenen markeert, en een andere landingspagina die meer algemene zomerkleding markeert. De activiteit bepaalt de voorwaarden die controleren wanneer elk van deze landingspagina&#39;s verschijnt, en de metriek die bepalen welke pagina succesvoller is. De activiteit wordt gevormd om te beginnen en te beëindigen wanneer specifieke voorwaarden, zoals tussen specifieke data worden voldaan, of om te beginnen wanneer de activiteit wordt goedgekeurd en te beëindigen wanneer het wordt gedeactiveerd.

Wanneer het ontwerpen van een activiteit, zou u zorgvuldig moeten plannen. Bepaal wanneer de activiteit begint en hoe lang het duurt. Geef vervolgens een lijst met uw aanbiedingen en wijs een doelgroep toe aan elk aanbod.

## Activiteitenlijst {#section_DE8E2DB30D534962A931EF8BB48240F5}

De [!UICONTROL Activities] lijst is de standaardweergave wanneer u opent [!DNL Target]. U kunt activiteiten maken op deze pagina en bestaande activiteiten beheren.

U kunt ook de [!UICONTROL Activities] door op de lijst te klikken [!UICONTROL Activities] tabblad boven aan het dialoogvenster [!DNL Target] UI.

![Activiteitenlijst](/help/main/c-activities/assets/activities-list-new.png)

De [!UICONTROL Activities] De lijst geeft een overzicht van alle activiteiten en biedt u de mogelijkheid om verschillende handelingen uit te voeren:

| Element | Beschrijving |
|--- |--- |
| Linkernavigatieregel | Schakel tussen uw opgeslagen of live activiteiten en mislukt of [ontwerpactiviteiten](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Show filters] pictogram<P>![Pictogram Filters tonen](/help/main/c-activities/assets/show-filters-icon.png) | De filters van de toegang door te klikken **[!UICONTROL Show Filters]** aan de bovenkant van de lijst.<P>Zie voor meer informatie [Filters toepassen op de lijst Activiteiten](#filters) hieronder. |
| Zoekvak | Snel een activiteit vinden of het aantal activiteiten verminderen dat in [!UICONTROL Activity] lijst. U kunt zoeken op [!UICONTROL Name], [!UICONTROL URL], of [!UICONTROL ID]. |
| [!UICONTROL Create Activity] | Maak een activiteit. Zie voor meer informatie over het maken van de verschillende typen activiteiten: <ul><li>[Een A/B-test maken](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[Een activiteit voor automatisch toewijzen maken](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[Een automatisch doelactiviteit maken](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[Een Automated Personalization-activiteit maken](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[Een belevenis maken die gericht is op activiteit](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[Een multivariatietest maken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[Een Recommendations-activiteit maken](/help/main/c-recommendations/recommendations.md)</li></ul>Voor meer informatie over elk type, zie [Typen activiteiten](#types) hieronder. |
| [!UICONTROL Create mobile preview link]<P>![Menu Meer handelingen](/help/main/c-activities/assets/icon-create-mobile-link.png) | Gebruiken [mobiele voorvertoningskoppelingen](https://experienceleague.adobe.com/docs/target-dev/developer/mobile-apps/target-mobile-preview.html) om eenvoudige end-to-end QA voor mobiele toepassingsactiviteiten uit te voeren.<P>Klik op de knop **Meer opties** pictogram (de verticale ellips), selecteer **Koppeling voor mobiele voorvertoning maken** Kies vervolgens de activiteiten die u op mobiele apparaten wilt testen. |
| Tabel aanpassen<P>![Pictogram Tabel aanpassen](/help/main/c-activities/assets/icon-customize-table.png) | Wijzigen welke kolommen worden weergegeven in het dialoogvenster [!UICONTROL Activity] door op de lijst te klikken **[!UICONTROL Customize Table]** aan de rechterbovenzijde van de tabel en vervolgens de gewenste kolommen selecteren of de selectie ervan opheffen.<P>De wijzigingen worden toegepast op uw account en blijven actief, zelfs nadat u zich hebt afgemeld bij [!DNL Target]. |
| Selectievakjes voor bulkbewerkingen | bulktransacties uitvoeren op alle activiteiten of op geselecteerde activiteiten.<P>Voor een lijst van acties die beschikbaar zijn (afhankelijk van uw toestemmingen en de activiteitenstatus), zie [Snelle handelingen uitvoeren](#quick-actions) hieronder. |
| [!UICONTROL Type] | Het type activiteit. De [!UICONTROL Type] in de kolom kunt u snel elke activiteit op type identificeren. <ul><li>AB-M: handleiding [!UICONTROL A/B Test]</li><li>AB-AA: [!UICONTROL Auto-Allocate]</li><li>AB-AT: [!UICONTROL Auto-Target]</li><li>AP: [!UICONTROL Automated Personalization]</li><li>XT: [!UICONTROL Experience Targeting]</li><li>MVT: [!UICONTROL Multivariate Test]</li><li>REC: [!UICONTROL Recommendations]</li></ul>Voor meer informatie over elk type, zie [Typen activiteiten](#types) hieronder. |
| [!UICONTROL Name] | De naam van de activiteit. Klik op de naam van een activiteit om die activiteit weer te geven [!UICONTROL Overview] pagina. <P>Klik op de knop **[!UICONTROL Quick Info]** naast elke naam van de activiteit om meer informatie over die activiteit in een pop-up kaart te bekijken.<p>Klik op de knop **[!UICONTROL More actions]** pictogram (de horizontale ellips) naast elke activiteitennaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren. De volgende acties zijn beschikbaar (afhankelijk van uw machtigingen en de activiteitsstatus): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete], en [!UICONTROL Archive]. Zie voor meer informatie over elke actie [Snelle handelingen uitvoeren](#quick-actions) hieronder.<P>Klik op de tabelkop om de lijst alfabetisch te sorteren in oplopende of aflopende volgorde op naam. |
| [!UICONTROL Status] | De status van de activiteit kan een van de volgende zijn:<ul><li>**Live**: De activiteit wordt momenteel uitgevoerd.</li><li>**Concept**: De activiteiteninstelling is gestart, maar de activiteit is in [conceptmodus](/help/main/c-activities/edit-activity.md) en is nog niet klaar om te worden uitgevoerd.</li><li>**Gepland**: De activiteit kan worden geactiveerd wanneer de opgegeven begindatum en -tijd aankomen.</li><li>**Inactief**: De activiteit is onderbroken of gedeactiveerd.</li><li>**Synchroniseren**: De activiteit is opgeslagen en wordt gesynchroniseerd met de [!DNL Target] leveringsnetwerk.</li><li>**Afgelopen**: De opgegeven einddatum en -tijd van de activiteit zijn bereikt en de activiteit wordt niet meer uitgevoerd.</li><li>**Gearchiveerd**: De activiteit is gearchiveerd. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.</li></ul>**Opmerking**: Wanneer u bepaalde handelingen uitvoert, zoals het activeren van een activiteit buiten de [!DNL Target] UI die API methodes gebruikt, kan de update tot tien minuten aan propageren aan [!DNL Target] UI. |
| [!UICONTROL Last Updated] | De datum en het tijdstip waarop de activiteit voor het laatst is bijgewerkt en door wie.<P>Klik op de tabelkop om de lijst op datum in oplopende of aflopende volgorde te sorteren. |
| [!UICONTROL Priority] | De prioriteit van de activiteit.<P>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<P>Afhankelijk van uw [instellingen](/help/main/administrating-target/reporting.md)de [!DNL Target] UI en opties voor [!UICONTROL Priority] variëren. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen. |
| [!UICONTROL Property] | Hiermee wordt het dialoogvenster [eigenschap](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) voor de activiteit.<P>Gebruikersmachtigingen voor ondernemingen zijn [Doelpremie](/help/main/c-intro/intro.md#premium) gebruiken. |
| [!UICONTROL Estimated Lift in Revenue] | Toont de voorspelde toename van inkomsten als 100% van het publiek de winnende ervaring ziet.<P>Berekend met de volgende formule:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Dit getal wordt afgerond tot op één decimaal (maximaal) als het versmalde formulier slechts één cijfer voor het decimaalteken heeft. Bijvoorbeeld: $1,6M, $60K, $900, $8,5K, $205K<P>Deze kolom toont &quot;—&quot; voor activiteiten die niet genoeg gegevens hebben om een winnaar te roepen of geen kostenraming hebben.<P>Zie [Schatting van de opbrengst](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie . |
| [!UICONTROL Source] | Toont waar de activiteit werd gecreeerd: [!DNL Adobe Target], [ADOBE TARGET API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html), [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html), [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html), of [Adobe mobiele services](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Location] | De URL voor de activiteit identificeert waar de activiteit wordt getoond. Deze kolom helpt u snel een activiteit identificeren en bepalen of een bepaalde pagina reeds een activiteit heeft die op het loopt.<P>Als een activiteit op veelvoudige URLs loopt, toont een verbinding hoeveel meer URLs worden gebruikt. Klik op de koppeling om de volledige lijst met URL&#39;s voor die activiteit weer te geven.<P>U kunt zoeken op basis van URL. Gebruik de vervolgkeuzelijst naast het zoekvak en selecteer [!UICONTROL URL]. |
| Auteur | De naam van de persoon die de activiteit heeft gemaakt. |
| [!UICONTROL Decisioning Method] | De bij elke activiteit gebruikte beslissingsmethode: [Server-kant](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html) of [Client-kant](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html). |

## Typen activiteiten {#types}

[!DNL Target] bevat diverse activiteitstypen. In de volgende tabel vindt u een overzicht van elk type activiteit met koppelingen voor meer informatie. Om u beter te helpen het beste type activiteit voor uw doeleinden kiezen, hebben wij ook gecreeerd [Adobe Target Activity Guide](/help/main/c-activities/target-activities-guide.md).

| Type activiteit | Beschrijving |
|--- |--- |
| [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) | Bij een A/B-test worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode. |
| [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Auto-Allocate], een type A/B test, identificeert een winnaar onder twee of meer ervaringen en wijst automatisch meer verkeer aan de winnaar toe om omzettingen te verhogen terwijl de test blijft lopen en leren. |
| [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![Doelpremie](/help/main/assets/premium.png) | Auto-Target, een type A/B test, gebruikt geavanceerd machine leren om veelvoudige high-performance marketer-bepaalde ervaringen te identificeren, en dient de meest op maat gemaakte ervaring aan elke bezoeker die op het profiel van de individuele klant en het gedrag van vorige bezoekers met gelijkaardige profielen wordt gebaseerd, om inhoud en aandrijvingsomzettingen te personaliseren. |
| [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) vergelijkt combinaties aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert, en identificeert welk element het meest van invloed is op het succes van de activiteit. |
| [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT) levert inhoud aan een specifiek publiek dat op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd. |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![Doelpremie](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende verschillen met elke bezoeker op basis van hun individuele klantprofiel met elkaar in overeenstemming te brengen, om inhoud en schijfconversies aan te passen. |
| [Recommendations](/help/main/c-recommendations/recommendations.md)<P>![Doelpremie](/help/main/assets/premium.png) | Een aanbeveling bepaalt hoe een product aan een websitebezoeker wordt voorgesteld, afhankelijk van de activiteiten van die bezoeker op de plaats.<P>U kunt bijvoorbeeld mensen die een rugzak kopen aanmoedigen om wandelschoenen en wandelstokken te kopen. U kunt een aanbeveling maken die items toont die vaak samen worden aangeschaft met het algoritme &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. U kunt bezoekers ook aanmoedigen om meer tijd te besteden aan uw mediasite door vergelijkbare video&#39;s aan te bevelen als de video die ze bekijken. Gebruik hiervoor het algoritme &quot;Personen die dit hebben bekeken&quot;.<P>**OPMERKING**: U kunt ook aanbevelingen opnemen in [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Experience Targeting] (XT) activiteiten. Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit hebt u een [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium). |

## Filters toepassen op de lijst Activiteiten {#filters}

De filters van de toegang door te klikken **[!UICONTROL Show Filters]** aan de bovenkant van de lijst.

![Filteropties](/help/main/c-activities/assets/show-filters-options.png)

In het menu kunt u activiteiten filteren op de volgende kenmerken: |Kenmerk|Details| | — | — | |[!UICONTROL Type]|Filteren op [type activiteit](#types).| |[!UICONTROL Status]|Filteren op activiteitsstatus.| |[!UICONTROL Reporting Source]|Filteren op rapportagebron.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): Weergaveactiviteiten die gebruikmaken [!UICONTROL Analytics for Target] (A4T) als bron van rapportage.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): Weergaveactiviteiten die gebruikmaken [!DNL Target] als de bron van de rapportage.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): Weergaveactiviteiten die gebruikmaken [!DNL Adobe Customer Analytics] als de bron van de rapportage.</li></ul>| |[!UICONTROL Experience Composer]|Filter waarmee de ervaring van composer tijdens het creëren van activiteit werd gebruikt:<ul><li>[Zichtbaar](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): Hiermee geeft u activiteiten weer die zijn gemaakt met de [!UICONTROL Visual Experience Composer] (VEC).</li><li>[Op basis van formulier](/help/main/c-experiences/form-experience-composer.md): Geef activiteiten weer die zijn gemaakt met de [!UICONTROL Form-Based Experience Composer].</li></ul>| |[!UICONTROL Metrics Type]|Filter waardoor [succesmetrisch](/help/main/c-activities/r-success-metrics/success-metrics.md) is gekozen tijdens het maken van activiteiten.<ul><li>Conversie</li><li>Ontvangsten</li><li>Betrokkenheid</li></ul>| |[!UICONTROL Decisioning Method]|Filteren volgens de bij elke activiteit gebruikte beslissingsmethode<ul><li>[Server-kant](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html): De activiteiten van de vertoning die server-zijbesluit gebruiken.</li><li>[Client-kant](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html): De activiteiten van de vertoning die cliënt-zijbeslissing gebruiken.</li></ul>| |[!UICONTROL Activity Source]|Filteren op de activiteitsbron die wordt gebruikt om elke activiteit te maken.<ul><li>[!DNL Adobe Target]</li><li>[ADOBE TARGET API](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html)</li><li>[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html)</li><li>[Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html)</li><li>[Adobe mobiele services](https://developer.adobe.com/client-sdks/documentation/)</li></ul>| |[!UICONTROL Property]|Filteren op [eigenschap](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) waarin de activiteit is gecreëerd.|

## Snelle handelingen uitvoeren {#quick-actions}

Klik op de knop **[!UICONTROL More actions]** pictogram (de horizontale ellips) naast elke activiteitennaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren.

![Opties voor snelle handelingen](/help/main/c-activities/assets/quick-actions.png)

De volgende acties zijn beschikbaar (afhankelijk van uw machtigingen en de activiteitsstatus):

| Handeling | Beschrijving |
| --- | --- |
| [!UICONTROL Edit] | Wijzig de activiteit. Elke activiteit kan worden bewerkt.<P>Voor meer informatie over de verschillende manieren kunt u activiteiten uitgeven, zie [Een activiteit bewerken of opslaan als concept](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deactivate] | Stop een live of geplande activiteit. Een gedeactiveerde activiteit kan opnieuw worden geactiveerd of worden gearchiveerd.<P>Als u een activiteit deactiveert of archiveert en deze later opnieuw activeert, blijft een bezoeker deel uitmaken van die activiteit nadat de activiteit opnieuw is geactiveerd, als hij of zij zich daarin bevond voordat de activiteit werd gedeactiveerd of gearchiveerd. Alle conversiemetriek die tijdens de tijd tussen de twee gebeurtenissen is vastgelegd, worden niet aan die activiteit toegewezen. |
| [!UICONTROL Activate] | Start een inactieve activiteit of een activiteit die klaar is om te worden geactiveerd. |
| [!UICONTROL Archive] | Verzend de activiteit naar het archief. Gearchiveerde activiteiten worden standaard niet meer weergegeven in de [!UICONTROL Activities] lijst. Wijzig het filter voor de activiteitenlijst om gearchiveerde activiteiten op te nemen om ze te zien. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.<P>Als u een activiteit deactiveert of archiveert en deze later opnieuw activeert, blijft een bezoeker deel uitmaken van die activiteit na de reactivering als hij of zij die activiteit had voordat deze werd gedeactiveerd of gearchiveerd. Alle conversiemetriek die tijdens de tijd tussen de twee gebeurtenissen is vastgelegd, worden niet aan die activiteit toegewezen. |
| [!UICONTROL Copy] | Kopieer een activiteit. Elke activiteit kan worden gekopieerd. Wanneer u een activiteit kopieert, wordt er een nieuwe activiteit met dezelfde naam gemaakt, die wordt toegevoegd met &quot;Copy&quot;. Een test met de naam &quot;Browser Offers&quot; wordt bijvoorbeeld gekopieerd naar &quot;Browser Offers Copy&quot;.<P>Visuele aanbiedingen worden gekopieerd met de activiteit. U kunt de voorstellen in de kopie veilig bewerken zonder dat dit invloed heeft op de oorspronkelijke activiteit. De enige uitzondering hierop vormen de opgeslagen aanbiedingen en afbeeldingen in de map Inhoud/Middelen. |
| [!UICONTROL Delete] | Een concept of activiteit verwijderen.<P>**OPMERKING**: Verwijderde activiteiten kunnen niet worden hersteld. Tenzij u zeker weet dat u deze activiteit nooit meer nodig hebt, kunt u de opdracht [!UICONTROL Archive] handeling. U kunt de activiteit dan opnieuw activeren indien nodig. |

## Overwegingen

Let op het volgende over de [!UICONTROL Activity] lijst:

* Gearchiveerde en beëindigde activiteiten worden niet weergegeven in de [!UICONTROL Activities] lijst. Als u deze activiteiten wilt weergeven, filtert u ze met de [Filterpictogram](#filters) boven aan de lijst.
* Wanneer een activiteit oorspronkelijk werd gecreeerd in [!DNL Target Classic] wordt gedeactiveerd of verwijderd, wordt het verwijderd uit [!DNL Target Standard/Premium]. Verwijderde activiteiten die oorspronkelijk zijn gemaakt in [!DNL Target Classic] worden niet verzonden naar de [!UICONTROL Archive] map in [!DNL Target Standard/Premium]. De functionaliteit voor gearchiveerde mappen is alleen van toepassing op activiteiten die zijn gemaakt in [!DNL Target Standard/Premium].
* Alle andere activiteitstypen [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate], en [!UICONTROL Auto-Target] u de keuze te geven of [!DNL Target] of [!DNL Adobe Analytics] als gegevensbron. [!UICONTROL AP], [!UICONTROL Auto-Allocate], en [!UICONTROL Auto-Target] *altijd* gebruiken [!DNL Target] gegevens.
* De activiteiten zijn beschikbaar voor verschillende kanalen:

   * Websites en mobiele sites
   * Schermen en apparaten met internetverbinding, waaronder kiosken en geldautomaten
   * E-mail en andere verwervingskanalen of partnerplaatsen
   * Mobiele apps
   * Overal waar u gecodeerde inhoud kunt leveren

## Beperkingen {#section_049D4684403A4E07B998067EB8E9BE56}

Elke doelactiviteit heeft de volgende inhoudsbeperkingen:

| Item | Limiet |
|--- |--- |
| Unieke kiezers | 300 wanneer een kiezer in een andere ervaring wordt herhaald, wordt deze eenmaal meegeteld. Als het echter in dezelfde ervaring wordt herhaald, wordt het opnieuw geteld. |
| Aanbiedingen in elke ervaring | 350 |
| Klik op kiezers bijhouden in metriek | 50 |
| Mboxen in metriek | 50 |
| Soorten publiek en locaties | 50 combinaties van soorten publiek en locaties (mbox) mogen niet meer dan 50 zijn. |

De activiteit kan niet worden bewaard als u om het even welk van deze grenzen overschrijdt.

Als u het aantal van deze items in uw activiteit vergroot, neemt ook de tijd die nodig is om de activiteit te synchroniseren over [!DNL Target].

Voor aanvullende grenswaarden van V[!UICONTROL isual Experience Composer] VEC, zie [Beperkingen van composers voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Kenmerken geïmporteerd in [!DNL Target] voor activiteiten die buiten [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

Indien activiteiten die zijn gemaakt in [!DNL Target] worden bijgewerkt van buiten [!DNL Target] (bijvoorbeeld via API) worden de volgende activiteitskenmerken weer geïmporteerd in [!DNL Target]: `thirdpartyId`, `startDate`, `endDate`, `status`, `priority`, en `marketingCloudMetadata(remoteModifiedBy)`.

Deze importtaak wordt uitgevoerd wanneer de pagina met activiteiten wordt geopend, met een maximale vertraging van tien minuten.

## Trainingsvideo&#39;s {#section_BE80D13A2E81460C885F902010E1AD87}

De volgende video bevat meer informatie over de concepten die in dit artikel worden besproken.

### Typen activiteiten (9:03)

In deze video wordt uitgelegd welke soorten activiteiten beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

