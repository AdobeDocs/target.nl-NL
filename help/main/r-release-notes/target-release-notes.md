---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cf00d2e43b0d0746e4369fcc7933a79f465c9549
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatste bijgewerkte: 11 December, 2024**

>[!NOTE]
>
>Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel ](release-notes.md). [ De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!UICONTROL Offers Library] update gebruikersinterface (9 januari 2025)

Deze release werkt de gebruikersinterface van [!UICONTROL Offers Library] bij om de gebruikerservaring voor [!DNL Adobe Target] -gebruikers te verbeteren. Met behulp van het nieuwste ontwerpsysteem van [!DNL Adobe Spectrum] worden inconsistente ontwerppatronen gestandaardiseerd en worden nieuwe verbeteringen geïntroduceerd, waaronder:

* **Bulk aanbiedt beheer**: Selecteer en schrap veelvoudige aanbiedingen gelijktijdig.

* **[!UICONTROL Code Editor]upgrades** : vernieuwde HTML- en JSON-editors met syntaxismarkering en regelnummering.

* **Verbeterde aanbiedingskaarten**: Verbeterde snelle informatie en detailkaarten voor gemakkelijkere informatietoegang.

* **Persistent onderzoek en filters**: Voegt zitting-blijvend onderzoek en filteropties toe.

Vanaf 9 januari 2025 krijgen alle [!DNL Target] klanten toegang tot de nieuwe interface, met de optie om indien nodig terug te schakelen naar de huidige versie van de interface.

Hier volgt een korte video waarin de wijzigingen in deze release worden belicht:

![ aanbiedingen UI verfrist video ](/help/main/r-release-notes/assets/offers-video-v2.gif)

## [!DNL Adobe Experience Platform Web SDK] `__view__` bereik optimaliseren (22 oktober 2024)

Tussen 22 juli 2024 en 15 augustus 2024 heeft het team van [!DNL Target] het bereik van `__view__` geoptimaliseerd, wat de nauwkeurigheid van het weergeven van activiteiten, het bezoek en het melden van bezoekers vergroot. Deze optimalisatie is bedoeld om automatisch rapportagegegevens vast te leggen voor automatisch gegenereerde voorstellingen en moet voor de meeste accounts transparant zijn.

Deze optimalisatie is ingeschakeld voor alle nieuwe klanten van [!DNL Adobe Experience Platform Web SDK] . Klanten die van at.js zijn gemigreerd en de onderstaande implementatiestappen niet hebben uitgevoerd, hebben de optimalisatie echter uitgeschakeld. We dringen er bij deze klanten op aan hun implementaties vóór 3 februari 2025 te evalueren. Na deze datum, zullen wij optimalisering voor alle klanten toelaten. Als de implementaties niet tegen die tijd worden geëvalueerd en aangepast, kan dit gevolgen hebben voor rapporten, zoals hieronder wordt vermeld. Neem contact op met [!DNL Adobe Customer Care] als u wilt bevestigen of de implementatie wordt beïnvloed of als u meer tijd nodig hebt om uw implementatie aan te passen.

>[!IMPORTANT]
>
>Als u uw implementatieoverzicht niet kunt voltooien en problemen op 3 februari 2025 kunt oplossen, kunt u een eenmalige verlenging van zes maanden aanvragen. Zorg ervoor dat uw verzoek uiterlijk op 31 januari 2025 wordt ingediend. De Adobe zal uw verzoek beoordelen en beslissen.

Om van deze optimalisering in het geval van manueel voorstel terug te winnen, herzie [[!DNL Platform Web SDK implementation] ](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk) {target=_blank} om ervoor te zorgen dat u berichten na manueel teruggevende ervaringen verzendt of wanneer het gebruiken van de `applyPropositions` methode (of de overeenkomstige [!DNL Launch] actie als helper) om ervaringen terug te geven.

De gemeenschappelijkste scenario&#39;s wanneer de ervaringen manueel worden teruggegeven omvatten:

* JSON-aanbiedingen gebruiken
* Een aangepast beslissingsbereik gebruiken in een activiteit die is gemaakt in de [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)
* `renderDecisions: true` niet gebruiken bij het ophalen van een activiteit die is gemaakt met de [!UICONTROL Form-Based Experience Composer] die het algemene bereik `__view__` gebruikt

Als de berichten niet zoals gedocumenteerd in [ worden uitgevoerd geven gepersonaliseerde inhoud ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content) {target=_blank} in de *gids van de Inzameling van Gegevens* terug, zou het melden van gegevens in [!DNL Target] en in [ Analytics voor Doel kunnen ontbreken die ](/help/main/c-integrating-target-with-mac/a4t/a4t.md) rapporteert (A4T). In bepaalde scenario&#39;s, zou u een onjuiste verkeerspleet kunnen opmerken omdat de rapporteringsgegevens niet worden gevangen. In andere scenario&#39;s wordt dezelfde gebeurtenis herhaaldelijk gerapporteerd.

Afhankelijk van uw implementatie, controleer [!DNL Analytics] en A4T rapporteringsgevolgen.

[!DNL Platform Web SDK] steunt twee implementatietypen voor het teruggeven ervaringen en verpersoonlijkingen:

* **Enige vraag voor verpersoonlijking en meting.**

  Aanvankelijk geadviseerd, is de enige-vraag benadering voor [!DNL Platform Web SDK] gepland om in plaats van de spleet-vraag benadering te worden vervangen. De Adobe adviseert alle nieuwe implementaties om de nieuwe spleet-vraag benadering te gebruiken en adviseert dat de bestaande klantenovergang aan de spleet-vraagmethode eveneens.

  Als u de methode voor één aanroep blijft gebruiken, kunnen de volgende onverwachte wijzigingen in uw [!DNL Analytics] -rapporten optreden:

   * Een dip in de bellen.
   * A4T en [!UICONTROL Page View] raken niet samengebonden, die het lastig maken om bepaalde uitsplitsingen en correlaties van uw A4T- rapporten uit te voeren gebruikend [!DNL Analytics] gebeurtenissen en gebeurtenissen.

* **Gesplitste vraag (die ook als bovenkant en bodem van paginagebeurtenissen wordt bekend).**

  Dit implementatietype is de nieuwe [ spleet-vraag implementatiebenadering ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events) {target=_blank} geadviseerd door [!DNL Adobe]. Met deze methode heeft de nieuwe optimalisatie geen invloed op [!DNL Analytics] - of A4T-rapporten.

Als u vragen hebt, contacteer ](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C) de Zorg van de Klant van de Adobe [. (kB-2179)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: SDK van het Web van de Ervaring van het Platform van Adobe Target ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html) {target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
