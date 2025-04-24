---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b09796cd8464b54dcc1945ae1ec00eb914ba218c
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Recentste Bijgewerkt: 24 april, 2025**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel ](release-notes.md). [ De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.4.5 (25 april 2025)

Deze release bevat de volgende correcties en updates:

* Probleem verholpen waarbij verschillen optraden tussen de pagina met [!UICONTROL Activity] instellingen en de overzichtspagina van [!UICONTROL Reporting] . (TGT-52203)
* Probleem verholpen waardoor het toevoegen van een nieuwe pagina aan een activiteit niet mogelijk was vanwege een ongeldige fout bij de gebruikersinvoer. (TGT-52263)
* Correctie van een probleem waarbij aanbevelingen niet werden weergegeven op de website van de klant na activering van de [!DNL Recommendations] -activiteit. (TGT-52164)
* Probleem verholpen waarbij `OptionLocalIDs` onjuist werd verhoogd wanneer de optie ongewijzigd blijft. (TGT-52187)
* Probleem verholpen zodat gedownloade rapportbestanden gegevens correct weergeven in de rapportage-UI. (TGT-52068)
* Probleem verholpen zodat batchbewerkingen niet meer mislukken nadat de regels voor het leveren van pagina&#39;s waren toegevoegd. (TGT-52097)
* Probleem opgelost waarbij [!DNL Target] alle queryparameters van de URL van de website bijsnijde. (TGT-52100)
* Oplossing voor een consolefout die klanten verhinderde activiteiten in zowel erfenis als bijgewerkte Doel UI tot stand te brengen. (TGT-52181)
* Probleem verholpen waarbij klanten werden verhinderd nieuwe pagina&#39;s toe te voegen, wat een ongeldige fout bij gebruikersinvoer tot gevolg had. (TGT-52258)
* Probleem verholpen waarbij wijzigingen verdwenen nadat extra pagina&#39;s waren toegevoegd en weer naar het tabblad [!UICONTROL Experiences] werd genavigeerd. (TGT-52264)
* Probleem verholpen waarbij klanten werden verhinderd het publiek te wijzigen in een [!UICONTROL Experience Targeting] (XT) -activiteit. (TGT-52191)
* Correctie van een fout die het bewerken van een XT-activiteit als gevolg van een niet-ondersteunde UI-regel heeft verhinderd. (TGT-52273)
* Probleem verholpen waarbij wijzigingen in de activiteit niet werden weergegeven in de gebruikersinterface van [!DNL Target] , ondanks dat deze wel op de webpagina werden weergegeven. (TGT-52192)
* Probleem verholpen in de bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC), waarbij broodkruimels niet altijd onder aan de editor werden weergegeven, waardoor er problemen optraden bij het nauwkeurig selecteren van elementen. (TGT-51169)
* Probleem verholpen waarbij in de vervolgkeuzelijst [!UICONTROL Audience] niet alle soorten publiek werden weergegeven vanwege paginering. (TGT-52204)
* Probleem verholpen die een ongeldig bericht veroorzaakte dat de gebruiker invoerde bij het toevoegen van nieuwe aanbiedingen in [!UICONTROL Automated Personalization] (AP) activiteiten. (TGT-52210)
* Probleem verholpen waarbij [!UICONTROL Analytics for Target] (A4T) ten onrechte als bron voor rapportage werd geselecteerd, ook al had de klant geen toegang tot A4T. (TGT-5226)
* Probleem verholpen waarbij het opslaan van een activiteit met de metrische URL van [!UICONTROL View a Page] werd voorkomen. (TGT-52260)
* Probleem verholpen waarbij klanten werden verhinderd werkruimten te selecteren tijdens het maken van aanbiedingen binnen een activiteit. (TGT-52289)
* Probleem verholpen waarbij wijzigingen van de ene ervaring onjuist werden weergegeven bij het schakelen naar een andere ervaring. (TGT-52184)
* Probleem verholpen waarbij de standaardaanbieding onjuist werd weergegeven in de gebruikersinterface van [!DNL Target] bij het openen van de activiteit. (TGT-52198)

## Update voor doelmachtigingen (22 april 2025)

Deze toekomstige update verbetert de organisatorische controle over [!DNL Target] instantieconfiguraties, die toevallige updates verhinderen die activiteitenlevering over diverse test en verpersoonlijkingsteams zouden kunnen beïnvloeden.

Vanaf 22 april 2025 kunnen alleen [!UICONTROL Product] - en [!UICONTROL Solutions] -beheerders instellingen in de [!UICONTROL Administration] -secties bijwerken, ongeacht hun rollen in [!DNL Target] -werkruimten. Gebruikers zonder deze machtiging hebben alleen-lezen toegang tot de secties van [!UICONTROL Administration] .

Voor meer informatie, zie [ Doel beheren ](/help/main/administrating-target/start-target.md).

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
