---
keywords: autotarget;het richten;verkeerstoewijzing;vaak gestelde vragen;faq;het oplossen van problemen;het oplossen van problemen;verkeer
description: Onderzoek het oplossen van problemenonderwerpen en Veelgestelde Vragen over activiteiten Auto-Target in Adobe Target.
title: Hoe kan ik auto-doelactiviteiten problemen oplossen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 0%

---

# Veelgestelde vragen en problemen automatisch oplossen

Problemen oplossen en veelgestelde vragen (FAQ&#39;s) over [!UICONTROL Auto-Target] activiteiten in [!DNL Adobe Target].

## [!UICONTROL Auto-Target] Veelgestelde vragen {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u werkt met [!UICONTROL Auto-Target] activiteiten:

### Wat zijn de beste werkwijzen om een [!UICONTROL Auto-Target] activiteit?

+++Antwoord
* Bepalen of de bedrijfswaarde van een [!UICONTROL Revenue per Visit] (RPV) succes metrisch is de extra verkeersvereisten waard. RPV heeft doorgaans minstens 1.000 conversies per ervaring nodig om een activiteit te kunnen gebruiken in plaats van conversie.
* Beslis over de toewijzing tussen controle en gepersonaliseerde ervaringen alvorens met de activiteit te beginnen die op uw doelstellingen wordt gebaseerd.
* Bepaal of u voldoende verkeer hebt naar de pagina waar uw [!UICONTROL Auto-Target] de activiteit zal voor verpersoonlijkingsmodellen lopen om in een redelijke hoeveelheid tijd op te bouwen.
   * Als u het verpersoonlijkingsalgoritme test, zou u geen ervaringen moeten veranderen of profielattributen toevoegen of verwijderen terwijl de activiteit levend is.

* U kunt een A/B-activiteit uitvoeren tussen de aanbiedingen en locaties die u in uw [!UICONTROL Auto-Target] activiteiten om ervoor te zorgen dat de locaties en aanbiedingen van invloed zijn op de optimalisatiedoelstelling. Indien een A/B-activiteit geen significant verschil aantoont, [!UICONTROL Auto-Target] er zal waarschijnlijk ook geen lift worden gegenereerd .

   * Als een A/B test geen statistisch significante verschillen tussen ervaringen toont, is het waarschijnlijk dat de aanbiedingen u overweegt niet genoeg van elkaar verschillend zijn, beïnvloeden de plaatsen u selecteerde niet succesmetrisch, of het optimalisatiedoel is te ver in de omzettingrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Probeer de ervaringen tijdens de activiteiten niet ingrijpend te wijzigen.

+++

### Wordt Adobe aanbevolen [!UICONTROL Auto Target] met een 90(Control)/10(Targeted) verdeling tot de modellen worden gebouwd?

+++Antwoord Uw optimale verdeling van de verkeerstoewijzing hangt van af wat u wilt verwezenlijken.

Als uw doel is zoveel mogelijk verkeer te personaliseren, kunt u met 90% gerichte toewijzing en 10% controle voor het leven van de activiteit blijven. Als uw doel een experiment is dat vergelijkt hoe goed gepersonaliseerde algoritmen tegenover de controle doen, dan is een 50/50 splitsing best voor het leven van de activiteit.

De beste praktijken moeten het verkeer-verdeling voor het leven van de activiteit handhaven zodat de bezoekers niet tussen gerichte en controleervaringen schakelen.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Als een bezoeker **niet** zie [!UICONTROL Auto-Target] activiteit en converteert, telt de omzetting in mijn activiteit?

+++Antwoord nr., slechts bezoekers die voor kwalificeren en bekijken [!UICONTROL Auto-Target] activiteit wordt meegeteld in de rapportage.

+++

### Waarom niet mijn [!UICONTROL Auto-Target] de activiteit lijkt een lift te genereren .

+++Antwoord Er zijn vier factoren vereist voor een [!UICONTROL Auto-Target] activiteit om lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen.

Als uit de resultaten van een A/B-test statistisch significante resultaten van een of meer ervaringen blijken, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

+++

### Wanneer moet ik mijn [!UICONTROL Auto-Target] activiteit?

+++Antwoord
[!UICONTROL Auto-Target] kan worden gebruikt als &quot;altijd op&quot;verpersoonlijking die constant zal optimaliseren. Met name voor de meest groene inhoud is het niet nodig om uw [!UICONTROL Auto-Target] activiteit.

Als u de inhoud van uw [!UICONTROL Auto-Target] de beste manier is om een nieuwe activiteit te starten zodat andere gebruikers die rapporten evalueren, eerdere resultaten niet verwarren of met andere inhoud in verband brengen.

+++

### Hoe lang moet ik wachten op modellen om te bouwen? {#how-long}

++ + Antwoord De tijd die nodig is om modellen op te bouwen in uw [!UICONTROL Auto-Target] activiteit hangt typisch van het verkeer aan uw geselecteerde activiteitenplaatsen en omzettingen verbonden aan uw metrisch van het activiteitensucces af.

[!UICONTROL Auto-Target] probeert niet om een gepersonaliseerd model voor een bepaalde ervaring te bouwen tot er minstens 50 omzettingen voor die ervaring zijn. Bovendien, als het gebouwde model van ontoereikende kwaliteit is (zoals bepaald door off-line evaluatie van &quot;test&quot;gegevens van de greep, die [een metrisch die als AUC wordt bekend](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), wordt het model niet gebruikt om verkeer op een gepersonaliseerde manier te dienen.

Enkele andere punten die u in gedachten wilt houden [!UICONTROL Auto-Target]Modelgebouw:

* Wanneer een activiteit actief is, [!UICONTROL Auto-Target] overweegt tot de laatste 45 dagen van willekeurig gediende gegevens wanneer het proberen om modellen (bijvoorbeeld, controleverkeer, plus sommige extra willekeurig gediende gegevens die door het algoritme worden gehouden) te bouwen.
* Wanneer [!UICONTROL Revenue per Visit] Is uw succes metrisch, deze activiteiten vereisen typisch meer gegevens om modellen te bouwen wegens de hogere gegevensvariantie die typisch in bezoek-opbrengst in vergelijking met omzettingspercentage bestaat.
* Omdat de modellen op een per-ervaringsbasis worden voortgebouwd, betekent het vervangen van één ervaring met een andere ervaring dat voldoende verkeer (minstens 50 omzettingen) voor de nieuwe ervaring moet worden verzameld alvorens de gepersonaliseerde modellen kunnen worden herbouwd.

+++

### Eén model is ingebouwd in mijn activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd?

+++Antwoord nr, er moeten minstens twee modellen binnen uw activiteit worden gebouwd voor verpersoonlijking beginnen.

+++

### Wanneer kan ik beginnen te kijken naar de resultaten van mijn [!UICONTROL Auto-Target] activiteit?

+++Antwoord U kunt beginnen bekijkend de resultaten van uw [!UICONTROL Auto-Target] test nadat u minstens twee ervaringen met gebouwde modellen hebt (groen vinkje) voor de ervaring die modellen heeft gebouwd.

+++

### Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?

+++Antwoord U kunt een ervaring selecteren die als controle wordt gebruikt terwijl het creëren van een [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het verkeer-toewijzingspercentage wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Zie voor meer informatie [Een specifieke ervaring gebruiken als besturingselement](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Kan ik het doel metrisch halverwege veranderen door een [!UICONTROL Auto-Target] activiteit? {#change-metric}

+++Antwoord Adobe adviseert niet dat u het doel metrisch midden door een activiteit verandert. Hoewel het mogelijk is om het doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. Wij garanderen niet wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] activiteiten die [!DNL Target] of [!DNL Analytics] (A4T) als bron van rapportage.

+++

### Kan ik de [!UICONTROL Reset Report Data] optie tijdens het uitvoeren van een [!UICONTROL Auto-Target] activiteit?

+++Antwoord gebruiken [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Target] activiteiten worden niet voorgesteld. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords verwijderd uit de [!UICONTROL Auto-Target] model. In plaats van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Target] activiteiten, een nieuwe activiteit creëren en de oorspronkelijke activiteit deactiveren.

Deze leidraad geldt ook voor [!UICONTROL Auto-Allocate] en [!UICONTROL Automated Personalization] activiteiten.

+++

### Wat gebeurt er als ik één ervaring uit een [!UICONTROL Auto-Target] activiteit?

+++Antwoord
[!DNL Target] bouwt één model per ervaring, zodat het verwijderen van één ervaringsmiddel [!DNL Target] bouwt één minder model en zal geen modellen voor de andere ervaringen beïnvloeden.

Stel dat u een [!UICONTROL Auto-Target] activiteit met acht ervaringen en u houdt niet van de prestaties van één ervaring. U kunt die ervaring verwijderen en het beïnvloedt niet de modellen voor de zeven resterende ervaringen.

+++

## Problemen oplossen [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Soms gaan activiteiten niet zoals verwacht. Hier zijn enkele potentiële uitdagingen waarmee u kunt worden geconfronteerd wanneer u het gebruik van [!UICONTROL Auto-Target] en enkele voorgestelde oplossingen.

### Mijn [!UICONTROL Auto-Target] het duurt te lang om modellen te bouwen .

+++suggesties voor probleemoplossing Er zijn verschillende wijzigingen in de activiteiteninstellingen die de verwachte tijd voor het samenstellen van modellen kunnen verminderen, waaronder het aantal ervaringen in uw [!UICONTROL Auto-Target] activiteit, het verkeer aan uw plaats, en uw geselecteerd succes metrisch.

**Oplossing:** Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen zullen bouwen.

* Als uw succesmetrisch wordt geplaatst aan [!UICONTROL RPV], kunt u overschakelen op conversie? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest geen activiteitsgegevens als u de succesmaatstaf wijzigt van RPV in Conversie.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lagere tarief van de activiteitenomzetting verhoogt de verkeersvereisten nodig voor modellen om te bouwen, omdat een minimumaantal omzettingen wordt vereist.
* Zijn er sommige ervaringen u van uw activiteit kunt laten vallen? Het verminderen van het aantal ervaringen in een activiteit vermindert de tijd om modellen te bouwen.
* Is er een pagina voor hoger verkeer waarop deze activiteit succesvoller zou zijn? Hoe meer verkeer en conversies er in uw activiteitenlocaties plaatsvinden, hoe sneller de modellen worden.

+++

### Mijn [!UICONTROL Auto-Target] activiteit genereert geen lift.

+++Suggesties voor probleemoplossing Er zijn vier factoren vereist voor een AT-activiteit om een lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** Eerst, zorg ervoor dat uw activiteit verkeer personaliseert. Als modellen niet voor alle ervaringen worden gebouwd, [!UICONTROL Auto-Target] de activiteit bedient nog steeds willekeurig een aanzienlijk deel van de bezoeken om te proberen alle modellen zo snel mogelijk te bouwen . Als modellen niet zijn gebouwd, [!UICONTROL Auto-Target] is geen personaliserend verkeer.

Daarna, zorg ervoor de aanbiedingen en de activiteitenplaatsen werkelijk een verschil aan de algemene reactiesnelheden gebruikend een eenvoudige, niet-gepersonaliseerde test A/B maken. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als een A/B-testresultaten statistisch significante lift op een of meer van de ervaringen laten zien, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen en locaties die niet voldoende effect hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

+++

### Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om.

+++Suggesties voor probleemoplossing Dit wordt verwacht.

In een [!UICONTROL Auto-Target] activiteit, zodra een omzettingsmetrisch (of optimalisatiedoel of post doel) wordt omgezet, wordt de gebruiker vrijgegeven van de ervaring en de activiteit is opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat zodra C1 wordt omgezet, de bezoeker wordt vrijgegeven.

+++
