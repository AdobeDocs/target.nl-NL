---
keywords: google;samesite;cookies;chroom 80;ietf
description: Ontdek hoe Adobe Target omgaat met de SameSite IETF-standaard die is geïntroduceerd met Google Chrome versie 80 en wat u moet doen om aan dit beleid te voldoen.
title: Hoe handelt Target het Samesite Cookie-beleid van Google af?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '2050'
ht-degree: 0%

---


# Google Chrome SameSite-cookiebeleid

Google zal standaard een nieuw beleid voor cookies gaan toepassen voor gebruikers die beginnen met Chrome 80, dat begin 2020 wordt gepubliceerd. In dit artikel wordt uitgelegd wat u allemaal moet weten over het nieuwe beleid voor SameSite-cookies, hoe [!DNL Adobe Target] dit beleid ondersteunt en hoe u [!DNL Target] kunt gebruiken om te voldoen aan het nieuwe beleid voor SameSite-cookie van Google Chrome.

Vanaf Chrome 80 moeten webontwikkelaars expliciet opgeven welke cookies op verschillende websites kunnen worden gebruikt. Dit is het eerste van de vele aankondigingen die Google voornemens is te doen om de privacy en veiligheid op het web te verbeteren.

Gezien het feit dat Facebook op het punt van privacy en veiligheid op de proppen is gekomen, hebben andere belangrijke spelers zoals Apple en nu Google snel geprofiteerd van de mogelijkheid om nieuwe identiteiten te creëren als privacy- en veiligheidskampioen. Apple leidde het pakket door begin dit jaar via ITP 2.1 en onlangs, ITP 2.2, wijzigingen aan te kondigen in zijn beleid voor cookies. In ITP 2.1 blokkeert Apple cookies van derden volledig en worden cookies die zijn gemaakt op de browser slechts zeven dagen bewaard. In ITP 2.2 worden cookies slechts één dag bewaard. De aankondiging van Google is bij lange na niet zo agressief als die van Apple, maar het is de eerste stap naar hetzelfde einddoel. Zie [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md) voor meer informatie over het beleid van Apple.

## Wat zijn cookies en hoe worden ze gebruikt?

Voordat we gaan duiken in de wijzigingen die Google aanbrengt in zijn beleid voor cookies, moeten we ons afvragen wat cookies zijn en hoe ze worden gebruikt. Eenvoudig gezet, zijn de koekjes kleine tekstdossiers die in Webbrowser worden opgeslagen die worden gebruikt om gebruikersattributen te herinneren.

Cookies zijn belangrijk omdat ze de gebruiker meer doen terwijl ze op het web surfen. Als u bijvoorbeeld boodschappen doet op een eCommerce-website en iets toevoegt aan uw winkelwagentje maar zich niet aanmeldt of koopt tijdens dat bezoek, onthouden cookies uw items en houden ze in uw winkelwagentje voor uw volgende bezoek. Of stel je voor dat je je gebruikersnaam en wachtwoord telkens opnieuw moet invoeren als je je favoriete website van sociale media bezoekt. Cookies lossen dat probleem ook op, omdat ze informatie opslaan die sites helpt te identificeren wie u bent. Dit soort cookies worden cookies van de eerste partij genoemd, omdat ze worden gemaakt en gebruikt door de website die u hebt bezocht.

Er bestaan ook cookies van andere leveranciers. Laten we dit voorbeeld in overweging nemen om ze beter te begrijpen:

Stel dat een hypothetisch socialemedebedrijf met de naam &quot;Vrienden&quot; een knop Delen heeft die andere sites implementeren zodat Vriendengebruikers de inhoud van de site kunnen delen via de Vriendenfeed. Nu leest een gebruiker een nieuwsartikel op een nieuwswebsite dat de knop Delen gebruikt en klikt hij erop om het automatisch op zijn vriendenaccount te plaatsen.

Hiervoor haalt browser de knoop van het Aandeel van Vrienden van `platform.friends.com` wanneer het nieuwsartikel wordt geladen. Binnen dit proces koppelt de browser de cookies van Vrienden, die de aanmeldingsgegevens van de gebruiker bevatten, aan de aanvraag aan Vriendenservers. Hierdoor kunnen vrienden het nieuwsartikel in hun feed voor de gebruiker posten zonder dat de gebruiker zich hoeft aan te melden.

Dit is allemaal mogelijk door cookies van derden te gebruiken. In dit geval wordt het cookie van de andere fabrikant in de browser opgeslagen voor `platform.friends.com`, zodat `platform.friends.com` de cookie namens de gebruiker in de vriendenapp kan plaatsen.

Als u zich even voorstelt hoe u dit gebruiksgeval zonder derdekoekjes kunt bereiken, zou de gebruiker veel handstappen moeten volgen. Ten eerste moet de gebruiker de koppeling naar het nieuwsartikel kopiëren. Ten tweede moet de gebruiker zich afzonderlijk aanmelden bij de app Vrienden. Vervolgens klikt de gebruiker op de knop Post maken. Vervolgens kopieert en plakt de gebruiker de koppeling in het tekstveld en klikt u op Plaatsen. Zoals u ziet, helpen cookies van andere leveranciers de gebruiker enorm bij het uitvoeren van handmatige stappen.

Meer in het algemeen maken cookies van derden het mogelijk dat gegevens worden opgeslagen in de browser van een gebruiker zonder dat de gebruiker een website expliciet hoeft te bezoeken.

## Beveiligingsproblemen

Hoewel cookies de gebruikerservaring en energiereclame verbeteren, kunnen ze ook beveiligingskwetsbaarheden zoals CSRF-aanvallen (Cross-Site Request Modification) introduceren. Als een gebruiker zich bijvoorbeeld aanmeldt bij een banksite om creditcardrekeningen te betalen en de site verlaat zonder zich af te melden en vervolgens in dezelfde sessie naar een kwaadaardige site bladert, kan een CSRF-aanval optreden. De kwaadaardige site kan code bevatten die een aanvraag doet naar de banksite die wordt uitgevoerd wanneer de pagina wordt geladen. Aangezien de gebruiker nog steeds op de banksite is geverifieerd, kan het sessiecookie worden gebruikt om een CSRF-aanval te starten en een gebeurtenis voor de overboeking van gelden vanuit de bankrekening van de gebruiker te starten. Dit komt omdat wanneer u een site bezoekt, alle cookies in de HTTP-aanvraag zijn opgenomen. Vanwege deze veiligheidsproblemen probeert Google ze nu te verzachten.

## Hoe gebruikt Target cookies?

Met al deze elementen kunt u zien hoe cookies worden gebruikt. [!DNL Target] Als u [!DNL Target] in de eerste plaats wilt gebruiken, moet u de JavaScript-bibliotheek [!DNL Target] op uw site installeren. Hierdoor kunt u een cookie van de eerste partij plaatsen in de browser van de gebruiker die uw site bezoekt. Wanneer de gebruiker op uw website werkt, kunt u de gedrags- en interessegegevens van de gebruiker doorgeven aan [!DNL Target] via de JavaScript-bibliotheek. De JavaScript-bibliotheek [!DNL Target] gebruikt cookies van de eerste partij om identificatiegegevens over de gebruiker op te halen en toe te wijzen aan de gedragsgegevens en interessegegevens van de gebruiker. Deze gegevens worden vervolgens door [!DNL Target] gebruikt om uw personalisatieactiviteiten te stimuleren.

Het doel gebruikt (soms) ook cookies van derden. Als u meerdere websites hebt die op verschillende domeinen wonen en u de gebruikersreis over die websites wilt bijhouden, kunt u cookies van derden gebruiken door interdomeintracering te gebruiken. Als u het bijhouden van bestanden tussen domeinen inschakelt in de JavaScript-bibliotheek [!DNL Target], wordt het gebruik van cookies van derden voor uw account gestart. Aangezien een gebruiker van één domein aan een ander hoopt, communiceert browser met de achterste deelserver van [!DNL Target], en in dit proces, wordt een derdekoekje gecreeerd en op browser van de gebruiker geplaatst. Met behulp van het cookie van derden dat zich in de browser van de gebruiker bevindt, kan [!DNL Target] een consistente ervaring op verschillende domeinen bieden voor één gebruiker.

## Google&#39;s nieuwe kookrecept

Om waarborgen rond te verstrekken wanneer de koekjes over plaatsen worden verzonden zodat de gebruikers beschermd zijn, is Google van plan om steun voor een norm toe te voegen IETF genoemd SameSite, die Webontwikkelaars vereist om koekjes met de ZelfdeSite attributencomponent in de reeks-Koekjeskopbal te beheren.

Er zijn drie verschillende waarden die in het attribuut SameSite kunnen worden doorgegeven: Strikt, Lax of Geen.

| Waarde | Beschrijving |
| --- | --- |
| Strikt | Cookies met deze instelling zijn alleen toegankelijk wanneer u het domein bezoekt waarop de instelling oorspronkelijk is ingesteld. Met andere woorden, Strict blokkeert volledig het koekje van wordt gebruikt over plaatsen. Deze optie is het beste voor toepassingen die hoge veiligheid vereisen, zoals banken. |
| Lax | Cookies met deze instelling worden alleen verzonden op aanvragen voor dezelfde site of navigatie op hoofdniveau met niet-epidemiologische HTTP-aanvragen, zoals `HTTP GET`. Daarom zou deze optie worden gebruikt als het koekje door derde partijen kan worden gebruikt, maar met een toegevoegd veiligheidsvoordeel dat gebruikers beschermt tegen worden gevierd door aanvallen CSRF. |
| Geen | Cookies met deze instelling werken op dezelfde manier als cookies vandaag de dag werken. |

Rekening houdend met het bovenstaande, introduceert Chrome 80 twee onafhankelijke montages voor gebruikers: &quot;Cookies zonder SameSite moeten beveiligd zijn.&quot; Deze instellingen worden standaard ingeschakeld in Chrome 80.

![Het dialoogvenster SameSite](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

* **SameSite standaard cookies**: Als deze optie is ingesteld, worden alle cookies die niet hetzelfde kenmerk van SameSite opgeven, automatisch gedwongen om te gebruiken  `SameSite = Lax`.
* **Cookies zonder SameSite moeten veilig** zijn: Als deze optie is ingesteld,  `SameSite = None` moeten cookies zonder het kenmerk SameSite of met de functie Secure. Beveiligen betekent in deze context dat alle browserverzoeken het HTTPS-protocol moeten volgen. Cookies die niet aan deze eis voldoen, worden afgewezen. Alle websites moeten HTTPS gebruiken om aan deze vereiste te voldoen.

## Doel volgt de best practices van Google op het gebied van beveiliging

Bij Adobe willen we altijd de meest recente beste praktijken van de branche op het gebied van beveiliging en privacy ondersteunen. We zijn blij te kunnen aankondigen dat [!DNL Target] de nieuwe beveiligings- en privacyinstellingen ondersteunt die door Google zijn geïntroduceerd.

Voor de instelling &quot;SameSite by default cookies&quot; blijft [!DNL Target] personalisatie leveren zonder enige invloed en tussenkomst van u. [!DNL Target] gebruikt cookies van de eerste partij en blijft correct werken naarmate de markering door Google Chrome  `SameSite = Lax` wordt toegepast.

Voor de optie &quot;Cookies zonder SameSite moet veilig zijn&quot;, als u zich niet aanmeldt voor de functie voor het bijhouden van meerdere domeinen in [!DNL Target], blijven de cookies van de eerste partij in [!DNL Target] werken.

Wanneer u echter de optie voor domeinoverschrijdende tracering gebruikt om [!DNL Target] in meerdere domeinen te gebruiken, vereist Chrome `SameSite = None`- en Secure-vlaggen die moeten worden gebruikt voor cookies van derden. Dit betekent dat u ervoor moet zorgen dat uw sites het HTTPS-protocol gebruiken. Client-side bibliotheken in [!DNL Target] gebruiken automatisch het HTTPS-protocol en voegen de `SameSite = None`- en Secure-vlaggen toe aan cookies van derden in [!DNL Target] om ervoor te zorgen dat alle activiteiten blijven uitvoeren.

## Wat moet je doen?

Als u wilt begrijpen wat u moet doen om ervoor te zorgen dat [!DNL Target] blijft werken voor Google Chrome 80+-gebruikers, raadpleegt u de onderstaande tabel, waarvan u de volgende kolommen ziet:

* **Doel JavaScript-bibliotheek**: Als u mbox.js, bij.js 1 gebruikt.*x*, of at.js 2.** Sluit uw sites af.
* **SameSite by default cookies = Enabled**: Als uw gebruikers &quot;SameSite door gebrek toegelaten koekjes&quot;hebben, hoe beïnvloedt het u en is er om het even wat u moet doen om  [!DNL Target] te blijven werken.
* **Cookies zonder SameSite moeten secure = Enabled** zijn: Als uw gebruikers &quot;Cookies zonder SameSite moeten veilig&quot;toegelaten zijn, hoe beïnvloedt het u en is er om het even wat u moet doen  [!DNL Target] blijven werken.

| Doel JavaScript-bibliotheek | SameSite standaard cookies = Ingeschakeld | Cookies zonder SameSite moeten beveiligd zijn = Ingeschakeld |
| --- | --- | --- |
| mbox.js met alleen cookie van de eerste fabrikant. | Geen effect. | Geen effect als u geen interdomeintracering gebruikt. |
| mbox.js waarvoor cross-domain tracking is ingeschakeld. | Geen effect. | U moet het HTTPS-protocol inschakelen voor uw site.<br>[!DNL Target] gebruikt een cookie van een andere fabrikant om gebruikers bij te houden en Google vereist dat cookies van andere bedrijven markering  `SameSite = None` en Beveiliging hebben. De markering voor Beveiligen vereist dat uw sites het HTTPS-protocol gebruiken. |
| te.js 1.** Exwith first-party cookie. | Geen effect. | Geen effect als u geen interdomeintracering gebruikt. |
| te.js 1.** xwith cross-domain tracking enabled. | Geen effect. | U moet het HTTPS-protocol inschakelen voor uw site.<br>[!DNL Target] gebruikt een cookie van een andere fabrikant om gebruikers bij te houden en Google vereist dat cookies van andere bedrijven markering  `SameSite = None` en Beveiliging hebben. De markering voor Beveiligen vereist dat uw sites het HTTPS-protocol gebruiken. |
| te.js 2.*x* | Geen effect. | Geen effect. |

## Wat moet Target doen?

Wat moesten we dus doen in ons platform om u te helpen te voldoen aan het nieuwe Google Chrome 80+ SameSite cookie beleid?

| Doel JavaScript-bibliotheek | SameSite standaard cookies = Ingeschakeld | Cookies zonder SameSite moeten beveiligd zijn = Ingeschakeld |
| --- | --- | --- |
| mbox.js met alleen cookie van de eerste fabrikant. | Geen effect. | Geen effect als u geen interdomeintracering gebruikt. |
| mbox.js waarvoor cross-domain tracking is ingeschakeld. | Geen effect. | [!DNL Target] voegt  `SameSite = None` en Veilige vlag aan het derdekoekje toe wanneer de  [!DNL Target] servers worden geroepen. |
| te.js 1.** Exwith first-party cookie. | Geen effect. | Geen effect als u geen interdomeintracering gebruikt. |
| te.js 1.** xwith cross-domain tracking enabled. | Geen effect. | te.js 1.** xwith cross-domain tracking enabled. |
| te.js 2.*x* | Geen effect. | Geen effect. |

## Wat is het effect als u het HTTPS-protocol niet gebruikt?

Het enige gebruiksgeval dat u zal beïnvloeden is als u de dwars-domein volgende eigenschap in [!DNL Target] door mbox.js of at.js 1 gebruikt.*x*. Als u niet overschakelt naar HTTPS, wat een vereiste is voor Google, wordt er een spiek weergegeven in unieke bezoekers over uw domeinen, omdat de cookie van derden die we gebruiken, door Google wordt verwijderd. En omdat het derdekoekje zal worden gelaten vallen, [!DNL Target] zal niet een verenigbare en gepersonaliseerde ervaring voor die gebruiker kunnen verstrekken aangezien de gebruiker van één domein aan een ander navigeert. Het cookie van derden wordt vooral gebruikt om één gebruiker te identificeren die door domeinen navigeert die u bezit.

## Conclusie

Aangezien de branche zich inzet voor het creëren van een veiliger web voor consumenten, is [!DNL Adobe] absoluut geëngageerd om onze klanten te helpen persoonlijke ervaringen te leveren op een manier die veiligheid en privacy voor eindgebruikers verzekert. U hoeft alleen de bovenstaande best practices te volgen en [!DNL Target] te gebruiken om te voldoen aan het nieuwe beleid voor SameSite Cookie van Google Chrome.
