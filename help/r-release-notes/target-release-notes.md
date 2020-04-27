---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-versies.
title: Opmerkingen bij de prerelease van Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: d45a38376ebe98d212fba3097159a7b89b792c53

---


# Opmerkingen bij de release Doel (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 27 april 2020**

Voor informatie over de huidige versie, zie de Nota&#39;s [van de Versie van het](release-notes.md)Doel. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020, zullen alle vraag die van mbox.js wordt gemaakt ontbreken en zullen uw pagina&#39;s beïnvloeden die de actieve activiteiten van het Doel hebben. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)At.js voor meer informatie. Zie *Adobe Target Skill Builder: Chat ontwikkelaar, migreer mbox.js van Adobe Target aan om.js* hieronder voor informatie over het registreren voor een aanstaande ontwikkelaarpraatje over dit onderwerp.
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.


## Adobe Target Skill Builder: Chat op ontwikkelaar, migrate mbox.js van Adobe Target aan at.js {#skill-builder}

Sluit u aan bij David Son, Adobe Target Product Manager, als u de voordelen van het migreren van mbox.js naar at.js inziet. Heer de recentste updates at.js, leer over zijn verbeterde mogelijkheden en hoe zij zich aan grotere tendensen in het technische landschap richten, evenals sommige praktische uiteinden om ervoor te zorgen dat u evenveel waarde van Doel haalt wanneer u van mbox.js aan at.js migreert. Adobe Target Developers will not want to don&#39;t!

Dinsdag 5 mei, 8:00 - 9:00 (PDT)

[Nu hier registreren!](https://atskillbuilder-devchat.experienceleague.adobeevents.com/)

## Target Standard/Premium 20.4.1 (27 april 2020)

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij een apparaat en browsertype voor een publiek onjuist worden gekwalificeerd. (TGT-36266)
* Probleem verholpen waarbij rapportgegevens niet konden worden weergegeven wanneer ze werden weergegeven op schermen met een breedte van minder dan 963 pixels. (TGT-36549)
* Probleem verholpen waardoor rapporten voor automatische personalisatie niet correct worden weergegeven. (TGT-36619)
* Probleem verholpen waarbij bepaalde opties in de Visual Experience Composer (VEC) niet correct werden weergegeven. (TGT-36571)
* Probleem verholpen in de interface Doel die ertoe heeft geleid dat andere aanbevelingen voorvertoningen van de bewerkte inhoud aanbieden nadat een gebruiker de inhoud in één ervaring heeft vervangen. (TGT-36053 &amp; TGT-36894)
* Probleem verholpen waarbij sommige gebruikers items niet konden verwijderen uit een catalogus met aanbevelingen. (TGT-36455)
* Probleem verholpen waardoor gebruikers geen criteria voor Aanbevelingen konden opslaan voor activiteiten van meerdere pagina&#39;s. (TGT-36249)
* Probleem verholpen waarbij de keuzerondjes voor de gegevensbron met gedragingen voor een tweede opeenvolgende keer werden verborgen bij het bewerken van de criteria. (TGT-36796)
* Probleem verholpen waarbij een algoritme met aanbevelingen een lange periode &#39;ophaalresultaten&#39; weergaf. (TGT-36550 &amp; TGT-36551)
* Veel UI-tekenreeksen die in verschillende talen zijn gelokaliseerd, zijn bijgewerkt.

## Wijzigingen in de profielbatchstatus-API v2 (4 mei 2020)

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
