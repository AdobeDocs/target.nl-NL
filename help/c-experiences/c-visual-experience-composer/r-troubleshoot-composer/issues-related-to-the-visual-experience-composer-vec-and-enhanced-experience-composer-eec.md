---
keywords: Targeting;visual experience composer;whitelist;white list;allowlist;allow list;enhanced visual experience composer;vec;troubleshoot visual experience composer;troubleshooting;eec;enhanced experience composer;tls;tls 1.2
description: Weergaveproblemen doen zich soms onder bepaalde omstandigheden voor in de Visual Experience Composer (VEC) en de Enhanced Experience Composer (EEC).
title: Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer
feature: vec
uuid: 93f646d9-fcbc-43f0-9f84-0ce8e486ff7f
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 0%

---


# Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer{#troubleshooting-issues-related-to-the-visual-experience-composer-and-enhanced-experience-composer}

Weergaveproblemen en andere problemen doen zich soms onder bepaalde omstandigheden voor in de Visual Experience Composer (VEC) en de Enhanced Experience Composer (EEC).

## Hoe beïnvloedt het onlangs aangekondigde beleid van Google Chrome SameSite voor de handhaving van cookies de VEC en EEC? {#samesite}

Met de recentste veranderingen (Augustus 2020), alle gebruikers met Chrome 80+ browser versies:

* De VEC (met of zonder de VEC Helper-extensie geïnstalleerd en ingeschakeld) kan *niet* worden gebruikt op pagina&#39;s van hun sites die met een wachtwoord zijn beveiligd. De reden hiervoor is dat hun aanmeldcookie(s) voor de site als een cookie van een andere fabrikant worden beschouwd en niet samen met de aanmeldingsaanvraag worden verzonden. De enige uitzondering is wanneer voor het aanmeldingscookie van de site van de klant al de parameter SameSite is ingesteld op &quot;none&quot;.
* Bibliotheken kunnen *niet* [!DNL Target] worden gedownload tijdens het bewerken van een activiteit (als deze nog niet op de site staan). Dit is omdat de downloadvraag van het klantendomein aan een beveiligd Adobe domein wordt gemaakt en als unauthenticated wordt verworpen.
* De E.E.G. werkt *niet* voor alle gebruikers omdat het niet het attribuut SameSite voor koekjes op kan plaatsen `adobemc.com domain`. Zonder dit kenmerk zal de browser deze cookies negeren, waardoor de EEG mislukt.

Adobe heeft een bijgewerkte VEC Helper-extensie ingediend bij de Google Chrome Store. Deze extensie overschrijft de cookie-kenmerken om het `SameSite="none"` kenmerk zo nodig in te stellen. De [bijgewerkte extensie vindt u hier](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en). Voor meer informatie over het installeren van en het gebruiken van de Uitbreiding van de Helper VEC, zie de helperuitbreiding [van Composer van de](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md)Visuele Ervaring.

Voor uw eigen sitecookies moet u de cookies op naam opgeven. Schakel de [!UICONTROL Cookie] schuifregelaar in of uit naar de aan-positie en geef vervolgens de cookie op naam en het cookiedomein op. De cookienaam is &quot;mbox&quot;en het koekjesdomein is de tweede en hoogste niveaus van de domeinen waarvan u mbox dient. Omdat het van het domein van uw bedrijf wordt gediend, is het koekje een eerste partijkoekje. Voorbeeld: `mycompany.com`. Zie [Adobe Target Cookies](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-target.html) in de gebruikershandleiding *van de* Experience Cloud Interface voor meer informatie.

![Kookies in de VEC helperuitbreiding](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

### Alternatieven en tijdelijke oplossingen

Gebruik één van de volgende opties om ervoor te zorgen dat uw VEC en EEG blijven werken zoals verwacht:

* Download en gebruik de bijgewerkte [VEC Helper-extensie](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak?hl=en).
* Gebruik de browser Mozilla Firefox. Firefox voert dit beleid nog niet uit.
* Blijf Chrome gebruiken, maar stel de `chrome://flags/#same-site-by-default-cookies` markering in op &quot;Uitgeschakeld&quot;.

   >[!NOTE]
   >
   >Dit is *niet* genoeg als cookies al het SameSite-kenmerk op &quot;Lax&quot; of &quot;Strikt&quot; van de server zijn ingesteld.

## Biedt het Doel ondersteuning voor iframes op meerdere niveaus?

Doel ondersteunt geen iframes op meerdere niveaus. Als uw website een iframe laadt dat een onderliggend iframe heeft, werken doelbibliotheken (at.js en mbox.js) alleen met het bovenliggende iframe. Doelbibliotheken hebben geen interactie met het onderliggende iframe.

Als tussenoplossing kunt u een pagina toevoegen in de ervaring met de URL van het onderliggende iframe.

## Wanneer ik een pagina probeer te bewerken, zie ik alleen een spinner in plaats van mijn pagina. (VEC en EEG) {#section_313001039F79446DB28C70D932AF5F58}

Dit kan gebeuren als de URL een #-teken bevat. Om de kwestie te bevestigen, schakelaar op Browse wijze in de Visuele Composer van de Ervaring, en dan terug te schakelen om wijze samen te stellen. De spinner moet weggaan en de pagina moet worden geladen.

## De kopballen van het Beleid van de Veiligheid van de inhoud (CSP) blokkeren de bibliotheken van het Doel op mijn website. (VEC en EEG) {#section_89A30C7A213D43BFA0822E66B482B803}

Als de CSP-headers van uw website de doelbibliotheken blokkeren, wordt de website geladen, maar wordt het bewerken voorkomen, zorgt u ervoor dat de doelbibliotheken niet worden geblokkeerd.

>[!NOTE]
>
>Naast de volgende informatie kunt u de [Adobe Target VEC Helper-browserextensie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor Google Chrome gebruiken.

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

## Mijn gehoste bestand target.js kan niet worden geladen wanneer de pagina opnieuw wordt geladen. (VEC en EEG) {#section_87F6418C2CD142A7B4D1E7037935F81F}

Dit probleem treedt op wanneer klanten een versie mbox.js hebben die ouder is dan 57 (versie 56 of eerder).

Wij adviseren dat alle gebruikers VEC aan de [recentste versie van mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A)bevorderen, of minstens aan versie 57 bevorderen. U zou ook moeten overwegen [makend de overgang aan at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).

## Wanneer ik één element op de pagina verander, veranderen de veelvoudige elementen. (VEC en EEG) {#section_309188ACF34942989BE473F63C5710AF}

Als dezelfde DOM-element-id wordt gebruikt op meerdere elementen op de pagina en u een van deze elementen wijzigt, worden alle elementen met die id gewijzigd. Om dit te voorkomen, zou een identiteitskaart slechts eenmaal op elke pagina moeten worden gebruikt. Dit is een standaard HTML aanbevolen werkwijze. Zie Scenario&#39;s voor [paginawijziging voor meer informatie](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Ik kan geen ervaringen bewerken voor een iFrame-opbouwende site. (VEC en EEG) {#section_9FE266B964314F2EB75604B4D7047200}

Dit probleem kan worden opgelost door de Enhanced Experience Composer in te schakelen. Klik **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]** en schakel het selectievakje Enhanced Experience Composer in. De Enhanced Experience Composer gebruikt een proxy met Adobe-beheer om uw pagina te laden voor bewerken. Op deze manier kunt u sites bewerken op iFrame en kunt u ze bewerken op sites en pagina&#39;s waaraan u nog geen Adobe Target-code hebt toegevoegd. De activiteiten leveren niet aan de plaats tot de code is toegevoegd. Sommige sites worden mogelijk niet geladen via de Enhanced Experience Composer. In dat geval kunt u deze optie uitschakelen om de Visual Experience Composer via een iFrame te laden. []

>[!NOTE]
>
>De lokaal gehoste pagina&#39;s of pagina&#39;s die niet toegankelijk zijn buiten uw netwerk, zijn niet toegankelijk voor de Adobe-proxyserver en kunnen niet worden geopend in de EEG. Deze pagina&#39;s kunnen URL&#39;s in fasen, UAT-URL&#39;s (User Acceptance Testing) of lokaal gehoste pagina&#39;s bevatten.

## Ik wil tests opzetten op pagina&#39;s die mbox/doelimplementatie nog niet hebben gedaan. (VEC en EEG) {#section_DE63BCCB5B124E10A71FA579B582A80A}

Zie &quot;Ik kan bovenstaande ervaringen voor een iFrame-bursting site niet bewerken&quot;.

## Vette en cursieve tekststijlen met Tekst bewerken/HTML of Tekst wijzigen/HTML worden niet op mijn pagina weergegeven. Soms verdwijnt de tekst na het toepassen van deze stijlwijzigingen. (VEC en EEG) {#section_7A71D6DF41084C58B34C18701E8774E5}

Als u **[!UICONTROL Edit Text/HTML]** in de Visuele Composer van de Ervaring voor A/B of Ervaring gerichte activiteiten of **[!UICONTROL Change Text/HTML]** voor Automated Personalization of Multivariate activiteiten van de Test gebruikt om tekst vette of cursief te maken, zouden die stijlen niet op de pagina kunnen worden toegepast of de tekst verdwijnt van de pagina in Visual Experience Composer. De manier waarop de RTF-editor deze stijlen toepast, kan de websiteopmaak beïnvloeden.

Als u dit probleem ziet:

1. Klik op de **[!UICONTROL HTML]** knop in de RTF-editor om de bronbewerkingsmodus te activeren.
1. Zoek de tekstelementen voor stijlen.

   * Wijzig voor vette tekst de `<strong>` elementen in `<b>`.

   * Wijzig voor cursieve tekst de `<em>` elementen in `<i>`.

## Bij Automated Personalization-activiteiten wordt het wisselen van afbeeldingen in de VEC of EEC verbroken. (VEC en EEG) {#section_88AABFDFE6A3420299B0D508B12A3994}

Als u een afbeeldingsaanbieding aan een locatie toevoegt, krijgt de oorspronkelijke afbeeldingsruimte in VEC of EEC de volledige grootte. Bij levering wordt de afbeelding niet uitgevouwen en wordt deze weergegeven zoals deze is, zodat er geen invloed is op de levering.
