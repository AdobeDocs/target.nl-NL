---
keywords: tekenlimiet;mbox-parameters;batch-levering api;profielparameters;limieten;ingebouwde profielen;maximum;limit;constraint;character;best practice;orderTotal;mbox3rdPartyID;category;categoryID;problemen oplossen
description: Een lijst weergeven met tekenlimieten en andere beperkingen die van invloed zijn op activiteiten en andere elementen in [!DNL Adobe Target].
title: Wat zijn de verschillende karakter, grootte en andere grenzen in [!DNL Adobe Target]?
feature: Troubleshooting
mini-toc-levels: 3
exl-id: b318ab16-1382-4f3a-8764-064adf384d6b
source-git-commit: aa7242a20d6e80623dfe14b5e2f9c2996d9579b7
workflow-type: tm+mt
source-wordcount: '1600'
ht-degree: 0%

---

# Limieten

Tekengrenzen en andere beperkingen (grootte van aanbieding, publiek, profielen, waarden, parameters, enz.) die van invloed zijn op activiteiten en andere elementen in [!DNL Adobe Target].

>[!NOTE]
>
>De onderstaande limieten moeten als &quot;harde&quot; limieten worden beschouwd, tenzij ze als &quot;aanbevolen&quot; worden opgegeven.
>
>Wanneer de limieten die als &quot;aanbevolen&quot; zijn opgegeven, worden benaderd of overschreden, kan de prestatie trager worden. Trage tijden van interfacebelasting kunnen ook worden veroorzaakt door een zeer complexe activiteit, zoals vele publiek, doelstellingen, en ervaringen allen in één activiteit.
>
>Zeer complexe activiteiten moeten worden herzien met [!DNL Adobe] Consulting en tests in een beperkte omgeving voordat ze worden vrijgegeven voor productie.

## Activiteiten

### Activiteitennamen

* **Limiet**: 250 tekens.

### Aantal activiteiten per rekening

* **Aanbevolen limiet**: 10.000 actieve live-activiteiten.

* **Aanbevolen limiet**: 10.000 actieve opgeslagen (en niet beëindigde) activiteiten.

## API-aanroepen van doel

* **Limiet**: 50 aanroepen per minuut voor de API&#39;s Admin, Reporting en bulkprofielupdate. Deze limiet geldt niet voor de API&#39;s voor levering en één profiel bijwerken.

  Als u meer dan 50 API vraag per minuut maakt, [!DNL Target] retourneert een foutbericht &quot;503 HTTP status&quot;.

## Soorten publiek

### Namen publiek

* **Limiet**: 255 tekens.

### Soorten publiek, herbruikbaar per account

* **Aanbevolen limiet**: 20.000 publiek.

### Aantal soorten publiek per doos, metrisch, of ervaring

* **Limiet**: 50 soorten publiek

## categoryId, parameter

* **Limiet**: 256 tekens.

## Inhoud leveren {#content-delivery}

* **Limiet**: 100 gelijktijdige [!DNL Target] aanvragen voor de levering van inhoud per gebruikerssessie.

  Als een klant meer dan 100 gelijktijdige [!DNL Target] verzoeken om de levering van inhoud voor een bepaalde gebruikerssessie, alle volgende aanvragen voor die gebruikerssessie worden geblokkeerd. Twee of meer verzoeken worden beschouwd als gelijktijdig als zij allen naar [!DNL Target] -server voordat de reactie voor een van de reacties wordt ontvangen. [!DNL Target] verwerkt opeenvolgende gezamenlijke aanvragen voor dezelfde sessie.

   * **Foutgedrag**:

      * Delivery API and Batch Mbox v2:
         * Foutcode: HTTP 420 Te veel aanvragen
         * Foutbericht: &quot;Te veel aanvragen met dezelfde sessie-id&quot;

      * Verouderde mbox-API:
         * Standaardinhoud met opmerking &quot;Te veel aanvragen met dezelfde sessie-id&quot;

      * at.js:
         * Standaardinhoud weergegeven

* **Limiet**: 50 dozen per [!DNL Target] aanvraag voor batchverwerking van inhoud.

  van meer dan 50 dozen per doos [!DNL Target] inhoud leveren batch-aanvraag resulteert in een foutcode voor reactie `HTTP 400` met foutbericht `size must be between 0 and 50`.

  De verzoeken van de partijdoos worden opeenvolgend verwerkt, die de algemene reactietijd met elke herhaling verhogen. Hoe meer vakjes in het batchverzoek, des te meer responslatentie kan worden verwacht en daarom is er mogelijk time-outs. Als de ervaring het teruggeven op deze hoge latentiepartijverzoeken wordt geblokkeerd, zou de latentie in een degraded gebruikerservaring kunnen resulteren aangezien de gebruikers op ervaringen wachten om terug te geven.

* **Limiet**: 60 MB de lichaamsomvang van de POST van HTTP voor [!DNL Target] verzoeken om levering van inhoud.

  Meer dan 60 MB op de lichaamsgrootte van de POST van HTTP [!DNL Target] de leveringsaanvraag van de inhoud resulteert in een code van de reactiefout `HTTP 413 Request Entity Too Large`.

* **Aanbevolen limiet**: 50 meldingen per [!DNL Target] aanvraag voor leveringsbatch.

  Meer dan 50 meldingen per [!DNL Target] aanvraag voor de leveringsbatch leidt waarschijnlijk tot meer responslatentie en time-outs.

  De verzoeken van het partijbericht worden opeenvolgend verwerkt, die de algemene reactietijd met elke herhaling verhogen. Hoe meer meldingen over het batchverzoek, des te meer responslatentie kan worden verwacht, en dus ook de mogelijkheid van time-outs. Sommige extra latentie op de verzoeken van het partijbericht zou voor sommige klanten aanvaardbaar kunnen zijn, maar ben zich ervan bewust dat onderbrekingen en om het even welke verdere pogingen nog latentie zouden kunnen veroorzaken.

## Klantkenmerken

### Kenmerknamen van klant

* **Limiet**: 250 tekens via feed of API.

### Aliasid van kenmerk Klant

* **Limiet** 50 tekens.

### Klantkenmerken, uploaden

* **Maximale bestandsgrootte voor elke upload met de HTTP-methode**: 100 MB.
* **maximale bestandsgrootte voor elke upload met de FTP-methode**: 4 GB.
* **Aantal toegestane kenmerken voor abonnement**: 5 for [!DNL Target Standard] en 200 voor [!DNL Target Premium].

## Entiteiten

### Aantal entiteiten

* Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, is 99, ofwel hardcoded ofwel via lussen.
* De aanbevolen limiet voor de beste prestaties is om de catalogus minder dan 1 miljoen items per omgeving en minder dan 10 miljoen items in alle omgevingen te houden.
* De maximumgrens is tien miljoen punten per milieu en 100 miljoen punten over alle milieu&#39;s. Als u tussen één miljoen en tien miljoen punten per milieu hebt, prestaties [!UICONTROL Catalog Search] De interface is hierdoor beïnvloed. [!DNL Target Recommendations], maar blijft aanbevelingen opstellen en doen.

### Aangepaste kenmerken van entiteit

* **Aangepaste entiteitskenmerken**: 100.

* **Limiet tekens**: De maximale tekenlengte is afhankelijk van de taal.

   * 15.000 tekens (talen van één waarde, van één en van twee bytes)
   * 500 waarden, 100 tekens per waarde (meerdere waarden)

  De maximale lengte van aangepaste kenmerken van entiteiten met een enkele waarde is 15.000 tekens (voor UTF-8-gecodeerde talen van één byte en twee byte, zoals Engelse en andere Latijnse alfabeten) of 10.000 tekens (voor UTF-8-gecodeerde talen van drie bytes, zoals Chinees, Japans en Koreaans).

  Aangepaste kenmerken van entiteiten met meerdere waarden mogen niet meer dan 500 waarden bevatten. Elke individuele waarde is beperkt tot 100 tekens. Het totale aantal tekens voor alle waarden moet in overeenstemming zijn met de beperkingen voor de maximumlengte van aangepaste attributen voor entiteiten met één waarde (zie hierboven).

### entity.id

* **Limiet voor implementaties waarvoor aankoopgegevens moeten worden vastgelegd**: 50 tekens.

  Deze limiet geldt omdat de `productPurchasedId` met de parameter mbox wordt het bestand entity.ids vastgelegd. Dit beperkt het aantal tekens tot 50.

* **Limiet voor implementaties die alleen op weergave gebaseerde algoritmen vereisen:**: 1.000 tekens.

  Op weergave gebaseerde algoritmen zijn onder andere weergave/weergave, meest bekeken, onlangs weergegeven enzovoort.

## excludeIds {#excludedid}

* **Limiet**: 5 kB voor verzoeken om POST. 2.083 tekens min de lengte van de URL voor aanvragen van GET.

  Voor GET-aanvragen geldt dat, hoewel de limiet voor het achterste gedeelte 5 kB is, omdat Microsoft Internet Explorer de URL beperkt tot 2083 tekens, de realistische limiet 2083 tekens min de huidige lengte van de URL is.

## Ervaringen

### Ervaringsnamen

* **Limiet**: 50 tekens.

### Ervaringen per activiteit

* **Limiet**: 2.000 ervaringen per [!UICONTROL Experience Targeting] (XT), [!UICONTROL A/B Test], [!UICONTROL Multivariate Test] (MVT), en [!UICONTROL Auto-Target] activiteit.

  30.000 ervaringen per Automated Personalization (AP) activiteit.

### Wijzigingen per ervaring

* **Limiet**: 50 per ervaring op elke activiteit

## mboxes

### In-box-profielkenmerkwaarde {#in-mbox}

* **Limiet**: 256 tekens.

  Waarden van meer dan 256 tekens worden afgebroken bij gebruik van at.js 1.*x*. Er wordt een foutbericht weergegeven wanneer u waarden met meer dan 256 tekens verzendt bij gebruik van at.js 2.*x* of de [!DNL Adobe Experience Platform Web SDK]. Waarden worden niet automatisch afgekapt.

### In-box-profielnamen

* **Limiet**: 128 tekens.

### mbox-namen {#mbox-names}

* **Limiet**: 250 tekens.

  Voor levering-API (at.js 2.*x*), Batch mbox V2, en AEP Web SDK (alloy.js) integraties, mbox namen *kan* bevatten alfanumerieke tekens (A-Z, a-z, 0-9) en een of meer van de volgende tekens:

  ```
  - , . _ / = ` : ; & ! @ # $ % ^ & * ( ) _ + | ? ~ [ ] { }
  ```

  Voor om.js 1.*x* integraties, mbox-namen *kan* bevatten een van de volgende tekens:

  ```
  ' " %22 %27 < > %3C %3E 
  ```

### mbox-parameters {#mbox-parameters}

* **Limiet**: De volgende limieten gelden voor mbox-parameters:

  Voor standaard mbox vraag:

   * mbox-parameters: 500 parameters per mbox.
   * Profielparameters: 500 parameters van het parameterprofiel per mbox.
   * Andere parameters (URL, verwijzende URL, enz.): 50 per mbox voor elk ander parametertype.

  Deze limieten zijn van toepassing, tenzij de aanvraag wordt ingekort vanwege beperkingen in de webbrowser.

  Als u de Batch Delivery-API gebruikt, is de limiet 50 dozen per aanvraag voor de batch.

  Als u de Batch Delivery-API in de Mobile Services SDK gebruikt, zijn de limiet van 50 mbox-parameters, 50 profielparameters en 50 voor andere parametertypen beperkingen van de API zelf. Het is niet mogelijk om een aanvraag met meer dan deze nummers te verzenden via de Batch Delivery-API. Als een aanvraag meer dan deze limieten bevat, retourneert de API het volgende foutbericht:

  &quot;Het aantal mboxParameters mag niet groter zijn dan 50.&quot;

  Limieten ingesteld voor eindpunten:

  **Batchbox v2**:

   * mbox-parameters 100
   * naam van parameter mbox max. lengte 128
   * parameterwaarde mbox mag niet null zijn
   * parameterwaarde mbox 5000
   * profielparameters 50
   * naam van profielparameter max. lengte 128
   * waarde van profielparameter mag niet null zijn
   * waarde van profielparameter max. lengte 5000

  **API-eindpunt voor levering**:

   * mbox-parameters 100
   * naam van parameter mbox max. lengte 128
   * parameterwaarde mbox mag niet null zijn
   * parameterwaarde mbox 5000
   * profielparameters 50
   * naam van profielparameter max. lengte 128
   * waarde van profielparameter mag niet null zijn
   * waarde van profielparameter max. lengte 5000

### verzoek-URL&#39;s

* **Limiet**: 2.083 tekens.

  Deze limiet is het gevolg van beperkingen voor de URL-lengte van Microsoft Internet Explorer.

### mbox3rdPartyId, parameter

* **Limiet**: 256 tekens.

## Aanbiedingen

### Aanbiedingsnamen

* **Limiet**: 250 tekens.

### Aantal aanbiedingen

* **Aanbevolen limiet**: in totaal 50.000 aanbiedingen.

### Grootte voorstel {#offer-size}

Voor aanbiedingen gelden de volgende groottegrenzen:

* 1024 kB voor aanbiedingen van HTML.
* 1024 kB (voor elke ervaring) voor visuele aanbiedingen van UI.
* 1024 kB vanaf de API.

  Als u een globale box gebruikt, is de grens voor de volledige reeks inhoud teruggekeerd voor de pagina. Door het beperken van de aanbiedingsgrootte worden de laadtijden van de pagina verbeterd. Als de limiet wordt overschreden, wordt het volgende bericht weergegeven:

  &quot;De inhoud voor de ervaring is te groot om te leveren. Pas de ervaring aan om minder paginacode te beïnvloeden.&quot;

## orderId, parameter

* **Aanbevolen limiet**: 120 tekens.

## orderTotal, parameter

* **Aanbevolen limiet**: 120 tekens.

## productPurchasedId, parameter

* **Limiet**: 50 tekens per door komma&#39;s gescheiden waarde en 250 tekens in totaal. Individuele waarden van meer dan 50 tekens worden door het systeem afgekapt. Totale lengte boven 250 tekens resulteert in een fout van 400.

## Profielscripts

* **Aanbevolen limiet voor actieve profielscripts (die zijn ingeschakeld)**: 300

* **Aanbevolen limiet voor totale profielscripts per account**: 2.000

* **Recommendations voor het beperken van de complexiteit van profielscripts**: Profielscripts kunnen een beperkt aantal instructies uitvoeren. Zie voor meer informatie [Aanbevolen procedures](/help/main/c-target/c-visitor-profile/profile-parameters.md#best) in *Profielkenmerken*.

## Eigenschappen

* **Aanbevolen limiet**: 5.000 eigenschappen.

## Publiek/segmenten rapporteren

* **Limiet**: 50 verslaggevingspubliek/segmenten per activiteit.

## Script-profielinvoervak in het dialoogvenster [!DNL Target] UI

* **Aanbevolen limiet**: 2.000 tekens.

  Afhankelijk van de grootte van de gecodeerde tekenreeks, die veel langer kan zijn dan de onbewerkte tekenreeks. Als de tekenreeks te groot is, mislukt deze voordat deze wordt uitgevoerd [!DNL Adobe Target].

## Scriptprofielen

### Scriptprofielnamen

* **Limiet**: 50 tekens.

### Scriptprofielwaarden

* **Limiet**: 2.048 tekens.

  Om prestatieredenen raden we een geretourneerde waarde aan die niet langer is dan 256 tekens.

  Als de geretourneerde waarde van een tekenreeks groter is dan 2.048 tekens, wordt het script door het systeem uitgeschakeld.

  Als voor een geretourneerde waarde van een array de grootte van de samengevoegde waarden van de array groter is dan 2.048 tekens, wordt het script door het systeem uitgeschakeld.

## Succeswaarden

* **Limiet**: 200 per activiteit.

## Targeting

### Doelvoorwaarden

* **Aanbevolen limiet**: 1.000 waarden.

  Dit verwijst naar het aantal waarden met regelscheiding in het tekstgebied dat als doel is ingesteld. U kunt bijvoorbeeld 1000 ZIP-codes invoeren in een ZIP-codedoel.

### Doelstellingen {#targeting-rules}

* **Aanbevolen limiet**: 2.500 tekens per doelregelwaarde.
* **Aanbevolen limiet**: 50.000 unieke waarden per publiek over het richten van regels.
* **Aanbevolen limiet**: 100.000 unieke waarden voor doelregels per activiteit.
