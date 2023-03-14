---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe functies en verbeteringen worden opgenomen in de komende [!DNL Target] Vrijgeven?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 2c4f5666b65bfc36885aad3907639a309e8c69f2
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 14 maart 2023**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] Standard/Premium 22.15.1 (8 en 9 maart 2023)

Deze release is beschikbaar volgens het volgende schema:

* **8 maart**: Amerikaanse regio
* **9 maart**: Europa, Midden-Oosten en Afrika (EMEA)
* **9 maart**: Regio Azië-Stille Oceaan (APAC)

>[!NOTE]
>
>Vanwege problemen die sindsdien zijn verholpen, zijn de &quot;Geoptimaliseerde A4T metriek voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]De functie &quot; die op 8 en 9 maart is uitgebracht, is tijdelijk verwijderd. Na verdere interne tests wordt de functie in de komende weken opnieuw vrijgegeven.

Deze versie bevat de volgende oplossingen:

* Updates voor het ontwerpen van aangepaste webcomponenten met de [!UICONTROL Visual Experience Composer] (VEC):

   * De Vaste de elementenselectie van de Schaduw DOM in VEC door het auteursproces te verbeteren zodat is er geen afhankelijkheid van [!DNL Target] implementatietype bij het ontwerpen van de schaduwhoofdmap. Het selecteren van Schaduw-DOM-elementen in de VEC werkt nu voor elke website.
   * Probleem opgelost waarbij het laden van HTML-elementen met #Shadow DOM in de VEC werd voorkomen. (TGT-35801)
   * VEC-problemen met SPA websites opgelost met ShadowDOM. (TGT-43169)
   * Probleem verholpen met de optimalisatiedoelstelling: &quot;clicked an element&quot; dat de CSS-kiezer niet correct identificeerde in ShadowDOM.

>[!NOTE]
>
>Zorg ervoor dat u een [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js) met een versie groter dan 2.8.

**Bekend probleem**: Klikken en volgen op een schaduwbasiselement bij gebruik [!DNL Adobe Experience Platform Web SDK] werkt niet correct. (TNT-47012)

## at.js versie 2.10.2 (7 maart 2023)

* Het probleem dat de oorzaak was van de `trackEvent` om altijd een fout te retourneren.

Voor informatie over alle versies at.js, zie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |


## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
