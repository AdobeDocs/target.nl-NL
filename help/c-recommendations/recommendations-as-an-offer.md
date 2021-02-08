---
keywords: Recommendations;aanbieding
description: Leer hoe u Adobe Recommendations kunt gebruiken als een aanbieding voor A/B-tests (inclusief automatisch toewijzen en automatisch richten) en Experience Targeting (XT)-activiteiten.
title: Hoe gebruik ik Recommendations als een voorstel in andere soorten activiteiten?
feature: Recommendations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMR-aanbevelingen als een aanbieding

U kunt nu aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Druk automatisch het verkeer naar de best-presterende aanbevelingen ervaring gebruikend [!UICONTROL Auto-Allocate].
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel met [!UICONTROL Auto-Target].

Als u aan de slag wilt gaan, maakt u een [!UICONTROL A/B Test]- of [!UICONTROL Experience Targeting]-activiteit met behulp van [!UICONTROL Visual Experience Composer] en gebruikt u de handeling [!UICONTROL Insert Before], [!UICONTROL Insert After] of [!UICONTROL Replace With] om aanbevelingen aan een ervaring toe te voegen.

## Een aanbeveling toevoegen als een aanbieding in een A/B Test- of XT-activiteit

1. Start de workflow met instructies in drie stappen met behulp van Visual Experience Composer (VEC) om een [A/B Test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) of [Experience Targeting](/help/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activiteit te maken.

   >[!NOTE]
   >
   >Houd er bij A/B-tests rekening mee dat u de optie [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) kunt kiezen om automatisch het verkeer aan de best presterende aanbevelingen te onderwerpen of de optie [Automatisch doel](/help/c-activities/auto-target/auto-target-to-optimize.md) om bezoekers toe te wijzen aan op maat gemaakte aanbevelingen op basis van hun profiel.

1. Tijdens het creëren van [ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md), klik het element u een aanbeveling aan als aanbieding wilt toevoegen, selecteer **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]**, of **[!UICONTROL Replace With]** actie, dan uitgezocht [!UICONTROL Recommendation].

   In de volgende afbeelding ziet u de optie [!UICONTROL Insert After > Recommendation].

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

1. Selecteer de gewenste [criteria](/help/c-recommendations/c-algorithms/algorithms.md), dan klik [!UICONTROL Next].
1. Selecteer het gewenste [ontwerp](/help/c-recommendations/c-design-overview/design-overview.md), dan klik [!UICONTROL Next].
1. Geef in het dialoogvenster [!UICONTROL Options] het volgende op:

   * Kies een [verzameling](/help/c-recommendations/c-products/collections.md).
   * Configureer desgewenst de opties [Aanbieding aan de voorzijde en Back Promotion](/help/c-recommendations/t-create-recs-activity/adding-promotions.md).

1. Klik op [!UICONTROL Save].
1. Voltooi de configuratie van de A/B Test- of XT-activiteit met behulp van de driedelige geleide workflow.

## De configuratie van een aanbevolen aanbieding bewerken

Er zijn twee manieren u de configuratie van een aanbieding kunt uitgeven:

* Het menu [!UICONTROL Edit] gebruiken
* Het deelvenster [!UICONTROL Modifications] gebruiken

### Een aantal aanbevelingen bewerken via het menu Bewerken

1. Klik op de aanbieding die u wilt bewerken en klik op **[!UICONTROL Edit]**.

   ![Aanbevelingen bewerken](/help/c-recommendations/assets/recs-offer-edit.png)

1. Kies een van de volgende opties:

   * [Criteria wijzigen](/help/c-recommendations/c-algorithms/algorithms.md)
   * [Ontwerp wijzigen](/help/c-recommendations/c-design-overview/design-overview.md)
   * [Verzameling wijzigen](/help/c-recommendations/c-products/collections.md)
   * [Aanbieding wijzigen](/help/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Breng de gewenste wijzigingen aan.

### Een aantal aanbevelingen bewerken via het deelvenster Wijzigingen

1. Klik op het [!UICONTROL Modifications]-pictogram **( `</>` )** om het venster [Modifications](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) weer te geven.
1. Houd de cursor boven de gewenste handeling en klik op het pictogram **[!UICONTROL Edit]**.

   ![Deelvenster Wijzigingen](/help/c-recommendations/assets/recs-offer-modifications.png)

1. Breng de gewenste wijzigingen aan.

## Een voorstel voor aanbevelingen verwijderen

U kunt een aanbevolen versie op twee manieren verwijderen:

* Het menu [!UICONTROL Edit] gebruiken
* Het deelvenster [!UICONTROL Modifications] gebruiken

### Een aantal aanbevelingen verwijderen via het menu Bewerken

1. Klik op de aanbieding die u wilt verwijderen en klik vervolgens op **[!UICONTROL Layout > Remove]**.

   ![Verwijderen](/help/c-recommendations/assets/recs-offer-remove.png)

### Een aantal aanbevelingen verwijderen via het deelvenster Wijzigingen

1. Klik op het [!UICONTROL Modifications]-pictogram **( &lt;/> )** om het venster [Modifications](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) weer te geven.
1. Houd de cursor boven de gewenste handeling en klik op het pictogram [!UICONTROL Delete].

   ![Pictogram Verwijderen](/help/c-recommendations/assets/recs-offer-delete.png)

### De status van de aanbevelingen bekijken {#status}

De aanbevelingen bieden (algoritme) status vertoningen bij de bodem van [!UICONTROL Overview] pagina voor A/B Test en XT activiteiten aan die de aanbiedingen van Recommendations bevatten:

* Resultaten gereed
* Resultaten niet gereed
* Feed-fout

![Status Recommendations-aanbieding](/help/c-recommendations/assets/recs-offer-status.png)

## Trainingsvideo: Recommendations als een aanbieding ![Beknopte badge](/help/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)