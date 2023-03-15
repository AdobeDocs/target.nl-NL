---
keywords: visuele ervaringscomposer;vec;standaard url;verbeterde ervaringscomposer;eec;gemengde inhoud;beleving momentopnamen;mobiele viewport;css;css kiezers
description: Leer hoe te om Adobe te vormen [!DNL Target] Visual Experience Composer (VEC) door zijn algemene montages, mobiele viewport configuratie, en CSS selecteurs te specificeren.
title: Hoe vorm ik de Visuele Composer van de Ervaring (VEC)?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
source-git-commit: fa11f93058b69e5e59e0ee20c65cffa4a1344ca0
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Vorm Composer van de Visuele Ervaring

Configureer de [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.

Om toegang te krijgen tot [!UICONTROL Visual Experience Composer] configuratiepagina, klik **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer].**

>[!NOTE]
>
>Houd er rekening mee dat de instellingen op deze pagina van toepassing zijn op de gehele [!DNL Target] account.

![Configuratiepagina Visual Experience Composer](/help/main/administrating-target/assets/vec.png)

## Algemene instellingen

U kunt algemene instellingen opgeven voor Visual Experience Composer.

![Sectie Algemene instellingen](/help/main/administrating-target/assets/general-settings.png)

De volgende instellingen zijn beschikbaar:

### Standaard-URL

Stel de standaard-URL in die door de [!UICONTROL Visual Experience Composer]. Dit is de standaardpagina, zoals uw homepage, die wordt gebruikt wanneer u opstelling een ervaring voor elke nieuwe activiteit. Als u geen standaard-URL instelt, moet u voor elke activiteit een URL invoeren wanneer u deze maakt.

### Enhanced Experience Composer inschakelen {#eec}

Hiermee kunt u iFrame-sites en sites met gemengde inhoud bewerken. Sommige sites zijn mogelijk niet compatibel met de verbeterde versie. Schakel deze optie uit als u wilt terugkeren naar het origineel [!UICONTROL Visual Experience Composer]. Deze keuze heeft geen invloed op de levering van activiteiten op sites.

Zie voor meer informatie [Het oplossen van problemen de Visuele Composer van de Ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

U kunt ook de opdracht [!UICONTROL Enhanced Experience Composer] op het niveau van de activiteit.

### Gemengde inhoud laden

Gemengde inhoud inschakelen bij het openen van een website met de opdracht [!UICONTROL Enhanced Experience Composer] (EEG) Als u deze optie inschakelt, wordt de extra overhead van het laden van statische bronnen via [!DNL Target] proxyservers.

Deze optie is bijvoorbeeld handig als:

* Met de CSP-headers (Content Security Policy) kunt u gemengde inhoud laden zonder dat proxyservers worden gebruikt waarvoor de EEG is ingeschakeld.
* Uw HTTP-website heeft te maken met een langere laadtijd in de EEG, waardoor het langer duurt om JavaScript-afbeeldingen te laden via proxy.

### Erviteitsmomentopnamen genereren in het activiteitsstroomdiagram

Als u ervaringsmomentopnamen inschakelt, worden miniaturen voor uw ervaringen in het activiteitenwerkstroomdiagram gegenereerd. Het uitschakelen van momentopnamen kan voor sommige gebruikers tot snellere prestaties leiden.

## [!BADGE Premium]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."}

U kunt apparaten toevoegen om te gebruiken wanneer het previewing ervaringen. Elk apparaat heeft een bijbehorend publiek.

![Mobiele Viewportconfiguratie](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Klikken **[!UICONTROL Add]**, geeft u een beschrijvende naam op voor de mobiele viewport, geeft u de breedte en hoogte op, selecteert u het gewenste besturingssysteem en klikt u op [!UICONTROL Save].

Voor informatie over het toevoegen van een mobiele viewport raadpleegt u [Configuratie mobiele viewport](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## CSS-kiezers {#css}

Opgeven hoe [!DNL Target] genereert CSS-kiezers.

![Sectie CSS-kiezers](/help/main/administrating-target/assets/css-selectors.png)

Deze opties helpen [!DNL Target] begrijpen de structuur van uw site om betere CSS-kiezers te genereren voor de levering van inhoud. Standaard, [!DNL Target] Hiermee genereert u kiezers op basis van element-id&#39;s op de pagina. Als uw site weinig id&#39;s gebruikt of ID&#39;s op dezelfde pagina dupliceert, kunt u beter klassen gebruiken.

U kunt een van de volgende opties of beide opties kiezen:

### Element-id&#39;s gebruiken

Schakel deze optie uit als dezelfde id wordt gebruikt voor meerdere elementen of als de element-id kan veranderen bij het laden van de pagina.

### Elementklassen gebruiken

Standaard, [!DNL Target] gebruikt alleen element-id&#39;s. Als uw pagina echter is ontworpen om klassen te gebruiken voor het identificeren van elementen, zoals een pagina die is gemaakt met [!DNL Adobe Experience Manager], dient u ook [!UICONTROL Use element classes].

>[!NOTE]
>
>Hoewel alles is gedaan om nauwkeurigheid te verzekeren, houd er rekening mee dat het gebruik van klassen tot fouten kan leiden. Als u geen van beide opties selecteert, heeft dit ook invloed op de nauwkeurigheid. De nauwkeurigheidsvolgorde is ID&#39;s > klassen > geen van beide opties. Zorg altijd dat u de pagina test om te controleren of de kiezers correct zijn.

U kunt deze instelling per activiteit overschrijven (klik op [!UICONTROL Settings] tandwielpictogram, selecteer vervolgens [!UICONTROL CSS Selectors]). Dit is vooral nuttig als u veelvoudige plaatsen hebt die verschillend worden gevormd.

>[!NOTE]
>
>De instelling per activiteit overschrijven is niet beschikbaar in [!UICONTROL Automated Personalization] en [!UICONTROL Multivariate Testing] activiteiten.  Zie [Elementkiezers die worden gebruikt in de composer voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md) voor aanvullende informatie over kiezers.

## Trainingsvideo: Accountvoorkeuren (7:33) ![Overzicht badge](/help/main/assets/overview.png)

Deze video bevat informatie over accountvoorkeuren.

* Beschrijf de beschikbare accountinstellingen in [!DNL Target Standard]

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
