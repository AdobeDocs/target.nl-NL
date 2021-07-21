---
keywords: gericht;visuele ervaringscomposer;whitelist;witte lijst;lijst van gewenste personen;lijst van gewenste personen;verbeterde visuele ervaringscomposer;vec;los visuele ervaringscomposer problemen op;het oplossen van problemen;eec;verbeterde ervaringscomposer;tls 1.2
description: Leer hoe te om problemen problemen op te lossen die soms in Adobe [!DNL Target] Visual Experience Composer (VEC) en Verbeterde Composer van de Ervaring (EEC) onder bepaalde voorwaarden voorkomen.
title: Hoe los ik kwesties met betrekking tot Visual Experience Composer en Verbeterde Composer van de Ervaring problemen op?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: 068cce681946382365049fdc69671cd011431201
workflow-type: tm+mt
source-wordcount: '1477'
ht-degree: 0%

---

# Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer

Weergaveproblemen en andere problemen doen zich soms voor in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) en [!UICONTROL Enhanced Experience Composer] (EEC) onder bepaalde omstandigheden.

## Hoe beïnvloedt het Google Chrome SameSite-beleid voor de handhaving van cookies de VEC en EEC? {#samesite}

Met de aanstaande veranderingen die voor de Versie van Chrome 94 (21 September, 2021) worden gepland, beïnvloedt de volgende verandering alle gebruikers met Chrome 94+ browser versies:

* De opdrachtregelmarkering `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wordt verwijderd.

Met de wijzigingen die zijn geïmplementeerd voor de Chrome 91-release (25 mei 2021), is de volgende wijziging van invloed op alle gebruikers met Chrome 91+-browserversies:

* De markeringen `#same-site-by-default-cookies` en `#cookies-without-same-site-must-be-secure` zijn verwijderd uit `chrome://flags`. Dit gedrag is nu standaard ingeschakeld.

Met de veranderingen die in Augustus 2020 worden uitgevoerd, alle gebruikers met Chrome 80+ browser versies:

* Zal *niet* VEC (met of zonder de geïnstalleerde en toegelaten uitbreiding van de Helper VEC) in wachtwoord-beschermde pagina&#39;s van hun plaatsen kunnen gebruiken. De aanmeldcookies van uw site worden beschouwd als een cookie van een andere fabrikant en worden samen met de aanmeldingsaanvraag verzonden. De enige uitzondering is wanneer voor het aanmeldcookie van de site de parameter SameSite al is ingesteld op &quot;none&quot;.
* *niet* kan [!DNL Target] bibliotheken downloaden tijdens het bewerken van een activiteit (als deze nog niet op de site staan). Dit is omdat de downloadvraag van het klantendomein aan een beveiligd Adobe domein wordt gemaakt en als unauthenticated wordt verworpen.
* De E.E.G. zal *niet* functie voor alle gebruikers omdat het niet het attribuut SameSite voor koekjes op `adobemc.com domain` kan plaatsen. Zonder dit kenmerk weigert de browser deze cookies, waardoor de EEG mislukt.

Gebruik de Developer Tools in Chrome om te controleren welke cookies zijn geblokkeerd vanwege het beleid voor het toepassen van cookies op de SameSite.

1. Om tot de Hulpmiddelen van de Ontwikkelaar toegang te hebben, terwijl het bekijken van VEC in Chrome, klik het **[!UICONTROL ellipsis]** pictogram bij de hoger-juiste hoek van Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]**.
1. Klik op het tabblad **[!UICONTROL Network]** en zoek op geblokkeerde cookies.

   In de volgende afbeelding ziet u een geblokkeerde cookie:

   ![Gereedschappen voor ontwikkelaars > tabblad Netwerk waarop een geblokkeerd cookie wordt weergegeven](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/chrome-developer-tools.png)

Adobe heeft een bijgewerkte VEC Helper-extensie ingediend bij de Google Chrome Store. Deze extensie overschrijft de cookie-kenmerken om, indien nodig, het `SameSite="none"`-kenmerk in te stellen. De [bijgewerkte extensie vindt u hier](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en). Voor meer informatie over het installeren van en het gebruiken van de Uitbreiding van de Helper VEC, zie [de helperuitbreiding van de Composer van de Visuele Ervaring](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

Voor uw eigen sitecookies moet u de cookies op naam opgeven.

>[!NOTE]
>
>Deze aanpak is alleen geschikt wanneer alle cookies in één domein zijn ingesteld. De hulp VEC staat [!DNL Target] niet toe om koekjes voor meer dan één domein te specificeren.

Schakel de schuifregelaar [!UICONTROL Cookie] in op de aan-positie en geef vervolgens de cookie op naam en het cookiedomein op. De cookienaam is &quot;mbox&quot;en het koekjesdomein is de tweede en hoogste niveaus van de domeinen waarvan u mbox dient. Omdat het van het domein van uw bedrijf wordt gediend, is het koekje een eerste partijkoekje. Voorbeeld: `mycompany.com`. Voor meer informatie, zie [Adobe Target Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html) in *de Gids van de Gebruiker van de Interface van de Experience Cloud*.

![Kookies in de VEC helperuitbreiding](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

### Alternatieven en tijdelijke oplossingen

Gebruik één van de volgende opties om ervoor te zorgen dat uw VEC en EEG blijven werken zoals verwacht:

* Download en gebruik de bijgewerkte [VEC Helper extension](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en).
* Gebruik de browser Mozilla Firefox. Firefox voert dit beleid nog niet uit.
* Gebruik de volgende markeringen om Google Chrome uit te voeren vanaf de opdrachtregel tot 21 september 2021. Na 21 september werkt uw website niet meer in de VEC. Als u Chrome 94 bijwerkt, moet u cookies handmatig genereren met `SameSite=none` en `Secure` op uw websites.

   ```
   --disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure
   ```

## Biedt [!DNL Target] ondersteuning voor iframes op meerdere niveaus?

[!DNL Target] biedt geen ondersteuning voor iframes met meerdere niveaus. Als uw website een iframe laadt dat een onderliggend iframe heeft, heeft at.js alleen invloed op het bovenliggende iframe. [!DNL Target] bibliotheken hebben geen interactie met het onderliggende iframe.

Als tussenoplossing kunt u een pagina toevoegen in de ervaring met de URL van het onderliggende iframe.

## Wanneer ik een pagina probeer te bewerken, zie ik alleen een spinner in plaats van mijn pagina. (VEC en EEG) {#section_313001039F79446DB28C70D932AF5F58}

Deze situatie kan zich voordoen als de URL een #-teken bevat. Om de kwestie te bevestigen, schakelaar op Browse wijze in de Visuele Composer van de Ervaring, en dan terug te schakelen om wijze samen te stellen. De spinner moet weggaan en de pagina moet worden geladen.

## De kopballen van het Beleid van de Veiligheid van de inhoud (CSP) blokkeren de [!DNL Target] bibliotheken op mijn website. (VEC en EEG) {#section_89A30C7A213D43BFA0822E66B482B803}

Als de CSP-headers van uw website de doelbibliotheken blokkeren, wordt de website geladen, maar wordt het bewerken voorkomen, zorgt u ervoor dat de doelbibliotheken niet worden geblokkeerd.

>[!NOTE]
>
>Naast de volgende informatie kunt u de [Adobe Target VEC Helper browser extensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor Google Chrome gebruiken.

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

Als dezelfde DOM-element-id wordt gebruikt op meerdere elementen op de pagina en u een van deze elementen wijzigt, worden alle elementen met die id gewijzigd. Om dit te voorkomen, zou een identiteitskaart slechts eenmaal op elke pagina moeten worden gebruikt. Dit is een standaard beste HTML-praktijk. Zie [Paginawijzigingsscenario&#39;s](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB) voor meer informatie.

## Ik kan geen ervaringen bewerken voor een iFrame-opbouwende site. (VEC en EEG) {#section_9FE266B964314F2EB75604B4D7047200}

Dit probleem kan worden opgelost door de Enhanced Experience Composer in te schakelen. Klik op **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]** en schakel vervolgens het selectievakje in waarmee de Enhanced Experience Composer wordt ingeschakeld. De Enhanced Experience Composer gebruikt een proxy met Adobe-beheer om uw pagina te laden voor bewerken. Met deze proxy kunt u sites bewerken op iFrame en kunt u deze bewerken op sites en pagina&#39;s waar u nog geen Adobe Target-code hebt toegevoegd. De activiteiten leveren niet aan de plaats tot de code is toegevoegd. Sommige sites worden mogelijk niet geladen via de Enhanced Experience Composer. In dat geval kunt u deze optie uitschakelen om de Visual Experience Composer via een iFrame te laden.

>[!NOTE]
>
>De lokaal gehoste pagina&#39;s of pagina&#39;s die niet toegankelijk zijn buiten uw netwerk, zijn niet toegankelijk voor de Adobe-proxyserver en kunnen niet worden geopend in de EEG. Deze pagina&#39;s kunnen URL&#39;s in fasen, UAT-URL&#39;s (User Acceptance Testing) of lokaal gehoste pagina&#39;s bevatten.

## Ik wil tests opzetten op pagina&#39;s die mbox/doelimplementatie nog niet hebben gedaan. (VEC en EEG) {#section_DE63BCCB5B124E10A71FA579B582A80A}

Zie &quot;Ik kan bovenstaande ervaringen voor een iFrame-bursting site niet bewerken&quot;.

## Vette en cursieve tekststijlen met Tekst bewerken/HTML of Tekst wijzigen/HTML worden niet op mijn pagina weergegeven. Soms verdwijnt de tekst na het toepassen van deze stijlwijzigingen. (VEC en EEG) {#section_7A71D6DF41084C58B34C18701E8774E5}

Als u **[!UICONTROL Edit Text/HTML]** in de Composer van de Visuele Ervaring voor A/B of Ervaring richt activiteiten of **[!UICONTROL Change Text/HTML]** voor Automated Personalization of Multivariate de activiteiten van de Test gebruikt om tekst vet of cursief te maken, zouden die stijlen niet op de pagina kunnen worden toegepast of de tekst verdwijnt van de pagina in Visual Experience Composer. Dit gebeurt als gevolg van de manier waarop de RTF-editor deze stijlen toepast, waardoor de markering van de website mogelijk wordt beïnvloed.

Als u dit probleem ziet:

1. Klik op de knop **[!UICONTROL HTML]** in de RTF-editor om de bronbewerkingsmodus te activeren.
1. Zoek de tekstelementen voor stijlen.

   * Wijzig `<strong>`-elementen voor vette tekst in `<b>`.

   * Wijzig `<em>`-elementen voor cursieve tekst in `<i>`.

## Bij Automated Personalization-activiteiten wordt het wisselen van afbeeldingen in de VEC of EEC verbroken. (VEC en EEG) {#section_88AABFDFE6A3420299B0D508B12A3994}

Als u een afbeeldingsaanbieding aan een locatie toevoegt, krijgt de oorspronkelijke afbeeldingsruimte in VEC of EEC de volledige grootte. Bij levering wordt de afbeelding niet uitgevouwen en wordt deze weergegeven zoals deze is, zodat er geen invloed is op de levering.
