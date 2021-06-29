---
keywords: qa;qa-modus; activiteit qa;qa url;qa urls;voorvertoning url;voorvertoning urls
description: Leer hoe te om Adobe [!DNL Target] QA URLs te gebruiken om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.
title: Hoe kan ik QA-activiteiten uitvoeren?
feature: Activiteiten
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 0d24bcf335980291891e3198a13ec283d1dd325f
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# Activiteit QA

Gebruik QA URLs in [!DNL Adobe Target] om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.

[!UICONTROL Activity QA] Hiermee kunt u uw  [!DNL Target] activiteiten volledig testen voordat u ze live start. De [!UICONTROL Activity QA]-functionaliteit omvat:

* Verbindingen om met teamleden te delen die nooit veranderen of regeneratie vereisen, ongeacht updates die aan de ervaringen of de activiteiten worden aangebracht. Met deze functie kunt u uw activiteiten volledig testen tijdens de hele gebruikersreis.
* De voorwaarden van het publiek naar keuze gerespecteerd zodat kunnen de marketers het richten van criteria testen of het richten van criteria aan QA de verschijning van ervaringen negeren zonder het moeten aan de publieksvoorwaarden voldoen.
* QA-rapportage wordt vastgelegd zodat marketers kunnen bevestigen dat de metriek naar verwachting toeneemt en dat de QA-rapportgegevens gescheiden worden gehouden van productierapportage (voor niet-A4T-rapportage).
* De mogelijkheid om een ervaring afzonderlijk of met andere live activiteiten die aan de leveringscriteria voldoen (pagina/doelverzoek/publiek) voor te vertonen.
* De mogelijkheid om een kwaliteitscontrole uit te voeren voor de hele gebruikersreis. U hebt eenmalig toegang tot uw site met de koppeling voor kwaliteitscontrole en bladert vervolgens door de gehele site in Activiteit QA. U blijft in Activiteit QA tot u de zitting beëindigt of tot u [QA de referentie van het Doel ](/help/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) gebruikt om uit [!UICONTROL Activity QA] te dwingen. Deze functie is handig als u een activiteit hebt die meerdere webpagina&#39;s omvat.

   >[!NOTE]
   >
   >Deze functionaliteit geldt voor at.js-implementaties met versie 2.** xor later. Voor om.js 1.*Deze* functionaliteit is alleen waar als de browser van de bezoeker cookies van derden niet blokkeert.

## Een URL voor een kwaliteitscontrole openen en delen {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Klik op de koppeling **[!UICONTROL Activity QA]** van de pagina [!UICONTROL Overview] van een activiteit.

   ![QA-koppeling voor activiteit](assets/qa_link.png)

1. Configureer de volgende instellingen:

   ![Opties voor QA-koppelingsconfiguratie](assets/qa_link_config.png)

   * **[!UICONTROL Match audience rules to see experiences]:** Soms wilt u bevestigen dat uw publiek het aanpassen werkt. Andere tijden wilt u de blik en het gevoel van de activiteit controleren. Als deze instelling wordt overgeschakeld naar de &quot;aan&quot;-positie, moeten de testers voldoen aan de vereisten voor doelwitten om in aanmerking te komen voor het bekijken van de ervaringen. Voor Experience Targeting (XT)-activiteiten wordt één activiteit-URL opgegeven. De ervaring die u ziet, wordt bepaald door u die in aanmerking komt voor een van de doelregels.

      Als u deze instelling in- of uitschakelt, kunt u door op de koppelingen te klikken de ervaringen weergeven, ongeacht of u hiervoor in aanmerking komt of niet. Wanneer het uitvoeren van QA, kunt u afwisselend tussen vereisen of niet vereisen dat het publiek richt wordt gerespecteerd.

   * **Standaardinhoud weergeven voor alle andere activiteiten:** Als deze optie wordt ingeschakeld, wordt standaardinhoud weergegeven voor alle andere activiteiten. Bijvoorbeeld, wordt de voorproef getoond afzonderlijk zonder alle andere levende activiteiten op de zelfde pagina/[!DNL Target] verzoek te overwegen.

      Als deze instelling wordt uitgeschakeld, kunt u het volgende overwegen:

      * Als er botsingen zijn tussen de activiteit u test en andere levende activiteiten, [normale prioritaire regels](/help/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) zijn van toepassing. Wegens botsingen, is het mogelijk u niet de activiteit kunt zien die u aan QA van plan bent.
      * De toename van metriek voor de bekeken activiteiten, maar slechts in het QA rapporterend milieu.

1. Klik **[!UICONTROL Done]** om uw veranderingen te bewaren.
1. Deel de activiteiten link URLs met leden van uw organisatie voor het testen.

   Activiteitenkoppelingen verlopen nooit en u hoeft de koppelingen niet opnieuw te verzenden als iemand een activiteit of ervaring wijzigt. Nochtans, als u een verschillend publiek van [!UICONTROL Audience Library] toepast, eerder dan eenvoudig het uitgeven van de activiteit, wordt een nieuwe verbinding geproduceerd die u moet opnieuw delen.

   Met elke URL voor de activiteitenkoppeling (voor Experience A, Experience B enzovoort) kunt u de gebruikersreis starten vanuit de bijbehorende ervaring. Klik op de URL die voor een ervaring is gegenereerd en ga verder met het bladeren door de normale site om ervaringen op meerdere pagina&#39;s te zien (als er meerdere pagina&#39;s zijn). Er wordt slechts één URL gegenereerd per ervaring, zelfs als de ervaring meerdere pagina&#39;s beslaat (sjabloontesten of meerdere pagina&#39;s testen).

   U kunt op de site navigeren om de andere pagina&#39;s weer te geven, omdat de modus [!UICONTROL Activity QA] vast is. Deze situatie geldt voor at.js-implementaties met versie 2.** xor later. Voor om.js 1.*Deze* situatie geldt alleen als de browser van de bezoeker cookies van derden niet blokkeert.

1. Als u rapporten wilt zien die zijn gegenereerd via de URL&#39;s van de activiteitenkoppeling, klikt u op de pagina **[!UICONTROL Reports]**, klikt u op het pictogram **[!UICONTROL Settings]** ( ![](assets/icon_gear.png) ) en selecteert u **[!UICONTROL QA Mode Traffic]** in de vervolgkeuzelijst **[!UICONTROL Environment]**.

## Overwegingen {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* De koppeling [!UICONTROL Activity QA] wordt weergegeven op de pagina [!UICONTROL Overview] van alle typen activiteiten, behalve [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] (AP).
* [!UICONTROL Activity QA] het voorbeeld van koppelingen voor opgeslagen activiteiten wordt mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Het opnieuw proberen van de voorproefverbindingen zou moeten werken. Om te voorkomen dat deze situatie zich blijft voordoen, archiveert u opgeslagen activiteiten die niet meer actief worden gebruikt.
* [!UICONTROL Activity QA] URL&#39;s zijn beschikbaar met activiteiten waarbij Analytics de rapportagebron (A4T) is. De uren die tijdens het uitvoeren van QA worden geproduceerd gebruikend [!UICONTROL Activity QA] stromen aan de zelfde rapportreeks waar de de gegevensstromen van de activiteit zelfs nadat de activiteit levend gaat.
* [!UICONTROL Activity QA] geeft geen inhoud weer voor gearchiveerde activiteiten of activiteiten die hun einddatum hebben bereikt. Als u een beëindigde activiteit deactiveert, moet u de activiteit voor [!UICONTROL Activity QA] opnieuw bewaren om te werken.
* Activiteiten die worden geïmporteerd in [!DNL Target Standard/Premium] (bijvoorbeeld uit [!DNL Target Classic]) ondersteunen geen URL&#39;s met kwaliteitscontrole.
* In [!UICONTROL Auto-Allocate] en [!UICONTROL Recommendations] activiteiten, wordt het model niet beïnvloed door de bezoeken die in [!UICONTROL Activity QA] worden gevangen.
* [!UICONTROL Activity QA] is kleverig. Nadat u in [!UICONTROL Activity QA] door een website hebt gebladerd, moet uw [!DNL Target]-sessie verlopen of moet [!DNL Target] u loslaten uit [!UICONTROL Activity QA] voordat u uw site als een gebruikelijke bezoeker kunt weergeven. Gebruik [Doel QA bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) om uzelf uit [!UICONTROL Activity QA] te dwingen.

   U kunt uzelf ook handmatig afdwingen door een pagina op uw site te laden met de parameter `at_preview_token` met een lege waarde (bijvoorbeeld `https://www.mysite.com/?at_preview_token=`).

* Als u &quot;URL is&quot;terwijl het creëren van de activiteit [verfijningen in op vorm-gebaseerde Composer](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) of [paginaleveringsopties in Composer van de Visuele Ervaring)](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81) specificeerde, werkt QA URL niet omdat [!UICONTROL Activity QA] parameters URL toevoegt. Als u dit probleem wilt verhelpen, klikt u op de URL voor de kwaliteitscontrole om naar uw site te gaan, verwijdert u de toegevoegde parameters uit de URL en laadt u vervolgens de nieuwe URL.
* Als u at.js 1 hebt.*x*,  [!UICONTROL Activity QA] mode is niet kleverig als u Safari of een andere browser gebruikt die cookies van derden blokkeert. In deze gevallen moet u de voorvertoningsparameters toevoegen aan elke URL waarnaar u navigeert. Het zelfde is waar als u [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) hebt uitgevoerd.
* Als een activiteit veelvoudige ervaringspubliek gebruikt (bijvoorbeeld, een plaats van de V.S. en van het VK die in de zelfde activiteit inbegrepen zijn), worden de verbindingen van QA niet geproduceerd voor de vier combinaties (Ervaring A/US Plaats, Ervaring A/UK Plaats, Ervaring B/US Plaats, Ervaring B/UK Plaats). Er worden slechts twee QA-koppelingen (Experience A en Experience B) gemaakt en gebruikers moeten in aanmerking komen voor het juiste publiek om de pagina te kunnen zien. Een Britse QA-persoon kan de Amerikaanse site niet zien.
* Alle `at_preview` parameters en waarden zijn reeds gecodeerd URL. Meestal werkt alles zoals verwacht. Nochtans, moeten sommige klanten balancers of de servers van het Web laden die proberen om de parameters van het vraagkoord opnieuw te coderen.

   Vanwege deze dubbele codering kan [!DNL Target] de juiste tokenwaarde niet extraheren wanneer [!DNL Target] de `at_preview_token` probeert te decoderen, waardoor de voorvertoning niet werkt.

   Adobe raadt u aan contact op te nemen met uw IT-team om ervoor te zorgen dat alle voorvertoningsparameters worden gevoegd op lijst van gewenste personen, zodat deze waarden op geen enkele manier worden getransformeerd.

   De volgende lijst maakt een lijst van de parameters die in uw domein kunnen worden gevoegd op lijst van gewenste personen:

   | Parameter | Type | Waarde | Beschrijving |
   |--- |--- |--- |--- |
   | `at_preview_token` | Versleutelde tekenreeks | Verplicht; geen standaardwaarde | Een gecodeerde entiteit die de lijst van campagnes IDs bevat die op wijze kunnen worden uitgevoerd QA. |
   | `at_preview_index` | String | Leeg | De indeling van de parameter is `<campaignIndex>` of `<campaignIndex>_< experienceIndex>`<br>Beide indexen beginnen met 1. |
   | `at_preview_listed_activities_only` | Boolean (true/false) | Standaardwaarde: false | Indien &quot;true&quot;, worden alle campagnes die zijn opgegeven in de parameters `at_preview_index` verwerkt.<br>Als &quot;false&quot;, worden alle campagnes van de pagina verwerkt, zelfs als deze niet zijn opgegeven in de voorbeeldtoken. |
   | `at_preview_evaluate_as_true_audience_ids` | String | Leeg | Onderstrepingsteken-gescheiden (&quot;_&quot;) lijst van segmentId-s die (bij het richten en het melden van niveau) altijd als &quot;waar&quot;in het werkingsgebied van [!DNL Target] verzoek zou moeten worden beoordeeld. |
   | `_AT_Debug` | String | Venster of console | Logboekregistratie voor console of nieuw venster. |
   | `adobe_mc_ref` |  |  | Geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Als `AppMeasurement.js` versie 2.1 (of hoger) wordt gebruikt, gebruikt [!DNL Adobe Analytics] deze parameterwaarde als verwijzende URL op de nieuwe pagina. |
   | `adobe_mc_sdid` |  |  | Geeft de [!DNL Supplemental Data Id] (SDID) en [!DNL Experience Cloud Org Id] van de standaardpagina door aan de nieuwe pagina. Als u deze id&#39;s doorgeeft, kan [!UICONTROL Analytics for Target] (A4T) het [!DNL Target]-verzoek op de standaardpagina samenvoegen met het [!DNL Analytics]-verzoek op de nieuwe pagina. |

* De interface [!UICONTROL Target QA Mode] toont slechts eerste URL van een ervaring in een multi-paginaactiviteit. De veronderstelling is dat u een reistest creeert en u zich van URL1 aan URL2 beweegt. Als u echter onafhankelijk naar URL2 wilt gaan, kopieert u alle URL-parameters die via URL1 zijn opgegeven en past u deze toe op URL2 nadat u een &#39;?&#39; hebt geplaatst net als in URL1.

## Doelcompatibiliteit met JavaScript-bibliotheek [!UICONTROL QA Mode]

[!DNL Target] ondersteunt de volgende JavaScript-bibliotheken:

* [at.js 1.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)
* [at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)
* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)

In de volgende tabel worden de verschillende typen activiteiten vermeld en wordt aangegeven of de modus [!UICONTROL Activity QA] voor elke bibliotheek wordt ondersteund:

| Type activiteit | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B Test] | Ja | Ja | Ja |
| [!UICONTROL Auto-Allocate] | Ja | Ja | Ja |
| [!UICONTROL Auto-Target] | Nee | Nee | Nee |
| [!UICONTROL Automated Personalization] (AP) | Nee | Nee | Nee |
| [!UICONTROL Experience Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Test] (MVT) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |

## Voorvertoning van URL&#39;s {#preview}

De voorproef URLs van de ervaring kan voor alle [!DNL Target] activiteitentypes worden geproduceerd. Met voorbeeld-URL&#39;s kunt u inhoud direct op uw site bekijken voordat de activiteit live is voor voorvertoning en kwaliteitscontrole. Ervaar de voorvertoning van URL&#39;s en omzeilt het opgeven van doelen om een bepaalde ervaring geforceerd weer te geven.

Zie [Automated Personalization-activiteiten voorvertonen met URL&#39;s voor voorvertoningen[!UICONTROL Automated Personalization] (AP)-activiteiten.](/help/c-activities/t-automated-personalization/experience-preview.md)

Als u een voorbeeld-URL vanaf de pagina **[!UICONTROL Overview]** van een activiteit wilt openen en delen, klikt u op de koppeling **[!UICONTROL Activity QA]**.

>[!NOTE]
>
>De koppeling [!UICONTROL Activity QA] en de voorbeeld-URL zijn hetzelfde voor alle andere activiteiten dan AP-activiteiten [!DNL Target].

In de volgende tabel worden de verschillende typen activiteiten vermeld en wordt aangegeven of de functie URL&#39;s voorvertonen wordt ondersteund voor elke bibliotheek of API:

| Type activiteit | at.js 1.x | at.js 2.x | Platform Web SDK | Leverings-API | Admin-API |
| --- | --- | --- | --- | --- | --- |
| [!UICONTROL A/B Test] | Ja | Ja | Ja | Niet van toepassing | Ja |
| [!UICONTROL Auto-Allocate] | Ja | Ja | Ja | Niet van toepassing | Ja |
| [!UICONTROL Auto-Target] | Ja | Ja | Ja | Niet van toepassing | Ja |
| [!UICONTROL Automated Personalization] (AP) | Ja | Ja | Nee | Niet van toepassing | Ja |
| [!UICONTROL Experience Targeting] (XT) | Ja | Ja | Ja | Niet van toepassing | Ja |
| [!UICONTROL Multivariate Test] (MVT) | Ja | Ja | Ja | Niet van toepassing | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja | Niet van toepassing | Ja |






