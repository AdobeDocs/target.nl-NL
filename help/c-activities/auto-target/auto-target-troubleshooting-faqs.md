---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting
description: Problemen oplossen en Veelgestelde vragen over automatisch doel in Adobe Target.
title: Automatische probleemoplossing en veelgestelde vragen
feature: auto-target
topic: Standard
translation-type: tm+mt
source-git-commit: e18f18e6d6e0b8fc6eb5ada845e2fe5377d6c5d0
workflow-type: tm+mt
source-wordcount: '1722'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Auto-Target Problemen oplossen en Veelgestelde vragen

Problemen oplossen en veelgestelde vragen (FAQ&#39;s) over [!UICONTROL Auto-Target] in [!DNL Adobe Target].

## Veelgestelde vragen over automatisch doel {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u met [!UICONTROL Auto-Target] activiteiten werkt:

### Wat zijn de beste praktijken om een [!UICONTROL Auto-Target] activiteit te vestigen?

* Beslissen of de bedrijfswaarde van een (RPV) succesmetrisch van de Inkomsten per Bezoek de extra verkeersvereisten waard is. RPV heeft doorgaans minstens 1.000 conversies per ervaring nodig om een activiteit te kunnen gebruiken in plaats van conversie.
* Beslis over de toewijzing tussen controle en gepersonaliseerde ervaringen alvorens met de activiteit te beginnen die op uw doelstellingen wordt gebaseerd.
* Bepaal als u voldoende verkeer aan de pagina hebt waar uw [!UICONTROL Auto-Target] activiteit voor verpersoonlijkingsmodellen zal lopen om in een redelijke hoeveelheid tijd te bouwen.
   * Als u het verpersoonlijkingsalgoritme test, moet u geen ervaringen veranderen of profielkenmerken toevoegen/verwijderen terwijl de activiteit actief is.

* Overweeg een A/B activiteit tussen de aanbiedingen en plaatsen te voltooien u in uw [!UICONTROL Auto-Target] activiteit van plan bent te gebruiken om te verzekeren de plaats(en) en de aanbiedingen een effect op het optimalisatiedoel hebben. Als een A/B-activiteit geen significant verschil aantoont, zal het [!UICONTROL Auto-Target] waarschijnlijk ook niet lukken om een lift te genereren.

   * Als een A/B test geen statistisch significante verschillen tussen ervaringen toont, is het waarschijnlijk dat de aanbiedingen u overweegt niet genoeg van elkaar verschillend zijn, beïnvloeden de plaatsen u selecteerde niet succesmetrisch, of het optimalisatiedoel is te ver in de omzettingrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Probeer de ervaringen tijdens de activiteiten niet ingrijpend te wijzigen.

### Zijn de vinkjes die erop wijzen dat een model voor die ervaring wordt gebouwd update als de waaier van de rapportdatum verandert?

Nee, de vinkjes voor het genereren van modellen geven alleen de modellen weer die tot op heden zijn gemaakt. Er is geen manier om terug te gaan en te zien wanneer een model werd voltooid.

### Als een bezoeker de [!UICONTROL Auto-Target] activiteit NIET ziet en omzet, telt de omzetting in mijn activiteit?

Nee, alleen bezoekers die in aanmerking komen voor de [!UICONTROL Auto-Target] activiteit worden meegeteld in de rapportage.

### Mijn [!UICONTROL Auto-Target] activiteit lijkt geen lift te genereren. Wat is er aan de hand?

Er zijn vier factoren vereist voor een [!UICONTROL Auto-Target] activiteit om lift te produceren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen.

Als uit de resultaten van een A/B-test statistisch significante resultaten van een of meer ervaringen blijken, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

### Wanneer moet ik mijn [!UICONTROL Auto-Target] activiteit stopzetten?

[!UICONTROL Auto-Target] kan worden gebruikt als &quot;altijd op&quot;verpersoonlijking die constant zal optimaliseren. Met name voor de groengroene inhoud is het niet nodig om uw [!UICONTROL Auto-Target] activiteit te stoppen.

Als u substantiële wijzigingen wilt aanbrengen in de inhoud van uw [!UICONTROL Auto-Target] activiteit, kunt u het beste een nieuwe activiteit starten zodat andere gebruikers die rapporten controleren, oude resultaten niet verwarren of met andere inhoud in verband brengen.

### Hoe lang moet ik wachten op modellen om te bouwen? {#how-long}

De tijdsduur die het voor modellen vergt om in uw [!UICONTROL Auto-Target] activiteit te bouwen hangt typisch van het verkeer aan uw geselecteerde activiteitenplaats(en) en omzettingspercentages verbonden aan u metrische activiteit af.

[!UICONTROL Auto-Target] zal niet proberen om een gepersonaliseerd model voor een bepaalde ervaring te bouwen tot er minstens 50 omzettingen voor die ervaring zijn. Bovendien als het gebouwde model van ontoereikende kwaliteit is (zoals die door off-line evaluatie op greep &quot;test&quot;gegevens wordt bepaald, gebruikend metrisch die als AUC [](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)wordt bekend), zal het model niet worden gebruikt om verkeer op een gepersonaliseerde manier te dienen.

Nog enkele punten die u in gedachten wilt houden over [!UICONTROL Auto-Target]het modelgebouw:

* Zodra een activiteit levend is, [!UICONTROL Auto-Target] overweegt tot de laatste 45 dagen van willekeurig gediende gegevens wanneer het proberen om modellen (d.w.z. controleverkeer, plus sommige extra willekeurig gediende gegevens die door ons algoritme worden gehouden) te bouwen.
* Wanneer [!UICONTROL Revenue per Visit] uw succes metrisch is, vereisen deze activiteiten typisch meer gegevens om modellen te bouwen wegens de hogere gegevensvariantie die typisch in bezoek-opbrengst in vergelijking met omzettingspercentage bestaat.
* Omdat de modellen op een per-ervaringsbasis worden voortgebouwd, die één ervaring met een andere middelen vervangen die voldoende verkeer (d.w.z. minstens 50 omzettingen) voor de nieuwe ervaring moeten worden verzameld alvorens de gepersonaliseerde modellen kunnen worden herbouwd.

### Eén model is ingebouwd in mijn activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd?

Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

### Wanneer kan ik naar de resultaten van mijn [!UICONTROL Auto-Target] activiteit gaan kijken?

U kunt de resultaten van uw [!UICONTROL Auto-Target] test bekijken nadat u minstens twee ervaringen met gebouwde modellen hebt (groen vinkje) voor de ervaring die modellen heeft gebouwd.

### Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?

U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Auto-Doel](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Zie Een specifieke ervaring [gebruiken als controle](/help/c-activities/t-automated-personalization/experience-as-control.md)voor meer informatie.

### Kan ik het doel metrische middenweg door een auto-Doelactiviteit veranderen? {#change-metric}

Wij adviseren niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. Wij garanderen niet wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target]en [!UICONTROL Automated Personalization] activiteiten die ofwel [!DNL Target] of [!DNL Analytics] (A4T) als rapportagebron gebruiken.

### Kan ik de optie Rapportgegevens opnieuw instellen gebruiken tijdens het uitvoeren van een automatisch doelactiviteit?

Het gebruik van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Target] activiteiten wordt niet voorgesteld. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords uit het [!UICONTROL Auto-Target] model verwijderd. In plaats van de [!UICONTROL Reset Report Data] optie voor [!UICONTROL Auto-Target] activiteiten te gebruiken, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit. (Opmerking: Deze leidraad is ook van toepassing op [!UICONTROL Auto-Allocate] en [!UICONTROL Automated Personalization] activiteiten.)

## Problemen oplossen [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen die u tijdens het gebruik kunt aangaan [!UICONTROL Auto-Target], en enkele voorgestelde oplossingen.

### Mijn [!UICONTROL Auto-Target] activiteit duurt te lang om modellen te bouwen.

Er zijn verscheidene veranderingen van de activiteitenopstelling die de verwachte tijd kunnen verminderen om modellen te bouwen, met inbegrip van het aantal ervaringen in uw [!UICONTROL Auto-Target] activiteit, het verkeer aan uw plaats, en uw geselecteerde succesmetrisch.

**Oplossing:** Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen zullen bouwen.

* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest geen activiteitsgegevens als u de succesmaatstaf wijzigt van RPV in conversie.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting zal de verkeersvereisten verhogen nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Zijn er sommige ervaringen u van uw activiteit kunt laten vallen? Het verminderen van het aantal ervaringen in een activiteit zal de hoeveelheid tijd verminderen om modellen te bouwen.
* Is er een pagina voor hoger verkeer waarop deze activiteit succesvoller zou zijn? Hoe meer verkeer en conversies er in uw activiteitenlocaties plaatsvinden, hoe sneller de modellen worden.

### Mijn [!UICONTROL Auto-Target] activiteit genereert geen lift.

Er zijn vier factoren vereist voor een AP-activiteit om lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** Eerst, zorg ervoor dat uw activiteit verkeer personaliseert. Als modellen niet voor alle ervaringen worden gebouwd, dient uw [!UICONTROL Auto-Target] activiteit nog steeds willekeurig een aanzienlijk deel van bezoeken om te proberen om alle modellen zo snel mogelijk te bouwen. Als de modellen niet worden gebouwd, [!UICONTROL Auto-Target] is geen het personaliseren verkeer.

Daarna, zorg ervoor de aanbiedingen en de activiteitenplaatsen werkelijk een verschil aan de algemene reactiesnelheden gebruikend een eenvoudige, niet-gepersonaliseerde test A/B maken. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als een A/B-testresultaten statistisch significante lift op een of meer van de ervaringen laten zien, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

### Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om.

Dit wordt verwacht.

In een [!UICONTROL Auto-Target] activiteit, zodra een omzettingsmetrische (of optimalisatiedoel of post doel) wordt omgezet, wordt de gebruiker vrijgegeven van de ervaring en de activiteit wordt opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat zodra C1 wordt omgezet, de bezoeker wordt vrijgegeven.
