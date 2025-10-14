---
keywords: ervaring;json;aem;adobe Experience Manager;exporteren naar adobe target;beleving, fragmenten;fragmenten;XF
description: Leer hoe te om  [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in  [!DNL Adobe Target]  activiteiten te gebruiken.
title: Hoe gebruik ik  [!DNL Adobe Experience Manager]  (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
source-git-commit: 51e484d54f4d318ea59fdfdb16d1ed7014abdfdb
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 0%

---

# AEM [!UICONTROL Experience Fragments]

Gebruik [!UICONTROL Experience Fragments] (XF&#39;s) die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] -activiteiten voor optimalisatie en personalisatie.

## Overwegingen

Houd rekening met het volgende terwijl u met AEM [!UICONTROL Experience Fragments] werkt in [!DNL Target] :

* Deze functie vereist dat u een [!DNL Adobe Experience Manager] (AEM)-klant bent. Voor meer informatie, zie [&#x200B; Vereisten &#x200B;](#section_AE6F0971E1574B3AA324003599B96E5A) hieronder.
* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn beschikbaar voor de volgende typen activiteiten:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn niet beschikbaar voor de volgende typen activiteiten:

   * [[!UICONTROL Multivariate Test] (MV)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* U kunt [!UICONTROL Experience Fragments] in [!DNL Target] activiteiten verbruiken gebruikend [&#x200B; Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md).

Meer over AEM [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] leren, zie [&#x200B; AEM [!UICONTROL Experience Fragments] en het overzicht van de Fragmenten van de Inhoud &#x200B;](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Vereisten {#requirements}

U moet de [!UICONTROL Experience Fragments] -functionaliteit binnen [!DNL Target] ontvangen. Daarnaast moet u [!DNL AEM] as a Cloud Service of [!DNL AEM] 6.4 (of hoger) gebruiken. Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

* [!DNL Adobe Experience Manager] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard] of [!DNL Adobe Target Premium] account

[!DNL Adobe Experience Manager] 6.3 en 6.4 hebben het einde van de levensduur bereikt en worden niet meer ondersteund (behalve voor klanten die uitgebreide ondersteuning hebben aangeschaft).

De Zorg van de Klant van Adobe Target van het contact [&#x200B; om de integratie toe te laten en u van authentificatiedetails te voorzien.](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

## [!UICONTROL Experience Fragments] maken en configureren in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Als u [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target] wilt gebruiken, moet u de volgende stappen uitvoeren:

### Stap 1: Integreer [!DNL AEM] met [!DNL Target]

Zie voor meer informatie:

* **AEM as a Cloud Service**: [&#x200B; Integrerend met Adobe Target &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target){target=_blank} in de *as a Cloud Service van Experience Manager* gids.
* **Adobe Developer**: [&#x200B; Integratie met Adobe Target gebruikend Adobe I/0 &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-target-ims-adobe-io.html?lang=nl-NL){target=_blank} in de *Beherende documentatie van de Gids van de Gebruiker*.
* **[!DNL AEM]6.5**: [&#x200B; Opting in Adobe Analytics en Adobe Target &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=nl-NL){target=_blank} in *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6.4**: [&#x200B; Opting in Adobe Analytics en Adobe Target &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=nl-NL){target=_blank} in *Adobe Experience Manager 6.4* documentatie.

### Stap 2: Maak het ervaringsfragment

[!UICONTROL Experience Fragments] worden gemaakt in [!DNL AEM] . Zie voor meer informatie:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments] &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=nl-NL){target=_blank} in de *as a Cloud Service van Experience Manager* gids.
* **[!DNL AEM]6.5**: [[!UICONTROL Experience Fragments] &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=nl-NL){target=_blank} in *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6.4**: [[!UICONTROL Experience Fragments] &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=nl-NL){target=_blank} in *Adobe Experience Manager 6.4* documentatie.

### Stap 3: Configureer [!DNL AEM] om de lus [!UICONTROL Experience Fragment] with [!DNL Target] te delen

1. Selecteer vanuit [!DNL AEM] de gewenste [!UICONTROL Experience Fragment] map of de bijbehorende map en klik op **[!UICONTROL Properties]** .
2. Klik op de tab **[!UICONTROL Cloud Services]** en selecteer vervolgens in de vervolgkeuzelijst **[!UICONTROL Cloud Service Configuration]** de optie **[!UICONTROL Adobe Target]** .

   Bij de vorige stap wordt ervan uitgegaan dat iemand in uw organisatie de configuratie [!DNL Adobe Target] heeft gemaakt.

3. Klik op **[!UICONTROL Save & Close]**.

### Stap 4: Publiceer de [!UICONTROL Experience Fragment] en exporteer deze naar [!DNL Target]

Afhankelijk van uw [!DNL AEM] versie, zie de volgende verbindingen voor geleidelijke instructies:

* **AEM as a Cloud Service**: [&#x200B; Exporterend [!UICONTROL Experience Fragments] aan Adobe Target &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target?lang=en){target=_blank} in de *as a Cloud Service van Experience Manager* gids.
* **[!DNL AEM]6.5**: [&#x200B; Exporterend een Fragment van de Ervaring aan Doel &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=nl-NL){target=_blank} in *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6.4**: [&#x200B; Exporterend een Fragment van de Ervaring aan Doel &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=nl-NL){target=_blank} in *Adobe Experience Manager 6.4* documentatie.

## [!UICONTROL Experience Fragments] gebruiken in [!DNL Target] -activiteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nadat u de voorgaande taken hebt uitgevoerd, wordt [!UICONTROL Experience Fragment] weergegeven op de [!UICONTROL Offers] pagina in [!DNL Target] .

[!DNL Target] zoekt momenteel naar [!UICONTROL Experience Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Experience Fragment] moet binnen tien minuten beschikbaar zijn in [!DNL Target] , maar dit tijdsbestek verkort de verdere ontwikkeling.

[!UICONTROL Experience Fragment] wordt geïmporteerd in [!DNL Target] als een HTML- of JSON-aanbieding. De [!UICONTROL Experience Fragment] &#39;primaire&#39; versie blijft in [!DNL AEM] . U kunt de [!UICONTROL Experience Fragment] in [!DNL Target] niet bewerken.

U kunt filteren en zoeken op [!UICONTROL HTML XFs] en [!UICONTROL JSON XFs] om u te helpen onderscheid te maken tussen [!UICONTROL Experience Fragment] typen die worden geëxporteerd naar [!DNL Target] .

![&#x200B; Filter door de types van Fragment van de Ervaring: HTML of JSON in het Doel UI &#x200B;](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

U kunt over [!UICONTROL Experience Fragment] in de lijst bewegen, dan het [!UICONTROL View] pictogram ![&#x200B; pictogram van Info &#x200B;](/help/main/assets/icons/InfoOutline.svg) klikken om extra informatie over [!UICONTROL Experience Fragment], met inbegrip van zijn [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path], en laatste wijzigingsinformatie te zien. Klik op [!UICONTROL [!UICONTROL View Full Details]] om de activiteiten te bekijken die naar deze aanbieding verwijzen.

![&#x200B; de informatie pop-up van het Fragment van de Ervaring &#x200B;](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

U kunt [!UICONTROL Experience Fragments] in [!DNL Target] activiteiten verbruiken gebruikend [&#x200B; Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md).

>[!TIP]
>
>Gebruik Kunstmatige intelligentie, Machine Learning en aanbevelingen met [!UICONTROL Experience Fragments] :
>
>* Om de [!DNL Target] functionaliteit van AI en van ML volledig te gebruiken, kunt u [&#x200B; auto-toewijzen &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) of [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) terwijl het creëren van een activiteit selecteren.
>
>* [!UICONTROL Experience Fragments] wordt niet ondersteund in [!DNL Recommendations] -activiteiten. Nochtans, om [!UICONTROL Experience Fragments] voor aanbevelingen te gebruiken kunt u een [!UICONTROL A/B Test] activiteit (met inbegrip van [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) of een [!UICONTROL Experience Targeting] (XT) activiteit tot stand brengen en [&#x200B; omvatten aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

**om [!UICONTROL Experience Fragments] te verbruiken gebruikend VEC:**

1. In [!DNL Target], terwijl het creëren van of het uitgeven van een ervaring in [&#x200B; Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), klik de plaats op de pagina waar u [!DNL AEM] inhoud wilt opnemen, dan klik **[!UICONTROL Replace Content]** > **[!UICONTROL Experience Fragment]** om de [!UICONTROL Experience Fragment] dialoogdoos te tonen.

   In het dialoogvenster [!UICONTROL Experience Fragment] wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] en die nu in het programma oorspronkelijk beschikbaar is vanuit [!DNL Target] .

   >[!NOTE]
   >
   >De optie [!UICONTROL Replace Content] is niet beschikbaar voor afbeeldingen. Als u deze optie bij een afbeelding wilt gebruiken, klikt u op het containerelement dat de gewenste afbeelding bevat.

   ![&#x200B; experience_fragment_list beeld &#x200B;](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Selecteer de gewenste [!UICONTROL Experience Fragment] en klik op **[!UICONTROL Add]** .
1. Voltooi de configuratie van de activiteit.

   Voor meer informatie over het vormen van de diverse activiteitentypes, zie de volgende onderwerpen:

   * **Test A/B:** [&#x200B; creeer een Test A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **auto-Wijs toe:** [&#x200B; auto-Wijst &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) toe
   * **auto-Doel:** [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automated Personalization (AP):** [&#x200B; Creërend een Activiteit van Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Ervaring richtend (XT):** [&#x200B; creeer een Ervaring richtend Activiteit &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Aanbevelingen in een A/B Test of activiteit XT:** [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments] geëxporteerd als JSON in [!DNL Target] kan niet worden gebruikt in activiteiten die zijn gemaakt met de VEC. Alleen HTML [!UICONTROL Experience Fragments] wordt ondersteund in op VEC gebaseerde activiteiten. Als u JSON [!UICONTROL Experience Fragments] wilt gebruiken, gebruik hen in activiteiten die gebruikend [&#x200B; op vorm-gebaseerde ervaringscomposer &#x200B;](/help/main/c-experiences/form-experience-composer.md) worden gecreeerd.

**om [!UICONTROL Experience Fragments] te verbruiken gebruikend [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target], terwijl het creëren van of het uitgeven van een ervaring in [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), selecteer de plaats op de pagina waar u [!DNL AEM] inhoud wilt opnemen, klik het **[!UICONTROL More Details]** pictogram ( ![&#x200B; Meer pictogram van Details &#x200B;](/help/main/assets/icons/MoreSmall.svg) ), dan uitgezocht **[!UICONTROL Change Experience Fragment]** om de [!UICONTROL Change Experience Fragment] dialoogdoos te tonen.

   ![&#x200B; experience_fragment_list beeld &#x200B;](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   In het dialoogvenster [!UICONTROL Experience Fragment] wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] en die nu in het programma oorspronkelijk beschikbaar is vanuit [!DNL Target] .

1. Selecteer de gewenste [!UICONTROL Experience Fragment] en klik op **[!UICONTROL Add]** .
1. Voltooi de configuratie van de activiteit.

## Aanvullende informatie

* [!DNL Target] zoekt momenteel naar [!UICONTROL Experience Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Experience Fragment] moet binnen tien minuten beschikbaar zijn in [!DNL Target] , maar dit tijdsbestek verkort de verdere ontwikkeling.
* [!UICONTROL Experience Fragment] wordt geïmporteerd in [!DNL Target] als een HTML- of JSON-aanbieding. De [!UICONTROL Experience Fragment] &#39;primaire&#39; versie blijft in [!DNL AEM] . U kunt de [!UICONTROL Experience Fragment] in [!DNL Target] niet bewerken.
* U kunt [!UICONTROL Experience Fragments] niet maken met [!DNL Adobe Developer] . Maak [!UICONTROL Experience Fragments] met AEM, zoals hierboven beschreven.
* Als u [!UICONTROL Experience Fragment] in AEM bijwerkt, moet [!UICONTROL Experience Fragment] worden gepubliceerd en opnieuw worden geëxporteerd naar [!DNL Target] , zodat [!DNL Target] de meest recente wijzigingen kan gebruiken.

## Clibs en externe HTML verwijderen uit [!UICONTROL Experience Fragments] geëxporteerd naar [!UICONTROL Target]

Wanneer u [!UICONTROL Experience Fragment] -aanbiedingen gebruikt met [!DNL Target] op een pagina die wordt geleverd door AEM, bevat de doelpagina al de benodigde clientbibliotheken. Ook andere HTML-elementen in de aanbieding zijn niet nodig.

Soms lopen hele HTML-pagina&#39;s de [!UICONTROL Experience Fragment] om en veroorzaken ze problemen. Zorg ervoor dat [!UICONTROL Experience Fragment] een klein stukje HTML is en geen volledige HTML-pagina met HTML, HEAD, BODY enzovoort.

Voor meer informatie, zie de volgende blogpost: [&#x200B; AEM 6.5: Verwijderend clientlibs van [!UICONTROL Experience Fragments] die naar Doel &#x200B;](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser/){target=_blank} wordt uitgevoerd.

## Trainingsvideo: AEM gebruiken [!UICONTROL Experience Fragments] met [!DNL Adobe Target]

In de volgende video wordt getoond hoe u [!UICONTROL Experience Fragments] kunt instellen en gebruiken:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>De [!DNL AEM] deplink eigenschap die bij 4 :54 wordt besproken is verwijderd.

Voor meer gedetailleerde informatie, zie [&#x200B; Gebruikend [!UICONTROL Experience Fragments] met Adobe Target &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=nl-NL) op de *pagina van de Video&#39;s en van Leerprogramma&#39;s van AEM Sites*.
