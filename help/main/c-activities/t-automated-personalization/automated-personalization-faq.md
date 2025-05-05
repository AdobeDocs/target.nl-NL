---
keywords: problemen oplossen;veelgestelde vragen;Veelgestelde vragen;Veelgestelde vragen;geautomatiseerde verpersoonlijking;controle;standaardervaring;beste praktijken
description: Ontdek een lijst met veelgestelde vragen (FAQ's) en antwoorden over [!UICONTROL Automated Personalization] (AP) [!UICONTROL Adobe Target].
title: Hoe kan ik veelgestelde vragen vinden over [!UICONTROL Automated Personalization] Activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: 2bf62cc1-1781-4021-a400-2884e0bae893
source-git-commit: 336da9dd876243a0eea662b4604a8fc1e6a69b1a
workflow-type: tm+mt
source-wordcount: '1946'
ht-degree: 0%

---

# Veelgestelde vragen over Automated Personalization

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u werkt met [!UICONTROL Automated Personalization] activiteiten in [!DNL Adobe Target].

## Kan ik een specifieke ervaring specificeren die als controle in een [!UICONTROL Automated Personalization] activiteit?

+++Zie details

U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Zie voor meer informatie [Een specifieke ervaring gebruiken als besturingselement](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

## Hoe kan ik vergelijken? [!UICONTROL Automated Personalization] voor een standaardeigenschap? {#section_46C1A620A2384C2C8392D6716DD18495}

+++Zie details

Er is geen optie voor het vergelijken met een andere toets [!UICONTROL Automated Personalization] in een standaardervaring. Als een oplossing echter een standaardaanbieding of -ervaring bestaat als onderdeel van de algemene activiteit, klikt u op &quot;[!UICONTROL Control]&quot;in rapporten te segmenteren en die specifieke aanbieding te vinden in het resulterende aanbiedingsniveau-rapport. De voor deze aanbieding geregistreerde omrekeningskoers kan worden gebruikt om met het gesprekstarief van het volledige segment &quot;Random Forest&quot; te vergelijken. Dit helpt om te vergelijken hoe de machine in vergelijking met het standaardaanbod doet.

+++

## Wat zijn de beste werkwijzen om een [!UICONTROL Automated Personalization] activiteit? {#section_E155B26282BE49B58EA2683413D11DE6}

+++Zie details

* Als u een laag-verkeerspagina wilt personaliseren, of u wilt structurele veranderingen in de ervaring aanbrengen u zich personaliseert, denk na gebruikend [!UICONTROL Auto-Target] in plaats van [!UICONTROL Automated Personalization]. Zie [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md).
* Overweeg een [!UICONTROL A/B Test] activiteit tussen de aanbiedingen en plaatsen die u in uw wilt gebruiken [!UICONTROL Automated Personalization] activiteiten om ervoor te zorgen dat de locatie en de aanbiedingen van invloed zijn op de optimalisatiedoelstelling. Als een [!UICONTROL A/B Test] de activiteit heeft geen significant verschil aangetoond; [!UICONTROL Automated Personalization] er kan ook geen lift worden gegenereerd.

   * Als een A/B...N test geen statistisch significante verschillen tussen ervaringen toont, is één of meer van de volgende situaties waarschijnlijk verantwoordelijk:

      * De aanbiedingen verschillen waarschijnlijk niet voldoende van elkaar.
      * De locaties die u hebt geselecteerd, hebben geen invloed op de succesmetrische gegevens.
      * Het optimalisatiedoel is te ver in de conversietrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Zorg ervoor dat u de [Verkeersschatting](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) zodat u een idee kunt hebben hoe lang het duurt voor verpersoonlijkingsmodellen om in uw [!UICONTROL Automated Personalization] activiteit.
* Beslis over de toewijzing tussen de controle en gericht alvorens de activiteit te beginnen, die op uw doelstellingen wordt gebaseerd.

  Er zijn drie scenario&#39;s om te overwegen gebaseerd op het doel van uw activiteit en het type van controle u hebt geselecteerd:

   * **Willekeurige Ervaringen als uw controle en uw activiteitendoel is de doeltreffendheid van het verpersoonlijkingsalgoritme te testen**: Als je het personalisatiealgoritme wilt evalueren, wil je een nauwkeuriger beeld van lift hebben. U wilt waarschijnlijk ook vergelijken wat de conversiekoers voor uw ervaringen of aanbiedingen is als u gewoon een [!UICONTROL A/B Test] (een willekeurig bediende controle). In die situatie wordt het gebruik van een 50%-toewijzing voor een controle van willekeurig bediende ervaringen aanbevolen.
   * **&quot;Willekeurige Ervaringen&quot;aangezien uw controle en uw activiteitendoel gepersonaliseerd verkeer moet maximaliseren**: Als u vertrouwd bent met het algoritme en de maximumhoeveelheid verkeer gepersonaliseerd wilt hebben, wordt een 10% tot 30% toewijzing aan controle geadviseerd. De handel hier is de nauwkeurigheid die je in je liftinformatie ziet. De betrouwbaarheidsintervallen van uw controleverkeer zijn groter omdat er minder verkeer dat aan hen stroomt.
   * **Specifieke Ervaring als uw controle, met één van beide doeltype**: Als u een specifieke markeringsgestuurde ervaring wilt vergelijken met de personalisatiemodellen, wordt een 10 tot 30%-toewijzing voor controle aanbevolen. Wanneer u slechts één ervaring als controle selecteert, wordt dat verkeer niet verspreid over elke aanbieding of ervaring in de activiteit.

* De gerichte regels zouden zo spaarzaam mogelijk moeten worden gebruikt omdat zij het vermogen van het model om te optimaliseren kunnen verhinderen.
* Rapporterende groepen kunnen het succes van uw [!UICONTROL Automated Personalization] activiteit. Gebruik alleen rapportgroepen onder specifieke omstandigheden:

   * Gebruik alleen rapportgroepen als aan de volgende voorwaarden is voldaan:

      * U bent van plan nieuwe aanbiedingen te vervangen of toe te voegen terwijl de activiteit loopt.
      * De aanbiedingen in de rapportagegroep doen een beroep op dezelfde bezoekers.
      * De aanbiedingen in die rapportagegroep hebben ongeveer hetzelfde totale responspercentage.

   * Er is geen personalisatie tussen aanbiedingen in een rapportagegroep. De aanbiedingen worden allemaal op dezelfde manier behandeld door het personalisatiemodel.
   * Plaats nooit alle aanbiedingen in een activiteit in één rapporteringsgroep. Hierdoor worden alle aanbiedingen gelijkmatig willekeurig aan alle bezoekers in de activiteit aangeboden.

+++

## Wat zijn enkele limieten in [!UICONTROL Automated Personalization]? {#section_08BA09ED51B547299963C94FE6417CFA}

+++Zie details

[!DNL Target] heeft een harde grens van 30.000 ervaringen, maar het functioneert op zijn best wanneer minder dan 10.000 ervaringen worden gecreeerd.

Deze limiet wordt ook toegepast als de activiteit de optie [!UICONTROL Disalow Duplicates] -optie.

Voor meer informatie over tekengrenzen en andere beperkingen (grootte van aanbieding, publiek, profielen, waarden, parameters, enzovoort) die van invloed zijn op activiteiten en andere elementen in [!DNL Target], zie [Limieten](/help/main/r-troubleshooting-target/target-limits.md).

+++

## Hoe wordt het aanbieden-niveau richten uitgevoerd? {#section_9D7A86EA93D74E9B8C81072A681263A4}

+++Zie details

Wanneer elke bezoeker aankomt, wordt de reeks mogelijke aanbiedingen die de bezoeker kan zien bepaald door de aanbiedingsniveau richtingsregels. Dan, kiest het algoritme de aanbieding die het model voorspelt de beste verwachte opbrengst of de kans van omzetting van onder die aanbiedingen heeft. Het richten van aanbiedingen beïnvloedt de doeltreffendheid van [!DNL Target] machinaal leeralgoritmen en moeten daarom zo spaarzaam mogelijk worden gebruikt.

+++

## Waarom is mijn [!UICONTROL Automated Personalization] activiteit zonder lift aan te geven? {#section_BFA07C8C258F45318F73A461B8F32737}

+++Zie details

Er zijn vier factoren vereist voor een [!UICONTROL Automated Personalization] activiteit om lift te genereren:

* De aanbiedingen op elke locatie moeten verschillend genoeg zijn om de bezoekers te beïnvloeden.
* De locaties moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* De activiteit moet voldoende verkeer en statistische kracht hebben om de lift te kunnen detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages, met behulp van een eenvoudige, niet-gepersonaliseerde [!UICONTROL A/B Test] activiteit. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als uit de resultaten van de A/B-test statistisch significante lift op een of meer ervaringen blijkt, is het waarschijnlijk dat een gepersonaliseerde activiteit succesvol is. Personalisatie kan ook werken als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen of locaties die onvoldoende effect hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

Voor meer informatie, [Problemen met Automated Personalization oplossen](/help/main/c-activities/t-automated-personalization/ap-trouble.md#reference_281954549C3E49E2B5498009BBDC62CA).

+++

## Hoe wordt [!UICONTROL Automated Personalization] het verkeer van mijn activiteit toewijzen? {#section_4369364F77804E0D9B78BEE551DA5659}

+++Zie details

[!UICONTROL Automated Personalization] leidt bezoekers naar de ervaring die het hoogst voorspelde succes metrisch gebaseerd op het meest recente heeft [Willekeurig bos](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) modellen die voor elk model zijn gemaakt. Deze prognose is gebaseerd op de specifieke informatie en de context van het bezoek van de bezoeker.

Stel bijvoorbeeld dat een [!UICONTROL Automated Personalization] de activiteit had twee locaties met elk twee aanbiedingen . Op de eerste locatie wordt voor Offer A een omrekeningskoers van 3% voor een specifieke bezoeker voorspeld en voor Aanbieding B een omrekeningskoers van 1%. Op de tweede locatie wordt voor Offer C een omrekeningskoers van 2% voor dezelfde bezoeker voorspeld, terwijl Offer D een omrekeningskoers van 5% heeft. Daarom [!UICONTROL Automated Personalization] dient deze bezoeker een ervaring met aanbod A en aanbod D.

+++

## Wanneer moet ik mijn [!UICONTROL Automated Personalization] activiteit? {#section_C51F3DAB8887463BB147373F6FE06B93}

+++Zie details

[!UICONTROL Automated Personalization] kan worden gebruikt als &quot;altijd op&quot;verpersoonlijking die constant optimaliseert. Met name voor de meest groene inhoud is het niet nodig om uw [!UICONTROL Automated Personalization] activiteit. Als u wezenlijke veranderingen in de inhoud wilt aanbrengen die niet aan aanbiedingen momenteel in uw zijn [!UICONTROL Automated Personalization] de beste praktijk is om een nieuwe activiteit te starten . Het starten van een nieuwe activiteit helpt andere gebruikers die rapporten evalueren om vroegere resultaten met verschillende inhoud niet te verwarren of met elkaar in verband te brengen.

+++

## Hoe lang moet ik wachten op modellen om te bouwen? {#section_6F6A5A9DB3564BE6B22FFEDFA5B29619}

+++Zie details

De tijd het voor modellen neemt om in uw activiteit te bouwen hangt typisch van het verkeer aan uw geselecteerde activiteitenplaatsen en uw metrisch van het activiteitensucces af. Gebruik de [Verkeersschatting](/help/main/c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714) om de verwachte tijdsduur te bepalen het voor modellen om in uw activiteit te bouwen vergt.

+++

## Eén model is gebouwd in mijn [!UICONTROL Automated Personalization] activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd? {#section_51EA953C6D1D4A3185FC9DD290D66621}

+++Zie details

Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

+++

## Wanneer kan ik naar de resultaten van mijn [!UICONTROL Automated Personalization] activiteit? {#section_05DB5ACAE6AD429C9510766A7268EE2C}

+++Zie details

U kunt beginnen naar de resultaten van uw [!UICONTROL Automated Personalization] activiteit nadat u minstens twee ervaringen met gebouwde modellen (groen vinkje) voor de ervaring hebt die modellen heeft gebouwd.

+++

## Hoe kan ik de tijd verminderen die nodig is om modellen op te bouwen in mijn [!UICONTROL Automated Personalization] activiteit? {#section_CCB8CEE98DAA40BA93AADCD596C48D82}

+++Zie details

Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen bouwen.

* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting verhoogt de verkeersvereisten nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen.
* Zijn er sommige ervaringen die u uit uw activiteit kunt laten vallen? Door het aantal ervaringen in een activiteit te verminderen, duurt het langer om modellen te bouwen.
* Is er een hoger-verkeerspagina waar deze activiteit succesvoller zou zijn? De meer verkeer en omzettingen in uw activiteitenplaatsen, bouwen de snellere modellen.

+++

## Waarom zien bezoekers ervaringen voor een [!UICONTROL Automated Personalization] activiteit die ze niet zouden moeten zien? {#section_41CECEAE0881446A8D9F3B016857914B}

+++Zie details

[!UICONTROL Automated Personalization] de activiteiten worden één keer per sessie geëvalueerd . Als er actieve sessies zijn die in aanmerking komen voor een bepaalde ervaring en er nu nieuwe aanbiedingen aan zijn toegevoegd, zien bezoekers de nieuwe inhoud samen met de eerder weergegeven aanbiedingen. Omdat deze bezoekers eerder gekwalificeerd waren voor die ervaringen, zien ze die ervaringen nog tijdens de sessie. Als u dit tijdens elk paginabezoek wilt beoordelen, gaat u naar [!UICONTROL Experience Targeting] (XT) type activiteit.

+++

## Kan ik het doel metrisch halverwege veranderen door een [!UICONTROL Automated Personalization] activiteit? {#change-metric}

+++Zie details

[!DNL Adobe] adviseert niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om het doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. [!DNL Adobe] niet garantie wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling geldt voor [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] activiteiten die [!DNL Target] of [!DNL Analytics] (A4T) als bron van rapportage.

+++

## Kan ik de [!UICONTROL Reset Report Data] optie tijdens het uitvoeren van een [!UICONTROL Automated Personalization] activiteit?

+++Zie details

[!DNL Adobe] raadt u niet aan het [!UICONTROL Reset Report Data] optie voor [!UICONTROL Automated Personalization] activiteiten. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords verwijderd uit het dialoogvenster [!UICONTROL Automated Personalization] model. In plaats van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Automated Personalization] , een nieuwe activiteit maken en de oorspronkelijke activiteit deactiveren. Deze leidraad geldt ook voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.

+++

## Hoe werkt [!UICONTROL Automated Personalization] modellen ontwikkelen met betrekking tot omgevingen?

+++Zie details

Één model wordt gebouwd om de prestaties van de gepersonaliseerde strategie tegenover willekeurig gediend verkeer tegenover het verzenden van al verkeer naar het algemeen het winnen ervaring te identificeren. In dit model worden alleen resultaten en omzettingen in de standaardomgeving bekeken.

Het verkeer van een tweede reeks modellen wordt gebouwd voor elke modelleringsgroep ([!UICONTROL Automated Personalization]) of ervaring ([!UICONTROL Auto-Target]). Voor elk van deze modellen worden hits en conversies in alle omgevingen in overweging genomen.

De verzoeken worden daarom met hetzelfde model behandeld, ongeacht het milieu. De pluraliteit van het verkeer moet echter afkomstig zijn uit de standaardomgeving om ervoor te zorgen dat de geïdentificeerde overkoepelende ervaring consistent is met het gedrag in de praktijk.

+++
