---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: b9ec7af30fda6e97e3b0372a02a682a177764742
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard] - en [!DNL Target Premium] -release. Daarnaast worden releaseopmerkingen voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Target Standard/Premium] 25.4.3 (11 april 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waardoor klanten de publieksinformatie-pop-up voor bepaalde [!UICONTROL Experience Targeting] (XT) activiteiten niet konden openen. (TGT-52049)
* Probleem verholpen waarbij de publieksinstelling terugkeerde naar &quot;[!UICONTROL All Visitors]&quot; na wijzigingen die in [!UICONTROL Visual Experience Composer] (VEC) waren aangebracht. (TGT-52132)
* Correctie van een probleem waarbij publieksverfijningen niet werden weergegeven voor specifieke activiteiten (TGT-52057)
* Probleem verholpen waardoor klanten [!UICONTROL Experience Fragment] niet konden invoegen in de standaardwerkruimte. (TGT-52073)
* Probleem verholpen waarbij een aanbieding liet zien dat &quot;Inhoud niet gevonden&quot; en niet op de pagina [!UICONTROL Offers] werd weergegeven voor een [!UICONTROL Automated Personalization] -activiteit (AP). (TGT-52150)
* De mogelijkheid toegevoegd om dubbele doelgroepen binnen een activiteit toe te staan. (TGT-51200)
* Probleem verholpen waarbij de verkeerde naam van het selectievakje op de pagina [!UICONTROL Goals & Settings] werd weergegeven voor een XT-activiteit na bewerking. (TGT-52026)
* Correctie van een probleem waarbij `defaultContent` werd weergegeven in opties ondanks dat het zich niet in `experiences/optionLocations` bevond. (TGT-52036)
* Oplossing voor een probleem dat ervoor zorgde dat lege tekenreeksen niet werden omgezet in null-waarden. (TGT-52037)
* Probleem verholpen waarbij klanten de [!UICONTROL Optimization Goal] in [!UICONTROL Reporting Settings] op de [!UICONTROL Goals & Settings] pagina na bewerkingen opnieuw moesten configureren. (TGT-52071)
* Probleem verholpen waarbij een activiteit zonder leveringsregels voor pagina&#39;s meerdere regels op de pagina [!UICONTROL Overview] weergaven. (TGT-52084)
* Er is een foutbericht toegevoegd voor gebruikers die een aanbieding proberen op te slaan met tekens buiten het meertalige basisvlak, zoals emojis. (TGT-52105)
* Probleem verholpen waarbij het openen van een activiteit het foutbericht veroorzaakte: &quot;Deze activiteit gebruikt een of meer soorten publiek die bij de bron zijn verwijderd.&quot; (TGT-52120)
* Probleem verholpen waarbij ClickTrack-meetgegevens niet werden weergegeven in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) tijdens het bewerken. (TGT-52152)
* Probleem verholpen waarbij een URL met een queryparameter als de activiteitenlocatie de queryparameter niet op de pagina [!UICONTROL Overview] van de activiteit weergaf. (TGT-51635)
* Probleem verholpen waarbij de volledige URL voor de beleving niet kon worden weergegeven in [!UICONTROL Browse mode] binnen de [!UICONTROL Visual Experience Composer] (VEC). (TGT-52101)
* Probleem verholpen waarbij tijdens het bewerken van een activiteit de levering van een pagina ertoe leidde dat &#39;/&#39; aan het einde van de URL werd toegevoegd, waardoor deze ongeldig werd. (TGT-52114)
* Probleem verholpen waarbij de koppeling [!UICONTROL Activity QA] in de [!UICONTROL Form-Based Experience Composer] -pagina onjuist werd omgeleid naar de [!DNL Adobe Experience Cloud] -startpagina. (TGT-52055)
* Probleem verholpen waarbij extra pagina&#39;s die aan de [!UICONTROL A/B Test] -activiteit zijn toegevoegd, niet werden behouden na het opslaan en opnieuw openen. (TGT-51994)
* Probleem verholpen waarbij klanten stijlen niet konden verwijderen uit de sectie inline stijl. (TGT-52070)
* Herstelde toegang tot [ kaarten van de publieksdefinitie ](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) in de [!UICONTROL Activity QA] dialoogdoos, gelijkend op erfenis UI. (TGT-52056)
* De bijgewerkte interface heeft pagina&#39;s of publiek niet zonder wijzigingen opgeslagen. Als klanten nieuwe pagina&#39;s of publiek aan een activiteit toevoegden maar geen veranderingen in hen aanbrengen, [!DNL Target] verwierp het ongewijzigde publiek bij het bewaren. Meldingen zijn toegevoegd op relevante plaatsen om gebruikers op de hoogte te stellen van dit gedrag. (TGT-52104)

## [!DNL Target Standard/Premium] 25.4.1 (2 april 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij het ervaringspubliek uit activiteiten verdween. (TGT-52003)
* Probleem verholpen dat onverwachte elementen veroorzaakte tijdens levering. (TGT-52011)
* Vaste een kwestie die klanten van het bekijken van het publiek in de het richten grafiek op de Ove [!UICONTROL r] meningspagina en tijdens activiteit het uitgeven blokkeerde. (TGT-52050)
* Probleem verholpen waardoor klanten hun ervaringen niet opnieuw konden rangschikken in volgorde van prioriteit in [!UICONTROL Experience Targeting] (XT)-activiteiten. (TGT-52054)
* Probleem verholpen dat onjuiste rendering veroorzaakte wanneer wijzigingen in tekststijl ongedaan werden gemaakt. (TGT-51876)
* Probleem verholpen waarbij [!DNL Target] bij het wijzigen van een omleidingsaanbieding ook alle [!UICONTROL ClickTrack] -kiezers verwijdert die aan die aanbieding zijn gekoppeld. (TGT-51936)
* Correctie van een probleem dat ertoe leidde dat [!DNL Target] de kiezer verkeerd opsloot bij het annuleren van [!UICONTROL ClickTrack] . (TGT-51937)
* Probleem verholpen waarbij een fout met een ongeldige naam werd gegenereerd na het openen en sluiten van de kiezer op de pagina [!UICONTROL Goals & Settings] zonder wijzigingen aan te brengen. (TGT-51983)
* Probleem verholpen waarbij het bewerken van ad-hocaanbiedingen die zijn gemaakt in de oudere gebruikersinterface van [!DNL Target] , werd geblokkeerd. (TGT-51984)
* Probleem verholpen waarbij bewerkingsactiviteiten met ad-hocvoorstellen met aangepaste code werden geblokkeerd. (TGT-51995)
* Probleem opgelost waarbij uitsluitingsregels werden weergegeven als insluitingsregels tijdens het bewerken van gecombineerde publieksdefinities. (TGT-51999)
* Probleem verholpen waardoor aangepaste code niet correct kon worden weergegeven tijdens het bewerken. (TGT-52005)
* Probleem verholpen waarbij de optie [!UICONTROL Insert Before] niet beschikbaar was voor het invoegen van inhoud vóór de navigatiebalk. (TGT-52031)
* Probleem verholpen waardoor de standaardervaring bij rapportage niet correct kon worden gemarkeerd. (TGT-51716)
* Probleem verholpen waarbij een `default message [Invalid optionLocalIds: xx]]` -bericht werd geactiveerd tijdens het maken van een activiteit. (TGT-52038)

## at.js versie 2.11.8 (31 maart 2025)

* Opgeloste CodeQL-geïdentificeerde kwetsbaarheid in de bevestiging van het koordachtervoegsel om randgevallen tijdens resize te verhinderen en verrichtingen te bewegen. (TNT-51516)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html) {target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html) {target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html) {target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
