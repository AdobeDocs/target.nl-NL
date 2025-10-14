---
keywords: geautomatiseerde verkeerstoewijzing;het richten;het Telling van de verhoging en houdt Gebruiker in Activiteit;verkeerstoewijzing;auto-toewijst;auto toewijzen
description: Leer hoe te om een [!UICONTROL Auto-Allocate] activiteit in  [!DNL Adobe Target]  te gebruiken die een winnaar onder twee of meer ervaringen identificeert en automatisch meer verkeer aan de winnaar opnieuw toewijst.
title: Wat is een [!UICONTROL Auto-Allocate] activiteit?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
source-git-commit: 1b1b2271738d12f8da4e695900b70e280f50d8cf
workflow-type: tm+mt
source-wordcount: '3502'
ht-degree: 0%

---

# [!UICONTROL Auto-Allocate] overzicht

Een [!UICONTROL Auto-Allocate] -activiteit in [!DNL Adobe Target] identificeert een winnaar onder twee of meer ervaringen en wijst automatisch meer verkeer toe aan de winnaar om de conversie te verhogen terwijl de test doorgaat en leert.

Terwijl [&#x200B; creërend een activiteit A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) gebruikend het driestappe geleide werkschema, kies de **[!UICONTROL Auto-Allocate to best experience]** optie op de **[!UICONTROL Targeting]** pagina (stap 2).

## De uitdaging {#section_85D5A03637204BACA75E19646162ACFF}

Standaard A/B-tests hebben inherente kosten. U moet verkeer uitgeven om prestaties van elke ervaring te meten en door analyse de het winnen ervaring te berekenen. De verdeling van het verkeer blijft vast zelfs nadat u erkent dat sommige ervaringen anderen overtreffen. Bovendien is het ingewikkeld om de steekproefgrootte te bepalen, en de activiteit moet zijn volledige cursus in werking stellen alvorens u op een winnaar kunt handelen. En er is nog steeds een kans dat de geïdentificeerde winnaar geen echte winnaar is.

## De oplossing: [!UICONTROL Auto-Allocate] {#section_98388996F0584E15BF3A99C57EEB7629}

Een [!UICONTROL Auto-Allocate] -activiteit verlaagt deze kosten en overheadkosten voor het bepalen van een winnende ervaring. [!UICONTROL Auto-Allocate] bewaakt de beoogde metrische prestaties van alle ervaringen en stuurt meer nieuwkomers proportioneel naar de hoogwaardige ervaringen. Voldoende verkeer is gereserveerd om de andere ervaringen te onderzoeken. U kunt de voordelen van de test op uw resultaten zien, zelfs terwijl de activiteit nog loopt: optimalisatie komt parallel met leren voor.

Met [!UICONTROL Auto-Allocate] krijgen bezoekers geleidelijk de overstap naar het winnen van ervaringen, in plaats van dat u wacht tot een activiteit eindigt om de winnaar te bepalen. U profiteert sneller van een lift omdat deelnemers aan activiteiten die naar minder succesvolle ervaringen zouden zijn gestuurd, potentiële winnende ervaringen kunnen laten zien.

Bij een normale A/B-test in [!DNL Target] worden alleen paarsgewijze vergelijkingen van klaplopers met het besturingselement getoond. Als een activiteit bijvoorbeeld ervaringen heeft: A, B, C en D waarbij A het besturingselement is, zou een normale [!DNL Target] A/B test A versus B, A versus C en A versus D vergelijken.

In dergelijke tests, gebruiken de meeste producten, met inbegrip van [!DNL Target], t-test van a [&#x200B; Welch &#x200B;](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} om op p-waarde gebaseerd vertrouwen te produceren. Deze betrouwbaarheidswaarde wordt vervolgens gebruikt om te bepalen of de toerist voldoende van de controle verschilt. [!DNL Target] voert echter niet automatisch de impliciete vergelijkingen uit (B versus C, B versus D, en C versus D) die nodig zijn om de &quot;beste&quot; ervaring te vinden. Het resultaat is dat de markeerstift de resultaten handmatig moet analyseren om de &quot;beste&quot; ervaring te bepalen.

[!UICONTROL Auto-Allocate] voert alle impliciete vergelijkingen uit over ervaringen en produceert een &quot;ware&quot;winnaar. Er bestaat geen begrip van een &quot;controle&quot;ervaring in de test.

[!UICONTROL Auto-Allocate] wijst nieuwe bezoekers intelligent aan ervaringen toe tot het betrouwbaarheidsinterval van de beste ervaring niet met het betrouwbaarheidsinterval van een andere ervaring overlapt. Normaal zou dit proces valse positieven kunnen veroorzaken, maar [!UICONTROL Auto-Allocate] gebruikt betrouwbaarheidsintervallen die op [&#x200B; worden gebaseerd Bernstein Ongelijkheid &#x200B;](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29){target=_blank} die voor herhaalde evaluaties compenseert. Op dit moment is er een echte winnaar. Wanneer [!UICONTROL Auto-Allocate] stopt, op voorwaarde dat de bezoekers die op de pagina aankomen niet in aanzienlijke mate afhankelijk zijn van de tijd, is er ten minste een kans van 95% dat [!UICONTROL Auto-Allocate] een ervaring retourneert waarvan de werkelijke respons niet minder is dan 1% (relatief) dan de werkelijke respons van de winnende ervaring.

## Wanneer moet u [!UICONTROL Auto-Allocate] versus [!UICONTROL A/B Test] - of [!UICONTROL Automated Personalization] -activiteiten gebruiken? {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Gebruik **[!UICONTROL Auto-Allocate]** als u uw activiteit vanaf het begin wilt optimaliseren en de winnende ervaringen zo snel mogelijk wilt identificeren. Doordat de prestaties van de activiteit in het algemeen vaker worden benut, worden de prestaties van de activiteit verhoogd.
* Gebruik een standaard **[Test A/B](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** wanneer u de prestaties van alle ervaringen wilt karakteriseren alvorens uw plaats te optimaliseren. Met een A/B-test kunt u al uw ervaringen rangschikken, terwijl met [!UICONTROL Auto-Allocate] topuitvoerders worden gevonden, maar geen onderscheid tussen de lagere uitvoerders wordt gegarandeerd.
* Het gebruik [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) wanneer u optimaliseringsalgoritmen van de hoogste ingewikkeldheid, zoals machine-leert modellen wilt die voorspellingen bouwen die op individuele profielattributen worden gebaseerd. [!UICONTROL Auto-Allocate] bekijkt het totale gedrag van ervaringen (net als standaard A/B tests), en maakt geen onderscheid tussen bezoekers.

## Belangrijkste voordelen van [!UICONTROL Auto-Allocate] {#section_0913BF06F73C4794862561388BBDDFF0}

* Behoudt de strengheid van een A/B-test
* Vindt een statistisch significante winnaar sneller dan een handmatige A/B test
* Biedt een hogere gemiddelde campagnelift dan een handmatige A/B-test

## Terminologie {#section_670F8785BA894745B43B6D4BFF953188}

De volgende termen zijn handig wanneer u [!UICONTROL Auto-Allocate] bespreekt:

**Meervoudig-gewapende bandit:** a [&#x200B; multi-gewapende bandit &#x200B;](https://en.wikipedia.org/wiki/Multi-armed_bandit){target=_blank} benadering van optimalisatiebalansen exploratief leren en exploitatie van dat leren.

## Hoe het algoritme werkt {#section_ADB69A1C7352462D98849F2918D4FF7B}

In de algemene logica achter [!UICONTROL Auto-Allocate] zijn zowel gemeten prestaties (zoals de conversiesnelheid) als betrouwbaarheidsintervallen van de cumulatieve gegevens opgenomen. In tegenstelling tot een standaard A/B test waarbij het verkeer gelijkmatig over ervaringen wordt verdeeld, verandert [!UICONTROL Auto-Allocate] verkeerstoewijzing over ervaringen.

* 80 % van de bezoekers wordt toegewezen op basis van de hieronder beschreven intelligente logica .
* 20% van de bezoekers wordt willekeurig toegewezen in alle ervaringen om zich aan te passen aan het veranderende gedrag van de bezoeker.

De multi-gewapende bandibenadering houdt sommige ervaringen vrij voor onderzoek terwijl het exploiteren van de ervaringen die goed presteren. Meer nieuwe bezoekers worden geplaatst in beter presterende ervaringen terwijl het vermogen behouden om op veranderende omstandigheden te reageren. Deze modellen worden minstens eenmaal per uur bijgewerkt om ervoor te zorgen dat het model reageert op de meest recente gegevens.

Naarmate meer bezoekers de activiteit betreden, worden sommige ervaringen succesvoller en wordt meer verkeer verzonden naar de succesvolle ervaringen. 20% van het verkeer blijft willekeurig worden bediend om alle ervaringen te onderzoeken. Als één van de minder presterende ervaringen begint beter te presteren, wordt meer verkeer toegewezen aan die ervaring. Of als het succes van een meer presterende activiteit vermindert, wordt minder verkeer toegewezen aan die ervaring. Als bezoekers bijvoorbeeld naar andere informatie op uw mediasite zoeken tijdens een gebeurtenis, levert de weekendverkoop op uw detailhandelssite andere resultaten op.

In de volgende afbeelding ziet u hoe het algoritme tijdens een test met vier ervaringen kan worden uitgevoerd (klik om de illustratie uit te vouwen):

![&#x200B; auto-wijs beeld &#x200B;](assets/auto-allocate.png){width="600" zoomable="yes"} toe

De illustratie toont hoe het verkeer dat aan elke ervaring wordt toegewezen zich over verscheidene ronden van het activiteitenleven ontwikkelt tot een duidelijke winnaar wordt bepaald.

| Rond | Beschrijving |
|--- |--- |
| ![&#x200B; Warm-omhoog rond &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png){width="200" zoomable="yes"} | **Warm-omhoog Rond (0)**: Tijdens opwarmen rond, krijgt elke ervaring gelijke verkeerstoewijzing tot elke ervaring in de activiteit een minimum van 1.000 bezoekers en 50 omzettingen heeft.<ul><li>Ervaring A=25%</li><li>Ervaring B=25%</li><li>Ervaring C=25%</li><li>Ervaring D=25%</li></ul>Nadat elke ervaring 1.000 bezoekers en 50 omzettingen krijgt, begint [!DNL Target] geautomatiseerde verkeerstoewijzing. Alle toewijzingen vinden plaats in rondes en voor elke ronde worden twee ervaringen gekozen.<br> slechts twee ervaringen bewegen zich vooruit in de volgende ronde: D en C.<br> Bewegend betekent vooruit dat de twee ervaringen 80% van het verkeer gelijkelijk worden toegewezen. De andere twee ervaringen blijven deelnemen, maar worden slechts gebruikt als onderdeel van de 20% willekeurige verkeerstoewijzing wanneer nieuwe bezoekers de activiteit betreden.<br> Alle toewijzingen worden bijgewerkt elk uur (aangetoond door rondes langs de x-as hierboven). Na elke ronde worden de cumulatieve gegevens vergeleken. |
| ![&#x200B; rond 1 &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png){width="200" zoomable="yes"} | **Rond 1**: Tijdens deze ronde, wordt 80% van verkeer toegewezen aan ervaringen C en D (40% elk). 20% van het verkeer wordt willekeurig toegewezen aan ervaringen A, B, C, en D (elk 5%). Tijdens deze ronde presteert A goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring A om zich ook vooruit te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en A gaan verder. |
| ![&#x200B; rond 2 &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png){width="200" zoomable="yes"} | **Rond 2**: Tijdens deze ronde, wordt 80% van verkeer toegewezen aan ervaringen A en D (40% elk). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde functioneert ervaring B goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring B om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en B gaan verder. |
| ![&#x200B; rond 3 &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png){width="200" zoomable="yes"} | **Rond 3**: Tijdens deze ronde, wordt 80% van verkeer toegewezen aan ervaringen B en D (40% elk). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde blijft de ervaring D goed presteren en de ervaring C functioneert goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring C om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en C gaan verder. |
| ![&#x200B; rond 4 &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png){width="200" zoomable="yes"} | **Rond 4**: Tijdens deze ronde, wordt 80% van verkeer toegewezen aan ervaringen C en D (40% elk). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde functioneert ervaring C goed.<ul><li>Het algoritme verkiest ervaring C om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring D om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen C en D gaan verder. |
| ![&#x200B; rond n &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png){width="200" zoomable="yes"} | **Rond *n***: Aangezien de activiteit vordert, begint een hoog-presterende ervaring te verschijnen en het proces gaat verder tot er een het winnen ervaring is. Als het betrouwbaarheidsinterval van de ervaring met de hoogste conversiesnelheid niet overlapt met het betrouwbaarheidsinterval van een andere ervaring, wordt dit aangeduid als de winnaar. A [&#x200B; badge toont op de winnende pagina van activiteit &#x200B;](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) en in de [!UICONTROL Activity] lijst.<ul><li>Het algoritme kiest ervaring C als duidelijke winnaar.</li></ul>Op dit punt dient het algoritme 80% van het verkeer om C te ervaren, terwijl 20% van het verkeer willekeurig aan alle ervaringen (A, B, C, en D) wordt gediend. In totaal krijgt C 85% van het verkeer. In het onwaarschijnlijke geval dat het betrouwbaarheidsinterval van de winnaar opnieuw begint te overlappen, keert het algoritme terug naar het gedrag van ronde 4 hierboven.<P>**Belangrijk**: Als u manueel een winnaar vroeger in het proces koos, zou het gemakkelijk zijn geweest om de verkeerde ervaring te kiezen. Daarom is het aan te raden te wachten totdat het algoritme de winnende ervaring bepaalt. |

>[!NOTE]
>
>Als een activiteit slechts twee ervaringen heeft, krijgen beide ervaringen gelijk verkeer tot [!DNL Target] een het winnen ervaring met 75% vertrouwen vindt. Op dat moment wordt tweederde van het verkeer toegewezen aan de winnaar, en eenderde aan de verliezer. Als een ervaring 95% betrouwbaarheid bereikt, wordt 90% van het verkeer aan de winnaar toegewezen en wordt 10% aan de verliezer toegewezen. [!DNL Target] verzendt altijd wat verkeer naar de &quot;het verliezen&quot;ervaring om valse positieven in het eind te vermijden (namelijk om wat exploratie te handhaven).

Nadat een [!UICONTROL Auto-Allocate] activiteit wordt geactiveerd, krijgen de volgende verrichtingen van Tar  UI niet toegestaan:

* De modus &quot;Verkeerstoewijzing&quot; omzetten in &quot;Handmatig&quot;
* Het metrische type van het doel wijzigen
* Opties wijzigen in het deelvenster [!UICONTROL Advanced Settings]

## Controleren hoe Automatisch toewijzen werkt

Voor meer informatie, zie [&#x200B; auto-toewijst kan u snellere testresultaten en hogere opbrengst dan een handtest &#x200B;](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md) geven.

## Caveats {#section_5C83F89F85C14FD181930AA420435E1D}

Houd rekening met de volgende informatie wanneer u met [!UICONTROL Auto-Allocate] werkt:

### De functie [!UICONTROL Auto-Allocate] werkt met slechts één geavanceerde metrische instelling: [!UICONTROL Increment Count and Keep User in Activity]

De volgende geavanceerde metrische instellingen worden niet ondersteund: [!UICONTROL Increment Count] , [!UICONTROL Release User] , [!UICONTROL Allow Reentry and Increment Count] en [!UICONTROL Release User and Bar from Reentry] .

### De frequente terugkeerbezoekers kunnen ervaring omzettingspercentages opblazen.

Als een bezoeker die A ziet vaak terugkeert en verscheidene keren omzet, wordt het Tarief van de Omzetting (CR) van ervaring A kunstmatig verhoogd. Vergelijk dit resultaat met B, waar bezoekers wel converteren maar niet vaak terugkeren. Als gevolg hiervan ziet de CR van ervaring A er beter uit dan de CR van ervaring B, zodat nieuwe bezoekers eerder aan A zullen worden toegewezen dan aan B. Als u ervoor kiest om één keer per toetreder te tellen, kan de CR van A en CR van B identiek zijn.

Als retourbezoekers willekeurig worden verdeeld, is het waarschijnlijker dat hun effect op de omrekeningskoersen wordt gelijkgetrokken. Om dit effect te verlichten, denk na veranderend de tellende methode van doel metrisch om slechts eenmaal per ingang te tellen.

### Verschillen tussen hoogpresteerders, niet tussen slechtpresterende.

[!UICONTROL Auto-Allocate] is goed in het onderscheiden tussen krachtige ervaringen (en het vinden van een winnaar). Er kunnen momenten zijn dat je niet genoeg onderscheid hebt tussen de ondermaatse ervaringen.

Als u statistisch significante differentiatie tussen alle ervaringen wilt veroorzaken, zou u kunnen willen overwegen gebruikend de handwijze van de verkeerstoewijzing.

### Conversietarieven die zijn gecorreleerd aan de tijd (of contextueel variëren), kunnen de toewijzingsbedragen scheeftrekken.

Sommige factoren die tijdens een standaard A/B-test kunnen worden genegeerd omdat ze alle ervaringen evenveel beïnvloeden, kunnen niet worden genegeerd in een [!UICONTROL Auto-Allocate] -activiteit. Het algoritme is gevoelig voor de waargenomen omrekeningskoersen.

Hier volgen voorbeelden van factoren die de prestaties op verschillende manieren kunnen beïnvloeden:

* Ervaringen met verschillende contextuele (tijd, locatie, geslacht, enzovoort) relevantie.

  Bijvoorbeeld:

   * &quot;God zij dank is het vrijdag&quot;resulteert in hogere omzettingen op Vrijdag.
   * &quot;Springen en starten op uw maandag&quot; heeft een hogere conversie op maandag.
   * &quot;Opruimen voor een winter voor de oostkust&quot; zorgt voor een hogere ombouw in door de oostkust of de winter getroffen gebieden.

  Het gebruik van ervaringen met verschillende contextuele relevanties kan de resultaten in een [!UICONTROL Auto-Allocate] -test meer scheeftrekken dan in een A/B-test, omdat de A/B-test de resultaten over een langere periode analyseert.

* Ervaringen met uiteenlopende vertragingen bij de conversie, mogelijk als gevolg van de urgentie van de boodschap.

  &quot;30% verkoop eindigt vandaag de dag&quot; geeft de bezoeker bijvoorbeeld de boodschap om te zetten, maar &quot;50% korting op eerste aankoop&quot; geeft niet hetzelfde gevoel van urgentie.

## Veelgestelde vragen {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u met [!UICONTROL Auto-Allocate] -activiteiten werkt:

### Biedt [!UICONTROL Analytics for Target] (A4T) ondersteuning voor [!UICONTROL Auto-Allocate] -activiteiten?

Ja. Voor meer informatie, zie [&#x200B; steun A4T voor auto-Wijs en auto-Doel activiteiten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) toe.

### Worden de terugkerende bezoekers automatisch opnieuw toegewezen aan hoog presterende ervaringen?

Nee. Alleen nieuwe bezoekers worden automatisch toegewezen. Terugkerende bezoekers blijven hun oorspronkelijke ervaring zien om de geldigheid van de A/B-test te beschermen.

### Hoe behandelt het algoritme valse positieven?

Het algoritme garandeert een betrouwbaarheid van 95% of een percentage van 5% ten onrechte als u wacht tot de winnaar-badge wordt weergegeven.

### Wanneer begint [!UICONTROL Auto-Allocate] verkeer toe te wijzen?

Het algoritme begint te werken nadat alle ervaringen in de activiteit minimaal 1000 bezoekers en 50 conversies hebben.

### Hoe agressief benut het algoritme?

80% van het verkeer wordt gediend gebruikend [!UICONTROL Auto-Allocate] en 20% van verkeer wordt willekeurig gediend. Wanneer een winnaar is geïdentificeerd, gaat 80% van het verkeer naar het, terwijl alle ervaringen wat verkeer als deel van de 20%, met inbegrip van de winnende ervaring blijven krijgen.

### Worden er al ervaringen verloren?

Ja. De multigewapende bandit zorgt ervoor dat minstens 20% van het verkeer wordt gereserveerd om veranderende patronen of omzettingspercentages over alle ervaringen te onderzoeken.

### Wat gebeurt er met activiteiten met lange omzettingsvertragingen?

Zolang alle ervaringen die worden geoptimaliseerd vergelijkbare vertragingen hebben, is het gedrag hetzelfde als een activiteit met een snellere conversiecyclus. Nochtans, duurt het langer om de 50 omzettingsdrempel te bereiken alvorens het proces van de verkeerstoewijzing begint.

### Hoe verschilt [!UICONTROL Auto-Allocate] van [!UICONTROL Automated Personalization] ?

[!UICONTROL Automated Personalization] gebruikt de profielkenmerken van elke bezoeker om de beste ervaring te bepalen. Hierdoor wordt niet alleen de activiteit geoptimaliseerd, maar wordt ook de activiteit voor die gebruiker aangepast.

[!UICONTROL Auto-Allocate] daarentegen is een A/B-test die een gezamenlijke winnaar oplevert (de meest populaire ervaring, maar niet noodzakelijkerwijs de meest effectieve ervaring voor elke bezoeker).

### Worden de terugkerende bezoekers de omzettingspercentage op mijn succes metrisch?

Op dit moment bevoordeelt de logica bezoekers die snel converteren of vaker bezoeken, omdat dergelijke bezoekers tijdelijk de algemene conversiesnelheid verhogen van de ervaring waartoe zij behoren. Het algoritme past zich regelmatig aan, zodat wordt de verhoging van omzettingspercentage versterkt bij elke momentopname. Als de site talloze retouradres krijgt, kan de conversie van deze sites de algemene conversiekoers verhogen voor de ervaring waartoe ze behoren. Er is een goede kans dat retourbezoekers willekeurig worden verdeeld, waardoor het totale effect (verhoogde lift) gelijkmatig wordt verdeeld. Om dit effect te verzachten, kunt u de telmethode van de succesmetrische methode zo wijzigen dat deze slechts eenmaal per entry wordt geteld.

### Kan ik de voorbeeldgroottecalculator gebruiken om te schatten hoe lang de activiteit duurt om de winnaar te identificeren wanneer ik [!UICONTROL Auto-Allocate] gebruik?

U kunt de bestaande [!DNL Adobe Target] [&#x200B; calculator van de Grootte van de Steekproef &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6) gebruiken om een schatting van te krijgen hoe lang de test loopt. (Zoals bij traditionele A/B-tests kunt u Bonferroni-correctie toepassen als u meer dan twee aanbiedingen of meer dan één omzettingsmeting/hypothese test.) Deze rekenmachine is ontworpen voor traditionele A/B-tests met een vaste tijdshorizon en biedt alleen een schatting. Het gebruik van de rekenmachine voor een [!UICONTROL Auto-Allocate] -activiteit is optioneel omdat [!UICONTROL Auto-Allocate] een winnaar voor u declareert. U hoeft geen vast punt in de tijd te kiezen om de testresultaten te bekijken. De opgegeven waarden zijn altijd statistisch geldig.

Interne [!DNL Adobe] experimenten hebben het volgende gevonden:

* Wanneer u precies twee ervaringen test, wordt in [!UICONTROL Auto-Allocate] sneller een winnaar gevonden dan tijdens een vaste periode getest (dat wil zeggen, het tijdframe dat wordt voorgesteld door de voorbeeldgroottecalculator) wanneer het prestatieverschil tussen ervaringen groot is. Het kan echter zijn dat [!UICONTROL Auto-Allocate] extra tijd nodig heeft om een winnaar te identificeren wanneer het prestatieverschil tussen ervaringen klein is. In deze gevallen zouden de vastrentende tests doorgaans zijn geëindigd zonder een statistisch significant resultaat.
* Bij het testen van meer dan twee ervaringen, vindt [!UICONTROL Auto-Allocate] een winnaar sneller dan het testen met een vaste tijdshorizon (dat wil zeggen, het tijdkader dat wordt voorgesteld door de voorbeeldgroottecalculator) wanneer één ervaring alle andere ervaringen sterk overtreft. Wanneer twee of meer ervaringen beide &#39;winnen&#39; zijn in vergelijking met andere ervaringen, maar veel op elkaar zijn afgestemd, kan [!UICONTROL Auto-Allocate] extra tijd nodig hebben om te bepalen wat beter is. In deze gevallen zouden de tests met een vaste looptijd doorgaans zijn geëindigd door te concluderen dat de &quot;winnende&quot; ervaringen beter waren dan de minder presterende ervaringen, maar niet hebben vastgesteld welke beter was.

### Moet ik een ondermaatse ervaring uit een [!UICONTROL Auto-Allocate] -activiteit verwijderen om het proces voor het bepalen van een winnaar te versnellen?

Er is echt geen reden om een ondermaatse ervaring te verwijderen. [!UICONTROL Auto-Allocate] bedient automatisch high-performance ervaringen vaker en werkt minder vaak aan ondermaatse ervaringen. Een ondermaatse ervaring in de activiteit heeft geen significante invloed op de snelheid om een winnaar te bepalen.

20% van de bezoekers wordt willekeurig toegewezen in alle ervaringen. De hoeveelheid verkeer die aan een ondermaatse ervaring wordt besteed, is minimaal (20% gedeeld door het aantal ervaringen).

### Kan ik het doel metrisch halverwege door een [!UICONTROL Auto-Allocate] activiteit veranderen? {#change-metric}

[!DNL Adobe] adviseert niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. [!DNL Adobe] garandeert niet wat er gebeurt als u het doel metrisch wijzigt in een activiteit nadat deze is uitgevoerd.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate] -, [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -activiteiten die [!DNL Target] - of [!DNL Analytics] (A4T) gebruiken als rapportagebron.

### Kan ik de rapportbron halverwege een [!UICONTROL Auto-Allocate] activiteit veranderen? {#change-reporting}

[!DNL Adobe] adviseert niet dat u de rapporteringsbron halverwege een activiteit verandert. Hoewel het mogelijk is om de rapportbron te wijzigen (van [!DNL Target] in A4T of op de tegenovergestelde manier) tijdens een activiteit met de [!DNL Target] -gebruikersinterface, moet u altijd een nieuwe activiteit starten. [!DNL Adobe] garandeert niet wat er gebeurt als u de rapportbron wijzigt in een activiteit nadat deze is uitgevoerd.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate] -, [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -activiteiten die [!DNL Target] - of [!DNL Analytics] (A4T) gebruiken als rapportagebron.

### Kan ik de optie [!UICONTROL Reset Report Data] gebruiken tijdens het uitvoeren van een [!UICONTROL Auto-Allocate] -activiteit?

Het gebruik van de optie [!UICONTROL Reset Report Data] voor [!UICONTROL Auto-Allocate] -activiteiten wordt niet aanbevolen. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords uit het [!UICONTROL Auto-Allocate] -model verwijderd. In plaats van de optie [!UICONTROL Reset Report Data] te gebruiken voor [!UICONTROL Auto-Allocate] -activiteiten, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit. (Deze handleiding is ook van toepassing op [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -activiteiten.)

### Hoe bouwt [!UICONTROL Auto-Allocate] modellen met betrekking tot milieu&#39;s?

[!UICONTROL Auto-Allocate] bouwt modellen die op het verkeer en omzettingsgedrag worden gebaseerd dat in het standaardmilieu slechts wordt geregistreerd. Door gebrek, [!UICONTROL Production] is het standaardmilieu, maar het standaardmilieu kan in [!DNL Target] worden veranderd ([&#x200B; Beleid > Milieu&#39;s &#x200B;](/help/main/administrating-target/environments.md)).

Als een treffer in een andere (niet gebrek) milieu voorkomt, wordt het verkeer verdeeld volgens het waargenomen omzettingsgedrag in het standaardmilieu. Het resultaat van die hit (conversie of niet-conversie) wordt opgenomen voor rapportagedoeleinden, maar wordt niet in het [!UICONTROL Auto-Allocate] -model meegenomen.

Wanneer het selecteren van een ander milieu, toont het rapport verkeer en omzettingen voor dat milieu. De standaard geselecteerde omgeving voor een rapport is de standaard voor de gehele account die is geselecteerd. De standaardomgeving kan niet per activiteit worden ingesteld.

### Kan een [!UICONTROL Auto-Allocate] activiteit het raadplegingsvenster tijdens een test aanpassen om veranderende tendensen in tijd te overwegen?

Bijvoorbeeld, kan de activiteit de maand van December voor het beslissen over hoe te om verkeer toe te wijzen, eerder dan het bekijken van de gegevens van de bezoeker van September (toen de test begon) overwegen?

Nr, [!UICONTROL Auto-Allocate] overweegt prestaties van de volledige activiteit.

### Geeft [!UICONTROL Auto-Allocate] een winnende ervaring weer voor een terugkerende bezoeker als de winnende ervaring verschilt van wat de bezoeker zag toen hij in aanmerking kwam voor de activiteit?

[!UICONTROL Auto-Allocate] maakt gebruik van kleverige beslissingen om dezelfde redenen dat [!UICONTROL A/B Test] -activiteiten plakken. De verkeerstoewijzing werkt alleen voor nieuwe bezoekers.

## Trainingsvideo&#39;s {#section_893E5B36DC4A415C9B1D287F51FCCB83}

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Het Werkschema van de activiteit - het richten (2 :14) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video omvat informatie over vestiging verkeerstoewijzing.

* Een publiek toewijzen aan uw activiteit
* Verkeer omhoog of omlaag duwen
* Selecteer uw methode voor verkeerstoewijzing
* Verkeer toewijzen tussen verschillende ervaringen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Creërend A/B Tests (8 :36) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de driestapige workflow met instructies voor het doel. [!UICONTROL Auto-Allocate] wordt besproken beginnend bij 4 :45.

* Een A/B-activiteit maken in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
