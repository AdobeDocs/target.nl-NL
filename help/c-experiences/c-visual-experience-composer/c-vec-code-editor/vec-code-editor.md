---
keywords: css selector;custom code;code editor;Mobile Web Experience Editor
description: Informatie over de pagina Wijzigingen waarmee u wijzigingen op de pagina kunt bekijken en aanvullende wijzigingen (CSS-kiezer, Mbox en Aangepaste code) kunt toevoegen.
title: Wijzigingen
feature: vec
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '2068'
ht-degree: 0%

---


# Wijzigingen{#modifications}

Informatie over de pagina Wijzigingen waarmee u wijzigingen op de pagina kunt bekijken en aanvullende wijzigingen (CSS-kiezer, Mbox en Aangepaste code) kunt toevoegen.

De pagina van Wijzigingen toont alle veranderingen die aan uw pagina in Visuele Composer van de Ervaring (VEC) zijn aangebracht en laat u extra veranderingen aanbrengen door elk element op de pagina te klikken en een actie [te](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81)selecteren. Elke wijziging die u aanbrengt, wordt als een afzonderlijke actie of als een afzonderlijk element in de [!UICONTROL Modifications] lijst weergegeven. U kunt ook wijzigingen toevoegen, zoals de volgende wijzigingstypen: CSS-kiezer, Mbox. en Aangepaste code.

## Overzicht van wijzigingen {#section_EE27E7572AA74397BBDED563B2B3D509}

Op de [!UICONTROL Modifications] pagina staan alle wijzigingen die in de VEC op uw pagina zijn aangebracht. Elke wijziging die u aanbrengt, wordt als een afzonderlijke actie of als een afzonderlijk element in de [!UICONTROL Modifications] lijst weergegeven.

![](assets/codeeditor_page_mods.png)

Gebruik de pagina van Wijzigingen om kleine veranderingen in selecteur aan te brengen die het Doel kiest wanneer u VEC gebruikt om te vormen hoe de inhoud wordt geleverd. U kunt de inhoud of een HTML-kenmerk wijzigen. U kunt de code ook bewerken om het equivalent van een HTML-aanbieding in een box te maken.

Met de pagina Wijzigingen kunt u:

* Bekijk een handeling die in de visuele composer is uitgevoerd.

   ![](assets/codeeditor_viewchange.png)

* Bewerk een bestaande handeling. Houd de muisaanwijzer boven de gewenste wijziging en klik op het **[!UICONTROL Edit]** pictogram.

   ![](assets/codeeditor_edit.png)

   Breng de gewenste wijzigingen aan.

   ![](assets/codeeditor_changechange1.png)

* Een bestaande handeling verwijderen. Houd de muisaanwijzer boven de gewenste wijziging en klik op het **[!UICONTROL Delete]** pictogram.

   ![](assets/codeditor_delete.png)

* Voeg een nieuwe wijziging toe. Klik op **[!UICONTROL Add Modification]** of het pictogram + en geef de wijzigingen op zoals hieronder beschreven.

   ![](assets/codeeditor_new.png)

   Nadat één wijziging is gemaakt, wordt boven in het deelvenster Wijzigingen een pictogram + weergegeven in plaats van de knop Wijziging toevoegen onder in het deelvenster.

* Koppel het deelvenster Wijzigingen verticaal langs de zijkant van de doelinterface of horizontaal onder aan het venster. Klik op het [!UICONTROL Dock] pictogram om te schakelen tussen de twee instellingen.

   ![](assets/codeditor_dock.png)

   In het volgende voorbeeld ziet u het deelvenster Wijzigingen dat aan de onderkant van het scherm is gekoppeld:

   ![](assets/codeeditor_dock_bottom.png)

## Wijzigingen toevoegen {#section_C7ABCD5731A048CB8F90EDC31A32EDF9}

1. Als u de [!UICONTROL Modifications] pagina voor een geselecteerde ervaring wilt weergeven, klikt u in de VEC op het pictogram **[!UICONTROL Modifications]** &lt;/>.

   ![](assets/codeeditor_icon_big.png)

   >[!NOTE]
   >
   >Als u het deelvenster Wijzigingen wilt openen in de Form-based Experience Composer, maakt of bewerkt u een HTML-aanbieding. Zie Op [formulier gebaseerde Experience Composer](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)voor meer informatie.

   De [!UICONTROL Modifications] pagina wordt geopend, waarbij het scherm wordt gesplitst tussen de visuele modus aan de linkerkant en het deelvenster Wijzigingen aan de rechterkant. Klik op het [!UICONTROL Dock] pictogram om het deelvenster Wijzigingen verticaal langs de zijde van de doelinterface of horizontaal onder aan het venster te koppelen. U ziet dat de ervaring A in de volgende afbeelding geen eerdere wijzigingen heeft ondergaan.

   ![](assets/codeeditor_page.png)

   De ervaring B toont de vorige wijzigingen in het [!UICONTROL Modifications] paneel op het recht.

   ![](assets/codeeditor_page_mods.png)

1. Een wijziging toevoegen:

   * Als er geen vorige wijzigingen in de ervaring zijn aangebracht, klikt u op de **[!UICONTROL Add Modification]** knop onder aan het [!UICONTROL Modifications] deelvenster aan de rechterkant.
   * Als er vorige wijzigingen zijn aangebracht in de ervaring, klikt u op het pictogram + boven in het [!UICONTROL Modifications] deelvenster aan de rechterkant.

   In het deelvenster Wijzigingen wordt het volgende weergegeven:

   ![](assets/codeeditor_page_mods_add.png)

1. Kies het gewenste type in de **[!UICONTROL Modifications Type]** vervolgkeuzelijst:

   | Type wijzigingen | Details |
   |--- |--- |
   | CSS-kiezer | Geef in het vak CSS-elementkiezer het gewenste CSS-element op dat u wilt wijzigen, selecteer een handelingstype (Inhoud instellen of Kenmerk instellen) en vul vervolgens de vereiste informatie en de gewenste inhoud in. |
   | Mbox | Geef de naam van de box en de gewenste inhoud op. |
   | Aangepaste code | Geef een optionele naam op, schakel het selectievakje [!UICONTROL Add Code in the `<HEAD>` Sectie] naar wens in of uit en voeg uw aangepaste code toe.<br>Als u [!UICONTROL Add Code in the `<HEAD>` Sectie]selecteert, wordt de douanecode toegevoegd aan de `<head>` sectie en zijn uitvoering wacht niet op lichaam of pagina-lading gebeurtenissen. Alleen `<script>` en `<style>` elementen toevoegen. Als u `<div>` tags en andere elementen toevoegt, komen de resterende `<head>` elementen mogelijk in de pop-up terecht `<body>`. Als u mbox.js versie 60 of recenter of om het even welke versie van at.js gebruikt, zullen alle aanbiedingen asynchroon leveren.<br> Als u de optie [!UICONTROL Add Code in the `<HEAD>` Sectie]uitschakelt, wordt de aangepaste code direct na de `<body>` tag uitgevoerd. Plaats alle code in één code om de DOM-structuur `<div>` te behouden. Als u mbox.js versie 60 of recenter of om het even welke versie van at.js gebruikt, zullen alle aanbiedingen asynchroon leveren.<br>**Opmerking**: Scripts worden asynchroon uitgevoerd. Dit betekent dat u bijvoorbeeld geen scriptmethoden kunt gebruiken `document.write` of gebruiken.<br>De code van de douane verstrekt een niet visuele interface aan mening, geeft uit en voegt nieuwe acties binnen VEC, op vorm-gebaseerde Composer van de Ervaring toe, en HTML biedt redacteur aan. Het paneel verstrekt een codemening van een ervaring om u te helpen complexere ervaringen bouwen, bestaande ervaringen verfijnen, en kwesties problemen oplossen.<br>Aangepaste code is bedoeld voor geavanceerde gebruikers die vertrouwd zijn met HTML, JavaScript en CSS. De codeweergave kan u helpen wijzigingen aan te passen of te perfectioneren, of selecteurproblemen te verhelpen. Deze kan ook worden gebruikt om nieuwe aangepaste code en handelingen toe te voegen. U kunt meerdere aangepaste code toevoegen en elke aangepaste code optioneel een naam geven.<br>**Opmerking**: De aangepaste code is momenteel alleen beschikbaar voor activiteiten van het type A/B en Experience Targeting (XT). Aangepaste code is uitgeschakeld voor overlay en als een omleidingsvoorstel wordt toegepast.<br>De code van de douane steunt de volgende gebruiksgevallen:<ul><li>Aangepaste JavaScript, HTML of CSS toevoegen die boven aan de pagina moet worden uitgevoerd</li><li>De code weergeven of bewerken die door VEC wordt gegenereerd nadat wijzigingen zijn aangebracht</li><li>HTML-inhoud instellen voor een kiezer (alleen CSS-kiezers)</li><li>Een kenmerk instellen op een HTML-element</li><li>Aanbiedingsinhoud toevoegen die in een regionale box moet worden geleverd</li><li>Omwisselen op DOM-gereed met jQuery</li><li>Wisselen op DOM-klaar, geen jQuery (ondersteunt Internet Explorer 8 niet)</li><li>Wisselen met DOM-polling via &quot;elementOnLoad&quot;-plug-in</li><li>Aangepaste omleiding</li></ul>Aangepaste code biedt:<ul><li>Regelnummers voor betere bruikbaarheid.</li><li>Syntaxis markeren om onjuiste syntaxis voor HTML-aanbiedingen te voorkomen.</li><li>De mogelijkheid om meerdere aangepaste codes te maken en voor elke code een optionele naam op te geven. Door meerdere aangepaste codes te maken, kunt u in de toekomst gemakkelijker fouten opsporen. In plaats van bijvoorbeeld één aangepaste code te maken om verschillende wijzigingen door te voeren, kunt u voor elke wijziging een aparte aangepaste code met een beschrijvende naam maken. Als u afzonderlijke aangepaste codes hebt, kunt u uw wijzigingen modulair en beter beheren. Merk op dat de uitvoering van veelvoudige douanecodes in een activiteit niet gewaarborgd is om in de opeenvolging te gebeuren waarin zij werden gecreeerd.</li></ul>In het deelvenster Wijzigingen wordt het scherm opgesplitst tussen de visuele modus en de codemodus. Beide modi blijven gesynchroniseerd. Elke visueel aangebrachte wijziging heeft een overeenkomstige rij in de codemening. Op dezelfde manier elke verandering die in de codemening wordt begaan toont in de visuele ervaring. Wanneer u op een rij in de codeweergave klikt, wordt het bijbehorende element op de visuele pagina geselecteerd.<br>Aangepaste code ondersteunt HTML, scripts en stijlen. U kunt elke geldige HTML-code of elk geldig script toevoegen of bewerken. |

1. Voeg desgewenst aanvullende wijzigingen toe.

## Aangepaste praktijkgevallen voor code {#section_26CB3360097D400FB02E20AE5FDBA352}

Het **[!UICONTROL Custom Code]** deelvenster bevat code die wordt uitgevoerd aan het begin van het laden van de pagina.

U kunt de JavaScript-code in de `<head>` tag uitvoeren. De uitvoering van code wacht niet tot de `<body>` tag aanwezig is in het DOM.

Kiezers voor volgende visuele handelingen zijn afhankelijk van de HTML-elementen die op dit tabblad zijn toegevoegd.

Het deelvenster Aangepaste code wordt vaak gebruikt om JavaScript of CSS boven aan de pagina toe te voegen.

![](assets/codeeditor_custom.png)

Gebruik de **[!UICONTROL Custom Code]** tab om:

* JavaScript inline gebruiken of koppelen naar een extern JavaScript-bestand

   Bijvoorbeeld om de kleur van een element te wijzigen:

   ```
   <script type="text/javascript"> 
   document.getElementById("element_id").style.color = "blue"; 
   </script> 
   ```

* Een stijl inline configureren of koppelen naar een externe stijlpagina

   U kunt bijvoorbeeld een klasse definiëren voor een overlay-element:

   ```
   <style> 
   .overlay 
   { position: absolute; top:0; left: 0; right: 0; bottom: 0; background: red; } 
   </style> 
   ```

* HTML-fragmenten toevoegen om nieuwe elementen te definiëren

   Gebruik bijvoorbeeld het volgende HTML-fragment om een overlay te maken `<div>` met de hierboven gedefinieerde CSS-klasse:

   ```
   <div class="overlay"></div>
   ```

* Omwisselen op DOM-gereed met jQuery

   ```
   <style>#default_content {visibility:hidden;}</style> 
   <script> 
   jQuery( document ).ready(function() { 
       jQuery("#default_content").html( "<span style='color:red'>Hello <strong>Again</strong></span>" ); 
       jQuery("#default_content").css("visibility","visible"); 
   }); 
   </script> 
   ```

* Wisselen op DOM-gereed, geen jQuery (ondersteunt Internet Explorer 8 niet)

   ```
   <style>#default_content {visibility:hidden;}</style> 
   <script> 
   document.addEventListener("DOMContentLoaded", function(event) {  
       document.getElementById("default_content").innerHTML = "<span style='color:red'>Hello <strong>Again</strong></span>"; 
       document.getElementById("default_content").style.visibility="visible"; 
   }); 
   </script> 
   ```

* Wisselen met DOM-opiniepeiling via `elementOnLoad` plug-in

   Het voordeel hiervan is dat de swap eerder plaatsvindt dan op DOM-gereed. De insteekmodule handelt het vooraf verbergen en tonen af en vereist een id op het element.

   ```
   <style>#default_content {visibility:hidden;}</style> 
   <script> 
   /*elementOnLoad DOM Swizzling v3 ==>Mbox.js Extra Javascript*/window.elementOnLoad=function(e,l){var m=document.getElementById(e);if(m){setTimeout(function(){l(m);setTimeout(function(){m.style.visibility='visible';m.style.display='block'},20)},20)}else{setTimeout(function(){elementOnLoad(e,l)},20)}},addEvent=function(a){var d=document,w=window,wa=w.addEventListener,da=d.addEventListener,e='load',o='on'+e;if(wa){wa(e,a,false)}else if(da){da(e,a,false)}else if(d.attachEvent){w.attachEvent(o,a)}};addEvent(function(){setTimeout("elementOnLoad=function(){}",500)}); 
   elementOnLoad('default_content',function(e){ 
       e.innerHTML = "<span style='color:red'>Hello <strong>Again</strong></span>"; 
   }); 
   </script> 
   ```

* Aangepaste omleiding door bestaande params, `s_tnt` param (voor verouderde integratie naar Analytics), verwijzerparam, en mbox zitting

   ```
   <style type="text/css">body{display:none!important;}</style> 
   <script type="text/javascript"> 
    var qs='';window.location.search?qs=window.location.search+'&':qs='?'; 
    window.location.replace('//www.mywebsite.com/'+qs+'s_tnt=${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}&s_tntref='+encodeURIComponent(document.referrer)+'&mboxSession='+mboxFactoryDefault.getSessionId().getId()+''+window.location.hash+''); 
   </script> 
   ```

* Voeg Adobe Target Experience Templates toe voor gebruik in aangepaste code. De Malplaatjes van de Ervaring van het doel zijn vooraf gecodeerde steekproeven met configureerbare input die moeten worden gebruikt om gemeenschappelijke telleruse-cases uit te voeren. Deze ervaringssjablonen worden gratis aan ontwikkelaars en marketers aangeboden als uitgangspunt voor het uitvoeren van veelvoorkomende gebruiksgevallen, hetzij via de VEC of de Form-based Experience Composer. Gebruiksgevallen zijn onder andere lichtbakken, carrousels, aftellingen en meer.

   Voor meer informatie, zie de Malplaatjes van de [Ervaring](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652).

## Aangepaste aanbevolen procedures voor code {#section_10DFFD9FB92A43C1BB444A45E0272B28}

**Plaats de aangepaste code altijd in één element.**

Bijvoorbeeld:

```
<div id="custom-code"> 
// My Code goes here 
</div>
```

Breng wijzigingen aan in deze container als er wijzigingen nodig zijn.

Als u de aangepaste code niet meer nodig hebt, laat u deze container leeg, maar verwijdert u deze niet. Dit zorgt ervoor dat andere ervaringswijzigingen niet worden beïnvloed.

**Gebruik de element-id &#39;CDQID&#39; niet voor wijzigingen aan de pagina die in de Code-editor is gemaakt.**

Het doel past een nieuwe elementidentiteitskaart met de waarde &quot;CDQID&quot;op om het even welk element op de pagina toe die door Doel wordt gewijzigd. Omdat deze id door Doel wordt toegepast, zou het niet voor enige verdere wijzigingen of aanpassingen in de Redacteur van de Code moeten worden gebruikt.

**Voer geen document.write acties in de manuscripten van de douanecode uit.**

Scripts worden asynchroon uitgevoerd. Hierdoor worden `document.write` handelingen vaak op de verkeerde plaats op de pagina weergegeven. Het gebruik `document.write` in scripts die in aangepaste code zijn gemaakt, wordt afgeraden.

**Als u een element maakt en het vervolgens wijzigt, verwijdert u het oorspronkelijke element niet.**

Bij elke wijziging wordt een nieuw element gemaakt in het deelvenster Wijzigingen. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft die actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer. Zie &quot;Problemen oplossen&quot; hieronder voor meer informatie.

**Wees voorzichtig als u de aangepaste codefunctie gebruikt voor twee activiteiten die dezelfde URL als doel hebben.**

Als u de aangepaste codefunctie gebruikt voor twee activiteiten die op dezelfde URL zijn gericht, wordt het JavaScript vanuit beide activiteiten in de pagina geïnjecteerd. Doel bepaalt automatisch de volgorde van de geleverde inhoud. Zorg ervoor dat de code niet afhankelijk is van plaatsing. Het is aan u om ervoor te zorgen dat er geen conflicten in de code zijn.

## Problemen met aangepaste code oplossen {#section_6C965CBC31C348D7AA5B57B63DAB9E7F}

**Ik heb een waarschuwing ontvangen dat een actie niet kan worden toegepast vanwege structurele wijzigingen op een pagina. Wat betekent dit?**

Dit bericht geeft aan dat de structuur van de pagina is gewijzigd sinds de activiteit voor het laatst is opgeslagen.

De ontbrekende kiezers zijn mogelijk bereikt in de modus Bladeren. We raden u aan elke ervaring te verwijderen en opnieuw te maken om ervoor te zorgen dat de inhoud er zo uitziet als u verwacht, zoals in het waarschuwingsbericht wordt aangegeven.

![](assets/code_editor_2.png)

***Als ik een element verwijder, krijg ik een waarschuwing te zien waarin staat: &quot;Het verwijderen van deze handeling kan gevolgen hebben voor vervolghandelingen.&quot; Wat betekent dit?***

Als u bijvoorbeeld twee handelingen hebt uitgevoerd:

* Een klasse toegevoegd aan Element 1
* De HTML voor Element 1 is bewerkt

Bij elke wijziging wordt een nieuw element gemaakt in het deelvenster Wijzigingen. Omdat de tweede actie Element 1 wijzigt, als u Element 1 schrapt, heeft de tweede actie niet meer om het even wat te wijzigen, zodat werkt de verandering niet meer.

Met andere woorden, als u een element met tekst toevoegt, dan in een afzonderlijke actie bewerkt u dat element met verschillende tekst, toont het paneel van Wijzigingen beide acties als afzonderlijke elementen. Wanneer u het element hebt bewerkt, hebt u een nieuw element gemaakt dat het oorspronkelijke element wijzigt dat u hebt gemaakt en dat de bewerkte tekst bevat. Als u vervolgens het oorspronkelijke element verwijdert, kan de bewerkte tekst het bewerkte element niet vinden en wordt deze niet weergegeven. Het tweede element blijft in de lijst met elementen, maar heeft geen invloed op de pagina omdat het element dat wordt gewijzigd, niet meer bestaat.

***Een element dat ik met behulp van `document.write` een script heb gemaakt, wordt niet weergegeven op de positie die ik verwacht.***

Scripts worden asynchroon uitgevoerd. Hierdoor worden `document.write` handelingen vaak op de verkeerde plaats op de pagina weergegeven. Adobe raadt u niet aan deze functie te gebruiken `document.write` in scripts die in de aangepaste code zijn gemaakt.

***Mijn JavaScript geeft fouten in de aangepaste code weer.***

Voor inline JavaScript die geen geldig JavaScript is, worden fouten in de aangepaste code weergegeven.

***Ik kan een wijziging in mijn aangepaste code niet ongedaan maken.***

Ongedaan maken wordt momenteel niet ondersteund voor het bewerken en verwijderen van handelingen vanuit het deelvenster Wijzigingen en in aangepaste code. Als u een van deze bewerkingen ongedaan maakt, kan de ervaring in de VEC inconsistent lijken met de werkelijke acties die zichtbaar zijn in de aangepaste code. De acties in de aangepaste code hebben echter de juiste status en hebben geen invloed op de levering. Dit is een UI-probleem. Als u de ervaring wilt vernieuwen, slaat u deze op en opent u deze opnieuw. U kunt ook naar de volgende stap gaan en terugkeren. Bij een van deze handelingen wordt de ervaring opnieuw geladen en wordt de weergave zoals verwacht weergegeven. Deze handeling is consistent met de handelingen in het deelvenster Wijzigingen.

**De code van de douane veroorzaakt niet de verwachte resultaten in Internet Explorer 8.**

Doel biedt geen ondersteuning meer voor IE8.
