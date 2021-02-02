---
keywords: email;ESP;email service provider;rawbox;delivery API;download-only template;email template;batch processing;build-time e-mail
description: Informatie over de manieren om e-mail met Recommendations te integreren.
title: Recommendations integreren met e-mail
feature: Recommendations
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---


# ![recommendations ](/help/assets/premium.png) integreren met e-mail{#integrate-recommendations-with-email}

Informatie over de manieren om e-mail met Recommendations te integreren.

De mogelijkheden van uw e-mailserviceprovider bepalen welke methode moet worden gebruikt. Uw accountmanager of consultant kan u helpen de optie te kiezen die het beste voor u werkt.

## Optie 1: De leverings-API gebruiken {#section_9F00D271BABA4B7390B461F4C44EC319}

De bezorgings-API is een verzoek van een POST dat werkt met e-mail tijdens de build. Deze optie is de voorkeursmethode voor e-mails tijdens het samenstellen.

De meeste e-mailclients staan geen verzoeken om POST toe. Daarom wordt deze API niet aanbevolen voor open-time-gebruiksgevallen. Sommige e-mailcliënten, zoals Gmail of Vooruitzichten, zouden de inhoud in het voorgeheugen kunnen plaatsen of het beeld blokkeren en de ontvanger vereisen om pro-actief toe te staan het beeld om terug te geven.

U kunt de standaardinhoud niet retourneren met de API voor levering.

De volgende code is een voorbeeld-API-leveringsaanvraag:

```javascript
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

Waarbij `clientcode` uw doelclientcode is.

>[!NOTE]
>
>Zorg ervoor dat u een unieke waarde opgeeft voor zowel `sessionId` als `tntId` of `thirdPartyId` voor elke e-mailontvanger (bijvoorbeeld voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd.

Zie [Delivery API documentation](https://developers.adobetarget.com/api/#server-side-delivery) voor meer informatie.

## Optie 2: Een e-mailsjabloon voor een rawbox gebruiken {#section_C0D48A42BCCE45D6A68852F722C7C352}

Een box is gelijkaardig aan een mbox verzoek, maar voor milieu&#39;s buiten het Web, zoals e-maildienstverleners (ESPs). Omdat u [!DNL mbox.js] of [!DNL at.js] niet om in brievenbusverzoeken hebt te gebruiken, moet u uw verzoeken manueel tot stand brengen. In de onderstaande voorbeelden wordt uitgelegd hoe u met e-mailverzoeken in een tekstvak werkt.

>[!NOTE]
>
>Wanneer het gebruiken van een rawbox en [!DNL Target], zie de belangrijke veiligheidskennisgeving onder [creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel te verzenden](/help/administrating-target/hosts.md#allowlist).

Op deze manier kunt u de prestaties van aanbevelingen in e-mails volgen, deze op de normale manier testen met een aanbeveling en doorgaan met bijhouden op de site.

Stel een [!DNL Recommendations]-activiteit in [!DNL Adobe Target] in met de optie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E). Voor de plaats, selecteer de naam van mbox u om in de radibox verzoek hebt gekozen te gebruiken die uit ESP komt. Selecteer een ontwerp met de vormgeving die u voor uw e-mail wilt gebruiken. Tijdens het maken van e-mails roept het ESP de [!DNL Adobe Target]-servers aan voor elke rawbox in elke e-mail die wordt gegenereerd. Uw ESP moet een manier hebben om teruggestuurde HTML in de e-mail op te nemen wanneer het wordt verzonden.

Het e-mailsysteem dat u gebruikt, moet deze scenario&#39;s kunnen verwerken:

### Er is een geldig antwoord ontvangen, maar er zijn geen aanbevelingen

* In dit geval zal de reactie wat als mboxDefault parameterwaarde wordt geplaatst zijn. Zie de uitleg hieronder over deze parameter.
* De e-mailprovider moet een standaard HTML-blok met aanbevelingen hebben om in dit geval te gebruiken.

### De time-out van de doelserver en retourneert deze zonder gegevens

* In dit geval retourneert de doelserver de volgende inhoud:

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
>Als u [!DNL Recommendations] in e-mail wilt gebruiken, moet de rawbox-aanroep meestal `entity.id` of `entity.categoryId` of beide bevatten, afhankelijk van het type aanbevolen criteria. De voorbeeldvraag hierboven omvat beide.

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `client_code` | *client_code* | De code van de client die in Recommendations wordt gebruikt. Uw consultant voor Adobe kan deze waarde opgeven. |  |
| `mbox` | *mboxName* | De naam van de box die voor het richten wordt gebruikt. | Zelfde bevestiging zoals voor alle mbox vraag.<br>Maximaal 250 tekens.<br>Kan geen van de volgende tekens bevatten:  `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | uitgeschakeld | Voorkomt dat de reactie een cookie instelt in een andere omgeving dan het web. |  |
| `entity.id`<br>(Vereist voor bepaalde soorten criteria: weergave/weergave, bekijken/kopen, kopen/kopen) | *entity_id* | De productID de aanbeveling is gebaseerd op, zoals een verlaten product in het karretje, of een vorige aankoop.<br>Indien vereist door de criteria, moet de radibox vraag het  `entity.id`. |  |
| `entity.event.detailsOnly` | true | Als `entity.id` wordt overgegaan, wordt het hoogst geadviseerd om deze parameter ook over te gaan om het verzoek te verhinderen het aantal van getalleerde paginameningen voor een punt te verhogen, zodat niet op productmening-gebaseerde algoritmen schuin te trekken. |  |
| `entity.categoryId`<br>(Vereist voor bepaalde soorten criteria: meest bekeken op rubriek en topverkopers op rubriek) | *category_id* | De rubriek waarop de aanbeveling is gebaseerd, zoals topverkopers in een rubriek.<br>Indien vereist door de criteria, moet de radibox vraag het  `entity.categoryId`. |  |
| `mboxDefault` | *`https://www.default.com`* | Als de parameter `mboxNoRedirect` niet aanwezig is, `mboxDefault` zou een absolute URL moeten zijn die standaardinhoud zal terugkeren als geen aanbeveling beschikbaar is. Dit kan een afbeelding of andere statische inhoud zijn.<br>Als de  `mboxNoRedirect` parameter aanwezig is,  `mboxDefault` kan elke tekst zijn die aangeeft dat er bijvoorbeeld geen aanbevelingen zijn  `no_content`.<br>De e-mailprovider moet het geval afhandelen waar deze waarde wordt geretourneerd en standaard-HTML in de e-mail invoegen.  <br> **Beste praktijken** op het gebied van beveiliging: Merk op dat als het domein dat in  `mboxDefault` URL wordt gebruikt niet wordt toegevoegd op lijst van gewenste personen, u aan een risico van Open Redirect Kwetsbaarheid kunt worden blootgesteld. Om het ongeoorloofde gebruik van verbindingen van Redirector of `mboxDefault` door derden te vermijden, adviseren wij u &quot;geautoriseerde gastheren&quot;gebruiken om de gebrek te lijsten van gewenste personen omleiding URL domeinen. Het gebruik van het doel gastheren aan lijst van gewenste personen domeinen waaraan u redirects wilt toestaan. Voor meer informatie, zie [Lijsten van gewenste personen creëren die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel te verzenden ](/help/administrating-target/hosts.md#allowlist) in *Gastheren*. |  |
| `mboxHost` | *mbox_host* | Dit is het domein dat aan het standaardmilieu (gastheergroep) wordt toegevoegd wanneer de vraag brandt. |  |
| `mboxPC` | Leeg | (Vereist voor aanbevelingen die het profiel van een bezoeker gebruiken.)<br>Als er geen &quot;thirdPartyId&quot; is opgegeven, wordt een nieuwe tntId gegenereerd en geretourneerd als onderdeel van de reactie. Anders blijft het leeg.<br>**Opmerking**: Zorg ervoor dat u een unieke waarde opgeeft voor  `mboxSession` en  `mboxPC` voor elke e-mailontvanger (dus voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; Length &lt; 128<br>Kan niet meer dan één &quot;.&quot; bevatten (punt).<br>Het enige toegestane punt is voor het achtervoegsel van de profiellocatie. |

### Optionele parameters

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `mboxPC`<br>(Optioneel) | *mboxPCId* | Doelbezoeker-id. Gebruik deze waarde als u een volledige cirkel van een gebruiker bij meerdere bezoeken naar uw site wilt bijhouden of als u een parameter voor gebruikersprofielen gebruikt.<br>Deze waarde moet de werkelijke Adobe Target PCID voor de gebruiker zijn, die van de website naar uw CRM wordt geëxporteerd. De e-mailprovider haalt deze id op van uw CRM of Data-entrepot en gebruikt deze voor de waarde van deze parameter.<br>De  `mboxPC` waarde is ook handig voor het bijhouden van het gedrag van de bezoekerssite bij meerdere bezoeken voor het bijhouden van statistieken wanneer een aanbeveling deel uitmaakt van een A/B-activiteit.<br>**Opmerking**: Zorg ervoor dat u een unieke waarde opgeeft voor  `mboxSession` en  `mboxPC` voor elke e-mailontvanger (dus voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; Length &lt; 128<br>Kan niet meer dan één &quot;.&quot; bevatten (punt).<br>Het enige toegestane punt is voor het achtervoegsel van de profiellocatie. |
| `mboxNoRedirect`<br>(Optioneel) | 3 | Standaard wordt de aanroeper omgeleid wanneer geen te leveren inhoud wordt gevonden. Gebruik deze optie om het standaardgedrag uit te schakelen. |  |
| `mbox3rdPartyId` | *xxx* | Gebruik deze optie als u uw eigen aangepaste bezoeker-id wilt gebruiken voor het opgeven van profielen. |  |

### Mogelijke reacties op doelserver

| Antwoord | Beschrijving |
|--- |--- |
| //FOUT: | Gegenereerd door taakverdelingsmechanisme wanneer inhoud niet kan worden geretourneerd |
| succes | De parameter `mboxNoRedirect` is ingesteld op &#39;true&#39; en de server retourneert geen aanbevelingen (er is dus geen overeenkomst voor de box of de servercache is niet geïnitialiseerd). |
| ongeldige aanvraag | De parameter `mbox` ontbreekt.<ul><li>Ofwel `mboxDefault` of `mboxNoRedirect` wordt parameter niet gespecificeerd.</li><li>`mboxTrace` request parameter is gespecificeerd maar  `mboxNoRedirect` is niet.</li><li>`mboxTarget`parameter wordt niet opgegeven wanneer mbox-namen met  `-clicked` achtervoegsel eindigen.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` niet opgegeven wanneer er geen overeenkomst voor de aanvraag bestaat en er geen  `mboxNoRedirect` parameter is opgegeven. |
| `Invalid mbox name:= MBOX_NAME` | Geeft aan dat de parameter `mbox` ongeldige tekens bevat. |
| `Mbox name [MBOX_NAME] is too long` | Geeft aan dat de parameter `mbox` langer is dan 250 tekens. |

## Optie 3: De alleen-downloadsjabloon {#section_518C279AF0094BE780F4EA40A832A164} gebruiken

Stel een aanbeveling op de gebruikelijke manier in, maar kies **alleen downloaden** in de presentatiesectie in plaats van een sjabloon- en maboxcombinatie. Geef vervolgens in het ESP aan welke aanbeveling-id u hebt gemaakt. Het ESP heeft toegang tot de gegevens van de aanbeveling via API. Deze gegevens laten zien welke items moeten worden aanbevolen voor een bepaalde categorie of een bepaald sleutelitem, zoals items in een verlaten winkelwagentje. Het ESP slaat deze gegevens op, verbindt het met hun eigen blik en voelen, toont informatie over elk punt, en levert dat in e-mail.

Met deze optie, kan de aanbevelingen server niet direct de prestaties van een aanbeveling volgen of verkeer over veelvoudige algoritme/malplaatjecombinaties verdelen. De aanbevelingen zijn ook niet gekoppeld aan een bezoekersprofiel.

Zie [Verouderde API&#39;s > Downloaden](/help/assets/adobe-recommendations-classic.pdf) voor meer informatie over de download-API.
