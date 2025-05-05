---
keywords: gericht;visuele ervaringscomposer;vec;los visuele ervaringscomposer problemen op;het oplossen van problemen;tls;tls 1.2
description: Leer hoe u problemen in de [!UICONTROL Visual Experience Composer] (VEC).
title: Hoe los ik kwesties met betrekking tot [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: 7c0d0154b81fbd3f89a82b31cd18541a7f0ea1a7
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# Problemen met het oplossen van problemen in verband met de [!UICONTROL Visual Experience Composer]

Er kunnen weergaveproblemen optreden in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) onder bepaalde voorwaarden.

## Wanneer ik mijn website in het dialoogvenster [!UICONTROL Visual Experience Composer]de [!DNL Target] bibliotheken worden niet geladen. (alleen VEC) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

[!DNL Target] voegt twee parameters toe (`mboxEdit=1` en `mboxDisable=1`) bij het openen van de website in de [!UICONTROL Visual Experience Composer].

Als uw website (met name Apps met één pagina) parameters bijsnijdt of deze verwijdert terwijl u van de ene pagina naar de andere navigeert (zonder dat de pagina opnieuw wordt geladen), worden de [!DNL Target] functies en de [!DNL Target] bibliotheken worden niet geladen.

U voorkomt dit probleem door deze twee parameters niet bij te snijden of te verwijderen.

## Mijn pagina wordt niet geopend in de EEG, of wordt langzaam geladen. Activiteiten of ervaringen worden langzaam in de VEC geladen. (alleen VEC) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Verschillende problemen kunnen van invloed zijn op de paginaprestaties in het dialoogvenster [!UICONTROL Target] ervaren componisten. Enkele veelvoorkomende problemen zijn:

* U hebt geen box op de pagina.
* Uw site gebruikt proxyblokkering, waardoor de pagina in geen van beide composers kan worden geopend.
* Uw site staat het openen van een iFrame niet toe.

Als er problemen optreden in het dialoogvenster [!UICONTROL Enhanced Experience Composer], probeer de [!UICONTROL Enhanced Experience Composer] en gebruiken de [!UICONTROL Visual Experience Composer] in plaats daarvan.

Om het [!UICONTROL Enhanced Experience Composer], ga naar **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** en zet de **[!UICONTROL Enable Enhanced Experience Composer]** -optie.

Sommige gebruikers zien het volgende foutbericht in de console:

![Foutbericht voor console](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Als geen van beide [!UICONTROL Visual Experience Composer] noch de [!UICONTROL Enhanced Experience Composer] werkt, gebruik een browser extensie zoals [!DNL Requestly] ([!DNL Chrome] of [!DNL Firefox]) of Reactiekoppen wijzigen (Firefox) waarmee de koptekstopties voor X-frames voor uw site kunnen worden overschreven en geladen in iFrames, waardoor de VEC wordt ingeschakeld. Als u geen browserextensies kunt gebruiken, gebruikt u de [Form-based Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Naast de volgende informatie kunt u de opdracht [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) for [!DNL Google Chrome].


>[!NOTE]
>
>Deze plug-ins mogen alleen worden gebruikt in de context van VEC-bewerking.
>
>Voor de [!DNL Requestly] Als u headers moet verwijderen, moet u een van de volgende handelingen uitvoeren:
>
>* Voeg URL-regels toe voor de URL die u in de VEC wilt openen, zodat kopteksten alleen voor die URL&#39;s worden verwijderd.
>
>* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.
>
>Voor de [!UICONTROL Modify Response Header] extensie ([!DNL Firefox]), omdat u geen URL-regel kunt toevoegen, moet u het volgende doen:
>
>* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.

**Als u de opdracht [!DNL Requestly] verlenging op [!DNL Chrome] of [!DNL Firefox]:**

1. Schakel de [!UICONTROL Enhanced Experienced Composer].
1. Installeer de [!DNL Requestly] browserextensie op [!DNL Chrome] of [!DNL Firefox].
1. Open de extensie en configureer deze als volgt:
1. Selecteren **[!UICONTROL Modify headers]**.
1. Voer het volgende in:

   * Naam van regel
   * Wijzigingsvoorschriften

      * Schakelen **[!UICONTROL Add]** tot **[!UICONTROL Remove]**.
      * Schakelen **[!UICONTROL Request]** tot **[!UICONTROL Response]**.
      * Voer &quot;X-Frame-Opties&quot; in als koptekst.
      * Herhaal de vorige stappen en voer &quot;x-frame-options&quot; in als koptekst.

        >[!NOTE]
        >
        >Kopteksten die via worden gemanipuleerd [!DNL Requestly] zijn hoofdlettergevoelig.

      * Wijzigen **[!UICONTROL Equals]** tot **[!UICONTROL Contains]** als de voorwaarde voor de bron-URL en voer de URL in van de activiteit die u probeert te laden in de VEC.

     ![chrome_extensieafbeelding](assets/chrome_extension.png)

1. Klik op **[!UICONTROL Save]**.

   ![vaak beeld](assets/requestly.png)

   U moet nu de pagina snel kunnen laden met de [!UICONTROL Visual Experience Composer].

**Als u de opdracht [!DNL Modify Response Headers] verlenging op [!UICONTROL Firefox]:**

1. Installeer de [!UICONTROL Modify Response Headers] op [!DNL Firefox] en start de browser opnieuw.
1. Van uw [!DNL Firefox] extensies, selecteert u de extensie Responsheaders wijzigen.
1. Klik op **[!UICONTROL Preferences]**.
1. Selecteren **[!UICONTROL Filter]** van de [!UICONTROL Action] vallen.
1. In de [!UICONTROL Header Name] veld, voert u in: **[!UICONTROL X-Frame-Options]**.
1. Stap 4 en 5 herhalen om een filter toe te voegen met **[!UICONTROL x-frame-options]**.
1. Klik op **[!UICONTROL Add]**.
1. Klik op **[!UICONTROL Start]**.

![Firefox-extensie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

Na het instellen van een extensie opent u [!DNL Target]. Uw pagina&#39;s moeten nu worden geladen in het dialoogvenster [!UICONTROL Visual Experience Composer], zelfs als de [!UICONTROL Enhanced Experience Composer] is uitgeschakeld.

## Mijn pagina wordt niet weergegeven in de VEC (alleen VEC) {#does-not-load}

* De meest recente versie van de extensie garandeert een optimale compatibiliteit met VEC: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

  Ga naar [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] klik vervolgens op [!UICONTROL Details].

* De [!UICONTROL Visual Experience Composer] vereist ontwerpbibliotheken om wijzigingen op de webpagina uit te voeren. Deze bibliotheken zijn ingesloten in de bibliotheek at.js en worden gedownload via de extensie [!DNL Adobe] servers elke keer dat VEC wordt gebruikt.

  De extensie wordt gedownload naar de bibliotheek at.js, ongeacht of at.js of de [!DNL Adobe Experience Platform Web SDK] worden al op de pagina opgenomen.

  Zorg ervoor dat er geen ongeldige wijzigingen zijn toegevoegd aan de headers at.js die zijn geconfigureerd in het dialoogvenster [!UICONTROL Administration] > [!UICONTROL Implementation] sectie.

* Zorg ervoor dat de webpagina geen aanvragen blokkeert die verplicht moeten worden geladen wanneer deze zijn ingesloten in een iFrame. Dit omvat het gebruik van CSP-richtlijnen of aangepaste JS-code die zijn ingesloten in de website van de klant, tags meta HTML of de header x-frame-options.

* Zorg ervoor dat Javascript van de webpagina zich niet mengt in de ontwerpbibliotheken. Gebruik of neem geen bestanden op met de volgende gereserveerde namen:

   * `target-vec-helper.js`
   * `target-vec.js`
   * `target.js`
   * `admin.css`
   * `sizzle.js`
   * `mixContentCheck.html`

     Bovendien kan het per ongeluk overschrijven van variabelen of gebeurtenissen die in deze bestanden zijn gedefinieerd, leiden tot problemen met VEC.

* De browser blokkeert een niet-beveiligde pagina op een beveiligde site.

  Klik op het pictogram links van de URL in de adresbalk van de browser en klik op **[!UICONTROL Disable protection on this page]**

* U hebt een ongeldige URL ingevoerd.
* Als uw website niet in de VEC kan worden geladen of zich onverwacht gedraagt, kunt u cookies op uw website in de browser accepteren voordat u de website probeert te laden in [!DNL Target].

## De VEC wordt verbroken weergegeven wanneer ik de modus Bladeren gebruik. (alleen VEC) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Als u in de modus Bladeren een URL opent die niet [!DNL Target] geïmplementeerde bibliotheken ([at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=nl-NL){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=nl-NL){target=_blank}) of bevat een koptekst voor de framebuffer, wordt de VEC verbroken weergegeven. Vanwege beveiligingsproblemen in de browser, [!DNL Target] heeft geen juiste toegang tot de URL waarnaar u bent genavigeerd of de VEC-URL wordt niet consistent bijgewerkt wanneer de pagina wordt geladen.

Dit probleem doet zich voor omdat VEC de webpagina in een `<iframe>`. De huidige beveiligingsmechanismen van browsers verhinderen de [!DNL Target] UI heeft geen toegang tot de elementen van het bepaalde kader wegens het zelfde-oorsprongbeleid. Browsers blokkeren scripts die toegang proberen te krijgen tot een frame met een andere oorsprong en die informatie bevatten zoals de `location.href`.

U moet de nieuwe [De extensie Visuele bewerkingshulp](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) (aanbevolen) [oude extensie](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) om de [!DNL Target] om de pagina&#39;s optimaal te kunnen doorbladeren.

## Problemen die worden veroorzaakt door CSS-conflicten in de [!UICONTROL Visual Experience Composer]

Controleer of er CSS-bestanden zijn die invloed hebben op de zichtbaarheid tijdens het laden van de webpagina in de editor. Als u bijvoorbeeld de `overflow: hidden` De eigenschap in de hoofdtekst van de pagina kan schuifproblemen veroorzaken of klikgebeurtenissen activeren die het menu voor het schrijven kunnen beïnvloeden.
