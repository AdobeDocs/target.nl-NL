---
keywords: qa;qa, modus; activiteit qa;qa url;qa urls;voorvertoning url;voorvertoning urls
description: Leer hoe te om Adobe  [!DNL Target]  QA URLs te gebruiken om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richtend, en QA rapporterend die van levende activiteitengegevens gesegmenteerd blijft.
title: Hoe kan ik QA-activiteiten uitvoeren?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 99ea312405e397e97e64e32d2685e8a6966d8928
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 0%

---

# Activiteit QA

Gebruik URL&#39;s met kwaliteitsgarantie in [!DNL Adobe Target] om eenvoudige end-to-end activiteit-QA met voorvertoningskoppelingen uit te voeren die nooit veranderen, optionele publieksgerichtheid en QA-rapportage die gesegmenteerd blijft van live-activiteitgegevens.

Met [!UICONTROL Activity QA] kunt u uw [!DNL Target] -activiteiten volledig testen voordat u deze live start. De functionaliteit [!UICONTROL Activity QA] omvat:

* Verbindingen om met teamleden te delen die nooit veranderen of regeneratie vereisen, ongeacht updates die aan de ervaringen of de activiteiten worden aangebracht. Met deze functie kunt u uw activiteiten volledig testen tijdens de hele gebruikersreis.
* De voorwaarden van het publiek naar keuze gerespecteerd zodat kunnen de marketers het richten van criteria testen of het richten van criteria aan QA de verschijning van ervaringen negeren zonder het moeten aan de publieksvoorwaarden voldoen.
* QA-rapportage wordt vastgelegd zodat marketers kunnen bevestigen dat de metriek naar verwachting toeneemt en dat de QA-rapportgegevens gescheiden worden gehouden van productierapportage (voor niet-A4T-rapportage).
* De mogelijkheid om een ervaring afzonderlijk of met andere live activiteiten te bekijken die aan de leveringscriteria voldoen (pagina/[!DNL Target] verzoek/publiek).
* De mogelijkheid om een kwaliteitscontrole uit te voeren voor de hele gebruikersreis. U hebt eenmalig toegang tot uw site met de koppeling voor kwaliteitscontrole en bladert vervolgens door de gehele site in Activiteit QA. U blijft in Activiteit QA tot u de zitting beëindigt of tot u [&#x200B; QA bookmarklet van het Doel &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) gebruikt om zich uit [!UICONTROL Activity QA] te dwingen. Deze functie is handig als u een activiteit hebt die meerdere webpagina&#39;s beslaat.

  >[!NOTE]
  >
  >Deze functionaliteit geldt voor at.js-implementaties met versie 2.*x* of later. Voor om.js 1.*x* implementaties, is deze functionaliteit waar slechts als browser van de bezoeker geen derdekoekjes blokkeert.

## Een URL voor een kwaliteitscontrole openen en delen {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Klik op [!UICONTROL Overview] op de pagina van een activiteit **[!UICONTROL Activity QA]** .

1. Configureer de volgende instellingen:

   * **[!UICONTROL Match audience rules to see experiences]:** Soms wilt u bevestigen dat uw publiek het aanpassen werkt. Andere tijden wilt u de blik en het gevoel van de activiteit controleren. Als deze instelling wordt overgeschakeld naar de &quot;aan&quot;-positie, moeten de testers voldoen aan de vereisten voor doelwitten om in aanmerking te komen voor het bekijken van de ervaringen. Voor Experience Targeting (XT)-activiteiten wordt één activiteit-URL opgegeven. De ervaring die u ziet, wordt bepaald door u die in aanmerking komt voor een van de doelregels.

     Als u deze instelling in- of uitschakelt, kunt u door op de koppelingen te klikken de ervaringen weergeven, ongeacht of u hiervoor in aanmerking komt of niet. Wanneer het uitvoeren van QA, kunt u afwisselend tussen vereisen of niet vereisen dat het publiek richt wordt gerespecteerd.

   * **toon standaardinhoud voor alle andere activiteiten:** als deze optie aan de &quot;op&quot;positie van een knevel wordt voorzien, wordt de standaardinhoud getoond voor alle andere activiteiten. Bijvoorbeeld, wordt de voorproef getoond geïsoleerd zonder alle andere levende activiteiten op de zelfde pagina/ [!DNL Target] verzoek te overwegen.

     Als deze instelling wordt uitgeschakeld, kunt u het volgende overwegen:

      * Als er botsingen tussen de activiteit zijn u en andere levende activiteiten test, [&#x200B; normale prioritaire regels &#x200B;](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) van toepassing zijn. Wegens botsingen, is het mogelijk u niet de activiteit kunt zien die u aan QA van plan bent.
      * De toename van metriek voor de bekeken activiteiten, maar slechts in het QA rapporterend milieu.

1. Klik op **[!UICONTROL Done]** om de wijzigingen op te slaan.
1. Deel de activiteiten link URLs met leden van uw organisatie voor het testen.

   Activiteitenkoppelingen verlopen nooit en u hoeft de koppelingen niet opnieuw te verzenden als iemand een activiteit of ervaring wijzigt. Als u echter een ander publiek toepast dan de [!UICONTROL Audience Library] , in plaats van gewoon de activiteit te bewerken, wordt een nieuwe koppeling gegenereerd die u opnieuw moet delen.

   Met elke URL voor de activiteitenkoppeling (voor Experience A, Experience B enzovoort) kunt u de gebruikersreis starten vanuit de bijbehorende ervaring. Klik op de URL die voor een ervaring is gegenereerd en ga verder met het bladeren door de normale site om ervaringen op meerdere pagina&#39;s te zien (als er meerdere pagina&#39;s zijn). Er wordt slechts één URL gegenereerd per ervaring, zelfs als de ervaring meerdere pagina&#39;s beslaat (sjabloontesten of meerdere pagina&#39;s testen).

   U kunt op de site navigeren om de andere pagina&#39;s weer te geven, omdat de modus [!UICONTROL Activity QA] vast is. Deze situatie geldt voor at.js-implementaties met versie 2.*x* of later. Voor om.js 1.*x* implementaties, is deze situatie waar slechts als browser van de bezoeker geen derdekoekjes blokkeert.

1. Om rapporten te zien die van activiteit worden geproduceerd verbind URLs, klik de pagina van de activiteit **[!UICONTROL Reports]**, klik het **[!UICONTROL Settings]** pictogram ( ![&#x200B; icon_tandbeeld &#x200B;](assets/icon_gear.png) ), dan selecteer **[!UICONTROL QA Mode Traffic]** van **[!UICONTROL Environment]** drop-down lijst.

## Het vrijgeven van zich van wijze QA

[!UICONTROL Activity QA] blijft behouden. Nadat u in [!UICONTROL Activity QA] door een website hebt gebladerd, moet de [!DNL Target] -sessie verlopen of moet [!DNL Target] u loslaten vanuit [!UICONTROL Activity QA] voordat u uw site als een doorsnee bezoeker kunt weergeven.

### te.js 2.*x*

Als uw site op 0,js 2 staat.*x* opgesteld, gebruik [&#x200B; QA bookmarklet van het Doel &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) om zich uit [!UICONTROL Activity QA] te dwingen. Het laden van een pagina op uw plaats met een lege waarde, zoals die in de volgende kogel wordt beschreven, verwijdert *niet* het koekje QA van browser wanneer at.js 2.*x* wordt opgesteld.

### te.js 1.*x*

Als uw site is ingesteld op 0,js 1.*x* opgesteld, naast het gebruiken van [&#x200B; QA bookmarklet van het Doel &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), kunt u zich ook manueel dwingen uit door een pagina op uw plaats met de `at_preview_token` parameter met een lege waarde te laden. Bijvoorbeeld:

`https://www.mysite.com/?at_preview_token=`

### [!DNL Adobe Experience Platform Web SDK]

Als de [[!UICONTROL Platform Web SDK] &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} is geïmplementeerd op uw site, kunt u uzelf handmatig afdwingen door een pagina op uw site te laden met de parameter `at_qa_mode` met een lege waarde. Bijvoorbeeld:

`https://www.mysite.com/?at_qa_mode=`

## Overwegingen {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Omdat Activity QA nu beschikbaar is voor alle [!DNL Target] -activiteitstypen, is de functie &#39;Voorvertonen van Automated Personalization-activiteiten met voorbeeld-URL&#39;s&#39; niet langer nodig.
* [!UICONTROL Activity QA] koppelingen voor opgeslagen activiteiten worden mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Het opnieuw proberen van de voorproefverbindingen zou moeten werken. Om te voorkomen dat deze situatie zich blijft voordoen, archiveert u opgeslagen activiteiten die niet meer actief worden gebruikt.
* [!UICONTROL Activity QA] URLs is beschikbaar met activiteiten met [&#x200B; Analytics als rapporterende bron &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). De uren die tijdens het uitvoeren van QA gebruikend [!UICONTROL Activity QA] worden geproduceerd stromen aan de zelfde rapportreeks waar de de gegevensstromen van de activiteit zelfs nadat de activiteit levend gaat.
* [!UICONTROL Activity QA] geeft geen inhoud weer voor gearchiveerde activiteiten of activiteiten die hun einddatum hebben bereikt. Als u een beëindigde activiteit deactiveert, moet u de activiteit opnieuw bewaren voor [!UICONTROL Activity QA] om te werken.
* Activiteiten die worden geïmporteerd in [!DNL Target Standard/Premium] (bijvoorbeeld vanuit [!DNL Target Classic] ) ondersteunen geen URL&#39;s met kwaliteitscontrole.
* Bij [!UICONTROL Auto-Allocate] - en [!UICONTROL Recommendations] -activiteiten wordt het model niet beïnvloed door de bezoeken die worden vastgelegd in [!UICONTROL Activity QA] .
* Als u &quot;URL&quot;specificeert terwijl het creëren van de activiteit [&#x200B; verfijningen in de op vorm-gebaseerde Composer &#x200B;](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) of [&#x200B; de opties van de paginalevering in de Visuele Composer van de Ervaring) &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81) specificeert, werkt QA URL niet omdat [!UICONTROL Activity QA] parameters URL toevoegt. Als u dit probleem wilt verhelpen, klikt u op de URL voor de kwaliteitscontrole om naar uw site te gaan, verwijdert u de toegevoegde parameters uit de URL en laadt u vervolgens de nieuwe URL.
* Als u at.js 1 hebt.*x*, [!UICONTROL Activity QA] wijze is niet kleverig als u Safari of een andere browser gebruikt die derdekoekjes blokkeert. In deze gevallen moet u de voorvertoningsparameters toevoegen aan elke URL waarnaar u navigeert. Het zelfde is waar als u [&#x200B; CNAME &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html?lang=nl-NL){target=_blank} hebt uitgevoerd.
* Als een activiteit veelvoudige ervaringspubliek gebruikt (bijvoorbeeld, een plaats van de V.S. en van het VK die in de zelfde activiteit inbegrepen zijn), worden de verbindingen van QA niet geproduceerd voor de vier combinaties (Ervaring A/US Plaats, Ervaring A/UK Plaats, Ervaring B/US Plaats, Ervaring B/UK Plaats). Er worden slechts twee QA-koppelingen (Experience A en Experience B) gemaakt en gebruikers moeten in aanmerking komen voor het juiste publiek om de pagina te kunnen zien. Een Britse QA-persoon kan de Amerikaanse site niet zien.
* Alle parameters en waarden van `at_preview` zijn al gecodeerd met URL. Meestal werkt alles zoals verwacht. Nochtans, moeten sommige klanten balancers of de servers van het Web laden die proberen om de parameters van het vraagkoord opnieuw te coderen.

  Vanwege deze dubbele codering kan [!DNL Target] wanneer de code `at_preview_token` wordt gedecodeerd, de juiste tokenwaarde niet worden opgehaald. De voorvertoning werkt dus niet. [!DNL Target]

  [!DNL Adobe] raadt u aan contact op te nemen met uw IT-team om ervoor te zorgen dat alle voorvertoningsparameters worden gevoegd op lijst van gewenste personen, zodat deze waarden op geen enkele manier worden getransformeerd.

  De volgende lijst maakt een lijst van de parameters die in uw domein kunnen worden gevoegd op lijst van gewenste personen:

  | Parameter | Type | Waarde | Beschrijving |
  |--- |--- |--- |--- |
  | `at_preview_token` | Versleutelde tekenreeks | Verplicht; geen standaardwaarde | Een gecodeerde entiteit die de lijst van campagnes IDs bevat die op wijze kunnen worden uitgevoerd QA. |
  | `at_preview_index` | String | Leeg | Het formaat van de parameter is `<campaignIndex>` of `<campaignIndex>_< experienceIndex>`<br> beide indexen beginnen met 1. |
  | `at_preview_listed_activities_only` | Boolean (true/false) | Standaardwaarde: false | Indien &quot;true&quot;, worden alle campagnes die in de parameters `at_preview_index` zijn opgegeven, verwerkt.<br> als &quot;vals,&quot;alle campagnes van de pagina worden verwerkt, zelfs als zij niet in het voorproefteken werden gespecificeerd. |
  | `at_preview_evaluate_as_true_audience_ids` | String | Leeg | Lijst met segmentenId&#39;s die door onderstrepingsteken van elkaar zijn gescheiden (&quot;_&quot;) en die altijd (op doelniveau en rapportageniveau) als &quot;waar&quot; moeten worden beschouwd in het bereik van de [!DNL Target] aanvraag. |
  | `_AT_Debug` | String | Venster of console | Logboekregistratie voor console of nieuw venster. |
  | `adobe_mc_ref` |  |  | Geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Wanneer `AppMeasurement.js` versie 2.1 (of hoger) wordt gebruikt, gebruikt [!DNL Adobe Analytics] deze parameterwaarde als verwijzende URL op de nieuwe pagina. |
  | `adobe_mc_sdid` |  |  | Geeft de standaardpagina [!DNL Supplemental Data Id] (SDID) en [!DNL Experience Cloud Org Id] door aan de nieuwe pagina. Als u deze id&#39;s doorgeeft, kan [!UICONTROL Analytics for Target] (A4T) de [!DNL Target] -aanvraag op de standaardpagina samenvoegen met de [!DNL Analytics] -aanvraag op de nieuwe pagina. |

* De gebruikersinterface van [!UICONTROL Target QA Mode] toont alleen de eerste URL van een ervaring in een activiteit van meerdere pagina&#39;s. De veronderstelling is dat u een reistest creeert en u zich van URL1 aan URL2 beweegt. Als u echter onafhankelijk naar URL2 wilt gaan, kopieert u alle URL-parameters die via URL1 zijn opgegeven en past u deze toe op URL2 nadat u een &#39;?&#39; hebt geplaatst net als in URL1.
* De QA-voorbeeldkoppelingen voor activiteit voor opgeslagen activiteiten worden mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Probeer de voorbeeldkoppelingen opnieuw. Opgeslagen activiteiten archiveren die niet meer actief worden gebruikt om te voorkomen dat dit probleem zich blijft voordoen.

## Compatibiliteit met de JavaScript-doelbibliotheek [!UICONTROL QA Mode] {#compatibility}

[!DNL Target] ondersteunt de volgende JavaScript-bibliotheken:

* [&#x200B; at.js 1.x &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=nl-NL)
* [&#x200B; at.js 2.x &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=nl-NL)
* [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html)

In de volgende tabel worden de verschillende typen activiteiten vermeld en wordt aangegeven of de modus [!UICONTROL Activity QA] wordt ondersteund voor elke bibliotheek:

| Type activiteit | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B Test] | Ja | Ja | Ja |
| [!UICONTROL Auto-Allocate] | Ja | Ja | Ja |
| [!UICONTROL Auto-Target] | Ja | Ja | Ja |
| [!UICONTROL Automated Personalization] (AP) | Ja | Ja | Ja |
| [!UICONTROL Experience Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Test] (MV) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |