---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die in de komende release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe functies en verbeteringen worden opgenomen in de komende [!DNL Target] Vrijgeven?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 2f553151e480d48178389132a0a97fa7de4e04c5
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor volgende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 22 mei 2023**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] Standard/Premium 23.5.1 (23-25 mei 2023)

Deze release is beschikbaar volgens het volgende schema:

23 mei: Europa, Midden-Oosten en Afrika (EMEA) 24 mei: Regio Azië-Stille Oceaan (APAC) 25 mei: Amerikaanse regio

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
|--- |--- |
| Real-Time CDP-profielkenmerken die worden gedeeld met [!DNL Target] | [!UICONTROL Real-Time CDP Profile Attributes] kan worden gedeeld met [!DNL Target] voor gebruik in HTML- en JSON-aanbiedingen.<P>Zie voor meer informatie [Real-Time CDP-profielkenmerken delen met [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes). |

* Probleem verholpen waardoor bepaalde klanten geen publiek konden maken met bezoekersprofielen met de operatoren &quot;groter dan&quot; of &quot;kleiner dan&quot;. (TGT-45271)

## [!DNL Target] Standard/Premium 23.5.2 (31 mei 2023)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen waarbij een lege pagina werd weergegeven terwijl een API-autorisatietoken voor profielen werd gegenereerd. (TGT-45387)
* Probleem verholpen waarbij een afbeelding niet kon worden weergegeven in het dialoogvenster [!UICONTROL Create Design] als de afbeeldingsnaam 18030 GB tekens bevat. (TGT-44614)
* Probleem verholpen waarbij rapporten werden gegenereerd voor [!UICONTROL Auto Personalization] activiteiten om tijdens de analyse te bevriezen. (TGT-44820)
* Probleem verholpen waarbij geen activiteiten werden weergegeven in de interface Doel voor de werkruimte Standaard voor bepaalde klanten. (TGT-45286)
* De werking van de markering Duplicaten niet toestaan is bijgewerkt. Markten voor uitgesloten herhalingsaanbiedingen worden bijgewerkt om herhalende aanbiedingen toe te staan als deze de standaardinhoudsaanbieding zijn (voor API&#39;s v3, v4) en om dubbele opties toe te staan als de opties verwijzen naar de standaardinhoudsaanbieding en geen sjablonen hebben gedefinieerd. (TNT-46617)
* Probleem verholpen waarin een vraagparameter aan een URL werd toegevoegd die de pagina verhinderde in Visuele Composer van de Ervaring (VEC) te laden. (TGT-44873)
* Probleem verholpen waarbij sommige tekens in een ervarende taal onjuist werden beschermd tegen tekst/HTML. (TGT-44600)

## [!DNL Target] Standard/Premium 23.5.3 (nog te bepalen datum)

Deze release bevat de volgende verbeteringen:

| Functie | Details |
|--- |--- |
| [!UICONTROL QA mode] for [!UICONTROL Automated Personalization] activiteiten | [!DNL Adobe Target] [!UICONTROL QA mode] is nu beschikbaar voor [!UICONTROL Automated Personalization] activiteiten, vervangen [!UICONTROL Preview links] functionaliteit.<P>Zie voor meer informatie [Activiteit QA](/help/main/c-activities/c-activity-qa/activity-qa.md). |

* Prestatieverbeteringen om de functionaliteit van duplicaten (waaronder een kortere laadtijd) uit te schakelen [uitsluitingen beheren](/help/main/c-activities/t-automated-personalization/managing-exclusions.md#concept_4EF78013F80E48EFA024AE0274C9F037) in [!UICONTROL Automated Personalization] activiteiten.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
