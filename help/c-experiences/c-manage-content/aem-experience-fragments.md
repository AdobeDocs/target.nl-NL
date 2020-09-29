---
keywords: experience;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
description: Informatie over het gebruik van ervaringsfragmenten die in Adobe Experience Manager (AEM) zijn gemaakt in Adobe Target-activiteiten om optimalisatie of personalisatie te ondersteunen.
title: Adobe Experience Manager (AEM) ervaart fragmenten in Adobe Target
feature: aem
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: e846109c476f98b4adc09d8b9dd2c2ef039b5ef7
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---


# AEM ervaren fragmenten{#aem-experience-fragments}

Informatie over het gebruik van ervaringsfragmenten die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) bij [!DNL Target] activiteiten ter ondersteuning van optimalisatie of personalisatie.

>[!NOTE]
>
>Deze functie vereist dat u een [!DNL Adobe Experience Manager] ([!DNL AEM]) klant bent. Zie [Vereisten](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A)hieronder voor meer informatie.

## Overzicht {#section_95A91830530F493B81C5C9CDB9B783EA}

Door ervaringsfragmenten te gebruiken die zijn gemaakt in [!DNL AEM] de [!DNL Target] activiteiten, kunt u het gebruiksgemak en de kracht van [!DNL AEM] [!DNL Target] deze fragmenten combineren met de krachtige mogelijkheden van Automated Intelligence (AI) en Machine Learning (ML) om ervaringen op schaal te testen en te personaliseren.

[!DNL AEM] brengt al uw inhoud en middelen op een centrale plaats samen om uw verpersoonlijkingsstrategie te voeden. [!DNL AEM] Hiermee kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder code te schrijven. Het is niet nodig om pagina&#39;s te maken voor elk apparaat. [!DNL AEM] past automatisch elke ervaring aan met uw inhoud.

[!DNL Target] Hiermee kunt u gepersonaliseerde ervaringen op schaal bieden op basis van een combinatie van op regels gebaseerde en door AI aangedreven methoden voor het leren van machines die gedragsvariabelen, contextafhankelijke en offlinevariabelen bevatten. Met [!DNL Target] u kunt gemakkelijk opstelling en looppas [A/B Test](/help/c-activities/t-test-ab/test-ab.md) en [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activiteiten om de beste aanbiedingen, inhoud, en ervaringen te bepalen.

De fragmenten van de ervaring vertegenwoordigen een enorme stap voorwaarts om de tevreden/ervaringsscheppers en managers aan de optimalisering en verpersoonlijkingsberoeps te verbinden die bedrijfsuitkomsten drijven gebruikend [!DNL Target].

## Vereisten {#section_AE6F0971E1574B3AA324003599B96E5A}

U moet beschikken over de functionaliteit voor ervaringsfragmenten binnen [!DNL Target]. Daarnaast moet u [!DNL AEM] 6.3 gebruiken met de juiste service pack of [!DNL AEM] 6.4 (of hoger). Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

* [!DNL Adobe Experience Manager] 6.4 (of hoger).
* [!DNL Adobe Experience Manager] 6.3 SP2 (of hoger).
* [!DNL Adobe Target Standard] of [!DNL Adobe Target Premium] account.
* Neem contact op met de klantenservice [van](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Adobe Target om de integratie in te schakelen en u verificatiegegevens te verstrekken.

## Ervingsfragmenten maken en configureren in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Voer de volgende stappen uit om [!DNL AEM] ervaringsfragmenten in te kunnen gebruiken [!DNL Target]:

### Stap 1: Integreren [!DNL AEM] met [!DNL Target]

Zie voor meer informatie:

* **[!DNL AEM]6.3**: [U kunt kiezen voor Adobe Analytics en Adobe Target](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) in de documentatie voor _Adobe Experience Manager 6.3_ .
* **[!DNL AEM]6.4**: [U kunt kiezen voor Adobe Analytics en Adobe Target](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) in de documentatie voor _Adobe Experience Manager 6.4_ .
* **[!DNL AEM]6.5**: [U kunt kiezen voor Adobe Analytics en Adobe Target](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html) in de documentatie van *Adobe Experience Manager 6.5* .

### Stap 2: Het ervaringsfragment maken

Er worden ervaringsfragmenten gemaakt in [!DNL AEM]. Zie voor meer informatie:

* **[!DNL AEM]6.3**: [Ervaar Fragments](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) in de documentatie van *Adobe Experience Manager 6.3* .
* **[!DNL AEM]6.4**: [Ervaar Fragments](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) in de documentatie van *Adobe Experience Manager 6.4* .
* **[!DNL AEM]6.5**: [Ervaar Fragments](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html) in de documentatie van *Adobe Experience Manager 6.5* .

### Stap 3: Configureren [!DNL AEM] om het ervaringsfragment te delen met [!DNL Target]

1. Van binnen [!DNL AEM], selecteer het gewenste ervaringsfragment of zijn bevattende omslag, dan klik **[!UICONTROL Properties]**.
2. Klik op het **[!UICONTROL Cloud Services]** tabblad en selecteer vervolgens in de **[!UICONTROL Cloud Service Configuration]** vervolgkeuzelijst de optie **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >De vorige stap veronderstelt dat iemand in uw organisatie de [!DNL Adobe Target] configuratie heeft gecreeerd.

3. Klik op **[!UICONTROL Save & Close]**.

### Stap 4: Het ervaringsfragment publiceren en exporteren naar [!DNL Target]

Afhankelijk van uw [!DNL AEM] versie raadpleegt u de volgende koppelingen voor stapsgewijze instructies:

* **[!DNL AEM]6.3**: [Een ervaringsfragment naar doel](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html) exporteren in de documentatie van *Adobe Experience Manager 6.3* .
* **[!DNL AEM]6.4**: [Een ervaringsfragment naar doel](https://docs.adobe.com/content/help/en/experience-manager-64/administering/integration/experience-fragments-target.html) exporteren in de documentatie bij *Adobe Experience Manager 6.4* .
* **[!DNL AEM]6.5**: [Een ervaringsfragment naar doel](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html) exporteren in de documentatie van *Adobe Experience Manager 6.5* .

## Werken met ervaringsfragmenten in doelactiviteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nadat u de voorgaande taken hebt uitgevoerd, wordt het ervaringsfragment weergegeven op de [!UICONTROL Offers] pagina in [!DNL Target].

>[!NOTE]
>
>[!DNL Target] zoekt momenteel naar ervaringsfragmenten die om de tien minuten moeten worden geïmporteerd. Het geïmporteerde ervaringsfragment moet binnen tien [!DNL Target] minuten beschikbaar zijn, maar dit tijdsbestek kan de voortgang verkorten.

>[!IMPORTANT]
>
>Het ervaringsfragment wordt momenteel geïmporteerd in [!DNL Target] de vorm van een HTML-aanbieding. Het ervaringsfragment &#39;primaire&#39; versie blijft in [!DNL AEM]. U kunt het ervaringsfragment niet bewerken in [!DNL Target].

U kunt de muisaanwijzer boven een ervaringsfragment in de lijst plaatsen en vervolgens op het pictogram [!UICONTROL View]![Weergave klikken](assets/icon_info.png) om aanvullende informatie over het ervaringsfragment weer te geven, zoals de URL voor de openbare aanbieding en het bijbehorende [!DNL AEM] pad.

U kunt ervaringsfragmenten in [!DNL Target] activiteiten verbruiken gebruikend de Composer [van de](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) Visuele Ervaring (VEC) of de [Formulier-Gebaseerde Composer](/help/c-experiences/form-experience-composer.md)van de Ervaring.

>[!NOTE]
>
>Als u de [!DNL Target] AI- en ML-functionaliteit volledig wilt gebruiken, selecteert u [Automatisch toewijzen](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) of [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) tijdens het maken van een A/B-test.

**Ervaar fragmenten met de VEC als u deze wilt gebruiken:**

1. In [!DNL Target], terwijl het creëren van of het uitgeven van een ervaring in [Visuele Composer](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)van de Ervaring, klik de plaats op de pagina waar u [!DNL AEM] inhoud wilt opnemen, dan selecteer de gewenste optie om de [!UICONTROL Choose an Experience Fragment] lijst te tonen.

   * [!UICONTROL Insert Before]
   * [!UICONTROL Insert After]
   * [!UICONTROL Swap with Experience Fragment]

   In de [!UICONTROL Experience Fragment] lijst wordt alle inhoud weergegeven die is gemaakt in [!DNL AEM] dat nu standaard beschikbaar is vanuit de lijst [!DNL Target].

   >[!NOTE]
   >
   >De [!UICONTROL Swap with Experience Fragment] optie is niet beschikbaar voor afbeeldingen. Als u deze optie bij een afbeelding wilt gebruiken, klikt u op het containerelement dat de gewenste afbeelding bevat.

   ![](assets/experience_fragment_list.png)

1. Selecteer het gewenste ervaringsfragment en klik op **[!UICONTROL Done]**.
1. Voltooi de configuratie van de activiteit.

   Voor meer informatie over het vormen van de diverse activiteitentypes, zie de volgende onderwerpen:

   * **A/B-test:** [Een A/B-test maken](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
   * **Automatisch toewijzen:** [Automatisch toewijzen](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisch doel:** [Auto-Target voor persoonlijke ervaringen](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)
   * **Automated Personalization (AP):** [Automated Personalization-activiteiten maken](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Gericht op ervaring (XT):** [Een ervaring maken die gericht is op activiteiten](../../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **MVT (Multivariate Test):** [Een multivariatietest maken](../../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendations:** [Een Recommendations-activiteit maken](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**Ervaar fragmenten op basis van de Form-based Experience Composer:**

1. Tijdens het maken of bewerken van een ervaring in de [!DNL Target]Form-Based Experience Composer [selecteert u op de pagina de locatie waar u](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)inhoud wilt invoegen en selecteert u [!DNL AEM] om de **[!UICONTROL Change Experience Fragment]** [!UICONTROL Choose an Experience Fragment] lijst weer te geven.

   ![](assets/experience_fragment_list.png)

   In de [!UICONTROL Experience Fragment] lijst wordt alle inhoud weergegeven die is gemaakt in [!DNL AEM] dat nu standaard beschikbaar is vanuit de lijst [!DNL Target].

1. Selecteer het gewenste ervaringsfragment en klik op **[!UICONTROL Save]**.
1. Voltooi de configuratie van de activiteit.

## Overwegingen {#considerations}

* [!DNL Target] zoekt momenteel naar ervaringsfragmenten die om de tien minuten moeten worden geïmporteerd. Het geïmporteerde ervaringsfragment moet binnen tien [!DNL Target] minuten beschikbaar zijn, maar dit tijdsbestek kan de voortgang verkorten.
* Het ervaringsfragment wordt momenteel geïmporteerd in [!DNL Target] de vorm van een HTML-aanbieding. Het ervaringsfragment &#39;primaire&#39; versie blijft in [!DNL AEM]. U kunt het ervaringsfragment niet bewerken in [!DNL Target].
* U kunt JSON-aanbiedingen importeren als ervaringsfragmenten in [!DNL Target]. Deze aanbiedingen worden echter geïmporteerd als HTML-aanbiedingen. JSON-aanbiedingen (ervaringsfragmenten) worden momenteel niet volledig ondersteund in de [!DNL Target] gebruikersinterface.
* U kunt geen ervaringsfragmenten maken met gebruik van Adobe IO. U moet ervaringsfragmenten maken met behulp van AEM, zoals hierboven beschreven.

## Trainingsvideo: Fragmenten voor AEM ervaring gebruiken met een Adobe Target ![Tutorial badge](/help/assets/overview.png) {#section_C0EDC54063464F41A182492D2045BC64}

In de volgende video ziet u hoe u ervaringsfragmenten instelt en gebruikt:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>De functie voor [!DNL AEM] verdiepen die in 4:54 wordt besproken, is verwijderd.

Zie [Experience Fragments gebruiken met Adobe Target](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) op de pagina *AEM Sites Video&#39;s and Tutorials* voor meer informatie.
