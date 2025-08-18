---
keywords: Aanbevelingen;aanbieding
description: Leer hoe u Adobe Recommendations kunt gebruiken als een aanbieding voor A/B-tests (inclusief automatisch toewijzen en automatisch richten) en Experience Targeting (XT)-activiteiten.
title: Hoe gebruik ik Aanbevelingen als Voorstel in Andere Types van Activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
source-git-commit: f848c79cb95009b5810a1707d04e548a57220e12
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Aanbevelingen als voorstel

U kunt nu aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Met [!UICONTROL Auto-Allocate] wordt het verkeer automatisch naar de best presterende aanbevelingen verschoven.
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel met [!UICONTROL Auto-Target] .

Als u aan de slag wilt gaan, maakt u een [!UICONTROL A/B Test] - of [!UICONTROL Experience Targeting] -activiteit met behulp van [!UICONTROL Visual Experience Composer] en gebruikt u de handeling [!UICONTROL Insert Before] , [!UICONTROL Insert After] of [!UICONTROL Replace With] om aanbevelingen aan een ervaring toe te voegen.

## Een aanbeveling toevoegen als een aanbieding in een A/B Test- of XT-activiteit

1. Begin het drie-stap geleide werkschema gebruikend de Visuele Composer van de Ervaring (VEC) om een [ A/B Test ](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) of [ Begeleidende Begeleidende ](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activiteit tot stand te brengen.

   >[!NOTE]
   >
   >Voor Tests A/B, herinner dat u [ auto-toewijs ](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) optie kunt kiezen om verkeer aan de best-presterende aanbevelingen of de [ auto-Doel ](/help/main/c-activities/auto-target/auto-target-to-optimize.md) optie automatisch te duwen om bezoekers aan op maat gemaakte aanbevelingen toe te wijzen ervaringen die op hun profiel worden gebaseerd.

1. Terwijl het creëren van een [ ervaring ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), klik het element u een aanbeveling aan als aanbieding wilt toevoegen, **[!UICONTROL Replace Content]** klikken, dan selecteren **[!UICONTROL Recommendation]**.

   ![ aanbeveling van het Tussenvoegsel als aanbieding ](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Selecteer een van de volgende opties om criteria voor populaire aanbevelingen per paginatype weer te geven:

   * Winkelpagina
   * Categoriepagina
   * Startpagina
   * Openingspagina
   * Productpagina
   * Pagina met zoekresultaten
   * Dankbriefje
   * Overige

1. Selecteer de gewenste [ criteria ](/help/main/c-recommendations/c-algorithms/algorithms.md), dan klik [!UICONTROL Next].
1. Selecteer het gewenste [ ontwerp ](/help/main/c-recommendations/c-design-overview/design-overview.md), dan klik [!UICONTROL Next].
1. Geef in het dialoogvenster [!UICONTROL Options] het volgende op:

   * Kies a [ inzameling ](/help/main/c-recommendations/c-products/collections.md).
   * Vorm de [ Voorste Bevordering en de Achteropties van de Bevordering ](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md), zonodig.

1. Klik op [!UICONTROL Save].
1. Voltooi de configuratie van de A/B Test- of XT-activiteit met behulp van de driedelige geleide workflow.

## De configuratie van een aanbevolen aanbieding bewerken

Er zijn twee manieren u de configuratie van een aanbieding kunt uitgeven:

* Het menu [!UICONTROL Edit] gebruiken
* Het deelvenster [!UICONTROL Modifications] gebruiken

### Een aantal aanbevelingen bewerken via het menu Bewerken

1. Klik op de aanbieding die u wilt bewerken en klik vervolgens op **[!UICONTROL Edit]** .

   ![ geef aanbevelingen uit aanbieden ](/help/main/c-recommendations/assets/recs-offer-edit.png)

1. Kies een van de volgende opties:

   * [Criteria wijzigen](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Ontwerp wijzigen](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Verzameling wijzigen](/help/main/c-recommendations/c-products/collections.md)
   * [Aanbieding wijzigen](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Breng de gewenste wijzigingen aan.

### Een aantal aanbevelingen bewerken via het deelvenster Wijzigingen

1. Klik het [!UICONTROL Modifications] pictogram **( `</>`)** om de [ ruit van Wijzigingen ](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) te tonen.
1. Houd de cursor boven de gewenste handeling en klik op het pictogram **[!UICONTROL Edit]** .

   ![ het paneel van Wijzigingen ](/help/main/c-recommendations/assets/recs-offer-modifications.png)

1. Breng de gewenste wijzigingen aan.

## Een voorstel voor aanbevelingen verwijderen

U kunt een aanbevolen versie op twee manieren verwijderen:

* Het menu [!UICONTROL Edit] gebruiken
* Het deelvenster [!UICONTROL Modifications] gebruiken

### Een aantal aanbevelingen verwijderen via het menu Bewerken

1. Klik op de aanbieding die u wilt verwijderen en klik vervolgens op **[!UICONTROL Layout > Remove]** .

   ![ verwijder ](/help/main/c-recommendations/assets/recs-offer-remove.png)

### Een aantal aanbevelingen verwijderen via het deelvenster Wijzigingen

1. Klik het [!UICONTROL Modifications] pictogram **( &lt;/>)** om de [ ruit van Wijzigingen ](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) te tonen.
1. Houd de cursor boven de gewenste handeling en klik op het pictogram [!UICONTROL Delete] .

   ![ pictogram van de Schrapping ](/help/main/c-recommendations/assets/recs-offer-delete.png)

### De status van de aanbevolen aanbieding bekijken {#status}

De status (algoritme) van de aanbevolen aanbieding wordt onder aan de pagina [!UICONTROL Overview] weergegeven voor A/B Test- en XT-activiteiten die de aanbevolen opties bevatten:

* Resultaten gereed
* Resultaten niet gereed
* Feed-fout

![ de aanbiedingsstatus van Aanbevelingen ](/help/main/c-recommendations/assets/recs-offer-status.png)

## De video van de opleiding: Aanbevelingen als de badge van het Overzicht van de aanbieding ![ ](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
