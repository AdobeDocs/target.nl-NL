---
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;automated personalization
description: Lijst met veelgestelde vragen (FAQ's) over Automated Personalization (AP).
title: Veelgestelde vragen over Automated Personalization
feature: ap
uuid: 4c8aadd3-75c3-4388-b838-e62576dfb955
translation-type: tm+mt
source-git-commit: 6278a01928fcb9dd0b34d7a8b5313f09f1e8da0f
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Automated Personalization - Veelgestelde vragen{#automated-personalization-faq}

Lijst met veelgestelde vragen (FAQ&#39;s) over Automated Personalization (AP).

## Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?

U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Auto-Doel](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Zie Een specifieke ervaring [gebruiken als controle](/help/c-activities/t-automated-personalization/experience-as-control.md)voor meer informatie.

## Hoe kan ik Automated Personalization vergelijken met een standaardervaring? {#section_46C1A620A2384C2C8392D6716DD18495}

Er is geen optie om AP met een andere toets te vergelijken met een standaardervaring. Nochtans, als een oplossing, als een standaardaanbieding of een ervaring als deel van de algemene activiteit bestaat, om zijn basislijnprestaties te begrijpen kunt u het &quot;Controle&quot;segment in de rapporten klikken en van die bepaalde aanbieding in het resulterende aanbod-vlakke rapport de plaats bepalen. De voor deze aanbieding geregistreerde omrekeningskoers kan worden gebruikt om met het gesprekstarief van het volledige segment &quot;Random Forest&quot; te vergelijken. Dit helpt om te vergelijken hoe de machine in vergelijking met het standaardaanbod doet.

## Wat zijn de beste praktijken om een activiteit van Automated Personalization op te zetten? {#section_E155B26282BE49B58EA2683413D11DE6}

* Als u een pagina met minder verkeer wilt personaliseren, of u wilt structurele veranderingen in de ervaring aanbrengen u personaliseert, denk na gebruikend auto-Doel in plaats van Automated Personalization. Zie [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md).
* Overweeg een A/B-activiteit uit te voeren tussen de aanbiedingen en locaties die u in uw Automated Personalization-activiteit wilt gebruiken om te controleren of de locatie(s) en aanbiedingen van invloed zijn op de optimalisatiedoelstelling. Indien een A/B-activiteit geen significant verschil aantoont, zal Automated Personalization waarschijnlijk ook geen lift genereren.

   * Als een A/B...N test geen statistisch significante verschillen tussen ervaringen toont, waarschijnlijk zijn de aanbiedingen u overweegt niet voldoende verschillend van elkaar, beïnvloeden de plaatsen u selecteerde niet succesmetrisch, of het optimalisatiedoel is te ver in de conversietrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Zorg ervoor om de [schatter](../../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) van het Verkeer te gebruiken zodat kunt u een idee hebben van hoe lang het voor verpersoonlijkingsmodellen zal vergen om in uw activiteit van Automated Personalization op te bouwen.
* Beslis over de toewijzing tussen controle en gericht alvorens met de activiteit te beginnen die op uw doelstellingen wordt gebaseerd.

   Er zijn drie scenario&#39;s die u kunt overwegen op basis van het doel van uw activiteit en het type besturingselement dat u hebt geselecteerd:

   * **Willekeurige Ervaringen als uw controle en uw activiteitendoel is de doeltreffendheid van het verpersoonlijkingsalgoritme** te testen: Als u het verpersoonlijkingsalgoritme wilt evalueren, wilt u een nauwkeuriger beeld van uw lift hebben. U wilt waarschijnlijk ook vergelijken met wat de omrekeningskoers voor uw ervaringen/aanbiedingen zou zijn als u eenvoudig een A/B Test (een willekeurig bediende controle) zou doen. In die situatie wordt het gebruik van een 50%-toewijzing voor een controle van willekeurig bediende ervaringen aanbevolen.
   * **&quot;Willekeurige Ervaringen&quot;aangezien uw controle en uw activiteitendoel gepersonaliseerd verkeer** moet maximaliseren: Als u vertrouwd bent met het algoritme en de maximumhoeveelheid verkeer gepersonaliseerd wilt hebben, wordt een 10% tot 30% toewijzing aan controle geadviseerd. De hier weggevoerde handel is de nauwkeurigheid u in uw liftinformatie zult kunnen zien (aangezien de betrouwbaarheidsintervallen van uw controleverkeer groter zullen zijn omdat er minder verkeer aan hen stroomt).
   * **Specifieke Ervaring als uw controle, met één van beide doeltype**: Als u een specifieke markeringsgedreven ervaring met de verpersoonlijkingsmodellen wilt vergelijken, wordt een 10% tot 30% toewijzing aan controle geadviseerd. Als u slechts één ervaring als controle selecteert, wordt dat verkeer niet over elke aanbieding/ervaring in de activiteit verspreid.

* De gerichte regels zouden zo spaarzaam mogelijk moeten worden gebruikt omdat zij het vermogen van het model om te optimaliseren kunnen verhinderen.
* Rapportagegroepen kunnen het succes van je Automated Personalization-activiteiten beperken. Zij mogen alleen onder specifieke omstandigheden worden gebruikt.

   * Gebruik alleen rapportgroepen als aan de volgende voorwaarden is voldaan: (1) u van plan bent nieuwe aanbiedingen te vervangen of toe te voegen terwijl de activiteit actief is, (2) de aanbiedingen in de rapportagegroep richten zich tot dezelfde bezoekers en (3) de aanbiedingen in die rapportagegroep hebben ongeveer hetzelfde totale responspercentage.
   * Er is geen personalisatie tussen aanbiedingen in een rapportagegroep: de aanbiedingen worden door het personaliseringsmodel op dezelfde wijze behandeld .
   * Plaats nooit alle aanbiedingen in een activiteit in één rapporteringsgroep. Dit besluit zal ertoe leiden dat alle aanbiedingen gelijkmatig willekeurig aan alle bezoekers in de activiteit worden betekend.

## Veelgestelde vragen

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u werkt met activiteiten voor automatisch toewijzen:

### Wat zijn enkele limieten in Automated Personalization? {#section_08BA09ED51B547299963C94FE6417CFA}

Het doel heeft een harde limiet van 30.000 ervaringen, maar het werkt op zijn best als er minder dan 10.000 ervaringen worden gecreëerd.

### Hoe wordt het aanbieden-niveau richten uitgevoerd? {#section_9D7A86EA93D74E9B8C81072A681263A4}

Wanneer elke bezoeker aankomt, wordt de reeks mogelijke aanbiedingen die de bezoeker kan zien bepaald door de aanbiedingsniveau richtingsregels. Dan, kiest het algoritme de aanbieding die het model voorspelt de beste verwachte opbrengst of de kans van omzetting van onder die aanbiedingen zal hebben. Het aanbieden van gerichte toepassingen heeft invloed op de effectiviteit van de computerleeralgoritmen van Target en moet daarom zo spaarzaam mogelijk worden gebruikt.

### Mijn activiteit laat geen lift zien. Wat is er aan de hand? {#section_BFA07C8C258F45318F73A461B8F32737}

Er zijn vier factoren vereist voor een AP-activiteit om lift te genereren:

* De aanbiedingen op elke locatie moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De plaatsen moeten ergens zijn die een verschil aan het optimalisatiedoel maakt.
* Er moet voldoende verkeer en statistische kracht in de activiteit aanwezig zijn om de lift te kunnen detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als een A/B-testresultaten statistisch significante lift op een of meer van de ervaringen laten zien, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

Voor meer informatie, [het Oplossen van problemen Automated Personalization](../../c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

### Hoe wijst Automated Personalization het verkeer van mijn activiteiten toe? {#section_4369364F77804E0D9B78BEE551DA5659}

Automated Personalization leidt bezoekers naar de ervaring die de hoogst voorspelde succesmetrisch gebaseerd op de meest recente modellen van het [Willekeurige Bos](/help/c-activities/t-automated-personalization/algo-random-forest.md) heeft die voor elk model worden gebouwd. Deze prognose is gebaseerd op de specifieke informatie en de context van het bezoek van de bezoeker.

Stel bijvoorbeeld dat een AP-activiteit twee locaties had met elk twee aanbiedingen. Op de eerste locatie wordt voor Offer A een omrekeningskoers van 3% voor een specifieke bezoeker voorspeld en voor Aanbieding B een omrekeningskoers van 1%. Op de tweede locatie wordt voor Offer C een omrekeningskoers van 2% voor dezelfde bezoeker voorspeld, terwijl Offer D een omrekeningskoers van 5% heeft. Automated Personalization zou deze bezoeker dan ook een ervaring bieden met voorstel A en aanbod D.

### Wanneer moet ik mijn Automated Personalization-activiteiten stopzetten? {#section_C51F3DAB8887463BB147373F6FE06B93}

Automated Personalization kan worden gebruikt als &#39;altijd op&#39;-personalisatie die voortdurend wordt geoptimaliseerd. Met name voor steeds groene inhoud is het niet nodig om je Automated Personalization-activiteiten te stoppen. Als u substantiële veranderingen in de inhoud wilt aanbrengen die niet aan aanbiedingen momenteel in uw Automated Personalization activiteit gelijkaardig zijn, is de beste praktijk om een nieuwe activiteit te beginnen zodat andere gebruikers die rapporten herzien geen verwarrings of betrekking hebben verleden resultaten met verschillende inhoud.

### Hoe lang moet ik wachten op modellen om te bouwen? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

De tijdsduur die nodig is voor modellen om uw activiteit uit te breiden, is doorgaans afhankelijk van het verkeer naar de geselecteerde locatie(s) van de activiteit en van de mate van succes van de activiteit. Gebruik de [schatter](../../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) van het Verkeer om de verwachte tijdsduur te bepalen het voor modellen zal vergen om in uw activiteit te bouwen.

### Eén model is gebouwd binnen mijn activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd? {#section_51EA953C6D1D4A3185FC9DD290D66621}

Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

### Wanneer kan ik naar de resultaten van mijn Automated Personalization-activiteiten kijken? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

U kunt de resultaten bekijken van uw Automated Personalization-activiteiten zodra u minstens twee ervaringen hebt met gebouwde modellen (groen vinkje) voor de ervaring die modellen heeft gebouwd.

### Hoe kan ik de hoeveelheid tijd verminderen nodig voor modellen om in mijn activiteit te bouwen? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen zullen bouwen.

* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting zal de verkeersvereisten verhogen nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen.
* Zijn er sommige ervaringen u van uw activiteit kunt laten vallen? Als u het aantal ervaringen in een activiteit verlaagt, wordt de hoeveelheid tijd die nodig is om modellen te bouwen, versneld.
* Is er een hoger-verkeerspagina daar deze activiteit succesvoller zou zijn? Hoe meer verkeer en conversies er in uw activiteitenlocaties plaatsvinden, hoe sneller de modellen worden.

### Waarom zien bezoekers ervaringen voor een AP-activiteit die ze niet zouden moeten zien? {#section_41CECEAE0881446A8D9F3B016857914B}

Automated Personalization-activiteiten worden één keer per sessie geëvalueerd. Als er actieve sessies waren die in aanmerking kwamen voor een bepaalde ervaring en er nu nieuwe aanbiedingen aan zijn toegevoegd, zien gebruikers de nieuwe inhoud samen met de eerder weergegeven aanbiedingen. Omdat ze eerder gekwalificeerd waren voor die ervaringen, zouden ze ze nog steeds zien gedurende de sessie. Als u dit bij elk paginabezoek wilt evalueren, kunt u beter overschakelen op het type activiteit Experience Targeting (XT).

### Kan ik het doel metrisch halverwege door een activiteit van Automated Personalization veranderen? {#change-metric}

Wij adviseren niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. Wij garanderen niet wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target]en [!UICONTROL Automated Personalization] activiteiten die ofwel [!DNL Target] of [!DNL Analytics] (A4T) als rapportagebron gebruiken.

### Kan ik de optie Rapportgegevens opnieuw instellen gebruiken tijdens het uitvoeren van een Automated Personalization-activiteit?

Het gebruik van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Automated Personalization] activiteiten wordt niet voorgesteld. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords uit het [!UICONTROL Automated Personalization] model verwijderd. In plaats van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Automated Personalization] activiteiten te gebruiken, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit. (Opmerking: Deze leidraad is ook van toepassing op [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.)

### Hoe bouwt Automated Personalization modellen met betrekking tot omgevingen?

Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemene winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep (AP) of ervaring (AT). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

De verzoeken zullen daarom met hetzelfde model worden gediend, ongeacht het milieu, maar de pluraliteit van het verkeer zou van het standaardmilieu moeten komen om ervoor te zorgen dat de geïdentificeerde over het geheel genomen winnende ervaring verenigbaar met echt gedrag is.
