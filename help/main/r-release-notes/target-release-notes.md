---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cd25bda52b7a1b916a73ca5e531a7134ba8cef4e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**laatst bijgewerkt: 17 april, 2025**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel ](release-notes.md). [ De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.4.4 (17 april 2025)

Deze release bevat de volgende correcties en updates:

* Er is een foutbericht toegevoegd om gebruikers te begeleiden bij het oplossen van dubbele opties in een activiteit. (TGT-51927)
* Correctie van een probleem waarbij `ClickTrack` kiezers niet werden verwijderd wanneer ze pagina&#39;s of ervaringen met omleidingsvoorstellen verwijderden. (TGT-51952)
* Probleem verholpen dat werd veroorzaakt door het toestaan van lege `ClickTrack` kiezers. [!DNL Target] vereist nu dat het selectieveld niet leeg is. (TGT-52107)
* Probleem verholpen waarbij metrische gegevens met dubbele namen onjuist werden toegestaan. Metriek vereist nu unieke namen. (TGT-52201)
* Probleem verholpen waarbij publieksdefinities niet zichtbaar waren tijdens het bewerken van doelwitten op aanbiedingsniveau in [!UICONTROL Automated Personalization] (AP)-activiteiten. (TGT-52148)
* Probleem verholpen waardoor klanten met [!UICONTROL Editor] -rechten geen activiteiten konden opslaan. (TGT-5227)
* `OptionLocalIDs` wordt niet meer verkeerd verhoogd wanneer de optie ongewijzigd blijft. (TGT-52139)
* Probleem verholpen waarbij het bericht &#39;Invalid `optionLocalIds`&#39; werd gegenereerd bij het maken van een activiteit. (TGT-52154)
* De discrepanties tussen de definitie van `OptionLocalIDs` voor een activiteit en de definitie van ervaringen zijn gecorrigeerd. (TGT-52215)
* Probleem verholpen dat een validatiefout veroorzaakte die optrad bij het maken van een A/B-activiteit. (TGT-51923)

## Update voor doelmachtigingen (22 april 2025)

Deze toekomstige update verbetert de organisatorische controle over [!DNL Target] instantieconfiguraties, die toevallige updates verhinderen die activiteitenlevering over diverse test en verpersoonlijkingsteams zouden kunnen beïnvloeden.

Vanaf 22 april 2025 kunnen alleen [!UICONTROL Product] - en [!UICONTROL Solutions] -beheerders instellingen in de [!UICONTROL Administration] -secties bijwerken, ongeacht hun rollen in [!DNL Target] -werkruimten. Gebruikers zonder deze machtiging hebben alleen-lezen toegang tot de secties van [!UICONTROL Administration] .

Voor meer informatie, zie [ Doel beheren ](/help/main/administrating-target/start-target.md).

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
