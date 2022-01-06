---
keywords: visuele ervaringscomposer-opties;beleving composer-opties;ervaringsopties;bied beslissing aan;offer decisioning;ajo;optimaliseer de reis
description: Meer informatie over het toevoegen van een beslissing over voorstellen die is gemaakt in [!DNL Adobe Journey Optimizer] aan een activiteit.
title: 'Hoe gebruik ik beslissingen over aanbiedingen? '
feature: Visual Experience Composer (VEC)
source-git-commit: 39d278747cec838ef7855116c820e3c80160d364
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Besluiten over aanbiedingen gebruiken

Gebruiken [!DNL Adobe Target] with [!DNL Adobe Journey Optimizer] biedt beslissingen om de volgende beste aanbieding voor uw bezoekers op internet en mobiel te bepalen en te leveren.

Aanbiedingsbesluiten toevoegen die zijn gemaakt in [!DNL Adobe Journey Optimizer] tot [!DNL Target] activiteiten (handboek [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting]) met behulp van [!UICONTROL Visual Experience Composer] (VEC) of de [!UICONTROL Form-Based Composer] om persoonlijke aanbiedingen te testen en te leveren aan uw bezoekers op uw binnenkomende kanalen aangedreven door [!DNL Target].

>[!NOTE]
>
>De functionaliteit van de aanbieding die in dit onderwerp wordt beschreven is gepland om 13 Januari, 2022 met te worden vrijgegeven [!DNL Target Standard/Premium] Release 22.1.1.

Meer informatie over [!DNL Adobe Journey Optimizer], zie [Aan de slag met Journey Optimizer](https://experienceleague-review.corp.adobe.com/docs/journey-optimizer/using/get-started/get-started.html) in de *Journey Optimizer* documentatie.

Voor meer informatie over biedingsbesluiten, zie [Over Besluitbeheer](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/get-started/starting-offer-decisioning.html) in de *[!DNL Journey Optimizer]documentatie*.

## Vereisten

Aanbiedingsbesluiten gebruiken in [!DNL Target]hebt u het volgende nodig:

* [!DNL Adobe Target Standard] of [!DNL Adobe Target Premium] geïmplementeerd met behulp van de [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md).

   De functie is niet beschikbaar tijdens de implementatie [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* [!DNL Adobe Journey Optimizer Ultimate] (AJ0 + Offer decisioning) of [!DNL Adobe Experience Platform] en de [!UICONTROL Offer Decisioning] toepassingsservice-invoegtoepassing.

## Gebruiksvoorbeelden

In het volgende voorbeeld wordt beschreven hoe u de [!DNL Target]/[!DNL Adobe Journey Optimizer] integratie om de besluiten van het aanbod te gebruiken in [!DNL Target] activiteiten:

### Sport

Als markator voor een sportieve ligging wilt u de inhoud op uw homepage (zowel op de website voor bureaublad als op de website voor mobiele apparaten) aanpassen. U wilt inhoud personaliseren op basis van het favoriete team van de bezoeker en de recente speler probeert hen een aanbieding te presenteren aan winkelgerelateerde franchiseproducten. Bijvoorbeeld, om een gepersonaliseerde ervaring voor elk van de volgende gebieden te leveren: Dortmund, Frankfurt en Bochum en voor impliciete en expliciete fans van deze teams. Als metriek, wilt u bezoeken bekijken en aan de plaats van koopwaar klikken.

U wilt een activiteit van de Test A/B (50/50 splitsing) tussen de standaardervaring en de gepersonaliseerde ervaring (die een aanbiedingsbesluit met aanbiedingen voor elke regio en team omvat) ontwerpen. U wilt deze activiteit gebruiken om de omzetting en de lift voor de gepersonaliseerde ervaring tegenover controle te bepalen.

### Spelstreamingplatforms

Als een marketeer voor een sportorganisatie, wilt u een gepersonaliseerde aanbieding voor een gamestreamingsplatform voor Desktop en mobiele gebruikers van verschillende aardrijkskundigen leveren: Duitsland, Frankrijk, Mexico en Brazilië. Wanneer een bezoeker de website voor bureaublad of mobiele apparaten opent vanuit een van deze regio&#39;s, wilt u een aanbieding voor streaming van games aanbieden in de lokale taal en met een overeenkomstige prijs voor de lokale valuta.

In [!DNL Adobe Journey Optimizer], kunt u een persoonlijk aanbod van de homepage held maken voor elk van de beoogde geografische gebieden, plus een fallback-aanbod met een standaard homepage-held. Vervolgens kunt u een besluit over het voorstel maken waarin deze aanbiedingen en de bijbehorende voorwaarden zijn opgenomen. Dan, binnen [!DNL Target]kunt u een [!DNL Experience Targeting] (XT) en voeg die beslissing toe op uw bureaublad of mobiele website om de persoonlijke ervaring aan bezoekers te leveren.

## Maak een ervaring die gebruikmaakt van een beslissing over een aanbieding:

1. Tijdens het bewerken of maken van een handleiding [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] (XT) in de [!UICONTROL Visual Experience Composer] (VEC), klikt u op een pagina-element om het [optiemenu](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![Het menu Opties in de Composer Visuele ervaring](assets/options-menu1.png)

   >[!NOTE]
   >
   >U kunt ook een ervaring maken die [!UICONTROL Offer Decisions] in de [[!UICONTROL Form-Based Experience Composer]](/help/c-experiences/form-experience-composer.md).

1. Klikken **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]**, of **[!UICONTROL Replace Content]** en klik vervolgens op **[!UICONTROL Offer Decision]**.

   De [!UICONTROL Offer Decision] Deze optie is beschikbaar bij het bewerken of maken van [handmatig [!UICONTROL A/B Test]](/help/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten. Welke opties beschikbaar zijn in het menu, is afhankelijk van het geselecteerde element.

   ![Het menu Opties in de Composer Visuele ervaring](assets/options-menu.png)

1. In de **[!UICONTROL Add Offer Decision]** selecteert u de gewenste sandbox en plaatsing.

   A [sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} in het dialoogvenster [!DNL Adobe Experience Platform] Hiermee kunt u uw instantie in virtuele omgevingen verdelen. U hebt bijvoorbeeld een productieomgeving en een testomgeving. A [plaatsing](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioniong/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] zorgt u ervoor dat de inhoud van het juiste aanbod op de juiste locatie wordt weergegeven.

   ![vervolgkeuzelijsten Sandbox en Placements in het dialoogvenster Adviseringsbesluit toevoegen](/help/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

1. Selecteer het gewenste aanbiedingsbesluit en klik op **[!UICONTROL Create]**.

   ![Geselecteerde biedingsbeslissing in het dialoogvenster Besluit voorstel toevoegen](assets/offer-decision.png)

   Uw website wordt weergegeven in de VEC waar u het nieuwe besluit over het voorstel kunt bekijken in het dialoogvenster [!UICONTROL Modifications] aan de rechterkant. U kunt de muisaanwijzer boven de wijziging plaatsen en op de knop [!UICONTROL Preview] pictogram om het besluit over het voorstel te bekijken.

   ![Pictogram Voorvertoning](assets/preview-icon.png)

   U kunt de verschillende aanbiedingen in de aanbieding bekijken door op het desbetreffende pictogram onder aan het dialoogvenster [!UICONTROL Offer Preview] , inclusief de fallback-aanbieding. Een fallback-aanbieding is de standaardaanbieding die wordt weergegeven wanneer een bezoeker niet in aanmerking komt voor een van de persoonlijke aanbiedingen in de collectie.

   ![Voorvertoning voorstel](assets/offer-preview.png)

1. Voltooi het maken van de activiteit door het dialoogvenster [!UICONTROL Targeting] en [!UICONTROL Goals & Settings] stappen van de driedelige geleide workflow.

   >[!IMPORTANT]
   >
   >Om ervoor te zorgen dat [!DNL Target] de activiteit wordt gepersonaliseerd, zorg ervoor de huidige begin/einddata van de activiteit synchroon zijn met de begin/einddata van de biedingsbeslissing in [!DNL Adobe Journey Optimizer]. Als de [!DNL Target] start-/einddatums vallen buiten het begin-/einddatumbereik van het besluit van de aanbieding, de standaarddatum [!DNL Target] inhoud wordt weergegeven voor bezoekers.

   ![Waarschuwingsbericht voor biedingsbeslissing](/help/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## Opmerkingen en beperkingen

Houd rekening met de volgende opmerkingen en beperkingen wanneer u werkt met beslissingen over aanbiedingen:

* De integratie van de offer decisioning werkt voor [!DNL Target] op de [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md). Deze functie is niet beschikbaar tijdens de implementatie [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* De integratie tussen Doel en Adobe Journey Optimizer ondersteunt [handmatig [!UICONTROL A/B Test]](/help/c-activities/t-test-ab/test-ab.md#types) en [[!UICONTROL Experience Targeting]](/help/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze functie is niet beschikbaar voor andere typen activiteiten.

* Aanbiedingen met het inhoudstype text/html bieden geen ondersteuning voor levering van inhoud via de URL. De deliveryURL wordt alleen ondersteund via de Form-Based Experience Composer wanneer de client verantwoordelijk is voor het expliciet ophalen en samenstellen van de inhoud.

* [!DNL Target] rapportage biedt geen rapportage op het niveau van de biedingsbeschikking.

* Visualisatie [QA-koppelingen](/help/c-activities/c-activity-qa/activity-qa.md) for [!DNL Target] ervaringen met biedbeslissingen hebben invloed op de in [!DNL Adobe Journey Optimizer] voor deze biedingsbesluiten.








