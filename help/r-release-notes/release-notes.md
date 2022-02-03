---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5d3e5a15a262d29bd1d95af71baae52ed288b33e
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast bevat de release notities voor doel-API&#39;s, SDK&#39;s en de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## Target Standard/Premium 22.2.1 (1 februari 2022)

Deze onderhoudsversie bevat de volgende oplossingen en verbeteringen voor de nieuwe [!UICONTROL Audiences] UI die in de Versie van het Doel Standard/Premium 22.1.2 wordt aangekondigd die aan klanten over alle gebieden in de volgende zes weken uitrolt. Met deze correcties lijnt u de functionaliteit uit van publiek dat is gemaakt in [!DNL Adobe Target Standard/Premium].

* Probleem verholpen waarbij geïmporteerd publiek werd verhinderd [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud], en [!DNL Adobe Target Classic] worden toegewezen als rapportagepubliek. (TGT-43140)
* Toegevoegde [!UICONTROL Delete] in de [!UICONTROL Audiences] lijst voor geïmporteerde soorten publiek uit [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud], en [!DNL Adobe Target Classic]. Ook functionaliteit voor bulksgewijs verwijderen toegevoegd. (TGT-42914)

## at.js versie 2.8.1 (28 januari 2022)

* Vast `pageLoad` niet toegewezen aan target-global-mbox in [!UICONTROL On Device Decisioning] (ODD) hybride uitvoeringsmodus.
* Probleem verholpen met analytische details voor mbox-aanvraag.
* Verbeterde dev-afhankelijkheden om beveiligingskwetsbaarheden te verhelpen.

## [!DNL Target Standard/Premium] 22.1.2 (26 januari 2022)

| Functie | Details |
| --- | --- |
| [!DNL Adobe Experience Platform] publiek in [!DNL Target] | U kunt nu consumeren en gebruiken [!DNL Adobe Experience Platform] publiek in [!DNL Target]. De [!DNL Target] team, [!DNL Experience Platform] [!DNL Destinations] en de [!DNL Unified Profile Service] -team is verheugd de algemene beschikbaarheid van de gebruiksgevallen &quot;Zelfde pagina/Volgende pagina aanpassen&quot; aan te kondigen.<br>Het publiek gebruiken dat is gemaakt in [!DNL Adobe Experience Platform] Verstrek rijkere klantengegevens die tot uitvoerigere verpersoonlijking leiden. De [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), gebouwd op [!DNL Adobe Experience Platform] helpt bedrijven bekende en anonieme gegevens van veelvoudige ondernemingsbronnen samenbrengen om klantenprofielen tot stand te brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in real time te verstrekken.<br>Zie voor meer informatie [Soorten publiek uit Adobe Experience Platform gebruiken](/help/c-target/c-audiences/audiences.md#aep) in *Soorten publiek maken* en [Gebruiksgevallen voor personalisatie op dezelfde pagina en op de volgende pagina](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} in het dialoogvenster *Overzicht van doelen* hulplijn. |
| [!UICONTROL Audiences] UI vernieuwen | Als onderdeel van het [!DNL Adobe Target] de voortdurende inspanning van het team om de gebruiker-ervaring voor te verbeteren [!DNL Target] gebruikers, deze versie vernieuwt de [!UICONTROL Audiences] en [!UICONTROL Profile Scripts] pagina&#39;s in het dialoogvenster [!DNL Target] UI. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen, zoals:<ul><li>De mogelijkheid om meerdere soorten publiek tegelijk te selecteren en te verwijderen</li><li>Een vernieuwd [ontwerp van publiek builder](/help/c-target/c-audiences/create-audience.md)</li><li>Ondersteuning voor uitsluitingsregels in het dialoogvenster [!UICONTROL Audience] bibliotheekregelbouwer</li><li>Een nieuw filter &quot;Bron publiek&quot;, waarmee u sneller uw doelgroep kunt detecteren</li><li>Opties voor permanent zoeken en filteren tijdens sessies</li><li>De mogelijkheid om het publiek tussen werkruimten te verplaatsen voor [!DNL Target Premium] klanten.</li></ul>Zie voor meer informatie [Soorten publiek](/help/c-target/target.md).<br>**OPMERKING**: Deze functie wordt de komende acht weken uitgerold naar klanten in verschillende regio&#39;s. |
| [!UICONTROL Profile Scripts] UI vernieuwen | De [!UICONTROL Profile Scripts] De bibliotheek is ook bijgewerkt en bevat een vernieuwde interface en diverse productiviteitsupdates:<ul><li>De mogelijkheid om meerdere profielscripts tegelijk te selecteren en te verwijderen</li><li>Een nieuwe code-editor voor profielscripts</li><li>Syntaxis markeren en fout controleren in de code-editor</li><li>Automatisch aanvullen van tokens (mbox of profiel) via sneltoetsen</li></ul>Zie voor meer informatie [Bezoekerprofielen](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**OPMERKING**: Deze functie wordt de komende acht weken uitgerold naar klanten in verschillende regio&#39;s. |

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
