---
keywords: gericht;visuele ervaringscomposer;vec;los visuele ervaringscomposer problemen op;het oplossen van problemen;tls;tls 1.2
description: Leer hoe u problemen in de map [!UICONTROL Visual Experience Composer] (VEC) kunt oplossen.
title: Hoe los ik problemen op met betrekking tot [!UICONTROL Visual Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: ca251025-25e8-4e56-9b59-81310fc763c1
source-git-commit: ef5df0ae37ca1d07c0e51c06ed78739b2d2983fc
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 0%

---

# Problemen met de [!UICONTROL Visual Experience Composer] oplossen

Weergaveproblemen treden soms op in de modus [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) onder bepaalde omstandigheden.

## Wanneer ik mijn website in [!UICONTROL Visual Experience Composer] open, laden de [!DNL Target] bibliotheken niet. (alleen VEC) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

+++Details
[!DNL Target] voegt twee parameters toe (`mboxEdit=1` en `mboxDisable=1`) terwijl de website wordt geopend in de [!UICONTROL Visual Experience Composer] .

Als uw website (met name Apps met één pagina) parameters bijsnijdt of deze verwijdert terwijl u van de ene pagina naar de andere navigeert (zonder dat de pagina opnieuw wordt geladen), worden de [!DNL Target] -functionaliteit verbroken en worden de [!DNL Target] -bibliotheken niet geladen.

U voorkomt dit probleem door deze twee parameters niet bij te snijden of te verwijderen.

+++

## Mijn pagina wordt niet geopend in de EEG, of wordt langzaam geladen. Activiteiten of ervaringen worden langzaam in de VEC geladen. (alleen VEC) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

+++Details
Verschillende problemen kunnen de paginaprestaties in de [!UICONTROL Target] Experience-composers beïnvloeden. Enkele veelvoorkomende problemen zijn:

* U hebt geen box op de pagina.
* Uw site gebruikt proxyblokkering, waardoor de pagina in geen van beide composers kan worden geopend.
* Uw site staat het openen van een iFrame niet toe.

Als er problemen optreden in de [!UICONTROL Enhanced Experience Composer] , schakelt u de [!UICONTROL Enhanced Experience Composer] uit en gebruikt u de [!UICONTROL Visual Experience Composer] .

Als u [!UICONTROL Enhanced Experience Composer] wilt uitschakelen, gaat u naar **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** en schakelt u de optie **[!UICONTROL Enable Enhanced Experience Composer]** uit.

Sommige gebruikers zien het volgende foutbericht in de console:

![&#x200B; de foutenmelding van de Console &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Als [!UICONTROL Visual Experience Composer] noch [!UICONTROL Enhanced Experience Composer] werkt, gebruik een browser uitbreiding zoals [!DNL Requestly] ( [!DNL Chrome] of [!DNL Firefox]) of wijzigt de Kopballen van de Reactie (Firefox) die de X-Kaders kopbalopties voor uw plaats kan overschrijven en hen om in iFrames toelaat worden geladen, toelatend VEC. Als u browser uitbreidingen niet kunt gebruiken, gebruik [&#x200B; Op vorm-gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Naast de volgende informatie kunt u de extensie [[!DNL Adobe Target] [!UICONTROL Visual Editing Helper] &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) for [!DNL Google Chrome] gebruiken.

>[!NOTE]
>
>Deze plug-ins mogen alleen worden gebruikt in de context van VEC-bewerking.
>
>Voor de extensie [!DNL Requestly] moet u een van de volgende twee handelingen uitvoeren wanneer er headers moeten worden verwijderd:
>
>* Voeg URL-regels toe voor de URL die u in de VEC wilt openen, zodat kopteksten alleen voor die URL&#39;s worden verwijderd.
>
>* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.
>
>Voor de extensie [!UICONTROL Modify Response Header] ([!DNL Firefox]), omdat u geen URL-regel kunt toevoegen, moet u het volgende doen:
>
>* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.

**om de [!DNL Requestly] uitbreiding op [!DNL Chrome] of [!DNL Firefox] te gebruiken:**

1. Schakel de [!UICONTROL Enhanced Experienced Composer] uit.
1. Installeer de [!DNL Requestly] browserextensie op [!DNL Chrome] of [!DNL Firefox] .
1. Open de extensie en configureer deze als volgt:
1. Selecteer **[!UICONTROL Modify headers]** .
1. Voer het volgende in:

   * Naam van regel
   * Wijzigingsvoorschriften

      * Schakelen **[!UICONTROL Add]** naar **[!UICONTROL Remove]** .
      * Schakelen **[!UICONTROL Request]** naar **[!UICONTROL Response]** .
      * Voer &quot;X-Frame-Opties&quot; in als koptekst.
      * Herhaal de vorige stappen en voer &quot;x-frame-options&quot; in als koptekst.

        >[!NOTE]
        >
        >Kopteksten die via [!DNL Requestly] worden gemanipuleerd, zijn hoofdlettergevoelig.

      * Wijzig **[!UICONTROL Equals]** in **[!UICONTROL Contains]** als de voorwaarde voor de bron-URL en voer de URL in van de activiteit die u wilt laden in de VEC.

     ![&#x200B; chroom_extension beeld &#x200B;](assets/chrome_extension.png)

1. Klik op **[!UICONTROL Save]**.

   ![&#x200B; vaak beeld &#x200B;](assets/requestly.png)

   U moet nu de pagina snel kunnen laden met de [!UICONTROL Visual Experience Composer] .

**om de [!DNL Modify Response Headers] uitbreiding op [!UICONTROL Firefox] te gebruiken:**

1. Installeer de lus [!UICONTROL Modify Response Headers] on [!DNL Firefox] en start de browser opnieuw.
1. Selecteer in uw [!DNL Firefox] -extensies de extensie Responsheaders wijzigen.
1. Klik op **[!UICONTROL Preferences]**.
1. Selecteer **[!UICONTROL Filter]** in de vervolgkeuzelijst [!UICONTROL Action] .
1. Typ in het veld [!UICONTROL Header Name] : **[!UICONTROL X-Frame-Options]** .
1. Herhaal stap 4 en 5 om een filter toe te voegen met **[!UICONTROL x-frame-options]** .
1. Klik op **[!UICONTROL Add]**.
1. Klik op **[!UICONTROL Start]**.

![&#x200B; uitbreiding Firefox &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox_extension.png)

Open [!DNL Target] nadat u een extensie hebt ingesteld. De pagina&#39;s moeten nu in de [!UICONTROL Visual Experience Composer] worden geladen, zelfs als de [!UICONTROL Enhanced Experience Composer] is uitgeschakeld.

+++

## Mijn pagina wordt niet weergegeven in de VEC (alleen VEC) {#does-not-load}

+++Details
* De beste compatibiliteit met VEC wordt gegarandeerd door de nieuwste versie van de extensie: [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper extension]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) .

  Als u wilt controleren of u de meest recente versie gebruikt, gaat u naar [!UICONTROL Extensions] > [!UICONTROL Manage Extensions] en klikt u op [!UICONTROL Details] .

* [!UICONTROL Visual Experience Composer] vereist auteursbibliotheken om wijzigingen op de Web-pagina uit te voeren. Deze bibliotheken zijn ingesloten in de bibliotheek at.js en worden door de extensie van [!DNL Adobe] -servers gedownload wanneer VEC wordt gebruikt.

  De extensie downloadt de bibliotheek at.js, ongeacht of at.js of [!DNL Adobe Experience Platform Web SDK] al in de pagina is opgenomen.

  Controleer of er geen ongeldige wijzigingen zijn toegevoegd aan de headers van at.js die zijn geconfigureerd in de sectie [!UICONTROL Administration] > [!UICONTROL Implementation] .

* Zorg ervoor dat de webpagina geen aanvragen blokkeert die verplicht moeten worden geladen wanneer deze zijn ingesloten in een iFrame. Dit omvat het gebruik van CSP-richtlijnen of aangepaste JS-code van framevoorouders die zijn ingesloten in de website van de klant, HTML-tags van meta of de header x-frame-options.

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
* Als uw website niet in de VEC kan worden geladen of zich onverwacht gedraagt, kunt u cookies op uw website in de browser accepteren voordat u probeert de website te laden in [!DNL Target] .

+++

## De VEC wordt verbroken weergegeven wanneer ik de modus [!UICONTROL Browse] gebruik. (alleen VEC) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

+++Details
Terwijl het gebruiken van [!UICONTROL Browse] wijze, als u tot een URL toegang hebt die [!DNL Target] uitgevoerde bibliotheken ([&#x200B; at.js &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} of [&#x200B; Adobe Experience Platform Web SDK &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}) niet heeft of een kader-Buster kopbal bevat, lijkt VEC gebroken. Vanwege beveiligingsproblemen in de browser heeft [!DNL Target] geen toegang tot de URL waarnaar u hebt genavigeerd of wordt de VEC-URL niet consistent bijgewerkt als de pagina wordt geladen.

Dit probleem doet zich voor omdat VEC de webpagina in een `<iframe>` laadt. De huidige beveiligingsmechanismen van browsers verhinderen dat de gebruikersinterface van [!DNL Target] toegang krijgt tot de elementen van het opgegeven frame vanwege het beleid van dezelfde oorsprong. Browsers blokkeren scripts die toegang proberen te krijgen tot een frame met een andere oorsprong en die informatie bevatten zoals de `location.href` .

U moet de nieuwe [&#x200B; Visuele het Uitgeven uitbreiding van de Helper &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) gebruiken om de [!DNL Target] bibliotheek in de pagina&#39;s in te spuiten om hen optimaal te doorbladeren.

+++

## Problemen veroorzaakt door CSS-conflicten in de [!UICONTROL Visual Experience Composer]

+++Details
Controleer of er CSS-bestanden zijn die invloed hebben op de zichtbaarheid tijdens het laden van de webpagina in de editor. Als u bijvoorbeeld de eigenschap `overflow: hidden` op de hoofdtekst van de pagina gebruikt, kan dit leiden tot schuifproblemen of kunnen klikgebeurtenissen activeren die het menu voor het schrijven van documenten kunnen beïnvloeden.

+++
