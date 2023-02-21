---
keywords: css kiezer;aangepaste code;code editor;Mobile Web Experience Editor
description: Leer hoe u het deelvenster Wijzigingen in Adobe gebruikt [!DNL Target] om paginawijzigingen weer te geven en extra wijzigingen toe te voegen (CSS-kiezer, Mbox en Aangepaste code).
title: Welke wijzigingen kan ik aanbrengen in mijn pagina?
feature: Visual Experience Composer (VEC)
exl-id: 23456a4b-9457-4f05-989e-a7c39ce17cc2
source-git-commit: 85319079e00db70184950d36778f2e4060b44209
workflow-type: tm+mt
source-wordcount: '2190'
ht-degree: 0%

---

# Wijzigingen

Informatie over de [!UICONTROL Modifications] pagina in [!DNL Adobe Target] Hiermee kunt u wijzigingen op de pagina weergeven en aanvullende wijzigingen toevoegen (CSS-kiezer, Mbox en Aangepaste code).

De [!UICONTROL Modifications] De pagina toont alle veranderingen die aan uw pagina in Visuele Composer van de Ervaring (VEC) zijn aangebracht en laat u extra veranderingen aanbrengen door elk element op de pagina te klikken en [een handeling selecteren](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81). Elke wijziging die u aanbrengt, verschijnt als een afzonderlijke actie of als een afzonderlijk element in het dialoogvenster [!UICONTROL Modifications] lijst. U kunt ook wijzigingen toevoegen, zoals de volgende wijzigingstypen: CSS-kiezer, Mbox. en Aangepaste code.

## Overzicht van wijzigingen {#section_EE27E7572AA74397BBDED563B2B3D509}

De [!UICONTROL Modifications] toont alle veranderingen die aan uw pagina in VEC zijn aangebracht. Elke wijziging die u aanbrengt, verschijnt als een afzonderlijke actie of als een afzonderlijk element in het dialoogvenster [!UICONTROL Modifications] lijst.

![codeeditor_page_mods, afbeelding](assets/codeeditor_page_mods.png)

Gebruik de pagina van Wijzigingen om kleine veranderingen in selecteur aan te brengen die het Doel kiest wanneer u VEC gebruikt om te vormen hoe de inhoud wordt geleverd. U kunt de inhoud of het kenmerk HTML wijzigen. U kunt de code ook bewerken om het equivalent van een HTML-aanbieding binnen een mbox te maken.

Met de pagina Wijzigingen kunt u:

* Bekijk een handeling die in de visuele composer is uitgevoerd.

   ![codeeditor_viewchange, afbeelding](assets/codeeditor_viewchange.png)

* Bewerk een bestaande handeling. Houd de aanwijzer boven de gewenste wijziging en klik vervolgens op de knop **[!UICONTROL Edit]** pictogram.

   ![codeeditor_afbeelding bewerken](assets/codeeditor_edit.png)

   Breng de gewenste wijzigingen aan.

   ![codeeditor_change1, afbeelding](assets/codeeditor_changechange1.png)

* Een bestaande handeling verwijderen. Houd de aanwijzer boven de gewenste wijziging en klik vervolgens op de knop **[!UICONTROL Delete]** pictogram.

   ![codeditor_delete afbeelding](assets/codeditor_delete.png)

* Voeg een nieuwe wijziging toe. Klikken **[!UICONTROL Add Modification]** of het + pictogram, dan specificeer uw veranderingen zoals hieronder beschreven.

   ![codeeditor_nieuwe afbeelding](assets/codeeditor_new.png)

   Nadat één wijziging is gemaakt, wordt boven in het deelvenster Wijzigingen een pictogram + weergegeven in plaats van de knop Wijziging toevoegen onder in het deelvenster.

* Koppel het deelvenster Wijzigingen verticaal langs de zijkant van de doelinterface of horizontaal onder aan het venster. Klik op de knop [!UICONTROL Dock] om tussen de twee instellingen te schakelen.

   ![codeditor_dock, afbeelding](assets/codeditor_dock.png)

   In het volgende voorbeeld ziet u het deelvenster Wijzigingen dat aan de onderkant van het scherm is gekoppeld:

   ![codeeditor_dock_bottom, afbeelding](assets/codeeditor_dock_bottom.png)

## Wijzigingen toevoegen {#section_C7ABCD5731A048CB8F90EDC31A32EDF9}

1. Als u het dialoogvenster [!UICONTROL Modifications] pagina voor een geselecteerde ervaring, in VEC klikken **[!UICONTROL Modifications]** &lt;/>-pictogram.

   ![codeeditor_pictogram_grote afbeelding](assets/codeeditor_icon_big.png)

   >[!NOTE]
   >
   >Als u het deelvenster Wijzigingen wilt openen in de Form-based Experience Composer, maakt of bewerkt u een HTML-aanbieding. Zie voor meer informatie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E).

   De [!UICONTROL Modifications] pagina wordt geopend, waarbij het scherm wordt gesplitst tussen de visuele modus aan de linkerkant en het deelvenster Wijzigingen aan de rechterkant. Klik op de knop [!UICONTROL Dock] pictogram om het deelvenster Wijzigingen verticaal langs de zijde van de doelinterface of horizontaal onderaan te koppelen. U ziet dat de ervaring A in de volgende afbeelding geen eerdere wijzigingen heeft ondergaan.

   ![codeeditor_pagina, afbeelding](assets/codeeditor_page.png)

   De ervaring B toont de vorige wijzigingen in [!UICONTROL Modifications] aan de rechterkant.

   ![codeeditor_page_mods, afbeelding](assets/codeeditor_page_mods.png)

1. Een wijziging toevoegen:

   * Als er geen eerdere wijzigingen voor de ervaring zijn aangebracht, klikt u op de knop **[!UICONTROL Add Modification]** onder aan het dialoogvenster [!UICONTROL Modifications] aan de rechterkant.
   * Als er vorige wijzigingen zijn aangebracht in de ervaring, klikt u op het pictogram + boven aan het dialoogvenster [!UICONTROL Modifications] aan de rechterkant.

   In het deelvenster Wijzigingen wordt het volgende weergegeven:

   ![codeeditor_page_mods_add image](assets/codeeditor_page_mods_add.png)

1. Van de **[!UICONTROL Modifications Type]** Kies het gewenste type in de vervolgkeuzelijst:

   | Type wijzigingen | Details |
   |--- |--- |
   | CSS-kiezer | Geef in het vak CSS-elementkiezer het gewenste CSS-element op dat u wilt wijzigen, selecteer een handelingstype (Inhoud instellen of Kenmerk instellen) en vul vervolgens de vereiste informatie en de gewenste inhoud in. |
   | Mbox | Geef de naam van het selectievakje en de gewenste inhoud op.<p>**Opmerking**: Mboxes worden niet meer ondersteund in de VEC op pagina&#39;s die at.js 2 gebruiken.*x*.<p>Als tijdelijke oplossing:<ul><li>Als u at.js 2 gebruikt.*x* voegt u een CSS-selectorwijziging toe in plaats van een Mbox-wijziging en voegt u de inhoud toe aan de kiezer die uw box gebruikte. </li><li>Gebruik op formulieren gebaseerde activiteiten (werkt met vakken en at.js 1.*x* en te.js 2.*x*).</li><li>Gebruik at.js 1.*x* in de VEC.</li></ul> |
   | Aangepaste code | Geef een optionele naam op of schakel de optie [!UICONTROL Add Code in the `<HEAD>` Sectie] Schakel het selectievakje naar wens in en voeg vervolgens uw aangepaste code toe.<p>Als u [!UICONTROL Add Code in the `<HEAD>` Sectie], wordt aangepaste code toegevoegd aan de  `<head>`  en de uitvoering ervan wachten niet op de gebeurtenissen body of page-load. Alleen toevoegen `<script>` en  `<style>` elementen. Toevoegen  `<div>`  tags en andere elementen kunnen de resterende  `<head>`  elementen die in de  `<body>`. Als u at.js gebruikt, zullen alle aanbiedingen asynchroon leveren.<p> Als u [!UICONTROL Add Code in the `<HEAD>` Sectie], wordt de aangepaste code direct na de gebeurtenis `<body>` tag. Alle code onderbrengen in één code `<div>` om de DOM-structuur te behouden. Als u at.js gebruikt, zullen alle aanbiedingen asynchroon leveren.<p>Indien HTML for `<BODY>` contains `<SCRIPT>` en `<DIV>`vervolgens `<DIV>` wordt toegevoegd aan `<BODY>` en `<SCRIPT>` wordt uitgevoerd in `<HEAD>`. Ook, `<SCRIPT>` dat een extern bestand laadt, wordt toegevoegd aan `<HEAD>`.<p>**Opmerking**: Scripts worden asynchroon uitgevoerd. Dit betekent dat u bijvoorbeeld niet kunt gebruiken `document.write`  of vergelijkbare scriptmethoden.<p>De code van de douane verstrekt een niet visuele interface aan mening, geeft uit en voegt nieuwe acties binnen VEC, op vorm-gebaseerde Composer van de Ervaring toe, en de HTML biedt redacteur aan. Het paneel verstrekt een codemening van een ervaring om u te helpen complexere ervaringen bouwen, bestaande ervaringen verfijnen, en kwesties problemen oplossen.<p>Aangepaste code is bedoeld voor geavanceerde gebruikers die comfortabel zijn met HTML, JavaScript en CSS. De codeweergave kan u helpen wijzigingen aan te passen of te perfectioneren, of selecteurproblemen te verhelpen. Deze kan ook worden gebruikt om nieuwe aangepaste code en handelingen toe te voegen. U kunt meerdere aangepaste code toevoegen en elke aangepaste code optioneel een naam geven.<p>**Opmerking**: De aangepaste code is momenteel alleen beschikbaar voor activiteiten van het type A/B en Experience Targeting (XT). Aangepaste code is uitgeschakeld voor overlay en als een omleidingsvoorstel wordt toegepast.<p>De code van de douane steunt de volgende gebruiksgevallen:<ul><li>Aangepaste JavaScript, HTML of CSS toevoegen die boven aan de pagina moet worden uitgevoerd</li><li>De code weergeven of bewerken die door VEC wordt gegenereerd nadat wijzigingen zijn aangebracht</li><li>Inhoud van HTML instellen voor een kiezer (alleen CSS-kiezers)</li><li>Een kenmerk instellen op een HTML-element</li><li>Aanbiedingsinhoud toevoegen die in een regionale box moet worden geleverd</li><li>Omwisselen op DOM-gereed met jQuery</li><li>Wisselen op DOM-klaar, geen jQuery (ondersteunt Internet Explorer 8 niet)</li><li>Wisselen met DOM-polling via &quot;elementOnLoad&quot;-plug-in</li><li>Aangepaste omleiding</li></ul>Aangepaste code biedt:<ul><li>Regelnummers voor betere bruikbaarheid.</li><li>Syntaxis markeren om onjuiste syntaxis voor HTML-aanbiedingen te voorkomen.</li><li>De mogelijkheid om meerdere aangepaste codes te maken en voor elke code een optionele naam op te geven. Door meerdere aangepaste codes te maken, kunt u in de toekomst gemakkelijker fouten opsporen. In plaats van bijvoorbeeld één aangepaste code te maken om verschillende wijzigingen door te voeren, kunt u voor elke wijziging een aparte aangepaste code met een beschrijvende naam maken. Als u afzonderlijke aangepaste codes hebt, kunt u uw wijzigingen modulair en beter beheren. Merk op dat de uitvoering van veelvoudige douanecodes in een activiteit niet gewaarborgd is om in de opeenvolging te gebeuren waarin zij werden gecreeerd.</li></ul>In het deelvenster Wijzigingen wordt het scherm opgesplitst tussen de visuele modus en de codemodus. Beide modi blijven gesynchroniseerd. Elke visueel aangebrachte wijziging heeft een overeenkomstige rij in de codemening. Op dezelfde manier elke verandering die in de codemening wordt begaan toont in de visuele ervaring. Wanneer u op een rij in de codeweergave klikt, wordt het bijbehorende element op de visuele pagina geselecteerd.<p>Aangepaste code ondersteunt HTML, scripts en stijlen. U kunt elke geldige HTML-code of elk geldig script toevoegen of bewerken. |

1. Voeg desgewenst aanvullende wijzigingen toe.

## Aangepaste praktijkgevallen voor code {#section_26CB3360097D400FB02E20AE5FDBA352}

De **[!UICONTROL Custom Code]** bevat code die wordt uitgevoerd aan het begin van het laden van de pagina.

U kunt de JavaScript-code in het dialoogvenster `<head>` tag. De uitvoering van code wacht niet op de `<body>` -tag aanwezig in het DOM.

Kiezers voor volgende visuele handelingen zijn afhankelijk van de HTML-elementen die op dit tabblad worden toegevoegd.

Het deelvenster Aangepaste code wordt vaak gebruikt om JavaScript of CSS boven aan de pagina toe te voegen.

![codeeditor_aangepaste afbeelding](assets/codeeditor_custom.png)

Gebruik de **[!UICONTROL Custom Code]** tab naar:

* JavaScript inline gebruiken of koppelen naar een extern JavaScript-bestand

   Bijvoorbeeld om de kleur van een element te wijzigen:

   ```javascript
   <script type="text/javascript"> 
   document.getElementById("element_id").style.color = "blue"; 
   </script> 
   ```

* Een stijl inline configureren of koppelen naar een externe stijlpagina

   U kunt bijvoorbeeld een klasse definiëren voor een overlay-element:

   ```html
   <style> 
   .overlay 
   { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; } 
   </style> 
   ```

* HTML-fragmenten toevoegen om nieuwe elementen te definiëren

   Gebruik bijvoorbeeld het volgende HTML-fragment om een bedekking te maken `<div>` de hierboven gedefinieerde CSS-klasse gebruiken:

   ```html
   <div class="overlay"></div>
   ```

* Omwisselen op DOM-gereed met jQuery

In het volgende voorbeeld met JQuery wordt ervan uitgegaan dat op de website van de klant jQuery beschikbaar is op de pagina wanneer [!DNL Target] voert de voorstellen uit.

```javascript
<style>#default_content {visibility:hidden;}</style> 
<script> 
jQuery( document ).ready(function() { 
    jQuery("#default_content").html( "<span style='color:red'>Hello <strong>Again</strong></span>" ); 
    jQuery("#default_content").css("visibility","visible"); 
}); 
</script> 
```

* Wisselen op DOM-gereed, geen jQuery (ondersteunt Internet Explorer 8 niet)

   ```javascript
   <style>#default_content {visibility:hidden;}</style> 
   <script> 
   document.addEventListener("DOMContentLoaded", function(event) {  
       document.getElementById("default_content").innerHTML = "<span style='color:red'>Hello <strong>Again</strong></span>"; 
       document.getElementById("default_content").style.visibility="visible"; 
   }); 
   </script> 
   ```

* Aangepaste omleiding door bestaande params `s_tnt` param (voor verouderde integratie aan Analytics), verwijzerparam, en mbox zitting

   ```javascript
   <style type="text/css">body{display:none!important;}</style> 
   <script type="text/javascript"> 
    var qs='';window.location.search?qs=window.location.search+'&':qs='?'; 
    window.location.replace('//www.mywebsite.com/'+qs+'s_tnt=${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}&s_tntref='+encodeURIComponent(document.referrer)+'&mboxSession='+mboxFactoryDefault.getSessionId().getId()+''+window.location.hash+''); 
   </script> 
   ```

* Voeg Adobe Target Experience Templates toe voor gebruik in aangepaste code. De Malplaatjes van de Ervaring van het doel zijn vooraf gecodeerde steekproeven met configureerbare input die moeten worden gebruikt om gemeenschappelijke telleruse-cases uit te voeren. Deze ervaringssjablonen worden gratis aan ontwikkelaars en marketers aangeboden als uitgangspunt voor het uitvoeren van veelvoorkomende gebruiksgevallen, hetzij via de VEC of de Form-based Experience Composer. Gebruiksgevallen zijn onder andere lichtbakken, carrousels, aftellingen en meer.

   Zie voor meer informatie [Experience Templates](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652).

## Aangepaste aanbevolen procedures voor code {#section_10DFFD9FB92A43C1BB444A45E0272B28}

**Plaats de aangepaste code altijd in één element.**

Bijvoorbeeld:

```html
<div id="custom-code"> 
// My Code goes here 
</div>
```

Breng wijzigingen aan in deze container als er wijzigingen nodig zijn.

Als u de aangepaste code niet meer nodig hebt, laat u deze container leeg, maar verwijdert u deze niet. Dit zorgt ervoor dat andere ervaringswijzigingen niet worden beïnvloed.

**Gebruik de element-id &#39;CDQID&#39; niet voor wijzigingen aan de pagina die in de Code-editor is gemaakt.**

Het doel past een nieuwe elementidentiteitskaart met de waarde &quot;CDQID&quot;op om het even welk element op de pagina toe die door Doel wordt gewijzigd. Omdat deze id door Doel wordt toegepast, zou het niet voor enige verdere wijzigingen of aanpassingen in de Redacteur van de Code moeten worden gebruikt.

**Voer geen document.write acties in de manuscripten van de douanecode uit.**

Scripts worden asynchroon uitgevoerd. Dit veroorzaakt vaak `document.write` acties die op de verkeerde plaats op uw pagina worden weergegeven. Gebruiken `document.write` in scripts die in aangepaste code worden gemaakt, wordt niet aangeraden.

**Als u een element maakt en het vervolgens wijzigt, verwijdert u het oorspronkelijke element niet.**

Bij elke wijziging wordt een nieuw element gemaakt in het deelvenster Wijzigingen. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft die actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer. Zie &quot;Problemen oplossen&quot; hieronder voor meer informatie.

**Wees voorzichtig als u de aangepaste codefunctie gebruikt voor twee activiteiten die dezelfde URL als doel hebben.**

Als u de aangepaste codefunctie gebruikt voor twee activiteiten die op dezelfde URL zijn gericht, wordt het JavaScript vanuit beide activiteiten in de pagina geïnjecteerd. Doel bepaalt automatisch de volgorde van de geleverde inhoud. Zorg ervoor dat de code niet afhankelijk is van plaatsing. Het is aan u om ervoor te zorgen dat er geen conflicten in de code zijn.

## Problemen met aangepaste code oplossen {#section_6C965CBC31C348D7AA5B57B63DAB9E7F}

**Ik heb een waarschuwing ontvangen dat een actie niet kan worden toegepast vanwege structurele wijzigingen op een pagina. Wat betekent dit?**

Dit bericht geeft aan dat de structuur van de pagina is gewijzigd sinds de activiteit voor het laatst is opgeslagen.

De ontbrekende kiezers zijn mogelijk bereikt in de modus Bladeren. We raden u aan elke ervaring te verwijderen en opnieuw te maken om ervoor te zorgen dat de inhoud er zo uitziet als u verwacht, zoals in het waarschuwingsbericht wordt aangegeven.

![code_editor_2 afbeelding](assets/code_editor_2.png)

***Als ik een element verwijder, krijg ik een waarschuwing te zien waarin staat: &quot;Het verwijderen van deze handeling kan gevolgen hebben voor vervolghandelingen.&quot; Wat betekent dit?***

Als u bijvoorbeeld twee handelingen hebt uitgevoerd:

* Een klasse toegevoegd aan Element 1
* De HTML voor Element 1 is bewerkt

Bij elke wijziging wordt een nieuw element gemaakt in het deelvenster Wijzigingen. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft de tweede actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer.

Met andere woorden, als u een element met tekst toevoegt, dan in een afzonderlijke actie bewerkt u dat element met verschillende tekst, toont het paneel van Wijzigingen beide acties als afzonderlijke elementen. Wanneer u het element hebt bewerkt, hebt u een nieuw element gemaakt dat het oorspronkelijke element wijzigt dat u hebt gemaakt en dat de bewerkte tekst bevat. Als u vervolgens het oorspronkelijke element verwijdert, kan de bewerkte tekst het bewerkte element niet vinden en wordt deze niet weergegeven. Het tweede element blijft in de lijst met elementen, maar heeft geen invloed op de pagina omdat het element dat wordt gewijzigd, niet meer bestaat.

***An element I created using `document.write` in een script wordt niet weergegeven op de positie die ik verwacht.***

Scripts worden asynchroon uitgevoerd. Dit veroorzaakt vaak `document.write` acties die op de verkeerde plaats op uw pagina worden weergegeven. Adobe adviseert niet gebruikend `document.write` in scripts die in de aangepaste code worden gemaakt.

***Mijn JavaScript geeft fouten in de aangepaste code weer.***

Voor inline JavaScript die geen geldig JavaScript is, worden fouten in de aangepaste code weergegeven.

***Ik kan een wijziging in mijn aangepaste code niet ongedaan maken.***

Ongedaan maken wordt momenteel niet ondersteund voor het bewerken en verwijderen van handelingen vanuit het deelvenster Wijzigingen en in aangepaste code. Als u een van deze bewerkingen ongedaan maakt, kan de ervaring in de VEC inconsistent lijken met de werkelijke acties die zichtbaar zijn in de aangepaste code. De acties in de aangepaste code hebben echter de juiste status en hebben geen invloed op de levering. Dit is een UI-probleem. Als u de ervaring wilt vernieuwen, slaat u deze op en opent u deze opnieuw. U kunt ook naar de volgende stap gaan en terugkeren. Bij een van deze handelingen wordt de ervaring opnieuw geladen en wordt de weergave zoals verwacht weergegeven. Deze handeling is consistent met de handelingen in het deelvenster Wijzigingen.

**De code van de douane veroorzaakt niet de verwachte resultaten in Internet Explorer 8.**

Doel biedt geen ondersteuning meer voor IE8.
