---
keywords: email;ESP;email service provider;rawbox;delivery API;download-only template;email template;batch processing;build-time e-mail
description: Leer hoe te om e-mail met Adobe  [!DNL Target Recommendations], including using the [!DNL Target]  Levering API, kadermalplaatjes, en neer-lading slechts malplaatjes te integreren.
title: Hoe kan ik aanbevelingen integreren met e-mail?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 08fcb507-2c91-444a-b8ac-26165e359f6f
source-git-commit: 1f505991ea9a0caf0d6d49f6464550243128ffaf
workflow-type: tm+mt
source-wordcount: '1734'
ht-degree: 0%

---

# [!DNL Recommendations] integreren met e-mail

[!DNL Adobe Target] biedt ondersteuning voor het aanpassen van aanbevelingen tijdens het verzenden van e-mailberichten.

Er zijn drie methoden beschikbaar voor de integratie van [!DNL Target Recommendations] met uw e-mailserviceprovider (ESP). De mogelijkheden van uw ESP bepalen welke methode moet worden gebruikt. Uw accountmanager of consultant kan u helpen de optie te kiezen die het beste voor u werkt.

| Methode | Details |
| --- | --- |
| [&#x200B; Methode 1: [!DNL Adobe Target Delivery API]](#delivery-api) (Voorkeur) | Gebruik [!DNL Adobe Target Delivery API] om per-klant/per-e-mail verzoeken om aanbevelingen te doen. |
| [&#x200B; Methode 2: [!DNL Adobe Rawbox API]](#rawbox) | Gebruik [!DNL Adobe Target Rawbox API] om per-klant/per-e-mail verzoeken om aanbevelingen te doen. |
| [&#x200B; Methode 3: [!DNL Recommendations Download API]](#download-api) | Met de API Aanbevelingen downloaden kunt u bulkaanbevelingen aanvragen voor een lijst met producten of categorieën in CSV-indeling. |

Het gebruiken van methode 1 of methode 2 vereist uw ESP om vraag aan een externe API per-klant/per-e-mailbasis te maken en op te wachten tot de inhoud is teruggekeerd. Deze methoden worden niet door alle ESP&#39;s ondersteund. Neem contact op met uw ESP om te bepalen of deze compatibel is met dit integratiepatroon.

Als je methode 3 gebruikt, moet je ESP zich aansluiten bij een lijst met aanbevelingen per product-id of rubriek-ID in je lijst met e-mailberichten. Deze methode kan worden gebaseerd op een kenmerk zoals het laatst bekeken product van de klant, het laatst aangeschafte product of de meest bekeken categorie. Uw ESP moet echter toegang hebben tot deze gegevens in zijn klantprofiel om de verbinding uit te voeren. Neem contact op met uw ESP om te bepalen of deze toegang heeft tot deze gegevens en compatibel is met dit integratiepatroon.

Aanpassing in opentijd van aanbevelingen wordt niet ondersteund door [!DNL Adobe Target] .

>[!IMPORTANT]
>
>De volgende capaciteitsrichtlijnen zijn van toepassing op de hieronder beschreven sjabloonmethoden voor levering-API en e-mailboxes (methoden 1 en 2):
>
>* Aanvragen dienen beperkt te blijven tot het laagste van 1.000 verzoeken per seconde of 25 keer het piekdagelijkse verkeer.
>* Het verkeer van de slag in stappen van 200 verzoeken per seconde elke minuut.
> 
>Neem contact op met uw accountmanager als u hogere tarieflimieten wilt gebruiken.

## Methode 1: De API voor levering gebruiken (voorkeur) {#delivery-api}

De bezorgings-API is een POST-aanvraag die werkt met e-mail tijdens de build. Deze optie is de voorkeursmethode voor e-mails tijdens het samenstellen.

De meeste e-mailclients staan POST-aanvragen niet toe. Daarom wordt deze API niet aanbevolen voor open-time-gebruiksgevallen. Sommige e-mailcliënten, zoals Gmail of Vooruitzichten, kunnen de inhoud in het voorgeheugen plaatsen of het beeld blokkeren en vereisen de ontvanger proactief het beeld om toe te staan terug te geven.

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

Waar `clientcode` uw [!DNL Target] -clientcode is.

>[!NOTE]
>
>Zorg ervoor dat u een unieke waarde opgeeft voor zowel `sessionId` als een van `tntId` of `thirdPartyId` voor elke e-mailontvanger (bijvoorbeeld voor elke API-aanroep). Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege de vele gebeurtenissen die binnen één profiel zijn gegenereerd.

Zie [&#x200B; Levering API documentatie &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/api/delivery-api/overview.html?lang=nl-NL){target=_blank} voor meer informatie.

## Methode 2: Een e-mailsjabloon voor een rawbox gebruiken {#rawbox}

Een box is gelijkaardig aan een mbox verzoek, maar voor milieu&#39;s buiten het Web, zoals e-maildienstverleners (ESPs). Omdat u niet over de [!DNL Adobe Experience Platform Web SDK] of [!DNL at.js] beschikt om te gebruiken in rawbox verzoeken, moet u uw verzoeken manueel tot stand brengen. In de onderstaande voorbeelden wordt uitgelegd hoe u met e-mailverzoeken in een tekstvak werkt.

>[!NOTE]
>
>Wanneer het gebruiken van een rawbox en [!DNL Target], zie de belangrijke veiligheidskennisgeving onder [&#x200B; lijsten van gewenste personen creëren die gastheren specificeren die worden gemachtigd om mbox vraag naar  [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist) te verzenden.

Op deze manier kunt u de prestaties van aanbevelingen in e-mails volgen, deze op de normale manier testen met een aanbeveling en doorgaan met bijhouden op de site.

Opstelling a [!DNL Recommendations] activiteit in [!DNL Target], gebruikend de [&#x200B; op vorm-Gebaseerde optie van de Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E). Voor de plaats, selecteer de naam van mbox u om in de radibox verzoek hebt gekozen te gebruiken die uit ESP komt. Selecteer een ontwerp met de vormgeving die u voor uw e-mail wilt gebruiken. Tijdens het maken van e-mails roept het ESP de [!DNL Target] -servers aan voor elke e-mail die wordt gegenereerd. Je ESP moet een manier hebben om de geretourneerde HTML op te nemen in het e-mailbericht wanneer het wordt verzonden.

Het e-mailsysteem dat u gebruikt, moet de volgende scenario&#39;s kunnen afhandelen:

### Er is een geldig antwoord ontvangen, maar er zijn geen aanbevelingen

* In dit geval is de reactie wat dan ook ingesteld is als de `mboxDefault` -parameterwaarde. Zie hieronder voor meer informatie over deze parameter.
* De e-mailprovider moet een standaard HTML-blok met aanbevelingen hebben om in dit geval te gebruiken.

### De [!DNL Target] -server keer uit en retourneert deze zonder gegevens

* In dit geval retourneert de [!DNL Target] -server de volgende inhoud:

  `//ERROR: application server timeout`

* De e-mailtoepassing moet naar die tekst zoeken en de fout kunnen verwerken. De e-mailprovider heeft meerdere opties voor het afhandelen van deze kwestie:

   * Probeer onmiddellijk een andere servervraag (geadviseerd, misschien met een pogingsteller).
   * Dat e-mailbericht weergeven en doorgaan met het volgende e-mailbericht.
   * De wachtrij van die e-mail en het opnieuw uitvoeren mislukte e-mails als een batch aan het einde van de eerste uitvoering.

### Voorbeeld van aanvraag-URL

```
https://client_code.tt.omtrdc.net/m2/client_code/ubox/raw?mbox=mbox_name&mboxSession=1396032094853-955654&mboxPC=1396032094853-955654&mboxXDomain=disabled&entity.event.detailsOnly=true&mboxDefault=nocontent&mboxNoRedirect=1&entity.id=2A229&entity.categoryId=5674
```

### Vereiste parameters: {#reqparams}

>[!NOTE]
>
>Als u [!DNL Recommendations] in e-mail wilt gebruiken, moet de rawbox-aanroep meestal de `entity.id` of `entity.categoryId` of beide bevatten, afhankelijk van het type aanbevelingen. De voorbeeldvraag hierboven omvat beide.

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `client_code` | *client_code* | De code van de cliënt die in Aanbevelingen wordt gebruikt. Deze waarde kan worden opgegeven door uw Adobe-consultant. |  |
| `mbox` | *mboxName* | De naam van de box die voor het richten wordt gebruikt. | Zelfde bevestiging zoals voor alle mbox vraag.<br> 250 karaktergrens.<br> Kan geen van de volgende tekens bevatten: `', ", %22, %27, <, >, %3C, %3E` |
| `mboxXDomain` | uitgeschakeld | Voorkomt dat de reactie een cookie instelt in een andere omgeving dan het web. |  |
| `entity.id`<br> (Vereist voor bepaalde soorten criteria: weergave/weergave, weergave/aangekocht, aangekocht/aangekocht) | *entity_id* | De productID de aanbeveling is gebaseerd op, zoals een verlaten product in het karretje, of een vorige aankoop.<br> Indien vereist door de criteria, moet de radibox vraag `entity.id` omvatten. |  |
| `entity.event.detailsOnly` | true | Als `entity.id` wordt overgegaan, wordt het hoogst geadviseerd om deze parameter ook over te gaan om het verzoek te verhinderen het aantal van de sprekende paginameningen voor een punt te verhogen, zodat niet op productmening-gebaseerde algoritmen schuin te trekken. |  |
| `entity.categoryId`<br> (Vereist voor bepaalde soorten criteria: de meeste bekeken op basis van rubriek en topverkopers op basis van rubriek) | *category_id* | De rubriek waarop de aanbeveling is gebaseerd, zoals topverkopers in een rubriek.<br> Indien vereist door de criteria, moet de radibox vraag `entity.categoryId` omvatten. |  |
| `mboxDefault` | *`https://www.default.com`* | Als de parameter `mboxNoRedirect` niet aanwezig is, moet `mboxDefault` een absolute URL zijn die standaardinhoud retourneert als er geen aanbeveling beschikbaar is. Deze URL kan een afbeelding of andere statische inhoud zijn.<br> Als de `mboxNoRedirect` parameter aanwezig is, `mboxDefault` kan om het even welke tekst zijn die erop wijst dat er geen aanbevelingen, bijvoorbeeld `no_content` zijn.<br> de e-mailleverancier moet het geval behandelen waar deze waarde is teruggekeerd en standaard HTML in e-mail opnemen. <br> **beste praktijken van de Veiligheid**: Als het domein in `mboxDefault` URL wordt gebruikt niet wordt gevoegd op lijst van gewenste personen, kunt u aan een risico van Open worden blootgesteld Redirect Vulnerability. Om te voorkomen dat Redirector-koppelingen of `mboxDefault` door derden zonder toestemming worden gebruikt, raadt Adobe u aan &quot;geautoriseerde hosts&quot; te gebruiken om de standaard omleidings-URL-domeinen te lijsten van gewenste personen. Het gebruik van het doel gastheren aan lijst van gewenste personen domeinen waaraan u redirects wilt toestaan. Voor meer informatie, zie [&#x200B; Lijsten van gewenste personen creëren die gastheren specificeren die worden gemachtigd om mbox vraag naar  [!DNL Target]](/help/main/administrating-target/hosts.md#allowlist) in *Gastheren* te verzenden. |  |
| `mboxHost` | *mbox_host* | Het domein dat aan het standaardmilieu (gastheergroep) wordt toegevoegd wanneer de vraag brandt. |  |
| `mboxPC` | Leeg | (Vereist voor aanbevelingen die het profiel van een bezoeker gebruiken.)<br> als geen &quot;thirdPartyId&quot;werd verstrekt, wordt een nieuwe tntId geproduceerd en als deel van de reactie teruggekeerd. Anders blijft het leeg.<br>**Nota**: Ben zeker om een unieke waarde van `mboxSession` en `mboxPC` voor elke e-mailontvanger (d.w.z., voor elke API vraag) te verstrekken. Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; Lengte &lt; 128 <br> kan meer dan één enkel bevatten &quot;.&quot; (punt).<br> het enige toegestane punt is voor het achtervoegsel van de profielplaats. |

### Optionele parameters

| Parameter | Waarde | Beschrijving | Validatie |
|--- |--- |--- |--- |
| `mboxPC`<br> (optioneel) | *mboxPCId* | Doelbezoeker-id. Gebruik deze waarde als u een volledige cirkel van een gebruiker bij meerdere bezoeken naar uw site wilt bijhouden of als u een parameter voor het gebruikersprofiel wilt gebruiken.<br> Deze waarde moet daadwerkelijke [!DNL Adobe Target] PCID voor de gebruiker zijn, die van de website aan uw CRM zou worden uitgevoerd. De e-mailprovider haalt deze id op van uw CRM of Data Warehouse en gebruikt deze voor de waarde van deze parameter.<br> de `mboxPC` waarde is ook nuttig om het gedrag van de bezoekersplaats over veelvoudige bezoeken voor metriek het volgen te volgen wanneer een aanbeveling deel van een activiteit A/B uitmaakt.<br>**Nota**: Ben zeker om een unieke waarde van `mboxSession` en `mboxPC` voor elke e-mailontvanger (d.w.z., voor elke API vraag) te verstrekken. Als u geen unieke waarden voor deze velden opgeeft, kan de API-respons vertragen of mislukken vanwege het grote aantal gebeurtenissen dat binnen één profiel wordt gegenereerd. | 1 &lt; Lengte &lt; 128 <br> kan meer dan één enkel bevatten &quot;.&quot; (punt).<br> het enige toegestane punt is voor het achtervoegsel van de profielplaats. |
| `mboxNoRedirect`<br> (optioneel) | 1 | Standaard wordt de aanroeper omgeleid wanneer geen te leveren inhoud wordt gevonden. Hiermee kunt u het standaardgedrag uitschakelen. |  |
| `mbox3rdPartyId` | *xxx* | Gebruik deze optie als u uw eigen aangepaste bezoeker-id wilt gebruiken voor het opgeven van profielen. |  |

### Potentiële [!DNL Target] serverreacties

| Antwoord | Beschrijving |
|--- |--- |
| //FOUT: | Gegenereerd door taakverdelingsmechanisme wanneer inhoud niet kan worden geretourneerd |
| Succes | De parameter `mboxNoRedirect` wordt ingesteld op &#39;true&#39; en de server retourneert geen aanbevelingen (er is dus geen overeenkomst voor de mbox of de servercache wordt niet geïnitialiseerd). |
| ongeldige aanvraag | De parameter `mbox` ontbreekt.<ul><li>De parameter `mboxDefault` of `mboxNoRedirect` wordt niet opgegeven.</li><li>`mboxTrace` request parameter is specified but `mboxNoRedirect` is not.</li><li>`mboxTarget` de parameter wordt niet gespecificeerd wanneer de mbox namen met `-clicked` achtervoegsel beëindigen.</li></ul> |
| `Cannot redirect to default content, please specify mboxDefault parameter` | `mboxDefault` niet opgegeven wanneer er geen overeenkomende aanvraag bestaat en er geen parameter `mboxNoRedirect` is opgegeven. |
| `Invalid mbox name:= MBOX_NAME` | Geeft aan dat de parameter `mbox` ongeldige tekens bevat. |
| `Mbox name [MBOX_NAME] is too long` | Geeft aan dat de parameter `mbox` langer is dan 250 tekens. |

## Methode 3: De API voor downloaden van aanbevelingen gebruiken {#download-api}

Opstelling een aanbeveling zoals gebruikelijk, maar kies **download slechts** in de presentatiesectie in plaats van een malplaatje en een mbox combinatie. Geef vervolgens in het ESP aan welke aanbeveling-id u hebt gemaakt. Het ESP heeft toegang tot de gegevens van de aanbeveling via API. Deze gegevens laten zien welke items moeten worden aanbevolen voor een bepaalde categorie of een bepaald sleutelitem, zoals items in een verlaten winkelwagentje. Het ESP slaat deze gegevens op, verbindt het met hun eigen blik en voelen, toont informatie over elk punt, en levert dat in e-mail.

Met deze optie, kan de aanbevelingen server niet direct de prestaties van een aanbeveling volgen of verkeer over veelvoudige algoritme/malplaatjecombinaties verdelen. De aanbevelingen zijn ook niet gekoppeld aan een bezoekersprofiel.

Voor meer informatie over de download API, zie [&#x200B; Verouderde APIs > Download &#x200B;](/help/main/assets/adobe-recommendations-classic.pdf).
