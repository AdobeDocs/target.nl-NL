---
keywords: implement;implementing;setting up;setup;page parameter;tomcat;url encoded;in-page profile attribute;mbox parameter;in-page profile attributes;script profile attribute;bulk profile update API;single file update API;customer attributes;data providers;dataprovider;data provider
description: Informatie over de verschillende methoden die u kunt gebruiken om gegevens op te halen uit Target, zoals paginaparameters, paginageprofielkenmerken, kenmerken van scriptprofielen, gegevensproviders, de API voor bulkprofielupdate, de single-profile-update-API en klantkenmerken.
title: Methoden om gegevens op te halen in Doel
feature: null
subtopic: Getting Started
topic: Standard
uuid: a6d64e39-6cdc-49fe-afe5-ecf7dcacf97d
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---


# Methoden om gegevens op te halen in Doel{#methods-to-get-data-into-target}

Informatie over de verschillende methoden die u kunt gebruiken om gegevens op te halen uit Target, zoals paginaparameters, paginageprofielkenmerken, scriptprofielkenmerken, gegevensproviders, de API voor het bijwerken van bulkprofielen, de single-profile-update-API en klantkenmerken.

## Paginaparameters (ook wel &quot;parameters mbox&quot; genoemd) {#section_5A297816173C4FE48DC4FE03860CB42B}

Paginaparameters zijn naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik.

Paginaparameters zijn handig voor het verzenden van aanvullende paginagegevens naar Doel die niet met het profiel van de bezoeker hoeven te worden opgeslagen voor toekomstig doelgebruik. Deze waarden worden in plaats daarvan gebruikt om de pagina of de actie te beschrijven die de gebruiker op de specifieke pagina heeft ondernomen.

### Indeling

De parameters van de pagina worden overgegaan in Doel via een servervraag als koordnaam/waardepaar. Parameternamen en -waarden kunnen worden aangepast (hoewel er enkele &#39;gereserveerde namen&#39; zijn voor specifieke toepassingen).

Voorbeelden:

* `page=productPage`

* `categoryId=homeLoans`

### Voorbeelden

**Productpagina**&#39;s: Informatie verzenden over het bekeken specifieke product (dit is de manier waarop Recommendations werkt)

**Bestelgegevens**: Order-id, orderTotal enzovoort verzenden voor het verzamelen van bestellingen

**Categorie-affiniteit**: Door een categorie bekeken informatie naar Doel verzenden om kennis van de affiniteit van de gebruiker met bepaalde sitecategorieën te vergroten

**Gegevens** van derden: Verstuur informatie van derde gegevensbronnen, zoals weergerichte leveranciers, rekeningsgegevens (bijvoorbeeld, DemandBase), demografische gegevens (bijvoorbeeld Experian), en meer.

### Voordelen van methode

De gegevens worden verzonden naar Doel in real time, en kunnen op de zelfde servervraag worden gebruikt de gegevens waarop het binnen komt.

### Caveats

* Vereist een update van de paginacode (direct of via een systeem van het markeringsbeheer).
* Als de gegevens voor het richten op een volgende pagina/servervraag moeten worden gebruikt, moet het in een profielmanuscript worden vertaald.
* De koorden van de vraag kunnen slechts karakters volgens de norm [van de Techniek van de Techniek van](https://www.ietf.org/rfc/rfc3986.txt) Internet (IETF) bevatten.

   Naast die vermeld op de plaats IETF, staat het Doel de volgende karakters in vraagkoorden toe:

   `&lt; > # % &quot; { } | \\ ^ \[\] \``

   Al het andere moet met url gecodeerd zijn. De standaard geeft de volgende notatie aan ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ), zoals hieronder wordt geïllustreerd:

   ![](assets/ietf1.png)

   Of, de volledige lijst voor eenvoud:

   ![](assets/ietf2.png)

### Codevoorbeelden

targetPageParamsAll (voegt de parameters aan alle mbox vraag op de pagina toe):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams (voegt de parameters aan globale mbox op de pagina toe):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

Parameters in mboxCreate-code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

### Koppelingen naar relevante informatie

Recommendations: [Implementatie volgens paginatype](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

Bevestiging van bestelling: [Conversies bijhouden](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

Categorie-affiniteit: [Categorie-affiniteit](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)

## Profielkenmerken in pagina (ook wel &#39;profielkenmerken in de box&#39; genoemd) {#section_57E1C161AA7B444689B40B6F459302B6}

Profielkenmerken in pagina zijn naam-/waardeparen die rechtstreeks door paginacode worden doorgegeven en die in het profiel van de bezoeker worden opgeslagen voor toekomstig gebruik.

Met profielkenmerken van pagina&#39;s kunnen gebruikersspecifieke gegevens in het doelprofiel worden opgeslagen, zodat deze later kunnen worden toegewezen en gesegmenteerd.

### Indeling

Profielkenmerken in pagina&#39;s worden doorgegeven aan Target via een serveraanroep als een naam-/waardepaar met het voorvoegsel &quot;profiel&quot;. vóór de kenmerknaam.

Kenmerknamen en -waarden kunnen worden aangepast (hoewel er enkele &#39;gereserveerde namen&#39; zijn voor specifieke toepassingen).

Voorbeelden:

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

### Voorbeelden

**Aanmeldingsgegevens**: Deel niet-PII (Persoonlijk Identificeerbare Informatie) gegevens aan Doel die op login van de gebruiker wordt gebaseerd. Dit kan lidmaatschapsstatus, ordergeschiedenis of meer zijn.

**Winkelgegevens**: Houd bij welke winkel de voorkeurslocatie van deze gebruiker is.

**Vorige interacties**: Volg wat de gebruiker eerder op de site heeft gedaan om toekomstige personalisatie te informeren.

### Voordelen van methode

De gegevens worden verzonden naar Doel in real time, en kunnen op de zelfde servervraag worden gebruikt waarop de gegevens binnen komen.

### Caveats

Vereist updates van paginacode (direct of via een systeem van het markeringsbeheer).

Kenmerken en waarden zijn zichtbaar in serveraanroepen, zodat een bezoeker de waarden kan zien. Als het delen van informatie zoals kredietbereiken of andere potentieel particuliere informatie, zou dit niet de beste benadering kunnen zijn.

### Codevoorbeelden

targetPageParamsAll (voegt de kenmerken toe aan alle mbox-aanroepen op de pagina):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (voegt de kenmerken toe aan het globale mabox op de pagina):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attributen in mboxCreate code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

### Koppelingen naar relevante informatie

[Profielkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Bezoekerprofiel](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)

## Scriptprofielkenmerken {#section_3E27B58C841448C38BDDCFE943984F8D}

Scriptprofielkenmerken zijn naam-/waardeparen die zijn gedefinieerd in de doeloplossing. De waarde wordt bepaald door het uitvoeren van een JavaScript-fragment op de server van Target per serveraanroep.

Gebruikers schrijven kleine codefragmenten die per mbox vraag uitvoeren, en alvorens een bezoeker voor publiek en activiteitenlidmaatschap wordt geëvalueerd.

### Indeling

Scriptprofielkenmerken worden gemaakt in de sectie Soorten publiek van Doel. Elke kenmerknaam is geldig en de waarde is het resultaat van een JavaScript-functie die door de doelgebruiker is geschreven. De kenmerknaam wordt automatisch voorafgegaan door &quot; gebruiker. &quot; in Doel om ze te onderscheiden van de profielkenmerken in de pagina.

Het codefragment wordt geschreven in de taal Rhino JS en kan naar tokens en andere waarden verwijzen.

### Voorbeelden

**Afschaffing** van winkelwagentje: Wanneer de bezoeker het winkelwagentje bereikt, stelt u het profielscript in op 1. Wanneer de bezoeker omzet, stel het aan 0 terug. Als de waarde =1 is, bevat de bezoeker een item in de winkelwagentje.

**Aantal** bezoeken: Bij elk nieuw bezoek verhoogt u het aantal met 1 om te controleren hoe vaak een bezoeker naar de site terugkeert.

### Voordelen van methode

Er zijn geen updates van paginacode vereist.

Voert uit vóór publiek en de besluiten van het activiteitenlidmaatschap, zodat kunnen deze attributen van het profielmanuscript lidmaatschap op één enkele servervraag beïnvloeden.

Kan zeer robuust zijn. Er kunnen maximaal 2000 instructies per script worden uitgevoerd.

### Caveats

Hiervoor is JavaScript-kennis vereist.

De uitvoeringsvolgorde van profielscripts kan niet worden gegarandeerd, zodat ze niet op elkaar kunnen vertrouwen.

Kan moeilijk zijn om fouten op te sporen.

### Codevoorbeelden

Profielscripts zijn tamelijk flexibel:

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### Koppelingen naar relevante informatie

[Profielscriptkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)

## Gegevensleveranciers {#section_14FF3BE20DAA42369E4812D8D50FBDAE}

Gegevensleveranciers zijn een mogelijkheid waarmee u gegevens van derden eenvoudig aan Doel kunt doorgeven.

Opmerking: Data Providers vereist op .js 1.3 of hoger.

### Indeling

De `window.targetGlobalSettings.dataProviders` instelling is een array met gegevensproviders.

Voor meer informatie over de structuur voor elke gegevensleverancier, zie de Leveranciers van [Gegevens](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

### Voorbeelden

Verzamel gegevens van derden, zoals een weerservice, een DMP of zelfs uw eigen webservice. Vervolgens kunt u deze gegevens gebruiken om een publiek te maken, inhoud te benoemen en het profiel van de bezoeker te verrijken.

### Voordelen van methode

Met deze instelling kunnen klanten gegevens verzamelen van gegevensleveranciers van derden, zoals Demandbase, BlueKai en aangepaste services, en de gegevens doorgeven aan Target als mbox-parameters in het algemene mbox-verzoek.

Het steunt de inzameling van gegevens van veelvoudige leveranciers via async en synchronisatieverzoeken.

Op deze manier kunt u flikkering van de standaardpagina-inhoud eenvoudig beheren en onafhankelijke time-outs opnemen voor elke provider om de invloed op de paginaprestaties te beperken

### Caveats

Als de gegevensleveranciers aan worden toegevoegd asynchroon `window.targetGlobalSettings.dataProviders` zijn, zullen zij parallel worden uitgevoerd. De aanvraag voor de Bezoeker-API wordt parallel met de toegevoegde functies uitgevoerd `window.targetGlobalSettings.dataProviders` om een minimale wachttijd mogelijk te maken.

at.js zal niet proberen om de gegevens in het voorgeheugen onder te brengen. Als de gegevensleverancier gegevens slechts één keer haalt, zou de gegevensleverancier ervoor moeten zorgen dat de gegevens in het voorgeheugen wordt opgeslagen en, wanneer de leveranciersfunctie wordt aangehaald, de geheim voorgeheugengegevens voor de tweede aanroeping dienen.

### Codevoorbeelden

Verschillende voorbeelden zijn te vinden in [Data Providers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers).

### Koppelingen naar relevante informatie

Documentatie: [Gegevensleveranciers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers)

### Trainingsvideo&#39;s:

* [Gegevensleveranciers gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html)
* [Gegevensleveranciers implementeren in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html)

## Bulkprofielupdate-API {#section_92AB4820A5624C669D9A1F1B6220D4FA}

Verzend via de API een CSV-bestand naar Target met updates van het bezoekersprofiel voor veel bezoekers. Elk bezoekersprofiel kan met veelvoudige in-pagina profielattributen in één vraag worden bijgewerkt.

Deze optie lijkt sterk op Customer Attributes met een paar verschillen:

* Klantkenmerken gebruiken een FTP-upload terwijl de API voor het bijwerken van het doelbulkprofiel een HTTP-POST-API gebruikt.
* De gegevens van de Attributen van de klant kunnen met Analytics worden gedeeld. Bulkprofielupdate kan alleen worden gebruikt in Doel.
* De steun van de Attributen van de klant die tot een profiel voor een gebruikersDoel leidt heeft nog niet gezien. De API voor het bijwerken van het bulkprofiel werkt alleen bestaande doelprofielen bij.
* Klantkenmerken vereisen het gebruik van de Experience Cloud-id (ECID). Voor de API voor het bijwerken van het bulkprofiel is de TNT-id of de `mbox3rdPartyId`TNT-id vereist.
* U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plus-teken (+) en slash (/).

### Indeling

Het .csv-bestand moet naar elke bezoeker verwijzen via zijn of haar doel-PCID of mboxThirdPartyId. De Experience Cloud-id (ECID) wordt niet ondersteund. Alle profielkenmerken/waarden worden gemaakt en bijgewerkt via de API. De indelingsgegevens zijn beschikbaar in de API-documentatie.

### Voorbeelden

Uw CRM of ander intern systeem slaat waardevolle gegevens over uw bezoekers op die u constant in Doel wilt bijwerken, zonder de profielgegevens in uw paginaimplementatie bloot te stellen.

### Voordelen van methode

Geen limiet voor het aantal profielkenmerken.

Profielkenmerken die via de site worden verzonden, kunnen via de API worden bijgewerkt en andersom.

### Caveats

Het batchbestand moet kleiner zijn dan 50 MB. Bovendien mag het totale aantal rijen niet groter zijn dan 500.000 rijen per upload.

Er geldt geen limiet voor het aantal rijen dat of de rijen die u kunt uploaden over een periode van 24 uur in volgende batches. Nochtans, zou het innameproces tijdens kantooruren kunnen worden vertraagd om ervoor te zorgen dat andere processen efficiënt lopen.

Opeenvolgende [V2 vraag](https://developers.adobetarget.com/api/#updating-profiles) van de partijupdate zonder mbox vraag binnen tussen voor zelfde thirdPartyIds treedt de eigenschappen met voeten die in de eerste vraag van de partijupdate worden bijgewerkt.

### Codevoorbeelden

Zie Profielen [bijwerken](https://developers.adobetarget.com/api/#updating-profiles).

### Koppelingen naar relevante informatie

[Profielen bijwerken](https://developers.adobetarget.com/api/#updating-profiles)

## API voor bijwerken van één profiel {#section_5D7A9DD7019F40E9AEF2F66F7F345A8D}

Bijna identiek aan de API voor het bijwerken van het bulkprofiel, maar één bezoekersprofiel wordt tegelijk bijgewerkt, in lijn in de API-aanroep in plaats van met een .csv-bestand

### Indeling

De bezoeker moet via de waarde van Target mboxPC of de waarde mboxThirdPartyId worden geïdentificeerd. De Experience Cloud-id (ECID) wordt niet ondersteund.

### Voorbeelden

U wilt Doel in real time bijwerken wanneer een bezoeker één of andere off-line actie uitvoert, zoals het bereiken van een callcenter, wordt een lening gefinancierd, gebruikend een loyaliteitskaart in opslag, die tot een kiosk toegang hebben, etc.

### Voordelen van methode

Geen limiet voor het aantal profielkenmerken.

Profielkenmerken die via de site worden verzonden, kunnen via de API worden bijgewerkt en andersom.

### Caveats

Limiet van 1.000.000 API-aanroepen (1 miljoen) per periode van 24 uur

Alleen profielen worden bijgewerkt. Kan geen profiel maken voor een mogelijk gebruikersdoel dat nog niet is te zien.

### Codevoorbeelden

GET en POST ondersteund. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

### Koppelingen naar relevante informatie

[Profielen bijwerken](https://developers.adobetarget.com/api/#updating-profiles)

## Customer Attributes {#section_C47FC7980A9A4608BD1A5F0BD900FA70}

Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target.

Doelklanten van Standard kunnen 5 kenmerken gebruiken, doelklanten kunnen 200 kenmerken gebruiken.

### Indeling

Een .csv-bestand met Experience Cloud-id&#39;s (ECID&#39;s) en paren van kenmerknaam/waarde wordt geüpload via FTP of handmatig in de gebruikersinterface van de Experience Cloud.

### Voorbeelden

Uw CRM of ander intern systeem slaat waardevolle informatie op u met Adobe Experience Cloud, met inbegrip van Doel en Analytics wilt delen.

### Voordelen van methode

Als u klantgegevens uploadt, wordt voor die bezoeker in Target een profielvermelding gemaakt, zelfs als Target de bezoeker nog niet heeft kunnen zien.

Dezelfde gegevens zijn automatisch beschikbaar in Doel en Analyse.

FTP kan een eenvoudigere implementatiemethode zijn dan API.

### Caveats

Doelklanten van Standard kunnen 5 kenmerken benutten, doelklanten kunnen 200 kenmerken benutten

Kan waarden alleen bijwerken via Customer Attributes, niet op pagina.

Vereist Experience Cloud ID-implementatie (ECID).

### Codevoorbeelden

De details kunnen in [Create worden gevonden een bron van klantenattributen en het gegevensdossier](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html)uploaden.

### Koppelingen naar relevante informatie

[Maak een bron voor klantkenmerken en upload het gegevensbestand](https://docs.adobe.com/content/help/en/core-services/interface/customer-attributes/t-crs-usecase.html).