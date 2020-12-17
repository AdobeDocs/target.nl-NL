---
keywords: auto-target;targeting;traffic allocation;frequently asked questions;faq;troubleshooting;trouble shooting;traffic
description: Problemen oplossen en Veelgestelde vragen over automatisch doel in Adobe Target.
title: Automatische probleemoplossing en veelgestelde vragen
feature: auto-target
translation-type: tm+mt
source-git-commit: d5444f1053cdea0ab121a5a5331556f906b17c6f
workflow-type: tm+mt
source-wordcount: '1854'
ht-degree: 0%

---


# ![Problemen met ](/help/assets/premium.png) PREMIUMAuto-Target en veelgestelde vragen

Problemen oplossen en Veelgestelde vragen (FAQ&#39;s) over [!UICONTROL Auto-Target] in [!DNL Adobe Target].

## Veelgestelde vragen {#section_5C120A2B11D14D9BAF767BBAB50FED23} automatisch bepalen

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u werkt met [!UICONTROL Auto-Target]-activiteiten:

### Wat zijn beste praktijken aan opstelling een [!UICONTROL Auto-Target] activiteit?

* Beslissen of de bedrijfswaarde van een (RPV) succesmetrisch van de Inkomsten per Bezoek de extra verkeersvereisten waard is. RPV heeft doorgaans minstens 1.000 conversies per ervaring nodig om een activiteit te kunnen gebruiken in plaats van conversie.
* Beslis over de toewijzing tussen controle en gepersonaliseerde ervaringen alvorens met de activiteit te beginnen die op uw doelstellingen wordt gebaseerd.
* Bepaal als u voldoende verkeer aan de pagina hebt waar uw [!UICONTROL Auto-Target] activiteit voor verpersoonlijkingsmodellen zal lopen om in een redelijke hoeveelheid tijd te bouwen.
   * Als u het verpersoonlijkingsalgoritme test, moet u geen ervaringen veranderen of profielkenmerken toevoegen/verwijderen terwijl de activiteit actief is.

* Overweeg een A/B-activiteit tussen de aanbiedingen en locaties die u in uw [!UICONTROL Auto-Target]-activiteit wilt gebruiken, uit te voeren om ervoor te zorgen dat de locatie(s) en aanbiedingen van invloed zijn op de optimalisatiedoelstelling. Als een A/B-activiteit geen significant verschil aantoont, zal [!UICONTROL Auto-Target] waarschijnlijk ook geen lift genereren.

   * Als een A/B test geen statistisch significante verschillen tussen ervaringen toont, is het waarschijnlijk dat de aanbiedingen u overweegt niet genoeg van elkaar verschillend zijn, beïnvloeden de plaatsen u selecteerde niet succesmetrisch, of het optimalisatiedoel is te ver in de omzettingrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Probeer de ervaringen tijdens de activiteiten niet ingrijpend te wijzigen.

### adviseert u dat wij AutoDoel met 90 (Controle)/10 (Gericht) verdelen gebruiken tot de modellen worden gebouwd?

Uw optimale verdeling van de verkeerstoewijzing hangt af van wat u wilt verwezenlijken.

Als uw doel is zoveel mogelijk verkeer te personaliseren, kunt u met 90% gerichte en 10% controle voor het leven van de activiteit blijven. Als uw doel een experiment is dat vergelijkt hoe goed gepersonaliseerde algoritmen tegenover de controle doen, dan is een 50/50 splitsing best voor het leven van de activiteit.

De beste praktijken moeten het verkeer-verdeling voor het leven van de activiteit handhaven zodat de bezoekers niet tussen gerichte en controleervaringen schakelen.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

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

### Wanneer zou ik mijn [!UICONTROL Auto-Target] activiteit moeten tegenhouden?

[!UICONTROL Auto-Target] kan worden gebruikt als &quot;altijd op&quot;verpersoonlijking die constant zal optimaliseren. Met name voor de groenere inhoud hoeft u uw [!UICONTROL Auto-Target]-activiteit niet te stoppen.

Als u substantiële veranderingen in de inhoud in uw [!UICONTROL Auto-Target] activiteit wilt aanbrengen, is de beste praktijken om een nieuwe activiteit te beginnen zodat andere gebruikers die rapporten herzien geen verwarrings of betrekking hebbend voorbij resultaten met verschillende inhoud zullen hebben.

### Hoe lang moet ik wachten op modellen om te bouwen? {#how-long}

De tijdsduur die nodig is voor modellen om uw [!UICONTROL Auto-Target]-activiteit uit te breiden, is doorgaans afhankelijk van het verkeer naar de geselecteerde locatie(s) van de activiteit en de conversietarieven die aan de maatstaf van het succes van de activiteit zijn gekoppeld.

[!UICONTROL Auto-Target] zal niet proberen om een gepersonaliseerd model voor een bepaalde ervaring te bouwen tot er minstens 50 omzettingen voor die ervaring zijn. Bovendien als het gebouwde model van ontoereikende kwaliteit is (zoals die door off-line evaluatie op greep &quot;test&quot;gegevens wordt bepaald, gebruikend [metrisch genoemd als AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve)), zal het model niet worden gebruikt om verkeer op een gepersonaliseerde manier te dienen.

Enkele andere punten om in mening over het modelgebouw van [!UICONTROL Auto-Target] te houden:

* Zodra een activiteit levend is, [!UICONTROL Auto-Target] overweegt tot de laatste 45 dagen van willekeurig gediende gegevens wanneer het proberen om modellen (d.w.z. controleverkeer, plus sommige extra willekeurig gediende gegevens die door ons algoritme worden gehouden) te bouwen.
* Wanneer [!UICONTROL Revenue per Visit] uw succesmetrisch is, vereisen deze activiteiten typisch meer gegevens om modellen te bouwen wegens de hogere gegevensvariantie die typisch in bezoek-opbrengst in vergelijking met omzettingspercentage bestaat.
* Omdat de modellen op een per-ervaringsbasis worden voortgebouwd, die één ervaring met een andere middelen vervangen die voldoende verkeer (d.w.z. minstens 50 omzettingen) voor de nieuwe ervaring moeten worden verzameld alvorens de gepersonaliseerde modellen kunnen worden herbouwd.

### Eén model is ingebouwd in mijn activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd?

Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

### Wanneer kan ik beginnen de resultaten van mijn [!UICONTROL Auto-Target] activiteit te bekijken?

U kunt de resultaten van uw [!UICONTROL Auto-Target] test beginnen te bekijken nadat u minstens twee ervaringen met gebouwde modellen (groen controleteken) voor de ervaring hebt die modellen hebben gebouwd.

### Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?

U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Zie [Een specifieke ervaring gebruiken als controle](/help/c-activities/t-automated-personalization/experience-as-control.md) voor meer informatie.

### Kan ik het doel metrische middenweg door een auto-Doelactiviteit veranderen? {#change-metric}

Wij adviseren niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. Wij garanderen niet wat gebeurt als u het doel metrisch in een activiteit verandert nadat het loopt.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] activiteiten die ofwel [!DNL Target] of [!DNL Analytics] (A4T) als rapportagebron gebruiken.

### Kan ik de optie Rapportgegevens opnieuw instellen gebruiken tijdens het uitvoeren van een automatisch doelactiviteit?

Het gebruik van de optie [!UICONTROL Reset Report Data] voor [!UICONTROL Auto-Target]-activiteiten wordt niet aanbevolen. Hoewel de zichtbare rapportgegevens worden verwijderd, verwijdert deze optie niet alle trainingsrecords uit het model [!UICONTROL Auto-Target]. In plaats van de optie [!UICONTROL Reset Report Data] te gebruiken voor [!UICONTROL Auto-Target]-activiteiten, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit. (Opmerking: Deze leidraad is ook van toepassing op [!UICONTROL Auto-Allocate]- en [!UICONTROL Automated Personalization]-activiteiten.)

## Problemen oplossen [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen waarmee u kunt worden geconfronteerd wanneer u [!UICONTROL Auto-Target] gebruikt, en enkele voorgestelde oplossingen.

### Mijn [!UICONTROL Auto-Target] activiteit duurt te lang om modellen te bouwen.

Er zijn verscheidene veranderingen van de activiteitenopstelling die de verwachte tijd kunnen verminderen om modellen te bouwen, met inbegrip van het aantal ervaringen in uw [!UICONTROL Auto-Target] activiteit, het verkeer aan uw plaats, en uw geselecteerde succesmetrisch.

**Oplossing:** herzie uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent om te maken om de snelheid te verbeteren waarop de modellen zullen bouwen.

* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest geen activiteitsgegevens als u de succesmaatstaf wijzigt van RPV in conversie.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting zal de verkeersvereisten verhogen nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Zijn er sommige ervaringen u van uw activiteit kunt laten vallen? Het verminderen van het aantal ervaringen in een activiteit zal de hoeveelheid tijd verminderen om modellen te bouwen.
* Is er een pagina voor hoger verkeer waarop deze activiteit succesvoller zou zijn? Hoe meer verkeer en conversies er in uw activiteitenlocaties plaatsvinden, hoe sneller de modellen worden.

### Mijn [!UICONTROL Auto-Target] activiteit produceert geen lift.

Er zijn vier factoren vereist voor een AP-activiteit om lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** Eerst, zorg ervoor dat uw activiteit verkeer personaliseert. Als de modellen niet voor alle ervaringen worden gebouwd, uw [!UICONTROL Auto-Target] activiteit nog willekeurig een significant deel van bezoeken dient om te proberen om alle modellen zo snel mogelijk te bouwen. Als de modellen niet worden gebouwd, [!UICONTROL Auto-Target] is geen het personaliseren verkeer.

Daarna, zorg ervoor de aanbiedingen en de activiteitenplaatsen werkelijk een verschil aan de algemene reactiesnelheden gebruikend een eenvoudige, niet-gepersonaliseerde test A/B maken. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als een A/B-testresultaten statistisch significante lift op een of meer van de ervaringen laten zien, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

### Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om.

Dit wordt verwacht.

In een [!UICONTROL Auto-Target] activiteit, zodra een omzettingsmetrisch (of optimalisatiedoel of post doel) wordt omgezet, wordt de gebruiker vrijgegeven uit de ervaring en de activiteit wordt opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat zodra C1 wordt omgezet, de bezoeker wordt vrijgegeven.

### Wat gebeurt er als ik één ervaring uit een auto-doelactiviteit verwijder?

[!DNL Target] bouwt één model per ervaring, zodat het verwijderen van één ervaring slechts één minder model  [!DNL Target] zal bouwen, en geen modellen voor de andere ervaringen zal beïnvloeden.

Stel dat u een [!UICONTROL Auto-Target]-activiteit hebt met acht ervaringen en dat u de prestaties van één ervaring niet leuk vindt. U kunt die ervaring verwijderen en het heeft geen invloed op de modellen voor de zeven resterende ervaringen.
