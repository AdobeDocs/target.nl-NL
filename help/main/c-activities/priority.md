---
keywords: instellingen;prioriteit
description: Leer hoe  [!DNL Adobe Target]  bepaalt welke activiteit (of activiteiten) om aan een pagina te leveren verschillend afhankelijk van welke  [!DNL Target]  interface en welke functie van de activiteitenverwezenlijking u gebruikt.
title: Hoe wijst  [!DNL Target]  Prioriteit aan verschillende Activiteiten toe?
feature: Activities
exl-id: c32f1699-e564-40dd-8ff1-7c75a672c6ef
source-git-commit: be6e45ff301f549eb5be24a65b05c4a9c1cd6089
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Prioriteit

[!DNL Adobe Target] bepaalt welke activiteit (of activiteiten) om aan een pagina te leveren verschillend afhankelijk van welke [!DNL Target] interface en welke functie van de activiteitenverwezenlijking ([[!UICONTROL Visual Experience Composer (VEC)]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) of [&#x200B; Form-Based Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md)) u gebruikt.

## [!UICONTROL Visual Experience Composer] alleen of [!UICONTROL Form-Based Experience Composer] alleen een algemene [!DNL Target] aanvraag gebruiken {#section_4A0A317DFED345649B58B0CB5B410C8B}

Als uw bedrijf VEC exclusief gebruikt, kan de inhoud van veelvoudige activiteiten voor de zelfde vraag zijn teruggekeerd. De activiteiten worden geleverd gebruikend de volgende beslissingsstroom:

1. De serveraanroep [!DNL Target] wordt geleverd aan [!DNL Target] met informatie over de URL.
1. [!DNL Target] trekt elke activiteit die op die URL loopt.
1. [!DNL Target] probeert de bezoeker in activiteiten te passen.

   Als de bezoeker al een [!UICONTROL A/B Test] - of [!UICONTROL Multivariate Test] -activiteit heeft, komen ze overeen met die activiteit totdat ze worden omgezet. Als ze zich eerder in een [!UICONTROL Experience Targeting] -activiteit bevonden, moeten ze er opnieuw bij aansluiten. Als ze aan de publieksregels voldoen, valt de bezoeker in die activiteiten en in specifieke ervaringen.

1. Inhoud voor alle activiteiten en ervaringen die de bezoekersovereenkomsten opleveren, wordt teruggestuurd naar de pagina.
1. Als de inhoud voor elke activiteitenverwijzingen verschillende [&#x200B; CSS selecteurs &#x200B;](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337), dan wordt al inhoud getoond.

   Als er sprake is van een overlapping of een gedupliceerde CSS-kiezer, wordt de activiteiteninhoud met de hoogste prioriteit weergegeven. De resultaten van alle activiteiten die op de pagina worden uitgevoerd, worden geteld en weerspiegeld in de rapporten.

   >[!IMPORTANT]
   >
   >[!DNL Target] retourneert de inhoud voor alle activiteiten op de pagina, te beginnen met de inhoud met de laagste prioriteit, die vervolgens door elke activiteit wordt overschreven, van laagste naar hoogste prioriteit. Gewoonlijk wordt hierdoor inhoud met de hoogste prioriteit weergegeven. Als een activiteit met een lagere prioriteit de structuur van het DOM voor de pagina echter verandert, is het mogelijk dat de activiteit met een hogere prioriteit de paginastructuur niet herkent, zodat de inhoud met lagere prioriteit wordt weergegeven. De resultaten van alle activiteiten die op de pagina worden uitgevoerd, worden geteld en weerspiegeld in de rapporten.

1. Als meerdere activiteiten een prioriteitsniveau hebben, zijn er twee bandenspanners:

   * Als slechts één activiteit het richten van het publiek heeft, wordt die activiteit getoond.
   * Als alles of niets het richten heeft, dan wordt de activiteit die eerst werd goedgekeurd getoond.

## [!UICONTROL Form-Based Experience Composer] en [!UICONTROL Visual Experience Composer] {#section_4620253E1CE942DD830724C7822B175F}

Als uw bedrijf [!UICONTROL Form-Based Experience Composer] *en* VEC gebruikt, kan de inhoud van veelvoudige [!UICONTROL Form-Based Experience Composer] en activiteiten VEC leveren. Voorheen kon slechts één activiteit van de formuliergebaseerde workflow leveren. Er geldt niet langer een beperking voor het aantal op formulieren gebaseerde activiteiten dat kan leveren.

De levering van de activiteit wordt bepaald gebruikend de volgende beslissingsstroom:

1. [!DNL Target] -serveraanroep wordt geleverd aan [!DNL Target] met informatie over de [!DNL Target] -aanvraag en URL.
1. [!DNL Target] trekt elke activiteit die in die [!DNL Target] aanvraag wordt uitgevoerd.
1. [!DNL Target] probeert de bezoeker in activiteiten te passen.

   Als de bezoeker al een [!UICONTROL A/B Test] - of [!UICONTROL Multivariate Test] -activiteit heeft, komen ze overeen met die test totdat ze worden omgezet. Als ze zich eerder in een [!UICONTROL Experience Targeting] -activiteit bevonden, moeten ze er opnieuw bij aansluiten. Als ze aan de publieksregels voldoen, valt de bezoeker in die activiteiten en in specifieke ervaringen.

1. Als een op vorm-gebaseerde activiteit de hoogste prioriteit is, dan is die activiteiteninhoud teruggekeerd samen met alle passende activiteiteninhoud van VEC activiteiten.
1. Als een activiteit VEC de hoogste prioriteit is, dan wordt de inhoud van alle passende activiteiten VEC teruggegeven, maar geen op vorm-gebaseerde activiteiteninhoud is teruggekeerd.

   De resultaten van alle activiteiten die op de pagina worden uitgevoerd, worden geteld en weerspiegeld in de rapporten.

**Voorbeeld**

Als u twee activiteiten hebt, één gericht op het branded onderzoekssleutelwoord &quot;Nike&quot;en tweede gericht op het non-branded sleutelwoord &quot;sneakers&quot;, worden de prioriteiten van beide activiteiten gecontroleerd. Als de Nike-activiteit een hogere prioriteit heeft, wordt die inhoud weergegeven. Als de sluiersactiviteit de hogere prioriteit heeft, wordt zijn inhoud getoond.

Als beide doelactiviteiten dezelfde prioriteit hebben, wordt de activiteit weergegeven die het laatst is bekeken. Als de bezoeker nieuw is voor de pagina, wordt de activiteit weergegeven die het laatst is geactiveerd.

## [!UICONTROL Form-Based Experience Composer] met niet-globale [!DNL Target] aanvragen {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

Als uw bedrijf [!DNL Target] andere verzoeken dan het algemene [!DNL Target] -verzoek in de op formulier gebaseerde composer gebruikt, kan inhoud van slechts één activiteit per aanroep worden geretourneerd. De levering van de activiteit wordt bepaald gebruikend de volgende beslissingsstroom:

1. De [!DNL Target] -serveraanroep wordt naar [!DNL Target] verzonden met informatie over de [!DNL Target] -aanvraag en URL.
1. [!DNL Target] trekt elke activiteit die in die [!DNL Target] aanvraag wordt uitgevoerd.
1. [!DNL Target] probeert de bezoeker in de hoogste prioritaire activiteit aan te passen.

   Als de bezoeker al een [!UICONTROL A/B Test] - of [!UICONTROL Multivariate Test] -activiteit heeft, komen ze overeen met die activiteit totdat ze worden omgezet. Als ze zich eerder in een [!UICONTROL Experience Targeting] -activiteit bevonden, moeten ze er opnieuw bij aansluiten. Als ze aan de publieksregels voldoen, valt de bezoeker in die activiteiten en in specifieke ervaringen.

1. Als meerdere activiteiten een prioriteitsniveau hebben, zijn er twee bandenspanners:

   * Als slechts één activiteit het richten van het publiek heeft, wordt die activiteit getoond.
   * Als alles of niets het richten heeft, dan wordt de activiteit die eerst werd goedgekeurd getoond.

## Voorbeelden {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Afhankelijk van uw instellingen variëren de prioriteitswaarden. U kunt de oudere instellingen van [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] gebruiken of u kunt fijngeoriënteerde prioriteiten van 0 tot en met 999 inschakelen. Voor meer informatie, zie [&#x200B; montages van de Activiteit &#x200B;](/help/main/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02).

Reactie: aanbieding1

**twee activiteiten gebruiken slechts aanbiedingen die in [!UICONTROL Visual Experience Composer] voor verschillende selecteurs** worden gecreeerd

* Activiteit 1: target-global-mbox, selector1, visualExpCompOffer1, priority low
* Activiteit 2: target-global-mbox, selector2, visualExpCompOffer2, prioriteit hoog

Response: visualExpCompOffer1, visualExpCompOffer2

**Twee activiteiten gebruiken slechts aanbiedingen die in [!UICONTROL Visual Experience Composer] voor zelfde selecteur** worden gecreeerd

* Activiteit 1: target-global-mbox, selector1, visualExpCompOffer1, priority low
* Activiteit 2: target-global-mbox, selector1, visualExpCompOffer2, prioriteit hoog

Response: visualExpCompOffer1, visualExpCompOffer2

## Trainingsvideo: Instellingen voor activiteit (3 :02)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
