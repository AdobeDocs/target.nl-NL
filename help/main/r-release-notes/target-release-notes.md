---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 83a7fb03dcf334cb82eb507d2803e955a655b40a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 5 mei 2022**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target Standard/Premium] 22.5.1 (gespreide vrijgave; mei (10-12 mei 2022)

Deze release is beschikbaar volgens het volgende schema:

* **10 mei**: Europa, Midden-Oosten en Afrika (EMEA)
* **11 mei**: Regio Azië-Stille Oceaan (APAC)
* **12 mei**: Noord-Amerika (NA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen dat een JavaScript-fout veroorzaakte en sommige klanten de toegang tot de activiteitsgegevens voor bepaalde [!UICONTROL Automated Personalization] (AP) activiteiten. (TGT-43526)
* Probleem verholpen waardoor sommige klanten geen specifieke aanbieding aan een AP-activiteit konden toevoegen (of bewerken). (TGT-43503)
* Probleem opgelost in het dialoogvenster [!DNL Target] UI die het volgende foutenbericht toonde: &quot;Uw globale box is mogelijk niet synchroon. Probeer het opnieuw op te slaan.&quot; Dit probleem betrof een UI-probleem en had geen invloed op de implementaties van klanten. (TGT-43475)
* Probleem verholpen waardoor één klant geen verfijningen en publiek op ervaringsniveau kon bewerken voor een activiteit als de verfijningen en het publiek vóór de nieuwe [!UICONTROL Audiences] UI is geïmplementeerd. (TGT-43433)
* Het probleem waarbij klanten dubbele gegevens konden selecteren, is opgelost. [!DNL Adobe Audience Manager] (AAM) publiek tijdens het bewerken van het rapportagepubliek voor een activiteit. (TGT-43430)
* Probleem verholpen waardoor klanten geen dubbel publiek konden maken, maar in verschillende werkruimten. (TGT-43423)
* Probleem verholpen waardoor klanten geen locaties konden verwijderen die ad-hocaanbiedingen hadden in activiteiten die in het dialoogvenster [!UICONTROL Form-Based Experience Composer]. (TGT-43315)
* Probleem verholpen waarbij klanten geen toegang kregen tot de aangeboden code nadat ze op de aanbiedingen voor afbeeldingen hadden geklikt en de interface vervolgens hadden vernieuwd. (TGT-43566)
* Zorgde ervoor dat de lijst van metriek beschikbaar in [!DNL Target] UI wanneer het creëren van activiteiten die gebruiken [!DNL Analytics for Target] (A4T) geeft alleen die metriek weer die zijn verzameld door [!DNL Adobe Analytics]. (TGT-43294)
* Probleem verholpen dat soms veroorzaakte [!UICONTROL Setup] paginaverzoeken om te mislukken. Als u bijvoorbeeld &quot;[!UICONTROL Reporting Experience Cloud Solution]&quot; van &quot;[!UICONTROL Analytics]&quot; in &quot;[!UICONTROL Target]&quot; of &quot;[!UICONTROL Select per Activity]&quot;. (TGT-43272)
* Probleem opgelost waarbij wijzigingen in profielscripts soms niet correct werden bijgewerkt. (TGT-43249)
* Probleem verholpen waarbij de volgende fout is opgetreden bij een poging een publiek naar een andere werkruimte te verplaatsen: &quot;We kunnen je aanvraag niet voltooien. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-43212)
* Correctie van een fout die een fout veroorzaakte bij het klonen van aangepaste codewijzigingen voor App-pagina&#39;s (SPA) van één pagina. (TGT-43137)
* Veranderd de manier waarop metrisch met &quot;paginaweergaven&quot;in SPA wordt behandeld. In plaats van de pagina-URL weer te geven in het dialoogvenster [!DNL Target] UI, toont nu UI &quot;mening.&quot; (TGT-41200)
* Probleem verholpen waarbij de oorspronkelijke aanbieding werd beïnvloed nadat een ervaring was gedupliceerd en de promotie vervolgens was bewerkt. (TGT-41775)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
