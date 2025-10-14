---
keywords: Aanbevelingen;aanbieding
description: Leer hoe u Adobe Recommendations kunt gebruiken als een aanbieding voor A/B-tests (inclusief automatisch toewijzen en automatisch richten) en Experience Targeting (XT)-activiteiten.
title: Hoe gebruik ik Aanbevelingen als Voorstel in Andere Types van Activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 3821d868f45b85d2f6f0e204f9828544b759067b
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Aanbevelingen als voorstel

U kunt nu aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Met [!UICONTROL Auto-Allocate] wordt het verkeer automatisch naar de best presterende aanbevelingen verschoven.
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel met [!UICONTROL Auto-Target] .

Als u aan de slag wilt gaan, maakt u een [!UICONTROL A/B Test] - of [!UICONTROL Experience Targeting] -activiteit met behulp van [!UICONTROL Visual Experience Composer] en gebruikt u de handeling [!UICONTROL Recommend] om aanbevelingen aan een ervaring toe te voegen.

## Een aanbeveling toevoegen als een aanbieding in een A/B Test- of XT-activiteit

1. Begin het drie-stap geleide werkschema gebruikend de Visuele Composer van de Ervaring (VEC) om een [&#x200B; A/B Test &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) of [&#x200B; Begeleidende Begeleidende &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activiteit tot stand te brengen.

   >[!NOTE]
   >
   >Voor Tests A/B, herinner dat u [&#x200B; auto-toewijs &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) optie kunt kiezen om verkeer aan de best-presterende aanbevelingen of de [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) optie automatisch te duwen om bezoekers aan op maat gemaakte aanbevelingen toe te wijzen ervaringen die op hun profiel worden gebaseerd.

1. Terwijl het creëren van een [&#x200B; ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), klik het element u een aanbeveling aan als aanbieding wilt toevoegen, klik **[!UICONTROL Replace Content]** ( ![&#x200B; vervangt het pictogram van de Inhoud &#x200B;](/help/main/assets/icons/Switch.svg)), dan selecteren **[!UICONTROL Recommendation]**.

   ![&#x200B; aanbeveling van het Tussenvoegsel als aanbieding &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/recs-as-offer.png)

1. Klik in de [!UICONTROL Recommendation] -lus aan de rechterkant op **[!UICONTROL Select a Recommendation]** om het dialoogvenster [!UICONTROL Select Criteria] weer te geven.

1. Klik op **[!UICONTROL Create Criteria]** of selecteer een bestaand criterium.

1. (Facultatief) klik het **[!UICONTROL Filter]** pictogram ( ![&#x200B; pictogram van de Filter &#x200B;](/help/main/assets/icons/Filter.svg) ) om van de volgende opties te selecteren om populaire aanbevelingen criteria door paginatype te bekijken:

   * Winkelpagina
   * Categoriepagina
   * Startpagina
   * Openingspagina
   * Productpagina
   * Pagina met zoekresultaten
   * Dankbriefje
   * Overige

1. Klik **[!UICONTROL Create Criteria]** of selecteer bestaande [&#x200B; criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md), dan klik **[!UICONTROL Next]** om de [!UICONTROL Select Design] dialoogdoos te tonen.

1. Klik **[!UICONTROL Create Design]** of selecteer een bestaand [&#x200B; ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/design-overview.md), dan klik **[!UICONTROL &#x200B; Next]**.

1. Geef in het dialoogvenster [!UICONTROL Options] het volgende op:

   * Kies a [&#x200B; inzameling &#x200B;](/help/main/c-recommendations/c-products/collections.md).
   * Vorm de [&#x200B; Voorste Bevordering en de Achteropties van de Bevordering &#x200B;](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md), zonodig.

1. Klik op **[!UICONTROL Save]**.
1. Voltooi de configuratie van de A/B Test- of XT-activiteit met behulp van de driedelige geleide workflow.

## De configuratie van een aanbevolen aanbieding bewerken

1. Van het [!UICONTROL Recommendation] spoor, klik het **[!UICONTROL Edit]** pictogram ( ![&#x200B; geef pictogram &#x200B;](/help/main/assets/icons/Edit.svg)) naast [!UICONTROL Criteria Name] uit, [!UICONTROL Design Name], of [!UICONTROL Collection Name] om het element te veranderen.

## Een voorstel voor aanbevelingen verwijderen

1. Klik het **[!UICONTROL Delete]** pictogram ( ![&#x200B; pictogram van de Schrapping &#x200B;](/help/main/assets/icons/Delete.svg)) bij de bovenkant van het [!UICONTROL Recommendation] paneel.

### De status van de aanbevolen aanbieding bekijken {#status}

De aanbevelingen (algoritme) statusvertoningen bij de bodem van de activiteit [!UICONTROL Overview] pagina voor A/B Test en XT activiteiten aan die de aanbiedingen van Aanbevelingen bevatten:

* Resultaten gereed
* Resultaten niet gereed
* Feed-fout
