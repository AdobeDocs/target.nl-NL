---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe functies en verbeteringen worden opgenomen in de komende [!DNL Target] Vrijgeven?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 04d4cf13e0054a767e9bf08770cdace1e130067f
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 20 maart 2023**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] Standard/Premium 23.3.1 (28-30 maart 2023)

Deze release is beschikbaar volgens het volgende schema:

* **28 maart**: Europa, Midden-Oosten en Afrika (EMEA)
* **29 maart**: Regio Azië-Stille Oceaan (APAC)
* **30 maart**: Amerikaanse regio

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
|--- |--- |
| AEM inhoudfragmenten voor hoofdloze personalisatie en experimenten | Gebruiken [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments] in [!DNL Target] activiteiten. Combineer het gebruiksgemak en de kracht van AEM met krachtige mogelijkheden voor kunstmatige intelligentie (AI) en het leren van machines (ML) in [!DNL Target] om ervaringen op schaal te testen en te personaliseren. |
| Geoptimaliseerde A4T-meetwaarden voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] | [!DNL Target] Hiermee kunt u metriek kiezen op basis van binomiale gebeurtenissen of metriek op basis van doorlopende gebeurtenissen wanneer u [!UICONTROL A4T] for [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.<P>Houd rekening met de volgende wijziging in ondersteunde meetwaarden:<ul><li>[!DNL Target] het eerdere gedrag voor bestaande activiteiten tot 9 september 2023 behouden. Na deze datum worden activiteiten waarbij niet-ondersteunde metriek wordt gebruikt, stopgezet om de migratie van bestaande activiteiten naar het nieuwe gedrag te forceren.</li></ul> |
| [!UICONTROL Auto-Allocate] gebruiken [!UICONTROL Analytics for Target] (A4T) | Bijgewerkte zelfstudie:<ul><li>[A4T-rapporten instellen in [!DNL Analysis Workspace] for [!UICONTROL Auto-Allocate] activiteiten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Auto-Target] gebruiken [!UICONTROL Analytics for Target] (A4T) | Bijgewerkte zelfstudie:<ul><li>[A4T-rapporten instellen in [!DNL Analysis Workspace] for [!UICONTROL Auto-Target] activiteiten](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

* Verbeterde publieks- en activiteitensynchronisatie zodat items zijn gemaakt in [!DNL Adobe Experience Platform] en [!DNL Adobe Audience Manager] zijn beschikbaar in [!DNL Target] UI sneller. (TGT-44568)
* Wijzigingen aangebracht om gebruikers toe te staan de [!UICONTROL Default URL] krachtens [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer] > [!UICONTROL Default URL]. Met deze wijziging kunnen klanten de standaard-URL terugzetten in een lege tekenreeks, die eerder niet mogelijk was na de eerste configuratie. (TGT-44577)
* Verwijderd beperkingen waardoor klanten niet langer in de box konden bewerken of verwijderen (publiek met gereserveerde namen). (TGT-44655)
* De optie &quot;[!UICONTROL Done]&quot;-optie tijdens het laden van spinners zijn zichtbaar in het dialoogvenster [!DNL Target] UI bij het maken van [gecombineerd publiek](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* Vaste het [!UICONTROL Language] koppeling onder aan [!UICONTROL Audiences] pagina zodat het correct met &quot;[!UICONTROL Account communication preferences]&quot; pagina. (TGT-43562)
* Probleem opgelost waarbij klanten soms werden belet om [!UICONTROL A/B Test] activiteiten na de selectie van de [!UICONTROL Adobe Analytics] optie onder [!UICONTROL Administration] > [!UICONTROL Reporting] > [!UICONTROL Reporting Experience Cloud Solution]. (TGT-44844)
* Probleem verholpen waardoor klanten de laatste ervaring in een [!UICONTROL Multivariate Test] activiteit met vele ervaringen van binnen [!UICONTROL Visual Experience Composer] (VEC). De [DOM-pad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) onderaan de VEC hebben klanten soms verhinderd de laatste ervaring te zien. (TGT-44578)
* Probleem verholpen waardoor de URL Bladeren in de VEC de huidige pagina die zichtbaar is in een normale browsersessie niet weerspiegelde als de pagina autorisatie vereist of omleidingen aanroept. (TGT-44350)
* Probleem verholpen waardoor klanten het [!UICONTROL Filter Incompatible Criteria] instellen in [!UICONTROL Recommendations] > [!UICONTROL Settings]. (TGT-44398)
* Probleem verholpen waarbij verzoeken van POSTEN om nieuwe gegevens werden gemaakt. Dit probleem is nu opgelost. [!DNL Recommendations] feeds die mislukken bij gebruik [!UICONTROL Analytics Classifications] met rapportsuites met punten in hun naam. (TGT-44598)
* Bijgewerkte koppelingen in het dialoogvenster [!DNL Target] UI om naar de nieuwe [De extensie Visuele bewerkingshulp](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Uitgebreide beveiliging om te voorkomen dat SSRF-pogingen (Server-Side Request Smeery) worden uitgevoerd in [!DNL Recommendations] feeds. (TGT-43769)
* Probleem verholpen waarbij klanten afbeeldingen niet konden bekijken in [!DNL Recommendations] ontwerpen als de afbeeldingsnaam [GB18030-tekens](https://en.wikipedia.org/wiki/GB_18030){target=_blank}. (TGT-44614)
* Probleem verholpen dat enkele problemen veroorzaakte [GB18030-tekens](https://en.wikipedia.org/wiki/GB_18030){target=_blank} die in de [!UICONTROL Modifications] deelvenster tijdens bewerken [!UICONTROL Text/HTML] op een activiteit [!UICONTROL Experiences] pagina.
* Verschillende lokalisatieoplossingen in de hele [!DNL Target] UI.


## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |


## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
