---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c5016d212edafa908b8755044e73d28167e20e8a
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 24 juli 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.8.2 (13 augustus 2025)

Deze release bevat de volgende correcties en updates:

**[!UICONTROL Activities]**

+++Zie details
* Probleem verholpen waarbij bepaalde activiteiten niet konden worden geladen tijdens een poging tot bewerken in de bijgewerkte gebruikersinterface van [!DNL Target] . Dit probleem heeft ertoe geleid dat klanten gebruikers in een onbepaald laadscherm hebben verlaten. Deze kwestie had gevolgen voor meerdere activiteiten en zou onsamenhangend zijn voor alle klanten. Met deze oplossing worden de betrokken activiteiten nu correct geladen, zodat ze naadloos kunnen worden bewerkt en de workflows met activiteiten minder worden verstoord. (TGT-53209)
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij klanten geen wijzigingen konden opslaan als gevolg van een validatiefout aan het einde: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` dit probleem is opgetreden bij het wijzigen van specifieke elementen binnen een activiteit, wat resulteerde in een mislukte opslagbewerking. De oplossing zorgt ervoor dat `optionLocalId` -verwijzingen nu correct worden gevalideerd, zodat klanten activiteiten kunnen opslaan zonder deze fout te ondervinden. (TGT-53293)
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij de interface vastliep nadat tijdens het bewerken drie keer van pagina&#39;s was gewisseld. Het neerstorten werd teweeggebracht door ongeldige optieverwijzingen, resulterend in consolefouten zoals &quot;Optie met localId &quot;7&quot;niet gevonden.&quot; Met deze update kunnen klanten nu schakelen tussen pagina&#39;s en wijzigingen toepassen zonder systeemfouten of onderbrekingen te ondervinden. (TGT-53295)
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij klanten geen wijzigingen konden opslaan in een activiteit als gevolg van een ongeldige gebruikersinvoerfout. De fout kwam bij het wijzigen van ervaringen in bijgewerkte UI voor, die updates verhinderen worden begaan. De activiteit kan nu met succes worden bewaard, toestaand klanten om zonder onderbreking uit te geven en te publiceren. (TGT-53267)
* Probleem verholpen tijdens het &#39;activity-create&#39;-proces waarbij klanten geen activiteiten konden bewerken in de bijgewerkte gebruikersinterface vanwege een doorlopend laadscherm. Klanten kunnen nu activiteiten openen en wijzigen zonder dat er problemen optreden bij het laden. (TGT-53415)

+++

**Fragmenten van de Ervaring (XFs)**

+++Zie details
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij klanten de HTML van [!DNL Experience Fragments] (XFs) konden bewerken die vanuit [!DNL Adobe Experience Manager] (AEM) binnen [!DNL Target] waren geëxporteerd. Dit gedrag was onbedoeld, aangezien XFs voor het uitgeven zou moeten gesloten blijven zodra gepubliceerd van AEM. De oplossing zorgt ervoor dat de optie HTML bewerken niet langer beschikbaar is voor AEM-geëxporteerde fragmenten, zodat de integriteit van de inhoud en het verwachte beheer behouden blijven. (TGT-53286)

+++

**wijze QA**

+++Zie details
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij de spaties aan het begin van de activiteit in de activiteit-URL niet correct werden bijgesneden tijdens het opslaan. Dit veroorzaakte ongeldige verbindingen QA en onjuiste formatteren in het achterste eind. Na de update, worden URLs nu bewaard zuiverder, verhinderend gebroken verbindingen en verbeterend de betrouwbaarheid van QA werkschema&#39;s voor klanten. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Zie details
* Correctie van een probleem in de nieuwe gebruikersinterface van [!UICONTROL Catalog Search] waarbij de functie van [!UICONTROL Advanced Search] geen suggesties kon bieden. De gebruikers werden vereist om nauwkeurige waarden met nauwkeurige spelling in te voeren, die de onderzoekservaring omslachtig en fout-gevoelig maken. Met deze oplossing biedt [!UICONTROL Advanced Search] nu relevante suggesties zoals gebruikers typen, die bruikbaarheid verbeteren en wrijving bij het zoeken naar producten verminderen. (TGT-52008)
* Verschillende problemen zijn opgelost, zoals een slechte respons op de details van criteria op apparaten met een klein scherm, een gebrek aan resultaten bij het selecteren van &quot;Alle hostgroepen&quot; in het filter [!UICONTROL Environment] en het onvermogen om te communiceren met entiteiten zonder naam. Deze correcties verbeteren de bruikbaarheid in verschillende schermgrootten, zorgen voor nauwkeurige filtering en maken volledige interactie met alle productentiteiten mogelijk, waardoor de algemene gebruikerservaring wordt verbeterd. (TGT-52992)
* Probleem verholpen in het [!DNL Recommendations] activity-create proces waarbij product-id&#39;s ontbraken in het detailscherm van het product, waardoor het voor klanten moeilijk was om tijdens workflows te kopiëren of te verwijzen naar product-id&#39;s. De product-id&#39;s worden nu duidelijk weergegeven in de gedetailleerde weergave, waardoor de zichtbaarheid wordt verbeterd en een efficiënter productbeheer voor klanten wordt ondersteund. (TGT-51964)
* Probleem verholpen in het activity-create proces waarbij de kolom [!UICONTROL Message] in de [!DNL Recommendations] -weergave geen productgegevens weergaf, ook al waren er berichten aanwezig. Klanten moesten de kolom handmatig verwijderen en opnieuw toevoegen om de inhoud tijdelijk weer te geven. Deze verdwijnt vaak weer wanneer ze schuiven of zoeken. Deze update herstelt consistente zichtbaarheid van productberichten, waardoor de workflows voor catalogusnavigatie en -revisie worden verbeterd. (TGT-52777)
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij het selecteren van de omgeving Alle hostgroepen in de weergave [!DNL Recommendations] geen resultaten heeft opgeleverd. Klanten kunnen productgegevens nu op alle hostgroepen weergeven zoals verwacht, waardoor de zichtbaarheid en filternauwkeurigheid tijdens het instellen van de activiteit worden verbeterd. (TGT-53006)
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij het uitschakelen van de voorste promotieschakeloptie in de activiteiteninstellingen niet meer voorkwam na het opslaan. Klanten die probeerden de frontbevordering te verwijderen, vonden de knevel opnieuw-toegelaten na het herzien van de activiteit, die correcte aanpassing verhinderden. Met deze update kunnen wijzigingen op betrouwbare wijze worden opgeslagen, zodat klanten de volledige controle hebben over instellingen voor speciale acties. (TGT-53215)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* Probleem verholpen tijdens het proces voor het maken van activiteiten waarbij bepaalde activiteiten niet konden worden geladen, zodat klanten geen toegang hadden tot wijzigingen. Bovendien reageerde de knop [!UICONTROL Cancel] niet, waardoor klanten het laadproces niet konden stoppen of de bewerkingsweergave konden verlaten. Deze correctie zorgt ervoor dat activiteiten nu betrouwbaar worden geladen en de [!UICONTROL Cancel] knopfuncties naar behoren werken, wat de algehele stabiliteit en gebruikerservaring in Visual Experience Composer (VEC) verbetert (TGT-53218)
* Probleem verholpen in de bijgewerkte VEC UI waar de wijzigingen er niet in slaagden om te schakelen tussen ervaringen in een (XT) activiteit van de Ervaring richtend. Klanten konden de ervaringen die ze oorspronkelijk hadden ingevoerd, niet bewerken en de knop [!UICONTROL Cancel] ontbreekt of reageert niet. Deze correctie zorgt ervoor dat wijzigingen nu correct worden geladen over alle ervaringen en dat de knop [!UICONTROL Cancel] betrouwbaar werkt, zelfs zonder de Helper-extensie, waardoor bewerkingsworkflows worden verbeterd en frustratie wordt verminderd. (TGT-53256)
* Probleem verholpen waarbij het schakelen tussen meerdere ervaringen een wit scherm veroorzaakte. Probleem verholpen tijdens het &#39;activity-create&#39;-proces waarbij klanten een wit scherm tegenkwamen bij het wijzigen van meerdere ervaringen binnen een activiteit. Dit probleem is opgetreden nadat u wijzigingen hebt aangebracht in twee ervaringen en vervolgens een derde ervaring hebt gekozen, waardoor verdere bewerkingen zijn voorkomen. De update zorgt voor vloeiende overgangen tussen ervaringen, waardoor klanten zonder onderbreking wijzigingen kunnen aanbrengen. (TGT-53266)
* Probleem verholpen waarbij de wijzigingen van de douanecode die in Visual Experience Composer (VEC) werden aangebracht, niet betrouwbaar in één enkele poging werden opgeslagen. Klanten meldden dat wijzigingen, zoals styling updates of HTML-bewerking, periodiek ontbraken van de website en QA-URL&#39;s, zelfs nadat ze zowel de [!UICONTROL Edit Content] - als de laatste [!UICONTROL Save] -knoppen hadden gebruikt. Deze regressie is opgelost, zodat alle wijzigingen in de aangepaste code tijdens de bewerkingssessies ongewijzigd blijven. (TGT-53418)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
