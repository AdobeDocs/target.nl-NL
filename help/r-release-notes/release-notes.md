---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: cc260620cf87feebcd4c43f45f05406ac845cf5b
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast bevat de release notities voor doel-API&#39;s, SDK&#39;s en de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021, [!DNL Adobe Target] ondersteunt de bibliotheek mbox.js niet meer. Post Maart 31, 2021, zullen alle vraag die van mbox.js wordt gemaakt zachtjes ontbreken en uw pagina&#39;s beïnvloeden die hebben [!DNL Target] activiteiten die worden uitgevoerd door het bedienen van standaardinhoud.
>
>Migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek op at.js om mogelijke problemen met uw sites te voorkomen. Zie voor meer informatie [Overzicht: Doel voor client-side web implementeren](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## at.js versie 2.7.0 (28 oktober 2021)

Deze release bevat de volgende verbeteringen:

* Extra ondersteuning voor [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). Deze versie van at.js wordt vereist om gepersonaliseerde ervaringen en aanbiedingen op douaneelementen en op elementen binnen douaneelementen tot stand te brengen en te testen. Deze functionaliteit is opgenomen in de [!DNL Target Standard/Premium] Release 21.10.5.

## [!DNL Target Standard/Premium] 21.10.5 (28 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| [!UICONTROL Visual Experience Composer] (VEC) | Extra ondersteuning voor [Webcomponenten](https://developer.mozilla.org/en-US/docs/Web/Web_Components). U kunt persoonlijke ervaringen en aanbiedingen maken en testen op aangepaste elementen en op elementen in aangepaste elementen.<br>Zie voor meer informatie [Opties voor Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#custom). |

## [!DNL Target Standard/Premium] 21.10.4 (21 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen:

| Functie | Details |
| --- | --- |
| Recommendations op basis van winkelwagentjes | Er is een nieuwe reeks algoritmen toegevoegd om aanbevelingen te doen op basis van de inhoud van het winkelwagentje van de bezoeker.<br>Zie &quot;Op winkelwagentje gebaseerd&quot; in [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md), &quot;Winkelwagentjes toevoegen/winkelwagentjes weergeven/uitchecken van pagina&#39;s&quot; en &quot;Items uitsluiten die zich al in de winkelwagentje van de bezoeker bevinden&quot; in [Recommendations plannen en implementeren](/help/c-recommendations/plan-implement.md)en op basis van winkelwagentje in [De aanbeveling baseren op een aanbevelingen](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md). |

## [!DNL Target Standard/Premium] 21.10.3 (19 oktober 2021)

Deze onderhoudrelease bevat de volgende verbeteringen, correcties en wijzigingen:

* Opgeloste problemen waardoor klanten de [!UICONTROL A4T] in [!DNL Analysis Workspace] door op de knop [!UICONTROL View in Analytics] knop in [!DNL Target] activiteitenrapportage. (TGT-42099, TGT-42100)
* Het probleem dat de oorzaak was van de [!UICONTROL Edit Design] knop niet weergeven tijdens bewerken [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die de [!UICONTROL Form-Based Experience Composer]. (TGT-41980)
* Het probleem dat ervoor zorgde dat de [!UICONTROL Compatible] selectievakje van weergave in selectie criteria tijdens het maken van een nieuwe [!UICONTROL Recommendations] activiteit. (TGT-42053)
* Probleem verholpen waarbij een foutbericht werd weergegeven dat niet kon worden geselecteerd [!DNL Analytics] als rapportagebron (A4T) wegens gebrek aan [!DNL Analytics] machtigingen. (TGT-41954)
* Geïmplementeerde veelvoudige toegankelijkheidsmoeilijke situaties om toetsenbordnavigatie over de [!DNL Target] UI.

## [!DNL Target Standard/Premium] 21.10.2 (13 oktober 2021)

De volgende verbeteringen zijn toegevoegd tijdens het gebruik [!DNL Target] [!UICONTROL Audiences] met de [!DNL Adobe Experience Platform Web SDK]:

* Er zijn waarschuwingspictogrammen, popovers en berichten toegevoegd op verschillende plaatsen in het dialoogvenster [!DNL Target] UI om aan te geven dat het publiek bij de bron is verwijderd en niet langer beschikbaar is voor gebruik in [!DNL Target] activiteiten.

   In de volgende afbeeldingen ziet u een aantal plaatsen waar de pictogrammen, popovers en berichten worden weergegeven:

   * [!UICONTROL Activity] lijstpagina

      ![Publiek verwijderd bij bronbericht op pagina Activiteiten](assets/deleted-at-source-audiences-list.png)

   * Activiteit [!UICONTROL Overview] pagina&#39;s:

      ![Publiek verwijderd bij bronbericht op overzichtspagina](assets/deleted-at-source-overview.png)

   * [!UICONTROL Experiences] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op [!UICONTROL Experiences] page](assets/deleted-at-source-experiences.png)

   * [!UICONTROL Targeting] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op [!UICONTROL Targeting] page](assets/deleted-at-source-targeting.png)

   * [!UICONTROL Goals & Settings] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op de [!UICONTROL Goals & Settings] page](assets/deleted-at-source-goals-settings.png)

   * Poortverfijningen ([!UICONTROL Replace Audience] op de [!UICONTROL Targeting] stap van de workflow voor het maken van activiteiten):

* Als u de functie Soorten publiek combineren probeert te gebruiken en een van de soorten publiek bij de bron is verwijderd, [!UICONTROL Save] is uitgeschakeld.

## [!DNL Target Standard/Premium] 21.10.1 (6 oktober 2021)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| [!UICONTROL Audiences] UI vernieuwen | Als onderdeel van het [!DNL Adobe Target] de voortdurende inspanning van het team om de gebruiker-ervaring voor te verbeteren [!DNL Target] gebruikers, deze versie vernieuwt de [!UICONTROL Audiences] en [!UICONTROL Profile Scripts] pagina&#39;s in het dialoogvenster [!DNL Target] UI. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen, zoals:<ul><li>De mogelijkheid om meerdere soorten publiek tegelijk te selecteren en te verwijderen</li><li>Een vernieuwd [ontwerp van publiek builder](/help/c-target/c-audiences/create-audience.md)</li><li>Ondersteuning voor uitsluitingsregels in het dialoogvenster [!UICONTROL Audience] bibliotheekregelbouwer</li><li>Een nieuw filter &quot;Bron publiek&quot;, waarmee u sneller uw doelgroep kunt detecteren</li><li>Opties voor permanent zoeken en filteren tijdens sessies</li></ul>Zie voor meer informatie [Soorten publiek](/help/c-target/target.md).<br>**OPMERKING**: De nieuwe [!UICONTROL Audiences] UI is beschikbaar om klanten slechts te selecteren. De update wordt vanaf januari 2022 geleidelijk aan voor alle klanten beschikbaar gesteld. |
| [!UICONTROL Profile Scripts] UI vernieuwen | De [!UICONTROL Profile Scripts] De bibliotheek is ook bijgewerkt en bevat een vernieuwde interface en diverse productiviteitsupdates:<ul><li>De mogelijkheid om meerdere profielscripts tegelijk te selecteren en te verwijderen</li><li>Een nieuwe code-editor voor profielscripts</li><li>Syntaxis markeren en fout controleren in de code-editor</li><li>Automatisch aanvullen van tokens (mbox of profiel) via sneltoetsen</li></ul>Zie voor meer informatie [Bezoekerprofielen](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**OPMERKING**: De nieuwe [!UICONTROL Profile Scripts] UI is beschikbaar om klanten slechts te selecteren. De update wordt vanaf januari 2022 geleidelijk aan voor alle klanten beschikbaar gesteld. |
| ![Premium badge](/help/assets/premium.png) Recommendations-criteria maken en bewerken | De [!UICONTROL Recommendations Criteria] de workflow voor het maken en bewerken van bestanden is gestroomlijnd om het kiezen van het juiste algoritme en de juiste instellingen voor het uitvoeren van aanbevelingen te vereenvoudigen.<br>Zie voor meer informatie [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Premium badge](/help/assets/premium.png) Verbeteringen in de snelheid van Recommendations-terugzoekvensters en -algoritmes | U kunt de algoritmen &quot;Meest bekeken&quot; en &quot;Hoogste verkopers&quot; nu uitvoeren met een terugkijkvenster van zes uur om de inhoud vast te leggen die het laatst wordt doorzocht. Wanneer het terugkijkvenster van zes uur wordt geselecteerd, worden uw aanbevelingen resultaten bijgewerkt om de 3-6 uur door de dag.<br>Zie voor meer informatie [Gegevensbron](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *Criteria maken*. |

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie voor meer informatie [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Zie voor meer informatie [Opmerkingen bij de release van vorige releases](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie voor meer informatie [Opmerkingen bij de release Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie [Opmerkingen bij de doelversie - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
