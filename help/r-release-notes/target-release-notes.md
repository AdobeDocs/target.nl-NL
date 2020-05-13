---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-versies.
title: Opmerkingen bij de prerelease van Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: ae97b36e9a5aaa0394fb3b4ab1ad40b38a0c97be
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# Opmerkingen bij de release Doel (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 4 mei 2020**

Voor informatie over de huidige versie, zie de Nota&#39;s [van de Versie van het](release-notes.md)Doel. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020, zullen alle vraag die van mbox.js wordt gemaakt ontbreken en zullen uw pagina&#39;s beïnvloeden die de actieve activiteiten van het Doel hebben. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)At.js voor meer informatie. Zie *Adobe Target Skill Builder: Chat ontwikkelaar, migreer mbox.js van Adobe Target aan om.js* hieronder voor informatie.
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.


## Adobe Target Skill Builder: Chat op ontwikkelaar, migrate mbox.js van Adobe Target aan at.js {#skill-builder}

Met de aanstaande veroudering van mbox.js op 30 augustus 2020, ontving David Son, de Manager van het Product van het Doel van Adobe onlangs een ontwikkelaarspraatje om de voordelen van het migreren van mbox.js aan te bespreken. De komende 30 dagen kunt u de webinar opname [](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true)bekijken.

## Target Standard/Premium 20.5.1 (10 juni 2020)

Details van deze release worden hier gepubliceerd.

## Wijzigingen in de status-API van profielbatch v2 (TBD-datum)

Met de release van 4 mei retourneert de profielbatchstatus alleen gegevens voor mislukkingen op rijniveau die worden uitgevoerd (succesgegevens worden niet geretourneerd). Mislukte profiel-id&#39;s worden door de API geretourneerd.

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

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Meld u aan voor de Adobe Priority Product Update als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
