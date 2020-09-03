---
keywords: visual experience composer;vec;default url;enhanced experience composer;eec;mixed content;experience snapshots;mobile viewport;css;css selectors
description: Configureer de Adobe Target Visual Experience Composer (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.
title: De Adobe Target Visual Experience Composer configureren
feature: administration general
topic: Standard
translation-type: tm+mt
source-git-commit: ee618961faa12a7352aaf9ed1d869f9e5ab39cdd
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---


# Vorm Composer van de Visuele Ervaring

Configureer de [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.

Klik op [!UICONTROL Visual Experience Composer] > **[!UICONTROL Administration]** **[!UICONTROL Visual Experience Composer].**

>[!NOTE]
>
>Houd er rekening mee dat de instellingen op deze pagina van toepassing zijn op het gehele [!DNL Target] account.

![Configuratiepagina Visual Experience Composer](/help/administrating-target/assets/vec.png)

## Algemene instellingen

U kunt algemene instellingen opgeven voor Visual Experience Composer.

![Sectie Algemene instellingen](/help/administrating-target/assets/general-settings.png)

De volgende instellingen zijn beschikbaar:

### Standaard-URL

Stel de standaard-URL in die door de [!UICONTROL Visual Experience Composer]URL wordt gebruikt. Dit is de standaardpagina, zoals uw homepage, die wordt gebruikt wanneer u opstelling een ervaring voor elke nieuwe activiteit. Als u geen standaard-URL instelt, moet u voor elke activiteit een URL invoeren wanneer u deze maakt.

### Enhanced Experience Composer inschakelen {#eec}

Hiermee kunt u iFrame-sites en sites met gemengde inhoud bewerken. Sommige sites zijn mogelijk niet compatibel met de verbeterde versie. Schakel deze optie uit om terug te keren naar het origineel [!UICONTROL Visual Experience Composer]. Deze keuze heeft geen invloed op de levering van activiteiten op sites.

Voor meer informatie, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.

U kunt het ook inschakelen [!UICONTROL Enhanced Experience Composer] op het activiteitsniveau.

### Gemengde inhoud laden

Gemengde inhoud inschakelen bij het openen van een website met behulp van [!UICONTROL Enhanced Experience Composer] (EEG). Als u deze optie inschakelt, voorkomt u de extra overhead van het laden van statische bronnen via [!DNL Target] proxyservers.

Deze optie is bijvoorbeeld handig als:

* Met de CSP-headers (Content Security Policy) kunt u gemengde inhoud laden zonder dat proxyservers worden gebruikt waarvoor de EEG is ingeschakeld.
* Uw HTTP-website heeft te maken met een langere laadtijd in de EEG, waardoor het langer duurt om JavaScript-afbeeldingen te laden via proxy.

### Erviteitsmomentopnamen genereren in het activiteitsstroomdiagram

Als u ervaringsmomentopnamen inschakelt, worden miniaturen voor uw ervaringen in het activiteitenwerkstroomdiagram gegenereerd. Het uitschakelen van momentopnamen kan voor sommige gebruikers tot snellere prestaties leiden.

## ![Premium badge](/help/assets/premium.png) Mobile Viewport Configuration

U kunt apparaten toevoegen om te gebruiken wanneer het previewing ervaringen. Elk apparaat heeft een bijbehorend publiek.

![Mobiele Viewportconfiguratie](/help/administrating-target/assets/mobile-viewport-configuration.png)

Klik **[!UICONTROL Add]**, geef een beschrijvende naam op voor de mobiele viewport, geef de breedte en hoogte op, selecteer het gewenste besturingssysteem en klik op [!UICONTROL Save].

Voor informatie over hoe te om een mobiele viewport toe te voegen, zie de [Mobiele Configuratie](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md)van de Viewport.

## CSS-kiezers {#css}

Geef op hoe CSS-kiezers moeten worden [!DNL Target] gegenereerd.

![Sectie CSS-kiezers](/help/administrating-target/assets/css-selectors.png)

Met deze opties krijgt u inzicht in de structuur van uw site en kunt u betere CSS-kiezers voor de levering van inhoud genereren. [!DNL Target] Standaard worden kiezers [!DNL Target] gegenereerd op basis van element-id&#39;s op de pagina. Als uw site weinig id&#39;s gebruikt of ID&#39;s op dezelfde pagina dupliceert, kunt u beter klassen gebruiken.

U kunt een van de volgende opties of beide opties kiezen:

### Element-id&#39;s gebruiken

Schakel deze optie uit als dezelfde id wordt gebruikt voor meerdere elementen of als de element-id kan veranderen bij het laden van de pagina.

### Elementklassen gebruiken

Standaard worden [!DNL Target] alleen element-id&#39;s gebruikt. Als uw pagina echter is ontworpen om klassen te gebruiken voor het identificeren van elementen, zoals een pagina die is gemaakt met [!DNL Adobe Experience Manager], moet u ook [!UICONTROL Use element classes]selecteren.

>[!NOTE]
>
>Hoewel alles is gedaan om nauwkeurigheid te verzekeren, houd er rekening mee dat het gebruik van klassen tot fouten kan leiden. Als u geen van beide opties selecteert, heeft dit ook invloed op de nauwkeurigheid. De nauwkeurigheidsvolgorde is ID&#39;s > klassen > geen van beide opties. Zorg altijd dat u de pagina test om te controleren of de kiezers correct zijn.

U kunt deze instelling per activiteit overschrijven (klik op het [!UICONTROL Settings] tandwielpictogram en selecteer [!UICONTROL CSS Selectors]). Dit is vooral nuttig als u veelvoudige plaatsen hebt die verschillend worden gevormd.

>[!NOTE]
>
>Het overschrijven van de instelling per activiteit is niet beschikbaar in [!UICONTROL Automated Personalization] en [!UICONTROL Multivariate Testing] activiteiten.  Zie [Elementkiezers die in de Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/vec-selectors.md) worden gebruikt voor aanvullende informatie over kiezers.

## Trainingsvideo: Accountvoorkeuren (7:33) - ![overzichtspagina](/help/assets/overview.png)

Deze video bevat informatie over accountvoorkeuren.

* Beschrijf de beschikbare accountinstellingen in [!DNL Target Standard]

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] menu (voorheen [!UICONTROL Administration] [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
