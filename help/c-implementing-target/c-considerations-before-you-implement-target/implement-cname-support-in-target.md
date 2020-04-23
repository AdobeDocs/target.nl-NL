---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informatie over het werken met de Zorg van de Cliënt van Adobe om de steun van CNAME (Canonical Name) in het Doel van Adobe uit te voeren.
title: CNAME en Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: 8267de6c27566ec397651d3bfc88aad0818ed8d2

---


# CNAME en Adobe Target {#cname-and-adobe-target}

Instructies voor het werken met de Zorg van de Cliënt van Adobe om de steun van CNAME (Canonical Name) in uit te voeren [!DNL Adobe Target]. Om kwesties, of op ITP betrekking hebbende koekjesbeleid het best te behandelen en te blokkeren, wordt een CNAME gebruikt zo vraag wordt gemaakt aan een domein dat door de klant eerder dan een domein wordt bezeten dat door Adobe wordt bezeten.

## CNAME-ondersteuning aanvragen

Voer de volgende stappen uit om CNAME-ondersteuning aan te vragen in [!DNL Target]:

1. De certificeringsinstantie (DigiCert) van Adobe moet controleren of Adobe gemachtigd is om certificaten te genereren onder uw domein.

   DigiCert roept deze DCV (Process [Domain Control Validation)](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/)aan en Adobe mag geen certificaat onder uw domein genereren totdat dit proces is voltooid voor ten minste een van de onderstaande DCV-methoden:

   * De snelste methode DCV is de __DNS CNAME methode__, waarin u een DNS CNAME- verslag (die een teken bevatten) aan uw domein toevoegt dat aan DCV hostname van DigiCert (dcv.digicert.com) richt. Deze CNAME-record geeft DigiCert aan dat Adobe geautoriseerd is om het certificaat te genereren. De Zorg van de Cliënt van Adobe zal u de instructies met de noodzakelijke DNS verslagen verzenden. Een voorbeeld:

      ```
      3b0332e02daabf31651a5a0d81ba830a.target.example.com.  IN  CNAME  dcv.digicert.com.
      ```

      >[!NOTE]
      >
      >Deze DCV-tokens verlopen na 30 dagen, waarna Adobe Client Care contact met u opneemt met bijgewerkte tokens. Voor de snelste tijd aan resolutie voor uw verzoek van CNAME, gelieve bereid te zijn om deze DNS veranderingen op alle gevraagde domeinen aan te brengen alvorens uw verzoek voor te leggen.

      >[!NOTE]
      >
      >Als uw domein [DNS CAA verslagen](https://en.wikipedia.org/wiki/DNS_Certification_Authority_Authorization)heeft, zult u moeten toevoegen `digicert.com` als het niet reeds is toegevoegd. Dit DNS-record geeft aan welke certificeringsinstanties gemachtigd zijn certificaten voor het domein uit te geven. Het resulterende DNS-record ziet er als volgt uit: `example.com. IN CAA 0 issue "digicert.com"`. U kunt [de Toolbox](https://toolbox.googleapps.com/apps/dig/#CAA) van de Reeks van G gebruiken om te bepalen als uw worteldomein een bestaand verslag van de CAA heeft. U kunt meer lezen over de manier waarop DigiCert CAA-records [hier](https://docs.digicert.com/manage-certificates/dns-caa-resource-record-check)verwerkt.

   * DigiCert zal ook de __e-mailmethode__ proberen, waarin zij e-mails naar adressen verzenden die in de informatie van WHOIS van het domein evenals vooraf bepaalde e-mailadressen (admin, beheerder, webmaster, hostmaster, en postmaster `@[domain_name]`) worden gevonden. Raadpleeg de documentatie bij [de](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) DCV-methoden voor meer informatie.

      DigiCert geeft de volgende aanbeveling om het DCV-e-mailproces te versnellen:

      &quot;Controleer of uw registrar/WHOIS-provider [relevante e-mailadressen]niet heeft gemaskeerd of verwijderd. Als dat het geval is, moet u nagaan of deze een manier bieden (bijvoorbeeld een geanonimiseerd e-mailadres of webformulier) waarmee [certificeringsinstanties] toegang hebben tot de WHOIS-gegevens van uw domein.&quot;

1. Creeer een verslag CNAME op DNS van uw domein richtend aan uw regelmatige hostname `clientcode.tt.omtrdc.net`. Bijvoorbeeld, als uw cliëntcode klant is en uw voorgestelde hostname is `target.example.com`, zou uw DNS CNAME- verslag iets als dit moeten kijken:

   ```
   target.example.com.  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Open een [Adobe Client Care-ticket waarmee CNAME-ondersteuning](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) voor uw [!DNL Target] aanroepen wordt aangevraagd.

   Adobe werkt met DigiCert om uw certificaat aan te schaffen en te implementeren op de productieservers van Adobe. DigiCert start het DCV-proces en Adobe Client Care geeft een melding wanneer de implementatie gereed is.

1. Nadat u de voorgaande taken hebt voltooid en Adobe Client Care u heeft laten weten dat de implementatie gereed is, moet u de toepassing bijwerken naar de nieuwe CNAME in at.js. `serverDomain`

## Veelgestelde vragen

De volgende informatie beantwoordt vaak gestelde vragen over het verzoeken van en het uitvoeren van de steun van CNAME in [!DNL Target]:

### Kan ik mijn eigen certificaat verstrekken (ook bekend als &quot;bring-your-own-certificate&quot;, ook bekend als &quot;BYOC&quot;)? Zo ja, wat is het proces?

Ja, u kunt uw eigen certificaat opgeven, maar __dit wordt niet aanbevolen__. Het beheer van de levenscyclus van het SSL-certificaat is aanzienlijk eenvoudiger voor zowel Adobe als de klant wanneer Adobe het certificaat aanschaft en beheert. SSL-certificaten moeten elk jaar worden vernieuwd. Dit betekent dat Adobe Client Care jaarlijks contact met u moet opnemen om Adobe een nieuw certificaat te kunnen sturen. Sommige klanten kunnen moeite hebben om een vernieuwd certificaat tijdig te produceren elk jaar, wat hun [!DNL Target] implementatie in gevaar brengt omdat browsers verbindingen zullen weigeren wanneer het certificaat verloopt.

>[!NOTE]
>
>Houd er rekening mee dat als u een CNAME-implementatie voor uw eigen certificaat [!DNL Target] aanvraagt, u verantwoordelijk bent voor het jaarlijks verstrekken van vernieuwde certificaten aan de klantenservice van Adobe. Als u toestaat dat uw CNAME-certificaat verloopt voordat Adobe een vernieuwd certificaat kan implementeren, leidt dit tot een storing voor uw specifieke [!DNL Target] implementatie.

1. Sla stap 1 hierboven over, maar voltooi stap 2 en 3. Wanneer u een Adobe Client Care-ticket (stap 3) opent, geeft u aan dat u uw eigen certificaat opgeeft.

   Adobe genereert en stuurt u een CSR-verzoek (Certificate Signing Request).

1. Gebruik de CSR om het certificaat aan te schaffen via de door u gekozen certificeringsinstantie (CA).

1. Verzend het nieuwe openbare certificaat naar Adobe. Adobe-vertegenwoordigers implementeren het openbare certificaat op de productieservers.

1. Voltooi stap 4 nadat Adobe Client Care u heeft laten weten dat de implementatie gereed is.

### Hoe lang tot mijn nieuwe SSL certificaat verloopt?

Certificaten die vóór 1 september 2020 zijn afgegeven, zijn certificaten van twee jaar. Certificaten die zijn uitgegeven op 1 september 2020 en daarna zijn certificaten van één jaar. U kunt [hier](https://www.digicert.com/position-on-1-year-certificates)meer lezen over de overgang naar een jaarcertificaat.

### Welke hostnames moet ik kiezen? Hoeveel hostnames per domein zou ik moeten kiezen?

[!DNL Target] De implementaties van CNAME vereisen slechts één hostname per domein op het SSL certificaat en in DNS van de klant, zodat is wat wij adviseren. Sommige klanten kunnen extra hostnames per domein voor hun eigen doeleinden (het testen in het opvoeren, bijvoorbeeld) vereisen, wat gesteund wordt.

De meeste klanten kiezen hostname als `target.example.com`, zodat is wat wij adviseren, maar de keus is uiteindelijk van u. Gelieve te zijn zeker om geen hostname van een bestaand DNS verslag aan te vragen aangezien dat een conflict en vertragingstijd aan resolutie van uw verzoek [!DNL Target] CNAME zou veroorzaken.

### Ik heb reeds een implementatie CNAME voor, [!DNL Adobe Analytics]kunnen wij het zelfde certificaat of hostname gebruiken?

Nee, [!DNL Target] vereist een aparte hostnaam en certificaat.

### Heeft mijn huidige implementatie van Target gevolgen voor ITP 2.1 of 2.2?

Navigeer in een Safari-browser naar uw website waarop u een Target JavaScript-bibliotheek hebt. Als u een koekje ziet van het Doel in de context van een CNAME, zoals `analytics.company.com`, dan wordt u niet beïnvloed door ITP 2.1 of 2.2.

ITP problemen kunnen voor Doel met enkel een Analytics CNAME worden opgelost. U zult een afzonderlijke NAAM van het Doel slechts in het geval van ad-blokkerende scenario&#39;s nodig hebben waar het Doel wordt geblokkeerd.

Zie [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)voor meer informatie over ITP.

### Kan Adobe/DigiCert de DCV-e-mails naar een ander e-mailadres verzenden `<someone>@example.com`?

Nr, zal DigiCert (of om het even welke certificaatautoriteit) slechts iedereen met een e-mailadres onder een domein toestaan om een SSL certificaat onder dat zelfde domein toe te laten tenzij dat e-mailadres ook in de informatie van WHOIS van het domein of de vooraf bepaalde lijst van adressen (zie hierboven) wordt omvat. Hierdoor kunnen alleen geautoriseerde personen DCV voor een bepaald domein goedkeuren. Als dit niet uitvoerbaar voor u is, adviseren wij het gebruiken van de DNS methode CNAME DCV (zie hierboven).

### Hoe kan ik mijn implementatie CNAME klaar voor verkeer bevestigen?

Gebruik de volgende set opdrachten (in de opdrachtregelterminal van MacOS of Linux, met bash en curl 7.49+):

1. Plak deze basisfunctie eerst in de terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..32},34,35,37,38}.tt.omtrdc.net; do
           echo "$edge: $(curl -sSv --connect-to $domain:443:$edge:443 https://$domain 2>&1 | grep subject:)"
       done
   }
   ```

1. Vervolgens plakt u deze opdracht (door `target.example.com` uw hostnaam te vervangen):

   ```
   validateEdgeFpsslSni target.example.com
   ```

   Als de implementatie gereed is, ziet u de uitvoer hieronder. Het belangrijkste onderdeel is dat alle regels worden weergegeven `CN=target.example.com`, wat overeenkomt met onze gewenste hostnaam. Als een van deze programma&#39;s `CN=*.tt.omtrdc.net`zichtbaar is, is de implementatie **niet** gereed.

   ```
   $ validateEdgeFpsslSni target.example.com
   mboxedge17.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge21.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge22.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge26.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge28.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge29.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge30.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge31.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge32.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge34.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge35.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge37.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   mboxedge38.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Valideer uw nieuwe DNS NAAM met een ander curl verzoek, dat ook zou moeten tonen `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Als dit bevel ontbreekt maar het bovenstaande `validateEdgeFpsslSni` bevel slaagt, zou u op uw DNS updates kunnen moeten wachten om volledig te verspreiden. DNS verslagen hebben bijbehorende [TTL (tijd-aan-levende)](https://en.wikipedia.org/wiki/Time_to_live#DNS_records) die geheim voorgeheugenvervaltijd voor DNS antwoorden van die verslagen dicteert, zodat kunt u minstens moeten wachten zolang uw TTLs. U kunt het `dig target.example.com` bevel of Toolbox [van](https://toolbox.googleapps.com/apps/dig/#CNAME) de Reeks van G gebruiken om uw specifieke TTLs te zoeken.
