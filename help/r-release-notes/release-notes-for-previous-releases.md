---
keywords: Release notes
description: Opmerkingen bij de release voor vorige Target-releases, waaronder releaseopmerkingen voor Target Standard/Premium, het doelplatform en de Javascript-doelbibliotheken (at.js en mbox.js). Opmerkingen bij de release worden in aflopende volgorde weergegeven per maand en jaar van de release.
title: Opmerkingen bij de release van vorige releases
topic: Recommendations
uuid: a1f0ddae-39f1-4e28-bf86-03e82e3cb91e
translation-type: tm+mt
source-git-commit: 2aca4490a70c0f6a1f38fab2e62cdab55b5b7a4f
workflow-type: tm+mt
source-wordcount: '29079'
ht-degree: 0%

---


# Opmerkingen bij de release van vorige releases{#release-notes-for-previous-releases}

Opmerkingen bij de release voor vorige Target-releases, waaronder releaseopmerkingen voor Target Standard/Premium, het doelplatform en de Javascript-doelbibliotheken (at.js en mbox.js). Opmerkingen bij de release worden in aflopende volgorde weergegeven per maand en jaar van de release.

>[!NOTE]
>
>Zie Opmerkingen bij de release [Target (huidig)](../r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) voor informatie over de Target-releases van de huidige maand (platform en Target Standard/Premium).

## Opmerkingen bij de release - 2020

### Doel om.js (25 maart 2020)

De volgende nieuwe versies van de JavaScript-bibliotheken van Target at.js zijn beschikbaar:

* at.js versie 2.3.0
* at.js versie 1.8.1

Zie [de versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)at.js voor meer informatie.

### Target Standard/Premium 20.2.1 (23 maart 2020)

>[!IMPORTANT]
>
>Zie de bovenstaande informatie over de afschrijving van mbox.js.

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij klanten een verzameling niet konden selecteren tijdens het uitvoeren van een cataloguszoekopdracht. (TGT-36230)
* Probleem verholpen waarbij een criterium dat via API is gemaakt, maar waarnaar niet wordt verwezen door een activiteit die in de doelinterface is gemaakt, ten onrechte uit de gebruikersinterface kan worden verwijderd. (TGT-35917)
* Geïmplementeerde veiligheidsverbeteringen aan het Beleid van de Veiligheid van de Inhoud (CSP). (TGT-36190)
* Probleem verholpen waarbij &quot;NaN%&quot; werd weergegeven wanneer de percentagebalk voor kenmerkweging naar links werd verschoven. (TGT-36211)
* Opgeloste lokalisatieproblemen zodat de UI-tekst in verschillende talen correct wordt weergegeven.
* We hebben de lijst met beschikbare meetgegevens van Adobe Analytics for Target (A4T)-activiteiten gestandaardiseerd door de meetgegevens van Adobe Analytics af te drukken die niet worden ondersteund in de huidige versie van Adobe Analytics API&#39;s. Hierdoor kunnen we onze A4T-ondersteuning uitbreiden in toekomstige versies van Adobe Target.

   De volgende wijzigingen zijn aangebracht:

   * &quot;Gemiddelde tijd die op pagina wordt besteed&quot; is vervangen door &quot;Gemiddelde tijd die ter plekke wordt besteed.&quot; Om het even welke activiteiten die dit als metrisch metrisch het Primaire Metrische Doel gebruiken zullen &quot;Gemiddelde Tijd die op Plaats wordt uitgegeven&quot;hebben (nota: (gemeten in minuten in plaats van seconden) geselecteerd als Primair doel Metrisch wanneer de activiteit de volgende keer wordt bewerkt.
   * &quot;Bezoekers&quot; is vervangen door &quot;Unieke Bezoekers&quot;. Voor alle activiteiten waarbij deze metrische waarde wordt gebruikt als &#39;Primaire Goal Metric&#39;, worden &#39;Unieke bezoekers&#39; geselecteerd als &#39;Primaire Goal Metric&#39; wanneer de activiteit de volgende keer wordt bewerkt.

* De volgende metriek zijn afgekeurd en kunnen niet meer worden geselecteerd als Primair doel Metrisch wanneer het creëren van een nieuwe activiteit A4T.

   | Vervangen metrisch(e) | Voorgestelde vervangende metrische(n) |
   |--- |--- |
   | Dagelijkse Bezoekers, Uur Bezoekers, Maandelijkse Bezoekers, Driemaandelijkse Bezoekers, Wekelijkse Bezoekers, Jaarlijkse Bezoekers | Unieke bezoekers |
   | Gemiddelde visdiepte | n.v.t. Niet voorgesteld als primair doel metrisch |
   | Bots | n.v.t. Niet voorgesteld als primair doel metrisch |
   | Snelheid bij vastlopen van mobiele apparaten, Mobile Avg vorige sessielengte, Mobile App Store Avg Rank, Mobile App Performance Crash Rate, Mobile App Store Avg Rating | n.v.t. Niet voorgesteld als primair doel metrisch |

### Adobe Experience Cloud navigation (22 februari 2019)

* Wanneer u zich bij het programma aanmeldt, gaat u naar de nieuwe koptekstnavigatie. [!DNL Adobe Experience Cloud] Het lijkt sterk op de vorige navigatie met de zwarte balk bovenaan, maar biedt de volgende verbeteringen:

   * Eenvoudiger overschakelen tussen [!DNL Identity Management System] (IMS) organisaties of naar een andere oplossing.
   * Verbeterde gebruikershulp: Zoekresultaten zijn resultaten uit de [!DNL Target] productdocumentatie, maar ook uit communityforums en meer video-inhoud. Hierdoor hebt u gemakkelijker toegang tot meer inhoud om optimaal te profiteren [!DNL Target]. We hebben ook een feedbackmechanisme toegevoegd in het [!UICONTROL Help] menu, waardoor het gemakkelijker wordt om problemen te melden of uw ideeën te delen.

   * De verbeterde NPS-feedbackfunctionaliteit (Net Promoter Score), zodat de enquêtemodale modus uw workflow niet verstoort.
   * Verbeterde aanmeldstroom. Eerder zijn alle [!DNL Target] klanten op de bestemmingspagina geland nadat ze op het [!DNL Target] pictogram in de koptekst hadden geklikt. Op deze pagina konden klanten verder gaan met [!DNL Target Standard/Premium], [!DNL Search&Promote]of [!DNL Recommendations Classic], zoals hieronder wordt getoond:

      ![Openingspagina](/help/r-release-notes/assets/landing.png)

      We hebben deze bestemmingspagina voor al onze klanten verwijderd. U wordt nu altijd rechtstreeks naar de [!UICONTROL Activities List] pagina geleid door op het [!DNL Target] pictogram in de nieuwe koptekstnavigatiebalk te klikken.

      Als u gebruikt [!DNL Recommendations Classic], kunt u of rechtstreeks naar de oplossing gaan of u kunt van de korte verbinding gaan die op het [!UICONTROL Recommendations] lusje wordt gecreeerd, zoals hieronder getoond:

      ![Klassieke koppeling opnieuw instellen](/help/r-release-notes/assets/recs-classic.png)

      Als u [!DNL Search&Promote]deze optie gebruikt, moet u rechtstreeks naar de URL [voor](https://center.atomz.com/center/?ims=1) zoeken en bevorderen (https://center.atomz.com/center/?ims=1) gaan. Het pad dat moet worden bereikt [!DNL Search&Promote] van binnenuit van [!DNL Adobe Target] is volledig verwijderd.

   * Meldingen voor [!DNL Target] zijn momenteel niet beschikbaar in de [!UICONTROL Notifications] vervolgkeuzelijst in de koptekst.
   >[!NOTE]
   >
   >Tijdens de introductie van de nieuwe navigatiebalk zult u ook enkele URL-wijzigingen zien. Alle vorige bladwijzerkoppelingen werken nog steeds, maar we raden u aan nieuwe bladwijzerkoppelingen te maken om deze sneller te openen.

### Target Standard/Premium 20.1.1 (4 februari 2020)

De Target Standard/Premium 20.1.1-release is een onderhoudrelease en bevat verbeteringen en verbeteringen voor de back-endserver. Daarnaast zijn de volgende correcties opgenomen:

* Probleem verholpen waarbij het serverveld Adobe Analytics tracking leeg was op de pagina Doelstellingen en instellingen voor bestaande Adobe for Target-activiteiten (A4T). (TGT-35960)
* Probleem verholpen in de gebruikersinterface waardoor de selectie in de tweede vervolgkeuzelijst niet werd weergegeven tijdens het maken van een publiek voor categorie-affiniteit. (TGT-36098)

## Opmerkingen bij de release - 2019 {#releases-2019}

### Target Java SDK versie 1.1.0 (16 december 2019)

* Ondersteuning voor proxyconfig toegevoegd vanwege een open-bronbijdrage van @hisham-hassan.

Zie Opmerkingen bij de [release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md)voor meer informatie.

### Doel Java SDK versie 1.0.1 (11 november 2019)

Het volgende probleem is opgelost in versie 1.0.1:

* Stuur een aanvullende gegevens-id in een doelaanvraag, zelfs als er geen bezoeker-API cookie aanwezig is.

Zie Opmerkingen bij de [release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md)voor meer informatie.

### Doelplatform (31 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Java SDK | Met de [!DNL Target] Java SDK kunt u [!DNL Target] server-side implementeren. Met deze Java SDK kunt u eenvoudig integreren [!DNL Target] met andere [!DNL Adobe Experience Cloud] oplossingen, zoals de [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics]en [!DNL Adobe Audience Manager].<br>De SDK van Java introduceert beste praktijken en verwijdert ingewikkeldheid wanneer het integreren met [!DNL Target] via onze levering API zodat uw techniekteams zich op bedrijfslogica kunnen concentreren. Hieronder volgen opmerkelijke elementen die we in de nieuwste versie introduceren:<ul><li>Ondersteuning voor prefetching en meldingen waarmee u de prestaties kunt optimaliseren via caching.</li><li>Ondersteuning voor het optimaliseren van prestaties wanneer u een hybride integratie van [!DNL Target] zowel webpagina&#39;s als serverpagina&#39;s hebt. Wij introduceren het plaatsen genoemd `serverState` die door ervaringen wordt bevolkt die via server-kant worden teruggewonnen zodat at.js 2.2 geen extra servervraag meer zal maken om de ervaringen terug te winnen. Deze aanpak optimaliseert de prestaties bij het laden van pagina&#39;s.</li><li>Ondersteuning voor het ophalen van VEC-activiteiten via de Java SDK, wat mogelijk wordt gemaakt door de nieuwe Delivery API.</li><li>Open-sourced zodat uw ontwikkelaars kunnen bijdragen aan de [Target Java SDK](https://github.com/adobe/target-java-sdk).</li></ul>Zie Opmerkingen bij de [release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md)voor meer informatie.<br>Meer informatie over de Target Java SDK vindt u op de Adobe Tech Blog - [Server-Side Optimization met de nieuwe Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2). |

### Target Standard/Premium 19.10.2 (31 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) Multi-value-kenmerken | Soms wilt u werken met een veld met meerdere waarden. Neem de volgende voorbeelden:<ul><li>U biedt films aan gebruikers aan. Een bepaalde film heeft meerdere acteurs.</li><li>Je verkoopt tickets aan concerten. Een bepaalde gebruiker heeft meerdere favoriete banden.</li><li>Je verkoopt kleding. Een shirt is verkrijgbaar in verschillende formaten.</li></ul>Om aanbevelingen in deze scenario&#39;s te behandelen, kunt u multi-waardegegevens tot de Aanbevelingen van het Doel overgaan en speciale multi-waardeexploitanten gebruiken.<br>Zie [Werken met kenmerken](/help/c-recommendations/c-algorithms/work-with-multi-value-attributes.md)met meerdere waarden voor meer informatie. |

### Target Standard/Premium 19.10.1 (22 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium badge](/help/assets/premium.png) Op gebruiker gebaseerde aanbevelingen<br>(24 oktober 2019) | Aanbevolen objecten op basis van de browsergeschiedenis, weergavegeschiedenis en aankoopgeschiedenis van elke bezoeker. Deze objecten worden doorgaans &#39;Aanbevolen voor je&#39; genoemd.<br>Met deze criteria kunt u persoonlijke inhoud en ervaringen aanbieden aan zowel nieuwe als geretourneerde bezoekers. De lijst met aanbevelingen is gericht op de meest recente activiteit van de bezoeker en wordt tijdens de sessie bijgewerkt en wordt meer gepersonaliseerd naarmate de bezoeker door uw site bladert.<br>Zie op gebruiker gebaseerde aanbevelingen in [criteria/algoritmen](/help/c-recommendations/c-algorithms/algorithms.md#criteria-algorithms)voor meer informatie. |

**Adobe Experience Cloud-navigatie**

* Wanneer u zich bij het programma aanmeldt, gaat u naar de nieuwe koptekstnavigatie. [!DNL Adobe Experience Cloud] Het lijkt sterk op de vorige navigatie met de zwarte balk bovenaan, maar biedt de volgende verbeteringen:

   * Eenvoudiger overschakelen tussen [!DNL Identity Management System] (IMS) organisaties of naar een andere oplossing.
   * Verbeterde gebruikershulp: Zoekresultaten zijn resultaten uit de [!DNL Target] productdocumentatie, maar ook uit communityforums en meer video-inhoud. Hierdoor hebt u gemakkelijker toegang tot meer inhoud om optimaal te profiteren [!DNL Target]. We hebben ook een feedbackmechanisme toegevoegd in het [!UICONTROL Help] menu, waardoor het gemakkelijker wordt om problemen te melden of uw ideeën te delen.

   * De verbeterde NPS-feedbackfunctionaliteit (Net Promoter Score), zodat de enquêtemodale modus uw workflow niet verstoort.
   * Verbeterde aanmeldstroom. Eerder zijn alle [!DNL Target] klanten op de bestemmingspagina geland nadat ze op het [!DNL Target] pictogram in de koptekst hadden geklikt. Op deze pagina konden klanten verder gaan met [!DNL Target Standard/Premium], [!DNL Search&Promote]of [!DNL Recommendations Classic], zoals hieronder wordt getoond:

      ![Openingspagina](/help/r-release-notes/assets/landing.png)

      We hebben deze bestemmingspagina voor al onze klanten verwijderd. U wordt nu altijd rechtstreeks naar de [!UICONTROL Activities List] pagina geleid door op het [!DNL Target] pictogram in de nieuwe koptekstnavigatiebalk te klikken.

      Als u gebruikt [!DNL Recommendations Classic], kunt u of rechtstreeks naar de oplossing gaan of u kunt van de korte verbinding gaan die op het [!UICONTROL Recommendations] lusje wordt gecreeerd, zoals hieronder getoond:

      ![Klassieke koppeling opnieuw instellen](/help/r-release-notes/assets/recs-classic.png)

      Als u [!DNL Search&Promote]deze optie gebruikt, moet u rechtstreeks naar de URL [voor](https://center.atomz.com/center/?ims=1) zoeken en bevorderen (https://center.atomz.com/center/?ims=1) gaan. Het pad dat moet worden bereikt [!DNL Search&Promote] van binnenuit van [!DNL Adobe Target] is volledig verwijderd.

   * Meldingen voor [!DNL Target] zijn momenteel niet beschikbaar in de [!UICONTROL Notifications] vervolgkeuzelijst in de koptekst.
   >[!NOTE]
   >
   >Deze functies worden niet meteen geïmplementeerd en worden ook niet samen aan alle klanten aangeboden. We zullen deze functies in de loop van de komende weken implementeren, te beginnen met de release [!DNL Target Standard/Premium] 19.10.1 (22 oktober 2019).
   >
   >Tijdens de introductie van de nieuwe navigatiebalk zult u ook enkele URL-wijzigingen zien. Alle vorige bladwijzerkoppelingen werken nog steeds, maar we raden u aan nieuwe bladwijzerkoppelingen te maken om deze sneller te openen.

### at.js versie 2.2 en 1.8 (10 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| at.js versie 2.2<br><br>andat.js versie 1.8 | Deze versies van at.js verstrekken:<ul><li>Verbeterde prestaties bij het gebruik van de Experience Cloud ID Service (ECID) v4.4 en at.js 2.2 of at.js 1.8 op uw webpagina&#39;s.</li><li>Eerder, maakte ECID twee blokkerende vraag alvorens at.js ervaringen kon halen. Dit is verminderd tot één enkele vraag, die beduidend prestaties verbetert.</li></ul> Als u deze prestatieverbeteringen wilt benutten, kunt u de upgrade naar at.js 2.2 of at.js 1.8 in combinatie met ECID Library v4.4.<br>at.js 2.2 uitvoeren:<ul><li>**serverState**: Een instelling die beschikbaar is in at.js v2.2+ en die kan worden gebruikt om de paginaprestaties te optimaliseren wanneer een hybride integratie van Target wordt geïmplementeerd. Hybride integratie betekent dat u zowel at.js v2.2+ op de client-kant als de levering-API of een doel-SDK op de server-kant gebruikt om ervaringen te bieden. `serverState` geeft at.js v2.2+ de capaciteit om ervaringen direct van inhoud toe te passen die op de server wordt gehaald en aan de cliënt als deel van de pagina teruggegeven wordt.<br>Zie &quot;serverState&quot; in [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#server-state)voor meer informatie.</li></ul> |

### Doelplatform (9 oktober 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Node.js SDK versie 1.0 | Met de SDK van Target Node.js kunt u de doelserver implementeren.<br>Met deze Node.js SDK kunt u Target eenvoudig integreren met andere Experience Cloud-oplossingen, zoals de Adobe Experience Cloud Identity Service, Adobe Analytics en Adobe Audience Manager.<br>De SDK van Node.js introduceert best practices en verwijdert complexiteit bij de integratie met Adobe Target via onze API voor levering, zodat uw engineeringteams zich kunnen richten op bedrijfslogica. Hieronder volgen opmerkelijke elementen die we in de nieuwste versie introduceren:<ul><li>Ondersteuning voor prefetching en meldingen waarmee u de prestaties kunt optimaliseren via caching.</li><li>Ondersteuning voor het optimaliseren van prestaties wanneer u een hybride integratie van Target hebt op zowel uw webpagina&#39;s als op de server. Wij introduceren het plaatsen genoemd `serverState` die door ervaringen zal worden bevolkt die via server-kant worden teruggewonnen zodat at.js 2.2 geen extra servervraag meer zal maken om de ervaringen terug te winnen. Deze aanpak optimaliseert de prestaties bij het laden van pagina&#39;s.</li><li> Steun voor het terugwinnen van VEC-gecreeerde activiteiten via Node.js SDK, die door nieuwe Levering API mogelijk wordt gemaakt.</li><li>Open-sourced zodat uw ontwikkelaars een bijdrage kunnen leveren aan de Node.js SDK.</li></ul><br>Voor meer informatie, zie de Nota&#39;s van de [Versie - Doel Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md). |
| Leverings-API | Een geheel nieuw levering API eindpunt (/v1/levering) is beschikbaar in productie. Opmerkelijke functies zijn:<ul><li>Één eindpunt om ervaringen voor één of meerdere dozen terug te winnen.</li><li>Haal VEC-activiteiten op via de API.</li><li>Ondersteuning voor een geheel nieuw object genaamd Weergaven dat wordt gebruikt voor toepassingen van één pagina (SPA&#39;s) en mobiele toepassingen.</li></ul><br>Zie Opmerkingen bij de [release - Doelserver-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md)voor meer informatie. |

### Target Standard/Premium 19.9.2 (30 september 2019)

Deze onderhoudrelease bevat de volgende verbeteringen:

* Verscheidene veiligheidsmoeilijke situaties, met inbegrip van een veiligheidsupdate aan de Rich Text Editor (RTE) in de Visuele Composer van de Ervaring (VEC). (TGT-35383)
* Aanbevelingen kunnen nu worden toegevoegd aan andere elementen dan DIV (bv. P, UL, H1), naast DIV, in A/B Test and Experience Targeting-activiteiten. (TGT-34333)
* Gebeurtenismeldingen (het belpictogram in de doelgebruikersinterface) zijn niet meer beschikbaar. Binnenkort wordt er een nieuwe zoekfunctie voor meldingen weergegeven.

### Target Standard/Premium 19.9.1 (10 september 2019)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium-badge](/help/assets/premium.png) Enterprise-machtigingen | Met de Target-release van september 2019 bieden Enterprise-machtigingen klanten de volgende toegangsopties:<UL><li>U kunt de werkruimten kiezen waarop de integratie kan worden toegepast.</li><li>U kunt een rol op de integratie van Adobe I/O toepassen: Fiatteur, Editor of waarnemer.</li></ul>Zie [Adobe I/O-integraties toegang verlenen tot werkruimten en rollen](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md)toewijzen voor stapsgewijze instructies en meer informatie. |

### Target Standard/Premium 19.7.1 (24 juli 2019) {#tgt-19-7-1}

Deze release bevat de volgende nieuwe functies en verbeteringen:

(De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Premium](/help/assets/premium.png)<br>badgeRecommendations in A/B Test and Experience Targeting (XT)-activiteiten | De de statusvertoningen van de Aanbiedingen van Aanbevelingen (algoritme) op de pagina van het Overzicht voor A/B Test en XT activiteiten die de aanbiedingen van Aanbevelingen bevatten. Voorbeelden van statussen zijn: Resultaten gereed, resultaten niet gereed en Feed-fout. (TGT-33649)<br>Zie [Aanbevelingen als aanbieding](/help/c-recommendations/recommendations-as-an-offer.md#status). |
| Ondersteuning voor interdomeintracering voor at.js 2.0+ via de ECID-bibliotheek (Experience Cloud ID) | Eerder werd interdomeintracering niet ondersteund in at.js 2.*x*. Met deze release kunnen klanten die at.js 2.0 of hoger gebruiken nu interdomeintracering gebruiken via de ECID-bibliotheek. De ECID-bibliotheek moet op de pagina worden geïnstalleerd in combinatie met at.js 2.0 of hoger om interdomeintracering mogelijk te maken. [Gebruik hiervoor de Cloud ID-bibliotheek 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) .<br>Zie Ondersteuning voor [interdomeintracering in at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md#cross-domain). |
| Doelondersteuning voor ITP 2.1 en ITP 2.2 van Apple via de Experience Cloud ID-bibliotheek 4.3 | Vandaag, kunnen de klanten van het Doel ITP 2.1 en ITP 2.2 van Apple verlichten door het certificatieprogramma van CNAME van Adobe te gebruiken.<br>Met deze release introduceert Target een naadloze integratie met de ECID-bibliotheek 4.3, die een servercookie gebruikt om ITP 2.1 en ITP 2.2 te beperken. Het wordt ten zeerste aanbevolen dat doelklanten [ECID-bibliotheek 4.3+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) samen met de JavaScript-bibliotheek van Target implementeren om toekomstige ITP-releases te beperken. De ECID-bibliotheek blijft verbeterde functies implementeren die een robuuste oplossing bieden voor het voortdurend veranderende beleid van cookies dat door browsers wordt geïntroduceerd.<br>Zie [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md). |

**Verbeteringen, correcties en wijzigingen**

* Probleem verholpen waarbij werd voorkomen dat uitsluitingswaarden in activiteiten met aanbevelingen werden gewist bij het toevoegen van dubbele waarden. (TGT-34996)
* U kunt nu een ontwerp in een activiteit van Aanbevelingen uit de Doelpagina (Stap 2 van de driedelige geleide werkschema) verwijderen. Als u een ontwerp wilt verwijderen, moet er meer dan één ontwerp zijn geselecteerd. (TGT-35118)
* Probleem verholpen waarbij aangepaste criteria niet konden worden gebruikt voor het correct laden van bepaalde klanten in de interface van het doel of om te kunnen worden bewerkt. (TGT-35170)

### at.js versie 2.1.1 (24 juli 2019)

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

Voor informatie over dit en vorige versies van at.js, zie [at.js versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

### Target Standard/Premium 19.6.1 (26 juni 2019) {#tgt-19-6-1-historical}

Deze release bevat de volgende nieuwe functies en verbeteringen:

(De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Visual Experience Composer (VEC) | **Nieuwe VEC-menuopties**: Wanneer u een paginaelement in VEC klikt, toont een menu de opties die voor dat elementtype beschikbaar zijn.<ul><li>U kunt nu de [!UICONTROL Styles > Background] optie gebruiken om de achtergrondafbeelding en -kleur voor het geselecteerde element te wijzigen. (TGT-15001)</li></ul>Zie *Stijlen* in de Opties [van de](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles)Visuele Ervaring.<br>**Verbeteringen **voor klikspatiëring: Wij hebben het proces verbeterd om klik het volgen binnen VEC en de Enige Toepassing van de Pagina (SPA) VEC te vormen.<ul><li>Als u elementen selecteert die u wilt gebruiken bij het bijhouden van klikken, worden de namen van alle beschikbare elementen aan de rechterkant weergegeven in het deelvenster Wijzigingen, zodat u snel en gemakkelijk de gewenste elementen kunt selecteren.</li><li>Op de [!UICONTROL Goals & Settings] pagina met instructies-workflow voor drie delen wordt een nummer weergegeven dat het aantal elementen vertegenwoordigt dat is geselecteerd voor het bijhouden van klikken. U kunt de muisaanwijzer op dit nummer plaatsen om de namen van alle geselecteerde elementen weer te geven. (TGT-33878)</li></ul>Zie [Klikken op bijhouden](/help/c-activities/r-success-metrics/click-tracking.md). |
| Single Page App Visual Experience Composer (SPA VEC) | **Workflow** met instructies: Een nieuwe geleide werkstroom helpt u begrijpen hoe pagina-levering-regel montages zou moeten worden gevormd om een activiteit voor uw Enige Pagina App met succes uit te voeren en in werking te stellen. (TGT-33718)<br> Zie [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Kloonwijzigingen **: U kunt een wijziging nu bepalen gebruikend het KUUROORD VEC en dan klonen die wijziging voor gebruik in andere meningen in uw Enige Pagina App. (TGT-33882)<br>Zie[Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md). |
| ![Premium-badge](/help/assets/premium.png) Automated Personalization (AP) en Auto-Target | **Specifieke ervaring als controle**: U kunt een ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een AP of een auto-Doel activiteit. Deze eigenschap laat u het volledige controleverkeer aan een specifieke ervaring leiden, die op het percentage van de verkeerstoewijzing wordt gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die één ervaring dan evalueren. De huidige controleoptie (willekeurig bediende ervaringen) zal beschikbaar blijven. (TGT-32801, TGT-26572, &amp; TGT-26571)<br>Zie [Selecteer de controle voor uw Geautomatiseerde Personalisatie of auto-Doel Activiteit](/help/c-activities/t-automated-personalization/experience-as-control.md). Er is een [bekend probleem](/help/r-release-notes/known-issues-resolved-issues.md) met deze functie.<br>**Persoonlijkheidsgegevens **: De markeringsvriendelijke naamgeving voor kenmerken wanneer een bezoeker een bepaald stuk inhoud op een specifieke locatie ziet, levert zinvollere informatie op. (TGT-33421 &amp; TGT-34957)<br>Zie[Gegevensverzameling voor de de verpersoonlijkingsalgoritmen](/help/c-activities/t-automated-personalization/ap-data.md)van het Doel. |
| ![Aanbevelingen voor speciale badge](/help/assets/premium.png) | U kunt de optie Aanbevolen eerder aangeschafte items gebruiken tijdens het maken van de logica Onlangs bekeken items. (TGT-34030)<br>Zie [Onlangs bekeken Punten](/help/c-recommendations/c-algorithms/create-new-algorithm.md#previously-purchased) in &quot;criteria creëren&quot;voor meer informatie. |
| Google Chrome SameSite-cookiebeleid | Google heeft onlangs aangekondigd dat ontwikkelaars vanaf Chrome 76, die is gepland voor een release van 30 juli 2019, expliciet moeten opgeven welke cookies op verschillende websites kunnen werken en welke cookies gebruikers kunnen volgen.<br>Aangezien de industrie streeft naar het creëren van een veiliger web voor consumenten, is Target absoluut geëngageerd om persoonlijke ervaringen te leveren terwijl aan de privacyverwachtingen van bezoekers wordt voldaan en deze wordt overschreden.<br>Zie [Google Chrome SameSite cookie policies](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md). |

### at.js versie 2.1.0 (3 juni 2019) {#atjs-210}

We zijn blij om de volgende spannende functies aan te kondigen in at.js 2.1.0:

| Functie/verbetering | Beschrijving |
| --- | --- |
| Ondersteuning voor Adobe Opt-in | Adobe Opt-In is een manier om de integratie van Adobe-oplossingen met compatibiliteitsbeheerplatforms te vereenvoudigen.<br>Zie [Privacy and General Data Protection Regulation (GDPR)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)voor meer informatie over Adobe Opt-in. |
| Compatibel met industriestandaard CSP | at.js gebruikt eval() niet meer om JavaScript uit te voeren. |
| Logboekregistratie voor analyses op de client | Klanten hebben volledige controle over de manier waarop ze analysegegevens naar Adobe Analytics willen verzenden, zowel op de client als op de server.<br>Voor meer informatie, zie [cliënt-kant Analytics het registreren](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Alvorens u uitvoert*. |
| Meldingen verzenden | Staat ontwikkelaars toe om berichten te verzenden wanneer een ervaring door hun code in plaats van het gebruiken `applyOffer()` of `applyOffers()`wordt teruggegeven.<br>Zie [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)voor meer informatie. |
| Beperkte bestandsgrootte | De grootte van at.js wordt verminderd met ~24%. De kleinere bestandsgrootte verbetert de laadprestaties van de pagina en verkort de downloadtijd op .js op de pagina. |
| op.js documentatie updates | Voor een volledige lijst van alle artikelen die wegens de versie van at.js 2.1.0 worden bijgewerkt, zie de 3 juni 2019 ingangen in de veranderingen [van de](/help/r-release-notes/doc-change.md)Documentatie. |

### [!DNL Target] Standard/Premium 19.5.1 (21 mei 2019) {#tgt-19-5-1-historical}

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

#### Functie-updates

| Functie/verbetering | Beschrijving |
| --- | --- |
| Single Page App Visual Experience Composer (SPA VEC) | Het KUUROORD VEC omvat de volgende verhogingen om uw werk sneller en efficiënter te maken:<ul><li>Wanneer u op een handeling in de SPA klikt, wordt het element op de site gemarkeerd waarop deze handeling wordt toegepast. Elke VEC-actie die onder een weergave wordt gemaakt, heeft vier corresponderende pictogrammen: Informatie, Bewerken, Verplaatsen en Verwijderen. Met de nieuwe functie &quot;Verplaatsen&quot; in deze release kunt u de handeling verplaatsen naar een gebeurtenis Pagina laden of een andere weergave die al bestaat in het deelvenster Wijzigingen. (TGT-33746)</li><li>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel). Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de doelinterface. (TGT-33851 &amp; TGT-34149)</li></ul>Voor meer informatie, zie [Enige Pagina App (SPA) Visuele Composer](/help/c-experiences/spa-visual-experience-composer.md)van de Ervaring. |

#### Verbeteringen, correcties en wijzigingen

* De pictogrammen van de werkbalk worden correct weergegeven nadat u het laden van een pagina in de VEC hebt geannuleerd. Als specifieke handelingen pas kunnen worden uitgevoerd nadat de pagina volledig is geladen, worden de bijbehorende werkbalkpictogrammen uitgeschakeld. (TGT-33811)

### [!DNL Target] Standard/Premium 19.4.2 (30 april 2019) {#release-19-4-2}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

#### Functie-updates

| Functie/verbetering | Beschrijving |
| --- | --- |
| [!UICONTROL Visual Experience Composer] | De [!UICONTROL Visual Experience Composer] (VEC) bevat de volgende verbeteringen om uw werk sneller en efficiënter te maken:<ul><li>De DOM-padfunctie is nu beschikbaar wanneer u klikt op bijhouden.<br>Zie [Klikken op bijhouden](/help/c-activities/r-success-metrics/click-tracking.md#considerations)voor meer informatie.</li><li>In het deelvenster Stijlen kunt u de waarde van bestaande stijlen voor het geselecteerde element weergeven of bewerken. U kunt ook extra stijlen toevoegen.<br>U opent het deelvenster Stijlen door vanuit de VEC op een pagina-element te klikken en vervolgens op [!UICONTROL Edit] > [!UICONTROL Styles]te klikken.<br>Het deelvenster Stijlen wordt rechts van de VEC weergegeven. Het deelvenster bevat een lijst met stijlen waarmee u het geselecteerde element kunt bewerken of uitbreiden. Met een real-time CSS-editor kunt u wijzigingen weergeven en stijlen toevoegen als u dit comfortabel vindt met CSS (Cascading Style Sheets) of als u code van uw ontwikkelaar ontvangt.<br>Voor meer informatie, zie [Stijlen](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles) in de Opties *van de Composer van de* Visueel Ervaring.</li><li>De Rich Text Editor ondersteunt nu geneste HTML5-elementen.<br>HTML5-specificaties staan nieuwe combinaties van tags voor nesten toe. In de vorige versie van de RTF-editor werd het nesten van tags niet ondersteund, zoals is toegestaan door de HTML5-specificatie. Dientengevolge, werden om het even welke genestelde die elementen in VEC werden geselecteerd niet behoorlijk behandeld, die tot ongewenste HTML- veranderingen leidden. (TGT-33618)<br>Zie Tekst/HTML [](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#edit-text-html) bewerken in Composer-opties *voor* visuele ervaring voor meer informatie.</li> |

#### Verbeteringen, correcties en wijzigingen

* We hebben de workflow verbeterd wanneer u elementen verwijdert met de VEC. Verwijderde elementen worden nu verwijderd uit de map [!UICONTROL Offers library] en uit [!DNL Scene7] (indien van toepassing). Verwijderde elementen worden niet meer weergegeven in zoekresultaten. (TGT-31981)
* U kunt nu elementmappen verwijderen, zelfs als deze afbeeldingen bevatten (niet-lege mappen). (TGT-33265)

   Eerder kon u geen niet-lege map verwijderen uit de bibliotheek met doelafbeeldingen ([!UICONTROL Offers] > [!UICONTROL Image Offers]). Er wordt dan een &#39;&#39;Map is niet leeg!&#39;&#39; weergegeven bericht wanneer u probeert de map te verwijderen uit de gebruikersinterface.  Met deze functie voegen we de mogelijkheid toe om het verwijderen van mappen uit te voeren en een volledige map te verwijderen die een willekeurig aantal elementen en submappen in de map bevat. Deze functie is beschikbaar in de doelgebruikersinterface en in de gebruikersinterface van Adobe Experience Cloud Assets.

   * U kunt niet-lege mappen uit de bibliotheek met afbeeldingsaanbiedingen verwijderen. Als in geen enkele activiteit naar alle afbeeldingen in de map wordt verwezen, worden de volledige map en de inhoud ervan verwijderd. Als er in een willekeurige activiteit naar bepaalde afbeeldingen in de map wordt verwezen, worden alle afbeeldingen zonder referenties verwijderd, maar blijven de afbeeldingen en mappen waarin naar wordt verwezen, behouden.
   * Het renderen van afbeeldingsaanbiedingen in de Afbeeldingselementkiezer gaat sneller en efficiënter.
   Zie [Werken met inhoud in de bibliotheek](/help/c-experiences/c-manage-content/assets-working.md)voor meer informatie. (TGT-32897)

* We hebben de rendering van afbeeldingsaanbiedingen verbeterd in de middelenkiezer. Het weergeven en selecteren van aanbiedingen voor afbeeldingen gaat nu sneller en efficiënter. (TGT-32897)
* We hebben de verwerking van omleidingen naar URL&#39;s verbeterd wanneer u het laden van een pagina in de VEC annuleert. (TGT-33815)
* Nadat u een [!UICONTROL Recommendations] verzameling hebt geselecteerd in de kiezer voor verzamelingen, moet u nu op de [!UICONTROL Save] knop klikken. Deze workflow is consistent met andere workflows binnen [!DNL Target]. (TGT-33205)
* Probleem verholpen waarbij een kleine set inzichtsrapporten 0% omzettingspercentages retourneerde in plaats van de werkelijke omrekeningskoersen. (TNT-32125)

### [!DNL Target] Standard/Premium 19.4.1 (15 april 2019) {#release-19-4-1}

Deze release is een onderhoudrelease en bevat de volgende wijziging:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

* De [!DNL Adobe Experience Cloud] gebruikersinterface is bijgewerkt om de wijzigingen in branding en producten weer te geven. (TGT-33546, TGT-33272, en TGT-33331)

#### [!DNL Target] Standard/Premium 19.3.1 (29 maart 2019) {#release-19-3-1}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Visual Experience Composer | Visual Experience Composer (VEC) omvat de volgende verhogingen om uw werk sneller en efficiënter te maken:<ul><li>U kunt het laden van een website in VEC nu annuleren om het bewerken van een activiteit te deblokkeren. Deze verbetering is bijvoorbeeld handig als u een kleine bewerking wilt uitvoeren op de activiteit, de instellingen wilt controleren of aangepaste code wilt toevoegen en u niet wilt wachten tot de site is geladen. (TGT-31288)<br>Zie Het laden van een pagina in de VEC [](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#cancel-loading)annuleren.</li><li>U kunt vele acties uitvoeren alvorens de pagina in VEC laadt, of zelfs als de pagina er niet in slaagt volledig te laden (bijvoorbeeld, is de douanecode niet meer operationeel). Handelingen die niet kunnen worden bewerkt voordat de site wordt geladen, worden uitgeschakeld in de doelinterface. (TGT-31288, TGT-31611, en TGT-32602)<br>Zie Een pagina [bewerken terwijl de pagina wordt geladen of nadat de pagina niet is geladen](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md#loading).</li><li>De VEC geeft het DOM-pad weer, zodat u het juiste element eenvoudig kunt selecteren tijdens het maken of bewerken van ervaringen. (TGT-13422)<br>Zie [Navigeren door elementen die het DOM-pad](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path)gebruiken.</li></ul> |

### at.js versie 2.0.1 (19 maart 2019) {#atjs201}

Dit is een onderhoudrelease met de volgende verbeteringen en oplossingen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

* Probleem verholpen met een zeldzame omstandigheid in de opiniepeilingscode voor DOM die JavaScript-uitzonderingen voor bepaalde klanten veroorzaakte. (TNT-31869)
* Meldingen dat weergaven werden gerenderd, zijn losgekoppeld van gebeurtenishandlers voor het bijhouden van klikken. In eerste instantie heeft Target geen meldingen verzonden als click-event-handlers die tot een weergegeven weergave behoren, niet konden worden gekoppeld. Het doel verzendt nu een meningsbericht zelfs wanneer de klikelementen niet worden gevonden. (TNT-31969)
* Probleem verholpen waarbij de omleidingsvlag voor de gebeurtenis die na het verzoek werd uitgevoerd, altijd werd ingesteld op true. (TNT-31907)
* Probleem opgelost dat ertoe leidde dat VEC opnieuw rangschikte actie als succes werd geregistreerd, zelfs wanneer de elementen ontbraken. (TNT-31924)
* Probleem opgelost waarbij meldingen voor bepaalde klanten werden verzonden om de eigenschappentoken voor Enterprise-machtigingen niet te bevatten. (TNT-31999)

>[!NOTE]
>
>Als u [!DNL Adobe] Opt-in steun voor de Algemene Verordening van de Bescherming van Gegevens (GDPR) vereist, zou u bij.js 1.7.1 moeten uitvoeren. Ondersteuning voor aanmelden wordt momenteel niet ondersteund in at.js 2.*x*.

### at.js versie 1.7.1 (19 maart 2019) {#atjs171}

Dit is een onderhoudrelease met de volgende oplossing:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

* Probleem verholpen met een zeldzame omstandigheid in de opiniepeilingscode voor DOM die JavaScript-uitzonderingen voor bepaalde klanten veroorzaakte. (TNT-31869)

### Platformwijzigingen (19 februari 2019) {#atjs2}

| Functie/verbetering | Beschrijving |
| --- | --- |
| te.js versie 2.0.0<br>19 februari 2019 | at.js 2.x is nu beschikbaar.<br>De nieuwste versie van at.js verstrekt rijke eigenschapreeksen die uw zaken uitrusten om verpersoonlijking op volgende generatie cliënt-zijtechnologieën uit te voeren. Deze nieuwe versie wordt geconcentreerd op bevordering at.js om harmonieuze interactie met enige paginatoepassingen (SPAs) te hebben.<br>Hier volgen enkele voordelen van het gebruik van at.js 2.x die niet beschikbaar zijn in eerdere versies:<ul><li>De capaciteit om alle aanbiedingen op paginading in het voorgeheugen onder te brengen om veelvoudige servervraag aan één enkele servervraag te verminderen.</li><li>Verbeter de ervaringen van uw eindgebruikers op uw site aanzienlijk, omdat aanbiedingen direct via het cachegeheugen worden weergegeven zonder vertraging die traditionele serveraanroepen introduceren.</li><li>Eenvoudige one-line van code en éénmalige ontwikkelaarsopstelling om uw marketers toe te laten om A/B en de activiteiten van de Ervaring (XT) via Visual Experience Composer (VEC) op uw enige paginatoepassingen tot stand te brengen en in werking te stellen.</li></ul>at.js 2.x introduceert de volgende nieuwe functies:<ul><li>getOffers()</li><li>applyOffers()</li><li>triggerView()</li></ul>De volgende functies zijn vervangen door de introductie van at.js 2.x:<ul><li>mboxCreate()</li><li>mboxDefine</li><li>registerExtension()</li></ul>Voor meer informatie, zie [Bevordering van at.js 1.x aan at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/upgrading-from-atjs-1x-to-atjs-20.md) en [at.js functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md).<br>**Opmerking **: Als u ondersteuning voor Adobe Opt-in nodig hebt voor de[algemene gegevensbeschermingsverordening](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md)(GDPR), moet u momenteel op 0,js 1.7.0 werken. Ondersteuning voor aanmelden wordt niet ondersteund in at.js 2.x. |
| te.js versie 1.7.0<br>februari 2019 | om.js 1.7.0 is beschikbaar.<br>Deze release biedt ondersteuning voor Adobe Opt-In. Adobe Opt-In is een manier om de integratie van Adobe-oplossingen met compatibiliteitsbeheerplatforms te vereenvoudigen.<br>Voor meer informatie over Adobe Opt-in, zie [Privacy en Algemene Verordening](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) van de Bescherming van Gegevens (GDPR).<br>Deze versie verhelpt ook een probleem waarbij Doel URL-parameters omleiden kan negeren met parameters die afkomstig zijn van de omleidings-URL.<br>**Opmerking **: Als u ondersteuning voor Adobe Opt-in voor GDPR nodig hebt, moet u momenteel op 0.js 1.7.0 gebruiken. Ondersteuning voor aanmelden wordt niet ondersteund in at.js 2.x.<br>Raadpleeg de versiedetails[van](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)at.js voor een lijst met alle versies. |

### [!DNL Target] Standard/Premium 19.2.1 (19 februari 2019) {#target-19-2-1}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Single Page App Visual Experience Composer | De visuele Composer van de Ervaring (VEC) voor Enige Pagina Apps (SPAs) laat marketers tests tot stand brengen en inhoud op SPAs op een doe-het-zelf wijze zonder ononderbroken ontwikkelingsgebiedsdelen personaliseren. De VEC kan worden gebruikt om activiteiten op populaire kaders, zoals React en Angular tot stand te brengen. (TGT-27916)<br>Voor meer informatie, zie [Enige Pagina App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md) en de integratie [van de Toepassing van de](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md)Enige Pagina.<br>Naast het bovengenoemde artikel, zijn er vele onderwerpen met betrekking tot SPAs en at.js die deze eigenschap richten en hoe te om het uit te voeren. Zie Wijzigingen in [documentatie voor meer informatie](/help/r-release-notes/doc-change.md). |
| Visual Experience Composer | Visual Experience Composer (VEC) omvat de volgende verhogingen om uw werk sneller en efficiënter te maken:<ul><li>U kunt nu de opties Invoegen voor en Invoegen na in de VEC gebruiken terwijl u [AEM-ervaringsfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md)invoegt. Zie Opties voor [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/viztarget-options.md). (TGT-32385)</li><li>Met de extensie van de VEC Helper-browser voor Google Chrome kunt u websites betrouwbaar laden binnen de VEC zodat u snel een product kunt ontwerpen en een kwaliteitscontrole kunt gebruiken. [!DNL Adobe Target] Zie [Visual Experience Composer helperuitbreiding](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). (TGT-32746)</li></ul> |
| ![Premium](/help/assets/premium.png)<br>badgeRecommendations in [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] activiteiten | U kunt nu aanbevelingen opnemen binnen [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten. Dit opent volledig nieuwe mogelijkheden, zoals:<ul><li>Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.</li><li>Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.</li><li>Duw automatisch verkeer aan de best-presterende aanbevolen ervaring het gebruiken [!UICONTROL Auto-Allocate].</li><li>Wijs bezoekers dynamisch toe aan op maat gesneden aanbevelingen die op hun individuele profielen worden gebaseerd gebruikend [!UICONTROL Auto-Target].</li></ul>Om te beginnen, creeer een [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] activiteit gebruikend VEC en gebruik [!UICONTROL Insert Before], [!UICONTROL Insert After], of [!UICONTROL Replace With] actie om aanbevelingen aan een ervaring toe te voegen. (RECS-6166)<br>Zie [Aanbevelingen als een aanbieding](/help/c-recommendations/recommendations-as-an-offer.md)voor meer informatie. |
| ![Premium-](/help/assets/premium.png)<br>badgeEnterprise-machtigingen in doel-API&#39;s | [Adobe Target Admin API&#39;s](http://developers.adobetarget.com/api/#admin-apis) maken nu ten volle gebruik van dezelfde mogelijkheden voor Enterprise-machtigingen in de doelinterface. Vanaf **21 februari 2019** kunnen systeembeheerders via programmacode toegang krijgen tot rapportgegevens en activiteiten, aanbiedingen en doelgroepen binnen elke werkruimte maken en beheren. Deze acties waren voorheen beperkt tot de standaardwerkruimte. De steun voor de activiteiten van Automated Personalization (AP) zal in een toekomstige versie komen.<br>**Opmerking:**Er is een[bekend probleem](/help/r-release-notes/known-issues-resolved-issues.md#api)met deze functionaliteit. |

**Verbeteringen, correcties en wijzigingen**

* Om de beveiliging te verbeteren, kunt u [!DNL Target] nu de eindpunten van metagegevens van Amazon Web Services (AWS) niet meer gebruiken tijdens het laden van de VEC. (TGT-33129)

### Platformwijzigingen (januari 2019) {#platform-19-1-previous}

| Functie/verbetering | Beschrijving |
| --- | --- |
| <br>gericht op 25 januari 2019 | Wijzigingen aangebracht in de manier waarop &#39;target&#39; overeenkomt met functie voor &#39;equals&#39;-vergelijkingen met niet-decimale en decimale waarden die worden geretourneerd door profielscripts of een andere invoerbron, zoals mbox-parameters, profielparameters, enz.<br>Zie Veelgestelde vragen over [doelen en doelgroepen](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md) voor meer informatie. |
| Profielscripts<br>17 januari 2019 | Om prestatieredenen raden we een geretourneerde waarde aan die niet langer is dan 256 tekens.<br>Als de geretourneerde waarde van een tekenreeks groter is dan 2048 tekens, wordt het script door het systeem uitgeschakeld.<br>Als voor een geretourneerde waarde van een array de grootte van de samengevoegde waarden van de array groter is dan 2048 tekens, wordt het script door het systeem uitgeschakeld.<br>Voor meer informatie over de tekenlimieten en andere limieten (grootte, publiek, profielen, waarden, parameters, enz.) die van invloed zijn op activiteiten en andere elementen in Target, zie [Limieten](../r-troubleshooting-target/target-limits.md). |
| om 16<br>januari 2019 | at.js 1.6.4 is een onderhoudsrelease en behandelt de volgende problemen:<ul><li>Probleem verholpen waarbij zich in Microsoft Internet Explorer 11 een zeldzame omstandigheid manifesteerde die dubbele aanbiedingen veroorzaakte die moesten worden toegepast. (TNT-31374)</li><li>Probleem verholpen dat invloed had op het bijhouden van klikken als er een standaardaanbieding is met een click-token en HTML-aanbiedingen. (TNT-31493)</li><li>Het mboxEdgeCluster-cookie is uitgebreid met elke doelaanvraag. Dit wordt alleen gebruikt wanneer mboxEdgeOverride is ingeschakeld. (TNT-31485)</li></ul> |

### [!DNL Target] Standard/Premium 19.1.1 (22 januari 2019) {#release-19-1-1-previous}

Deze release bevat de volgende functies, wijzigingen en verbeteringen:

(De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.)

| Functie/verbetering | Beschrijving |
| --- | --- |
| ![Ondersteuning voor Target Premium-badge](/help/assets/premium.png)<br/>[!UICONTROL Enterprise Permissions] in API&#39; [!DNL Target] s | [Adobe Target Admin API&#39;s](http://developers.adobetarget.com/api/#admin-apis) maken nu ten volle gebruik van dezelfde mogelijkheden voor Enterprise-machtigingen in de doelinterface. Vanaf **21 februari 2019** kunnen systeembeheerders via programmacode toegang krijgen tot rapportgegevens en activiteiten, aanbiedingen en publiek binnen elke werkruimte maken en beheren. Deze acties waren voorheen beperkt tot de standaardwerkruimte. De steun voor de activiteiten van Automated Personalization (AP) zal in een toekomstige versie komen. |
| ![Doelpremiumbadge](/help/assets/premium.png)<br/>[!UICONTROL Recommendations]: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep) | U kunt nu een voorvertoning weergeven van de inhoud van [!UICONTROL Recommendations] verzamelingen en uitsluitingen voor een geselecteerde omgeving (hostgroep).<br/>Eerder, toen u een inzameling of een uitsluiting bekeken, waren de getoonde punten in resultaten voor de standaardgastheergroep (gespecificeerd in [!UICONTROL Recommendations > Settings > Default Host Group]).<br/>Wanneer u nu een verzameling of uitsluiting maakt of bijwerkt, kunt u de [!UICONTROL Environment] kiezer gebruiken om de omgeving te kiezen waarvoor u een voorvertoning van de resultaten wilt weergeven. Het nieuwe [!UICONTROL Environment] filter bespaart u tijd en moeite omdat u niet meer naar de [!UICONTROL Settings] pagina hoeft te navigeren om de juiste standaardhostgroep te selecteren voordat u verzamelingen en uitsluitingen maakt of bewerkt.<br/>**Opmerking:**Nadat u de geselecteerde omgeving hebt gewijzigd, moet u klikken[!UICONTROL Search]om de geretourneerde resultaten bij te werken.<br/>Het nieuwe[!UICONTROL Environment]filter is beschikbaar bij de volgende plaatsen in[!DNL Target]UI:<ul><li>[!UICONTROL Catalog Search] ([!UICONTROL Recommendations > Catalog Search])</li><li>[!UICONTROL Create Collection] dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])</li><li>[!UICONTROL Update Collection] dialoogvenster ([!UICONTROL Recommendations > Collections > Edit])</li><li>[!UICONTROL Create Exclusion] dialoogvenster ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>[!UICONTROL Update Exclusion] dialoogvenster ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul><br>Raadpleeg de volgende onderwerpen voor meer informatie:<uL><li>[Verzamelingen](/help/c-recommendations/c-products/collections.md)</li><li>[Uitsluitingen](/help/c-recommendations/c-products/exclusions.md)</li><li>[Catalogus zoeken](/help/c-recommendations/c-products/catalog-search.md)</li><li>[Instellingen](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)</li><li>[Aanbevelingen: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep)](/help/administrating-target/hosts.md)</li></ul>(TGT-20622)</ul> |

**Verbeteringen, correcties en wijzigingen**

* Probleem verholpen waarbij de knop Opslaan uitgeschakeld bleef wanneer de gebruiker zich bij het verlopen van de sessie aanmeldt bij het dialoogvenster voor aanmelding tijdens het bewerken van een publiek. (TGT-32722)

## Opmerkingen bij de release - 2018 {#reference_36ACC83E135A41F28104C44755C26D5B}

### Platform (15 november 2018) {#section_484A56774E004282B98FFFF851E4E670}

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>om.js 1.6.3 </p> </td> 
   <td colname="col2"> <p>at.js versie 1.6.3 is nu beschikbaar. </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Kiezers hebben nu een CSS-escape-teken als ze id's of CSS-klassen bevatten die beginnen met een cijfer, twee afbreekstreepjes of een afbreekstreepje gevolgd door een cijfer (bijvoorbeeld #-123). (TNT-31061) </p> </li> 
      <li id="li_6504E90D7C534A1BB9A2DE8510CE3B90"> <p>Probleem verholpen dat werd geïntroduceerd met at.js 1.6.2, waarbij VEC-aanbiedingen (Visual Experience Composer) uit verschillende activiteiten die van toepassing zijn op dezelfde CSS-kiezer de prioriteit van de activiteit niet respecteerde. (TNT-31052) </p> </li> 
      <li id="li_D347CA513F1240E4BF79D757287AB30C"> <p>Probleem verholpen waarbij een belofte werd nagekomen in omgevingen waar geen native ondersteuning voor beloften bestond. (TNT-30974) </p> </li> 
      <li id="li_17F41A84CCFF41D7993E35DE10F87066"> <p>Problemen worden nu correct vastgelegd en gerapporteerd via de gebeurtenis content-rendering mislukt. Eerder werd mogelijk gemeld dat JavaScript goed was uitgevoerd, zelfs als dat niet het geval was. (TNT-30599) </p> </li> 
     </ul> </p> <p>Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details</a>van de Versie. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.11.1 (12 november 2018) {#section_6BBA8B1EE9D241C28E12856A375E97F6}

De [!DNL Target] Standard/Premium-release van 12 november bevat back-endverbeteringen, correcties en wijzigingen. De [!UICONTROL Personalization Insights] verslagen zijn beschikbaar op 14 november.

<table id="table_EF529199D1C741F7BDBC9C41A37B7D26"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Persoonlijkheidsrapporten </p> <p> <p>Opmerking:  Beschikbaar op 14 november 2018. </p> </p> </td> 
   <td colname="col2"> <p>Er zijn twee gespecialiseerde rapporten beschikbaar voor gebruikers van de activiteiten <span class="wintitle"> Automated Personalization (AP)</span> en <span class="wintitle"> Auto-Target (AT)</span> : </p> <p> 
     <ul id="ul_C338AC34C57C49E1A8DFA471167EC40A"> 
      <li id="li_2329BFC8CC524EBBA99C2F8EDC745B90"> <p><b><span class="wintitle"> Geautomatiseerde segmenten</span>:</b> Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd. </p> </li> 
      <li id="li_48556C9BAD48476DA00DD666F5265E2B"> <p><b><span class="wintitle"> Belangrijke kenmerken</span>:</b> In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden. </p> </li> 
     </ul> </p> <p>Zie de rapporten over <a href="../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"></a>persoonlijke informatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.10.1 (24 oktober 2018) {#section_FA37BF4E840B424E8BC4791D7234FE2A}

Deze release bevat de volgende functies en verbeteringen:

(De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.)

<table id="table_B1911F55CCE1428881D258380A8254A9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ervaringen </p> </td> 
   <td colname="col2"> <p>U kunt nu een ervaring kopiëren in een Experience Targeting-activiteit (XT), zodat u er kleine wijzigingen in kunt aanbrengen zonder dat u de ervaring helemaal opnieuw hoeft te maken. Deze mogelijkheid was al beschikbaar voor A/B-tests. (TGT-31504) </p> <p>Zie Ervaring <a href="https://docs.adobe.com/content/help/en/target/using/activities/experience-targeting/create-targeting/xt-add-experience.html" format="html" scope="external"> maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbiedingen in activiteiten van Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p>In de release van september 2018 hebben we een verbetering toegevoegd waarmee u aanbiedingen kunt filteren op rapportagegroepen. U kunt nu filteren op Niet toegewezen aanbiedingen zodat u een rapportgroep kunt toewijzen aan een aanbieding die momenteel niet aan een rapportgroep is toegewezen. (TGT-31882) </p> <p>Zie <a href="https://docs.adobe.com/content/help/en/target/using/activities/automated-personalization/create-ap-activity.html" format="html" scope="external"> Een geautomatiseerde personalisatieactiviteit maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage bron voor activiteiten </p> </td> 
   <td colname="col2"> <p>In <span class="wintitle"> Opstelling </span> &gt; <span class="wintitle"> Voorkeur </span>, kunt u de rapporteringsbron voor uw activiteiten selecteren, of <span class="keyword"> Doel </span> of <span class="keyword"> de Analyse van Adobe </span>. U kunt ook de rapportbron per activiteit selecteren. </p> <p>Vanaf deze release zijn er enkele belangrijke workflowoverwegingen waarmee u rekening moet houden wanneer u de rapportbron kiest in <span class="wintitle"> Voorkeuren </span> of per activiteit. </p> <p>Zie <a href="https://docs.adobe.com/content/help/en/target/using/administer/preferences/target-account-preferences.html" format="html" scope="external"> Voorkeuren </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* Verbeterde verwerking van publiek waarnaar wordt verwezen in Doelactiviteiten die zijn verwijderd in Adobe Audience Manager (AAM). (TGT-2338)

   * Als een publiek in AAM werd geschrapt, toont een waarschuwingspictogram in zowel de [!UICONTROL Audience] lijst als de publieksplukker. Een hulpmiddel-uiteinde in UI wijst ook erop dat het publiek in AAM werd geschrapt.
   * Als u meerdere soorten publiek probeert te combineren met een verwijderd publiek of als u een activiteit probeert op te slaan die verwijst naar een verwijderd publiek, wordt een waarschuwingsbericht weergegeven.
   Zie [Informatie over publiek](https://docs.adobe.com/content/help/en/target/using/audiences/create-audiences/audiences.html).

* Probleem verholpen waardoor gebruikers in bepaalde situaties geen activiteit konden maken toen Adobe Analytics als de bron voor rapportage op de [!UICONTROL Setup] pagina werd geselecteerd. Gebruikers zagen een bericht &quot;Selecteer een rapportsuite&quot;, ook al kregen ze niet de mogelijkheid om de rapportsuite te selecteren. (TGT-31968)

### Platform (19 oktober 2018)

<table id="table_7320E43397D2471FA313A9D6FC21E55F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>om.js 1.6.2 </p> </td> 
   <td colname="col2"> <p>Dit is een onderhoudsrelease en het volgende probleem wordt opgelost: </p> <p> 
     <ul id="ul_2C7CB74B1AAF4B52B6EB382977F7DC28"> 
      <li id="li_07CF8EDB25E24A7AB9B7A0F3402BAEB1"> <p>Probleem verholpen waarbij sites van bepaalde klanten tot een oneindige 'async'-lus leiden. </p> </li> 
     </ul> </p> <p> <p>Belangrijk:  Daarnaast bevat at.js versie 1.6.2 ook alle verbeteringen en correcties die zijn opgenomen in at.js versie 1.6.1 en 1.6.0. Deze versies kunnen niet meer worden gedownload. We raden u aan een upgrade naar versie 1.6.2 uit te voeren als u 1.6.1 of 1.6.0 gebruikt. </p> </p> <p>Voor meer informatie, zie <a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/target-atjs-versions.html" format="html" scope="external"> bij.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.9.1 (26 september 2018) {#section_95CF405C95E44DBEA3CB308FDD5071CD}

<!-- 

target/r_release-notes-2018.xml

 -->

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_7ABC8E7477194D4C8C9E82ECE60E3498"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbiedingen in activiteiten van Automated Personalization (AP) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_9C39ACD865CE4167BDBAA093EDFD3B68"> 
      <li id="li_19710BA5965E4F858B128E1E9FF89471"> <p>U kunt nu meerdere voorstellen van dezelfde locatie in een uitsluitingsgroep gebruiken. Voor een groot aantal uitsluitingen (volgorde van 1.000) ziet u ook hoe sneller het laden van het dialoogvenster Inhoud beheren en de voorvertoningspagina wordt uitgevoerd wanneer u een activiteit Automated Personalization (AP) ontwerpt. (TGT-31329) Zie <a href="../c-activities/t-automated-personalization/managing-exclusions.md#topic_30B4E4F89C914EB2B20B038C0299ED2E" format="dita" scope="local"> Uitsluitingen beheren </a>. </p> </li> 
      <li id="li_542C66E2998541BC87D0A96F4672C665"> <p>U kunt voorstellen nu filteren door groepen te melden. (TGT-31643) Zie <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> het Creëren van een Geautomatiseerde Personalisatieactiviteit </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>We hebben een <span class="wintitle"> Invoegen voor </span> de actie (VEC) toegevoegd. Dit is vergelijkbaar met de vorige <span class="wintitle"> </span> optie Invoegen na. Wanneer u een element op de pagina selecteert, kunt u op <span class="wintitle"> Invoegen voor klikken </span> en kiezen of u een afbeelding, HTML of tekst wilt invoegen. Het ingevoegde element wordt vóór het geselecteerde element weergegeven. (TGT-30473) Zie Opties voor <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> Visual Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* We hebben de look and feel van de Criteria cards bijgewerkt om intuïtiever en gebruiksvriendelijker te zijn. (TGT-30469)
* Prestatieverbeteringen in de gebruikersinterface voor sneller laden van pagina&#39;s.

### Target Standard/Premium 18.8.1 (21 augustus 2018) {#section_66A0030993D54565BE30E56AC9CAC1DA}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_4785030753B24AA1A973E1DF790B83DD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Persoonlijkheidsrapporten </p> </td> 
   <td colname="col2"> <p>Heb toegang tot gespecialiseerde rapporten voor uw Geautomatiseerde Persoonlijke (AP) en auto-Doel (AT) activiteiten: </p> <p> 
     <ul id="ul_54652C5AE0984657BB9A0E46673CB2F1"> 
      <li id="li_0807959BA7D94114BE47A43D3454CAB4"> <p><b>Geautomatiseerde segmenten:</b> Zie hoe de verschillende geautomatiseerde segmenten die door de verpersoonlijkingsmodellen van Target worden bepaald op aanbiedingen/ervaringen in uw activiteit antwoorden. </p> </li> 
      <li id="li_48210B1E4EB24288B96CDECAF1CEE34A"> <p><b>Waardering modelkenmerk:</b> Zie de hoogste attributen die de personalisatiemodellen van het Doel en het relatieve belang van elk attribuut beïnvloedden. </p> </li> 
     </ul> </p> <p> <p>Opmerking:  Deze functie is binnenkort beschikbaar. Blijf op de hoogte voor een aankondiging van de exacte datum waarop deze functie klaar is voor gebruik. </p> </p> <p>Zie de <a href="../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767" format="dita" scope="local"> rapporten met informatie over personalisatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_406B95728467496CA6CC5892F88B69FE"> 
      <li id="li_6D717868FB204A3A95832E709773B424"> <p>U kunt het deelvenster Wijzigingen verticaal aan de zijkant van de doelinterface koppelen of horizontaal aan de onderkant. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Wijzigingen </a>. </p> </li> 
      <li id="li_27750AFBCB3E4CB8B0B53592B2447E59"> <p>We hebben verschillende VEC-acties gegroepeerd om uw werk sneller en efficiënter te maken. (TGT-30472) </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </li> 
      <li id="li_27FEBEE245E64ADF9ADF561C6CBBDE8F"> <p>U kunt aanbiedingen efficiënter bewerken dankzij een groter bewerkingsvenster. (TGT-31052) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tips en trucs </p> </td> 
   <td colname="col2"> <p>Haal het meeste uit Adobe Target door meer te leren over verschillende functies en te zien waarom u ze een poging moet doen. De functies Tips en trucs worden weergegeven op de pagina Activiteiten en bevatten koppelingen naar video's, gebruiksscenario's, blogs, documentatie en nog veel meer. Word een doelenergiegebruiker! </p> <p>Zie <a href="../c-activities/activities.md#section_F77F30A246A14B538D9363B7F3639F97" format="dita" scope="local"> Tips en trucs </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doelbasis van de webinarreeks </p> </td> 
   <td colname="col2"> <p>Neem deel aan de nieuwe Webinar Reeks van de Grondbeginselen van het Doel, een Reeksen van het Succes van de Klant Webinar die aan u door de Gemeenschap wordt gebracht. </p> <p> De volgende webinar, Best Practices in Reporting &amp; Value Socialization, is gepland voor 22 augustus 2018 van 8 tot 9.00 uur. (PDT). </p> <p>Zie <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Webinar reeks van de Grondbeginselen van het Doel </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* We hebben verschillende verbeteringen toegevoegd om Target nog veiliger te maken dan voorheen. (TGT-31090, TGT-31089, TGT-31143)

### Target Standard/Premium 18.7.1 (25 juli 2018) {#section_A4A9C20EB677455F84FF0BA389F645E5}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_7E3513EABA4948DC92EADCCE0234A9FF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activiteiten in het kader van A/B en Experience Targeting (XT) </p> </td> 
   <td colname="col2"> <p>Bewerk en verwijder ervaringen rechtstreeks uit het activiteitendiagram. Nu kunt u in de Visuele Composer van de Ervaring (VEC) voor een specifieke ervaring springen of een ervaringsrecht van het diagram schrappen. </p> <p> <img src="assets/experience_edit.png" id="image_FA6E5F07B04A4B4BA02EA71EDB6908A7" /> </p> <p>Zie: </p> <p> 
     <ul id="ul_CB0C1146716F4C09BF924CF3DFA7DC1A"> 
      <li id="li_3767DD36F597481FB312CC577CD668F0"> <p>A/B-activiteit: <a href="../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Ervaring toevoegen </a> </p> </li> 
      <li id="li_E2990CA178C6446BA7206643A3164FEF"> <p>XT-activiteit: <a href="../c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> Ervaring maken </a> </p> </li> 
     </ul> </p> <p>(TGT-30229) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Vergelijk een profielkenmerk met een ander profielkenmerk in plaats van met een statisch getal. </p> <p>Zie <a href="../c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md#concept_4C2124B79A5B4556A6C1D10C0F5E40A0" format="dita" scope="local"> Een vergelijkingspubliek voor profielkenmerken maken </a>. </p> <p> (TGT-28406) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste code </p> </td> 
   <td colname="col2"> <p>'Aangepaste code' is nu beschikbaar in het deelvenster 'Wijzigingen toevoegen' in plaats van een eigen tabblad. U kunt ook meer dan één aangepaste code toevoegen en elke aangepaste code optioneel een naam geven. (TGT-28504) </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Wijzigingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_371C18DFC6D24E94B3D4FFFD83FC8D3A"> 
      <li id="li_9D11939014E7479AB7FD8910852A5386"> <p>Een lijst met activiteiten weergeven die verwijzen naar een geselecteerde criteria op de bijbehorende Criteria-kaart. De kaart vermeldt actieve en inactieve activiteiten. (TGT-27672) </p> </li> 
      <li id="li_B97BF9305EB04F6D8B1F6178B2E0CB34"> <p>In het activiteitendiagram worden nu Criteria-kaarten weergegeven wanneer de resultaten gereed zijn om te worden weergegeven. (TGT-27673) </p> <p>Zie <a href="../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Templates </p> </td> 
   <td colname="col2"> <p>De Malplaatjes van de Ervaring van het Doel van Adobe zijn vooraf gecodeerde aanbiedingen met configureerbare input die in Doel moet worden gebruikt om sommige gemeenschappelijke gevallen van het marktorgebruik uit te voeren. Deze ervaringssjablonen zijn gratis beschikbaar voor ontwikkelaars en marketers als startpunt voor het uitvoeren van enkele gangbare gevallen voor extern gebruik in Adobe Target - via Visual Experience Composer of Form-Based Experience Composer. Mogelijk moet u de configuratie aanpassen om de integratie met uw webpagina- of platformarchitectuur te voltooien. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/experience-templates.md#concept_109BBD7EABC04DD39E6B7B1687786652" format="dita" scope="local"> Experience Templates </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doelbasis van de webinarreeks </p> </td> 
   <td colname="col2"> <p>Neem deel aan de nieuwe Webinar-reeks van de Grondbeginselen van het <a href="../cmp-resources-and-contact-information.md#concept_11902FAC95C64479AABE020557A7EEE4" format="dita" scope="local"> Doel </a>, een reeks van het Succes van de Klant Webinar die aan u door de Gemeenschap wordt gebracht. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* De modale grootte van de Rich Text Editor is groter geworden voor betere bruikbaarheid. (TGT-24775)
* De diagrammen in de stap Doel (stap 2 van de driestappenworkflow met instructies) voor de activiteiten Automated Personalization (AP) en Multivariate Test (MVT) zijn opnieuw ontworpen om consistenter te zijn met de ontwerpen die worden gebruikt voor de activiteiten A/B, Experience Targeting (XT) en Recommendations. (TGT-30712)
* De metrische waarde voor het MVT-rapport (Multivariate Test Location Contribution) is nu consistenter met de waarden voor andere metriek, die tot twee decimalen wordt afgerond. (TGT-30921)

### at.js versie 1.5.0 (22 juni 2018) {#section_53C622F4978F4BC9ACD932D4B7194C12}

<table id="table_B332A93D4A6E4568BA3F7FA8EC0787F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js versie 1.5.0 is nu beschikbaar. </p> <p> <p>Opmerking:  De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe. </p> </p> <p> 
     <ul id="ul_41FE0EED2D8B4ADE84FC4CA0FA0CE8A0"> 
      <li id="li_2DC17381CB7949AFA35B054B9CA723FA"> <p>De details van de <span class="codeph"> op verzoek-geleide </span> gebeurtenis bevatten de omleidingsvlag. Met deze markering kunt u bepalen of de pagina wordt omgeleid naar een andere URL. Als u de URL wilt weten, meldt u zich aan <span class="codeph"> at-content-rendering-redirect </span>. (TNT-29834) </p> </li> 
      <li id="li_2852878862724BB2BD475C8FC7BF20DA"> <p>Probleem verholpen waarbij <span class="codeph"> </span> window.targetGlobalSettings.enabled mislukte met een runtime-uitzondering als deze op false was ingesteld. (TNT-29829) </p> </li> 
      <li id="li_96E5E409B36444F1B0E3E2606DC03996"> <p>Probleem verholpen die ertoe leidde dat de pagina mislukte tijdens het laden in Visual Experience Composer (VEC) als het gebruiken van douanecode aan een brand globale mbox verzoek en het gebruiken van lichaam het verbergen. (TNT-29795) </p> </li> 
      <li id="li_818AA4EDDAC04D8B9BB4BA708D6BEF99"> <p>Toegevoegde ondersteuning voor <span class="codeph"> screenOrientation </span>, <span class="codeph"> devicePixelRatio </span>, en <span class="codeph"> webGLRenderer </span>. Deze nieuwe parameters voor doelverzoeken worden gebruikt voor iPhone X en andere moderne apparaatdetectie. Zie <a href="../c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobiel voor meer informatie </a>. (TNT-29781) </p> </li> 
      <li id="li_87E3FB8B423C472AB1EE0DF2D7C64885"> <p>Probleem verholpen waarbij de locatie-hint van Adobe Audience Manager (AAM) niet altijd werd verzonden. (TNT-29695) </p> </li> 
      <li id="li_E9E5A5035AC24F54ADEF5447E3F15D3B"> <p>Voor browsers die dit ondersteunen, schakelt at.js 1.5.0 over naar MutationObserver voor kiezersopiniepeiling. In versies vóór at.js 1.0.0 werd een MutationObserver-polyfill gebruikt, wat problematisch bleek te zijn. Om de polyfill problemen te voorkomen, gebruikt versie 1.5.0 de volgende pseudo-code om te bepalen welk planningsmechanisme moet worden gebruikt: </p> <p> 
        <code>
          if MutationObserver is supported scheduler = MutationObserver else if document is visible scheduler = requestAnimationFrame else scheduler = setTimeout 
        </code> </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.6.1 (20 juni 2018) {#section_B63C660815B245DA9922BE33E03734A1}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_5A60FFE5E86148F4BDC6A7031D03D6BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie/verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>Wanneer u een actie in het paneel van Aanpassingen klikt, scrolt VEC automatisch de Web-pagina en het overeenkomstige element wordt benadrukt. U hoeft niet meer handmatig omlaag te schuiven om het HTML-element te zoeken dat door de wijziging is beïnvloed. </p> <p> <img src="assets/modifications_panel.png" id="image_6E01280636E34ADDA9527AD18A34310B" /> </p> <p>(TGT-30441) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ondersteunde browsers </p> </td> 
   <td colname="col2"> <p>Toegevoegde Microsoft Edge-ondersteuning voor de doelgebruikersinterface en voor het leveren van inhoud. </p> <p>Zie voor meer informatie. <a href="../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Ondersteunde browsers </a> (TGT-14102) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen </p> </td> 
   <td colname="col2"> <p>De criteria voor onlangs bekeken items geven nu resultaten die specifiek zijn voor een bepaalde <a href="../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> omgeving </a>. Als twee sites tot verschillende omgevingen behoren en een bezoeker tussen de twee sites schakelt, worden op elke site alleen recent bekeken items van de desbetreffende site weergegeven. Als twee sites zich in dezelfde omgeving bevinden en een bezoeker schakelt tussen de twee sites, ziet de bezoeker dezelfde onlangs weergegeven items voor beide sites. </p> <p>Voor meer informatie, zie <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B" format="dita" scope="local"> Baseer de Aanbeveling op een Sleutel van de Aanbeveling </a>. (RECS-5865) </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* De back-uprij van de CSV-download met aanbevelingen heeft nu een &quot;*&quot; (dubbele aanhalingstekens die een sterretje omsluiten) in plaats van * (één sterretje).
* De bovenste rij Verkocht / Bovenste bekeken rij in de CSV-download met aanbevelingen heeft niet langer een komma aan het begin.

### Wijzigingen in doelplatform (19 juni 2018) {#section_0638BD69F3C640479A2A258AD78C0884}

Deze release bevat de volgende verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

* Bijgewerkt de apparatenlijst om de recentste telefoonmodellen te omvatten. De mogelijkheid om gerichte inhoud te leveren aan specifieke iPhone-modellen is toegevoegd met de marketingnaam of het apparaatmodel van het apparaat.

   Klanten die de SDK voor mobiele apparaten gebruiken, hoeven niets te doen om deze functionaliteit te benutten. Klanten die at.js gebruiken, moeten een upgrade uitvoeren naar at.js versie 1.5.0.

   Zie [Mobiel](../c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89)voor meer informatie. (TNT-26714 &amp; TNT-28288)

### Doel-API voor downloaden (5 juni 2018) {#section_B8729DA10F18433C8D8E01B04F308ED2}

U kunt de aanbevelingen downloaden API om uw aanbevelingen in een .CSV dossier te downloaden dat in een spreadsheet of een tekstredacteur kan worden bekeken. Voor betere beveiliging, vanaf 5 **juni 2018**, blokkeert Target HTTP-aanvragen en staan alleen HTTPS-aanvragen toe.

### Target Standard/Premium 18.5.1 (22 mei 2018) {#section_7C1427793C2A48DBAC39F8290717DC5B}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_1C51F61184684072BC69AD15BA68BEBB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_8D08FE4AC7D748EFB2BBFF87DBDC5CE5"> 
      <li id="li_B8929C19276D42168A28A3775CDEDFB3"> <p>U kunt maximaal tien verschillende voorinstellingen van een activiteitenrapport opslaan nadat u het rapport naar wens hebt geconfigureerd (metriek, publiek, geavanceerde instellingen, enzovoort). Alle gebruikers van het Doel kunnen, de diverse vooraf instelt tonen uitgeven en schrappen, ongeacht wie hen creeerde. (TGT-21268) </p> </li> 
      <li id="li_7ADA62F2ACA049C9B4A8986B09A9F4AA"> <p>U kunt het rapport van een individuele activiteit vormen zoals gewenst en dan die configuratie opslaan als uw gebrek/favoriete voorinstelling. Dit is de mening die toont wanneer u het rapport van die activiteit vooruitgaat. (TGT-10082) </p> </li> 
      <li id="li_DC63C04F3A884BDDA55B5515E4643B7B"> <p>Het alarm en de berichten binnen rapporten laten u weten of één (of meerdere) publiek, metrisch, gastheergroep, of ervaring van een eerder gevormd vooraf ingesteld rapport is geschrapt. Met de waarschuwing of het bericht kunt u een ander publiek, een ander metrisch publiek, een andere hostgroep of een andere ervaring kiezen om opnieuw een voorinstelling te maken. (TGT-29424) </p> </li> 
     </ul> </p> <p>Zie de sectie Voorinstelling doel in <a href="../c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Rapportinstellingen voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Profielscripts </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F382C8E7708846A08676E1534BC92878"> 
      <li id="li_70E89504525C4119B588C230DCE772E8"> <p>U kunt pop-upkaarten met profielscriptinformatie weergeven, vergelijkbaar met informatiekaarten. Met deze informatiekaarten voor profielscripts kunt u een lijst weergeven met activiteiten die verwijzen naar het geselecteerde profielscript, samen met andere nuttige metagegevens. (TGT-28253) </p> <p>Zie de sectie View Profile Script Information Cards in <a href="../c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profile Script Attributes voor meer informatie </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_DFEB778393024E3EBBC482F31A5B39BC"> 
      <li id="li_4049E334A38F4F94842FF1E35F177FE9"> <p>De verwezenlijking van de Audience van de douane staat nu het gebruiken van de mbox parameter direct toe zonder het moeten verplicht de mbox naam specificeren. De naam van het selectievakje is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen. U kunt ook op de parameter mbox filteren met het naamfilter van de box. </p> <p>Deze zelfde verbetering is ook uitgebreid tot de Criteria van Aanbevelingen, de Bevorderingen van Aanbevelingen, en de Testende regels van het Malplaatje. </p> </li> 
     </ul> </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/custom-parameters.md#concept_C4C6E00D7C5A4BE9B72D471DB2E3027B" format="dita" scope="local"> Aangepaste parameters voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7765B69E679D4C94B1E863E340DFDE15"> 
      <li id="li_F2AF7E1AFBD6461990EF1D83D1989582"> <p>Bij het selecteren van criteria voor Aanbevelingen in de Form-Based Experience Composer is er nu een directe koppeling naar de geselecteerde Criteria Card zodat u de criteria snel en eenvoudig kunt bewerken. (TGT-28483) </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer voor meer informatie </a>. </p> </li> 
      <li id="li_517F0A174587416B8621D6F710C1AC48"> <p>De Criteria van de aanbevelingen, de Bevorderingen van Aanbevelingen, en de het testende regels van het Malplaatje maken nu het gebruiken van de mbox parameter direct zonder het moeten verplicht de mbox naam specificeren. De naam van het selectievakje is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen. U kunt ook op de parameter mbox filteren met het naamfilter van de box. </p> <p>Deze verbetering is ook uitgebreid tot het creëren van de Audience van de Douane. </p> <p>Zie Veelgestelde vragen over <a href="../c-recommendations/c-recommendations-faq/recommendations-faq.md#concept_EF272DE4AC6C47B19026BFBE816F5DB8" format="dita" scope="local"> aanbevelingen voor meer informatie </a>. </p> </li> 
      <li id="li_AAB242830D1E47B78E58A980B717C736"> <p>Bijgewerkt UI voor de kaarten van het Ontwerp van Aanbevelingen. </p> </li> 
      <li id="li_1BE3178663E54F4CA8714FE3ACDBB97B"> <p>De documentatie over de API voor doelaanbevelingen vindt u op de website <a href="https://www.adobe.io/apis/experiencecloud/target/docs/getting-started.html" format="html" scope="external"> Adobe I/0 Adobe Target </a> (https://www.adobe.io/apis/experiencecloud/target/docs/getting-started.html). </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* Bijgewerkt UI voor Stap 2 van het Doel driestappe die werkschema wordt gebruikt om een Test A/B, de Gerichte ervaring (XT), of de activiteit van Aanbevelingen tot stand te brengen of uit te geven. (TGT-18911)

### Target Standard/Premium 18.4.1 (25 april 2018) {#section_445DBC5402BA456BAF2D24AEA33A91C9}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_6D99C48B72D24728BF623608053931D3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Experience Manager (AEM) - Fragmenten </p> </td> 
   <td colname="col2"> <p>Door ervaringsfragmenten te gebruiken die in AEM zijn gemaakt voor doelactiviteiten, kunt u het gebruiksgemak en de kracht van AEM combineren met de krachtige mogelijkheden van Automated Intelligence (AI) en Machine Learning (ML) in Target om ervaringen op schaal te testen en te personaliseren.&amp;nbsp;&amp;nbsp; </p> <p>AEM brengt al uw inhoud en middelen op een centrale locatie samen om uw personalisatiestrategie te voeden. Met AEM kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder dat u code hoeft te schrijven. Het is niet nodig om pagina's te maken voor elk apparaat. AEM past automatisch elke ervaring aan met uw inhoud. </p> <p> Met Doel kunt u gepersonaliseerde ervaringen op schaal bieden op basis van een combinatie van op regels gebaseerde en op AI gebaseerde methoden voor het leren van machines die gedrags-, context- en offlinevariabelen bevatten.&amp;nbsp; Met Doel kunt u eenvoudig A/B- en Multivariate-activiteiten instellen en uitvoeren om de beste aanbiedingen, inhoud en ervaringen te bepalen. </p> <p>De fragmenten van de ervaring vertegenwoordigen een enorme stap voorwaarts om de tevreden/ervaringsscheppers en managers aan de optimalisering en verpersoonlijkingsberoeps te verbinden die bedrijfsresultaten gebruikend Doel drijven. </p> <p>Voor meer informatie, zie de Fragmenten van de Ervaring <a href="../c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8" format="dita" scope="local"> AEM </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> 
    <ul id="ul_EAB90C510EA04D6A8AEFF23A77DB2337"> 
     <li id="li_47DA6EB92CC84FFDBFDC9CC9386AF654"> <p>U kunt een rapport nu verfrissen om de lijst en grafiekmening van het rapport bij te werken zonder de volledige pagina, zijn configuratie, of zijn datumwaaier te verfrissen. (TGT-28125) </p> <p>Zie <a href="../c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Rapportinstellingen voor meer informatie </a>. </p> </li> 
     <li id="li_AB2DE7A45D914FD7AEB0832187AF3844"> <p>De kalender in rapporten bevat nu vooraf gedefinieerde datumbereiken, zoals Laatste 7 dagen, Laatste 15 dagen enzovoort. (TGT-29171) </p> <p>Zie <a href="../c-reports/c-report-settings/report-settings.md#concept_3A80D5A394EC4B639DC715E06085BDB0" format="dita" scope="local"> Rapportinstellingen voor meer informatie </a>. </p> </li> 
     <li id="li_46DF9037E0ED4935B3BCDB35E8BED065"> <p>De kolombreedte van de tabelweergave is gewijzigd om horizontaal schuiven te beperken wanneer meerdere maateenheden worden toegepast. (TGT-26575) </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>UI-lokalisatie </p> </td> 
   <td colname="col2"> <p>De doelinterface is nu beschikbaar in de volgende talen: </p> <p> 
     <ul id="ul_DB6C771FCFDF43F498F8754920A70BCD"> 
      <li id="li_A65D07DF66844AC8BEEC1D413F214191"> <p>Vereenvoudigd Chinees </p> </li> 
      <li id="li_5986DD06AF5B4F76B3A02CFBF2DC3644"> <p>Traditioneel Chinees </p> </li> 
      <li id="li_341FDC1CEC2B4C4BBD45CB2A0A54F2A3"> <p>Koreaans </p> </li> 
      <li id="li_A4C31539B98E42348D5F1A18C63EAB6C"> <p>Italiaans </p> </li> 
      <li id="li_97E3E0A916B64601BBF601AAED581174"> <p>Portugees </p> </li> 
     </ul> </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Wanneer het creëren van een douanepubliek dat op een mbox parameter wordt gebaseerd, <span class="codeph"> mboxParameter </span> veroorzaakt u niet meer voor <span class="codeph"> mboxName </span>. mbox name is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen. (TGT-25807) </p> <p> <p>Opmerking:  Deze functie is zichtbaar in de doelinterface, maar is momenteel uitgeschakeld. Deze functie wordt binnenkort ingeschakeld (datum waarop moet worden gecommuniceerd). </p> </p> 
  </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* De Veiligheid van de Laag van het vervoer (TLS) is het wijdst opgestelde veiligheidsprotocol dat vandaag voor Webbrowsers en andere toepassingen wordt gebruikt die gegevens vereisen om veilig over een netwerk worden geruild. Adobe heeft normen voor beveiligingscompatibiliteit die het einde van de levensduur van oudere protocollen vereisen en die het gebruik van TLS 1.2 verplicht stellen om de meest actuele en veilige versie in gebruik te hebben. Vanaf de doelversie 18.4.1 (25 april 2018) zal Adobe Target stappen ondernemen om de codering van TLS 1.2 te bevorderen en de ondersteuning voor TLS 1.0-codering volledig te beëindigen tegen 12 september 2018. Het is belangrijk dat u de details doorloopt en de wijzigingen uitwerkt voor een vloeiende overgang. Voor meer informatie, zie de Veranderingen [van de Encryptie van](../c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)TLS (de Veiligheid van de Laag van het Vervoer).
* De gebruikersinterface voor Cards met aanbevolen criteria is verbeterd en is nu gebruiksvriendelijker. (TGT-27829)

### om.js (3 april 2018) {#section_932DF1004F4648668FE4984BFAF2EC49}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_76576D9D931B4DA99900F2C03175938E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js versie 1.3.0 is nu beschikbaar. Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Download bij.js </a> en <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> <p> 
     <ul id="ul_349BEB37B6C94FF0801F121042037803"> 
      <li id="li_4C2F82F4DD394ED5A0BFF978B15FEDDF"> <p>De volgende nieuwe gebeurtenissen zijn beschikbaar om u te helpen bij het traceren, opsporen van fouten en het aanpassen van interactie met at.js: </p> <p> 
        <ul id="ul_EFF7E2FCEA0D42298779DDE13B54503F"> 
         <li id="li_6A2B06A522004EDE96D9A552571A7C30"> <p>LIBRARY_LOADED </p> </li> 
         <li id="li_61AA203A21DF4B7EAE075374A09C8FF0"> <p>REQUEST_START </p> </li> 
         <li id="li_DAF9CC1E86834C62B93419429B43A2CB"> <p>CONTENT_RENDERING_START </p> </li> 
         <li id="li_A52DC337115248A1BE5AF5B358BE5A9A"> <p>CONTENT_RENDERING_NO_OFFERS </p> </li> 
         <li id="li_7D71E48016B1446995493EBBF7D32447"> <p>CONTENT_RENDERING_REDIRECT </p> </li> 
        </ul> </p> <p>Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#reference_A828E4BA535F4E7692A075F3D70CF6CD" format="dita" scope="local"> aangepaste gebeurtenissen at.js voor meer informatie </a>. </p> </li> 
      <li id="li_E2704294F8BA47FFAABE7572F67FB5C0"> <p>U kunt een verzoek at.js met extra parameters uitbreiden die uit gegevensleveranciers komen. Gegevensleveranciers moeten worden toegevoegd aan <span class="codeph"> window.targetGlobalSettings </span> onder de <span class="codeph"> gegevensaanbieder </span>. </p> <p>Zie voor meer informatie "Data Providers" in <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> targetGlobalSettings() </a>. </p> </li> 
      <li id="li_02EAFE6DA0D44CF88980184FD14226A5"> <p>Bij.js-aanvragen wordt nu GET gebruikt, maar er wordt overgeschakeld naar POST wanneer de URL groter is dan 2048 tekens. Er is een nieuwe eigenschap met de naam <span class="codeph"> urlSizeLimit </span> waarmee u de maximale grootte indien nodig kunt verhogen. Dankzij deze wijziging kan Target worden uitgelijnd op .js naar AppMeasurement, die dezelfde techniek gebruikt. </p> </li> 
      <li id="li_43363A4F3A764394AA88D2595F93D8C0"> <p>Doel dwingt nu af of de <span class="codeph"> mbox- </span> toets in de <span class="codeph"> functie adobe.target.applyOffer(options) </span> wordt gebruikt. Deze sleutel is in het verleden vereist, maar Doel dwingt nu zijn gebruik af om ervoor te zorgen dat Doel juiste bevestiging heeft en klanten correct de functie gebruiken. </p> <p>Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#reference_BBE83F513B5B4E03BBC3F50D90864245" format="dita" scope="local"> adobe.target.applyOffer(options) voor meer informatie </a> . </p> </li> 
      <li id="li_7336D8D48A894291A378E0BB212B7F9B"> <p>at.js heeft de functie voor het bijhouden van gebeurtenissen verbeterd en klikt op tracking. at.js gebruikt <span class="codeph"> navigator.sendBeacon() </span> om gegevens voor het bijhouden van gebeurtenissen te verzenden en fallback naar synchrone XHR wanneer <span class="codeph"> navigator.sendBeacon() </span> niet wordt ondersteund. Deze fallback heeft vooral invloed op Internet Explorer 10 en 11 en op sommige versies van Safari. Safari voegt ondersteuning voor <span class="codeph"> navigator.sendBeacon() toe </span> in de iOS 11.3-release. </p> </li> 
      <li id="li_28D7324137B14C75BF6F1EA0B2487C9B"> <p>Met at.js kunt u nu aanbiedingen renderen, zelfs als een pagina wordt geopend op tabbladen op de achtergrond. Sommige klanten van het Doel ondervonden een probleem toen requestAnimationFrame() <span class="codeph"> </span> was uitgeschakeld vanwege het browsergedrag voor achtergrondtabbladen. </p> </li> 
      <li id="li_3278979E1C6C41DEA7E8025AEB337985"> <p>Deze versie voegt vele prestatiesverbeteringen, met inbegrip van kortere callstacks toe wanneer het inspecteren van een profiel van Chrome cpu. </p> </li> 
      <li id="li_AAA9C0DCC3354DFA8907968C8E6427F6"> <p>at.js 1.3.0 biedt geen ondersteuning meer voor de levering van inhoud in Microsoft Internet Explorer 9. Zie <a href="../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Ondersteunde browsers voor een lijst met ondersteunde browsers </a>. Voorwaarts worden alle aanvragen uitgevoerd via <span class="codeph"> XMLHttpRequest </span> met CORS-ondersteuning zonder JSONP-aanvragen. Deze wijziging verbetert de veiligheid aanzienlijk. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.3.1 (20 maart 2018) {#section_880706BE15544A03A2C951F267F4AEC5}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_AE38682151A948AEA21E35A353F18D76"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Populariteit op kenmerk Entiteit </p> </td> 
   <td colname="col2"> <p><b>Nieuw: 22 maart 2018</b> </p> <p>U kunt nu het kenmerk Populariteit op entiteit in de bestaande stroom kiezen wanneer een kenmerk Aangepast als de sleutel wordt geselecteerd. </p> <p>Na het selecteren van de gewenste sleutel (in dit geval, een attribuut van het douaneprofiel), voor "de Logica van de Aanbeveling,"kunt u twee nieuwe opties kiezen: </p> <p> 
     <ul id="ul_7A6F2398ADE846EF8A7A3110C2736BF7"> 
      <li id="li_66BFF016564749B298B88F6B9638B64E"> <p>Meest bekeken </p> </li> 
      <li id="li_937FE5C40ED8471391B282D1ACE8C133"> <p>Topverkopers </p> </li> 
     </ul> </p> <p>Voor meer informatie, zie de rij "van het Attribuut van de Douane"in <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B" format="dita" scope="local"> Baseer de Aanbeveling op een Sleutel van de Aanbeveling </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Terwijl het bekijken van de definities pop-up kaart van een publiek (bijvoorbeeld, van de Bibliotheek van de Publiek), kunt u andere activiteiten nu zien die van dat publiek van verwijzingen voorzien, als toepasselijk. Op deze manier kunt u onbedoelde gevolgen voor activiteiten tijdens het bewerken van soorten publiek voorkomen. </p> <p>Eerder, toen u probeerde om een publiek te schrappen dat door activiteiten van verwijzingen werd voorzien, toonde een waarschuwing die u erop deelde dat het publiek niet met maximaal 10 activiteiten kon worden geschrapt die het publiek van verwijzingen voorzien. </p> <p>Zie <a href="../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Informatie over soorten publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> <p>Verbeterde de informatie over de lift en de begrenzingen in rapporten om deze uitgebreider en handiger te maken, inclusief knopinfo waarin wordt uitgelegd hoe de grenzen worden berekend. (TGT-28729) </p> <p>Zie <a href="../c-reports/c-report-settings/average-lift-bounds-and-confidence-interval.md#topic_AFFDC672A8A34D028B100EF6BE5D8129" format="dita" scope="local"> Gemiddelde optillen, Grenzen optillen en Vertrouwensinterval voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Geautomatiseerde Personalisatie (AP) en Auto-Target activiteiten </p> </td> 
   <td colname="col2"> <p>De extra begeleiding is beschikbaar in UI en in Hulp om u te helpen verkeerspercentages in Geautomatiseerde Persoonlijke (AP) en Auto-Doelactiviteiten effectiever toewijzen. </p> <p>Voor meer informatie, zie het <a href="../c-activities/auto-target-to-optimize.md#section_AB3656F71D2D4C67A55A24B38092958F" format="dita" scope="local"> Bepalen van de Toewijzing van het Verkeer </a> en het <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Creëren van een Geautomatiseerde Activiteit van de Aanpassing </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen: Opnameregels, verzamelingen en uitsluitingen voor aangepaste criteria </p> </td> 
   <td colname="col2"> <p>U kunt het filtreren in real time bovenop uw eigen output van douanecriteria nu uitvoeren. U kunt bijvoorbeeld de aanbevolen objecten beperken tot objecten van de favoriete rubriek of het favoriete merk van een bezoeker. Dit geeft u de macht om off-line berekeningen met het filtreren in real time te combineren. </p> <p>Met de toevoeging van inclusieregels op de Criteria van de Douane, verandert dit anders statische aanbevelingen in dynamische aanbevelingen gebaseerd op de belangen van een bezoeker. </p> <p> 
     <ul id="ul_BDD55AB34F4A43C691D2399C16AA3D6C"> 
      <li id="li_133C33E0D02E4861A4C855BD8A492E69"> <p>Aangepaste criteria kunnen nu worden geconfigureerd, net als andere criteria in aanbevelingen. </p> </li> 
      <li id="li_AC201F0917BF465C985E8947635F762E"> <p>U kunt inzamelingen, uitsluitingen, en opneming (met inbegrip van de speciale regels voor Prijs en Voorraad) op de zelfde manier gebruiken zoals om het even welke andere criteria. Verzamelingen en uitsluitingen werden al ondersteund. In deze release worden invoegingen toegevoegd. </p> </li> 
     </ul> </p> <p>Zie <a href="../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria voor meer informatie </a>. </p> <p>(TGT-28488) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen: Opnameregels, verzamelingen en uitsluitingen voor recent bekeken criteria </p> </td> 
   <td colname="col2"> <p>Onlangs bekeken items kunnen nu worden gefilterd, zodat alleen items met een bepaald kenmerk worden weergegeven. Een multinationaal bedrijf met meerdere bedrijven kan bijvoorbeeld items van de bezoekersweergave over meerdere digitale eigenschappen hebben. In dit geval kunt u de onlangs weergegeven items beperken tot weergave voor de desbetreffende eigenschap waar deze is weergegeven. Hiermee voorkomt u dat onlangs bekeken items worden weergegeven op de site van een andere digitale eigenschap. </p> <p> 
     <ul id="ul_A2D260F01CA047EEA72EF56BD0EE88FA"> 
      <li id="li_DB107DD357B741CCB2B7A4FDAD16F9D6"> <p>De onlangs bekeken Criteria zijn nu configureerbaar, zoals andere criteria in aanbevelingen. </p> </li> 
      <li id="li_85452C03F0924D4C8D854509F1293021"> <p>U kunt inzamelingen, uitsluitingen, en opneming (met inbegrip van de speciale regels voor Prijs en Voorraad) op de zelfde manier gebruiken zoals om het even welke andere criteria. Verzamelingen en uitsluitingen werden al ondersteund. In deze release worden invoegingen toegevoegd. </p> </li> 
     </ul> </p> <p>Zie <a href="../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria voor meer informatie </a>. </p> <p>(TGT-22843) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doelextensie voor starten van Adobe </p> </td> 
   <td colname="col2"> <p>Starten is de volgende generatie mogelijkheden voor tagbeheer van Adobe. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren. </p> <p>Met de extensie Doel kunt u Doel snel en eenvoudig implementeren in uw omgeving. </p> <p>Zie Doel <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25" format="dita" scope="local"> implementeren met Adobe Launch voor meer informatie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende verbeteringen, correcties en wijzigingen:

* Wanneer het creëren van of het uitgeven van A/B en Ervaring richtend (XT) activiteiten, behoudt Doel informatie over de laatste geopende ervaring, pagina, of ervaringsversie (via veelvoudige publiekseigenschap) en opent de aangewezen pagina de volgende tijd u het Doel UI opent. (TGT-28225)
* Voor compatibiliteitsdoeleinden zijn beveiligingscorrecties aangebracht.

### Target Standard/Premium 18.2.1 (15 februari 2018) {#section_837CBBB7A89D45D99855A8C5F5E7BFFB}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_1C7A462AE8D4492FA5555F060031F665"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>De Adobe Marketing Cloud is van nieuwe merken voorzien en wordt nu de Adobe Experience Cloud genoemd. </p> </td> 
   <td colname="col2"> <p>De Experience Cloud is de geïntegreerde reeks oplossingen en services voor digitale marketing van Adobe. Het is ook een intuïtieve interface waarmee u snel toegang hebt tot uw cloudoplossingen en kernservices. </p> <p>Wijzigingen voor herbranding en gebruikersinterface: Adobe Marketing Cloud is van nieuwe merken voorzien en wordt nu de Adobe Experience Cloud genoemd. Bovendien zult u veranderingen UI in de interface van het Doel en in de Schakelaar van de Oplossing zien. </p> <p>Zie <a href="https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/solutions-core-services.html" format="html" scope="external"> Informatie over de nieuwe cloudnamen in Experience Cloud voor meer informatie over deze wijziging </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] versie bevat enkele back-endverbeteringen, oplossingen en wijzigingen.

### Doelplatform (18 januari 2018) {#section_F6A0DC31636D403F92BDB9DCE7A3F6ED}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_0F5BF9370E214302BDFE0AC2D66EC773"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js 1.2.3 voegt ondersteuning toe voor JSON-aanbiedingen. JSON-aanbiedingen worden alleen ondersteund in activiteiten die zijn gemaakt met de Form-based Experience Composer. De enige manier om JSON-aanbiedingen te gebruiken is momenteel via directe API-aanroepen. Zie <a href="../c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> JSON-voorstel maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Overige wijzigingen </p> </td> 
   <td colname="col2"> <p>Uitsluitingsregels, catalogi, regels voor het opnemen van algoritmen en het filteren van runtimeprogramma zijn nu hoofdlettergevoelig. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 18.1.1 (23 januari 2018) {#section_3A2216543B064D6F82EC03E1F8AEC74D}

Deze release bevat de volgende functies en verbeteringen:

>[!NOTE]
>
>De nummer van de uitgave tussen haakjes is bedoeld voor intern gebruik door Adobe.

<table id="table_872FE2BE61CC4A5CA369D9A6C730686E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_42D7C86043C94A7BBA5ED405B2902E3A"> 
      <li id="li_50F2A7D05AB244E18D263A476BD906B3"> <p>U kunt nu tijdkadersoorten maken zonder begin- of einddatum. Hierdoor kunt u hetzelfde publiek in meerdere activiteiten gebruiken (zonder een kopie van het publiek te maken) en tegelijk de begin- en einddatums op activiteitsniveau beheren. Zie <a href="../c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdkader </a>. (TGT-25975) </p> </li> 
      <li id="li_6F08D63BC4F040859D51C47C3521C5E1"> <p>De functies Kopiëren en Bewerken zijn alleen beschikbaar voor gebruikers die alleen actief zijn wanneer u de muisaanwijzer op de pagina Publiek kiezen &gt; Alleen activiteit plaatsen boven een publiek. Eerder bestond deze functionaliteit alleen voor bibliotheekpubliek. Zie <a href="../c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> Een alleen-activiteit publiek maken </a>. (TGT-27410) </p> </li> 
      <li id="li_A8CF45E6DC37401AA273F7D6CF617524"> <p>Activiteits-slechts publiek over activiteiten kan de zelfde naam hebben. Eerder, zouden de dubbele namen in de toevoeging van tijdstempels resulteren - een dubbel publiek genoemd "Doel op Weekdag"zou als "Doel op Weekdag-1456732099201 worden bewaard." </p> <p>Voor bibliotheekpubliek zijn nog steeds unieke namen vereist. (TGT-17967) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapporten </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C595EEF916494342AD99FF0FDF999927"> 
      <li id="li_8C74478D3480406591DC876F69C19329"> <p>U kunt nu betrouwbaarheidsintervallen voor doorlopende variabelen weergeven. (TGT-22085) </p> </li> 
      <li id="li_21B31F91685C46CAA47688FDE5735312"> <p>Doel geeft nu liftgrenzen weer wanneer dit statistisch significant is in rapporten.(TGT-27301, TGT-27794, en TGT-26387) </p> </li> 
     </ul> </p> <p>Zie <a href="../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanbiedingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_BD0C5B260E7E4F139FBC1FBA286C0B81"> 
      <li id="li_FCDBABE6C5034A3596F5BBF024245FB9"> <p>Doel ondersteunt nu het maken van JSON-aanbiedingen in de aanbiedingsbibliotheek voor gebruik in de Form-Based Experience Composer. Zie <a href="../c-experiences/c-manage-content/create-json-offer.md#concept_63C7BEE1F0DB4A7596D997219B7C136D" format="dita" scope="local"> JSON-voorstel maken </a>. (TGT-27064) </p> </li> 
      <li id="li_5500AE7DCF4146E88E4619382CE8E836"> <p>U kunt nu de activiteiten bekijken die verwijzen naar een codeaanbieding in de definitie pop-up kaart van elke aanbieding. Deze functionaliteit is niet van toepassing op afbeeldingsaanbiedingen. Zie <a href="../c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> voorstellen </a>. (TGT-26277) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_63613AD2D744442AA12CD23F4DAC75B4"> 
      <li id="li_4DD5CF06D93A4083BCB34A4FFA293C89"> <p>In de gebruikersinterface wordt nu de status weergegeven van het uploaden van aangepaste algoritmegegevens voor aanbevelingen. Zie Aangepaste criteria <a href="../c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> uploaden </a>. (TGT-23891) </p> </li> 
      <li id="li_14FCFDD0A0E84B47AF1488DB4DDF197B">De waarde is Aanwezig en de Waarde is niet Huidige exploitanten zijn nu beschikbaar terwijl het creëren van de regels van de algoritmeopneming. Zie <a href="../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> Dynamische en statische inclusieregels gebruiken </a>. (TGT-24110) </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwsbrief Adobe Target Insider </p> </td> 
   <td colname="col2"> <p>Adobe Target Insider is een maandelijkse nieuwsbrief voor leden van de Adobe Target-community. Meer informatie over productupdates en toekomstige plannen, tips en trucs voor personalisatie en optimalisatie, successen van klanten, aanstaande gebeurtenissen, whitepapers met informatie, populaire blogberichten en nog veel meer. Lees de <a href="https://theblog.adobe.com/stay-optimized-adobe-target-insider-newsletter/" format="https" scope="external"> aankondigingsbrief </a> voor meer informatie. </p> <p> <a href="https://www.adobe.com/subscription/adobe_target_newsletter.html" format="html" scope="external"> Abonneren op de nieuwsbrief </a> om u te helpen de uitzonderlijke klantervaringen te leveren die bedrijfssucces drijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] versie bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen:

* U kunt nu door de pagina bladeren terwijl u de ervaringen met stap 2 van de driestapige workflow met instructies opnieuw indeelt terwijl u activiteiten maakt. (TGT-27652)
* U kunt met de rechtermuisknop op een activiteit in de Activiteitenlijst klikken om de activiteit op een nieuw tabblad te openen. Klik in Firefox bijvoorbeeld met de rechtermuisknop op de gewenste activiteit > Koppeling openen op nieuw tabblad. (TGT-27409)
* Prestatieverbeteringen zijn aangebracht op de pagina Ontwerpen (Aanbevelingen > Ontwerpen). De weergave- en zoeksnelheid voor ontwerpen is verbeterd. (TGT-21792)
* at.js is nu de standaardimplementatieoptie om te downloaden. (TGT-24676)
* Bij URL-validatie kunt u nu dubbele afbreekstreepjes gebruiken in de URL. Eerder, kon een URL met dubbele koppeltekens niet in Visual Experience Composer (VEC) worden geladen. (TGT-28176)
* Meerdere oplossingen voor de lokalisatie van de gebruikersinterface voor ondersteunde talen.

## Uitzettingen 2017 {#reference_59C7622A111C4147804A8AAC6D27BB8D}

### Doelplatform (8 november 2017) {#section_536B3C0F32ED441C8D82704B94F6AF7E}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_793CDDF1BD9E48BDBABBF6CD979BE186"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>at.js </p> </td> 
   <td colname="col2"> <p>at.js versie 1.2.2 is nu beschikbaar. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Downloaden op .js voor meer informatie </a>. </p> <p> 
     <ul id="ul_3C4C9385A0F3489AA2137A2C88AE93CF"> 
      <li id="li_E658799D930547E6901ACFBF7C541F1F"> <p>Probleem verholpen waarbij een JavaScript-fout werd geretourneerd wanneer de doelbibliotheek in de QUIRKS-modus op een pagina werd geladen. (TNT-28312) </p> </li> 
      <li id="li_050620115ED84CBDA736D94E9AAC6550"> <p>Oplossing een kwestie die Doel veroorzaakte klikken het volgen om de vraag van de gegevensinzameling van de Analyse te breken. (TNT-28261) </p> </li> 
      <li id="li_97BC1B7295364ACDAD3FB07005ED592F"> <p>Probleem verholpen waarbij <span class="codeph"> getOffer() params </span> mislukten wanneer <span class="codeph"> targetPageParams() een lege tekenreeks </span> retourneert. (TNT-28359) </p> </li> 
      <li id="li_B542D4A4E37141BA8BE79D416E1B58DB"> <p>Probleem verholpen met genereren van sessie-id bij gebruik van alleen x. (TNT-28361) </p> </li> 
     </ul> </p> <p>De standaardonderbreking voor at.js wordt veranderd van 15 seconden in 5 seconden. </p> <p>Als uw huidige instelling 15 seconden was, wordt deze bijgewerkt naar de nieuwe standaardinstelling van 5 seconden. Als u deze eerder hebt gewijzigd in iets anders, heeft dit geen invloed op de instelling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>mbox.js </p> </td> 
   <td colname="col2"> <p>De standaardtime-out voor mbox.js is gewijzigd van 15 seconden in 5 seconden. </p> <p>Als uw huidige instelling 15 seconden was, wordt deze bijgewerkt naar de nieuwe standaardinstelling van 5 seconden. Als u deze eerder hebt gewijzigd in iets anders, heeft dit geen invloed op de instelling. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.11.1 (8 november 2017) {#section_324A9B1DA0B14F5999FEE41F15B13A44}

Deze release bevat de volgende functies en verbeteringen (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

<table id="table_6ADDF3552AD04666B76F2D3F457BB042"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aanbiedingen </p> </td> 
   <td colname="col2"> <p> Als een gebruiker de toestemming van de "Redacteur"heeft, kan die gebruiker geen aanbieding uitgeven die aan een levende of geplande activiteit van verwijzingen wordt voorzien. </p> <p> <p>Opmerking:  Als een gebruiker de optie Alle werkruimten selecteert, gebruikt Target voor klanten met <a href="https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html" format="html" scope="external"> Enterprise-gebruikersmachtigingen </a>de hoogste machtigingen van de gebruiker in alle werkruimten. Als de hoogste toestemming "Redacteur is,"Doel beperkt het uitgeven zoals hierboven vermeld </p>. </p> <p>Deze beperkingen gelden voor alle aanbiedingen, niet alleen voor aanbiedingen die zijn gemaakt met Target. (TGT-27276) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reactietokens </p> </td> 
   <td colname="col2"> <p>De volgende ingebouwde parameters zijn toegevoegd: </p> <p> 
     <ul id="ul_17AD5B9788514E9DB14ED435A4224BFE"> 
      <li id="li_334F10A5B7934215B4D37278901BAF96"> <p>profile.tntId </p> </li> 
      <li id="li_AA9B4611035344549CC933FFC499289F"> <p>profile.marketingCloudVisitorId </p> </li> 
      <li id="li_DD751027371D4293BF9DB872278BD1B3"> <p>profile.thirdPartyId </p> </li> 
      <li id="li_B6D983A1B68D49AAA40CB401437676F1"> <p>profile.categoryAffinity </p> </li> 
      <li id="li_F5E86BFD14CA4C198F36F3F9987750F9"> <p>profile.categoryAffinities </p> </li> 
     </ul> </p> <p>Voor meer informatie, zie de Tokens van de <a href="../administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.10.1 (25 oktober 2017) {#section_EF74751744024C209A02F45322642D37}

Deze release bevat de volgende functies en verbeteringen (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

<table id="table_307DF0CD143048BC9E419444C556B8FB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6E91AEC68A6E45D8B2907C77E752FEC6"> 
      <li id="li_A5778B528358433DB31D700D8F9BCB79"> <p>U kunt een alleen-activiteit publiek maken vanuit de driestappenworkflow met instructies bij het maken van een activiteit. Dit publiek kan op andere plaatsen binnen de zelfde activiteit worden gebruikt, maar wordt niet opgeslagen in de Bibliotheek van Soorten publiek voor gebruik in andere activiteiten. (TGT-25474) </p> <p> <img src="assets/adhoc_audience.png" id="image_32C7C8B72F51425595A2E266AEFA17E9" /> </p> <p>Voor meer informatie, zie <a href="../c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483" format="dita" scope="local"> het Creëren van een activiteit-slechts publiek </a>. </p> </li> 
      <li id="li_691812682A5B42C0941324F2BC7D5740"> <p>Voor alle activiteiten, kunt u een succesmetrisch kiezen die de gebruiker voor het publiek kwalificeert. In het verleden, kwalificeerde het Doel gebruikers voor een publiek toen zij de activiteit inging, terwijl nu u kunt kiezen wanneer om het publiek te evalueren door een succes metrisch te kiezen. (TGT-15805) </p> <p> <img src="assets/success_metric.png" id="image_0CEC6015A2C4429790A063FE54CC1A35" /> </p> </li> 
     </ul> </p> <p>Voor meer informatie, zie een <a href="../c-target/apply-reporting-audience-success-metric.md#concept_5F11149ACCA84FE79C7B9F766B6B0595" format="dita" scope="local"> Publiek van de Rapportering op Metrisch van het Succes toepassen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automatisch doel </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6F89BD36373E47C4B3A6F8584D431D82"> 
      <li id="li_5F7B590AF8F24066ADD270E9F75CB12F"> <p>Auto-Target activiteiten steunen nu segment-vlakke rapportering. (TGT-22777) </p> <p>Voor meer informatie, zie <a href="../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> auto-Doel voor Persoonlijke Ervaringen </a>. </p> </li> 
      <li id="li_35042E7D6BB04265B42F08A23A774E92"> <p>U kunt het percentage van de Controle voor Auto-Doelactiviteiten veranderen. (TGT-26467) </p> <p> <img src="assets/auto-target-control-small.png" id="image_81F6F61DB61240C289FB71362851AA53" /> </p> <p>Voor meer informatie, zie <a href="../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> auto-Doel voor Persoonlijke Ervaringen </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aanbiedingen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_667DDEDDC5284C8393F8BCA5CD9EF12A"> 
      <li id="li_E00DB93297EC4100B46E42D867757DAA"> <p>U kunt nu definitiedetails van voorstellen op een pop-up kaart in de Bibliotheek van Aanbiedingen bekijken zonder de aanbieding te openen. (TGT-26377) </p> <p> <img src="assets/offer-card.png" id="image_1980AE8E9BED424085CC482C773C20EC" /> </p> <p>Zie <a href="../c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen voor meer informatie </a>. </p> </li> 
      <li id="li_F71AC4FDAC0E4BEE81D39490E82686C0"> <p>U kunt aanbiedingen en mappen in de keuzelijst Aanbieding kopiëren en bewerken terwijl u een activiteit maakt. (TGT-26936) </p> <p> <img src="assets/offer-picker.png" id="image_1077A6C7A8DD40FB9370CB55BD7260E5" /> </p> <p>Zie <a href="../c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen voor meer informatie </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Form-based Experience Composer </p> </td> 
   <td colname="col2"> <p>In de Form-based Experience Composer zijn Refinements vervangen door volledige publieksfunctionaliteit. De verfijningen voor bestaande activiteiten zijn gemigreerd naar alleen-activiteiten-publiek. (TGT-13646) </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Reactiepunten </p> </td> 
   <td colname="col2"> <p>U kunt nu responstokens maken van Target zonder te wachten tot deze zijn gemaakt in of geïmporteerd naar Target. Eerder, in de Symbolische UI van de Token van de Reactie, kon u slechts de tokens zien die via API werden gecreeerd. Als u de functie wijzigt, voorkomt u ook duplicaten van reactietokens. (TGT-26534) </p> <p>Voor meer informatie, zie de Tokens van de <a href="../administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] versie bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen:

* U kunt geïmporteerde soorten publiek verwijderen (Doel Klassiek, Experience Cloud enzovoort) uit de Audience Library. Het doel waarschuwt u als u probeert om een publiek te schrappen dat voor een actieve activiteit wordt gebruikt. (TGT-25171)
* Uit Target Classic geïmporteerde soorten publiek worden nu in de Audience Library aangeduid als Adobe Target Classic. In het verleden maakte de interface geen onderscheid tussen Target Standard/Premium en Target Classic. (TGT-27093)
* Verzamelingen gelden nu voor alle criteria (inclusief onlangs bekeken objecten). (TGT-26646)
* U kunt filteren op Workspace in de Audience Library and Offer Library (van toepassing op Target Premium-gebruikers met Enterprise-gebruikersmachtigingen). (TGT-26813)
* Verbeterde gebruikersinterface voor rapporten voor beter schuiven in tabellen en plaatsen van vervolgkeuzelijsten met filters. (TGT-23713 &amp; TGT-26819)

### Wijzigingen in het doelplatform (13 oktober 2017) {#section_6C298C5C3D01415CB4B658EB2166096C}

<table id="table_8457FAE3508F454F9DFDEF093FBD7E40"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>13 oktober 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.2.1 is nu beschikbaar. Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> <p> 
     <ul id="ul_14D6BB3B51974789BBFC036A45B7A56B"> 
      <li id="li_AE9826C8FC4A4DF4BE61BB72C2946C93"> <p>Probleem verholpen wanneer op een koppeling met target="_blank" werd geklikt, zodat Target de koppeling niet op een nieuw tabblad kon openen. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.9.1 (25 september 2017 en 12 oktober 2017) {#section_ECC5DD8B6ED443788B46F53E25FC896E}

Deze release bevat de volgende functies en verbeteringen (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

<table id="table_0A8817F64F434875A485FD671C6988AB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Voorvertoning van mobiele beleving </p> </td> 
   <td colname="col2"> <p><b>Bijgewerkt: 12 oktober 2017</b> </p> <p> U kunt nu meerdere activiteiten voor mobiele apps selecteren in de gebruikersinterface en deze voorvertonen op uw apparaat. Met deze functie kunt u zich inschrijven voor meerdere ervaringen voor voorvertonen en QA zonder te hoeven vertrouwen op speciale testbuilds en simulators. </p> <p>Voor deze functie is het vereist dat u de juiste versie 4.14 (of hoger) van de Adobe Mobile SDK downloadt en installeert. </p> <p>Zie <a href="../c-target-mobile-app/target-mobile-preview.md#concept_5FBF12C2FDFC42429FE4F5CFBD78E19D" format="dita" scope="local"> Doelmobiele voorvertoning voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Mobiele batchverwerking en Prefetch-levering </p> </td> 
   <td colname="col2"> <p><b>Bijgewerkt: 12 oktober 2017</b> </p> <p> De inhoud voor veelvoudige dozen kan in één enkele vraag worden pre-opgehaald en plaatselijk in het voorgeheugen ondergebracht op het apparaat zonder zich het ongerust maken hoe, wanneer, en als de eindgebruiker de inhoud zal zien. </p> <p>Voor deze functie is het vereist dat u de juiste versie 4.14 (of hoger) van de Adobe Mobile SDK downloadt en installeert. </p> <p>Zie Inhoud <a href="../c-target-mobile-app/prefetch-offer-content.md#concept_A355D9D55E1C429AA31FA4055A1DDFAF" format="dita" scope="local"> Prefetch-aanbieding voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activiteiten </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn doorgevoerd in de workflow voor het maken van activiteiten: </p> <p> 
     <ul id="ul_2D251AC11FC54E86AE84DEFFB6FDF43C"> 
      <li id="li_AB8F12B3CF654120BD16EAE570517741"> <p>Terwijl het uitgeven van een activiteit, kunt u de gewenste veranderingen op de momenteel getoonde stap aanbrengen, het drop-down op de gespleten knoop klikken, dan selecteert <span class="wintitle"> naast </span> aan de volgende stap, sparen en dicht klikken <span class="wintitle"> om uw veranderingen te bewaren en de pagina van het </span> Overzicht van de activiteit te tonen <span class="wintitle"> , of </span> <span class="wintitle"> </span> sparen klikt om uw veranderingen op te slaan en op die stap te blijven. </p> <p> <img src="assets/edit_split_button_2.png" id="image_ABC7EE42F5D341EC88AACC54CA98DA2F" /> </p> <p>Zie Een activiteit bewerken of Opslaan als concept voor meer informatie <a href="../c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> </a>. </p> </li> 
      <li id="li_4C71E2570ECF4BBAB08443D89230CE82"> <p>Tijdens het bewerken van een activiteit kunt u de gewenste workflowstap openen, wijzigingen aanbrengen (bijvoorbeeld percentages, soorten publiek enzovoort) en de activiteit vervolgens opslaan of sluiten zonder de driestappenworkflow met instructies te doorlopen. </p> <p> <img src="assets/edit_activity.png" id="image_0B9A2EF729C34A1D9FA84B8B7B17A3C1" /> </p> <p>Zie Een activiteit bewerken of Opslaan als concept voor meer informatie <a href="../c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> </a>. </p> </li> 
      <li id="li_43C15B13E4F7475E9376A98222AA0253"> <p>Wanneer u een nieuwe activiteit creeert die nog niet is opgeslagen, of u een activiteit uitgeeft die eerder in ontwerp vorm werd opgeslagen, <span class="wintitle"> sparen de </span> opties van het Ontwerp in de spleet tonen. </p> <p> <img src="assets/save_draft.png" id="image_3975786947CE4E39B900AA81D838B9B3" /> </p> <p>Zie Een activiteit bewerken of Opslaan als concept voor meer informatie <a href="../c-activities/edit-activity.md#concept_BB064C0D4A194BD1A1AE7CCA1E6BB8F0" format="dita" scope="local"> </a>. </p> </li> 
      <li id="li_36EF9AD13B2D40ADB99343C9F758D5FD"> <p>U kunt een publiek nu bewerken of kopiëren door de muisaanwijzer boven het gewenste publiek in het dialoogvenster <span class="wintitle"> Publiek kiezen te houden en u kiest voor </span> doelgroep in stap 2 van de driestappenworkflow met instructies. </p> <p> <img src="assets/audience_picker_hover.png" id="image_6DC33A0856A346948E517F0BA4C9039F" /> </p> </li> 
     </ul> </p> <p>Zie Publiek <a href="../c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087" format="dita" scope="local"> selecteren voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage </p> </td> 
   <td colname="col2"> <p>De volgende nieuwe functies en verbeteringen zijn beschikbaar voor rapportage: </p> <p> 
     <ul id="ul_2D1AF91D1B4E478FBFFA0B83EE30075E"> 
      <li id="li_98E67A4DA8BF4CFF90C279FAC12F4C54"> <p>U kunt de telmethode voor grafieken kiezen in rapporten. Merk op dat dit niet in auto-Doel en Geautomatiseerde Personalisatie (AP) activiteiten wordt gesteund. </p> <p>Zie de rij "Methodologie tellen" in <a href="../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen voor meer informatie </a>. </p> </li> 
      <li id="li_5803CE90DB764C9E983702CB6C1AFEE3"> <p>U kunt veelvoudige metriek in één enkel rapport voor auto-Doel A/B activiteiten bekijken. (TGT-23464) </p> <p>Voor meer informatie, zie Meerdere Metriek van de Mening in een Rapport <a href="../c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> bekijken </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>U kunt nu de definities bekijken van publiek dat is geïmporteerd uit Target Classic of gemaakt via API. (TGT-22630) </p> <p> <img src="assets/imported_mobile_audience_rn.png" id="image_6ED9EA63FD7D440286DBAFDBD696BA64" /> </p> <p>Voor meer informatie, zie "het Bekijken van de Definities van het Publiek"in <a href="../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> over Publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Code-editor </p> </td> 
   <td colname="col2"> <p>De op vorm-gebaseerde Composer van de Ervaring en de HTML biedt redacteur nu het zelfde coderedacteur aan die de Visuele Composer van de Ervaring (VEC) in douanecode gebruikt. (TGT-25808) </p> <p>Deze verbetering geeft u de volgende eigenschappen wanneer het gebruiken van de code redacteur in de Op vorm-gebaseerde Composer van de Ervaring en wanneer het creëren van HTML- aanbiedingen: </p> <p> 
     <ul id="ul_CBB17806FBF34774A8160A61204ED014"> 
      <li id="li_22665F583F1742E280D5BC7EC4203007"> <p>Regelnummers zijn nu zichtbaar voor betere bruikbaarheid. </p> </li> 
      <li id="li_B0D863CDAD2E46A4B133BB86886EB527"> <p>Met syntaxismarkering voorkomt u onjuiste syntaxis voor HTML-aanbiedingen. </p> </li> 
     </ul> </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code-editor </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geo gericht </p> </td> 
   <td colname="col2"> <p>U kunt breedte- en lengtegraad nu gebruiken voor geo-doelen. (TGT-12129) </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Node.JS SDK </p> </td> 
   <td colname="col2"> <p>U kunt de node.js SDK van <a href="https://www.npmjs.com/package/@adobe/target-node-client" format="https" scope="external"> npm @adobe/target-node-client installeren </a> om servertests op uw node.js-toepassingen gemakkelijk te implementeren en uit te voeren. De service VisitorID is ingeschakeld in het knooppunt SDK om al uw Adobe-gegevens te verbinden en u kunt Adobe Analytics gebruiken als uw rapportbron (A4T). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] release bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen (nummer van de uitgave tussen haakjes is voor intern gebruik door Adobe):

* Gebruikers met de machtiging fiatteur kunnen nu tokens voor API-profielverificatie genereren en inschakelen. (TGT-24074)

   Zie [Profiel-API-instellingen](../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/profile-api-settings.md#concept_5C4ABA5FA64E4D6CAE9C5902572F2794)voor meer informatie.

* Wanneer het creëren van een activiteit in de Visuele Composer van de Ervaring en de gebruiker herlaadt de pagina, worden de activiteit URL en bijbehorende eigenschappen behouden in UI. De noodzaak om opnieuw te laden kan voorkomen als de activiteit gemengde inhoud (veilige en onveilige inhoud) gebruikt of er toestemmingskwesties zijn. (TGT-28230)
* Verbeterde berichten wanneer een activiteit gemengde inhoud (veilige en onveilige inhoud) gebruikt. Het bericht bevat informatie waarmee gebruikers de benodigde stappen kunnen uitvoeren die nodig zijn om een HTTP-site of een site met gemengde aanroepen (HTTPS en HTTP) te openen. (TGT-26271)

Zie Gemengde inhoud [inschakelen in uw browser](../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/mixed-content.md#concept_46D022D50280468C9EF6D5DF6EFC911C)voor meer informatie.

* Verbeterde werkstroom wanneer de de zittingstijden van het Doel van een gebruiker uit terwijl het vormen van opties op de Opstelling, de Soorten van het publiek, en de pagina&#39;s van Aanbevelingen. Wanneer de gebruiker op Opslaan klikt, wordt het bericht dat de sessie is verlopen weergegeven, maar na het aanmelden, wordt de gebruiker in een dialoogvenster op de hoogte gebracht van een geslaagde aanmelding en blijft de gebruikersinterface op dezelfde pagina in Target staan zonder gegevensverlies. (TGT-2557)

### Wijzigingen in doelplatform (27 september 2017) {#section_AC32516DFBA64AD2AC9A74171D452778}

<table id="table_701D8D53D1DF4F28ADAC6EC221B0208A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>27 september 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.2.0 is nu beschikbaar als onderhoudsversie die hoofdzakelijk insectenmoeilijke situaties bevat. Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> <p> 
     <ul id="ul_D11024549C3643C7A756988087498D24"> 
      <li id="li_E1B3994125B64F6AB20B29FE8BCD8459"> <p>Probleem verholpen waarbij standaardhandelingen voor speciale gevallen met klikken werden voorkomen. (TNT-28089) </p> </li> 
      <li id="li_53806C902AA04B31B59AA87A1E707348"> <p>Probleem verholpen waarbij klikken en volgen op een koppeling met <span class="codeph"> target="_blank" </span> waardoor Target de koppeling niet op een nieuw tabblad kon openen. (TNT-28072) </p> </li> 
      <li id="li_94F5794330D14C71BA07B3F17D0705FD"> <p> IP de adressen kunnen als koekjesdomein worden gebruikt. (TNT-28002) </p> </li> 
      <li id="li_7D2A11B17672419583F9632CDA00D28F"> <p>Probleem verholpen dat flikkering veroorzaakte bij omleidingsvoorstellen met een global mbox of andere regionale dozen. (TNT-27978) </p> </li> 
      <li id="li_BA27A749A7A242478080F3D8E04148FC"> <p> Probleem verholpen in Experience Targeting activity setup mislukt binnen de VEC bij het schakelen tussen Bladeren en Samenstellen. (TNT-27942) </p> </li> 
      <li id="li_FA11ABA5B9CD435080426805C5359A51"> <p> Probleem verholpen met onjuiste afhandeling van flikkerstijlklassen voor kliktrackelementen. (TNT-27896) </p> </li> 
      <li id="li_E2DFBAE52FCA4996BA083868CBFCCD10"> <p>Probleem verholpen waarbij algemene mbox-parameters werden gemengd met alle mbox-parameters. (TNT-27846) </p> </li> 
      <li id="li_B3153BBD66AA4D51AE81EF6C903CF78D"> <p>Wijzigingen aangebracht om ervoor te zorgen dat Handlebars, Mustache en andere sjabloonbibliotheken aan de clientzijde correct worden afgehandeld door <span class="filepath"> at.js </span>. (TNT-27831) </p> </li> 
      <li id="li_B859939C1B5A4DF78CF8ADF236B88306"> <p>Wijzigingen aangebracht om ervoor te zorgen dat <span class="codeph"> SharedParamExpiry correct </span> wordt geïnitialiseerd en wordt doorgegeven aan de Bezoeker-API. Dit is een regressie die is toegevoegd aan <span class="codeph"> at.js 1.1.0 </span>. Dit heeft geen invloed op eerdere <span class="filepath"> </span> versies om.js. Dit is alleen van invloed op clients die omleidingsaanbiedingen en A4T gebruiken. (TNT-27791) </p> </li> 
      <li id="li_24A748DFB7824AE6AC7331B7EA940BFF"> <p>Wijzigingen aangebracht om ervoor te zorgen dat <span class="codeph"> SCRIPT </span> wordt uitgevoerd, ongeacht het type-kenmerk dat wordt gebruikt. (TNT-27865) </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gericht op ervaring (XT) </p> </td> 
   <td colname="col2"> <p><b>21 september 2017</b> </p> <p>Met de release op 21 september wijzigt Target de manier waarop gebruikers worden geplaatst in Experience Targeting (XT)-activiteiten (Landing Page campagnes in Target Classic). Voor alle nieuwe en bestaande activiteiten in zowel Target Standard/Premium als Target Classic, moeten gebruikers de ervaring naleven die op regels gericht is op elke indruk om de inhoud van de ervaring te blijven zien en in rapporten te worden geteld. Eerder, als de gebruiker niet meer gekwalificeerd voor om het even welke ervaring was, zou de gebruiker de inhoud van blijven zien en in rapporten voor, de laatste ervaring worden geteld die zij kwalificeerden. </p> <p>Deze wijziging wordt automatisch doorgevoerd als onderdeel van de release voor alle bestaande activiteiten en voor alle nieuwe activiteiten die na de release worden gemaakt. Als de vorige methode (van vóór 21 september) gewenst is, kunt u publiek tot stand brengen gebruikend profielmanuscripten zodat een gebruiker slechts aan een voorwaarde moet voldoen één keer om in dat publiek in de toekomst te blijven vallen. Gebruik vervolgens die soorten publiek voor elke ervaring in de activiteit. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.8.1 (22 augustus 2017) {#section_71A554D072F04B18B359C1626529E5D8}

<table id="table_AAC16F89060D4CC09762A370B86C0885"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Gebruikersmachtigingen voor doelversie </p> </td> 
   <td colname="col2"> <p>Maak afzonderlijke werkruimten in Doel en wijs gebruikers verschillende rollen en machtigingen toe voor afzonderlijke digitale eigenschappen. </p> <p>Voor meer informatie, zie de Toestemmingen van de Gebruiker van de <a href="../administrating-target/c-user-management/property-channel/property-channel.md#concept_E396B16FA2024ADBA27BC056138F9838" format="dita" scope="local"> Onderneming </a>. </p> <p>Zie <a href="../r-release-notes/known-issues-resolved-issues.md#concept_625C3A16B7F24D4B82EFF130F0945541" format="dita" scope="local"> Bekende problemen en Opgeloste problemen </a> voor meer informatie over de implementatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>QA-modus </p> </td> 
   <td colname="col2"> <p>Voer gemakkelijke activiteit QA met voorproefverbindingen uit die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft. </p> <p>Voor meer informatie, zie <a href="../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40" format="dita" scope="local"> Activiteit QA </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen, correcties en wijzigingen**

Deze [!DNL Target] versie bevat de volgende klantgerichte verbeteringen, oplossingen en wijzigingen: (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

* We hebben meer plaatsen toegevoegd waar u de details van de publieksdefinitie op een pop-upkaart in de doelinterface kunt weergeven zonder het publiek te openen. Deze functionaliteit is alleen van toepassing op publiek dat is gemaakt in [!DNL Target Standard/Premium. (TGT-25772)]
* U kunt nu definities van ad-hocpubliek weergeven in het maken/overzicht van activiteiten. (TGT-25570)
* De volgende variabelen zijn nu beschikbaar als [snelheidsarrays](../c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59) : `entiites` en `entityN.categoriesList`.

### Wijzigingen in doelplatform (3 augustus 2017) {#section_FA5BF6808EA74F3A9E8E941530879208}

<table id="table_1B43199F1AE64E69AE65313B23741444"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>3 augustus 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.1 is nu beschikbaar. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Downloaden op .js voor meer informatie </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> at.js </span> versie 1.1: </p> <p> 
     <ul id="ul_B7408267413347888938E2E7D48ABDBD"> 
      <li id="li_4DDF6DCFE6014C6795B6A9C9DFB54C21"> <p>Toegevoegde verwerking van responstoken. Voor meer informatie, zie de Tokens van de <a href="../administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactie </a>. </p> </li> 
      <li id="li_741CD22B7D074FBA90180B2E36FACE0D"> <p>Correctie van het probleem zodat <span class="codeph"> document.currentScript-polyfill </span> geen invloed heeft op hoekig 1.X. </p> </li> 
      <li id="li_EF1B3D3DCC7F4D2490D2BFE660EC661C"> <p>Wijzigingen aangebracht om ervoor te zorgen dat het bijhouden van klikken geen invloed heeft op de zichtbaarheidseigenschap. Klik op de volgende elementen worden gemarkeerd met de <span class="codeph"> CSS-klasse voor het bijhouden van klikken op elementen bij het element in plaats van met </span> een markering voor het element <span class="codeph"> </span>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> </p> </td> 
   <td colname="col2"> <p><b>18 juli 2017</b> </p> <p> <span class="filepath"> mbox.js </span> versie 63 is nu beschikbaar. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/target-download-config-mbox.md#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local"> Download mbox.js </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> mbox.js </span> versie 63: </p> <p> 
     <ul id="ul_F876FABA804A459D84387102DC38B7DC"> 
      <li id="li_E840AFDFAD394F5E9CDF52FABCA27EF7">Oplossing voor een probleem met het genereren van SDID bij gebruik van <span class="codeph"> mboxDefine() </span> en <span class="codeph"> mboxUpdate() </span>. Dit is alleen van toepassing op clients met de API voor bezoekers op de pagina. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.3 (3 augustus 2017) {#section_D90CB766679442C7A0642E5D79657674}

<table id="table_C81EA97B251547169BC9681E5DDB4B8F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Reactiepunten </p> </td> 
   <td colname="col2"> <p>Met responstokens kunt u automatisch in aanmerking komende variabelen (bijvoorbeeld profielkenmerken) uitvoeren in de doelreacties die activiteiten leveren (bijvoorbeeld weergavekaders). De tokens van de reactie kunnen voor het zuiveren doeleinden of voor integratie met derdeleveranciers (zoals Clicktale) worden gebruikt. </p> <p>Responstokens zijn vergelijkbaar met <span class="keyword"> Adobe Target Klassieke </span> serverplug-ins en bieden pariteit tussen de twee oplossingen. </p> <p> <p>Opmerking:  Responstokens zijn beschikbaar bij <span class="filepath"> at.js </span> 1.1 of hoger. Responstempels worden niet ondersteund met <span class="codeph"> mbox.js </span>. </p> </p> <p>Voor meer informatie, zie de Tokens van de <a href="../administrating-target/response-tokens.md#concept_2B21B222F6A344D68CA5929817E836C4" format="dita" scope="local"> Reactie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.2 (27 juli 2017) {#section_6980EC04D3CF4A00919953B9B10BC472}

<table id="table_DB51BD66756F4EBD875ED008B2C7C5D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automatisch doel </p> </td> 
   <td colname="col2"> <p>Auto-Target nu beschikbaar aan alle klanten van de Premium van het Doel. </p> <p>Auto-Target maakt gebruik van geavanceerd leren van machines om meerdere ervaren die door markters worden gedefinieerd, te identificeren en biedt elke bezoeker de meest op maat gemaakte ervaring op basis van zijn individuele klantprofiel en het gedrag van eerdere bezoekers met vergelijkbare profielen, om inhoud en stationsomzettingen aan te passen. </p> <p>Tijdens het maken van een A/B-activiteit met behulp van de driestappenworkflow met instructies kunt u ervoor kiezen om verkeer toe te wijzen met de <span class="wintitle"> </span> optie Automatisch richten op persoonlijke ervaringen: </p> <p> <img src="assets/auto-target-ui-small.png" id="image_DB7899CAD51D411EAB858CE132BECAA5" /> </p> <p>Voor meer informatie, zie <a href="../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> auto-Doel voor Persoonlijke Ervaringen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.7.1 (20 juli 2017) {#section_BB75DE30174F4ADD963451909FB81D74}

<table id="table_BCE36E0D56804E7B8861858DCF2F380E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>U kunt nu de definitiedetails van het publiek op een pop-up kaart in diverse plaatsen in het Doel UI bekijken zonder het publiek te openen. Deze functionaliteit is alleen van toepassing op publiek dat is gemaakt in <span class="keyword"> Target Standard/Premium. </span> </p> <p> <img src="assets/audience_details.png" id="image_AD0F411715DA43ACB4A913B1E54C13DC" /> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Succeswaarden </p> </td> 
   <td colname="col2"> <p>Eerder, stond Doel gebiedsdeel op enige metrisch toe en dat metrisch moest worden bereikt alvorens zijn telling werd verhoogd. U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit nu verstrekken om te kiezen of metrisch voor de telling aan toename zou moeten worden bereikt of niet. </p> <p>De multimetrische gebiedsdeelfunctionaliteit wordt niet gesteund voor het volgende: </p> <p> 
     <ul id="ul_EC856F910B704D648065EA7DA13EE5B0"> 
      <li id="li_1A82414FE50B414CAA1A0A88E80BCC1B"> <p>Activiteiten van aanbevelingen. Deze functionaliteit wordt ondersteund voor alle andere typen activiteiten. </p> </li> 
      <li id="li_2D6CF42264D445FCB6C400ED321DE952"> <p>Als u Analytics als uw rapporteringsbron (A4T) gebruikt. </p> </li> 
      <li id="li_E3A983A70BB04AE8B25A7CEC1F5FE1D9"> <p>Het metrische type "Viewed a Page". </p> </li> 
      <li id="li_9AAF6BB275F7489BA691676E308172D5"> <p>Het metrische type "Clicked an Element" voor VEC-activiteiten (Visual Experience Composer). </p> </li> 
     </ul> </p> <p>Raadpleeg de volgende onderwerpen voor meer informatie: </p> <p> 
     <ul id="ul_4B0EFFDD257C42579E19569DCBE15BE3"> 
      <li id="li_2402575F27F547968BD536C460BF81B5"> <p>A/B: <a href="../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </p> </li> 
      <li id="li_FB5E7CBC0154406C989F5A5C6CAA0C8F"> <p>Automatische personalisatie (AP): <a href="../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Een geautomatiseerde personalisatieactiviteit maken </a> </p> </li> 
      <li id="li_57C36A7945A24A52BCBD62CA0F15B668"> <p>Gericht op ervaring (XT): <a href="../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </p> </li> 
      <li id="li_06674A3152A547268A1AE5EE818EF1A5"> <p>Multivariatie (MVT): <a href="../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage (automatisch A/B-tests toewijzen) </p> </td> 
   <td colname="col2"> <p>De capaciteit om veelvoudige metriek te bekijken is nu beschikbaar voor auto-Wijs A/B activiteiten. </p> <p>Voor meer informatie, zie Meerdere Metriek van de Mening in een Rapport <a href="../c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> bekijken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>Sitepaginatypen en vergelijkingsoperatoren voor de doelsite komen nu overeen met typen en vergelijkingsoperatoren in Target Classic. </p> <p>U kunt nu het publiek van sitepagina's maken met behulp van uw eigen 'door de gebruiker gedefinieerde queryparameter' of 'door de gebruiker gedefinieerde header'. </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/site-pages.md#concept_6425D5304568490899E8340CC94798A9" format="dita" scope="local"> Sitepagina's voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activiteiten </p> </td> 
   <td colname="col2"> <p>In de lijst Activiteit kunt u nu filteren op de activiteitstypen Automatisch toewijzen en Automatisch doel. </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Criteria en aanbiedingen voor aanbevelingen </p> </td> 
   <td colname="col2"> <p>U kunt lege waarden nu afhandelen door te filteren op Vergelijking kenmerk entiteit, Vergelijking kenmerken profiel en Overeenkomende parameters. </p> <p>Zie Dynamische en statische insluitingsregels <a href="../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> gebruiken voor meer informatie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze [!DNL Target] versie bevat de volgende klantgerichte verbeteringen en oplossingen: (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

* Verbeterde workflow wanneer de [!DNL Target] sessietijden van een gebruiker tijdens het maken of bewerken van een activiteit of aanbieding aflopen. Wanneer de gebruiker klikt [!UICONTROL Save], wordt het bericht dat de sessie is verlopen weergegeven, maar na het aanmelden, wordt de gebruiker in een dialoogvenster op de hoogte gebracht van een geslaagde aanmelding en blijft de interface op dezelfde pagina aanwezig [!DNL Target] zonder gegevensverlies.

   Als een gebruiker intermitterende actie op een [!DNL Target] pagina uitvoert en een zittingsonderbreking ervaart, wordt de gebruiker geleid aan re-login en dan aan de laatste pagina geleid die in [!DNL Target] UI wordt gewerkt.

* Probleem verholpen waarbij wijzigingen in aangepaste code verloren gingen als de gebruiker wegbladert (wijzigt ervaringen, wisselpagina, wisselend publiek, klikt op Volgende enz.) en vergeet wijzigingen op te slaan. De gebruiker wordt nu gevraagd de wijzigingen op te slaan. (TGT-23766)
* Wanneer een activiteit wordt gearchiveerd, wordt &quot;Gearchiveerd de activiteit&quot; weergegeven in plaats van &quot;De activiteit bijwerken&quot;. (kB-1517)
* De drop-down kiezer in de volgende plaatsen binnen het Doel UI is vervangen met auto-volledige functionaliteit om snelheid en prestaties te verbeteren: (TGT-22939)

   * Activiteitspagina > *activiteit* > Stap3 > Suite-kiezer rapporteren
   * Soorten publiek > Soorten publiek maken > Bezoekersprofiel
   * Recommendations > Feed Creation > When source type > Analytics > Report Suite picker

* Verbeterd foutbericht wanneer voor een site &quot;X-Frame-options&quot; is ingesteld op SAMEORIGIN en de site niet kan worden geladen in Visual Experience Composer (VEC). In dit bericht wordt de gebruiker gevraagd om over te schakelen naar de Enhanced Experience Composer in Setup > Voorkeuren. (TGT-17356)
* Rapporten in Standaard/Premium worden nu weergegeven in de tijdzone van uw account in plaats van in de tijdzone van de doelserver (US EST). (TGT-24868)
* Als in gemaakte activiteiten van buiten [!DNL Target] worden bijgewerkt [!DNL Target] (bijvoorbeeld via Adobe I/O), worden de volgende activiteitskenmerken weer geïmporteerd in [!DNL Target]:

   `thirdpartyId`

   `startDate`

   `endDate`

   `status`

   `priority`

   `marketingCloudMetadata(remoteModifiedBy)`

   Deze importtaak wordt uitgevoerd wanneer de activiteitenpagina wordt geopend, met een maximale vertraging van tien minuten. (kB-1526)

### Wijzigingen in doelplatform (18 juli 2017) {#section_08A2B80060FE4833B1BDD12D1AF5E3D6}

<table id="table_17607030DA7948819F73FA9F2B22AB5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js </span> </p> </td> 
   <td colname="col2"> <p><b>18 juli 2017</b> </p> <p> <span class="filepath"> mbox.js </span> versie 63 is nu beschikbaar. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/target-download-config-mbox.md#task_4EAE26BB84FD4E1D858F411AEDF4B420" format="dita" scope="local"> Download mbox.js </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> mbox.js </span> versie 63: </p> <p> 
     <ul id="ul_6C88DB6332A94858B278F7F846E2F8EB"> 
      <li id="li_597D15CAD9DA44008FEC01E6BB3CB9A7">Oplossing voor een probleem met het genereren van SDID bij gebruik van <span class="codeph"> mboxDefine() </span> en <span class="codeph"> mboxUpdate() </span>. Dit is alleen van toepassing op clients met de API voor bezoekers op de pagina. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p><b>7 juli 2017</b> </p> <p> <span class="filepath"> at.js </span> versie 1.0 is nu beschikbaar. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Downloaden op .js voor meer informatie </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> at.js </span> versie 1.0: </p> <p> 
     <ul id="ul_4407D3923CE34CD8AD7120A2580A34DF"> 
      <li id="li_34C8D0572A0340DF99294DD33E352D2C"> <p>Ondersteuning voor asynchroon laden op .js voor sneller laden van pagina's. </p> </li> 
      <li id="li_BC944624B3104418854140484E682D69"> <p>Ondersteuning voor het vooraf verbergen van pagina-inhoud bij het asynchroon laden van at.js. </p> </li> 
      <li id="li_F9D0AD095A2A425CB78772DDE8FCCF97"> <p>Betere foutberichten wanneer de levering van inhoud is uitgeschakeld. </p> </li> 
      <li id="li_4B32468665A34FC0AF66C1CD15DE7AFC"> <p>Prestatieverbeteringen bij het uitvoeren van meerdere activiteiten. </p> </li> 
      <li id="li_48EAD25A4077411E954CCCDB95058924"> <p>Ondersteuning voor YUI-compressor. </p> </li> 
      <li id="li_3598B4223C0A478D956A7EC618BFBCD6"> <p>Foutenmelding voor aangepaste gebeurtenissen tijdens de levering van de activiteit. </p> </li> 
      <li id="li_28A5DDF1A9D64D66BF8BD0E89E5BD69B"> <p>Oplossen voor prestatieproblemen in Microsoft Internet Explorer 11. </p> </li> 
      <li id="li_BB1C11A76FB14341AB7699F2C7753377"> <p>Oplossing voor de <span class="codeph"> </span> functie getOffer() die een fout geeft op sommige websites. </p> </li> 
      <li id="li_4C7F3DE9A0A346C38E9EDCE21C83843D"> <p>Laad de doelbibliotheek asynchroon. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.6.2 (22 juni 2017) {#section_F0372B07B56E454CB048CE79FF56E9CD}

<table id="table_8C4DB1B83B874E4C85CE9FF352E7B857"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" class="premium"> <p>Activiteiten op het gebied van geautomatiseerde personalisatie </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_F5BB1074DD4140C798CB55D68DEEF824"> 
      <li id="li_9596AABA14C64DEEB2E70E8ADED8AA74">De geautomatiseerde activiteiten van de Personalisering kunnen worden gecreeerd gebruikend op vorm-gebaseerde samensteller. </li> 
      <li id="li_315F5FF590404670A677FEA6E4E0DF5D">Nieuwe betrouwbaarheidsnummers voor automatische personalisatie </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen: Criteria en aanbiedingen </p> </td> 
   <td colname="col2"> <p> U kunt nu dynamische criteria en promoties maken op basis van overeenkomsten tussen profielkenmerken en parameters. </p> <p> <img src="assets/inclusion_rules.png" id="image_D136F75A5C2B428390FE231559AEC2D3" /> </p> <p> <p>Opmerking:  Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen ("overeenkomsten" zijn nu "gelijk"), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbeteringen in de VEC Code Editor </p> </td> 
   <td colname="col2"> <p> Als de paginaopmaak verandert en de handelingen niet kunnen worden toegepast, verschijnt nu een waarschuwing naast elke mislukte handeling. Eerder heeft een algemene fout de gebruiker laten weten dat de paginastructuur is gewijzigd. De code-editor markeert nu elke mislukte handeling. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze [!DNL Target] versie bevat de volgende klantgerichte verbeteringen en oplossingen:

* Verbeterde prestaties op hostgroepen en aanbevelingen voor zoekpagina&#39;s van entiteiten.
* Beschrijvende foutberichten voor het hele doel, vooral als deze betrekking hebben op synchronisatiefouten.
* Probleem verholpen waarbij de telling van het activiteitsdiagram soms onjuist was in de gebruikersinterface wanneer automatisch dedupliceren wordt toegepast na het maken van uitsluitingsgroepen.
* Probleem verholpen waarbij handmatige insluitingen mogelijk niet correct worden weergegeven in de gebruikersinterface wanneer een bestaande activiteit met uitsluitingsgroep wordt bewerkt.

### Target Standard/Premium 17.6.1 (8 juni 2017) {#section_1D05FE23CE3744DDB5D28E933341F575}

<table id="table_47117524922A472AA977C652B581B356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Targeting (XT)-activiteiten </p> </td> 
   <td colname="col2"> <p>Met de functie slepen en neerzetten kunt u het publiek en de ervaringen in de gewenste volgorde rangschikken tijdens het maken of bewerken van XT-activiteiten. Bezoekers worden op hun ervaringen beoordeeld, van boven naar beneden. </p> <p> <img src="assets/move_exp.jpg" id="image_0AA2EE2B5B00462C8E125A30F145E654" /> </p> <p>Zie Ervaring maken voor meer informatie <a href="../c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage: A/B, XT, en Aanbevelingen </p> </td> 
   <td colname="col2"> <p>De rapporten voor A/B, XT, en de activiteiten van Aanbevelingen omvatten visuele vertegenwoordiging die u visueel het betrouwbaarheidsinterval laten zien en optillen zodat u een winnaar nauwkeuriger kunt bepalen. U kunt de muis boven de representaties houden om de werkelijke getallen te zien. Deze functie is niet beschikbaar voor activiteiten die Analytics als rapportagebron (A4T) gebruiken. </p> <p> <img src="assets/whisker.JPG" id="image_DFD8EED61D52497280066D55AD473479" /> </p> <p>Zie <a href="../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Activiteiten op het gebied van geautomatiseerde personalisatie </p> </td> 
   <td colname="col2"> <p>U kunt uitsluitingsgroepen maken in AP-activiteiten om ervoor te zorgen dat ervaringen met de toegewezen aanbiedingen automatisch worden uitgesloten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen: Criteria en aanbiedingen </p> </td> 
   <td colname="col2"> <p><b>(Gepland om 22 juni 2017 vrij te geven)</b> U kunt nu dynamische criteria en promoties tot stand brengen die op profielkenmerkaanpassing en parameter aanpassing worden gebaseerd. </p> <p> <img src="assets/inclusion_rules.png" id="image_694305D969AF43F7822012F69614250C" /> </p> <p>Zie Dynamische en statische insluitingsregels <a href="../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> gebruiken voor meer informatie </a>. </p> <p> <p>Opmerking:  Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen ("overeenkomsten" zijn nu "gelijk"), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Naamgevingsactiviteiten </p> </td> 
   <td colname="col2"> <p>U wordt nu gevraagd de activiteit een naam te geven voordat u deze opslaat. U kunt een activiteit zonder een naam niet opslaan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe locatie voor doelforum </p> </td> 
   <td colname="col2"> <p> Het Target Forum is verplaatst naar het nieuwe <a href="https://forums.adobe.com/community/experience-cloud/marketing-cloud/target" format="https" scope="external"> Adobe Community Platform </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze [!DNL Target] versie bevat de volgende klantgerichte verbeteringen en oplossingen: (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

* Probleem met XSS-beveiliging verholpen met [!DNL mbox.js]. Deze correctie is een servercorrectie waarvoor geen [!DNL mbox.js] update nodig is.

### Target Standard/Premium 17.4.1 (27 april 2017) {#section_24E6889AF1E0405497F6F77A407A9A46}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_9554D0094421417C88548BDC97B710F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Rapportage </td> 
   <td colname="col2"> <p><b>Meerdere doelen/cijfers weergeven:</b> U kunt veelvoudige metriek in A/B en Ervaring nu bekijken richtend (XT) activiteiten, met uitzondering van <a href="../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> auto-Wijs </a> en <a href="../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> Auto-Doel </a> A/B activiteiten. </p> <p>Voor meer informatie, zie Meerdere Metriek van de Mening in een Rapport <a href="../c-reports/c-report-settings/view-multiple-metrics.md#concept_9E3C3F6F3EC1412FAF252975AC0720B7" format="dita" scope="local"> bekijken </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze [!DNL Target] versie concentreert zich op achterste-eindmoeilijke situaties en omvat de volgende klant-onder ogen ziende verhogingen en moeilijke situaties: (nummer van de uitgave staat tussen haakjes voor intern gebruik door Adobe):

* Probleem verholpen waarbij de instelling &quot;Aantal verhogen, Gebruiker vrijgeven &amp; opnieuw invoeren toestaan&quot; in Geavanceerde instellingen ertoe leidde dat activiteiten niet correct zouden werken. (TNT-26556)
* Probleem verholpen waarbij klantkenmerkgegevens niet van Target konden worden verwijderd nadat ze met NULL waren bijgewerkt in de gebruikersinterface van Experience Cloud. (TNT-26462)

### Wijzigingen in doelplatform (13 april 2017) {#section_B59C26405EB7482AA80820D6D39B9C44}

<table id="table_6167ECB7B44F40DCADF299F46F1F795C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> at.js </span> versie 0.9.6 is nu beschikbaar. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2" format="dita" scope="local"> Downloaden op .js voor meer informatie </a>. </p> <p>De volgende verbeteringen en correcties zijn opgenomen in <span class="filepath"> at.js </span> versie 0.9.6: </p> <p> 
     <ul id="ul_108DF85393614C69988E299485D338FD"> 
      <li id="li_4117C900982240B5AFFCFE1B2716A443"> <p>Omleiding biedt ondersteuning voor A4T. Nadat u hebt gedownload en geïnstalleerd <span class="filepath"> in .js </span> versie 0.9.6, kunt u aanbiedingen in activiteiten gebruiken die <span class="keyword"> de Analyse van Adobe </span> als Rapporterende Bron voor <span class="keyword"> </span> Doel (A4T) gebruiken. Naast <span class="filepath"> at.js </span> versie 0.9.6, zijn er andere minimumeisen uw implementatie moet voldoen om te gebruiken doorleidt aanbiedingen en A4T. Voor meer informatie en extra belangrijke informatie zou u moeten weten, zie Aanbiedingen van de Omleiding - Veelgestelde vragen A4T <a href="../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> </a>. </p> </li> 
      <li id="li_DA5321D72E81496DB7C49D589E1A59C4"> <p>Voorafgaand aan <span class="filepath"> 0.js </span> .9.6, toen de bezoeker-API aanwezig was op de pagina en de <span class="codeph"> bezoekerApiTimeout </span> -instelling te agressief was, kon Target in een situatie terechtkomen waarin geen MCID-gegevens werden verzonden in de <span class="keyword"> aanvraag van het Doel </span> . Dit kan bij het gebruik van A4T leiden tot problemen zoals onverwachte resultaten in <span class="keyword"> Analytics </span> . </p> <p>Dit gedrag is gewijzigd in <span class="filepath"> at.js </span> 0.9.6, zelfs als bezoekerApiTimeout om 1 ms <span class="codeph"> </span> wordt geplaatst te zeggen, zal het Doel proberen om SDID, volgende servers, en de gegevens van klant IDs te verzamelen en die in het verzoek van het Doel te verzenden. </p> </li> 
      <li id="li_B11CE11D9A594CB1ABB85BD0D93C4A15"> <p>De <span class="codeph"> </span> instelling SelectorsPollingTimeout is toegevoegd. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> targetGlobalSettings() voor meer informatie </a>. </p> </li> 
      <li id="li_D6F862099A374FE394F4DA3520A1BBF0"> <p>De indeling van de reactie van <span class="codeph"> getOffer() </span> is gewijzigd. Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#reference_C81525D1598A4A1199740DCAB81A7FDF" format="dita" scope="local"> adobe.target.getOffer(options) voor meer informatie </a>. </p> </li> 
      <li id="li_80166567ED8945ECB37FEEE2C5F06ACE"> <p>Logboekregistratie voor console is toegevoegd voor niet-ondersteunde <span class="codeph"> &lt;!DOCTYPE&gt;- </span> declaraties. </p> </li> 
      <li id="li_02904EBAE8D3400092B762F0B28B0C86"> <p>Probleem verholpen waarbij <span class="keyword"> standaard niet-geselecteerde Klassieke </span> plug-ins correct werden toegepast wanneer meerdere standaardaanbiedingen naar één box werden geleverd. (TGT-22664)</p> </li> 
      <li id="li_7016022D9DDE4529B77984F195825AB7"> <p>Verbeterde cookie-instelling voor twee TLD's (Top-Level-Domain) om ervoor te zorgen dat de box-cookie correct is ingesteld voor deze domeinen (bijvoorbeeld <span class="filepath"> test.no </span>, <span class="filepath"> autodrives.ca </span>enzovoort). </p> </li> 
      <li id="li_3B1F618DEC744056B5BB172C4DBB359A"> <p>Het algoritme voor het extraheren van het domein op hoofdniveau dat moet worden gebruikt bij het opslaan van cookies is gewijzigd in <span class="codeph"> versie 0.js </span> 0.9.6. Vanwege deze wijziging kunnen cookies niet worden opgeslagen naar adressen die IP gebruiken. Meestal worden IP-adressen gebruikt voor testdoeleinden, maar als tijdelijke oplossingen kunt u DNS-vermeldingen gebruiken of het hostbestand op een lokaal vak aanpassen. </p> </li> 
      <li id="li_A52181499E63402DB4E16E33E36A9400"> <p>Correctie van het verplaatsen en herschikken van handelingen waarbij eigenschappen tekenreekswaarden zijn in plaats van gehele getallen. </p> </li> 
     </ul> </p> <p>Voor informatie over dit en vorige versies van <span class="filepath"> at.js </span>, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.3.1 (30 maart 2017 - Bijgewerkt op 13 april 2017) {#section_5C13660A8AA34F35A9CBEFEEC88738D0}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_4BA8DA701BC64427957355E144570EFE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Analyses voor doel (A4T) </p> <p>Omleidingsvoorstellen </p> </td> 
   <td colname="col2"> <p><b>Bijgewerkt op 13 april 2017.</b> </p> <p>U kunt nu omleidingsaanbiedingen gebruiken in activiteiten die <span class="keyword"> Analytics </span> als rapportbron gebruiken. </p> <p>Deze bibliotheken moeten op de pagina worden opgenomen met het omleidingsvoorstel en de pagina waarnaar de bezoeker wordt omgeleid. Als onderdeel van deze wijziging worden automatisch nieuwe URL-parameters toegevoegd aan uw omleidings-URL's als de service Bezoeker-id op uw site is geïmplementeerd, ongeacht of u Analytics als rapportbron voor die activiteit gebruikt of niet. </p> <p>Zie <a href="../c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905" format="dita" scope="local"> Aanbiedingen omleiden - A4T Veelgestelde vragen voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn doorgevoerd voor doelgroepen: </p> <p> 
     <ul id="ul_C920198404654C97A33190A29ACA6990"> 
      <li id="li_DB52EF909C9640649981940460CDF2B5"> <p><b>Wek- en dagscheiding:</b> U kunt de opties voor <span class="wintitle"> </span> Week- en Dagscheiding instellen om terugkerende patronen te maken voor doelgroepen. </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdkader </a>. </p> </li> 
      <li id="li_2541A6EF2D604CE098012A16909C237E"> <p><b> Uitsluitingen bij gecombineerd publiek:</b> U kunt uitsluitingsregels nu toevoegen en het publiek uitsluiten wanneer u meerdere soorten publiek combineert. </p> <p>Zie Meerdere soorten publiek <a href="../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> combineren voor meer informatie </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen </p> </td> 
   <td colname="col2"> <p><b>Dynamische promoties:</b> Doelaanbevelingen ondersteunen nu dynamische overeenkomsten voor promoties. </p> <p>Zie Dynamische en statische insluitingsregels <a href="../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F" format="dita" scope="local"> gebruiken voor meer informatie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De capaciteit om veelvoudige metriek in een rapport te bekijken, inbegrepen in Doelversie 17.3.1 (30 maart, 2017) is verwijderd toe te schrijven aan onverwacht gedrag. Deze functie is in een volgende release weer beschikbaar.

Deze [!DNL Target] release bevat de volgende verbeteringen en oplossingen: :

* De [!DNL Target] gebruikersinterface is bijgewerkt om aanbiedingen voor omleiding te ondersteunen in activiteiten die [!UICONTROL Analytics for Target] (A4T) als rapportagebron gebruiken. Voor deze functionaliteit is [!DNL at.js] 0,9,6 vereist, die binnenkort beschikbaar is.
* De [!DNL Target] gebruikersinterface is op sommige plaatsen bijgewerkt:

   * In rapporten en activiteiten zijn er opties ( [!UICONTROL Edit], [!UICONTROL Share to Feed], [!UICONTROL View Experience URLs]enz.) zijn nu toegankelijk door op het [!UICONTROL More Options] pictogram (  ![](assets/icon_more_options.png)

      ).
   * In de [!UICONTROL Offers] bibliotheek worden nu in een lijst weergegeven in plaats van als kaarten. Er zijn andere kleine wijzigingen aangebracht in de gebruikersinterface van de [!UICONTROL Offers] bibliotheek.

* Aanzienlijk verbeterde prestaties op de [!UICONTROL Activity] [!UICONTROL Audience] lijsten en op de lijsten. Bovendien worden de laadtijden voor zoekresultaten aanzienlijk sneller weergegeven.
* &quot;Weergaven&quot; staat nu &quot;Bezoekingen&quot; in de [!UICONTROL Offer Level Report] lijst voor [!UICONTROL Automated Personalization] rapporten.
* [!DNL Target] ondersteunt nu het schakelen van omgevingen (hostgroepen) voor [!UICONTROL Automated Personalization] activiteiten.
* [!UICONTROL Automated Personalization] de activiteiten ondersteunen nu hostgroepen .

### Target Standard/Premium 17.2.1 (21 februari 2017) {#section_FC6412353DE64E848FFD5E8EFF72C7C7}

>[!NOTE]
>
>[!DNL Adobe Experience Manager] 6.2 met FP-11577 (of later) steunt nu [!DNL at.js] implementaties met zijn [!UICONTROL Adobe Target Cloud Services] integratie. Zie [Feature Packs](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) en [Integrating with Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in de documentatie van *Adobe Experience Manager 6.2* voor meer informatie.

Deze [!DNL Target] release is gericht op verbeteringen van de bruikbaarheid en prestaties en bevat de volgende verbeteringen en correcties (nummer van de uitgave tussen haakjes zijn voor intern gebruik door Adobe):

* Extra items toegevoegd aan het menu Help die toegankelijk zijn vanuit de rechterbovenhoek van de [!DNL Target] gebruikersinterface. Tot de nieuwe opties behoren: &quot;Blogs&quot; en &quot;Video&#39;s&quot;. De optie &#39;Adobe Experience Cloud Status&#39; is nu &#39;Adobe Target Standard/Premium Status&#39;. (TGT-22629)
* Wanneer het schrappen van een publiek, [!DNL Target] toont een lijst van activiteiten die van dat publiek van verwijzingen voorzien. Gebruikers kunnen op elke activiteit in de lijst klikken om de bijbehorende [!UICONTROL Overview] pagina weer te geven. (TGT-17997)
* Verbeterd `user.activeCampaigns` om de campagne-id te retourneren voor alle campagnes/activiteiten waarin de gebruiker zich bevindt, zelfs als hij of zij tijdens de huidige sessie niet heeft gereageerd op de campagne/activiteit. (TNT-26237)
* De [!UICONTROL Create Activity] knop op de [!UICONTROL Activities] pagina is nu actief voordat alle activiteitennamen in de lijst worden geladen. Deze verbetering laat gebruikers nieuwe activiteiten sneller tot stand brengen, vooral wanneer de rekening vele gevormde activiteiten heeft. (TGT-21470)
* Verbeterde laadtijd voor websites met HTTPS die via proxy kunnen worden benaderd. Dit is een verbetering van de Enhanced Experience Composer (EEC). Het doel haalt geen statische middelen meer via volmacht. (TGT-21793)
* Prestatieverbeteringen op de [!UICONTROL Goals & Settings] pagina zijn aangebracht, vooral tijdens laadtijd wanneer er veel metriek zijn gedefinieerd voor een activiteit. (TGT-21654)
* Knopinfo op de [!UICONTROL Goals & Settings] pagina van alle activiteiten is toegevoegd met behulp van [!UICONTROL Analytics for Target] (A4T)-rapporten die gebruikers informeren dat een trackingserver niet vereist is als de pagina&#39;s van de activiteit op .js (versie 0.9.1 of hoger) of mbox.js (versie 61 of hoger) zijn geladen. (TGT-22607)
* Er worden nu metrische namen op de [!UICONTROL Goals & Settings] pagina weergegeven zonder dat gebruikers elke metrische waarde hoeven uit te vouwen om de volledige metrische naam weer te geven. Deze verbetering laat gebruikers metriek sneller en efficiënter uitgeven. (TGT-21276)
* U kunt nu [!DNL Recommendations] inclusieregels op douanecriteria (geupload via CSV), enkel zoals om het even welke andere criteria toepassen. (TGT-21896)
* Verbeterde gebruikersinterface en bruikbaarheid van de [!UICONTROL Offers] pagina, vooral bij het maken of beheren van mappen en het maken van aanbiedingen. (TGT-22509 en TGT-22187)
* Verbeterde gebruikerservaring in [!UICONTROL Visual Experience Composer] (VEC) bij het selecteren van items die u wilt verbergen.
(TGT-2224)
* De gebruikerservaring is verbeterd bij het maken van activiteiten met de [!UICONTROL Form-Based Experience Composer]. Wanneer u een locatie voor het selectievakje kiest, blijft het validatierand gemarkeerd nadat u op de locatie hebt geklikt [!UICONTROL Next]. (TGT-2221)
* Verbeterde de gedownloade rapporten om onderscheid te maken tussen actieve en verwijderde aanbiedingen. (TGT-22449)
* Probleem verholpen waardoor oudere elementen niet konden worden weergegeven in de lijst met oneindig schuifbare elementen in de gebruikersinterface van de Experience Cloud Assets core service. (TGT-19733)
* Probleem verholpen waarbij de extreme orderinstelling niet in gedownloade CSV-rapporten werd gebruikt. (TGT-21871)
* Probleem verholpen waarbij extreme bestellingen niet correct werden gemarkeerd in het gedownloade [!UICONTROL Order Details]CSV-rapport. (TGT-22500)
* Probleem verholpen waarbij de onjuiste ordertijd in het gedownloade [!UICONTROL Campaign Audit] CSV-rapport werd weergegeven, ook al werd in het rapport de juiste besteldatum weergegeven. (TNT-26469)
* Probleem verholpen waardoor de [!UICONTROL Disable JavaScript] optie niet correct werkte bij activiteiten van meerdere pagina&#39;s. (TGT-15130)
* Als u de op vorm-Gebaseerde Composer van de Ervaring met een doos buiten auto-gecreeerde globale mbox ( `target-global-mbox`) gebruikt, en dan een betrokkenheidsmetrisch kiest als succes metrisch, de metrische verhogingen slechts op pagina&#39;s die de mbox hebben die in de activiteit wordt gebruikt. Als voorbeeld, als uw mbox is `homepage_mbox`, is [!UICONTROL Pages Per Visit] metrisch het aantal klappen aan `homepage_mbox` tijdens dat bezoek.

   Als u dit niet wilt, kunt u een andere locatie aan de activiteit toevoegen en het globale vakje aan die locatie toewijzen en de standaardinhoud ervan geven. Deze tijdelijke oplossing verbindt globale mbox met de activiteit en staat Doel toe om metrisch voor het melden te tellen.

### Wijzigingen in doelplatform (18 januari 2017) {#section_EA41802B2B24426FBA88D25E17DBE360}

<table id="table_3A2CD47252894F119B0E60BF6A9285B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js, </span> versie 0.9.4 </p> </td> 
   <td colname="col2"> <p>18 januari 2017 </p> <p> <span class="codeph"> at.js </span> versie 0.9.4 bevat de volgende wijzigingen: </p> <p> 
     <ul id="ul_8F149C28E2D946B9888B4D2F45167C3C"> 
      <li id="li_93E866BBFE374E93BCDB65BCFAC33B62"> <p> mbox-namen kunnen nu speciale tekens bevatten, zoals ampersands ( &amp; ), zodat deze consistent zijn met de naamgevingsvereisten voor mbox-namen met <span class="codeph"> mbox.js </span>. (TNT-26144) </p> <p>Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local"> in.js Configurations voor meer informatie </a>. </p> </li> 
      <li id="li_99309046030B4D93B59113C01A8789DA"> <p>Toegevoegde <span class="codeph"> veiligeAlleen- </span> instelling die aangeeft of <span class="codeph"> at.js alleen HTTPS </span> mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld en die via <span class="codeph"> targetGlobalSettings kan worden overschreven </span>. (TNT-26183) </p> <p>Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md#concept_8DACBC47ABDE4279BB102B42609FE506" format="dita" scope="local"> targetGlobalSettings() voor meer informatie </a>. </p> </li> 
      <li id="li_D84D578C43A24D4896795999F841CEB8"> <p>De optie <span class="wintitle"> Oudere browserondersteuning </span> is beschikbaar in <span class="codeph"> versie 0.js </span> versie 0.9.3 en lager. Deze optie is verwijderd in <span class="codeph"> at.js </span> versie 0.9.4. </p> <p>Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812" format="dita" scope="local"> in.js Configurations voor meer informatie </a>. </p> </li> 
     </ul> </p> <p>Voor gedetailleerde informatie over de veranderingen in elke versie van <span class="codeph"> at.js </span>, zie <a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/target-atjs-versions.html" format="html" scope="external"> bij.js de Details van de Versie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mbox.js, </span> versie 62 </p> </td> 
   <td colname="col2"> <p>18 januari 2017 </p> <p> <span class="codeph"> mbox.js </span> versie 62 bevat de volgende verbeteringen en oplossingen: </p> <p> 
     <ul id="ul_1D4351AEB0D74FE4B09196113A4672C1"> 
      <li id="li_653D9C605A0B447AB1FFEE5D22D3AD05"> <p>Problemen met flikkering bij omleidingsactiviteiten zijn opgelost bij weergave in Google Chrome-browsers. (TNT-24928) </p> </li> 
      <li id="li_2196D7CD9B144C0A96AE8B8D13976C69"> <p>Toegevoegde <span class="codeph"> alleen-beveiligde </span> instelling die aangeeft of <span class="codeph"> mbox.js alleen HTTPS </span> mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld. (TNT-26183) </p> <p>Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C" format="dita" scope="local"> vorm mbox.js </a>. </p> </li> 
     </ul> </p> <p>Voor gedetailleerde informatie over de veranderingen in elke versie van <span class="codeph"> mbox.js </span>, zie <a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mboxjs-change-log.html" format="html" scope="external"> mbox.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 17.1.1 (19 januari 2017) {#section_88AFA2F54CF24DF7822CFEBB07DFABE2}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_4F7D4A71F5DF4E8782C7DBEEEF24AD04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Inhoud/aanbiedingen </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn nu beschikbaar voor aanbiedingen: </p> <p> 
     <ul id="ul_7D8E81443E0F48B6A0C1D1DF6F27D292"> 
      <li id="li_EA529EF4EBC2416E9D3B9E7251E7AAAB"> <p>De naam van de pagina Inhoud is gewijzigd in Aanbiedingen. Bovendien zijn er nu twee tabbladen aan de rechterkant om codes aan te bieden van afbeeldingsaanbiedingen. </p> <p>Als u vóór deze release code en afbeeldingen in dezelfde map had, worden deze door Target gesplitst in twee dubbele mappen. </p> </li> 
      <li id="li_9574FA6BDCFB4BAB938273BF7F4B21C8"> <p>Aanbiedingen die zijn gemaakt via Target Classic, Adobe Experience Manager (AEM), Adobe Mobile Services (AMS) en API's zijn nu zichtbaar in de gebruikersinterface Target Standard/Premium. Aanbiedingen die zijn gemaakt in Target Classic, kunnen worden bewerkt in Target Standard/Premium. (TGT-15738) </p> <p> Aanbiedingen die in de laatste twee jaar met behulp van deze methoden zijn bijgewerkt, zijn zichtbaar in Target Standard/Premium (d.w.z. januari 2015 en daarna). </p> </li> 
      <li id="li_CAD67C9EBB564525ABD2269D918275F8"> <p>U kunt aanbiedingen nu filteren op bron en type. </p> </li> 
     </ul> </p> <p>Zie <a href="../c-experiences/c-manage-content/manage-content.md#concept_17874A6FCBB743AA84C5988E8571CCF3" format="dita" scope="local"> Aanbiedingen voor meer informatie </a>. </p> <p>De volgende verbeteringen zijn aangebracht op het gebied van geolocatie: </p> <p> 
     <ul id="ul_DD8B50F980B8447A8C37EA96530D8949"> 
      <li id="li_348E04AB29B14E6F83E3A7E7BF7D75B8"> <p>U kunt nu <span class="codeph"> profile.geolocation- </span> waarden rechtstreeks als tokens gebruiken in aanbiedingen, plug-ins enzovoort. (TNT-25967) </p> </li> 
     </ul> </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportage </p> <p> <p>Opmerking:  Deze verbeteringen zijn niet van toepassing op Analytics for Target (A4T)-rapporten. </p> </p> </td> 
   <td colname="col2"> <p>De volgende rapporteringsverhogingen zijn nu beschikbaar voor de rapporten van het Doel. </p> <p> 
     <ul id="ul_ACFCA821B120419EA252EF5031309D52"> 
      <li id="li_0B634602BB044AEDB26DAF78189AB833"> <p>De gebruikersinterface voor rapporten is opnieuw ontworpen. </p> </li> 
      <li id="li_309435D10AE84E8795C4CCC1F36747F7"> <p>Doelrapporten hebben nu een optie om rapportgegevens opnieuw in te stellen om oude gegevens te verwijderen. (TGT-5933) </p> </li> 
      <li id="li_9D30BFCC4CD6461B9DDCD5797A5E2B3A"> <p>De opties voor de telmethode voor rapportage omvatten Bezoekers (de standaardinstelling), Bezoeken en Activity Impressions. (TGT-10002) </p> </li> 
     </ul> </p> <p>Zie <a href="../c-reports/c-report-settings/report-settings.md#concept_4BB6A7FDAB6F4806A632F9CD989B8BFA" format="dita" scope="local"> Rapportinstellingen </a> en <a href="../c-reports/conversion-rate.md#concept_EC19BC897D66411BABAF2FA27BCE89AA" format="dita" scope="local"> Telmethode </a>. </p> <p>De volgende rapportverbeteringen zijn nu beschikbaar voor downloadbare CSV-rapporten: </p> <p> 
     <ul id="ul_18B0636A41B94F9F903ABFE3E13285DA"> 
      <li id="li_2422075AA0A34F868809C5D580FC5D4B"> <p>Het CSV-rapport op het niveau van de aanbieding bevat nu aanvullende details over elke aanbieding. (TGT-18995) </p> </li> 
      <li id="li_659D126E846348D4BE4544962F41539F"> <p>Gedownloade CSV-bestanden op aanbiedingsniveau bevatten nu altijd gegevens uit de besturingselementen en doelsegmenten voor <span class="wintitle"> Automated Personalization- </span> rapporten. (TGT-22000) </p> </li> 
     </ul> </p> <p>De volgende rapporteringsverhogingen zijn nu beschikbaar voor Geautomatiseerde Persoonlijke (AP) rapporten. </p> <p> 
     <ul id="ul_5743684487CD4905BA998C298FD423D7"> 
      <li id="li_EB48BA21E00C4878B4408D24DD23BA9C"> <p>Verbeterde rapporttijd voor Automated Personalization-activiteiten. </p> </li> 
      <li id="li_B8ECCE250A674B83A66705AD5C45B9C3"> <p>Het betrouwbaarheidsinterval voor ononderbroken variabelen (de metrische types van Inkomsten en van de Betrokkenheid) wordt nu getoond in de Geautomatiseerde samenvattingsrapporten van de Personalisatie (AP). </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activiteiten </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn nu beschikbaar voor doelactiviteiten: </p> <p> 
     <ul id="ul_436556860E6C4AEEB35411A02E78A199"> 
      <li id="li_5CC3B995D0AF4B658B3D6C3F6895AA41"> <p>Activiteiten die in <span class="keyword"> Adobe Mobile Services zijn gemaakt, worden </span> nu weergegeven in de <span class="keyword"> gebruikersinterface Target Standard/Premium </span> . (TGT-10806) </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </li> 
      <li id="li_684F9FC5CF414F4A892E6495352B5939"> <p>Wanneer het creëren van multivariate tests, kunt u meer dan 10 percenten van ervaringen van de test nu uitsluiten, op voorwaarde dat u de waarschuwing erkent dat u dan off-line rapportering voor analyse moet gebruiken. (TGT-21719) </p> <p>Zie Ervaringen voorvertonen voor een multivariate test voor meer informatie <a href="../c-activities/c-multivariate-testing/t-create-multivariate-test/preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> </a>. </p> </li> 
      <li id="li_B2FC7414C76848B39AD6EA20EE483F06"> <p>De campagne-id is nu zichtbaar op de overzichtspagina van elke activiteit. Dit is nuttig voor API en het oplossen van problemenverrichtingen. (TGT-20928) </p> </li> 
      <li id="li_5A9880AFE5FB46168D92255AA088B854"> <p>Het ontwerp voor de pagina's van het Logboek van de Aantekeningen en van de Verandering is verbeterd. </p> </li> 
      <li id="li_1489EA6C30C94B2AB394189E5FAFF6F6"> <p>De maximale toegestane lengte van anonieme aanbiedingsnamen in activiteiten van Automated Personalization (AP) is verhoogd van 30 tot 250 tekens. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Soorten publiek </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn nu beschikbaar voor het publiek: </p> <p> 
     <ul id="ul_F1D1F97266134D4ABE627CF2DCE2C6D4"> 
      <li id="li_99A611FCC1254D229D79B8FD075B952A"> <p> <span class="wintitle"> Marketingnaam voor apparaten </span> is nu als ingebouwde optie beschikbaar in de vervolgkeuzelijst wanneer u een publiek maakt dat zich richt op mobiele apparaten. </p> <p>Met deze wijziging kunt u eenvoudig de naam van een apparaatmodel kiezen in plaats van te zoeken naar het juiste modelnummer van het apparaat. De naam van het marketingapparaat van Galaxy S7 is bijvoorbeeld "Samsung Galaxy S7 Edge", terwijl het apparaatmodel "SM-G9350" is. (TGT-18393) </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobiel voor meer informatie </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen </p> </td> 
   <td colname="col2"> <p>De volgende verbeteringen zijn doorgevoerd in Aanbevelingen: </p> <p> 
     <ul id="ul_9D3644890C0C472D8B485DE9A52898B3"> 
      <li id="li_1E5662348F6E4ABDB2B74FE3326F2FD3"> <p>De resultaatregel voor Back-upalgoritme is nu opgenomen in de bovenste weergave en de bovenste downloadbestanden voor CSV-bestanden. De back-upaanbeveling begint met "*," </p> </li> 
      <li id="li_91DFD809378D4C20918F8F875747CE07"> <p>De extra statussen laten u de vooruitgang van uw voer van de Aanbeveling weten. </p> <p>Zie <a href="../c-recommendations/c-products/feeds.md#concept_1228B31E3D0B483B9DD42C5E2AE436E3" format="dita" scope="local"> Feeds </a>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhanced Visual Experience Composer (VEC) </p> </td> 
   <td colname="col2"> <p>Bijgewerkt de IP adressen voor Verbeterde Visual Experience Composer (VEC). </p> <p>Als u whitelist IP adressen die voor VEC worden gebruikt, voeg de nieuwe IP adressen toe. </p> <p>Voor meer informatie, zie het Oplossen van <a href="../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4" format="dita" scope="local"> problemen de Visuele Composer van de Ervaring </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Uitzettingen 2016 {#reference_607661929B504CCFAB3791B13C0DCDBE}

### Target Standard/Premium 16.10.2 (8 november 2016) {#section_2FDEFB3D56CC4BD7BC04DBEECFF6E942}

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij [!DNL Recommendations] geen feeds konden worden gemaakt voor niet-standaardomgevingen (hostgroepen).
* Verschillende verbeteringen zijn aangebracht om syntaxisfouten te reduceren.
* U kunt geen omleidingsvoorstellen meer maken voor activiteiten die [!DNL Analytics for Target] (A4T) gebruiken.

### Target Standard/Premium 16.10.1 (25 oktober 2016) {#section_F76F7329FCAC452FB88F8BE0BA727044}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_F8C01B2A9F07443490DB3025AC3AAC2A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Automatisch toewijzen: Winnerbadge </td> 
   <td colname="col2"> <p>We hebben het nu eenvoudiger gemaakt om een winnaar te bepalen in een Auto-Allocate A/B-activiteit. </p> <p>Veel marketeers maken de fout om voortijdig een winnende ervaring te declareren voordat de resultaten de duidelijke winnaar aangeven. </p> <p>Wanneer het gebruiken van de <span class="wintitle"> Geautomatiseerde eigenschap van de Toewijzing van het Verkeer, </span> <span class="keyword"> </span> toont het Doel een badge bij de bovenkant van de pagina die van de activiteit "Geen Winner nog"wijst tot de activiteit het minimumaantal omzettingen met voldoende vertrouwen bereikt. Wanneer een duidelijke winnaar wordt gedeclareerd, geeft <span class="keyword"> Doel de winnaar </span> weer: Beleef X." </p> <p>Voor meer informatie, zie de Geautomatiseerde Toewijzing van het Verkeer <a href="../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> en </a> bepaal een Winner <a href="../c-activities/automated-traffic-allocation/determine-winner.md#concept_5741A89ED7224E1285A3BC34B2CCD0F9" format="dita" scope="local"> </a>. </p> <p> <p>Opmerking:  Automatische toewijzing van A/B-activiteiten wordt niet meer ondersteund in Analytics for Target (A4T) forward. Met deze versie, zullen om het even welke actieve auto-Wijs A/B activiteiten met toegelaten A4T worden geschakeld naar <span class="wintitle"> Handmatige </span> wijze (gelijke verkeerstoewijzing). </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiele apparaten zoeken op drager </td> 
   <td colname="col2"> <p>Maak een publiek voor mobiele apparaten die zich op mobiele dragers richten (Verizon, Sprint, AT&amp;T, T-Mobile, enz.). De <span class="wintitle"> optie </span> Mobiele drager staat onder de <span class="wintitle"> Geo- </span> instellingen. </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670" format="dita" scope="local"> Geo </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> MboxTrace-verificatietoken genereren vanuit de gebruikersinterface van het doel </td> 
   <td colname="col2"> <p>Schakel geavanceerde <span class="keyword"> hulpprogramma's voor </span> foutopsporing van het doel in door een tijdelijk verificatietoken te maken. </p> <p>Klik op <span class="uicontrol"> Verificatietoken genereren </span> op de pagina <span class="wintitle"> Implementatiedetails </span> ( <span class="uicontrol"> Instellen </span> &gt; <span class="uicontrol"> Implementatie </span>). Vervolgens kunt u de resulterende parameter toevoegen aan de URL's van uw webpagina voor het oplossen van problemen. </p> <p>Voor meer informatie, zie "het Token van de Token van de Vergunning aan Gebruik met het Zuiveren Hulpmiddelen"in de Levering van de Inhoud van het <a href="../c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Oplossen van problemen terugwinnen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aanbevelingen: Criteria ingesteld op volgorde </td> 
   <td colname="col2"> <p>Gebruik in één ervaring maximaal vijf vooraf gedefinieerde criteria voor meer controle over de aanbevelingen die aan bezoekers worden voorgelegd. </p> <p>Zie <a href="../c-recommendations/c-algorithms/create-criteria-sequence.md#task_8A9CB465F28D44899F69F38AD27352FE" format="dita" scope="local"> Criteria-reeksen maken voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aanbevelingen: Externe aanbiedingen invoegen </td> 
   <td colname="col2"> <p>Voeg gepromoveerde objecten toe en controleer de plaatsing ervan in uw ontwerpen met aanbevelingen. </p> <p>Zie Promoties toevoegen voor meer informatie <a href="../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="firstlook"> <p><b>Eerste weergave</b> </p> Automatisch aanwijzen in A/B-activiteiten </td> 
   <td colname="col2"> <p> <p>Opmerking:  Dit "First Look"-aanbod is voor een paar klanten in deze release beschikbaar voor tests en feedback. </p> </p> <p>Automatisch ervaringen in A/B-tests als doel instellen voor de juiste ervaring voor de juiste bezoeker. </p> <p>Voor meer informatie, zie <a href="../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3" format="dita" scope="local"> auto-Doel voor Persoonlijke Ervaringen </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Wijzigingen in doelplatform (10 oktober 2016) {#section_0761AED70C3E44EA9D8546107B162CC1}

<table id="table_E3E52A4362724D05A8472DB5F51A2429"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> versie 0.9.3 </p> </td> 
   <td colname="col2"> <p>10 oktober 2016 </p> <p> <span class="codeph"> at.js </span> versie 0.9.3 is beschikbaar. </p> <p> 
     <ul id="ul_E4D300700390433E9EF8D5C9D3AA7669"> 
      <li id="li_E916EB3A77ED4CFF90CF6B4D30F188B1"> <p>Zorgt ervoor dat mbox in Microsoft Internet Explorer 11 vuur aanroept wanneer oudere browsers in de <span class="codeph"> at.js- </span> instellingen zijn uitgeschakeld. </p> </li> 
      <li id="li_1130509832CE429DB6DE636404CC54E1"> <p>Zorgt ervoor dat de standaardinhoud wordt teruggegeven als een dynamische verre aanbieding ontbreekt (bijvoorbeeld, als URL onjuist is en een fout 404 terugkeert). </p> </li> 
      <li id="li_21B5225D894B43CB863A775C937F66F4"> <p>Zorgt ervoor dat elementen snel worden onthuld wanneer VEC klik-volgende selecteurs niet in DOM kan worden gevonden. </p> </li> 
     </ul> </p> <p>Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (22 september 2016) {#section_3CD20678B6254DE1A9BD41FDD2255DDD}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_FED049F97C054CA895E0AEA3F2B180BF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Soorten publiek combineren </td> 
   <td colname="col2"> <p>Combineer meerdere soorten publiek (inclusief <span class="keyword"> Adobe Experience Cloud- </span> publiek en <span class="keyword"> </span> doelpubliek) tijdens de workflow voor het maken van activiteiten. </p> <p>Bijvoorbeeld, kunt u alle loyaliteitklanten richten door een specifiek segment van de Manager van de <span class="keyword"> Audience voor loyaliteitsstatus te omvatten en het te combineren met een </span> <span class="keyword"> </span> segment van het Doel dat uit mensen wordt samengesteld die zich voor uw loyaliteitsprogramma tijdens de huidige zitting, in plaats van het creëren van een derde, permanent publiek hebben aangemeld. </p> <p>Zie Meerdere soorten publiek <a href="../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> combineren voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Doelbezoekers gedurende een specifieke periode </td> 
   <td colname="col2"> <p>Begin- en einddatums toevoegen voor een publiek. </p> <p>Met het nieuwe gecombineerde, ad-hocpubliek dat hierboven is vermeld, kunt u bijvoorbeeld low-spenders met specifieke inhoud aanspreken gedurende de drie dagen voorafgaand aan de Zwarte Vrijdag en andere inhoud na Zwarte Vrijdag. </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdkader </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Slimme verzamelingen opslaan </td> 
   <td colname="col2"> <p>De zoekfunctionaliteit op de <span class="wintitle"> pagina </span> Inhoud bevat nu opgeslagen mappen, zogenaamde slimme verzamelingen, waarmee u tijd bespaart wanneer u vergelijkbare zoekopdrachten uitvoert. </p> <p>Zie Inhoud zoeken en Slimme verzamelingen maken voor meer informatie <a href="../c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Voeg een koppeling toe aan een afbeelding. De verbinding kan een klik-door verbinding, bestemmingsverbinding, of een landende verbinding zijn. </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer voor meer informatie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Deze release bevat de volgende verbeteringen:

| Verbetering | Beschrijving |
|---|---|
| Visual Experience Composer (VEC) | Verbeterd foutbericht. |

**Bekende problemen**

* De [!UICONTROL Render Using JavaScript] optie wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

### Wijzigingen in doelplatform (september 2016) {#section_1955146045A247D393DB824669A2A916}

<table id="table_8FDAEED5D84C4C718AB863BD6C383F20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> at.js </span> versie 0.9.2 </p> </td> 
   <td colname="col2"> <p>21 september 2016 </p> <p> <span class="codeph"> at.js </span> versie 0.9.2 is beschikbaar. </p> <p> 
     <ul id="ul_0778A9049C9D48A7B6CB4B79A95F0F4C"> 
      <li id="li_689FF306179F4EC3B391DEE3C53F4B1D"> <p>Er is een <span class="codeph"> optieEnabled- </span> instelling toegevoegd om de optie Weigering apparaatgrafiek in of uit te schakelen. Als deze instelling is ingesteld op <span class="codeph"> true </span> en de bezoeker de instelling niet meer heeft gevolgd, wordt er door de browser van de bezoeker geen mbox-aanroepen uitgevoerd. Apparaatgrafiek bevindt zich momenteel in bètaversie. Deze instelling is standaard ingesteld op <span class="codeph"> false </span> , maar moet zijn ingesteld op <span class="codeph"> true </span> als u Apparaatgrafiek gebruikt. Een vergelijkbare optie maakt deel uit van <span class="codeph"> mbox.js </span> v61. </p> </li> 
      <li id="li_663462C0680049F89CA8FE1853F31807"> <p>Extra ondersteuning voor <span class="codeph"> CustomEvent </span> voor het meldingsmechanisme. Eerder kon het meldingsmechanisme voor de <span class="codeph"> gebeurtenis at.js niet worden gebruikt via standaard DOM API's, zoals </span> document.addEventListener() <span class="codeph"> </span>. Nu kunt u <span class="codeph"> document.addEventListener() gebruiken </span> om een abonnement te nemen op <span class="codeph"> at.js- </span> gebeurtenissen, zoals aanvraaggebeurtenissen en gebeurtenissen voor het renderen van inhoud. </p> </li> 
      <li id="li_3FB2914F8D2F4AFFAA9B4622E8CA1EFF"> <p>Oplossing voor een probleem met betrekking tot aanbiedingen die zijn gemaakt in Visual Experience Composer (VEC). Vóór deze release heeft Target de kiezers verborgen en deze alleen niet verborgen wanneer alle kiezers overeenkomen. In <span class="codeph"> 0.js </span> 0.9.2 worden de kiezers niet verborgen zodra ze overeenkomen. </p> </li> 
     </ul> </p> <p>Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Target Standard/Premium 16.9.1 (22 september 2016) {#section_60ADF842E4A0424E8D2A81FB8B813A7A}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_896218AECE4C4EC691B76E79CC7DC356"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Soorten publiek combineren </td> 
   <td colname="col2"> <p>Combineer meerdere soorten publiek (inclusief <span class="keyword"> Adobe Experience Cloud- </span> publiek en <span class="keyword"> </span> doelpubliek) tijdens de workflow voor het maken van activiteiten. </p> <p>Bijvoorbeeld, kunt u alle loyaliteitklanten richten door een specifiek segment van de Manager van de <span class="keyword"> Audience voor loyaliteitsstatus te omvatten en het te combineren met een </span> <span class="keyword"> </span> segment van het Doel dat uit mensen wordt samengesteld die zich voor uw loyaliteitsprogramma tijdens de huidige zitting, in plaats van het creëren van een derde, permanent publiek hebben aangemeld. </p> <p>Zie Meerdere soorten publiek <a href="../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5" format="dita" scope="local"> combineren voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Doelbezoekers gedurende een specifieke periode </td> 
   <td colname="col2"> <p>Begin- en einddatums toevoegen voor een publiek. </p> <p>Met het nieuwe gecombineerde, ad-hocpubliek dat hierboven is vermeld, kunt u bijvoorbeeld low-spenders met specifieke inhoud aanspreken gedurende de drie dagen voorafgaand aan de Zwarte Vrijdag en andere inhoud na Zwarte Vrijdag. </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/time-frame.md#concept_0FE1E8DACD104F8B870B0BADE3197F0A" format="dita" scope="local"> Tijdkader </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Slimme verzamelingen opslaan </td> 
   <td colname="col2"> <p>De zoekfunctionaliteit op de <span class="wintitle"> pagina </span> Inhoud bevat nu opgeslagen mappen, zogenaamde slimme verzamelingen, waarmee u tijd bespaart wanneer u vergelijkbare zoekopdrachten uitvoert. </p> <p>Zie Inhoud zoeken en Slimme verzamelingen maken voor meer informatie <a href="../c-experiences/c-manage-content/filter-and-search-content.md#concept_3B59B8F025BF4CEA82ECC5199D365276" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Form-based Experience Composer </td> 
   <td colname="col2"> <p>Voeg een koppeling toe aan een afbeelding. De verbinding kan een klik-door verbinding, bestemmingsverbinding, of een landende verbinding zijn. </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer voor meer informatie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Deze release bevat de volgende verbeteringen:

| Verbetering | Beschrijving |
|---|---|
| Visual Experience Composer (VEC) | Verbeterd foutbericht. |

**Bekende problemen**

* De [!UICONTROL Render Using JavaScript] optie wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

### Wijzigingen in doelplatform (augustus 2016) {#section_8D8BA8C628E747338C84564EC34CE0FD}

<table id="table_0035B0D7ECD444C68B1B6CB0F150C55E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js, </span> versie 61 </p> </td> 
   <td colname="col2"> <p>23 augustus 2016 </p> <p> <span class="filepath"> mbox.js, </span> versie 61, bevat de volgende wijzigingen in de release van augustus: </p> <p> 
     <ul id="ul_DC4E5AB3B48A4D2D9B08B6CDA5DFE8FB"> 
      <li id="li_B52F3AE60D324C2A8FAD03C1495F26D7"> <p> <span class="filepath"> mbox.js </span> versie 61 is nu de standaarddownload in de <span class="keyword"> Standaard/Premium- </span> en Klassieke <span class="keyword"> </span> gebruikersinterfaces van het Doel. </p> </li> 
      <li id="li_41C2D2E552BF4F8E8A4375AF368F7728"> <p>Er is een <span class="codeph"> optieEnabled- </span> instelling toegevoegd ter ondersteuning van toekomstige Adobe Experience Cloud-uitschakelfunctionaliteit. De standaardwaarde is false. Als dit bezit wordt toegelaten, voeren alle verzoeken asynchroon tegen het <span class="filepath"> /ajax </span> eindpunt, enkel als versie 60 uit. </p> </li> 
     </ul> </p> <p>Voor meer informatie over alle veranderingen in <span class="filepath"> mbox.js </span> versie 61, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> mbox.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe Target Standard/Premium 16.8.1 (23 augustus 2016) {#section_A8854D4EDF014AEBB81F49EB104D4A20}

Adobe Target Standard/Premium 16.8.1 (23 augustus 2016) bevat de volgende functies en verbeteringen:

<table id="table_AE048CB9EA1C4C7BBC2E9D90D26F7395"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Hosts en omgevingsbeheer (hostgroep) </p> </td> 
   <td colname="col2"> <p>Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage. </p> <p>Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. De vooraf ingestelde omgevingen zijn onder andere Productie, Staging en Ontwikkeling. U kunt ook nieuwe omgevingen toevoegen. </p> <p>Deze eigenschap bereikt eigenschappariteit met <span class="keyword"> Doel Klassiek </span>. </p> <p>Zie <a href="../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E" format="dita" scope="local"> Gastheren voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Categorie-affiniteit </p> </td> 
   <td colname="col2"> <p>Met de functie voor affiniteit van categorieën worden automatisch de categorieën vastgelegd die een gebruiker bezoekt en wordt de affiniteit van de gebruiker voor de categorie berekend, zodat deze kan worden geactiveerd en gesegmenteerd. Dit helpt ervoor te zorgen dat de inhoud gericht is op bezoekers die het meest waarschijnlijk op die informatie handelen. </p> <p>Deze eigenschap bereikt eigenschappariteit met <span class="keyword"> Doel Klassiek </span>. </p> <p>Zie <a href="../c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC" format="dita" scope="local"> Categorie-affiniteit voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enhanced Experience Composer inschakelen/uitschakelen op activiteitsniveau </p> </td> 
   <td colname="col2"> <p>Schakel de <span class="wintitle"> Enhanced Experience Composer </span> in of uit op accountniveau (van toepassing op alle activiteiten die in de account zijn gemaakt) of op het niveau van de individuele activiteit. </p> <p>Eerder kon u de Enhanced Experience Composer alleen op accountniveau in- en uitschakelen. </p> <p>Zie <a href="../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Ervaringen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automatische personalisatie: prestatierapport van de aanbieding </p> </td> 
   <td colname="col2"> <p>Download een prestatierapport voor de aanbieding met alle maatstaven voor succes van de geautomatiseerde personaliseringsactiviteit. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Deze release bevat de volgende verbeteringen:

<table id="table_E2E4BE72BD79413A821C6A6D1A3AB0F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Gebruikersinterface van code-editor opnieuw ontwerpen </p> </td> 
   <td colname="col2"> <p>De interface van de code-editor is bijgewerkt zodat deze intuïtiever en gebruiksvriendelijker wordt. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code-editor </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De volgende bekende problemen zijn gemeld:

* Enkele UI-tekst voor de [!UICONTROL Category Affinity] functie wordt alleen in het Engels weergegeven. Tekst in andere talen is beschikbaar in de [!DNL Target] release van september.

### Wijzigingen in doelplatform (juli 2016) {#section_09C18773707B4059852A41C764F817E4}

<table id="table_33B60910EAE24BAFA778F280F72FB683"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Wijzigen </th> 
   <th colname="col2" class="entry"> Details </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> at.js </span> versie 0.9.1 </p> </td> 
   <td colname="col2"> <p>14 juli 2016 </p> <p> <span class="filepath"> at.js </span> versie 0.9.1 is nu beschikbaar. </p> <p>Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> bij.js de Details van de Versie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> mbox.js, </span> versie 61 </p> </td> 
   <td colname="col2"> <p>28 juli 2016 </p> <p> <span class="codeph"> mbox.js </span> versie 61 kan nu worden gedownload. Versie 61 is momenteel niet de standaarddownload. </p> <p>Voor meer informatie, zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A" format="dita" scope="local"> mbox.js de Details van de Versie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe Target Standard/Premium 16.7.1 (21 juli 2016) {#section_DB583EF9A30247A488EE319583911F22}

Adobe Target Standard/Premium 16.7.1 (21 juli 2016) bevat de volgende functies en verbeteringen:

<table id="table_EBA34BD2F5C745DD9EC5231AD79F6C00"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Prioriteitsinstellingen voor activiteiten </td> 
   <td colname="col2"> <p>U kunt activiteit prioritaire niveaus van 0-999 nu plaatsen om voor fijnere controle toe te staan over welke activiteitenvertoningen als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. </p> <p>Deze optie moet zijn ingeschakeld in <span class="wintitle"> Instellen </span> &gt; <span class="wintitle"> Voorkeuren </span> . </p> <p>De optie Fine-grained priority is van toepassing op A/B Test-, Automated Personalization-, Experience Targeting- en Multivariate Test-activiteiten. </p> <p>Raadpleeg de volgende onderwerpen voor meer informatie: </p> <p> 
     <ul id="ul_FD92CD06CF25480887AC171274262E18"> 
      <li id="li_D321FAED82944D2685DA69EB310D80BE"><b>A/B-test: </b> <a href="../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </li> 
      <li id="li_12ECDFD71DB94E22A85AB13B487E8503"><b>Automatische personalisatie: </b> <a href="../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Geautomatiseerde personalisatie </a> </li> 
      <li id="li_84B893C214994246AB36E28E84C51460"><b>Gericht op ervaring: </b> <a href="../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </li> 
      <li id="li_26533B659C0E49D6A6D3B3FEBE9CA930"><b>Multivariatietest: </b> <a href="../c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC" format="dita" scope="local"> Doelstellingen en instellingen </a> </li> 
      <li id="li_FBACF2B73B2E491BBB85618153AC4568"><b>Activiteiten: </b> <a href="../c-activities/activity-settings.md#task_C6B2FF8374724933BE79A83549B9CD02" format="dita" scope="local"> Activiteiteninstellingen </a> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Kenmerken van multigetaxeerde aanbevelingen </td> 
   <td colname="col2"> <p>Alle aangepaste <span class="keyword"> Aanbevelingen- </span> kenmerken kunnen nu meerdere entiteitswaarden bevatten. </p> <p>Zie Kenmerken aangepaste entiteit voor meer informatie <a href="../c-recommendations/c-products/custom-entity-attributes.md#concept_E5CF39BCAC8140309A73828706288322" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ondersteuning voor dynamische/externe aanbiedingen </td> 
   <td colname="col2"> <p>Dynamische inhoud kan onderdeel zijn van elke op formulieren gebaseerde activiteit in <span class="keyword"> Target Standard/Premium </span>. Dynamische inhoud wordt buiten <span class="keyword"> Doel opgeslagen </span>. </p> <p>Zie Externe aanbiedingen <a href="../c-experiences/c-manage-content/about-remote-offers.md#concept_657016A0E6174C22B89036E9C8A0170F" format="dita" scope="local"> maken voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Soorten publiek en profielscripts kopiëren </td> 
   <td colname="col2"> <p>U kunt nu een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken. </p> <p>Voor meer informatie, zie het <a href="../c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Creëren van een Publiek </a>. </p> <p>U kunt ook bestaande profielscripts kopiëren. </p> <p>Zie <a href="../c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2" format="dita" scope="local"> Profielscriptkenmerken voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Klassen gebruiken om elementkiezers te bepalen </td> 
   <td colname="col2"> <p>De selecteurs van het element kunnen nu op klassen of IDs in Geautomatiseerde Personalisatie en Multivariate de activiteiten van de Test worden gebaseerd. In vorige versies was deze optie alleen beschikbaar voor A/B-testactiviteiten. </p> <p>Voor meer informatie, zie de Kiezers van het Element die in Visual Experience Composer worden gebruikt <a href="../c-experiences/c-visual-experience-composer/vec-selectors.md#concept_4EB7663E255F439B8D24079D23479337" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aanbevelingen: Overeenkomende inhoud </td> 
   <td colname="col2"> <p> Gebruik de regels voor gelijkenis met inhoud om aanbevelingen te doen op basis van item- of mediakenmerken. </p> </td> 
  </tr> 
 </tbody> 
</table>

<table id="table_699755B33F8F48ECABB6FC7E78289A79"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Verbetering </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Rapportageverbeteringen </p> </td> 
   <td colname="col2"> <p>De metrische het rapportdownloads van het succes tonen nu metrische en segmentnamen in plaats van IDs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Evalueer mbox ingangsvoorwaarde op elk verzoek in de Geautomatiseerde activiteiten van de Personalisatie </td> 
   <td colname="col2"> <p>In de Geautomatiseerde activiteiten van de Personalisatie, worden de ingencriteria (URL die, malplaatjeregels, publieksdoel richten) geëvalueerd voor elk verzoek voor nauwkeurigere aanbiedingslevering. </p> <p>Voor meer informatie, zie <a href="../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Geautomatiseerde Personalisatie </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe Target Standard/Premium 16.6.1 (16 juni 2016) {#section_C1E9F43111BF4160AF31482CD53E00BD}

Er is geen klant-onder ogen ziende versie gepland voor Juni.

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij sommige klanten een wit scherm zagen toen ze probeerden hun pagina in de Visual Experience Composer te bewerken.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Probleem met voorbeeld-URL&#39;s voor ervaringen met omleiding. Als tussenoplossing klikt u in de composer voor ervaring op **[!UICONTROL Configure]**, kiest u **[!UICONTROL Multiple Audiences]** en voegt u toe **[!UICONTROL All visitors]** als het enige publiek. Sla je activiteit verder op. Dit verandert niets aan de levering van uw activiteit, maar staat voorproef toe om te werken. Dit wordt opgelost in de release van juli van Adobe Target.

* De documentatie toont het verwachte gedrag voor Redirect URL checkbox. Vanwege een bug wordt het selectievakje echter niet standaard ingeschakeld weergegeven. Dit gebrek zal spoedig worden opgelost.

   Als u deze optie wilt controleren in een bestaande activiteit met een omleidingsvoorstel, gebruikt u de volgende tijdelijke oplossing:

   1. Open het pop-upvenster Omleiden naar URL.
   1. Wijzig de URL in een dummy-URL en sla deze op.
   1. Wijzig de dummy-URL opnieuw in de verwachte omleiding van de campagne-URL.
   1. Schakel de optie Inclusief huidige queryparameters in en sla deze op.
   Als u de optie controleert terwijl het creëren van een nieuwe omleidingsaanbieding, kunt u uw vraagparameters verwachten om in redirection worden omvat.

   Voor oudere activiteiten, als deze optie in ervaringscomposer van uw activiteit wordt gecontroleerd, betekent het uw redirection de vraagparameters zal omvatten. Als het niet wordt gecontroleerd, zullen de huidige vraagparameters niet in redirection worden omvat.

### Adobe Target Standard/Premium 16.5.1 (19 mei 2016) {#section_406CE09317994F55A26C2FDB77C77FEA}

Adobe Target Standard/Premium 16.5.1 (19 mei 2016) bevat de volgende functies en verbeteringen:

<table id="table_DDC5356FD6B8443EAA6EB81C03ADF73A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Ervaar versies </td> 
   <td colname="col2"> <p>Versies die gericht zijn op verschillende doelgroepen kunnen nu worden opgezet binnen de ervaringen in A/B-activiteiten. </p> <p>Zie <a href="../c-activities/t-test-ab/t-test-create-ab/target-experience-to-multiple-audiences.md#task_0138112E283A4A5B9F8AB9AAF2FBC2FF" format="dita" scope="local"> Een ervaring toewijzen aan meerdere soorten publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> URL's voor kwaliteitscontrole/voorvertoning </td> 
   <td colname="col2"> <p>Voorbeeld-URL's zijn nu beschikbaar voor de op formulieren gebaseerde ervaringscomposer. </p> <p>Zie Ervaring-URL' <a href="../c-activities/t-automated-personalization/experience-preview.md#task_586C6655A6FD4AF08F5678FC3F481EFC" format="dita" scope="local"> s weergeven </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aangepaste algoritmen voor aanbevelingen </td> 
   <td colname="col2"> <p>Aangepaste algoritme-toewijzingen kunnen worden geüpload in een CSV-bestand. Het is niet meer nodig om de op XML gebaseerde API te gebruiken. </p> <p>Zie Aangepaste criteria <a href="../c-recommendations/c-algorithms/recommendations-csv.md#task_1BBA49883E794670A09F0ABE1B3F4288" format="dita" scope="local"> uploaden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Analyses voor doel: Analysescherm </td> 
   <td colname="col2"> <p>Voor een correcte rapportering moet u een volgserver opgeven wanneer u activiteiten maakt of bewerkt die Analytics for Target (A4T) gebruiken. Bestaande activiteiten worden uitgevoerd met de huidige instellingen. </p> <p>Zie <a href="../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823" format="dita" scope="local"> Een Analytics Tracking Server gebruiken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe instructievideo's </td> 
   <td colname="col2"> <p>De volgende instructievideo's zijn toegevoegd aan de Help: </p> <p> 
     <ul id="ul_47BAE946E764404497B7D81EE4C5D076"> 
      <li id="li_E16E50F94D3748E2985FB78F75140626">DTM gebruiken om parameters aan globale mbox over te gaan </li> 
      <li id="li_A8CCDE3EFF25430580E6C372000CF964">DTM gebruiken om Target te implementeren </li> 
      <li id="li_8897F7B5930B448D87274CEDFCC75AE4">Een multivariatietest instellen </li> 
      <li id="li_2573DF52CE974ED0AF9EA433C97BC4C0">Een A/B-activiteit maken </li> 
      <li id="li_52F28040D54D43E787B763E6AA998614">Werken met activiteitstypen </li> 
      <li id="li_577C8DDEB4CE429CA3C14BE5655F6E11">Instellingen voor activiteit configureren </li> 
      <li id="li_2F7FCA657FD04E02ADD6E6964A8EA1F0">Een activiteit als doel instellen </li> 
      <li id="li_A08B8AFF48764D1B9EA706977F72AA66">Soorten publiek maken </li> 
      <li id="li_493CDC3BEA5F4EA0821B971579177E03">Soorten publiek gebruiken </li> 
      <li id="li_19045C86E1524649B56F82416934EF13">De inhoudsbibliotheek gebruiken </li> 
      <li id="li_8E89F3691A6F4400A2DFDFE5186DFA83">Profielscripts gebruiken </li> 
      <li id="li_2EBB2B61BFA24F5FB858C0551AB20F70">Accountvoorkeuren instellen </li> 
      <li id="li_E1886818C7BF4F36B07EC293F1A45911">De modus Visual Experience Composer </li> 
      <li id="li_F74D2BA5ACD04595B658955A489602E5">Mbox.js configureren en implementeren </li> 
      <li id="li_A87B876298344B2987BDC5FFD5580EC0">Doelgebruikers maken en beheren </li> 
      <li id="li_F90E1083444E4DBAA8C406AC293C0FD6">Metingen voor succes instellen </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbeteringen in de gebruikersinterface </td> 
   <td colname="col2"> <p>De de interfaceverbeteringen van de gebruiker zijn aangebracht aan het Visueel Composer van de Ervaring en onderzoek van Aanbevelingen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> CSV-download met aanbevelingen </td> 
   <td colname="col2"> <p>CSV-downloads hebben nu een regel voor alle omgevingen, inclusief omgevingen die geen aanbevelingen voor entiteiten hebben (bijvoorbeeld: 
     <code>
       # environment: 1724 
     </code>). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbeteringen**

Verbeteringen om het A4T-inrichtingsproces te verbeteren.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Probleem met voorbeeld-URL&#39;s voor ervaringen met omleiding. Als tussenoplossing klikt u in de composer voor ervaring op **[!UICONTROL Configure]**, kiest u **[!UICONTROL Multiple Audiences]** en voegt u toe **[!UICONTROL All visitors]** als het enige publiek. Sla je activiteit verder op. Dit verandert niets aan de levering van uw activiteit, maar staat voorproef toe om te werken. Dit wordt opgelost in de release van juli van Adobe Target.

### Nieuwe doeluitvoeringsbibliotheek, 0.js 0.8.0 (5 mei 2016) {#section_6A44C277E82D409AB6DCD0901F43794A}

at.js is een nieuwe implementatiebibliotheek voor Doel die voor zowel typische implementaties van het Web als enig-paginatoepassingen wordt ontworpen.

at.js vervangt mbox.js voor de implementaties van het Doel van Adobe.

>[!NOTE]
>
>Hoewel mbox.js door at.js wordt vervangen, blijft mbox.js ondersteund. Voor de meeste mensen biedt at.js voordelen ten opzichte van mbox.js. Dit geeft u tijd om te testen om.js en de implementatie op uw pagina&#39;s te veranderen.

Onder andere voordelen, verbetert at.js de tijden van de paginalading voor de implementaties van het Web, verbetert veiligheid, en verstrekt betere implementatieopties voor single-page toepassingen.

at.js bevat de componenten die in target.js inbegrepen waren, zodat is er niet meer een vraag aan target.js.

Houd rekening met het volgende wanneer u at.js implementeert:

* Omleiding van composer voor visuele ervaring werkt niet.
* Internet Explorer-versies ouder dan 8 worden niet ondersteund.
* Asynchrone implementatie betekent dat verouderde integratie, zoals de insteekmodule Testen en Doel naar SiteCatalyst, mogelijk niet werkt.
* Doelplug-ins die verwijzen naar objecten en methoden mbox.js, worden niet ondersteund.
* Alle aanroepen naar Target worden uitgevoerd via XMLHTTPRequest en de inhoud wordt geretourneerd via JSON.

### Doelplatformen wijzigen {#section_8295A808A4CE405C9DA2893E7935238E}

* [Mbox.js versie 60](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md#section_3BDAB885FA13444A8D35940A4BFF5825) is nu de standaarddownload.
* Mbox.js-versies ouder dan 50 worden niet meer actief getest. Als uw implementatie nog niet wordt bijgewerkt, zorg ervoor extra QA op al levering van de Inhoud van het Doel en rapporteringsinzameling wordt uitgevoerd.
* Flash-campagnes en andere Flash-gerelateerde items zijn uit Target verwijderd.
* Internet Explorer 10 wordt niet meer ondersteund in de doelinterface.
* De ondersteuning voor de levering van inhoud in Internet Explorer 8, 9 en 10 zal naar verwachting in een komende release eindigen.

   Het actieve testen zal in een toekomstige versie voor deze browsers worden stopgezet, na het eind van actieve steun voor deze browsers door Microsoft. Het doel zal inhoud aan deze browsers blijven leveren, maar u zou inhoudslevering en gegevensinzameling voor rapporten moeten testen.

### Adobe Target Standard/Premium 16.4.1 Fix (5 mei 2016) {#section_70552F61E83140C7B4D2A245198B630E}

* at.js v 0.8.0 is nu beschikbaar voor download van de interface van het Doel.
* Doel-API&#39;s gewijzigd. `applyOffer` nu vereist `mbox param [0]`.

   ```
   adobe.target.applyOffer({ 
       "mbox": "target-global-mbox", 
    "params": {"test": "true"}, 
       "selector": ".banner-text", 
       "offer": offer 
   });
   ```

### Adobe Target Standard/Premium 16.4.1 (21 april 2016) {#section_C968860FAB81485BA12BD588F4ECA401}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_162CC5A0DB324B38A8A4252A18976686"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Verbeteringen gebruikersinterface </td> 
   <td colname="col2"> <p>De gebruikersinterface is aanzienlijk gewijzigd in deze release. De belangrijkste wijzigingen zijn: </p> <p> 
     <ul id="ul_28F382C60ADE43F5A3A4BD0CD5A5CE52"> 
      <li id="li_C47240826E5844D6843314F453F042FC">Navigatie is van links naar boven verplaatst </li> 
      <li id="li_3BB03504E98C40CC85583DCD9A4CEA06">Verbeterde dialoogvensters </li> 
      <li id="li_AE71506DF1E748A788C40E1F09951732">Verbeterde stroom voor het maken van activiteiten </li> 
     </ul> </p> <p>De manier waarop u de cloudoplossingen van de Ervaring, inclusief Target, selecteert, is ook gewijzigd. Klik op het menupictogram om toegang te krijgen tot Experience Cloud-oplossingen en -services: </p> <p> <img src="assets/menu-shell-400.png" id="image_6E9323E0EBEA41B1A7319D6BCC43E769" width="400" height="140" /> </p> <p>Zie <a href="../c-intro/target-access-from-mac.md#task_5467C72DAFCB4BB583762CAAFC00A5CF" format="dita" scope="local"> Toegangsdoel in de Adobe Experience Cloud voor meer informatie over het benaderen van Target en het instellen van de standaardpagina Target nadat u zich hebt aangemeld bij de Experience Cloud </a>. </p> <p>Voor meer informatie over de verbeteringen van de gebruikersinterface raadpleegt u <a href="https://docs.adobe.com/content/help/en/core-services/interface/release-notes/marketing-cloud-interface.html" format="https" scope="external"> Nieuw in de Adobe Experience Cloud - Voorjaar 2016 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Opnameregels kunnen worden uitgeschakeld voor aanbevelingen voor back-ups </td> 
   <td colname="col2"> <p>Wanneer de reserveaanbevelingen worden toegelaten, kunt u verkiezen om integratieregels op uw reserveaanbevelingen niet toe te passen. . </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aanbevelingen: Nieuwe mogelijkheden voor foutopsporing in tekstgebied via <span class="codeph"> mboxTrace </span> </td> 
   <td colname="col2"> <p>Als u <span class="codeph"> &amp;mboxTrace toevoegt </span> aan een URL, worden aanbevelingen op die pagina vervangen door foutopsporingsgegevens, waaronder informatie over aanbevolen aanbevelingen, criteria, ontwerp, uitsluitingen, opgenomen gegevens, aanbevolen back-upinstructies en meer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aanbevelingen-API: Een CSV uploaden voor de aangepaste criteria </td> 
   <td colname="col2"> <p>U kunt een CSV voor de Aangepaste Criteria via API uploaden. </p> <p>Deze mogelijkheid wordt in een komende release toegevoegd aan de gebruikersinterface van Target Premium. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Aanbevelingen-API: Nieuwe ontwerp-API's </td> 
   <td colname="col2"> <p>Met de nieuwe ontwerp-API's kunt u uw Aanbevelingsontwerpen beheren via de API. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Metrische gegevens voor afhankelijk succes </td> 
   <td colname="col2"> De geautomatiseerde Personalisering steunt nu de capaciteit om succesmetrisch te beperken tot slechts telling als vorige succes metrisch reeds is voldaan. <p>Zie Metriek <a href="../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> succes voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> AP: Rapporten overzicht downloaden </td> 
   <td colname="col2"> De downloadoptie staat nu gebruikers toe om summiere mening (d.w.z. het vergelijken van Controle en Geautomatiseerd verkeer) te downloaden zoals die door alle beschikbare succesmetriek wordt verdeeld. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Kenmerken van klanten kunnen als tokens worden gebruikt in aanbiedingen </td> 
   <td colname="col2"> <p>Voorheen kon in profielscripts naar klantkenmerken worden verwezen, opgemaakt als <span class="codeph"> crs.get('&lt; Naam gegevensbron <span class="varname"> &gt; </span>&gt;.&lt; <span class="varname"> Kenmerknaam </span>&gt;') </span>. </p> <p>De kenmerken zijn nu beschikbaar als tokens in profielscripts en rechtstreeks in aanbiedingen zonder eerst een profielscript te hoeven schrijven. De token moet de volgende vorm hebben: <span class="codeph"> $crs. <span class="varname"> datasourceName </span>. <span class="varname"> attributeName </span> </span>. </p> <p>Zie <a href="../c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_62B4821EB6564FF4A14159A837AD4EDB" format="dita" scope="local"> CRS Tokens </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering aangepaste code </td> 
   <td colname="col2"> De aangepaste code kan nu de JavaScript-code in de <span class="codeph"> &lt;head&gt;- </span> tag uitvoeren. Uitvoering van code wacht niet langer tot de tag <span class="codeph"> &lt;body&gt; </span> in DOM aanwezig is. Eerder was de kiezer alleen het eerste element in de <span class="codeph"> &lt;body&gt;- </span> tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe instructievideo's </td> 
   <td colname="col2"> Instructievideo's zijn toegevoegd aan de Help. Momenteel, kunt u video's over de Composer van de Ervaring van <a href="../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Visuele en op vorm-Gebaseerde Composer van de Ervaring bekijken </a>. De komende weken worden meer video's toegevoegd. </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* De kwestie die door Chrome versie 48 wordt geïntroduceerd die Visual Experience Composer ertoe bracht om verkeerd in Chrome te functioneren is opgelost. Werk een update naar Chrome versie 50 uit om van deze correctie te profiteren.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.

### Adobe Target Standard/Premium 16.3.1 (15 maart 2016) {#section_A5A9B03A5CCD4213AD656BE722B5FF67}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_F2A89DF1EAB443B4B4C7E0BC6118384B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Eerste weergave: </p> <p>Nieuwe doelimplementatiebibliotheek, at.js </p> </td> 
   <td colname="col2"> <p> <p>Opmerking:  Dit "First Look"-aanbod is beschikbaar via API-download. Het zal via de interface van het Doel in een aanstaande versie beschikbaar zijn. In de tussentijd kunt u de bibliotheek at.js downloaden, deze in uw omgeving testen en deze implementeren in de implementatie van het productiedoel. </p> </p> <p> at.js is een nieuwe implementatiebibliotheek voor Doel die voor zowel typische implementaties van het Web als enig-paginatoepassingen wordt ontworpen. </p> <p> at.js vervangt mbox.js voor de implementaties van het Doel van Adobe. </p> <p> <p>Opmerking:  Hoewel at.js mbox.js vervangt, zal mbox.js worden gesteund, hoewel, voor de meeste mensen, at.js voordelen boven mbox.js verstrekt. Dit geeft u tijd om te testen om.js en de implementatie op uw pagina's te veranderen. </p> </p> <p>Onder andere voordelen, verbetert at.js de tijden van de paginalading voor de implementaties van het Web, verbetert veiligheid, en verstrekt betere implementatieopties voor single-page toepassingen. </p> <p>at.js bevat de componenten die in target.js inbegrepen waren, zodat is er niet meer een vraag aan target.js. </p> <p>Houd rekening met het volgende wanneer u at.js implementeert: </p> <p> 
     <ul id="ul_8C50C669AA7B4464A5FDECFCFD8662ED"> 
      <li id="li_6065B208480D46178055B40A2654E0C6">Omleiding van composer voor visuele ervaring werkt niet. </li> 
      <li id="li_A2FABD3C21994511A45DED84283E526E">Internet Explorer-versies ouder dan 8 worden niet ondersteund. </li> 
      <li id="li_04499B391F784B89B09A1D6329B1C790">Asynchrone implementatie betekent dat verouderde integratie, zoals de insteekmodule Testen en Doel naar SiteCatalyst, mogelijk niet werkt. </li> 
      <li id="li_D3C00EF206154038A54F53CA40B34DC3"> Doelplug-ins die verwijzen naar objecten en methoden mbox.js, worden niet ondersteund. </li> 
     </ul> </p> <p>Zie <a href="../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17" format="dita" scope="local"> at.js Implementation </a> voor documentatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Metrische gegevens voor afhankelijk succes </td> 
   <td colname="col2"> <p>Deze eigenschappen verstrekken de optie per succes metrisch om iemand te tellen zoals het bereiken van metrisch succes slechts als zij eerder een verschillend succes metrisch hebben bereikt. </p> <p> Een test kan bijvoorbeeld de hoofdafbeelding op de startpagina veranderen. De markeerteken wil mogelijk alleen conversies tellen voor mensen die op de hoofdafbeelding hebben geklikt. De markator kan dus een succesmaatstaf instellen voor "geklikt op een homepage held" en een andere maatstaf voor aankoop. Vervolgens kan de markeerteken een regel toevoegen op de metrische waarde voor "kopen" om ervoor te zorgen dat bezoekers eerst de succesmaatstaf "geklikt op de held van de homepage" hebben bereikt. </p> <p> <p>Opmerking:  Als het publiek dat zich op een plaats in succes metrisch richt wordt geplaatst, wordt deze eigenschap niet gesteund voor die metrisch. </p> </p> <p> De afhankelijke Metriek van het Succes wordt slechts gesteund in AB, XT, en activiteiten MVT. Ondersteuning voor automatische personalisatie en aanbevelingen is later beschikbaar. </p> <p>Zie Metriek <a href="../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> succes voor meer informatie </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbeteringen in de bruikbaarheid automatisch toewijzen </td> 
   <td colname="col2"> <p>Nadat het model voor een auto-Wijs activiteit klaar is, worden de volgende verrichtingen van UI niet toegestaan: </p> <p> 
     <ul id="ul_52B790B2B0D746769A3471E09CE1A122"> 
      <li id="li_B9F0FFF019CE4CB697F5D0B60061DC27">De modus "Verkeerstoewijzing" omzetten in "Handmatig" </li> 
      <li id="li_C271B0BE4C5C4B06BB21703239E7B061">De rapportbron wijzigen van "Adobe Target" in "Analytics" en andersom </li> 
      <li id="li_E023DDA7ED9142B58D54F42904ADC994">Het metrische type van het doel wijzigen </li> 
      <li id="li_619F4765CEEC48E0A45E1821C282A082">Opties wijzigen in het deelvenster Geavanceerde instellingen </li> 
     </ul> </p> <p>Raadpleeg <a href="../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Automatische verkeerstoewijzing </a> voor documentatie over Automatisch toewijzen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Sommige interfaceproblemen kunnen zich voordoen in Internet Explorer 10, inclusief schermflikkering en mogelijke vertraging.
* De update van Chrome versie 48 introduceerde een kwestie die de Visuele Composer van de Ervaring veroorzaakt om verkeerd in Chrome te functioneren. Google werkt aan een oplossing. Raadpleeg voor meer informatie [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). U kunt dit probleem als volgt oplossen:

   * Gebruik Firefox of Internet Explorer.
   * Schakel de Enhanced Experience Composer in, die kan worden geconfigureerd via het tabblad **[!UICONTROL Setup]** > **[!UICONTROL Preferences]** .

### Adobe Target Standard/Premium 16.2.1 (18 februari 2016) {#section_47E5CEE2EED24CB3B71D7457673F3200}

Deze release bevat de volgende functies en verbeteringen:

| Functie | Beschrijving |
|---|---|
| Doelstelling activiteit volgens percentage. | U kunt vermeldingen in [A/B](../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72) en [multivariate](../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710) activiteiten nu beperken tot een percentage bezoekers of publieksleden. U kunt bijvoorbeeld items beperken tot 50% van alle bezoekers of 45% van uw &quot;Californische&quot; publiek. |
| Ondersteuning voor inkomsten, bestellingen en betrokkenheid bij automatisch toewijzen | U kunt nu de metriek van de Inkomsten (RPV), van Orden, en van de Betrokkenheid als doelstellingen voor A/B activiteiten kiezen met auto-Toewijzing geselecteerd. Eerder werden alleen conversiemetriek ondersteund. Zie [Geautomatiseerde verkeerstoewijzing](../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4). |
| Filteren op bron | U kunt de lijst Activiteiten nu filteren op de bron waar de activiteit is gemaakt. U kunt kiezen uit Adobe Target en Adobe Experience Manager. Zie [Activiteiten](../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). |
| Verbeteringen voor geautomatiseerde personalisatieprestaties | Automated Personalization is herontworpen om beter te presteren met een groot aantal aanbod-/locatiecombinaties. |

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is geselecteerd voor pagina A in een activiteit met meerdere pagina&#39;s, wordt JavaScript overal uitgeschakeld, ook al is JavaScript uitschakelen niet geselecteerd voor andere pagina&#39;s.
* Sommige interfaceproblemen kunnen zich voordoen in Internet Explorer 10, inclusief schermflikkering en mogelijke vertraging.
* De update van Chrome versie 48 introduceerde een kwestie die de Visuele Composer van de Ervaring veroorzaakt om verkeerd in Chrome te functioneren. Google werkt aan een oplossing. Raadpleeg voor meer informatie [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). U kunt dit probleem als volgt oplossen:

   * Gebruik Firefox of Internet Explorer.
   * Schakel de Enhanced Experience Composer in, die kan worden geconfigureerd via het tabblad **[!UICONTROL Setup]** > **[!UICONTROL Preferences]** .

### Adobe Target Standard/Premium 16.1.1 (28 januari 2016) {#section_8BF7705B452C449F961AEFC568A0778C}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_8525ECC9B6D0435ABEF8C27F747B7A0C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Verbeteringen in de gebruikersinterface. </td> 
   <td colname="col2"> <p>De lijst met activiteiten en het ontwerp van de lijst met doelgroepen zijn verbeterd, net als de functie voor zoeken en sorteren. De extra veranderingen van het gebruikersinterface zullen in volgende versies worden omvat. </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> "Superpubliek" </td> 
   <td colname="col2"> <p>Gebruik geneste AND/OR-logica bij het configureren van soorten publiek. </p> <p>Zie <a href="../c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558" format="dita" scope="local"> Een publiek maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hostgroepen selecteren in rapporten </td> 
   <td colname="col2"> <p>De groepen van de gastheer zijn beschikbaar in rapporten. </p> <p> <p>Opmerking:  Deze optie is niet beschikbaar voor Automated Personalization. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ondersteuning voor Internet Explorer 11 </td> 
   <td colname="col2"> <p>Internet Explorer 11 wordt nu ondersteund in de doelinterface. </p> <p>Zie <a href="../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100" format="dita" scope="local"> Ondersteunde browsers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Het Interval van het Vertrouwen van de mening in de rapporten van het Doel voor ononderbroken variabelen </td> 
   <td colname="col2"> <p>Toon de Waaier van het Interval van het Vertrouwen voor het opbrengstmetrische type (RPV, AOV, Verkoop, Orders), en voor betrokkenheidsmetriek. </p> <p>Bijvoorbeeld, als RPV = 200.00 en CI Waaier = 50.00, dan zou dit voor RPV moeten worden getoond: 200,00 +/- 50,00 </p> <p>Deze wijziging is van toepassing op tests voor A/B, Experience Targeting en Multivariate. </p> <p>Zie <a href="../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B" format="dita" scope="local"> Vertrouwensniveau en Vertrouwensinterval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering van URL-regels voor Visual Experience Composer </td> 
   <td colname="col2"> <p>Eerder vormden de URL-sjabloonregels in de Visual Experience Composer een OF-voorwaarde met de Pagina-URL. Nu kunt u AND of OR kiezen wanneer het specificeren van veelvoudige URLs. OR is de standaardwaarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Aanbevelingen: </p> <p>Wijziging in algemene mbox-leveringscodering </p> </td> 
   <td colname="col2"> <p>Bij het maken van een ontwerp is het nu de standaardinstelling om een HTML-ontwerp in een <span class="codeph"> &lt;div&gt;- </span> element te plaatsen. </p> <p>Zie Een ontwerp maken voor meer informatie over het maken van een ontwerp <a href="../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>LTV (Life Time Value) machine learningversterkingtechniek </p> </td> 
   <td colname="col2"> <p>Dit nieuwe algoritme concentreert zich op lange termijn omzetting over vele zittingen in plaats van zich op het verbeteren van omzetting enkel in deze zitting. Deze techniek is geschikt voor sites met veel terugkerende bezoekers, omdat deze de totale inkomsten optimaliseert voor de volledige interactie met de bezoeker. </p> <p>Zie <a href="../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verbetering: Doelgerichtheid toestaan op hash-fragmenten (#) </p> </td> 
   <td colname="col2"> <p>U kunt nu richten op het gedeelte van een URL dat volgt op een hash (#). </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Dezelfde ervaring opnemen op vergelijkbare pagina's </a> en andere relevante onderwerpen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Rapport met succesmetriek downloaden </p> </td> 
   <td colname="col2"> <p> Download één enkel csv- dossier met al succes metrisch vermeld, in plaats van een rapport dat slechts het definitieve activiteitendoel had. </p> <p>Zie <a href="../c-reports/reports.md#concept_B5077F5503AA4C98901AA99EDCE6CDE6" format="dita" scope="local"> Rapporten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem opgelost waarbij alle op AEM gebaseerde activiteiten als Experience Targeting (XT)-activiteiten werden veroorzaakt. AEM gebruikt nu de correcte activiteitentypes voor A/B en XT activiteiten.
* Verwijderd een optie om niet-omzettingsmetriek als doel in nieuwe Auto Toegewezen activiteiten te gebruiken. Deze beperking wordt in een volgende release opgeheven.
* Probleem verholpen waarbij een profielscript dat in Target Classic is gemaakt, niet kon worden verwijderd uit Target Standard.
* Probleem verholpen waarbij een sjabloon voor niet-HTML-aanbevelingen in een `<div>` element werd geplaatst bij gebruik in een formuliergebaseerde workflow.
* Probleem verholpen waarbij botsingsberekeningen de tijd verlieten met een groot aantal activiteiten.
* Probleem verholpen waarbij de CSV-download het rapport Summary in plaats van het rapport Success Metrics weergaf.
* Het pop-upbericht &#39;Unieke id&#39; is verwijderd dat soms werd weergegeven tijdens het bewerken van elementen.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.
* Sommige interfaceproblemen kunnen zich voordoen in Internet Explorer 10, inclusief schermflikkering en mogelijke vertraging.
* De update van Chrome versie 48 introduceerde een kwestie die de Visuele Composer van de Ervaring veroorzaakt om verkeerd in Chrome te functioneren. Google werkt aan een oplossing. Raadpleeg voor meer informatie [https://code.google.com/p/chromium/issues/detail?id=582603](https://code.google.com/p/chromium/issues/detail?id=582603). U kunt dit probleem als volgt oplossen:

   * Gebruik Firefox of Internet Explorer.
   * Schakel de Enhanced Experience Composer in, die kan worden geconfigureerd via het tabblad **[!UICONTROL Setup]** > **[!UICONTROL Preferences]** .

## Uitzettingen 2015 {#reference_8E940F500A374F9FBCD68CDE9E7E1A00}

### Adobe Target Standard/Premium 15.10.1 (2 november 2015) {#section_B5135D75FA0D42A1A3C2711CA3A1B812}

<!-- 

target/r_release-notes-2015.xml

 -->

Deze release bevat de volgende functies en verbeteringen:

<table id="table_EE13D9B959DA4FB0AD6BC03FBF78AEF6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Automatisch toewijzen in A/B-tests </p> </td> 
   <td colname="col2"> <p> U hebt nu de optie om automatisch verkeer toe te wijzen om de algemene campagnelift te verhogen en het winnen van ervaringen sneller te ontdekken. Dit algoritme verhoogt de algemene campagneprestaties terwijl het handhaven van de integriteit van een A/B test. </p> <p>Het algoritme steunt op gemeten prestaties (b.v. omzettingspercentage) en betrouwbaarheidsintervallen om een verkeersverdeling te veroorzaken die tot tweemaal per uur wordt veranderd. </p> <p>Belangrijkste voordelen </p> <p> 
     <ul id="ul_A41C74C0C7C844F3A923CD6EA5D5D952"> 
      <li id="li_86D3C6A4993F4DC0907BF42986E6CCD1">Behoudt de integriteit van een A/B-test door ervoor te zorgen dat bezoekers in dezelfde ervaring blijven, zoals ze doen bij een handmatige A/B-test </li> 
      <li id="li_B849EB2709F84831A1B7A4F312EAFA7E">Vindt een statistisch significante winnaar sneller dan een handmatige A/B test </li> 
      <li id="li_3F258C6DEB7245E2924115C5628BC3C6">Biedt een hogere gemiddelde campagnelift dan een handmatige A/B-test </li> 
      <li id="li_C9E82388B93E4A298000984B69CBAEDE">Hiermee kunt u op elk gewenst moment overschakelen op een handtest </li> 
     </ul> </p> <p>Zie <a href="../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4" format="dita" scope="local"> Geautomatiseerde verkeerstoewijzing </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klantkenmerken </p> </td> 
   <td colname="col2"> <p> Upload gegevens van één partij, klantkenmerken genoemd, met de Experience Cloud-kernservice en kies kenmerken die u wilt delen met Target. Deze functionaliteit is in maart voor Analytics gestart en kan nu rechtstreeks met Target worden geïntegreerd. </p> <p> U kunt bijvoorbeeld klantgegevens zoals lidmaatschapsstatus (goud, zilver, enz.), koopgeschiedenis, favoriete bestemming, lokale opslag gebruiken, enzovoort in uw CRM- of eCommerce/POS-systeem. Nu kunt u die gegevens uploaden naar Experience Cloud. Nadat de gebruiker op uw site heeft geverifieerd, kunnen de gegevens door Target worden afgestemd op hun webgedrag. </p> <p>Zie <a href="https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/attributes.html" format="https" scope="external"> Klantkenmerken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Er zijn meerdere bedrijven beschikbaar wanneer u Analytics selecteert als rapportagebron voor Target. </p> </td> 
   <td colname="col2"> <p>Wanneer u Analytics selecteert als de rapporteringsbron voor Target, selecteert u een Analytics-rapportsuite die doelactiviteitgegevens ontvangt. Hiervoor kiest u eerst een van de Analytics-bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij Adobe Experience Cloud om het opnieuw te proberen. Neem contact op met de klantenservice als de rapportsuite nog steeds ontbreekt in de lijst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe ingebouwde opties voor het maken van publiek </p> </td> 
   <td colname="col2"> <p>Er zijn nieuwe ingebouwde publieksopties: </p> <p> 
     <ul id="ul_16E7B53E324B4FB79E1B1E97A1CE65AC"> 
      <li id="li_60B55A81119E48FE83639B9740A2FD21">Doelbezoekers op basis van de taal die ze in hun browser gebruiken. Dit is nauwkeuriger dan geo-based taalgerichte richten. </li> 
      <li id="li_84CAAE7E02CA48FA9C7C00C0415046B6">De bezoekers van het doel die op browser versie worden gebaseerd, niet alleen welke browser wordt gebruikt. </li> 
      <li id="li_AAF8170CAF4C45BB965D1A9A4E9204D5">U kunt nu op meerdere browsers in plaats van op slechts één browser gericht zijn. </li> 
     </ul> </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/browser.md#concept_221D8EEF53CC45AEACEB17CF336A3658" format="dita" scope="local"> Browseropties </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p class="Premium">Exclusief aankopen in het verleden </p> </td> 
   <td colname="col2"> <p>Eerder aangeschafte objecten worden nu automatisch uitgesloten van de aanbevelingen van een bezoeker. Deze optie kan voor om het even welke criteria worden onbruikbaar gemaakt. </p> <p>Deze optie is nu ingeschakeld voor alle criteria buiten de box, inclusief de criteria die werden gebruikt in activiteiten die vóór deze release werden uitgevoerd. Als u eerdere aankopen niet wilt uitsluiten, moet u deze activiteiten bewerken. </p> <p>Zie <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_28DB20F968B1451481D8E51BAF947079" format="dita" scope="local"> Insluitingsregels </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p> Kenmerkweging </p> </td> 
   <td colname="col2"> <p> De rangorde van aanbevelingen is gewijzigd voor criteria. Deze wijziging is van invloed op bestaande aanbevelingen. </p> <p> Gebruik kenmerkweging om het algoritme te verschuiven. Marketers kunnen het algoritme beïnvloeden op basis van een belangrijke beschrijving of metagegevens over de inhoudscatalogus. Pas een hogere weging toe op deze onverkochte artikelen, zodat deze vaker in de aanbeveling worden weergegeven. Niet-verkochte objecten worden niet volledig uitgesloten, maar ze worden minder vaak weergegeven. Er kunnen meerdere wegingen worden toegepast op hetzelfde algoritme en de wegingen kunnen in de aanbeveling op gesplitst verkeer worden getest. </p> <p>Deze nieuwe gewichten zijn automatisch toegepast op alle activiteiten. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p>Tijd instellen voor Feed-verwerking </p> </td> 
   <td colname="col2"> <p>Geef de tijd op waarop u een feed wilt bijwerken. </p> <p>Zie <a href="../c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Feed maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p>Gebruik de lijst van het Gegeven om een Diervoeder te plaatsen om nooit te lopen </p> </td> 
   <td colname="col2"> <p>Stel in de lijst met feed een feed in die nooit moet worden uitgevoerd als u die feed niet wilt bijwerken. </p> <p>Zie <a href="../c-recommendations/c-products/feeds.md#task_C6CD9EA905744C2CA0BB8259BB74C867" format="dita" scope="local"> Feed maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p>Een nieuw type criteria instellen op basis van gelijkenis met inhoud </p> </td> 
   <td colname="col2"> <p>Een op item gebaseerde criteria die kunnen worden gebruikt voor: </p> <p> 
     <ul id="ul_86BDF2DE0FCE4665A2985D0C56E50A53"> 
      <li id="li_D83669F9019B431891E072C973B317D7">Huidige items met vergelijkbare kenmerken </li> 
      <li id="li_4E45848423F2450999C699C64E0EE9E2">Laatst gekocht item met vergelijkbare kenmerken </li> 
      <li id="li_901D4AAF7BE244FCB9277DC7EDD91E32">Aangepaste kenmerken die overeenkomen met een opgegeven entiteit.id en items met vergelijkbare kenmerken gebruiken </li> 
      <li id="li_49D52B0182F346E982C11A0C2DA50B4F">Laatst weergegeven item met vergelijkbare kenmerken </li> 
      <li id="li_2DBAF32476AC435EB57D08D96CB55683">Meest bekeken item met vergelijkbare kenmerken </li> 
     </ul> </p> <p>Zie <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#task_28DB20F968B1451481D8E51BAF947079" format="dita" scope="local"> Insluitingsregels </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe activiteitslijstfilters </td> 
   <td colname="col2"> <p>Er zijn verschillende filters toegevoegd om u te helpen de activiteiten weer te geven die u het interessantst vindt in de lijst Activiteiten. </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p>Verbetering: Configuratie van relevante criteria voor de industrie </p> </td> 
   <td colname="col2"> <p>Niet-relevante opties tijdens de installatie zijn verwijderd. In het verleden, waren sommige opstellingsopties voor sommige industrie verticale als, zoals Media, niet altijd relevant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p>Nieuwe criteria voor Buiten-de-box </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_47E67312A04E414EB797F9AE2A1F7599"> 
      <li id="li_5EDF9006145B4498B2EAD95D642057C5">Meer video's als deze </li> 
      <li id="li_6A8DAACE7CD741D0BB766EBCB52BCD88">Meer artikelen als deze </li> 
      <li id="li_1B44AB35B045416B8D8B72C428750822">Meer inhoud als deze </li> 
      <li id="li_FEC84CCF3DF3444DAB39F4764DE897B0">Meer presentaties als deze </li> 
      <li id="li_5E874ACB5B004CACBDB4F8FF217BC593">Meer producten als deze </li> 
     </ul> </p> <p>Zie <a href="../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750" format="dita" scope="local"> Criteria </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Verbeterde rapportdetails die worden weergegeven wanneer u Analytics als rapportbron gebruikt. </td> 
   <td colname="col2"> <p>De details die door gebrek in een rapport van de Analyse wanneer het gebruiken van A4T worden getoond passen nu de details aan die in het rapport van het Doel worden getoond. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen in Global Experience Composer waarbij het slepen van een hoek om het formaat van een aangepaste viewport te wijzigen werd voorkomen.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.

### Adobe Target Standard/Premium 15.9.1 (30 september 2015) {#section_A54204291A99476688E8C0BD8255F93C}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_907A952F54084C2A9C61F10E2B7A7BFF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Mobiele webervaringscomposer </td> 
   <td colname="col2"> <p> Bekijk uw site zoals deze eruit ziet op verschillende mobiele apparaten en verschillende schermgrootten. Stel responsieve onderbrekingspunten voor sites eenmaal in en gebruik deze voor alle activiteiten om ervoor te zorgen dat uw optimalisatieactiviteiten er goed uitzien op alle apparaten die uw bezoekers gebruiken. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5" format="dita" scope="local"> Mobiele Viewports voor responsieve ervaringen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Locatie waarop het maken van formuliergebaseerde activiteiten is gericht </td> 
   <td colname="col2"> <p> Pas het richten op uw mbox plaatsen toe om te beperken waar uw activiteit toont. </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Achtergrondkleur selecteren in Visual Experience Composer voor MVT en Geautomatiseerde Personalisatieactiviteiten </td> 
   <td colname="col2"> <p>Met een kleurkiezer kunt u achtergrondkleuren instellen tijdens het bewerken van Automatische personalisatie en Multivariatie in testactiviteiten. </p> <p>Deze functie was voorheen alleen beschikbaar voor activiteiten van A/B en Gericht op ervaring. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rijke Tekst en HTML die in Visual Experience Composer voor MVT en Geautomatiseerde de Personalisatieactiviteiten uitgeven </td> 
   <td colname="col2"> <p> Tekst- en HTML-opmaak in een tekstverwerker-achtig venster bij het bewerken van Automated Personalization en Multivariate Test-activiteiten. </p> <p> Deze functie was voorheen alleen beschikbaar voor activiteiten van A/B en Gericht op ervaring. </p> <p>Deze acties bieden mogelijkheden voor tekstbewerking door HTML-tags toe te voegen of stijlen toe te passen. Deze wijzigingen door de rijke tekstredacteur voor om het even welke actie kunnen in zijn bronmening worden gezien. Gebruikers kunnen op de knop HTML in de RTF-editor drukken om de bronweergave te bekijken. De stijlen die door de rijke redacteur worden toegevoegd kunnen zich met de stijlen van klantenwebsites mengen. In dit geval kunnen gebruikers naar de bronweergave gaan en de wijzigingen bewerken om deze uit te lijnen met de stijlen van hun websites. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p class="Premium">Formuliergebaseerde aanbevelingen </p> </td> 
   <td colname="col2"> <p> Aanbevelingsactiviteiten voor locaties buiten de site maken, zoals e-mails, consoles, kiosken, enz. </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Aanbevelingen </p> <p> Informatie weergeven over de sleutel in het ontwerp </p> </td> 
   <td colname="col2"> <p>Toon het belangrijkste punt in uw ontwerp van Aanbevelingen. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium">Geautomatiseerde personalisatie </p> <p>Conversierapport </p> </td> 
   <td colname="col2"> <p> Als het optimalisatiedoel omzettings metrisch is, dan toont het rapport van het Detail van de Aanbieding nu het effect van de hoogste voorspellende variabelen in lift en stijgende omzettingen. Dit verslag was pas eerder gebaseerd op inkomsten, zodat deze mogelijkheid ervoor zorgt dat activiteiten zonder inkomstengegevens nog steeds relevante en activeerbare inzichten produceren. </p> <p>Zie <a href="../c-reports/reports-ap.md#concept_C02BAFC922114A44846998FD956E345A" format="dita" scope="local"> Geautomatiseerde Personalisatierapporten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adobe Campagne e-mailintegratie met Target Standard </td> 
   <td colname="col2"> <p> Eerder was het vereist om Target Classic te gebruiken voor het opzetten van een doelgerichte e-mailcampagne met Adobe Campaign. Met de release van twee nieuwe functies in Target Standard (op formulieren gebaseerde activiteiten maken en aanbiedingen omleiden) is het nu mogelijk om Target Standard te gebruiken om een doelgerichte e-mailcampagne op te zetten met Adobe Campagne.</p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Aanbiedingen omleiden in op formulier gebaseerde activiteiten maken </td> 
   <td colname="col2"> <p> Ondersteuning voor de omleiding biedt functionaliteit van Target Classic die is toegevoegd in de formuliergebaseerde workflow voor het maken van activiteiten op basis van Target Standard. </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Ervaar URL's in activiteiten die geen onsite cookie meer gebruiken </td> 
   <td colname="col2"> <p> De ervaring URLs beschikbaar per activiteit is nu betrouwbaarder. Kopieer eenvoudig de URL's en deel deze met andere teamleden, zelfs als ze Adobe Target niet gebruiken. </p> <p> <p>Opmerking:  Bijgewerkte ervaring URLs werkt slechts aan activiteiten die na 30 juli 2015 worden gecreeerd. Oudere activiteiten blijven gebruikmaken van de voorbeeldfunctionaliteit op basis van cookies. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Verbetering van de rapportage voor Analytics als rapportagebron voor Target </p> </td> 
   <td colname="col2"> <p> Klik om het volledige rapport Analytics rechtstreeks van de pagina van het activiteitenrapport te bekijken. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Prestatieverbeteringen van de activiteitenlijst </td> 
   <td colname="col2"> <p>De laadtijd voor activiteiten in de lijst is aanzienlijk verbeterd. Zoeken en filteren gaat veel sneller, vooral wanneer de lijst veel activiteiten bevat. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waardoor de doelrapportsuites niet konden worden weergegeven in de selector van de doelrapportsuite nadat deze was ingeschakeld voor Analytics for Target.
* Probleem verholpen waardoor het zoeken naar activiteiten via URL niet mogelijk was.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.

### Adobe Target Standard/Premium 15.8.1 (20 augustus 2015) {#section_1C26CB72316A404DB655EBE655F5B8C1}

Het doel van deze versie is eigenschappariteit van het Klassieke Doel te verstrekken. De meest gebruikte eigenschappen van Doel Klassiek zijn nu beschikbaar in de Norm van het Doel.

Deze release bevat de volgende functies en verbeteringen:

<table id="table_DF5B434D639345B4ACE2467B8966A908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Profielscripts maken en bewerken </td> 
   <td colname="col2"> <p>Profielscripts voeren profielkenmerk 'catchers' uit op elke aanvraag van een box. Wanneer een mbox verzoek wordt ontvangen, stelt het Doel om het even welke relevante profielmanuscripten in werking, bepaalt welke activiteit zou moeten lopen, en toont inhoud die aan die activiteit en die ervaring aangewezen is, dan het succes van de activiteit volgt. Op deze manier kunt u informatie over het bezoek bijhouden, zoals de locatie, het tijdstip van de bezoeker, het aantal keren dat de bezoeker naar de site is geweest, als hij of zij voor en op de site heeft gekocht. Deze informatie wordt vervolgens toegevoegd aan het profiel van de bezoeker, zodat u de activiteiten van die bezoeker op uw site beter kunt bijhouden. </p> <p>Zie <a href="../c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201" format="dita" scope="local"> Profielkenmerken </a>. 
     <!--(Copy help from Classic)--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Vertrouwensinterval voor binaire metriek </td> 
   <td colname="col2"> <p>De bijgewerkte rapporten die op doel-gebaseerde gegevens gebruiken tonen het betrouwbaarheidsinterval van de lift, in vergelijking met de controle. </p> <p>Zie <a href="../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B" format="dita" scope="local"> Vertrouwensniveau en Vertrouwensinterval </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gegevens exportactiviteitenrapport downloaden </td> 
   <td colname="col2"> <p>Download gegevens in de CSV-indeling, zodat u deze snel kunt importeren in Excel of andere programma's voor gegevensanalyse. Deze functie werkt voor A/B-, Experience Targeting- en Multivariate-activiteiten. </p> <p>Zie Rapporten <a href="../c-reports/reports.md#section_3099BC87DCAE46A2B075E1FF5B6552A6" format="dita" scope="local"> downloaden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Rijke tekst en HTML-bewerking in Visual Experience Composer </td> 
   <td colname="col2"> <p>De het formatteren van de tekst opties zijn beschikbaar wanneer het uitgeven van tekst en HTML voor A/B en de Gerichte Ervaring activiteiten in Visual Experience Composer. U kunt een lettertype kiezen, een lettertypestijl selecteren, de tekstuitlijning wijzigen en andere standaardopties voor tekstopmaak opgeven. Bij het wijzigen van HTML kunt u schakelen tussen de codeweergave en de rijke-bewerkingsweergave van de HTML. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Achtergrondkleur selecteren in Visual Experience Composer </td> 
   <td colname="col2"> <p>Met een kleurkiezer kunt u achtergrondkleuren instellen tijdens het bewerken van A/B en bij het uitvoeren van activiteiten in de Visual Experience Composer. Deze optie is niet beschikbaar als een achtergrondafbeelding is ingesteld. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Archiefactiviteit </td> 
   <td colname="col2"> <p>Een activiteit naar het archief verzenden. U kunt een gearchiveerde activiteit goedkeuren om het opnieuw actief te maken. Activiteiten in het archief worden niet standaard weergegeven in de lijst Activiteiten. </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Geautomatiseerde personalisatie </p> <p>Aanbiedingsniveau </p> </td> 
   <td colname="col2"> <p>Staat marketers toe om het richten van regels op aanbiedingen in Geautomatiseerde Personalisatie toe te passen. Hiermee kunt u uitsluiten dat bepaalde aanbiedingen aan een bepaalde groep personen worden getoond. </p> <p>Zie <a href="../c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E" format="dita" scope="local"> AP-aanbiedingen doel </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Aantal activiteiten weergeven die gebruikmaken van ontwerpen </p> </td> 
   <td colname="col2"> <p>In de ontwerpbibliotheek ziet u hoeveel actieve en inactieve activiteiten elk ontwerp gebruiken. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>Aangepaste dynamische titelweergaven in ontwerp </p> </td> 
   <td colname="col2"> <p>Kies een titel die u wilt weergeven wanneer u een bepaald ontwerp gebruikt. Deze titel hoeft niet overeen te komen met de titel die aan bezoekers op de pagina wordt weergegeven. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Recommendations Premium </p> <p>API-token </p> </td> 
   <td colname="col2"> <p>U kunt uw client-API-token instellen via Recommendations Premium. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Veelgebruikte URL's </td> 
   <td colname="col2"> Wanneer u een URL voor een activiteit of een nieuwe pagina binnen een activiteit invoert, wordt in een menu de meest recente en meest gebruikte URL's weergegeven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe opties voor mobiele apparaten </td> 
   <td colname="col2"> <p>U kunt nu meerdere mobiele apparaten activeren zonder een profielscript te vereisen. </p> <p>Zie <a href="../c-target/c-audiences/c-target-rules/mobile.md#concept_2A794199DC1A4D349FFFBC7DCF1FEB89" format="dita" scope="local"> Mobiel </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

### Adobe Target Standard/Premium 15.7.1 (30 juli 2015) {#section_9C888BFD04A94DD58616D3F67D209CCC}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_46FF5AF77D824ADC941B1E472234F05C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Logboek voor wijziging van de activiteit </td> 
   <td colname="col2"> <p>Het veranderingslogboek maakt een lijst van veranderingen die aan een activiteit worden aangebracht. De actie en de gebruiker worden vermeld met een timestamp voor elke verandering. </p> <p>Zie Logboek <a href="../c-activities/change-log.md#task_D6F224E8CE8346699187D21CD9A2B4AB" format="dita" scope="local"> Activiteitenwijziging </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere pagina's </td> 
   <td colname="col2"> <p>Met een activiteit van meerdere pagina's kunt u een artikel op meerdere pagina's maken, met een ontwerp dat specifiek is voor elke pagina. </p> <p>Je kunt bijvoorbeeld een voorstel voor gratis verzending testen met aankopen boven een bepaald bedrag. Mogelijk wilt u dat dit aanbod wordt weergegeven op uw openingspagina, een categoriepagina en bepaalde productpagina's, maar u wilt dat het een ander formaat heeft en zich op elk paginatype bevindt. Je kunt een opvallend voorstel op je homepage weergeven en dat aanbod vervolgens versterken met kleinere aanbiedingen op andere relevante pagina's. </p> <p>U kunt ook een activiteit met meerdere pagina's gebruiken om verschillende lay-outs voor uw bureaublad en mobiele sites te definiëren die niet reageren. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48" format="dita" scope="local"> Meerdere pagina's </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Op formulieren gebaseerde activiteiten maken </td> 
   <td colname="col2"> <p>Creeer een activiteit zonder de Visuele Composer van de Ervaring te gebruiken. Kies in plaats daarvan locaties en aanbiedingen via een formulier. Met dit, kunnen de Standaardactiviteiten van het Doel in e-mail, mobiele apps, kiosks, en andere plaatsen worden geleverd die niet met een Composer van de Visueel Ervaring werken. </p> <p>Zie <a href="../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E" format="dita" scope="local"> Formuliergebaseerde Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe mbox.js </p> </td> 
   <td colname="col2"> <p> Versie 58 van mbox.js verzekert de dienst van identiteitskaart van de Bezoeker van de Wolk van de Ervaring is klaar alvorens de vraag van het Doel wordt gemaakt. Dit zorgt ervoor dat publieksgegevens die via de kernservice Profielen en Soorten publiek worden gedeeld, beschikbaar zijn op dezelfde hit. Nochtans, kan het flikkeren op de pagina voorkomen terwijl het Doel op de dienst wacht om terug te keren, zodat is volledige QA belangrijk alvorens te bevorderen. Deze versie mbox.js is alleen beschikbaar via API. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Configureerbare succeswaarden </td> 
   <td colname="col2"> <p> Met de fijnkorrelige opties kunt u bepalen hoe u succesmetingen kunt tellen. U kunt onder andere de metrische waarde per impositie of één keer per bezoeker tellen en kiezen of u de gebruiker in de activiteit wilt houden of deze wilt verwijderen. Dit is gelijk aan de "geavanceerde opties" voor succesmetriek die beschikbaar zijn in Target Classic. </p> <p>Zie <a href="../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924" format="dita" scope="local"> Succeswaarden </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Verbetering: Experience Targeting Experience limit removed. </td> 
   <td colname="col2"> De vorige limiet van tien ervaringen in het praktijkgericht is opgeheven. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opties voor beheer en bewerking van Mbox.js </td> 
   <td colname="col2"> <p>Alle mbox.js configuratie en het uitgeven is nu beschikbaar binnen de Norm van het Doel. U hoeft geen wijzigingen meer aan te brengen in Target Classic. </p> <p>Zie <a href="https://marketing-beta.adobe.com/resources/help/target/ov/r_advanced_mboxjs_settings.html" format="https" scope="external"> Geavanceerde instellingen mbox.js </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Profielsynchronisatie in realtime voor gegevens van derdenId </td> 
   <td colname="col2"> Wanneer een bezoeker van een site zich halverwege de sessie aanmeldt en een 3d-partyId krijgt, zijn alle eerder geladen profielkenmerken die zijn gekoppeld aan de derde partijId nu direct beschikbaar. Zie <a href="../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E" format="dita" scope="local"> Bezoekersprofiel </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Premium voor aanbevelingen: Zoeken in factnaam </td> 
   <td colname="col2"> U kunt nu zoeken naar een facetnaam. </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> Automatische personalisatie: Metrische tracking na het doel </td> 
   <td colname="col2"> <p> Eerder startte Target een ervaring toen de bezoeker het modelleringsdoel bereikte. Gebruikers kunnen nu in de activiteit blijven voor traceringsdoeleinden nadat ze het modelleringsdoel hebben bereikt. </p> <p> Bijvoorbeeld, vaak wordt een Geautomatiseerde activiteit van de Aanpassing gebruikt om kliktarieven te verbeteren, en dat als modelleringsdoel wordt geplaatst. Nochtans, is het belangrijk om te zien hoe de verhoogde klikkoersen tot definitieve omzetting leiden, zodat is het volgen door de definitieve omzetting essentieel. </p> Zie <a href="../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Analytics as the reporting source for Target is now supported for XT activities.
* Probleem verholpen waarbij de besturingservaring die in Analytics wordt weergegeven, werd gewijzigd nadat de activiteit actief was geworden.
* Probleem verholpen die invloed had op de ingeschakelde functionaliteit van target.js wanneer nieuwe, provisioned gebruikers mbox.js downloadden.
* Probleem verholpen waarbij waarden na een # in een URL tijdens het maken van het publiek/segment als onderdeel van het pad werden beschouwd.

**Bekende problemen**

De volgende bekende problemen zijn gemeld:

* Wanneer JavaScript uitschakelen is ingeschakeld voor pageA in een activiteit met meerdere pagina&#39;s, blijft JavaScript ingeschakeld voor alle pagina&#39;s, maar blijft de functionaliteit uitgeschakeld.

### Adobe Target Standard/Premium 15.6.1 (25 juni 2015) {#section_43FEA310830E4E8E853FAB56B12B1301}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_C0B37E1730014ADA8C36310093F5C43A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verbeteringen in de compatibiliteit van Visual Experience Composer </p> </td> 
   <td colname="col2"> <p> Een nieuwe instelling voor de hele account, zodat Target gemakkelijker de juiste CSS-kiezers kan genereren. U kunt bijvoorbeeld opgeven of Doel klassen of id's moet gebruiken. Hierdoor wordt de compatibiliteit met AEM verbeterd. Deze instelling kan per activiteit worden overschreven </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ervaring Ondersteuning voor Analytics als bron voor rapportage </p> </td> 
   <td colname="col2"> <p>U kunt Analytics nu gebruiken als een rapporteringsbron voor de activiteiten van het Targeting van de Ervaring. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automatische personalisatie: Visuele indicatie van modelstatus </p> </td> 
   <td colname="col2"> <p> Zodra een voorspellend model aan de vereiste kwaliteitscriteria voldoet en als geldig wordt beschouwd, wordt het beschouwd klaar en gebruikt om een gepersonaliseerde score voor biedingsbesluit te berekenen. Een klokpictogram verandert in een vinkje wanneer het model klaar is en het Doel kan beginnen met het leveren van gepersonaliseerde inhoud. Aangezien de lift pas wordt verwacht nadat de modellen gereed zijn, kunt u met de visuele indicatie de juiste verwachting instellen. Gebruik de verkeersschatter in Visuele Composer van de Ervaring om een richtlijn te krijgen van wanneer de modellen klaar zullen zijn. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium-aanbevelingen: Bladeren en navigeren in de composer voor visuele ervaring </p> </td> 
   <td colname="col2"> <p> Hiermee kunt u de composer voor visuele beleving op één pagina openen en vervolgens koppelingen en formulierverzendingen volgen om andere pagina's op uw site te bereiken, zoals een winkelwagentje. Zodra op de pagina u wilt testen, draai de Visuele Composer van de Ervaring terug naar "stelt"wijze samen en creeer uw ervaringen. U kunt bijvoorbeeld een bericht wijzigen op de verzendpagina en het vervolgens testen op de standaardpagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Premium-aanbevelingen: Zoeken in gefactureerde catalogus </p> </td> 
   <td colname="col2"> <p> Biedt een robuustere manier om uw catalogus te doorzoeken. Ook maakt het gemakkelijker om de onderzoeksresultaten tot zeer specifieke reeks producten te beperken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Externe campagnes tonen in de lijst Standaardactiviteiten doel </p> </td> 
   <td colname="col2"> <p> In de lijst Standaardactiviteiten doel ziet u nu Klassieke campagnes. Als u uit Klassieke campagnes van het Doel wilt filtreren en slechts de Norm van het Doel bekijkt, kunt u de optie van het "Bron"onderzoeksfilter gebruiken. Als u bijvoorbeeld alleen Adobe Target Standard-activiteiten wilt weergeven, selecteert u het bronfilter en typt u "Adobe Target" als bron. De mogelijkheid om activiteiten te bekijken die zijn gemaakt in Recommendations Classic of Adobe Mobile Services, wordt in een toekomstige release toegevoegd. </p> <p>U kunt in andere oplossingen gemaakte activiteiten activeren en deactiveren via de gebruikersinterface van Doel. Voor alle andere veranderingen zult u de activiteiten in de bronoplossing moeten uitgeven. </p> <p> Voor activiteiten die in andere oplossingen worden gecreeerd, is de publieksinformatie niet zichtbaar op de pagina van het Overzicht. Bekijk de publieksinformatie in de oplossing waar de activiteit werd gecreeerd. </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Toegevoegd bericht om aan te geven dat een activiteit die niet kan worden bekeken beschikbaar is voor weergave in Doel Klassiek.
* Probleem opgelost waarbij URL&#39;s traag werden omgeleid.
* Probleem verholpen waarbij de parameters voor het bijhouden van klikken werden verbroken als andere succeswaarden in de activiteit werden verwijderd.
* Probleem verholpen waarbij de afbeelding die naar het ontwerp Aanbevelingen is geüpload niet correct werd weergegeven in de Visual Experience Composer.
* Probleem verholpen met de verkeersschatter in Geautomatiseerde Personalisatieactiviteiten waar het aantal combinaties in plaats van de som aanbiedingen over plaatsen werd gebruikt.
* Probleem verholpen waarbij mbox-parameters niet altijd op de schermen voor het maken van een publiek werden weergegeven.
* Probleem verholpen waarbij updates op de miniatuur voor het ontwerpen van Aanbevelingen werden geblokkeerd.

### Adobe Target Standard/Premium 15.5.1_Hotfix (28 mei 2015) {#section_D751F55A3812417FAA72BD6872AE3C2A}

Deze hotfix-release bevat de volgende oplossingen:

* Probleem verholpen waarbij het selectievakje Geschatte optillen in inkomsten niet zichtbaar was.
* Probleem verholpen waardoor de knop Activiteit maken voor sommige gebruikers niet correct werd weergegeven.
* Probleem verholpen dat ertoe leidde dat het tekstvak Naam activiteit in de Visual Experience Composer verdween tijdens het bewerken van A/B en de Experience Targeting-activiteiten.

### Adobe Target Standard/Premium 15.5.1 (21 mei 2015) {#section_FF0F959908784AF0906EFB9E8324F207}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_3985F758176F4884A94AFDFB78B24209"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Aangepaste code-invoer en -bewerking in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Laat u toe om, nieuwe acties te zien uit te geven en toe te voegen gebruikend een coderedacteur binnen de Visuele Composer van de Ervaring. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>JavaScript en CSS boven aan de pagina toevoegen </p> </td> 
   <td colname="col2"> <p> Voeg JavaScript-code toe aan de pagina('s) direct onder de <span class="codeph"> &lt;body&gt;- </span> tag, zonder dat u een element op de pagina hoeft te selecteren. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5" format="dita" scope="local"> Code Editor </a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Nieuwe opties voor het maken van publiek </p> </td> 
   <td colname="col2"> <p>U kunt nu als volgt een doel instellen (dit bevindt zich in de sectie Geo wanneer u een publiek maakt): </p> <p> 
     <ul id="ul_FE1E3605FB8042E9B5E80C0DB0C6C2AD"> 
      <li id="li_6D112A4DB2344B4E9F1B84E943A43DD8">ISP </li> 
      <li id="li_5C95F3F55D194D81905F8138FB546288">Netwerkdomein </li> 
      <li id="li_63E3606516BC4FFC8C91E49297542464">Verbindingssnelheid (opties zijn: breedband, dialup, mobiel, t1, t3, satelliet) </li> 
     </ul> </p> <p>Zie <a href="../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Soorten publiek </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Aanbevelingen Premium nieuwe functies </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6DC206CB52E34498BC762FCCF77807AA"> 
      <li id="li_B26568D642974F17B4B2D6E42CFDC5B9"> <p>Nieuwe modus Voorvertoning om ontwerpen weer te geven met JavaScript </p></li> 
      <li id="li_B8D1ADE874D244F198CBD3387ED3E310"> <p>Catalogus zoeken ondersteunt nu gratis zoeken naar Engelse talen </p> </li> 
      <li id="li_EB8D595EA8A84B37A3262F76543E1B05"> <p>Ondersteuning op accountniveau voor het invoeren van een statische, basis-URL die wordt toegevoegd aan alle relatieve <span class="codeph"> entiteit.thumbnailUrl- </span> waarden </p></td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Aanbevelingen Premium-verbeteringen </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_1CF5F2D0CDE84DDC9C445B5CD878EEAA"> 
      <li id="li_EB225752776449C6B21C2B2514B508C5"> <p>Verbeteringen aan ontwerpvoorproef in VEC </p> </li> 
      <li id="li_2CD8267EF166421DBB6EFBF704625848"> <p>Verbeteringen in de layout van out-of-the-box-ontwerpen </p> </li> 
      <li id="li_D737754C200844638B536A3BE02E9C5F"> Verzameling weergegeven in doeldiagram</li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p class="Premium"> Aanbevelingen Klassieke functionaliteit nu ondersteund in Recommendations Premium </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E0D6A9C12B514DE3B3EA753BB4D56662"> 
      <li id="li_2A728C8938834162A0C0C1C926AC5DD9"> Gedeeltelijke sjabloonrendering <p>Zie <a href="../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96" format="dita" scope="local"> Inhoud-instellingen </a>. </p> </li> 
      <li id="li_B1DFC829D19B4570AB5A7F937C7EF2CC"> Geef back-upregels op volgens criteria </li> 
      <li id="li_F8C9690CEC974E37B72A85C2FACFAA6D"> FTPS voor productfeeds ondersteunen</li> 
      <li id="li_3C0FA493C87345E4BE994936DF0D0162"> Aangepaste algoritmen worden nu automatisch weergegeven als criteria</li> 
      <li id="li_5B074C9FB3CB46EBA6EB4D8B1098480E"> Uurautomatische reïndexering van productcatalogi voor klanten zonder feeds </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" class="premium"> <p>Automatische personalisatie: Toegevoegde kwaliteitskoppelingen </p> </td> 
   <td colname="col2"> <p> U kunt nu een voorvertoning bekijken van de weergave van uw ervaringen bij levering. De mening en deelt verbindingen met uw AP ervaringen op uw plaats om een "ware voorproef"van de ervaringen buiten Composer van de Visuele Ervaring van het Doel te krijgen. </p> <p>Zie <a href="../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>MVT op basis van analysemogelijkheden: Voorvertoning van prestatierapport </p> </td> 
   <td colname="col2"> <p>Wanneer het gebruiken van Analytics als rapporteringsbron voor multivariate tests, kunt u voorproef uw activiteiten MVT van het rapport van Prestaties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> A/B-tests en ervaring gericht op: Activiteiten maken in drie stappen </p> </td> 
   <td colname="col2"> <p> <a href="../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72" format="dita" scope="local"> Maak een A/B </a>en <a href="../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765" format="dita" scope="local"> Ervaring die gericht zijn op </a> activiteit in drie stappen in plaats van vier. Deze verandering maakt het proces om deze activiteiten meer als het werkschema van andere activiteitentypes, zoals Geautomatiseerde Personalisatie en Multivariate Tests te creëren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Analyses als rapportbron zijn beschikbaar voor de meeste typen activiteiten. </p> </td> 
   <td colname="col2"> <p> De A/B met het activiteitstype Analytics bestaat niet meer. De optie om Analytics als uw rapporteringsbron te gebruiken is nu beschikbaar op de pagina van het Beleid &amp; van Montages voor alle activiteitstypes behalve Geautomatiseerde Personalisatie en het Targeting van de Ervaring. Dientengevolge, is er niet meer een afzonderlijk activiteitstype genoemd A/B Test met de Gegevens van de Analyse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Externe campagnes tonen in de lijst Standaardactiviteiten doel </p> </td> 
   <td colname="col2"> <p> In de lijst Standaardactiviteiten doel ziet u nu Klassieke campagnes. Als u uit Klassieke campagnes van het Doel wilt filtreren en slechts de Norm van het Doel bekijkt, kunt u de optie van het "Bron"onderzoeksfilter gebruiken. Als u bijvoorbeeld alleen Adobe Target Standard-activiteiten wilt weergeven, selecteert u het bronfilter en typt u "Adobe Target" als bron. De mogelijkheid om activiteiten te bekijken die zijn gemaakt in Recommendations Classic of Adobe Mobile Services, wordt in een toekomstige release toegevoegd. </p> <p>Zie <a href="../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03" format="dita" scope="local"> Activiteiten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Controlerapport exportorder </p> </td> 
   <td colname="col2"> <p> Mogelijkheid om het Rapport van de Controle van de Orde uit te voeren/te downloaden dat aan de rapporten van het Doel wordt toegevoegd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bèta: A4T-lift en -betrouwbaarheid </p> </td> 
   <td colname="col2"> <p> Optillen en vertrouwen zijn nu beschikbaar voor standaardmeetgegevens en aangepaste gebeurtenissen van Analytics. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen bij het maken van een publiek waarbij gewijzigde operatoren kenmerkwaarden gewist hadden.
* De aangebrachte verbeteringen zodat douane-gecodeerde regionale dozen in Visuele Composer van de Ervaring selecteerbaar zijn.
* Probleem verholpen in Aanbevelingen waarbij kenmerken met double-bytetekens (voor meertalige gevallen) de regels voor het filteren van insluiting omzeilden.
* Alle activiteitstypen ondersteunen nu activiteitennamen van maximaal 200 tekens.

### Adobe Target Standard/Premium15.3.1 (26 maart 2015) {#section_591371851693496C820175753F588E73}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_5A2F2058ACFB455E9F69484CA0C8D3DE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verbeteringen in Visual Experience Composer </p> </td> 
   <td colname="col2"> <p>Inhoud die alleen op de muisaanwijzer wordt weergegeven, zoals vervolgmenu's en minikaarten, kan nu worden geselecteerd voor bewerking in de composer voor visuele ervaring. </p> <p>Zie <a href="../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Ervaringen </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automatische personalisatie: Verkeersschatting </p> </td> 
   <td colname="col2"> <p>De schatter van het Verkeer, vroeger beschikbaar slechts in het Multivariate de activiteitstype van de Test, is nu beschikbaar voor de Geautomatiseerde activiteiten van de Personalisatie. </p> <p>Zie <a href="../c-activities/t-automated-personalization/ap-traffic-estimator.md#task_71AA6922AFD447EA8C5E610A78ABA714" format="dita" scope="local"> Schatting het Verkeer Vereist voor Succes </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Automatische personalisatie: Visuele voorvertoning </p> </td> 
   <td colname="col2"> <p>Bekijk een visuele voorvertoning van elke inhoudscombinatie in de Visual Experience Composer. </p> <p>Zie Ervaringen voorvertonen voor een geautomatiseerde personalisatietest <a href="../c-activities/t-automated-personalization/ap-preview-experiences.md#task_21A700587E88453A9FC2210C0DE53A28" format="dita" scope="local"> </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Aanbevelingen: Verbeterde weergave van inhoud </p> </td> 
   <td colname="col2"> <p>U kunt nu elk item zien dat in aanmerking komt voor een verzameling of uitsluiting wanneer u de verzameling weergeeft of bewerkt. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p class="premium">Aanbevelingen: Verbeterde zoekresultaten </p> </td> 
   <td colname="col2"> <p>Het totale aantal items dat aan elke zoekreeks voldoet, wordt weergegeven. </p>  </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Klantkenmerken uploaden in Adobe Analytics </p> </td> 
   <td colname="col2"> <p>Gebruikers van Analytics die gegevens van bedrijfsklanten vastleggen in een CRM-database (Customer relationship management) kunnen die gegevens uploaden naar de Experience Cloud. </p> <p>Zodra de gegevens in de Cloud van de Ervaring zijn, kunt u, bijvoorbeeld, een publiekssegment in Analytics tot stand brengen die klantenattributen in de segmentdefinitie omvat, en dan dat publiek met Doel delen. </p> <p> <p>Opmerking:  Het doel kan nog niet rechtstreeks onbewerkte klantkenmerken gebruiken. </p> </p></td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Voor Analytics voor op Doel gebaseerde activiteiten, zijn de Lift en de kolommen van het Vertrouwen nu verborgen voor de metriek van de Analyse waar de berekeningen niet kunnen worden uitgevoerd.
* Probleem verholpen waarbij de korte indeling van de `charset` metatag niet werd herkend in de Enhanced Experience Composer

**Bekende problemen**

* Doelgebaseerde conversiegebeurtenissen voor multivariate tests in Target Standard/Premium worden niet gerapporteerd wanneer Analytics wordt gebruikt als rapportagebron voor Target. Dit probleem zal naar verwachting binnenkort worden opgelost.
* mbox.js, versie 56, heeft de sectie &quot;Extra JavaScript&quot; verplaatst, zodat deze wordt uitgevoerd vóór globale mbox.

   Alle instellingen in v56+ hebben een naamruimte. Als er functies zijn gedeclareerd in &quot;extra JavaScript&quot;, moeten deze vooraf worden ingesteld door venster. Zie [mbox.js Wijzigingslogboek](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mboxjs-change-log.html).

### Adobe Target 15.2.1 (19 februari 2015) {#section_9AA19B060D814E08A673FB752E21D0C3}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_1558E5A5BAB64CC281C193F5A49E2ECE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p class="premium">Type nieuwe activiteit: Aanbevelingen </p> </td> 
   <td colname="col2"> <p>De activiteiten van aanbevelingen tonen automatisch producten of inhoud die uw klanten op vorige gebruikersactiviteit zouden kunnen interesseren. De aanbevelingen helpen klanten aan relevante punten leiden zij anders niet op de hoogte zouden kunnen zijn. </p> <p>Aanbevelingen zijn beschikbaar als onderdeel van de Target Premium-oplossing. Het is niet inbegrepen bij de Standaard van Doel zonder een vergunning van de Premie van het Doel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mbox.js v56 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4D4AEAC314964ECFA6C3A2669233060F"> 
      <li id="li_F71CE15AD70E4A6E9216521E8AE2B102"> Wijzigingen voor Premium-aanbevelingen ter ondersteuning van het doorgeven van parameters in algemene mbox </li> 
      <li id="li_11F777D04DE04B848F681997C6458C8B"> Voegt een 5 tweede onderbreking aan de target.js ladingsvraag toe. In het zeldzame geval dat het dossier niet laadt, zal de pagina teruggeven en geen activiteiten van de Norm van het Doel zullen tonen. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Correctie van een fout die ervoor zorgde dat een omleidingsaanbieding niet werkte wanneer het herzien van een pagina.

### Adobe Target 15.1.1 (22 januari 2015) {#section_059F9B41804B4FA58D05C4485EDF926D}

Deze release bevat de volgende functies en verbeteringen:

<table id="table_5D4C3C5695BA4A88BC65E2721CFB073A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Type nieuwe activiteit: Multivariatietest </td> 
   <td colname="col2"> <p> In een multivariate test met volledige factorial worden alle mogelijke combinaties van aanbiedingen in uw inhoudsgebieden vergeleken om u te helpen de best mogelijke combinatie van inhoud te bepalen. Uit de multivariatie-tests blijkt ook welke inhoud op welke gebieden de meeste activiteiten succesvol zijn. Een veelvoorkomend gebruik van multivariate tests is een volledige pagina te optimaliseren nadat u een A/B test hebt gebruikt om een optimale lay-out te bepalen. Met de multivariate test kunt u de afzonderlijke elementen op de pagina optimaliseren (zoals de hoofdafbeelding, kopregels of promotionele inhoud). </p> <p>Ga naar <a href="https://my.adobeconnect.com/p2k6u8iiu6l/" format="https" scope="external"> https://my.adobeconnect.com/p2k6u8iiu6l/ </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Blader naar pagina's en pagina-elementen in de Visual Experience Composer </td> 
   <td colname="col2"> <p> Hiermee kunt u de composer voor visuele beleving op één pagina openen en vervolgens koppelingen en formulierverzendingen volgen om andere pagina's op uw site te bereiken, zoals een winkelwagentje. Zodra op de pagina u wilt testen, draai de Visuele Composer van de Ervaring terug naar "stelt"wijze samen en creeer uw ervaringen. U kunt bijvoorbeeld een bericht wijzigen op de verzendpagina en het vervolgens testen op de standaardpagina. </p> <p> In de modus Bladeren kunt u ook communiceren met een pagina om de juiste status te krijgen, zoals door een afbeeldingscarrousel gaan, een miniwinkelwagentje openen of een pop-up sluiten. Als de pagina de gewenste status heeft, schakelt u over naar de modus Samenstellen en maakt u de test. </p> <p> Werkt momenteel met A/B-tests, ervaring gericht op en A/B-tests met Analytics. </p> <p>Zie <a href="../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D" format="dita" scope="local"> Ervaringen </a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mobiel apparaat </td> 
   <td colname="col2"> U kunt opties voor mobiele apparaten selecteren wanneer u een publiek maakt. <p>Zie <a href="../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Soorten publiek </a> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Klik op Tekstspatiëring (automatische personalisatie) </td> 
   <td colname="col2"> <p>U kunt klikken in Geautomatiseerde Personalisatie nu volgen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> mboxTrace-foutopsporingshulpprogramma </td> 
   <td colname="col2"> <p> Onderzoek details over uw de paginaimplementatie van het Doel en activiteit/ervaringsleveringsstatus voor het betere oplossen van problemen. </p> <p>Zie <a href="../c-activities/c-troubleshooting-activities/content-trouble.md#concept_D2548B486C984B1E97ED7A72075B8EEA" format="dita" scope="local"> Inhoudslevering voor probleemoplossing </a> voor meer informatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij schuiven niet correct werkte in IE10.

## Uitzettingen 2014 {#reference_A841709C803C4ECEB236F62E6513EB0F}

### Adobe Target 14.10.2 (6 november 2014) {#section_E7036B45DF974FB7B81E67261357A01B}

<!-- 

target/r_release-notes-2014.xml

 -->

Deze kleine release is vooral gericht op serverstabiliteit. Er zijn geen nieuwe functies als onderdeel van deze patch.

### Adobe Target 14.10.1 (30 oktober 2014) {#section_D557CB331A004155B91CFE5B197076F3}

Deze release bevat de volgende functies en verbeteringen:

| Functie | Beschrijving |
|---|---|
| Aanbiedingen omleiden | Leid een ervaring om naar een andere URL zodat u één pagina tegen een andere pagina kunt testen. Zie Een omleidingsvoorstel [maken](../c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA). |
| Doelgerichtheid toepassen op succesmetriek | Kies een opgeslagen publiek dat u wilt toepassen op een succesmetrische methode. Met deze functie kunt u beperken wat acties tellen voor een bepaalde succesgebeurtenis. Een voorbeeld zou omzettingen kunnen beperken tot wanneer de orde meer dan $0 is, of slechts telend succes wanneer een gebruiker een bepaalde pagina in de zelfde zitting bekijkt zoals het ingaan van de activiteit. |
| Automatische personalisatie: Selecteren en rapporteren op basis van RPV/AOV-meetgegevens | U kunt nu de RPV- en AOV-meetgegevens selecteren in de ontwerpworkflow voor automatische personalisatie. Voor meer informatie over het creëren van een Geautomatiseerde activiteit van de Personalisatie, zie [Geautomatiseerde Personalisatie](../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9). |
| Verbeterde besturingselementen voor machtigingen | Alleen gebruikers met de juiste machtigingen kunnen het publiek bewerken. |

Deze release bevat de volgende verbeteringen:

* De overzichtspagina toont het activiteitendoel.
* Er wordt een waarschuwing weergegeven wanneer JavaScript wordt ingevoerd in het HTML-bewerkingsvak.

### Adobe Target 14.9.1 (19 september 2014) {#section_681F27FBFDFF46FE8A1A8E24A50A26F4}

Deze release bevat de volgende functies en verbeteringen:

| Functie/verbetering | Beschrijving |
|---|---|
| Invoegen en bewerken van JavaScript toestaan | U hebt de mogelijkheid toegevoegd om aangepaste JavaScript te bewerken en te injecteren in de ervaringseditor wanneer u een optie kiest in het **[!UICONTROL Edit HTML]** menu Handelingen. |
| Automatisch publiek importeren | Soorten publiek worden automatisch op de achtergrond geïmporteerd wanneer een gebruiker de lijst met doelgroepen opent en het geïmporteerde publiek langer dan 10 minuten oud is. |
| Meer HTML-aanbiedingen dan kunnen worden gesynchroniseerd [!DNL Target Classic] | De voormalige 64 kB-limiet is verhoogd tot 256 kB. |

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij videovoorstellen niet correct werden geleverd op Firefox.
* Probleem verholpen waardoor een ongedaan maken van het bewerken van een koppeling niet kon worden weergegeven als ongedaan gemaakt in de composer voor visuele ervaring.
* Probleem verholpen in de ervaringseditor voor Geautomatiseerde personalisatie die ertoe leidde dat een gewijzigd videoaanbod niet als gewijzigd werd weergegeven.
* Correctie van een fout die ervoor zorgde dat de botsingspagina van een activiteit in Google Chrome als lege pagina werd getoond.

### Adobe Target 14.8.1 (21 augustus 2014) {#section_02D0DFA7A8D145B2B3FEFF83591243E1}

Deze release bevat de volgende nieuwe functies en verbeteringen:

| Functie/verbetering | Beschrijving |
|---|---|
| Verbeterde synchronisatie van HTML-aanbiedingen met [!DNL Target Classic] door de tekenlimiet te verhogen | De tekenlimiet van een HTML-aanbieding bij Inhoud is verhoogd om deze uit te lijnen op de limiet van 256 kB voor HTML-aanbiedingen die zijn gesynchroniseerd met [!DNL Target Classic]. |
| Verbeterde gebruikerservaring wanneer een fout wordt gecreeerd in de Redacteur van de Ervaring. | De Experience Editor geeft een bericht weer wanneer de wijzigingen in de DOM-structuur op de pagina de kiezers afbreekt. |

**Oplossingen**

* Probleem verholpen waarbij de rapportgrafiek niet werd gegenereerd tijdens het navigeren tussen activiteiten.
* Probleem verholpen waarbij geselecteerde koppelingen niet werden gemarkeerd als geselecteerd wanneer gebruikers **[!UICONTROL Select Link]** op de [!UICONTROL Goals and Settings] pagina klikten.

* Probleem verholpen waarbij een nieuwe activiteit niet in de pagina kon worden weergegeven [!UICONTROL Activity List] nadat deze op de [!UICONTROL Overview] pagina was geactiveerd.

* Probleem verholpen waardoor gebruikers geen koppeling konden selecteren voor klikken op bijhouden.
* Probleem verholpen waarbij dubbele aanbiedingen werden weergegeven in een rapport op aanbiedingsniveau.
* Probleem verholpen waardoor mbox-elementen niet konden worden ingevoegd.
* Correctie van een fout die ervoor zorgde dat de conversies van de verbindingsklik niet werkten.
* Oplossing voor een fout bij klikconversie die is genegeerd `target="_blank" functions.`
* Probleem verholpen waarbij met klikken bijhouden werd genavigeerd buiten de pagina.

### Adobe Target 14.6.1 (25 juni 2014) {#section_A520F01EEE0A4C2CBB3F2A37E6DD6F83}

Deze release bevat de volgende nieuwe functies:

>[!NOTE]
>
>Sommige functies in deze release zijn alleen beschikbaar als onderdeel van de [!DNL Target Premium] oplossing.

<table id="table_A2A978B157D54E17BD7366ADC04C8FC9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="keyword"> Geautomatiseerde personalisatie (Target Premium) </span> </td> 
   <td colname="col2"> <p> <span class="keyword"> Automated Personalization </span> biedt geavanceerde computerleeralgoritmen om persoonlijke ervaringen en verbeterde conversiesnelheden voor digitale ervaringen te stimuleren. </p> <p> <p>Opmerking:  <span class="keyword"> Automated Personalization </span> is beschikbaar als onderdeel van de <span class="keyword"> Target Premium- </span> oplossing. Deze wordt niet bij <span class="keyword"> Target Standard geleverd </span> zonder <span class="keyword"> Target Premium- </span> licentie. Als u een <span class="keyword"> Target Standard- </span> of <span class="keyword"> Target Premium- </span> licentie hebt, gebruikt u de <span class="keyword"> Target- </span> kaart in de Adobe Experience Cloud. </p> </p> <p>Eén bestand op uw site implementeren en de mogelijkheid bieden om naar inhoud te wijzen en erop te klikken en vervolgens visueel aanvullende inhoudsopties voor dat gebied maken en selecteren. Vervolgens bepaalt het modelleringssysteem automatisch welk stuk inhoud aan elk individu moet worden geleverd op basis van alle gedragsgegevens die het systeem over de bezoeker heeft. Deze mogelijkheid biedt een persoonlijke ervaring voor elke bezoeker. De markeerteken hoeft geen test uit te voeren, vervolgens de resultaten te analyseren en vervolgens een winnaar te leveren voordat de lift die uit optimalisatie is gevonden, wordt gerealiseerd. </p> <p> <span class="keyword"> Automated Personalization </span> biedt: </p> 
    <ul id="ul_9EF654B10FFA46169EE2E033683BA82E"> 
     <li id="li_8D201BF8F37B4B2489D039A0340E065E">Twee machinaal leeralgoritmen: 
      <ul id="ul_E1DF69071C9047EEA692B5EF01176E4B"> 
       <li id="li_1F4ED87AB6D044C1BE04D0360F42D56F"> <span class="keyword"> Willekeurig bos </span> </li> 
       <li id="li_BE6388BA88684501B741713CECF5AE91"> <span class="keyword"> Residuvariatiemodel </span> </li> 
      </ul> </li> 
     <li id="li_36E18493A95B4C96BFA3133CDFD8826A">Eén regel code-implementatie met WYSIWYG-inhoud bewerken </li> 
     <li id="li_79B1878FA64A40E88A973C57C39FC5FF">Het primaire doel voor de activiteit gebruikt momenteel metrisch Conversie. Opbrengsten en betrokkenheid zijn beschikbaar als extra maatstaven. </li> 
     <li id="li_FE94A79767EF4534BD02B2AFD7E27E1B">Verbinding met het <span class="keyword"> Hoofdmarketingprofiel </span> voor naadloze verzameling van gedragsgegevens van bezoekers vooraf </li> 
    </ul> <p>Zie <a href="../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9" format="dita" scope="local"> Automated Personalization </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Meerdere activiteiten op één pagina </td> 
   <td colname="col2"> <p>De inhoud van veelvoudige Standaardactiviteiten van het Doel kan op één pagina van één <span class="keyword"> </span> de servervraag van het Doel worden geleverd. </p> <p> <p>Opmerking:  Dit is niet van invloed op de beoordeling van de Klassieke Doelprioriteiten. </p> </p><p>Voor informatie over hoe het Doel bepaalt welke ervaring om te tonen wanneer de veelvoudige activiteiten de zelfde plaats op een pagina richten, zie <a href="../c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F" format="dita" scope="local"> Prioriteit </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Oplossingen**

* Probleem verholpen waarbij sommige gedeelde soorten publiek die zijn verwijderd, nog steeds in de [!UICONTROL Audiences] lijst worden weergegeven.
* Probleem verholpen waarbij een onverwacht [!UICONTROL Save] dialoogvenster werd weergegeven in Internet Explorer 10.
* Synchronisatiefout bij het opslaan van een campagne gecorrigeerd.
* Probleem verholpen waarbij het publiek voor een ervaring niet werd weergegeven in rapporten.
* Probleem verholpen waardoor de cijferlijsten in [!DNL Target] en [!DNL Analytics] niet konden overeenkomen.

* Probleem verholpen waarbij gebruikers hun globale box konden opgeven als een box die wordt gebruikt om HTML-inhoud te leveren door [!DNL Target Standard]. Het gebruik van de globale box heeft op die manier een negatief effect op de levering van inhoud en [!DNL Target Classic]op de mogelijkheid om meerdere campagnes op één pagina in één aanvraag te leveren.

* Probleem verholpen waarbij de weergave van verwijderde items werd voortgezet.

### Adobe Target Standard 14.5 (28 mei 2014) {#section_530EAB9376414D4989CA0740361DDCC2}

Deze release bevat de volgende opgeloste problemen:

* Probleem verholpen waarbij het voorvertonen van een ervaring niet naar behoren functioneerde.

### Adobe Target Standard 1.7 (28 april 2014) {#section_2C2B9B6299ED4F48A3B983AB015F381A}

[Doelstandaard 1.7-releasewebinar](https://my.adobeconnect.com/p1oabaz3cxi/)

Deze release bevat de volgende nieuwe functies:

<table id="table_11CD9EE0C9534FF19C9154784C4BFCF0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Adobe Analytics-verbeterde rapportage voor Adobe Target </td> 
   <td colname="col2"> Klanten van Adobe Analytics kunnen Analytics selecteren als de standaardrapporteringsbron tijdens het <a href="../c-activities/t-test-ab/t-test-create-ab/create-a4t.md#task_FE48F7B077C44A5BA015B087428412EF" format="dita" scope="local"> testinstallatieproces </a>. Het selecteren van alle succesmetriek of publiek dat u wilt gebruiken om uw resultaten te filteren, is niet meer vereist. Binnen rapportering, kunt u om het even welk succes metrisch of publiekssegment selecteren dat in Analytics wordt bepaald en het retroactief toepassen op uw rapportering voor het uitgebreide filtreren en boor-down analyse van uw optimalisatieresultaten. <p> <p>Opmerking:  Ga naar <a href="https://www.adobe.com/go/audiences" format="http" scope="external"> https://www.adobe.com/go/audiences </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Hoofd marketingprofiel in realtime publiek </td> 
   <td colname="col2"> Gebruik het algemene marketingprofiel dat bezoeker-id's en -gegevens verenigt in één actionabel profiel voor gebruik in verschillende oplossingen. Met een selectievakje tijdens het maken van segmenten in Adobe Analytics is het segment beschikbaar in de aangepaste publieksbibliotheek van Adobe Target. Een segment dat is gemaakt in Analytics of Audience Manager, kan worden gebruikt om bezoekers in Target als doel in te stellen. <p> <p>Opmerking:  Ga naar <a href="https://www.adobe.com/go/audiences" format="http" scope="external"> https://www.adobe.com/go/audiences </a>. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ervaring voor activiteitstype </td> 
   <td colname="col2"> <a href="../c-activities/t-experience-target/experience-target.md#task_A53DF336CB9F4D7BB87EF2106099EFC4" format="dita" scope="local"> Verschillende ervaringen op verschillende soorten publiek in één activiteit richten </a>. <p> <p>Opmerking:  Dit verstrekt gelijkaardige functionaliteit aan de Landing de campagne van de Pagina in Geavanceerd Doel. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Testen van meerdere pagina's </td> 
   <td colname="col2"> <p> <a href="../c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781" format="dita" scope="local"> Kies of u een test- of doelactiviteit wilt uitvoeren op een set webpagina's </a>. U kunt nu tests uitvoeren op elke productpagina of uw algemene nav wijzigen op elke pagina van de site. Gebruik een eenvoudige regelbouwer om op te geven wat de groep pagina's moet zijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Opgeloste problemen**

Deze release bevat de volgende opgeloste problemen:

* Probleem verholpen waardoor Edge `target.js` niet kon worden gecomprimeerd.
* Probleem verholpen in rapporten die ervoor zorgden dat het aantal conversies in de rij Activiteit niet kon worden weergegeven voor A/B-activiteiten.
* Probleem verholpen waarbij een rapport niet meer werd weergegeven nadat een ervaring met gegevens was verwijderd.
* Er is een tijdelijke oplossing gemaakt om automatisch een fout in Chrome versie 34 te omzeilen waardoor pagina&#39;s met gemengde inhoud niet konden worden weergegeven. Alle versies van Chrome kunnen nu worden gebruikt.

**Bekende problemen**

Deze release bevat de volgende bekende problemen. Dit probleem wordt in een volgende update opgelost.

* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Doelstandaard wanneer geolocatie wordt uitgeschakeld in Geavanceerd doel.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.
* Als u een afbeelding omwisselt en deze vervolgens vergroot of verkleint, worden de ervaringen in de Experience Editor niet correct weergegeven.

### Adobe Target Standard 1.6 (17 maart 2014) {#section_DB1319CDD8944F6FB749E525EB551017}

Deze release bevat de volgende nieuwe functies:

| Functie | Beschrijving |
|---|---|
| Gelokaliseerde versies beschikbaar | De doelstandaard is in het Frans, Duits, Japans en Spaans gelokaliseerd |
| Vereenvoudigde implementatie | De norm van het doel is verbeterd om het voor bestaande Geavanceerde gebruikers van het Doel gemakkelijker te maken om uit te voeren. De nieuwe implementatie gebruikt uw bestaande globale vakjes om de activiteiten van de Norm van Adobe in werking te stellen. |

**Opgeloste problemen**

Deze release bevat de volgende opgeloste problemen:

* Probleem opgelost waarbij Item verwijderen en HTML bewerken in bepaalde gevallen niet werkte.

**Bekende problemen**

Deze release bevat de volgende bekende problemen. Dit probleem wordt in een volgende update opgelost.

* De winnende werken die op Goal slechts worden gebaseerd en verandert niet gebaseerd op geselecteerde metriek.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Doelstandaard wanneer geolocatie wordt uitgeschakeld in Geavanceerd doel.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.
* Het nieuwe viztarget mbox-type werkt niet met de integratie Target Advanced/Adobe Analytics v4, de huidige versie.
* In rapporten komen de getalnotatie en de valuta in de grafiek niet overeen met de tabel als de landinstelling is ingesteld op iets anders dan de dollar.
* Het zoekvak Soorten publiek ondersteunt geen niet-ASCII-tekens.
* Voor gebruikers van de Spaanse en Japanse versie leidt het opslaan van een activiteit na het instellen van de begin- en einddatum tot een fout. U wordt aangeraden op te slaan zonder begin- en einddatum in te stellen en uw activiteit vervolgens te activeren en stop te zetten vanuit de pagina Overzicht van activiteit of Activiteitenlijst wanneer dat nodig is.

### Adobe Target Standard 1.5 (25 februari 2014) {#section_5E9E3DDBCB82494AA62A21AC9282063F}

Deze release bevat de volgende nieuwe functies:

<table id="table_67115780726F48859DC8E46E34567DC3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Conflicten bij activiteit </td> 
   <td colname="col2"> <p> De Standaard van het doel verstrekt nu een lijst van activiteitenbotsingen. Een activiteitenbotsing komt voor wanneer de veelvoudige activiteiten opstelling zijn om inhoud aan de zelfde pagina te leveren. Als een activiteitenbotsing voorkomt, kunt u niet de verwachte inhoud op uw pagina zien omdat u een verschillende activiteit hebt ingegaan. </p> <p> Alle activiteiten op dezelfde URL worden vermeld, ongeacht de doelgroep in elke activiteit. </p> <p> Als uw activiteit botsingen bevat, is een <span class="wintitle"> </span> lusje van Botsingen beschikbaar op de pagina van het activiteitenoverzicht. Open dit tabblad voor een lijst met activiteiten die botsen. Klik op een activiteit in de lijst om de overzichtspagina voor die activiteit weer te geven. </p> <p>Zie <a href="../c-experiences/c-visual-experience-composer/activity-collisions.md#concept_0BC6B929592744DFA7DA01FF4F91052E" format="dita" scope="local"> Activiteitenconflicten </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Nieuwe doelopties: Profiel, gebruiker </td> 
   <td colname="col2"> U kunt nu profiel- en gebruikersparameters als doel instellen. Zie <a href="../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271" format="dita" scope="local"> Soorten publiek </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Elementen invoegen </td> 
   <td colname="col2"> <p>U kunt nu elk element aan uw pagina toevoegen en de bestaande inhoud wijzigen. Voeg tekst, code, lijsten en meer toe om geheel verschillende ervaringen te maken die u wilt testen. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze release bevat de volgende bekende problemen. Dit probleem wordt in een volgende update opgelost.

* De winnende werken die op Goal slechts worden gebaseerd en verandert niet gebaseerd op geselecteerde metriek.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Doelstandaard wanneer geolocatie wordt uitgeschakeld in Geavanceerd doel.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.

### Adobe Target Standard 1.4 (20 januari 2014) {#section_CD27AEE32B4F40BDAB422711B96739A5}

Deze release bevat de volgende nieuwe functies en verbeteringen:

<table id="table_9E303FF0CD954795A29369A6D4166DB5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Functie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Schatting van inkomstenbelasting </td> 
   <td colname="col2"> <p>Doel kan een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. </p> <p>In deze schatting wordt de hoeveelheid lift berekend die door de winnende ervaring wordt behaald en het totale aantal bezoekers gedurende de duur van de test, en wordt de lift weergegeven die u kunt behalen als elke bezoeker de winnende ervaring ziet, als de trends doorzetten zoals ze tijdens de test hebben. </p> <p> De juistheid van de raming hangt af van een aantal factoren, waaronder de geraamde cijfers indien de huidige tendensen aanhouden. Deze waarden zijn schattingen op basis van de in het verleden behaalde resultaten en mogen niet worden gebruikt voor financiële richtsnoeren. Toekomstige resultaten kunnen afwijken. </p> <p>Zie <a href="../administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE" format="dita" scope="local"> Raming Lift in Revenue </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Ongedaan maken/Opnieuw </td> 
   <td colname="col2"> <p>Tijdens een bewerkingssessie kunt u wijzigingen in uw activiteiten ongedaan maken. U kunt ongedaan gemaakte wijzigingen ook opnieuw uitvoeren. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Element verplaatsen </td> 
   <td colname="col2"> <p>U kunt elementen op uw pagina verplaatsen. In tegenstelling tot Elements herschikken, verschuift Verplaatsen andere elementen niet om ruimte te maken voor het element dat wordt verplaatst. Gebruik de pijltoetsen om de verplaatsing te verfijnen. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Element vergroten/verkleinen </td> 
   <td colname="col2"> <p>U kunt het formaat van een element op uw pagina wijzigen. Wanneer u Formaat wijzigen selecteert, wordt een greep weergegeven in een hoek van het element waarmee u die hoek kunt slepen om het formaat te wijzigen. </p> <p>Zie Opties <a href="../c-experiences/c-visual-experience-composer/viztarget-options.md#reference_3BD1BEEAFA584A749ED2D08F14732E81" format="dita" scope="local"> van Visual Experience Composer </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Een locatie kiezen bij het instellen van een publiek </td> 
   <td colname="col2"> <p>Wanneer u een publiek maakt, kunt u een locatie (mbox) selecteren en parameters voor die locatie opgeven. </p> <p>Zie <a href="../c-target/c-audiences/create-audience.md#task_1D507519D3AD4390B507F188BD294DC1" format="dita" scope="local"> Een nieuw publiek maken </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Koppelingen voorvertonen (verbetering) </td> 
   <td colname="col2"> <p>Voorvertoning van koppelingen werkt naar behoren. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze release bevat de volgende oplossingen:

* Correctie van problemen waardoor voorvertoningskoppelingen niet naar behoren konden worden weergegeven.

Deze release bevat de volgende bekende problemen. Deze problemen worden in een volgende update opgelost.

* Als Geschatte Lift in de Norm van het Doel wordt toegelaten, en het Doel Geavanceerd wordt geplaatst aan een verschillende tijdzone dan browser van de gebruiker, zou de voorspelde opbrengstwaarde niet op de lijst van Activiteiten of in de de statusbar van Rapporten voor maximaal één volledige dag kunnen verschijnen. Omdat de Mening van het Rapport datum maar niet tijd gebruikt, verschijnen de gegevens in de Mening van het Rapport maar niet voor geprojecteerde lift.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Doelstandaard wanneer geolocatie wordt uitgeschakeld in Geavanceerd doel.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.

## Uitzettingen 2013

### Adobe Target Standard 1.3 (19 november 2013) {#section_D633ACA56FA941648219EB3748D814EC}

Deze release bevat de volgende nieuwe functies en verbeteringen:

| Functie | Beschrijving |
|---|---|
| Geo-targeting | Doel op land, staat, plaats, postcode, of DMA. |
| Gebruik Composer visuele ervaring om elementen opnieuw te rangschikken. | U kunt kindelementen binnen hun ouderelement opnieuw rangschikken gebruikend de Visuele Composer van de Ervaring. |
| Rechtstreeks op uw site wordt een voorvertoning weergegeven. | Nadat u een activiteit hebt opgeslagen, kunt u deze direct op uw site bekijken, zelfs als de activiteit niet actief is. Op deze manier kunt u zien hoe het eruitziet, zonder dat dit via een iFrame wordt weergegeven. U kunt koppelingen naar elke testervaring kopiëren om die ervaringen in uw browser te bekijken of om ze naar uw teamleden te sturen zodat ze deze kunnen bekijken. Personen die deze pagina&#39;s weergeven, worden niet meegeteld in de rapporten. |

Deze release bevat de volgende oplossingen:

* Probleem verholpen waarbij de metrische gegevens voor het bijhouden van klikken niet uit een activiteit zijn verwijderd als de URL voor de ervaring opnieuw is ingesteld.
* Probleem verholpen in de ervaringscomposer die ervoor zorgde dat de standaardervaring snel flitst voordat nieuwe inhoud wordt weergegeven tijdens het navigeren door ervaringen.

Deze release bevat de volgende bekende problemen. Deze problemen worden in een volgende update opgelost.

* Er treedt een synchronisatiefout op als Geo-publiek wordt gemaakt in Doelstandaard wanneer geolocatie wordt uitgeschakeld in Geavanceerd doel.
* Kan een afbeelding niet wisselen wanneer naar de afbeelding wordt verwezen in CSS.
* Klik het volgen werkt niet aan elementen die zijn herschikt gebruikend Composer van de Visuele Ervaring. Vermijd het instellen van het bijhouden van klikken op opnieuw gerangschikte elementen totdat deze fout is opgelost.
* Gebruikers kunnen de **[!UICONTROL Remove]** actie niet selecteren voor inhoud die in een box is opgenomen.

### Adobe Target Standard 1.2 (31 oktober 2013) {#section_420B5E910D7341AA8DB059C8E1071D53}

Er zijn vier bekende problemen met deze release. Deze problemen worden in een volgende update opgelost.

* Op sommige clusters wordt het bewerken van een herbruikbare aanbieding mogelijk niet weerspiegeld op de locatie van de klant voor activiteiten die buiten een box worden aangeboden.
* Als u afbeeldingen omwisselt in een gebied van een pagina die niet door een box wordt beheerd, treedt mogelijk een fout van 404 op.
* Wanneer u een nieuw publiek maakt of een bestaand publiek bewerkt en opslaat, wordt dit pas weergegeven in de lijst Soorten publiek als u het scherm vernieuwt of naar het publiek zoekt.
* Als u een HTML-aanbieding verwijdert uit de Target Standard, wordt deze niet verwijderd uit Geavanceerd doel.

Deze release bevat de volgende correcties en verbeteringen:

* Oplossing voor meerdere problemen die ertoe leidden dat sommige activiteiten en ervaringen niet correct werden gesynchroniseerd met Target Advanced.
* Probleem verholpen waarbij andere scripts uit de [!DNL target.js] `<head>` sectie van een pagina werden verplaatst.

* Probleem verholpen waarbij bepaalde middelen waarnaar wordt verwezen, werden gekopieerd wanneer een activiteit wordt gekopieerd.
* Oplossing een kwestie die een bijgewerkte beeldaanbieding ertoe bracht om inhoud niet bij te werken in zowel Scene7 als Geavanceerd Doel.
* Probleem verholpen waarbij door het toepassen van een zoekfilter het publiek dat is geselecteerd in &quot;Soorten publiek voor rapportage&quot;, werd gewist.
* Verbeterde grafieken worden standaard op uurresultaten toegepast wanneer een test minder dan twee dagen actief is geweest.
* Probleem verholpen waarbij het kopiëren van een niet-gesynchroniseerde activiteit mislukte.
* Toegevoegde functionaliteit voor toetsenbordinvoer voor vervolgkeuzemenu&#39;s voor locatie.
* Probleem verholpen waarbij de naam van een [!DNL mbox.js] bestand dat u van Target Standard hebt gedownload, bekend is [!DNL mboxEditor.at.js].

* Verbeterde de foutmelding die wordt weergegeven wanneer u een aanbieding verwijdert die in een activiteit wordt gebruikt.

### Adobe Target Standard 1.1 (18 oktober 2013) {#section_79FA6A61D2284D41A34F00014A342F07}

Deze release bevat de volgende functie:

| Functie | Beschrijving |
|---|---|
| [!DNL mbox.js] downloaden vanuit Target Standard | Het [!DNL mbox.js] bestand kan nu rechtstreeks van **[!UICONTROL Setup]** > **[!UICONTROL Implementation]** worden gedownload in de interface Target Standard. Eerder moest het bestand worden gedownload van Target Advanced of worden geleverd door uw accountvertegenwoordiger of consultant. |

Deze release bevat de volgende correcties en verbeteringen:

* Probleem verholpen waarbij activiteitensynchronisatie mislukte tijdens de eerste synchronisatiepoging nadat er geldige ervaringen waren toegevoegd aan een gedeeltelijke activiteit.
* Probleem verholpen waarbij 500 fouten in het rapport Samenvatting werden gegenereerd nadat een ervaring was verwijderd en toegevoegd.
* Probleem verholpen dat onnauwkeurige bezoekersgegevens veroorzaakte wanneer een bezoeker meerdere ervaringen bekijkt.
* De begin- en eindtijd van de activiteit synchroniseren nu correct tussen Standaard en Geavanceerd.
* De weergave van gemengde inhoud is verbeterd.
* Probleem verholpen waardoor de composer voor visuele ervaring niet goed functioneerde als JavaScript in de HTML-code de browserdefinitie van het JSON-object overschrijft.
* Probleem verholpen waarbij het weergegeven aantal activiteiten onjuist was tijdens het sorteren op status.
* Probleem verholpen waarbij witruimte in het veld Doel niet correct werd gevalideerd.
* Probleem verholpen waarbij meerdere aanbiedingen voor één functie werden gemaakt in Geavanceerd toen de afbeelding werd gewisseld.
* Probleem verholpen waarbij de zoekopdracht ertoe leidde dat er niet aan afbeeldingen in de inhoudkiezer werd gewerkt.
* Probleem verholpen waarbij de volgorde van de omgekeerde activiteitslijst werd gewijzigd bij het sorteren op naam of status.
* Probleem verholpen waarbij anonieme aanbiedingen niet werden verwijderd wanneer ze niet meer in een activiteit werden gebruikt.
* Probleem verholpen waarbij een onjuiste ervaringsnaam werd weergegeven op een gedeelde kaart tijdens het bewerken van een activiteit.
* Oplossing een gebrek waar een bijgewerkte beeldaanbieding de inhoud in zowel Scene7 als Geavanceerd van het Doel niet correct bijwerkte.
* Het kopiëren van een afbeeldingselement heeft een probleem verholpen waarbij ook Scene7-gerelateerde eigenschappen werden gekopieerd die niet hadden mogen worden gekopieerd.
