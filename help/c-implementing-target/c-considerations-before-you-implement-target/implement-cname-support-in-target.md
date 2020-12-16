---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informatie over het werken met de Zorg van de Cliënt van Adobe om steun CNAME (Canonical Name) in Adobe Target uit te voeren.
title: CNAME en Adobe Target
feature: privacy and security
translation-type: tm+mt
source-git-commit: 677d5ed16377fc32b4506ca736084319e5643e67
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---


# CNAME en Adobe Target {#cname-and-adobe-target}

Instructies voor het werken met de Zorg van de Cliënt van Adobe om steun CNAME (Canonical Name) in [!DNL Adobe Target] uit te voeren. Om kwesties, of op ITP betrekking hebbende koekjesbeleid het best te behandelen en te blokkeren, wordt een CNAME gebruikt zodat wordt de vraag gemaakt aan een domein dat door de klant eerder dan een domein wordt bezeten dat door Adobe wordt bezeten.

## CNAME-ondersteuning aanvragen

Voer de volgende stappen uit om CNAME-ondersteuning aan te vragen in [!DNL Target]:

1. Bepaal de lijst met hostnamen die u nodig hebt voor uw SSL-certificaat (zie Veelgestelde vragen).

1. Voor elke hostname, creeer een verslag CNAME in uw DNS richtend aan uw regelmatige [!DNL Target] hostname `clientcode.tt.omtrdc.net`.

   Bijvoorbeeld, als uw cliëntcode &quot;klant&quot;is en uw voorgestelde hostname `target.example.com` is, zou uw DNS CNAME- verslag iets als dit moeten kijken:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

   >[!NOTE]
   >
   >Adobe, DigiCert, kan pas een certificaat uitgeven als deze stap is voltooid. Daarom kan Adobe uw verzoek om een implementatie CNAME niet vervullen tot deze stap volledig is.

1. [Vul dit ](https://experienceleague.adobe.com/docs/core-services/assets/FPC_Request_Form.xlsx?lang=en) formulier in en neem het op wanneer u een Adobe Client Care-ticket  [opent dat CNAME-ondersteuning](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) aanvraagt:

   * Adobe [!DNL Target] clientcode:
   * SSL-certificaathostnamen (voorbeeld: `target.example.com target.example.org`):
   * Aankoper van SSL-certificaat (Adobe wordt ten zeerste aanbevolen, zie Veelgestelde vragen): Adobe/klant
   * Als de klant het certificaat aanschaft (ook bekend als BYOC), vult u de volgende aanvullende gegevens in:
      * Certificaatorganisatie (voorbeeld: Voorbeeld van Company Inc):
      * Organisatorische eenheid van het certificaat (facultatief, voorbeeld: Marketing):
      * Certificaatland (voorbeeld: VS):
      * Certificaatstatus/gebied (voorbeeld: Californië):
      * Plaats certificaat (voorbeeld: San Jose):

1. Als Adobe het certificaat aanschaft, werkt Adobe samen met DigiCert aan de aanschaf en implementatie van het certificaat op Adobe productieservers.

   Als de klant het certificaat (BYOC) koopt, zal de Zorg van de Adobe Cliënt u het certificaat verzenden ondertekenend verzoek (CSR), dat u zult moeten gebruiken wanneer het kopen van het certificaat door uw certificaatgezag van keus. Nadat het certificaat wordt uitgegeven, moet u een exemplaar van het certificaat en om het even welke tussencertificaten terug naar de Zorg van de Cliënt van Adobe voor plaatsing verzenden.

   De Zorg van de Cliënt van Adobe zal u op de hoogte brengen wanneer uw implementatie klaar is.

1. Na de voltooiing van de voorafgaande taken en de Zorg van de Cliënt van Adobe heeft u meegedeeld dat de implementatie klaar is, moet u `serverDomain` aan nieuwe CNAME in at.js bijwerken.

## Veelgestelde vragen

De volgende informatie beantwoordt vaak gestelde vragen over het verzoeken van en het uitvoeren van steun CNAME in [!DNL Target]:

### Kan ik mijn eigen certificaat verstrekken (ook bekend als &#39;bring-your-own-certificate&#39; of &#39;BYOC&#39;)?

Ja, u kunt uw eigen certificaat opgeven. dit wordt echter niet aanbevolen . Het beheer van de SSL-certificaatlevenscyclus is aanzienlijk eenvoudiger voor zowel Adobe als u wanneer Adobe het certificaat aanschaft en beheert. SSL-certificaten moeten elk jaar worden vernieuwd. Dit betekent dat de Adobe Client Care jaarlijks contact met u moet opnemen om Adobe een nieuw certificaat tijdig te kunnen verzenden. Sommige klanten kunnen problemen hebben om een vernieuwd certificaat tijdig te produceren elk jaar, wat hun [!DNL Target] implementatie in gevaar brengt omdat browsers verbindingen zullen weigeren wanneer het certificaat verloopt.

>[!IMPORTANT]
>
>Houd er rekening mee dat als u een [!DNL Target]-implementatie van CNAME-certificaat aanvraagt, u verantwoordelijk bent voor het jaarlijks verstrekken van vernieuwde certificaten aan de Zorg van de Adobe-client. Als u toestaat dat uw CNAME-certificaat verloopt voordat Adobe een vernieuwd certificaat kan implementeren, resulteert dit in een stroomstoring voor uw specifieke [!DNL Target]-implementatie.

### Hoe lang tot mijn nieuwe SSL certificaat verloopt?

Certificaten die vóór 1 september 2020 zijn afgegeven, zijn certificaten van twee jaar. Certificaten die op of na 1 september 2020 worden afgegeven, zijn certificaten van één jaar. U kunt meer over de beweging aan één jaar certificaten [hier ](https://www.digicert.com/position-on-1-year-certificates) lezen.

### Welke hostnames moet ik kiezen? Hoeveel hostnames per domein zou ik moeten kiezen?

[!DNL Target] De implementaties van CNAME vereisen slechts één hostname per domein op het SSL certificaat en in DNS van de klant, zodat is wat wij adviseren. Sommige klanten vereisen mogelijk extra hostnames per domein voor hun eigen doeleinden (bijvoorbeeld testen in opvoeren), wat wordt ondersteund.

De meeste klanten kiezen een hostnaam zoals `target.example.com`, zodat is wat wij adviseren, maar de keus is uiteindelijk van u. Ben zeker om geen hostname van een bestaand DNS verslag aan te vragen aangezien dat een conflict en vertragingstijd aan resolutie van uw [!DNL Target] verzoek CNAME zou veroorzaken.

### Ik heb reeds een implementatie CNAME voor [!DNL Adobe Analytics], kunnen wij het zelfde certificaat of hostname gebruiken?

Nee, [!DNL Target] vereist een aparte hostnaam en certificaat.

### Is mijn huidige implementatie van Doel beïnvloed door ITP 2.x?

Navigeer in een Safari-browser naar uw website waarop u een Target JavaScript-bibliotheek hebt. Als u een koekje ziet van het Doel in de context van een CNAME, zoals `analytics.company.com` wordt geplaatst, dan wordt u niet beïnvloed door ITP 2.x.

ITP problemen kunnen voor Doel met enkel een Analytics CNAME worden opgelost. U zult een afzonderlijke NAAM van het Doel slechts in het geval van ad-blokkerende scenario&#39;s nodig hebben waar het Doel wordt geblokkeerd.

Voor meer informatie over ITP, zie [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md).

### Welk soort de dienstverstoringen kan ik verwachten wanneer mijn implementatie CNAME wordt opgesteld?

Er is geen de dienstverstoring wanneer het certificaat wordt opgesteld (met inbegrip van certificaatvernieuwingen). Wanneer u echter de hostnaam in de [!DNL Target]-implementatiecode (`serverDomain` in at.js) wijzigt in de nieuwe CNAME-hostnaam (`target.example.com`), behandelen webbrowsers terugkerende bezoekers als nieuwe bezoekers en gaan hun profielgegevens verloren omdat het vorige cookie niet toegankelijk is onder de oude hostnaam (`clientcode.tt.omtrdc.net`) vanwege beveiligingsmodellen van de browser. Dit is een eenmalig onderbreking slechts op de aanvankelijke besnoeiing-over aan nieuwe CNAME. De vernieuwingen van certificaten hebben niet hetzelfde effect omdat de hostnaam niet verandert.

### Welk zeer belangrijk type en algoritme van de certificaathandtekening voor mijn implementatie CNAME zal worden gebruikt?

Alle certificaten zijn RSA SHA-256 en de sleutels zijn RSA 2048 beetje, door gebrek. Toetsgrootten die groter zijn dan 2048 bits, worden momenteel niet ondersteund.

### Hoe kan ik mijn implementatie CNAME klaar voor verkeer bevestigen?

Gebruik de volgende set opdrachten (in de opdrachtregelterminal van MacOS of Linux, met bash en curl 7.49+):

1. Plak deze basisfunctie eerst in de terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{31,32,{34..38}}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Vervolgens plakt u deze opdracht (waarbij `target.example.com` wordt vervangen door uw hostnaam):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Als de implementatie gereed is, ziet u de uitvoer hieronder. Het belangrijkste onderdeel is dat alle regels `CN=target.example.com` tonen, wat overeenkomt met onze gewenste hostnaam. Als een van deze `CN=*.tt.omtrdc.net` zichtbaar is, is de implementatie **niet** gereed.

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
   >Als dit bevel ontbreekt maar het `validateEdgeFpsslSni` bevel hierboven slaagt, zou u op uw DNS updates kunnen moeten wachten om volledig te verspreiden. DNS verslagen hebben een bijbehorende [TTL (tijd-aan-levend)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) die geheim voorgeheugenvervaltijd voor DNS antwoorden van die verslagen dicteert, zodat kunt u minstens zolang moeten wachten aangezien uw TTLs. U kunt `dig target.example.com` bevel of [Toolbox van de Reeks van G gebruiken ](https://toolbox.googleapps.com/apps/dig/#CNAME) om uw specifieke TTLs omhoog te zoeken.

## Bekende beperkingen

* De wijze QA zal niet kleverig zijn wanneer u CNAME en at.js 1.x hebt omdat het op een derdekoekje gebaseerd is. Als tussenoplossing kunt u de voorvertoningsparameters toevoegen aan elke URL waarnaar u navigeert. De modus QA blijft behouden wanneer u CNAME en at.js 2.x hebt.
* De instelling `overrideMboxEdgeServer` werkt momenteel niet correct met CNAME wanneer versies at.js vóór at.js 1.8.2 en at.js 2.3.1 worden gebruikt. Als u een oudere versie van at.js gebruikt, zou dit als `false` moeten worden geplaatst om het ontbreken verzoeken te vermijden. U kunt ook [het bijwerken van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) naar een nieuwere, ondersteunde versie overwegen.
* Wanneer het gebruiken van CNAME het waarschijnlijker wordt dat de grootte van de koekjeskopbal voor de vraag van het Doel zal stijgen. We raden u aan de grootte van de cookie onder 8 kB te houden.
