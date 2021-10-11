---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: f6efc1e921535abdd11501979d6f44e84e443a1f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 11 oktober 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

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

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
