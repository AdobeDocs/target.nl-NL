---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen en verhogingen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 33d85fcbfc971c188f4154cca5b4d21103b4dbb7
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 23 januari 2023**

Voor informatie over de huidige versie raadpleegt u [Opmerkingen bij de doelversie](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruik.

## [!DNL Target] Standard/Premium 22.13.3 (25 januari 2023)

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| Automated Personalization (AP) | Extra ondersteuning voor JSON-aanbiedingen in [!UICONTROL Automated Personalization] (AP) activiteiten met behulp van de Form-Based Experience Composer.<br>Zie voor meer informatie [JSON-aanbiedingen maken](/help/main/c-experiences/c-manage-content/create-json-offer.md). (TGT-41460) |
| Recommendations | Vriendelijke namen in [!UICONTROL Analytics for Target] A4T-rapportage is nu beschikbaar. Eerder [!DNL Target] Alleen vermelde ervaring-id&#39;s. Dankzij deze verbetering kunt u de rapportage afstemmen op [!DNL Adobe Analytics] en [!DNL Target] en helpt klanten het samenstellen van rapporten in A4T stroomlijnen. (TGT-41853) |
| Activiteit QA | Geïmplementeerd [QA-modus](/help/main/c-activities/c-activity-qa/activity-qa.md) voor AP-activiteiten voor geselecteerde klanten. Deze functionaliteit is beschikbaar voor alle klanten na een eerste testfase. (TGT-44341) |

* Probleem verholpen waarbij de fout &quot;500&quot; werd veroorzaakt in [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die aanbevelingen bevatten. Dit probleem is ontstaan toen [!DNL Target] heeft niet correct criteria-objecten uit het [!DNL Target] UI en [!DNL Recommendations] back-end die niet meer in gebruik zijn. (TGT-44383)
* De locatie is verwijderd uit de naam van de weergegeven aanbieding in het dialoogvenster [!UICONTROL Offer Level] verslag voor [!UICONTROL Automated Personalization] activiteiten. Deze wijziging maakt het verslag leesbaarder. (TGT-44294)
* De naam van de &quot;[!UICONTROL Experience Fragment]&quot; in de [!UICONTROL Visual Experience Composer] (VEC) workflow. De optie is nu &quot;[!UICONTROL HTML XF].&quot; (TGT-44132)
* De kalenderopties van 45 dagen en 90 dagen zijn verwijderd uit het toegangspunt en [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] en [!UICONTROL Important Attributes] in de [!DNL Target] UI. Vanwege gebruikspatronen en om de prestaties te verbeteren, zijn deze datumbereiken afgekeurd. De interface is bijgewerkt om de momenteel toegestane bereiken te weerspiegelen: 15, 30 en 60 dagen. (TGT-39357)
* De mogelijkheid om de [!UICONTROL Same as Optimization Goal] instellen op de [!UICONTROL Goals & Settings] pagina nadat de activiteit live is. (TGT-43923)
* Probleem verholpen dat problemen veroorzaakte met de standaardwerkplek in de [!DNL Target] back-end bij upgrade vanaf [!DNL Target Standard] tot [!DNL Target Premium]. (TGT-44081 &amp; TGT-44306)
* De koppeling op het tabblad [!UICONTROL Implementation] pagina ([!UICONTROL Administration] > [!UICONTROL Implementation]) voor &quot;Implementatiemethodes met Apparaatbesluit&quot; om te verwijzen naar de pagina met uitleg over het gebruik van apparaatbeslissingen voor alle ondersteunde SDK&#39;s: Node.js, Java, .NET, en Python. Zie voor meer informatie [Aan de slag met doel-SDK&#39;s](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Probleem verholpen die bij het gebruik van bestanden problemen bij het uploaden veroorzaakte. [!DNL Scene7] en [!DNL Target].
* De toegankelijkheid van de [!DNL Target] UI voor personen met een handicap door resultaten van een interne bruikbaarheidscontrole te gebruiken. Deze toegankelijkheidsverbeteringen omvatten toegang tot functies die voorheen niet via het toetsenbord toegankelijk waren, alt-tekstverbeteringen, de mogelijkheid om te zoomen op onderdelen van de gebruikersinterface om bruikbaarder te zijn, verbeterde toetsenbordfocus en meer.   (TGT-42759)
* Verschillende lokalisatieoplossingen in de hele [!DNL Target] UI.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |


## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Om voorafgaande berichten over aanstaande productverhogingen te ontvangen aan [!DNL Target] en andere [!DNL Adobe Experience Cloud] oplossingen, aanmelden voor de [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
