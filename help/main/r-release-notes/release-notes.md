---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 63df83fd7479c7be7e4cd4c08501ab17511a41fb
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard] - en [!DNL Target Premium] -release. Daarnaast worden releaseopmerkingen voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Adobe Target] [!DNL AI Assistant] release (16 mei 2025)

We zijn blij dat we de start van de [!DNL AI Assistant] in [!DNL Adobe Target] aankondigen! Deze krachtige gebruikersinterfacefunctie is ontworpen om u te helpen gemakkelijk door [!DNL Target] concepten te navigeren en deze te begrijpen. Deze functie is beschikbaar voor meerdere producten in [!DNL Adobe Experience Cloud] , inclusief [!DNL Target] , [!DNL AI Assistant] om uw ervaring te veranderen.

[!DNL AI Assistant] in [!UICONTROL Target] is een conversatieprogramma dat u kunt gebruiken om uw workflows te versnellen met [!DNL Experience Platform] -toepassingen en -services. Gebruik [!DNL AI Assistant] om uw algehele productiviteit te verhogen en uw inzicht in productkennis te vergroten

In [!DNL Target] biedt de eerste fase van [!DNL AI Assistant] waardevolle productkennis die in [!DNL Experience League] -documentatie is gebaseerd. Of u nu een profielscript instelt, fouten met het oplossen van problemen oplost of een upgrade naar AEP Web SDK overweegt, [!DNL AI Assistant] heeft u behandeld.

Voor meer informatie, zie [ de Medewerkingsoverzicht van Adobe Experience Platform AI ](/help/main/c-intro/ai-assistant.md).

## [!DNL Target Standard/Premium] 25.5.2 (8 mei 2025)

Deze release bevat de volgende correcties en updates:

* [!DNL Target] -gebruikers met [!UICONTROL Product Administrator] - en [!UICONTROL System Administrator] -rechten kunnen nu alle instellingen op de [!UICONTROL Administration] -pagina&#39;s bewerken, ongeacht hun rol in [!DNL Target] . Gebruikers zonder deze machtigingen hebben alleen-lezen toegang tot deze instellingen. Deze update verzekert striktere toegangscontrole over [ montages van het Beleid ](/help/main/administrating-target/administrating-target.md). (TGT-48179)
* Vaste een caching kwestie die sparen activiteit [ Voorkeur van de Plaats ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) verhinderde. (TGT-52213)
* Klanten konden geen selectie via id en klasse inschakelen in de sectie [!UICONTROL Site Preferences] nadat ze de site in de VEC hadden geladen. Dit probleem is nu opgelost. De instelling [!UICONTROL Site Preferences] wordt automatisch teruggezet naar uitgeschakeld, zelfs nadat deze is ingeschakeld. (TGT-52207)
* Oplossing voor een kwestie waar [!UICONTROL Visual Experience Composer] (VEC) er niet in slaagde om de correcte pagina te tonen wanneer [ paginalevering ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#settings) URLs met een voorwaartse schuine streep (/) beëindigde. (TGT-52237)
* Probleem verholpen waarbij wijzigingen in aangepaste code niet konden worden verwijderd tijdens het wijzigen van ervaringen. (TGT-52240)
* Probleem verholpen waarbij HTML-wijzigingen in de VEC bestaande pagina-elementen overlapten. (TGT-52265)
* Probleem verholpen waarbij het bewerken van aangepaste code in de bijgewerkte VEC werd verhinderd omdat de bestaande aangepaste code niet zichtbaar was in de editor. (TGT-52272)
* Probleem verholpen waarbij het foutbericht &#39;Dubbele namen zijn niet toegestaan&#39; werd gegenereerd bij het opslaan van een activiteit met aanbevelingen. (TGT-52318)
* Probleem verholpen in de bijgewerkte VEC waardoor klanten tekstelementen niet konden bewerken of containerobjecten konden verwijderen. (TGT-52348)
* Probleem verholpen waarbij [!DNL Customer Journey Analytics] werd geblokkeerd zodat deze niet correct kon worden weergegeven op een pagina met [!UICONTROL Overview] -activiteiten. (TGT-52359)
* Probleem verholpen waardoor rapportgroepen niet konden doorgaan met [!UICONTROL Automated Personalization] (AP)-activiteiten. (TGT-52368)
* Probleem verholpen waarbij het opslaan van activiteiten zoals het bepalen van aanbiedingen werd voorkomen. (TGT-52390)
* Probleem verholpen waarbij de standaardaanbieding was geselecteerd, maar andere aanbiedingsinhoud die in [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Multivariate Test] (MVT)-activiteiten werd weergegeven. (TGT-52372)
* Oplossing voor GET-machtigingenlogica voor controle met OR tussen volledige toegang tot org en specifieke toegang voor org + gebruiker. (TGT-52374)
* Probleem verholpen waarbij publieksnamen niet werden weergegeven nadat een publiek voor [!UICONTROL Managed Content] en [!UICONTROL Reporting Audiences] was geselecteerd, ook al was [!UICONTROL Show Only Selected] ingeschakeld. (TGT-52393)

## [!DNL Target Standard/Premium] 25.5.1 (5 mei 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij werd voorkomen dat publieksverfijningen worden weergegeven voor bepaalde activiteiten in de bijgewerkte gebruikersinterface. (TGT-52057)
* Probleem verholpen waarbij het gebruik van gecombineerd publiek in activiteiten werd voorkomen. (TGT-52346)
* Probleem verholpen waarbij het maken van een nieuwe activiteit in een niet-standaardwerkruimte werd voorkomen met een alleen-activiteit publiek in dezelfde werkruimte. (TGE-52349)
* Probleem verholpen waarbij alleen-activiteit publiek uit de bijgewerkte gebruikersinterface verdween nadat een nieuw publiek was gemaakt en geselecteerd. (TGT=52091)
* Probleem verholpen waarbij het gebruik van dubbele doelgroepen in activiteiten werd voorkomen. (TGT-51200 &amp; TGT-52057)
* Probleem verholpen waarbij publieksverfijningen en het activiteitenpubliek werden omgekeerd in de bijgewerkte gebruikersinterface. (TGT-52158)
* Probleem verholpen waarbij het maken van een nieuwe activiteit niet mogelijk was als gevolg van een gebruikersinvoerfout: &quot;Niet-standaardwerkruimte niet toegestaan voor deze gebruiker.&quot; (TGT-52267)
* Probleem verholpen waardoor voorstellen niet konden worden weergegeven in de bijgewerkte gebruikersinterface voor zowel standaardwerkruimten als niet-standaardwerkruimten. [!DNL Target] geeft nu voorstellen van beide werkruimten weer. (TGT-52339)
* [!DNL Target] heeft een probleem verholpen waarbij klanten niet werden gewaarschuwd wanneer ze een activiteit bewerkten en een gewijzigd website-element veranderden. (TGT-52100)
* Probleem verholpen waarbij tijdens het bewerken van een voorstel met ad-hocaanbiedingen een nieuwe aanbieding werd gemaakt in plaats van de bestaande aanbieding bij te werken. (TGT-52135)
* Probleem verholpen dat een ongeldige laadfout veroorzaakte bij het verplaatsen van voorstellen naar mappen. (TGT-52325)
* Probleem verholpen waarbij een fout met gebruikersinvoer werd veroorzaakt bij het verplaatsen van aanbiedingen naar mappen. (TGT-52296)
* Er is een veld `audienceMetadata` toegevoegd voor elke activiteit en er is voor gezorgd dat dit wordt gelezen en bijgewerkt tijdens het bewerken van de activiteit. (TGT-51004)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=nl-NL) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
