---
keywords: clientzorg;naam;certificaatprogramma;canonieke naam;cookies;certificaat;amc;adobe managed certificaat;digicert;domeincontroledetectie;dcv
description: Werk met de Zorg van de Cliënt van Adobe om de steun van CNAME (Canonical Name) in Adobe Target uit te voeren om ad-blokkerende kwesties of ITP-verwante koekjesbeleid te behandelen.
title: Hoe gebruik ik CNAME als doel?
feature: Privacy en beveiliging
role: Ontwikkelaar
translation-type: tm+mt
source-git-commit: 69677b9d384d9817a39386fc1388a4aa42121713
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---


# CNAME en Adobe Target

Instructies voor het werken met de Zorg van de Cliënt [!DNL Adobe] om steun CNAME (Canonical Name) in &lt;a1 uit te voeren/>. [!DNL Adobe Target] Gebruik CNAME om problemen met of beleid voor ITP-cookies (Intelligent Tracking Prevention) te verwerken en te blokkeren. Met CNAME, worden de vraag gemaakt aan een domein dat door de klant eerder dan een domein wordt bezeten van [!DNL Adobe].

## Ondersteuning voor CNAME aanvragen in Doel

1. Bepaal de lijst met hostnamen die u nodig hebt voor uw SSL-certificaat (zie de Veelgestelde vragen hieronder).

1. Voor elke hostname, creeer een verslag CNAME in uw DNS richtend aan uw regelmatige [!DNL Target] hostname `clientcode.tt.omtrdc.net`.

   Bijvoorbeeld, als uw cliëntcode &quot;klant&quot;is en uw voorgestelde hostname `target.example.com` is, ziet uw DNS CNAME- verslag gelijkaardig aan:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!IMPORTANT]
   >
   >Adobe, DigiCert, kan pas een certificaat uitgeven als deze stap is voltooid. Daarom [!DNL Adobe] kan uw verzoek om een implementatie CNAME niet vervullen tot deze stap volledig is.

1. [Vul dit ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) formulier in en neem het op wanneer u een Adobe Client Care-ticket  [opent dat CNAME-ondersteuning](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) aanvraagt:

   * Adobe [!DNL Target] clientcode:
   * SSL-certificaathostnamen (voorbeeld: `target.example.com target.example.org`):
   * Aankoper van SSL-certificaat (Adobe wordt ten zeerste aanbevolen, zie Veelgestelde vragen): Adobe/klant
   * Als de klant het certificaat aanschaft, ook wel &#39;Create Your Own Certificate&#39; (BYOC) genoemd, voert u de volgende aanvullende gegevens in:
      * Certificaatorganisatie (voorbeeld: Voorbeeld van Company Inc):
      * Organisatorische eenheid van het certificaat (facultatief, voorbeeld: Marketing):
      * Certificaatland (voorbeeld: VS):
      * Certificaatstatus/gebied (voorbeeld: Californië):
      * Plaats certificaat (voorbeeld: San Jose):

1. Als [!DNL Adobe] het certificaat aanschaft, werkt [!DNL Adobe] samen met DigiCert om uw certificaat aan te schaffen en te implementeren op Adobe-/productieservers.

   Als de klant het certificaat (BYOC) aanschaft, verzendt [!DNL Adobe] de Zorg van de Cliënt u het certificaat ondertekenend verzoek (CSR). Gebruik de CSR wanneer u het certificaat aanschaft via de gekozen certificeringsinstantie. Nadat het certificaat is uitgegeven, verzendt u een kopie van het certificaat en eventuele tussenliggende certificaten naar [!DNL Adobe] Client Care voor implementatie.

   [!DNL Adobe] De Zorg van de cliënt brengt u op de hoogte wanneer uw implementatie klaar is.

1. Werk `serverDomain` aan nieuwe CNAME in at.js bij.

## Veelgestelde vragen

De volgende informatie beantwoordt vaak gestelde vragen over het verzoeken van en het uitvoeren van steun CNAME in [!DNL Target]:

### Kan ik mijn eigen certificaat opgeven (breng uw eigen certificaat of BYOC)?

U kunt uw eigen certificaat opgeven. [!DNL Adobe] adviseert deze praktijk echter niet. Het beheer van de levenscyclus van het SSL-certificaat is zowel voor [!DNL Adobe] als voor u eenvoudiger als [!DNL Adobe] het certificaat aanschaft en beheert. SSL-certificaten moeten elk jaar worden vernieuwd. Daarom moet [!DNL Adobe] de Zorg van de Cliënt u elk jaar contacteren om een nieuw certificaat op een geschikte manier te verkrijgen. Sommige klanten kunnen moeite hebben om een vernieuwd certificaat tijdig te produceren. Uw [!DNL Target]-implementatie wordt in gevaar gebracht wanneer het certificaat verloopt omdat browsers geen verbindingen toestaan.

>[!IMPORTANT]
>
>Als u een [!DNL Target] de implementatie-uw-eigen-certificaat van CNAME verzoekt, bent u verantwoordelijk voor het verstrekken van vernieuwde certificaten aan [!DNL Adobe] de Zorg van de Cliënt elk jaar. Als u toestaat dat uw CNAME-certificaat verloopt voordat [!DNL Adobe] een vernieuwd certificaat kan implementeren, resulteert dit in een stroomstoring voor uw specifieke [!DNL Target]-implementatie.

### Hoe lang tot mijn nieuwe SSL certificaat verloopt?

Certificaten die vóór 1 september 2020 zijn afgegeven, zijn certificaten van twee jaar. Certificaten die op of na 1 september 2020 zijn afgegeven, zijn certificaten van één jaar. U kunt meer over de beweging aan één jaar certificaten [hier ](https://www.digicert.com/position-on-1-year-certificates) lezen.

### Welke hostnames moet ik kiezen? Hoeveel hostnames per domein zou ik moeten kiezen?

[!DNL Target] De implementaties van CNAME vereisen slechts één hostname per domein op het SSL certificaat en in DNS van de klant. Adobe raadt één hostnaam aan. Sommige klanten vereisen meer hostnames per domein voor hun eigen doeleinden (bijvoorbeeld het testen in het opvoeren), wat wordt ondersteund.

De meeste klanten kiezen een hostnaam zoals `target.example.com`. Adobe beveelt aan deze praktijk te volgen, maar uiteindelijk is de keuze aan u. Vraag geen hostname van een bestaand DNS verslag aan. Dit veroorzaakt een conflict en vertraagt tijd aan resolutie van uw [!DNL Target] verzoek CNAME.

### Ik heb reeds een implementatie CNAME voor [!DNL Adobe Analytics], kunnen wij het zelfde certificaat of hostname gebruiken?

Nee, [!DNL Target] vereist een aparte hostnaam en certificaat.

### Is mijn huidige implementatie van Doel beïnvloed door ITP 2.x?

Navigeer in een Safari-browser naar uw website waarop u een JavaScript-bibliotheek [!DNL Target] hebt. Als u een [!DNL Target] koekje ziet dat in de context van een CNAME, zoals `analytics.company.com` wordt geplaatst, dan wordt u niet beïnvloed door ITP 2.x.

ITP problemen kunnen voor [!DNL Target] met enkel een [!DNL Analytics] CNAME worden opgelost. U hebt een afzonderlijke [!DNL Target] CNAME slechts in ad-blokkerende scenario&#39;s nodig waar [!DNL Target] wordt geblokkeerd.

Voor meer informatie over ITP, zie [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welk soort de dienstverstoringen kan ik verwachten wanneer mijn implementatie CNAME wordt opgesteld?

Er is geen de dienstverstoring wanneer het certificaat wordt opgesteld (met inbegrip van certificaatvernieuwingen).

Nadat u echter de hostnaam in uw [!DNL Target]-implementatiecode (`serverDomain` in at.js) hebt gewijzigd in de nieuwe CNAME-hostnaam (`target.example.com`), behandelen webbrowsers het retourneren van bezoekers als nieuwe bezoekers. Het retourneren van bezoekersprofielgegevens gaat verloren omdat het vorige cookie niet toegankelijk is onder de oude hostnaam (`clientcode.tt.omtrdc.net`). De vorige cookie is niet toegankelijk vanwege beveiligingsmodellen van de browser. Deze verstoring komt slechts op de aanvankelijke besnoeiing-over aan nieuwe CNAME voor. Certificaatverlengingen hebben niet hetzelfde effect omdat de hostnaam niet verandert.

### Welk zeer belangrijk type en algoritme van de certificaathandtekening voor mijn implementatie CNAME wordt gebruikt?

Alle certificaten zijn RSA SHA-256 en de sleutels zijn RSA 2048 beetje, door gebrek. Toetsgrootten die groter zijn dan 2048 bits, worden momenteel niet ondersteund.

### Hoe kan ik bevestigen dat mijn implementatie CNAME klaar voor verkeer is?

Gebruik de volgende set opdrachten (in de opdrachtregelterminal van MacOS of Linux, met bash en curl 7.49+):

1. Plak deze basfunctie in de terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Plak deze opdracht (waarbij `target.example.com` wordt vervangen door uw hostnaam):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Als de implementatie gereed is, ziet u de uitvoer hieronder. Het belangrijkste onderdeel is dat alle regels `CN=target.example.com` bevatten, wat overeenkomt met de gewenste hostnaam. Als een regel `CN=*.tt.omtrdc.net` bevat, is de implementatie **niet** gereed.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge36.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Valideer uw nieuwe DNS NAAM met een ander curl verzoek, dat `CN=target.example.com` ook zou moeten tonen:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Als dit bevel ontbreekt maar het `validateEdgeFpsslSni` bevel hierboven slaagt, wacht op uw DNS updates om volledig te verspreiden. DNS-records hebben een gekoppelde [TTL (time-to-live)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) die de verlooptijd van de cache voor DNS-antwoorden van die records dicteert. Dientengevolge, zou u minstens zolang uw TTLs kunnen moeten wachten. U kunt `dig target.example.com` bevel of [Toolbox van de Reeks van G gebruiken ](https://toolbox.googleapps.com/apps/dig/#CNAME) om uw specifieke TTLs omhoog te zoeken.

## Bekende beperkingen

* De modus QA blijft niet behouden wanneer u CNAME en at.js 1.x hebt omdat deze is gebaseerd op een cookie van een andere fabrikant. Als tussenoplossing kunt u de voorvertoningsparameters toevoegen aan elke URL waarnaar u navigeert. De modus QA blijft behouden wanneer u CNAME en at.js 2.x hebt.
* De instelling `overrideMboxEdgeServer` werkt momenteel niet correct met CNAME wanneer versies at.js voor at.js 1.8.2 en at.js 2.3.1 worden gebruikt. Als u een oudere versie van at.js gebruikt, zou dit plaatsen als `false` moeten worden geplaatst om het ontbreken verzoeken te vermijden. U kunt ook [het bijwerken van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) naar een nieuwere, ondersteunde versie overwegen.
* Wanneer het gebruiken van CNAME, wordt het waarschijnlijker dat de grootte van de koekjeskopbal voor [!DNL Target] vraag stijgt. [!DNL Adobe] raadt u aan de grootte van de cookie onder 8 kB te houden.
