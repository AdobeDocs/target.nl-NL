---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release van Adobe Target (huidige) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 81b9735ea1fa6c42aa9c73565efd68a4d474622c
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---


# Opmerkingen bij de doelversie (huidig){#target-release-notes-current}

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke doelstandaard- en doelpremiumversie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>* **Adobe noemde opnieuw een leider in het Magisch Kwadrant Gartner voor Personalisatietechnieken**: Adobe werd opnieuw benoemd tot leider in het derde jaarlijkse Gartner Magic Quadrant for Personalization Engines, verslag 2020. Het Magische kwadrant van Gartner voor de Motoren van de Personalisatie evalueerde verkopers over 15 criteria die in twee categorieën vallen: de volledigheid van het gezichtsvermogen en de uitvoerbaarheid. [Lees er over op The Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **afdruk** mbox.js: Op 18 januari 2021 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 18 januari 2021, zullen alle vraag die van mbox.js wordt gemaakt zachtjes ontbreken en zullen uw pagina&#39;s beïnvloeden die de activiteiten van het Doel hebben die door standaardinhoud te dienen lopen. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, zullen onze ingenieurs en steunpersoneel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.
   >
   >
* **Doelaankondigingen**: Zie de de aankondigingspagina van het Doel voor informatie over aanstaande gebeurtenissen, met inbegrip van de zittingen van de Bouwer van de Vaardigheid van het Doel, ontwikkelaarchats, webinars, en de zittingen van het Break van de Koffie van het Doel. Voor meer informatie, zie [de aankondigingen](/help/r-release-notes/target-announcements.md)van het Doel.


De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

## te.js 2.3.2 (24 juli 2020)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:

* Het probleem is opgelost wanneer een script of code een standaardeigenschap aan het venster of document toevoegt.

## Target Standard/Premium 20.7.1 (27 juli 2020)

Deze release bevat de volgende wijzigingen:

### [!UICONTROL Administration] sectie-UI vernieuwen

We herschrijven geleidelijk de gehele [!DNL Target] gebruikersinterface met behulp van een nieuwe technologiestapel om verbeterde prestaties te kunnen bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De eerste sectie die is vernieuwd, is de [!UICONTROL Setup] sectie, die is hernoemd [!UICONTROL Administration].

Als onderdeel van deze vernieuwing kunt u gemakkelijk veel handelingen uitvoeren met de pagina&#39;s in de [!UICONTROL Administration] sectie, zoals:

* Download het meest recente bestand at.js van het [!UICONTROL Implementation] tabblad (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Pas de instellingen op at.js aan en bekijk de wijzigingen eenvoudig (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Wijzig verbeterde rapporteringsmontages, zoals de standaardmunt en tijdzone, IPs om van rapportering uit te sluiten, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* IP-adressen van bezoekers om privacyredenen verduisteren (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* Bekijk de bestaande lijst met gebruikers per werkruimte en hun rollen, voordat u ze beheert in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**).
* Alle tabellen in de [!UICONTROL Administration] sectie zoeken en filteren.

Voor meer informatie, zie het Overzicht [van het Doel](/help/administrating-target/administrating-target.md)beheren.

### Verbeteringen, correcties en wijzigingen

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij sitevoorkeuren niet konden worden behouden na vernieuwen. (TGT-37239)
* Probleem verholpen waarbij het functioneren van > [!UICONTROL Insert After] [!UICONTROL Image] met SVG-afbeeldingen (Scalable Vector Graphics) werd verhinderd. (TGT-37242)
* Oplossing voor een probleem voor gebruikers met de [!UICONTROL Publisher] rol die het verwijderen van conceptactiviteiten heeft verhinderd. (TGT-37358)
* Probleem verholpen waardoor gebruikers een activiteit niet konden bewerken wanneer deze [!UICONTROL All My Workspaces] is geselecteerd. (TGT-37276)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release - Doelserver-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Opmerkingen bij de release met betrekking tot API&#39;s van de Adobe Target-server. |
| [Opmerkingen bij de release - Doel Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Release-aantekeningen met betrekking tot Adobe Target Node.js SDK. |
| [Opmerkingen bij de release - Doel Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Opmerkingen bij de release met betrekking tot de Adobe Target Java SDK. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek van Adobe Target at.js. |
| [mbox.js, versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.<br>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie [Documentatiewijzigingen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de [Versie voor vorige versies](../r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release [Experience Cloud voor meer informatie](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdatelijst | Meld u aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie de Nota&#39;s van de Versie van het [Doel - pre-releasepagina](/help/r-release-notes/target-release-notes.md) . |
