---
keywords: settings;priority
description: Adobe Target bepaalt welke activiteit (of activiteiten) om aan een pagina te leveren verschillend afhankelijk van welke interface van het Doel en welke functie van de activiteitenverwezenlijking (Visuele Composer van de Ervaring of Vorm Gebaseerde composer) u gebruikt.
title: Prioriteit in Adobe Target
feature: activities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 0%

---


# Prioriteit{#priority}

Het doel bepaalt welke activiteit (of activiteiten) om aan een pagina te leveren verschillend afhankelijk van welke interface van het Doel en welke functie van de activiteitenverwezenlijking (Visuele Composer van de Ervaring of Vorm Gebaseerde composer) u gebruikt.

## Alleen de doelstandaard/Premium Visual Experience Composer of op formulier gebaseerde Composer die gebruikmaakt van alleen Global Target Request {#section_4A0A317DFED345649B58B0CB5B410C8B}

Als uw bedrijf Norm/Premium van het Doel en Visual Experience Composer exclusief gebruikt, dan kan de inhoud van veelvoudige activiteiten voor de zelfde vraag zijn teruggekeerd. De activiteiten worden geleverd gebruikend de volgende beslissingsstroom:

1. De de servervraag van het Doel komt aan Doel met informatie over URL.
1. Het doel trekt elke activiteit die op die URL loopt.
1. Doelpogingen om de bezoeker in activiteiten aan te passen.

   Als de bezoeker al aan een A/B-test of een multivariatietest deelneemt, komen zij tot de conversie overeen met die test. Als zij eerder een ervaring hadden die gericht op activiteit was, moeten zij in het opnieuw aanpassen. Als ze aan de publieksregels voldoen, valt de bezoeker in die activiteiten en in specifieke ervaringen.

1. Inhoud voor alle activiteiten en ervaringen die de bezoekersovereenkomsten opleveren, wordt teruggestuurd naar de pagina.
1. Als de inhoud voor elke activiteit naar andere [CSS-kiezers](/help/c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337) verwijst, wordt alle inhoud weergegeven.

   Als er sprake is van een overlapping of een gedupliceerde CSS-kiezer, wordt de activiteiteninhoud met de hoogste prioriteit weergegeven. De resultaten van alle activiteiten die op de pagina worden uitgevoerd, worden geteld en weerspiegeld in de rapporten.

   >[!IMPORTANT]
   >
   >Doel retourneert de inhoud voor alle activiteiten op de pagina, te beginnen met de inhoud met de laagste prioriteit, die vervolgens door elke activiteit wordt overschreven, van laagste naar hoogste prioriteit. In de meeste gevallen leidt dit ertoe dat inhoud met de hoogste prioriteit wordt weergegeven. Als een activiteit met een lagere prioriteit de structuur van het DOM voor de pagina echter verandert, is het mogelijk dat de activiteit met een hogere prioriteit de paginastructuur niet herkent, zodat de inhoud met lagere prioriteit wordt weergegeven. De resultaten van alle activiteiten die op de pagina worden uitgevoerd, worden geteld en weerspiegeld in de rapporten.

1. Als de veelvoudige activiteiten het zelfde prioritaire niveau delen, dan zijn er twee tiedoorbrekers:

   * Als slechts één activiteit het richten van het publiek heeft, wordt die activiteit getoond.
   * Als alles of niets het richten hebben, dan wordt de activiteit die eerst werd goedgekeurd getoond.

## Target Standard/Premium-composer op basis van formulieren en Target Standard/Premium Visual Experience Composer {#section_4620253E1CE942DD830724C7822B175F}

>[!NOTE]
>
>Deze informatie is ook van toepassing op campagnes die worden uitgevoerd en die zijn gemaakt in [!DNL Target Classic].

Als uw bedrijf de op vorm-gebaseerde composer in Norm van het Doel/Premium en de Standaard/Premie Composer van de Ervaring van het Doel gebruikt, dan kan de inhoud van de veelvoudige activiteiten van Composer van de Visueel Ervaring leveren, maar slechts één activiteit van de op vorm-gebaseerde werkschema. De levering van de activiteit wordt bepaald gebruikend de volgende beslissingsstroom:

1. De vraag van de server van het doel komt aan Doel met informatie over [!DNL Target] verzoek en URL.
1. Het doel Klassieke en Standaard trekken elke activiteit die in dat [!DNL Target] verzoek loopt.
1. Doelpogingen om de bezoeker in activiteiten aan te passen.

   Als de bezoeker al aan een A/B-test of een multivariatietest deelneemt, komen zij tot de conversie overeen met die test. Als zij eerder een ervaring hadden die gericht op activiteit was, moeten zij in het opnieuw aanpassen. Als ze aan de publieksregels voldoen, valt de bezoeker in die activiteiten en in specifieke ervaringen.

1. Als een op vorm-gebaseerde activiteit de hoogste prioriteit is, dan is die activiteiteninhoud teruggekeerd samen met alle passende activiteiteninhoud van de activiteiten van Composer van de Visuele Ervaring.
1. Als een Visual Experience Composer-activiteit de hoogste prioriteit heeft, wordt de inhoud van alle overeenkomende visuele ervaringscomposer-activiteiten geretourneerd, maar wordt er geen Classic van het Doel of op vorm gebaseerde activiteiteninhoud geretourneerd.

   De resultaten van alle activiteiten die op de pagina worden uitgevoerd, worden geteld en weerspiegeld in de rapporten.

**Voorbeeld**

Als u twee activiteiten hebt, één gericht op het branded onderzoekssleutelwoord Nike en tweede gericht op het non-branded sleutelwoord niakers, worden de prioriteiten van beide activiteiten gecontroleerd. Als de Nike-activiteit een hogere prioriteit heeft, wordt die inhoud weergegeven. Als de sluiersactiviteit de hogere prioriteit heeft, wordt zijn inhoud getoond.

Als beide doelactiviteiten dezelfde prioriteit hebben, wordt de activiteit weergegeven die het laatst is bekeken. Als de bezoeker nieuw is voor de pagina, wordt de activiteit weergegeven die het laatst is geactiveerd.

## Doel Standaard/Premium op formulier gebaseerde composer met niet-globale doelverzoeken {#section_C3F5F09B0B2D4EF795C5929D5C426A8C}

>[!NOTE]
>
>Deze informatie is ook van toepassing op alle campagnes die worden uitgevoerd en die zijn gemaakt in Target Classic.

Als uw bedrijf [!DNL Target] verzoeken buiten het globale [!DNL Target] verzoek in op vorm-gebaseerde composer gebruikt, kan de inhoud van slechts één activiteit per vraag worden teruggekeerd. De levering van de activiteit wordt bepaald gebruikend de volgende beslissingsstroom:

1. De [!DNL Target] servervraag komt aan [!DNL Target] met informatie over [!DNL Target] verzoek en URL.
1. [!DNL Target] trekt elke activiteit die in dat  [!DNL Target] verzoek loopt.
1. [!DNL Target] pogingen om de bezoeker in de hoogste prioritaire activiteit aan te passen.

   Als de bezoeker al aan een A/B-test of een multivariatietest deelneemt, komen zij tot de conversie overeen met die test. Als zij eerder een ervaring hadden die gericht op activiteit was, moeten zij in het opnieuw aanpassen. Als ze aan de publieksregels voldoen, valt de bezoeker in die activiteiten en in specifieke ervaringen.

1. Als de veelvoudige activiteiten het zelfde prioritaire niveau delen, dan zijn er twee tiedoorbrekers:

   * Als slechts één activiteit het richten van het publiek heeft, wordt die activiteit getoond.
   * Als alles of niets het richten hebben, dan wordt de activiteit die eerst werd goedgekeurd getoond.

## Voorbeelden {#section_F6A788AAC3884A2FA03E47F0557A1213}

>[!NOTE]
>
>Afhankelijk van uw instellingen variëren de prioriteitswaarden. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen. Zie [Activiteitsinstellingen](/help/c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02) voor meer informatie.

**Twee Klassieke doelcampagnes gebruiken niet-globale doelverzoeken**

* Campagne 1: homePageHero, aanbieding1, prioriteit hoog
* Campagne 2: homePageHero, aanbieding2, prioriteit laag

Reactie: aanbieding1

**Twee activiteiten gebruiken slechts aanbiedingen die in de Visuele Composer van de Ervaring voor verschillende selecteurs worden gecreeerd**

* Activiteit 1: target-global-mbox, selector1, visualExpCompOffer1, priority low
* Activiteit 2: target-global-mbox, selector2, visualExpCompOffer2, priority high

Reactie: visualExpCompOffer1, visualExpCompOffer2

**Twee activiteiten gebruiken slechts aanbiedingen die in de Visuele Composer van de Ervaring voor zelfde selecteur worden gecreeerd**

* Activiteit 1: target-global-mbox, selector1, visualExpCompOffer1, priority low
* Activiteit 2: target-global-mbox, selector1, visualExpCompOffer2, priority high

Reactie: visualExpCompOffer1, visualExpCompOffer2

>[!NOTE]
>
>Dit is de zelfde reactie zoals in het tweede gebruik hierboven geval omdat het Klassieke Doel selecteurbotsingen niet behandelt. De Standaard van het doel vangt dergelijk gedrag en andere gebruiksgevallen wanneer de selecteurs zowel in DOM als visueel zouden kunnen botsen (gewoonlijk gedaan op het niveau van de ervaringsredacteur of op de wijze van de campagnesimulatie).

**Twee activiteiten gebruiken aanbiedingen die in de Visuele Composer van de Ervaring worden gecreeerd en twee Klassieke campagnes van het Doel**

* Activiteit 1: target-global-mbox, selector1, visualExpCompOffer1, gemiddeld hoog
* Activiteit 2: target-global-mbox, selector2, visualExpCompOffer2, priority low
* Campagne 1: target-global-mbox, aanbieding1, prioriteit hoog
* Campagne 2: target-global-mbox, aanbieding2, prioriteit laag

Reactie: aanbieding1, visualExpCompOffer2, visualExpCompOffer1

>[!NOTE]
>
>De orde van gecombineerde reacties is dat de klassieke inhoud eerst komt (slechts één klassieke reactie zal worden onderhouden zoals in gebruikscase 1) en dan de aanbiedingen van de Composer van de Ervaring van de Visueel die antwoorden aanbiedt die door omgekeerde prioriteit worden bevolen.

## Trainingsvideo: Activiteitsinstellingen (3:02)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)