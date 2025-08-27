---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cc0bf794e366f304b52db309d4e3a66292d7ea32
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 27 augustus 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd. De informatie in dit artikel wordt regelmatig bijgewerkt, vooral vóór versies.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.8.4 (1 september 2025)

Deze release bevat de volgende updates en oplossingen:

**[!UICONTROL Activities]**

+++Zie details
* **Klanten konden activiteit of documentnamen van[!UICONTROL Activity Overview]** niet kopiëren: Eerder, konden de klanten niet de naam van een activiteit of de bijbehorende aanbieding/document direct van [!UICONTROL Activity Overview] in het bijgewerkte activiteit-creeer proces kopiëren. Deze beperking beïnvloedde de bruikbaarheid, vooral op kleinere schermen. Klanten kunnen nu gemakkelijk zowel activiteit- als documentnamen kopiëren zonder tijdelijke oplossingen. (TGT-51850)
* **Proactieve opname van gebogen [!DNL Target] klantengegevens tijdens activiteitenverwezenlijking**: Verbeter de activiteit-creeer proces door de pro-actieve inzameling van rapporten, inhoud, en screenshots van [!DNL Target] klanten toe te laten. Deze verbetering verhelpt gegevenshiaten die in bestaande gebruiksgevallen worden geïdentificeerd en helpt nauwkeurigere inzichten tijdens activiteit en experimenteeropstelling te verzekeren. (TGT-52415)

+++

**[!UICONTROL Recommendations]**

+++Zie details
* **lijst van het Product was niet zichtbaar in de [!UICONTROL View Collection] dialoog:** Eerder, konden de klanten niet de productlijst zien wanneer het bekijken van een inzameling in [!UICONTROL Recommendations] tabel. In het dialoogvenster [!UICONTROL View Collection] worden nu correct de bijbehorende producten weergegeven, waardoor de transparantie en bruikbaarheid in de bijgewerkte gebruikersinterface van Aanbevelingen worden verbeterd. (TGT-50531)
* **Vaste een kwestie die case-sensitive het filtreren in [!UICONTROL Product Catalog Search] geavanceerde onderzoek** veroorzaakte: Het geavanceerde onderzoek het filtreren in de [!UICONTROL Product Catalog Search] pagina negeert nu correct casegevoeligheid, die op het gedrag van zowel de backend als de diensten van GraphQL richt. Deze update zorgt voor consistente en nauwkeurige resultaten voor suggesties voor klanten, ongeacht de tekstbehuizing. (TGT-53585)

+++

**[!UICONTROL Reports]**

+++Zie details
* **de Rapporten slaagden er niet in om voor het publiek van de Desktop wegens een ongeldige fout van de publieksnaam** te laden: De klanten ontmoetten een fout van GraphQL toen het proberen om rapporten voor één publiek in activiteit-creeer proces te bekijken. Het systeem heeft een bericht &quot;Invalid publieksnaam: XXXXX&quot; geretourneerd, waardoor toegang tot rapportgegevens wordt voorkomen. Rapporten worden nu correct geladen voor het desktoppubliek. (TGT-53371)

+++

**[!UICONTROL Visual Experience Composer] (VEC)**

+++Zie details
* **klikkend &quot;Accept Cookies&quot;gebruikend [!UICONTROL Enhanced Experience Composer] (EEG) ontbroken toe te schrijven aan een ontbrekende functie**: De klanten rapporteerden dat het proberen om koekjes via EEG goed te keuren in een consolefout resulteerde: `handleclickAcceptAllButton is not defined`. De functionaliteit voor het accepteren van cookies werkt nu zoals u had verwacht en zorgt voor een vloeiender ervaring tijdens het maken van activiteiten in de bijgewerkte gebruikersinterface. (TGT-52794)
* **Nieuwe E.E.G. UI slaagde er niet in om bepaalde pagina&#39;s te laden die eerder in erfenis UI** werden gesteund: De klanten rapporteerden dat nieuwe EEG sommige pagina&#39;s niet kon laden, die in erfenis UI ondanks iframe-het bouwen code aanwezig op de plaats toegankelijk waren. Het bijgewerkte activity-create proces ondersteunt nu het laden van deze pagina&#39;s en het herstellen van compatibiliteit voor workflows voor het maken van activiteiten. (TGT-53061)
* **VEC toonde een leeg wit scherm wanneer het uitgeven van ervaringen**: De klanten van een bepaalde huurder rapporteerden dat het scherm VEC leeg ging wanneer het proberen om ervaringen in bijgewerkte VEC uit te geven. Deze kwestie beïnvloedde zowel nieuw gecreëerde als oudere activiteiten, die werkschemacontinuïteit verhinderen. VEC laadt nu correct, toestaand klanten om ervaringen zonder onderbreking uit te geven. (TGT-53547)
* **VEC crashte en toonde een leeg scherm wanneer het laden van bepaalde activiteiten**: De klanten van een bepaalde huurder rapporteerden dat VEC er niet in slaagde om specifieke activiteiten te laden. De ervaringseditor bleef vastzitten op &quot;Aanvankelijke wijzigingen toepassen&quot; voordat deze vastliep en een leeg scherm weergaf. Consolefouten duiden op een fout bij het lezen van niet-gedefinieerde eigenschappen. De redacteur laadt nu betrokken activiteiten zonder fouten in bijgewerkte VEC. (TGT-53548)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
