---
keywords: visuele ervaringscomposer;vec;standaard url;verbeterde ervaringscomposer;eec;gemengde inhoud;beleving momentopnamen;mobiele viewport;css;css kiezers
description: Leer hoe te om Adobe  [!DNL Target]  Visuele Composer van de Ervaring (VEC) te vormen door zijn algemene montages, mobiele viewport configuratie, en CSS selecteurs te specificeren.
title: Hoe vorm ik de Visuele Composer van de Ervaring (VEC)?
feature: Administration & Configuration
role: Admin
exl-id: cf6c9ece-6745-477e-81ac-a3e9a9fddb09
source-git-commit: 12831d6584acc482db415629d7e70a18e39c47c2
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# De [!UICONTROL Visual Experience Composer] configureren

Configureer [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.

Als u de configuratiepagina van [!UICONTROL Visual Experience Composer] wilt openen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer].**

{{permissions-update}}

>[!NOTE]
>
>Houd er rekening mee dat de instellingen op deze pagina van toepassing zijn op het gehele [!DNL Target] -account.

## Algemene instellingen

U kunt algemene instellingen opgeven voor de [!UICONTROL Visual Experience Composer] .

![&#x200B; Algemene sectie van Montages &#x200B;](/help/main/administrating-target/assets/general-settings.png)

De volgende instellingen zijn beschikbaar:

### Standaard-URL

Stel de standaard-URL in die door de [!UICONTROL Visual Experience Composer] wordt gebruikt. Dit is de standaardpagina, zoals uw homepage, die wordt gebruikt wanneer u opstelling een ervaring voor elke nieuwe activiteit. Als u geen standaard-URL instelt, moet u voor elke activiteit een URL invoeren wanneer u deze maakt.

### Enhanced Experience Composer inschakelen {#eec}

Hiermee kunt u iFrame-sites en sites met gemengde inhoud bewerken. Sommige sites zijn mogelijk niet compatibel met de verbeterde versie. Schakel deze optie uit als u het origineel wilt herstellen [!UICONTROL Visual Experience Composer] . Deze keuze heeft geen invloed op de levering van activiteiten op sites.

Voor meer informatie, zie [&#x200B; het Oplossen van problemen de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

U kunt [!UICONTROL Enhanced Experience Composer] ook inschakelen op activiteitsniveau.

### Gemengde inhoud laden

Schakel gemengde inhoud in terwijl u een website opent met [!UICONTROL Enhanced Experience Composer] (EEC). Als u deze optie inschakelt, voorkomt u de extra overhead van het laden van statische bronnen via [!DNL Target] -proxyservers.

Deze optie is bijvoorbeeld handig als:

* Met de CSP-headers (Content Security Policy) kunt u gemengde inhoud laden zonder dat proxyservers worden gebruikt waarvoor de EEG is ingeschakeld.
* Uw HTTP-website heeft te maken met een langere laadtijd in de EEG, waardoor het langer duurt om JavaScript-afbeeldingen te laden via proxy.

### Erviteitsmomentopnamen genereren in het activiteitsstroomdiagram

Als u ervaringsmomentopnamen inschakelt, worden miniaturen voor uw ervaringen in het activiteitenwerkstroomdiagram gegenereerd. Het uitschakelen van momentopnamen kan voor sommige gebruikers tot snellere prestaties leiden.

## Configuratie mobiele viewport

>[!NOTE]
>
>De [!UICONTROL Mobile Viewport Configuration] montages is a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) eigenschap.


U kunt apparaten toevoegen om te gebruiken wanneer het previewing ervaringen. Elk apparaat heeft een bijbehorend publiek.

![&#x200B; Mobiele sectie van de Configuratie van de Viewport &#x200B;](/help/main/administrating-target/assets/mobile-viewport-configuration.png)

Klik op **[!UICONTROL Add]** , geef een beschrijvende naam op voor de mobiele viewport, geef de breedte en hoogte op, selecteer het gewenste besturingssysteem en klik op [!UICONTROL Save] .

Voor informatie over hoe te om een mobiele viewport toe te voegen, zie [&#x200B; Mobiele Configuratie van de Viewport &#x200B;](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

## CSS-kiezers {#css}

Geef op hoe [!DNL Target] CSS-kiezers genereert.

![&#x200B; CSS de sectie van Kiezers &#x200B;](/help/main/administrating-target/assets/css-selectors.png)

Met deze opties krijgt [!DNL Target] inzicht in de structuur van uw site, zodat u betere CSS-kiezers voor de levering van inhoud kunt genereren. Standaard genereert [!DNL Target] kiezers op basis van element-id&#39;s op de pagina. Als uw site weinig id&#39;s gebruikt of ID&#39;s op dezelfde pagina dupliceert, kunt u beter klassen gebruiken.

U kunt een van de volgende opties of beide opties kiezen:

### Element-id&#39;s gebruiken

Schakel deze optie uit als dezelfde id wordt gebruikt voor meerdere elementen of als de element-id kan veranderen bij het laden van de pagina.

### Elementklassen gebruiken

Standaard gebruikt [!DNL Target] alleen element-id&#39;s. Als uw pagina echter is ontworpen om klassen te gebruiken voor het identificeren van elementen, zoals een pagina die is gemaakt met [!DNL Adobe Experience Manager] , moet u ook [!UICONTROL Use element classes] selecteren.

>[!NOTE]
>
>Hoewel alles is gedaan om nauwkeurigheid te verzekeren, houd er rekening mee dat het gebruik van klassen tot fouten kan leiden. Als u geen van beide opties selecteert, heeft dit ook invloed op de nauwkeurigheid. De nauwkeurigheidsvolgorde is ID&#39;s > klassen > geen van beide opties. Zorg altijd dat u de pagina test om te controleren of de kiezers correct zijn.

U kunt deze instelling per activiteit overschrijven (klik op het tandwielpictogram [!UICONTROL Settings] en selecteer vervolgens [!UICONTROL CSS Selectors] ). Dit is vooral nuttig als u veelvoudige plaatsen hebt die verschillend worden gevormd.

>[!NOTE]
>
>Het overschrijven van de instelling per activiteit is niet beschikbaar in [!UICONTROL Automated Personalization] - en [!UICONTROL Multivariate Testing] -activiteiten.  Zie [&#x200B; de Kiezers van het Element die in de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/vec-selectors.md) voor extra informatie over selecteurs worden gebruikt.

## De video van de opleiding: De Voorkeur van de Rekening (7 :33) ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

Deze video bevat informatie over accountvoorkeuren.

* Beschrijf de beschikbare accountinstellingen in [!DNL Target Standard]

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] [!UICONTROL Administration] menu (voorheen [!UICONTROL Setup] ) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is over het algemeen correct; nochtans, zouden de opties in lichtjes verschillende plaatsen kunnen zijn. Bijgewerkte video&#39;s worden binnenkort gepost.

>[!VIDEO](https://video.tv.adobe.com/v/17379)
