---
keywords: qa;qa, modus; activiteit qa;qa url;qa urls;voorvertoning url;voorvertoning urls
description: Leer hoe u Adobe gebruikt [!DNL Target] QA URLs om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.
title: Hoe kan ik QA-activiteiten uitvoeren?
feature: Activities
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
source-git-commit: 87cfc86bdabeb87424d2cf9fff7754dd85f7ac0b
workflow-type: tm+mt
source-wordcount: '1690'
ht-degree: 0%

---

# Activiteit QA

QA-URL&#39;s gebruiken in [!DNL Adobe Target] om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek het richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.

[!UICONTROL Activity QA] laat u volledig testen [!DNL Target] activiteiten voordat ze worden gelanceerd. De [!UICONTROL Activity QA] functionaliteit omvat:

* Verbindingen om met teamleden te delen die nooit veranderen of regeneratie vereisen, ongeacht updates die aan de ervaringen of de activiteiten worden aangebracht. Met deze functie kunt u uw activiteiten volledig testen tijdens de hele gebruikersreis.
* De voorwaarden van het publiek naar keuze gerespecteerd zodat kunnen de marketers het richten van criteria testen of het richten van criteria aan QA de verschijning van ervaringen negeren zonder het moeten aan de publieksvoorwaarden voldoen.
* QA-rapportage wordt vastgelegd zodat marketers kunnen bevestigen dat de metriek naar verwachting toeneemt en dat de QA-rapportgegevens gescheiden worden gehouden van productierapportage (voor niet-A4T-rapportage).
* De mogelijkheid om een ervaring afzonderlijk of met andere live activiteiten die aan de leveringscriteria voldoen, voor te vertonen (pagina/[!DNL Target] verzoek/publiek).
* De mogelijkheid om een kwaliteitscontrole uit te voeren voor de hele gebruikersreis. U hebt eenmalig toegang tot uw site met de koppeling voor kwaliteitscontrole en bladert vervolgens door de gehele site in Activiteit QA. U blijft in Activiteit QA tot u de zitting beëindigt of tot u gebruikt [QA-doelbladwijzer](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) om uzelf te dwingen [!UICONTROL Activity QA]. Deze functie is handig als u een activiteit hebt die meerdere webpagina&#39;s beslaat.

  >[!NOTE]
  >
  >Deze functionaliteit geldt voor at.js-implementaties met versie 2.*x* of hoger. Voor om.js 1.*x* implementaties, is deze functionaliteit alleen waar als de browser van de bezoeker cookies van derden niet blokkeert.

## Een URL voor een kwaliteitscontrole openen en delen {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Van een activiteit [!UICONTROL Overview] pagina, klikt u **[!UICONTROL Activity QA]**.

   ![QA-koppeling voor activiteit](assets/qa_link.png)

1. Configureer de volgende instellingen:

   ![Opties voor QA-koppeling](assets/qa_link_config.png)

   * **[!UICONTROL Match audience rules to see experiences]:** Soms wilt u bevestigen dat uw publiek het aanpassen werkt. Andere tijden wilt u de blik en het gevoel van de activiteit controleren. Als deze instelling wordt overgeschakeld naar de &quot;aan&quot;-positie, moeten de testers voldoen aan de vereisten voor doelwitten om in aanmerking te komen voor het bekijken van de ervaringen. Voor Experience Targeting (XT)-activiteiten wordt één activiteit-URL opgegeven. De ervaring die u ziet, wordt bepaald door u die in aanmerking komt voor een van de doelregels.

     Als u deze instelling in- of uitschakelt, kunt u door op de koppelingen te klikken de ervaringen weergeven, ongeacht of u hiervoor in aanmerking komt of niet. Wanneer het uitvoeren van QA, kunt u afwisselend tussen vereisen of niet vereisen dat het publiek richt wordt gerespecteerd.

   * **Standaardinhoud weergeven voor alle andere activiteiten:** Als deze optie wordt geschakeld naar de positie &quot;Aan&quot;, wordt de standaardinhoud weergegeven voor alle andere activiteiten. De voorvertoning wordt bijvoorbeeld afzonderlijk weergegeven zonder rekening te houden met alle andere live activiteiten op dezelfde pagina/[!DNL Target] verzoek.

     Als deze instelling wordt uitgeschakeld, kunt u het volgende overwegen:

      * Als er botsingen zijn tussen de activiteit u test en andere levende activiteiten; [normale prioriteitsregels](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) van toepassing. Wegens botsingen, is het mogelijk u niet de activiteit kunt zien die u aan QA van plan bent.
      * De toename van metriek voor de bekeken activiteiten, maar slechts in het QA rapporterend milieu.

1. Klikken **[!UICONTROL Done]** om uw wijzigingen op te slaan.
1. Deel de activiteiten link URLs met leden van uw organisatie voor het testen.

   Activiteitenkoppelingen verlopen nooit en u hoeft de koppelingen niet opnieuw te verzenden als iemand een activiteit of ervaring wijzigt. Als u echter een ander publiek toepast dan de opdracht [!UICONTROL Audience Library]In plaats van alleen maar de activiteit te bewerken, wordt er een nieuwe koppeling gegenereerd die u opnieuw moet delen.

   Met elke URL voor de activiteitenkoppeling (voor Experience A, Experience B enzovoort) kunt u de gebruikersreis starten vanuit de bijbehorende ervaring. Klik op de URL die voor een ervaring is gegenereerd en ga verder met het bladeren door de normale site om ervaringen op meerdere pagina&#39;s te zien (als er meerdere pagina&#39;s zijn). Er wordt slechts één URL gegenereerd per ervaring, zelfs als de ervaring meerdere pagina&#39;s beslaat (sjabloontesten of meerdere pagina&#39;s testen).

   U kunt op de site navigeren om de andere pagina&#39;s te zien, omdat de [!UICONTROL Activity QA] de modus blijft ongewijzigd. Deze situatie geldt voor at.js-implementaties met versie 2.*x* of hoger. Voor om.js 1.*x* implementaties, is deze situatie alleen waar als de browser van de bezoeker cookies van derden niet blokkeert.

1. Als u rapporten wilt zien die zijn gegenereerd via de URL&#39;s van de activiteitenkoppeling, klikt u op de activiteit **[!UICONTROL Reports]** pagina, klikt u op de **[!UICONTROL Settings]** icon (  ![icon_tandbeeld](assets/icon_gear.png) ), selecteert u vervolgens **[!UICONTROL QA Mode Traffic]** van de **[!UICONTROL Environment]** vervolgkeuzelijst.

## Het vrijgeven van zich van wijze QA

[!UICONTROL Activity QA] is kleverig. Nadat u in een website bladert [!UICONTROL Activity QA], uw [!DNL Target] sessie moet verlopen of u moet [!DNL Target] vrijgeven van [!UICONTROL Activity QA] voordat u uw site als een gebruikelijke bezoeker kunt weergeven.

* **te.js 2.*x***: Als uw site at.js 2 heeft.*x* geïmplementeerd, gebruik de [Doel QA-bladwijzer](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) om uzelf te dwingen [!UICONTROL Activity QA]. Als u een pagina op uw site laadt met een lege waarde, zoals wordt beschreven in het volgende opsommingsteken, wordt *niet* Verwijder het cookie QA uit de browser wanneer at.js 2.*x* wordt geïmplementeerd.

* **te.js 1.*x***: Als uw site at.js 1 heeft.*x* geïmplementeerd, naast het gebruik van [Doel QA-bladwijzer](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879), kunt u uzelf ook handmatig afdwingen door een pagina op uw site te laden met de `at_preview_token` parameter met een lege waarde. Bijvoorbeeld:

  `https://www.mysite.com/?at_preview_token=`

* **[!DNL Adobe Experience Platform Web SDK]**: Als uw site de [[!UICONTROL Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} geïmplementeerd, kunt u zichzelf handmatig afdwingen door een pagina op uw site te laden met de `at_qa_mode` parameter met een lege waarde. Bijvoorbeeld:

  `https://www.mysite.com/?at_qa_mode=`

## Overwegingen {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* Omdat Activiteit QA nu beschikbaar voor allen is [!DNL Target] Type activiteit, de &quot;VoorproefAutomated Personalization activiteiten met ervaring voorproefURLs&quot;eigenschap is niet meer noodzakelijk.
* [!UICONTROL Activity QA] het voorbeeld van koppelingen voor opgeslagen activiteiten wordt mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Het opnieuw proberen van de voorproefverbindingen zou moeten werken. Om te voorkomen dat deze situatie zich blijft voordoen, archiveert u opgeslagen activiteiten die niet meer actief worden gebruikt.
* [!UICONTROL Activity QA] URL&#39;s zijn beschikbaar bij activiteiten met [Analyses als bron van rapportage](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Hits die tijdens het uitvoeren van QA worden geproduceerd gebruikend [!UICONTROL Activity QA] stroom aan de zelfde rapportreeks waar de de gegevensstromen van de activiteit zelfs nadat de activiteit levend gaat.
* [!UICONTROL Activity QA] geeft geen inhoud weer voor gearchiveerde activiteiten of activiteiten die hun einddatum hebben bereikt. Als u een eindactiviteit deactiveert, moet u de activiteit opnieuw opslaan voor [!UICONTROL Activity QA] om te werken.
* Activiteiten geïmporteerd in [!DNL Target Standard/Premium] (van [!DNL Target Classic], bijvoorbeeld) geen QA-URL&#39;s ondersteunen.
* In [!UICONTROL Auto-Allocate] en [!UICONTROL Recommendations] de in [!UICONTROL Activity QA].
* Als u &quot;URL is&quot; hebt opgegeven tijdens het maken van de activiteit [verfijningen in de op formulier gebaseerde Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) of [de opties van de paginalevering in de Visuele Composer van de Ervaring)](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81), werkt de URL voor kwaliteitscontrole niet omdat [!UICONTROL Activity QA] voegt URL-parameters toe. Als u dit probleem wilt verhelpen, klikt u op de URL voor de kwaliteitscontrole om naar uw site te gaan, verwijdert u de toegevoegde parameters uit de URL en laadt u vervolgens de nieuwe URL.
* Als u at.js 1 hebt.*x*, [!UICONTROL Activity QA] Deze modus blijft niet behouden als u Safari gebruikt of een andere browser die cookies van derden blokkeert. In deze gevallen moet u de voorvertoningsparameters toevoegen aan elke URL waarnaar u navigeert. Hetzelfde geldt als u al hebt geïmplementeerd [CNAME](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/implement-cname-support-in-target.html){target=_blank}.
* Als een activiteit veelvoudige ervaringspubliek gebruikt (bijvoorbeeld, een plaats van de V.S. en van het VK die in de zelfde activiteit inbegrepen zijn), worden de verbindingen van QA niet geproduceerd voor de vier combinaties (Ervaring A/US Plaats, Ervaring A/UK Plaats, Ervaring B/US Plaats, Ervaring B/UK Plaats). Er worden slechts twee QA-koppelingen (Experience A en Experience B) gemaakt en gebruikers moeten in aanmerking komen voor het juiste publiek om de pagina te kunnen zien. Een Britse QA-persoon kan de Amerikaanse site niet zien.
* Alles `at_preview` parameters en waarden zijn al gecodeerd met URL. Meestal werkt alles zoals verwacht. Nochtans, moeten sommige klanten balancers of de servers van het Web laden die proberen om de parameters van het vraagkoord opnieuw te coderen.

  Vanwege deze dubbele codering, wanneer [!DNL Target] probeert de `at_preview_token`, [!DNL Target] kan de juiste tokenwaarde niet extraheren, waardoor de voorvertoning niet werkt.

  [!DNL Adobe] U kunt het beste contact opnemen met uw IT-team om ervoor te zorgen dat alle voorvertoningsparameters worden gevoegd op lijst van gewenste personen, zodat deze waarden op geen enkele manier worden getransformeerd.

  De volgende lijst maakt een lijst van de parameters die in uw domein kunnen worden gevoegd op lijst van gewenste personen:

  | Parameter | Type | Waarde | Beschrijving |
  |--- |--- |--- |--- |
  | `at_preview_token` | Versleutelde tekenreeks | Verplicht; geen standaardwaarde | Een gecodeerde entiteit die de lijst van campagnes IDs bevat die op wijze kunnen worden uitgevoerd QA. |
  | `at_preview_index` | String | Leeg | De indeling van de parameter is `<campaignIndex>` of `<campaignIndex>_< experienceIndex>`<br>Beide indexen beginnen met 1. |
  | `at_preview_listed_activities_only` | Boolean (true/false) | Standaardwaarde: false | Indien waar (true), worden alle campagnes opgegeven in het dialoogvenster `at_preview_index` parameters worden verwerkt.<br>Als &quot;false&quot;, worden alle campagnes van de pagina verwerkt, zelfs als deze niet zijn opgegeven in de voorbeeldtoken. |
  | `at_preview_evaluate_as_true_audience_ids` | String | Leeg | Lijst met segmentId&#39;s met onderstrepingsteken als scheidingsteken (&quot;_&quot;) die altijd (op richtings- en rapportageniveau) als &quot;waar&quot; in het bereik van de [!DNL Target] verzoek. |
  | `_AT_Debug` | String | Venster of console | Logboekregistratie voor console of nieuw venster. |
  | `adobe_mc_ref` |  |  | Geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Indien gebruikt met `AppMeasurement.js` versie 2.1 (of hoger), [!DNL Adobe Analytics] gebruikt deze parameterwaarde als verwijzende URL op de nieuwe pagina. |
  | `adobe_mc_sdid` |  |  | Hiermee geeft u de [!DNL Supplemental Data Id] (SDID) en [!DNL Experience Cloud Org Id] van de standaardpagina naar de nieuwe pagina. Het overgaan van deze IDs staat toe [!UICONTROL Analytics for Target] (A4T) om de [!DNL Target] verzoek op de standaardpagina met [!DNL Analytics] op de nieuwe pagina aanvragen. |

* De [!UICONTROL Target QA Mode] In de gebruikersinterface wordt alleen de eerste URL van een ervaring in een activiteit van meerdere pagina&#39;s weergegeven. De veronderstelling is dat u een reistest creeert en u zich van URL1 aan URL2 beweegt. Als u echter onafhankelijk naar URL2 wilt gaan, kopieert u alle URL-parameters die via URL1 zijn opgegeven en past u deze toe op URL2 nadat u een &#39;?&#39; hebt geplaatst net als in URL1.
* De QA-voorbeeldkoppelingen voor activiteit voor opgeslagen activiteiten worden mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Probeer de voorbeeldkoppelingen opnieuw. Opgeslagen activiteiten archiveren die niet meer actief worden gebruikt om te voorkomen dat dit probleem zich blijft voordoen.

## Doel JavaScript-bibliotheek [!UICONTROL QA Mode] compatibiliteit {#compatibility}

[!DNL Target] ondersteunt de volgende JavaScript-bibliotheken:

* [at.js 1.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [at.js 2.x](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html)
* [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html)

In de volgende tabel worden de verschillende typen activiteiten vermeld en wordt aangegeven of [!UICONTROL Activity QA] Deze modus wordt ondersteund voor elke bibliotheek:

| Type activiteit | at.js 1.x | at.js 2.x | Platform Web SDK |
| --- | --- | --- | --- |
| [!UICONTROL A/B Test] | Ja | Ja | Ja |
| [!UICONTROL Auto-Allocate] | Ja | Ja | Ja |
| [!UICONTROL Auto-Target] | Ja | Ja | Ja |
| [!UICONTROL Automated Personalization] (AP) | Ja | Ja | Ja |
| [!UICONTROL Experience Targeting] (XT) | Ja | Ja | Ja |
| [!UICONTROL Multivariate Test] (MVT) | Ja | Ja | Ja |
| [!UICONTROL Recommendations] | Ja | Ja | Ja |

