---
keywords: geautomatiseerde verkeerstoewijzing;het richten;het Telling van de verhoging en houdt Gebruiker in Activiteit;verkeerstoewijzing;auto-toewijst;auto toewijzen
description: Leer hoe u een activiteit Automatisch toewijzen in Adobe gebruikt [!DNL Target] die een winnaar onder twee of meer ervaringen identificeert en automatisch meer verkeer aan de winnaar toewijst.
title: Wat is een automatisch toegewezen activiteit?
feature: Auto-Allocate
exl-id: 2d1ddd71-2ca6-4f00-9d0c-eb25ede8fdb8
source-git-commit: 393ab5b9e2b8fbdf0dcee0640775c73bf6899afe
workflow-type: tm+mt
source-wordcount: '3447'
ht-degree: 0%

---

# [!UICONTROL Auto-Allocate] overzicht

An [!UICONTROL Auto-Allocate] activiteit in [!DNL Adobe Target] identificeert een winnaar onder twee of meer ervaringen en wijst automatisch meer verkeer aan de winnaar toe om omzettingen te verhogen terwijl de test blijft lopen en leren.

Tijdens het maken van een A/B-activiteit met behulp van de driestappe geleide workflow kunt u de optie [!UICONTROL Auto-Allocate to best experience] optie.

## De uitdaging {#section_85D5A03637204BACA75E19646162ACFF}

Standaard A/B-tests hebben inherente kosten. U moet verkeer uitgeven om prestaties van elke ervaring te meten en door analyse de het winnen ervaring te berekenen. De verdeling van het verkeer blijft vast zelfs nadat u erkent dat sommige ervaringen anderen overtreffen. Bovendien is het ingewikkeld om de steekproefgrootte te bepalen, en de activiteit moet zijn volledige cursus in werking stellen alvorens u op een winnaar kunt handelen. En er is nog steeds een kans dat de geïdentificeerde winnaar geen echte winnaar is.

## De oplossing: [!UICONTROL Auto-Allocate] {#section_98388996F0584E15BF3A99C57EEB7629}

[!UICONTROL Auto-Allocate] vermindert deze kosten en overheadkosten van het bepalen van een het winnen ervaring. [!UICONTROL Auto-Allocate] bewaakt de beoogde metrische prestaties van alle ervaringen en stuurt meer nieuwkomers proportioneel naar de hoogwaardige ervaringen. Voldoende verkeer is gereserveerd om de andere ervaringen te onderzoeken. U kunt de voordelen van de test op uw resultaten zien, zelfs terwijl de activiteit nog loopt: optimalisatie vindt plaats in combinatie met leren .

[!UICONTROL Auto-Allocate] bezoekers gaan geleidelijk aan de winnende ervaringen op in plaats van te vereisen dat u wacht tot een activiteit eindigt om een winnaar te bepalen. U profiteert sneller van een lift omdat deelnemers aan activiteiten die naar minder succesvolle ervaringen zouden zijn gestuurd, potentiële winnende ervaringen kunnen laten zien.

Een normale A/B-test in [!DNL Target] toont alleen paarsgewijze vergelijkingen van challengers met controle. Als een activiteit bijvoorbeeld ervaringen heeft: A, B, C en D, waarbij A het besturingselement is, een normaal [!DNL Target] A/B test zou A versus B, A versus C, en A versus D vergelijken.

Bij dergelijke tests worden de meeste producten, waaronder [!DNL Target], gebruik de t-test van een student om op p-waarde gebaseerd vertrouwen te produceren. Deze betrouwbaarheidswaarde wordt vervolgens gebruikt om te bepalen of de toerist voldoende van de controle verschilt. Maar [!DNL Target] voert niet automatisch de impliciete vergelijkingen (B tegen C, B tegen D, en C tegen D) uit die worden vereist om de &quot;beste&quot;ervaring te vinden. Het resultaat is dat de markeerstift de resultaten handmatig moet analyseren om de &quot;beste&quot; ervaring te bepalen.

[!UICONTROL Auto-Allocate] alle impliciete vergelijkingen tussen ervaringen worden uitgevoerd en er wordt een &#39;&#39;echte&#39;&#39; winnaar gegenereerd. Er bestaat geen begrip van een &quot;controle&quot;ervaring in de test.

[!UICONTROL Auto-Allocate] Wijst intelligent nieuwe bezoekers aan ervaringen toe tot het betrouwbaarheidsinterval van de beste ervaring niet met het betrouwbaarheidsinterval van een andere ervaring overlapt. Normaal gesproken kan dit proces leiden tot valse positieven, maar [!UICONTROL Auto-Allocate] gebruikt betrouwbaarheidsintervallen gebaseerd op de [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) dit compenseert herhaalde evaluaties. Op dit moment is er een echte winnaar. Wanneer [!UICONTROL Auto-Allocate] stopt, mits de bezoekers die op de pagina aankomen niet in aanzienlijke mate afhankelijk zijn van tijd, is er ten minste een kans dat [!UICONTROL Auto-Allocate] retourneert een ervaring waarvan de werkelijke respons niet minder is dan 1% (relatief) dan de werkelijke respons van de winnende ervaring.

## Wanneer gebruiken [!UICONTROL Auto-Allocate] versus A/B of [!UICONTROL Automated Personalization] {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Gebruiken **[!UICONTROL Auto-Allocate]** wanneer u uw activiteit vanaf het begin wilt optimaliseren en de winnende ervaringen zo snel mogelijk wilt identificeren. Doordat de prestaties van de activiteit in het algemeen vaker worden verbeterd, zijn de prestaties beter afgestemd op de prestaties.
* Een standaard gebruiken **[A/B-test](/help/main/c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)** als u de prestaties van alle ervaringen wilt karakteriseren voordat u uw site optimaliseert. Een A/B test helpt u al uw ervaringen rangschikken, terwijl [!UICONTROL Auto-Allocate] vindt topuitvoerders, maar garandeert geen onderscheid tussen de onderuitvoerders.
* Gebruiken [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) als u optimalisatiealgoritmen van de hoogste complexiteit wilt, zoals computerleermodellen die voorspellingen bouwen op basis van individuele profielkenmerken. [!UICONTROL Auto-Allocate] kijkt naar het totale gedrag van ervaringen (net als standaard A/B tests), en maakt geen onderscheid tussen bezoekers.

## Belangrijkste voordelen {#section_0913BF06F73C4794862561388BBDDFF0}

* Behoudt de strengheid van een A/B-test
* Vindt een statistisch significante winnaar sneller dan een handmatige A/B test
* Biedt een hogere gemiddelde campagnelift dan een handmatige A/B-test

## Terminologie {#section_670F8785BA894745B43B6D4BFF953188}

De volgende termen zijn handig wanneer u discussieert over [!UICONTROL Auto-Allocate]:

**Meervoudig bewapende bandit:** A [meerbewapende bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit) de optimalisatiebenadering maakt een balans op tussen verkennend leren en het benutten van dat leren.

## Hoe het algoritme werkt {#section_ADB69A1C7352462D98849F2918D4FF7B}

De algemene logica achter [!UICONTROL Auto-Allocate] omvat zowel gemeten prestaties (zoals omrekeningskoers) als betrouwbaarheidsintervallen van de cumulatieve gegevens. In tegenstelling tot een standaard A/B-test waarbij het verkeer gelijkmatig over de ervaringen wordt verdeeld, [!UICONTROL Auto-Allocate] verandert verkeerstoewijzing over ervaringen.

* 80 % van de bezoekers wordt toegewezen op basis van de hieronder beschreven intelligente logica .
* 20% van de bezoekers wordt willekeurig toegewezen in alle ervaringen om zich aan te passen aan het veranderende gedrag van bezoekers.

De multi-gewapende bandibenadering houdt sommige ervaringen vrij voor onderzoek terwijl het exploiteren van de ervaringen die goed presteren. Meer nieuwe bezoekers worden geplaatst in beter presterende ervaringen terwijl het vermogen behouden om op veranderende omstandigheden te reageren. Deze modellen worden minstens eenmaal per uur bijgewerkt om ervoor te zorgen dat het model reageert op de meest recente gegevens.

Naarmate meer bezoekers de activiteit betreden, worden sommige ervaringen succesvoller en wordt meer verkeer verzonden naar de succesvolle ervaringen. 20% van het verkeer blijft willekeurig worden bediend om alle ervaringen te onderzoeken. Als één van de minder presterende ervaringen begint beter te presteren, wordt meer verkeer toegewezen aan die ervaring. Of als het succes van een meer presterende activiteit vermindert, wordt minder verkeer toegewezen aan die ervaring. Als bezoekers bijvoorbeeld naar andere informatie op uw mediasite zoeken tijdens een gebeurtenis, levert de weekendverkoop op uw detailhandelssite andere resultaten op.

De volgende illustratie vertegenwoordigt hoe het algoritme tijdens een test met vier ervaringen zou kunnen uitvoeren:

![](assets/auto-allocate.png)

De illustratie toont hoe het verkeer dat aan elke ervaring wordt toegewezen zich over verscheidene ronden van het activiteitenleven ontwikkelt tot een duidelijke winnaar wordt bepaald.

| Rond | Beschrijving |
|--- |--- |
| ![Warm-omhoog rond](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-0.png) | **Warm-omhoog rond (0)**: Tijdens de opwarmen ronde, krijgt elke ervaring gelijke verkeerstoewijzing tot elke ervaring in de activiteit een minimum van 1.000 bezoekers en 50 omzettingen heeft.<ul><li>Ervaring A=25%</li><li>Ervaring B=25%</li><li>Ervaring C=25%</li><li>Ervaring D=25%</li></ul>Nadat elke ervaring 1.000 bezoekers en 50 omzettingen krijgt, begint Doel geautomatiseerde verkeerstoewijzing. Alle toewijzingen vinden plaats in rondes en voor elke ronde worden twee ervaringen gekozen.<br>Slechts twee ervaringen gaan verder in de volgende ronde: D en C.<br>Als we vooruit gaan, krijgen de twee ervaringen 80 procent van het verkeer gelijk toegewezen. De andere twee ervaringen blijven deelnemen, maar worden slechts gebruikt als onderdeel van de 20% willekeurige verkeerstoewijzing wanneer nieuwe bezoekers de activiteit betreden.<br>Alle toewijzingen worden elk uur bijgewerkt (weergegeven aan de hand van rondes langs de x-as hierboven). Na elke ronde worden de cumulatieve gegevens vergeleken. |
| ![Afgerond 1](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-1.png) | **Afgerond 1**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen C en D (elk 40%). 20% van het verkeer wordt willekeurig toegewezen aan ervaringen A, B, C, en D (elk 5%). Tijdens deze ronde presteert A goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring A om zich ook vooruit te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en A gaan verder. |
| ![Rond 2](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-2.png) | **Rond 2**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen A en D (elk 40%). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde functioneert ervaring B goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring B om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en B gaan verder. |
| ![Rond 3](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-3.png) | **Rond 3**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen B en D (40% elk). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde blijft de ervaring D goed presteren en de ervaring C functioneert goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring C om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en C gaan verder. |
| ![Afgerond 4](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-4.png) | **Afgerond 4**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen C en D (elk 40%). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde functioneert ervaring C goed.<ul><li>Het algoritme verkiest ervaring C om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring D om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen C en D gaan verder. |
| ![Rond n](/help/main/c-activities/automated-traffic-allocation/assets/aa-phase-n.png) | **Rond n**: Naarmate de activiteit vordert, begint een krachtige ervaring op te komen en gaat het proces door tot er een winnende ervaring is. Als het betrouwbaarheidsinterval van de ervaring met de hoogste conversiesnelheid niet overlapt met het betrouwbaarheidsinterval van een andere ervaring, wordt dit aangeduid als de winnaar. A [badge wordt weergegeven op de pagina van de winnende activiteit](/help/main/c-activities/automated-traffic-allocation/determine-winner.md) en in de [!UICONTROL Activity] lijst.<ul><li>Het algoritme kiest ervaring C als duidelijke winnaar</li></ul>Op dit punt dient het algoritme 80% van het verkeer om C te ervaren, terwijl 20% van het verkeer willekeurig aan alle ervaringen (A, B, C, en D) wordt gediend. In totaal krijgt C 85% van het verkeer. In het onwaarschijnlijke geval dat het betrouwbaarheidsinterval van de winnaar opnieuw begint te overlappen, keert het algoritme terug naar het gedrag van ronde 4 hierboven.<br>**Belangrijk**: Als u eerder tijdens het proces handmatig een winnaar koos, was het gemakkelijk geweest om de verkeerde ervaring te kiezen. Daarom is het aan te raden te wachten totdat het algoritme de winnende ervaring bepaalt. |

>[!NOTE]
>
>Als een activiteit slechts twee ervaringen heeft, krijgen beide ervaringen gelijk verkeer tot [!DNL Target] vindt een winnende ervaring met 75 % vertrouwen. Op dat moment wordt tweederde van het verkeer toegewezen aan de winnaar, en eenderde aan de verliezer. Als een ervaring 95% betrouwbaarheid bereikt, wordt 90% van het verkeer aan de winnaar toegewezen en wordt 10% aan de verliezer toegewezen. [!DNL Target] er blijft altijd wat verkeer over naar de &quot; verliezende &quot; ervaring om valse positieven te voorkomen ( d.w.z. enige exploratie te behouden ) .

Na een [!UICONTROL Auto-Allocate] activiteit wordt geactiveerd, zijn de volgende verrichtingen van UI niet toegestaan:

* De modus &quot;Verkeerstoewijzing&quot; omzetten in &quot;Handmatig&quot;
* Het metrische type van het doel wijzigen
* Opties wijzigen in het deelvenster Geavanceerde instellingen

## Controleren hoe Automatisch toewijzen werkt

Zie voor meer informatie [Automatisch toewijzen kan u snellere testresultaten en hogere opbrengsten opleveren dan een handmatige test](/help/main/c-activities/automated-traffic-allocation/faster-results-higher-revenue.md)

## Caveats {#section_5C83F89F85C14FD181930AA420435E1D}

**De [!UICONTROL Auto-Allocate] Deze functie werkt met slechts één geavanceerde metrische instelling:[!UICONTROL Increment Count and Keep User in Activity]**

De volgende geavanceerde metrische instellingen worden niet ondersteund: [!UICONTROL Increment Count], [!UICONTROL Release User], [!UICONTROL Allow Reentry and Increment Count], en [!UICONTROL Release User and Bar from Reentry].

**De frequente terugkeerbezoekers kunnen ervaring omzettingspercentages opblazen.**

Als een bezoeker die A ziet vaak terugkeert en verscheidene keren omzet, wordt het Tarief van de Omzetting (CR) van ervaring A kunstmatig verhoogd. Vergelijk dit resultaat met B, waar bezoekers zich converteren maar niet vaak terugkeren. Als gevolg hiervan ziet de CR van ervaring A er beter uit dan de CR van ervaring B, zodat nieuwe bezoekers eerder aan A zullen worden toegewezen dan aan B. Als u ervoor kiest om één keer per toetreder te tellen, kan de CR van A en CR van B identiek zijn.

Als retourbezoekers willekeurig worden verdeeld, is het waarschijnlijker dat hun effect op de omrekeningskoersen wordt gelijkgetrokken. Om dit effect te verlichten, denk na veranderend de tellende methode van doel metrisch om slechts eenmaal per ingang te tellen.

**Verschillen tussen hoogpresteerders, niet tussen slechtpresterende.**

[!UICONTROL Auto-Allocate] is goed in het differentiëren tussen hoogwaardige ervaringen (en het vinden van een winnaar). Er kunnen momenten zijn dat je niet genoeg onderscheid hebt tussen de ondermaatse ervaringen.

Als u statistisch significante differentiatie tussen alle ervaringen wilt veroorzaken, zou u kunnen willen overwegen gebruikend de handwijze van de verkeerstoewijzing.

**Conversietarieven die zijn gecorreleerd aan de tijd (of contextueel variëren), kunnen de toewijzingsbedragen scheeftrekken.**

Sommige factoren die tijdens een standaard A/B-test kunnen worden genegeerd omdat ze alle ervaringen evenzeer beïnvloeden, kunnen niet worden genegeerd in een [!UICONTROL Auto-Allocate] test. Het algoritme is gevoelig voor de waargenomen omrekeningskoersen. Hier volgen voorbeelden van factoren die de prestaties op verschillende manieren kunnen beïnvloeden:

* Ervaringen met verschillende contextuele (tijd, locatie, geslacht, enzovoort) relevantie.

   Bijvoorbeeld:

   * &quot;God zij dank is het Vrijdag&quot;resulteert in hogere omzettingen op Vrijdag
   * &quot;Springen naar uw maandag&quot; heeft een hogere conversie op maandag
   * &quot;Opslaan voor een winter voor de oostkust&quot; zorgt voor een hogere ombouw in door de oostkust of de winter getroffen gebieden

Het gebruik van ervaringen met verschillende contextafhankelijke relevanties kan de resultaten scheeftrekken in een [!UICONTROL Auto-Allocate] test meer dan bij een A/B-test omdat de A/B-test de resultaten over een langere periode analyseert.

* Ervaringen met uiteenlopende vertragingen bij de conversie, mogelijk als gevolg van de urgentie van de boodschap.

   Zo geeft &#39;30% verkoop eindigt vandaag&#39; de bezoeker de boodschap om te zetten, maar &#39;50% korting op eerste aankoop&#39; geeft niet hetzelfde gevoel van urgentie.

## Veelgestelde vragen {#section_0E72C1D72DE74F589F965D4B1763E5C3}

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u werkt met [!UICONTROL Auto-Allocate] activiteiten:

### doet [!UICONTROL Analytics for Target] (A4T)-ondersteuning [!UICONTROL Auto-Allocate] activiteiten?

Ja. Zie voor meer informatie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

### Worden de terugkerende bezoekers automatisch opnieuw toegewezen aan hoog presterende ervaringen?

Nee. Alleen nieuwe bezoekers worden automatisch toegewezen. Terugkerende bezoekers blijven hun oorspronkelijke ervaring zien om de geldigheid van de A/B-test te beschermen.

### Hoe behandelt het algoritme valse positieven?

Het algoritme garandeert een betrouwbaarheid van 95% of een percentage van 5% ten onrechte als u wacht tot de winnaar-badge wordt weergegeven.

### Wanneer doet [!UICONTROL Auto-Allocate] verkeersverdeling?

Het algoritme begint te werken nadat alle ervaringen in de activiteit minimaal 1000 bezoekers en 50 conversies hebben.

### Hoe agressief benut het algoritme?

80% van het verkeer wordt bediend [!UICONTROL Auto-Allocate] en 20 % van het verkeer wordt willekeurig bediend. Wanneer een winnaar werd geïdentificeerd, gaat alle 80% van het verkeer naar het, terwijl alle ervaringen wat verkeer als deel van de 20%, met inbegrip van de het winnen ervaring blijven krijgen.

### Worden er al ervaringen verloren?

Ja. De multigewapende bandit zorgt ervoor dat minstens 20% van het verkeer wordt gereserveerd om veranderende patronen of omzettingspercentages over alle ervaringen te onderzoeken.

### Wat gebeurt er met activiteiten met lange omzettingsvertragingen?

Zolang alle ervaringen die worden geoptimaliseerd vergelijkbare vertragingen hebben, is het gedrag hetzelfde als een activiteit met een snellere conversiecyclus. Nochtans, duurt het langer om de 50 omzettingsdrempel te bereiken alvorens het proces van de verkeerstoewijzing begint.

### Hoe wordt [!UICONTROL Auto-Allocate] verschillend van [!UICONTROL Automated Personalization]?

[!UICONTROL Automated Personalization] gebruikt de profielkenmerken van elke bezoeker om de beste ervaring te bepalen. Hierdoor wordt niet alleen de activiteit geoptimaliseerd, maar wordt ook de activiteit voor die gebruiker aangepast.

[!UICONTROL Auto-Allocate]Anderzijds is er een A/B-test die een gezamenlijke winnaar oplevert (de meest populaire ervaring, maar niet noodzakelijkerwijs de meest effectieve ervaring voor elke bezoeker).

### Worden de terugkerende bezoekers de omrekeningskoers op mijn succes metrisch?

Op dit moment bevoordeelt de logica bezoekers die snel converteren of vaker bezoeken, omdat dergelijke bezoekers tijdelijk de algemene conversiesnelheid verhogen van de ervaring waartoe zij behoren. Het algoritme past zich regelmatig aan, zodat wordt de verhoging van omzettingspercentage versterkt bij elke momentopname. Als de site talloze retouradres krijgt, kan de conversie van deze sites de algemene conversiekoers verhogen voor de ervaring waartoe ze behoren. Er is een goede kans dat retourbezoekers willekeurig worden verdeeld, waardoor het totale effect (verhoogde lift) gelijkmatig wordt verdeeld. Om dit effect te verzachten, kunt u de telmethode van de succesmetrische methode zo wijzigen dat deze slechts eenmaal per entry wordt geteld.

### Kan ik de voorbeeldgroottecalculator gebruiken bij het gebruik van [!UICONTROL Auto-Allocate] hoe lang duurt het om de winnaar te identificeren ?

U kunt de bestaande [voorbeeldgroottecalculator](https://experienceleague.adobe.com/tools/calculator/testcalculator.html) om een schatting te krijgen van de duur van de test. (Zoals bij traditionele A/B-tests kunt u Bonferroni-correctie toepassen als u meer dan twee aanbiedingen of meer dan één omzettingsmeting/hypothese test.) Deze rekenmachine is ontworpen voor traditionele A/B-tests met een vaste tijdshorizon en biedt alleen een schatting. De rekenmachine gebruiken voor een [!UICONTROL Auto-Allocate] activiteit is optioneel omdat [!UICONTROL Auto-Allocate] Hiermee wordt een winnaar voor je gedeclareerd. U hoeft geen vast punt in de tijd te kiezen om de testresultaten te bekijken. De opgegeven waarden zijn altijd statistisch geldig. In onze experimenten hebben we het volgende gevonden:
* Bij het testen van precies twee ervaringen: [!UICONTROL Auto-Allocate] vindt een winnaar sneller dan het testen met een vaste horizon (d.w.z. het tijdkader dat wordt voorgesteld door de calculator van de steekproefgrootte) wanneer het prestatiesverschil tussen ervaringen groot is. Maar [!UICONTROL Auto-Allocate] Het kan extra tijd vergen om een winnaar te identificeren wanneer het prestatiesverschil tussen ervaringen klein is. In deze gevallen zouden de vastrentende tests doorgaans zijn geëindigd zonder een statistisch significant resultaat.
* Bij het testen van meer dan twee ervaringen [!UICONTROL Auto-Allocate] vindt een winnaar sneller dan het testen met een vaste horizon (d.w.z. het tijdkader dat wordt voorgesteld door de calculator van de steekproefgrootte) wanneer één enkele ervaring alle andere ervaringen sterk overtreft. Wanneer twee of meer ervaringen zowel &quot;winnen&quot; ten opzichte van andere ervaringen maar nauw met elkaar overeenkomen, [!UICONTROL Auto-Allocate] kan extra tijd vereisen om te bepalen wat superieur is. In deze gevallen zouden de tests met een vaste looptijd doorgaans zijn geëindigd door te concluderen dat de &quot;winnende&quot; ervaringen beter waren dan de minder presterende ervaringen, maar niet hebben vastgesteld welke beter was.

### Moet ik een ondermaatse ervaring verwijderen uit een [!UICONTROL Auto-Allocate] activiteiten om de procedure voor de vaststelling van een winnaar te versnellen?

Er is echt geen reden om een ondermaatse ervaring te verwijderen. [!UICONTROL Auto-Allocate] Deze service dient automatisch vaker voor hoogwaardige ervaringen en werkt minder vaak voor ondermaatse ervaringen. Een ondermaatse ervaring in de activiteit heeft geen significante invloed op de snelheid om een winnaar te bepalen.

20% van de bezoekers wordt willekeurig toegewezen in alle ervaringen. De hoeveelheid verkeer die aan een ondermaatse ervaring wordt besteed, is minimaal (20% gedeeld door het aantal ervaringen).

### Kan ik het doel metrisch halverwege veranderen door een [!UICONTROL Auto-Allocate] activiteit? {#change-metric}

[!DNL Adobe] adviseert niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om het doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. [!DNL Adobe] garandeert niet wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] activiteiten die [!DNL Target] of [!DNL Analytics] (A4T) als bron van rapportage.

### Kan ik de rapportbron halverwege veranderen [!UICONTROL Auto-Allocate] activiteit? {#change-reporting}

[!DNL Adobe] adviseert niet dat u de rapporteringsbron halverwege een activiteit verandert. Hoewel het mogelijk is de bron van de rapportage te wijzigen (van [!DNL Target] naar A4T of vice versa) tijdens een activiteit die [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. [!DNL Adobe] garandeert niet wat er gebeurt als u de rapportbron wijzigt in een activiteit nadat deze is uitgevoerd.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] activiteiten die [!DNL Target] of [!DNL Analytics] (A4T) als bron van rapportage.

### Kan ik de [!UICONTROL Reset Report Data] optie tijdens het uitvoeren van een [!UICONTROL Auto-Allocate] activiteit?

Met de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Allocate] activiteiten worden niet voorgesteld. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords verwijderd uit de [!UICONTROL Auto-Allocate] model. In plaats van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Allocate] activiteiten, een nieuwe activiteit creëren en de oorspronkelijke activiteit deactiveren. (Deze richtsnoeren zijn ook van toepassing op [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] activiteiten.)

### Hoe werkt [!UICONTROL Auto-Allocate] modellen ontwikkelen met betrekking tot omgevingen?

[!UICONTROL Auto-Allocate] bouwt modellen die op het verkeer en omzettingsgedrag worden gebaseerd dat in het standaardmilieu slechts wordt geregistreerd. Standaard, [!UICONTROL Production] is de standaardomgeving, maar de standaardomgeving kan worden gewijzigd in [!DNL Target] [Beheer > Omgevingen](/help/main/administrating-target/environments.md).

Als een treffer in een andere (niet gebrek) milieu voorkomt, wordt het verkeer verdeeld volgens het waargenomen omzettingsgedrag in het standaardmilieu. Het resultaat van die treffer (conversie of niet-conversie) wordt geregistreerd voor rapportagedoeleinden, maar wordt niet in de [!UICONTROL Auto-Allocate] model.

Wanneer het selecteren van een ander milieu, toont het rapport verkeer en omzettingen voor dat milieu. De standaard geselecteerde omgeving voor een rapport is de standaard voor de gehele account die is geselecteerd. De standaardomgeving kan niet per activiteit worden ingesteld.

### Kan [!UICONTROL Auto-Allocate] de activiteit past het raadplegingsvenster over de cursus van een test aan om rekening te houden met veranderende tendensen in tijd?

Bijvoorbeeld, kan de activiteit de maand van December voor het beslissen over hoe te om verkeer toe te wijzen, eerder dan het bekijken van de gegevens van de bezoeker van September (toen de test begon) overwegen?

Nee, [!UICONTROL Auto-Allocate] rekening houdt met de uitvoering van de gehele activiteit.

### doet [!UICONTROL Auto-Allocate] een winnende ervaring tonen aan een terugkerende bezoeker als de winnende ervaring verschilt van wat de bezoeker zag toen hij in aanmerking kwam voor de activiteit?

[!UICONTROL Auto-Allocate] om dezelfde redenen een krappe beslissing gebruikt [!UICONTROL A/B Test] de activiteiten blijven steken . De verkeerstoewijzing werkt alleen voor nieuwe bezoekers.

## Trainingsvideo&#39;s {#section_893E5B36DC4A415C9B1D287F51FCCB83}

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Activiteitsworkflow - gericht (2:14) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video omvat informatie over vestiging verkeerstoewijzing.

* Een publiek toewijzen aan uw activiteit
* Verkeer omhoog of omlaag duwen
* Selecteer uw methode voor verkeerstoewijzing
* Verkeer toewijzen tussen verschillende ervaringen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### A/B-tests maken (8:36) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de driestapige workflow met instructies voor het doel. [!UICONTROL Auto-Allocate] wordt om 4:45 uur besproken.

* Een A/B-activiteit maken in [!DNL Adobe Target]
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
