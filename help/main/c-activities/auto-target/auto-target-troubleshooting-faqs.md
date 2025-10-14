---
keywords: autotarget;het richten;verkeerstoewijzing;vaak gestelde vragen;faq;het oplossen van problemen;het oplossen van problemen;verkeer
description: Verken onderwerpen voor het oplossen van problemen en Veelgestelde vragen over [!UICONTROL Auto-Target] activiteiten.
title: Hoe kan ik [!UICONTROL Auto-Target] activiteiten oplossen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Auto-Target
exl-id: 934f738e-560a-4847-9608-432ecfa2afe7
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '1850'
ht-degree: 0%

---

# [!UICONTROL Auto-Target] Veelgestelde vragen en problemen oplossen

Problemen oplossen en Veelgestelde vragen (FAQ&#39;s) over [!UICONTROL Auto-Target] -activiteiten in [!DNL Adobe Target] .

## [!UICONTROL Auto-Target] Veelgestelde vragen {#section_5C120A2B11D14D9BAF767BBAB50FED23}

Raadpleeg de volgende veelgestelde vragen en antwoorden terwijl u met [!UICONTROL Auto-Target] -activiteiten werkt:

### Wat zijn tips en trucs om een [!UICONTROL Auto-Target] -activiteit in te stellen?

+++Antwoord
* Bepaal als de bedrijfswaarde van a [!UICONTROL Revenue per Visit] (RPV) succes metrisch de extra verkeersvereisten waard is. RPV heeft doorgaans minstens 1.000 conversies per ervaring nodig om een activiteit te kunnen gebruiken in plaats van conversie.
* Beslis over de toewijzing tussen controle en gepersonaliseerde ervaringen alvorens met de activiteit te beginnen die op uw doelstellingen wordt gebaseerd.
* Bepaal of u voldoende verkeer hebt naar de pagina waarop uw [!UICONTROL Auto-Target] -activiteit wordt uitgevoerd, zodat u verpersoonlijkingsmodellen binnen een redelijke tijd kunt bouwen.
* Als u het verpersoonlijkingsalgoritme test, zou u geen ervaringen moeten veranderen of profielattributen toevoegen of verwijderen terwijl de activiteit levend is.
* Overweeg een A/B activiteit tussen de aanbiedingen en de plaatsen te voltooien die u van plan bent in uw [!UICONTROL Auto-Target] activiteit te gebruiken om ervoor te zorgen de plaatsen en de aanbiedingen een invloed op het optimalisatiedoel hebben. Als een A/B-activiteit geen significant verschil aantoont, genereert [!UICONTROL Auto-Target] waarschijnlijk ook geen lift.

  Als een A/B test geen statistisch significante verschillen tussen ervaringen toont, is het waarschijnlijk dat de aanbiedingen u overweegt niet genoeg van elkaar verschillend zijn, beïnvloeden de plaatsen u selecteerde niet succesmetrisch, of het optimalisatiedoel is te ver in de omzettingrechter om door uw gekozen aanbiedingen te worden beïnvloed.

* Probeer de ervaringen tijdens de activiteit niet ingrijpend te wijzigen.

+++

### Wilt u [!UICONTROL Adobe] aanbevelen om [!UICONTROL Auto Target] te gebruiken met een splitsing van 90 (Besturing)/10 (Gericht) totdat de modellen zijn gemaakt?

+++Antwoord 
Uw optimale verdeling van de verkeerstoewijzing hangt af van wat u wilt verwezenlijken.

Als uw doel is zoveel mogelijk verkeer te personaliseren, kunt u met 90% gerichte toewijzing en 10% controle voor het leven van de activiteit blijven. Als uw doel een experiment is dat vergelijkt hoe gepersonaliseerde algoritmen tegenover de controle doen, dan is een 50/50 splitsing best voor het leven van de activiteit.

De beste praktijken moeten het verkeer-verdeling voor het leven van de activiteit handhaven zodat de bezoekers niet tussen gerichte en controleervaringen schakelen.

<!-- 
### Do the check marks indicating a model is built for that experience update if the report date range changes?

No, check marks for model generation show only the models built to date. There's no way to go back and see when a model was completed.
-->

+++

### Als een bezoeker **niet** de [!UICONTROL Auto-Target] activiteit ziet en omzet, telt de omzettingstelling in mijn activiteit?

+++Antwoord
Nee, alleen bezoekers die in aanmerking komen voor de [!UICONTROL Auto-Target] -activiteit worden meegeteld in de rapportage.

+++

### Waarom genereert mijn [!UICONTROL Auto-Target] activiteit geen lift.

+++Antwoord
Er zijn vier factoren vereist voor een [!UICONTROL Auto-Target] -activiteit om een lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen.

Als uit de resultaten van een A/B-test statistisch significante resultaten van een of meer ervaringen blijken, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen en locaties die niet voldoende effect hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

+++

### Wanneer moet ik mijn [!UICONTROL Auto-Target] activiteit stoppen?

+++Antwoord
[!UICONTROL Auto-Target] kan worden gebruikt als &#39;altijd aan&#39; personalisatie die constant optimaliseert. Met name voor steeds groene inhoud is het niet nodig om de [!UICONTROL Auto-Target] -activiteit te stoppen.

Als u substantiële wijzigingen wilt aanbrengen in de inhoud van uw [!UICONTROL Auto-Target] -activiteit, kunt u het beste een nieuwe activiteit starten zodat andere gebruikers die rapporten controleren, oude resultaten niet verwarren of met andere inhoud in verband brengen.

+++

### Hoe lang moet ik wachten op modellen om te bouwen? {#how-long}

+++Antwoord
De tijd die het voor modellen vergt om in uw [!UICONTROL Auto-Target] activiteit te bouwen hangt typisch van het verkeer aan uw geselecteerde activiteitenplaatsen en omzettingen verbonden aan uw metrische activiteit af.

[!UICONTROL Auto-Target] probeert geen gepersonaliseerd model voor een bepaalde ervaring te bouwen tot er minstens 50 omzettingen voor die ervaring zijn. Voorts als het gebouwde model van ontoereikende kwaliteit is (zoals die door off-line evaluatie op greep-out &quot;test&quot;gegevens wordt bepaald, gebruikend [&#x200B; metrisch die als AUC &#x200B;](https://en.wikipedia.org/wiki/Receiver_operating_characteristic#Area_under_the_curve) wordt bekend), wordt het model niet gebruikt om verkeer op een gepersonaliseerde manier te dienen.

Houd rekening met het volgende: [!UICONTROL Auto-Target] modelgebouw:

* Nadat een activiteit levend is, overweegt [!UICONTROL Auto-Target] tot de laatste 45 dagen van willekeurig gediende gegevens wanneer het proberen om modellen te bouwen. Bijvoorbeeld, controleverkeer, plus wat extra willekeurig gediende gegevens die door het algoritme worden gehouden.
* Wanneer [!UICONTROL Revenue per Visit] uw succesmetrische waarde is, vereisen deze activiteiten typisch meer gegevens om modellen te bouwen wegens de hogere gegevensvariantie die typisch in bezoek-opbrengst in vergelijking met omzettingspercentage bestaat.
* Omdat de modellen op een per-ervaringsbasis worden voortgebouwd, betekent het vervangen van één ervaring met een andere ervaring dat voldoende verkeer (minstens 50 omzettingen) voor de nieuwe ervaring moet worden verzameld alvorens de gepersonaliseerde modellen kunnen worden herbouwd.

+++

### Eén model is ingebouwd in mijn activiteit. Zijn de bezoeken aan die ervaring gepersonaliseerd?

+++Antwoord
Nee, er moeten ten minste twee modellen in uw activiteiten zijn ingebouwd voordat de personalisatie begint.

+++

### Wanneer kan ik beginnen te kijken naar de resultaten van mijn [!UICONTROL Auto-Target] activiteit?

+++Antwoord
U kunt de resultaten van de [!UICONTROL Auto-Target] -test bekijken nadat u minstens twee ervaringen hebt met gebouwde modellen (groen vinkje) voor de ervaring die modellen heeft gebouwd.

+++

### Kan ik een specifieke ervaring specificeren die als controle moet worden gebruikt?

+++Antwoord
U kunt een ervaring selecteren die als controle wordt gebruikt terwijl het creëren van a [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het verkeer-toewijzingspercentage wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren.

Voor meer informatie, zie [&#x200B; Gebruik een specifieke ervaring als controle &#x200B;](/help/main/c-activities/t-automated-personalization/experience-as-control.md).

+++

### Kan ik het doel metrisch halverwege door een [!UICONTROL Auto-Target] activiteit veranderen? {#change-metric}

+++Antwoord
Adobe adviseert niet dat u het doel metrische middenweg door een activiteit verandert. Hoewel het mogelijk is om doel metrisch tijdens een activiteit te veranderen gebruikend [!DNL Target] UI, zou u altijd een nieuwe activiteit moeten beginnen. Adobe garandeert niet wat er gebeurt als u het doel metrisch wijzigt in een activiteit nadat deze is uitgevoerd.

Deze aanbeveling is van toepassing op [!UICONTROL Auto-Allocate] -, [!UICONTROL Auto-Target] - en [!UICONTROL Automated Personalization] -activiteiten die [!DNL Target] - of [!DNL Analytics] (A4T) gebruiken als rapportagebron.

+++

### Kan ik de optie [!UICONTROL Reset Report Data] gebruiken tijdens het uitvoeren van een [!UICONTROL Auto-Target] -activiteit?

+++Antwoord
Het gebruik van de optie [!UICONTROL Reset Report Data] voor [!UICONTROL Auto-Target] -activiteiten wordt niet aanbevolen. Hoewel de zichtbare rapportgegevens worden verwijderd, worden met deze optie niet alle trainingsrecords uit het [!UICONTROL Auto-Target] -model verwijderd. In plaats van de optie [!UICONTROL Reset Report Data] te gebruiken voor [!UICONTROL Auto-Target] -activiteiten, maakt u een nieuwe activiteit en deactiveert u de oorspronkelijke activiteit.

Deze handleiding is ook van toepassing op [!UICONTROL Auto-Allocate] - en [!UICONTROL Automated Personalization] -activiteiten.

+++

### Wat gebeurt er als ik één ervaring uit een [!UICONTROL Auto-Target] activiteit verwijder?

+++Antwoord
[!DNL Target] bouwt één model per ervaring, zodat het verwijderen van één ervaring betekent [!DNL Target] één minder model bouwt en geen modellen voor de andere ervaringen beïnvloedt.

Stel dat u een [!UICONTROL Auto-Target] -activiteit hebt met acht ervaringen en dat u de prestaties van één ervaring niet leuk vindt. U kunt die ervaring verwijderen en het beïnvloedt niet de modellen voor de zeven resterende ervaringen.

+++

## Problemen oplossen [!UICONTROL Auto-Target] {#section_23995AB813F24525AF294D20A20875C8}

Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen waarmee u kunt worden geconfronteerd bij het gebruik van [!UICONTROL Auto-Target] en enkele voorgestelde oplossingen.

### Mijn [!UICONTROL Auto-Target] -activiteit duurt te lang om modellen te maken.

+++Oplossingen voor problemen
Er zijn verscheidene veranderingen van de activiteitenopstelling die de verwachte tijd kunnen verminderen om modellen te bouwen, met inbegrip van het aantal ervaringen in uw [!UICONTROL Auto-Target] activiteit, het verkeer aan uw plaats, en uw geselecteerde succesmetrisch.

**Oplossing:** herzie uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen bouwen.

* Als uw succesmetrische waarde is ingesteld op [!UICONTROL RPV] , kunt u dan overschakelen op conversie? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest geen activiteitsgegevens als u de succesmaatstaf wijzigt van RPV in conversie.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lagere tarief van de activiteitenomzetting verhoogt de verkeersvereisten nodig voor modellen om te bouwen, omdat een minimumaantal omzettingen wordt vereist.
* Zijn er sommige ervaringen u van uw activiteit kunt laten vallen? Het verminderen van het aantal ervaringen in een activiteit vermindert de tijd om modellen te bouwen.
* Is er een pagina voor hoger verkeer waarop deze activiteit succesvoller zou zijn? De meer verkeer en omzettingen in uw activiteitenplaatsen, bouwen de snellere modellen.

+++

### Mijn [!UICONTROL Auto-Target] -activiteit genereert geen lift.

+++Oplossingen voor problemen
Er zijn vier factoren vereist voor een [!UICONTROL Auto-Target] -activiteit om een lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** eerst, zorg ervoor dat uw activiteit verkeer personaliseert. Als modellen niet voor alle ervaringen worden gebouwd, bedient uw [!UICONTROL Auto-Target] activiteit nog steeds willekeurig een aanzienlijk deel van bezoeken om te proberen om alle modellen zo snel mogelijk te bouwen. Als modellen niet worden gebouwd, personaliseert [!UICONTROL Auto-Target] geen verkeer.

Daarna, zorg ervoor dat de aanbiedingen en de activiteitenplaatsen werkelijk een verschil aan de algemene reactiesnelheden gebruikend een eenvoudige, niet-gepersonaliseerde test A/B maken. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als uit een A/B-testresultaten blijkt dat een of meer ervaringen statistisch significant zijn, is het waarschijnlijk dat een gepersonaliseerde activiteit werkt. Personalization kan ook werken als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen en locaties die niet voldoende effect hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

+++

### Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om.

+++Oplossingen voor problemen
Dit wordt verwacht.

In een [!UICONTROL Auto-Target] activiteit, zodra een omzettingsmetrische (of optimalisatiedoel of post doel) wordt omgezet, wordt de gebruiker vrijgegeven uit de ervaring, en de activiteit wordt opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat wanneer C1 wordt omgezet, de bezoeker wordt vrijgegeven.

+++
