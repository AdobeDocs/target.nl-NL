---
keywords: mvt;multivariërende test;aanbiedingen;combinaties
description: Leer hoe te om [!UICONTROL Visual Experience Composer] (VEC) in Adobe  [!DNL Target]  te gebruiken om de aanbiedingen tot stand te brengen u in uw [!UICONTROL Multivariate Test] (MVT) wilt omvatten.
title: Hoe maak ik combinaties in een [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 8b5883de-de76-403d-ae20-c933a8665555
source-git-commit: 8f9c0ea65197fd639d463628e54db79db993c2da
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Combinaties maken

Gebruik [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om de aanbiedingen te maken die u in uw [!UICONTROL Multivariate Test] (MVT) wilt opnemen.

Voor meer informatie over het gebruiken van VEC om aanbiedingen tot stand te brengen en uit te geven, zie {de opties van Composer van de 1} Visuele Ervaring.[&#128279;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

>[!NOTE]
>
>U kunt op **[!UICONTROL Expand Selection]** klikken wanneer u objecten op de pagina selecteert om naast het oorspronkelijk geselecteerde element ook het bovenliggende element te selecteren. Wanneer u een bovenliggend element selecteert, worden alle onderliggende elementen van dat element automatisch geselecteerd. U kunt de selectie meerdere keren uitbreiden.
>
>U kunt de [&#x200B; weg van het DOM &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) ook gebruiken om elementen te navigeren.

## Afbeeldingsaanbiedingen {#section_A48333211DB149ED926AE467D0032914}

Test meerdere afbeeldingen die op een bepaalde locatie beschikbaar zijn om te bepalen welke afbeelding het meest succesvol is.

1. Klik op een afbeelding op de pagina en selecteer vervolgens **[!UICONTROL Change Image]** .

   ![&#x200B; de optie van het Beeld van de Verandering &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changeimage.png)

1. Selecteer alle afbeeldingen die u in de test wilt opnemen en klik op **[!UICONTROL Save]** .

   ![&#x200B; Uitgezochte de dialoogdoos van de Inhoud die wordt gebruikt om beelden toe te voegen &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/addimage.png)

Elke afbeelding wordt een aparte ervaring op die locatie.

## HTML-aanbiedingen {#section_DF016101AFA9412C9B99862C23DE77B1}

Test meerdere Text/HTML-aanbiedingen binnen een locatie om te bepalen welke aanbieding het meest succesvol is.

1. Klik op een Text/HTML-aanbieding op uw pagina en klik vervolgens op **[!UICONTROL Change Text/HTML]** .

   ![&#x200B; de Tekst van de Verandering/HTML &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/changehtml.png)

1. Klik op **[!UICONTROL Add Text/HTML Offer]**, geef een naam op voor de aanbieding en typ of plak de code voor de aanbieding voor Text/HTML.

   ![&#x200B; geef aanbiedingen &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/editoffers.png) uit

   Herhaal dit voor alle andere Text/HTML-aanbiedingen die u wilt opnemen.

1. Klik op **[!UICONTROL Save]**.

Elke Text/HTML-aanbieding wordt een aparte ervaring op die locatie.

## Aanbevolen procedures {#section_2E98C23D2F1A460FA732A31799CE6291}

* Neem niet meer locaties op dan nodig is voor de test. Elke ervaring die u in de test opneemt, verhoogt aanzienlijk de hoeveelheid verkeer en de tijd die nodig is om acceptabele resultaten te bereiken. Als u bijvoorbeeld pagina-elementen hebt met elk drie aanbiedingen, zijn er negen mogelijke combinaties (3x3). Drie elementen, waarbij twee mogelijke aanbiedingen bevatten en één twee aanbiedingen, bieden 18 opties (3x3x2). De aantallen stijgen substantieel met elk extra element en aanbod.
* Wanneer het creëren van multivariate tests, kunt u meer dan 10 percenten van ervaringen van de test uitsluiten, op voorwaarde dat u de waarschuwing erkent dat u dan off-line rapportering voor analyse moet gebruiken.
* Gebruik de voorvertoningsfuncties om ongewenste combinaties van inhoud te voorkomen. Je hebt bijvoorbeeld twee afbeeldingen die verschillende kortingen bieden op hetzelfde object of dezelfde service. Het weergeven van beide afbeeldingen op dezelfde pagina is onlogisch en kan tot verwarring leiden.
* Gebruik de [&#x200B; schatter van het Verkeer &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/traffic-estimator.md) om ervoor te zorgen dat uw test voor de hoeveelheid verkeer wordt ontworpen uw pagina ontvangt. Zorg ervoor dat de schatter van het Verkeer uw testconfiguratie het groene licht geeft zodat kunt u de resultaten krijgen u wenst.
* U moet ten minste drie elementen hebben om te testen. Als u minder hebt, stel een reeks tests A/B in werking.
* De alternatieven van elk element moeten aanzienlijk van elkaar verschillen.
* Hoewel niet vereist, is het een goede praktijk voor elk element om het zelfde aantal alternatieven te hebben.

