---
keywords: faq;frequently asked questions;analytics for target;a4T;redirect;redirect offer;adobe-mc-sdid;adobe_mc_ref
description: Dit onderwerp bevat antwoorden op vragen die vaak worden gevraagd over het gebruiken van doorverwijzing aanbiedingen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Aanbiedingen omleiden - Veelgestelde vragen A4T
topic: Standard
uuid: a45cef89-3003-4177-bf84-3d5a486b950d
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Aanbiedingen omleiden - Veelgestelde vragen A4T{#redirect-offers-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak worden gevraagd over het gebruiken van doorverwijzing aanbiedingen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).

## Biedt Analytics for Target (A4T) ondersteuning voor omleidingsaanbiedingen? {#section_46B8B03ED4D542C6AD875F5F61176298}

Ja, op voorwaarde dat uw implementatie wordt gebruikt [!DNL at.js]. Uw implementatie moet echter voldoen aan de onderstaande minimumvereisten om [omleidingsaanbiedingen](../../../c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) te kunnen gebruiken voor activiteiten die Analytics als rapportagebron gebruiken.

>[!NOTE]
>
>Een bekende kwestie weggaat die een beperkt aantal klanten veroorzaakt die omleidingen met A4T gebruiken om een hoger percentage van unstitched hit tarieven te zien. Bekende [problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#redirect)bekijken.

## Wat zijn de minimumeisen die nodig zijn om omleidingsaanbiedingen met A4T te gebruiken? {#section_FA9384C2AA9D41EDBCE263FFFD1D9B58}

Uw implementatie moet aan de volgende minimumvereisten voldoen:

* Experience Cloud Visitor ID Service: [!DNL visitorAPI.js] versie 2.3.0 of hoger.
* Adobe Analytics: [!DNL appMeasurement.js] versie 2.1.
* Adobe-doel: [!DNL at.js] versie 1.6.2 of hoger.

   De [!DNL mbox.js] bibliotheek ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet worden gebruikt [!DNL at.js].

De drie bibliotheken moeten op zowel de pagina met het omleidingsaanbod als de pagina worden opgenomen waarnaar de bezoeker wordt omgeleid.

## Waarom zijn er soms gegevensdiscrepanties tussen A4T en Analytics?

Sommige gegevensdiscrepanties worden verwacht. Voor meer informatie, zie de [Verwachte gegevensvariaties tussen Doel en Analytics wanneer het gebruiken van en niet het gebruiken van A4T](/help/c-integrating-target-with-mac/a4t/understanding-expected-data-variances.md).

## Waarom worden paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina soms geteld? {#section_B8F6CC2190B84CF08D945E797C5AF07B}

Bij gebruik van at.js versie 1.6.3 of hoger is dit geen probleem. Deze rasvoorwaarde beïnvloedt slechts klanten die vroegere versies gebruiken. Het team van het Doel handhaaft twee versies van at.js: de huidige versie en de tweede nieuwste versie. Voer indien nodig een upgrade naar .js uit om ervoor te zorgen dat u een [ondersteunde versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)gebruikt.

Als u een vroegere, niet-gesteunde versie van at.js gebruikt, is er een mogelijkheid dat een rassenvoorwaarde kan voorkomen die de Analytische vraag zou kunnen veroorzaken om te vuren alvorens redirect op de eerste pagina uitvoert. Hierdoor kunnen paginaweergaven op de oorspronkelijke pagina en op de omleidingspagina worden geteld. Deze situatie leidt tot een extra paginaweergave op de eerste pagina, wanneer de bezoeker deze eerste pagina nooit echt &#39;zag&#39;.

Het wordt aanbevolen om met de op formulieren gebaseerde composer een omleidingsactiviteit te maken om de omleiding van de pagina te versnellen. Dit komt doordat de code op de pagina wordt uitgevoerd. Bovendien wordt het aangeraden een omleidingsaanbieding voor elke ervaring te maken, zelfs voor de standaardervaring, waarbij omleiding de oorspronkelijke pagina zou retourneren. Dit zorgt ervoor dat als er sprake is van foutief tellen, dit gebeurt in alle ervaringen, zodat rapportage en analyse nog steeds geldig zijn voor de test.

Eén reden dat u omleidingsaanbiedingen wilt gebruiken voor alle ervaringen in de activiteit, inclusief de standaardeigenschap (controle), is om dezelfde voorwaarden op alle ervaringen te plaatsen. Bijvoorbeeld, als de standaardervaring geen omleidingsaanbod heeft maar de andere ervaringen hebben omleidingsaanbiedingen, heeft de snelheid van de ervaring zonder de omleidingsaanbieding een inherent voordeel. Aanbiedingen voor omleiding worden alleen aanbevolen voor tijdelijke scenario&#39;s, zoals testen. Het doorsturen van aanbiedingen wordt niet aanbevolen voor permanente scenario&#39;s, zoals personalisatie. Nadat u de winnaar hebt bepaald, moet u de omleiding verwijderen om de prestaties bij het laden van de pagina te verbeteren.

Zie de informatie over aanbiedingen doorsturen in [Bekende problemen](/help/r-release-notes/known-issues-resolved-issues.md#redirect)voor meer informatie over dit probleem.

## Kan ik omleidingsaanbiedingen met A4T gebruiken als ik de JavaScript-bibliotheek mbox.js gebruik? {#section_D2A8B182B7254D61A8BB2BCBA0C0F64A}

De [!DNL mbox.js] bibliotheek ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet worden gebruikt [!DNL at.js].

## Wordt zowel Visual Experience Composer (VEC) als Form-Based Experience Composer ondersteund? {#section_FDA26FE7909B48539DA770559E687677}

Ja, beide composers worden ondersteund zolang u de ingebouwde omleidingsaanbiedingen gebruikt.

Als u uw eigen aangepaste code voor omleiding gebruikt, moet u ervoor zorgen dat u de twee nieuwe parameters vult die aan omleiding URLs ( `adobe_mc_sdid` en `adobe_mc_ref`, hieronder verklaard) worden geassocieerd.

## Wat zijn de nieuwe parameters van het vraagkoord toegevoegd aan omleiding URLs? {#section_BA73E8B3CFCC4CBEB5BE3F76B2BC8682}

De volgende parameters van het vraagkoord worden geassocieerd met omleidingsaanbiedingen:

| Parameter | Beschrijving |
|--- |--- |
| `adobe_mc_sdid` | De `adobe_mc_sdid` parameter gaat Supplemental identiteitskaart van Gegevens (SDID) en de Identiteitskaart van de Wolk van de Ervaring van de standaardpagina tot de nieuwe pagina over zodat A4T &quot;samen&quot;het verzoek van het Doel op de standaardpagina met het Analytische verzoek op de nieuwe pagina. |
| `adobe_mc_ref` | De `adobe_mc_ref` parameter geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Wanneer deze parameter wordt gebruikt met AppMeturement.js versie 2.1 (of hoger), gebruikt Analytics deze parameterwaarde als verwijzende URL op de nieuwe pagina. |

Deze parameters worden automatisch toegevoegd aan omleiding URLs wanneer het gebruiken van de ingebouwde omleidingsaanbiedingen in VEC en op vorm-Gebaseerde Composer van de Ervaring wanneer de dienst van Bezoeker Id op de pagina wordt uitgevoerd. Als u uw eigen aangepaste omleidingscode in de VEC of op vorm gebaseerde Composer gebruikt, moet u ervoor zorgen dat u deze parameters doorgeeft met uw aangepaste code.

## Mijn webservers verwijderen deze parameters van mijn URL&#39;s. Wat moet ik doen? {#section_0C2DDB72939F4875B6D0428B8DCB38E5}

U zult met uw team van IT moeten werken om deze parameters ( `adobe_mc_sdid` en `adobe_mc_ref`) te hebben gewhitelisted.

## Wat als ik geen A4T met mijn omleidingsactiviteit gebruik en niet deze extra parameters aan mijn URLs wil hebben toevoegen? {#section_9E608D75FF9349FE96C65FEDD7539F45}

Als u geen A4T met uw omleidingsactiviteit gebruikt, hebt u de uitgevoerde dienst van identiteitskaart van de Bezoeker, en u wilt niet deze parameters automatisch aan uw URLs worden toegevoegd, moet u een douane-gecodeerde omleiding gebruiken.

Als beste praktijken kunt u de `adobe_mc_ref` parameter echter in de URL opnemen om de verwijzingsinformatie [!DNL Analytics] correct te rapporteren.

## Waarom zijn de parameters adobe_mc_ref en adobe_mc_sdid dubbel-URL gecodeerd in mijn implementatie? {#section_5EFE5F012B944C40865731EA18E7E79E}

Als u aanbiedingen A4T gebruikt en omleidt, voegt Target de `adobe_mc_ref` en de `adobe_mc_sdid` parameters aan URL toe. Deze waarden zijn al gecodeerd met URL. Meestal werkt alles zoals verwacht, echter, zouden sommige klanten ladingsbalancers of servers kunnen hebben WEB die proberen om de parameters van het vraagkoord één meer keer te coderen.

Vanwege deze dubbele codering wanneer de bezoeker-API de `adobe_mc_sdid` waarde probeert te decoderen, kan deze de SDID-waarde niet extraheren en wordt een nieuwe SDID gegenereerd. Dit leidt tot onjuiste waarden SDID die naar Doel en Analytics worden verzonden en u zult ongelijkmatige verdeling voor herleidingen in de rapporten van de Analytics zien.

Wij adviseren dat u met hun team van IT spreekt om ervoor te zorgen dat `adobe_mc_ref` en `adobe_mc_sdid` wit-vermeld zodat deze waarden op geen enkele manier worden getransformeerd.

## Waarom moet de verwijzende URL aan de nieuwe pagina worden overgegaan? {#section_91AB8B0891F6416CBF7E973DCAF54EB5}

Stel dat een bezoeker op een koppeling klikt [!DNL `www.google.com`] naar uw homepage ( [!DNL `www.mysite.com/index.html]`) waarop een omleidingsactiviteit actief is en vervolgens wordt omgeleid naar een nieuwe pagina ( [!DNL `www.mysite.com/index2.html`]).

Voorheen zou het [!DNL Analytics] verzoek op de nieuwe pagina een verwijzende URL van in [!DNL `www.mysite.com/index.html`] plaats van [!DNL `www.google.com`]rapporteren. Dit veroorzaakte onjuiste rapportering in [!DNL Analytics] verband met verwijzende URLs (de rapporten van het Kanaal van de Marketing, bijvoorbeeld). De verslagen hadden het feit verloren dat u van [!DNL `www.google.com`]de plaats kwam.

Met [!DNL at.js] versie 0.9.6 (of hoger) en [!DNL AppMeasurement.js] 2.1 (of hoger) rapporteert het [!DNL Analytics] verzoek op de nieuwe pagina een referentie-URL van [!DNL `www.google.com`].

## Kan ik aangepaste/HTML-omleidingsvoorstellen gebruiken? {#section_E49F9A83A286488C8F1098A040203D7E}

Nee, u moet een ingebouwde omleidingsaanbieding gebruiken voor activiteiten die [!DNL Analytics] als rapportagebron (A4T) worden gebruikt. Vanuit [!DNL Target] perspectief zijn de HTML-aanbiedingen dekkend: [!DNL Target] kan niet weten dat een bepaald deel van HTML JavaScript bevat dat een omleiding concretiseert.
