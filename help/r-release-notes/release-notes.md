---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release van Adobe Target (huidige) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 25f7ce65f4f9b863ce6ebfe0a7ff8df08e561741
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---


# Opmerkingen bij de release van Target (huidige){#target-release-notes-current}

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke release van Target Standard en Target Premium. Daarnaast worden releaseopmerkingen voor Target API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020 zullen alle oproepen van mbox.js mislukken en gevolgen hebben voor uw pagina&#39;s waarop Target-activiteiten worden uitgevoerd. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.
   >
   >
* **Aankondigingen** van Target: Zie de Target-aankondigingspagina voor informatie over aanstaande gebeurtenissen, zoals Target Skill Builder-sessies, ontwikkelaarstekkers, webinars en Target Coffee Break-sessies. Zie [Target-aankondigingen](/help/r-release-notes/target-announcements.md)voor meer informatie.


De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

## Wijzigingen in de profielbatchstatus-API v2 (14 mei 2020)

Met de versie van 20 mei, zal de status van de Batch van het Profiel slechts rij-vlakke mislukkingsgegevens terugkeren die door:gaan (de succesgegevens zullen niet worden teruggekeerd). Mislukte profiel-id&#39;s worden door de API geretourneerd.

De vorige en nieuwe API-reacties zijn als volgt:

`ProfileBatchStatus Api
http://<<edge>>/m2/<<client>>/profile/batchStatus?batchId=<batchid>`

**Momenteel zien we het antwoord als:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>1514187733806-729395</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>1573612762055-214017</id>
 
        <status>success</status>
 
    </profile>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

**Na 4 mei zal het antwoord zijn:**

```
<response>
 
    <batchId>samplebatch-1585929692655-59449976</batchId>
 
    <status>complete</status>
 
    <batchSize>164</batchSize>
 
    <profile>
 
        <id>some profile id</id>
 
        <status>failed</status>
 
    </profile>
 
</response>
```

## Target Standard/Premium 20.4.1 (6 mei 2020)

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij een apparaat en browsertype voor een publiek onjuist worden gekwalificeerd. (TGT-36266)
* Probleem verholpen waarbij rapportgegevens niet konden worden weergegeven wanneer ze werden weergegeven op schermen met een breedte van minder dan 963 pixels. (TGT-36549)
* Probleem verholpen waardoor rapporten voor automatische personalisatie niet correct worden weergegeven. (TGT-36619)
* Probleem verholpen waarbij incompatibele metriek kon worden geselecteerd in Auto-Allocate en Auto-Target activiteiten die Analytics voor Target (A4t) gebruiken. (TGT-36646)
* Probleem verholpen waarbij bepaalde opties in de Visual Experience Composer (VEC) niet correct werden weergegeven. (TGT-36571)
* Probleem verholpen in de gebruikersinterface van Target die ertoe heeft geleid dat andere aanbevelingen voorvertoningen van bewerkte inhoud aanbieden nadat een gebruiker de inhoud in één ervaring heeft vervangen. (TGT-36053 &amp; TGT-36894)
* Probleem verholpen waarbij sommige gebruikers items niet konden verwijderen uit een catalogus met aanbevelingen. (TGT-36455)
* Probleem verholpen waardoor gebruikers geen criteria voor Aanbevelingen konden opslaan voor activiteiten van meerdere pagina&#39;s. (TGT-36249)
* Probleem verholpen waarbij de keuzerondjes voor de gegevensbron met gedragingen voor een tweede opeenvolgende keer werden verborgen bij het bewerken van de criteria. (TGT-36796)
* Probleem verholpen waarbij een algoritme met aanbevelingen een lange periode &#39;ophaalresultaten&#39; weergaf. (TGT-36550 &amp; TGT-36551)
* Veel UI-tekenreeksen die in verschillende talen zijn gelokaliseerd, zijn bijgewerkt.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release - Target server-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Opmerkingen bij de release met betrekking tot API&#39;s van de Adobe Target-server. |
| [Opmerkingen bij de release - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Release-aantekeningen met betrekking tot Adobe Target Node.js SDK. |
| [Opmerkingen bij de release - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Opmerkingen bij de release met betrekking tot de Adobe Target Java SDK. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek van Adobe Target at.js. |
| [mbox.js, versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.<br>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie [Documentatiewijzigingen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de [Versie voor vorige versies](../r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release van [Experience Cloud voor meer informatie](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

Met de volgende bronnen kunt u zien wat er in de volgende Target-release komt.

| Resource | Details |
|--- |--- |
| Update-lijst voor producten van Adobe Priority | Meld u aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de Target-releases van deze maand, waaronder pre-releasegegevens, raadpleegt u de [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
