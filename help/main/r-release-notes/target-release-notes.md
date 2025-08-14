---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: d09e02db4ea94671e2450d1748b07def932916d9
workflow-type: tm+mt
source-wordcount: '1378'
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

## [!DNL Target Standard/Premium] 25.8.2 (14 augustus 2025)

Deze release bevat de volgende correcties en updates:

**[!UICONTROL Activities]**

+++Zie details
* **Vaste activiteit-ladende kwestie in bijgewerkte [!DNL Target] UI**: Oplossing een kwestie in bijgewerkte [!DNL Target] UI waar bepaalde activiteiten er niet in slaagden toen het proberen uit te geven. Dit probleem heeft ertoe geleid dat klanten gebruikers in een onbepaald laadscherm hebben verlaten. Deze kwestie had gevolgen voor meerdere activiteiten en zou onsamenhangend zijn voor alle klanten. Met deze oplossing worden de betrokken activiteiten nu correct geladen, zodat ze naadloos kunnen worden bewerkt en de workflows met activiteiten minder worden verstoord. (TGT-53209)
* **Vaste sparen fout in activiteit-creeer proces toe te schrijven aan `optionLocalId` bevestiging**: Vaste een kwestie in het activiteit-creeer proces dat klanten verhinderde veranderingen toe te schrijven aan een fout van de achterste plaatsbevestiging: `OptionLocalIdReferentialIntegrity.ABActivity - Invalid optionLocalIds:` Deze kwestie kwam voor wanneer het wijzigen van specifieke elementen binnen een activiteit, resulterend in ontbroken sparen verrichting. De oplossing zorgt ervoor dat `optionLocalId` -verwijzingen nu correct worden gevalideerd, zodat klanten activiteiten kunnen opslaan zonder deze fout te ondervinden. (TGT-53293)
* **Vaste neerstorting in activiteit-creeer proces dat door ongeldige optieverwijzingen wordt veroorzaakt wanneer het schakelen van pagina&#39;s**: Vaste een kwestie in het activiteit-creeer proces dat UI veroorzaakte om na het schakelen van pagina&#39;s drie keer tijdens het uitgeven te crashen. Het neerstorten werd teweeggebracht door ongeldige optieverwijzingen, resulterend in consolefouten zoals &quot;Optie met localId &quot;7&quot;niet gevonden.&quot; Met deze update kunnen klanten nu schakelen tussen pagina&#39;s en wijzigingen toepassen zonder systeemfouten of onderbrekingen te ondervinden. (TGT-53295)
* **Vaste sparen fout in activiteit-creeer proces dat door ongeldige gebruikersinput wordt veroorzaakt wanneer het uitgeven van ervaringen**: Vaste een kwestie in het activiteit-creeer proces waar de klanten veranderingen in een activiteit niet konden bewaren toe te schrijven aan een ongeldige fout van de gebruikersinput. De fout kwam bij het wijzigen van ervaringen in bijgewerkte UI voor, die updates verhinderen worden begaan. De activiteit kan nu met succes worden bewaard, toestaand klanten om zonder onderbreking uit te geven en te publiceren. (TGT-53267)
* **Vaste ladingskwestie in activiteit-creeer proces dat het blokkeerde uitgeven in bijgewerkte UI**: Vaste een kwestie in activiteit-creeert proces waar de klanten geen activiteiten in bijgewerkte UI wegens een ononderbroken ladingsscherm konden uitgeven. Klanten kunnen nu activiteiten openen en wijzigen zonder dat er problemen optreden bij het laden. (TGT-53415)

+++

**Fragmenten van de Ervaring (XFs)**

+++Zie details
* **Vaste kwestie in activiteit-creeer proces dat onbedoelde het uitgeven van HTML van AEM-Uitgevoerde fragmenten** toeliet: Vaste een kwestie in activiteit-creeer proces dat klanten toeliet om HTML van [!DNL Experience Fragments] (XFs) uit [!DNL Adobe Experience Manager] (AEM) binnen uit te geven [!DNL Target]. Dit gedrag was onbedoeld, aangezien XFs voor het uitgeven zou moeten gesloten blijven zodra gepubliceerd van AEM. De oplossing zorgt ervoor dat de optie HTML bewerken niet langer beschikbaar is voor AEM-geëxporteerde fragmenten, zodat de integriteit van de inhoud en het verwachte beheer behouden blijven. (TGT-53286)

+++

**wijze QA**

+++Zie details
* **Vaste kwestie in activiteit-creeer proces waar de belangrijke ruimten in URLs gebroken verbindingen QA** veroorzaakte: Vaste een kwestie in activiteit-creeer proces waar de belangrijke ruimten in de activiteit URL niet behoorlijk werden bijgesneden toen het bewaren. Dit veroorzaakte ongeldige verbindingen QA en onjuiste formatteren in het achterste eind. Na de update, worden URLs nu bewaard zuiverder, verhinderend gebroken verbindingen en verbeterend de betrouwbaarheid van QA werkschema&#39;s voor klanten. (TGT-53427)

+++

**[!UICONTROL Recommendations]**

+++Zie details
* **Vaste kwestie in catalogusonderzoek UI waar het geavanceerde onderzoek er niet in slaagde om suggesties** te verstrekken: Oplossing een kwestie in nieuwe [!UICONTROL Catalog Search] UI waar de [!UICONTROL Advanced Search] eigenschap geen suggesties kon verstrekken. De gebruikers werden vereist om nauwkeurige waarden met nauwkeurige spelling in te voeren, die de onderzoekservaring omslachtig en fout-gevoelig maken. Met deze oplossing biedt [!UICONTROL Advanced Search] nu relevante suggesties zoals gebruikers typen, die bruikbaarheid verbeteren en wrijving bij het zoeken naar producten verminderen. (TGT-52008)
* **lost veelvoudige UI en het filtreren kwesties op om ontvankelijkheid en entiteitinteractie te verbeteren**: Oplossing verscheidene kwesties, met inbegrip van slechte ontvankelijkheid van criteria details op klein-schermapparaten, gebrek aan resultaten wanneer het selecteren van &quot;Alle gastheergroepen&quot;in de filter van het Milieu, en onvermogen om met entiteiten op te treden die geen naam hebben. Deze correcties verbeteren de bruikbaarheid in verschillende schermgrootten, zorgen voor nauwkeurige filtering en maken volledige interactie met alle productentiteiten mogelijk, waardoor de algemene gebruikerservaring wordt verbeterd. (TGT-52992)
* **Vaste ontbrekende product IDs in de gedetailleerde mening van Aanbevelingen tijdens activiteitenverwezenlijking**: Vaste een kwestie in [!DNL Recommendations] activiteit-creeer proces waar product IDs van het scherm van het productdetail mist, die het voor klanten moeilijk maken om product IDs tijdens werkschema&#39;s te kopiëren of van verwijzingen te voorzien. De product-id&#39;s worden nu duidelijk weergegeven in de gedetailleerde weergave, waardoor de zichtbaarheid wordt verbeterd en een efficiënter productbeheer voor klanten wordt ondersteund. (TGT-51964)
* **Vaste kwestie in activiteit-creeer proces waar de productberichten om in aanbevelingen mening** ontbraken te tonen: Vaste een kwestie in het activiteit-creeer proces waar de [!UICONTROL Message] kolom in de [!DNL Recommendations] mening productgegevens niet vertoonde, alhoewel de berichten aanwezig waren. Klanten moesten de kolom handmatig verwijderen en opnieuw toevoegen om de inhoud tijdelijk weer te geven. Deze verdwijnt vaak weer wanneer ze schuiven of zoeken. Deze update herstelt consistente zichtbaarheid van productberichten, waardoor de workflows voor catalogusnavigatie en -revisie worden verbeterd. (TGT-52777)
* **Vaste kwestie in activiteit-creeer proces waar het selecteren van &quot;Alle gastheergroepen&quot;geen resultaten in aanbevelingen terugkeerde mening**: Vaste een kwestie in activiteit-creeer proces waar het selecteren van het &quot;Alle gastheergroepenmilieu in de [!DNL Recommendations] mening geen resultaten terugkeerde. Klanten kunnen productgegevens nu op alle hostgroepen weergeven zoals verwacht, waardoor de zichtbaarheid en filternauwkeurigheid tijdens het instellen van de activiteit worden verbeterd. (TGT-53006)
* **Vaste kwestie in activiteit-creeer proces waar de voorpromotieknevel niet na sparen** voorthield: Vaste een kwestie in het activiteit-creeer proces waar het onbruikbaar maken van de voorbevorderingsknevel in activiteitenmontages niet na besparing voorhield. Klanten die probeerden de frontbevordering te verwijderen, vonden de knevel opnieuw-toegelaten na het herzien van de activiteit, die correcte aanpassing verhinderden. Met deze update kunnen wijzigingen op betrouwbare wijze worden opgeslagen, zodat klanten de volledige controle hebben over instellingen voor speciale acties. (TGT-53215)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* **Vaste activiteit ladend en [!UICONTROL Cancel] knoopkwesties in activiteit-creeer proces**: Vaste een kwestie in activiteit-creeer proces waar bepaalde activiteiten er niet in slaagden, verlatend klanten niet tot wijzigingen kunnen toegang hebben. Bovendien reageerde de knop [!UICONTROL Cancel] niet, waardoor klanten het laadproces niet konden stoppen of de bewerkingsweergave konden verlaten. Deze correctie zorgt ervoor dat activiteiten nu betrouwbaar worden geladen en dat de knop [!UICONTROL Cancel] naar behoren functioneert, wat de algehele stabiliteit en gebruikerservaring in de Visual Experience Composer verbetert. (VEC)(TGT-53218)
* **Vaste kwestie van de ervaringsomschakeling in bijgewerkte VEC UI die het uitgeven en gehandicapten [!UICONTROL Cancel] knoop** blokkeerde: Vaste een kwestie in bijgewerkte VEC UI waar de wijzigingen ontbraken om te laden wanneer het schakelen tussen ervaringen in een Ervaring richtend (XT) activiteit. Klanten konden de ervaringen die ze oorspronkelijk hadden ingevoerd, niet bewerken en de knop [!UICONTROL Cancel] ontbreekt of reageert niet. Deze correctie zorgt ervoor dat wijzigingen nu correct worden geladen over alle ervaringen en dat de knop [!UICONTROL Cancel] betrouwbaar werkt, zelfs zonder de Helper-extensie, waardoor bewerkingsworkflows worden verbeterd en frustratie wordt verminderd. (TGT-53256)
* **Vaste witte het schermkwestie wanneer het schakelen tussen veelvoudige ervaringen in activiteit-creeer proces**: Vaste een kwestie waar het schakelen tussen veelvoudige ervaringen een wit scherm veroorzaakte. Probleem verholpen tijdens het &#39;activity-create&#39;-proces waarbij klanten een wit scherm tegenkwamen bij het wijzigen van meerdere ervaringen binnen een activiteit. Dit probleem is opgetreden nadat u wijzigingen hebt aangebracht in twee ervaringen en vervolgens een derde ervaring hebt gekozen, waardoor verdere bewerkingen zijn voorkomen. De update zorgt voor vloeiende overgangen tussen ervaringen, waardoor klanten zonder onderbreking wijzigingen kunnen aanbrengen. (TGT-53266)
* **Vaste kwestie in VEC waar de veranderingen van de douanecode niet betrouwbaar over het uitgeven zittingen** werden bewaard: Vaste een kwestie waar de wijzigingen van de douanecode die in Visuele Composer van de Ervaring (VEC) werden aangebracht niet betrouwbaar in één enkele poging werden bewaard. Klanten meldden dat wijzigingen, zoals styling updates of HTML-bewerking, periodiek ontbraken van de website en QA-URL&#39;s, zelfs nadat ze zowel de [!UICONTROL Edit Content] - als de laatste [!UICONTROL Save] -knoppen hadden gebruikt. Deze regressie is opgelost, zodat alle wijzigingen in de aangepaste code tijdens de bewerkingssessies ongewijzigd blijven.** (TGT-53418)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
