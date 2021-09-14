---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 6957eb88e2ee7d54fdad5afeaedf75b091b601e7
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 14 september 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.9.1 (14 september 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

* Problemen verholpen waardoor klanten zich niet konden aanmelden bij [!UICONTROL Visual Experience Composer] (VEC) vanwege nieuw beveiligingsbeleid voor cookies van derden in sommige webbrowsers. Dit probleem is besproken in &quot;Pagina&#39;s die niet worden geladen in Visual Experience Composer (VEC) of Enhanced Experience Composer (EEC) bij gebruik van Google Chrome versie 80+&quot; in [Problemen oplossen met betrekking tot Visual Experience Composer en Enhanced Experience Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* Probleem verholpen waarbij aanbiedingsnamen in de VEC het pad van de aanbieding weergeven in plaats van de vriendelijke naam van de aanbieding. (TGT-41300)
* Probleem verholpen in [!DNL Recommendations] waarbij wijzigingen in de entiteit-id bij een promotie in een gedupliceerde activiteit ten onrechte werden toegepast op de oorspronkelijke activiteit. (TGT-41482)
* Probleem verholpen waardoor de knop &quot;Criteria bewerken&quot; niet correct kon worden weergegeven op de pagina [!UICONTROL Experiences] voor [!DNL Recommendations]-activiteiten in de VEC. (TGT-39512)
* Probleem verholpen waarbij synchronisatie van activiteiten tijdens het dupliceren en kopiëren naar een testwerkruimte werd voorkomen. (TGT-40686)
* Probleem verholpen waarbij wijzigingen in een kiezer met [ervaringsfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md) tijdens het gebruik van &quot;[!UICONTROL Insert After]&quot; in de VEC werden voorkomen. (TGT-41802)
* Probleem verholpen waarbij lege JSON-inhoud in een aanbieding niet naar de achtergrond kon worden verzonden. [!DNL Target] verzendt nu het JSON-object, ook al is het leeg. (TGT-41555)
* Probleem verholpen waarbij rapportage [!DNL Analytics] werd geopend in plaats van [!DNL Analysis Workspace] wanneer klanten tijdens het weergeven van een rapport op &quot;[!UICONTROL View in Analytics]&quot; hadden geklikt. (TGT-41867)
* Er is extra verduidelijking toegevoegd aan het weergegeven UI-bericht wanneer een klant [!DNL Analytics] probeert te selecteren als rapportagebron (A4T) voor een [!UICONTROL Automated Personalization]-activiteit. In het bericht staat dat &quot;[!DNL Target] de enige ondersteunde bron is voor [!UICONTROL Automated Personalization]-activiteiten.&quot; (TGT-41954)
* Er is extra verduidelijking toegevoegd aan het foutbericht wanneer klanten proberen hosts te scheiden met &quot;newline&quot; in plaats van met komma&#39;s. (TGT-40671)
* Het veld [!UICONTROL Type] voor segmenten is bijgewerkt zodat [!DNL Platform] en [!DNL AAM] ([!DNL Adobe Audience Manager]) correct worden opgenomen. (TGT-41328)
* Probleem verholpen waarbij operands van verkeersbronnen werden gewijzigd nadat op [!UICONTROL Save] was geklikt. (TGT-41408)
* Nadat een activiteit-slechts publiek (of op regel-gebaseerd of gecombineerd) wordt opgeslagen, laadt UI nu [!UICONTROL Audience] plukker met toegepaste activiteit-slechts filter. (TGT-41747).
* Probleem verholpen waarbij het publiek dat uit de bron ([!DNL Adobe Experience Platform], [!UICONTROL AAM], enzovoort) werd verwijderd, verder werd weergegeven in de interface [!DNL Target].
* Er is een filteroptie toegevoegd aan de pagina [!UICONTROL Audiences] om alleen publiek weer te geven dat is geïmporteerd uit [!DNL Adobe Experience Platform]. (TGT-41298)
* Verbeterde toegankelijkheidsopties voor het toetsenbord toegevoegd in de gebruikersinterface [!UICONTROL Audiences]. (TGT-39927)
* Probleem verholpen waarbij de datums &quot;[!UICONTROL Last Updated]&quot; van sommige activiteiten verschilden van de Engelse gebruikersinterface voor Spaanse en Japanse klanten (wanneer de gebruikersinterface wordt weergegeven in het Spaans en Japans). (TGT-38980)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
