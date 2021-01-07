---
keywords: Targeting;visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;tls;tls 1.2
description: Weergaveproblemen treden soms onder bepaalde omstandigheden op in de Adobe Target Visual Experience Composer (VEC).
title: Problemen oplossen met betrekking tot Visual Experience Composer
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 0%

---


# Problemen met de Visual Experience Composer oplossen

Weergaveproblemen treden soms op in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) onder bepaalde omstandigheden.

## Wanneer ik mijn website in de Visuele Composer van de Ervaring open, laden de bibliotheken van het Doel niet. (Alleen VEC) {#section_8A7D3F4AD2CC4C3B823EE9432B97E06F}

Doel voegt twee parameters toe (`mboxEdit=1` en `mboxDisable=1`) terwijl het openen van de website in de Composer van de Visuele Ervaring.

Als uw website (met name Apps met één pagina) uw parameters bijsnijdt of deze verwijdert terwijl u van de ene pagina naar de andere navigeert (zonder dat de pagina opnieuw wordt geladen), wordt de functie Doel verbroken en worden de doelbibliotheken niet geladen.
U voorkomt dit probleem door deze twee parameters niet bij te snijden of te verwijderen.

## Mijn pagina wordt niet geopend in de EEG, of wordt langzaam geladen. Activiteiten of ervaringen laden langzaam in de VEC. (Alleen VEC) {#section_71E7601BE9894E3DA3A7FBBB72B6B0C1}

Verschillende problemen kunnen van invloed zijn op de paginaprestaties in de doelervaringscomposers. Enkele veelvoorkomende problemen zijn:

* U hebt geen box op de pagina.
* Uw site gebruikt proxyblokkering, waardoor de pagina in geen van beide composers kan worden geopend.
* Uw site staat het openen van een iFrame niet toe.

Als er problemen optreden in de Enhanced Experience Composer, kunt u de Enhanced Experience Composer uitschakelen en in plaats daarvan de Visual Experience Composer gebruiken.

Als u de Enhanced Experience Composer wilt uitschakelen, gaat u naar **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]** en schakelt u de optie **[!UICONTROL Enable Enhanced Experience Composer]** uit.

Sommige gebruikers zien het volgende foutbericht in de console:

![Foutbericht voor console](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/console_error_message.jpg)

Als noch Composer van de Visuele Ervaring noch de Verbeterde Composer van de Ervaring werkt, gebruik een browser uitbreiding zoals (Chrome of Firefox) of wijzigt de Kopballen van de Reactie (Firefox) die de X-Kaders kopbalopties voor uw plaats kan overschrijven en hen om in iFrames toelaat worden geladen, toelatend VEC. Als u geen browserextensies kunt gebruiken, gebruikt u de Form Composer.

>[!NOTE]
>
>Naast de volgende informatie kunt u de [Adobe Target VEC Helper browser extensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor Google Chrome gebruiken.


>[!NOTE]
>
>Deze plug-ins mogen alleen worden gebruikt in de context van VEC-bewerking.
>
>Voor de extensie &quot;strikt vereist&quot; moet u een van de volgende handelingen uitvoeren wanneer er headers moeten worden verwijderd:
>
>* Voeg URL-regels toe voor de URL die u in de VEC wilt openen, zodat kopteksten alleen voor die URL&#39;s worden verwijderd.
   >
   >
* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.
>
>
Voor de Modify Header uitbreiding (Firefox) van de Reactie, omdat u geen URL regel kunt toevoegen, moet u het volgende doen:
>
>* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.


**De extensie Vereisen gebruiken op Chrome of Firefox:**

1. Schakel de Enhanced Experience Composer uit.
1. Installeer de gewenste browserextensie op Chrome of Firefox.
1. Open de extensie en configureer deze als volgt:
1. Selecteer **[!UICONTROL Modify headers]**.
1. Voer het volgende in:

   * Naam van regel
   * Wijzigingsvoorschriften

      * Schakelen tussen **[!UICONTROL Add]** en **[!UICONTROL Remove]**.
      * Schakelen tussen **[!UICONTROL Request]** en **[!UICONTROL Response]**.
      * Voer &quot;X-Frame-Opties&quot; in als koptekst.
      * Herhaal de vorige stappen en voer &quot;x-frame-options&quot; in als koptekst.

         >[!NOTE]
         >
         >Kopteksten die worden gemanipuleerd via Requely zijn hoofdlettergevoelig.

      * Wijzig **[!UICONTROL Equals]** in **[!UICONTROL Contains]** als voorwaarde voor de bron-URL en voer de URL in van de activiteit die u in de VEC wilt laden.

      ![](assets/chrome_extension.png)


1. Klik op **[!UICONTROL Save]**.

   ![](assets/requestly.png)

   U zou de pagina met Visual Experience Composer nu moeten kunnen snel laden.

**De extensie Responsheaders wijzigen in Firefox gebruiken:**

1. Installeer de Modify Kopballen van de Reactie op Firefox en begin browser opnieuw.
1. Selecteer in uw Firefox-extensies de extensie Responsheaders wijzigen.
1. Klik op **[!UICONTROL Preferences]**.
1. Selecteer **[!UICONTROL Filter]** in de vervolgkeuzelijst Handeling.
1. Voer in het veld Naam koptekst het volgende in: **[!UICONTROL X-Frame-Options]**.
1. Herhaal stap 4 en 5 om een filter toe te voegen met **[!UICONTROL x-frame-options]**.
1. Klik op **[!UICONTROL Add]**.
1. Klik op **[!UICONTROL Start]**.

![](assets/firefox_extension.png)

Open Target nadat u een extensie hebt ingesteld. De pagina&#39;s moeten nu worden geladen in de composer voor visuele ervaring, zelfs als de composer voor verbeterde ervaring is uitgeschakeld.

## Mijn pagina wordt niet weergegeven in de VEC (alleen VEC) {#section_87B3BEA4B6174CFDA6C9A69A1A051FA1}

* De browser wordt niet ondersteund.
* De browser blokkeert een niet-beveiligde pagina op een beveiligde site.

   Klik op het pictogram links van de URL in de adresbalk van de browser en klik op **[!UICONTROL Disable protection on this page]**
* U hebt een ongeldige URL ingevoerd.
* U hebt geen standaard-URL ingevoerd op de pagina voor het instellen van uw account.

Zorg ervoor dat deze instelling is ingeschakeld en download en werk mbox.js op uw website bij.

## De VEC wordt verbroken weergegeven wanneer ik de modus Bladeren gebruik. (Alleen VEC) {#section_FA2A18E8FD6A4274B2E395DBAA2FB407}

Wanneer het gebruiken doorbladert wijze, als u tot een URL toegang hebt die target.js niet heeft of een kader-busterkopbal bevat, lijkt de Visuele Composer van de Ervaring gebroken. Vanwege beveiligingsproblemen in de browser heeft Target geen toegang tot de URL waarnaar u bent genavigeerd.
