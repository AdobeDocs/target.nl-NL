---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die in de komende release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe functies en verbeteringen worden opgenomen in de komende [!DNL Target] Vrijgeven?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b0bdb7d5004af73c6dff8323266ea4c58972fd80
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor volgende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 15 september 2023**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] Standard/Premium 23.9.3 (18 september 2023)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Verbeterde het [!UICONTROL Visual Experience Composer] (VEC) ter ondersteuning van Lightning DOM (Web Components). (TGT-45422)
* Probleem opgelost waarbij VEC-handelingen in de onjuiste volgorde werden toegepast. In sommige gevallen paste VEC sommige wijzigingen asynchroon toe en het toevoegen van extra aanpassingen aan een element veroorzaakte fouten als dat element na een [!UICONTROL Insert] handeling. (TGT-45983)
* Probleem opgelost met VEC [!UICONTROL Overlay] -functie, die nu elementen in DOM&#39;s met schaduw ondersteunt. (TGT-45202 &amp; TGT-45262)
* Probleem verholpen bij het openen van een toepassingspagina voor één pagina (SPA) in de VEC en vervolgens naar [!UICONTROL Browse] De modus voor de pijlen Vorige en Volgende functioneren niet correct. (TGT-45956)
* Probleem verholpen waardoor sommige webpagina&#39;s niet in de VEC konden worden geladen. (TGT-45983)

## [!DNL Target] Standard/Premium 23.9.2 (12-14 september 2023)

Deze release is beschikbaar volgens het volgende schema voor gefaseerde installatie:

* **12 september**: Amerikaanse regio
* **13 september**: regio Azië-Stille Oceaan (APAC)
* **14 september** Betreft: Europa, Midden-Oosten en Afrika (EMEA)

Deze versie bevat de volgende verbeteringen en oplossingen:

* De [!DNL Analytics] API voor de nieuwe [!DNL Analytics] API versie 2.0. (TGT-45345)
* Opgeloste problemen met gevolgen [!UICONTROL Automated Personalization] (AP) activiteiten voor sommige klanten, met inbegrip van het tijdig synchroniseren van de activiteit op [!DNL Target] back-end maken en de verwachte ervaring bieden met voorvertoningskoppelingen. (TGT-46202)

## [!DNL Target] Standard/Premium 23.9.1 (6-11 september 2023)

Deze release is beschikbaar volgens het volgende schema voor gefaseerde installatie:

* **6 september**: Amerikaanse regio
* **7 september** Betreft: Europa, Midden-Oosten en Afrika (EMEA)
* **11 september**: regio Azië-Stille Oceaan (APAC)

Deze versie bevat de volgende verbeteringen en oplossingen:

* Probleem verholpen waarbij inconsistente rapportgegevens in het dialoogvenster [!DNL Target] UI en de [!DNL Adobe Analytics] UI voor [!UICONTROL Auto-Allocate] activiteiten die [!UICONTROL Analytics for Target] (A4T) als bron van rapportage. (TGT-46112)
* De time-out voor aanroepen van PUTTEN naar de API voor doellevering is verhoogd tot 15 seconden om time-outfouten te voorkomen. (TGT-46091)
* Probleem verholpen waardoor de URL niet constant kon worden bijgewerkt wanneer er door een website van de toepassing Eén pagina (SPA) werd gebladerd. (TGT-45417)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details at.js-versie](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
