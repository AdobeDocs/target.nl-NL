---
keywords: automated traffic allocation;targeting;Increment Count and Keep User in Activity;traffic allocation
description: Met Automatisch toewijzen wordt een winnaar geïdentificeerd aan de hand van twee of meer ervaringen en wordt automatisch meer verkeer toegewezen aan de winnaar, zodat de conversie toeneemt terwijl de test nog steeds wordt uitgevoerd en opgedaan.
title: Automatisch toewijzen
topic: Standard
uuid: e8aee4d7-2b99-4e1f-8004-2efc820658b5
translation-type: tm+mt
source-git-commit: a7669e3af01da50750ab7f61be692b6d7197476f
workflow-type: tm+mt
source-wordcount: '3009'
ht-degree: 0%

---


# Automatisch toewijzen{#auto-allocate}

Met Automatisch toewijzen wordt een winnaar geïdentificeerd op basis van twee of meer ervaringen en wordt automatisch meer verkeer toegewezen aan de winnaar, zodat de conversies toenemen terwijl de test nog steeds wordt uitgevoerd en opgedaan.

Tijdens het [maken van een A/B-activiteit met behulp van de driestappenworkflow](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)met instructies kunt u de [!UICONTROL Auto-Allocate to Best Experience] optie kiezen.

## De uitdaging {#section_85D5A03637204BACA75E19646162ACFF}

Standaard A/B-tests hebben inherente kosten. U moet verkeer uitgeven om prestaties van elke ervaring te meten en door analyse de het winnen ervaring te berekenen. De verdeling van het verkeer blijft vast zelfs nadat u erkent dat sommige ervaringen anderen overtreffen. Bovendien is het ingewikkeld om de steekproefgrootte te bepalen, en de activiteit moet zijn volledige cursus in werking stellen alvorens u op een winnaar kunt handelen. Na dit alles is er nog steeds een kans dat de geïdentificeerde winnaar geen echte winnaar is.

## De oplossing: Automatisch toewijzen {#section_98388996F0584E15BF3A99C57EEB7629}

Automatisch toewijzen verlaagt deze kosten en overheadkosten voor het bepalen van een winnende ervaring. Automatisch toewijzen bewaakt de beoogde metrische prestaties van alle ervaringen en stuurt meer nieuwkomers proportioneel naar de hoogwaardige ervaringen. Voldoende verkeer is gereserveerd om de andere ervaringen te onderzoeken. U kunt de voordelen van de test op uw resultaten zien, zelfs terwijl de activiteit nog loopt: optimalisatie vindt plaats in combinatie met leren .

Met Automatisch toewijzen gaan bezoekers geleidelijk over op het winnen van ervaringen, in plaats van dat u wacht tot een activiteit eindigt om een winnaar te bepalen. U profiteert sneller van een lift omdat deelnemers aan activiteiten die naar minder succesvolle ervaringen zouden zijn gestuurd, potentiële winnende ervaringen kunnen laten zien.

Bij een normale A/B-test in Target worden alleen paarsgewijze vergelijkingen van alkenen met besturing getoond. Als een activiteit bijvoorbeeld ervaringen heeft: A, B, C en D waarbij A de controle is, zou een normale Target A/B test A versus B, A versus C, en A versus D vergelijken.

In dergelijke tests gebruiken de meeste producten, waaronder Target, de t-test van een student om op p-waarde gebaseerd vertrouwen te produceren. Deze betrouwbaarheidswaarde wordt vervolgens gebruikt om te bepalen of de toerist voldoende van de controle verschilt. Target voert echter niet automatisch de impliciete vergelijkingen uit (B versus C, B versus D, en C versus D) die vereist zijn om de &quot;beste&quot; ervaring te vinden. Het resultaat is dat de markeerstift de resultaten handmatig moet analyseren om de &quot;beste&quot; ervaring te bepalen.

Automatisch toewijzen voert alle impliciete vergelijkingen tussen ervaringen uit en levert een &quot;echte&quot; winnaar op. Er bestaat geen begrip van een &quot;controle&quot;ervaring in de test.

Automatisch toewijzen wijst nieuwe bezoekers op intelligente wijze toe aan ervaringen totdat de betrouwbaarheidsinterval van de beste ervaring niet overlapt met die van een andere ervaring. Normaal zou dit proces valse positieven kunnen veroorzaken, maar auto-Wijs gebruikt betrouwbaarheidsintervallen die op de Ongelijkheid [van](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) Bernstein worden gebaseerd die voor herhaalde evaluaties compenseert. Op dit moment hebben we een echte winnaar. Wanneer Automatisch toewijzen stopt, mits de bezoekers die op de pagina aankomen niet in aanzienlijke mate afhankelijk zijn van de tijd, is er ten minste een kans van 95% dat automatisch toewijzen een ervaring retourneert waarvan de werkelijke respons niet minder is dan 1% (relatief) dan de werkelijke respons van de winnende ervaring.

## Wanneer om Auto-Toewijzing tegenover A/B of Geautomatiseerde Personalisatie te gebruiken {#section_3F73B0818A634E4AAAA60A37B502BFF9}

* Gebruik **Automatisch toewijzen** als u uw activiteiten vanaf het begin wilt optimaliseren en de winnende ervaringen zo snel mogelijk wilt identificeren. Doordat de prestaties van de activiteit in het algemeen vaker worden verbeterd, zijn de prestaties beter afgestemd op de prestaties.
* Gebruik een standaard **[A/B-test](../../c-activities/t-test-ab/test-ab.md#task_05E33EB15C4D4459B5EAFF90A94A7977)**als u de prestaties van alle ervaringen wilt karakteriseren voordat u uw site optimaliseert. Een A/B test helpt u al uw ervaringen te rangschikken, terwijl de Geautomatiseerde Toewijzing van het Verkeer hoogste uitvoerders vindt maar geen verschil tussen de lagere uitvoerders garandeert.
* Gebruik [Geautomatiseerde personalisatie](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) wanneer u optimalisatiealgoritmen van de hoogste ingewikkeldheid, zoals machine-leert modellen wilt die voorspellingen bouwen die op individuele profielattributen worden gebaseerd. De geautomatiseerde Toewijzing van het Verkeer kijkt naar het gezamenlijke gedrag van ervaringen (enkel als standaard A/B tests), en maakt geen onderscheid tussen bezoekers.

## Belangrijkste voordelen {#section_0913BF06F73C4794862561388BBDDFF0}

* Behoudt de strengheid van een A/B-test
* Vindt een statistisch significante winnaar sneller dan een handmatige A/B test
* Biedt een hogere gemiddelde campagnelift dan een handmatige A/B-test

## Terminologie {#section_670F8785BA894745B43B6D4BFF953188}

De volgende termen zijn handig bij het bespreken van Automatisch toewijzen:

**Meervoudig bewapende bandit:** Een [veelbewapende bandibenadering](https://en.wikipedia.org/wiki/Multi-armed_bandit) voor optimalisering brengt een evenwicht tot stand tussen verkennend leren en het gebruik van dat leren.

## Hoe het algoritme werkt {#section_ADB69A1C7352462D98849F2918D4FF7B}

In de algemene logica achter Automatisch toewijzen zijn zowel gemeten prestaties (zoals de conversiesnelheid) als betrouwbaarheidsintervallen van de cumulatieve gegevens opgenomen. In tegenstelling tot een standaard A/B test waar het verkeer gelijkelijk tussen ervaringen wordt verdeeld, verandert de auto-Toewijzing verkeerstoewijzing over ervaringen.

* 80 % van de bezoekers wordt toegewezen op basis van de hieronder beschreven intelligente logica .
* 20% van de bezoekers wordt willekeurig toegewezen in alle ervaringen om zich aan te passen aan het veranderende gedrag van bezoekers.

De multi-gewapende bandibenadering houdt sommige ervaringen vrij voor onderzoek terwijl het exploiteren van de ervaringen die goed presteren. Meer nieuwe bezoekers worden geplaatst in beter presterende ervaringen terwijl het vermogen behouden om op veranderende omstandigheden te reageren. Deze modellen worden minstens eenmaal per uur bijgewerkt om ervoor te zorgen dat het model reageert op de meest recente gegevens.

Naarmate meer bezoekers de activiteit betreden, worden sommige ervaringen succesvoller en wordt meer verkeer verzonden naar de succesvolle ervaringen. 20% van het verkeer blijft willekeurig worden bediend om alle ervaringen te onderzoeken. Als één van de minder presterende ervaringen begint beter te presteren, wordt meer verkeer toegewezen aan die ervaring. Of als het succes van een meer presterende activiteit vermindert, wordt minder verkeer toegewezen aan die ervaring. Als bezoekers bijvoorbeeld naar andere informatie op uw mediasite zoeken tijdens een gebeurtenis, levert de weekendverkoop op uw detailhandelssite andere resultaten op.

De volgende illustratie vertegenwoordigt hoe het algoritme tijdens een test met vier ervaringen zou kunnen uitvoeren:

![](assets/auto-allocate.png)

De illustratie toont hoe het verkeer dat aan elke ervaring wordt toegewezen zich over verscheidene ronden van het activiteitenleven ontwikkelt tot een duidelijke winnaar wordt bepaald.

| Rond | Beschrijving |
|--- |--- |
| ![Warm-omhoog rond](/help/c-activities/automated-traffic-allocation/assets/aa-phase-0.png) | **Warm-omhoog rond (0)**: Tijdens de opwarmen ronde, krijgt elke ervaring gelijke verkeerstoewijzing tot elke ervaring in de activiteit een minimum van 1.000 bezoekers en 50 omzettingen heeft.<ul><li>Ervaring A=25%</li><li>Ervaring B=25%</li><li>Ervaring C=25%</li><li>Ervaring D=25%</li></ul>Nadat elke ervaring 1.000 bezoekers en 50 omzettingen krijgt, begint Target geautomatiseerde verkeerstoewijzing. Alle toewijzingen vinden plaats in rondes en voor elke ronde worden twee ervaringen gekozen.<br>Slechts twee ervaringen gaan verder in de volgende ronde: D en C.<br>Vooruit bewegen betekent dat de twee ervaringen 80% van het verkeer gelijkelijk worden toegewezen, terwijl de andere twee ervaringen blijven deelnemen, maar slechts dienen als deel van de 20% willekeurige verkeersverdeling wanneer nieuwe bezoekers de activiteit betreden.<br>Alle toewijzingen worden elk uur bijgewerkt (weergegeven aan de hand van rondes langs de x-as hierboven). Na elke ronde worden de cumulatieve gegevens vergeleken. |
| ![Afgerond 1](/help/c-activities/automated-traffic-allocation/assets/aa-phase-1.png) | **Rond 1**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen C en D (elk 40%). 20% van het verkeer wordt willekeurig toegewezen aan ervaringen A, B, C, en D (elk 5%). Tijdens deze ronde presteert A goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring A om zich ook vooruit te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en A gaan verder. |
| ![Rond 2](/help/c-activities/automated-traffic-allocation/assets/aa-phase-2.png) | **Rond 2**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen A en D (elk 40%). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde functioneert ervaring B goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring B om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en B gaan verder. |
| ![Rond 3](/help/c-activities/automated-traffic-allocation/assets/aa-phase-3.png) | **Rond 3**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen B en D (40% elk). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde blijft de ervaring D goed presteren en de ervaring C functioneert goed.<ul><li>Het algoritme plukt ervaring D om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring C om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen D en C gaan verder. |
| ![Afgerond 4](/help/c-activities/automated-traffic-allocation/assets/aa-phase-4.png) | **Rond 4**: Tijdens deze ronde wordt 80% van het verkeer toegewezen aan ervaringen C en D (elk 40%). 20% van het verkeer wordt willekeurig toegewezen, zodat A, B, C, en D elk 5% van het verkeer krijgen. Tijdens deze ronde functioneert ervaring C goed.<ul><li>Het algoritme verkiest ervaring C om zich in de volgende ronde vooruit te bewegen omdat het de hoogste omzettingspercentage heeft (zoals die door op de verticale schaal van elke activiteit wordt vermeld).</li><li>Het algoritme plukt ervaring D om zich eveneens te bewegen omdat het de hoogste bovengrens van Bernstein 95% betrouwbaarheidsinterval van de resterende ervaringen heeft.</li></ul>De ervaringen C en D gaan verder. |
| ![Rond n](/help/c-activities/automated-traffic-allocation/assets/aa-phase-n.png) | **Rond n**: Naarmate de activiteit vordert, begint een krachtige ervaring op te komen en gaat het proces door tot er een winnende ervaring is. Wanneer het betrouwbaarheidsinterval van de ervaring met de hoogste omzettingspercentage niet met het betrouwbaarheidsinterval van een andere ervaring overlapt, wordt het geëtiketteerd de winnaar en een [badge vertoningen op de pagina](/help/c-activities/automated-traffic-allocation/determine-winner.md) van de activiteit en in de lijst van de Activiteit.<ul><li>Het algoritme kiest ervaring C als duidelijke winnaar</li></ul>Op dit punt dient het algoritme 80% van het verkeer om C te ervaren, terwijl 20% van het verkeer willekeurig aan alle ervaringen (A, B, C, en D) wordt gediend. In totaal krijgt C 85% van het verkeer. In het onwaarschijnlijke geval dat het betrouwbaarheidsinterval van de winnaar opnieuw begint te overlappen, keert het algoritme terug naar het gedrag van ronde 4 hierboven.<br>**Belangrijk **: Als u eerder tijdens het proces handmatig een winnaar koos, was het gemakkelijk geweest om de verkeerde ervaring te kiezen. Daarom is het aan te raden te wachten totdat het algoritme de winnende ervaring bepaalt. |

Als de activiteit slechts twee ervaringen heeft, krijgen allebei gelijk verkeer tot Target een ervaring met 90% vertrouwen vindt. Op dat moment wordt 70% van het verkeer toegewezen aan de winnaar en 30% aan de verliezer. Nadat die ervaring 95% betrouwbaarheid heeft bereikt, wordt 100% van het verkeer toegewezen aan de winnaar en 0% aan de verliezer.

Nadat een [!UICONTROL Auto-Allocate] activiteit wordt geactiveerd, zijn de volgende verrichtingen van UI niet toegestaan:

* De modus &quot;Verkeerstoewijzing&quot; omzetten in &quot;Handmatig&quot;
* Het metrische type van het doel wijzigen
* Opties wijzigen in het deelvenster Geavanceerde instellingen

## Caveats {#section_5C83F89F85C14FD181930AA420435E1D}

**De functie Automatisch toewijzen werkt met slechts één geavanceerde metrische instelling: Aantal verhogen en Gebruiker in activiteit houden**

De volgende geavanceerde metrische instellingen worden niet ondersteund: Het Aantal van de verhoging, de Gebruiker van de Versie, staat het Aantal van de Terugkeer en van de Toename, en de Gebruiker en de Bar van de Versie van de Versie van Terugkeer toe.

**De frequente terugkeerbezoekers kunnen ervaring omzettingspercentages opblazen.**

Als een bezoeker die A ziet vaak terugkeert en verscheidene keren omzet, wordt het Tarief van de Omzetting (CR) van ervaring A kunstmatig verhoogd. Vergelijk dit met B, waar bezoekers zich bekeren maar niet vaak terugkeren. Als gevolg hiervan ziet de CR van A er beter uit dan de CR van B, zodat nieuwe bezoekers eerder aan A zullen worden toegewezen dan aan B. Als u ervoor kiest om één keer per toetreder te tellen, kan de CR van A en CR van B identiek zijn.

Als retourbezoekers willekeurig worden verdeeld, is het waarschijnlijker dat hun effect op de omrekeningskoersen wordt gelijkgetrokken. Om dit effect te verlichten, denk na veranderend de tellende methode van doel metrisch om slechts eenmaal per ingang te tellen.

**Verschillen tussen hoogpresteerders, niet tussen slechtpresterende.**

Automatisch toewijzen is goed in het onderscheid maken tussen hoogwaardige ervaringen (en het zoeken naar een winnaar). Er kunnen momenten zijn dat je niet genoeg onderscheid hebt tussen de ondermaatse ervaringen.

Als u statistisch significante differentiatie tussen alle ervaringen wilt veroorzaken, zou u het gebruiken van de manuele wijze van de Toewijzing van het Verkeer kunnen willen overwegen.

**Conversietarieven die zijn gecorreleerd aan de tijd (of contextueel variëren), kunnen de toewijzingsbedragen scheeftrekken.**

Sommige factoren die tijdens een standaard A/B test kunnen worden genegeerd omdat zij alle ervaringen evenzeer beïnvloeden kunnen niet in een auto-Wijs test worden genegeerd. Het algoritme is gevoelig voor de waargenomen omrekeningskoersen. Hier volgen voorbeelden van factoren die de prestaties op verschillende manieren kunnen beïnvloeden:

* Ervaringen met verschillende contextuele (tijd, locatie, geslacht, enz.) relevantie.

   Bijvoorbeeld:

   * &quot;God zij dank is het Vrijdag&quot;resulteert in hogere omzettingen op Vrijdag
   * &quot;Springen naar uw maandag&quot; heeft een hogere conversie op maandag
   * &quot;Opslaan voor een winter voor de oostkust&quot; zorgt voor een hogere ombouw in door Oost-Coast of winter getroffen gebieden

Deze kunnen de resultaten bij een autotoewijzing meer scheeftrekken dan bij een A/B-test, omdat de resultaten bij de A/B-test gedurende een langere periode worden geanalyseerd.

* Ervaringen met uiteenlopende vertragingen bij de conversie, mogelijk als gevolg van de urgentie van de boodschap.

   Zo geeft &#39;30% verkoop eindigt vandaag&#39; de bezoeker de boodschap om te zetten, maar &#39;50% korting op eerste aankoop&#39; geeft niet hetzelfde gevoel van urgentie.

## Veelgestelde vragen {#section_0E72C1D72DE74F589F965D4B1763E5C3}

** Steunt Analytics for Target (A4T) Auto-Allocate activiteiten?

Ja. Zie [Analytics for Target (A4T)-ondersteuning voor Auto-Allocate-activiteiten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) in *Activity creation* voor meer informatie.

**Worden de terugkerende bezoekers automatisch opnieuw toegewezen aan hoog presterende ervaringen?**

Nee. Alleen nieuwe bezoekers worden automatisch toegewezen. De terugkerende bezoekers blijven hun originele ervaring zien. Hiermee wordt de geldigheid van de A/B-test beschermd.

**Hoe behandelt het algoritme valse positieven?**

Het algoritme garandeert een betrouwbaarheid van 95% of een percentage van 5% ten onrechte als u wacht tot de winnaar-badge wordt weergegeven.

**Wanneer begint de auto-Toewijzing verkeer toe te wijzen?**

Het algoritme begint te werken nadat alle ervaringen in de activiteit minimaal 1000 bezoekers en 50 conversies hebben.

**Hoe agressief benut het algoritme?**

80% van het verkeer wordt gediend gebruikend auto-Toewijzing en 20% van verkeer wordt willekeurig gediend. Wanneer een winnaar werd geïdentificeerd, gaat alle 80% van het verkeer naar het, terwijl alle ervaringen wat verkeer als deel van de 20%, met inbegrip van de het winnen ervaring blijven krijgen.

**Worden er al ervaringen verloren?**

Ja. De multigewapende bandit zorgt ervoor dat minstens 20% van het verkeer wordt gereserveerd om veranderende patronen of omzettingspercentages over alle ervaringen te onderzoeken.

**Wat gebeurt er met activiteiten met lange omzettingsvertragingen?**

Zolang alle ervaringen die worden geoptimaliseerd met gelijkaardige vertragingen worden geconfronteerd, is het gedrag het zelfde als een activiteit met een snellere omzettingscyclus, hoewel het langer zal duren om de 50 omzettingsdrempel te bereiken alvorens het proces van de verkeerstoewijzing begint.

**Hoe verschilt Automatisch toewijzen van geautomatiseerde personalisatie?**

Bij Geautomatiseerde personalisatie worden de profielkenmerken van elke bezoeker gebruikt om de beste ervaring te bepalen. Hierdoor wordt niet alleen de activiteit geoptimaliseerd, maar wordt ook de activiteit voor die gebruiker aangepast.

Auto-Allocate daarentegen is een A/B test die een gezamenlijke winnaar (de populairste ervaring, maar niet noodzakelijk de meest efficiënte ervaring voor elke bezoeker) produceert.

**Worden de terugkerende bezoekers de omzettingspercentage op mijn succes metrisch?**

Op dit moment is de logica gunstig voor bezoekers die snel converteren of vaker een bezoek brengen. De reden hiervoor is dat dergelijke bezoekers tijdelijk de algemene omrekeningskoers van de ervaring die zij hebben, verhogen. Het algoritme past zich regelmatig aan, zodat wordt de verhoging van omzettingspercentage versterkt bij elke momentopname. Als de site veel bezoekers retourneert, kunnen hun conversies de algemene conversiekoers voor de ervaring tot wie ze behoren, potentieel verhogen. Er is een goede kans dat retourbezoekers willekeurig worden verdeeld, waardoor het totale effect (verhoogde lift) gelijkmatig wordt verdeeld. Om dit effect te verzachten, kunt u de telmethode van de succesmetrische methode zo wijzigen dat deze slechts eenmaal per entry wordt geteld.

**Kan ik de calculator van de steekproefgrootte gebruiken wanneer het gebruiken van auto-Toewijzing om te schatten hoe lang de activiteit zal duren om de winnaar te identificeren?**

U kunt de bestaande calculator [van de](https://docs.adobe.com/content/target-microsite/testcalculator.html) steekproefgrootte gebruiken om een schatting van te krijgen hoe lang de test zal lopen. (Zoals bij traditionele A/B-tests kunt u Bonferroni-correctie toepassen als u meer dan twee aanbiedingen of meer dan één omzettingsmeting/hypothese test.) Deze rekenmachine is ontworpen voor traditionele A/B-tests met een vaste tijdshorizon en biedt alleen een schatting. Het gebruiken van de calculator voor een auto-Wijs activiteit is facultatief omdat auto-toewijst een winnaar voor u zal verklaren-u te hoeven om geen vast punt in tijd te kiezen om de testresultaten-verstrekt waarden te bekijken altijd statistisch geldig zijn. In onze experimenten hebben we het volgende gevonden:
* Bij het testen van precies twee ervaringen wordt met Automatisch toewijzen een winnaar sneller gevonden dan met tests met een vaste tijdshorizon (dat wil zeggen het tijdsbestek dat wordt voorgesteld door de calculator voor de voorbeeldgrootte) wanneer het prestatieverschil tussen ervaringen groot is, maar extra tijd nodig kan zijn om een winnaar te identificeren wanneer het prestatieverschil tussen ervaringen klein is. In deze gevallen zouden de vastrentende tests doorgaans zijn geëindigd zonder een statistisch significant resultaat.
* Bij het testen van meer dan twee ervaringen wordt met Automatisch toewijzen een winnaar sneller gevonden dan met tests met een vaste tijdshorizon (d.w.z. het tijdpad dat wordt voorgesteld door de calculator voor voorbeeldgrootte) wanneer één ervaring alle andere ervaringen sterk overtreft. Wanneer twee of meer ervaringen allebei &quot;het winnen&quot;tegen andere ervaringen maar dicht bij elkaar aansluiten, zou de auto-Toewijzing extra tijd kunnen vereisen om te bepalen wat superieur is. In deze gevallen zouden de tests met een vaste looptijd doorgaans zijn geëindigd door te concluderen dat de &quot;winnende&quot; ervaringen beter waren dan de minder presterende ervaringen, maar niet hebben vastgesteld welke beter was.

**Moet ik een ondermaatse ervaring verwijderen uit een automatisch toegewezen activiteit om het proces van het bepalen van een winnaar te versnellen?**

Er is echt geen reden om een ondermaatse ervaring te verwijderen. Automatisch toewijzen dient automatisch hogere prestaties en ondermaatse ervaringen. Als u een ondermaatse ervaring in de activiteit laat staan, heeft dat geen significante invloed op de snelheid waarmee de winnaar wordt bepaald.

20% van de bezoekers wordt willekeurig toegewezen in alle ervaringen. De hoeveelheid verkeer die wordt gebruikt voor een ondermaatse ervaring is minimaal (20% gedeeld door het aantal ervaringen).

## Trainingsvideo&#39;s {#section_893E5B36DC4A415C9B1D287F51FCCB83}

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Werkstroom voor activiteiten - gerichte ![zelfstudie (2:14)](/help/assets/tutorial.png)

Deze video omvat informatie over vestiging verkeerstoewijzing.

* Een publiek toewijzen aan uw activiteit
* Verkeer omhoog of omlaag duwen
* Selecteer uw methode voor verkeerstoewijzing
* verdeel verkeer tussen verschillende ervaringen

>[!VIDEO](https://video.tv.adobe.com/v/17385)

### Een ![zelfstudie-badge voor A/B-tests maken (8:36)](/help/assets/tutorial.png)

In deze video ziet u hoe u een A/B-test maakt met behulp van de driestappenworkflow met instructies voor Target. De geautomatiseerde verkeerstoewijzing wordt besproken beginnend bij 4:45.

* A/B-activiteit maken in Adobe Target
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
