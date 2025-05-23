---
keywords: faq;veelgestelde vragen;analytische gegevens voor doel;a4T;omleiden;aanbod omleiden;adobe-mc-sdid;adobe_mc_ref
description: Zoek antwoorden op vragen over het gebruik van omleidingsaanbiedingen wanneer u Analyses gebruikt voor [!DNL Target] (A4T). Met A4T kunt u analytische rapporten gebruiken voor [!DNL Target] activiteiten.
title: Waar kan ik veelgestelde vragen vinden over omleidingsaanbiedingen met A4T?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# Aanbiedingen omleiden - Veelgestelde vragen A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gevraagd over het gebruiken van omleidingsaanbiedingen wanneer het gebruiken [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T).

## Biedt Analytics for Adobe Target (A4T) ondersteuning voor omleidingsaanbiedingen? {#section_46B8B03ED4D542C6AD875F5F61176298}

+++ Antwoord ja, als uw implementatie gebruikt [!DNL at.js]. Uw implementatie moet echter voldoen aan de onderstaande minimumvereisten om te kunnen worden gebruikt [omleiding van aanbiedingen](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in activiteiten die Analytics als rapportbron gebruiken.

+++

## Wat zijn de minimumeisen om aanbiedingen om te leiden met A4T te gebruiken? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

+++ Antwoord Uw implementatie moet aan de volgende minimale vereisten voldoen:

* Experience Cloud Bezoeker-id-service: [!DNL visitorAPI.js] versie 2.3.0 of hoger.
* Adobe Analytics: [!DNL appMeasurement.js] versie 2.1.
* Adobe Target: [!DNL at.js] versie 1.6.2 of hoger.

De drie bibliotheken moeten op zowel de pagina met het omleidingsaanbod als de pagina worden opgenomen waarnaar de bezoeker wordt omgeleid.

+++

## Waarom zijn er soms gegevensdiscrepanties tussen A4T en Analytics?

+++Antwoord Sommige gegevensdiscrepanties worden verwacht. Zie voor meer informatie [Verwachte gegevensvariaties tussen Doel en Analytics bij gebruik en niet bij gebruik van A4T](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

+++

## Hoe kan ik discrepanties in verkeersdistributie minimaliseren wanneer het gebruiken van omleidingsaanbiedingen in A4T activiteiten? {#discrepancies}

+++Antwoord Een beperkt aantal klanten heeft hogere graden van variatie in verkeersdistributie gemeld wanneer het gebruiken van aanbiedingen in activiteiten die met worden gevormd [!UICONTROL Analytics for Target] (A4T).

Overweeg het volgende:

* Onjuiste volgorde van [!DNL Target] en [!DNL Analytics] de vraag zou voor hogere graad van variantie kunnen verantwoordelijk zijn.

   De [!DNL Target] de vraag moet voorafgaan aan [!DNL Analytics] de vraag op de bronpagina (waar redirect voorkomt) en op de bestemmingspagina (waar redirect beëindigt).

* Zorg ervoor dat u omleidingsaanbiedingen in A4T omleidingsactiviteiten gebruikt.
* Als er meerdere [!DNL Target] locatieverzoeken op de bronpagina (waar de omleiding plaatsvindt); [!DNL Adobe] raadt u aan de omleidingsactiviteit uit te voeren op de eerste [!DNL Target] locatieverzoek.

   De omleidingsactiviteit uitvoeren op de eerste [!DNL Target] locatieverzoek verkleint de kans dat er op andere activiteiten kwalificaties plaatsvinden [!DNL Target] locatieverzoeken en meegeteld in het rapport. Bezoekers die worden omgeleid, hoeven niet mee te tellen in de verslagen van andere activiteiten, aangezien zij de ervaringen niet zullen zien.

+++

## Waarom worden paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina soms geteld? {#section_B8F6CC2190B84CF08D945E797C5AF07B}

+++Antwoord Bij gebruik van versie 1.js 1.6.3 of hoger is het niet van belang om paginaweergaven op beide pagina&#39;s te tellen. Deze rasvoorwaarde beïnvloedt slechts klanten die vroegere versies gebruiken. Het team van het Doel handhaaft twee versies van at.js: de huidige versie en de tweede nieuwste versie. Voer indien nodig een upgrade uit naar .js om ervoor te zorgen dat u een [ondersteunde versie](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank}.

Als u een vroegere, niet-gesteunde versie van at.js gebruikt, is er een mogelijkheid dat een rassenvoorwaarde kan voorkomen die de Analytische vraag zou kunnen veroorzaken om te vuren alvorens redirect op de eerste pagina uitvoert. Hierdoor kunnen paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina worden geteld. Deze situatie leidt tot een extra paginaweergave op de eerste pagina, wanneer de bezoeker deze eerste pagina nooit echt &#39;zag&#39;.

Het wordt aanbevolen om met de op formulieren gebaseerde composer een omleidingsactiviteit te maken om de omleiding van de pagina te versnellen, omdat de code op de pagina wordt uitgevoerd. Bovendien wordt het aangeraden een omleidingsaanbieding voor elke ervaring te maken, zelfs voor de standaardervaring, waarbij omleiding de oorspronkelijke pagina zou retourneren. Het creëren van een omleidingsaanbieding voor elke ervaring zorgt ervoor dat als fout-telling voorkomt, het over alle ervaringen gebeurt. Rapportage en analyse zijn nog steeds geldig voor de test.

Eén reden dat u omleidingsaanbiedingen wilt gebruiken voor alle ervaringen in de activiteit, inclusief de standaardeigenschap (controle), is om dezelfde voorwaarden op alle ervaringen te plaatsen. Bijvoorbeeld, als de standaardervaring geen omleidingsaanbod heeft maar de andere ervaringen hebben omleidingsaanbiedingen, heeft de snelheid van de ervaring zonder de omleidingsaanbieding een inherent voordeel. Aanbiedingen voor omleiding worden alleen aanbevolen voor tijdelijke scenario&#39;s, zoals testen. Het doorsturen van aanbiedingen wordt niet aanbevolen voor permanente scenario&#39;s, zoals personalisatie. Nadat u de winnaar hebt bepaald, moet u de omleiding verwijderen om de prestaties bij het laden van de pagina te verbeteren.

+++

## Wordt zowel Visual Experience Composer (VEC) als Form-Based Experience Composer ondersteund? {#section_FDA26FE7909B48539DA770559E687677}

+++ Antwoord ja, beide composers worden gesteund zolang u de ingebouwde omleidingsaanbiedingen gebruikt.

Als u uw eigen aangepaste code voor omleiding gebruikt, moet u ervoor zorgen dat u de twee nieuwe parameters vult die aan omleiding URLs ( `adobe_mc_sdid` en `adobe_mc_ref`, hieronder toegelicht).

+++

## Wat zijn de nieuwe parameters van het vraagkoord toegevoegd aan omleiding URLs? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

+++Antwoord De volgende parameters van het vraagkoord worden geassocieerd met opnieuw richten aanbiedingen:

| Parameter | Beschrijving |
|--- |--- |
| `adobe_mc_sdid` | De `adobe_mc_sdid` De parameter gaat de Supplemental Identiteitskaart van Gegevens (SDID) en Experience Cloud die identiteitskaart van de standaardpagina tot de nieuwe pagina over. Met deze id&#39;s kan A4T het doelverzoek samenvoegen op de standaardpagina met het analyseverzoek op de nieuwe pagina.<br>De verwachte indeling voor het doorgeven van gegevens in de URL (voor hybride apps of van de ene app naar de website of de ene website naar de andere) is `ex. adobe_mc_sdid=SDID=123|MCORGID=123456789@AdobeOrg|TS=1498569322` |
| `adobe_mc_ref` | De `adobe_mc_ref` geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Wanneer deze parameter wordt gebruikt met AppMeturement.js versie 2.1 (of hoger), gebruikt Analytics deze parameterwaarde als verwijzende URL op de nieuwe pagina. |

Deze parameters worden automatisch toegevoegd aan omleiding URLs wanneer het gebruiken van de ingebouwde omleidingsaanbiedingen in VEC en op vorm-Gebaseerde Composer van de Ervaring wanneer de dienst van Bezoeker Id op de pagina wordt uitgevoerd. Als u uw eigen aangepaste omleidingscode in de VEC of op vorm gebaseerde Composer gebruikt, moet u ervoor zorgen dat u deze parameters doorgeeft met uw aangepaste code.

+++

## Mijn webservers verwijderen deze parameters van mijn URL&#39;s. Wat moet ik doen? {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

+++Antwoord Werk met uw IT-team om deze parameters te krijgen ( `adobe_mc_sdid` en `adobe_mc_ref`) gevoegd op lijst van gewenste personen.

+++

## Wat als ik geen A4T met mijn omleidingsactiviteit gebruik en niet deze extra parameters aan mijn URLs wil hebben toevoegen? {#section_9E608D75FF9349FE96C65FEDD7539F45}

+++Antwoord Gebruik een aangepaste omleiding als:

* U gebruikt geen A4T met uw omleidingsactiviteit
* De service Visitor-id is geïmplementeerd
* U wilt niet dat deze parameters automatisch aan uw URLs worden toegevoegd

Als beste praktijken, zou u kunnen willen houden `adobe_mc_ref` parameter in de URL om de informatie van de verwijzer aan te melden [!DNL Analytics] correct.

+++

## Waarom zijn de parameters adobe_mc_ref en adobe_mc_sdid dubbel-URL gecodeerd in mijn implementatie? {#section_5EFE5F012B944C40865731EA18E7E79E}

+++Antwoord Als u A4T gebruikt en aanbiedingen opnieuw richt, voegt Target toe `adobe_mc_ref` en `adobe_mc_sdid` parameters aan URL. Deze waarden zijn al gecodeerd met URL. Meestal werkt alles zoals verwacht, echter, zouden sommige klanten ladingsbalancers of servers kunnen hebben WEB die proberen om de parameters van het vraagkoord één meer keer te coderen.

Vanwege deze dubbele codering wanneer de bezoeker-API de code `adobe_mc_sdid` waarde, kan de SDID-waarde niet worden opgehaald en wordt een nieuwe SDID gegenereerd. Dit proces leidt tot onjuiste waarden SDID die naar Doel en Analytics worden verzonden en u ziet ongelijkmatige verdeling voor herleidingen in de rapporten van de Analyse.

Adobe raadt u aan contact op te nemen met uw IT-team om ervoor te zorgen dat `adobe_mc_ref` en `adobe_mc_sdid` zodanig worden gevoegd op lijst van gewenste personen dat deze waarden op geen enkele wijze worden getransformeerd.

+++

## Waarom moet de verwijzende URL aan de nieuwe pagina worden overgegaan? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

+++Antwoord Stel dat een bezoeker op een koppeling klikt [!DNL `www.google.com`] op uw homepage (`www.mysite.com/index.html`) waarop een omleidingsactiviteit actief is en vervolgens wordt omgeleid naar een nieuwe pagina (`www.mysite.com/index2.html`).

Eerder [!DNL Analytics] aanvraag op de nieuwe pagina zou een verwijzende URL van [!DNL `www.mysite.com/index.html`] in plaats van [!DNL `www.google.com`]. Dit heeft geleid tot onjuiste rapportage [!DNL Analytics] worden gekoppeld aan de verwijzende URL&#39;s (bijvoorbeeld marketingrapporten). De rapporten hadden het feit verloren dat u van [!DNL `www.google.com`].

Met [!DNL at.js] versie 0.9.6 (of hoger) en [!DNL AppMeasurement.js] 2.1 (of hoger), de [!DNL Analytics] request on new page meldt een verwijzende URL van [!DNL `www.google.com`].

+++

## Kan ik aangepaste/HTML omleidingsvoorstellen gebruiken? {#section_E49F9A83A286488C8F1098A040203D7E}

+++Antwoord nr, moet u een ingebouwde omleidingsaanbieding voor activiteiten gebruiken die [!DNL Analytics] als bron van rapportage (A4T). Van de [!DNL Target] perspectief, zijn de aanbiedingen van HTML ondoorzichtig: [!DNL Target] kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding concretiseert.

+++

## ![Adobe Experience Platform Web SDK-badge](/help/main/assets/platform.png) doet het [!DNL Adobe Experience Platform Web SDK] steun omleidingsaanbiedingen voor A4T? {#platform}

De volgende veelgestelde vragen bieden meer informatie over het gebruik van een A4T en het omleiden van aanbiedingen met de [!DNL Platform Web SDK].

### Biedt Analytics for Target (A4T) ondersteuning voor omleidingsaanbiedingen?

+++ Antwoord ja, A4T via de Steun van SDK van het Web van het Platform [omleiding van aanbiedingen](/help/main/c-experiences/c-manage-content/offer-redirect.md).

+++

### zijn [!UICONTROL Visual Experience Composer] (VEC) en [!UICONTROL Form-Based Experience Composer] ondersteund?

+++ Antwoord ja, de [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en de [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) worden ondersteund als u ingebouwde omleidingsvoorstellen gebruikt.

+++

### Kan ik aangepaste/HTML omleidingsvoorstellen gebruiken met de [!DNL Platform Web SDK]?

+++Antwoord nr, moet u een ingebouwde omleidingsaanbieding voor activiteiten gebruiken die A4T gebruiken. Van de [!DNL Target] HTML-aanbiedingen zijn dekkend. [!DNL Target] kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding concretiseert.

+++