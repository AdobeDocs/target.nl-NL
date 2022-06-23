---
keywords: google;samesite;cookies;chroom 80;ietf
description: Ontdek hoe Adobe [!DNL Target] behandelt de norm SameSite IETF die met Google Chrome versie 80 wordt geïntroduceerd en wat u moet doen om aan dit beleid te voldoen.
title: Hoe werkt [!DNL Target] Handelen met Samesite Cookie-beleid voor Google?
feature: Privacy & Security
role: Developer
exl-id: 5abd2065-3692-4a6d-9ac9-6d416604c2d2
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1955'
ht-degree: 0%

---

# Beleid voor cookies van Google Chrome SameSite

Google zal standaard een nieuw beleid voor cookies gaan toepassen voor gebruikers die beginnen met Chrome 80, dat begin 2020 wordt gepubliceerd. In dit artikel wordt uitgelegd wat u allemaal moet weten over het nieuwe beleid voor SameSite-cookies, hoe [!DNL Adobe Target] ondersteunt dit beleid en hoe u dit kunt gebruiken [!DNL Target] om te voldoen aan het nieuwe SameSite Cookie-beleid van Google Chrome.

Vanaf Chrome 80 moeten webontwikkelaars expliciet opgeven welke cookies op verschillende websites kunnen worden gebruikt. Dit is het eerste van de vele mededelingen die Google van plan is te doen om privacy en veiligheid op het web te verbeteren.

Gezien het feit dat Facebook op het gebied van privacy en veiligheid op de proppen is gekomen, hebben andere belangrijke spelers zoals Apple en nu Google snel geprofiteerd van de mogelijkheid om nieuwe identiteiten te creëren als beschermers van privacy en veiligheid. Apple leidde het pakket door begin dit jaar via ITP 2.1 en onlangs, ITP 2.2, voor het eerst wijzigingen aan te kondigen in zijn beleid inzake cookies. In ITP 2.1 blokkeert Apple cookies van derden en worden cookies die op de browser zijn gemaakt, slechts zeven dagen bewaard. In ITP 2.2 worden cookies slechts één dag bewaard. De aankondiging van Google is bij lange na niet zo agressief als die van Apple, maar het is de eerste stap naar hetzelfde einddoel. Voor meer informatie over het beleid van Apple raadpleegt u [Apple Intelligent Tracking Prevention (ITP) 2.x](https://developer.adobe.com/target/before-implement/privacy/apple-itp-2x/).

## Wat zijn cookies en hoe worden ze gebruikt?

Voordat we gaan duiken in de wijzigingen die Google aanbrengt in zijn beleid voor cookies, moeten we ons afvragen welke cookies zijn en hoe ze worden gebruikt. Eenvoudig gezet, zijn de koekjes kleine tekstdossiers die in Webbrowser worden opgeslagen die worden gebruikt om gebruikersattributen te herinneren.

Cookies zijn belangrijk omdat ze de gebruiker meer doen terwijl ze op het web surfen. Als u bijvoorbeeld boodschappen doet op een eCommerce-website en iets toevoegt aan uw winkelwagentje maar zich niet aanmeldt of koopt tijdens dat bezoek, onthouden cookies uw items en houden ze in uw winkelwagentje voor uw volgende bezoek. Of stel je voor dat je je gebruikersnaam en wachtwoord telkens opnieuw moet invoeren als je je favoriete website van sociale media bezoekt. Cookies lossen dat probleem ook op, omdat ze informatie opslaan die sites helpt te identificeren wie u bent. Dit soort cookies worden cookies van de eerste partij genoemd, omdat ze worden gemaakt en gebruikt door de website die u hebt bezocht.

Er bestaan ook cookies van andere leveranciers. Laten we dit voorbeeld in overweging nemen om ze beter te begrijpen:

Stel dat een hypothetisch socialemedebedrijf met de naam &quot;Vrienden&quot; een knop Delen heeft die andere sites implementeren zodat Vriendengebruikers de inhoud van de site kunnen delen via de Vriendenfeed. Nu leest een gebruiker een nieuwsartikel op een nieuwswebsite dat de knop Delen gebruikt en klikt hij erop om het automatisch op zijn vriendenaccount te plaatsen.

Hiervoor haalt browser de knop Vrienden delen op van `platform.friends.com` wanneer het nieuwsartikel wordt geladen. Binnen dit proces koppelt de browser de cookies van Vrienden, die de aanmeldingsgegevens van de gebruiker bevatten, aan de aanvraag aan Vriendenservers. Hierdoor kunnen vrienden het nieuwsartikel in hun feed voor de gebruiker posten zonder dat de gebruiker zich hoeft aan te melden.

Dit is allemaal mogelijk door cookies van derden te gebruiken. In dit geval wordt het cookie van de andere fabrikant in de browser opgeslagen voor `platform.friends.com`, zodat `platform.friends.com` U kunt de advertentie namens de gebruiker in de app Vrienden plaatsen.

Als u zich even voorstelt hoe u dit gebruiksgeval zonder derdekoekjes kunt bereiken, zou de gebruiker veel handstappen moeten volgen. Ten eerste moet de gebruiker de koppeling naar het nieuwsartikel kopiëren. Ten tweede moet de gebruiker zich afzonderlijk aanmelden bij de app Vrienden. Vervolgens klikt de gebruiker op de knop Post maken. Vervolgens kopieert en plakt de gebruiker de koppeling in het tekstveld en klikt u op Plaatsen. Zoals u ziet, helpen cookies van andere leveranciers de gebruiker enorm bij het uitvoeren van handmatige stappen.

Meer in het algemeen maken cookies van derden het mogelijk dat gegevens worden opgeslagen in de browser van een gebruiker zonder dat de gebruiker een website expliciet hoeft te bezoeken.

## Beveiligingsproblemen

Hoewel cookies de gebruikerservaring en energiereclame verbeteren, kunnen ze ook beveiligingskwetsbaarheden zoals CSRF-aanvallen (Cross-Site Request Modification) introduceren. Als een gebruiker zich bijvoorbeeld aanmeldt bij een banksite om creditcardrekeningen te betalen en de site verlaat zonder zich af te melden en vervolgens in dezelfde sessie naar een kwaadaardige site bladert, kan een CSRF-aanval optreden. De kwaadaardige site kan code bevatten die een aanvraag doet naar de banksite die wordt uitgevoerd wanneer de pagina wordt geladen. Aangezien de gebruiker nog steeds op de banksite is geverifieerd, kan het sessiecookie worden gebruikt om een CSRF-aanval te starten en een gebeurtenis voor de overboeking van gelden vanuit de bankrekening van de gebruiker te starten. Dit komt omdat wanneer u een site bezoekt, alle cookies in de HTTP-aanvraag zijn opgenomen. Vanwege deze veiligheidsproblemen probeert Google ze nu te verzachten.

## Hoe werkt [!DNL Target] cookies gebruiken?

Laten we met dit alles eens kijken hoe [!DNL Target] gebruikt cookies. Voor gebruik [!DNL Target] in de eerste plaats moet u [!DNL Target] JavaScript-bibliotheek op uw site. Hierdoor kunt u een cookie van de eerste partij plaatsen in de browser van de gebruiker die uw site bezoekt. Wanneer de gebruiker op uw website werkt, kunt u gedragsgegevens en interessegegevens van de gebruiker doorgeven aan [!DNL Target] via de JavaScript-bibliotheek. De [!DNL Target] JavaScript-bibliotheek gebruikt cookies van de eerste partij om identificatiegegevens van de gebruiker te extraheren en toe te wijzen aan de gedragsgegevens en interessegegevens van de gebruiker. Deze gegevens worden vervolgens gebruikt door [!DNL Target] om uw personalisatieactiviteiten te ondersteunen.

Het doel gebruikt (soms) ook cookies van derden. Als u meerdere websites hebt die op verschillende domeinen wonen en u de gebruikersreis over die websites wilt bijhouden, kunt u cookies van derden gebruiken door interdomeintracering te gebruiken. Door domeinoverschrijdende tracering in te schakelen in het dialoogvenster [!DNL Target] JavaScript-bibliotheek, wordt uw account gestart met cookies van andere bedrijven. Aangezien een gebruiker van één domein aan een ander hoopt, communiceert browser met de achterste deelserver van [!DNL Target]en tijdens dit proces wordt een cookie van een andere fabrikant gemaakt en in de browser van de gebruiker geplaatst. Via het cookie van derden die zich in de browser van de gebruiker bevindt, [!DNL Target] kan een consistente ervaring bieden op verschillende domeinen voor één gebruiker.

## Google&#39;s nieuwe koekjesrecept

Om waarborgen rond te verstrekken wanneer de koekjes over plaatsen worden verzonden zodat de gebruikers beschermd zijn, is Google van plan om steun voor een norm toe te voegen IETF genoemd SameSite, die Webontwikkelaars vereist om koekjes met de de attributencomponent SameSite in de reeks-Koekjeskopbal te beheren.

Er zijn drie verschillende waarden die in het attribuut SameSite kunnen worden doorgegeven: Strikt, Lax of Geen.

| Waarde | Beschrijving |
| --- | --- |
| Strikt | Cookies met deze instelling zijn alleen toegankelijk wanneer u het domein bezoekt waarop de instelling oorspronkelijk is ingesteld. Met andere woorden, Strikt blokkeert volledig het cookie dat op verschillende sites wordt gebruikt. Deze optie is het beste voor toepassingen die hoge veiligheid vereisen, zoals banken. |
| Lax | Cookies met deze instelling worden alleen verzonden op aanvragen voor dezelfde site of navigatie op hoofdniveau met niet-epidemiologische HTTP-aanvragen, zoals `HTTP GET`. Daarom zou deze optie worden gebruikt als het koekje door derde partijen kan worden gebruikt, maar met een toegevoegd veiligheidsvoordeel dat gebruikers beschermt tegen worden gevierd door aanvallen CSRF. |
| Geen | Cookies met deze instelling werken op dezelfde manier als cookies vandaag de dag werken. |

Rekening houdend met het bovenstaande, introduceert Chrome 80 twee onafhankelijke montages voor gebruikers: &quot;Cookies zonder SameSite moeten beveiligd zijn.&quot; Deze instellingen worden standaard ingeschakeld in Chrome 80.

![Het dialoogvenster SameSite](/help/main/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **ZelfdeSite, standaard cookies**: Als deze optie is ingesteld, worden alle cookies die niet hetzelfde kenmerk van SameSite opgeven automatisch gedwongen om te worden gebruikt `SameSite = Lax`.
* **Cookies zonder SameSite moeten beveiligd zijn**: Cookies zonder het kenmerk SameSite of met `SameSite = None` moet veilig zijn. Beveiligen betekent in deze context dat alle browserverzoeken het HTTPS-protocol moeten volgen. Cookies die niet aan deze eis voldoen, worden afgewezen. Alle websites moeten HTTPS gebruiken om aan deze vereiste te voldoen.

## Doel volgt best practices voor beveiliging in Google

Bij Adobe willen we altijd de meest recente beste praktijken van de branche op het gebied van beveiliging en privacy ondersteunen. We zijn blij dat we kunnen aankondigen dat [!DNL Target] biedt ondersteuning voor de nieuwe beveiligings- en privacyinstellingen die Google heeft geïntroduceerd.

Voor de instelling &quot;SameSite by default cookies&quot;, [!DNL Target] U kunt zich blijven aanpassen aan uw persoonlijke wensen, zonder dat u daar invloed op hebt. [!DNL Target] gebruikt cookies van de eerste fabrikant en blijft correct functioneren als markering `SameSite = Lax` wordt toegepast door Google Chrome.

Voor de optie &#39;Cookies zonder SameSite moet veilig&#39; zijn, als u zich niet aanmeldt voor de functie voor het bijhouden van meerdere domeinen in [!DNL Target], de eerste cookies in [!DNL Target] zal blijven werken.

Als u echter de optie Interdomeintracering gebruikt voor hefboomwerking [!DNL Target] over meerdere domeinen, vereist Chrome `SameSite = None` en Veilige vlaggen die voor derdekoekjes moeten worden gebruikt. Dit betekent dat u ervoor moet zorgen dat uw sites het HTTPS-protocol gebruiken. Client-side bibliotheken in [!DNL Target] gebruikt automatisch het HTTPS-protocol en voegt het `SameSite = None` en beveilig vlaggen aan derdekoekjes in [!DNL Target] ervoor te zorgen dat alle activiteiten hun vruchten blijven afwerpen .

## Wat moet je doen?

Om te begrijpen wat u moet doen om te hebben [!DNL Target] Blijf werken voor Google Chrome 80+ gebruikers, raadpleeg de onderstaande tabel, waarvan u de volgende kolommen ziet:

* **Doel JavaScript-bibliotheek**: Als u at.js 1 gebruikt.*x* of om .js 2.*x* op uw sites.
* **SameSite standaard cookies = Ingeschakeld**: Als uw gebruikers &#39;SameSite via standaard cookies&#39; hebben ingeschakeld, hoe beïnvloedt dit dan uw toepassing en is er iets waarvoor u iets moet doen [!DNL Target] blijven werken.
* **Cookies zonder SameSite moeten beveiligd zijn = Ingeschakeld**: Als uw gebruikers &quot;Cookies zonder SameSite moeten veilig&quot;toegelaten zijn, hoe beïnvloedt het u en is er alles u moet doen hebben [!DNL Target] blijven werken.

| Doel JavaScript-bibliotheek | SameSite standaard cookies = Ingeschakeld | Cookies zonder SameSite moeten beveiligd zijn = Ingeschakeld |
| --- | --- | --- |
| te.js 1.*x* met cookie van de eerste partij. | Geen effect. | Geen effect als u geen interdomeintracering gebruikt. |
| te.js 1.*x* waarbij cross-domain tracking ingeschakeld is. | Geen effect. | U moet het HTTPS-protocol inschakelen voor uw site.<br>[!DNL Target] gebruikt een cookie van derden om gebruikers bij te houden en Google vereist dat cookies van derden `SameSite = None` en Veilige vlag. De markering voor Beveiligen vereist dat uw sites het HTTPS-protocol gebruiken. |
| te.js 2.*x* | Geen effect. | Geen effect. |

## Wat doet [!DNL Target] moeten doen?

Wat moesten we dus doen in ons platform om u te helpen te voldoen aan het nieuwe Google Chrome 80+ SameSite cookie beleid?

| Doel JavaScript-bibliotheek | SameSite standaard cookies = Ingeschakeld | Cookies zonder SameSite moeten beveiligd zijn = Ingeschakeld |
| --- | --- | --- |
| te.js 1.*x* met cookie van de eerste partij. | Geen effect. | Geen effect als u geen interdomeintracering gebruikt. |
| te.js 1.*x* waarbij cross-domain tracking ingeschakeld is. | Geen effect. | te.js 1.*x* waarbij cross-domain tracking ingeschakeld is. |
| te.js 2.*x* | Geen effect. | Geen effect. |

## Wat is het effect als u het HTTPS-protocol niet gebruikt?

Het enige gebruiksgeval dat van invloed is op u is als u de functie voor het bijhouden van meerdere domeinen gebruikt in [!DNL Target] tot en met at.js 1.*x*. Als u niet overschakelt naar HTTPS, wat een vereiste is voor Google, wordt er een piek weergegeven in unieke bezoekers over uw domeinen, omdat de cookie van derden die we gebruiken, door Google wordt verwijderd. En omdat het cookie van de andere fabrikant dan wordt verwijderd, [!DNL Target] zal geen verenigbare en gepersonaliseerde ervaring voor die gebruiker kunnen verstrekken aangezien de gebruiker van één domein aan een ander navigeert. Het cookie van derden wordt vooral gebruikt om één gebruiker te identificeren die door domeinen navigeert die u bezit.

## Conclusie

Aangezien de industrie zich inspant om een veiliger internet voor consumenten te creëren, [!DNL Adobe] is absoluut geëngageerd om onze klanten te helpen persoonlijke ervaringen op een manier te leveren die veiligheid en privacy voor eindgebruikers verzekert. Alles wat u hoeft te doen, is de bovenstaande best practices volgen en gebruikmaken van [!DNL Target] om te voldoen aan het nieuwe SameSite Cookie-beleid van Google Chrome.
