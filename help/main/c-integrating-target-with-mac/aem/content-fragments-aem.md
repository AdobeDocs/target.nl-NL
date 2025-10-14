---
keywords: ervaring;json;aem;adobe Experience Manager;export naar adobe target;content fragments;fragments;CF;cf;headless;personalisatie;experimentation
description: Leer hoe te om  [!DNL Adobe Experience Manager] [!UICONTROL Content Fragments] in  [!DNL Adobe Target]  activiteiten te gebruiken.
title: Hoe gebruik ik  [!DNL Adobe Experience Manager]  (AEM) [!UICONTROL Content Fragments]?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
source-git-commit: b29614680b27c9c33f11eed85d8ab4feebc28b0d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# AEM [!UICONTROL Content Fragments]

Gebruik [!UICONTROL Content Fragments] (CF&#39;s) die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] -activiteiten voor een headless personalisatie en experimenteren.

## Overwegingen

Houd rekening met het volgende terwijl u met AEM [!UICONTROL Content Fragments] werkt in [!DNL Target] :

* Deze functie vereist dat u een [!DNL Adobe Experience Manager as a Cloud Service] klant bent. Voor meer informatie, zie [&#x200B; Vereisten &#x200B;](#section_AE6F0971E1574B3AA324003599B96E5A) hieronder.
* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn beschikbaar voor de volgende typen activiteiten:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn niet beschikbaar voor de volgende typen activiteiten:

   * [[!UICONTROL Multivariate Test] (MV)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* U kunt [!UICONTROL Content Fragments] in [!DNL Target] activiteiten gebruiken gebruikend [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) slechts. U *kunt niet* verbruiken [!UICONTROL Content Fragments] in [!DNL Target] activiteiten gebruikend [!UICONTROL Visual Experience Composer] (VEC).

Meer over AEM [!UICONTROL Content Fragments] en [!UICONTROL Experience Fragments] leren, zie [&#x200B; AEM [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] overzicht &#x200B;](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Vereisten {#requirements}

U moet [[!DNL AEM]  as a Cloud Service &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=nl-NL){target=_blank} gebruiken. Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

De Zorg van de Klant van Adobe Target van het contact [&#x200B; om de integratie toe te laten en u van authentificatiedetails te voorzien.](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

## [!UICONTROL Content Fragments] configureren en gebruiken in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Als u [!UICONTROL Content Fragments] wilt exporteren voor gebruik in [!DNL Target] -activiteiten, moet u een aantal voorbereidende stappen uitvoeren in AEM. Voor meer informatie, zie [&#x200B; het Uitvoeren van de Fragmenten van de Inhoud naar Adobe Target &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=nl-NL){target=_blank} in de *documentatie van as a Cloud Service van Experience Manager*.

Voor informatie over het ontwerpen van, het creëren van, het beoefenen van, en het publiceren [!UICONTROL Content Fragments], zie [[!UICONTROL Content Fragments] &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=nl-NL){target=_blank} en [&#x200B; het Werken met de Fragmenten van de Inhoud &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=nl-NL){target=_blank} in de [&#x200B; documentatie van as a Cloud Service van Experience Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=nl-NL){target=_blank}.

## [!UICONTROL Content Fragments] gebruiken in [!DNL Target] -activiteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nadat u de voorgaande taken hebt uitgevoerd, wordt [!UICONTROL Content Fragment] weergegeven op de [!UICONTROL Offers] pagina in [!DNL Target] .

[!DNL Target] zoekt momenteel naar [!UICONTROL Content Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Content Fragment] moet binnen tien minuten beschikbaar zijn in [!DNL Target] , maar dit tijdsbestek verkort de verdere ontwikkeling.

[!UICONTROL Content Fragment] wordt geïmporteerd in [!DNL Target] als een JSON-aanbieding. De [!UICONTROL Content Fragment] &#39;primaire&#39; versie blijft in [!DNL AEM] . U kunt de [!UICONTROL Content Fragment] in [!DNL Target] niet bewerken.

U kunt filteren en zoeken op [!UICONTROL HTML XFs] , [!UICONTROL JSON XFs] en [!UICONTROL Content Fragments] om u te helpen onderscheid te maken tussen verschillende aanbiedingstypen die worden geëxporteerd naar [!DNL Target] .

![&#x200B; Filter door de types van Fragment van de Inhoud: HTML of JSON in het Doel UI &#x200B;](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

U kunt over [!UICONTROL Experience Fragment] in de lijst bewegen, dan het [!UICONTROL View] pictogram ![&#x200B; pictogram van Info &#x200B;](/help/main/assets/icons/InfoOutline.svg) klikken om extra informatie over [!UICONTROL Content Fragment], met inbegrip van zijn [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path], en laatste wijzigingsinformatie te zien. Klik op [!UICONTROL [!UICONTROL View Full Details]] om de activiteiten te bekijken die naar deze aanbieding verwijzen.

U kunt [!UICONTROL Content Fragments] in [!DNL Target] activiteiten gebruiken gebruikend [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) slechts. U *kunt niet* verbruiken [!UICONTROL Content Fragments] in [!DNL Target] activiteiten gebruikend [&#x200B; Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). [!UICONTROL Content Fragments] worden geëxporteerd als JSON in [!DNL Target] en kunnen niet worden gebruikt in activiteiten die zijn gemaakt met de VEC.

>[!TIP]
>
>Gebruik Kunstmatige intelligentie, Machine Learning en aanbevelingen met [!UICONTROL Content Fragments] :
>
>* Om de [!DNL Target] functionaliteit van AI en van ML volledig te gebruiken, kunt u [&#x200B; auto-toewijzen &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) selecteren of [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) terwijl het creëren van een [!UICONTROL A/B Test] activiteit.
>
>* [!UICONTROL Content Fragments] wordt niet ondersteund in [!DNL Recommendations] -activiteiten. Nochtans, om [!UICONTROL Content Fragments] voor aanbevelingen te gebruiken kunt u een [!UICONTROL A/B Test] activiteit (met inbegrip van [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) of een [!UICONTROL Experience Targeting] (XT) activiteit tot stand brengen en [&#x200B; omvatten aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

**om [!UICONTROL Content Fragments] te verbruiken gebruikend [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target], terwijl het creëren van of het uitgeven van een ervaring in [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), selecteer de plaats op de pagina waar u [!DNL AEM] inhoud wilt opnemen, dan selecteren **[!UICONTROL Change Content Fragment]** om de [!UICONTROL Choose a Content Fragment] lijst te tonen.

   ![&#x200B; content_fragment_list beeld &#x200B;](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   In de lijst [!UICONTROL Content Fragment] wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] en die nu oorspronkelijk beschikbaar is vanuit [!DNL Target] .

1. Selecteer de gewenste [!UICONTROL Content Fragment] en klik op **[!UICONTROL Save]** .
1. Voltooi de configuratie van de activiteit.

## Aanvullende informatie

* [!DNL Target] zoekt momenteel naar [!UICONTROL Content Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Content Fragment] moet binnen tien minuten beschikbaar zijn in [!DNL Target] , maar dit tijdsbestek verkort de verdere ontwikkeling.
* [!UICONTROL Content Fragment] wordt geïmporteerd in [!DNL Target] als een JSON-aanbieding. De [!UICONTROL Content Fragment] &#39;primaire&#39; versie blijft in [!DNL AEM] . U kunt de [!UICONTROL Content Fragment] in [!DNL Target] niet bewerken.
* U kunt [!UICONTROL Content Fragments] niet maken met [!DNL Adobe I/O] . Maak [!UICONTROL Content Fragments] met AEM, zoals hierboven beschreven.
* Als u [!UICONTROL Content Fragment] in AEM bijwerkt, moet [!UICONTROL Content Fragment] worden gepubliceerd en opnieuw worden geëxporteerd naar [!DNL Target] , zodat [!DNL Target] de meest recente wijzigingen kan gebruiken.
