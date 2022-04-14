---
keywords: visuele ervaring composer-opties;beleving composer-opties;ervaringsopties;geef tekst uit;bewerk tekst/html;bewerk achtergrondkleur;voeg element in;bewerk de koppeling;link;visuele ervaring composer-koppeling;bewerk css-klasse;css-klasse;wisselaanbod;bied;afbeeldingswisseling;verwijder item;item verwijderen;item verbergen;element verplaatsen;element verplaatsen;element vergroten;element wijzigen; element wijzigen;element;selectie uitbreiden;navigeren naar deze koppeling;navigeren naar koppeling;koppeling navigeren;navigeren;koppeling;ongedaan maken;opnieuw uitvoeren;ongedaan maken/opnieuw uitvoeren;aangepaste gebeurtenissen;webcomponenten;aanbieden, beslissing;offer decisioning
description: Ontdek de opties in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).
title: Hoe gebruik ik de [!UICONTROL Visual Experience Composer] (VEC) Opties?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: 20db97843e2b60f3186d46f7b70d2b2bc35acaf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opties voor Visual Experience Composer

Wanneer u op een pagina-element klikt in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC), toont een menu de opties die voor dat elementtype beschikbaar zijn. Bovendien wordt onder aan de pagina een DOM-pad weergegeven waarmee u gemakkelijk door de paginastructuur kunt navigeren.

De verschillende [!UICONTROL Visual Experience Composer] (VEC) Acties worden gegroepeerd in de juiste menuopties om uw taak sneller en efficiënter te maken:

![Menu VEC-opties](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Welke opties beschikbaar zijn, is afhankelijk van het type activiteit dat u maakt of bewerkt.

## [!UICONTROL Edit]

De volgende opties zijn beschikbaar:

### [!UICONTROL Text/HTML] {#edit-text-html}

Wijzig de HTML-code voor het element, zoals de tekst voor een tekstgebied, knop of koppeling.

Naast HTML-code kunt u aangepaste JavaScript bewerken en injecteren.

Er zijn verschillende opties voor tekstopmaak beschikbaar wanneer u tekst en HTML bewerkt voor [!UICONTROL A/B] en [!UICONTROL Experience Targeting] activiteiten. U kunt een lettertype kiezen, een lettertypestijl selecteren, de tekstuitlijning wijzigen en andere standaardopties voor tekstopmaak opgeven. Wanneer u HTML wijzigt, kunt u schakelen tussen de codeweergave en de rijke bewerkingsweergave van de HTML.

De volgende HTML5-tags kunnen worden genest:

| Tag | Geneste tags toegestaan |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

### [!UICONTROL Background Color]

Gebruik de kleurkiezer om een achtergrondkleur te selecteren of te configureren. U kunt een kleurstaal selecteren en dit aanpassen met RGB-waarden of kleurhexcodes. De rode x in de kleurkiezer maakt de achtergrond transparant.

**Opmerking:** Deze optie is niet beschikbaar voor een element waarbij een achtergrondafbeelding is ingesteld.

### [!UICONTROL Styles] {#styles}

Gebruik de [!UICONTROL Styles] om de waarde van bestaande stijlen voor het geselecteerde element weer te geven of te bewerken. U kunt ook extra stijlen toevoegen.

Om toegang te krijgen tot [!UICONTROL Styles] klikt u in het deelvenster VEC op een pagina-element en vervolgens klikt u op **[!UICONTROL Edit]** > **[!UICONTROL Styles]**.

De [!UICONTROL Styles] aan de rechterkant van de VEC. Het deelvenster bevat een lijst met stijlen waarmee u het geselecteerde element kunt bewerken of uitbreiden. Met een real-time CSS-editor kunt u wijzigingen weergeven en stijlen toevoegen als u dit comfortabel vindt met CSS (Cascading Style Sheets) of als u code van uw ontwikkelaar ontvangt.

![Deelvenster Stijlen](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Als u verschillende stijlen toepast, kunt u de wijzigingen altijd herstellen door op de knop [!UICONTROL Revert] pictogram dat in de rechterbovenhoek van [!UICONTROL Styles] nadat u een sectie hebt gewijzigd. Klik op de knop [!UICONTROL Revert] worden alle wijzigingen in het deelvenster van de huidige sectie hersteld.

Breid elke sectie uit om stijlen te bewerken of toe te voegen, zoals hieronder wordt uitgelegd. Als u de wijzigingen wilt opslaan, klikt u op de knop [!UICONTROL Back] om terug te keren naar de hoofdweergave van het deelvenster en vervolgens op **[!UICONTROL Save]**.

Blauwe stippen in het hoofddeelvenster en naast elke optie in de verschillende sectiedeelvensters geven aan dat u de bijbehorende stijlen hebt gewijzigd. Met deze visuele indicator kunt u gemakkelijk uw wijzigingen bekijken voordat u op [!UICONTROL Save].

>[!NOTE]
>
>Snelle acties voor lay-outveranderingen, achtergrondkleur, resizing, en beweging zijn ook beschikbaar als afzonderlijke acties in het menu VEC. Deze opties kunnen als afzonderlijke acties worden gebruikt of u kunt het menu van Stijlen gebruiken, zoals hier wordt uitgelegd.

* **[!UICONTROL Background]**

   Wijzig de achtergrondkleur en -afbeelding.

   * Kleur (geef de kleurcode op of gebruik de kleurkiezer)
   * Afbeelding (selecteer een afbeelding in de afbeeldingskiezer)
   * Afbeeldingsbron (een externe URL opgeven)
   * Bijlage
      * Klik op de bovenste vervolgkeuzelijst om de gewenste scroll, fixed of local te selecteren
      * Klik op de onderste vervolgkeuzelijst om Herhalen, Herhalen-x, Herhalen-y, Geen herhaling, Ruimte of Rond te selecteren
   * Clip
      * Klik op de bovenste vervolgkeuzelijst om een randvak, opvulvak, inhoudsvak of tekst te selecteren
      * Klik op de onderste vervolgkeuzelijst om automatische audio of audio te selecteren

* **[!UICONTROL Typography]**

   De typografie van een element wijzigen. Typografische bewerkingen zijn snel en gemakkelijk.

   Hoewel de rijke tekstredacteur (geef Tekst/HTML uit) voor het verfijnen beschikbaar is, zijn de snelle acties om het volledige element te veranderen beschikbaar via deze optie. Als u wijzigingen in de typografie wilt toepassen op slechts een deel van de tekst (en niet op de volledige tekst), gebruikt u de optie [rijke teksteditor](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   U kunt de volgende typografiestijlen bewerken:

   * [!UICONTROL Font size]
   * [!UICONTROL Font weight]
   * [!UICONTROL Font style]
   * [!UICONTROL Color] (geef de kleurcode op of gebruik de kleurkiezer)
   * [!UICONTROL Word spacing]
   * [!UICONTROL Line height]
   * [!UICONTROL Text alignment]

* **[!UICONTROL Margin]**

   Wijzig de marge voor het geselecteerde element. U kunt de linker-, rechter-, onder- en bovenmarge wijzigen.

   Klik op het vervolgkeuzepictogram voor elke marge om een van de volgende opties te kiezen:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (Sleep de schuifregelaar om de marge in te stellen of het aantal pixels voor elke marge op te geven)

   Marge ondersteunt positieve en negatieve waarden.

   Het doel ondersteunt ook andere grootteeenheden, zoals rem, pc en em. Zie voor meer informatie over deze eenheden [CSS-tips en trucs voor webstijlpagina&#39;s](https://www.w3.org/Style/Examples/007/units.en.html).

* **[!UICONTROL Padding]**

   Wijzig de opvulling voor het geselecteerde element. U kunt de opvulling links, rechts, onder en boven wijzigen.

   Sleep de schuifregelaar om de opvulling in te stellen of geef het aantal pixels voor de opvulling op.

   Opvulling ondersteunt de breedte vanaf 0.

   Ook ondersteuning voor target [andere maateenheden](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em.

* **[!UICONTROL Border]**

   Klik op de randpictogrammen boven in het deelvenster om de rand van het geselecteerde element te wijzigen.

   U kunt de volgende stijlen voor elke rand (boven, rechts, onder en links) bewerken:

   * [!UICONTROL Border style] (geen, verborgen, gestippeld, onderbroken, effen of dubbel)
   * [!UICONTROL Border color] (geef de kleurcode op of gebruik de kleurkiezer)
   * [!UICONTROL Border width] (Sleep de schuifregelaar om een randbreedte te selecteren of geef de breedte op in pixels)

   Rand ondersteunt breedteschalen vanaf 0.

   Ook ondersteuning voor target [andere maateenheden](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em.

* **[!UICONTROL Position]**

   Verplaats het geselecteerde element vanaf de huidige positie. U kunt de boven-, onder-, links-, rechts- en [Z-index](https://www.w3schools.com/cssref/pr_pos_z-index.asp) positie.

   Klik op de knop [!UICONTROL Static] een vervolgkeuzelijst die u kunt kiezen uit de volgende plaatsingsopties:

   * [!UICONTROL Static]
   * [!UICONTROL Relative]
   * [!UICONTROL Absolute]
   * [!UICONTROL Sticky]
   * [!UICONTROL Fixed]

   Klik op het vervolgkeuzepictogram voor elke positie om een van de volgende opties te kiezen:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (Sleep de schuifregelaar om het element te plaatsen of geef het aantal pixels op dat u het element wilt verplaatsen)

   De positie ondersteunt positieve en negatieve waarden.

   Ook ondersteuning voor target [andere maateenheden](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em.

* **[!UICONTROL Size]**

   Wijzig de breedte en hoogte van het geselecteerde element.

   Klik op het vervolgkeuzepictogram naast [!UICONTROL Width] en [!UICONTROL Height] kiezen uit de volgende opties:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (sleep de schuifregelaar om het formaat van het element te wijzigen of om het aantal pixels voor elke dimensie op te geven)

* **[!UICONTROL Filter]**

   Sleep de schuifregelaar voor elke filteroptie of geef het gewenste percentage op:

   * [!UICONTROL Sepia]
   * [!UICONTROL Contrast]
   * [!UICONTROL Brightness]
   * [!UICONTROL GrayScale]
   * [!UICONTROL Blur]
   * [!UICONTROL Opacity]
   * [!UICONTROL Invert]
*
[!UICONTROL  Hue-rotate]
   * [!UICONTROL Saturate]

* **[!UICONTROL CSS Editor]**

   Met de CSS-editor in real-time kunt u wijzigingen bekijken en stijlen toevoegen als u het prettig vindt Cascading Style Sheets (CSS) te gebruiken of als u code van uw ontwikkelaar ontvangt.

   In de CSS-editor worden alle wijzigingen weergegeven die u aanbrengt in het deelvenster Stijlen. Zoals in de onderstaande afbeelding wordt getoond, zijn de tekengrootte, de bovenrand en de afbeeldingsgrootte gewijzigd:

   ![CSS-editor met wijzigingen](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Let op de blauwe stippen naast de [!UICONTROL Typography], [!UICONTROL Border], en [!UICONTROL Size] opties in de vorige illustratie. Deze punten geven aan dat u deze secties hebt gewijzigd. Als u deze sectievensters opent, worden blauwe stippen weergegeven naast de specifieke opties die u hebt gewijzigd.

   U kunt uw eigen code typen als de gewenste stijl niet standaard beschikbaar is in het dialoogvenster [!UICONTROL Styles].

   In de CSS-editor worden alleen details voor de huidige sessie weergegeven. Als u de wijzigingen opslaat en de editor vervolgens opnieuw opent, worden de gegevens over de vorige wijziging niet weergegeven in de editor, zelfs niet als u hetzelfde element opnieuw selecteert.

   >[!IMPORTANT]
   >
   >U kunt een achtergrondafbeelding toepassen met de CSS-editor, maar dit kan flikkering veroorzaken. Test uw wijzigingen vóór de implementatie.

### [!UICONTROL CSS Class]

Geef de vooraf gedefinieerde CSS-klasse op die voor het element wordt gebruikt. Als er meer dan één element is geselecteerd, scheidt u meerdere CSS-klassen met een spatie.

Beschikbaar voor [!UICONTROL A/B], [!UICONTROL Automated Personalization], en [!UICONTROL Multivariate Test] activiteiten.

### [!UICONTROL Link]

Wijzig de URL in de koppeling.

Gebruik Koppeling bewerken om de kiezer bij te werken zodat deze naar hetzelfde afbeeldingselement wijst. Koppelingen naar een ander afbeeldingselement worden echter niet ondersteund. Als u een koppeling wilt maken naar een ander afbeeldingselement, verwijdert u de oorspronkelijke handeling uit de code-editor en gebruikt u de opdracht [!UICONTROL Visual Experience Composer] om de handeling toe te passen op het andere afbeeldingselement.

## [!UICONTROL Insert Before]

De volgende opties zijn beschikbaar:

### [!UICONTROL Offer Decision]

Een [voorstel gemaakt in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} om uw klanten met offer decisioning de beste aanbieding en ervaring te bieden.

**Opmerking:** Deze optie is beschikbaar bij het bewerken of maken van [handmatig [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten.

Zie voor meer informatie [Besluiten over aanbiedingen gebruiken](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], en [!UICONTROL Text]

Voeg om het even welk soort element aan uw pagina naast het wijzigen van bestaande inhoud toe. Voeg tekst, code, lijsten en meer toe om geheel verschillende ervaringen te maken die u wilt testen.

Selecteer een element op de pagina en klik op [!UICONTROL Insert Before] en kiest u of u een afbeelding, HTML of tekst wilt invoegen. Het ingevoegde element wordt vóór het geselecteerde element weergegeven.

Het gedrag van het ingevoegde element is afhankelijk van de structuur van de pagina, uw CSS en andere opties voor paginaconfiguratie. Geldige HTML is vereist om de pagina correct weer te geven. Test de pagina altijd nadat u een item hebt ingevoegd om er zeker van te zijn dat het er naar behoren uitziet.

[!UICONTROL Recommendations] supports [!UICONTROL Insert Before] de inhoud van DIV-, SECTION- en ARTIKEL-tags.

**Opmerking:** Als u een afbeelding invoegt, moet u [!DNL Adobe Scene7 Publishing System] is ingeschakeld, zodat u toegang hebt tot de afbeeldingsbibliotheek.

### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Ervaringsfragmenten invoegen die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten ter bevordering van optimalisatie of personalisatie. Zie voor meer informatie [Fragmenten voor AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Insert After]

De volgende opties zijn beschikbaar:

### [!UICONTROL Offer Decision]

Een [voorstel gemaakt in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} om uw klanten met offer decisioning de beste aanbieding en ervaring te bieden.

**Opmerking:** Deze optie is beschikbaar bij het bewerken of maken van [handmatig [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten.

Zie voor meer informatie [Besluiten over aanbiedingen gebruiken](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image], [!UICONTROL HTML], en [!UICONTROL Text]

Voeg om het even welk soort element aan uw pagina naast het wijzigen van bestaande inhoud toe. Voeg tekst, code, lijsten en meer toe om geheel verschillende ervaringen te maken die u wilt testen.

Selecteer een element op de pagina en klik op [!UICONTROL Insert After] en kiest u of u een afbeelding, HTML of tekst wilt invoegen. Het ingevoegde element verschijnt na het geselecteerde element.

Het gedrag van het ingevoegde element is afhankelijk van de structuur van de pagina, uw CSS en andere opties voor paginaconfiguratie. Geldige HTML is vereist om de pagina correct weer te geven. Test de pagina altijd nadat u een item hebt ingevoegd om er zeker van te zijn dat het er naar behoren uitziet.

[!UICONTROL Recommendations] supports [!UICONTROL Insert After] de inhoud van DIV-, SECTION- en ARTIKEL-tags.

**Opmerking:** Als u een afbeelding invoegt, moet u [!DNL Adobe Scene7 Publishing System] is ingeschakeld, zodat u toegang hebt tot de afbeeldingsbibliotheek.

### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Ervaringsfragmenten invoegen die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten ter bevordering van optimalisatie of personalisatie. Zie voor meer informatie [Fragmenten voor AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Replace Content]

De volgende opties zijn beschikbaar:

### [!UICONTROL Offer Decision]

Een [voorstel gemaakt in [!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html){target=_blank} om uw klanten met offer decisioning de beste aanbieding en ervaring te bieden.

**Opmerking:** Deze optie is beschikbaar bij het bewerken of maken van [handmatig [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten.

Zie voor meer informatie [Besluiten over aanbiedingen gebruiken](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image]

Selecteer een andere afbeelding in de inhoudsbibliotheek. Tot de afbeeldingen die u kunt wisselen, behoren de afbeeldingen die naar de map Experience Cloud Assets zijn geüpload of die in de inhoudsbibliotheek in Doel zijn geüpload.

Tijdens het maken van de eerste activiteit is de weergegeven URL niet de URL die voor levering wordt gebruikt. Bij het synchroniseren van activiteiten wordt die URL bijgewerkt naar een productie-Scene7-URL.

De eerste URL kan er bijvoorbeeld als volgt uitzien:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Na het synchroniseren van activiteiten, zou de levering URL als het volgende voorbeeld kunnen kijken:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations biedt ondersteuning voor Vervangen door in DIV-, SECTION- en ARTIKEL-tags.

**Opmerking:** Voor het wisselen van afbeeldingen is een Adobe Scene7 Publishing System-account vereist.

### [!UICONTROL HTML Offer]

Selecteer een ander voorstel van de [!UICONTROL Content Library].

**Opmerking:** HTML-aanbiedingen worden opgeslagen op [!DNL Target] servers.

Een HTML-aanbieding kan maximaal 256 kB bedragen.

### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Ervaringsfragmenten invoegen die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten ter bevordering van optimalisatie of personalisatie. Zie voor meer informatie [Fragmenten voor AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

## [!UICONTROL Layout]

De volgende opties zijn beschikbaar:

### [!UICONTROL Rearrange]

Sleep het element naar een andere locatie binnen hetzelfde bovenliggende element of DIV. Andere elementen verschuiven de locatie om ruimte te maken voor het opnieuw gerangschikte element.

**Opmerking**: Klikken en bijhouden werkt niet bij opnieuw gerangschikte items.

Momenteel, bepaalde acties VEC, zoals [!UICONTROL Rearrange] en [!UICONTROL Move], veronderstellen dat de elementen van de bron en bestemmingsouder elementen volledig worden geladen. Als lazy het laden onder de ouderelementen DOM (bron of bestemming) voorkomt, kunnen deze acties VEC inconsistent gedrag veroorzaken. We werken aan een betrouwbaardere benadering om VEC-acties te laten werken in lui geladen DOM-elementen. Als tijdelijke oplossing kunt u [!UICONTROL Custom Code] in deze scenario&#39;s om uw ervaringen terug te geven.

### [!UICONTROL Resize]

Wijzig de grootte van een element op de pagina. Wanneer u [!UICONTROL Resize], wordt een handgreep weergegeven in de rechterbenedenhoek van het element waarmee u die hoek kunt slepen om het formaat te wijzigen. Houd Shift ingedrukt als u dezelfde hoogte-breedteverhouding wilt behouden.

**Opmerking:** Inline-elementen kunnen niet worden vergroot of verkleind.

### [!UICONTROL Move] {#move}

Verplaats elementen op de pagina. In tegenstelling tot [!UICONTROL Rearrange] optie, [!UICONTROL Move] verschuift andere elementen niet om ruimte te maken voor het element dat wordt verplaatst. Gebruik de pijltoetsen om de verplaatsing te verfijnen. (Geplande verbetering: ondersteuning om ervoor te zorgen dat verplaatste elementen niet achter andere elementen worden verborgen.)

In bepaalde situaties, bijvoorbeeld wanneer een CSS-beperking vereist dat een element binnen het bovenliggende element blijft, kunt u het element niet buiten het bovenliggende element plaatsen. Een element kan niet worden verplaatst buiten een container met de volgende CSS-eigenschap: `overflow: hidden`.

Zie [!UICONTROL Rearrange] voor meer informatie over inconsequent gedrag met de [!UICONTROL Move] en [!UICONTROL Rearrange] handelingen als gevolg van het uitgestelde laden van DOM-elementen.

### [!UICONTROL Hide]

Verberg het element. De witruimte blijft behouden, maar de inhoud wordt verwijderd.

### [!UICONTROL Remove]

Verwijder het element. De witruimte achter de afbeelding wordt verwijderd en de ruimte waar het element is samengevouwen.

**Opmerking:** Items in een &#39;klassieke&#39; box (een box die is gemaakt in een campagne voor &#39;klassieke inhoud&#39; van Target) kunnen met deze optie niet worden verwijderd.

## [!UICONTROL Expand Section]

Selecteer naast het oorspronkelijk geselecteerde element ook het bovenliggende element. Wanneer u een bovenliggend element selecteert, worden alle onderliggende elementen van dat element automatisch geselecteerd. U kunt de selectie meerdere keren uitbreiden.

## [!UICONTROL Navigate to Link]

Open de bestemming van de koppeling.

## [!UICONTROL Undo]/[!UICONTROL Redo]

Wijzigingen die u tijdens een bewerkingssessie in uw activiteiten aanbrengt, ongedaan maken. U kunt ook wijzigingen opnieuw uitvoeren die eerder ongedaan zijn gemaakt.

## Overwegingen {#considerations}

* Als een aanbieding HTML-inhoud bevat, raadpleegt u &quot;Hoe geeft at.js aanbiedingen met HTML-inhoud weer&quot; in [Hoe werkt at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render) voor meer informatie .

## Ondersteuning voor aangepaste elementen {#custom}

De steun VEC [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components) om persoonlijke ervaringen en aanbiedingen op aangepaste elementen en op elementen in aangepaste elementen te maken en te testen. Deze functionaliteit is beschikbaar in de VEC voor alle [!DNL Target] typen activiteiten.

>[!NOTE]
>
>VEC-ondersteuning voor aangepaste elementen wordt ondersteund in [at.js-versie](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) 2.7.0 (of hoger). Zorg ervoor dat de vereiste versie van uw website is geïmplementeerd. Als u het [Helpextensie Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), moet ook de vereiste versie van at.js worden opgesteld. De hierboven beschreven VEC-opties zijn niet zichtbaar en zijn beschikbaar voor gebruik met niet-ondersteunde versies van at.js.
>
>VEC-ondersteuning voor aangepaste elementen wordt momenteel niet ondersteund door de [Adobe Experience Platform Web SDK](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

De meeste acties VEC worden gesteund op douanegebeurtenissen en binnen douanegebeurtenissen, met de volgende uitzonderingen:

De volgende acties zijn niet beschikbaar voor aangepaste elementen:

* [!UICONTROL Edit]
   * [!UICONTROL Text/HTML]
   * [!UICONTROL Link]
   * [!UICONTROL Edit Source]

* [!UICONTROL Replace Content]

De volgende actie is niet beschikbaar in aangepaste elementen:

* [!UICONTROL Layout]
   * [!UICONTROL Rearrange]

## Navigeren door elementen met het DOM-pad {#dom-path}

Wanneer u een element op de pagina klikt, toont het VEC optiesmenu. Wanneer u op een element klikt, wordt bovendien het bijbehorende DOM-pad onder aan de pagina weergegeven.

![DOM-pad](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path.png)

U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

Wanneer u de cursor op het DOM-pad plaatst, wordt het bijbehorende element in de VEC gemarkeerd met een blauw vak. Wanneer u op het element klikt, wordt het element gemarkeerd met een oranje vak en wordt het menu VEC-opties weergegeven, zoals hierboven wordt uitgelegd.

U kunt gemakkelijk aan om het even welk ouder, sibling, of kindelement binnen VEC navigeren gebruikend de weg DOM.

De DOM-padfunctie is ook beschikbaar bij het instellen [klikken op bijhouden](/help/main/c-activities/r-success-metrics/click-tracking.md).
