---
keywords: gericht;visuele ervaringscomposer;whitelist;witte lijst;lijst van gewenste personen;lijst van gewenste personen;verbeterde visuele ervaringscomposer;vec;los visuele ervaringscomposer problemen op;het oplossen van problemen;eec;verbeterde ervaringscomposer;tls 1.2
description: Leer hoe te om problemen op te lossen die soms in de Adobe voorkomen [!DNL Target] Visual Experience Composer (VEC) en Enhanced Experience Composer (EEC) onder bepaalde omstandigheden.
title: Hoe los ik kwesties met betrekking tot Visual Experience Composer en Verbeterde Composer van de Ervaring problemen op?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: cf8bb1a438681ccb5bf9e825503f9f929fbcfdbf
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---

# Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer

Weergaveproblemen en andere problemen doen zich soms voor in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) en de [!UICONTROL Enhanced Experience Composer] (EEG) onder bepaalde voorwaarden.

## Hoe beïnvloedt het Google Chrome SameSite cookie handhavingsbeleid VEC en EEC? {#samesite}

Wees op de hoogte van de wijzigingen die van invloed zijn op de VEC en de EEG wanneer u de volgende Chrome-releases gebruikt:

>[!NOTE]
>
>De volgende wijziging is van invloed op de drie updates die hieronder worden beschreven:
>
> * Will *niet* U kunt de VEC gebruiken zonder de extensie VEC Helper geïnstalleerd en ingeschakeld voor pagina&#39;s van uw sites die met een wachtwoord zijn beveiligd. De aanmeldcookies van uw site worden beschouwd als cookies van derden en worden niet verzonden met aanmeldingsaanvragen in de VEC-editor in de modus Bladeren. De enige uitzondering is wanneer uw aanmeldcookies voor de site al beschikken over de `SameSite=None` en `Secure` attributen set.


**Chrome 94 (21 september 2021)**: Met de aanstaande veranderingen die voor de Versie van Chrome 94 (21 September, 2021) worden gepland, beïnvloedt de volgende verandering alle gebruikers met Chrome 94+ browser versies:

* De opdrachtregelmarkering `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wordt verwijderd.

**Chrome 91 (25 mei 2021)**: Met de wijzigingen die zijn geïmplementeerd voor de Chrome 91-release (25 mei 2021), is de volgende wijziging van invloed op alle gebruikers met Chrome 91+-browserversies:

* De markeringen `#same-site-by-default-cookies` en `#cookies-without-same-site-must-be-secure` zijn verwijderd uit `chrome://flags`. Dit gedrag is nu standaard ingeschakeld.

**Chrome 80 (augustus 2020)**: Met de veranderingen die in Augustus 2020 worden uitgevoerd, alle gebruikers met Chrome 80+ browser versies:

* Will *niet* kunnen downloaden [!DNL Target] bibliotheken tijdens het bewerken van een activiteit (als deze nog niet op de site staan). Dit is omdat de downloadvraag van het klantendomein aan beveiligd wordt gemaakt [!DNL Adobe] en wordt afgewezen als niet-geverifieerd.
* De EEG *niet* functies voor alle gebruikers omdat het niet in staat is het kenmerk SameSite voor cookies in te stellen op `adobemc.com domain`. Zonder dit kenmerk weigert de browser deze cookies, waardoor de EEG mislukt.

### Bepalen welke cookies worden geblokkeerd

Gebruik de Developer Tools in Chrome om te bepalen welke cookies worden geblokkeerd vanwege het beleid voor het toepassen van SameSite-cookies.

1. Om tot de Hulpmiddelen van de Ontwikkelaar toegang te hebben, terwijl het bekijken van VEC in Chrome, klik **[!UICONTROL ellipsis]** pictogram in de rechterbovenhoek van Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]**.
1. Klik op de knop **[!UICONTROL Network]** > zoekt vervolgens naar geblokkeerde cookies.

   >[!NOTE]
   >
   >Gebruik de **[!UICONTROL Has blocked cookies]** Schakel het selectievakje in om geblokkeerde cookies gemakkelijker te vinden.

   In de volgende afbeelding ziet u een geblokkeerde cookie:

   ![Gereedschappen voor ontwikkelaars > tabblad Netwerk waarop een geblokkeerd cookie wordt weergegeven](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

### [!DNL Adobe Target] VEC Helper-extensie

Vanaf versie 0.7.1 worden de [!DNL Adobe Target] VEC Helper browser-extensie voegt de extensie `SameSite=None` en `Secure` kenmerken voor alle cookies op reacties die afkomstig zijn van webpagina&#39;s die in de VEC zijn bewerkt wanneer de schakeloptie &quot;Cookies&quot; is ingeschakeld in de gebruikersinterface van de extensie:

![Adobe Target VEC Helper-extensie UIAdobe Target VEC Helper-extensie UI](assets/cookies-vec-helper.png)

### Alternatieven en tijdelijke oplossingen

Gebruik één van de volgende opties om ervoor te zorgen dat uw VEC en EEG blijven werken zoals verwacht:

* De bijgewerkte versie downloaden en gebruiken [VEC Helper-extensie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en).
* Gebruik de browser Mozilla Firefox. Firefox voert dit beleid nog niet uit.
* Gebruik de volgende markeringen om Google Chrome uit te voeren vanaf de opdrachtregel tot 21 september 2021. Na 21 september werken functies die cookies vereisen niet meer in de VEC, zoals aanmeldings- of cookie-acceptatie-popups. Als u een update naar Chrome 94 uitvoert, moet u cookies handmatig genereren met `SameSite=none` en `Secure` op uw websites.

   ```
   --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
   ```

## doet [!DNL Target] iframes op meerdere niveaus ondersteunen?

[!DNL Target] biedt geen ondersteuning voor iframes met meerdere niveaus. Als uw website een iframe laadt dat een onderliggend iframe heeft, heeft at.js alleen invloed op het bovenliggende iframe. [!DNL Target] bibliotheken hebben geen interactie met het onderliggende iframe.

Als tussenoplossing kunt u een pagina toevoegen in de ervaring met de URL van het onderliggende iframe.

## Wanneer ik een pagina probeer te bewerken, zie ik alleen een spinner in plaats van mijn pagina. (VEC en EEG) {#section_313001039F79446DB28C70D932AF5F58}

Deze situatie kan zich voordoen als de URL een #-teken bevat. Om de kwestie te bevestigen, schakelaar op Browse wijze in de Visuele Composer van de Ervaring, en dan terug te schakelen om wijze samen te stellen. De spinner moet weggaan en de pagina moet worden geladen.

## De kopballen van het Beleid van de Veiligheid van de inhoud (CSP) blokkeren [!DNL Target] bibliotheken op mijn website. (VEC en EEG) {#section_89A30C7A213D43BFA0822E66B482B803}

Als de CSP-headers van uw website de doelbibliotheken blokkeren, wordt de website geladen, maar wordt het bewerken voorkomen, zorgt u ervoor dat de doelbibliotheken niet worden geblokkeerd.

>[!NOTE]
>
>Naast de volgende informatie kunt u de opdracht [Adobe Target VEC Helper-browserextensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor Google Chrome.

![](assets/cps_headers.png)

Als tussenoplossing kunt u een regel Vraagbaar configureren om CSP-koppen te verwijderen, zoals hieronder wordt weergegeven:

![](assets/cps_headers_2.png)

U kunt een gelijkaardige Vergelijkbare regel voor om het even welke kopbal vormen die een middel ertoe leidt om niet binnen VEC te laden.

Wanneer het nodig is headers te verwijderen, moet u voor Standaard een van de volgende handelingen uitvoeren:

* Voeg URL-regels toe voor de URL die u in de VEC wilt openen, zodat kopteksten alleen voor die URL&#39;s worden verwijderd.
* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.

## VEC of EEC lijkt gebroken of initialiseert niet wanneer het heruitgeven van een bewaarde activiteit. (VEC en EEG) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

Als de website buiten Visual Experience Composer is veranderd nadat de ervaring werd bepaald, kunnen de selecteurs waarop de acties vroeger werden genomen niet worden gevonden wanneer de activiteit voor het heruitgeven wordt geopend. De pagina wordt verbroken weergegeven en er wordt geen waarschuwing weergegeven.

## In de VEC of EEC worden mijn roterende banners en andere inhoud met JavaScript niet weergegeven. (VEC en EEG) {#section_8B5BE6EB050B42D6A14A054724C41330}

Standaard blokkeert de Visual Experience Composer JavaScript-elementen. U kunt met deze elementen werken als u JavaScript in de montages van Composer van de Visuele Ervaring onbruikbaar maakt. Afhankelijk van de manier waarop de site is ingesteld, worden sommige items mogelijk onjuist weergegeven of blijven ze niet beschikbaar.

## Wanneer ik één element op de pagina verander, veranderen de veelvoudige elementen. (VEC en EEG) {#section_309188ACF34942989BE473F63C5710AF}

Als dezelfde DOM-element-id wordt gebruikt op meerdere elementen op de pagina en u een van deze elementen wijzigt, worden alle elementen met die id gewijzigd. Om dit te voorkomen, zou een identiteitskaart slechts eenmaal op elke pagina moeten worden gebruikt. Dit is een standaard beste HTML-praktijk. Zie voor meer informatie [Paginawijzigingsscenario&#39;s](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Ik kan geen ervaringen bewerken voor een iFrame-opbouwende site. (VEC en EEG) {#section_9FE266B964314F2EB75604B4D7047200}

Dit probleem kan worden opgelost door de Enhanced Experience Composer in te schakelen. Klikken **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]** schakelt u het selectievakje Enhanced Experience Composer in. De Enhanced Experience Composer gebruikt een proxy met Adobe-beheer om uw pagina te laden voor bewerken. Met deze proxy kunt u sites bewerken op iFrame en kunt u deze bewerken op sites en pagina&#39;s waar u nog geen Adobe Target-code hebt toegevoegd. De activiteiten leveren niet aan de plaats tot de code is toegevoegd. Sommige sites worden mogelijk niet geladen via de Enhanced Experience Composer. In dat geval kunt u deze optie uitschakelen om de Visual Experience Composer via een iFrame te laden.

>[!NOTE]
>
>De lokaal gehoste pagina&#39;s of pagina&#39;s die niet toegankelijk zijn buiten uw netwerk, zijn niet toegankelijk voor de Adobe-proxyserver en kunnen niet worden geopend in de EEG. Deze pagina&#39;s kunnen URL&#39;s in fasen, UAT-URL&#39;s (User Acceptance Testing) of lokaal gehoste pagina&#39;s bevatten.

## Ik wil tests opzetten op pagina&#39;s die mbox/doelimplementatie nog niet hebben gedaan. (VEC en EEG) {#section_DE63BCCB5B124E10A71FA579B582A80A}

Zie &quot;Ik kan bovenstaande ervaringen voor een iFrame-bursting site niet bewerken&quot;.

## Vette en cursieve tekststijlen met Tekst/HTML bewerken of Tekst/HTML wijzigen worden niet op mijn pagina weergegeven. Soms verdwijnt de tekst na het toepassen van deze stijlwijzigingen. (VEC en EEG) {#section_7A71D6DF41084C58B34C18701E8774E5}

Als u **[!UICONTROL Edit Text/HTML]** in de Visual Experience Composer voor A/B of Experience Targeting Activiteiten of **[!UICONTROL Change Text/HTML]** voor Automated Personalization of Multivariate Test-activiteiten om tekst vet of cursief te maken, worden deze stijlen mogelijk niet toegepast op de pagina of verdwijnt de tekst van de pagina in Visual Experience Composer. Dit gebeurt als gevolg van de manier waarop de RTF-editor deze stijlen toepast, waardoor de markering van de website mogelijk wordt beïnvloed.

Als u dit probleem ziet:

1. Klik op de knop **[!UICONTROL HTML]** in de RTF-editor om de bronbewerkingsmodus te activeren.
1. Zoek de tekstelementen voor stijlen.

   * Voor vetgedrukte tekst wijzigt u `<strong>` elementen naar `<b>`.

   * Voor cursieve tekst wijzigen `<em>` elementen naar `<i>`.

## Bij Automated Personalization-activiteiten wordt het wisselen van afbeeldingen in de VEC of EEC verbroken. (VEC en EEG) {#section_88AABFDFE6A3420299B0D508B12A3994}

Als u een afbeeldingsaanbieding aan een locatie toevoegt, krijgt de oorspronkelijke afbeeldingsruimte in VEC of EEC de volledige grootte. Bij levering wordt de afbeelding niet uitgevouwen en wordt deze weergegeven zoals deze is, zodat er geen invloed is op de levering.
