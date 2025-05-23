---
keywords: ervaring;json;aem;adobe Experience Manager;exporteren naar adobe target;beleving, fragmenten;fragmenten;XF
description: Leren gebruiken [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in [!DNL Adobe Target] activiteiten.
title: Hoe gebruikt u [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
source-git-commit: 7c81362a82ca6692bb8c183b8e8fc50c6329e2e8
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 0%

---

# AEM [!UICONTROL Experience Fragments]

Gebruiken [!UICONTROL Experience Fragments] (XFs) gecreeerd in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten ter ondersteuning van optimalisatie en personalisatie.

## Overwegingen

Houd rekening met het volgende terwijl u met AEM werkt [!UICONTROL Experience Fragments] in [!DNL Target]:

* Deze functie vereist dat u een [!DNL Adobe Experience Manager] (AEM) klant. Zie voor meer informatie [Vereisten](#section_AE6F0971E1574B3AA324003599B96E5A) hieronder.
* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn beschikbaar voor de volgende activiteitstypen:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments] zijn niet beschikbaar voor de volgende soorten activiteiten:

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* U kunt [!UICONTROL Experience Fragments] in [!DNL Target] activiteiten die gebruikmaken van de [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md).

Meer informatie over AEM [!UICONTROL Experience Fragments] en [!UICONTROL Content Fragments], zie [AEM [!UICONTROL Experience Fragments] en het overzicht van inhoudsfragmenten](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Vereisten {#requirements}

U moet zijn voorzien van [!UICONTROL Experience Fragments] functionaliteit binnen [!DNL Target]. Bovendien moet u [!DNL AEM] as a Cloud Service of [!DNL AEM] 6.4 (of hoger). Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

* [!DNL Adobe Experience Manager &#x200B;] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard] of [!DNL Adobe Target Premium] account

[!DNL Adobe Experience Manager] 6.3 en 6.4 hebben het einde van de levensduur bereikt en worden niet meer ondersteund (behalve voor klanten die uitgebreide ondersteuning hebben aangeschaft).

Contact [Adobe Target Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om de integratie toe te laten en u van authentificatiedetails te voorzien.

## Maken en configureren [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Voor gebruik [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target]moet u de volgende stappen uitvoeren:

### Stap 1: Integreren [!DNL AEM] with [!DNL Target]

Zie voor meer informatie:

* **AEM as a Cloud Service**: [Integreren met Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html?lang=nl-NL){target=_blank} in de *Experience Manager as a Cloud Service* hulplijn.
* **Adobe I/O**: [Integratie met Adobe Target met behulp van Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html?lang=nl-NL){target=_blank} in de *Gebruikershandleiding beheren* documentatie.
* **[!DNL AEM]6,5**: [Opteren in Adobe Analytics en Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=nl-NL){target=_blank} in de *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6,4**: [Opteren in Adobe Analytics en Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=nl-NL){target=_blank} in de *Adobe Experience Manager 6.4* documentatie.

### Stap 2: Het fragment Ervaring maken

[!UICONTROL Experience Fragments] worden gemaakt in [!DNL AEM]. Zie voor meer informatie:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=nl-NL){target=_blank} in de *Experience Manager as a Cloud Service* hulplijn.
* **[!DNL AEM]6,5**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=nl-NL){target=_blank} in de *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6,4**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=nl-NL){target=_blank} in de *Adobe Experience Manager 6.4* documentatie.

### Stap 3: Configureren [!DNL AEM] om de [!UICONTROL Experience Fragment] with [!DNL Target]

1. Van binnen [!DNL AEM]selecteert u de gewenste [!UICONTROL Experience Fragment] of de bovenliggende map, klikt u op **[!UICONTROL Properties]**.
2. Klik op de knop **[!UICONTROL Cloud Services]** dan vanaf de **[!UICONTROL Cloud Service Configuration]** vervolgkeuzelijst, selecteert u **[!UICONTROL Adobe Target]**.

   De vorige stap veronderstelt dat iemand in uw organisatie tot [!DNL Adobe Target] configuratie.

3. Klik op **[!UICONTROL Save & Close]**.

### Stap 4: Publiceer de [!UICONTROL Experience Fragment] en exporteer het naar [!DNL Target]

Afhankelijk van uw [!DNL AEM] versie, zie de volgende verbindingen voor geleidelijke instructies:

* **AEM as a Cloud Service**: [Exporteren [!UICONTROL Experience Fragments] naar Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=nl-NL){target=_blank} in de *Experience Manager as a Cloud Service* hulplijn.
* **[!DNL AEM]6,5**: [Een ervaringsfragment naar doel exporteren](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=nl-NL){target=_blank} in de *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6,4**: [Een ervaringsfragment naar doel exporteren](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=nl-NL){target=_blank} in de *Adobe Experience Manager 6.4* documentatie.

## Gebruiken [!UICONTROL Experience Fragments] in [!DNL Target] activiteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Na het uitvoeren van de voorafgaande taken, [!UICONTROL Experience Fragment] worden weergegeven op de [!UICONTROL Offers] pagina in [!DNL Target].

[!DNL Target] zoekt momenteel naar [!UICONTROL Experience Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Experience Fragment] dient beschikbaar te zijn in [!DNL Target] binnen tien minuten, maar dit tijdsbestek moet de verdere ontwikkeling verkorten.

De [!UICONTROL Experience Fragment] wordt geïmporteerd in [!DNL Target] als een HTML- of JSON-aanbieding. De [!UICONTROL Experience Fragment] &quot;primaire&quot; versie blijft in [!DNL AEM]. U kunt de [!UICONTROL Experience Fragment] in [!DNL Target].

U kunt filteren en zoeken op [!UICONTROL HTML XFs] en [!UICONTROL JSON XFs] zodat u beter onderscheid kunt maken tussen [!UICONTROL Experience Fragment] typen waarnaar wordt geëxporteerd [!DNL Target].

![Filteren op ervaringsfragmenttypen: HTML of JSON in de doelinterface](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

U kunt de muis boven een [!UICONTROL Experience Fragment] in de lijst klikt u op de knop [!UICONTROL View] pictogram ![Info, pictogram](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) voor meer informatie over de [!UICONTROL Experience Fragment], met inbegrip van [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path]en informatie over laatste wijzigingen. Klik op de knop [!UICONTROL Offer Usage] om de activiteiten te bekijken die naar deze aanbieding verwijzen.

![Pop-up Experience Fragment-informatie](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

U kunt [!UICONTROL Experience Fragments] in [!DNL Target] activiteiten die gebruikmaken van de [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) en de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md).


>[!TIP]
>
>Gebruik kunstmatige intelligentie, het Leren van de Machine, en aanbevelingen met [!UICONTROL Experience Fragments]:
>
>* Om de [!DNL Target] AI- en ML-functionaliteit kunt u selecteren [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) tijdens het maken van een activiteit.
>
>* [!UICONTROL Experience Fragments] worden niet ondersteund in [!DNL Recommendations] activiteiten. Om [!UICONTROL Experience Fragments] voor aanbevelingen kunt u een [!UICONTROL A/B Test] activiteit (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) of een [!UICONTROL Experience Targeting] (XT) en [aanbevelingen als aanbod opnemen](/help/main/c-recommendations/recommendations-as-an-offer.md).


**Om te verbruiken [!UICONTROL Experience Fragments] met behulp van de VEC:**

1. In [!DNL Target]tijdens het maken of bewerken van een ervaring in de [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), klikt u op de locatie op de pagina waar u het invoegpunt wilt invoegen [!DNL AEM] selecteert u vervolgens de gewenste optie om de [!UICONTROL Choose an Experience Fragment] lijst.

   * [!UICONTROL Insert Before]
   * [!UICONTROL Insert After]
   * [!UICONTROL Swap with Experience Fragment]

   De [!UICONTROL Experience Fragment] in de lijst wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] die nu standaard beschikbaar zijn vanuit [!DNL Target].

   >[!NOTE]
   >
   >De [!UICONTROL Swap with Experience Fragment] is niet beschikbaar voor afbeeldingen. Als u deze optie bij een afbeelding wilt gebruiken, klikt u op het containerelement dat de gewenste afbeelding bevat.

   ![experience_fragment_list, afbeelding](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Selecteer het gewenste [!UICONTROL Experience Fragment]en klik vervolgens op **[!UICONTROL Done]**.
1. Voltooi de configuratie van de activiteit.

   Voor meer informatie over het vormen van de diverse activiteitentypes, zie de volgende onderwerpen:

   * **A/B-test:** [Een A/B-test maken](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Automatisch toewijzen:** [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisch doel:** [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automated Personalization (AP):** [Automated Personalization-activiteiten maken](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Gericht op ervaring (XT):** [Een ervaring maken die gericht is op activiteiten](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Recommendations in een A/B Test- of XT-activiteit:** [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments] geëxporteerd als JSON in [!DNL Target] niet kan worden gebruikt bij activiteiten die met de VEC worden gecreëerd; alleen HTML [!UICONTROL Experience Fragments] worden ondersteund in VEC-activiteiten. Als u JSON wilt gebruiken [!UICONTROL Experience Fragments], gebruiken in activiteiten die zijn gemaakt met de [Formuliergebaseerde ervaringscomposer](/help/main/c-experiences/form-experience-composer.md).

**Om te verbruiken [!UICONTROL Experience Fragments] met de [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target]tijdens het maken of bewerken van een ervaring in de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)selecteert u de locatie op de pagina waar u het invoegpunt wilt invoegen [!DNL AEM] inhoud, selecteert u vervolgens **[!UICONTROL Change Experience Fragment]** om de [!UICONTROL Choose an Experience Fragment] lijst.

   ![experience_fragment_list, afbeelding](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   De [!UICONTROL Experience Fragment] in de lijst wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] die nu standaard beschikbaar zijn vanuit [!DNL Target].

1. Selecteer het gewenste [!UICONTROL Experience Fragment]en klik vervolgens op **[!UICONTROL Save]**.
1. Voltooi de configuratie van de activiteit.

## Aanvullende informatie

* [!DNL Target] zoekt momenteel naar [!UICONTROL Experience Fragments] om de tien minuten te importeren. De geïmporteerde [!UICONTROL Experience Fragment] dient beschikbaar te zijn in [!DNL Target] binnen tien minuten, maar dit tijdsbestek moet de verdere ontwikkeling verkorten.
* De [!UICONTROL Experience Fragment] wordt geïmporteerd in [!DNL Target] als een HTML- of JSON-aanbieding. De [!UICONTROL Experience Fragment] &quot;primaire&quot; versie blijft in [!DNL AEM]. U kunt de [!UICONTROL Experience Fragment] in [!DNL Target].
* U kunt niet maken [!UICONTROL Experience Fragments] gebruiken [!DNL Adobe I/O]. Maken [!UICONTROL Experience Fragments] gebruik van AEM, zoals hierboven uiteengezet.
* Als u uw [!UICONTROL Experience Fragment] in AEM [!UICONTROL Experience Fragment] moet worden gepubliceerd en geëxporteerd naar [!DNL Target] opnieuw [!DNL Target] De meest recente wijzigingen kunnen worden gebruikt.

## ClientLibs en externe HTML verwijderen uit [!UICONTROL Experience Fragments] geëxporteerd naar [!UICONTROL Target]

Wanneer u [!UICONTROL Experience Fragment] voorstellen met [!DNL Target] op een pagina die wordt geleverd door AEM, bevat de doelpagina al alle benodigde clientbibliotheken. Er zij ook op gewezen dat het aanbod ook geen andere HTML-elementen behoeft.

Soms worden hele HTML pagina&#39;s omlopen [!UICONTROL Experience Fragment] en problemen veroorzaken. Zorg ervoor dat de [!UICONTROL Experience Fragment] is een klein stuk HTML en geen volledige HTML pagina met HTML, HEAD, BODY enzovoort.

Raadpleeg het volgende blogbericht voor meer informatie: [AEM 6.5: ClientLibs verwijderen uit [!UICONTROL Experience Fragments] geëxporteerd naar Doel](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Trainingsvideo: AEM gebruiken [!UICONTROL Experience Fragments] with [!DNL Adobe Target]

In de volgende video ziet u hoe u het programma instelt en gebruikt [!UICONTROL Experience Fragments]:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>De [!DNL AEM] De functie voor diepte die in 4:54 wordt besproken, is verwijderd.

Zie voor meer informatie [Gebruiken [!UICONTROL Experience Fragments] met Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=nl-NL) op de *AEM Sites-video&#39;s en -Tutorials* pagina.
