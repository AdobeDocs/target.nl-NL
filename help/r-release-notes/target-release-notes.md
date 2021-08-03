---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Opmerkingen bij de release
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 113e4627d491ea10192359c755dba29fc92e8e22
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 3 augustus 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.8.1 (4 augustus 2021)

Deze onderhoudsversie bevat vele achterste verbeteringen, waaronder de volgende klantgerichte wijziging:

* Probleem verholpen waarbij rapporten werden gegenereerd voor [!UICONTROL Auto Personalization]-activiteiten die zijn gemaakt in [!UICONTROL Form-Based Experience Composer] om te verwijzen naar verwijderde aanbiedingen in rapporten. Dit gaf het volgende foutenbericht aan vertoning toe, &quot;wij hebben probleem het terugwinnen van gegevens voor dit rapport. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-41028)

## Doelleverings-API (te bepalen datum)

Deze release bevat de volgende verbeteringen:

* De limiet voor mbox-parameters is verhoogd tot 100 parameters. De vorige limiet was 50 parameters. (TNT-41717)
* De limiet voor `categoryId` is verhoogd tot 256 tekens. De vorige limiet was 128 tekens.
* De volgende [!DNL Adobe Audience Manager] (AAM) details zijn toegevoegd aan de leverings-API:

   * UUID AAM (unieke gebruikersnaam van Adobe Audience Manager)
   * dataPartnerId
   * dataPartnerUserId

   Eerder bevatte de leverings-API alleen `dcsLocationHint` en `blob`. (TNT-41644)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
