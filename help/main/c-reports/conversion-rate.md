---
keywords: Doelstelling
description: Meer informatie over Adobe [!DNL Target] toont en berekent de omrekeningskoers, de lift, het vertrouwen, en het betrouwbaarheidsinterval voor elke ervaring.
title: Hoe bekijk ik het Tarief van de Omzetting, Lift, en het Niveau van het Vertrouwen?
feature: Reports
exl-id: b4cfe926-eb36-4ce1-b56c-7378150b0b09
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '2139'
ht-degree: 0%

---

# Omrekeningskoers

Voor elke ervaring worden de omrekeningskoers, de lift, het betrouwbaarheidsinterval en het betrouwbaarheidsinterval gerapporteerd.

In de volgende afbeelding ziet u de diagramkop voor een voorbeeldactiviteit met de [!UICONTROL Conversion Rate], [!UICONTROL Lift], en [!UICONTROL Confidence] kopteksten gemarkeerd.

![afbeelding met conversiesnelheid](assets/conversion-rate.jpg)

>[!NOTE]
>
>In alle gegevens worden dubbele orders genegeerd als een `orderID` wordt doorgegeven. In het auditrapport worden de genegeerde dubbele orders vermeld.

## Omzetsnelheid {#section_07A36846C4E84D0881906809B9CE5A74}

Hiermee geeft u de mediaan van de conversiesnelheid, het vertrouwen, het interval en het aantal conversies weer.

Kijk bijvoorbeeld naar de volgende rapportkolom Conversiesnelheid:

![conversie-rate-detail-afbeelding](assets/conversion-rate-detail.jpg)

De eerste regel is de besturingservaring. Het toont een 15% omzettingspercentage, met drie omzettingen. De tweede regel, Experience B, toont een 15% conversiesnelheid, met een betrouwbaarheidsinterval van 15,65% of minder en drie conversies.

>[!NOTE]
>
>Momenteel, wordt het betrouwbaarheidsinterval berekend slechts voor binaire metriek.

## Optillen {#section_0F409572C720433D9378092ABC999982}

Vergelijkt de omrekeningskoers voor elke ervaring met controle.

Lift = (Experience CR - Control CR) / Control CR

Als de controle 0 is, is er geen percentagelift.


## Detailgegevens {#section_30A674731BA6440E9BB93C421BE990EE}

De AOV-, RPV- en verkoopgegevens worden voor elke ervaring weergegeven als u een plaatsorder hebt ingevoegd (`orderConfirmPage`) en selecteert u deze als het conversiekader.

## Vertrouwensniveau en betrouwbaarheidsinterval {#concept_0D0002A1EBDF420E9C50E2A46F36629B}

Voor elke ervaring, worden het vertrouwen en het betrouwbaarheidsinterval getoond.

U kunt offlineberekeningen voor Analytics voor Doel (A4T) uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics]. Zie &quot;Offlineberekeningen uitvoeren voor analyse voor doel (A4T)&quot; hieronder voor meer informatie.

### Vertrouwen {#section_26FE5E44BDD5478792A65FCFD83DCCDC}

Het vertrouwen van een getoonde ervaring of aanbieding is een waarschijnlijkheid (uitgedrukt als percentage) om een minder extreem resultaat te verkrijgen dan het resultaat dat daadwerkelijk wordt waargenomen, als de nulhypothese waar is (in wezen als er geen verschil is in omrekeningskoersen tussen die ervaring of dat aanbod en de ervaring/het aanbod van de controle). Wat de p-waarden betreft, wordt dit vertrouwen weergegeven als een 1-p-waarde. Eenvoudiger gezegd, geeft een hoger vertrouwen aan dat de gegevens minder consistent zijn met de aanname dat het aanbod/de ervaring van de controle en de niet-controle gelijke omrekeningskoersen hebben.

Het vertrouwen beloopt tot 100,00% wanneer het vertrouwen 99,995% of meer bedraagt.

![conf_report, afbeelding](assets/conf_report.png)  ![conf_report_detail, afbeelding](assets/conf_report_detail.png)

Alvorens om het even welke bedrijfsbesluiten te nemen, probeer om te wachten tot uw steekproefgrootte groot genoeg is en dat de vier bars van vertrouwen op één of meerdere ervaringen voor een ononderbroken tijdsduur verenigbaar blijven om de resultaten te verzekeren stabiel zijn.


### Vertrouwelijk interval {#section_F582738DFE1648C78B93D81EBC6CACF7}

>[!NOTE]
>
>Momenteel, wordt het betrouwbaarheidsinterval berekend slechts voor binaire metriek.

De *betrouwbaarheidsinterval* is een reeks schattingen waarbinnen de werkelijke waarde van de maatstaf op een bepaald betrouwbaarheidsniveau kan worden gevonden. Doel geeft altijd een betrouwbaarheidsinterval van 95% weer. Het betrouwbaarheidsinterval wordt weergegeven als een lichtgrijs +/- percentage in de kolom Conversiesnelheid. In het onderstaande voorbeeld is het betrouwbaarheidsinterval voor de lift van Experience B plus of min 15,65%.

![omzetten_afbeelding waarderen](assets/conversion_rate.png)

**Voorbeeld:** De waargenomen RPV van een ervaring is $10, en zijn 95% **betrouwbaarheidsinterval** is $5 tot $15. Onbekend voor ons is de werkelijke RPV $12. Als we deze test meerdere keren uitvoeren, zal 95% van de tijd die we berekenen het betrouwbaarheidsinterval bevatten _true_ waarde van de RPV van $12.

**Wat beïnvloedt het vertrouwensinterval?** De formule volgt de statistische standaardmethoden voor de berekening van betrouwbaarheidsintervallen.

* **Voorbeeldformaat:** Als het monster groeit, zal het interval krimpen of smal. Dit wordt geprefereerd aangezien het betekent uw rapporten dichter aan de ware waarde van succes metrisch raken.
* **Standaardafwijking kleiner:** Vergelijkbare resultaten, zoals vergelijkbare AOV&#39;s of vergelijkbare nummers of bezoekers die elke dag converteren, verminderen de standaardafwijking.

## De Berekening van het vertrouwen en hoe te om het off-line uit te voeren {#section_86F7C231943043A5B8B6BFE67B706E3B}

De [gedownload CSV-rapport](/help/main/c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) omvat alleen onbewerkte gegevens en omvat geen berekende meetwaarden, zoals inkomsten per bezoeker, lift of betrouwbaarheid die voor A/B-tests worden gebruikt.

Als u deze berekende meetwaarden wilt berekenen, downloadt u de [Complete betrouwbaarheidscalculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel-bestand om de waarde van de activiteit in te voeren of te reviseren [Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

>[!NOTE]
>
>Deze rekenmachine is bedoeld voor op Target gebaseerde rapportage en niet voor A4T-rapportage.

## Offlineberekeningen uitvoeren voor analyses voor Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics].

Voor A4T gebruiken wij [T-test van Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} berekening voor doorlopende variabelen (in plaats van binaire metriek). In Analytics wordt een bezoeker altijd bijgehouden en wordt elke actie geteld. Daarom als de bezoeker veelvoudige tijden koopt of een succes metrisch veelvoudige tijden bezoekt, worden die extra treffers geteld. Dit maakt metrisch een ononderbroken variabele. Om de t-test-berekening van het Welch uit te voeren, is de &quot;som van de vierkanten&quot; vereist om de variantie te berekenen, die wordt gebruikt in de noemer van de t-statistiek. [Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) licht de details van de gebruikte wiskundige formules toe. De som van de vierkanten kan worden opgehaald [!DNL Analytics]. Om de som gegevens van vierkanten te krijgen, moet u een bezoekersvlakke uitvoer voor metrisch uitvoeren u aan optimaliseert, voor een steekproeftijdspanne.

Bijvoorbeeld, als u aan paginameningen per bezoeker optimaliseert, zou u een steekproef van het totale aantal paginameningen op een per bezoekersbasis voor een gespecificeerd tijdkader uitvoeren, misschien een paar dagen (een paar duizend gegevenspunten is allen u nodig). Vervolgens vigeert u elke waarde en somt u de totalen op (de volgorde van de bewerkingen is hier van essentieel belang). Deze &quot;som van vierkanten&quot;waarde wordt dan gebruikt in de Volledige Berekening van het Vertrouwen. Gebruik de sectie &quot;opbrengst&quot; van dat spreadsheet voor deze waarden.

**Als u de opdracht [!DNL Analytics] functie voor het exporteren van gegevens om dit te doen:**

1. Aanmelden bij [!DNL Adobe Analytics].
1. Klik op **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Op de **[!UICONTROL Data Warehouse Request]** , vult u de velden in.

   Voor meer informatie over elk gebied, zie &quot;Beschrijvingen van de Data Warehouse&quot;in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Veld | Instructies |
   |--- |--- |
   | Naam aanvraag | Geef een naam op voor uw aanvraag. |
   | Datum van rapportage | Geef een tijdsperiode en granulariteit op.<br>Als beste praktijken, kies niet meer dan een uur of één dag van gegevens voor uw eerste verzoek.  De dossiers van de Data Warehouse nemen langer om de langere gevraagde tijdspanne te verwerken, zodat is het altijd beste om een kleine tijdspanne eerst om gegevens te verzoeken om ervoor te zorgen uw dossier het verwachte resultaat terugkeert. Ga vervolgens naar de Request Manager, dupliceer uw verzoek en vraag de tweede keer om meer gegevens. Ook, als u granularity aan om het even wat buiten &quot;niets&quot;schakelt, zal de dossiergrootte drastisch stijgen.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Beschikbare segmenten | Pas indien nodig een segment toe. |
   | Uitsplitsingen | Selecteer de gewenste afmetingen: Standaard is OOTB (out-of-the-box) en Aangepast bevat Vars en props. U kunt het beste &quot;Bezoeker-id&quot; gebruiken als er gegevens op bezoekersidentiteitsniveau nodig zijn in plaats van &quot;Bezoeker-id Experience Cloud&quot;.<ul><li>Bezoeker-id is de laatste id die wordt gebruikt door Analytics. Het zal of HULP (als de klant erfenis is) of MID (als de klant nieuwe of ontruimde koekjes is sinds de dienst van bezoekersidentiteitskaart van MC werd gelanceerd) zijn.</li><li>De Experience Cloud Bezoeker-id wordt alleen ingesteld voor klanten die nieuwe of verwijderde cookies zijn sinds de service MC bezoeker-id is gestart.</li></ul> |
   | Metrisch | Selecteer de gewenste meetgegevens. Standaard is OOTB, terwijl Aangepast aangepaste gebeurtenissen bevat. |
   | Voorvertoning van rapport | Controleer uw instellingen voordat u het rapport plant.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Levering plannen | Voer een e-mailadres in waarnaar u het bestand wilt verzenden, geef het bestand een naam en selecteer vervolgens [!UICONTROL Send Immediately].<br>Opmerking: Het bestand kan via FTP worden geleverd onder [!UICONTROL Advanced Delivery Options]<br>![Levering plannen](/help/main/c-reports/assets/datawarehouse3.png). |

1. Klik op **[!UICONTROL Request this Report]**.

   De levering van het dossier kan tot 72 uren, afhankelijk van de gevraagde hoeveelheid gegevens vergen. U kunt de voortgang van uw verzoek op elk gewenst moment controleren door op [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager].

   Als u gegevens opnieuw wilt aanvragen die u in het verleden hebt aangevraagd, kunt u een oude aanvraag van de [!UICONTROL Request Manager] indien nodig.

Meer informatie over [!DNL Data Warehouse], zie de volgende koppelingen in de [!DNL Analytics] Help-documentatie:

* [Een Data Warehouse-aanvraag maken](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Aanbevolen werkwijzen voor Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)

## Telmethode {#concept_EC19BC897D66411BABAF2FA27BCE89AA}

U kunt ervoor kiezen om rapporten te bekijken met verschillende telmethoden om te begrijpen hoe uw activiteiten van invloed zijn op uw gebruikers gedurende hun levensduur of tijdens één sessie.

De telmethode wordt ondersteund voor de volgende soorten activiteiten:

* A/B-test

   Bij wijze van uitzondering ondersteunen Auto-Target A/B-activiteiten alleen de standaardmethode voor het tellen van bezoekers.

* Gericht op ervaring (XT)
* MVT (Multivariate Test)

   Voor het MVT Element Contribution Report ondersteunt Target geen Activity Impressions voor de Metrische types van Ontvangsten.

* Recommendations

Momenteel wordt alleen de standaardtelmethode (Visits) ondersteund voor Automated Personalization-activiteiten (AP).

U kunt rapporten weergeven met de volgende telmethoden:

* **Bezoeker:** Een unieke deelnemer aan de activiteit, gedurende de levensduur van de activiteit.

   Een persoon wordt als nieuwe gegadigde beschouwd als hij of zij de site bezoekt vanuit een nieuwe computer of een nieuwe browser; verwijdert het cookie; of converteert en retourneert de activiteit met dezelfde cookie. Een deelnemer wordt door de PCID geïdentificeerd in het cookie van de bezoeker. Als de PCID verandert, wordt de persoon beschouwd als een nieuwe bezoeker.

* **Bezoek:** Een unieke deelnemer aan een ervaring tijdens een enkele browsersessie van 30 minuten.

   Als een conversie is bereikt of een bezoeker na minimaal 30 minuten weer naar de site terugkeert, telt een terugkerende bezoeker als een nieuw bezoek. Een bezoek wordt vastgesteld door de `sessionID` in het cookie van de bezoeker. Wanneer de `sessionID` wijzigingen , wordt het bezoek als nieuw beschouwd .

* **Afdruk-/paginaweergave:** Telkens wanneer een bezoeker een pagina van de activiteit laadt.

   Eén bezoek kan verschillende indrukken van bijvoorbeeld uw homepage bevatten.

>[!NOTE]
>
>Meestal worden tellingen bepaald door cookies en sessieactiviteit. Als u echter het laatste conversiepunt van een activiteit bereikt en vervolgens de activiteit weer betreedt, wordt u beschouwd als een nieuwe deelnemer en een nieuw bezoek aan de activiteit. Dit geldt ook voor PCID&#39;s en `sessionID` waarden veranderen niet.

## Waarom doet [!DNL Target] het gebruik van de t-tests van Welch aanbevelen? {#t-test}

A/B-tests zijn experimenten om de gemiddelde waarde van bepaalde metrische bedrijfswaarden in een besturingsvariant (ook wel een ervaring genoemd) te vergelijken met de gemiddelde waarde van die metrische waarde in een of meer alternatieve ervaringen.

[!DNL Target] raadt u aan [T-test van Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test), aangezien deze minder veronderstellingen vereisen dan alternatieven zoals z-tests, en de geschikte statistische test zijn voor het uitvoeren van paarsgewijze vergelijkingen van (kwantitatieve) bedrijfsmetriek tussen een controleervaring en alternatieve ervaringen.

### Meer details

Wanneer het runnen van online A/B tests, wordt elke gebruiker/bezoeker willekeurig toegewezen aan één enkele variant. Vervolgens meten we de maatstaven(s) van de betrokken ondernemingen (bijv. omzettingen, orders, inkomsten, enz.) voor bezoekers in elke variant. De statistische test die we vervolgens gebruiken, test de hypothese dat de gemiddelde maatstaf van het bedrijfsleven (bv. omrekeningskoers, orders per gebruiker, inkomsten per gebruiker, enz.) gelijk is voor het bedieningsorgaan en een bepaalde alternatieve variant.

Hoewel de bedrijfsmetrische waarde zelf volgens één of andere willekeurige distributie zou kunnen worden verdeeld, zou de distributie van het gemiddelde van dit metrisch (binnen elke variant) in een normale distributie via moeten samenkomen [Centrale limiet](https://en.wikipedia.org/wiki/Central_limit_theorem). Hoewel er geen garantie is voor de snelheid waarmee deze bemonsteringsspreiding van het gemiddelde zal converteren naar normaal, wordt deze voorwaarde doorgaans bereikt gezien de omvang van de bezoekers bij online testen.

Gezien deze normaliteit van het gemiddelde kan worden aangetoond dat de te gebruiken teststatistiek een t-verdeling volgt, omdat het de verhouding is tussen een normaal verdeelde waarde (het verschil in gemiddelden) en een schaaltermijn op basis van een schatting op basis van de gegevens (de standaardfout van het verschil in gemiddelden). De **t-test** Vervolgens wordt de juiste hypothesetest uitgevoerd, aangezien de teststatistiek een t-verdeling volgt.

### Waarom geen andere tests worden gebruikt

A **z-test** technisch niet geschikt is omdat in het typische A/B-testscenario de noemer van de teststatistiek geen afgeleid product is van een bekende variantie en in plaats daarvan moet worden geschat op basis van de gegevens. Voor grote monsters zijn de z-test en de t-test echter identiek.

**Chi-kwadraat testen** niet worden gebruikt omdat deze geschikt zijn om te bepalen of er een kwalitatieve relatie bestaat tussen twee varianten (d.w.z. een nulhypothese dat er geen verschil is tussen varianten). T-tests zijn geschikter voor het scenario van _kwantitatief_ het vergelijken van metriek.

De **Mann-Whitney U test** is een niet-parametrische test, die geschikt is wanneer de bemonsteringsverdeling van de gemiddelde metrische waarde van het bedrijf (voor elke variant) normaal niet wordt verdeeld. Nochtans zoals eerder besproken, gezien de omvang van verkeer betrokken bij online het testen, typisch de Centrale Grenswaarden van Theorem van toepassing, en zodat kan t-test veilig worden toegepast.

Complexere methoden zoals **ANOVA** (waarbij t-tests tot meer dan twee varianten worden veralgemeend) kan worden toegepast wanneer een test meer dan twee ervaringen heeft (&quot;A/Bn-tests&quot;). ANOVA beantwoordt echter de vraag of alle varianten hetzelfde gemiddelde hebben, terwijl we bij de typische A/Bn-test meer geïnteresseerd zijn in _specifieke variant_ is het beste. In [!DNL Target]Daarom passen we regelmatig t-tests toe waarbij elke variant op een controle wordt vergeleken, met een Bonferroni-correctie om rekening te houden met meerdere vergelijkingen.