---
kewords: Automated Personalization;ap;troublshoot;troubleshooting;model;lift
description: Ontdek potentiële uitdagingen die u tijdens het gebruiken zou kunnen ontmoeten [!UICONTROL Automated Personalization] (AP) activiteiten in Adobe Target, samen met voorgestelde oplossingen.
title: Hoe los ik problemen op [!UICONTROL Automated Personalization] activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: bc23e5db-5b65-44be-be45-c972287a64e7
source-git-commit: 2cb2c2b68f6487d1af41ecc7e73750afa1ad85f9
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Problemen oplossen [!UICONTROL Automated Personalization]

Soms gaan activiteiten niet zoals verwacht. Hier volgen enkele potentiële uitdagingen waarmee u kunt worden geconfronteerd wanneer u het gebruik ervan uitvoert [!UICONTROL Automated Personalization] (AP) en enkele voorgestelde oplossingen.

## Mijn [!UICONTROL Automated Personalization] het duurt te lang om modellen te bouwen . {#section_20028B204DBB4D77A324BA193434AEE2}

+++Zie details

Er zijn verscheidene veranderingen van de activiteitenopstelling die de verwachte tijd kunnen verminderen om modellen te bouwen, met inbegrip van het aantal ervaringen in uw [!UICONTROL Automated Personalization] activiteit, het verkeer aan uw plaats, en uw geselecteerd succes metrisch.

**Oplossing:** Controleer uw activiteitenopstelling en zie of zijn er om het even welke veranderingen u bereid bent aan te brengen om de snelheid te verbeteren waarop de modellen bouwen.

* Als uw succesmetrisch wordt geplaatst aan RPV, kunt u in omzetting veranderen? De activiteiten van de omzetting neigen om minder verkeer te vereisen om modellen te bouwen. U verliest activiteitsgegevens niet als u de succesmetrische waarde van RPV in omzetting verandert.
* Is uw succes metrisch ver onderaan de verkooptrechter van uw activiteitenervaringen? Een lager tarief van de activiteitenomzetting verhoogt de verkeersvereisten nodig voor modellen om te bouwen, aangezien een minimumaantal omzettingen wordt vereist.
* Zijn er enkele aanbiedingen of ervaringen die je van je activiteit kunt uitsluiten? Door het aantal ervaringen in een activiteit te verminderen, duurt het langer om modellen te bouwen.
* Is er een hoger-verkeerspagina waar deze activiteit succesvoller zou zijn? De meer verkeer en omzettingen in uw activiteitenplaatsen, bouwen de snellere modellen.

+++

## Mijn [!UICONTROL Automated Personalization] activiteit heeft geen lift gegenereerd. {#section_8900BC8968474438B8092F7A94C0C6CF}

+++Zie details

Er zijn verschillende factoren vereist voor een [!UICONTROL Automated Personalization] activiteit om lift te genereren:

* De aanbiedingen moeten verschillend genoeg zijn om bezoekers te beïnvloeden.
* De aanbiedingen moeten zich ergens bevinden die een verschil maken met het optimalisatiedoel.
* Er moet voldoende verkeer en statistische &quot;kracht&quot; in de test aanwezig zijn om de lift te detecteren.
* Het verpersoonlijkingsalgoritme moet goed werken.

**Oplossing:** De beste manier van werken is eerst ervoor te zorgen dat de inhoud en de locaties waaruit de activiteitenervaringen bestaan daadwerkelijk een verschil maken met de totale responspercentages met behulp van een eenvoudige, niet-gepersonaliseerde A/B-test. Zorg ervoor dat u de sampleformaten vooraf berekent. Door de sampleformaten vooraf te berekenen, kunt u ervoor zorgen dat er voldoende kracht is om een redelijke lift te zien. U kunt de A/B test dan voor een vaste duur in werking stellen zonder het tegen te houden of om het even welke veranderingen aan te brengen. Als een A/B-testresultaat statistisch significante lift op een of meer van de ervaringen toont, is het waarschijnlijk dat een gepersonaliseerde activiteit succesvol is. Personalisatie kan ook werken als er geen verschillen zijn in de totale responspercentages van de ervaringen. Doorgaans is het probleem het gevolg van aanbiedingen of locaties die onvoldoende effect hebben op het optimalisatiedoel en die statistisch significant moeten worden opgespoord.

+++

## Mijn [!UICONTROL Automated Personalization] activiteit URL toont aanbiedingsinhoud op onjuiste pagina&#39;s. {#section_82A224406DBF4107B05204BEFBBE458C}

+++Zie details

In [!UICONTROL Automated Personalization], worden de URL- en sjabloontestregels toegevoegd aan de [!DNL Target] verzoek ingangsbeperking (bijvoorbeeld target-global-mbox), waar zij slechts eenmaal worden geëvalueerd. Zodra een gebruiker voor een activiteit kwalificeert, wordt het doel-verzoek-niveau richtend regels niet opnieuw geëvalueerd. Nochtans, wordt het gerichte publiek toegevoegd aan plaats richtend regels.

**Oplossing:** Voeg de noodzakelijke malplaatjeregels als input-publiek van de activiteit toe. De evaluatie van het publiek gebeurt op elk verzoek/vraag.

+++

## Om het even welk metrisch afhankelijk van omzettingsmetrisch zet nooit om. {#section_076D1F44298C4E4A849AC52F5A33214D}

+++Zie details

Dit wordt verwacht.

In een [!UICONTROL Automated Personalization] activiteit, zodra een omzettingsmetrisch (of optimalisatiedoel of post doel) wordt omgezet, wordt de bezoeker losgemaakt van de ervaring, en de activiteit wordt opnieuw begonnen.

Bijvoorbeeld, is er een activiteit met metrisch (C1) en extra metrisch (A1). A1 is afhankelijk van C1. Wanneer een bezoeker de activiteit voor het eerst ingaat, en de criteria voor het omzetten A1 en C1 niet worden omgezet, wordt metrische A1 niet omgezet toe te schrijven aan het succes metrische gebiedsdeel. Als de bezoeker C1 omzet en dan A1 omzet, wordt A1 nog niet omgezet omdat wanneer C1 wordt omgezet, de bezoeker wordt vrijgegeven.

+++

## Mijn ervaring-URL&#39;s werken niet zoals verwacht. {#section_7B08DA1F30AA483E9406336DAF361BA4}

+++Zie details

* Als u de voorvertoning niet kunt zien op het nieuwe tabblad (vanwege de cache van de browser), kunt u proberen de voorvertoning twee of drie keer te vernieuwen. U kunt de koppeling ook kopiëren en openen in een nieuwe browser of sessie.
* Regenereer de URL-koppelingen voor beleving als u inhoud hebt gewijzigd en deel de nieuwe koppelingen met uw collega&#39;s.

+++
