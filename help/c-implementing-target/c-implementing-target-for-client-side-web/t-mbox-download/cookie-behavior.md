---
keywords: Overview and Reference;webkit
description: Het gedrag van de cookie hangt af van het feit of het een cookie van een eerste partij, een cookie van een derde partij met een cookie van de eerste partij of van een cookie van een andere fabrikant alleen is.
title: mbox.js, cookies
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1565'
ht-degree: 0%

---


# mbox.js, cookies{#mbox-js-cookies}

Het gedrag van de cookie hangt af van het feit of het een cookie van een eerste partij, een cookie van een derde partij met een cookie van de eerste partij of van een cookie van een andere fabrikant alleen is.

>[!IMPORTANT]
>
>Dit onderwerp bevat informatie over `mboxSession` en `mboxPC`. Onze best practices voor implementatie raden u aan geen gevoelige informatie te koppelen aan of op te slaan met de cookiegegevens: `mboxSession` of `mboxPC`.

Zie ook Het doelcookie [verwijderen](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cookie-deleting.md).

## Wanneer om Eerste of derdekoekjes te gebruiken {#section_F71B29420C004A7FA3B1921E619B326E}

De site bepaalt welke cookies u wilt gebruiken. Het is handig om te begrijpen hoe Target werkt wanneer u probeert cookies van derden en van derden te begrijpen. Zie [Hoe werkt](/help/c-intro/how-target-works.md#concept_459AB4DEE7364A9290C2FD405DC29584) Adobe Target voor meer informatie.

Er zijn drie hoofdtoepassingen voor cookies:

1. Eén domein.

   Al uw tests vinden plaats binnen één top-level domein ( [!DNL `www.domain.com`], [!DNL store.domain.com], [!DNL anysub.domain.com], enz.).

   Aanpak: Gebruik alleen cookies van de eerste fabrikant. Dit is de standaardinstelling.

1. De gebruikers kruisen domeinen en u wilt hun gedrag over deze domeinen volgen en testen.

   Voorbeeld: Een gebruiker komt naar uw site om te winkelen, maar checkt dit uit via Yahoo-winkels. Drie benaderingen (werk samen met uw accountvertegenwoordiger om de beste aanpak te bepalen):

   * Cookies van de eerste en derde partij inschakelen.
   * Schakel alleen derden in (zeer zelden, maar heeft het voordeel dat de cookie uit uw domein blijft).
   * Schakel alleen cookies van eerste partijen en geef parameter door wanneer u een domein overschrijdt. `mboxSession`

      De `mboxSession` parameter moet worden doorgegeven aan een bestemmingspagina met [!DNL mbox.js] verwijzing. Het kan geen tussenliggende redirector-pagina zijn.

1. U gebruikt alleen adboxes of FlashBox op een externe site.

   Twee benaderingen (werk met uw manager van de cliëntdiensten om de beste benadering te bepalen):

   * Cookies van de eerste en derde partij inschakelen.

      Cookies van de eerste en derde partij zijn vereist voor FlashBox en dynamische creatieve producten.
   * Schakel alleen cookies van derden in.

      Deze benadering is slechts voor het zeldzame geval waar implementaties AdBox zonder onsite het richten worden gebruikt.

## Werking cookie van eerste partij {#section_CE6313D979EA4D0897D2F661E7A8AFA7}

Het cookie van de eerste partij wordt opgeslagen in [!DNL clientdomain.com], waar `clientdomain` is uw domein.

[!DNL Mbox.js] genereert een code `mboxSession ID` en slaat deze op in het cookie van de box. De eerste mbox-reactie bevat de aanbieding en de JavaScript-code voor het opslaan van de `mboxPC ID` door de toepassing gegenereerde code in het mbox-cookie.

>[!NOTE]
>
>Het cookie van de [!DNL AMCV_###@AdobeOrg] eerste partij wordt altijd ingesteld met de Experience Cloud-bezoeker-id.

## Gedrag cookie van derden {#section_4C3A83990BF8415BB1806602D84AED48}

Het cookie van de andere fabrikant wordt opgeslagen in [!DNL clientcode.tt.omtrdc.net] en het cookie van de eerste partij wordt opgeslagen in [!DNL clientdomain.com], waar `clientdomain` u het domein wilt.

[!DNL Mbox.js] genereert een `mboxSession ID`. De eerste plaatsaanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met naam `mboxSession` en `mboxPC` en een omleidingsverzoek met een extra parameter ( `mboxXDomainCheck=true`) in te stellen.

Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de aanbieding geretourneerd.

Als de browser cookies van derden afwijst, worden deze cookies niet opgenomen in de omleidingsaanvraag en wordt standaardinhoud weergegeven voor alle locaties op de pagina. Omdat er geen cookies zijn ingesteld, vindt hetzelfde proces hierboven opnieuw plaats bij elke paginaaanvraag.

>[!NOTE]
>
>Het [!DNL demdex.net] cookie wordt ingesteld als cookies van derden niet worden geblokkeerd.

## Gedrag cookie van derden en eerste partij {#section_F0C9AD8BFDF8457A999C4A07A0F7A981}

Het cookie van de andere fabrikant wordt opgeslagen in [!DNL clientcode.tt.omtrdc.net] en het cookie van de eerste partij wordt opgeslagen in [!DNL clientdomain.com], waar `clientdomain` u het domein wilt.

[!DNL Mbox.js] genereert een `mboxSession ID`. De eerste plaatsaanvraag retourneert HTTP-antwoordheaders die proberen cookies van derden met naam `mboxSession` en `mboxPC`in te stellen, en een omleidingsverzoek wordt teruggestuurd met een extra parameter ( `mboxXDomainCheck=true`).

Als de browser cookies van derden accepteert, bevat de omleidingsaanvraag deze cookies en wordt de aanbieding geretourneerd.

Sommige browsers wijzen cookies van derden af. Als het cookie van een andere fabrikant wordt geblokkeerd, werkt het cookie van de eerste partij nog steeds. Doel probeert het cookie van derden in te stellen. Als dit niet het geval is, kan Target alleen het specifieke domein van de client bijhouden. Het volgen tussen domeinen werkt niet als de derde wordt geblokkeerd, tenzij het in de verbinding wordt toegevoegd die domeinen kruist. `mboxSession` In dit geval wordt een ander cookie van de eerste fabrikant ingesteld en gesynchroniseerd met het cookie van het vorige domein.

## Cookie-instellingen {#section_B498B8D1A34A444BBF84CC720EE9D87F}

Het cookie heeft verschillende standaardinstellingen. U kunt deze instellingen desgewenst wijzigen, met uitzondering van de duur van het cookie. Vraag uw accountvertegenwoordiger wanneer u de cookie-instellingen wijzigt.

| Instelling | Informatie |
|--- |--- |
| Naam cookie | mbox. |
| Cookie-domein | Het tweede en bovenste niveau van de domeinen waaruit u de inhoud aanbiedt. Omdat het van het domein van uw bedrijf wordt gediend, is het koekje een eerste partijkoekje.<br>Voorbeeld:  `mycompany.com`. |
| Serverdomein | `clientcode.tt.omtrdc.net`, met de clientcode voor uw account. |
| Duur van cookie | Het cookie blijft twee weken na de laatste aanmelding in de browser van de bezoeker staan. U kunt de duur van het cookie niet wijzigen. |
| P3P-beleid | De cookie wordt gepubliceerd met een P3P-beleid, zoals vereist door de standaardinstelling in de meeste browsers. Een P3P-beleid geeft aan welke browser de cookie aanbiedt en hoe de informatie wordt gebruikt. |

Het cookie houdt een aantal waarden bij om te beheren hoe uw bezoekers campagnes ervaren:

| Waarde | Definitie |
|--- |--- |
| sessie-id | Een unieke id voor een gebruikerssessie. Standaard duurt dit 30 minuten. |
| pc-id | Een halfpermanente id voor de browser van een bezoeker. Laadt 14 dagen. |
| controleren | Een eenvoudige testwaarde die wordt gebruikt om te bepalen of een bezoeker cookies ondersteunt. Stel de instellingen in wanneer een bezoeker een pagina aanvraagt. |
| disable | Stel in of de laadtijd van de bezoeker langer is dan de time-out die is geconfigureerd in het bestand mbox.js. Standaard duurt dit 1 uur. |

## Effect op Doel voor Safari-bezoekers als gevolg van wijzigingen in het bijhouden van Apple WebKit {#section_2A2E5730ED7D4A0985C904AFEA310AAE}

**Hoe werkt Adobe Target Tracking?**

| Cookies | Details |
|--- |--- |
| Domeinen van eerste partij | Dit is de standaardimplementatie voor de klanten van het Doel.  De &quot;mbox&quot;koekjes wordt geplaatst in het domein van de klant. |
| Tekstspatiëring van derden | Tekstspatiëring door derden is belangrijk voor reclame en het richten van gebruiksgevallen in Target en Adobe Audience Manager (AAM).  Bij het bijhouden van externe gegevens zijn technieken voor scripts die verwijzen naar andere sites, vereist.  Het doel gebruikt twee cookies, &quot;mboxSession&quot; en &quot;mboxPC&quot; ingesteld in het `clientcode.tt.omtrd.net` domein. |


**Wat is de aanpak van Apple?**

Van Apple:

&quot;Intelligente preventie van tracering is een nieuwe WebKit-functie die het opsporen van gegevens via andere sites beperkt door cookies en andere websitegegevens verder te beperken.&quot;

&quot;Dit wordt &#39;cross-site tracking&#39; genoemd en het cookie dat door `example-tracker.com` wordt gebruikt, wordt een cookie van een andere fabrikant genoemd. In onze test vonden we populaire websites met meer dan 70 van dergelijke trackers, die allemaal ongemerkt gegevens over gebruikers verzamelen.&quot;

| Benadering | Details |
|--- |--- |
| Intelligente traceringspreventie | Voor meer informatie, zie [Intelligente het Volgen Preventie](https://webkit.org/blog/7675/intelligent-tracking-prevention/) op de WebKit Open Bron Web Browser Engine website. |
| Cookies | Hoe Safari cookies verwerkt:<ul><li>Cookies van derden die zich niet op een domein bevinden waartoe de gebruiker rechtstreeks toegang heeft, worden nooit opgeslagen. Dit gedrag is niet nieuw. Cookies van derden worden al niet ondersteund in Safari.</li><li>Cookies van derden die zijn ingesteld op een domein waartoe de gebruiker rechtstreeks toegang heeft, worden na 24 uur gewist.</li><li>Cookies van de eerste partij worden na 30 dagen gezuiverd als dat domein van de eerste partij als het volgen van gebruikers over plaatsen is geclassificeerd. Deze kwestie zou op grote bedrijven kunnen van toepassing zijn die gebruikers naar verschillende domeinen online verzenden. Apple heeft niet duidelijk gemaakt hoe deze domeinen precies zullen worden geclassificeerd, of hoe een domein kan bepalen als zij als het volgen van gebruikers dwars-plaats zijn geclassificeerd.</li></ul> |
| Machine die leert domeinen te identificeren die naar andere sites verwijzen | Van Apple:<br>leerclassificatie machine: Een machine het leren model wordt gebruikt om te classificeren welke hoogste privé-gecontroleerde domeinen de capaciteit hebben om de gebruiker dwars-plaats te volgen, die op de verzamelde statistieken wordt gebaseerd. Van de verschillende verzamelde statistieken bleken drie vectoren een sterk signaal te hebben voor classificatie op basis van de huidige volgpraktijken: subresource onder aantal unieke domeinen, subframe onder aantal unieke domeinen en aantal unieke domeinen waarnaar opnieuw is omgeleid. Alle gegevens verzamelen en classificeren gebeurt op het apparaat.<br>Nochtans, als de gebruiker met example.com als hoogste domein interactie heeft, die vaak als eerste-partijdomein wordt bedoeld, beschouwt de Intelligente het Volgen Preventie het een signaal dat de gebruiker in de website geinteresseerd is en tijdelijk zijn gedrag aanpast zoals die in deze chronologie wordt getoond:<br>Als de gebruiker met example.com de laatste 24 uren interactie aanging, zullen zijn koekjes beschikbaar zijn wanneer `example.com` een derde is. Dit staat voor &quot;Sign in met mijn rekening van X op Y&quot;login scenario&#39;s toe.<ul><li>Domeinen die als domein op het hoogste niveau worden bezocht, worden niet beïnvloed. Sites zoals bijvoorbeeld OKTA</li><li>Identificeert domeinen die subdomein of subframe zijn van de huidige pagina over meerdere unieke domeinen.</li></ul> |

**Hoe wordt Adobe beïnvloed?**

| Betrokken functionaliteit | Details |
|--- |--- |
| Ondersteuning voor uitschakelen | Met WebKit van Apple worden wijzigingen in WebKit doorgevoerd in de ondersteuning voor weigeren.<br>De optie om te weigeren gebruikt een cookie in het `clientcode.tt.omtrdc.net` domein. Zie [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md)voor meer informatie.<br>Doel ondersteunt twee opt-outs:<ul><li>Eén per client (de client beheert de koppeling om te weigeren).</li><li>Een via Adobe die de gebruiker uit alle functionaliteit van het Doel voor alle klanten kiest.</li></ul>Beide methoden gebruiken het cookie van derden. |
| Doelactiviteiten | Klanten kunnen hun [profiellevensduur](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) voor hun doelaccounts kiezen (maximaal 90 dagen). De zorg is dat als de het profiellevensduur van de rekening langer is dan 30 dagen, en het eerstepartijkoekje wordt gezuiverd omdat het domein van de klant als het volgen van gebruikers dwars-plaats is gemerkt, het gedrag voor bezoekers Safari op de volgende gebieden in Doel zal worden beïnvloed:<br>**de Rapporten** van het Doel: Als een gebruiker Safari in een activiteit ingaat, na 30 dagen terugkeert, en dan omzet, telt die gebruiker als twee bezoekers en één omzetting.<br>Dit gedrag is het zelfde voor activiteiten die Analytics gebruiken zoals de rapporteringsbron (A4T).<br>**Profiel en activiteitenlidmaatschap**:<ul><li>Profielgegevens worden gewist wanneer het cookie van de eerste partij verloopt.</li><li>Het lidmaatschap van de activiteit wordt gewist wanneer het eerste-partijkoekje verloopt.</li><li> Het doel werkt niet in Safari voor accounts die een cookie-implementatie van een andere fabrikant of een cookie-implementatie van een andere fabrikant gebruiken. Dit gedrag is niet nieuw. Safari heeft cookies van derden al een tijdje niet toegestaan.</li></ul><br>**Suggesties**: Als er een zorg is dat het klantendomein als één het volgen bezoekers dwars-zitting zou kunnen worden gemerkt, is het het veiligst om het profielleven aan 30 dagen of minder in Doel te plaatsen. Dit zorgt ervoor dat gebruikers op dezelfde manier worden bijgehouden in Safari en alle andere browsers. |