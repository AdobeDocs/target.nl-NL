---
description: Gebruik Visual Experience Composer (VEC) in Adobe Target om de aanbiedingen tot stand te brengen u in uw Multivariate Test (MVT) wilt omvatten.
title: Combinaties maken in MVT (Multivariate Tests) met Adobe Target
feature: mvt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---


# Combinaties maken{#create-combinations}

Gebruik Visual Experience Composer (VEC) in Adobe Target om de aanbiedingen tot stand te brengen u in uw Multivariate Test (MVT) wilt omvatten.

Voor meer informatie over het gebruiken van VEC om aanbiedingen tot stand te brengen en uit te geven, zie [Opties van Composer van de Visuele Ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

>[!NOTE]
>
>U kunt **[!UICONTROL Expand Selection]** klikken wanneer het selecteren van voorwerpen op de pagina om het ouderelement naast het oorspronkelijk geselecteerde element te selecteren. Wanneer u een bovenliggend element selecteert, worden alle onderliggende elementen van dat element automatisch geselecteerd. U kunt de selectie meerdere keren uitbreiden.
>
>U kunt ook het [DOM-pad](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) gebruiken om door elementen te navigeren.

## Afbeeldingsaanbiedingen {#section_A48333211DB149ED926AE467D0032914}

Test meerdere afbeeldingsmogelijkheden binnen een locatie om te bepalen welke afbeelding het meest succesvol is.

1. Klik op een afbeelding op de pagina en selecteer **[!UICONTROL Change Image]**.

   ![Afbeelding wijzigen, optie](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changeimage.png)

1. Selecteer alle afbeeldingen die u in de test wilt opnemen en klik op **[!UICONTROL Save]**.

   ![Dialoogvenster Inhoud selecteren voor het toevoegen van afbeeldingen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/addimage.png)

Elke afbeelding wordt een aparte ervaring op die locatie.

## HTML-aanbiedingen {#section_DF016101AFA9412C9B99862C23DE77B1}

Test meerdere Text/HTML-aanbiedingen binnen een locatie om te bepalen welke aanbieding het meest succesvol is.

1. Klik op een Text/HTML-aanbieding op uw pagina en klik vervolgens op **[!UICONTROL Change Text/HTML]**.

   ![Tekst/HTML wijzigen](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changehtml.png)

1. Klik op **[!UICONTROL Add Text/HTML Offer]**, geef een naam op voor de aanbieding en typ of plak de code voor de aanbieding voor Text/HTML.

   ![Aanbiedingen bewerken](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png)

   Herhaal dit voor alle extra Text/HTML-aanbiedingen die u wilt opnemen.

1. Klik op **[!UICONTROL Save]**.

Elke Text/HTML-aanbieding wordt een aparte ervaring op die locatie.

## Aanbevolen procedures {#section_2E98C23D2F1A460FA732A31799CE6291}

* Neem niet meer locaties op dan nodig is voor de test. Elke ervaring die u in de test opneemt, verhoogt aanzienlijk de hoeveelheid verkeer en de tijd die nodig is om acceptabele resultaten te bereiken. Als u bijvoorbeeld pagina-elementen hebt met elk drie aanbiedingen, zijn er negen mogelijke combinaties (3x3). Drie elementen, waarbij twee mogelijke aanbiedingen bevatten en één twee aanbiedingen, bieden 18 opties (3x3x2). De aantallen stijgen aanzienlijk met elk extra element en aanbod.
* Wanneer het creëren van multivariate tests, kunt u meer dan 10 percenten van ervaringen van de test nu uitsluiten, op voorwaarde dat u de waarschuwing erkent dat u dan off-line rapportering voor analyse moet gebruiken.
* Gebruik de voorvertoningsfuncties om ongewenste combinaties van inhoud te voorkomen. Je hebt bijvoorbeeld twee afbeeldingen die verschillende kortingen bieden op hetzelfde object of dezelfde service. Het weergeven van beide afbeeldingen op dezelfde pagina is onlogisch en kan tot verwarring leiden.
* Gebruik de schatter van het Verkeer om ervoor te zorgen dat uw test voor de hoeveelheid verkeer wordt ontworpen uw pagina ontvangt. Zorg ervoor de schatter van het Verkeer uw testconfiguratie het groene licht geeft zodat kunt u de resultaten krijgen u wenst.
* U moet ten minste drie elementen hebben om te testen. Als u minder hebt, stel een reeks tests A/B in werking.
* Aanbevolen wordt dat de alternatieven van elk element aanzienlijk van elkaar verschillen.
* Hoewel niet vereist, is het een goede praktijk voor elk element om het zelfde aantal alternatieven te hebben.

