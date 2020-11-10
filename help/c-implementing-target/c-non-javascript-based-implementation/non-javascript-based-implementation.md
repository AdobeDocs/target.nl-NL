---
keywords: Implementation;mbox.js non javascript;adbox;redirector;mbox
description: Informatie over het implementeren van Doel in niet-JavaScript-scenario's, zoals het gebruik van een AdBox of Redirector.
title: Doel e-mailimplementatie
feature: email implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---


# E-mail: Doel implementeren{#email-implement-target}

Informatie over het implementeren van Doel in niet-JavaScript-scenario&#39;s, zoals het gebruik van een AdBox of Redirector.

U kunt bezoeken aan advertenties en andere content buiten de site volgen. U kunt dezelfde gebruiker ook op en buiten uw site identificeren en een consistente ervaring bieden tijdens de hele webervaring. Met behulp van één URL staat AdBox tests toe zonder JavaScript of [!DNL at.js] of [!DNL mbox.js].

Een AdBox is handig voor sites die geen [!DNL at.js] of [!DNL mbox.js]filialen hebben. Als uw activiteit dynamisch creatief (bijvoorbeeld, moet u een product in de advertentie tonen die in het karretje werd verlaten) vereist, kunt u geen AdBox gebruiken.

Advertentievakken en Redirector kunnen met om het even welke soort activiteit worden gebruikt. In de volgende tabel worden ADBox en Redirector vergeleken en wanneer beide worden gebruikt:

|  | Doel | Wanneer gebruiken | URL-structuur | Type voorstel | Inhoud voorstellen |
|--- |--- |--- |--- |--- |--- |
| AdBox | Hiermee worden verschillende afbeeldingen naar de advertentie geretourneerd | De inhoud van een advertentie wijzigen | `clientcode&#x200B;.tt.&#x200B;omtrdc&#x200B;.net/&#x200B;m2&#x200B;/&#x200B;clientcode/ubox/&#x200B;image?` | omleiding | URL voor een afbeelding |
| Redirector | Hiermee wordt een bezoeker omgeleid naar een andere webpagina | De landingspagina van een advertentie wijzigen | `clientcode&#x200B;.tt.omtrdc.net/&#x200B;m2/clientcode&#x200B;/ubox/page?` | omleiding | URL voor een pagina |

## Aanbevolen werkwijzen voor beveiliging {#security}

Merk op dat met Redirector, u aan een risico van Open Redirect Kwetsbaarheid kunt worden blootgesteld. Om het ongeoorloofde gebruik van verbindingen van Redirector door derden te vermijden, adviseren wij u &quot;erkende gastheren&quot;gebruiken om de standaard omleiding URL domeinen te lijsten van gewenste personen. Het gebruik van het doel gastheren aan lijst van gewenste personen domeinen waaraan u redirects wilt toestaan. Voor meer informatie, zie [Create Lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel](/help/administrating-target/hosts.md#allowlist) in *Gastheren* te verzenden.

## Restricties {#section_38F559DCF1324271926608BCD4AB1227}

* Er is geen time-out aan de clientzijde, zoals bij standaardvakken. Als Doel volledig omlaag is, zien bezoekers van de advertentie de inhoud niet, zelfs niet standaard.
* Cookies van derden worden gebruikt om de bezoeken bij te houden. Als de PCIds verschillend zijn, door gebrek wordt de derde partij van de bezoeker samengevoegd met om het even welke bestaande 1st-partijprofielen.
* Als u cookies van één partij wilt gebruiken in de AdBox zelf, moet u de mBox-sessie doorgeven in de URL. Bespreek dit met uw accountvertegenwoordiger.
* Als u cookies van de eerste partij wilt gebruiken om cookies bij te houden en te klikken, geeft u de box-sessie door in de URL. Bespreek dit met uw accountvertegenwoordiger.
* Als u meerdere AdBox op dezelfde pagina wilt gebruiken, moet u de Mbox-sessie doorgeven in de URL. Bespreek dit met uw accountvertegenwoordiger. U hebt mogelijk één AdBox en één Redirector-koppeling op dezelfde pagina (omdat Redirector zich op een tweede pagina bevindt).