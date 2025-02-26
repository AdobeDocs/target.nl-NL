---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates,huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: b68c3d2e7e884e176a61598d1ab4a423aa1c9088
workflow-type: tm+mt
source-wordcount: '1520'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke [!DNL Adobe Target Standard] - en [!DNL Target Premium] -release. Daarnaast worden releaseopmerkingen voor [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformwijzigingen, indien van toepassing, ook opgenomen.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## [!DNL Target Standard/Premium] 25.2.3 (26 februari 2025)

Deze release bevat de volgende updates:

* Oplossing voor een probleem dat het bijwerken van activiteiten na [!DNL Target] release 25.2.1 voor bepaalde activiteiten verhinderde. (TGT-51781)
* Oplossing voor een probleem waarbij alle wijzigingen in het publiek in de status werden verwijderd na het annuleren van het proces voor het maken van activiteiten (door [!UICONTROL Cancel] te selecteren in plaats van [!UICONTROL Add Audience] ). (TGT-51769 &amp; TGT-51770)
* Het volgende probleem is opgelost: [!UICONTROL Visual Experience Composer] (VEC) kan niet worden geladen voor bepaalde activiteiten, met name wanneer aangepaste code is gebruikt.  Deze kwestie leidde ertoe dat VEC een leeg scherm of [!DNL Target] UI terugkerend aan zijn oudere versie toonde. (TGT-51758)
* Oplossing voor een probleem waarbij wijzigingen werden genegeerd na het bewerken van de paginalevering voor het publiek. (TGT-51756)
* Het volgende probleem is opgelost: alle niet-metrische doelgroepen (pagina- en ervaringspubliek) zijn uit activiteiten verwijderd wanneer een metrisch type op de pagina [!UICONTROL Goals & Settings] wordt gewijzigd. (TGT-51753)
* Probleem opgelost waarbij tijdens het bewerken van een activiteit door [!UICONTROL Cancel] werd genavigeerd naar de [!UICONTROL Activities List] -pagina in plaats van naar de [!UICONTROL Activity Details] -pagina. (TGT-51731)
* Oplossing voor een probleem waardoor klanten geen rapporten konden downloaden via de optie [!UICONTROL Export Reports to CSV] . (TGT-51708)
* Probleem opgelost in de Form-Based Experience Composer waarbij [!DNL Target Standard] -klanten ten onrechte werden weergegeven als gebruikers van [!UICONTROL Properties] , een [!DNL Target Premium] -functie. (TGT-51678)
* Oplossing voor een probleem waarbij de weergave van [!DNL Adobe Experience Platform] -kenmerken tijdens het maken van nieuwe aanbiedingen werd geblokkeerd. (TGT-51665)
* Alle actieve filters voor [!DNL Recommendations] -voorraad zijn verplaatst naar de snelle zoekopdracht, waarbij de interface wordt uitgelijnd met [!UICONTROL Catalog Search] in plaats van met de [!UICONTROL Filter] -rail. (TGT-50723)

## at.js versie 2.11.7 (26 februari 2025)

Deze release bevat de volgende update:

* Logboekregistratie van Telemetrie is opgelost wanneer `localStorage` niet beschikbaar is. Telemetrie zorgde voor een probleem voor sommige klanten die `localStorage` hadden uitgeschakeld in hun browsers.

## Target Standard/Premium 25.2.1 (17 februari 2025)

Deze release bevat de volgende updates:

* [!UICONTROL Activities] update gebruikersinterface
* [!DNL Recommendations] update gebruikersinterface

### [!UICONTROL Activities] update gebruikersinterface

Aangezien de modernisering van de gebruikersinterface van [!DNL Adobe Target] wordt voortgezet, zijn wij verheugd de algemene beschikbaarheid van de bijgewerkte gebruikersinterface van [!UICONTROL Activities] aan te kondigen.

>[!NOTE]
>
>Vanaf 17 februari hebben klanten geleidelijk toegang tot de nieuwe [!UICONTROL Activities] -interface. Om een naadloze uitrol voor alle klanten te verzekeren, zal deze versie in gecontroleerde stadia worden opgesteld. In de eerste fase wordt de eerste groep [!DNL Target] -klanten bijgewerkt naar de nieuwe [!UICONTROL Activities] -gebruikersinterface. De volgende stadia zullen de resterende klanten bevorderen.

Op basis van het nieuwste ontwerpsysteem van [!DNL Adobe Spectrum] worden eerder inconsistente ontwerppatronen gestandaardiseerd en worden nieuwe verbeteringen toegevoegd, zoals:

* [ opnieuw ontworpen rapporterend ](/help/main/administrating-target/reporting.md) voor betere inzichten in activiteitenresultaten.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) pagina, nu het krijgen van de informatie van [[!DNL Audit Query API] ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview) {target=_blank} voor inzicht in real time.
* [ Aanpasbare lijstmeningen ](/help/main/c-activities/activities.md) aan voor betere flexibiliteit over verschillende teambehoeften.
* [ Verbeterde snelle info en detailschermen ](/help/main/c-activities/activities.md) voor gemakkelijkere toegang tot informatie.
* [ Zitting-blijvende onderzoek en filteropties ](/help/main/c-activities/activities.md).
* Volledig [ herbouwd [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) met steun voor recentste veiligheidsupdates van browser leveranciers en een modern gebruikersinterface.

  Voor informatie over hoe de bijgewerkte VEC van de vorige versie verschilt, zie:

   * [ de veranderingen van Composer van de Visuele Ervaring ](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
   * [Opties voor Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [ bijgewerkte  [!DNL Chrome]  uitbreiding ](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) ondersteunend Duidelijke V3 voor verhoogde veiligheid en betere steun voor eerstepartijkoekjes.

![ Activiteiten verfrissen zich ](/help/main/r-release-notes/assets/activities-refresh.png)

### [!DNL Recommendations] update gebruikersinterface

Aangezien de modernisering van de gebruikersinterface van [!DNL Adobe Target] wordt voortgezet, zijn wij verheugd de algemene beschikbaarheid van de bijgewerkte gebruikersinterface van [!DNL Recommendations] aan te kondigen.

>[!NOTE]
>
>Vanaf 17 februari hebben klanten geleidelijk toegang tot de nieuwe [!UICONTROL Recommendations] -interface. Om een naadloze uitrol voor alle klanten te verzekeren, zal deze versie in gecontroleerde stadia worden opgesteld. In de eerste fase wordt de eerste groep [!DNL Target] -klanten bijgewerkt naar de nieuwe [!UICONTROL Activities] -gebruikersinterface. De volgende stadia zullen de resterende klanten bevorderen.

Op basis van het nieuwste ontwerpsysteem van [!DNL Adobe Spectrum] worden eerder inconsistente ontwerppatronen gestandaardiseerd en worden nieuwe verbeteringen toegevoegd, zoals:

* Het [ onderzoek van de productcatalogus ](/help/main/c-recommendations/c-products/catalog-search.md) kenmerkt nu een bijgewerkt gegevensbestand dat een synchronisatie in real time van producten toestaat.
* [!UICONTROL Recommendations] de voorwerpen ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections], en [!UICONTROL Exclusions]) [ over API worden gecreeerd zijn nu beschikbaar in UI ](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [ de montages van Aanbevelingen ](/help/main/administrating-target/recommendations-settings.md) zijn geconsolideerd onder de [!UICONTROL Administration] sectie.
* Aanpasbare lijstweergaven voor meer flexibiliteit in verschillende teambehoeften.
* Vernieuwde HTML en JSON coderedacteurs met [ syntaxis het benadrukken en lijnnummering ](/help/main/c-experiences/c-manage-content/create-json-offer.md).
* Verbeterde snelle info- en detailschermen voor eenvoudigere toegang tot informatie.
* Sessiepermanente zoek- en filteropties.

![ UI van Aanbevelingen verfrist zich ](/help/main/r-release-notes/assets/recs-ui-refresh.png)

## Target Standard/Premium 25.1.1 (9 januari 2025)

Deze release bevat de volgende updates:

### [!UICONTROL Offers Library] update gebruikersinterface

Deze release werkt de gebruikersinterface van [!UICONTROL Offers Library] bij om de gebruikerservaring voor [!DNL Adobe Target] -gebruikers te verbeteren.

>[!NOTE]
>
>Om een naadloze uitrol voor alle klanten te verzekeren, zal deze versie in gecontroleerde stadia worden opgesteld. In de eerste fase werd de eerste groep klanten van Target bijgewerkt naar de gebruikersinterface van de nieuwe aanbiedingen. De volgende stadia zullen de resterende klanten bevorderen.

Met behulp van het nieuwste ontwerpsysteem van [!DNL Adobe Spectrum] worden inconsistente ontwerppatronen gestandaardiseerd en worden nieuwe verbeteringen geïntroduceerd, waaronder:

* **Bulk aanbiedt beheer**: Selecteer en schrap of beweeg veelvoudige aanbiedingen gelijktijdig.

* **[!UICONTROL Code Editor]upgrades** : Vernieuwde HTML- en JSON-editors met syntaxismarkering en regelnummering.

* **Verbeterde aanbiedingskaarten**: Verbeterde snelle informatie en detailkaarten voor gemakkelijkere informatietoegang.

* **Persistent onderzoek en filters**: Voegt zitting-blijvend onderzoek en filteropties toe.

Voor meer informatie zie [ Aanbiedingen ](/help/main/c-experiences/c-manage-content/manage-content.md) en subartikelen in deze sectie. Alle artikelen voor aanbiedingen in deze sectie zijn bijgewerkt met deze wijzigingen in de gebruikersinterface.

Hier volgt een korte video waarin de wijzigingen in deze release worden belicht:

![ aanbiedingen UI verfrist video ](/help/main/r-release-notes/assets/offers-video-v2.gif)

## [!DNL Adobe Experience Platform Web SDK] `__view__` bereik optimaliseren (22 oktober 2024)

Tussen 22 juli 2024 en 15 augustus 2024 heeft het team van [!DNL Target] het bereik van `__view__` geoptimaliseerd, wat de nauwkeurigheid van het weergeven van activiteiten, het bezoek en het melden van bezoekers vergroot. Deze optimalisatie is bedoeld om automatisch rapportagegegevens vast te leggen voor automatisch gegenereerde voorstellingen en moet voor de meeste accounts transparant zijn.

Deze optimalisatie is ingeschakeld voor alle nieuwe klanten van [!DNL Adobe Experience Platform Web SDK] . Klanten die van at.js zijn gemigreerd en de onderstaande implementatiestappen niet hebben uitgevoerd, hebben de optimalisatie echter uitgeschakeld. We dringen er bij deze klanten op aan hun implementaties vóór 3 februari 2025 te evalueren. Na deze datum, zullen wij optimalisering voor alle klanten toelaten. Als de implementaties niet tegen die tijd worden geëvalueerd en aangepast, kan dit gevolgen hebben voor rapporten, zoals hieronder wordt vermeld. Neem contact op met [!DNL Adobe Customer Care] als u wilt bevestigen of de implementatie wordt beïnvloed of als u meer tijd nodig hebt om uw implementatie aan te passen.

>[!IMPORTANT]
>
>Als u uw implementatieoverzicht niet kunt voltooien en problemen op 3 februari 2025 kunt oplossen, kunt u een eenmalige verlenging van zes maanden aanvragen. Zorg ervoor dat uw verzoek uiterlijk op 31 januari 2025 wordt ingediend. Adobe beoordeelt en beslist over je aanvraag.

Om van deze optimalisering in het geval van manueel voorstel terug te winnen, herzie [[!DNL Platform Web SDK implementation] ](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk) {target=_blank} om ervoor te zorgen dat u berichten na manueel teruggevende ervaringen verzendt of wanneer het gebruiken van de `applyPropositions` methode (of de overeenkomstige [!DNL Launch] actie als helper) om ervaringen terug te geven.

De gemeenschappelijkste scenario&#39;s wanneer de ervaringen manueel worden teruggegeven omvatten:

* JSON-aanbiedingen gebruiken
* Een aangepast beslissingsbereik gebruiken in een activiteit die is gemaakt in de [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)
* `renderDecisions: true` niet gebruiken bij het ophalen van een activiteit die is gemaakt met de [!UICONTROL Form-Based Experience Composer] die het algemene bereik `__view__` gebruikt

Als de berichten niet zoals gedocumenteerd in [ worden uitgevoerd geven gepersonaliseerde inhoud ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content) {target=_blank} in de *gids van de Inzameling van Gegevens* terug, zou het melden van gegevens in [!DNL Target] en in [ Analytics voor Doel kunnen ontbreken die ](/help/main/c-integrating-target-with-mac/a4t/a4t.md) rapporteert (A4T). In bepaalde scenario&#39;s, zou u een onjuiste verkeerspleet kunnen opmerken omdat de rapporteringsgegevens niet worden gevangen. In andere scenario&#39;s wordt dezelfde gebeurtenis herhaaldelijk gerapporteerd.

Afhankelijk van uw implementatie, controleer [!DNL Analytics] en A4T rapporteringsgevolgen.

[!DNL Platform Web SDK] steunt twee implementatietypen voor het teruggeven ervaringen en verpersoonlijkingen:

* **Enige vraag voor verpersoonlijking en meting.**

  Aanvankelijk geadviseerd, is de enige-vraag benadering voor [!DNL Platform Web SDK] gepland om in plaats van de spleet-vraag benadering te worden vervangen. Adobe adviseert alle nieuwe implementaties om de nieuwe spleet-vraag benadering te gebruiken en adviseert dat de bestaande klanten overgang aan de spleet-vraagmethode eveneens.

  Als u de methode voor één aanroep blijft gebruiken, kunnen de volgende onverwachte wijzigingen in uw [!DNL Analytics] -rapporten optreden:

   * Een dip in de bellen.
   * A4T en [!UICONTROL Page View] raken niet samengebonden, die het lastig maken om bepaalde uitsplitsingen en correlaties van uw A4T- rapporten uit te voeren gebruikend [!DNL Analytics] gebeurtenissen en gebeurtenissen.

* **Gesplitste vraag (die ook als bovenkant en bodem van paginagebeurtenissen wordt bekend).**

  Dit implementatietype is de nieuwe [ spleet-vraag implementatiebenadering ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events) {target=_blank} geadviseerd door [!DNL Adobe]. Met deze methode heeft de nieuwe optimalisatie geen invloed op [!DNL Analytics] - of A4T-rapporten.

Als u vragen hebt, contacteer ](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C) de Zorg van de Klant van 0} Adobe. [ (kB-2179)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html) {target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html) {target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html) {target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
