---
keywords: at.js;2.0;1.x;cookies
description: Informatie over hoe Adobe Target op 2.js 2.x en at.js 1.x cookies verwerkt
title: at.js Cookies
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 0%

---


# at.js cookies {#at-js-cookies}

Informatie over at.js 2.x en at.js 1.** xcookie gedrag.

## at.js 2.x, gedrag voor cookie

Voor at.js versie 2.0.0, *slechts worden de eerste-partijkoekjes gesteund*. Net als in om.js 1.*x*, het eerste cookie, &quot;mbox,&quot; wordt opgeslagen in  `clientdomain.com`, waar  `clientdomain` je domein is.

at.js produceert een zitting - identiteitskaart en slaat het in het koekje op. De eerste reactie bevat activiteitsinformatie, evenals de `TNT` of `PC ID` die door de [!DNL Target] servers worden gegenereerd. at.js schrijft dan `TNT/PC ID` aan het koekje.

Het `AMCV_###@AdobeOrg` eersteklas koekje wordt altijd geplaatst door [!DNL Experience Cloud ID Service], hoewel `ECID` in [!DNL Target] verzoeken wordt overgegaan.

### Cookies van derden en interdomeintracering worden niet ondersteund

Met interdomeintracering kunt u sessies op twee verwante sites, maar met verschillende domeinen, als één sessie bekijken. U zou een [!DNL Target] activiteit kunnen tot stand brengen die `siteA.com` en `siteB.com` overspant en de bezoeker in de zelfde ervaring zou blijven wanneer zij domeinen kruisen. Deze functionaliteit is gebonden aan at.js 1.*Cookie-gedrag van* derden en van derden.

In at.js 1.*x*, werd het derdekoekje opgeslagen in het  `[CLIENTCODE].tt.omtrdc.net` domein en het eerste-partijkoekje werd opgeslagen in  `clientdomain.com`. Het eerste verzoek gaf de antwoordkopballen van HTTP terug die probeerden om derdekoekjes te plaatsen genoemd `mboxSession` en `mboxPC`, terwijl een omleidingsverzoek met een extra parameter (`mboxXDomainCheck=true`) wordt teruggestuurd. Als de browser cookies van derden accepteerde, bevat de omleidingsaanvraag deze cookies en is de aanbieding geretourneerd. Deze workflow was mogelijk omdat om .js 1.** heeft de methode HTTP-GET gebruikt.

In at.js 2.x wordt HTTP-GET echter niet meer gebruikt en wordt in plaats daarvan HTTP-POST gebruikt. De POST van HTTP wordt nu gebruikt via at.js om JSON nuttige lading naar [!DNL Target] randservers in plaats van zeer belangrijke parameters te verzenden. Dit betekent dat de omleidingsaanvraag om te controleren of een browser cookies van derden ondersteunt, nu wordt afgebroken. Dit komt doordat HTTP-GET-aanvragen epidemische transacties zijn, terwijl HTTP-POST niet-epidemiologisch is en niet willekeurig mag worden herhaald.

Daarom worden cookies van derden en interdomeintracering niet ondersteund in at.js 2.0.0.

## te.js 1.** xcookie, gedrag  {#at-js-1x-cookie-behavior}

Voor at.js versies 1.*x*, hangt het koekjesgedrag af van of het een eerderangs koekje, een derdekoekje met een eerstepartijkoekje, of een derdekoekje alleen is.

### Wanneer cookies van andere leveranciers of leveranciers gebruiken

De site-instelling bepaalt welke cookies u wilt gebruiken. Het is handig om te begrijpen hoe Target werkt wanneer u cookies van andere leveranciers of leveranciers probeert te begrijpen. Zie [Hoe werkt Adobe Target](/help/c-intro/how-target-works.md) voor meer informatie.

Er zijn drie hoofdtoepassingen voor cookies:

1. Eén domein.

   Al uw tests vinden plaats binnen één top-level domein (`www.domain.com`, `store.domain.com`, `anysub.domain.com`, etc.).

   Gebruik alleen cookies van de eerste fabrikant. Dit is de standaardinstelling.

1. De gebruikers kruisen domeinen en u wilt hun gedrag over deze domeinen volgen en testen.

   Voorbeeld: Een gebruiker komt naar uw site om te winkelen, maar checkt dit uit via Yahoo-winkels. Drie benaderingen (werk samen met uw accountvertegenwoordiger om de beste aanpak te bepalen):

   * Cookies van de eerste en derde partij inschakelen.
   * Schakel alleen derden in (zeer zelden, maar heeft het voordeel dat u het cookie at.js buiten uw domein houdt).
   * Schakel alleen cookies van de eerste partij in en geef `mboxSession`-parameter door wanneer u het domein overschrijdt.

      De parameter `mboxSession` moet worden doorgegeven aan een bestemmingspagina met de verwijzing at.js. Het kan geen tussenliggende redirector-pagina zijn.

1. U gebruikt alleen adboxes of FlashBox op een externe site.

   Twee benaderingen (werk met uw manager van de cliëntdiensten om de beste benadering te bepalen):

   * Cookies van eerste en van derden inschakelen.

      Cookies van de eerste en van derden zijn vereist voor FlashBox en dynamische creatieve producten.

   * Schakel alleen cookies van derden in.

      Deze aanpak geldt alleen in het zeldzame geval waarin adBox-implementaties worden gebruikt zonder dat er een onsite doelversie van de implementaties wordt gemaakt.

### Cookie-gedrag van de eerste partij

Het cookie van de eerste partij wordt opgeslagen in `clientdomain.com`, waarbij `clientdomain` uw domein is.

at.js produceert een `mboxSession ID` en slaat het in het koekje op. De eerste reactie bevat de aanbieding en het JavaScript om de `mboxPC ID` die door de toepassing wordt gegenereerd, in het cookie op te slaan.

>[!NOTE]
>
>Het cookie `AMCV_###@AdobeOrg` van de eerste partij wordt altijd ingesteld met [!DNL Experience Cloud Visitor ID].

### Cookiegedrag van derden

Het cookie van de andere fabrikant wordt opgeslagen in `clientcode.tt.omtrdc.net` en het cookie van de eerste partij wordt opgeslagen in `clientdomain.com`, waarbij `clientdomain` uw domein is.

at.js produceert een `mboxSession ID`. De eerste plaatsaanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met de naam `mboxSession` en `mboxPC` in te stellen en een omleidingsverzoek wordt teruggestuurd met een extra parameter (`mboxXDomainCheck=true`).

Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de aanbieding geretourneerd.

Als de browser cookies van derden afwijst, worden deze cookies niet opgenomen in de omleidingsaanvraag en wordt standaardinhoud weergegeven voor alle locaties op de pagina. Omdat er geen cookies zijn ingesteld, vindt hetzelfde proces hierboven opnieuw plaats bij elke paginaaanvraag.

### Cookie-gedrag van derden en van derden

Het cookie van de andere fabrikant wordt opgeslagen in `clientcode.tt.omtrdc.net` en het cookie van de eerste partij wordt opgeslagen in `clientdomain.com`, waarbij `clientdomain` uw domein is.

at.js produceert een `mboxSession ID`. De eerste plaatsaanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met de naam `mboxSession` en `mboxPC` in te stellen, en een omleidingsverzoek wordt teruggestuurd met een extra parameter (`mboxXDomainCheck=true`).

Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de aanbieding geretourneerd.

Sommige browsers wijzen cookies van derden af. Als het cookie van een andere fabrikant wordt geblokkeerd, werkt het cookie van de eerste partij nog steeds. [!DNL Target] pogingen om het cookie van derden in te stellen, en als dit niet het geval is,  [!DNL Target] kunnen alleen gegevens worden bijgehouden in het specifieke domein van de client. Het volgen tussen domeinen werkt niet als de derde wordt geblokkeerd, tenzij `mboxSession` in de verbinding wordt toegevoegd die domeinen kruist. In dit geval wordt een ander cookie van de eerste fabrikant ingesteld en gesynchroniseerd met het cookie van het vorige domein.

## Cookie-instellingen

Het cookie heeft verschillende standaardinstellingen. U kunt deze instellingen desgewenst wijzigen, met uitzondering van de duur van het cookie. Vraag uw accountvertegenwoordiger wanneer u de cookie-instellingen wijzigt.

| Instelling | Informatie |
|--- |--- |
| Naam cookie | mbox. |
| Cookie-domein | Het tweede en bovenste niveau van de domeinen waaruit u de inhoud aanbiedt. Omdat het van het domein van uw bedrijf wordt gediend, is het koekje een eerste partijkoekje. Voorbeeld: `mycompany.com`. |
| Serverdomein | `clientcode.tt.omtrdc.net`, met de clientcode voor uw account. |
| Duur van cookie | Het cookie blijft twee jaar na de laatste aanmelding in de browser van de bezoeker staan. U kunt de duur van het cookie niet wijzigen. |
| P3P-beleid | De cookie wordt gepubliceerd met een P3P-beleid, zoals vereist door de standaardinstelling in de meeste browsers. Een P3P-beleid geeft aan welke browser de cookie aanbiedt en hoe de informatie wordt gebruikt. |

Het cookie houdt een aantal waarden bij om te beheren hoe uw bezoekers campagnes ervaren:

| Waarde | Definitie |
|--- |--- |
| sessie-id | Een unieke id voor een gebruikerssessie. Standaard duurt dit 30 minuten. |
| pc-id | Een halfpermanente id voor de browser van een bezoeker. Laadt 14 dagen. |
| controleren | Een eenvoudige testwaarde die wordt gebruikt om te bepalen of een bezoeker cookies ondersteunt. Stel de instellingen in wanneer een bezoeker een pagina aanvraagt. |
| disable | Stel in of de laadtijd van de bezoeker langer is dan de time-out die is geconfigureerd in het bestand mbox.js. Standaard duurt dit 1 uur. |

## Effect op Doel voor Safari-bezoekers als gevolg van wijzigingen in het bijhouden van Apple WebKit

Houd rekening met het volgende:

### Hoe werkt Adobe Target Tracking?

| Cookies | Details |
|--- |--- |
| Domeinen van eerste partij | Dit is de standaardimplementatie voor de klanten van het Doel.  De &quot;mbox&quot;koekjes wordt geplaatst in het domein van de klant. |
| Tekstspatiëring van derden | Tekstspatiëring door derden is belangrijk voor reclame en het richten van gebruiksgevallen in Target en Adobe Audience Manager (AAM).  Bij het bijhouden van externe gegevens zijn technieken voor scripts die verwijzen naar andere sites, vereist.  Het doel gebruikt twee cookies, &quot;mboxSession&quot; en &quot;mboxPC&quot; die zijn ingesteld in het domein `clientcode.tt.omtrd.net`. |

### Wat is de aanpak van Apple?

Van Apple:

&quot;Intelligente preventie van tracering is een nieuwe WebKit-functie die het opsporen van gegevens via andere sites beperkt door cookies en andere websitegegevens verder te beperken.&quot;

&quot;Dit wordt intersite tracering genoemd en het cookie dat wordt gebruikt door `example-tracker.com` wordt een cookie van een andere fabrikant genoemd. In onze test vonden we populaire websites met meer dan 70 van dergelijke trackers, die allemaal ongemerkt gegevens over gebruikers verzamelen.&quot;

| Benadering | Details |
|--- |--- |
| Intelligente traceringspreventie | Voor meer informatie, zie [Intelligente het Volgen Preventie](https://webkit.org/blog/7675/intelligent-tracking-prevention/) op de WebKit Open Bron Web Browser Engine website. |
| Cookies | Hoe Safari cookies verwerkt:<ul><li>Cookies van derden die zich niet op een domein bevinden waartoe de gebruiker rechtstreeks toegang heeft, worden nooit opgeslagen. Dit gedrag is niet nieuw. Cookies van derden worden al niet ondersteund in Safari.</li><li>Cookies van derden die zijn ingesteld op een domein waartoe de gebruiker rechtstreeks toegang heeft, worden na 24 uur gewist.</li><li>Cookies van de eerste partij worden na 30 dagen gezuiverd als dat domein van de eerste partij als het volgen van gebruikers over plaatsen is geclassificeerd. Deze kwestie zou op grote bedrijven kunnen van toepassing zijn die gebruikers naar verschillende domeinen online verzenden. Apple heeft niet duidelijk gemaakt hoe deze domeinen precies zullen worden geclassificeerd, of hoe een domein kan bepalen als zij als het volgen van gebruikers dwars-plaats zijn geclassificeerd.</li></ul> |
| Machine die leert domeinen te identificeren die naar andere sites verwijzen | Apple:<br>Machine Learning Classifier: Een machine het leren model wordt gebruikt om te classificeren welke hoogste privé-gecontroleerde domeinen de capaciteit hebben om de gebruiker dwars-plaats te volgen, die op de verzamelde statistieken wordt gebaseerd. Van de verschillende verzamelde statistieken bleken drie vectoren een sterk signaal te hebben voor classificatie op basis van de huidige volgpraktijken: subresource onder aantal unieke domeinen, subframe onder aantal unieke domeinen en aantal unieke domeinen waarnaar opnieuw is omgeleid. Alle gegevens verzamelen en classificeren gebeurt op het apparaat.<br>Nochtans, als de gebruiker met example.com als hoogste domein interactie heeft, die vaak als eerste-partijdomein wordt bedoeld, beschouwt de Intelligente het Volgen Preventie het een signaal dat de gebruiker in de website geinteresseerd is en tijdelijk zijn gedrag aanpast zoals die in deze chronologie wordt getoond:<br>Als de gebruiker met example.com de laatste 24 uren interactie aanging, zullen zijn koekjes beschikbaar zijn wanneer een derde  `example.com` is. Dit staat voor &quot;Sign in met mijn rekening van X op Y&quot;login scenario&#39;s toe.<ul><li>Domeinen die als domein op het hoogste niveau worden bezocht, worden niet beïnvloed. Sites zoals bijvoorbeeld OKTA</li><li>Identificeert domeinen die subdomein of subframe zijn van de huidige pagina over meerdere unieke domeinen.</li></ul> |

### Hoe wordt Adobe beïnvloed?

| Betrokken functionaliteit | Details |
|--- |--- |
| Ondersteuning voor uitschakelen | Met WebKit van Apple worden wijzigingen in WebKit doorgevoerd in de ondersteuning voor weigeren.<br>De optie om te weigeren gebruikt een cookie in het  `clientcode.tt.omtrdc.net` domein. Zie [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md) voor meer informatie.<br>Doel ondersteunt twee opt-outs:<ul><li>Eén per client (de client beheert de koppeling om te weigeren).</li><li>Een via Adobe die de gebruiker uit alle functionaliteit van het Doel voor alle klanten kiest.</li></ul>Beide methoden gebruiken het cookie van derden. |
| Doelactiviteiten | Klanten kunnen hun [levensduur van het profiel](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) voor hun doelaccounts kiezen, tot 90 dagen. Het probleem is dat als de profiellevensduur van de account langer is dan 30 dagen en de cookie van de eerste partij wordt gewist omdat het domein van de klant is gemarkeerd als het bewaken van gebruikers naar andere sites, het gedrag voor Safari-bezoekers wordt beïnvloed in de volgende gebieden in Target:<br>**Doelrapporten**: Als een gebruiker Safari in een activiteit ingaat, na 30 dagen terugkeert, en dan omzet, telt die gebruiker als twee bezoekers en één omzetting.<br>Dit gedrag is het zelfde voor activiteiten die Analytics gebruiken zoals de rapporteringsbron (A4T).<br>**Profiel en activiteitenlidmaatschap**:<ul><li>Profielgegevens worden gewist wanneer het cookie van de eerste partij verloopt.</li><li>Het lidmaatschap van de activiteit wordt gewist wanneer het eerste-partijkoekje verloopt.</li><li> Het doel werkt niet in Safari voor accounts die een cookie-implementatie van een andere fabrikant of een cookie-implementatie van een andere fabrikant gebruiken. Dit gedrag is niet nieuw. Safari heeft cookies van derden al een tijdje niet toegestaan.</li></ul><br>**Suggesties**: Als er een zorg is dat het klantendomein als één het volgen bezoekers dwars-zitting zou kunnen worden gemerkt, is het het veiligst om het profielleven aan 30 dagen of minder in Doel te plaatsen. Dit zorgt ervoor dat gebruikers op dezelfde manier worden bijgehouden in Safari en alle andere browsers. |
