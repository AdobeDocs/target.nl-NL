---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 065220af5c8e3b6cc25ef7289d006a901d2e932a
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 22 juli 2025**

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
* Introduceerde een nieuw API eindpunt dat gebruikers toestaat om eerder geschrapte activiteitenopties van een secundair gegevensbestand te herstellen. Deze functionaliteit maakt gebruik van de bestaande infrastructuur die door de klassen `RemovedCampaignElements` en `RemovedOptionInfo` wordt geboden, zodat verwijderde opties naadloos kunnen worden geïntegreerd in actieve activiteiten. (TGT-52903)
* Correctie van een probleem in de bijgewerkte gebruikersinterface van [!DNL Target] waarbij verwijderde aanbiedingen in [!UICONTROL Automated Personalization] (AP)-activiteiten werden weergegeven als `Deleted option with ID: X` in plaats van als de oorspronkelijke namen (bijvoorbeeld `Offer Name [Deleted]` zoals weergegeven in de oudere gebruikersinterface). Met deze oplossing herstelt u betekenisvolle etikettering voor verwijderde aanbiedingen, waardoor de duidelijkheid wordt verbeterd en de rapportage nauwkeuriger en gebruiksvriendelijker wordt. (TGT-52921)
* Probleem verholpen in de achtergrondpersistentielaag waarbij verwijderde opties correct waren opgeslagen, maar niet toegankelijk waren via bestaande API-eindpunten. Dientengevolge, konden de frontend toepassingen geen zinvolle namen voor geschrapte opties terugwinnen, die historische rapporteringsmeningen beïnvloeden. Met deze correctie wordt ervoor gezorgd dat behouden verwijderde optiegegevens nu op de juiste wijze kunnen worden weergegeven in de gebruikersinterface. (TGT-52973)
* Probleem verholpen waarbij bepaalde activiteiten die van Target naar Target Central waren gemigreerd inconsistente metrische configuraties hadden als gevolg van een eerder opgeloste synchronisatiebug. Specifiek, behielden de activiteiten die oorspronkelijk een omzettingsmetrisch gebruikten en later aan analytisch-gebaseerde metrisch werden bijgewerkt achterhaalde waarden op `primaryMetricType` en `successCriteria` gebieden. (TGT-52643)

+++

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
* Probleem verholpen waarbij [!DNL Recommendations] -activiteiten met metrische namen van meer dan 25 tekens niet konden worden geopend of bewerkt vanwege API-beperkingen. Deze correctie zorgt voor compatibiliteit met metrische namen die de tekenlimiet overschrijden en herstelt volledige toegang tot de desbetreffende activiteiten. (TGT-52839)
* Probleem verholpen waarbij gebruikers de site_cart_z1 [!DNL Recommendation] -activiteit niet konden bewerken in de gebruikersinterface van [!DNL Target] . Als u de activiteit probeerde te openen, werd een fout op de pagina [!UICONTROL Overview] gegenereerd, waardoor de toegang tot de editor werd geblokkeerd. (TGT-53221)

+++

**Meldend**

+++Zie details
* Probleem verholpen waarbij het sandboxveld in de activiteitsdatabase niet werd gewist toen de rapportbron werd overgeschakeld van [!DNL Customer Journey Analytics] naar [!DNL Analytics] . [!DNL Target] Eerder heeft de gebruikersinterface de sandbox correct verzonden: null, maar de back-end heeft deze waarde genegeerd, waardoor verouderde sandboxgegevens op zijn plaats blijven. De backend ontruimt nu behoorlijk het zandbakgebied wanneer ongeldig wordt ontvangen. (TGT-52798)
* Implementeer de verwijderde optiepersistentielaag opnieuw in de doelachtergrond om nauwkeurige historische rapportage in [!UICONTROL Automated Personalization] (AP)-activiteiten te ondersteunen. Eerder, toen een optie werd geschrapt, werd zijn naam verloren, die het moeilijk maken om vroegere prestatiesgegevens te interpreteren.

  **Zeer belangrijke Verbeteringen**:

   * Verwijderde opties worden nu bijgehouden met behulp van de bestaande `RemovedCampaignElements` - en `RemovedOptionInfo` -infrastructuur.
   * Wanneer een optie uit een AP-activiteit wordt verwijderd, blijven de metagegevens (bijvoorbeeld ID en naam) behouden.
   * De rapportinterface kan nu de oorspronkelijke optienaam (bijvoorbeeld `Option Name [Deleted]` ) naast historische metriek weergeven, waardoor de duidelijkheid en bruikbaarheid worden verbeterd.

  Deze update zorgt voor consistente en betekenisvolle rapportage, zelfs nadat opties uit een activiteit zijn verwijderd. (TGT-52986)

* Een nieuw migratieeindpunt geïmplementeerd ter ondersteuning van de overdracht van opties voor verwijderde activiteit van op JCR gebaseerde activiteiten naar [!DNL Target] Central. Deze functionaliteit maakt consistente tracering en rapportage mogelijk voor alle systemen. Met deze functie zorgt u ervoor dat verwijderde opties behouden blijven en gesynchroniseerd blijven op de voorzijde en achterzijde van [!DNL Target] , waardoor de historische rapportage en gegevensintegriteit worden verbeterd. (TGT-53217)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details

* Probleem verholpen in de VEC waarbij het toepassen van een wijziging op een weergave dubbel werk veroorzaakte en een fout met &#39;Ongeldige gebruikersinvoer&#39; veroorzaakte. (TGT-52886)
* Probleem verholpen met [!UICONTROL Undo] functionaliteit voor de opties [!UICONTROL Insert Before] en [!UICONTROL Insert After] bij het configureren van afbeeldingsaanbiedingen in de VEC.

  Eerder leidde het ongedaan maken van een [!UICONTROL Insert Before] - of [!UICONTROL Insert After] -actie op afbeeldingsaanbiedingen tot inconsequent gedrag of tot het niet correct herstellen van de wijziging, vooral in activiteiten die zijn gemaakt in de oudere [!DNL Target] -gebruikersinterface. Dit probleem is opgelost om ervoor te zorgen dat acties voor ongedaan maken nu betrouwbaar werken voor deze wijzigingen. (TGT-52809)

* Probleem verholpen waarbij het kenmerk `contentEditable` onbedoeld werd ingesteld op true en bleef bestaan in opgeslagen HTML-inhoud. Deze update zorgt voor schonere, verwachte HTML-uitvoer zonder onbedoeld bewerkingsgedrag. (TGT-52319)
* Om permanent verlies van geschrapte opties te verhinderen en verenigbaar gedrag over de diensten te verzekeren, is de zachte schrappingsfunctionaliteit uitgevoerd voor opties in UI en verwante microservices.

  **Zeer belangrijke Veranderingen**:

   * De opties worden niet meer permanent verwijderd. In plaats daarvan worden ze gemarkeerd met een nieuwe verwijderde: ware markering in het XML-parameterobject.
   * Deze markering wordt alleen gebruikt door de bijgewerkte [!DNL Target] UI om verwijderde opties uit te sluiten van rendering en te voorkomen dat deze naar Edge-services worden verzonden.
   * Verwijderde opties blijven deel uitmaken van de taakbelasting tijdens bewerkingen, waardoor de traceerbaarheid wordt gewaarborgd en niet-bestaande opties aan klanten worden geleverd.

  Deze update verbetert de gegevensintegriteit en past de beste praktijken voor het beheren van schrappingen in verdeelde systemen aan. (TGT-52726)

+++

**Werkruimten**

+++Zie details
* Probleem verholpen bij het kopiëren van een activiteit van een niet-standaard naar een standaardwerkruimte of tussen niet-standaardwerkruimten. Aanbiedingen worden nu gedupliceerd met verbeterde tracking en naming om conflicten te voorkomen.

  **Zeer belangrijke Verbeteringen**:
   * Aanbiedingen worden opnieuw gemaakt in de doelwerkruimte met bijgewerkte id&#39;s en metagegevens.
   * De naam van gekopieerde voorstellen wordt gewijzigd in de indeling: &quot;Naam van voorstel kopiëren&quot; plus een willekeurig nummer of tijdstempel om ervoor te zorgen dat deze voorstellen uniek zijn.
   * De systeemupdates bieden de status van de activiteit en weerspiegelen deze met de nieuwe id&#39;s.
   * Deze functie voorkomt fouten die worden veroorzaakt door meerdere identieke namen voor &quot;Offertes kopiëren&quot; tijdens herhaalde kopieerhandelingen.
   * Aanbiedingen worden mogelijk niet direct weergegeven in de lijst met aanbiedingen van de doelwerkruimte, maar worden op de juiste wijze verwerkt en weergegeven.

  Deze update verbetert de betrouwbaarheid en traceerbaarheid bij het beheren van aanbiedingen in meerdere werkruimten. (TGT-53080)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
