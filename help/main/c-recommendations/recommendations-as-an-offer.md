---
keywords: Recommendations;aanbieding
description: Leer hoe u Adobe Recommendations kunt gebruiken als een aanbieding voor A/B-tests (inclusief automatisch toewijzen en automatisch richten) en Experience Targeting (XT)-activiteiten.
title: Hoe gebruik ik Recommendations als een voorstel bij andere soorten activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: ec520555-b439-46a9-ab2d-f0981532bffb
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Recommendations als voorstel

U kunt nu aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Druk automatisch het verkeer aan de best presterende aanbevelingen ervaring gebruikend [!UICONTROL Auto-Allocate].
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel [!UICONTROL Auto-Target].

Om aan de slag te gaan, maakt u een [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] activiteit met behulp van de [!UICONTROL Visual Experience Composer] en gebruiken de [!UICONTROL Insert Before], [!UICONTROL Insert After], of [!UICONTROL Replace With] actie om aanbevelingen aan een ervaring toe te voegen.

## Een aanbeveling toevoegen als een aanbieding in een A/B Test- of XT-activiteit

1. Start de driestapige geleide workflow met behulp van Visual Experience Composer (VEC) om een [A/B-test](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) of [Gericht op ervaring](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md) (XT) activiteit.

   >[!NOTE]
   >
   >Houd er bij A/B-tests rekening mee dat u de optie [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) optie om verkeer aan de best presterende aanbevelingen automatisch te duwen of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) optie om bezoekers op basis van hun profiel toe te wijzen aan specifieke aanbevelingen.

1. Tijdens het maken van een [ervaring](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md), klikt u op het element waaraan u een aanbeveling wilt toevoegen als een aanbieding, selecteert u de optie **[!UICONTROL Insert Before]**, **[!UICONTROL Insert After]**, of **[!UICONTROL Replace With]** actie, selecteert u vervolgens [!UICONTROL Recommendation].

   In de volgende afbeelding ziet u de [!UICONTROL Insert After > Recommendation] optie.

   ![Aanbeveling invoegen als een aanbieding](/help/main/c-recommendations/assets/replace-after-recommendations.png)

1. Selecteer een van de volgende opties om criteria voor populaire aanbevelingen per paginatype weer te geven:

   * Winkelpagina
   * Categoriepagina
   * Startpagina
   * Openingspagina
   * Productpagina
   * Pagina met zoekresultaten
   * Dankbriefje
   * Overige

1. Selecteer het gewenste [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md)en klik vervolgens op [!UICONTROL Next].
1. Selecteer het gewenste [ontwerp](/help/main/c-recommendations/c-design-overview/design-overview.md)en klik vervolgens op [!UICONTROL Next].
1. In de [!UICONTROL Options] geeft u het volgende op:

   * Kies een [collectie](/help/main/c-recommendations/c-products/collections.md).
   * Configureer de [Aanbieding aan de voorzijde en achterzijde](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md) opties, indien nodig.

1. Klik op [!UICONTROL Save].
1. Voltooi de configuratie van de A/B Test- of XT-activiteit met behulp van de driedelige geleide workflow.

## De configuratie van een aanbevolen aanbieding bewerken

Er zijn twee manieren u de configuratie van een aanbieding kunt uitgeven:

* Met de [!UICONTROL Edit] menu
* Met de [!UICONTROL Modifications] deelvenster

### Een aantal aanbevelingen bewerken via het menu Bewerken

1. Klik op het voorstel dat u wilt bewerken en klik vervolgens op **[!UICONTROL Edit]**.

   ![Aanbevelingen bewerken](/help/main/c-recommendations/assets/recs-offer-edit.png)

1. Kies een van de volgende opties:

   * [Criteria wijzigen](/help/main/c-recommendations/c-algorithms/algorithms.md)
   * [Ontwerp wijzigen](/help/main/c-recommendations/c-design-overview/design-overview.md)
   * [Verzameling wijzigen](/help/main/c-recommendations/c-products/collections.md)
   * [Aanbieding wijzigen](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md)

1. Breng de gewenste wijzigingen aan.

### Een aantal aanbevelingen bewerken via het deelvenster Wijzigingen

1. Klik op de knop [!UICONTROL Modifications] pictogram  **( `</>` )** om de [Wijzigingen](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) venster.
1. Houd de muisaanwijzer boven de gewenste handeling en klik vervolgens op de knop **[!UICONTROL Edit]** pictogram.

   ![Deelvenster Wijzigingen](/help/main/c-recommendations/assets/recs-offer-modifications.png)

1. Breng de gewenste wijzigingen aan.

## Een voorstel voor aanbevelingen verwijderen

U kunt een aanbevolen versie op twee manieren verwijderen:

* Met de [!UICONTROL Edit] menu
* Met de [!UICONTROL Modifications] deelvenster

### Een aantal aanbevelingen verwijderen via het menu Bewerken

1. Klik op de aanbieding die u wilt verwijderen en klik vervolgens op **[!UICONTROL Layout > Remove]**.

   ![Verwijderen](/help/main/c-recommendations/assets/recs-offer-remove.png)

### Een aantal aanbevelingen verwijderen via het deelvenster Wijzigingen

1. Klik op de knop [!UICONTROL Modifications] pictogram **( &lt;/> )** om de [Wijzigingen](/help/main/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md) venster.
1. Houd de muisaanwijzer boven de gewenste handeling en klik vervolgens op de knop [!UICONTROL Delete] pictogram.

   ![Pictogram Verwijderen](/help/main/c-recommendations/assets/recs-offer-delete.png)

### De status van de aanbevolen aanbieding bekijken {#status}

De status (algoritme) van de aanbevolen aanbieding wordt onder aan het dialoogvenster [!UICONTROL Overview] pagina voor A/B Test- en XT-activiteiten die Recommendations-aanbiedingen bevatten:

* Resultaten gereed
* Resultaten niet gereed
* Feed-fout

![Status Recommendations-aanbieding](/help/main/c-recommendations/assets/recs-offer-status.png)

## Trainingsvideo: Recommendations als voorstel ![Overzicht badge](/help/main/assets/overview.png)

>[!VIDEO](https://video.tv.adobe.com/v/28878)
