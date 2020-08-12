---
description: Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen waarmee u kunt worden geconfronteerd wanneer u Automated Personalization gebruikt en enkele oplossingen.
title: Problemen met Automated Personalization oplossen
feature: null
uuid: 50c5380f-bc7f-41ae-8a85-cdce2dcc0ccd
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Troubleshoot Automated Personalization{#troubleshoot-automated-personalization}

Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen waarmee u kunt worden geconfronteerd wanneer u Automated Personalization gebruikt en enkele oplossingen.

## Mijn AP-activiteit duurt te lang om modellen te bouwen. {#section_20028B204DBB4D77A324BA193434AEE2}

Er zijn verscheidene veranderingen van de activiteitenopstelling die de verwachte tijd kunnen verminderen om modellen te bouwen, met inbegrip van het aantal ervaringen in uw test van Automated Personalization, het verkeer aan uw plaats, en uw geselecteerde succesmetrisch.

**Oplossing:** Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen zullen bouwen.

* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest geen activiteitsgegevens als u de succesmetrische waarde wijzigt van RPV in Conversie.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting verhoogt de verkeersvereisten nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Zijn er enkele aanbiedingen of ervaringen die je van je activiteit kunt uitsluiten? Door het aantal ervaringen in een activiteit te verminderen, duurt het langer om modellen te bouwen.
* Is er een hoger-verkeerspagina daar deze activiteit succesvoller zou zijn? Hoe meer verkeer en conversies er in uw activiteitenlocaties plaatsvinden, hoe sneller de modellen worden.

## Mijn AP-activiteit heeft geen lift gegenereerd. {#section_8900BC8968474438B8092F7A94C0C6CF}

Er zijn verschillende factoren vereist voor een AP-activiteit om lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de monstergrootten vooraf berekent om ervoor te zorgen dat er voldoende kracht is om een redelijke lift te zien en de A/B-test voor een vaste duur uit te voeren zonder deze te stoppen of wijzigingen aan te brengen. Als een A/B-testresultaten statistisch significante lift op een of meer van de ervaringen laten zien, is het waarschijnlijk dat een gepersonaliseerde activiteit zal werken. Natuurlijk kan personalisatie werken zelfs als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen/locaties die niet voldoende invloed hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

## De URL van mijn AP-activiteit toont inhoud van de aanbieding op onjuiste pagina&#39;s. {#section_82A224406DBF4107B05204BEFBBE458C}

In AP, worden URL en malplaatje het testen regels toegevoegd aan de beperking van de [!DNL Target] verzoekingang (bijvoorbeeld, doel-globaal-mbox), waar zij slechts eenmaal worden geëvalueerd. Zodra een gebruiker voor een activiteit kwalificeert, wordt het doel-verzoek-niveau richtend regels niet opnieuw geëvalueerd. Nochtans, wordt het gerichte publiek toegevoegd aan plaats het richten regels.

**Oplossing:** Voeg de noodzakelijke malplaatjeregels als input-publiek van de campagne toe. De evaluatie van het publiek gebeurt op elk verzoek/vraag.

Dit wordt in een volgende release opgelost.

## Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om. {#section_076D1F44298C4E4A849AC52F5A33214D}

Dit wordt verwacht.

In een AP activiteit, zodra een omzettingsmetrische (of optimalisatiedoel of post doel) wordt omgezet, wordt de gebruiker vrijgegeven van de ervaring en de activiteit wordt opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat zodra C1 wordt omgezet, de bezoeker wordt vrijgegeven.

## Mijn ervaring-URL&#39;s werken niet zoals verwacht. {#section_7B08DA1F30AA483E9406336DAF361BA4}

* Als u de voorvertoning niet kunt zien op het nieuwe tabblad (vanwege de cache van de browser), probeert u de koppeling twee of drie keer te vernieuwen of kopieert u de koppeling en opent u deze in een nieuwe browser of sessie.
* Regenereer de URL-koppelingen voor beleving als u inhoud hebt gewijzigd en deel de nieuwe koppelingen met uw collega&#39;s.

