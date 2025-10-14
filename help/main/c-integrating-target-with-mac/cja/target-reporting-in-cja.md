---
keywords: analyse van de reis van de klant;de analyse van de klantenreis voor doel;de rapporteringsbron van de klantenreis analyseert;de analyse van de klantenreis als rapporteringsbron voor doel;doelrapportering in cja; doelrapportering in Customer Journey Analytics
description: Het gebruik  [!DNL Target]  dat in  [!DNL Adobe Customer Journey Analytics]  rapporteert om activiteiten tot stand te brengen die op  [!DNL Customer Journey Analytics]  worden gebaseerd omzettingsmetriek en publiekssegmenten en gebruik  [!DNL Customer Journey Analytics]  rapporten om resultaten te onderzoeken.
title: Wat is  [!DNL Target]  rapporterend in  [!DNL Adobe Customer Journey Analytics]?
feature: Integrations
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
source-git-commit: 05a4358e0115d7bfd13ec715a0e7eb96f1f2265b
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 0%

---

# [!DNL Target] rapporten in [!DNL Adobe Customer Journey Analytics]

De integratie tussen [&#x200B; Adobe Customer Journey Analytics &#x200B;](https://experienceleague.adobe.com/nl/docs/customer-journey-analytics){target=_blank} en [!DNL Target] verstrekt krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma.

De belangrijkste voordelen van het gebruik van [!DNL Customer Journey Analytics] als rapportagebron voor [!DNL Target] zijn:

* Marketers kunnen [!DNL Customer Journey Analytics] succeswaarden op elk gewenst moment dynamisch toepassen op activiteitenrapporten van [!DNL Target] . U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* De tellers kunnen uit [!DNL Customer Journey Analytics] eigenschappen, zoals het [&#x200B; Comité van de Experimentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank} voordeel halen, om hun websiteverpersoonlijking verder te analyseren.
* Marketers kunnen één bron voor rapportage voor [!DNL Adobe Journey Optimizer] en [!DNL Target] hebben. Beide verpersoonlijkingsproducten kunnen met [!DNL Customer Journey Analytics] voor een meer holistische mening van uw Webverpersoonlijking worden verbonden.

## Overwegingen

Overweeg de volgende informatie voordat u de [!DNL Customer Journey Analytics] - en [!DNL Target] -integratie gebruikt:

>[!IMPORTANT]
>
>Deze integratie is niet hetzelfde als [[!UICONTROL Adobe Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). De implementatie en de ondersteunde activiteitstypen zijn verschillend. Lees dit artikel aandachtig door voordat u deze integratie gebruikt voor uw [!DNL Target] -activiteiten.

* Als u [!DNL Customer Journey Analytics] als rapportagebron voor [!DNL Target] wilt gebruiken, moeten zowel u als uw bedrijf toegang hebben tot [!DNL Customer Journey Analytics] en [!DNL Target] . Als u toegang tot een van beide oplossingen nodig hebt, neemt u contact op met de beheerder van uw organisatie of uw accountvertegenwoordiger.
* Als u [!DNL Target] -activiteiten wilt maken met [!DNL Customer Journey Analytics] -rapportage, moet u de rol &quot;[!UICONTROL Approver]&quot; of &quot;[!UICONTROL Editor]&quot; in [!DNL Target] hebben.
   * Als u a [&#x200B; Target Standard &#x200B;](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) rekening hebt, zie [&#x200B; rollen en toestemmingen &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers* specificeren.
   * Als u a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) rekening hebt, zie [&#x200B; Rollen en toestemmingen &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *de gebruikerstoestemmingen van de Onderneming*.

* Maak deel uit van een rol in [!DNL Adobe Experience Platform] om een [!DNL Target] activiteit met [!DNL Customer Journey Analytics] als rapportagebron in te stellen. Voor meer informatie, zie [&#x200B; een Rol in  [!DNL Adobe Experience Platform] &#x200B;](https://experienceleague.adobe.com/nl/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions#add-a-role-in-adobe-experience-platform-requires-a-system-administrator-or-product-admin){target=_blank} in *vormen toestemmingen* in het *Architect van Gegevens en het Leerprogramma van de Ingenieur toevoegen.*
* Afhankelijk van uw instellingen kan de rapportage per activiteit of op organisatieniveau worden gewijzigd. Zie [&#x200B; het Melden van de Oplossing van de Wolk &#x200B;](/help/main/administrating-target/reporting.md#solution) in *het melden in Doel* vormen.
* Gebruik één rapporteringsbron of andere. U kunt geen gegevens voor één activiteit aan veelvoudige rapporteringsbronnen verzamelen.
* Wanneer u [!DNL Customer Journey Analytics] instelt als rapportbron, wordt u gevraagd de sandbox voor rapportage op te geven. Tijdens de configuratie ziet u alleen de sandboxen waartoe u toegang hebt.
* Bestaande [!DNL Target] -activiteiten blijven gebruikmaken van [!DNL Target] -gegevensverzameling en worden niet beïnvloed door het inschakelen van deze integratie.
* Om deze integratie te gebruiken, heeft de aangewezen implementatiemethode [[!DNL Adobe Experience Platform] &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform){target=_blank} en [!DNL Target] uitgevoerd door [[!DNL Adobe Experience Platform Web SDK] &#x200B;](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}.

  Als u momenteel niet [!DNL Adobe Experience Platform Web SDK] uitgevoerd hebt, kunt u een [[!DNL Adobe Analytics]  bronverbinding &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics) ook creëren om de gegevens in [!DNL Adobe Experience Platform] te brengen. Als u deze methode wilt gebruiken, moet u een [!DNL Analytics] rapportsuite selecteren naast de [!DNL Adobe Experience Platform] sandbox die u gebruikt met [!DNL Customer Journey Analytics] .

  ![&#x200B; optie Sandbox in het de dialoogvakje van de Montages van de Rapportering &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/aep-sandbox.png)

  >[!NOTE]
  >
  >Als u een [!DNL Adobe Analytics] -bronverbinding gebruikt, ziet u rapporten in zowel [!DNL Adobe Analytics] als [!DNL Customer Journey Analytics] . Vanwege verschillende algoritmen tussen beide oplossingen zullen de resultaten echter waarschijnlijk niet overeenkomen.

* Voor om het even welke vragen over timing, zie [&#x200B; Latentie overwegingen &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-overview/cja-faq#latency){target=_blank} in *Veelgestelde Vragen* in de *[!DNL Adobe Customer Analytics]Gids*.

## Ondersteunde activiteitstypen {#supported-activities}

De volgende activiteitentypes worden gesteund wanneer het gebruiken van [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} of de [&#x200B; at.js &#x200B;](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/overview){target=_blank} bibliotheek van JavaScript:

| Typen activiteiten | Ondersteund? |
|--- |--- |
| [&#x200B; A/B activiteit met handverkeer spleet &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |
| [&#x200B; A/B activiteit met auto-Wijs &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe | Nee |
| [&#x200B; activiteit A/B met auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Nee |
| [&#x200B; Ervaring die (XT) richt &#x200B;](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |
| [&#x200B; Multivariate test (MVT) &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja |
| [&#x200B; Automated Personalization (AP) activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nee |
| [&#x200B; activiteit van Aanbevelingen &#x200B;](/help/main/c-recommendations/recommendations.md) | Ja |

## Een activiteit maken die [!DNL Customer Journey Analytics] als bron voor rapportage gebruikt

Het maken van een [!DNL Target] -activiteit die [!DNL Customer Journey Analytics] als rapportagebron gebruikt, lijkt op het instellen van een normale [!DNL Target] -activiteit.

>[!TIP]
>
>U kunt ook opgeven dat [!DNL Target] rapportage in [!DNL Customer Journey Analytics] gebruikt voor alle activiteiten die in uw account worden gemaakt ( **[!UICONTROL Administration]** > **[!UICONTROL Reporting]** > **[!UICONTROL Reporting Experience Cloud Solution]** ). Voor meer informatie, zie *het Melden van de Oplossing van de Wolk* in [&#x200B; het melden in  [!DNL Target]](/help/main/administrating-target/reporting.md#solution) vormt.

1. Van de **[!UICONTROL Activities]** lijst, klik **[!UICONTROL Create Activity]**, dan selecteer het activiteitstype (volgens het [&#x200B; gesteunde activiteitengrafiek hierboven &#x200B;](#supported-activities)) en begin vestiging de activiteit.
1. Wanneer u op de pagina **[!UICONTROL Goals & Settings]** van de workflow voor het maken van activiteiten met drie delen komt, selecteert u **[!DNL Customer Journey Analytics]** als rapportbron.

   ![&#x200B; Customer Journey Analytics als rapporteringsbronoptie &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >De rapportbron kan niet worden gewijzigd nadat een [!DNL Target] -activiteit actief wordt.

1. Selecteer een sandbox.

   In deze vervolgkeuzelijst ziet u alleen de sandboxen waartoe u toegang hebt. Als een of meer sandboxen waartoe u toegang hebt, niet in de lijst voorkomen, controleert u of u toegang hebt tot de sandbox. De Zorg van de Klant van het contact [&#128279;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) als u kwesties blijft zien.

   ![&#x200B; Uitgezochte zandbak optie &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/sandbox.png)

1. Geef het doel van de activiteit op.

   Selecteer een succesmetrische waarde die u als doel voor elke activiteit wilt gebruiken. U kunt een van de [!DNL Target] omzettingsmetriek kiezen of [!DNL Customer Journey Analytics] metrisch gebruiken.

   ![&#x200B; gebruik een metrische optie van Customer Journey Analytics onder Metrische Goal &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/goal-metric.png)

1. Klik op **[!UICONTROL Save & Close]**.

## Een [!DNL Customer Journey Analytics] -verbinding instellen

Nadat u een [!DNL Target] -activiteit hebt gemaakt, moet u een verbinding maken in [!DNL Customer Journey Analytics] . Als u al een verbinding hebt ingesteld, kunt u de bestaande verbinding gebruiken en verderop stap 4 overslaan. Met de verbinding kan [!DNL Customer Journey Analytics] gegevens ophalen uit de gegevensset voor rapportage.

1. Klik in [!DNL Customer Journey Analytics] op de **[!UICONTROL Connections]** pagina op **[!UICONTROL Create a new connection]** .

   ![&#x200B; Nieuwe verbindingsverbinding tot stand brengen in [!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/assets/create-connection.png)

1. Vorm uw [&#x200B; verbinding en gegevensmontages &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-connections/overview){target=_blank} met de correcte informatie.
1. Voeg de gebeurtenisdataset toe die u toen het vormen van uw gegevensstroom gebruikte.
1. Voeg de **[!UICONTROL Adobe Target Classification Events]** opzoekgegevensset toe en klik vervolgens op **[!UICONTROL Next]** .

   ![&#x200B; voeg de dialoogdoos van gegevensreeksen in Customer Journey Analytics &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/add-datasets.png) toe

1. Vorm uw gebeurtenissendataset.

   Voor meer informatie, zie [&#x200B; datasets &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-connections/create-connection#add-dataset){target=_blank} in *toevoegen en vormen een verbinding* in de *[!DNL Adobe Customer Journey Analytics]Gids*.

1. Configureer uw opzoekgegevensset met het veld [!UICONTROL Key] als &quot;sleutel&quot; en het veld [!UICONTROL Matching] key met het volgende pad:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![&#x200B; de de gebeurtenisdialoogdoos van de Classificaties van Adobe Target in Customer Journey Analytics &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/classifications-events.png)

1. Klik op **[!UICONTROL Add datasets]** en klik vervolgens op **[!UICONTROL Save]** op het volgende scherm om de verbinding te voltooien.

## Gegevensweergaven instellen

Stel een gegevensweergave in in [!DNL Customer Journey Analytics] . Een gegevensweergave zorgt ervoor dat de gegevens van uw verbinding correct kunnen worden gebruikt.

1. Stel de gegevensweergave in en zorg ervoor dat deze naar de hierboven gemaakte verbinding verwijst.

   Voor meer informatie, zie [&#x200B; een gegevensmening &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-dataviews/create-dataview){target=_blank} in de *[!DNL Adobe Customer Journey Analytics]Gids* creëren of uitgeven.

1. Als u de [!DNL Target] gegevens correct wilt weergeven in [!DNL Customer Journey Analytics] , moet u de volgende velden uit de gegevensset Opzoeken toevoegen als afmetingen:

   * [!UICONTROL Experience Name]
   * [!UICONTROL Experience ID]
   * [!UICONTROL Activity Name]
   * [!UICONTROL Activity ID]

   ![&#x200B; Namen en IDs opties in Customer Journey Analytics &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Als u [!DNL Target] -afmetingen wilt gebruiken in het deelvenster [!UICONTROL Experimentation] , stelt u de volgende contextlabels in:

   * Gebruik voor [!UICONTROL Activity Name] &quot;Experimentatie-experiment&quot;.
   * [!UICONTROL Experience Name] gebruikt u &quot;Experimentatievariant&quot;.

   ![&#x200B; de etiketten van de Context in het paneel van de Experimentatie &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/context-labels.png){width="600" zoomable="yes"}

1. Voltooi het instellen van andere velden en klik vervolgens op **[!UICONTROL Save and continue]** wanneer u klaar bent.

## Activiteitenrapporten maken en weergeven in [!DNL Customer Journey Analytics]

Nadat u de instellingen hebt voltooid, [!DNL Customer Journey Analytics] via het tabblad [!DNL Adobe Experience Cloud] of [!UICONTROL Reports] van de activiteit in [!DNL Target] .

Het tabblad Rapporten bevat een koppeling **[!UICONTROL View in Customer Journey Analytics]** . Deze koppeling leidt u momenteel om naar de startpagina van [!DNL Customer Journey Analytics] .

![&#x200B; CJA die verbinding &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/report-link.png) meldt

>[!NOTE]
>
>Deze integratie is niet hetzelfde als [!UICONTROL Adobe Analytics for Target] (A4T).
>
>* De [!DNL Target]/ [!DNL Customer Journey Analytics] integratie omvat geen vooraf gebouwd rapport zoals A4T. Activiteitenrapporten moeten in [!DNL Customer Journey Analytics] zijn ingebouwd.
>
>* Als [!UICONTROL Use a CJA Metric] wordt geselecteerd als het doel van de activiteit metrisch wordt geselecteerd, verstrekt deze optie flexibiliteit aan wanneer specifieke succesmetriek moet worden bepaald. De succesmetrische waarde wordt geselecteerd wanneer het vormen van het [!UICONTROL Experimentation] paneel. Lift en betrouwbaarheid worden berekend aan de hand van de geselecteerde CJA-maatstaf.

1. Maak in [!DNL Customer Journey Analytics] een deelvenster Experimentatie en selecteer vervolgens de activiteit in het vervolgkeuzemenu **[!UICONTROL Experiment]** .

   Voor meer informatie, zie [&#x200B; het paneel van de Experimentatie van 0&rbrace; onder &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/panels/experimentation?lang=en#use){target=_blank} het paneel van de Experimentatie *in de* gids.*[!DNL Customer Journey Analytics]*

   ![&#x200B; het paneel van de Experimentatie in Customer Journey Analytics &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/experimentation-panel.png)

   >[!IMPORTANT]
   >
   >Als de activiteit niet in de [!UICONTROL Experiment] drop-down lijst verschijnt, verifieer dat de correcte gegevensmening wordt geselecteerd en dat de [!DNL Target] afmetingen de vereiste contextetiketten omvatten (zie Stap 3 in [&#x200B; de meningen van opstellingsgegevens &#x200B;](https://experienceleague.adobe.com/nl/docs/target/using/integrate/cja/target-reporting-in-cja#set-up-data-views){target=_blank}).

1. Klik op **[!UICONTROL Build]**.

   Het deelvenster [!UICONTROL Experimentation] retourneert een uitgebreide set gegevens en visualisaties om u te helpen beter te begrijpen hoe uw experimenten werken. Voor meer informatie, zie [[!UICONTROL Panel output] &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-workspace/panels/experimentation#panel-output){target=_blank} onder *het paneel van de Experimentatie* in de *[!DNL Customer Journey Analytics]* gids.

   ![&#x200B; Experimentatie &#x200B;](/help/main/c-integrating-target-with-mac/cja/assets/experimentation.png)