---
keywords: cja4t;analyse van de klantenreis;de analyse van de klantenreis voor doel;de rapporteringsbron van de klantenreis analyseert;de analyse van de klantenreis als rapporteringsbron voor doel
description: Gebruiken [!DNL Adobe Customer Journey Analytics] for [!DNL Target] (A4T) om activiteiten te creëren op basis van [!DNL Customer Journey Analytics] conversiemetriek en publiekssegmenten en gebruik [!DNL Customer Journey Analytics] verslagen om de resultaten te onderzoeken.
title: Wat is [!DNL Adobe Customer Journey Analytics] for [!DNL Target] (CJA4T)?
feature: Integrations
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn bètafuncties in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
source-git-commit: 16b325431224dfb6cd3e580937f6a3989d0ca577
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 0%

---

# [!DNL Adobe Customer Journey Analytics] als bron van rapportage voor [!DNL Adobe Target] (CJA4T)

De [!DNL Customer Journey Analytics for Target] (CJA4T) integratie tussen [Adobe Customer Journey Analytics (JA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html){target=_blank} en [!DNL Target] biedt krachtige hulpmiddelen voor analyse en tijdbesparend maken voor uw optimalisatieprogramma.

De belangrijkste voordelen van het gebruik [!DNL Customer Journey Analytics] als bron van rapportage voor [!DNL Target] zijn:

* Marketers kunnen dynamisch toepassen [!DNL Customer Journey Analytics] succescijfers naar [!DNL Target] activiteitenverslagen op elk moment. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Profiteer van [!DNL Customer Journey Analytics] functies, zoals de [Deelvenster Experimentatie](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/experimentation.html){target=_blank}, om de personalisatie van uw website verder te analyseren.
* Eén rapportagebron hebben voor [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/cja-ajo.html){target=_blank} en [!DNL Target]. Beide verpersoonlijkingsproducten kunnen met worden verbonden [!DNL Customer Journey Analytics] voor een meer holistische mening van uw Webverpersoonlijking.

## Overwegingen

Overweeg de volgende informatie alvorens de integratie te gebruiken CJA4T:

* Te gebruiken [!DNL Customer Journey Analytics] als bron van rapportage voor [!DNL Target], zowel u als uw bedrijf moeten toegang hebben tot [!DNL Customer Journey Analytics] en [!DNL Target]. Als u toegang tot een van beide oplossingen nodig hebt, neemt u contact op met de beheerder van uw organisatie of uw accountvertegenwoordiger.
* Om te creëren [!DNL Target] activiteiten met [!DNL Customer Journey Analytics] melden, moet u een van de &quot;[!UICONTROL Approver]&quot; of &quot;[!UICONTROL Editor]&quot; rol in [!DNL Target].
   * Als u een [Doelstandaard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) account, zie [Rollen en machtigingen opgeven](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers*.
   * Als u een [Doelpremie](/help/main/c-intro/intro.md#premium) account, zie [Rollen en machtigingen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Machtigingen voor Enterprise-gebruikers*.

* U moet deel uitmaken van een rol in [!DNL Adobe Experience Platform] een [!DNL Target] activiteit met [!DNL Customer Journey Analytics] als de bron van de rapportage. Zie voor meer informatie [Een rol toevoegen in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions.html){target=_blank} in *Machtigingen configureren* in de *Zelfstudie voor gegevensarchitect en engineer.*
* Afhankelijk van uw instellingen kan de rapportage per activiteit of op organisatieniveau worden gewijzigd. Zie [Cloudoplossing rapporteren](/help/main/administrating-target/reporting.md#solution) in *Rapportage in doel configureren*.
* Gebruik één rapporteringsbron of andere. U kunt geen gegevens voor één activiteit aan veelvoudige rapporteringsbronnen verzamelen.
* Wanneer u instelt [!DNL Customer Journey Analytics] als rapportbron wordt u gevraagd de sandbox voor rapportage op te geven. Tijdens de configuratie ziet u alleen de sandboxen waartoe u toegang hebt.
* Bestaande [!DNL Target] activiteiten blijven gebruiken [!DNL Target] gegevensverzameling en worden niet beïnvloed door het inschakelen van CJA4T.
* Als u CJA4T wilt gebruiken, heeft de voorkeursimplementatiemethode het [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform.html){target=_blank} and [!DNL Target] implemented through the [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}. Als u momenteel niet beschikt over de [!DNL Adobe Experience Platform Web SDK] geïmplementeerd, kunt u ook een [[!DNL Adobe Analytics] bronverbinding](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=en) om de gegevens [!DNL Adobe Experience Platform].
* Zie voor vragen over timing [Latentieoverwegingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html#latency){target=_blank} in *Veelgestelde vragen* in de *[!DNL Adobe Customer Analytics]Hulplijn*.

## Ondersteunde activiteitstypen {#supported-activities}

De volgende activiteitstypen worden ondersteund wanneer u de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} or the [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank} JavaScript-bibliotheek:

| Activiteitstypen | Compatibel met CJA4T? |
|--- |--- |
| [A/B-activiteit met handmatige verkeersverdeling](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [A/B-activiteit met automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Nee |
| [A/B activiteit met AutoTarget](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
| [Gericht op ervaring (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [MVT (Multivariate Test)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja |
| [Automated Personalization (AP)-activiteit](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nee |
| [Recommendations-activiteit](/help/main/c-recommendations/recommendations.md) | Ja |

## Een activiteit maken die [!DNL Customer Journey Analytics] als bron van de rapportage

Een [!DNL Target] activiteit die [!DNL Customer Journey Analytics] aangezien de bron van de rapportage vergelijkbaar is met het instellen van een [!DNL Target] activiteit.

1. Van de **[!UICONTROL Activities]** lijst, klik **[!UICONTROL Create Activity]** selecteert u vervolgens het type activiteit (volgens de [ondersteund activiteitenoverzicht boven](#supported-activities)) en beginnen met het instellen van de activiteit.
1. Wanneer u de **[!UICONTROL Goals & Settings]** pagina van de workflow voor het maken van activiteiten in drie delen, selecteert u **[!DNL Customer Journey Analytics]** als de bron van de rapportage.

   ![Customer Journey Analytics als optie voor de bron van de rapportage](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >De rapportbron kan na een [!DNL Target] activiteit gaat live .

1. Selecteer een sandbox.

   In deze vervolgkeuzelijst ziet u alleen de sandboxen waartoe u toegang hebt. Als een of meer sandboxen waartoe u toegang hebt, niet in de lijst voorkomen, controleert u of u toegang hebt tot de sandbox. Contact [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) als er problemen blijven optreden.

   ![Sandbox selecteren, optie](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. Geef het doel van de activiteit op.

   Selecteer een succesmetrische waarde die u als doel voor elke activiteit wilt gebruiken. U kunt een van de [!DNL Target] conversiewaarden of gebruik een [!DNL Customer Journey Analytics] metrisch.

   ![Een Customer Journey Analytics-metrische optie gebruiken onder Geel metrisch](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. Klik op **[!UICONTROL Save & Close]**.

## Een [!DNL Customer Journey Analytics] verbinding

Na een [!DNL Target] activiteit is gecreeerd, moet u een verbinding tot stand brengen in [!DNL Customer Journey Analytics]. Als u al een verbinding hebt ingesteld, kunt u de bestaande verbinding gebruiken en verderop stap 4 overslaan. De verbinding staat [!DNL Customer Journey Analytics] om gegevens uit de gegevensset voor rapportage te halen.

1. In [!DNL Customer Journey Analytics], over de **[!UICONTROL Connections]** pagina, klikt u **[!UICONTROL Create a new connection]**.

   ![Nieuwe verbindingskoppeling maken in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. Configureer uw [verbinding- en gegevensinstellingen](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html){target=_blank} met de juiste informatie.
1. Voeg de gebeurtenisdataset toe die u toen het vormen van uw gegevensstroom gebruikte.
1. Voeg de **[!UICONTROL Adobe Target Classification Events]** opzoekdataset, dan klik **[!UICONTROL Next]**.

   ![Dialoogvenster Gegevenssets toevoegen in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. Vorm uw gebeurtenissendataset.

   Zie voor meer informatie [Gegevenssets toevoegen en configureren](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#add-dataset){target=_blank} in *Verbinding maken* in de *Adobe Customer Journey Analytics Guide*.

1. Vorm uw raadplegingsdataset met de [!UICONTROL Key] veld als &quot;sleutel&quot; en het veld Overeenkomende sleutel met het volgende pad:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Dialoogvenster Adobe Target Classifications-gebeurtenis in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. Klikken **[!UICONTROL Add datasets]** en klik vervolgens op **[!UICONTROL Save]** op het volgende scherm om uw verbinding te voltooien.

## Gegevensweergaven instellen

Een gegevensweergave instellen in [!DNL Customer Journey Analytics]. Een gegevensweergave zorgt ervoor dat de gegevens van uw verbinding correct kunnen worden gebruikt.

1. Stel de gegevensweergave in en zorg ervoor dat deze naar de hierboven gemaakte verbinding verwijst.

   Zie voor meer informatie [Een gegevensweergave maken of bewerken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target=_blank} in de *Adobe Customer Journey Analytics Guide*.

1. Als u uw [!DNL Target] gegevens in [!DNL Customer Journey Analytics], moet u de volgende gebieden van uw Dataset van de Raadpleging als afmetingen toevoegen:

   * Naam van ervaring
   * Ervaring-id
   * Naam activiteit
   * Activiteits-id

   ![Opties voor namen en id&#39;s in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Te gebruiken [!DNL Target] afmetingen in de [!UICONTROL Experimentation] stelt u de volgende contextlabels in:

   * Voor [!UICONTROL Activity Name], gebruik &quot;Experimentatiedeskundige&quot;.
   * [!UICONTROL Experience Name], gebruik &quot;Variant van de Experimentatie.&quot;

   ![Contextlabels in het deelvenster Experimentatie](/help/main/c-integrating-target-with-mac/cja4t/assets/context-labels.png){width="600" zoomable="yes"}

1. Stel andere velden in en klik op **[!UICONTROL Save and continue]** wanneer gereed.
