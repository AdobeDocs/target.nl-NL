---
keywords: tekenlimiet;mbox-parameters;batch-levering api;profielparameters;limieten;ingebouwde profielen;maximum;limit;constraint;character;best practice;orderTotal;mbox3rdPartyID;category;categoryID;problemen oplossen
description: Bekijk een lijst van karaktergrenzen en andere grenzen die activiteiten en andere elementen in  [!DNL Adobe Target] beïnvloeden.
title: Wat zijn het diverse karakter, de grootte, en andere grenzen in  [!DNL Adobe Target]?
feature: Troubleshooting
mini-toc-levels: 3
exl-id: b318ab16-1382-4f3a-8764-064adf384d6b
source-git-commit: 720f70a97c5c9457f134085696dd79196c7869bc
workflow-type: tm+mt
source-wordcount: '1734'
ht-degree: 0%

---

# Limieten

Tekenbeperkingen en andere beperkingen (grootte, publiek, profielen, waarden, parameters, enz.) die van invloed zijn op activiteiten en andere elementen in [!DNL Adobe Target] .

>[!NOTE]
>
>De onderstaande limieten moeten als &quot;harde&quot; limieten worden beschouwd, tenzij ze als &quot;aanbevolen&quot; worden opgegeven.
>
>Wanneer de limieten die als &quot;aanbevolen&quot; zijn opgegeven, worden benaderd of overschreden, kan de prestatie trager worden. Trage tijden van interfacebelasting kunnen ook worden veroorzaakt door een zeer complexe activiteit, zoals vele publiek, doelstellingen, en ervaringen allen in één activiteit.
>
>Zeer complexe activiteiten dienen te worden beoordeeld met [!DNL Adobe] Consulting en getest in een beperkte omgeving voordat ze worden vrijgegeven voor productie.

## Activiteiten

### Activiteitennamen

* **Grens**: 250 karakters.

### Aantal activiteiten per rekening

* **geadviseerde grens**: 10.000 actieve levende activiteiten.

* **geadviseerde grens**: 10.000 actieve bewaarde (en niet gebeëindigde) activiteiten.

## API-aanroepen van doel

* **Grens**: 50 vraag per minuut voor Admin, het Melden, en bulkprofielupdate APIs. Deze limiet geldt niet voor de API&#39;s voor levering en één profiel bijwerken.

  Als u meer dan 50 API-aanroepen per minuut maakt, geeft [!DNL Target] een foutbericht &quot;503 HTTP status&quot;.

## Soorten publiek

### Namen publiek

* **Grens**: 255 karakters.

### Soorten publiek, herbruikbaar per account

* **geadviseerde grens**: 20.000 publiek.

### Aantal soorten publiek per doos, metrisch, of ervaring

* **Grens**: 50 publiek

## categoryId, parameter

* **Grens**: 256 karakters.

## Inhoud leveren {#content-delivery}

* **Grens**: 100 gezamenlijke [!DNL Target] verzoeken van de inhoudslevering per gebruikerszitting.

  Als een klant meer dan 100 gelijktijdige [!DNL Target] verzoeken om inhoud voor een bepaalde gebruikerssessie indient, worden alle volgende aanvragen voor die gebruikerssessie geblokkeerd. Twee of meer verzoeken worden beschouwd als gelijktijdige aanvragen als ze allemaal naar de [!DNL Target] -server worden verzonden voordat de reactie voor een van deze aanvragen wordt ontvangen. [!DNL Target] verwerkt opeenvolgende gelijktijdige aanvragen voor dezelfde sessie.

   * **het gedrag van de Fout**:

      * Delivery API and Batch Mbox v2:
         * Foutcode: HTTP 420 Te veel aanvragen
         * Foutbericht: &quot;Te veel aanvragen met dezelfde sessie-id&quot;

      * Verouderde mbox-API:
         * Standaardinhoud met opmerking &quot;Te veel aanvragen met dezelfde sessie-id&quot;

      * at.js:
         * Standaardinhoud weergegeven

* **Grens**: 50 dozen per [!DNL Target] verzoek van de partij van de inhoudslevering.

  Als u meer dan 50 vakken per batch-aanvraag voor [!DNL Target] levering van inhoud aanvraagt, treedt er een foutcode voor de reactie op `HTTP 400` met foutbericht `size must be between 0 and 50` .

  De verzoeken van de partijdoos worden opeenvolgend verwerkt, die de algemene reactietijd met elke herhaling verhogen. Hoe meer vakjes in het batchverzoek, des te meer responslatentie kan worden verwacht en daarom is er mogelijk time-outs. Als de ervaring het teruggeven op deze hoge latentiepartijverzoeken wordt geblokkeerd, zou de latentie in een degraded gebruikerservaring kunnen resulteren aangezien de gebruikers op ervaringen wachten om terug te geven.

* **Grens**: 60 MB POST van HTTP lichaamsomvang voor [!DNL Target] verzoeken van de inhoudslevering.

  Als de inhoud van een [!DNL Target] -aanvraag voor levering van inhoud groter is dan 60 MB, resulteert dit in een foutcode voor de reactie `HTTP 413 Request Entity Too Large` .

* **Geadviseerde grens**: 50 berichten per [!DNL Target] verzoek van de leveringspartij.

  Als u meer dan 50 berichten per aanvraag voor de leveringsbatch van [!DNL Target] verzendt, resulteert dit waarschijnlijk in een hogere responslatentie en time-outs.

  De verzoeken van het partijbericht worden opeenvolgend verwerkt, die de algemene reactietijd met elke herhaling verhogen. Hoe meer meldingen over het batchverzoek, des te meer responslatentie kan worden verwacht, en dus ook de mogelijkheid van time-outs. Sommige extra latentie op de verzoeken van het partijbericht zou voor sommige klanten aanvaardbaar kunnen zijn, maar ben zich ervan bewust dat onderbrekingen en om het even welke verdere pogingen nog latentie zouden kunnen veroorzaken.

## Klantkenmerken

### Kenmerknamen van klant

* **Grens**: 250 karakters door voer of API.

### Aliasid van kenmerk Klant

* **Grens** 50 karakters.

### Klantkenmerken, uploaden

* **Maximale dossiergrootte voor elke upload die de methode van HTTP** gebruikt: 100 MB.
* **maximumdossiergrootte voor elke upload die de methode van FTP gebruikt**: 4 GB.
* **Aantal attributen toegestaan om** in te tekenen: 5 voor [!DNL Target Standard] en 200 voor [!DNL Target Premium].

## Entiteiten

### Aantal entiteiten

* Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, is 99, ofwel hardcoded ofwel via lussen.
* De aanbevolen limiet voor de beste prestaties is om de catalogus minder dan 1 miljoen items per omgeving en minder dan 10 miljoen items in alle omgevingen te houden.
* De maximumgrens is tien miljoen punten per milieu en 100 miljoen punten over alle milieu&#39;s. Als u tussen een miljoen en tien miljoen items per omgeving hebt, heeft dit gevolgen voor de prestaties van de gebruikersinterface van [!UICONTROL Catalog Search] . [!DNL Target Recommendations] blijft echter aanbevelingen produceren en leveren.

### Aangepaste kenmerken van entiteit

* **de entiteitattributen van de Douane**: 100.

* **Grens van het Karakter**: De maximumkarakterlengte hangt van de taal af.

   * 15.000 tekens (talen van één waarde, van één en van twee bytes)
   * 500 waarden, 100 tekens per waarde (meerdere waarden)

  De maximale lengte van aangepaste kenmerken van entiteiten met een enkele waarde is 15.000 tekens (voor UTF-8-gecodeerde talen van één byte en twee byte, zoals Engelse en andere Latijnse alfabeten) of 10.000 tekens (voor UTF-8-gecodeerde talen van drie bytes, zoals Chinees, Japans en Koreaans).

  Aangepaste kenmerken van entiteiten met meerdere waarden mogen niet meer dan 500 waarden bevatten. Elke individuele waarde is beperkt tot 100 tekens. Het totale aantal tekens voor alle waarden moet in overeenstemming zijn met de beperkingen voor de maximumlengte van aangepaste attributen voor entiteiten met één waarde (zie hierboven).

### entity.id

* **Grens voor implementaties die het vangen van koopinformatie** vereisen: 50 karakters.

  Deze beperking wordt afgedwongen omdat de parameter `productPurchasedId` mbox de entiteit.ids vastlegt, die het aantal tekens tot 50 beperkt.

* **Grens voor implementaties die op mening-gebaseerde algoritmen slechts vereisen:**: 1.000 karakters.

  Op weergave gebaseerde algoritmen zijn onder andere weergave/weergave, meest bekeken, onlangs weergegeven enzovoort.

## excludeIds {#excludedid}

* **Grens**: 5 KB voor POST- verzoeken. 2.083 tekens min de lengte van de URL voor GET-aanvragen.

  Voor GET-verzoeken geldt dat, hoewel de limiet voor het achterste gedeelte 5 kB is, omdat Microsoft Internet Explorer de URL beperkt tot 2083 tekens, de realistische limiet 2083 tekens min de huidige lengte van de URL is.

## Ervaringen

### Ervaringsnamen

* **Grens**: 50 karakters.

### Ervaringen per activiteit

* **Grens**: 2.000 ervaringen per [!UICONTROL Experience Targeting] (XT), [!UICONTROL A/B Test], [!UICONTROL Multivariate Test] (MVT), en [!UICONTROL Auto-Target] activiteit.

  30.000 ervaringen per Automated Personalization (AP) activiteit.

### Wijzigingen per ervaring

* **Grens**: 50 per ervaring op om het even welke activiteit

## mboxes

### In-box-profielkenmerkwaarde {#in-mbox}

* **Grens**: 256 karakters.

  Waarden van meer dan 256 tekens worden afgebroken bij gebruik van at.js 1.*x*. Er wordt een foutbericht weergegeven wanneer u waarden met meer dan 256 tekens verzendt bij gebruik van at.js 2.*x* of [!DNL Adobe Experience Platform Web SDK]. Waarden worden niet automatisch afgekapt.

### In-box-profielnamen

* **Grens**: 128 karakters.

### mbox-namen {#mbox-names}

* **Grens**: 250 karakters.

  Voor [!DNL Delivery API] (at.js 2.*x*), de integratie van de Partij V2, en [!DNL Adobe Experience Platform Web SDK] (alloy.js), kunnen de namen van mbox *alfanumerieke karakters (a-z, a-z, 0-9) en om het even welke volgende karakters bevatten:*

  ```
  - , . _ / = ` : ; & ! @ # $ % ^ & * ( ) _ + | ? ~ [ ] { }
  ```

  Voor om.js 1.*x* integraties, kunnen de namen van mbox *niet* om het even welke volgende karakters bevatten:

  ```
  ' " %22 %27 < > %3C %3E 
  ```

### mbox-parameters {#mbox-parameters}

* **Grens**: De volgende grenzen zijn op mbox parameters van toepassing:

  Voor standaard mbox vraag:

   * mbox-parameters: 500 parameters per mbox.
   * Profielparameters: 500 parameters van het parameterprofiel per mbox.
   * Andere parameters (URL, verwijzende URL, enz.): 50 per mbox voor elk ander parametertype.

  Deze limieten zijn van toepassing, tenzij de aanvraag wordt ingekort vanwege beperkingen in de webbrowser.

  Als u de Batch Delivery-API gebruikt, is de limiet 50 dozen per aanvraag voor de batch.

  Als u de Batch Delivery-API in de Mobile Services SDK gebruikt, zijn de limiet van 50 mbox-parameters, 50 profielparameters en 50 voor andere parametertypen beperkingen van de API zelf. Het is niet mogelijk om een aanvraag met meer dan deze nummers te verzenden via de Batch Delivery-API. Als een aanvraag meer dan deze limieten bevat, retourneert de API het volgende foutbericht:

  &quot;Het aantal mboxParameters mag niet groter zijn dan 50.&quot;

  Limieten ingesteld voor eindpunten:

  **Batch mbox v2**:

   * mbox-parameters 100
   * naam van parameter mbox max. lengte 128
   * parameterwaarde mbox mag niet null zijn
   * parameterwaarde mbox 5000
   * profielparameters 50
   * naam van profielparameter max. lengte 128
   * waarde van profielparameter mag niet null zijn
   * waarde van profielparameter max. lengte 256

  **Eind van levering API**:

   * mbox-parameters 100
   * naam van parameter mbox max. lengte 128
   * parameterwaarde mbox mag niet null zijn
   * parameterwaarde mbox 5000
   * profielparameters 50
   * naam van profielparameter max. lengte 128
   * waarde van profielparameter mag niet null zijn
   * waarde van profielparameter max. lengte 256

### verzoek-URL&#39;s

* **Grens**: 2.083 karakters.

  Deze limiet is het gevolg van beperkingen voor de URL-lengte van Microsoft Internet Explorer.

### mbox3rdPartyId, parameter

* **Grens**: 256 karakters.

## Aanbiedingen

### Aanbiedingsnamen

* **Grens**: 250 karakters.

### Aantal aanbiedingen

* **Grens**: 150.000 totale aanbiedingen.

  Activiteitsynchronisatiefouten treden op als de limiet van 150.000 aanbiedingen wordt overschreden.

### Grootte voorstel {#offer-size}

Voor aanbiedingen gelden de volgende groottegrenzen:

* 1024 kB voor HTML-aanbiedingen.
* 1024 kB (voor elke ervaring) voor visuele aanbiedingen van UI.
* 1024 kB vanaf de API.

  Als u een globale box gebruikt, is de grens voor de volledige reeks inhoud teruggekeerd voor de pagina. Door het beperken van de aanbiedingsgrootte worden de laadtijden van de pagina verbeterd. Als de limiet wordt overschreden, wordt het volgende bericht weergegeven:

  &quot;De inhoud voor de ervaring is te groot om te leveren. Pas de ervaring aan om minder paginacode te beïnvloeden.&quot;

## orderId, parameter

* **geadviseerde grens**: 120 karakters.

## orderTotal, parameter

* **geadviseerde grens**: 120 karakters.

## productPurchasedId, parameter

* **Grens**: 50 karakters per komma-gescheiden waarde en 250 karakters in totaal. Individuele waarden van meer dan 50 tekens worden door het systeem afgekapt. Totale lengte boven 250 tekens resulteert in een fout van 400.

## Profielscripts

* **geadviseerde grens van actieve profielmanuscripten (die worden toegelaten)**: 300

* **geadviseerde grens van totale profielmanuscripten per rekening**: 2.000

* **Aanbevelingen voor het beperken van de ingewikkeldheid van het profielmanuscript**: De manuscripten van het profiel kunnen een beperkt aantal instructies uitvoeren. Voor meer informatie, zie [ Beste praktijken ](/help/main/c-target/c-visitor-profile/profile-parameters.md#best) in *attributen van het Profiel*.

## Eigenschappen

* **geadviseerde grens**: 5.000 eigenschappen.

## Publiek/segmenten rapporteren

* **Grens**: 50 rapporterend publiek/segmenten per activiteit.

## sessionID

De sessie-id kan elke afdrukbare tekenreeks zijn, behalve een spatie, vraagteken ( ? ), accolades ( { } ) of een slash ( / ). De waarde moet tussen 1 en 128 tekens lang zijn.

## Het invoervak voor scriptprofielen in de gebruikersinterface van [!DNL Target]

* **geadviseerde grens**: 2.000 karakters.

  Afhankelijk van de grootte van de gecodeerde tekenreeks, die veel langer kan zijn dan de onbewerkte tekenreeks. Als de tekenreeks te groot is, mislukt deze voordat deze op [!DNL Adobe Target] wordt ingesteld.

## Scriptprofielen

### Scriptprofielnamen

* **Grens**: 50 karakters.

### Scriptprofielwaarden

* **Grens**: 2.048 karakters.

  Om prestatieredenen raden we een geretourneerde waarde aan die niet langer is dan 256 tekens.

  Als de geretourneerde waarde van een tekenreeks groter is dan 2.048 tekens, wordt het script door het systeem uitgeschakeld.

  Als voor een geretourneerde waarde van een array de grootte van de samengevoegde waarden van de array groter is dan 2.048 tekens, wordt het script door het systeem uitgeschakeld.

## Succeswaarden

* **Grens**: 200 per activiteit.

## Targeting

### Doelvoorwaarden

* **geadviseerde grens**: 1.000 waarden.

  Dit verwijst naar het aantal waarden met regelscheiding in het tekstgebied dat als doel is ingesteld. U kunt bijvoorbeeld 1000 ZIP-codes invoeren in een ZIP-codedoel.

### Doelstellingen {#targeting-rules}

* **geadviseerde grens**: 2.500 karakters per het richten regelwaarde.
* **geadviseerde grens**: 50.000 unieke waarden per publiek over het richten van regels.
* **geadviseerde grens**: 100.000 uniek het richten regelwaarden per activiteit.
