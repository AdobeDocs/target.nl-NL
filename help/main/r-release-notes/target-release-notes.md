---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 71f88ad173599b3a582a1d2c261ba8a562cf734a
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 20 juni 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [&#128279;](release-notes.md).
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.6.3 (20 juni 2025)

Deze release bevat de volgende correcties en updates:

* De optie [!UICONTROL Rearrange] is toegevoegd aan de bijgewerkte interface van [!UICONTROL Visual Experience Composer] (VEC), zodat deze kan worden uitgelijnd met de functionaliteit die beschikbaar is in de oudere VEC. (TGT-46957)
* Probleem verholpen waarbij het kopiëren van een activiteit van de ene werkruimte naar een andere werkruimte tot fouten leidde zoals &quot;mag niet null zijn&quot; of &quot;Er is iets fout gegaan&quot;. (TGT-52474)
* Probleem verholpen waarbij [!UICONTROL Automated Segments] - en [!UICONTROL Important Attributes] -rapporten niet werden gegenereerd voor bepaalde activiteiten. (TGT-52904)
* Probleem verholpen in de bijgewerkte VEC waarbij de standaardverwerking van inhoud in [!UICONTROL Automated Personalization] (AP)-activiteiten niet overeenkwam met de oudere UI. Het systeem voegt nu automatisch de standaardwaarde `optionGroup` &quot;Standaardinhoud&quot; toe aan `optionGroupLocalId = 0` wanneer er geen groep expliciet wordt toegevoegd. Deze groep bevat de standaardoptie (bijvoorbeeld `optionLocalId: 0` ). Als de standaardinhoud wordt verwijderd, wordt ook de corresponderende optiegroep verwijderd. (TGT-52651)
* Probleem verholpen met [!UICONTROL Multivariate Test] (MVT)-activiteiten waarbij het hergebruik van een `experienceLocalId` uit eerder verwijderde ervaringen onjuist werd verboden. (TGT-52672)
* Probleem verholpen waarbij URL&#39;s op activiteitenlocaties geen queryparameters konden weergeven vanwege ongeldige tekens, zoals schuine strepen (/). (TNT52845)
* Het foutbericht voor de validatie van [!DNL A/B Test] activity updates via de back-end API is verbeterd. Wanneer dubbele locatienamen aanwezig zijn, staat nu duidelijk in het bericht: &quot;Dubbele namen zijn niet toegestaan&quot; voor `locations.selectors` . (TGT-52589)
* Oplossing voor een fout die optrad bij het bijwerken van een live [!UICONTROL Recommendations] -activiteit vanwege een niet-herkende eigenschap in de payload van de aanvraag. Het systeem handelt nu correct de &quot;Ongeldige JSON. Niet-herkende eigenschapsnaam&quot;. (TGT-52723)
* Probleem verholpen waarbij het maken van een [!DNL Recommendations] -ontwerp werd voorkomen. Als u op [!UICONTROL Create] klikt, wordt het bericht geactiveerd: &quot;Er moet ten minste één entiteitsvariabele in het script worden gebruikt.&quot; (TGT-52395 &amp; TGT-52899)
* Probleem opgelost waarbij het opnieuw opslaan van een [!DNL Recommendations] -ontwerp zonder wijzigingen werd geblokkeerd. (TGT-52879)
* Probleem verholpen met een validatiefout aan de achterkant die een fout van het type &quot;400 Onjuist verzoek&quot; veroorzaakte bij het opslaan van een [!UICONTROL Recommendations] -activiteit. (TGT-52716)
* Probleem verholpen in [!UICONTROL Form-Based Experience Composer] waarbij het aanwijzen van de muisaanwijzer over een box met speciale tekens in de vervolgkeuzelijst [!UICONTROL Location] ertoe leidde dat de editor leeg ging en dat er een &#39;QuerySelector&#39; kon niet worden uitgevoerd op &#39;Element&#39;. fout. (TGT-52717)
* Verbeterde nauwkeurigheid van de voederstatus met een nieuwe indicator &quot;PARTIALLY_IMPORTED&quot;. Eerder werden feeds gemarkeerd als &quot;succes&quot;, zelfs als niet alle rijen in een bestand werden geïmporteerd, wat misleidend was. (TGT-52892)
* Probleem verholpen waarbij bepaalde API-aanroepen naar `/admin/rest/ui/v1/campaigns` na de migratie naar AP V2 fouten aan de clientzijde (HTTP 4xx) veroorzaakten. (TGT-52721)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
