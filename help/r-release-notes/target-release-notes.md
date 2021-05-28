---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Opmerkingen bij de release
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 259f92328be9d8694740c1d7fbd342335bfd2878
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 28 mei 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## ![Adobe Experience Platform Web SDK ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] badgeversion 2.6.0 (1 juni 2021)

Deze versie van [!DNL Platform Web SDK] omvat steun voor het volgende:

| Functie | Details |
| --- | --- |
| Ondersteuning omleiden met [!UICONTROL Analytics for Target] (A4T) | De SDK van het Web van het Platform steunt nu [!DNL Target] omleidingen wanneer het gebruiken van A4T. Met omleiding van voorstellen in [!DNL Adobe Target] wordt een browser omgeleid naar een nieuwe pagina. |
| Reactietokens | De SDK van het Web van het Platform steunt nu [!DNL Target] reactietokens. Met responstokens kunt u automatisch specifieke informatie voor [!DNL Adobe Target] uitvoeren op de webpagina van uw merk. Deze informatie kan details over de activiteit, de aanbieding, de ervaring, het gebruikersprofiel, geo informatie, en meer omvatten. Deze details verstrekken extra reactiegegevens om met interne of derdesystemen te delen of voor het zuiveren te gebruiken. |

## [!DNL Target Standard/Premium] 21.5.1 (8 juni 2021)

| Functie | Details |
| --- | --- |
| ![Premium ](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL Catalog Search] badgeAPI | Zoek in uw [!DNL Recommendations] product- en inhoudscatalogus via de API programmatisch naar items die voldoen aan een zoekcriterium en vereenvoudig het beheer van uw catalogus.<br>**Beperkingen en opmerkingen**:<ul><li>Cataloguszoekopdrachten via API worden niet ondersteund voor omgevingen met meer dan 2.000.000 items.</li><li>Zoekresultaten van catalogi via API worden sneller bijgewerkt dan zoekresultaten van catalogi via de gebruikersinterface [!DNL Target]. Het zoeken naar catalogi in de interface [!DNL Target] kan extra tijd vergen om de meest recente resultaten weer te geven.</li></ul>Zie [Zoeken in entiteiten](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) in de handleiding *[!DNL Adobe Target][!DNL Recommendations] API* voor meer informatie. |

## [!DNL Target Standard/Premium] 21.5.2 (nog te bepalen datum)

Deze versie bevat de volgende nieuwe functies en verbeteringen. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

| Functie | Details |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | De volgende verbeteringen zijn van toepassing op populariteitsalgoritmen [!DNL Recommendations]:<ul><li>Er is een nieuwe optie van zes uur beschikbaar voor alle populariteit (Meest bekeken/Top Sellers)-algoritmen wanneer [!DNL Target] de gegevensbron met gedragsgegevens is. (Dit terugzoekvenster is *niet* beschikbaar wanneer [!DNL Adobe Analytics] de gegevensbron voor gedragsgegevens is.)</li><li>Als deze optie is geselecteerd, worden de volgende algoritmen ongeveer om de drie uur uitgevoerd (in plaats van om de twaalf uur).<ul><li>Meest bekeken</li><li>Meest aangeschaft</li><li>Meest bekeken op categorie</li><li>Meest gekocht per categorie</li><li>Meest weergegeven door aangepast kenmerk (met de functie groupBy)</li><li>Meest aangeschaft door aangepast kenmerk (met functie groupBy)</li></ul></ul>(TOP-1086) |

Deze versie bevat de volgende oplossingen.

* Inhoud wordt toegevoegd wanneer de releasedatum nadert.

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
