---
keywords: at.js;2.0;1.x;cookies
description: Details over hoe Adobe [!DNL Target] at.js 2.x en at.js 1.x verwerken cookies
title: at.js Cookies
feature: at.js
role: Developer
exl-id: 101be093-72fa-4f66-95bd-4b60e584a059
source-git-commit: f818125aa493be50da52f03fbbeccd1479c1193a
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# at.js cookies

Informatie over at.js 2.x en at.js 1.*x* cookie gedrag.

## at.js 2.x, gedrag voor cookie

Voor at.js versie 2.0.0, *alleen cookies van de eerste fabrikant worden ondersteund*. Net als in om.js 1.*x*, wordt het cookie van de eerste partij, &quot;mbox,&quot; opgeslagen in `clientdomain.com`, waarbij `clientdomain` is uw domein.

at.js produceert een zitting - identiteitskaart en slaat het in het koekje op. De eerste reactie bevat alle informatie over de activiteit en de `TNT` of `PC ID` door de [!DNL Target] servers. om.js schrijft dan `TNT/PC ID` naar de cookie.

De `AMCV_###@AdobeOrg` cookie van eerste partij wordt altijd ingesteld door de [!DNL Experience Cloud ID Service], hoewel de `ECID` wordt doorgegeven in [!DNL Target] verzoeken.

### Cookies van derden en interdomeintracering worden niet ondersteund

Met interdomeintracering kunt u sessies op twee verwante sites, maar met verschillende domeinen, als één sessie bekijken. U kunt een [!DNL Target] activiteit die zich uitstrekt `siteA.com` en `siteB.com` en de bezoeker zou in de zelfde ervaring blijven wanneer zij domeinen kruisen. Deze functionaliteit is gebonden aan at.js 1.*x* cookie van derden en van derden.

In at.js 1.*x*, is het cookie van de andere fabrikant opgeslagen in het dialoogvenster `[CLIENTCODE].tt.omtrdc.net` domein en cookie van eerste partij is opgeslagen in `clientdomain.com`. De eerste aanvraag retourneerde HTTP-antwoordheaders die probeerden cookies van derden in te stellen met de naam `mboxSession` en `mboxPC`, terwijl een omleidingsverzoek wordt teruggestuurd met een extra parameter (`mboxXDomainCheck=true`). Als de browser cookies van derden accepteerde, bevat de omleidingsaanvraag deze cookies en is de aanbieding geretourneerd. Deze workflow was mogelijk omdat om .js 1.*x* heeft de HTTP-GET-methode gebruikt.

In at.js 2.x wordt HTTP-GET echter niet meer gebruikt en wordt in plaats daarvan HTTP-POST gebruikt. HTTP-POST wordt nu gebruikt via at.js om JSON-nuttige taken te verzenden naar [!DNL Target] Edge-servers in plaats van parameters voor sleutelwaarden. Dit betekent dat de omleidingsaanvraag om te controleren of een browser cookies van derden ondersteunt, nu wordt afgebroken. Dit komt doordat HTTP-GET-aanvragen epidemische transacties zijn, terwijl HTTP-POST niet-epidemiologisch is en niet willekeurig mag worden herhaald.

Daarom worden cookies van derden en interdomeintracering niet ondersteund in at.js 2.0.0.

## te.js 1.*x* cookie, gedrag {#at-js-1x-cookie-behavior}

Voor at.js versies 1.*x*, is het gedrag van de cookie afhankelijk van het feit of het een cookie van de eerste fabrikant, een cookie van een derde partij met een cookie van de eerste partij of alleen een cookie van een derde partij is.

### Wanneer cookies van andere leveranciers of leveranciers gebruiken

De site-instelling bepaalt welke cookies u wilt gebruiken. Het is handig om te begrijpen hoe Target werkt wanneer u cookies van andere leveranciers of leveranciers probeert te begrijpen. Zie [Hoe Adobe Target werkt](/help/main/c-intro/how-target-works.md) voor meer informatie .

Er zijn drie hoofdtoepassingen voor cookies:

1. Eén domein.

   Al uw tests vinden plaats binnen één top-level domein (`www.domain.com`, `store.domain.com`, `anysub.domain.com`, enz.).

   Gebruik alleen cookies van de eerste fabrikant. Dit is de standaardinstelling.

1. De gebruikers kruisen domeinen en u wilt hun gedrag over deze domeinen volgen en testen.

   Voorbeeld: Een gebruiker komt naar uw site om te winkelen, maar checkt dit uit via Yahoo-winkels. Drie benaderingen (werk samen met uw accountvertegenwoordiger om de beste aanpak te bepalen):

   * Cookies van de eerste en derde partij inschakelen.
   * Schakel alleen derden in (zeer zelden, maar heeft het voordeel dat u het cookie at.js buiten uw domein houdt).
   * Alleen cookies van eerste partij inschakelen en doorgeven `mboxSession` parameter wanneer het oversteken van domein.

      De `mboxSession` parameter moet worden doorgegeven aan een bestemmingspagina met de verwijzing at.js. Het kan geen tussenliggende redirector-pagina zijn.

1. U gebruikt alleen adboxes of FlashBox op een externe site.

   Twee benaderingen (werk met uw manager van de cliëntdiensten om de beste benadering te bepalen):

   * Cookies van eerste en van derden inschakelen.

      Cookies van de eerste en van derden zijn vereist voor FlashBox en dynamische creatieve producten.

   * Schakel alleen cookies van derden in.

      Deze aanpak geldt alleen in het zeldzame geval waarin adBox-implementaties worden gebruikt zonder dat er een onsite doelversie van de implementaties wordt gemaakt.

### Cookie-gedrag van de eerste partij

Het cookie van de eerste partij wordt opgeslagen in `clientdomain.com`, waarbij `clientdomain` is uw domein.

at.js produceert een `mboxSession ID` en slaat het op in het cookie. De eerste reactie bevat de aanbieding en de JavaScript-code voor het opslaan van de `mboxPC ID` gegenereerd door de toepassing, in het cookie.

>[!NOTE]
>
>De `AMCV_###@AdobeOrg` cookie van eerste partij wordt altijd ingesteld met de [!DNL Experience Cloud Visitor ID].

### Cookiegedrag van derden

Het cookie van de andere fabrikant wordt opgeslagen in `clientcode.tt.omtrdc.net` en de cookie van de eerste partij wordt opgeslagen in `clientdomain.com`, waarbij `clientdomain` is uw domein.

at.js produceert een `mboxSession ID`. De eerste locatieaanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met een naam in te stellen `mboxSession` en `mboxPC` en een omleidingsverzoek wordt teruggestuurd met een extra parameter (`mboxXDomainCheck=true`).

Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de aanbieding geretourneerd.

Als de browser cookies van derden afwijst, worden deze cookies niet opgenomen in de omleidingsaanvraag en wordt standaardinhoud weergegeven voor alle locaties op de pagina. Omdat er geen cookies zijn ingesteld, vindt hetzelfde proces hierboven opnieuw plaats bij elke paginaaanvraag.

### Cookie-gedrag van derden en van derden

Het cookie van de andere fabrikant wordt opgeslagen in `clientcode.tt.omtrdc.net` en de cookie van de eerste partij wordt opgeslagen in `clientdomain.com`, waarbij `clientdomain` is uw domein.

at.js produceert een `mboxSession ID`. De eerste locatieaanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met een naam in te stellen `mboxSession` en `mboxPC`en er wordt een omleidingsverzoek teruggestuurd met een extra parameter (`mboxXDomainCheck=true`).

Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de aanbieding geretourneerd.

Sommige browsers wijzen cookies van derden af. Als het cookie van een andere fabrikant wordt geblokkeerd, werkt het cookie van de eerste partij nog steeds. [!DNL Target] pogingen om het cookie van derden in te stellen, en als dit niet het geval is, dan [!DNL Target] kan alleen het specifieke domein van de client bijhouden. Interdomeintracering werkt niet als de derde wordt geblokkeerd, tenzij de `mboxSession` wordt toegevoegd in de verbinding die domeinen kruist. In dit geval wordt een ander cookie van de eerste fabrikant ingesteld en gesynchroniseerd met het cookie van het vorige domein.

## Cookie-instellingen

Het cookie heeft verschillende standaardinstellingen. U kunt deze instellingen desgewenst wijzigen, met uitzondering van de duur van het cookie. Vraag uw accountvertegenwoordiger wanneer u de cookie-instellingen wijzigt.

| Instelling | Informatie |
|--- |--- |
| Naam cookie | mbox. |
| Cookie-domein | Het tweede en bovenste niveau van de domeinen waaruit u de inhoud aanbiedt. Omdat het van het domein van uw bedrijf wordt gediend, is het koekje een eerste partijkoekje. Voorbeeld: `mycompany.com`. |
| Serverdomein | `clientcode.tt.omtrdc.net`, met de clientcode voor uw account. |
| Duur van cookie | Het cookie blijft twee jaar na de laatste aanmelding in de browser van de bezoeker staan.<br>De `deviceIdLifetime` instelling kan worden overschreven in [at.js versie 2.3.1 of hoger](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). Zie voor meer informatie [targetGlobalSettings()](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). |
| P3P-beleid | De cookie wordt gepubliceerd met een P3P-beleid, zoals vereist door de standaardinstelling in de meeste browsers. Een P3P-beleid geeft aan welke browser de cookie aanbiedt en hoe de informatie wordt gebruikt. |

Het cookie houdt een aantal waarden bij om te beheren hoe uw bezoekers campagnes ervaren:

| Waarde | Definitie |
|--- |--- |
| sessie-id | Een unieke id voor een gebruikerssessie. Standaard duurt dit 30 minuten. |
| pc-id | Een halfpermanente id voor de browser van een bezoeker. Laadt 14 dagen. |
| at_check | Een eenvoudige testwaarde die wordt gebruikt om te bepalen of een bezoeker cookies ondersteunt. Stel de instellingen in wanneer een bezoeker een pagina aanvraagt. |
| disable | Instellen als de laadtijd van de bezoeker de time-out overschrijdt die is geconfigureerd in het dialoogvenster [!DNL Adobe Experience Platform Web SDK] of het bestand at.js. Standaard duurt dit 1 uur. |

## Gevolgen voor [!DNL Target] voor Safari-bezoekers vanwege wijzigingen in het bijhouden van Apple WebKit

Houd rekening met het volgende:

### Hoe werkt Adobe [!DNL Target] Werk volgen?

| Cookies | Details |
|--- |--- |
| Domeinen van eerste partij | Dit is de standaardimplementatie voor de klanten van het Doel.  De &quot;mbox&quot;koekjes wordt geplaatst in het domein van de klant. |
| Tekstspatiëring van derden | Tekstspatiëring door derden is belangrijk voor reclame en het richten van gebruiksgevallen in Target en Adobe Audience Manager (AAM).  Bij het bijhouden van externe gegevens zijn technieken voor scripts die verwijzen naar andere sites, vereist.  Het doel gebruikt twee cookies, &quot;mboxSession&quot; en &quot;mboxPC&quot; ingesteld in het dialoogvenster `clientcode.tt.omtrd.net` domein. |

### Wat is de aanpak van Apple?

Uit Apple:

&quot;Intelligente preventie van tracering is een nieuwe WebKit-functie die het opsporen van gegevens via andere sites beperkt door cookies en andere websitegegevens verder te beperken.&quot;

&quot;Dit wordt intersite tracering genoemd en het cookie dat wordt gebruikt door `example-tracker.com` wordt een cookie van een andere fabrikant genoemd. In onze test vonden we populaire websites met meer dan 70 van dergelijke trackers, die allemaal ongemerkt gegevens over gebruikers verzamelen.&quot;

| Benadering | Details |
|--- |--- |
| Intelligente traceringspreventie | Zie voor meer informatie [Intelligente traceringspreventie](https://webkit.org/blog/7675/intelligent-tracking-prevention/) op de WebKit Open Source Web Browser Engine website. |
| Cookies | Hoe Safari cookies verwerkt:<ul><li>Cookies van derden die zich niet op een domein bevinden waartoe de gebruiker rechtstreeks toegang heeft, worden nooit opgeslagen. Dit gedrag is niet nieuw. Cookies van derden worden al niet ondersteund in Safari.</li><li>Cookies van derden die zijn ingesteld op een domein waartoe de gebruiker rechtstreeks toegang heeft, worden na 24 uur gewist.</li><li>Cookies van de eerste partij worden na 30 dagen gezuiverd als dat domein van de eerste partij als het volgen van gebruikers over plaatsen is geclassificeerd. Deze kwestie zou op grote bedrijven kunnen van toepassing zijn die gebruikers naar verschillende domeinen online verzenden. Apple heeft niet duidelijk gemaakt hoe deze domeinen precies zullen worden geclassificeerd, of hoe een domein kan bepalen als zij als het volgen van gebruikers dwars-plaats zijn geclassificeerd.</li></ul> |
| Machine die leert domeinen te identificeren die naar andere sites verwijzen | Uit Apple:<br>Computer Learning Classifier: Een machine het leren model wordt gebruikt om te classificeren welke hoogste privé-gecontroleerde domeinen de capaciteit hebben om de gebruiker dwars-plaats te volgen, die op de verzamelde statistieken wordt gebaseerd. Van de verschillende verzamelde statistieken bleken drie vectoren een sterk signaal te hebben voor classificatie op basis van de huidige volgpraktijken: subresource onder aantal unieke domeinen, subframe onder aantal unieke domeinen en aantal unieke domeinen waarnaar opnieuw is omgeleid. Alle gegevens verzamelen en classificeren gebeurt op het apparaat.<br>Nochtans, als de gebruiker met example.com als hoogste domein interactie heeft, die vaak als eerste-partijdomein wordt bedoeld, beschouwt de Intelligente het Volgen Preventie het een signaal dat de gebruiker in de website geinteresseerd is en tijdelijk zijn gedrag zoals die in deze chronologie wordt getoond aanpast:<br>Als de gebruiker de laatste 24 uur op example.com heeft gereageerd, zijn cookies beschikbaar wanneer `example.com` is een derde. Dit staat voor &quot;Sign in met mijn rekening van X op Y&quot;login scenario&#39;s toe.<ul><li>Domeinen die als domein op het hoogste niveau worden bezocht, worden niet beïnvloed. Sites zoals bijvoorbeeld OKTA</li><li>Identificeert domeinen die subdomein of subframe zijn van de huidige pagina over meerdere unieke domeinen.</li></ul> |

### Hoe wordt Adobe beïnvloed?

| Betrokken functionaliteit | Details |
|--- |--- |
| Ondersteuning voor uitschakelen | Wijzigingen in WebKit voor Apple worden afgebroken.<br>De optie voor het niet volgen van doelen gebruikt een cookie in het dialoogvenster `clientcode.tt.omtrdc.net` domein. Zie voor meer informatie [Privacy](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md).<br>Doel ondersteunt twee opt-outs:<ul><li>Eén per client (de client beheert de koppeling om te weigeren).</li><li>Een via Adobe die de gebruiker uit alle functionaliteit van het Doel voor alle klanten kiest.</li></ul>Beide methoden gebruiken het cookie van derden. |
| Doelactiviteiten | Klanten kunnen hun [lengte van profielleven](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) voor hun Target-accounts: maximaal 90 dagen. Het probleem is dat als de profiellevensduur van de account langer is dan 30 dagen en de cookie van de eerste partij wordt gewist omdat het domein van de klant is gemarkeerd als het controleren van gebruikers naar andere sites, het gedrag voor Safari-bezoekers wordt beïnvloed in de volgende gebieden in Target:<br>**Doelrapporten**: Als een gebruiker Safari in een activiteit ingaat, na 30 dagen terugkeert, en dan omzet, telt die gebruiker als twee bezoekers en één omzetting.<br>Dit gedrag is het zelfde voor activiteiten die Analytics gebruiken zoals de rapporteringsbron (A4T).<br>**Profiel en activiteitenlidmaatschap**:<ul><li>Profielgegevens worden gewist wanneer het cookie van de eerste partij verloopt.</li><li>Het lidmaatschap van de activiteit wordt gewist wanneer het eerste-partijkoekje verloopt.</li><li> Het doel werkt niet in Safari voor accounts die een cookie-implementatie van een andere fabrikant of een cookie-implementatie van een andere fabrikant gebruiken. Dit gedrag is niet nieuw. Safari heeft cookies van derden al een tijdje niet toegestaan.</li></ul><br>**Suggesties**: Als er een zorg is dat het klantendomein als één het volgen bezoekers dwars-zitting zou kunnen worden gemerkt, is het het veiligst om het profielleven aan 30 dagen of minder in Doel te plaatsen. Dit zorgt ervoor dat gebruikers op dezelfde manier worden bijgehouden in Safari en alle andere browsers. |
