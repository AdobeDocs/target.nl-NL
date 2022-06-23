---
keywords: email;ESP;email service provider;rawbox;delivery API;download-only template;email template;batch processing;build-time e-mail
description: Leer hoe u e-mail kunt integreren met Adobe [!DNL Target Recommendations], including using the [!DNL Target] De levering API, de malplaatjes van de doos, en neer-lading slechts malplaatjes.
title: Hoe integreer ik Recommendations met e-mail?
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Integreren [!DNL Recommendations] met e-mail

[!DNL Adobe Target] biedt ondersteuning voor het aanpassen van aanbevelingen in e-mailberichten tijdens het verzenden.

Drie methoden voor integratie [!DNL Target Recommendations] met uw e-mailserviceprovider (ESP) beschikbaar zijn. De mogelijkheden van uw ESP bepalen welke methode moet worden gebruikt. Uw accountmanager of consultant kan u helpen de optie te kiezen die het beste voor u werkt.

| Methode | Details |
| --- | --- |
| [Methode 1: [!DNL Adobe Target Delivery API]](#delivery-api) (Voorkeur) | Gebruik de [!DNL Adobe Target Delivery API] om per klant/per e-mail verzoeken om aanbevelingen te doen. |
| [Methode 2: [!DNL Adobe Rawbox API]](#rawbox) | Gebruik de [!DNL Adobe Target Rawbox API] om per klant/per e-mail verzoeken om aanbevelingen te doen. |
| [Methode 3: [!DNL Recommendations Download API]](#download-api) | Met de Recommendations Download API kunt u bulkaanbevelingen aanvragen voor een lijst met producten of categorieën in CSV-indeling. |

Het gebruiken van methode 1 of methode 2 vereist uw ESP om vraag aan een externe API per-klant/per-e-mailbasis te maken en op te wachten tot de inhoud is teruggekeerd. Deze methoden worden niet door alle ESP&#39;s ondersteund; Neem contact op met uw ESP om te bepalen of het compatibel is met dit integratiepatroon.

Als je methode 3 gebruikt, moet je ESP zich aansluiten bij een lijst met aanbevelingen per product-id of rubriek-ID in je lijst met e-mailberichten. Deze methode kan op een attribuut zoals het laatst bekeken product van de klant, het laatst gekochte product, of de meeste bekeken categorie worden gebaseerd. Uw ESP moet echter toegang hebben tot deze gegevens in zijn klantprofiel om de verbinding uit te voeren. Neem contact op met uw ESP om te bepalen of deze toegang heeft tot deze gegevens en compatibel is met dit integratiepatroon.

De open-tijdpersonalisatie van aanbevelingen wordt niet gesteund door [!DNL Adobe Target].

>[!IMPORTANT]
>
>De volgende capaciteitsrichtlijnen zijn van toepassing op de hieronder beschreven sjabloonmethoden voor levering-API en e-mailboxes (methoden 1 en 2):
>
>* Aanvragen dienen beperkt te blijven tot het laagste van 1.000 verzoeken per seconde of 25 keer het piekdagelijkse verkeer.
>* Het verkeer van de slag in stappen van 200 verzoeken per seconde elke minuut.
> 
>Neem contact op met uw accountmanager als u hogere tarieflimieten wilt gebruiken.

## Methode 1: De API voor levering gebruiken (voorkeur) {#delivery-api}

De bezorgings-API is een verzoek van een POST dat werkt met e-mail tijdens de build. Deze optie is de voorkeursmethode voor e-mails tijdens het samenstellen.

De meeste e-mailclients staan geen verzoeken om POST toe. Daarom wordt deze API niet aanbevolen voor open-time-gebruiksgevallen. Sommige e-mailcliënten, zoals Gmail of Vooruitzichten, kunnen de inhoud in het voorgeheugen plaatsen of het beeld blokkeren en vereisen de ontvanger proactief het beeld om toe te staan terug te geven.

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

Wanneer `clientcode` is uw [!DNL Target] clientcode.

>[!NOTE]
>
>Zorg ervoor dat u een unieke waarde opgeeft voor beide `sessionId` en een van `tntId` of `thirdPartyId` voor elke e-mailontvanger (bijvoorbeeld voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege de vele gebeurtenissen die binnen één profiel zijn gegenereerd.

Zie [Leverings-API-documentatie](https://developer.adobe.com/target/implement/delivery-api/){target=_blank} voor meer informatie.

## Methode 2: Een e-mailsjabloon voor een rawbox gebruiken {#rawbox}

Een box is gelijkaardig aan een mbox verzoek, maar voor milieu&#39;s buiten het Web, zoals e-maildienstverleners (ESPs). Omdat je het [!DNL Adobe Experience Platform Web SDK] of [!DNL at.js] om in radibox verzoeken te gebruiken, moet u uw verzoeken manueel tot stand brengen. In de onderstaande voorbeelden wordt uitgelegd hoe u met e-mailverzoeken in een tekstvak werkt.

>[!NOTE]
>
>Bij gebruik van een rawbox en [!DNL Target], zie de belangrijke veiligheidskennisgeving onder [Creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om mbox vraag te verzenden naar [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist).

Op deze manier kunt u de prestaties van aanbevelingen in e-mails volgen, deze op de normale manier testen met een aanbeveling en doorgaan met bijhouden op de site.

Een [!DNL Recommendations] activiteit in [!DNL Target], met de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E) optie. Voor de plaats, selecteer de naam van mbox u om in de radibox verzoek hebt gekozen te gebruiken die uit ESP komt. Selecteer een ontwerp met de vormgeving die u voor uw e-mail wilt gebruiken. Tijdens de e-mailbuild-tijd roept het ESP de [!DNL Target] servers voor elke rawbox in elke e-mail die wordt gegenereerd. Uw ESP moet een manier hebben om de teruggekeerde HTML in e-mail op te nemen wanneer het wordt verzonden.

Het e-mailsysteem dat u gebruikt, moet de volgende scenario&#39;s kunnen verwerken:

### Er is een geldig antwoord ontvangen, maar er zijn geen aanbevelingen

* In dit geval is het antwoord wat er als de `mboxDefault` parameterwaarde. Zie de uitleg hieronder over deze parameter.
* De e-mailprovider moet in dit geval beschikken over een standaard HTML-blok met aanbevelingen.

### De [!DNL Target] servertime-out en geretourneerd zonder gegevens

* In dit geval worden de [!DNL Target] server retourneert de volgende inhoud:

   `//ERROR: application server timeout`

* De e-mailtoepassing moet naar die tekst zoeken en de fout kunnen verwerken. De e-mailprovider heeft meerdere opties voor het afhandelen van deze kwestie:

   * Probeer onmiddellijk een andere servervraag (geadviseerd, misschien met een pogingsteller).
   * Dat e-mailbericht weergeven en doorgaan met de volgende e-mail.
   * De wachtrij van die e-mail en het opnieuw uitvoeren mislukte e-mails als een batch aan het einde van de eerste uitvoering.

### Voorbeeld van aanvraag-URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Vereiste parameters: {#reqparams}

>[!NOTE]
>
>Te gebruiken [!DNL Recommendations] in e-mail, moet de radibox vraag gewoonlijk of `entity.id` of `entity.categoryId` of beide, afhankelijk van het soort aanbeveling criteria. De voorbeeldvraag hierboven omvat beide.

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `client_code` | *client_code* | De code van de client die in Recommendations wordt gebruikt. Uw consultant voor Adobe kan deze waarde opgeven. |  |
| `mbox` | *mboxName* | De naam van de box die voor het richten wordt gebruikt. | Zelfde bevestiging zoals voor alle mbox vraag.<br>Maximaal 250 tekens.<br>Kan geen van de volgende tekens bevatten: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | uitgeschakeld | Voorkomt dat de reactie een cookie instelt in een andere omgeving dan het web. |  |
| `entity.id`<br>(Vereist voor bepaalde soorten criteria: weergave/weergave, bekijken/kopen, kopen/kopen) | *entity_id* | De productID de aanbeveling is gebaseerd op, zoals een verlaten product in het karretje, of een vorige aankoop.<br>Indien vereist door de criteria, moet de radibox vraag omvatten `entity.id`. |  |
| `entity.event.detailsOnly` | true | Indien `entity.id` wordt overgegaan, wordt het hoogst geadviseerd om deze parameter ook over te gaan om het verzoek te verhinderen het aantal van getalleerde paginameningen voor een punt te verhogen, zodat niet op productmening-gebaseerde algoritmen schuin te trekken. |  |
| `entity.categoryId`<br>(Vereist voor bepaalde soorten criteria: meest bekeken op rubriek en topverkopers op rubriek) | *category_id* | De rubriek waarop de aanbeveling is gebaseerd, zoals topverkopers in een rubriek.<br>Indien vereist door de criteria, moet de radibox vraag omvatten `entity.categoryId`. |  |
| `mboxDefault` | *`https://www.default.com`* | Als de `mboxNoRedirect` parameter niet aanwezig is, `mboxDefault` moet een absolute URL zijn die standaardinhoud retourneert als er geen aanbeveling beschikbaar is. Deze URL kan een afbeelding of andere statische inhoud zijn.<br>Als de `mboxNoRedirect` parameter aanwezig is, `mboxDefault` kan elke tekst zijn die aangeeft dat er geen aanbevelingen zijn, bijvoorbeeld `no_content`.<br>De e-mailprovider moet het geval afhandelen waar deze waarde wordt geretourneerd en standaard HTML invoegen in de e-mail. <br> **Beste praktijken van de veiligheid**: Als het domein in `mboxDefault` URL wordt niet gevoegd op lijst van gewenste personen, u kunt aan een risico van Open Redirect Vulnerability worden blootgesteld. Om ongeoorloofd gebruik van Redirector verbindingen te vermijden of `mboxDefault` door derden raadt Adobe u aan &quot;geautoriseerde hosts&quot; te gebruiken om de standaard omleidings-URL-domeinen te lijsten van gewenste personen. Het gebruik van het doel gastheren aan lijst van gewenste personen domeinen waaraan u redirects wilt toestaan. Zie voor meer informatie [Creeer Lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om mbox vraag te verzenden naar [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist) in *Gastheren*. |  |
| `mboxHost` | *mbox_host* | Het domein dat aan het standaardmilieu (gastheergroep) wordt toegevoegd wanneer de vraag brandt. |  |
| `mboxPC` | Leeg | (Vereist voor aanbevelingen die het profiel van een bezoeker gebruiken.)<br>Als er geen &quot;thirdPartyId&quot; is opgegeven, wordt een nieuwe tntId gegenereerd en geretourneerd als onderdeel van de reactie. Anders blijft het leeg.<br>**Opmerking**: Zorg ervoor dat u een unieke waarde opgeeft van `mboxSession` en `mboxPC` voor elke e-mailontvanger (d.w.z. voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; lengte &lt; 128<br>Kan niet meer dan één &quot;.&quot; bevatten (punt).<br>Het enige toegestane punt is voor het achtervoegsel van de profiellocatie. |

### Optionele parameters

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `mboxPC`<br>(Optioneel) | *mboxPCId* | Doelbezoeker-id. Gebruik deze waarde als u een volledige cirkel van een gebruiker bij meerdere bezoeken naar uw site wilt bijhouden of als u een parameter voor gebruikersprofielen gebruikt.<br>Deze waarde moet de werkelijke waarde zijn [!DNL Adobe Target] PCID voor de gebruiker, die van de website naar uw CRM zou worden uitgevoerd. De e-mailprovider haalt deze id op van uw CRM of Data Warehouse en gebruikt deze voor de waarde van deze parameter.<br>De `mboxPC` Deze waarde is ook handig voor het bijhouden van het gedrag van bezoekerssites tijdens meerdere bezoeken voor het bijhouden van statistieken wanneer een aanbeveling deel uitmaakt van een A/B-activiteit.<br>**Opmerking**: Zorg ervoor dat u een unieke waarde opgeeft van `mboxSession` en `mboxPC` voor elke e-mailontvanger (d.w.z. voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; lengte &lt; 128<br>Kan niet meer dan één &quot;.&quot; bevatten (punt).<br>Het enige toegestane punt is voor het achtervoegsel van de profiellocatie. |
| `mboxNoRedirect`<br>(Optioneel) | 1 | Standaard wordt de aanroeper omgeleid wanneer geen te leveren inhoud wordt gevonden. Gebruik deze optie om het standaardgedrag uit te schakelen. |  |
| `mbox3rdPartyId` | *xxx* | Gebruik deze optie als u uw eigen aangepaste bezoeker-id wilt gebruiken voor het opgeven van profielen. |  |

### Potentieel [!DNL Target] serverreacties

| Antwoord | Beschrijving |
|--- |--- |
| //FOUT: | Gegenereerd door taakverdelingsmechanisme wanneer inhoud niet kan worden geretourneerd |
| Succes | De `mboxNoRedirect` parameter is ingesteld op &#39;true&#39; en de server retourneert geen aanbevelingen (er is dus geen overeenkomst voor de mbox of de servercache is niet geïnitialiseerd). |
| ongeldige aanvraag | De `mbox` parameter ontbreekt.<ul><li>Willekeurig `mboxDefault` of de `mboxNoRedirect` parameter is niet opgegeven.</li><li>`mboxTrace` request parameter is opgegeven maar `mboxNoRedirect` is niet.</li><li>`mboxTarget`parameter niet opgegeven wanneer mbox names end with `-clicked` achtervoegsel.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` niet opgegeven wanneer er geen overeenkomst voor de aanvraag bestaat en `mboxNoRedirect` parameter is niet opgegeven. |
| `Invalid mbox name:= MBOX_NAME` | Geeft aan `mbox` parameter bevat ongeldige tekens. |
| `Mbox name [MBOX_NAME] is too long` | Geeft aan `mbox` parameter langer is dan 250 tekens. |

## Methode 3: De Recommendations Download API gebruiken {#download-api}

Stel een aanbeveling op de gebruikelijke manier in, maar kies **alleen downloaden** in de presentatiesectie in plaats van een combinatie van een sjabloon en een kader. Geef vervolgens in het ESP aan welke aanbeveling-id u hebt gemaakt. Het ESP heeft toegang tot de gegevens van de aanbeveling via API. Deze gegevens laten zien welke items moeten worden aanbevolen voor een bepaalde categorie of een bepaald sleutelitem, zoals items in een verlaten winkelwagentje. Het ESP slaat deze gegevens op, verbindt het met hun eigen blik en voelen, toont informatie over elk punt, en levert dat in e-mail.

Met deze optie, kan de aanbevelingen server niet direct de prestaties van een aanbeveling volgen of verkeer over veelvoudige algoritme/malplaatjecombinaties verdelen. De aanbevelingen zijn ook niet gekoppeld aan een bezoekersprofiel.

Voor meer informatie over de download-API raadpleegt u [Verouderde API&#39;s > Downloaden](/help/main/assets/adobe-recommendations-classic.pdf).
