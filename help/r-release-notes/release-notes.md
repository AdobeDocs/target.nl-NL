---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release Adobe Target (huidig) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 51abcafed1641d073b38800d0fea756df92b3685

---


# Opmerkingen bij de doelversie (huidig){#target-release-notes-current}

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke doelstandaard- en doelpremiumversie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!NOTE]
>
>* **Wijzigingen** TLS-ondersteuning: Vanaf 1 maart 2020 schakelt Target de ondersteuning voor TLS 1.1- en TLS 1.0-codering uit. De Veiligheid van de Laag van het vervoer (TLS) is het wijdst opgestelde veiligheidsprotocol dat vandaag voor Webbrowsers en andere toepassingen wordt gebruikt die gegevens vereisen om veilig over een netwerk worden geruild. Deze wijziging is nodig om te voldoen aan de algemeen aanvaarde norm voor beveiligingsconformiteit van TLS 1.2 of hoger. Controleer welke TLS-versie u momenteel gebruikt. Als uw versie lager is dan 1.2, implementeert u de vereiste wijzigingen vóór 1 maart 2020 om Target te blijven gebruiken zoals u had verwacht.
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
   >
   >
* De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.


## Top Live: De Digital Experience Conference {#summit}

De Adobe-top is een virtuele gebeurtenis geworden! Adobe haalt alle stops uit dankzij een live digitale ervaring vanaf 31 maart 2020. Deze live ervaring omvat ons belangrijkste trefwoordadres, mini-keynotes met de nieuwste trends en verbeteringen, inzichten in het succes van toonaangevende bedrijven en brainstormsessies.

* **Bekijk de live** keynote: Heb over tendensen en nieuwe producten die industrieën van het gemak van uw overal veranderen.
* **Ontdek meer dan 100 brainstormsessies op aanvraag:** Profiteer van gratis toegang tot meer dan honderd brainstormsessies op aanvraag van Adobe, klanten en partners.
* **Maak een hoogtepunt in de toekomst**: Neem deel aan de speciale gast Chelsea Handler voor een overzicht van de nieuwste experimentele technologie van onze laboratoria — op Adobe Sneaks.

Als u zich wilt registreren voor gratis toegang tot de gehele digitale gebeurtenis, gaat u naar [de Digital Experience Conference: De pagina van de top](https://www.adobe.com/summit.html) .

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

## Adobe Experience Cloud navigation (22 februari 2019)

* Wanneer u zich bij het programma aanmeldt, gaat u naar de nieuwe koptekstnavigatie. [!DNL Adobe Experience Cloud] Het lijkt sterk op de vorige navigatie met de zwarte balk bovenaan, maar biedt de volgende verbeteringen:

   * Eenvoudiger overschakelen tussen [!DNL Identity Management System] (IMS) organisaties of naar een andere oplossing.
   * Verbeterde gebruikershulp: Zoekresultaten zijn resultaten uit de [!DNL Target] productdocumentatie, maar ook uit communityforums en meer video-inhoud. Hierdoor hebt u gemakkelijker toegang tot meer inhoud om optimaal te profiteren [!DNL Target]. We hebben ook een feedbackmechanisme toegevoegd in het [!UICONTROL Help] menu, waardoor het gemakkelijker wordt om problemen te melden of uw ideeën te delen.

   * De verbeterde NPS-feedbackfunctionaliteit (Net Promoter Score), zodat de enquêtemodale modus uw workflow niet verstoort.
   * Verbeterde aanmeldstroom. Eerder zijn alle [!DNL Target] klanten op de bestemmingspagina geland nadat ze op het [!DNL Target] pictogram in de koptekst hadden geklikt. Op deze pagina konden klanten verder gaan met [!DNL Target Standard/Premium], [!DNL Search&Promote]of [!DNL Recommendations Classic], zoals hieronder wordt getoond:

      ![Openingspagina](/help/r-release-notes/assets/landing.png)

      We hebben deze bestemmingspagina voor al onze klanten verwijderd. U wordt nu altijd rechtstreeks naar de [!UICONTROL Activities List] pagina geleid door op het [!DNL Target] pictogram in de nieuwe koptekstnavigatiebalk te klikken.

      Als u gebruikt [!DNL Recommendations Classic], kunt u of rechtstreeks naar de oplossing gaan of u kunt van de korte verbinding gaan die op het [!UICONTROL Recommendations] lusje wordt gecreeerd, zoals hieronder getoond:

      ![Klassieke koppeling opnieuw instellen](/help/r-release-notes/assets/recs-classic.png)

      Als u [!DNL Search&Promote]deze optie gebruikt, moet u rechtstreeks naar de URL [voor](https://center.atomz.com/center/?ims=1) zoeken en bevorderen (https://center.atomz.com/center/?ims=1) gaan. Het pad dat moet worden bereikt [!DNL Search&Promote] van binnenuit van [!DNL Adobe Target] is volledig verwijderd.

   * Meldingen voor [!DNL Target] zijn momenteel niet beschikbaar in de [!UICONTROL Notifications] vervolgkeuzelijst in de koptekst.
   >[!NOTE]
   >
   >Tijdens de introductie van de nieuwe navigatiebalk zult u ook enkele URL-wijzigingen zien. Alle vorige bladwijzerkoppelingen werken nog steeds, maar we raden u aan nieuwe bladwijzerkoppelingen te maken om deze sneller te openen.

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
