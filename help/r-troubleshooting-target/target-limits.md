---
keywords: tekenlimiet;mbox-parameters;batch-levering api;profielparameters;limieten;ingebouwde profielen;maximum;limit;constraint;character;best practice;orderTotal;mbox3rdPartyID;category;categoryID;problemen oplossen
description: Een lijst weergeven met tekenlimieten en andere limieten (grootte van aanbieding, publiek, profielen, waarden, parameters, enz.) die van invloed zijn op activiteiten en andere elementen in Adobe Target.
title: Wat zijn de verschillende tekens, grootte en andere limieten in Adobe Target?
feature: Problemen oplossen
mini-toc-levels: 3
exl-id: b318ab16-1382-4f3a-8764-064adf384d6b
source-git-commit: 7badceff58e00f8406d24621534d24ea4067a224
workflow-type: tm+mt
source-wordcount: '1362'
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
>Zeer complexe activiteiten moeten worden beoordeeld met [!DNL Adobe] Consulting en worden getest in een beperkte omgeving voordat ze worden vrijgegeven voor productie.

## Activiteiten

### Activiteitennamen

* **Limiet**: 250 tekens.

### Aantal activiteiten per rekening

* **Aanbevolen limiet**: 10.000 actieve live activiteiten.

* **Aanbevolen limiet**: 10.000 actieve opgeslagen (en niet beëindigde) activiteiten.

## API-aanroepen van doel

* **Limiet**: 50 aanroepen per minuut voor de API&#39;s Admin, Reporting en bulkprofielupdate. Deze limiet geldt niet voor de API&#39;s voor levering en één profiel bijwerken.

   Als u meer dan 50 API vraag per minuut maakt, [!DNL Target] keert een &quot;503 HTTP status&quot;foutenmelding terug.

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

* **Limiet**: 100 gelijktijdige aanvragen voor  [!DNL Target] inhoudslevering per gebruikerssessie.

   Als een klant meer dan 100 gelijktijdige [!DNL Target] verzoeken om inhoud voor een bepaalde gebruikerssessie indient, worden alle volgende verzoeken voor die gebruikerssessie geblokkeerd. Twee of meer verzoeken worden beschouwd als gelijktijdig als ze allemaal naar de [!DNL Target]-server worden verzonden voordat de reactie voor een van deze verzoeken wordt ontvangen. [!DNL Target] verwerkt opeenvolgende gezamenlijke aanvragen voor dezelfde sessie.

* **Foutgedrag**:

   * Delivery API and Batch Mbox v2:
      * Foutcode: HTTP 420 Te veel verzoeken
      * Foutbericht: &quot;Te veel aanvragen met dezelfde sessie-id&quot;
   * Verouderde mbox-API:
      * Standaardinhoud met opmerking &quot;Te veel aanvragen met dezelfde sessie-id&quot;
   * at.js:
      * Standaardinhoud weergegeven



## Klantkenmerken

### Kenmerknamen van klant

* **Limiet**: 250 tekens via feed of API.

### Aliasid van kenmerk Klant

* **Maximaal**  50 tekens.

### Klantkenmerken, uploaden

* **Maximale bestandsgrootte voor elke upload met de HTTP-methode**: 100 MB.
* **maximale bestandsgrootte voor elke upload met de FTP-methode**: 4 GB.
* **Aantal kenmerken dat mag worden geabonneerd**: 5 voor  [!DNL Target Standard] en 200 voor  [!DNL Target Premium].

## Entiteiten

### Aantal entiteiten

* Het maximumaantal entiteiten waarnaar in een ontwerp kan worden verwezen, is 99, ofwel hardcoded ofwel via lussen.
* De aanbevolen limiet voor de beste prestaties is om de catalogus minder dan 1 miljoen items per omgeving en minder dan 10 miljoen items in alle omgevingen te houden.
* De maximumgrens is tien miljoen punten per milieu en 100 miljoen punten over alle milieu&#39;s. Als u tussen één miljoen en tien miljoen punten per milieu hebt, worden de prestaties van [!UICONTROL Catalog Search] UI beïnvloed. [!DNL Target Recommendations], maar blijft aanbevelingen opstellen en doen.

### Aangepaste kenmerken van entiteit

* **Kenmerken** van aangepaste entiteit: 100.

* **Limiet** tekens: De maximale tekenlengte is afhankelijk van de taal.

   * 15.000 tekens (talen van één waarde, van één en van twee bytes)
   * 500 waarden, 100 tekens per waarde (meerdere waarden)

   De maximale lengte van aangepaste kenmerken van entiteiten met een enkele waarde is 15.000 tekens (voor UTF-8-gecodeerde talen van één byte en twee byte, zoals Engelse en andere Latijnse alfabeten) of 10.000 tekens (voor UTF-8-gecodeerde talen van drie bytes, zoals Chinees, Japans en Koreaans).

   Aangepaste kenmerken van entiteiten met meerdere waarden mogen niet meer dan 500 waarden bevatten. Elke individuele waarde is beperkt tot 100 tekens. Het totale aantal tekens voor alle waarden moet in overeenstemming zijn met de beperkingen voor de maximumlengte van aangepaste attributen voor entiteiten met één waarde (zie hierboven).

### entity.id

* **Limiet voor implementaties waarvoor aankoopgegevens** moeten worden vastgelegd: 50 tekens.

   Deze beperking wordt afgedwongen omdat de parameter `productPurchasedId` mbox de entiteit.ids vangt, die het karakteraantal tot 50 beperkt.

* **Limiet voor implementaties die alleen op weergave gebaseerde algoritmen vereisen:**: 1.000 tekens.

   Op weergave gebaseerde algoritmen zijn onder andere weergave/weergave, meest bekeken, onlangs weergegeven enzovoort.

## excludeIds {#excludedid}

* **Limiet**: 5 kB voor verzoeken van de POST. 2.083 tekens min de lengte van de URL voor aanvragen van GET.

   Voor verzoeken van GET, hoewel de grens op het achtereind 5 KB is, wegens het feit dat Microsoft Internet Explorer URL tot 2.083 karakters beperkt, is de realistische grens 2.083 karakters minus de huidige lengte van URL.

## Ervaringen

### Ervaringsnamen

* **Limiet**: 50 tekens.

### Ervaringen per activiteit

* **Limiet**: 2.000 ervaringen per ervaring gericht (XT), A/B Test, Multivariate Test (MVT), en auto-doelactiviteit.

   30.000 ervaringen per Automated Personalization (AP) activiteit.

### Wijzigingen per ervaring

* **Limiet**: 50 per ervaring op enige activiteit

## mboxes

### In-box-profielkenmerkwaarde

* **Limiet**: 256 tekens.

   Waarden die langer zijn dan deze worden afgebroken.

### In-box-profielnamen

* **Limiet**: 128 tekens.

### mbox-namen

* **Limiet**: 250 tekens.

### mbox-parameters

* **Limiet**: De volgende limieten gelden voor mbox-parameters:

   Voor standaard mbox-aanroepen:

   * mbox-parameters: 500 parameters per mbox.
   * Profielparameters: 500 parameters van het parameterprofiel per mbox.
   * Andere parameters (URL, verwijzende URL, enz.): 50 per mbox voor elk ander parametertype.

   Deze limieten zijn van toepassing, tenzij de aanvraag wordt ingekort vanwege beperkingen in de webbrowser.

   Als u de Batch Delivery-API gebruikt, is de limiet 50 dozen per aanvraag voor de batch.

   Als u de [Batch Delivery API](https://developers.adobetarget.com/api/#server-side-batch-delivery) in de Mobile Services SDK gebruikt, zijn de limiet van 50 mbox-parameters, 50 profielparameters en 50 voor andere parametertypen beperkingen van de API zelf. Het is niet mogelijk om een aanvraag met meer dan deze nummers te verzenden via de Batch Delivery-API. Als een aanvraag meer dan deze limieten bevat, retourneert de API het volgende foutbericht:

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

   **API-eindpunt** van levering:

   * mbox-parameters 100
   * naam van parameter mbox max. lengte 128
   * parameterwaarde mbox mag niet null zijn
   * parameterwaarde mbox 5000
   * profielparameters 50
   * naam van profielparameter max. lengte 128
   * waarde van profielparameter mag niet null zijn
   * waarde van profielparameter max. lengte 256



### verzoek-URL&#39;s

* **Limiet**: 2.083 tekens.

   Deze limiet is het gevolg van lengtebeperkingen voor Microsoft Internet Explorer URL.

### mbox3rdPartyId, parameter

* **Limiet**: 60 tekens.

## Aanbiedingen

### Aanbiedingsnamen

* **Limiet**: 250 tekens.

### Aantal aanbiedingen

* **Aanbevolen limiet**: in totaal 50.000 aanbiedingen.

### Grootte voorstel {#offer-size}

Voor aanbiedingen gelden de volgende groottegrenzen:

* 1024 kB voor HTML-aanbiedingen.
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

* **Aanbevolen limiet voor totale profielscripts per account**: 2 000

* **Recommendations voor het beperken van de complexiteit** van profielscripts: Profielscripts kunnen een beperkt aantal instructies uitvoeren. Zie [Beste werkwijzen](/help/c-target/c-visitor-profile/profile-parameters.md#best) in *Profielkenmerken* voor meer informatie.

## Eigenschappen

* **Aanbevolen limiet**: 5.000 eigenschappen.

## Publiek/segmenten rapporteren

* **Limiet**: 50 verslaggevingspubliek/segmenten per activiteit.

## Invoervak voor scriptprofiel in de gebruikersinterface [!DNL Target]

* **Aanbevolen limiet**: 2000 tekens.

   Afhankelijk van de grootte van de gecodeerde tekenreeks, die veel langer kan zijn dan de onbewerkte tekenreeks. Als de tekenreeks te groot is, mislukt deze voordat deze naar Adobe Target gaat.

## Scriptprofielen

### Scriptprofielnamen

* **Limiet**: 50 tekens.

### Scriptprofielwaarden

* **Limiet**: 2048 tekens.

   Om prestatieredenen raden we een geretourneerde waarde aan die niet langer is dan 256 tekens.

   Als de geretourneerde waarde van een tekenreeks groter is dan 2.048 tekens, wordt het script door het systeem uitgeschakeld.

   Als voor een geretourneerde waarde van een array de grootte van de samengevoegde waarden van de array groter is dan 2.048 tekens, wordt het script door het systeem uitgeschakeld.

## Succeswaarden

* **Limiet**: 200 per activiteit.

## Doelstelling

### Doelvoorwaarden

* **Aanbevolen limiet**: 1.000 waarden.

   Dit verwijst naar het aantal waarden met regelscheiding in het tekstgebied dat als doel is ingesteld. U kunt bijvoorbeeld 1000 ZIP-codes invoeren in een ZIP-codedoel.

### Doelstellingen

* **Aanbevolen limiet**: 2.500 tekens per doelregelwaarde.
* **Aanbevolen limiet**: 30.000 unieke waarden per publiek over het richten van regels.
* **Aanbevolen limiet**: 100.000 unieke waarden voor richtingsregels per activiteit.
