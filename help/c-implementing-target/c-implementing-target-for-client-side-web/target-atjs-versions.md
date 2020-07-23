---
keywords: at.js releases;at.js versions
description: Details over wijzigingen in elke versie van at.js.
title: details van de at.js-versie
subtopic: Getting Started
uuid: 3586af55-db15-4e68-90a7-d552338ec5e8
translation-type: tm+mt
source-git-commit: b9a445d1b9e0b4b06b10370c6fefd570380d48f7
workflow-type: tm+mt
source-wordcount: '3971'
ht-degree: 0%

---


# details van de at.js-versie {#at-js-version-details}

Gegevens over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js.

>[!IMPORTANT]
>
>Het Target-team ondersteunt beide om 1.js.*x* en at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert.
>
>[De Lancering](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) van het Adobe Experience Platform is de aangewezen methode om at.js te bevorderen. Extensieontwikkelaars voegen voortdurend nieuwe functies toe aan hun extensies en corrigeren vaak bugs. Deze updates worden verpakt in nieuwe versies van een extensie en beschikbaar gesteld in de [!DNL Launch] catalogus als upgrades. Zie Upgrade [van](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/extensions/extension-upgrade.html) extensies in de gebruikershandleiding *van het* Experience Platform Launch voor meer informatie.

## te.js 2.3.2 (24 juli 2020)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:

* Het probleem is opgelost wanneer een script of code een standaardeigenschap aan het venster of document toevoegt.

## om 1.8.2 uur (15 juni 2020)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:

* Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 1.*x* zou tot het serverdomein verkeerd kunnen leiden, dat in het [!DNL Target] verzoek mislukte. (TNT-35064)

## releases (15 juni 2020)

Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:

* De `deviceIdLifetime` instelling is overschreven via [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)
* Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 2.*x* zou tot het serverdomein verkeerd kunnen leiden, dat in het [!DNL Target] verzoek mislukte. (TNT-35065)
* Probleem verholpen bij het gebruik van de [!DNL Target] extensie v2 en de [!DNL Launch] [!DNL Adobe Analytics] extensie, [!DNL Launch] waarmee de [!DNL Target][!DNL Analytics] `sendBeacon` aanroep werd vertraagd. (TNT-36407, TNT-35990, TNT-36000)

## at.js versie 2.3.0 (25 maart 2020)

Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:

* Ondersteuning voor het instellen van Content Security Policy-nonces op SCRIPT- en STYLE-tags die aan het pagina-DOM zijn toegevoegd bij het toepassen van geleverde Target-aanbiedingen. Klanten kunnen de overeenkomstige script- en stijllabelnonces voor toegepaste aanbiedingen instellen `targetGlobalSettings.cspScriptNonce` en `targetGlobalSettings.cspStyleNonce` zo instellen dat at.js deze kan instellen. Zie [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) voor meer informatie.
* Probleem opgelost bij het compileren van at.js met de Google Closure-compiler voor de implementatie van Google Tag Manager.
* De naam van het controlecookie at.js is gewijzigd van `check` naar `at_check` om conflicten met de implementaties van klanten te voorkomen.

## at.js versie 1.8.1 (25 maart 2020)

Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:

* De naam van het controlecookie at.js is gewijzigd van `check` naar `at_check` om conflicten met de implementaties van klanten te voorkomen.

## at.js versie 2.2.0 (10 oktober 2019)

Deze versie van at.js bevat de volgende verbeteringen en oplossingen:

* Correctie van een probleem waarbij via bijhouden van klikken geen conversies werden gerapporteerd in Analytics for Target (A4T) toen Adobe Analytics-code niet aanwezig was op pagina-elementen.
* Betere prestaties bij het gebruik van zowel Experience Cloud ID Service (ECID) v4.4 als at.js 2.2 op uw webpagina&#39;s.
* Eerder, maakte ECID twee blokkerende vraag alvorens at.js ervaringen kon halen. Dit is verminderd tot één enkele vraag, die beduidend prestaties verbetert.

   >[!NOTE]
   >
   >Voer een upgrade uit van uw ECID-extensie voor starten naar versie 4.4 om te profiteren van deze prestatieverbetering.

* at.js versie 2.2 verstrekt ook een nieuw die plaatsen wordt genoemd `serverState`. Deze instelling kan worden gebruikt om de paginaprestaties te optimaliseren wanneer een hybride integratie van Target wordt geïmplementeerd. Hybride integratie betekent dat u zowel at.js v2.2+ aan de client-kant als de levering-API of een Target SDK aan de server-kant gebruikt om ervaringen te bieden. `serverState` geeft at.js v2.2+ de capaciteit om ervaringen direct van inhoud toe te passen die op de server wordt gehaald en aan de cliënt als deel van de pagina teruggegeven wordt. Zie &quot;serverState&quot; in [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state)voor meer informatie.

## at.js versie 1.8.0 (10 oktober 2019)

Deze versie van at.js bevat de volgende verbeteringen en oplossingen:

* Betere prestaties bij het gebruik van zowel Experience Cloud ID Service (ECID) v4.4 als at.js 1.8 op uw webpagina&#39;s.
* Eerder, maakte ECID twee blokkerende vraag alvorens at.js ervaringen kon halen. Dit is verminderd tot één enkele vraag, die beduidend prestaties verbetert.

>[!NOTE]
>
>Voer een upgrade uit van uw ECID-extensie voor starten naar versie 4.4 om te profiteren van deze prestatieverbetering.

## at.js versie 2.1.1 (24 juli 2019)

Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:

(De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.)

* Oplossing een kwestie die veelvoudige bakens aan brand veroorzaakte toen het gebruiken van de Metrisch van het Volgen van de Klik op de pagina van Doelstellingen &amp; van Montages in Visual Experience Composer (VEC). (TNT-32812)
* Probleem verholpen waarbij het renderen van aanbiedingen meerdere keren `triggerView()` werd voorkomen. (TNT-32780)
* Probleem verholpen met `triggerView()` om ervoor te zorgen dat de aanvraag MCID-gegevens (Marketing Cloud ID) bevat. (TNT-32776)
* Probleem verholpen waardoor de `triggerView()` melding niet kon worden uitgevoerd, zelfs als er geen opgeslagen weergaven zijn. (TNT-32614)
* Probleem verholpen die een fout veroorzaakte door het gebruik van de decodeURIcomponent die problemen veroorzaakte wanneer de URL een onjuist gevormde parameter van het vraagkoord bevat. (TNT-32710)
* De bakenvlag wordt nu geplaatst aan &quot;waar&quot;in de context van leveringsverzoeken die via `Navigator.sendBeacon()` API worden verzonden. (TNT-32683)
* Probleem verholpen waarbij Aanbevelingen voor een paar klanten niet konden worden weergegeven op websites. Klanten konden de inhoud van de aanbieding zien in de levering API vraag maar de aanbieding werd niet toegepast op de website. (TNT-32680)
* Probleem verholpen waarbij klikken-volgen over meerdere ervaringen ertoe leidde dat het programma niet naar behoren functioneerde. (TNT-32644)
* Probleem verholpen waardoor at.js de tweede metrische waarde niet kon toepassen na het renderen van de eerste metrische waarde. (TNT-32628)
* Probleem verholpen bij het doorgeven `mboxThirdPartyId` `targetPageParams` van de functie die ervoor zorgde dat de lading van de verzoeklading niet in of de vraagparameters of in de verzoeklading aanwezig was. (TNT-32613)
* Probleem verholpen waarbij weergave- en berichtreacties werden geblokkeerd in op Chromium gebaseerde browsers (inclusief Google Chrome). (TNT-32290)

## at.js versie 2.1.0 (3 juni 2019)

Deze release bevat de volgende functies en verbeteringen:

* **Ondersteuning** voor Adobe Opt-in: Adobe Opt-In is een manier om de integratie van Adobe-oplossingen met compatibiliteitsbeheerplatforms te vereenvoudigen. Zie [Privacy and General Data Protection Regulation (GDPR)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)voor meer informatie over Adobe Opt-in.

* **Compatibel met** industriestandaard CSP: at.js gebruikt eval() niet meer om JavaScript uit te voeren.

* **Logboekregistratie** voor analyses op de client: Geef klanten de volledige controle over de manier waarop ze analysegegevens naar Adobe Analytics willen verzenden, zowel op de client als op de server.

   Voor meer informatie, zie [cliënt-kant het registreren](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) van Analytics *Alvorens u implementeert*.

* **Meldingen** verzenden: Ontwikkelaars toestaan meldingen te verzenden wanneer een ervaring door hun code wordt gegenereerd in plaats van deze te gebruiken `applyOffer()` of `applyOffers()`.

   Zie [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)voor meer informatie.

* **grootte at.js verminderd met ~24%**: De grootte van at.js wordt verminderd met ~24%. De kleinere bestandsgrootte verbetert de laadprestaties van de pagina en verkort de downloadtijd op .js op de pagina.

## at.js versie 2.0.1 (19 maart 2019)

Dit is een onderhoudrelease met de volgende verbeteringen en oplossingen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

* Probleem verholpen met een zeldzame omstandigheid in de opiniepeilingscode voor DOM die JavaScript-uitzonderingen voor bepaalde klanten veroorzaakte. (TNT-31869)
* Meldingen dat weergaven werden gerenderd, zijn losgekoppeld van gebeurtenishandlers voor het bijhouden van klikken. Target heeft aanvankelijk geen meldingen verzonden als click-event-handlers die tot een weergegeven weergave behoren, niet konden worden gekoppeld. Target verzendt nu een weergavemelding, zelfs als klikelementen niet worden gevonden. (TNT-31969)
* Probleem verholpen waarbij de omleidingsvlag voor de gebeurtenis die na het verzoek werd uitgevoerd, altijd werd ingesteld op true. (TNT-31907)
* Probleem opgelost dat ertoe leidde dat VEC opnieuw rangschikte actie als succes werd geregistreerd, zelfs wanneer de elementen ontbraken. (TNT-31924)
* Probleem opgelost waarbij meldingen voor bepaalde klanten werden verzonden om de eigenschappentoken voor Enterprise-machtigingen niet te bevatten. (TNT-31999)

## at.js versie 1.7.1 (19 maart 2019)

Dit is een onderhoudrelease met de volgende oplossing:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

* Probleem verholpen met een zeldzame omstandigheid in de opiniepeilingscode voor DOM die JavaScript-uitzonderingen voor bepaalde klanten veroorzaakte. (TNT-31869)

## at.js Versie 2.0.0 {#at-js-200}

at.js 2.x verstrekt rijke eigenschapreeksen die uw zaken uitrusten om verpersoonlijking op volgende generatie cliënt-zijtechnologieën uit te voeren. Deze nieuwe versie wordt geconcentreerd op bevordering at.js om harmonieuze interactie met enige paginatoepassingen (SPAs) te hebben.

Hier volgen enkele voordelen van het gebruik van at.js 2.x die niet beschikbaar zijn in eerdere versies:

* De capaciteit om alle aanbiedingen op paginading in het voorgeheugen onder te brengen om veelvoudige servervraag aan één enkele servervraag te verminderen.
* Verbeter de ervaringen van uw eindgebruikers op uw site aanzienlijk, omdat aanbiedingen direct via het cachegeheugen worden weergegeven zonder vertraging die traditionele serveraanroepen introduceren.
* Eenvoudige one-line van code en éénmalige ontwikkelaarsopstelling om uw marketers toe te laten om A/B en de activiteiten van de Ervaring (XT) via Visual Experience Composer (VEC) op uw enige paginatoepassingen tot stand te brengen en in werking te stellen.

at.js 2.x introduceert de volgende nieuwe functies:

* getOffers()
* applyOffers()
* triggerView()

De volgende functies zijn vervangen door de introductie van at.js 2.x:

* mboxCreate()
* mboxDefine
* registerExtension()

Voor meer informatie, zie [Bevordering van at.js 1.x aan at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) en [at.js functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).

>[!NOTE]
>
>Als u ondersteuning voor Adobe Opt-in nodig hebt voor de [algemene gegevensbeschermingsverordening](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) (GDPR), moet u momenteel op 0.js 1.7.0 of op 0.js 2.1.0 werken.

## at.js versie 1.7.0 {#at-js-170}

at.js 1.7.0 biedt ondersteuning voor Adobe Opt-In. Adobe Opt-In is een manier om de integratie van Adobe-oplossingen met compatibiliteitsbeheerplatforms te vereenvoudigen.

Voor meer informatie over Adobe Opt-in, zie [Privacy en Algemene Verordening](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) van de Bescherming van Gegevens (GDPR).

In deze release is ook een probleem opgelost waarbij Target URL-parameters omleiden kan negeren met parameters die afkomstig zijn van de omleidings-URL.

>[! OPMERKING]
>
>Als u ondersteuning voor Adobe Opt-in voor GDPR nodig hebt, moet u momenteel 0.js 1.7.0 of 2.1.0 gebruiken.<br>Zie voor een lijst met alle versies de versiedetails [](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)at.js.

## at.js Versie 1.6.4 {#at-js-164}

at.js 1.6.4 is een onderhoudsrelease en behandelt het volgende probleem:

* Probleem verholpen waarbij zich in Microsoft Internet Explorer 11 een zeldzame omstandigheid manifesteerde die dubbele aanbiedingen veroorzaakte die moesten worden toegepast.

## at.js versie 1.6.3 {#section_484A56774E004282B98FFFF851E4E670}

at.js versie 1.6.3 bevat de volgende correcties en verbeteringen:

* Kiezers hebben nu een CSS-escape-teken als ze id&#39;s of CSS-klassen bevatten die beginnen met een cijfer, twee afbreekstreepjes of een afbreekstreepje gevolgd door een cijfer (bijvoorbeeld #-123). (TNT-31061)
* Probleem verholpen dat werd geïntroduceerd met at.js 1.6.2, waarbij VEC-aanbiedingen (Visual Experience Composer) uit verschillende activiteiten die van toepassing zijn op dezelfde CSS-kiezer de prioriteit van de activiteit niet respecteerde. (TNT-31052)
* Probleem verholpen waarbij een belofte werd nagekomen in omgevingen waar geen native ondersteuning voor beloften bestond. (TNT-30974)
* Problemen worden nu correct vastgelegd en gerapporteerd via de gebeurtenis content-rendering mislukt. Eerder werd mogelijk gemeld dat JavaScript goed was uitgevoerd, zelfs als dat niet het geval was. (TNT-30599)

## at.js versie 1.6.2 {#section_88BE2F69943D4280B8170F377886B58E}

Dit is een onderhoudsrelease en het volgende probleem wordt opgelost:

* Probleem verholpen waarbij sites van bepaalde klanten tot een oneindige &#39;async&#39;-lus leiden.

>[!IMPORTANT]
>
>Daarnaast bevat at.js versie 1.6.2 ook alle verbeteringen en correcties die zijn opgenomen in at.js versie 1.6.1 en 1.6.0. Deze versies kunnen niet meer worden gedownload. We raden u aan een upgrade naar versie 1.6.2 uit te voeren als u 1.6.1 of 1.6.0 gebruikt

Hier zijn de verhogingen en de moeilijke situaties die in at.js Versie 1.6.1 werden omvat:

* Probleem verholpen in at.js 1.6.0 dat ertoe leidde dat ervaringen met aanbevelingen werden gedupliceerd in Microsoft Internet Explorer 11. (TNT-30593)
* at.js zorgt er nu voor dat de logica voor het overschrijven van randen controleert of er een cookie met een randcluster bestaat om een ander randnummer te voorkomen als een gebruiker tijdens een sessie randen verlaat. (TNT-30563)
* Probleem verholpen waardoor at.js geen volgende handelingen kon uitvoeren als de HTML-inhoud ongeldige JS-code bevatte. at.js registreert nu de fout en geeft de resterende acties zonder kwestie terug. (TNT-30546)
* Er zijn wijzigingen aangebracht zodat er een uitzondering is wanneer een pagina omleiden wordt hergekwalificeerd voor een omleidingsactiviteit. (TNT-30532)
* Probleem verholpen waardoor de correcte time-out van de aanvraag niet kon worden doorgegeven aan de getOffer() API-aanvraag. (TNT-30498)
* Probleem verholpen waarbij het opslaan van cookies tijdens het gebruik van het bestandsprotocol door at.js 1.6.0 werd voorkomen. (TNT-30454)
* Het probleem dat ervoor zorgde dat niet alle ervaringen werden opgedaan met omleidingen bij gebruik van Analytics for Target (A4T), is opgelost. (TNT-30444)
* Probleem verholpen waarbij de pagina werd verborgen nadat de Target-aanroep was gelukt. (TNT-30358)

Hier zijn de verhogingen en de moeilijke situaties die in at.js Versie 1.6.0 werden omvat:

* Omleidingsaanbiedingen worden nu automatisch ondersteund in de integratie met Analytics for Target (A4T). De oplossing aan de clientzijde is verwijderd. (TNT-30247)
* Client-side edge routing is nu standaard ingeschakeld. (TNT-30261)
* Oplossing voor een probleem met VEC-actie (Visual Experience Composer) wanneer er afhankelijkheden zijn tussen handelingen. (TNT-30248)

## at.js Versie 1.5.0 {#section_128C6761884C4DA8AE50D6A605FF6F55}

at.js versie 1.5.0 is nu beschikbaar.

* De details van de `at-request-succeeded` gebeurtenis bevatten de omleidingsvlag. Met deze markering kunt u bepalen of de pagina wordt omgeleid naar een andere URL. Als u de URL wilt weten, meldt u zich aan `at-content-rendering-redirect`. (TNT-29834)
* Probleem verholpen waarbij een fout `window.targetGlobalSettings.enabled` bij uitvoering werd gegenereerd als deze op false was ingesteld. (TNT-29829)
* Probleem verholpen die ertoe leidde dat de pagina mislukte tijdens het laden in Visual Experience Composer (VEC) als het gebruiken van douanecode aan een brand globale mbox verzoek en het gebruiken van lichaam het verbergen. (TNT-29795)
* Extra ondersteuning voor `screenOrientation`, `devicePixelRatio`en `webGLRenderer`. Deze nieuwe Target-aanvraagparameters worden gebruikt voor iPhone X en andere moderne apparaatdetectie. Zie [Mobiel](../../c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89)voor meer informatie. (TNT-29781)
* Probleem verholpen waarbij de locatie-hint van de Adobe Audience Manager (AAM) niet altijd werd verzonden. (TNT-29695)
* Voor browsers die dit ondersteunen, schakelt at.js 1.5.0 over naar MutationObserver voor kiezersopiniepeiling. In versies vóór at.js 1.0.0 werd een MutationObserver-polyfill gebruikt, wat problematisch bleek te zijn. Om de polyfill problemen te voorkomen, gebruikt versie 1.5.0 de volgende pseudo-code om te bepalen welk planningsmechanisme moet worden gebruikt:

   ```
   if MutationObserver is supported
     scheduler = MutationObserver
   else if document is visible
     scheduler = requestAnimationFrame
   else
     scheduler = setTimeout
   ```

## at.js versie 1.3.0 {#section_24EAAE1CFA814EF8B19E61842F4D8321}

at.js versie 1.3.0 is nu beschikbaar.

* De volgende nieuwe gebeurtenissen zijn beschikbaar om u te helpen bij het traceren, opsporen van fouten en het aanpassen van interactie met at.js:

   * LIBRARY_LOADED
   * REQUEST_START
   * CONTENT_RENDERING_START
   * CONTENT_RENDERING_NO_OFFERS
   * CONTENT_RENDERING_REDIRECT

   Zie [aangepaste gebeurtenissen](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md)at.js voor meer informatie.

* U kunt een verzoek at.js met extra parameters uitbreiden die uit gegevensleveranciers komen. Gegevensleveranciers moeten worden toegevoegd `window.targetGlobalSettings` onder de `dataProviders key`richtlijn.

   Zie [Gegevensleveranciers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)voor meer informatie.

* Bij.js-aanvragen wordt nu GET gebruikt, maar er wordt overgeschakeld naar POST wanneer de URL groter is dan 2048 tekens. Er is een nieuwe eigenschap met de naam `urlSizeLimit` waarin u de maximale grootte indien nodig kunt verhogen. Dankzij deze wijziging kan Target zich bij .js uitlijnen op AppMeasurement, die dezelfde techniek gebruikt.
* Target dwingt nu af of de `mbox` toets in de `adobe.target.applyOffer(options)` functie wordt gebruikt. Deze sleutel is in het verleden vereist, maar Target dwingt nu het gebruik af om ervoor te zorgen dat Target de juiste validatie heeft en klanten de functie correct gebruiken.
* at.js heeft de functie voor het bijhouden van gebeurtenissen verbeterd en klikt op tracking. at.js gebruikt `navigator.sendBeacon()` om gegevens voor het bijhouden van gebeurtenissen te verzenden en fallback naar synchrone XHR wanneer `navigator.sendBeacon()` dit niet wordt ondersteund. Deze fallback heeft vooral invloed op Internet Explorer 10 en 11 en op sommige versies van Safari. Safari voegt ondersteuning toe voor `navigator.sendBeacon()` de volgende iOS 11.3-versie.
* Met at.js kunt u nu aanbiedingen renderen, zelfs als een pagina wordt geopend op tabbladen op de achtergrond. Sommige klanten van Target kwamen een probleem tegen toen deze `requestAnimationFrame()` was uitgeschakeld vanwege het browsergedrag voor achtergrondtabbladen.
* Deze versie voegt vele prestatiesverbeteringen, met inbegrip van kortere callstacks toe wanneer het inspecteren van een profiel van Chrome cpu.
* at.js 1.3.0 biedt geen ondersteuning meer voor de levering van inhoud in Microsoft Internet Explorer 9. Zie [Ondersteunde browsers](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100)voor een lijst met ondersteunde browsers. Voorwaarts, worden alle verzoeken uitgevoerd via `XMLHttpRequest` met steun CORS zonder JSONP- verzoeken. Deze wijziging verbetert de veiligheid aanzienlijk.

## at.js versie 1.2.3 {#section_CE4D14AF00D04F4C8A2F0513F5EA1A84}

[!DNL at.js] versie 1.2.3 is nu beschikbaar.

* Voegt ondersteuning toe voor JSON-aanbiedingen. JSON-aanbiedingen worden alleen ondersteund in activiteiten die zijn gemaakt met de Form-based Experience Composer. De enige manier om JSON-aanbiedingen te gebruiken is momenteel via directe API-aanroepen. Zie JSON-aanbiedingen [maken](../../c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D).

## at.js versie 1.2.2 {#section_4E96D13F2DFE4F1F81A1089877D53649}

[!DNL at.js] versie 1.2.2 is nu beschikbaar.

* Probleem verholpen waarbij een JavaScript-fout werd geretourneerd wanneer de Target-bibliotheek in de QUIRKS-modus op een pagina werd geladen. (TNT-28312)
* Probleem verholpen waarbij Target klikken bijhouden ertoe leidde dat aanroepen voor Analytics-gegevensverzameling werden afgebroken. (TNT-28261)
* Probleem verholpen die mislukte wanneer een lege tekenreeks `getOffer() params` wordt `targetPageParams()` geretourneerd. (TNT-28359)
* Probleem verholpen met genereren van sessie-id bij gebruik van alleen x. (TNT-28361)

## at.js versie 1.2.1 {#section_F757C8174BBA4F68AC5524ADC3D9C5E3}

[!DNL at.js] versie 1.2.1 is nu beschikbaar.

* Probleem verholpen wanneer op een koppeling met target=&quot;_blank&quot; werd geklikt omdat Target de koppeling niet op een nieuw tabblad kon openen.

## at.js versie 1.2.0 {#section_1C3A18C595C34B25A14A440D213F3B9C}

[!DNL at.js] versie 1.2 is nu beschikbaar als een onderhoudsversie die meestal foutoplossingen bevat.

* Probleem verholpen waarbij standaardhandelingen voor speciale gevallen met klikken werden voorkomen. (TNT-28089)
* Probleem verholpen waarbij klikken en volgen op een koppeling `target="_blank"` waardoor Target de koppeling niet op een nieuw tabblad kon openen. (TNT-28072)
* IP de adressen kunnen als koekjesdomein worden gebruikt. (TNT-28002)
* Probleem verholpen dat flikkering veroorzaakte bij omleidingsvoorstellen met een global mbox of andere regionale dozen. (TNT-27978)
* Probleem verholpen in Experience Targeting activity setup mislukt binnen de VEC bij het schakelen tussen Bladeren en Samenstellen. (TNT-27942)
* Probleem verholpen met onjuiste afhandeling van flikkerstijlklassen voor kliktrackelementen. (TNT-27896)
* Probleem verholpen waarbij algemene mbox-parameters werden gemengd met alle mbox-parameters. (TNT-27846)
* Wijzigingen zijn aangebracht om ervoor te zorgen dat Handlebars, Mustache en andere sjabloonbibliotheken aan de clientzijde correct worden afgehandeld door [!DNL at.js]. (TNT-27831)
* Wijzigingen aangebracht om ervoor te zorgen dat deze correct `sdidParamExpiry` worden geïnitialiseerd en worden doorgegeven aan de Bezoeker-API. Dit is een regressie waaraan is toegevoegd `at.js 1.1.0`. Dit heeft geen invloed op eerdere [!DNL at.js] versies. Dit is alleen van invloed op clients die omleidingsaanbiedingen en A4T gebruiken. (TNT-27791)
* Wijzigingen aangebracht om ervoor te zorgen dat dit kenmerk `SCRIPT` wordt uitgevoerd, ongeacht het type dat wordt gebruikt. (TNT-27865)

## at.js versie 1.1.0 {#section_8F494E1EA94E48A9B169F5CF9FE6DC56}

**Datum:** 2 augustus 2017

De volgende verbeteringen en correcties zijn opgenomen in [!DNL at.js] versie 1.1:

* Toegevoegde verwerking van responstoken. Zie [Reactietokens](../../administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4)voor meer informatie.
* Het probleem is opgelost, zodat `document.currentScript polyfill` dit niet interfereert met Hoek 1.X.
* Wijzigingen aangebracht om ervoor te zorgen dat het bijhouden van klikken geen invloed heeft op de zichtbaarheidseigenschap. Klik op de volgende elementen worden gemarkeerd met de `at-element-click-tracking` CSS-klasse in plaats van `at-element-marker`.

## at.js Versie 1.0.0 {#section_37A3D23FC4AD42A68AA831B89E03E725}

**Datum:** 7 juli 2017

De volgende verbeteringen en correcties zijn opgenomen in versie 1.js 1.0:

* Ondersteuning voor asynchroon laden op .js voor sneller laden van pagina&#39;s.
* Ondersteuning voor het vooraf verbergen van pagina-inhoud bij het asynchroon laden van at.js.
* Betere foutberichten wanneer de levering van inhoud is uitgeschakeld.
* Prestatieverbeteringen bij het uitvoeren van meerdere activiteiten.
* Ondersteuning voor YUI-compressor.
* Foutenmelding voor aangepaste gebeurtenissen tijdens de levering van de activiteit.
* Oplossen voor prestatieproblemen in Microsoft Internet Explorer 11.
* Oplossing voor `getOffer()` functie die een fout op sommige websites veroorzaakt.
* Laad de Target-bibliotheek asynchroon. Voor meer informatie, zie [bij.js Veelgestelde Vragen](../../c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769).

## at.js Versie 0.9.7 {#section_6C7B698BE21E40E495FD2850EFBF3E80}

**Datum:** 22 mei 2017

De volgende verbeteringen en correcties zijn opgenomen in [!DNL at.js] versie 0.9.7:

* Probleem verholpen met betrekking tot een elementensleutel die ontbrak aan `insertAfter` en `insertBefore` acties in Visual Experience Composer (VEC). Deze problemen hadden betrekking op de migratie van visuele aanbiedingen naar aanbiedingstemplates.

## at.js Versie 0.9.6 {#section_EEFA6413F2F947AD8C4A88128B90245D}

**Datum:** 13 april 2017

De volgende verbeteringen en correcties zijn opgenomen in [!DNL at.js] versie 0.9.6:

* Omleiding biedt ondersteuning voor A4T. Nadat u versie 0.9.6 downloadt en installeert, kunt u aanbiedingen in activiteiten gebruiken die [!DNL at.js] als Bron van de Rapportering voor [!DNL Adobe Analytics] [!DNL Target] (A4T) gebruiken. Naast [!DNL at.js] versie 0.9.6 zijn er andere minimumvereisten waaraan uw implementatie moet voldoen om omleidingsaanbiedingen en A4T te kunnen gebruiken. Voor meer informatie en extra belangrijke informatie zou u moeten weten, zie Aanbiedingen van de [Omleiding - Veelgestelde vragen](../../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905)A4T.
* Vóór [!DNL at.js] 0.9.6, toen de bezoeker-API op de pagina aanwezig was en de `visitorApiTimeout` instelling te agressief was, kon Target in een situatie terechtkomen waarin er geen MCID-gegevens werden verzonden in de [!DNL Target] aanvraag. Dit kan leiden tot problemen zoals onverwachte resultaten [!DNL Analytics] bij het gebruik van A4T.

   Dit gedrag is gewijzigd in [!DNL at.js] 0.9.6, zelfs als de waarde `visitorApiTimeout` is ingesteld op 1 ms, probeert Target SDID-, trackingservers en klant-id-gegevens te verzamelen en deze te verzenden in de Target-aanvraag.

* De `selectorsPollingTimeout` instelling is toegevoegd. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)voor meer informatie.
* De indeling van de reactie van `getOffer()` is gewijzigd. Zie [adobe.target.getOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md)voor meer informatie.
* Logboekregistratie voor console is toegevoegd voor niet-ondersteunde `<!DOCTYPE>` declaraties.
* Probleem verholpen waarbij [!DNL Target Classic] plug-ins niet correct werden toegepast wanneer meerdere standaardaanbiedingen naar één box werden geleverd. (TGT-22664)
* Verbeterde cookie-instelling voor twee TLD&#39;s (Top-Level-Domain) om ervoor te zorgen dat de cookie van de box correct is ingesteld voor deze domeinen (bijvoorbeeld [!DNL test.no], [!DNL autodrives.ca]enzovoort).
* Het algoritme voor het extraheren van het domein op hoofdniveau dat moet worden gebruikt bij het opslaan van cookies is gewijzigd in versie 0.js 0.9.6. Vanwege deze wijziging kunnen cookies niet worden opgeslagen naar adressen die IP gebruiken. Meestal worden IP-adressen gebruikt voor testdoeleinden, maar als tijdelijke oplossingen kunt u DNS-vermeldingen gebruiken of het hostbestand op een lokaal vak aanpassen.
* Correctie van het verplaatsen en herschikken van handelingen waarbij eigenschappen tekenreekswaarden zijn in plaats van gehele getallen.

## at.js Versie 0.9.4 {#section_A15B12F12CD94F07B3F56613A79A815F}

**Datum:** 19 januari 2017

* mbox-namen kunnen nu speciale tekens bevatten, waaronder ampersands ( &amp; ), zodat deze consistent zijn met de naamgevingsvereisten voor mbox-namen met mbox.js.

   Zie [at.js Configurations](../../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812)voor een lijst met toegestane speciale tekens.

* Toegevoegde `secureOnly` instelling die aangeeft of at.js alleen HTTPS mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld en via `targetGlobalSettings`deze instelling kan worden overschreven.
* De [!UICONTROL Legacy Browser Support] optie is beschikbaar in at.js versie 0.9.3 en eerder. Deze optie is verwijderd in versie 0.js 0.9.4.

## at.js Versie 0.9.3 {#section_DF13BC1D7C994AE7A36B81937A699DF4}

**Datum:** 10 oktober 2016

* Zorgt ervoor dat mbox in Microsoft Internet Explorer 11 vuur aanroept wanneer oudere browsers in de instellingen at.js zijn uitgeschakeld.
* Zorgt ervoor dat de standaardinhoud wordt teruggegeven als een dynamische verre aanbieding ontbreekt (bijvoorbeeld, als URL onjuist is en een fout 404 terugkeert).
* Zorgt ervoor dat elementen snel worden onthuld wanneer VEC klik-volgende selecteurs niet in DOM kan worden gevonden.

## at.js Versie 0.9.2 {#section_148549CBB4F046BAA8F79C79B64EC889}

**Datum:** 21 september 2016

* Er is een `optoutEnabled` instelling toegevoegd om de optie Weigeren apparaatgrafiek in of uit te schakelen. Als deze instelling is ingesteld op `true` en de bezoeker het bijhouden heeft beëindigd, wordt er door de browser van de bezoeker geen mbox-aanroepen uitgevoerd. Apparaatgrafiek bevindt zich momenteel in bètaversie. Deze instelling is standaard ingesteld op `false` Apparaatgrafiek, maar moet worden ingesteld op `true` als u Apparaatgrafiek gebruikt. Een vergelijkbare optie maakt deel uit van mbox.js v61.
* Extra `CustomEvent` ondersteuning voor het kennisgevingsmechanisme. Eerder kon het meldingsmechanisme voor de gebeurtenis at.js niet worden gebruikt via standaard-DOM API&#39;s, zoals `document.addEventListener()`. Nu kunt u gebruiken `document.addEventListener()` om u te abonneren op gebeurtenissen at.js, zoals aanvraaggebeurtenissen en gebeurtenissen voor het renderen van inhoud.
* Oplossing voor een probleem met betrekking tot aanbiedingen die zijn gemaakt in Visual Experience Composer (VEC). Vóór deze release heeft Target de kiezers verborgen en deze alleen niet verborgen wanneer alle kiezers overeenkomen. In 0.js 0.9.2 verbergt Target de kiezers zodra ze overeenkomen.

## at.js Versie 0.9.1 {#section_DAFB99114D604CFB8416C1BC7DEEAEEE}

**Datum:** 14 juli 2016

* Verstrekt at.js een onderbreking voor de Dienst van identiteitskaart van de Bezoeker, die van de eigen onderbreking van de dienst onafhankelijk is.
* Hiermee wordt een probleem in 0.9.0 verholpen dat invloed had op implementaties met at.js op sommige pagina&#39;s en mbox.js op andere pagina&#39;s.
* Als u Adobe Analytics gebruikt als rapportbron voor uw activiteit, hoeft u geen traceringsserver op te geven tijdens het maken van activiteiten als u mbox.js versie 61 (of hoger) of versie 0.9.1 (of hoger) gebruikt. De bibliotheek mbox.js of at.js verzendt automatisch het volgen serverwaarden naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het [!UICONTROL Tracking Server] veld leeg laten op de [!UICONTROL Goals & Settings] pagina.

## at.js Versie 0.9.0 {#section_2981CC9792F245389B39BB5B69F84C4E}

**Target-release:** 16.6.1.

**Datum:** 23 juni 2016

* Hiermee verhelpt u een whitescreen-probleem bij het gebruik van VEC-aanbiedingen. Iedereen die deze functie gebruikt, [!DNL at.js] moet een upgrade naar deze nieuwe versie uitvoeren.
* Nieuwe `registerExtension` API.

   Deze nieuwe API biedt ontwikkelaars toegang tot bepaalde jQuery-modules die worden gebruikt [!DNL at.js] om extensies (ook wel insteekmodules genoemd) voor de bibliotheek te ontwikkelen. Er zijn enkele gevolgen voor deze wijziging. Dit is alleen van invloed op gebruikers die de volgende functies gebruiken:

   * `getSettings()` API is verwijderd, maar dezelfde functionaliteit is beschikbaar via `registerExtension()`.
   * `getTracking()` API is verwijderd, maar dezelfde functionaliteit is beschikbaar via `registerExtension()`.

   * Bestaande extensies (bijvoorbeeld AngularJS-extensies) moeten worden bijgewerkt om de `registerExtension()` aanpak te kunnen gebruiken.

* Nieuwe At.js-melding]-API.

   Het doel van dit kennisgevingssysteem is meer inzicht te verschaffen in wat er op de pagina [!DNL at.js] gebeurt en wanneer er problemen zijn. Een veel voorkomend probleem met de VEC is dat een IT-release de pagina wijzigt, een VEC-kiezer afbreekt en de test stopt met het correct leveren van inhoud. Een doel van dit meldingssysteem is om deze leveringskwestie aan de pagina bekend te maken, zodat kunnen de ontwikkelaars tot deze informatie toegang hebben, het tot een systeem als overgaan [!DNL Adobe Analytics], en het alarm kan aan de bedrijfseigenaars worden verzonden dat hun test gebroken.

* Nieuwe `targetGlobalSettings()` API-methode.

   U kunt instellingen in de bibliotheek at.js overschrijven in plaats van de instellingen in de bibliotheek te configureren [!DNL Target Standard/Premium UI]of door REST API&#39;s te gebruiken.

## at.js Versie 0.8.0 {#section_E1C7B08EC0494388A022C28A8B8FE807}

**Datum:** 5 mei 2016.

Dit is de eerste officiële release van de [!DNL at.js] bibliotheek.

[!DNL at.js] is een nieuwe implementatiebibliotheek die is ontworpen voor zowel typische webimplementaties als toepassingen van één pagina. [!DNL Target]

[!DNL at.js] vervangt [!DNL mbox.js] voor [!DNL Adobe Target] implementaties.

>[!NOTE]
>
>Hoewel [!DNL at.js] mbox.js wordt vervangen [!DNL mbox.js], blijft deze ondersteund. Voor de meeste mensen [!DNL at.js] biedt dit meer voordelen dan [!DNL mbox.js]. Dit geeft u tijd om de implementatie op uw pagina&#39;s te testen [!DNL at.js] en te wijzigen.

De laadtijden van pagina&#39;s voor webimplementaties worden [!DNL at.js] onder andere verbeterd, de beveiliging wordt verbeterd en er worden betere implementatieopties geboden voor toepassingen van één pagina.

[!DNL at.js] bevat de componenten die in inbegrepen waren [!DNL target.js], zodat is er niet meer een vraag aan [!DNL target.js].

Houd bij de implementatie rekening met het volgende: [!DNL at.js]

* Internet Explorer-versies ouder dan 8 worden niet ondersteund.
* Asynchrone implementatie betekent dat verouderde integratie, zoals de insteekmodule [!DNL Test&Target] naar [!DNL SiteCatalyst] insteekmodule, mogelijk niet werkt.
* [!DNL Target] plug-ins die verwijzen naar [!DNL mbox.js] objecten en methoden, worden niet ondersteund.
* Alle aanroepen [!DNL Target] worden uitgevoerd via XMLHTTPRequest en de inhoud wordt geretourneerd via JSON.
