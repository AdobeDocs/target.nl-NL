---
keywords: ervaring;json;aem;adobe Experience Manager;export naar adobe target;content fragments;fragments;CF;cf;headless;personalisatie;experimentation
description: Leren gebruiken [!DNL Adobe Experience Manager] [!UICONTROL Content Fragments] in [!DNL Adobe Target] activiteiten.
title: Hoe gebruikt u [!DNL Adobe Experience Manager] AEM [!UICONTROL Content Fragments]?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
source-git-commit: 593cbcc1ff8ccae7afa6098524e95659aa6890f3
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# AEM [!UICONTROL Content Fragments]

Gebruiken [!UICONTROL Content Fragments] (CF&#39;s) gemaakt in [!DNL Adobe Experience Manager] (AEM) [!DNL Target] activiteiten om de grootscheepse personalisatie en experimenten te ondersteunen .

## Overwegingen

Houd rekening met het volgende terwijl u met AEM werkt [!UICONTROL Content Fragments] in [!DNL Target]:

* Deze functie vereist dat u een [!DNL Adobe Experience Manager as a Cloud Service] klant. Zie voor meer informatie [Vereisten](#section_AE6F0971E1574B3AA324003599B96E5A) hieronder.
* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn beschikbaar voor de volgende activiteitstypen:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn niet beschikbaar voor de volgende soorten activiteiten:

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* U kunt [!UICONTROL Content Fragments] in [!DNL Target] activiteiten die gebruikmaken van de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) alleen. U *kan* consumeren [!UICONTROL Content Fragments] in [!DNL Target] activiteiten die gebruikmaken van de [!UICONTROL Visual Experience Composer] (VEC).

Meer informatie over AEM [!UICONTROL Content Fragments] en [!UICONTROL Experience Fragments], zie [AEM [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] overzicht](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Vereisten {#requirements}

U moet [[!DNL AEM] as a Cloud Service](https://experienceleague.corp.adobe.com/docs/experience-manager-cloud-service.html){target=_blank}. Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

Contact [Adobe Target Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om de integratie toe te laten en u van authentificatiedetails te voorzien.

## Configureren en werken met [!UICONTROL Content Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Om te exporteren [!UICONTROL Content Fragments] om te gebruiken in [!DNL Target] activiteiten, moet u sommige inleidende stappen in AEM uitvoeren. Zie voor meer informatie [Inhoudsfragmenten exporteren naar Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html){target=_blank} in de *as a Cloud Service documentatie Experience Manager*.

Voor informatie over ontwerpen, maken, curven en publiceren [!UICONTROL Content Fragments], zie [[!UICONTROL Content Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=en){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html){target=_blank}.

## Gebruiken [!UICONTROL Content Fragments] in [!DNL Target] activiteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Na het uitvoeren van de voorafgaande taken, [!UICONTROL Content Fragment] worden weergegeven op de [!UICONTROL Offers] pagina in [!DNL Target].

[!DNL Target] zoekt momenteel naar [!UICONTROL Content Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Content Fragment] is beschikbaar in [!DNL Target] binnen tien minuten, maar dit tijdsbestek moet de verdere ontwikkeling verkorten.

De [!UICONTROL Content Fragment] wordt geïmporteerd in [!DNL Target] als een JSON-aanbieding. De [!UICONTROL Content Fragment] &quot;primaire&quot; versie blijft in [!DNL AEM]. U kunt de [!UICONTROL Content Fragment] in [!DNL Target].

U kunt filteren en zoeken op [!UICONTROL HTML XFs], [!UICONTROL JSON XFs], en [!UICONTROL Content Fragments] zodat u onderscheid kunt maken tussen verschillende soorten aanbiedingen waarnaar wordt geëxporteerd [!DNL Target].

![Filteren op inhoudfragmenttypen: HTML of JSON in de doelinterface](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

U kunt de muis boven een [!UICONTROL Content Fragment] in de lijst klikt u op de knop [!UICONTROL View] pictogram ![Info, pictogram](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) voor meer informatie over de [!UICONTROL Content Fragment], inclusief [!UICONTROL AEM path] en [!UICONTROL AEM deep link]. Klik op de knop [!UICONTROL Offer Usage] om de activiteiten te bekijken die naar deze aanbieding verwijzen.

![Pop-up Informatie inhoudsfragment](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

U kunt [!UICONTROL Content Fragments] in [!DNL Target] activiteiten die gebruikmaken van de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) alleen. U *kan* consumeren [!UICONTROL Content Fragments] in [!DNL Target] activiteiten die gebruikmaken van de [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC). [!UICONTROL Content Fragments] worden geëxporteerd als JSON in [!DNL Target] en kan niet worden gebruikt in activiteiten die met de VEC worden gecreëerd.

>[!TIP]
>
>Gebruik kunstmatige intelligentie, het Leren van de Machine, en aanbevelingen met [!UICONTROL Content Fragments]:
>
>* Om de [!DNL Target] AI- en ML-functionaliteit kunt u selecteren [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) terwijl u een [!UICONTROL A/B Test] activiteit.
>
>* [!UICONTROL Content Fragments] worden niet ondersteund in [!DNL Recommendations] activiteiten. Om [!UICONTROL Content Fragments] voor aanbevelingen kunt u een [!UICONTROL A/B Test] activiteit (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) of [!UICONTROL Experience Targeting] (XT) en [aanbevelingen opnemen als een aanbod](/help/main/c-recommendations/recommendations-as-an-offer.md).

**Om te verbruiken [!UICONTROL Content Fragments] met de [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target]tijdens het maken of bewerken van een ervaring in de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)selecteert u de locatie op de pagina waar u het invoegpunt wilt invoegen [!DNL AEM] inhoud, selecteert u vervolgens **[!UICONTROL Change Content Fragment]** om de [!UICONTROL Choose a Content Fragment] lijst.

   ![content_fragment_list, afbeelding](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   De [!UICONTROL Content Fragment] in de lijst wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] die nu standaard beschikbaar zijn vanuit [!DNL Target].

1. Selecteer het gewenste [!UICONTROL Content Fragment]en klik vervolgens op **[!UICONTROL Save]**.
1. Voltooi de configuratie van de activiteit.

## Aanvullende informatie

* [!DNL Target] zoekt momenteel naar [!UICONTROL Content Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Content Fragment] is beschikbaar in [!DNL Target] binnen tien minuten, maar dit tijdsbestek moet de verdere ontwikkeling verkorten.
* De [!UICONTROL Content Fragment] wordt geïmporteerd in [!DNL Target] als een JSON-aanbieding. De [!UICONTROL Content Fragment] &quot;primaire&quot; versie blijft in [!DNL AEM]. U kunt de [!UICONTROL Content Fragment] in [!DNL Target].
* U kunt niet maken [!UICONTROL Content Fragments] gebruiken [!DNL Adobe I/O]. Maken [!UICONTROL Content Fragments] gebruik van AEM, zoals hierboven uiteengezet.
* Als u uw [!UICONTROL Content Fragment] in AEM [!UICONTROL Content Fragment] moet worden gepubliceerd en geëxporteerd naar [!DNL Target] opnieuw [!DNL Target] De meest recente wijzigingen kunnen worden gebruikt.
