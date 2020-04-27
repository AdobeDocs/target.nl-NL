---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release Adobe Target (huidig) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: d45a38376ebe98d212fba3097159a7b89b792c53

---


# Opmerkingen bij de doelversie (huidig){#target-release-notes-current}

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke doelstandaard- en doelpremiumversie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020, zullen alle vraag die van mbox.js wordt gemaakt ontbreken en zullen uw pagina&#39;s beïnvloeden die de actieve activiteiten van het Doel hebben. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)At.js voor meer informatie. Zie *Adobe Target Skill Builder: Chat ontwikkelaar, migreer mbox.js van Adobe Target aan om.js* hieronder voor informatie over het registreren voor een aanstaande ontwikkelaarpraatje over dit onderwerp.
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.


De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

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

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release - Doelserver-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Opmerkingen bij de release die betrekking hebben op de API&#39;s aan de serverzijde van Adobe Target. |
| [Opmerkingen bij de release - Doel Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Opmerkingen bij de release die betrekking hebben op Node.js SDK van Adobe Target. |
| [Opmerkingen bij de release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Opmerkingen bij de release die betrekking hebben op de Java SDK van Adobe Target. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over de wijzigingen in elke versie van Adobe Target op JavaScript.js. |
| [mbox.js, versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.<br>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. |

## Documentatiewijzigingen, opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie [Documentatiewijzigingen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de [Versie voor vorige versies](../r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release van de [cloud voor meer informatie](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Update-lijst voor producten van Adobe Priority | Meld u aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie de Nota&#39;s van de Versie van het [Doel - pre-releasepagina](/help/r-release-notes/target-release-notes.md) . |
