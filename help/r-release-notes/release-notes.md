---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige versie van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de huidige Versie?
feature: Opmerkingen bij de release
translation-type: tm+mt
source-git-commit: 9155c487ed078f8af493755a2b4f067eafc8ae68
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard]- en [!DNL Target Premium]-versie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer vóór deze datum naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].)

## IP adresveranderingen voor de server van Recommendations feed-processing (16 maart 2021)

De IP-adressen van de [!DNL Target Recommendations]-server voor verwerking van bestandsgegevens zijn bijgewerkt op 16 maart 2021. Zie [IP-adressen die worden gebruikt door Recommendations-feed-processing-servers](/help/c-recommendations/c-recommendations-faq/ip-addresses-marketing-cloud.md) voor meer informatie.

## Target Standard/Premium 21.2.1 (9 maart 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

* De toegestane aanbiedingsgrootte is vergroot (TGT-38304):

   | Type | Vorige limiet | Nieuwe limiet |
   | --- | --- | --- |
   | HTML | 256 kB | 1024 kB |
   | Visuele aanbiedingen van het Doel UI | 64 kB | 1024 kB voor elke ervaring |
   | Via API | 512 kB | 1024 kB |

* [!UICONTROL Personalization Insights] Er worden nu dagelijks rapporten voor  [!UICONTROL Auto-Target] (AT)- en  [!UICONTROL Automated Personalization] (AP)-activiteiten opgesteld. U kunt een rapport kiezen dat [!UICONTROL Automated Segments] of [!UICONTROL Important Attributes] voor de laatste 15, 30, en 60 dagen verstrekt. De opties van 45 dagen en 90 dagen zijn verwijderd om de andere montages van het terugkijkvenster toe te laten om dagelijks te lopen. (TGT-39472)
* Probleem verholpen waarbij de huidige afhankelijkheid niet werd weergegeven wanneer klanten [!UICONTROL Edit Dependency] op de pagina [!UICONTROL Goals & Settings] van een activiteit klikken. (TGT-39340)
* Probleem verholpen bij het vernieuwen van de [!UICONTROL Audience Library] van een werkruimte. Vóór verfrist zich, toont het publiek voor de momenteel geselecteerde werkruimte. Na verfrissen, [!UICONTROL Default Workspace] en zijn publiek getoond. De huidige werkruimte en het publiek blijven nu behouden na het vernieuwen. (TGT-38871)
* Probleem verholpen bij het kopiëren van een [!UICONTROL Recommendations]-activiteit en later het bewerken van de oorspronkelijke activiteit door de volgorde van criteria te wijzigen. De wijziging in de volgorde van criteria in de oorspronkelijke activiteit werd ook onjuist toegepast op de gekopieerde activiteit. (TGT-39155)
* Probleem verholpen waarbij het onjuiste aantal producten voor uitsluitingen [!UICONTROL Recommendations] werd weergegeven. (TGT-39599)

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Voorlopige-releasegegevens {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
