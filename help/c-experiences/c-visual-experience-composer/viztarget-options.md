---
keywords: visual experience composer options;experience composer options;experience options;edit text;edit html;edit text/html;edit background color;background color;insert element;edit link;link;visual experience composer link;edit css class;css class;swap offer;offer swap;swap image;image swap;remove item;item remove;hide item;item hide;rearrange;move element;element move;resize element;element resize;element;expand selection;navigate to this link;navigate link;link navigate;navigate;link;undo;redo;undo/redo
description: Wanneer u op een paginaelement in Adobe Target Visual Experience Composer (VEC) klikt, toont een menu de opties die voor dat elementtype beschikbaar zijn.
title: Opties voor Adobe Target Visual Experience Composer (VEC)
feature: vec
topic: Standard
uuid: efd672ae-c684-455f-8ec1-0efcfe1e9534
translation-type: tm+mt
source-git-commit: d70e5c2c90b80b91ceb3b83800af330f436696d5
workflow-type: tm+mt
source-wordcount: '2358'
ht-degree: 0%

---


# Opties voor composer visuele ervaring{#visual-experience-composer-options}

Wanneer u een paginaelement in de Visuele Composer van de Ervaring (VEC) klikt, toont een menu de opties die voor dat elementtype beschikbaar zijn. Bovendien wordt onder aan de pagina een DOM-pad weergegeven waarmee u gemakkelijk door de paginastructuur kunt navigeren.

## VEC-opties

De diverse acties Visual Experience Composer (VEC) worden gegroepeerd aangewezen menuopties om uw baan sneller en efficiënter te maken:

![Menu VEC-opties](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/vec-options.png)

>[!NOTE]
>
>Welke opties beschikbaar zijn, is afhankelijk van het type activiteit dat u bewerkt.

### Bewerken

De volgende opties zijn beschikbaar:

#### Tekst/HTML {#edit-text-html}

Wijzig de HTML-code voor het element, zoals de tekst voor een tekstgebied, knop of koppeling.

Naast HTML-code kunt u aangepaste JavaScript bewerken en injecteren.

Er zijn verschillende opmaakopties voor RTF-tekst beschikbaar wanneer u tekst en HTML bewerkt voor [!UICONTROL A/B] en [!UICONTROL Experience Targeting] activiteiten. U kunt een lettertype kiezen, een lettertypestijl selecteren, de tekstuitlijning wijzigen en andere standaardopties voor tekstopmaak opgeven. Bij het wijzigen van HTML kunt u schakelen tussen de codeweergave en de rijke-bewerkingsweergave van de HTML.

De volgende HTML5-tags kunnen worden genest:

| Tag | Geneste tags toegestaan |
| --- | --- |
| `<a>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>`, `<div>`, `<figure>`, `<figcaption>` |
| `<ins>` | `<h1-h6>`, `<p>`, `<ul>`, `<ol>`, `<menu>` |
| `<del>` | `<ul>`, `<ol>`, `<menu>`, `<h1-h6>`, `<p>` |
| `<label>` | `<p>` |

#### Achtergrondkleur

Gebruik de kleurkiezer om een achtergrondkleur te selecteren of te configureren. U kunt een kleurstaal selecteren en dit aanpassen met RGB-waarden of kleurhexcodes. De rode x in de kleurkiezer maakt de achtergrond transparant.

**Opmerking:** Deze optie is niet beschikbaar voor een element waarbij een achtergrondafbeelding is ingesteld.

#### Stijlen {#styles}

In het [!UICONTROL Styles] deelvenster kunt u de waarde van bestaande stijlen voor het geselecteerde element weergeven of bewerken. U kunt ook extra stijlen toevoegen.

U opent het [!UICONTROL Styles] deelvenster door vanuit de VEC op een pagina-element te klikken en vervolgens op **[!UICONTROL Edit]** > **[!UICONTROL Styles]**.

Het [!UICONTROL Styles] deelvenster wordt aan de rechterkant van de VEC weergegeven. Het deelvenster bevat een lijst met stijlen waarmee u het geselecteerde element kunt bewerken of uitbreiden. Met een real-time CSS-editor kunt u wijzigingen weergeven en stijlen toevoegen als u dit comfortabel vindt met CSS (Cascading Style Sheets) of als u code van uw ontwikkelaar ontvangt.

![Deelvenster Stijlen](/help/c-experiences/c-visual-experience-composer/assets/styles-panel-new.png)

Als u verschillende stijlen toepast, kunt u uw wijzigingen altijd herstellen door te klikken op het [!UICONTROL Revert] pictogram dat in de rechterbovenhoek van het [!UICONTROL Styles] deelvenster wordt weergegeven nadat u een wijziging hebt aangebracht in een sectie. Door op het [!UICONTROL Revert] pictogram te klikken worden alle wijzigingen in het deelvenster van de huidige sectie ongedaan gemaakt.

Breid elke sectie uit om stijlen te bewerken of toe te voegen, zoals hieronder wordt uitgelegd. Als u de wijzigingen wilt opslaan, klikt u op het pictogram Vorige boven in het deelvenster om terug te keren naar de hoofdweergave van het deelvenster en klikt u vervolgens op **[!UICONTROL Save]**.

De blauwe stippen in het hoofddeelvenster en naast elke optie in de verschillende sectiedeelvensters geven aan dat u wijzigingen hebt aangebracht in de overeenkomende stijlen. Zo kunt u uw wijzigingen gemakkelijk controleren voordat u op de wijzigingen klikt [!UICONTROL Save].

>[!NOTE]
>
>Snelle acties voor lay-outveranderingen, achtergrondkleur, resizing, en beweging zijn ook beschikbaar als afzonderlijke acties in het menu VEC. U kunt deze opties gebruiken als afzonderlijke handelingen of u kunt het menu Stijlen gebruiken, zoals hier wordt uitgelegd.

* **Achtergrond**

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

* **Typografie**

   De typografie van een element wijzigen. Typografische bewerkingen zijn snel en gemakkelijk.

   Hoewel de rijke tekstredacteur (geef Tekst/HTML uit) beschikbaar voor het nauwkeurige stemmen is, zijn de snelle acties om veranderingen in het volledige element aan te brengen beschikbaar door deze optie. Als u typografie-wijzigingen alleen wilt toepassen op een deel van de tekst (en niet op de volledige tekst), gebruikt u de [RTF-editor](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md).

   U kunt de volgende typografiestijlen bewerken:

   * Fontgrootte
   * Lettertypedikte
   * Lettertypestijl
   * Kleur (geef de kleurcode op of gebruik de kleurkiezer)
   * Woordspatiëring
   * Lijnhoogte
   * Tekstuitlijning

* **Marge**

   Wijzig de marge voor het geselecteerde element. U kunt de linker-, rechter-, onder- en bovenmarge wijzigen.

   Klik op het vervolgkeuzepictogram voor elke marge om een van de volgende opties te kiezen:

   * Automatisch
   * Waarde (sleep de schuifregelaar om de marge in te stellen of geef het aantal pixels voor elke marge op)

   Marge ondersteunt positieve en negatieve waarden.

   Het doel ondersteunt ook andere grootteeenheden, zoals rem, pc, em, enz. Zie CSS-tips en trucs voor [webstijlpagina&#39;s voor meer informatie over deze eenheden](https://www.w3.org/Style/Examples/007/units.en.html).

* **Opvulling**

   Wijzig de opvulling voor het geselecteerde element. U kunt de opvulling links, rechts, onder en boven wijzigen.

   Sleep de schuifregelaar om de opvulling in te stellen of geef het aantal pixels voor de opvulling op.

   Opvulling ondersteunt de breedte vanaf 0.

   Het doel ondersteunt ook [andere grootteeenheden](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em, enz.

* **Rand**

   Klik op de randpictogrammen boven in het deelvenster om de rand van het geselecteerde element te wijzigen.

   U kunt de volgende stijlen voor elke rand (boven, rechts, onder en links) bewerken:

   * Randstijl (geen, verborgen, gestippeld, onderbroken, effen of dubbel)
   * Randkleur (geef de kleurcode op of gebruik de kleurkiezer)
   * Randbreedte (sleep de schuifregelaar om een randbreedte te selecteren of geef de breedte op in pixels)

   Rand ondersteunt breedteschalen vanaf 0.

   Het doel ondersteunt ook [andere grootteeenheden](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em, enz.

* **Positie**

   Verplaats het geselecteerde element vanaf de huidige positie. U kunt de boven-, onder-, links-, rechts- en [Z-indexpositie](https://www.w3schools.com/cssref/pr_pos_z-index.asp) van het element wijzigen.

   Klik op de [!UICONTROL Static] vervolgkeuzelijst om een van de volgende positieopties te kiezen:

   * Statisch
   * Relatief
   * Absoluut
   * Vast
   * Vast

   Klik op het vervolgkeuzepictogram voor elke positie om een van de volgende opties te kiezen:

   * Automatisch
   * Waarde (sleep de schuifregelaar om het element te plaatsen of geef het aantal pixels op dat u het element wilt verplaatsen)

   De positie ondersteunt positieve en negatieve waarden.

   Het doel ondersteunt ook [andere grootteeenheden](https://www.w3.org/Style/Examples/007/units.en.html), zoals rem, pc, em, enz.

* **Grootte**

   Wijzig de breedte en hoogte van het geselecteerde element.

   Klik op het vervolgkeuzepictogram naast [!UICONTROL Width] [!UICONTROL Height] en kies een van de volgende opties:

   * Automatisch
   * Waarde (sleep de schuifregelaar om de grootte van het element te wijzigen of om het aantal pixels voor elke dimensie op te geven)

* **Filter**

   Sleep de schuifregelaar voor elke filteroptie of geef het gewenste percentage op:

   * Sepia
   * Contrast
   * Helderheid
   * Grijswaarden
   * Vervagen
   * Dekking
   * Omkeren
   * Kleurtoon roteren
   * Verzadigen

* **CSS-editor**

   Met de CSS-editor in real-time kunt u wijzigingen bekijken en stijlen toevoegen als u het prettig vindt Cascading Style Sheets (CSS) te gebruiken of als u code van uw ontwikkelaar ontvangt.

   In de CSS-editor worden alle wijzigingen weergegeven die u aanbrengt in het deelvenster Stijlen. Zoals in de onderstaande afbeelding wordt getoond, zijn de tekengrootte, de bovenrand en de afbeeldingsgrootte gewijzigd:

   ![CSS-editor met wijzigingen](/help/c-experiences/c-visual-experience-composer/assets/css-changes.png)

   Let op de blauwe stippen naast de [!UICONTROL Typography], [!UICONTROL Border]en [!UICONTROL Size] opties in de voorafgaande illustratie. Deze punten geven aan dat u wijzigingen hebt aangebracht in deze secties. Als u deze sectievensters opent, worden blauwe stippen weergegeven naast de specifieke opties die u hebt gewijzigd.

   U kunt uw eigen code typen als de gewenste stijl niet standaard beschikbaar is in het [!UICONTROL Styles]dialoogvenster.

   Houd er rekening mee dat in de CSS-editor alleen details voor de huidige sessie worden weergegeven. Als u de wijzigingen opslaat en de editor vervolgens opnieuw opent, worden de gegevens over de vorige wijziging niet weergegeven in de editor, zelfs niet als u hetzelfde element opnieuw selecteert.

   >[!IMPORTANT]
   >
   >U kunt een achtergrondafbeelding toepassen met de CSS-editor, maar dit kan flikkering veroorzaken. Test uw wijzigingen vóór de implementatie.

#### CSS-klasse

Geef de vooraf gedefinieerde CSS-klasse op die voor het element wordt gebruikt. Als er meer dan één element is geselecteerd, scheidt u meerdere CSS-klassen met een spatie.

Beschikbaar voor [!UICONTROL A/B], [!UICONTROL Automated Personalization]en [!UICONTROL Multivariate Test] activiteiten.

#### Koppeling

Wijzig de URL in de koppeling.

Gebruik Koppeling bewerken om de kiezer bij te werken zodat deze naar hetzelfde afbeeldingselement wijst. Koppelingen naar een ander afbeeldingselement worden echter niet ondersteund. Als u een koppeling wilt maken naar een ander afbeeldingselement, verwijdert u de oorspronkelijke handeling uit de code-editor en gebruikt u de handeling [!UICONTROL Visual Experience Composer] om de handeling toe te passen op het andere afbeeldingselement.

### Invoegen voor

De volgende opties zijn beschikbaar:

#### Afbeelding, HTML en Tekst

Voeg om het even welk soort element aan uw pagina naast het wijzigen van bestaande inhoud toe. Voeg tekst, code, lijsten en meer toe om geheel verschillende ervaringen te maken die u wilt testen.

Selecteer een element op de pagina, klik [!UICONTROL Insert Before] en kies of u een beeld, HTML, of tekst wilt opnemen. Het ingevoegde element wordt vóór het geselecteerde element weergegeven.

Het gedrag van het ingevoegde element is afhankelijk van de structuur van de pagina, uw CSS en andere opties voor paginaconfiguratie. Geldige HTML is vereist om de pagina correct te laten verschijnen. Test de pagina altijd nadat u een item hebt ingevoegd om er zeker van te zijn dat het er naar behoren uitziet.

[!UICONTROL Recommendations] ondersteunt [!UICONTROL Insert Before] de inhoud van DIV-, SECTION- en ARTIKEL-tags.

**Opmerking:** Als u een afbeelding invoegt, moet deze [!DNL Adobe Scene7 Publishing System] zijn ingeschakeld, zodat u toegang hebt tot de afbeeldingsbibliotheek.

#### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Zie [Recommendations als een voorstel](/help/c-recommendations/recommendations-as-an-offer.md)voor meer informatie.

#### Ervaar fragment

Voeg ervaringsfragmenten in die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten om optimalisatie of personalisatie te ondersteunen. Zie Fragmenten voor [AEM ervaring voor meer informatie](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Invoegen na

De volgende opties zijn beschikbaar:

#### Afbeelding, HTML en Tekst

Voeg om het even welk soort element aan uw pagina naast het wijzigen van bestaande inhoud toe. Voeg tekst, code, lijsten en meer toe om geheel verschillende ervaringen te maken die u wilt testen.

Selecteer een element op de pagina, klik [!UICONTROL Insert After] en kies of u een beeld, HTML, of tekst wilt opnemen. Het ingevoegde element verschijnt na het geselecteerde element.

Het gedrag van het ingevoegde element is afhankelijk van de structuur van de pagina, uw CSS en andere opties voor paginaconfiguratie. Geldige HTML is vereist om de pagina correct te laten verschijnen. Test de pagina altijd nadat u een item hebt ingevoegd om er zeker van te zijn dat het er naar behoren uitziet.

[!UICONTROL Recommendations] ondersteunt [!UICONTROL Insert After] de inhoud van DIV-, SECTION- en ARTIKEL-tags.

**Opmerking:** Als u een afbeelding invoegt, moet deze [!DNL Adobe Scene7 Publishing System] zijn ingeschakeld, zodat u toegang hebt tot de afbeeldingsbibliotheek.

#### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Zie [Recommendations als een voorstel](/help/c-recommendations/recommendations-as-an-offer.md)voor meer informatie.

#### Ervaar fragment

Voeg ervaringsfragmenten in die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten om optimalisatie of personalisatie te ondersteunen. Zie Fragmenten voor [AEM ervaring voor meer informatie](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Vervangen door

De volgende opties zijn beschikbaar:

#### Afbeelding

Selecteer een andere afbeelding in de inhoudsbibliotheek. Tot de afbeeldingen die u kunt wisselen, behoren de afbeeldingen die naar de map Experience Cloud Assets zijn geüpload of die in de inhoudsbibliotheek in Doel zijn geüpload.

Tijdens het maken van de eerste activiteit is de weergegeven URL niet de URL die voor levering wordt gebruikt. Bij het synchroniseren van activiteiten wordt die URL bijgewerkt naar een productie-Scene7-URL.

De eerste URL kan er bijvoorbeeld als volgt uitzien:

`https://test.marketing.adobe.com/content/dam/mac/scholasticinc/Aug_MBM.jpeg?ch_ck=1470774943867`

Na het synchroniseren van activiteiten, zou de levering URL als het volgende voorbeeld kunnen kijken:

`http://s7d2.scene7.com/is/image/TargetTest/Aug_MBM?tm=1470768352933&fit=constrain&hei=173&wid=300`

Recommendations biedt ondersteuning voor Vervangen door in DIV-, SECTION- en ARTIKEL-tags.

**Opmerking:** Voor het wisselen van afbeeldingen is een Adobe Scene7 Publishing System-account vereist.

#### HTML-aanbieding

Selecteer een ander voorstel in de [!UICONTROL Content Library]lijst.

**Opmerking:** HTML-aanbiedingen worden opgeslagen op [!DNL Target] servers.

Een HTML-aanbieding kan maximaal 256 kB groot zijn.

#### Aanbeveling

Neem aanbevelingen op in A/B-testactiviteiten (inclusief Automatische toewijzing en Auto-Target) en Gericht op ervaring (XT). Zie [Recommendations als een voorstel](/help/c-recommendations/recommendations-as-an-offer.md)voor meer informatie.

#### Ervaar fragment

Voeg ervaringsfragmenten in die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten om optimalisatie of personalisatie te ondersteunen. Zie Fragmenten voor [AEM ervaring voor meer informatie](/help/c-experiences/c-manage-content/aem-experience-fragments.md).

### Layout

De volgende opties zijn beschikbaar:

#### Opnieuw rangschikken

Sleep het element naar een andere locatie binnen hetzelfde bovenliggende element of DIV. Andere elementen verschuiven de locatie om ruimte te maken voor het opnieuw gerangschikte element.

**Opmerking:** Klik op bijhouden om de items niet opnieuw te rangschikken.

#### Formaat wijzigen

Wijzig de grootte van een element op de pagina. Wanneer u [!UICONTROL Resize]deze optie selecteert, wordt rechtsonder in het element een greep weergegeven waarmee u die hoek kunt slepen om het formaat te wijzigen. Houd Shift ingedrukt als u dezelfde hoogte-breedteverhouding wilt behouden.

**Opmerking:** Inline-elementen kunnen niet worden vergroot of verkleind.

#### Verplaatsen {#move}

Verplaats elementen op de pagina. Anders dan bij de [!UICONTROL Rearrange] optie [!UICONTROL Move] worden andere elementen niet verschoven om ruimte te maken voor het element dat wordt verplaatst. Gebruik de pijltoetsen om de verplaatsing te verfijnen. (Geplande verbetering: ondersteuning om ervoor te zorgen dat verplaatste elementen niet achter andere elementen worden verborgen.)

In sommige gevallen, bijvoorbeeld wanneer een CSS-beperking vereist dat een element binnen het bovenliggende element blijft, kunt u het element niet buiten het bovenliggende element plaatsen. Een element kan niet worden verplaatst buiten een container met de volgende CSS-eigenschap: `overflow: hidden`.

#### Verbergen

Verberg het element. De witruimte blijft behouden, maar de inhoud wordt verwijderd.

#### Verwijderen

Verwijder het element. De witruimte achter de afbeelding wordt verwijderd en de ruimte waar het element is samengevouwen.

**Opmerking:** Items in een &#39;klassieke&#39; box (een box die is gemaakt in een campagne voor &#39;klassieke inhoud&#39; van Target) kunnen met deze optie niet worden verwijderd.

### Sectie uitvouwen

Selecteer naast het oorspronkelijk geselecteerde element ook het bovenliggende element. Wanneer u een bovenliggend element selecteert, worden alle onderliggende elementen van dat element automatisch geselecteerd. U kunt de selectie meerdere keren uitbreiden.

### Navigeren naar koppeling

Open de bestemming van de koppeling.

### Ongedaan maken/Opnieuw

Wijzigingen die u tijdens een bewerkingssessie in uw activiteiten aanbrengt, ongedaan maken. U kunt ook wijzigingen opnieuw uitvoeren die eerder ongedaan zijn gemaakt.

## Overwegingen {#considerations}

* Als een aanbieding HTML-inhoud bevat, raadpleegt u &quot;How at.js renders aanbiedingen with HTML content&quot; in [How at.js werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md#render) voor meer informatie.

## Navigeren door elementen met het DOM-pad {#dom-path}

Wanneer u een element op de pagina klikt, toont het VEC optiesmenu. Wanneer u op een element klikt, wordt bovendien het bijbehorende DOM-pad onder aan de pagina weergegeven.

![DOM-pad](/help/c-experiences/c-visual-experience-composer/assets/dom-path.png)

U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

Wanneer u de cursor op het DOM-pad plaatst, wordt het bijbehorende element in de VEC gemarkeerd met een blauw vak. Wanneer u op het element klikt, wordt het element gemarkeerd met een oranje vak en wordt het menu VEC-opties weergegeven, zoals hierboven wordt uitgelegd.

U kunt gemakkelijk aan om het even welk ouder, sibling, of kindelement binnen VEC navigeren gebruikend de weg DOM.

De DOM-padfunctie is ook beschikbaar wanneer u [klikt op bijhouden](/help/c-activities/r-success-metrics/click-tracking.md).