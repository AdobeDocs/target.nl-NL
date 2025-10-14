---
keywords: visuele ervaring composer-opties;beleving composer-opties;ervaringsopties;geef tekst uit;bewerk tekst/html;bewerk achtergrondkleur;voeg element in;bewerk de koppeling;link;visuele ervaring composer-koppeling;bewerk css-klasse;css-klasse;wisselaanbod;bied;afbeeldingswisseling;verwijder item;item verwijderen;item verbergen;element verplaatsen;element verplaatsen;element vergroten;element wijzigen; element wijzigen;element;selectie uitbreiden;navigeren naar deze koppeling;navigeren door koppeling;navigeren;koppelen;navigeren;koppeling ongedaan maken;opnieuw uitvoeren;ongedaan maken/opnieuw uitvoeren;aangepaste gebeurtenissen;webcomponenten;aanbieden, beslissing;aanbieden, beslissing
description: Onderzoek de opties beschikbaar in  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).
title: Hoe gebruik ik de opties voor [!UICONTROL Visual Experience Composer] (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 50993d6c-5025-488a-8b33-9ed7c142de6e
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '2667'
ht-degree: 0%

---

# Opties voor Visual Experience Composer

Wanneer u op een pagina-element in de map [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) klikt, wordt een menu weergegeven met de opties die beschikbaar zijn voor dat elementtype. Bovendien wordt onder aan de pagina een DOM-pad weergegeven waarmee u gemakkelijk door de paginastructuur kunt navigeren.

De verschillende [!UICONTROL Visual Experience Composer] (VEC) acties worden gegroepeerd in de juiste menuopties om uw taak sneller en efficiënter te maken:

![&#x200B; VEC optiemenu &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Welke opties beschikbaar zijn, is afhankelijk van het type activiteit dat u maakt of bewerkt.

## [!UICONTROL Edit]

De volgende opties zijn beschikbaar:

### [!UICONTROL Text/HTML] {#edit-text-html}

Wijzig de HTML-code voor het element, zoals de tekst voor een tekstgebied, knop of koppeling.

Naast de HTML-code kunt u aangepaste JavaScript bewerken en injecteren.

Er zijn diverse opmaakopties voor RTF-tekst beschikbaar wanneer u tekst bewerkt en HTML voor [!UICONTROL A/B] - en [!UICONTROL Experience Targeting] -activiteiten. U kunt een lettertype kiezen, een lettertypestijl selecteren, de tekstuitlijning wijzigen en andere standaardopties voor tekstopmaak opgeven. Als u HTML wijzigt, kunt u schakelen tussen de codeweergave en de rijke bewerkingsweergave van de HTML.

De volgende HTML5-tags kunnen worden genest:

| Tag | Geneste tags toegestaan |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

### [!UICONTROL Background Color]

Gebruik de kleurkiezer om een achtergrondkleur te selecteren of te configureren. U kunt een kleurstaal selecteren en dit aanpassen met RGB-waarden of kleurhexcodes. De rode x in de kleurkiezer maakt de achtergrond transparant.

**Nota:** Deze optie is niet beschikbaar voor een element waar een achtergrondbeeld wordt geplaatst.

### [!UICONTROL Styles] {#styles}

In het deelvenster [!UICONTROL Styles] kunt u de waarde van bestaande stijlen voor het geselecteerde element weergeven of bewerken. U kunt ook extra stijlen toevoegen.

U opent het deelvenster [!UICONTROL Styles] door vanuit de VEC op een pagina-element te klikken en vervolgens op **[!UICONTROL Edit]** > **[!UICONTROL Styles]** te klikken.

Het deelvenster [!UICONTROL Styles] wordt weergegeven aan de rechterkant van de VEC. Het deelvenster bevat een lijst met stijlen waarmee u het geselecteerde element kunt bewerken of uitbreiden. Met een real-time CSS-editor kunt u wijzigingen weergeven en stijlen toevoegen als u dit comfortabel vindt met CSS (Cascading Style Sheets) of als u code van uw ontwikkelaar ontvangt.

![&#x200B; het paneel van Stijlen &#x200B;](/help/main/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Als u verschillende stijlen toepast, kunt u uw wijzigingen altijd herstellen door te klikken op het pictogram [!UICONTROL Revert] dat in de rechterbovenhoek van het deelvenster [!UICONTROL Styles] wordt weergegeven nadat u een sectie hebt gewijzigd. Als u op het pictogram [!UICONTROL Revert] klikt, worden alle wijzigingen in het deelvenster van de huidige sectie ongedaan gemaakt.

Breid elke sectie uit om stijlen te bewerken of toe te voegen, zoals hieronder wordt uitgelegd. Als u de wijzigingen wilt opslaan, klikt u op het pictogram [!UICONTROL Back] boven in het deelvenster om terug te keren naar de hoofdweergave van het deelvenster en klikt u vervolgens op **[!UICONTROL Save]** .

Blauwe stippen in het hoofddeelvenster en naast elke optie in de verschillende sectiedeelvensters geven aan dat u de bijbehorende stijlen hebt gewijzigd. Met deze visuele indicator kunt u gemakkelijk uw wijzigingen controleren voordat u op [!UICONTROL Save] klikt.

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

  De typografie van een element wijzigen. Typografie-bewerkingen zijn snel en eenvoudig.

  Hoewel de rijke tekstredacteur (geef Tekst/HTML uit) beschikbaar voor het fijnstemmen is, zijn de snelle acties om het volledige element te veranderen beschikbaar via deze optie. Als u typografie veranderingen op slechts een deel van de tekst (niet op de volledige tekst) wilt toepassen, gebruik de [&#x200B; rijke tekstredacteur &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

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
   * [!UICONTROL Value] (sleep de schuifregelaar om de marge in te stellen of het aantal pixels voor elke marge op te geven)

  Marge ondersteunt positieve en negatieve waarden.

  Het doel ondersteunt ook andere grootteeenheden, zoals rem, pc en em. Voor meer informatie over deze eenheden, zie {de Bladen CSS van de Stijl van 0} Web Tips en Tricks [.](https://www.w3.org/Style/Examples/007/units.en.html)

* **[!UICONTROL Padding]**

  Wijzig de opvulling voor het geselecteerde element. U kunt de opvulling links, rechts, onder en boven wijzigen.

  Sleep de schuifregelaar om de opvulling in te stellen of geef het aantal pixels voor de opvulling op.

  Opvulling ondersteunt de breedte vanaf 0.

  Het doel steunt ook [&#x200B; andere grootteeenheden &#x200B;](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em.

* **[!UICONTROL Border]**

  Klik op de randpictogrammen boven in het deelvenster om de rand van het geselecteerde element te wijzigen.

  U kunt de volgende stijlen voor elke rand (boven, rechts, onder en links) bewerken:

   * [!UICONTROL Border style] (none, hidden, dotted, dashed, solid of double)
   * [!UICONTROL Border color] (geef de kleurcode op of gebruik de kleurkiezer)
   * [!UICONTROL Border width] (sleep de schuifregelaar om een randbreedte te selecteren of geef de breedte op in pixels)

  Rand ondersteunt breedteschalen vanaf 0.

  Het doel steunt ook [&#x200B; andere grootteeenheden &#x200B;](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em.

* **[!UICONTROL Position]**

  Verplaats het geselecteerde element vanaf de huidige positie. U kunt de bovenkant van het element, bodem, linker, recht, en [&#x200B; z-index &#x200B;](https://www.w3schools.com/cssref/pr_pos_z-index.asp) positie veranderen.

  Klik op de vervolgkeuzelijst [!UICONTROL Static] om een van de volgende positieopties te kiezen:

   * [!UICONTROL Static]
   * [!UICONTROL Relative]
   * [!UICONTROL Absolute]
   * [!UICONTROL Sticky]
   * [!UICONTROL Fixed]

  Klik op het vervolgkeuzepictogram voor elke positie om een van de volgende opties te kiezen:

   * [!UICONTROL Auto]
   * [!UICONTROL Value] (sleep de schuifregelaar om het element te plaatsen of geef het aantal pixels op dat u het element wilt verplaatsen)

  De positie ondersteunt positieve en negatieve waarden.

  Het doel steunt ook [&#x200B; andere grootteeenheden &#x200B;](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em.

* **[!UICONTROL Size]**

  Wijzig de breedte en hoogte van het geselecteerde element.

  Klik op het vervolgkeuzepictogram naast [!UICONTROL Width] en [!UICONTROL Height] om een van de volgende opties te kiezen:

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
*[!UICONTROL &#x200B; Hue-rotate]
   * [!UICONTROL Saturate]

* **[!UICONTROL CSS Editor]**

  Met de CSS-editor in real-time kunt u wijzigingen bekijken en stijlen toevoegen als u het prettig vindt Cascading Style Sheets (CSS) te gebruiken of als u code van uw ontwikkelaar ontvangt.

  In de CSS-editor worden alle wijzigingen weergegeven die u aanbrengt in het deelvenster Stijlen. Zoals in de onderstaande afbeelding wordt getoond, zijn de tekengrootte, de bovenrand en de afbeeldingsgrootte gewijzigd:

  ![&#x200B; CSS redacteur met veranderingen &#x200B;](/help/main/c-experiences/c-visual-experience-composer/assets/css-changes.png)

  U ziet de blauwe stippen naast de opties [!UICONTROL Typography] , [!UICONTROL Border] en [!UICONTROL Size] in de vorige illustratie. Deze punten geven aan dat u deze secties hebt gewijzigd. Als u deze sectievensters opent, worden blauwe stippen weergegeven naast de specifieke opties die u hebt gewijzigd.

  U kunt uw eigen code typen als de gewenste stijl niet standaard beschikbaar is in de [!UICONTROL Styles] .

  In de CSS-editor worden alleen details voor de huidige sessie weergegeven. Als u de wijzigingen opslaat en de editor vervolgens opnieuw opent, worden de gegevens over de vorige wijziging niet weergegeven in de editor, zelfs niet als u hetzelfde element opnieuw selecteert.

  >[!IMPORTANT]
  >
  >U kunt een achtergrondafbeelding toepassen met de CSS-editor, maar dit kan flikkering veroorzaken. Test uw wijzigingen vóór de implementatie.

### [!UICONTROL CSS Class]

Geef de vooraf gedefinieerde CSS-klasse op die voor het element wordt gebruikt. Als er meer dan één element is geselecteerd, scheidt u meerdere CSS-klassen met een spatie.

Beschikbaar voor [!UICONTROL A/B] -, [!UICONTROL Automated Personalization] - en [!UICONTROL Multivariate Test] -activiteiten.

### [!UICONTROL Link]

Wijzig de URL in de koppeling.

Gebruik Koppeling bewerken om de kiezer bij te werken zodat deze naar hetzelfde afbeeldingselement wijst. Koppelingen naar een ander afbeeldingselement worden echter niet ondersteund. Als u een koppeling wilt maken naar een ander afbeeldingselement, verwijdert u de oorspronkelijke handeling uit de code-editor en gebruikt u [!UICONTROL Visual Experience Composer] om de handeling toe te passen op het andere afbeeldingselement.

## [!UICONTROL Insert Before]

De volgende opties zijn beschikbaar:

### [!UICONTROL Offer Decision]

Voeg een [&#x200B; aanbieding toe die in  [!DNL Adobe Journey Optimizer] wordt gecreeerd &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=nl-NL){target=_blank} om de beste aanbieding en ervaring aan uw klanten voor te stellen gebruikend aanbiedingsbesluit.

**Nota:** Deze optie is beschikbaar wanneer het uitgeven van of het creëren van [&#x200B; handboek [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) slechts activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten.

Voor meer informatie, zie [&#x200B; Aanbiedingsbesluiten van het Gebruik &#x200B;](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image] , [!UICONTROL HTML] en [!UICONTROL Text]

Voeg om het even welk soort element aan uw pagina naast het wijzigen van bestaande inhoud toe. Voeg tekst, code, lijsten en nog veel meer toe om geheel andere ervaringen te maken die u wilt testen.

Selecteer een element op de pagina, klik vervolgens op [!UICONTROL Insert Before] en kies of u een afbeelding, HTML of tekst wilt invoegen. Het ingevoegde element wordt vóór het geselecteerde element weergegeven.

Het gedrag van het ingevoegde element is afhankelijk van de structuur van de pagina, uw CSS en andere opties voor paginaconfiguratie. Geldige HTML is vereist om de pagina correct weer te geven. Test de pagina altijd nadat u een item hebt ingevoegd om er zeker van te zijn dat het er naar behoren uitziet.

[!UICONTROL Recommendations] ondersteunt [!UICONTROL Insert Before] de inhoud van DIV-, SECTION- en ARTIKEL-tags.

**Nota:** het opnemen van een beeld vereist dat [!DNL Adobe Scene7 Publishing System] wordt toegelaten zodat hebt u toegang tot de beeldbibliotheek.

### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Voeg ervaringsfragmenten die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM), toe aan [!DNL Target] -activiteiten voor optimalisatie of personalisatie. Voor meer informatie, zie {de Fragmenten van de Ervaring van 0} AEM [.](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)

## [!UICONTROL Insert After]

De volgende opties zijn beschikbaar:

### [!UICONTROL Offer Decision]

Voeg een [&#x200B; aanbieding toe die in  [!DNL Adobe Journey Optimizer] wordt gecreeerd &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=nl-NL){target=_blank} om de beste aanbieding en ervaring aan uw klanten voor te stellen gebruikend aanbiedingsbesluit.

**Nota:** Deze optie is beschikbaar wanneer het uitgeven van of het creëren van [&#x200B; handboek [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) slechts activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten.

Voor meer informatie, zie [&#x200B; Aanbiedingsbesluiten van het Gebruik &#x200B;](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image] , [!UICONTROL HTML] en [!UICONTROL Text]

Voeg om het even welk soort element aan uw pagina naast het wijzigen van bestaande inhoud toe. Voeg tekst, code, lijsten en nog veel meer toe om geheel andere ervaringen te maken die u wilt testen.

Selecteer een element op de pagina, klik vervolgens op [!UICONTROL Insert After] en kies of u een afbeelding, HTML of tekst wilt invoegen. Het ingevoegde element verschijnt na het geselecteerde element.

Het gedrag van het ingevoegde element is afhankelijk van de structuur van de pagina, uw CSS en andere opties voor paginaconfiguratie. Geldige HTML is vereist om de pagina correct weer te geven. Test de pagina altijd nadat u een item hebt ingevoegd om er zeker van te zijn dat het er naar behoren uitziet.

[!UICONTROL Recommendations] ondersteunt [!UICONTROL Insert After] de inhoud van DIV-, SECTION- en ARTIKEL-tags.

**Nota:** het opnemen van een beeld vereist dat [!DNL Adobe Scene7 Publishing System] wordt toegelaten zodat hebt u toegang tot de beeldbibliotheek.

### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Voeg ervaringsfragmenten die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM), toe aan [!DNL Target] -activiteiten voor optimalisatie of personalisatie. Voor meer informatie, zie {de Fragmenten van de Ervaring van 0} AEM [.](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)

## [!UICONTROL Replace Content]

De volgende opties zijn beschikbaar:

### [!UICONTROL Offer Decision]

Voeg een [&#x200B; aanbieding toe die in  [!DNL Adobe Journey Optimizer] wordt gecreeerd &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html?lang=nl-NL){target=_blank} om de beste aanbieding en ervaring aan uw klanten voor te stellen gebruikend aanbiedingsbesluit.

**Nota:** Deze optie is beschikbaar wanneer het uitgeven van of het creëren van [&#x200B; handboek [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) slechts activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten.

Voor meer informatie, zie [&#x200B; Aanbiedingsbesluiten van het Gebruik &#x200B;](/help/main/c-integrating-target-with-mac/ajo/offer-decision.md).

### [!UICONTROL Image]

Selecteer een andere afbeelding in de inhoudsbibliotheek. Tot de afbeeldingen die u kunt wisselen, behoren de afbeeldingen die naar de map Experience Cloud Assets zijn geüpload of die in de Content Library in Target zijn geüpload.

Tijdens het maken van de eerste activiteit is de weergegeven URL niet de URL die voor levering wordt gebruikt. Op activiteit die synchroniseert, wordt die URL bijgewerkt aan een productie Scene7 URL.

De eerste URL kan er bijvoorbeeld als volgt uitzien:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Na het synchroniseren van activiteiten, zou de levering URL als het volgende voorbeeld kunnen kijken:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Aanbevelingen ondersteunen Vervangen door in DIV-, SECTION- en ARTIKEL-tags.

**Nota:** het ruilen beelden vereist een Rekening van het Systeem van Adobe Scene7 het Publiceren.

### [!UICONTROL HTML Offer]

Selecteer een andere aanbieding in de [!UICONTROL Content Library] .

**Nota:** Aanbiedingen van HTML worden opgeslagen op [!DNL Target] servers.

Een HTML-aanbieding kan maximaal 256 kB bedragen.

### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

### [!UICONTROL Experience Fragment]

Voeg ervaringsfragmenten die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM), toe aan [!DNL Target] -activiteiten voor optimalisatie of personalisatie. Voor meer informatie, zie {de Fragmenten van de Ervaring van 0} AEM [.](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md)

## [!UICONTROL Layout]

De volgende opties zijn beschikbaar:

### [!UICONTROL Rearrange]

Sleep het element naar een andere locatie binnen hetzelfde bovenliggende element of DIV. Andere elementen verschuiven de locatie om ruimte te maken voor het opnieuw gerangschikte element.

**Nota**: Het klikken-volgen werkt niet aan herschikte punten.

Op dit moment, veronderstellen bepaalde acties VEC, zoals [!UICONTROL Rearrange] en [!UICONTROL Move], dat de sibling elementen van de bron en bestemmings ouderelementen volledig worden geladen. Als lazy het laden onder de ouderelementen DOM (bron of bestemming) voorkomt, kunnen deze acties VEC inconsistent gedrag veroorzaken. We werken aan een betrouwbaardere benadering om VEC-acties te laten werken in lui geladen DOM-elementen. Als tijdelijke oplossing kunt u [!UICONTROL Custom Code] in deze scenario&#39;s gebruiken om uw ervaringen te renderen.

### [!UICONTROL Resize]

Wijzig de grootte van een element op de pagina. Wanneer u [!UICONTROL Resize] selecteert, wordt in de rechterbenedenhoek van het element een greep weergegeven waarmee u die hoek kunt slepen om het formaat te wijzigen. Houd Shift ingedrukt als u dezelfde hoogte-breedteverhouding wilt behouden.

**Nota:** De gealigneerde elementen kunnen niet resized.

### [!UICONTROL Move] {#move}

Verplaats elementen op de pagina. In tegenstelling tot de optie [!UICONTROL Rearrange] verschuift [!UICONTROL Move] andere elementen niet om ruimte te maken voor het element dat wordt verplaatst. Gebruik de pijltoetsen om de verplaatsing te verfijnen. (Geplande uitbreiding: ondersteuning om ervoor te zorgen dat verplaatste elementen niet achter andere elementen worden verborgen.)

In bepaalde situaties, bijvoorbeeld wanneer een CSS-beperking vereist dat een element binnen het bovenliggende element blijft, kunt u het element niet buiten het bovenliggende element plaatsen. Een element kan niet buiten een container worden verplaatst met de volgende CSS-eigenschap: `overflow: hidden` .

Zie [!UICONTROL Rearrange] hierboven voor meer informatie over inconsequent gedrag met de acties [!UICONTROL Move] en [!UICONTROL Rearrange] als gevolg van het uitgestelde laden van DOM-elementen.

### [!UICONTROL Hide]

Verberg het element. De witruimte blijft behouden, maar de inhoud wordt verwijderd.

### [!UICONTROL Remove]

Verwijder het element. De witruimte achter de afbeelding wordt verwijderd en de ruimte waar het element is samengevouwen.

**Nota:** De punten binnen een &quot;klassieke&quot;mbox (een mbox die binnen een Klassieke campagne van het Doel wordt gecreeerd) kunnen niet worden verwijderd gebruikend deze optie.

## [!UICONTROL Expand Section]

Selecteer naast het oorspronkelijk geselecteerde element ook het bovenliggende element. Wanneer u een bovenliggend element selecteert, worden alle onderliggende elementen van dat element automatisch geselecteerd. U kunt de selectie meerdere keren uitbreiden.

## [!UICONTROL Navigate to Link]

Open de bestemming van de koppeling.

## [!UICONTROL Undo]/[!UICONTROL Redo]

Wijzigingen die u tijdens een bewerkingssessie in uw activiteiten aanbrengt, ongedaan maken. U kunt ook wijzigingen opnieuw uitvoeren die eerder ongedaan zijn gemaakt.

## Overwegingen {#considerations}

* Als een aanbieding de inhoud van HTML bevat, zie &quot;hoe at.js aanbiedingen met de inhoud van HTML&quot;in [&#x200B; &quot;hoe at.js &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/at-js/how-atjs-works.html?lang=nl-NL){target=_blank} voor meer informatie teruggeeft.

## Ondersteuning voor aangepaste elementen {#custom}

VEC steunt {de Componenten van het Web 0} [&#x200B; om u gepersonaliseerde ervaringen en aanbiedingen op douaneelementen en op elementen binnen douaneelementen tot stand te brengen en te testen. &#x200B;](https://developer.mozilla.org/en-US/docs/Web/Web_Components) Deze functionaliteit is beschikbaar in VEC voor alle [!DNL Target] activiteitstypen.

>[!NOTE]
>
>De steun VEC voor douaneelementen wordt gesteund in [&#x200B; at.js versie &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} 2.7.0 (of later) {target=_blank}. Zorg ervoor dat de vereiste versie van uw website is geïmplementeerd. Als u de [&#x200B; Visuele de helperuitbreiding van Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) gebruikt, moet het ook de vereiste versie van at.js hebben opgesteld. De hierboven beschreven VEC-opties zijn niet zichtbaar en zijn beschikbaar voor gebruik met niet-ondersteunde versies van at.js.
>
>De steun VEC voor douaneelementen wordt momenteel niet gesteund met het [&#x200B; Web SDK van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

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

![&#x200B; DOM weg &#x200B;](/help/main/c-experiences/c-visual-experience-composer/assets/dom-path.png)

U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

Wanneer u de cursor op het DOM-pad plaatst, wordt het bijbehorende element in de VEC gemarkeerd met een blauw vak. Wanneer u op het element klikt, wordt het element gemarkeerd met een oranje vak en wordt het menu VEC-opties weergegeven, zoals hierboven wordt uitgelegd.

U kunt gemakkelijk aan om het even welk ouder, sibling, of kindelement binnen VEC navigeren gebruikend de weg DOM.

De DOM wegeigenschap is ook beschikbaar wanneer vestiging [&#x200B; het volgen &#x200B;](/help/main/c-activities/r-success-metrics/click-tracking.md) klikt.
