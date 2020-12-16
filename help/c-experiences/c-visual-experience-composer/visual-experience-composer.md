---
description: Informatie over het gebruik van Visual Experience Composer (VEC) in Adobe Target.
title: Adobe Target Visual Experience Composer (VEC)
feature: vec
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1353'
ht-degree: 0%

---


# Visual Experience Composer (VEC){#visual-experience-composer-vec}

Informatie over het gebruiken van Visual Experience Composer (VEC).

VEC is WYSIWYG gebruikersinterface die u gemakkelijk gepersonaliseerde ervaringen en aanbiedingen in de plaatscontext kunt creëren en testen. U kunt ervaringen en aanbiedingen voor doelactiviteiten maken door te slepen en neer te zetten, te wisselen en de lay-out en inhoud van een webpagina (of aanbieding) of mobiele webpagina te wijzigen.

VEC is één van de belangrijkste eigenschappen van [!DNL Adobe Target]. Met VEC kunnen marketers en ontwerpers inhoud maken en wijzigen via een visuele interface. Veel ontwerpkeuzes kunnen worden gemaakt zonder dat de code rechtstreeks moet worden bewerkt. Het bewerken van HTML en JavaScript is ook mogelijk met behulp van de bewerkingsopties die beschikbaar zijn in de composer.

Op het Doel **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** lusje, kunt u de Standaard Visuele Composer URL van de Ervaring ingaan.

![Standaard VEC URL-instellingen](/help/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Deze URL bepaalt waar u begint wanneer u VEC opent. Als u geen gebrek ingaat, dan begint u met een lege pagina wanneer u de redacteur opent, en specificeert een URL op dat ogenblik.

>[!NOTE]
>
>Bepaalde browsers, zoals Firefox, kunnen voorkomen dat een pagina in de VEC wordt weergegeven als de pagina gemengde inhoud bevat (bijvoorbeeld een niet-beveiligde pagina op een beveiligde site). Als de pagina niet wordt weergegeven, klikt u op het pictogram naast de URL in de adresbalk van de browser en klikt u op **[!UICONTROL Disable protection on this page]**. Dit probleem heeft geen invloed op de weergave van uw pagina&#39;s aan sitebezoekers.

Inhoud in een iframe op de pagina kan niet worden gewijzigd in de VEC. Als u de inhoud in een iframe wilt bewerken, moet u ervoor zorgen dat het iframe-document is ingeschakeld en moet u die iframe-URL vervolgens in de VEC laden.

U kunt de vervolgkeuzemenu&#39;s boven aan de pagina gebruiken om de pagina zo te bekijken dat deze bij verschillende doelgroepen of met verschillende ervaringen wordt weergegeven. U kunt een naam opgeven voor elke ervaring in de tweede vervolgkeuzelijst. Als u bijvoorbeeld de locatie van de koppeling Home op de navigatiebalk test, kunt u een ervaring benoemen waarin de koppeling Home eerst wordt weergegeven, bijvoorbeeld &quot;Koppeling Start&quot;, zodat u gemakkelijker de ervaringen in de lijst kunt identificeren.

>[!NOTE]
>
>Wijzigingen in de structuur van een pagina die van invloed zijn op de locaties die worden gebruikt in een activiteit die op die pagina is gemaakt, kunnen problemen veroorzaken met het bewerken van ervaringen. Als een locatie buiten de VEC is gewijzigd, kan Target mogelijk niet de locatie vinden waar de inhoud is gewijzigd.

Terwijl u de muis over de pagina beweegt, volgt er een contextgevoelig vak de cursor, waarin de elementen op de pagina worden gemarkeerd.

![VEC gemarkeerd](/help/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Klik op het pictogram **[!UICONTROL Overlays]** om de manier te wijzigen waarop de markering wordt weergegeven. U kunt bijvoorbeeld alleen afbeeldingen, koppelingen, regionale vakken, wijzigingen of JavaScript markeren. U kunt de kleur van de markering wijzigen. U kunt ook een markeerkleur en een type vulling opgeven waarmee verschillende elementtypen worden gemarkeerd.

![Bedekkingsinstellingen wijzigen](/help/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Klik op een gemarkeerd element voor een menu met opties die beschikbaar zijn voor dat elementtype. U kunt bijvoorbeeld op een afbeelding klikken en **[!UICONTROL Edit > Text/HTML]** selecteren om de tekst te wijzigen, of op een knop klikken en de achtergrondkleur wijzigen. Met de knoppen linksboven op de pagina kunt u de overlays in- en uitschakelen.

U kunt ook op **[!UICONTROL Browse]** klikken en vervolgens naar een pagina navigeren die beschikbaar is op de primaire pagina, zoals een verzendpagina of winkelwagentje, en de wijzigingen op die pagina testen. U kunt ook pagina-elementen openen die beschikbaar zijn wanneer u de muisaanwijzer houdt, zoals vervolgmenu&#39;s en mini-carts. Als u klaar bent met bladeren naar de pagina, klikt u op **[!UICONTROL Compose]** om de ervaring te bewerken. U kunt bijvoorbeeld het ontwerp van een keuzelijst met winkelwagentjes of een carrousel met afbeeldingen wijzigen.

>[!NOTE]
>
>Als een aanwijsstatus afhankelijk is van JavaScript, moet **[!UICONTROL Disable JavaScript]** niet zijn geselecteerd. JavaScript moet zijn ingeschakeld om JavaScript-elementen te bewerken.

Voor informatie over de opties beschikbaar in VEC, zie [Opties van Composer van de Visuele Ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

U kunt enkele wijzigingen op een pagina uitvoeren terwijl de pagina wordt geladen (of nadat de pagina niet is geladen), of u kunt het laden van de pagina in de VEC annuleren. Zie voor meer informatie:

* [Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen](#loading)
* [Het laden van een pagina in de VEC annuleren](#cancel-loading)

## Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina {#loading} niet is geladen

U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel).

Enkele redenen waarom u toegang wilt hebben tot een pagina of wijzigingen wilt aanbrengen in een pagina terwijl deze wordt geladen in de VEC of nadat het laden is mislukt:

* U wilt een eenvoudige wijziging aanbrengen in een pagina, zoals het toevoegen van aangepaste code of het wijzigen van de naam van een ervaring
* U wilt bestaande aangepaste code kopiëren van een pagina die niet meer toegankelijk is
* U weet dat een pagina niet wordt geladen in de VEC, maar u wilt toch eenvoudige bewerkingen uitvoeren

Terwijl de pagina wordt geladen (of nadat deze niet is geladen), zijn het [!UICONTROL Experiences]-deelvenster, [!UICONTROL Modifications]-deelvenster en de instellingen boven aan de ervaring (Bedekkingen, Wijzigingen, Configureren enzovoort) allemaal toegankelijk.

In de volgende afbeelding ziet u dat u aangepaste code kunt invoegen of andere handelingen kunt uitvoeren terwijl de pagina nog steeds wordt geladen:

![Pagina laden](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Laden van een pagina in de VEC annuleren {#cancel-loading}

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

![De knop Laden annuleren](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Als u ervaringen in de huidige activiteit wilt blijven beheren of nieuwe wijzigingen wilt toevoegen, moet u op de knop **[!UICONTROL Reload]** klikken.

![Knop Opnieuw laden](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>Er is een bekend probleem met deze functie dat in de volgende release wordt opgelost. Zie &quot;Laden van een pagina in de VEC annuleren&quot; op de pagina [Bekende problemen en opgeloste problemen](/help/r-release-notes/known-issues-resolved-issues.md#cancel) voor meer informatie.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Visual Experience Composer (1 van 2) (7:17) ![Zelfstudie badge](/help/assets/tutorial.png)

* De inhoud van een pagina wijzigen
* De lay-out van een pagina wijzigen

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2 van 2) (7:29) ![Zelfstudie badge](/help/assets/tutorial.png)

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Kantooruren: Visuele-ervaringscomposer ![Zelfstudie-badge](/help/assets/tutorial.png)

Deze video is een opname van &quot; [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot;, een initiatief onder leiding van het team van de klantenservice van Adobe.

* Hoe werkt VEC
* Hoe te vermijden gemeenschappelijke kwesties met VEC
* Werk-rond praktijken u met VEC kunt gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/20784/)