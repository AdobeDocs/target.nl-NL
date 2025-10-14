---
keywords: problemen oplossen;veelgestelde vragen;Veelgestelde vragen;Veelgestelde vragen;geautomatiseerde verpersoonlijking;controle;standaardervaring;beste praktijken
description: Ontdek een lijst met veelgestelde vragen (FAQ's) en antwoorden op [!UICONTROL Automated Personalization] (AP)-activiteiten in [!UICONTROL Adobe Target] .
title: Hoe kan ik veelgestelde vragen over [!UICONTROL Automated Personalization] activiteiten vinden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 0%

---

# Veelgestelde vragen over Automated Personalization

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u werkt met [!UICONTROL Automated Personalization] -activiteiten in [!DNL Adobe Target] .

## Kan ik een specifieke ervaring specificeren die als controle in een [!UICONTROL Automated Personalization] activiteit moet worden gebruikt?

+++Zie details

U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Voor meer informatie, zie [&#x200B; Gebruik een specifieke ervaring als controle &#x200B;](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## Hoe kan ik [!UICONTROL Automated Personalization] vergelijken met een standaardervaring? {#section_46C1A620A2384C2C8392D6716DD18495}

+++Zie details

Er is geen optie om [!UICONTROL Automated Personalization] te vergelijken met een standaardervaring. Nochtans, als een oplossing, als een standaardaanbieding of een ervaring als deel van de algemene activiteit bestaat, om zijn basislijnprestaties te begrijpen, klik het &quot;[!UICONTROL Control]&quot;segment in rapporten en bepaal de plaats van die bepaalde aanbieding in het resulterende aanbod-vlakke rapport. De voor deze aanbieding geregistreerde omrekeningskoers kan worden gebruikt om met het gesprekstarief van het volledige segment &quot;Random Forest&quot; te vergelijken. Dit helpt om te vergelijken hoe de machine in vergelijking met het standaardaanbod doet.

+++

## Wat zijn de beste werkwijzen om een [!UICONTROL Automated Personalization] activiteit op te zetten? {#section_E155B26282BE49B58EA2683413D11DE6}

+++Zie details

* Als u een pagina met minder verkeer wilt aanpassen, of u wilt structurele veranderingen in de ervaring aanbrengen u zich personaliseert, denk na gebruikend een [!UICONTROL Auto-Target] activiteit in plaats van [!UICONTROL Automated Personalization]. Zie [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* U kunt overwegen een [!UICONTROL A/B Test] -activiteit uit te voeren tussen de aanbiedingen en locaties die u wilt gebruiken in uw [!UICONTROL Automated Personalization] -activiteit om ervoor te zorgen dat de locatie en aanbiedingen een invloed hebben op de optimalisatiedoelstelling. Als een [!UICONTROL A/B Test] -activiteit geen significant verschil aantoont, genereert [!UICONTROL Automated Personalization] waarschijnlijk ook geen lift.

   * Als een A/B...N test geen statistisch significante verschillen tussen ervaringen toont, is één of meer van de volgende situaties waarschijnlijk verantwoordelijk:

      * De aanbiedingen verschillen waarschijnlijk niet voldoende van elkaar.
      * De locaties die u hebt geselecteerd, hebben geen invloed op de succesmetrische gegevens.
      * Het optimalisatiedoel is te ver in de conversietrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Zorg ervoor om de [&#x200B; schatter van het Verkeer &#x200B;](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) te gebruiken zodat kunt u een gevoel van hebben hoe lang het voor verpersoonlijkingsmodellen duurt om in uw [!UICONTROL Automated Personalization] activiteit te bouwen.
* Beslis over de toewijzing tussen de controle en gericht alvorens de activiteit te beginnen, die op uw doelstellingen wordt gebaseerd.

  Er zijn drie scenario&#39;s om te overwegen gebaseerd op het doel van uw activiteit en het type van controle u hebt geselecteerd:

   * **Willekeurige Ervaringen als uw controle en uw activiteitendoel is de doeltreffendheid van het verpersoonlijkingsalgoritme** te testen: Als uw doel het verpersoonlijkingsalgoritme moet evalueren, wilt u een nauwkeuriger beeld van lift hebben. U wilt waarschijnlijk ook vergelijken wat de conversiekoers voor uw ervaringen of aanbiedingen is als u gewoon een [!UICONTROL A/B Test] (een willekeurig bediende controle) doet. In die situatie wordt het gebruik van een 50%-toewijzing voor een controle van willekeurig bediende ervaringen aanbevolen.
   * **&quot;Willekeurige Ervaringen&quot;aangezien uw controle en uw activiteitendoel gepersonaliseerd verkeer** moet maximaliseren: Als u met het algoritme comfortabel bent en de maximumhoeveelheid gepersonaliseerd verkeer wilt hebben, wordt een 10% tot 30% toewijzing aan controle geadviseerd. De handel hier is de nauwkeurigheid die je in je liftinformatie ziet. De betrouwbaarheidsintervallen van uw controleverkeer zijn groter omdat er minder verkeer dat aan hen stroomt.
   * **Specifieke Ervaring als uw controle, met één van beide doeltype**: Als u een specifieke marketer-gedreven ervaring met de verpersoonlijkingsmodellen wilt vergelijken, wordt een 10% tot 30% toewijzing geadviseerd om te controleren. Wanneer u slechts één ervaring als controle selecteert, wordt dat verkeer niet verspreid over elke aanbieding of ervaring in de activiteit.

* De gerichte regels zouden zo spaarzaam mogelijk moeten worden gebruikt omdat zij het vermogen van het model om te optimaliseren kunnen verhinderen.
* Het rapporteren van groepen kan het succes van uw [!UICONTROL Automated Personalization] activiteit beperken. Gebruik alleen rapportgroepen onder specifieke omstandigheden:

   * Gebruik alleen rapportgroepen als aan de volgende voorwaarden is voldaan:

      * U bent van plan nieuwe aanbiedingen te vervangen of toe te voegen terwijl de activiteit loopt.
      * De aanbiedingen in de rapportagegroep doen een beroep op dezelfde bezoekers.
      * De aanbiedingen in die rapportagegroep hebben ongeveer hetzelfde totale responspercentage.

   * Er is geen personalisatie tussen aanbiedingen in een rapportagegroep. De aanbiedingen worden allemaal op dezelfde manier behandeld door het personalisatiemodel.
   * Plaats nooit alle aanbiedingen in een activiteit in één rapporteringsgroep. Hierdoor worden alle aanbiedingen gelijkmatig willekeurig aan alle bezoekers in de activiteit aangeboden.

+++

## Wat zijn enkele limieten in [!UICONTROL Automated Personalization] ? {#section_08BA09ED51B547299963C94FE6417CFA}

+++Zie details

[!DNL Target] heeft een harde limiet van 30.000 ervaringen, maar het werkt op zijn best als er minder dan 10.000 ervaringen zijn gemaakt.

Deze limiet wordt ook toegepast wanneer de activiteit de optie [!UICONTROL Disalow Duplicates] heeft ingeschakeld.

Voor meer informatie over karaktergrenzen en andere grenzen (aanbiedingsgrootte, publiek, profielen, waarden, parameters, enzovoort) die activiteiten en andere elementen in [!DNL Target] beïnvloeden, zie [&#x200B; Grenzen &#x200B;](/help/main/r-troubleshooting-target/target-limits.md).

+++

## Hoe wordt het aanbieden-niveau richten uitgevoerd? {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++Zie details

Wanneer elke bezoeker aankomt, wordt de reeks mogelijke aanbiedingen die de bezoeker kan zien bepaald door de aanbiedingsniveau richtingsregels. Dan, kiest het algoritme de aanbieding die het model voorspelt de beste verwachte opbrengst of de kans van omzetting van onder die aanbiedingen heeft. Aanbieding gericht op effecten op de effectiviteit van leeralgoritmen voor machines van [!DNL Target] en moet daarom zo spaarzaam mogelijk worden gebruikt.

+++

## Waarom laat mijn [!UICONTROL Automated Personalization] activiteit geen lift zien? {#section_BFA07C8C258F45318F73A461B8F32737}

+++Zie details

Er zijn vier factoren vereist voor een [!UICONTROL Automated Personalization] -activiteit om een lift te genereren:

* De aanbiedingen op elke locatie moeten verschillend genoeg zijn om de bezoekers te beïnvloeden.
* De locaties moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* De activiteit moet voldoende verkeer en statistische kracht hebben om de lift te kunnen detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier om actie te ondernemen is om er eerst voor te zorgen dat de inhoud en de locaties waaruit de ervaringen met activiteiten bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde [!UICONTROL A/B Test] activiteit. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als uit de resultaten van de A/B-test statistisch significante lift op een of meer ervaringen blijkt, is het waarschijnlijk dat een gepersonaliseerde activiteit succesvol is. Personalization kan ook werken als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen of locaties die onvoldoende effect hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

Voor meer informatie, [&#x200B; het Oplossen van problemen Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## Hoe wijst [!UICONTROL Automated Personalization] het verkeer van mijn activiteit toe? {#section_4369364F77804E0D9B78BEE551DA5659}

+++Zie details

[!UICONTROL Automated Personalization] routes bezoekers aan de ervaring die hoogste voorspelde succes metrisch heeft die op de meest recente [&#x200B; wordt gebaseerd Willekeurig bos &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) modellen die voor elk model worden gebouwd. Deze prognose is gebaseerd op de specifieke informatie en de context van het bezoek van de bezoeker.

Stel dat een [!UICONTROL Automated Personalization] -activiteit twee locaties had met elk twee aanbiedingen. Op de eerste locatie wordt voor Offer A een omrekeningskoers van 3% voor een specifieke bezoeker voorspeld en voor Aanbieding B een omrekeningskoers van 1%. Op de tweede locatie wordt voor Offer C een omrekeningskoers van 2% voor dezelfde bezoeker voorspeld, terwijl Offer D een omrekeningskoers van 5% heeft. Daarom biedt [!UICONTROL Automated Personalization] deze bezoeker een ervaring met aanbod A en aanbod D.

+++

## Wanneer moet ik mijn [!UICONTROL Automated Personalization] activiteit stoppen? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++Zie details

[!UICONTROL Automated Personalization] kan worden gebruikt als &#39;altijd aan&#39; personalisatie die constant optimaliseert. Met name voor steeds groene inhoud is het niet nodig om de [!UICONTROL Automated Personalization] -activiteit te stoppen. Als u substantiële wijzigingen wilt aanbrengen in de inhoud die niet overeenkomen met de aanbiedingen die momenteel in uw [!UICONTROL Automated Personalization] -activiteit worden aangeboden, kunt u het beste een nieuwe activiteit starten. Het starten van een nieuwe activiteit helpt andere gebruikers die rapporten evalueren om vroegere resultaten met verschillende inhoud niet te verwarren of met elkaar in verband te brengen.

+++

## Hoe lang moet ik wachten op modellen om te bouwen? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++Zie details

De tijd het voor modellen neemt om in uw activiteit te bouwen hangt typisch van het verkeer aan uw geselecteerde activiteitenplaatsen en uw metrisch van het activiteitensucces af. Gebruik de [&#x200B; schatter van het Verkeer &#x200B;](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) om de verwachte lengte van tijd te bepalen het voor modellen neemt om in uw activiteit te bouwen.

+++

## Eén model is gemaakt binnen mijn [!UICONTROL Automated Personalization] activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++Zie details

Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

+++

## Wanneer kan ik naar de resultaten van mijn [!UICONTROL Automated Personalization] activiteit kijken? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++Zie details

U kunt de resultaten van uw [!UICONTROL Automated Personalization] activiteit bekijken nadat u minstens twee ervaringen met gebouwde modellen (groen controleteken) voor de ervaring hebt gehad die modellen heeft gebouwd.

+++

## Hoe kan ik de tijd die nodig is om modellen te laten bouwen in mijn [!UICONTROL Automated Personalization] activiteit verminderen? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++Zie details

Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen bouwen.

* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting verhoogt de verkeersvereisten nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen.
* Zijn er sommige ervaringen die u uit uw activiteit kunt laten vallen? Door het aantal ervaringen in een activiteit te verminderen, duurt het langer om modellen te bouwen.
* Is er een hoger-verkeerspagina waar deze activiteit succesvoller zou zijn? De meer verkeer en omzettingen in uw activiteitenplaatsen, bouwen de snellere modellen.

+++

## Waarom zien bezoekers ervaringen voor een [!UICONTROL Automated Personalization] activiteit die ze niet zouden moeten zien? {#section_41CECEAE0881446A8D9F3B016857914B}

+++Zie details

[!UICONTROL Automated Personalization] -activiteiten worden één keer per sessie geëvalueerd. Als er actieve sessies zijn die in aanmerking komen voor een bepaalde ervaring en er nu nieuwe aanbiedingen aan zijn toegevoegd, zien bezoekers de nieuwe inhoud samen met de eerder weergegeven aanbiedingen. Omdat deze bezoekers eerder gekwalificeerd waren voor die ervaringen, zien ze die ervaringen nog tijdens de sessie. Als u dit tijdens elk paginabezoek wilt evalueren, wijzigt u het activiteitstype [!UICONTROL Experience Targeting] (XT).

+++

## Kan ik het doel metrisch halverwege door een [!UICONTROL Automated Personalization] activiteit veranderen? {#change-metric}

+++Zie details

[!DNL Adobe] adviseert niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. [!DNL Adobe] garandeert niet wat er gebeurt als u het doel metrisch wijzigt in een activiteit nadat deze is uitgevoerd.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate] -, [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -activiteiten die [!DNL Target] - of [!DNL Analytics] (A4T) gebruiken als rapportagebron.

+++

## Kan ik de optie [!UICONTROL Reset Report Data] gebruiken tijdens het uitvoeren van een [!UICONTROL Automated Personalization] -activiteit?

+++Zie details

[!DNL Adobe] raadt het gebruik van de optie [!UICONTROL Reset Report Data] voor [!UICONTROL Automated Personalization] -activiteiten niet aan. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords uit het [!UICONTROL Automated Personalization] -model verwijderd. In plaats van de optie [!UICONTROL Reset Report Data] te gebruiken voor [!UICONTROL Automated Personalization] -activiteiten, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit. Deze handleiding is ook van toepassing op [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten.

+++

## Hoe bouwt [!UICONTROL Automated Personalization] modellen met betrekking tot milieu&#39;s?

+++Zie details

Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemeen het winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep ([!UICONTROL Automated Personalization]) of ervaring ([!UICONTROL Auto-Target]). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

De verzoeken worden daarom met hetzelfde model behandeld, ongeacht het milieu. De pluraliteit van het verkeer moet echter afkomstig zijn uit de standaardomgeving om ervoor te zorgen dat de geïdentificeerde overkoepelende ervaring consistent is met het gedrag in de praktijk.

+++
