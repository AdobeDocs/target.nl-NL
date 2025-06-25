---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c882a5eb6530f3b3fe44484ee580beadeddaae23
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 25 juni 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [&#128279;](release-notes.md).
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.6.4 (26 juni 2025)

Deze release bevat de volgende correcties en updates:

* De optie [!UICONTROL Rearrange] is toegevoegd aan de bijgewerkte interface van [!UICONTROL Visual Experience Composer] (VEC), zodat deze kan worden uitgelijnd met de functionaliteit die beschikbaar is in de oudere VEC. (TGT-46957 &amp; TGT-52876)
* Correctie van een probleem waarbij wijzigingen die zijn aangebracht in ervaringen met varianten (bijvoorbeeld Experience B) in een [!UICONTROL A/B Test] -activiteit niet werden behouden. Na omschakeling tussen ervaringen, zouden de veranderingen in de variant verdwijnen. Dit probleem had geen invloed op de ervaring met controle. (TGT-52664)
* Probleem verholpen waarbij bepaalde klanten geen activiteiten konden maken of opslaan, terwijl andere klanten dezelfde acties zonder problemen konden uitvoeren. Het probleem was inconsistent tussen de accounts.(TGT-52842)
* Oplossing voor een null pointer-uitzondering die optrad bij het ophalen van rapportgegevens voor [!UICONTROL Automated Personalization] (AP)-activiteiten. (TGT-52362)
* Probleem verholpen waarbij details op aanbiedingsniveau niet konden worden weergegeven in het CSV-bestand voor [!UICONTROL Automated Personalization] (AP)-activiteiten. (TGT-52675)
* Wanneer het toepassen van wijzigingen in bijgewerkte VEC, verschijnen de veranderingen aanvankelijk correct, met inbegrip van verwachte [!UICONTROL Experience Fragment]. Nochtans, na omschakelingservaringen of het aanbrengen van extra uitgeeft, ontbreken sommige veranderingen om toe te passen toe te schrijven aan selecteurkwesties. (TGT-52679)
* Probleem verholpen waarbij de pagina-URL&#39;s van de oorspronkelijke activiteit niet werden behouden wanneer een nieuwe activiteit werd gemaakt door een bestaande activiteit te klonen. Dit probleem is nu opgelost. (TGT-52775)
* Probleem opgelost waarbij [!UICONTROL On-device Decisioning] per ongeluk niet beschikbaar was in de bijgewerkte VEC. (TGT-52371)
* Probleem verholpen waarbij het bewerken van een product [!DNL Recommendations] -activiteit werd verhinderd. Wanneer u via de doelinterface toegang probeert te krijgen tot de VEC, verschijnt er een fout op de pagina [!UICONTROL Overview] , waardoor bewerkingen worden voorkomen. (TGT-52823)
* Probleem verholpen waarbij het opslaan van een [!DNL Recommendations] -activiteit werd voorkomen wanneer namen langer dan 50 tekens voorkomen. (TGT-52619)
* Probleem verholpen waarbij klanten geen activiteit met aanbevelingen konden opslaan nadat ze de criteria in de nieuwe gebruikersinterface hadden gewijzigd. De kwestie lijkt op toestemming-verwant te zijn en beïnvloedt niet alle gebruikers met gelijkaardige rollen. (TGT-52816)
* Probleem verholpen waarbij gebruikers met de rol [!UICONTROL Editor] een [!DNL Recommendations] -activiteit niet konden bewerken. Het proberen om het ontwerp te veranderen en de activiteit te bewaren resulteerde in een 403 Verboden fout, verklarend dat &quot;[ redacteur ]&quot;voorrecht werd vereist, alhoewel de gebruiker reeds die rol in de relevante werkruimte had. (TGT-52836)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
