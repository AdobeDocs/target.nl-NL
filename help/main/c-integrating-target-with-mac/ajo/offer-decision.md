---
keywords: visuele ervaringscomposer-opties;beleving composer-opties;ervaringsopties;bied beslissing aan;offer decisioning;ajo;optimaliseer de reis
description: Meer informatie over het toevoegen van een beslissing over voorstellen die is gemaakt in [!DNL Adobe Journey Optimizer] aan een activiteit.
title: Hoe gebruik ik beslissingen over aanbiedingen?
feature: Integrations
exl-id: cec46d5c-bb5e-4cc9-8785-370f158d3f8e
source-git-commit: c6e14884dd0972a2de8c659ddb7a6fd659d083fc
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Besluiten over aanbiedingen gebruiken

Gebruiken [!DNL Adobe Target] with [!DNL Adobe Journey Optimizer] biedt beslissingen om de volgende beste aanbieding voor uw bezoekers op internet en mobiel te bepalen en te leveren.

Aanbiedingsbesluiten toevoegen die zijn gemaakt in [!DNL Adobe Journey Optimizer] tot [!DNL Target] activiteiten (handboek [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting]) met behulp van [!UICONTROL Visual Experience Composer] (VEC) of de [!UICONTROL Form-Based Composer] om persoonlijke aanbiedingen te testen en te leveren aan uw bezoekers op uw binnenkomende kanalen aangedreven door [!DNL Target].

Meer informatie over [!DNL Adobe Journey Optimizer] en bied besluiten aan, zie de volgende onderwerpen in *[!DNL Journey Optimizer]* documentatie:

* [Aan de slag met Journey Optimizer](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)

* [Over Besluitbeheer](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html)

## Vereisten

Aanbiedingsbesluiten gebruiken in [!DNL Target]hebt u het volgende nodig:

* [!DNL Adobe Target Standard] of [!DNL Adobe Target Premium] geïmplementeerd met behulp van de [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}.

   De functie is niet beschikbaar tijdens de implementatie [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* [!DNL Adobe Journey Optimizer Ultimate] (AJO + Offer decisioning) of [!DNL Adobe Experience Platform] en de [!UICONTROL Offer Decisioning] toepassingsservice-invoegtoepassing.

## Gebruiksvoorbeelden

In het volgende voorbeeld wordt beschreven hoe u de [!DNL Target]/[!DNL Adobe Journey Optimizer] integratie om de besluiten van het aanbod te gebruiken in [!DNL Target] activiteiten:

### Sport

Als markator voor een sportieve ligging wilt u de inhoud op uw homepage (zowel op de website voor bureaublad als op de website voor mobiele apparaten) aanpassen. U wilt inhoud aanpassen op basis van meerdere dimensies en een aanbieding doen aan winkelgerelateerde franchise-producten. U bent geïnteresseerd in:

* Het favoriete team van de bezoeker
* Recente activiteiten van atleten/spelers (bijvoorbeeld teambewegingen, contractupdates of verwondingen)

U wilt bijvoorbeeld een persoonlijke ervaring bieden voor elk van de volgende gebieden: Dortmund, Frankfurt en Bochum en voor impliciete en expliciete fans van deze teams. Als metriek, wilt u bezoeken bekijken en aan de plaats van koopwaar klikken.

U wilt een [!UICONTROL A/B Test] activiteit (50/50 splitsing) tussen de standaardervaring en de gepersonaliseerde ervaring (die een aanbodbesluit met aanbiedingen voor elke regio en elk team omvat). U wilt deze activiteit gebruiken om de omzetting en de lift voor de gepersonaliseerde ervaring tegenover controle te bepalen.

### Spelstreamingplatforms

Als marketeer voor een gamingorganisatie wilt u een gepersonaliseerde aanbieding leveren voor een gamestreamingplatform voor desktopgebruikers en mobiele gebruikers uit verschillende geografische regio&#39;s: Duitsland, Frankrijk, Mexico en Brazilië. Wanneer een bezoeker de website voor bureaublad of mobiele apparaten opent vanuit een van deze regio&#39;s, wilt u een aanbieding voor streaming van games aanbieden in de lokale taal en met een overeenkomstige prijs voor de lokale valuta.

In [!DNL Adobe Journey Optimizer], kunt u een persoonlijk aanbod van de homepage held maken voor elk van de beoogde geografische gebieden, plus een fallback-aanbod met een standaard homepage-held. Vervolgens kunt u een besluit over het voorstel maken waarin deze aanbiedingen en de bijbehorende voorwaarden zijn opgenomen. Dan, binnen [!DNL Target]kunt u een [!DNL Experience Targeting] (XT) en voeg die beslissing toe op uw bureaublad of mobiele website om de persoonlijke ervaring aan bezoekers te leveren.

## Maak een ervaring die gebruikmaakt van een beslissing over een aanbieding:

1. Tijdens het bewerken of maken van een handleiding [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] (XT) in de [!UICONTROL Visual Experience Composer] (VEC), klikt u op een pagina-element om het [optiemenu](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   ![Het menu Opties in de Composer Visuele ervaring](assets/options-menu1.png)

   >[!NOTE]
   >
   >U kunt ook een ervaring maken die [!UICONTROL Offer Decisions] in de [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md).

1. Klikken **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]**, of **[!UICONTROL Replace Content]** en klik vervolgens op **[!UICONTROL Offer Decision]**.

   De [!UICONTROL Offer Decision] Deze optie is beschikbaar bij het bewerken of maken van [handmatig [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) of [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze optie is niet beschikbaar voor andere typen activiteiten. Welke opties beschikbaar zijn in het menu, is afhankelijk van het geselecteerde element.

   ![Het menu Opties in de Composer Visuele ervaring](assets/options-menu.png)

1. In de **[!UICONTROL Add Offer Decision]** selecteert u de gewenste sandbox en plaatsing.

   A [sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/overview.html){target=_blank} in the [!DNL Adobe Experience Platform] lets you partition your instance into virtual environments. For example, you might have a production environment and a staging environment. A [placement](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/create-components/creating-placements.html){target=_blank} in [!DNL Adobe Journey Optimizer] zorgt u ervoor dat de inhoud van het juiste aanbod op de juiste locatie wordt weergegeven.

   ![vervolgkeuzelijsten Sandbox en Placements in het dialoogvenster Adviseringsbesluit toevoegen](/help/main/c-integrating-target-with-mac/ajo/assets/sandbox-placement.png)

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

   ![Waarschuwingsbericht voor biedingsbeslissing](/help/main/c-integrating-target-with-mac/ajo/assets/offer-decision-warning.png)

## Opmerkingen en beperkingen

Neem de volgende informatie in overweging wanneer u met de beslissingen over aanbiedingen werkt:

* De integratie van de offer decisioning werkt voor [!DNL Target] op de [Adobe Experience Platform Web SDK](https://developer.adobe.com/target/implement/client-side/aep-web-sdk/){target=_blank}. Deze functie is niet beschikbaar tijdens de implementatie [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* De [!DNL Target]/[!DNL Adobe Journey Optimizer] integratie-ondersteuning [handmatig [!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md#types) en [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) (XT) alleen activiteiten. Deze functie is niet beschikbaar voor andere typen activiteiten.

* U kunt niet [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) als u aanbiedingsbesluiten in een activiteit gebruikt. Kies [!DNL Target] als bron voor de rapportage in de [!UICONTROL Goals and Settings] pagina tijdens activiteitenopstelling als u aanbiedingsbesluiten in de activiteit gebruikt.

* Aanbiedingen met het inhoudstype text/html bieden geen ondersteuning voor levering van inhoud via de URL. De deliveryURL wordt ondersteund via de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) alleen wanneer de client verantwoordelijk is voor het expliciet ophalen en samenstellen van de inhoud.

* [!DNL Target] rapportage biedt geen rapportage op het niveau van de biedingsbeschikking.

* Visualisatie [QA-koppelingen](/help/main/c-activities/c-activity-qa/activity-qa.md) for [!DNL Target] ervaringen met biedbeslissingen hebben invloed op de in [!DNL Adobe Journey Optimizer] voor deze biedingsbesluiten.
