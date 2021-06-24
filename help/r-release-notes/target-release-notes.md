---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Opmerkingen bij de release
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b897829595ef1cdda28a995481fa1d2d5d1616f4
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 24 juni 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.6.1 (30 juni 2021)

Deze versie bevat de volgende nieuwe functies en verbeteringen. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

| Functie | Details |
| --- | --- |
| [!UICONTROL Analytics for Target] (A4T) | Wanneer u op de koppeling &quot;[!UICONTROL View in Analytics]&quot; op de pagina [!UICONTROL Reports] klikt vanuit een activiteit die [!DNL Analytics] als rapportagebron (A4T) gebruikt, wordt [!DNL Analysis Workspace] nu geopend. Eerder, opende de verbinding [!DNL Analytics] rapportering. (TGT-36959) |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | De volgende verbeteringen zijn van toepassing op populariteitsalgoritmen [!DNL Recommendations]:<ul><li>Er is een nieuwe optie van zes uur beschikbaar voor alle populariteitsalgoritmen (Meest bekeken/Top Sellers) wanneer [!DNL Target] de gegevensbron voor gedragsgegevens is. (Dit terugzoekvenster is *niet* beschikbaar wanneer [!DNL Adobe Analytics] de gegevensbron voor gedragsgegevens is.)</li><li>Als deze optie is geselecteerd, worden de volgende algoritmen ongeveer om de drie uur uitgevoerd (in plaats van om de twaalf uur).<ul><li>Meest bekeken</li><li>Meest aangeschaft</li><li>Meest bekeken op categorie</li><li>Meest gekocht per categorie</li><li>Meest weergegeven door aangepast kenmerk (met de functie groupBy)</li><li>Meest aangeschaft door aangepast kenmerk (met functie groupBy)</li></ul></ul>Releasedatum die moet worden aangekondigd. (TOP-1086) |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
