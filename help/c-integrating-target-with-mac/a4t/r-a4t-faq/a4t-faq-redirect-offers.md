---
keywords: faq;veelgestelde vragen;analytische gegevens voor doel;a4T;omleiden;aanbod omleiden;adobe-mc-sdid;adobe_mc_ref
description: Vind antwoorden op vragen over het gebruiken van redirect aanbiedingen wanneer het gebruiken van Analytics voor  [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] activiteiten.
title: Waar kan ik veelgestelde vragen vinden over omleidingsaanbiedingen met A4T?
feature: Analyses voor doel (A4T)
exl-id: 4706057f-bd8b-4562-94e0-be22b2e19297
source-git-commit: 3be6ad187b99472ccd3019e6998eba4953e2f5b5
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 0%

---

# Aanbiedingen omleiden - Veelgestelde vragen A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gevraagd over het gebruiken van omleidingsaanbiedingen wanneer het gebruiken van [!DNL Adobe Analytics] als rapporteringsbron voor [!DNL Adobe Target] (A4T).

## Biedt Analytics for Adobe Target (A4T) ondersteuning voor omleidingsaanbiedingen? {#section_46B8B03ED4D542C6AD875F5F61176298}

Ja, als uw implementatie [!DNL at.js] gebruikt. Uw implementatie moet echter voldoen aan de hieronder vermelde minimumvereisten om [aanbiedingen omleiden](/help/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) te kunnen gebruiken in activiteiten die Analytics als rapportagebron gebruiken.

>[!NOTE]
>
>Een bekende kwestie weggaat die een beperkt aantal klanten veroorzaakt die omleidingen met A4T gebruiken om een hoger percentage van unstitched hit tarieven te zien. Zie [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#redirect).

## Wat zijn de minimumeisen om aanbiedingen om te leiden met A4T te gebruiken? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

Uw implementatie moet aan de volgende minimumvereisten voldoen:

* Experience Cloud Bezoeker-id-service: [!DNL visitorAPI.js] versie 2.3.0 of hoger.
* Adobe Analytics: [!DNL appMeasurement.js] versie 2.1.
* Adobe Target: [!DNL at.js] versie 1.6.2 of hoger.

   De bibliotheek [!DNL mbox.js] biedt geen ondersteuning voor omleiding van aanbiedingen met A4T. Uw implementatie moet [!DNL at.js] gebruiken.

De drie bibliotheken moeten op zowel de pagina met het omleidingsaanbod als de pagina worden opgenomen waarnaar de bezoeker wordt omgeleid.

## Waarom zijn er soms gegevensdiscrepanties tussen A4T en Analytics?

Sommige gegevensdiscrepanties worden verwacht. Voor meer informatie, zie [Verwachte gegevensvariaties tussen Doel en Analytics wanneer het gebruiken en niet het gebruiken A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

## Waarom worden paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina soms geteld? {#section_B8F6CC2190B84CF08D945E797C5AF07B}

Wanneer u at.js versie 1.6.3 of hoger gebruikt, is het niet van belang om paginaweergaven op beide pagina&#39;s te tellen. Deze rasvoorwaarde beïnvloedt slechts klanten die vroegere versies gebruiken. Het team van het Doel handhaaft twee versies van at.js: de huidige versie en de tweede nieuwste versie. Voer desgewenst een upgrade uit bij .js om ervoor te zorgen dat u een [ondersteunde versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) uitvoert.

Als u een vroegere, niet-gesteunde versie van at.js gebruikt, is er een mogelijkheid dat een rassenvoorwaarde kan voorkomen die de Analytische vraag zou kunnen veroorzaken om te vuren alvorens redirect op de eerste pagina uitvoert. Hierdoor kunnen paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina worden geteld. Deze situatie leidt tot een extra paginaweergave op de eerste pagina, wanneer de bezoeker deze eerste pagina nooit echt &#39;zag&#39;.

Het wordt aanbevolen om met de op formulieren gebaseerde composer een omleidingsactiviteit te maken om de omleiding van de pagina te versnellen, omdat de code op de pagina wordt uitgevoerd. Bovendien wordt het aangeraden een omleidingsaanbieding voor elke ervaring te maken, zelfs voor de standaardervaring, waarbij omleiding de oorspronkelijke pagina zou retourneren. Het creëren van een omleidingsaanbieding voor elke ervaring zorgt ervoor dat als fout-telling voorkomt, het over alle ervaringen gebeurt. Rapportage en analyse zijn nog steeds geldig voor de test.

Eén reden dat u omleidingsaanbiedingen wilt gebruiken voor alle ervaringen in de activiteit, inclusief de standaardeigenschap (controle), is om dezelfde voorwaarden op alle ervaringen te plaatsen. Bijvoorbeeld, als de standaardervaring geen omleidingsaanbod heeft maar de andere ervaringen hebben omleidingsaanbiedingen, heeft de snelheid van de ervaring zonder de omleidingsaanbieding een inherent voordeel. Aanbiedingen voor omleiding worden alleen aanbevolen voor tijdelijke scenario&#39;s, zoals testen. Het doorsturen van aanbiedingen wordt niet aanbevolen voor permanente scenario&#39;s, zoals personalisatie. Nadat u de winnaar hebt bepaald, moet u de omleiding verwijderen om de prestaties bij het laden van de pagina te verbeteren.

Zie de informatie over &quot;Aanbiedingen doorsturen&quot; in [Bekende problemen](/help/r-release-notes/known-issues-resolved-issues.md#redirect) voor meer informatie over dit probleem.

## Kan ik omleidingsaanbiedingen met A4T gebruiken als ik de JavaScript-bibliotheek mbox.js gebruik? {#section_D2A8B182B7254D61A8BB2BCBA0C0F64A}

De bibliotheek [!DNL mbox.js] biedt geen ondersteuning voor omleiding van aanbiedingen met A4T. Uw implementatie moet [!DNL at.js] gebruiken.

## Wordt zowel Visual Experience Composer (VEC) als Form-Based Experience Composer ondersteund? {#section_FDA26FE7909B48539DA770559E687677}

Ja, beide composers worden ondersteund zolang u de ingebouwde omleidingsaanbiedingen gebruikt.

Als u uw eigen douanecode voor omleiding gebruikt, moet u ervoor zorgen dat u de twee nieuwe parameters verbonden aan omleiding URLs ( `adobe_mc_sdid` en `adobe_mc_ref`, hieronder verklaard) bevolkt.

## Wat zijn de nieuwe parameters van het vraagkoord toegevoegd aan omleiding URLs? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

De volgende parameters van het vraagkoord worden geassocieerd met omleidingsaanbiedingen:

| Parameter | Beschrijving |
|--- |--- |
| `adobe_mc_sdid` | De `adobe_mc_sdid` parameter gaat de Aanvullende Identiteitskaart van Gegevens (SDID) en identiteitskaart van de Experience Cloud van de Org van de standaardpagina tot de nieuwe pagina over. Met deze id&#39;s kan A4T het doelverzoek samenvoegen op de standaardpagina met het analyseverzoek op de nieuwe pagina. |
| `adobe_mc_ref` | De parameter `adobe_mc_ref` geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Wanneer deze parameter wordt gebruikt met AppMeturement.js versie 2.1 (of hoger), gebruikt Analytics deze parameterwaarde als verwijzende URL op de nieuwe pagina. |

Deze parameters worden automatisch toegevoegd aan omleiding URLs wanneer het gebruiken van de ingebouwde omleidingsaanbiedingen in VEC en op vorm-Gebaseerde Composer van de Ervaring wanneer de dienst van Bezoeker Id op de pagina wordt uitgevoerd. Als u uw eigen aangepaste omleidingscode in de VEC of op vorm gebaseerde Composer gebruikt, moet u ervoor zorgen dat u deze parameters doorgeeft met uw aangepaste code.

## Mijn webservers verwijderen deze parameters van mijn URL&#39;s. Wat moet ik doen? {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

Werk samen met uw IT-team om deze parameters ( `adobe_mc_sdid` en `adobe_mc_ref`) te laten gevoegd op lijst van gewenste personen.

## Wat als ik geen A4T met mijn omleidingsactiviteit gebruik en niet deze extra parameters aan mijn URLs wil hebben toevoegen? {#section_9E608D75FF9349FE96C65FEDD7539F45}

Gebruik een aangepaste omleiding als:

* U gebruikt geen A4T met uw omleidingsactiviteit
* De service Visitor-id is geïmplementeerd
* U wilt niet dat deze parameters automatisch aan uw URLs worden toegevoegd

Nochtans, als beste praktijken, zou u de `adobe_mc_ref` parameter in URL kunnen willen houden om de verwijzingsinformatie aan [!DNL Analytics] correct te melden.

## Waarom zijn de parameters adobe_mc_ref en adobe_mc_sdid dubbel-URL gecodeerd in mijn implementatie? {#section_5EFE5F012B944C40865731EA18E7E79E}

Als u aanbiedingen A4T gebruikt en omleidt, voegt Target de parameters `adobe_mc_ref` en `adobe_mc_sdid` aan URL toe. Deze waarden zijn al gecodeerd met URL. Meestal werkt alles zoals verwacht, echter, zouden sommige klanten ladingsbalancers of servers kunnen hebben WEB die proberen om de parameters van het vraagkoord één meer keer te coderen.

Vanwege deze dubbele codering wanneer de bezoeker-API de waarde `adobe_mc_sdid` probeert te decoderen, kan deze de SDID-waarde niet extraheren en wordt een nieuwe SDID gegenereerd. Dit proces leidt tot onjuiste waarden SDID die naar Doel en Analytics worden verzonden en u ziet ongelijkmatige verdeling voor herleidingen in de rapporten van de Analyse.

Adobe raadt u aan contact op te nemen met uw IT-team om ervoor te zorgen dat `adobe_mc_ref` en `adobe_mc_sdid` zijn gevoegd op lijst van gewenste personen, zodat deze waarden op geen enkele manier worden getransformeerd.

## Waarom moet de verwijzende URL aan de nieuwe pagina worden overgegaan? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

Stel dat een bezoeker op een koppeling [!DNL `www.google.com`] naar uw startpagina (`www.mysite.com/index.html`) klikt waarop een omleidingsactiviteit actief is en vervolgens wordt omgeleid naar een nieuwe pagina (`www.mysite.com/index2.html`).

Eerder zou het [!DNL Analytics] verzoek op de nieuwe pagina een verwijzende URL van [!DNL `www.mysite.com/index.html`] in plaats van [!DNL `www.google.com`] melden. Dit veroorzaakte onjuiste rapportering in [!DNL Analytics] verbonden aan verwijzende URLs (de rapporten van het Kanaal van de Marketing, bijvoorbeeld). De rapporten hadden het feit verloren dat u vanaf [!DNL `www.google.com`] naar de site kwam.

Met [!DNL at.js] versie 0.9.6 (of later) en [!DNL AppMeasurement.js] 2.1 (of later), meldt het [!DNL Analytics] verzoek op de nieuwe pagina een verwijzende URL van [!DNL `www.google.com`].

## Kan ik aangepaste/HTML-omleidingsvoorstellen gebruiken? {#section_E49F9A83A286488C8F1098A040203D7E}

Nee, u moet een ingebouwde omleidingsaanbieding gebruiken voor activiteiten die [!DNL Analytics] als rapportagebron (A4T) gebruiken. Vanuit het perspectief van [!DNL Target] zijn de HTML-aanbiedingen ondoorzichtig: [!DNL Target] kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding concretiseert.

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) badgeBiedt de  [!DNL Adobe Experience Platform Web SDK] ondersteuning een omleiding voor A4T? {#platform}

De volgende FAQs verstrekt meer informatie over het gebruiken van A4T en richt aanbiedingen met [!DNL Platform Web SDK] om.

>[!NOTE]
>
>A4T-ondersteuning in een [!DNL Adobe Experience Platform Web SDK]-implementatie die in dit artikel wordt besproken, is volgens de planning beschikbaar met de [!DNL Platform Web SDK] versie 2.5.0-release (1 juni 2021).

### Biedt Analytics for Target (A4T) ondersteuning voor omleidingsaanbiedingen?

Ja, A4T via het Web SDK van het Platform steunt [redirect aanbiedingen](/help/c-experiences/c-manage-content/offer-redirect.md).

### Wordt [!UICONTROL Visual Experience Composer] (VEC) en [!UICONTROL Form-Based Experience Composer] gesteund?

Ja, de [[!UICONTROL Visual Experience Composer]](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en [[!UICONTROL Form-Based Experience Composer]](/help/c-experiences/form-experience-composer.md) worden gesteund als u ingebouwde herleidingsaanbiedingen gebruikt.

### Kan ik aangepaste/HTML-omleidingsvoorstellen gebruiken met de [!DNL Platform Web SDK]?

Nee, u moet een ingebouwde omleidingsaanbieding gebruiken voor activiteiten die A4T gebruiken. Vanuit het perspectief van [!DNL Target], zijn de aanbiedingen van HTML ondoorzichtig. [!DNL Target] Kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding instantieert.
