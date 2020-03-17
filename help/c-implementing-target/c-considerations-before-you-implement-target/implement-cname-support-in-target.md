---
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate;digicert;domain control validation;dcv
description: Informatie over het werken met de Zorg van de Cliënt van Adobe om de steun van CNAME (Canonical Name) in het Doel van Adobe uit te voeren.
title: CNAME en Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
translation-type: tm+mt
source-git-commit: a2e4a4d1036d2c56d752d808054f6f4b4ab1d411

---


# CNAME en Adobe Target {#cname-and-adobe-target}

Instructies over het werken met de Zorg van de Cliënt van Adobe om de steun van CNAME (Canonical Name) in uit te voeren [!DNL Adobe Target]. Om kwesties, of op ITP betrekking hebbende koekjesbeleid het best te behandelen en te blokkeren, wordt een CNAME gebruikt zo vraag wordt gemaakt aan een domein dat door de klant eerder dan een domein wordt bezeten dat door Adobe wordt bezeten.

## CNAME-ondersteuning aanvragen

Voer de volgende stappen uit om CNAME-ondersteuning aan te vragen in [!DNL Target]:

1. De certificeringsinstantie (DigiCert) van Adobe moet controleren of Adobe gemachtigd is om certificaten te genereren onder uw domein.

   DigiCert roept deze DCV (Process [Domain Control Validation](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) ) aan en Adobe mag pas een certificaat onder uw domein genereren als dit proces is voltooid.

   DCV gebruikt een aantal methoden en er zijn een paar dingen die u kunt doen voordat u een Adobe Client Care-ticket (stap 3) opent om het DCV-proces te versnellen:

   * DigiCert zal eerst de e-mailmethode proberen, waarin zij e-mails naar adressen verzenden die in de informatie van WHOIS van het domein evenals vooraf bepaalde e-mailadressen (admin, beheerder, webmaster, hostmaster, en postmaster `@[domain_name]`) worden gevonden. Raadpleeg de documentatie bij [de](https://docs.digicert.com/manage-certificates/dv-certificate-enrollment/domain-control-validation-dcv-methods/) DCV-methoden voor meer informatie.

      DigiCert geeft de volgende aanbeveling om het DCV-e-mailproces te versnellen:

      &quot;Controleer of uw registrar/WHOIS-provider [relevante e-mailadressen]niet heeft gemaskeerd of verwijderd. Als dat het geval is, moet u nagaan of deze een manier bieden (bijvoorbeeld een geanonimiseerd e-mailadres of webformulier) waarmee [certificeringsinstanties] toegang hebben tot de WHOIS-gegevens van uw domein.&quot;

   * Als de DCV e-mailmethode geen optie voor u is, is de volgende methode de DNS TXT methode, waarin u een DNS TXT- verslag aan uw domein met een knoeiboelwaarde toevoegt. Deze TXT-record geeft DigiCert aan dat Adobe geautoriseerd is om het certificaat te genereren. Als u deze methode moet gebruiken, laat u de Zorg van de Cliënt van Adobe weten wanneer u een kaartje opent (stap 3). Dit zal helpen het DCV proces versnellen.

1. Creeer een verslag CNAME op DNS van uw domein richtend aan uw regelmatige hostname `clientcode.tt.omtrdc.net`. Bijvoorbeeld, als uw cliëntcode klant is en uw voorgestelde hostname is `target.example.com`, zou uw DNS CNAME- verslag iets als dit moeten kijken:

   ```
   target.example.com  IN  CNAME  cnamecustomer.tt.omtrdc.net.
   ```

1. Open een [Adobe Client Care-ticket waarmee CNAME-ondersteuning](https://docs.adobe.com/content/help/en/target/using/cmp-resources-and-contact-information.html#reference_ACA3391A00EF467B87930A450050077C) voor uw [!DNL Target] aanroepen wordt aangevraagd.

   Adobe werkt met DigiCert om uw certificaat aan te schaffen en te implementeren op de productieservers van Adobe. DigiCert start het DCV-proces en Adobe Client Care geeft een melding wanneer de implementatie gereed is.

1. Nadat u de voorgaande taken hebt voltooid en Adobe Client Care u heeft laten weten dat de implementatie gereed is, moet u de toepassing bijwerken naar de nieuwe CNAME in at.js. `serverDomain`

## Veelgestelde vragen

De volgende informatie beantwoordt vaak gestelde vragen over het verzoeken van en het uitvoeren van steun CNAM in [!DNL Target]:

### Kan ik mijn eigen certificaat verstrekken? Zo ja, wat is het proces?

Ja, u kunt hiervoor uw eigen certificaat opgeven:

1. Sla stap 1 hierboven over, maar voltooi stap 2 en 3. Wanneer u een Adobe Client Care-ticket (stap 3) opent, geeft u aan dat u uw eigen certificaat opgeeft.

   Adobe genereert en stuurt u een CSR-verzoek (Certificate Signing Request).

1. Gebruik de CSR om het certificaat aan te schaffen via de door u gekozen certificeringsinstantie (CA).

1. Verzend het nieuwe openbare certificaat naar Adobe. Adobe-vertegenwoordigers implementeren het openbare certificaat op de productieservers.

1. Voltooi stap 4 nadat Adobe Client Care u heeft laten weten dat de implementatie gereed is.

### Ik heb reeds een implementatie CNAME voor, [!DNL Adobe Analytics]kunnen wij het zelfde certificaat of hostname gebruiken?

Nee, [!DNL Target] vereist een aparte hostnaam en certificaat.

### Heeft mijn huidige implementatie van Target gevolgen voor ITP 2.1 of 2.2?

Navigeer in een Safari-browser naar uw website waarop u een Target JavaScript-bibliotheek hebt. Als u een koekje ziet van het Doel in de context van een CNAME, zoals `analytics.company.com`, dan wordt u niet beïnvloed door ITP 2.1 of 2.2.

ITP problemen kunnen voor Doel met enkel een Analytics CNAME worden opgelost. U zult een afzonderlijke NAAM van het Doel slechts in het geval van ad-blokkerende scenario&#39;s nodig hebben waar het Doel wordt geblokkeerd.

Zie [Apple Intelligent Tracking Prevention (ITP) 2.x](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/apple-itp-2x.md)voor meer informatie over ITP.

### Hoe kan ik mijn implementatie CNAME klaar voor verkeer bevestigen?

Gebruik de volgende set opdrachten (in de opdrachtregelterminal van MacOS of Linux, met bash en curl 7.49+):

1. Plak deze basisfunctie eerst in de terminal:

   ```
   function validateEdgeFpsslSni {
       domain=$1
       for edge in mboxedge{17,21,22,26,{28..33}}.tt.omtrdc.net; do
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
   mboxedge33.tt.omtrdc.net: *  subject: C=US; ST=California; L=San Jose; O=Adobe Systems Incorporated; CN=target.example.com
   ```

1. Valideer uw nieuwe DNS NAAM met een ander curl verzoek, dat ook zou moeten tonen `CN=target.example.com`:

   ```
   curl -sSv https://target.example.com 2>&1 | grep subject:
   ```

   >[!NOTE]
   >
   >Als dit bevel ontbreekt maar het bovenstaande `validateEdgeFpsslSni` bevel slaagt, zou u op uw DNS updates kunnen moeten wachten om volledig te verspreiden.
