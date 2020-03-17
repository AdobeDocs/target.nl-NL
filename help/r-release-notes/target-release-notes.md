---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-versies.
title: Opmerkingen bij de prerelease van Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 7e94e3f9aae0f710e1dff72c82c1c132bd4239b5

---


# Opmerkingen bij de release Doel (preRelease){#target-release-notes-prerelease}

Deze versienota&#39;s verstrekken informatie over eigenschappen, verhogingen, en moeilijke situaties voor de recentste of aanstaande [!DNL Adobe Target] versies.

**Laatst bijgewerkt: 9 maart 2020**

>[!NOTE]
>
>* Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd. Voor informatie over de huidige versie, zie de Nota&#39;s [van de Versie van het](release-notes.md)Doel. De informatie op deze pagina&#39;s kan hetzelfde zijn of anders, afhankelijk van de timing van de releases.
   >
   >
* De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.
   >
   >
* **Wijzigingen** TLS-ondersteuning: Vanaf 1 maart 2020 schakelt Target de ondersteuning voor TLS 1.1- en TLS 1.0-codering uit. De Veiligheid van de Laag van het vervoer (TLS) is het wijdst opgestelde veiligheidsprotocol dat vandaag voor Webbrowsers en andere toepassingen wordt gebruikt die gegevens vereisen om veilig over een netwerk worden geruild. Deze wijziging is nodig om te voldoen aan de algemeen aanvaarde norm voor beveiligingsconformiteit van TLS 1.2 of hoger. Controleer welke TLS-versie u momenteel gebruikt. Als uw versie lager is dan 1.2, implementeert u de vereiste wijzigingen vóór 1 maart 2020 om Target te blijven gebruiken zoals u had verwacht.
   >
   >   
   Voor gedetailleerde informatie over de mogelijke invloed en de stappen u zou kunnen moeten nemen om uw implementatie bij te werken, zie de encryptieveranderingen [van](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md)TLS (de Veiligheid van de Laag van het Vervoer).
   >
   >
* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020, zullen alle vraag die van mbox.js wordt gemaakt ontbreken en zullen uw pagina&#39;s beïnvloeden die de actieve activiteiten van het Doel hebben. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)At.js voor meer informatie.
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.


## Target Standard/Premium 20.2.1 (17 maart 2020)

>[!IMPORTANT]
>
>Zie de bovenstaande informatie over de afschrijving van mbox.js.

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij klanten een verzameling niet konden selecteren tijdens het uitvoeren van een cataloguszoekopdracht. (TGT-36230)
* Probleem verholpen waarbij een criterium dat via API is gemaakt, maar waarnaar niet wordt verwezen door een activiteit die in de doelinterface is gemaakt, ten onrechte uit de gebruikersinterface kan worden verwijderd. (TGT-35917)
* Geïmplementeerde veiligheidsverbeteringen aan het Beleid van de Veiligheid van de Inhoud (CSP). (TGT-36190)
* Probleem verholpen waarbij &quot;NaN%&quot; werd weergegeven wanneer de percentagebalk voor kenmerkweging naar links werd verschoven. (TGT-36211)
* Opgeloste lokalisatieproblemen zodat de UI-tekst in verschillende talen correct wordt weergegeven.
* De volgende Adobe Analytics-meetgegevens worden niet meer ondersteund voor Analytics for Target (A4T) die van kracht zijn met de Target-versie van maart 2020:
   * averagevisitdepth
   * bots
* De volgende metriek worden niet meer gesteund en automatisch omgezet in nieuwe versies van metrisch wanneer een gebruiker een activiteit wijzigt die metrisch bevat:

   | Vervangen metrisch | Nieuwe metrisch |
   |--- |--- |
   | `averagetimespentonpage` | `averagetimespentonsite` (opmerking: gemeten in minuten in plaats van seconden) |
   | `instances` | `occurrences` |
   | `singleaccess` | `singlepagevisits` |
   | `uniquevisitors` | `visitors` |
   | `visitorsdaily`, `visitorshourly`, `visitorsmonthly`, `visitorsquarterly`, `visitorsweekly`, `visitorsyearly` | `visitors` |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Meld u aan voor de Adobe Priority Product Update als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
