---
keywords: qa;voorvertoning;voorvertoning koppelingen;adobe target;target
description: Leer hoe te om Adobe [!DNL Target] QA URLs te gebruiken om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.
title: Hoe kan ik QA-activiteiten uitvoeren?
feature: Activiteiten
exl-id: 5c606d61-6d13-4a9b-9a23-4840f1754d3c
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1531'
ht-degree: 0%

---

# Activiteit QA

Gebruik QA URLs in [!DNL Adobe Target] om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.

## Overzicht {#section_11B761A522A14E61978275772210A4C2}

Met Activity QA kunt u uw doelactiviteiten volledig testen voordat u ze live start. De QA-functionaliteit voor activiteit omvat:

* Verbindingen om met teamleden te delen die nooit veranderen of regeneratie vereisen, ongeacht updates die aan de ervaringen of de activiteiten worden aangebracht. Dit laat u uw activiteiten over de volledige gebruikersreis volledig testen.

   Ondersteuning voor voorbeeldkoppelingen voor [!UICONTROL Automated Personalization]-activiteiten is toegevoegd met [at.js 2.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

* De voorwaarden van het publiek naar keuze gerespecteerd zodat kunnen de marketers het richten van criteria testen of het richten van criteria aan QA de verschijning van ervaringen negeren zonder het moeten aan de publieksvoorwaarden voldoen.
* QA-rapportage wordt vastgelegd zodat marketers kunnen bevestigen dat de metriek naar verwachting toeneemt en dat de QA-rapportgegevens gescheiden worden gehouden van productierapportage (voor niet-A4T-rapportage).
* De mogelijkheid om een ervaring op zichzelf of in combinatie met andere live activiteiten die aan de leveringscriteria voldoen (pagina/doelverzoek/publiek) voor te vertonen.
* De mogelijkheid om een kwaliteitscontrole uit te voeren voor de hele gebruikersreis. U hebt eenmalig toegang tot uw site met de koppeling voor kwaliteitscontrole en bladert vervolgens door de gehele site in Activiteit QA. U blijft in Activiteit QA tot u de zitting beëindigt of tot u [QA de referentie van het Doel ](/help/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) gebruikt om zich uit Activiteit QA te dwingen. Deze functie is vooral handig als u een activiteit hebt die meerdere webpagina&#39;s omvat.

   >[!NOTE]
   >
   >Dit geldt voor at.js-implementaties met versie 2.** xor later. Voor om.js 1.*Dit is alleen van* toepassing als de browser van de bezoeker cookies van derden niet blokkeert.

## Toegang tot en het Delen van een URL QA {#section_1C59BAA247B247BDB125D1BE8EAD4547}

1. Klik op de koppeling **[!UICONTROL Activity QA]** van de pagina [!UICONTROL Overview] van een activiteit.

   ![QA-koppeling voor activiteit](assets/qa_link.png)

1. Configureer de volgende instellingen:

   ![Opties voor QA-koppelingsconfiguratie](assets/qa_link_config.png)

   * **Regels van de Publiek aanpassen om Ervaringen te zien:** Soms wilt u bevestigen dat uw publiek het aanpassen werkt. Andere keren wil je gewoon de blik en het gevoel van de activiteit controleren. Als deze instelling wordt overgeschakeld naar de &quot;aan&quot;-positie, moeten de testers voldoen aan de vereisten voor doelwitten om in aanmerking te komen voor het bekijken van de ervaringen. Voor Experience Targeting (XT)-activiteiten wordt één activiteit-URL opgegeven. De ervaring die u ziet, wordt bepaald door u die in aanmerking komt voor een van de doelregels.

      Als u deze instelling in- of uitschakelt, kunt u door op de koppelingen te klikken de ervaringen weergeven, ongeacht of u hiervoor in aanmerking komt of niet. Wanneer het uitvoeren van QA, kunt u afwisselend tussen vereisen of niet vereisen dat het publiek richt wordt gerespecteerd.

   * **Standaardinhoud tonen voor alle andere activiteiten:** Als deze optie wordt ingeschakeld, wordt standaardinhoud weergegeven voor alle andere activiteiten (de voorvertoning wordt bijvoorbeeld afzonderlijk weergegeven zonder rekening te houden met alle andere live activiteiten op dezelfde pagina/[!DNL Target] aanvraag).

      Als deze instelling wordt uitgeschakeld, kunt u het volgende overwegen:

      * Als er botsingen zijn tussen de activiteit u test en andere levende activiteiten, [normale prioritaire regels](/help/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) zijn van toepassing. Hierdoor is het mogelijk dat je de activiteit die je wilt uitvoeren, niet ziet.
      * De toename van metriek voor de bekeken activiteiten, maar slechts in het QA rapporterend milieu.

1. Klik **[!UICONTROL Done]** om uw veranderingen te bewaren.
1. Deel de Activiteitenkoppeling-URL&#39;s met leden van uw organisatie voor testdoeleinden.

   De Verbindingen van de activiteit verlopen nooit en u te hoeven om geen verbindingen opnieuw te verzenden als iemand veranderingen in een activiteit of een ervaring aanbrengt. Nochtans, als u een verschillend publiek van de Bibliotheek van het Publiek toepast, eerder dan eenvoudig het uitgeven van de activiteit, wordt een nieuwe verbinding geproduceerd die u zult moeten opnieuw delen.

   Elke Activity Link-URL (voor bijv. A, Exp B, enz.) Hiermee kunt u de gebruikersreis starten vanuit de bijbehorende ervaring. U kunt op de URL klikken die voor een ervaring is gegenereerd en vervolgens doorgaan met het bladeren door de normale site om ervaringen op meerdere pagina&#39;s te zien (als er meerdere pagina&#39;s zijn). Er wordt slechts één URL gegenereerd per ervaring, zelfs als de ervaring meerdere pagina&#39;s beslaat (sjabloontesten of meerdere pagina&#39;s testen).

   U kunt op de site navigeren om de andere pagina&#39;s weer te geven, omdat Activiteit QA kleverig is. Merk op dat dit voor implementaties at.js met versie 2 waar is.** xor later. Voor om.js 1.*Dit is alleen van* toepassing als de browser van de bezoeker cookies van derden niet blokkeert.

1. Als u rapporten wilt bekijken die zijn gegenereerd via Activity Link URL&#39;s, klikt u op de pagina **[!UICONTROL Reports]** van de activiteit, klikt u op het pictogram **[!UICONTROL Settings]** ( ![](assets/icon_gear.png) ) en selecteert u **[!UICONTROL QA Mode]** in de vervolgkeuzelijst **[!UICONTROL Environment]**.

## Overwegingen {#section_B256EDD7BFEC4A6DA72A8A6ABD196D78}

* De koppeling [!UICONTROL Activity QA] wordt weergegeven op de pagina [!UICONTROL Overview] van alle typen activiteiten, behalve Automated Personalization (AP). U kunt [Koppelingen voorvertonen](/help/c-activities/t-automated-personalization/experience-preview.md#task_586C6655A6FD4AF08F5678FC3F481EFC) voor AP-activiteiten gebruiken.
* De QA-voorbeeldkoppelingen voor activiteit voor opgeslagen activiteiten worden mogelijk niet geladen als uw account te veel opgeslagen activiteiten bevat. Het opnieuw proberen van de voorvertoningskoppelingen zou moeten werken. Als u wilt voorkomen dat dit gebeurt, archiveert u opgeslagen activiteiten die niet meer actief worden gebruikt.
* Activiteit QA URLs is beschikbaar met activiteiten met Analytics als rapporteringsbron (A4T). De geproduceerde Hits terwijl het uitvoeren van QA gebruikend Activiteit QA zal aan de zelfde rapportreeks stromen waar de gegevens van de activiteit zullen stromen zelfs nadat de activiteit live gaat.
* Activiteits-QA geeft geen inhoud weer voor gearchiveerde activiteiten of activiteiten die hun einddatum hebben bereikt. Als u een beëindigde activiteit deactiveert, moet u de activiteit opnieuw bewaren voor Activiteit QA om te werken.
* Activiteiten die worden geïmporteerd in Target Standard/Premium (bijvoorbeeld uit Target Classic) ondersteunen geen URL&#39;s met kwaliteitscontrole.
* In Auto-Toewijzing, auto-Doel, en de activiteiten van Recommendations, zal het model niet door de bezoeken worden beïnvloed die in Activiteit QA worden gevangen.
* Omdat activiteit QA kleverig is, nadat u een website in Activiteit QA doorbladert, moet uw zitting van het Doel verlopen of u moet van Doel hebben u van Activiteit QA alvorens u uw plaats als een typische bezoeker kunt bekijken. Gebruik [Doel QA bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md#concept_A8A3551A4B5342079AFEED5ECF93E879) om uit Activiteit QA te dwingen.

   U kunt uzelf ook handmatig afdwingen door een pagina op uw site te laden met de parameter `at_preview_token` met een lege waarde (bijvoorbeeld `https://www.mysite.com/?at_preview_token=`).

* Als u &quot;URL is&quot;terwijl het creëren van de activiteit [verfijningen in de op vorm-gebaseerde Composer](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) of [pagina leveringsopties in de Visuele Composer van de Ervaring)](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81) specificeerde, zal QA URL niet werken omdat Activiteit QA parameters URL toevoegt. Als u dit probleem wilt verhelpen, klikt u op de URL voor de kwaliteitscontrole om naar uw site te gaan, verwijdert u de toegevoegde parameters uit de URL en laadt u vervolgens de nieuwe URL.
* Als u at.js 1 hebt.*x*, of mbox.js, de wijze van Activiteit QA zal niet kleven als u Safari of een andere browser gebruikt die derdekoekjes blokkeert. In deze gevallen moet u de voorvertoningsparameters toevoegen aan elke URL waarnaar u navigeert. Het zelfde is waar als u [CNAME](/help/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) hebt uitgevoerd.
* Als een activiteit meerdere ervaringssoorten publiek gebruikt (bijvoorbeeld een site in de VS en het Verenigd Koninkrijk die deel uitmaken van dezelfde activiteit), worden er geen QA-koppelingen gegenereerd voor de vier combinaties (Experience A/US Site, Experience A/UK Site, Experience B/US Site, Experience B/US Site, Experience B/UK Site). Er worden slechts twee QA-koppelingen (Experience A en Experience B) gemaakt en gebruikers moeten in aanmerking komen voor het juiste publiek om de pagina te kunnen zien. Een Britse kwaliteitscontrole-persoon kon de Amerikaanse site niet zien.
* Alle `at_preview` parameters en waarden zijn reeds gecodeerd URL. Meestal werkt alles zoals verwacht. nochtans, zouden sommige klanten ladingsbalancers of de servers van het Web kunnen hebben die proberen om de parameters van het vraagkoord opnieuw te coderen.

   Vanwege deze dubbele codering, wanneer we `at_preview_token` proberen te decoderen, kan Target niet de juiste tokenwaarde extraheren, waardoor de voorvertoning niet werkt.

   Wij adviseren dat u met uw team van IT spreekt om ervoor te zorgen dat alle voorproefparameters worden gevoegd op lijst van gewenste personen zodat deze waarden op geen enkele manier worden getransformeerd.

   De volgende lijst maakt een lijst van de parameters die in uw domein kunnen worden gevoegd op lijst van gewenste personen:

   | Parameter | Type | Waarde | Beschrijving |
   |--- |--- |--- |--- |
   | `at_preview_token` | Versleutelde tekenreeks | Verplicht; geen standaardwaarde | Een gecodeerde entiteit die de lijst bevat van campagnes-id&#39;s die mogen worden uitgevoerd in de QA-modus. |
   | `at_preview_index` | String | Leeg | De indeling van de parameter is `<campaignIndex>` of `<campaignIndex>_< experienceIndex>`<br>Beide indexen beginnen met 1. |
   | `at_preview_listed_activities_only` | Boolean (true/false) | Standaardwaarde: false | Indien &quot;true&quot;, worden alle campagnes die zijn opgegeven in de parameters `at_preview_index` verwerkt.<br>Als &quot;false&quot;, worden alle campagnes van de pagina verwerkt, zelfs als deze niet zijn opgegeven in de voorbeeldtoken. |
   | `at_preview_evaluate_as_true_audience_ids` | String | Leeg | Onderstrepingsteken-gescheiden (&quot;_&quot;) lijst van segmentId-s die altijd (bij gericht en rapporteringsniveau) als &quot;waar&quot;in het werkingsgebied van [!DNL Target] verzoek zou moeten worden beoordeeld. |
   | `_AT_Debug` | String | Venster of console | Logboekregistratie voor console of nieuw venster. |
   | `adobe_mc_ref` |  |  | Geeft de verwijzende URL van de standaardpagina door aan de nieuwe pagina. Als `AppMeasurement.js` versie 2.1 (of hoger) wordt gebruikt, gebruikt [!DNL Adobe Analytics] deze parameterwaarde als verwijzende URL op de nieuwe pagina. |
   | `adobe_mc_sdid` |  |  | Geeft de [!DNL Supplemental Data Id] (SDID) en [!DNL Experience Cloud Org Id] van de standaardpagina door aan de nieuwe pagina zodat Analytics for Target (A4T) het verzoek van het Doel op de standaardpagina met het verzoek Analytics op de nieuwe pagina &quot;samenvoegt&quot;. |

* De interface van de Wijze van het Doel QA toont enkel eerste URL van een ervaring in een multi-paginaactiviteit. De veronderstelling is dat u een reistest creeert en u zich van URL1 aan URL2 zult bewegen. Als u echter onafhankelijk naar URL2 wilt gaan, kopieert u alle URL-parameters die via URL1 zijn opgegeven en past u deze toe op URL2 nadat u een &#39;?&#39; hebt geplaatst net als in URL1.
