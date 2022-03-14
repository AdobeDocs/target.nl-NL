---
keywords: composer voor visuele ervaring;vec;wysiwyg
description: Learn the basics of using the Visual Experience Composer (VEC) in Adobe Target. VEC is een redacteur WYSIWYG die u gemakkelijk gepersonaliseerde ervaringen laat tot stand brengen.
title: Hoe gebruik ik de Visual Experience Composer (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 51650f2a-1f24-40c7-8692-77f55656b4f6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1375'
ht-degree: 0%

---

# Visual Experience Composer (VEC)

Informatie over het gebruik van de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].

VEC is een WYSIWYG gebruikersinterface die u gemakkelijk gepersonaliseerde ervaringen en aanbiedingen in de plaatscontext kunt creëren en testen. You can create experiences and offers for Target activities by dragging and dropping, swapping, and modifying the layout and content of a web page (or offer) or mobile web page.

De VEC is een van de belangrijkste kenmerken van [!DNL Adobe Target]. Met VEC kunnen marketers en ontwerpers inhoud maken en wijzigen via een visuele interface. Veel ontwerpkeuzes kunnen worden gemaakt zonder dat de code rechtstreeks moet worden bewerkt. U kunt HTML en JavaScript ook bewerken met de bewerkingsopties in de composer.

Op het doel **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** kunt u de URL van de standaardcomposer voor visuele ervaring invoeren.

![Standaard VEC URL-instellingen](/help/main/c-experiences/c-visual-experience-composer/assets/pref-default-url-new.png)

Deze URL bepaalt waar u begint wanneer u VEC opent. Als u geen gebrek ingaat, dan begint u met een lege pagina wanneer u de redacteur opent, en specificeert een URL op dat ogenblik.

>[!NOTE]
>
>Bepaalde browsers, zoals Firefox, kunnen voorkomen dat een pagina in de VEC wordt weergegeven als de pagina gemengde inhoud bevat (bijvoorbeeld een niet-beveiligde pagina op een beveiligde site). Als de pagina niet wordt weergegeven, klikt u op het pictogram naast de URL in de adresbalk van de browser en klikt u op **[!UICONTROL Disable protection on this page]**. Dit probleem heeft geen invloed op de weergave van uw pagina&#39;s aan sitebezoekers.

Inhoud in een iframe op de pagina kan niet worden gewijzigd in de VEC. To edit content within an iframe, ensure that the iframe document is Target-enabled, then load that iframe URL in the VEC.

U kunt de vervolgkeuzemenu&#39;s boven aan de pagina gebruiken om de pagina zo te bekijken dat deze bij verschillende doelgroepen of met verschillende ervaringen wordt weergegeven. U kunt een naam opgeven voor elke ervaring in de tweede vervolgkeuzelijst. For example, if you are testing the location of the Home link in your nav bar, you might name an experience where the Home link appears first something like, &quot;Home link&quot; to make it easier to identify the experiences in the list.

>[!NOTE]
>
>Wijzigingen in de structuur van een pagina die van invloed zijn op de locaties die worden gebruikt in een activiteit die op die pagina is gemaakt, kunnen problemen veroorzaken met het bewerken van ervaringen. Als een locatie buiten de VEC is gewijzigd, kan Target mogelijk niet de locatie vinden waar de inhoud is gewijzigd.

As you move your mouse around the page, a context-sensitive box follows the cursor, highlighting the elements on the page.

![VEC gemarkeerd](/help/main/c-experiences/c-visual-experience-composer/assets/vec-highlight-new.png)

Klik op de knop **[!UICONTROL Overlays]** om de manier te wijzigen waarop de markering wordt weergegeven. U kunt bijvoorbeeld alleen afbeeldingen, koppelingen, regionale vakken, wijzigingen of JavaScript markeren. U kunt de kleur van de markering wijzigen. You can also specify a highlight color and type of fill used to highlight different element types.

![Change Overlay settings](/help/main/c-experiences/c-visual-experience-composer/assets/change-overlay.png)

Click a highlighted element for a menu of options available for that element type For example, you can click on an image and select **[!UICONTROL Edit > Text/HTML]** to change the text, or click a button and change the background color. Met de knoppen linksboven op de pagina kunt u de overlays in- en uitschakelen.

You can also click **[!UICONTROL Browse]**, then navigate to a page that is available from the primary page, such as a shipping page or shopping cart, and test changes on that page. U kunt ook pagina-elementen openen die beschikbaar zijn wanneer u de muisaanwijzer houdt, zoals vervolgmenu&#39;s en mini-carts. Als u klaar bent met bladeren naar de pagina, klikt u op **[!UICONTROL Compose]** om de ervaring te bewerken. U kunt bijvoorbeeld het ontwerp van een keuzelijst met winkelwagentjes of een carrousel met afbeeldingen wijzigen.

>[!NOTE]
>
>Als een aanwijsstatus afhankelijk is van JavaScript, controleert u of **[!UICONTROL Disable JavaScript]** is niet geselecteerd. JavaScript moet zijn ingeschakeld om JavaScript-elementen te bewerken.

Voor informatie over de opties beschikbaar in VEC, zie [Opties voor composer visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81).

U kunt enkele wijzigingen op een pagina uitvoeren terwijl de pagina wordt geladen (of nadat de pagina niet is geladen), of u kunt het laden van de pagina in de VEC annuleren. Zie voor meer informatie:

* [Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen](#loading)
* [Het laden van een pagina in de VEC annuleren](#cancel-loading)

## Een pagina bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen {#loading}

U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel).

Enkele redenen waarom u toegang wilt hebben tot een pagina of wijzigingen wilt aanbrengen in een pagina terwijl deze wordt geladen in de VEC of nadat het laden is mislukt:

* You want to make a simple modification to a page, such as to add custom code or change an experience&#39;s name
* U wilt bestaande aangepaste code kopiëren van een pagina die niet meer toegankelijk is
* U weet dat een pagina niet wordt geladen in de VEC, maar u wilt toch eenvoudige bewerkingen uitvoeren

While the page loads (or after it fails to load), the [!UICONTROL Experiences] panel, [!UICONTROL Modifications] panel, and the settings at the top of the experience (Overlays, Modifications, Configure, and so forth) are all accessible.

In de volgende afbeelding ziet u dat u aangepaste code kunt invoegen of andere handelingen kunt uitvoeren terwijl de pagina nog steeds wordt geladen:

![Pagina laden](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/loading-page.png)

## Cancel loading of a page within the VEC {#cancel-loading}

U kunt het laden van een pagina in VEC annuleren om het bewerken van de activiteit te ontgrendelen zonder te wachten tot de pagina is geladen. Met deze functie bespaart u tijd en kunt u eenvoudige bewerkingen uitvoeren of aangepaste code efficiënter invoegen zonder te wachten tot de pagina in de VEC is geladen.

Enkele redenen waarom u het laden van pagina&#39;s in de VEC wilt annuleren, zijn:

* You want to make minor edits to existing modifications
* U wilt een of meer bestaande wijzigingen verwijderen
* U wilt aangepaste code invoegen of bewerken
* U hebt per ongeluk de onjuiste URL voor de pagina ingevoerd
* U wilt JavaScript in- of uitschakelen voordat u de pagina in de VEC laadt
* U wilt meer testregels voor sjablonen toevoegen aan de criteria voor het leveren van pagina&#39;s
* Als u een pagina via de EEG laadt, is het mogelijk dat het laden van een pagina per pagina afhankelijk is van het verschil tussen pagina&#39;s

Nadat u het laden van de pagina in VEC hebt geannuleerd, kunt u schakelen tussen ervaringen in de activiteit zonder te wachten tot de pagina is geladen. Als u de pagina weer wilt weergeven in de VEC, klikt u op de knop **[!UICONTROL Reload]** knop.

>[!IMPORTANT]
>
>Houd er rekening mee dat wanneer aangepaste code of wijzigingen worden aangebracht, u ervoor moet zorgen dat de codering of wijzigingen correct worden uitgevoerd door het laden in de VEC te annuleren. Zorg ervoor dat u juiste QA uitvoert om ervoor te zorgen dat uw douanecode en om het even welke andere wijzigingen worden geleverd zoals verwacht.

Als u het laden van een pagina in de VEC wilt annuleren, klikt u op de knop **[!UICONTROL Cancel Loading]** terwijl de pagina wordt geladen. De pagina wordt tijdens de huidige bewerkingssessie niet in de VEC voor deze activiteit geladen.

![Cancel Loading button](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/cancel-loading.png)

Als u ervaringen in de huidige activiteit wilt blijven beheren of nieuwe wijzigingen wilt toevoegen, klikt u op de knop **[!UICONTROL Reload]** knop.

![Knop Opnieuw laden](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/assets/reload-in-vec.png)

>[!NOTE]
>
>There is a current known issue with this feature that will be fixed in the next release. Zie &quot;Het laden van een pagina in de VEC annuleren&quot; op de pagina [Bekende problemen en opgeloste problemen](/help/main/r-release-notes/known-issues-resolved-issues.md#cancel) pagina.

## Training videos

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Visual Experience Composer (1 van 2) (7:17) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

* De inhoud van een pagina wijzigen
* De lay-out van een pagina wijzigen

>[!VIDEO](https://video.tv.adobe.com/v/17399)

### Visual Experience Composer (2 of 2) (7:29) ![Tutorial badge](/help/main/assets/tutorial.png)

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Office hours: Visual Experience Composer ![Tutorial badge](/help/main/assets/tutorial.png)

This video is a recording of &quot; [Office Hours](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7),&quot; an initiative led by the Adobe Customer Care team.

* Hoe werkt VEC
* Hoe te vermijden gemeenschappelijke kwesties met VEC
* Werk-rond praktijken u met VEC kunt gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/20784/)
