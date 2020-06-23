---
keywords: email;ESP;email service provider;rawbox;delivery API;download-only template;email template;batch processing;build-time email
description: Informatie over de manieren om e-mail met Aanbevelingen te integreren.
title: Aanbevelingen integreren met e-mail
topic: Recommendations
uuid: ae137d7c-58c5-4601-92fc-2dc5548760fd
translation-type: tm+mt
source-git-commit: 0b36f1b36b354d90a9d79313b1d2a35b55461943
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Aanbevelingen integreren met e-mail{#integrate-recommendations-with-email}

Informatie over de manieren om e-mail met Aanbevelingen te integreren.

De mogelijkheden van uw e-mailserviceprovider bepalen welke methode moet worden gebruikt. Uw accountmanager of consultant kan u helpen de optie te kiezen die het beste voor u werkt.

## Optie 1: De API voor levering gebruiken {#section_9F00D271BABA4B7390B461F4C44EC319}

De bezorgings-API is een POST-aanvraag die werkt met e-mail tijdens de build. Deze optie is de voorkeursmethode voor e-mails tijdens het samenstellen.

De meeste e-mailclients staan POST-aanvragen niet toe. Daarom wordt deze API niet aanbevolen voor open-time-gebruiksgevallen. Sommige e-mailcliënten, zoals Gmail of Vooruitzichten, zouden de inhoud in het voorgeheugen kunnen plaatsen of het beeld blokkeren en de ontvanger vereisen om pro-actief toe te staan het beeld om terug te geven.

U kunt de standaardinhoud niet retourneren met de API voor levering.

De volgende code is een voorbeeld-API-leveringsaanvraag:

```
curl -X POST \ 
  'https://clientcode.tt.omtrdc.net/rest/v1/mbox/?client=clientcode' \ 
  -H 'authorization: Bearer 3423614b-4843-4664-83c4-c6c3f6c8869b' \ 
  -H 'cache-control: no-cache' \ 
  -H 'content-type: application/json' \ 
  -d '{ 
  "mbox" : "email-mbox", 
  "tntId" : "111499796294071-449025.28_44", 
  "requestLocation" : { 
    "host" : "prod" 
  }, 
   "profileParameters" : { 
   }, 
  "mboxParameters" : { 
    "at_property": "b468a242-64a4-32a0-ca0c-890bddd78789", 
    "entity.id": "article-123", 
    "entity.event.detailsOnly" : "true" 
  } 
  "contentAsJson":  true 
}'
```

Waar `clientcode` is je Target-clientcode.

>[!NOTE]
>
>Zorg ervoor dat u een unieke waarde opgeeft voor zowel `sessionId` als een van `tntId` of `thirdPartyId` voor elke e-mailontvanger (bijvoorbeeld voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd.

Zie [Delivery API documentatie](https://developers.adobetarget.com/api/#server-side-delivery) voor meer informatie.

## Optie 2: Een e-mailsjabloon voor een rawbox gebruiken {#section_C0D48A42BCCE45D6A68852F722C7C352}

Een box is gelijkaardig aan een mbox verzoek, maar voor milieu&#39;s buiten het Web, zoals e-maildienstverleners (ESPs). Omdat u niet hebt [!DNL mbox.js] of in [!DNL at.js] te gebruiken radibox verzoeken, moet u uw verzoeken manueel tot stand brengen. In de onderstaande voorbeelden wordt uitgelegd hoe u met e-mailverzoeken in een tekstvak werkt.

>[!NOTE]
>
>Wanneer het gebruiken van een doos en [!DNL Target], zie de belangrijke veiligheidsmededeling onder [Create allowlists die gastheren specificeren die worden gemachtigd om mbox vraag naar Target](/help/administrating-target/hosts.md#allowlist)te verzenden.

Op deze manier kunt u de prestaties van aanbevelingen in e-mails volgen, deze op de normale manier testen met een aanbeveling en doorgaan met bijhouden op de site.

Stel een [!DNL Recommendations] activiteit in [!DNL Adobe Target]met de optie [Formuliergebaseerde Experience Composer](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) . Voor de plaats, selecteer de naam van mbox u om in de radibox verzoek hebt gekozen te gebruiken die uit ESP komt. Selecteer een ontwerp met de vormgeving die u voor uw e-mail wilt gebruiken. Tijdens het bouwen van e-mail, richt ESP een vraag aan de [!DNL Adobe Target] servers voor elke radibox in elke e-mail die wordt geproduceerd. Uw ESP moet een manier hebben om teruggestuurde HTML in de e-mail op te nemen wanneer het wordt verzonden.

Het e-mailsysteem dat u gebruikt, moet deze scenario&#39;s kunnen verwerken:

### Er is een geldig antwoord ontvangen, maar er zijn geen aanbevelingen

* In dit geval zal de reactie wat als mboxDefault parameterwaarde wordt geplaatst zijn. Zie de uitleg hieronder over deze parameter.
* De e-mailprovider moet een standaard HTML-blok met aanbevelingen hebben om in dit geval te gebruiken.

### De Target-server heeft een time-out en retourneert deze zonder gegevens

* In dit geval retourneert de Target-server de volgende inhoud:

   `//ERROR: application server timeout`

* De e-mailtoepassing moet naar die tekst zoeken en de fout kunnen verwerken. De e-mailprovider heeft meerdere opties voor het afhandelen van deze kwestie:

   * Probeer onmiddellijk een andere servervraag (geadviseerd, misschien met een pogingsteller).
   * Dat e-mailbericht weergeven en doorgaan met de volgende e-mail.
   * Wachtrij die bepaalde e-mail en re-run ontbrak e-mails als partij aan het eind van de aanvankelijke looppas.

### Voorbeeld van aanvraag-URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Vereiste parameters: {#reqparams}

>[!NOTE]
>
>Om [!DNL Recommendations] in e-mail te gebruiken, moet de kadervraag of `entity.id` of `entity.categoryId` of allebei omvatten, afhankelijk van het type van aanbeveling criteria. De voorbeeldvraag hierboven omvat beide.

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `client_code` | *client_code* | De code van de cliënt die in Aanbevelingen wordt gebruikt. Deze waarde kan door uw Adobe-consultant worden opgegeven. |  |
| `mbox` | *mboxName* | De naam van de box die voor het richten wordt gebruikt. | Zelfde bevestiging zoals voor alle mbox vraag.<br>Maximaal 250 tekens.<br>Kan geen van de volgende tekens bevatten: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | uitgeschakeld | Voorkomt dat de reactie een cookie instelt in een andere omgeving dan het web. |  |
| `entity.id`<br>(Vereist voor bepaalde soorten criteria: weergave/weergave, bekijken/kopen, kopen/kopen) | *entity_id* | De productID de aanbeveling is gebaseerd op, zoals een verlaten product in het karretje, of een vorige aankoop.<br>Indien vereist door de criteria, moet de radibox vraag het `entity.id`. |  |
| `entity.event.detailsOnly` | true | Als `entity.id` wordt overgegaan, wordt het hoogst geadviseerd om deze parameter ook over te gaan om het verzoek te verhinderen het aantal van getalleerde paginameningen voor een punt te verhogen, zodat niet op productmening-gebaseerde algoritmen schuin te trekken. |  |
| `entity.categoryId`<br>(Vereist voor bepaalde soorten criteria: meest bekeken op rubriek en topverkopers op rubriek) | *category_id* | De rubriek waarop de aanbeveling is gebaseerd, zoals topverkopers in een rubriek.<br>Indien vereist door de criteria, moet de radibox vraag het `entity.categoryId`. |  |
| `mboxDefault` | *`https://www.default.com`* | Als de `mboxNoRedirect` parameter niet aanwezig is, `mboxDefault` zou een absolute URL moeten zijn die standaardinhoud zal terugkeren als geen aanbeveling beschikbaar is. Dit kan een afbeelding of andere statische inhoud zijn.<br>Als de `mboxNoRedirect` parameter aanwezig is, `mboxDefault` kan elke tekst zijn die aangeeft dat er bijvoorbeeld geen aanbevelingen zijn `no_content`.<br>De e-mailprovider moet het geval afhandelen waar deze waarde wordt geretourneerd en standaard-HTML in de e-mail invoegen. <br> **Beste praktijken** op het gebied van beveiliging: Let op: als het domein dat in de `mboxDefault` URL wordt gebruikt niet is toegestaan, kunt u blootstaan aan een risico van een Open Redirect-kwetsbaarheid. Om het ongeoorloofde gebruik van verbindingen van Redirector of `mboxDefault` door derden te vermijden, adviseren wij u &quot;geautoriseerde gastheren&quot;gebruiken om van de standaard opnieuw te richten domeinen URL toe te staan. Target gebruikt hosts om domeinen toe te staan waaraan u omleidingen wilt toestaan. Voor meer informatie, zie [Create Toegestane lijsten die gastheren specificeren die worden gemachtigd om mbox vraag naar Target](/help/administrating-target/hosts.md#allowlist) in *Gastheren* te verzenden. |  |
| `mboxHost` | *mbox_host* | Dit is het domein dat aan het standaardmilieu (gastheergroep) wordt toegevoegd wanneer de vraag brandt. |  |
| `mboxPC` | Leeg | (Vereist voor aanbevelingen die het profiel van een bezoeker gebruiken.)<br>Als er geen &quot;thirdPartyId&quot; is opgegeven, wordt een nieuwe tntId gegenereerd en geretourneerd als onderdeel van de reactie. Anders blijft het leeg.<br>**Opmerking **: Zorg ervoor dat u een unieke waarde opgeeft voor`mboxSession`en`mboxPC`voor elke e-mailontvanger (dus voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; Lengte &lt; 128<br>Kan niet meer dan één &quot;.&quot; bevatten (punt).<br>Het enige toegestane punt is voor het achtervoegsel van de profiellocatie. |

### Optionele parameters

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `mboxPC`<br>(Optioneel) | *mboxPCId* | Target-bezoeker-id. Gebruik deze waarde als u een volledige cirkel van een gebruiker bij meerdere bezoeken naar uw site wilt bijhouden of als u een parameter voor gebruikersprofielen gebruikt.<br>Deze waarde moet de werkelijke Adobe Target PCID voor de gebruiker zijn, die van de website naar uw CRM wordt geëxporteerd. De e-mailprovider haalt deze id op van uw CRM of Data warehouse en gebruikt deze voor de waarde van deze parameter.<br>De `mboxPC` waarde is ook handig voor het bijhouden van het gedrag van bezoekerssites bij meerdere bezoeken voor het bijhouden van statistieken wanneer een aanbeveling deel uitmaakt van een A/B-activiteit.<br>**Opmerking **: Zorg ervoor dat u een unieke waarde opgeeft voor`mboxSession`en`mboxPC`voor elke e-mailontvanger (dus voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; Lengte &lt; 128<br>Kan niet meer dan één &quot;.&quot; bevatten (punt).<br>Het enige toegestane punt is voor het achtervoegsel van de profiellocatie. |
| `mboxNoRedirect`<br>(Optioneel) | 1 | Standaard wordt de aanroeper omgeleid wanneer geen te leveren inhoud wordt gevonden. Gebruik deze optie om het standaardgedrag uit te schakelen. |  |
| `mbox3rdPartyId` | *xxx* | Gebruik deze optie als u uw eigen aangepaste bezoeker-id wilt gebruiken voor het opgeven van profielen. |  |

### Mogelijke Target-serverreacties

| Antwoord | Beschrijving |
|--- |--- |
| //FOUT: | Gegenereerd door taakverdelingsmechanisme wanneer inhoud niet kan worden geretourneerd |
| succes | De `mboxNoRedirect` parameter wordt ingesteld op &#39;true&#39; en de server retourneert geen aanbevelingen (er is dus geen overeenkomst voor de mbox of de servercache wordt niet geïnitialiseerd). |
| ongeldige aanvraag | De `mbox` parameter ontbreekt.<ul><li>De parameter `mboxDefault` of de `mboxNoRedirect` parameter is niet opgegeven.</li><li>`mboxTrace` request parameter is gespecificeerd maar `mboxNoRedirect` niet.</li><li>`mboxTarget`parameter wordt niet opgegeven wanneer mbox-namen met `-clicked` achtervoegsel eindigen.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` niet opgegeven wanneer er geen overeenkomst voor de aanvraag bestaat en er geen `mboxNoRedirect` parameter is opgegeven. |
| `Invalid mbox name:= MBOX_NAME` | Geeft aan dat `mbox` parameter ongeldige tekens bevat. |
| `Mbox name [MBOX_NAME] is too long` | Geeft aan dat de parameter langer is dan 250 tekens. `mbox` |

## Optie 3: De sjabloon Alleen downloaden gebruiken {#section_518C279AF0094BE780F4EA40A832A164}

Stel een aanbeveling op de gebruikelijke manier in, maar kies alleen **in de presentatiesectie** downloaden in plaats van een sjabloon- en een mappencombinatie. Geef vervolgens in het ESP aan welke aanbeveling-id u hebt gemaakt. Het ESP heeft toegang tot de gegevens van de aanbeveling via API. Deze gegevens laten zien welke items moeten worden aanbevolen voor een bepaalde categorie of een bepaald sleutelitem, zoals items in een verlaten winkelwagentje. Het ESP slaat deze gegevens op, verbindt het met hun eigen blik en voelen, toont informatie over elk punt, en levert dat in e-mail.

Met deze optie, kan de aanbevelingen server niet direct de prestaties van een aanbeveling volgen of verkeer over veelvoudige algoritme/malplaatjecombinaties verdelen. De aanbevelingen zijn ook niet gekoppeld aan een bezoekersprofiel.

Zie [Verouderde API&#39;s > Downloaden](../../assets/adobe-recommendations-classic.pdf)voor meer informatie over de download-API.
