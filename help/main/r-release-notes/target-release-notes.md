---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: df7e28060a6add53e1aaed928351b4f399b19c17
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**laatst bijgewerkt: 10 juli, 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.7.3 (24 juli 2025)

Vanwege recente problemen die zijn vastgesteld en die voornamelijk verband houden met complexe klantaanpassingen, bevat deze release de volgende oplossingen en updates:

**Activiteiten**

+++Zie details
* Probleem verholpen waarbij de methode `buildViews` in de klasse builder `viewMaxLocalId` onjuist instelde op het totale aantal weergaven in plaats van op het hoogste toegewezen `viewLocalId` . (TGT-53207)

**vorm-Gebaseerde Composer van de Ervaring**

+++Zie details
* Oplossing een kwestie in [!UICONTROL Form-Based Experience Composer] die de redacteur aan neerstorting na het klikken van het **[!UICONTROL Manage Content]** pictogram ( ![ leidt het pictogram van de Inhoud ](/help/main/assets/icons/Experience.svg)) toen het creëren van of het uitgeven van een [!UICONTROL Automated Personalization] (AP) activiteit veroorzaakte. (TGT-53047)

+++

**Aanbevelingen**

+++Zie details
* Probleem verholpen waarbij [!UICONTROL Catalog Search] geen extra resultaten kon laden wanneer naar de onderkant van de lijst werd geschoven en het gedrag werd hersteld in overeenstemming met de oudere gebruikersinterface. (TGT-53088)
* Probleem verholpen waarbij de kolom [!UICONTROL Number of Products] ontbrak op de pagina [!UICONTROL Collections] in de bijgewerkte [!DNL Target] gebruikersinterface. De kolom wordt nu correct weergegeven en de verwachte functionaliteit wordt hersteld. (TGT-53168)
* Probleem verholpen waarbij [!UICONTROL Collection] -regels niet correct filteren volgens de regels. (TGT-53254)
* Probleem verholpen waarbij het verwijderen van items uit het dialoogvenster [!UICONTROL Criteria Details] werd geblokkeerd. (TGT-53245)
* Probleem verholpen waardoor het openen van producten zonder naam niet mogelijk was. Dit probleem is opgetreden bij het selecteren van omgevingen die onbenoemde resultaten hebben opgeleverd, waardoor toegang tot productdetails niet mogelijk was. (TGT-53007)
* Probleem verholpen waarbij de pagina [!UICONTROL Catalog Search] vastliep en een leeg scherm werd weergegeven wanneer bepaalde producten werden geselecteerd. (TGT-53087)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details

* Probleem verholpen in de VEC waarbij het toepassen van een wijziging op een weergave dubbel werk veroorzaakte en een fout met &#39;Ongeldige gebruikersinvoer&#39; veroorzaakte. (TGT-52886)
* Probleem verholpen met [!UICONTROL Undo] functionaliteit voor de opties [!UICONTROL Insert Before] en [!UICONTROL Insert After] bij het configureren van afbeeldingsaanbiedingen in de VEC.

  Eerder leidde het ongedaan maken van een [!UICONTROL Insert Before] - of [!UICONTROL Insert After] -actie op afbeeldingsaanbiedingen tot inconsequent gedrag of tot het niet correct herstellen van de wijziging, vooral in activiteiten die zijn gemaakt in de oudere [!DNL Target] -gebruikersinterface. Dit probleem is opgelost om ervoor te zorgen dat acties voor ongedaan maken nu betrouwbaar werken voor deze wijzigingen. (TGT-52809)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
