---
keywords: experience;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
description: Informatie over het gebruik van ervaringsfragmenten die zijn gemaakt in Adobe Experience Manager (AEM) bij Adobe Target-activiteiten voor optimalisatie of personalisatie.
title: Adobe Experience Manager (AEM) ervaart fragmenten in Adobe Target
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# AEM ervaart fragmenten{#aem-experience-fragments}

Informatie over het gebruik van ervaringsfragmenten die zijn gemaakt in [!DNL Adobe Experience Manager] (AEM) bij [!DNL Target] activiteiten om optimalisatie of personalisatie te ondersteunen.

>[!NOTE]
>
>Deze functie vereist dat u een [!DNL Adobe Experience Manager] (AEM-)klant bent. Zie [Vereisten](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A)hieronder voor meer informatie.

## Overzicht {#section_95A91830530F493B81C5C9CDB9B783EA}

Door ervaringsfragmenten te gebruiken die in AEM zijn gemaakt voor [!DNL Target] [!DNL Target] activiteiten kunt u het gebruiksgemak en de kracht van AEM combineren met krachtige mogelijkheden voor Automated Intelligence (AI) en Machine Learning (ML) om ervaringen op schaal te testen en aan te passen.

AEM brengt al uw inhoud en middelen op een centrale locatie samen om uw personalisatiestrategie te voeden. Met AEM kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder dat u code hoeft te schrijven. Het is niet nodig om pagina&#39;s te maken voor elk apparaat. AEM past automatisch elke ervaring aan met behulp van uw inhoud.

[!DNL Target] Hiermee kunt u gepersonaliseerde ervaringen op schaal bieden op basis van een combinatie van op regels gebaseerde en door AI aangedreven methoden voor het leren van machines die gedragsvariabelen, contextafhankelijke en offlinevariabelen bevatten. Met [!DNL Target] u kunt gemakkelijk opstelling en looppas [A/B Test](/help/c-activities/t-test-ab/test-ab.md) en [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activiteiten om de beste aanbiedingen, inhoud, en ervaringen te bepalen.

De fragmenten van de ervaring vertegenwoordigen een enorme stap voorwaarts om de tevreden/ervaringsscheppers en managers aan de optimalisering en verpersoonlijkingsberoeps te verbinden die bedrijfsuitkomsten drijven gebruikend [!DNL Target].

## Vereisten {#section_AE6F0971E1574B3AA324003599B96E5A}

U moet de functionaliteit van ervaringsfragmenten binnen [!DNl Doel]van provisioned zijn. Daarnaast moet u AEM 6.3 gebruiken met het juiste servicepakket of AEM 6.4 (of hoger). Uw accountvertegenwoordiger kan ervoor zorgen dat u voldoet aan de vereisten om deze functie te gebruiken:

* Adobe Experience Manager 6.4 (of hoger).
* Adobe Experience Manager 6.3 SP2 (of hoger).
* Adobe Target Standard of Adobe Target Premium-account.
* Neem contact op met de klantenservice [van](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Adobe Target om de integratie in te schakelen en u verificatiegegevens te verstrekken.

## Het creëren van en het Vormen de Fragmenten van de Ervaring in AEM {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Als u AEM-fragmenten wilt gebruiken in, moet u de volgende stappen uitvoeren: [!DNL Target]

### Stap 1: AEM integreren met doel

Zie voor meer informatie:

* **AEM 6.3**: [U kunt kiezen voor Adobe Analytics en Adobe Target](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) in de documentatie van _Adobe Experience Manager 6.3_ .
* **AEM 6.4**: [U kunt kiezen voor Adobe Analytics en Adobe Target](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) in de documentatie van _Adobe Experience Manager 6.4_ .
* **AEM 6.5**: [U kunt kiezen voor Adobe Analytics en Adobe Target](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html) in de *Adobe Experience Manager 6.5* -documentatie.

### Stap 2: Het ervaringsfragment maken

Experience-fragmenten worden gemaakt in AEM. Zie voor meer informatie:

* **AEM 6.3**: [Ervaar fragmenten](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) in de documentatie van *Adobe Experience Manager 6.3* .
* **AEM 6.4**: [Ervaar fragmenten](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) in de documentatie van *Adobe Experience Manager 6.4* .
* **AEM 6.5**: [Ervaar fragmenten](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html) in de documentatie van *Adobe Experience Manager 6.5* .

### Stap 3: AEM configureren om het ervaringsfragment te delen met Target

1. Selecteer in AEM het gewenste ervaringsfragment of de bijbehorende map en klik op **[!UICONTROL Properties]**.
2. Klik op het **[!UICONTROL Cloud Services]** tabblad en selecteer vervolgens in de **[!UICONTROL Cloud Service Configuration]** vervolgkeuzelijst de optie **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >De vorige stap veronderstelt dat iemand in uw organisatie de [!DNL Adobe Target] configuratie heeft gecreeerd.

3. Klik op **[!UICONTROL Save & Close]**.

### Stap 4: Het ervaringsfragment publiceren en exporteren naar Doel

Afhankelijk van uw AEM-versie raadpleegt u de volgende koppelingen voor stapsgewijze instructies:

* **AEM 6.3**: Een ervaringsfragment [exporteren naar doel](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html) in de documentatie van *Adobe Experience Manager 6.3* .
* **AEM 6.4**: Een ervaringsfragment [exporteren naar doel](https://docs.adobe.com/content/help/en/experience-manager-64/administering/integration/experience-fragments-target.html) in de documentatie van *Adobe Experience Manager 6.4* .
* **AEM 6.5**: Een ervaringsfragment [exporteren naar doel](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html) in de documentatie van *Adobe Experience Manager 6.5* .

## Werken met ervaringsfragmenten in doelactiviteiten {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Nadat u de voorgaande taken hebt uitgevoerd, wordt het ervaringsfragment weergegeven op de [!UICONTROL Offers] pagina in Doel.

>[!NOTE]
>
>[!DNL Target] zoekt momenteel naar ervaringsfragmenten die om de tien minuten moeten worden geïmporteerd. Het geïmporteerde ervaringsfragment moet binnen tien [!DNL Target] minuten beschikbaar zijn, maar dit tijdsbestek kan de voortgang verkorten.

>[!IMPORTANT]
>
>Het ervaringsfragment wordt momenteel geïmporteerd in [!DNL Target] de vorm van een HTML-aanbieding. Het ervaringsfragment &quot;master&quot;-versie blijft in AEM. U kunt het ervaringsfragment niet bewerken in Doel.

U kunt de muisaanwijzer boven een ervaringsfragment in de lijst houden en vervolgens op het pictogram ![](assets/icon_info.png) Weergave klikken om aanvullende informatie over het ervaringsfragment weer te geven, zoals de URL voor de openbare aanbieding, het AEM-pad en een diepe koppeling om het ervaringsfragment in AEM te openen.

U kunt de Fragmenten van de Ervaring in [!DNL Target] activiteiten gebruiken gebruikend Composer [van de](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) Visuele Ervaring (VEC) of de [vorm-Gebaseerde Composer](/help/c-experiences/form-experience-composer.md)van de Ervaring.

>[!NOTE]
>
>Als u de [!DNL Target] AI- en ML-functionaliteit volledig wilt gebruiken, selecteert u [Automatisch toewijzen](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) of [Automatisch toewijzen](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) tijdens het maken van een A/B-test.

**Om de Fragmenten van de Ervaring te verbruiken gebruikend VEC:**

1. In [!DNL Target], terwijl het creëren van of het uitgeven van een ervaring in Composer [van de](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)Visuele Ervaring, klik de plaats op de pagina waar u AEM inhoud wilt opnemen, dan selecteer de gewenste optie om de [!UICONTROL Choose an Experience Fragment] lijst te tonen.

   * [!UICONTROL Insert Before]
   * [!UICONTROL Insert After]
   * [!UICONTROL Swap with Experience Fragment]
   In de [!UICONTROL Experience Fragment] lijst wordt alle inhoud weergegeven die in AEM is gemaakt en die nu oorspronkelijk beschikbaar is vanuit de lijst [!DNL Target].

   >[!NOTE]
   >
   >De [!UICONTROL Swap with Experience Fragment] optie is niet beschikbaar voor afbeeldingen. Als u deze optie bij een afbeelding wilt gebruiken, klikt u op het containerelement dat de gewenste afbeelding bevat.

   ![](assets/experience_fragment_list.png)

1. Selecteer het gewenste ervaringsfragment en klik op **[!UICONTROL Done]**.
1. Voltooi de configuratie van de activiteit.

   Voor meer informatie over het vormen van de diverse activiteitentypes, zie de volgende onderwerpen:

   * **A/B-test:** Een A/B-test [maken](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
   * **Automatisch toewijzen:** [Automatisch toewijzen](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Automatisch doel:** [Auto-Target voor persoonlijke ervaringen](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)
   * **Automatische personalisatie (AP):** Een [geautomatiseerde personalisatieactiviteit maken](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Gericht op ervaring (XT):** Een ervaring [maken die gericht is op activiteiten](../../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **MVT (Multivariate Test):** Een multivariatietest [maken](../../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Aanbevelingen:** Activiteit voor aanbevelingen [maken](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**Met de Form-based Experience Composer kunt u Experience Fragments gebruiken:**

1. Selecteer tijdens het maken of bewerken van [!DNeen ervaring in de]Form-Based Experience Composer [in Doel](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)de locatie op de pagina waar u AEM-inhoud wilt invoegen en selecteer vervolgens **[!UICONTROL Change Experience Fragment]** om de [!UICONTROL Choose an Experience Fragment] lijst weer te geven.

   ![](assets/experience_fragment_list.png)

   In de [!UICONTROL Experience Fragment] lijst wordt alle inhoud weergegeven die in AEM is gemaakt en die nu oorspronkelijk beschikbaar is vanuit de lijst [!DNL Target].

1. Selecteer het gewenste ervaringsfragment en klik op **[!UICONTROL Save]**.
1. Voltooi de configuratie van de activiteit.

## Overwegingen {#considerations}

* [!DNL Target] zoekt momenteel naar ervaringsfragmenten die om de tien minuten moeten worden geïmporteerd. Het geïmporteerde ervaringsfragment moet binnen tien [!DNL Target] minuten beschikbaar zijn, maar dit tijdsbestek kan de voortgang verkorten.
* Het ervaringsfragment wordt momenteel geïmporteerd in [!DNL Target] de vorm van een HTML-aanbieding. Het ervaringsfragment &quot;master&quot;-versie blijft in AEM. U kunt het ervaringsfragment niet bewerken in [!DNL Target].
* U kunt JSON-aanbiedingen importeren als ervaringsfragmenten in [!DNL Target]. Deze aanbiedingen worden echter geïmporteerd als HTML-aanbiedingen. JSON-aanbiedingen (ervaringsfragmenten) worden momenteel niet volledig ondersteund in de [!DNL Target] gebruikersinterface.

## Trainingsvideo: AEM Experience Fragments gebruiken met Adobe Target {#section_C0EDC54063464F41A182492D2045BC64} ![Tutorial badge](/help/assets/overview.png)

In de volgende video ziet u hoe u ervaringsfragmenten instelt en gebruikt:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

Zie [Experience Fragments gebruiken met Adobe Target](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) op de pagina Video&#39;s en zelfstudies voor *AEM-sites* voor meer informatie.
