---
keywords: Opmerkingen bij de release;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates
description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target], inclusief SDK's, API's en JavaScript-bibliotheken.
landing-page-description: Meer informatie over de nieuwe functies, verbeteringen en oplossingen die zijn opgenomen in de huidige release van [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 62b0c6ca313ab5990b5e0bc6d33e913fd0bdd5ef
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke versie [!DNL Adobe Target Standard] en [!DNL Target Premium] vrijgeven. Daarnaast kunt u opmerkingen bij de release publiceren voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK]en andere platformwijzigingen worden, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn voor intern [!DNL Adobe] gebruiken.)

## [!DNL Target] Standard/Premium 22.13.3 (25-26 januari 2023)

Deze release is beschikbaar volgens het volgende schema:

* **25 januari**: Europa, Midden-Oosten en Afrika (EMEA)
* **25 januari**: Regio Azië-Stille Oceaan (APAC)
* **26 januari**: Amerikaanse regio

Deze release bevat de volgende nieuwe functies, verbeteringen en oplossingen:

| Functie | Details |
| --- | --- |
| [JSON-aanbieding](/help/main/c-experiences/c-manage-content/create-json-offer.md) ondersteuning in Automated Personalization (AP) | Extra ondersteuning voor JSON-aanbiedingen in [!UICONTROL Automated Personalization] (AP) activiteiten met behulp van de Form-Based Experience Composer. (TGT-41460) |
| [AEM ervaren fragmenten](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | De mogelijkheid toegevoegd om onderscheid te maken tussen [!DNL Adobe Experience Manager] fragmenttypen (AEM XF) die worden geëxporteerd naar [!DNL Target]. In plaats van de optie Fragment ervaren, [!DNL Target] kunt u nu filteren en zoeken op &quot;HTML XF&quot; en &quot;JSON XF&quot;. (TGT-44132) |

* Probleem verholpen waarbij de fout &quot;500&quot; werd veroorzaakt in [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten die aanbevelingen bevatten. Dit probleem is ontstaan toen [!DNL Target] heeft niet correct criteria-objecten uit het [!DNL Target] UI en [!DNL Recommendations] back-end die niet meer in gebruik zijn. (TGT-44383)
* De locatie is verwijderd uit de naam van de weergegeven aanbieding in het dialoogvenster [!UICONTROL Offer Level] verslag voor [!UICONTROL Automated Personalization] activiteiten. Deze wijziging maakt het verslag leesbaarder. (TGT-44294)
* De kalenderopties van 45 dagen en 90 dagen zijn verwijderd uit het toegangspunt en [!UICONTROL Auto-Target] [!UICONTROL Personalization Insights] en [!UICONTROL Important Attributes] in de [!DNL Target] UI. Vanwege gebruikspatronen en om de prestaties te verbeteren, zijn deze datumbereiken afgekeurd. De interface is bijgewerkt om de momenteel toegestane bereiken te weerspiegelen: 15, 30 en 60 dagen. (TGT-39357)
* De mogelijkheid om de [!UICONTROL Same as Optimization Goal] instellen op de [!UICONTROL Goals & Settings] pagina nadat de activiteit live is. (TGT-43923)
* Probleem verholpen dat problemen veroorzaakte met de standaardwerkplek in de [!DNL Target] back-end bij upgrade vanaf [!DNL Target Standard] tot [!DNL Target Premium]. (TGT-44081 &amp; TGT-44306)
* Een wijziging aanbrengen om toe te staan [!DNL Analytics] rapportsuites met punttekens &quot;.&quot; in de namen die in de [!DNL Target] UI voor het maken van [!DNL Analytics] classificatieffeeds.
* De koppeling op het tabblad [!UICONTROL Implementation] pagina ([!UICONTROL Administration] > [!UICONTROL Implementation]) voor &quot;Implementatiemethodes met Apparaatbesluit&quot; om te verwijzen naar de pagina met uitleg over het gebruik van apparaatbeslissingen voor alle ondersteunde SDK&#39;s: Node.js, Java, .NET, en Python. Zie voor meer informatie [Aan de slag met doel-SDK&#39;s](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* Probleem verholpen die bij het gebruik van bestanden problemen bij het uploaden veroorzaakte. [!DNL Scene7] en [!DNL Target].
* De toegankelijkheid van de [!DNL Target] UI voor personen met een handicap door resultaten van een interne bruikbaarheidscontrole te gebruiken. Deze toegankelijkheidsverbeteringen omvatten toegang tot functies die voorheen niet via het toetsenbord toegankelijk waren, alt-tekstverbeteringen, de mogelijkheid om te zoomen op onderdelen van de gebruikersinterface om bruikbaarder te zijn, verbeterde toetsenbordfocus en meer.   (TGT-42759)
* Verschillende lokalisatieoplossingen in de hele [!DNL Target] UI.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Details over de wijzigingen in elke versie van het dialoogvenster [!DNL Adobe Target] at.js JavaScript-bibliotheek. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen.<br>Zie voor meer informatie [Documentatiewijzigingen](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Zie voor meer informatie [Opmerkingen bij de release van vorige releases](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie voor meer informatie [Opmerkingen bij de release Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdate | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie, zie [Opmerkingen bij de doelversie - Prerelease](/help/main/r-release-notes/target-release-notes.md) pagina. |
