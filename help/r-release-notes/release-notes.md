---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en bibliotheken JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 53a7bd5bb258f2f12f68d3b4cfdfc77d5519c913
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard]- en [!DNL Target Premium]-versie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, [!DNL Adobe Experience Platform Web SDK], at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## [!DNL Target Standard/Premium] 21.10.2 (13 oktober 2021)

De volgende verbeteringen zijn toegevoegd bij het gebruik van [!DNL Target] [!UICONTROL Audiences] met [!DNL Adobe Experience Platform Web SDK]:

* Toegevoegde waarschuwingspictogrammen, popovers, en berichten op diverse plaatsen in [!DNL Target] UI om erop te wijzen dat het publiek bij de bron werd geschrapt en niet meer voor gebruik in [!DNL Target] activiteiten beschikbaar is.

   In de volgende afbeeldingen ziet u een aantal plaatsen waar de pictogrammen, popovers en berichten worden weergegeven:

   * [!UICONTROL Activity] lijstpagina

      ![Publiek verwijderd bij bronbericht op pagina Activiteiten](assets/deleted-at-source-audiences-list.png)

   * Pagina&#39;s van activiteit [!UICONTROL Overview]:

      ![Publiek verwijderd bij bronbericht op overzichtspagina](assets/deleted-at-source-overview.png)

   * [!UICONTROL Experiences] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op  [!UICONTROL Experiences] pagina](assets/deleted-at-source-experiences.png)

   * [!UICONTROL Targeting] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op  [!UICONTROL Targeting] pagina](assets/deleted-at-source-targeting.png)

   * [!UICONTROL Goals & Settings] stap van de workflow voor het maken van activiteiten:

      ![Publiek verwijderd bij bronbericht op de  [!UICONTROL Goals & Settings] pagina](assets/deleted-at-source-goals-settings.png)

   * Poortverfijningen ([!UICONTROL Replace Audience] in de stap [!UICONTROL Targeting] van de workflow voor het maken van activiteiten):

* Als u de functie Soorten publiek combineren probeert te gebruiken en een van de soorten publiek bij de bron is verwijderd, wordt [!UICONTROL Save] uitgeschakeld.

## [!DNL Target Standard/Premium] 21.10.1 (6 oktober 2021)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| [!UICONTROL Audiences] UI vernieuwen | Als onderdeel van de voortdurende inspanningen van het [!DNL Adobe Target]-team om de gebruikerservaring voor [!DNL Target]-gebruikers te verbeteren, vernieuwt deze release de [!UICONTROL Audiences]- en [!UICONTROL Profile Scripts]-pagina&#39;s in de [!DNL Target]-interface. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen, zoals:<ul><li>De mogelijkheid om meerdere soorten publiek tegelijk te selecteren en te verwijderen</li><li>Een vernieuwd [ontwerp voor publieksbuilder](/help/c-target/c-audiences/create-audience.md)</li><li>De regelsteun van de uitsluiting in [!UICONTROL Audience] de bouwer van de bibliotheekregel</li><li>Een nieuw filter &quot;Bron publiek&quot;, waarmee u sneller uw doelgroep kunt detecteren</li><li>Opties voor permanent zoeken en filteren tijdens sessies</li></ul>Zie [Soorten publiek](/help/c-target/target.md) voor meer informatie. |
| [!UICONTROL Profile Scripts] UI vernieuwen | De bibliotheek [!UICONTROL Profile Scripts] is ook bijgewerkt en bevat een vernieuwde interface en diverse productiviteitsupdates:<ul><li>De mogelijkheid om meerdere profielscripts tegelijk te selecteren en te verwijderen</li><li>Een nieuwe code-editor voor profielscripts</li><li>Syntaxis markeren en fout controleren in de code-editor</li><li>Automatisch aanvullen van tokens (mbox of profiel) via sneltoetsen</li></ul>Zie [Bezoekersprofielen](/help/c-target/c-visitor-profile/visitor-profile.md) voor meer informatie. |
| ![Criteria voor ](/help/assets/premium.png) het maken en bewerken van premiumbadgeRecommendations | De workflow voor het maken en bewerken van [!UICONTROL Recommendations Criteria] is gestroomlijnd en eenvoudiger om het juiste algoritme en de juiste instellingen voor aanbevelingen te kiezen om uw doelen te bereiken.<br>Zie  [Criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md) maken voor meer informatie. |
| ![Premium ](/help/assets/premium.png) badgeRecommendations lookback window en algoritme verfrissen tariefverbeteringen | U kunt de algoritmen &quot;Meest bekeken&quot; en &quot;Hoogste verkopers&quot; nu uitvoeren met een terugkijkvenster van zes uur om de inhoud vast te leggen die het laatst wordt doorzocht. Wanneer het terugkijkvenster van zes uur wordt geselecteerd, worden uw aanbevelingen resultaten bijgewerkt om de 3-6 uur door de dag.<br>Zie  [Gegevensbron in criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source)   ** maken voor meer informatie. |

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
