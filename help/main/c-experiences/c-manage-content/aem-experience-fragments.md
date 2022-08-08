---
keywords: ervaring;json;aem;adobe Experience Manager;exporteren naar adobe target;beleving, fragmenten;fragmenten;XF
description: Leren gebruiken [!DNL Adobe Experience Manager] ervaren fragmenten in [!DNL Adobe Target] activiteiten.
title: Hoe gebruikt u [!DNL Adobe Experience Manager] (AEM) Werken met fragmenten?
feature: Experiences and Offers
exl-id: 3dd811a4-c7be-443d-a5ad-5b9adcaf1a2c
source-git-commit: cc166a54ea4760b8024c05a98931d60cf46e7183
workflow-type: tm+mt
source-wordcount: '1321'
ht-degree: 0%

---

# AEM ervaren fragmenten

Ervingfragmenten gebruiken die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activiteiten ter bevordering van optimalisatie of personalisatie.

>[!NOTE]
>
>Deze functie vereist dat u een [!DNL Adobe Experience Manager] (AEM) klant. Zie voor meer informatie [Vereisten](#section_AE6F0971E1574B3AA324003599B96E5A) hieronder.

Ervingsfragmenten gebruiken die zijn gemaakt in [!DNL AEM] in [!DNL Target] Met deze activiteiten kunt u het gebruiksgemak en de kracht van [!DNL AEM] met krachtige mogelijkheden voor kunstmatige intelligentie (AI) en het leren van machines (ML) in [!DNL Target] om ervaringen op schaal te testen en te personaliseren.

[!DNL AEM] brengt al uw inhoud en middelen op een centrale plaats samen om uw verpersoonlijkingsstrategie te voeden. [!DNL AEM] Hiermee kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder code te schrijven. Het is niet nodig om pagina&#39;s te maken voor elk apparaat. [!DNL AEM] past automatisch elke ervaring aan met uw inhoud.

[!DNL Target] Hiermee kunt u gepersonaliseerde ervaringen op schaal bieden op basis van een combinatie van op regels gebaseerde en door AI aangedreven methoden voor het leren van machines die gedragsvariabelen, contextafhankelijke en offlinevariabelen bevatten. Met [!DNL Target]kunt u eenvoudig instellen en uitvoeren [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) en [Multivariëren](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activiteiten om de beste aanbiedingen, inhoud en ervaringen te bepalen.

De fragmenten van de ervaring vertegenwoordigen een enorme stap voorwaarts om de tevreden/ervaringsscheppers en managers aan de optimalisering en verpersoonlijkingsberoeps te verbinden die bedrijfsresultaten drijven gebruikend [!DNL Target].

## Vereisten {#section_AE6F0971E1574B3AA324003599B96E5A}

U moet beschikken over de functionaliteit voor ervaringsfragmenten binnen [!DNL Target]. Bovendien moet u [!DNL AEM] as a Cloud Service of [!DNL AEM] 6.4 (of hoger). Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* [!DNL Adobe Target Standard] of [!DNL Adobe Target Premium] account.

>[!NOTE]
>
>[!DNL Adobe Experience Manager] 6.3 en 6.4 hebben het einde van de levensduur bereikt en worden niet meer ondersteund (behalve voor klanten die uitgebreide ondersteuning hebben aangeschaft).

Contact [Adobe Target Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om de integratie toe te laten en u van authentificatiedetails te voorzien.

## Ervingsfragmenten maken en configureren in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Voor gebruik [!DNL AEM] ervaren fragmenten in [!DNL Target]moet u de volgende stappen uitvoeren:

### Stap 1: Integreren [!DNL AEM] with [!DNL Target]

Zie voor meer informatie:

* **AEM as a Cloud Service**: [Integreren met Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html){target=_blank} in het dialoogvenster *Experience Manager as a Cloud Service* hulplijn.
* **Adobe I/O**: [Integratie met Adobe Target met behulp van Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html){target=_blank} in het dialoogvenster *Gebruikershandleiding beheren* documentatie.
* **[!DNL AEM]6,5**: [Opteren in Adobe Analytics en Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=en){target=_blank} in het dialoogvenster *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6,4**: [Opteren in Adobe Analytics en Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html){target=_blank} in het dialoogvenster *Adobe Experience Manager 6.4* documentatie.

### Stap 2: Het ervaringsfragment maken

Experience-fragmenten gemaakt in [!DNL AEM]. Zie voor meer informatie:

* **AEM as a Cloud Service**: [Ervaar fragmenten](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=en){target=_blank} in het dialoogvenster *Experience Manager as a Cloud Service* hulplijn.
* **[!DNL AEM]6,5**: [Ervaar fragmenten](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=en){target=_blank} in het dialoogvenster *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6,4**: [Ervaar fragmenten](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=en){target=_blank} in het dialoogvenster *Adobe Experience Manager 6.4* documentatie.

### Stap 3: Configureren [!DNL AEM] om het ervaringsfragment te delen met [!DNL Target]

1. Van binnen [!DNL AEM]selecteert u het gewenste ervaringsfragment of de bijbehorende map en klikt u vervolgens op **[!UICONTROL Properties]**.
2. Klik op de knop **[!UICONTROL Cloud Services]** dan vanaf de **[!UICONTROL Cloud Service Configuration]** vervolgkeuzelijst, selecteert u **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >De vorige stap veronderstelt dat iemand in uw organisatie tot [!DNL Adobe Target] configuratie.

3. Klik op **[!UICONTROL Save & Close]**.

### Stap 4: Het ervaringsfragment publiceren en exporteren naar [!DNL Target]

Afhankelijk van uw [!DNL AEM] versie, zie de volgende verbindingen voor geleidelijke instructies:

* **AEM as a Cloud Service**: [Exporteren van ervaringsfragmenten naar Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=en){target=_blank} in het dialoogvenster *Experience Manager as a Cloud Service* hulplijn.
* **[!DNL AEM]6,5**: [Een ervaringsfragment naar doel exporteren](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=en){target=_blank} in het dialoogvenster *Adobe Experience Manager 6.5* documentatie.
* **[!DNL AEM]6,4**: [Een ervaringsfragment naar doel exporteren](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html){target=_blank} in het dialoogvenster *Adobe Experience Manager 6.4* documentatie.

## Ervaar fragmenten in [!DNL Target] activiteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nadat u de voorgaande taken hebt uitgevoerd, wordt het ervaringsfragment weergegeven op het tabblad [!UICONTROL Offers] pagina in [!DNL Target].

>[!NOTE]
>
>* [!DNL Target] zoekt momenteel naar ervaringsfragmenten die om de tien minuten moeten worden geïmporteerd. Het geïmporteerde ervaringsfragment moet beschikbaar zijn in [!DNL Target] binnen tien minuten, maar dit tijdsbestek moet de verdere ontwikkeling verkorten.
>
>* Het ervaringsfragment wordt geïmporteerd in [!DNL Target] als een HTML-voorstel. Het fragment &quot;primaire&quot; versie blijft behouden in [!DNL AEM]. U kunt het ervaringsfragment niet bewerken in [!DNL Target].


U kunt de muisaanwijzer boven een ervaringsfragment in de lijst plaatsen en vervolgens op de knop [!UICONTROL View] pictogram ![Weergavepictogram](assets/icon_info.png) voor meer informatie over het ervaringsfragment, waaronder de URL voor openbare aanbieding en de bijbehorende [!DNL AEM] pad.

U kunt ervaringsfragmenten gebruiken in [!DNL Target] activiteiten die gebruikmaken van de [Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) of de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Om de [!DNL Target] AI- en ML-functionaliteit kunt u selecteren [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) of [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) tijdens het maken van een A/B-test.
>
>Experience-fragmenten worden niet ondersteund in [!DNL Recommendations] activiteiten. Als u echter ervaringsfragmenten wilt gebruiken voor aanbevelingen, kunt u een [!UICONTROL A/B Test] activiteit (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) of een [!UICONTROL Experience Targeting] (XT) en [aanbevelingen als aanbod opnemen](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

**Ervaar fragmenten met de VEC als u deze wilt gebruiken:**

>[!NOTE]
>
>Ervaar fragmenten die als JSON zijn geëxporteerd in [!DNL Target] niet kan worden gebruikt bij activiteiten die met de VEC worden gecreëerd; alleen HTML-ervaringsfragmenten worden ondersteund in VEC-activiteiten. Als u JSON-ervaringsfragmenten wilt gebruiken, gebruikt u deze in activiteiten die u maakt met de [Formuliergebaseerde ervaringscomposer](/help/main/c-experiences/form-experience-composer.md).

1. In [!DNL Target]tijdens het maken of bewerken van een ervaring in de [Visual Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), klikt u op de locatie op de pagina waar u het invoegpunt wilt invoegen [!DNL AEM] selecteert u vervolgens de gewenste optie om de [!UICONTROL Choose an Experience Fragment] lijst.

   * [!UICONTROL Insert Before]
   * [!UICONTROL Insert After]
   * [!UICONTROL Swap with Experience Fragment]

   De [!UICONTROL Experience Fragment] in de lijst wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] die nu standaard beschikbaar zijn vanuit [!DNL Target].

   >[!NOTE]
   >
   >De [!UICONTROL Swap with Experience Fragment] is niet beschikbaar voor afbeeldingen. Als u deze optie bij een afbeelding wilt gebruiken, klikt u op het containerelement dat de gewenste afbeelding bevat.

   ![](assets/experience_fragment_list.png)

1. Selecteer het gewenste ervaringsfragment en klik op **[!UICONTROL Done]**.
1. Voltooi de configuratie van de activiteit.

   Voor meer informatie over het vormen van de diverse activiteitentypes, zie de volgende onderwerpen:

   * **A/B-test:** [Een A/B-test maken](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Automatisch toewijzen:** [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisch doel:** [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Automated Personalization (AP):** [Automated Personalization-activiteiten maken](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Gericht op ervaring (XT):** [Een ervaring maken die gericht is op activiteiten](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **MVT (Multivariate Test):** [Een multivariatietest maken](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendations:** [Een Recommendations-activiteit maken](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**Ervaar fragmenten op basis van de Form-based Experience Composer:**

1. In [!DNL Target]tijdens het maken of bewerken van een ervaring in de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)selecteert u de locatie op de pagina waar u het invoegpunt wilt invoegen [!DNL AEM] inhoud, selecteert u vervolgens **[!UICONTROL Change Experience Fragment]** om de [!UICONTROL Choose an Experience Fragment] lijst.

   ![](assets/experience_fragment_list.png)

   De [!UICONTROL Experience Fragment] in de lijst wordt de inhoud weergegeven die is gemaakt in [!DNL AEM] die nu standaard beschikbaar zijn vanuit [!DNL Target].

1. Selecteer het gewenste ervaringsfragment en klik op **[!UICONTROL Save]**.
1. Voltooi de configuratie van de activiteit.

## Overwegingen {#considerations}

* [!DNL Target] zoekt momenteel naar ervaringsfragmenten die om de tien minuten moeten worden geïmporteerd. Het geïmporteerde ervaringsfragment moet beschikbaar zijn in [!DNL Target] binnen tien minuten, maar dit tijdsbestek moet de verdere ontwikkeling verkorten.
* Het ervaringsfragment wordt geïmporteerd in [!DNL Target] als een HTML- of JSON-aanbieding. Het ervaringsfragment &quot;primaire&quot; versie blijft in [!DNL AEM]. U kunt het ervaringsfragment niet bewerken in [!DNL Target].
* U kunt geen ervaringsfragmenten maken met [!DNL Adobe I/O]. Maak ervaringsfragmenten met AEM, zoals hierboven beschreven.
* Als u het ervaringsfragment bijwerkt in AEM, moet het ervaringsfragment worden gepubliceerd en geëxporteerd naar [!DNL Target] opnieuw [!DNL Target] De meest recente wijzigingen kunnen worden gebruikt.

## ClientLibs en externe HTML verwijderen uit Experience Fragments die naar Target zijn geëxporteerd

Als u ervaring hebt met fragmentatieaanbiedingen met [!DNL Target] op een pagina die wordt geleverd door AEM, bevat de doelpagina al alle benodigde clientbibliotheken. Er zij ook op gewezen dat het aanbod ook geen andere HTML-elementen behoeft.

Soms lopen hele HTML pagina&#39;s het ervaringsfragment om en veroorzaken ze problemen. Zorg ervoor dat het ervaringsfragment een klein stuk HTML is en geen volledige HTML pagina met HTML, HEAD, BODY enzovoort.

Raadpleeg het volgende blogbericht voor meer informatie: [AEM 6.5: ClientLibs verwijderen uit Experience Fragments geëxporteerd naar Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Trainingsvideo: Fragmenten AEM ervaren met [!DNL Adobe Target]

In de volgende video ziet u hoe u ervaringsfragmenten instelt en gebruikt:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>De [!DNL AEM] De functie voor diepte die in 4:54 wordt besproken, is verwijderd.

Zie voor meer informatie [Experience Fragments gebruiken met Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) op de *AEM Sites-video&#39;s en -Tutorials* pagina.
