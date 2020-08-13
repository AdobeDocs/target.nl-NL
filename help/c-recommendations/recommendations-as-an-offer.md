---
keywords: Recommendations;offer
description: Adobe Recommendations als een aanbieding in A/B-tests (inclusief automatisch toewijzen en automatisch richten) en Experience Targeting (XT)-activiteiten
title: Adobe Recommendations als een aanbieding in A/B-tests (inclusief automatisch toewijzen en automatisch richten) en Experience Targeting (XT)-activiteiten
feature: recs creation
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Recommendations als een aanbieding

U kunt nu aanbevelingen opnemen binnen [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Duw automatisch verkeer aan de best-presterende aanbevolen ervaring het gebruiken [!UICONTROL Auto-Allocate].
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel [!UICONTROL Auto-Target].

Om te beginnen, creeer een [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] activiteit gebruikend [!UICONTROL Visual Experience Composer] en gebruik [!UICONTROL Insert Before], [!UICONTROL Insert After], of [!UICONTROL Replace With] actie om aanbevelingen aan een ervaring toe te voegen.

## Een aanbeveling toevoegen als een aanbieding in een A/B Test- of XT-activiteit

1. Start de driestappenworkflow met instructies met behulp van Visual Experience Composer (VEC) voor het maken van een [A/B Test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) of [Experience Targeting](/help/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT)-activiteit.

   >[!NOTE]
   >
   >Voor tests A/B, herinner dat u de [auto-Wijs](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) optie kunt kiezen om verkeer aan de best-presterende aanbevelingen automatisch te duwen of de [auto-Doel](/help/c-activities/auto-target-to-optimize.md) optie om bezoekers aan op maat gemaakte aanbevelingen toe te wijzen die op hun profiel worden gebaseerd.

1. Tijdens het creëren van een [ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md), klik het element u een aanbeveling aan als aanbieding wilt toevoegen, selecteren **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]**, of **[!UICONTROL Replace With]** actie, dan selecteren [!UICONTROL Recommendation].

   In de volgende afbeelding ziet u de [!UICONTROL Insert After > Recommendation] optie.

   ![Aanbeveling invoegen als een aanbieding](/help/c-recommendations/assets/replace-after-recommendations.png)

1. Selecteer een van de volgende opties om criteria voor populaire aanbevelingen per paginatype weer te geven:

   * Winkelpagina
   * Categoriepagina
   * Startpagina
   * Openingspagina
   * Productpagina
   * Pagina met zoekresultaten
   * Dankbriefje
   * Overige

1. Selecteer de gewenste [criteria](/help/c-recommendations/c-algorithms/algorithms.md)en klik op [!UICONTROL Next].
1. Selecteer het gewenste [ontwerp](/help/c-recommendations/c-design-overview/design-overview.md)en klik op [!UICONTROL Next].
1. Geef in het [!UICONTROL Options] dialoogvenster het volgende op:

   * Kies een [verzameling](/help/c-recommendations/c-products/collections.md).
   * Configureer desgewenst de opties [Aanbieding](/help/c-recommendations/t-create-recs-activity/adding-promotions.md) voor- en achterkant.

1. Klik op [!UICONTROL Save].
1. Voltooi de configuratie van de A/B Test- of XT-activiteit met behulp van de driedelige geleide workflow.

## De configuratie van een aanbevolen aanbieding bewerken

Er zijn twee manieren u de configuratie van een aanbieding kunt uitgeven:

* Het [!UICONTROL Edit] menu gebruiken
* Het [!UICONTROL Modifications] deelvenster gebruiken

### Aanbevelingen bewerken via het menu Bewerken

1. Klik op het voorstel dat u wilt bewerken en klik vervolgens op **[!UICONTROL Edit]**.

   ![Aanbevelingen bewerken](/help/c-recommendations/assets/recs-offer-edit.png)

1. Kies een van de volgende opties:

   * [Criteria wijzigen](/help/c-recommendations/c-algorithms/algorithms.md)
   * [Ontwerp wijzigen](/help/c-recommendations/c-design-overview/design-overview.md)
   * [Verzameling wijzigen](/help/c-recommendations/c-products/collections.md)
   * [Aanbieding wijzigen](/help/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Breng de gewenste wijzigingen aan.

### Een aantal aanbevelingen bewerken via het deelvenster Wijzigingen

1. Klik op het [!UICONTROL Modifications] pictogram **(`</>`)** om het deelvenster [Wijzigingen](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) weer te geven.
1. Houd de muisaanwijzer boven de gewenste handeling en klik op het **[!UICONTROL Edit]** pictogram.

   ![Deelvenster Wijzigingen](/help/c-recommendations/assets/recs-offer-modifications.png)

1. Breng de gewenste wijzigingen aan.

## Een voorstel voor aanbevelingen verwijderen

U kunt een aanbevolen versie op twee manieren verwijderen:

* Het [!UICONTROL Edit] menu gebruiken
* Het [!UICONTROL Modifications] deelvenster gebruiken

### Een aantal aanbevelingen verwijderen via het menu Bewerken

1. Klik op het voorstel dat u wilt verwijderen en klik vervolgens op **[!UICONTROL Layout > Remove]**.

   ![Verwijderen](/help/c-recommendations/assets/recs-offer-remove.png)

### Een aantal aanbevelingen verwijderen via het deelvenster Wijzigingen

1. Klik op het [!UICONTROL Modifications] pictogram **( &lt;/> )** om het deelvenster [Wijzigingen](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) weer te geven.
1. Houd de muisaanwijzer boven de gewenste handeling en klik op het [!UICONTROL Delete] pictogram.

   ![Pictogram Verwijderen](/help/c-recommendations/assets/recs-offer-delete.png)

### De status van de aanbevolen aanbieding bekijken {#status}

De aanbevelingen bieden (algoritme) status aan vertoningen bij de bodem van de [!UICONTROL Overview] pagina voor A/B Test en XT activiteiten die de aanbiedingen van Recommendations bevatten:

* Resultaten gereed
* Resultaten niet gereed
* Feed-fout

![Status Recommendations-aanbieding](/help/c-recommendations/assets/recs-offer-status.png)

## Trainingsvideo: Recommendations als ![overzichtsbadge voor aanbieding](/help/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)