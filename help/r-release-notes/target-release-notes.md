---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 14 januari 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Target Standard/Premium 21.1.1 (19 januari 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

* Er is een waarschuwing toegevoegd bij het selecteren van een [!DNL Adobe Analytics]-meting bij gebruik van [!UICONTROL Analytics as the reporting source] (A4T) in een [!UICONTROL Auto-Target]-activiteit. [!UICONTROL Auto-Target] modellen zijn geoptimaliseerd om met binaire (op omzetting-gebaseerde) metriek te werken. Het selecteren van ononderbroken metrisch, zoals opbrengst, zou suboptimale resultaten kunnen hebben en de [!UICONTROL Personalization Insights] rapporten zouden niet nauwkeurig kunnen zijn. (TGT-38926)
* Er is een statuspictogram toegevoegd in het [!UICONTROL Auto-Target Summary]-rapport voor [!UICONTROL Auto-Target]-activiteiten die gebruikmaken van A4T. Het groene controlepictogram naast elke ervaring in het rapport geeft aan dat er een gepersonaliseerd model voor machinaal leren is gegenereerd voor die ervaring. Het klokpictogram wijst erop dat niet genoeg verkeer is gediend om het model te bouwen. (TGT-38925)
* De [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] rapporteren voor [!UICONTROL Auto-Target] activiteiten die A4T en [!DNL Analytics] omzettingsmetriek gebruiken worden geproduceerd en kijken het zelfde als wanneer het gebruiken van [!DNL Target] als rapporteringsbron. (TGT-38931)
* Een omgevingsfilteroptie toegevoegd aan de lijst [!UICONTROL Recommendations] [!UICONTROL Collections]. (TGT-38353)
* Probleem verholpen waarbij het onjuiste aantal producten in verzamelingen [!UICONTROL Recommendations] werd weergegeven. (TGT-39162)
* Filter [!UICONTROL Last Updated] toegevoegd aan [!UICONTROL Recommendations] [!UICONTROL Catalog Search]. (TGT-38340)
* Probleem verholpen in [!UICONTROL Recommendations] dat ertoe leidde dat de pagina [!UICONTROL Create Sequence] vastliep nadat de verticale branche was gewijzigd. (TGT-38160)
* Probleem verholpen waardoor de activiteit niet kon worden opgeslagen als Device Co-op was ingeschakeld en de gebruiker van [!DNL Target] als rapportbron veranderde in [!DNL Analytics] (A4T). (TGT-38163)
* Probleem verholpen waardoor gebruikers een publiek niet konden verwijderen uit een aanbieding in een activiteit [!UICONTROL Automated Personalization] (AP). (TGT-39058)
* Probleem verholpen waarbij het onjuiste tijdframe (begin- en einddatum) voor sommige klanten werd weergegeven in [!UICONTROL Audience Info]-kaarten. (TGT-39150)
* Probleem verholpen waardoor sommige klanten de lijst met activiteiten in [!UICONTROL Default Workspace] niet konden zien. (TGT-38526)

## Voorlopige-releasegegevens {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
