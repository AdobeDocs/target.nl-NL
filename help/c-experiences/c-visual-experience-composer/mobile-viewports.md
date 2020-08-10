---
keywords: responsive;mobile viewports;viewport;devices;mobile;responsive web design;rwd
description: Met mobiele viewports kunt u een voorvertoning weergeven van uw Adobe Target-activiteiten op verschillende schermgrootten.
title: Mobiele Viewers voor responsieve ervaringen
uuid: 86a74584-4a4d-428b-9d29-f7ebdf0cef2a
translation-type: tm+mt
source-git-commit: 292c6a5f2a49e6de88778c944099f4971d8a10af
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---


# Mobiele Viewers voor responsieve ervaringen{#mobile-viewports-for-responsive-experiences}

Met de mobiele viewports kunt u een voorvertoning weergeven van uw [!DNL Target] activiteiten op schermen van verschillende formaten.

De voorvertoningsfunctie voor mobiele viewport is ontworpen voor responsieve sites die goed worden weergegeven op verschillende apparaten, vensters of schermgrootten. Responsieve sites worden automatisch aangepast en aangepast aan elke schermgrootte, zoals desktops, laptops, tablets of mobiele telefoons.

>[!NOTE]
>
> * Gebruik mobiele viewports als uw site reageert en dezelfde elementen op uw desktoppagina in een andere configuratie op uw mobiele pagina worden gebruikt. Als u een aparte mobiele site hebt met een aparte structuur, zoals `m.mysite.com`, gebruikt u een activiteit [die uit](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) meerdere pagina&#39;s bestaat.
   >
   >
* Mobiele viewports zijn niet beschikbaar als deze worden overlapt door een overlay voor omleidingsaanbiedingen.


Een viewport wordt bepaald door de grootte van de rechthoek die wordt gevuld door een webpagina op het scherm. Dit is de grootte van het browservenster, min de schuifbalken en werkbalken. Browsers gebruiken &#39;CSS-pixels&#39;. Voor veel apparaten, zoals apparaten met Retina-schermen, is de viewport kleiner dan de geadverteerde apparaatresolutie.

Hieronder staan de viewports en de resoluties voor sommige populaire apparaten. Vergeet niet de viewportgrootte in te gebruiken [!DNL Target]. Verschillende websites vermelden de viewportgrootten voor populaire apparaten. Zie bijvoorbeeld [https://viewportsizer.com/devices/](https://viewportsizer.com/devices/) of raadpleeg de website van de maker van het apparaat.

| Apparaat | Viewportgrootte | Apparaatresolutie |
|---|---|---|
| iPhone SE | 375 x 667 uur | 750 x 1334 uur |
| iPhone 11 Pro Max | 414 x 896 uur | 1242 x 2688 uur |
| iPhone 11 x max. | 414 x 896 uur | 1242 x 2688 uur |
| iPhone 11 | 414 x 896 uur | 828 x 1792 uur |
| iPhone 11 Xr | 414 x 896 uur | 828 x 1792 uur |
| iPhone 11 Pro | 375 x 812 uur | 1125b x 2436h |
| iPhone 11 X | 375 x 812 uur | 1125b x 2436h |
| iPhone 11 Xs | 375 x 812 uur | 1125b x 2436h |
| iPhone X | 375 x 812 uur | 1125b x 2436h |
| iPhone 8 Plus | 414 x 736 uur | 1080 x 1920 |
| iPhone 8 | 375 x 667 uur | 750 x 1334 uur |
| iPhone 7 Plus | 414 x 736 uur | 1080 x 1920 |
| iPhone 7 | 375 x 667 uur | 750 x 1334 uur |
| iPhone 6s Plus | 414 x 736 uur | 1080 x 1920 |
| iPhone 6s | 375 x 667 uur | 750 x 1334 uur |
| iPhone 6 Plus | 414 x 736 uur | 1080 x 1920 |
| iPhone 6 | 375 x 667 uur | 750 x 1334 uur |
| iPad Pro | 1024 x 1366 uur | 2048 x 2732 uur |
| Derde en vierde generatie iPad | 768 x 1024 uur | 1536 x 2048 uur |
| iPad AIR 1 &amp; 2 | 768 x 1024 uur | 1536 x 2048 uur |
| iPad Mini | 768 x 1024 uur | 768 x 1024 uur |
| iPad Mini 2 en 3 | 768 x 1024 uur | 1536 x 2048 uur |
| Nexus 6P | 411w x 731h | 1440b x 2560h |
| Nexus 5X | 411w x 731h | 1080 x 1920 |
| Google Pixel | 411w x 731h | 1080 x 1920 |
| Google Pixel XL | 411w x 731h | 1440b x 2560h |
| Google Pixel 2 | 411w x 731h | 1080 x 1920 |
| Google Pixel 2 XL | 411 x 823 uur | 1440b x 2880h |
| Samsung Galaxy Noot 5 | 480 x 853 uur | 1440b x 2560h |
| LG G5 | 480 x 853 uur | 1440b x 2560h |
| One Plus 3 | 480 x 853 uur | 1080 x 1920 |
| Samsung Galaxy S9 | 360 x 740 uur | 1440b x 2960h |
| Samsung Galaxy S9+ | 360 x 740 uur | 1440b x 2960h |
| Samsung Galaxy S8 | 360 x 740 uur | 1440b x 2960h |
| Samsung Galaxy S8+ | 360 x 740 uur | 1440b x 2960h |
| Samsung Galaxy S7 | 360 x 640 uur | 1440b x 2560h |
| Samsung Galaxy S7 Edge | 360 x 640 uur | 1440b x 2560h |
| Nexus 7 (2013) | 600 x 960 uur | 1200 x 1920 |
| Nexus 9 | 768 x 1024 uur | 1536 x 2048 uur |
| Samsung Galaxy Tab 10 | 800 x 1280 | 800 x 1280 |
| Chromebook Pixel | 1280 x 850 uur | 2560b x 1700h |

Als u een activiteit aan mensen op een bepaald apparaat wilt leveren, kies het aangewezen publiek voor dat apparaat in het activiteitendiagram. Gebruik de Mobiele Composer van het Web om de pagina in de activiteit voor dat apparaat uit te geven. Als u een activiteit over uw volledige digitale ervaring wilt in werking stellen en ervoor wilt zorgen het goed kijkt over alle apparaten, pas geen het richten toe, en gebruik mobiele viewports om de activiteit op elke het schermgrootte voor te vertonen.

Als u een responsieve site hebt, is uw site doorgaans ontworpen om in een andere weergave te worden geopend wanneer deze wordt geopend door een apparaat met een specifieke schermgrootte. De schermgrootten die de nieuwe weergaven activeren, worden CSS-onderbrekingspunten genoemd. CSS-onderbrekingspunten zijn punten waar de website-inhoud afhankelijk van de apparaatbreedte reageert om de optimale lay-out voor bezoekers weer te geven. CSS-onderbrekingspunten worden ook [mediaquery](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)&#39;s genoemd.

Sla uw CSS-onderbrekingspunten op in [!DNL Target] zodat u een voorvertoning van uw ervaringen kunt bekijken voor elke weergave die u definieert. Elk van deze ervaringen wordt getoond in een mobiele viewport in de [!DNL Target] interface. Open de weergave voor elke schermgrootte door op die viewport boven aan de weergave te klikken.

Als uw site niet reageert, kunt u nog steeds de Mobile Web Composer gebruiken om een site weer te geven als uw activiteit is gericht op een specifiek apparaat.

>[!IMPORTANT]
>
>Hoewel u een ervaring vanuit mobiele viewports kunt bewerken, zijn deze wijzigingen van toepassing op alle viewports en apparaten, niet alleen op de viewport waarin u werkt. Op dezelfde manier wordt bij het bewerken van een ervaring in de normale desktopweergave de pagina voor alle schermgrootten gewijzigd, en niet alleen voor de desktopweergave. Momenteel ondersteunen we geen wijzigingen die specifiek zijn voor viewport.

## Configuratie van mobiele viewport {#task_B4B161499DC0470584ED922A4D20FCAB}

Configureer alle mobiele viewports die u beschikbaar wilt maken wanneer u uw ervaringen maakt.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**.
1. Als u een nieuwe mobiele viewport wilt toevoegen, klikt u in de **[!UICONTROL Mobile viewports configuration]** sectie op **[!UICONTROL Add]**.

   ![viewport toevoegen](/help/c-experiences/c-visual-experience-composer/assets/viewpoert_add.png)

   Als u de configuratie van een bestaande mobiele viewport wilt wijzigen, selecteert u die viewport en klikt u op het pictogram [!UICONTROL Edit] (potlood).

1. Typ een naam voor de mobiele viewport.

   Geef uw mobiele viewport een beschrijvende naam die u gemakkelijk kunt herkennen. De naam mag maximaal 36 tekens lang zijn.

1. Voer de schermgrootte van het mobiele apparaat in, zowel de breedte als de hoogte.

   De breedte kan liggen tussen 150 en 968 pixels. De hoogte kan liggen tussen 150 en 1280 pixels.

1. (Optioneel) Selecteer het besturingssysteem van het apparaat.

   Opties:

   * Android
   * iOS
   * Windows
   * Symbian
   * Blackberry

   Als u de [Enhanced Experience Composer](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) gebruikt en een besturingssysteem kiest, [!DNL Target] emuleert u dat apparaat wanneer u de pagina bekijkt. Als er bijvoorbeeld een ander uiterlijk voor Android is dan voor iOS op uw responsieve site, [!DNL Target] wordt dat gedrag nagebootst.

1. Klik op **[!UICONTROL Save]**.

## Een responsieve ervaring maken {#task_D6332438B5EE48CCA8AF199270F1CAEF}

Voeg mobiele viewports aan uw [!DNL Target] activiteiten toe om responsieve ervaringen voor mobiele schermen te creëren.

1. Maak de [gewenste activiteit](/help/c-activities/activities.md).
1. Klik in Visual Experience Composer op het **[!UICONTROL Settings]** tandwielpictogram en selecteer **[!UICONTROL Add Mobile Viewports]**.

   ![Mobiele Viewports toevoegen, optie](/help/c-experiences/c-visual-experience-composer/assets/add-mobile-viewports.png)

1. Klik op het **[!UICONTROL Devices]** pictogram en schakel vervolgens elk apparaat in dat een mobiele viewport moet hebben.

   ![Mobiele viewports inschakelen](/help/c-experiences/c-visual-experience-composer/assets/mobileviewports.png)

   De mobiele viewports worden vermeld van kleinste tot grootste volgens breedte.

1. Bewerk de mobiele viewports naar wens.

   Wijzigingen die u aanbrengt in de ervaring (bijvoorbeeld als u de tekst in een kop wijzigt) worden toegepast op alle apparaten.

   Plaats de muis boven de naam van een viewport om de grootte van de viewport weer te geven.

   ![iPhone 11 Pro Max responsieve ervaring](/help/c-experiences/c-visual-experience-composer/assets/iphone11.png)

1. U kunt desgewenst schakelen tussen de modi Staand en Liggend door op het pictogram voor de gewenste richting te klikken.

   ![Afdrukopties](/help/c-experiences/c-visual-experience-composer/assets/orientation.png)

## Hoofdlettergebruik: Twee iPhone-versies als doel instellen {#task_CC3144BF5BA54034996E1D3DB0BC1A35}

In dit gebruiksgeval ziet u hoe u ervaringen voor twee iPhone-versies kunt configureren: iPhone 11 Pro Max en iPhone SE.

1. Klik op Doel **[!UICONTROL Administration]**.
1. Maak in de **[!UICONTROL Mobile viewport configuration]** sectie mobiele viewports voor iPhone 11 Pro Max en iPhone SE.

   Gebruik de volgende instellingen voor elke viewport:

   | Naam | Breedte | Hoogte | Besturingssysteem |
   |---|---|---|---|
   | iPhone 11 Pro Max | 414 | 896 | iOS |
   | iPhone SE | 375 | 667 | iOS |

   ![](assets/iphoneviewportconfig.png)

1. Maak een activiteit met de ervaring u zou willen richten.
1. Selecteer de ervaring die u wilt gebruiken voor bezoekers die uw site openen via een iPhone 11 Pro Max of iPhone SE.
1. Wanneer het selecteren van uw doel, klik **[!UICONTROL Create Audience]**, dan vorm een publiek zoals aangetoond in het hieronder beeld:

   ![](assets/iphoneaudiences.png)

   Omdat de telefoon aan landschap kon worden geroteerd, die zowel hoogte als breedte vereisen om groter te zijn dan 320 leidt gelijktijdig tot een voorwaarde dat slechts iPhone 11 Pro Max en iPhone SE zou kunnen ontmoeten, wanneer gecombineerd met het model van het iPhoneApparaat.
1. Klik op **[!UICONTROL Save]**.
1. Ga door met het instellen van je activiteit zoals je normaal zou doen.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Visual Experience Composer (2 van 2) (7:29) - badge ![Overzicht](/help/assets/overview.png)

De volgende demo video omvat informatie over het gebruiken van de composer van de Ervaring van Visual Studio om met mobiele viewports te werken:

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)

### Accountvoorkeuren in Adobe Target - ![overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het instellen van mobiele viewports vanaf 4:40 in de video.

>[!VIDEO](https://video.tv.adobe.com/v/17379)