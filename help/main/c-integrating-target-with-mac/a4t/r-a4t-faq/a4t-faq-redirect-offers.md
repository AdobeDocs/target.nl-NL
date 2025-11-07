---
keywords: faq;veelgestelde vragen;analytische gegevens voor doel;a4T;omleiden;aanbod omleiden;adobe-mc-sdid;adobe_mc_ref
description: Vind antwoorden op vragen over het gebruiken van redirect aanbiedingen wanneer het gebruiken van Analytics voor  [!DNL Target]  (A4T). A4T laat u Analytics gebruiken die voor  [!DNL Target]  activiteiten rapporteert.
title: Waar kan ik veelgestelde vragen vinden over omleidingsaanbiedingen met A4T?
feature: Analytics for Target (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: e45ac15a60c83e35b8b2b2ba29a42727faf746df
workflow-type: tm+mt
source-wordcount: '1431'
ht-degree: 0%

---

# Aanbiedingen omleiden - Veelgestelde vragen A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over het gebruik van omleidingsaanbiedingen wanneer [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T) wordt gebruikt.

## Biedt Analytics for Adobe Target (A4T) ondersteuning voor omleidingsaanbiedingen? {#section_46B8B03ED4D542C6AD875F5F61176298}

+++Antwoord
Ja, als uw implementatie gebruikmaakt van [!DNL at.js] . Nochtans, moet uw implementatie aan de hieronder vermelde minimumvereisten voldoen om [&#x200B; te gebruiken herleidt aanbiedingen &#x200B;](/help/main/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) in activiteiten die Analytics als rapporteringsbron gebruiken.

+++

## ![&#x200B; SDK van het Web van Adobe Experience Platform badge &#x200B;](/help/main/assets/platform.png) Omleidt de [!DNL Adobe Experience Platform Web SDK] steun aanbiedingen voor A4T opnieuw? {#platform}

+++Antwoord
De volgende veelgestelde vragen bieden meer informatie over het gebruik van een A4T en het omleiden van aanbiedingen met de [!DNL Platform Web SDK] .

+++

### Biedt Analytics for Target (A4T) ondersteuning voor omleidingsaanbiedingen?

+++Antwoord
Ja, A4T via het Web SDK van het Platform steunt [&#x200B; opnieuw gerichte aanbiedingen &#x200B;](/help/main/c-experiences/c-manage-content/offer-redirect.md).

+++

### Worden [!UICONTROL Visual Experience Composer] (VEC) en [!UICONTROL Form-Based Experience Composer] ondersteund?

+++Antwoord
Ja, [[!UICONTROL Visual Experience Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md) worden ondersteund als u ingebouwde omleidingsaanbiedingen gebruikt.

+++

## Wat zijn de minimumeisen om aanbiedingen om te leiden met A4T te gebruiken? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

+++Antwoord
Uw implementatie moet aan de volgende minimumvereisten voldoen:

* Experience Cloud Visitor ID Service: [!DNL visitorAPI.js] versie 2.3.0 of hoger.
* Adobe Analytics: [!DNL appMeasurement.js] versie 2.1.
* Adobe Target: [!DNL at.js] versie 1.6.2 of hoger.

De drie bibliotheken moeten op zowel de pagina met het omleidingsaanbod als de pagina worden opgenomen waarnaar de bezoeker wordt omgeleid.

+++

## Waarom zijn er soms gegevensdiscrepanties tussen A4T en Analytics?

+++Antwoord
Sommige gegevensdiscrepanties worden verwacht. Voor meer informatie, zie [&#x200B; Verwachte gegevensvariaties tussen Doel en Analytics wanneer het gebruiken van en het niet gebruiken van A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

+++

## Hoe kan ik discrepanties in verkeersdistributie minimaliseren wanneer het gebruiken van omleidingsaanbiedingen in A4T activiteiten? {#discrepancies}

+++Antwoord
Een beperkt aantal klanten heeft hogere mate van variatie in verkeersdistributie gemeld wanneer het gebruiken van omleidingsaanbiedingen in activiteiten die met [!UICONTROL Analytics for Target] (A4T) worden gevormd.

Overweeg het volgende:

* Onjuiste volgorde van aanroepen [!DNL Target] en [!DNL Analytics] kan de oorzaak zijn van hogere mate van variatie.

  De aanroep van [!DNL Target] moet voorafgaan aan de aanroep van [!DNL Analytics] op de bronpagina (waar omleiding plaatsvindt) en op de doelpagina (waar omleiding eindigt).

* Zorg ervoor dat u omleidingsaanbiedingen in A4T omleidingsactiviteiten gebruikt.
* Als er meerdere [!DNL Target] locatieaanvragen op de bronpagina staan (waar de omleiding plaatsvindt), raadt [!DNL Adobe] u aan de omleidingsactiviteit uit te voeren bij de eerste [!DNL Target] locatieaanvraag.

  Als u de omleidingsactiviteit uitvoert op de eerste [!DNL Target] locatieaanvraag, verkleint u de kans dat activiteitskwalificaties optreden op andere [!DNL Target] -locatieaanvragen en wordt het rapport geteld. Bezoekers die worden omgeleid, hoeven niet mee te tellen in de verslagen van andere activiteiten, aangezien zij de ervaringen niet zullen zien.

+++

## Waarom worden paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina soms geteld? {#section_B8F6CC2190B84CF08D945E797C5AF07B}

+++Antwoord
Wanneer u at.js versie 1.6.3 of hoger gebruikt, is het niet van belang om paginaweergaven op beide pagina&#39;s te tellen. Deze rasvoorwaarde beïnvloedt slechts klanten die vroegere versies gebruiken. Het team van het Doel handhaaft twee versies van at.js: de huidige versie en de tweede recentste versie. De verbetering at.js zonodig om ervoor te zorgen dat u a [&#x200B; gesteunde versie &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} in werking stelt.

Als u een vroegere, niet-gesteunde versie van at.js gebruikt, is er een mogelijkheid dat een rassenvoorwaarde kan voorkomen die de Analytische vraag zou kunnen veroorzaken om te vuren alvorens redirect op de eerste pagina uitvoert. Hierdoor kunnen paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina worden geteld. Deze situatie leidt tot een extra paginaweergave op de eerste pagina, wanneer de bezoeker deze eerste pagina nooit echt &#39;zag&#39;.

Het wordt aanbevolen om met de op formulieren gebaseerde composer een omleidingsactiviteit te maken om de omleiding van de pagina te versnellen, omdat de code op de pagina wordt uitgevoerd. Bovendien wordt het aangeraden een omleidingsaanbieding voor elke ervaring te maken, zelfs voor de standaardervaring, waarbij omleiding de oorspronkelijke pagina zou retourneren. Het creëren van een omleidingsaanbieding voor elke ervaring zorgt ervoor dat als fout-telling voorkomt, het over alle ervaringen gebeurt. Rapportage en analyse zijn nog steeds geldig voor de test.

Eén reden dat u omleidingsaanbiedingen wilt gebruiken voor alle ervaringen in de activiteit, inclusief de standaardeigenschap (controle), is om dezelfde voorwaarden op alle ervaringen te plaatsen. Bijvoorbeeld, als de standaardervaring geen omleidingsaanbod heeft maar de andere ervaringen hebben omleidingsaanbiedingen, heeft de snelheid van de ervaring zonder de omleidingsaanbieding een inherent voordeel. Aanbiedingen voor omleiding worden alleen aanbevolen voor tijdelijke scenario&#39;s, zoals testen. Het doorsturen van aanbiedingen wordt niet aanbevolen voor permanente scenario&#39;s, zoals personalisatie. Nadat u de winnaar hebt bepaald, moet u de omleiding verwijderen om de prestaties bij het laden van de pagina te verbeteren.

+++

## Wordt zowel Visual Experience Composer (VEC) als Form-Based Experience Composer ondersteund? {#section_FDA26FE7909B48539DA770559E687677}

+++Antwoord
Ja, beide composers worden ondersteund zolang u de ingebouwde omleidingsaanbiedingen gebruikt.

Als u uw eigen aangepaste code voor omleiding gebruikt, moet u ervoor zorgen dat u de twee nieuwe parameters vult die aan omleiding URLs ( `adobe_mc_sdid` en `adobe_mc_ref` worden geassocieerd, hieronder verklaard).

+++

## Wat zijn de nieuwe parameters van het vraagkoord toegevoegd aan omleiding URLs? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

+++Antwoord
De volgende parameters van het vraagkoord worden geassocieerd met omleidingsaanbiedingen:

| Parameter | Beschrijving |
|--- |--- |
| `adobe_mc_sdid` | De parameter `adobe_mc_sdid` geeft de aanvullende gegevens-id (SDID) en Experience Cloud-code-id door van de standaardpagina naar de nieuwe pagina. Met deze id&#39;s kan A4T het doelverzoek samenvoegen op de standaardpagina met het analyseverzoek op de nieuwe pagina.<br> Het verwachte formaat dat in url (voor hybride apps of van één app aan de website of één website aan een andere) wordt overgegaan is `ex. adobe_mc_sdid=SDID=123\|MCORGID=123456789@AdobeOrg\|TS=1498569322` |
| `adobe_mc_ref` | De parameter `adobe_mc_ref` geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Bij gebruik met AppMeasurement.js versie 2.1 (of hoger) gebruikt Analytics deze parameterwaarde als verwijzende URL op de nieuwe pagina. |

Deze parameters worden automatisch toegevoegd aan omleiding URLs wanneer het gebruiken van de ingebouwde omleidingsaanbiedingen in VEC en op vorm-Gebaseerde Composer van de Ervaring wanneer de dienst van Bezoeker Id op de pagina wordt uitgevoerd. Als u uw eigen aangepaste omleidingscode in de VEC of op vorm gebaseerde Composer gebruikt, moet u ervoor zorgen dat u deze parameters doorgeeft met uw aangepaste code.

+++

## Mijn webservers verwijderen deze parameters van mijn URL&#39;s. Wat moet ik doen? {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

+++Antwoord
Werk samen met uw IT-team om deze parameters ( `adobe_mc_sdid` en `adobe_mc_ref` ) te laten gevoegd op lijst van gewenste personen.

+++

## Wat als ik geen A4T met mijn omleidingsactiviteit gebruik en niet deze extra parameters aan mijn URLs wil hebben toevoegen? {#section_9E608D75FF9349FE96C65FEDD7539F45}

+++Antwoord
Gebruik een aangepaste omleiding als:

* U gebruikt geen A4T met uw omleidingsactiviteit
* De service Visitor-id is geïmplementeerd
* U wilt niet dat deze parameters automatisch aan uw URLs worden toegevoegd

Het is echter aan te raden de parameter `adobe_mc_ref` in de URL te houden om de verwijzingsgegevens correct aan [!DNL Analytics] te melden.

+++

## Waarom zijn de parameters adobe_mc_ref en adobe_mc_sdid dubbel-URL gecodeerd in mijn implementatie? {#section_5EFE5F012B944C40865731EA18E7E79E}

+++Antwoord
Als u aanbiedingen A4T gebruikt en omleidt, voegt Target de parameters `adobe_mc_ref` en `adobe_mc_sdid` aan URL toe. Deze waarden zijn al gecodeerd met URL. Meestal werkt alles zoals verwacht, echter, zouden sommige klanten ladingsbalancers of servers kunnen hebben WEB die proberen om de parameters van het vraagkoord één meer keer te coderen.

Vanwege deze dubbele codering wanneer de bezoeker-API de waarde `adobe_mc_sdid` probeert te decoderen, kan deze de waarde van de SDID niet extraheren en wordt een nieuwe SDID gegenereerd. Dit proces leidt tot onjuiste waarden SDID die naar Doel en Analytics worden verzonden en u ziet ongelijkmatige verdeling voor herleidingen in de rapporten van de Analyse.

Adobe raadt u aan contact op te nemen met uw IT-team om ervoor te zorgen dat `adobe_mc_ref` en `adobe_mc_sdid` gevoegd op lijst van gewenste personen zijn, zodat deze waarden op geen enkele manier worden getransformeerd.

+++

## Waarom moet de verwijzende URL aan de nieuwe pagina worden overgegaan? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

+++Antwoord
Veronderstel dat een bezoeker een verbinding op [!DNL `www.google.com`] aan uw homepage (`www.mysite.com/index.html`) klikt waarop een omleidingsactiviteit levend is en dan aan een nieuwe pagina (`www.mysite.com/index2.html`) wordt opnieuw gericht.

Eerder rapporteerde de [!DNL Analytics] aanvraag op de nieuwe pagina een verwijzende URL van [!DNL `www.mysite.com/index.html`] in plaats van [!DNL `www.google.com`] . Dit heeft geleid tot onjuiste rapportage in [!DNL Analytics] die is gekoppeld aan de verwijzende URL&#39;s (bijvoorbeeld marketingrapporten). De rapporten hadden het feit verloren dat u vanaf [!DNL `www.google.com`] naar de site kwam.

Bij [!DNL at.js] versie 0.9.6 (of hoger) en [!DNL AppMeasurement.js] 2.1 (of hoger) rapporteert de [!DNL Analytics] -aanvraag op de nieuwe pagina een referentie-URL van [!DNL `www.google.com`] .

+++

## Kan ik aangepaste of HTML omleidingsvoorstellen gebruiken? {#section_E49F9A83A286488C8F1098A040203D7E}

+++Antwoord
Nee, u moet een ingebouwde omleidingsaanbieding gebruiken voor activiteiten die [!DNL Analytics] als rapportbron (A4T) gebruiken. Vanuit het perspectief van [!DNL Target] zijn HTML-aanbiedingen ondoorzichtig: [!DNL Target] kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding instantieert.

+++

### Kan ik aangepaste of HTML omleidingsvoorstellen gebruiken met de [!DNL Platform Web SDK] ?

+++Antwoord
Nee, u moet een ingebouwde omleidingsaanbieding gebruiken voor activiteiten die A4T gebruiken. Vanuit het perspectief van [!DNL Target] zijn de HTML-aanbiedingen dekkend. [!DNL Target] kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding instantieert.

+++
