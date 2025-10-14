---
keywords: gericht;visuele ervaringscomposer;whitelist;witte lijst;lijst van gewenste personen;lijst van gewenste personen;verbeterde visuele ervaringscomposer;vec;los visuele ervaringscomposer problemen op;het oplossen van problemen;eec;verbeterde ervaringscomposer;tls 1.2
description: Leer hoe te om problemen op te lossen die soms in  [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) en [!UICONTROL Enhanced Experience Composer] (EEC) onder bepaalde voorwaarden voorkomen.
title: Hoe los ik problemen op met betrekking tot [!UICONTROL Visual Experience Composer] en [!UICONTROL Enhanced Experience Composer]?
feature: Visual Experience Composer (VEC)
exl-id: d829cd63-950f-4bb4-aa58-0247f85de383
source-git-commit: ef5df0ae37ca1d07c0e51c06ed78739b2d2983fc
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# Problemen met de [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] en [!UICONTROL Enhanced Experience Composer] oplossen

Weergaveproblemen en andere problemen doen zich soms voor in [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) en [!UICONTROL Enhanced Experience Composer] (EEC) onder bepaalde omstandigheden.

## Hoe beïnvloedt het Google Chrome SameSite cookie handhavingsbeleid VEC en EEC? {#samesite}

+++Details
Houd rekening met de wijzigingen die van invloed zijn op de VEC en EEC wanneer u de volgende [!DNL Chrome] -releases gebruikt:

>[!NOTE]
>
>De volgende wijziging is van invloed op de drie updates die hieronder worden beschreven:
>
> * Zal ** niet VEC zonder de [&#x200B; geïnstalleerde en toegelaten uitbreiding van de Helper VEC &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) voor wachtwoord-beschermde pagina&#39;s van uw plaatsen kunnen gebruiken. Inlogcookies van uw site worden beschouwd als cookies van derden en worden niet verzonden met aanmeldingsaanvragen in de VEC-editor in de modus [!UICONTROL Browse] . De enige uitzondering is wanneer voor uw aanmeldcookies van de site de kenmerken `SameSite=None` en `Secure` zijn ingesteld.

**Chrome 94 (21 september, 2021)**: Met de aanstaande veranderingen die voor de versie van Chrome 94 (21 september, 2021) worden gepland, beïnvloedt de volgende verandering alle gebruikers met Chrome 94+ browser versies:

* De opdrachtregelmarkering `--disable-features=SameSiteByDefaultCookies,CookiesWithoutSameSiteMustBeSecure` wordt verwijderd.

**Chrome 91 (25 mei, 2021)**: Met de veranderingen die voor de versie van Chrome 91 (25 mei, 2021) worden uitgevoerd, beïnvloedt de volgende verandering alle gebruikers met Chrome 91+ browser versies:

* De markeringen `#same-site-by-default-cookies` en `#cookies-without-same-site-must-be-secure` zijn verwijderd uit `chrome://flags` . Dit gedrag is nu standaard ingeschakeld.

**Chrome 80 (Augustus 2020)**: Met de veranderingen die in Augustus 2020 worden uitgevoerd, alle gebruikers met Chrome 80+ browser versies:

* Zal ** niet [!DNL Target] bibliotheken kunnen downloaden terwijl het uitgeven van een activiteit (wanneer deze niet reeds op de plaats) zijn. De reden hiervoor is dat de downloadaanroep van het klantdomein naar een beveiligd [!DNL Adobe] -domein wordt gemaakt en als niet-geverifieerd wordt afgewezen.

* EEC zal *niet* functie voor alle gebruikers omdat het niet het attribuut SameSite voor koekjes op `adobemc.com domain` kan plaatsen. Zonder dit kenmerk weigert de browser deze cookies, waardoor de EEG mislukt.

+++

### Bepalen welke cookies worden geblokkeerd

+++Details
Gebruik [!DNL Developer Tools] in [!DNL Chrome] om te bepalen welke cookies worden geblokkeerd vanwege het beleid voor het toepassen van SameSite-cookies.

1. Als u [!DNL Developer Tools] wilt openen en de VEC wilt weergeven in [!DNL Chrome] , klikt u op het pictogram **[!UICONTROL ellipsis]** in de rechterbovenhoek van Chrome > **[!UICONTROL More Tools]** > **[!UICONTROL Developer Tools]** .
1. Klik op het tabblad **[!UICONTROL Network]** > en zoek naar geblokkeerde cookies.

   >[!NOTE]
   >
   >Schakel het selectievakje **[!UICONTROL Has blocked cookies]** in om geblokkeerde cookies gemakkelijker te vinden.

+++

## Biedt [!DNL Target] ondersteuning voor iframes op meerdere niveaus?

+++Details
[!DNL Target] biedt geen ondersteuning voor iframes met meerdere niveaus. Als uw website een iframe laadt dat een onderliggend iframe heeft, heeft at.js alleen invloed op het bovenliggende iframe. [!DNL Target] -bibliotheken hebben geen interactie met het onderliggende iframe.

Als tussenoplossing kunt u een pagina toevoegen in de ervaring met de URL van het onderliggende iframe.

+++

## Wanneer ik een pagina probeer te bewerken, zie ik alleen een spinner in plaats van mijn pagina. (VEC en EEG) {#section_313001039F79446DB28C70D932AF5F58}

+++Details
Deze situatie kan zich voordoen als de URL een #-teken bevat. U kunt dit probleem verhelpen door over te schakelen naar de modus [!UICONTROL Browse] in de VEC of EEC en terug te gaan naar de modus [!UICONTROL Compose] . De spinner moet weggaan en de pagina moet worden geladen.

+++

## Met CSP-koppen (Content Security Policy) worden de [!DNL Target] -bibliotheken op mijn website geblokkeerd. (VEC en EEG) {#section_89A30C7A213D43BFA0822E66B482B803}


+++Details
Als de CSP-headers van uw website bibliotheken [!DNL Target] blokkeren, wordt de website geladen, maar wordt het bewerken voorkomen, zorgt u ervoor dat de [!DNL Target] -bibliotheken niet worden geblokkeerd.

>[!NOTE]
>
>Naast de volgende informatie, kunt u de [&#x200B; browser van de Helper van Adobe Target gebruiken VEC uitbreiding &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) voor [!DNL Google Chrome].

![&#x200B; cps_headers beeld &#x200B;](assets/cps_headers.png)

Als tussenoplossing kunt u een [!DNL Requestly] -regel configureren om CSP-headers te verwijderen, zoals hieronder wordt weergegeven:

![&#x200B; cps_headers_2 beeld &#x200B;](assets/cps_headers_2.png)

U kunt een gelijkaardige [!DNL Requestly] regel voor om het even welke kopbal vormen die een middel ertoe leidt om niet binnen VEC te laden.

Als u voor [!DNL Requestly] kopteksten wilt verwijderen, moet u een van de volgende handelingen uitvoeren:

* Voeg URL-regels toe voor de URL die u in de VEC wilt openen, zodat kopteksten alleen voor die URL&#39;s worden verwijderd.
* Laat de regel toe wanneer u in VEC uitgeeft en maak de regel onbruikbaar wanneer u niet VEC gebruikt.

+++

## VEC of EEC lijkt gebroken of initialiseert niet wanneer het heruitgeven van een bewaarde activiteit. (VEC en EEG) {#section_5AC3BA8F8FBB451EA814F298D0645E54}

+++Details
Als de website buiten de VEC is gewijzigd nadat de ervaring is gedefinieerd, kunnen kiezers waarop eerder handelingen zijn uitgevoerd, niet worden gevonden wanneer de activiteit wordt geopend voor herbewerking. De pagina wordt verbroken weergegeven en er wordt geen waarschuwing weergegeven.

+++

## In de VEC of EEC worden mijn roterende banners en andere inhoud met JavaScript niet weergegeven. (VEC en EEG) {#section_8B5BE6EB050B42D6A14A054724C41330}

+++Details
Standaard blokkeert de VEC JavaScript-elementen. U kunt met deze elementen werken als u JavaScript uitschakelt. Afhankelijk van de manier waarop de site is ingesteld, worden sommige items mogelijk onjuist weergegeven of blijven ze niet beschikbaar.

+++

## Wanneer ik één element op de pagina verander, veranderen de veelvoudige elementen. (VEC en EEG) {#section_309188ACF34942989BE473F63C5710AF}

+++Details
Als dezelfde DOM-element-id wordt gebruikt op meerdere elementen op de pagina en u een van deze elementen wijzigt, worden alle elementen met die id gewijzigd. Om dit te voorkomen, zou een identiteitskaart slechts eenmaal op elke pagina moeten worden gebruikt. Dit is een standaard beste HTML-praktijk. Voor meer informatie, zie [&#x200B; Scenario&#39;s van de Wijziging van de Pagina &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

+++

## Ik kan geen ervaringen bewerken voor een iFrame-opbouwende site. (VEC en EEG) {#section_9FE266B964314F2EB75604B4D7047200}

+++Details
Dit probleem kan worden opgelost door de optie [!UICONTROL Enhanced Experience Composer] (EEC) in te schakelen. Klik op **[!UICONTROL Administation]** > **[!UICONTROL Visual Experience Composer]** en schakel vervolgens het selectievakje in waarmee [!UICONTROL Enhanced Experience Composer] wordt ingeschakeld. De EEC gebruikt een proxy met [!DNL Adobe] beheer om uw pagina te laden voor bewerken. Met deze proxy kunt u sites bewerken op iFrame en kunt u de code bewerken op sites en pagina&#39;s waaraan u nog geen [!DNL Adobe Target] -code hebt toegevoegd. De activiteiten leveren niet aan de plaats tot de code is toegevoegd. Sommige sites worden mogelijk niet geladen via de EEG. In dat geval kunt u de optie uitschakelen om de EEG via een iFrame te laden.

>[!NOTE]
>
>De lokaal gehoste pagina&#39;s of pagina&#39;s die niet toegankelijk zijn buiten uw netwerk, zijn niet toegankelijk voor de proxyserver van [!DNL Adobe] en kunnen niet worden geopend in de EEG. Deze pagina&#39;s kunnen URL&#39;s in fasen, UAT-URL&#39;s (User Acceptance Testing) of lokaal gehoste pagina&#39;s bevatten.

+++

## Ik wil opstellingstests op pagina&#39;s die mbox/ [!DNL Target] implementatie nog niet hebben gedaan. (VEC en EEG) {#section_DE63BCCB5B124E10A71FA579B582A80A}

+++Details
Zie &quot;Ik kan bovenstaande ervaringen voor een iFrame-bursting site niet bewerken&quot;.

+++

## Vette en cursieve tekststijlen met [!UICONTROL Edit Text]/ [!UICONTROL Edit HTML] of [!UICONTROL Change Text]/ [!DNL Change HTML] worden niet weergegeven op mijn pagina. Soms verdwijnt de tekst na het toepassen van deze stijlwijzigingen. (VEC en EEG) {#section_7A71D6DF41084C58B34C18701E8774E5}

+++Details
Als u **[!UICONTROL Edit Text]/[!UICONTROL Edit HTML]** in VEC voor [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] activiteiten of **[!UICONTROL Change Text]/[!UICONTROL Change HTML]** voor [!UICONTROL Automated Personalization] of [!UICONTROL Multivariate Test] activiteiten gebruikt om tekst vet of cursief te maken, worden die stijlen mogelijk niet op de pagina toegepast of verdwijnt de tekst van de pagina in VEC. Dit gebeurt als gevolg van de manier waarop de RTF-editor deze stijlen toepast, waardoor de markering van de website mogelijk wordt beïnvloed.

Als u dit probleem ziet:

1. Klik op de knop **[!UICONTROL HTML]** in de RTF-editor om de bronbewerkingsmodus te activeren.
1. Zoek de tekstelementen voor stijlen.

   * Wijzig voor vette tekst `<strong>` -elementen in `<b>` .

   * Wijzig voor cursieve tekst `<em>` -elementen in `<i>` .

+++

## Bij Automated Personalization-activiteiten wordt het wisselen van afbeeldingen in de VEC of EEC verbroken. (VEC en EEG) {#section_88AABFDFE6A3420299B0D508B12A3994}

+++Details
Als u een afbeeldingsaanbieding aan een locatie toevoegt, krijgt de oorspronkelijke afbeeldingsruimte in VEC of EEC de volledige grootte. Bij levering wordt de afbeelding niet uitgevouwen en wordt deze weergegeven zoals deze is, zodat er geen invloed is op de levering.

+++
