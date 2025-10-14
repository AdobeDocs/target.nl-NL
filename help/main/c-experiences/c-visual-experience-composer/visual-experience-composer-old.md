---
keywords: composer voor visuele ervaring;vec;wysiwyg
description: Leer de grondbeginselen van het gebruiken van Visual Experience Composer (VEC) in Adobe Target. VEC is een redacteur van WYSIWYG die u gemakkelijk individuele ervaringen laat creëren.
title: Hoe gebruik ik de Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 0%

---

# Visual Experience Composer (VEC)

Informatie over het gebruik van [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] .

VEC is een gebruikersinterface van WYSIWYG waarmee u gemakkelijk persoonlijke ervaringen en aanbiedingen in de context van de site kunt maken en testen. U kunt ervaringen en aanbiedingen voor doelactiviteiten maken door te slepen en neer te zetten, te wisselen en de lay-out en inhoud van een webpagina (of aanbieding) of mobiele webpagina te wijzigen.

De VEC is een van de belangrijkste kenmerken van [!DNL Adobe Target] . Met VEC kunnen marketers en ontwerpers inhoud maken en wijzigen via een visuele interface. Veel ontwerpkeuzes kunnen worden gemaakt zonder dat de code rechtstreeks moet worden bewerkt. HTML en JavaScript kunnen ook worden bewerkt met behulp van de bewerkingsopties in de composer.

Op het tabblad Doel **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** kunt u de URL van de standaardcomposer voor visuele ervaring invoeren.

![&#x200B; StandaardVEC URL montages &#x200B;](/help/main/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Deze URL bepaalt waar u begint wanneer u VEC opent. Als u geen standaardwaarde opgeeft, begint u met een lege pagina wanneer u de editor opent en geeft u op dat moment een URL op.

>[!NOTE]
>
>Bepaalde browsers, zoals Firefox, kunnen voorkomen dat een pagina in de VEC wordt weergegeven als de pagina gemengde inhoud bevat (bijvoorbeeld een niet-beveiligde pagina op een beveiligde site). Als de pagina niet wordt weergegeven, klikt u op het pictogram naast de URL in de adresbalk van de browser en klikt u op **[!UICONTROL Disable protection on this page]** . Dit probleem heeft geen invloed op de weergave van uw pagina&#39;s aan sitebezoekers.

Inhoud in een iframe op de pagina kan niet worden gewijzigd in de VEC. Als u de inhoud in een iframe wilt bewerken, moet u ervoor zorgen dat het iframe-document is ingeschakeld en moet u die iframe-URL vervolgens in de VEC laden.

U kunt de vervolgkeuzemenu&#39;s boven aan de pagina gebruiken om de pagina zo te bekijken dat deze bij verschillende doelgroepen of met verschillende ervaringen wordt weergegeven. U kunt een naam opgeven voor elke ervaring in de tweede vervolgkeuzelijst. Als u bijvoorbeeld de locatie van de koppeling Home op de navigatiebalk test, kunt u een ervaring benoemen waarin de koppeling Home eerst wordt weergegeven, bijvoorbeeld &quot;Koppeling Start&quot;, zodat u gemakkelijker de ervaringen in de lijst kunt identificeren.

>[!NOTE]
>
>Wijzigingen in de structuur van een pagina die van invloed zijn op de locaties die worden gebruikt in een activiteit die op die pagina is gemaakt, kunnen problemen veroorzaken met het bewerken van ervaringen. Als een locatie buiten de VEC is gewijzigd, kan Target mogelijk niet de locatie vinden waar de inhoud is gewijzigd.

Terwijl u de muis over de pagina beweegt, volgt er een contextgevoelig vak de cursor, waarin de elementen op de pagina worden gemarkeerd.

![&#x200B; VEC benadrukte &#x200B;](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Klik op het pictogram **[!UICONTROL Overlays]** om de manier te wijzigen waarop de markering wordt weergegeven. U kunt bijvoorbeeld alleen afbeeldingen, koppelingen, regionale kaders, wijzigingen of JavaScript markeren. U kunt de kleur van de markering wijzigen. U kunt ook een markeerkleur en een type vulling opgeven waarmee verschillende elementtypen worden gemarkeerd.

![&#x200B; de montages van de Bedekking van de Verandering &#x200B;](/help/main/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Klik op een gemarkeerd element voor een menu met opties die beschikbaar zijn voor dat elementtype. U kunt bijvoorbeeld op een afbeelding klikken en **[!UICONTROL Edit > Text/HTML]** selecteren om de tekst te wijzigen, of op een knop klikken en de achtergrondkleur wijzigen. Met de knoppen linksboven op de pagina kunt u de overlays in- en uitschakelen.

U kunt ook op **[!UICONTROL Browse]** klikken, naar een pagina navigeren die beschikbaar is op de primaire pagina, zoals een verzendpagina of winkelwagentje, en wijzigingen op die pagina testen. U kunt ook pagina-elementen openen die beschikbaar zijn wanneer u de muisaanwijzer houdt, zoals vervolgmenu&#39;s en mini-carts. Wanneer u klaar bent met bladeren naar de pagina, klikt u op **[!UICONTROL Compose]** om de ervaring te bewerken. U kunt bijvoorbeeld het ontwerp van een keuzelijst met winkelwagentjes of een carrousel met afbeeldingen wijzigen.

>[!NOTE]
>
>Als een aanwijsstatus afhankelijk is van JavaScript, moet u ervoor zorgen dat **[!UICONTROL Disable JavaScript]** niet is geselecteerd. JavaScript moet zijn ingeschakeld om JavaScript-elementen te bewerken.

Voor informatie over de opties beschikbaar in VEC, zie {de Opties van Composer van 0} Visuele Ervaring [.](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81)

U kunt enkele wijzigingen op een pagina uitvoeren terwijl de pagina wordt geladen (of nadat de pagina niet is geladen), of u kunt het laden van de pagina in de VEC annuleren. Zie voor meer informatie:

* [Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen](#loading)
* [Het laden van een pagina in de VEC annuleren](#cancel-loading)

## Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen {#loading}

U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel).

Enkele redenen waarom u toegang wilt hebben tot een pagina of wijzigingen wilt aanbrengen in een pagina terwijl deze wordt geladen in de VEC of nadat het laden is mislukt:

* U wilt een eenvoudige wijziging aanbrengen in een pagina, zoals het toevoegen van aangepaste code of het wijzigen van de naam van een ervaring
* U wilt bestaande aangepaste code kopiëren van een pagina die niet meer toegankelijk is
* U weet dat een pagina niet wordt geladen in de VEC, maar u wilt toch eenvoudige bewerkingen uitvoeren

Terwijl de pagina wordt geladen (of nadat deze niet is geladen), zijn het deelvenster [!UICONTROL Experiences] , [!UICONTROL Modifications] en de instellingen boven aan de ervaring (Bedekkingen, Wijzigingen, Configureren enzovoort) allemaal toegankelijk.

In de volgende afbeelding ziet u dat u aangepaste code kunt invoegen of andere handelingen kunt uitvoeren terwijl de pagina nog steeds wordt geladen:

![&#x200B; het laden van de Pagina &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Het laden van een pagina in de VEC annuleren {#cancel-loading}

U kunt het laden van een pagina in VEC annuleren om het bewerken van de activiteit te ontgrendelen zonder te wachten tot de pagina is geladen. Met deze functie bespaart u tijd en kunt u eenvoudige bewerkingen uitvoeren of aangepaste code efficiënter invoegen zonder te wachten tot de pagina in de VEC is geladen.

Enkele redenen waarom u het laden van pagina&#39;s in de VEC wilt annuleren, zijn:

* U wilt kleine wijzigingen aanbrengen in bestaande wijzigingen
* U wilt een of meer bestaande wijzigingen verwijderen
* U wilt aangepaste code invoegen of bewerken
* U hebt per ongeluk de onjuiste URL voor de pagina ingevoerd
* U wilt JavaScript in- of uitschakelen voordat u de pagina in de VEC laadt
* U wilt meer testregels voor sjablonen toevoegen aan de criteria voor het leveren van pagina&#39;s
* Als u een pagina via de EEG laadt, is het mogelijk dat het laden van een pagina per pagina afhankelijk is van het verschil tussen pagina&#39;s

Nadat u het laden van de pagina in VEC hebt geannuleerd, kunt u schakelen tussen ervaringen in de activiteit zonder te wachten tot de pagina is geladen. Als u de pagina weer wilt zien in de VEC, moet u op de knop **[!UICONTROL Reload]** klikken.

>[!IMPORTANT]
>
>Houd er rekening mee dat wanneer aangepaste code of wijzigingen worden aangebracht, u ervoor moet zorgen dat de codering of wijzigingen correct worden uitgevoerd door het laden in de VEC te annuleren. Zorg ervoor dat u juiste QA uitvoert om ervoor te zorgen dat uw douanecode en om het even welke andere wijzigingen worden geleverd zoals verwacht.

Als u het laden van een pagina in de VEC wilt annuleren, klikt u op de knop **[!UICONTROL Cancel Loading]** terwijl de pagina wordt geladen. De pagina wordt tijdens de huidige bewerkingssessie niet in de VEC voor deze activiteit geladen.

![&#x200B; annuleert het Laden knoop &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Als u ervaringen met de huidige activiteit wilt blijven beheren of nieuwe wijzigingen wilt toevoegen, klikt u op de knop **[!UICONTROL Reload]** .

![&#x200B; opnieuw laden knoop &#x200B;](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### De visuele Composer van de Ervaring (1 van 2) (7 :17) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

* De inhoud van een pagina wijzigen
* De lay-out van een pagina wijzigen

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### De visuele Composer van de Ervaring (2 van 2) (7 :29) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### De uren van het bureau: De visuele Laag van de Ervaring Composer ![&#x200B; van de Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video is een opname van &quot; [&#x200B; Uren van het Bureau &#x200B;](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7),&quot;een initiatief dat door het team van de Zorg van de Klant van Adobe wordt geleid.

* Hoe werkt VEC
* Hoe te vermijden gemeenschappelijke kwesties met VEC
* Werk-rond praktijken u met VEC kunt gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/20784/)
