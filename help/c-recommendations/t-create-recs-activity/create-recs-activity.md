---
keywords: create recommendations;recommendations activity;new recommendations;recommendations overview
description: Gebruik de Composer van de Ervaring van het Doel Visuele (VEC) om een activiteit van Recommendations direct op een Doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen Doel te wijzigen.
title: Een Recommendations-activiteit maken
feature: recs creation
uuid: c3f22cce-204a-4509-92c4-8fec43fbaebe
translation-type: tm+mt
source-git-commit: d5a48db0c954871269714ef32d0545ed4898660f
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Een Recommendations-activiteit maken{#create-a-recommendations-activity}

Gebruik de Composer van de Ervaring van het Doel Visuele (VEC) om een activiteit van Recommendations direct op een Doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen Doel te wijzigen.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

   ![Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/assets/Menu_CreateActivity.png)

1. Selecteer **[!UICONTROL Visual (Default)]** indien nodig.

   ![Recommendations-activiteit maken, dialoogvenster](/help/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   Selecteer [!UICONTROL Form]Formulier-based Experience Composer als u liever wilt gebruiken. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Zie [Ervaringen en Aanbiedingen](/help/c-experiences/experiences.md)voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.
   >
   >De [!UICONTROL [Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorgaande illustratie is een [doelpremiumfunctie](/help/c-intro/intro.md) . Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een klant [van de Premium van het](/help/c-intro/intro.md#premium)Doel bent, kies een [werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef een activiteit-URL op en klik op **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide overeen.

   De activiteiten-URL is de pagina waarop de aanbevelingen worden weergegeven.

   Wanneer u klikt [!UICONTROL Next], opent VEC en toont uw pagina. U kunt een huidig element met aanbevelingen, of tussenvoegselaanbevelingen vervangen.

1. Klik op een element op de pagina en klik op **[!UICONTROL Replace w/ Recommendations]** of **[!UICONTROL Insert Recommendations Before]** of **[!UICONTROL Insert Recommendations After]** als er aanbevelingen beschikbaar zijn.

   ![Recommendations-opties](/help/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   Als u een element vervangt door aanbevelingen, wordt de huidige inhoud verwijderd en vervangen door uw aanbevelingen.

1. Selecteer een paginatype.

   Paginatypen kunnen het volgende zijn:

   * Winkelpagina
   * Categoriepagina
   * Startpagina
   * Openingspagina
   * Productpagina
   * Pagina met zoekresultaten
   * Dankbriefje
   * Overige

   ![Opties voor paginatype selecteren](/help/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. Selecteer een of meer [criteria](/help/c-recommendations/c-algorithms/algorithms.md).

   De criteria worden getoond als kaarten die informatie over elke criteria tonen. Standaard worden op het [!UICONTROL Select Criteria] scherm criteria weergegeven die compatibel zijn met de verticale instellingen en het geselecteerde paginatype. U kunt deze opties wijzigen om andere criteria weer te geven.

   >[!NOTE]
   >
   >Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het selectievakje moet worden ingeschakeld `entity.id` of `entity.categoryId` de huidige aanbevelingen voor het item of de huidige categorie zijn compatibel. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, schakelt u het **[!UICONTROL Compatible]** selectievakje uit. De [!UICONTROL Compatible] optie wordt mogelijk niet weergegeven, afhankelijk van uw Recommendations-instellingen ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**). Zie [Instellingen](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84)voor meer informatie.

   ![Selectiecriteria, dialoogvenster](/help/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

   * Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als een groot aantal kaarten met criteria wordt weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u **[!UICONTROL Next]**.

      Er worden enkele criteria verstrekt [!DNL Recommendations]. U en uw team kunnen ook uw eigen aangepaste criteria maken.

   * Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult u de gegevens voor de nieuwe criteria in. Zie [Criteria](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE)maken voor meer informatie over het maken van nieuwe criteria.
   * U kunt criteria ook in reeksen groeperen. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Zie [Criteria-reeksen](../../c-recommendations/c-algorithms/create-criteria-sequence.md#task_8A9CB465F28D44899F69F38AD27352FE) maken voor meer informatie.

1. Klik op **[!UICONTROL Next]**.
1. Selecteer een [ontwerp](/help/c-recommendations/c-design-overview/design-overview.md).

   Een ontwerp is een sjabloon die het uiterlijk van de locaties op de pagina bepaalt. [!DNL Target] omvat verscheidene preconfigured ontwerpen. U kunt ook uw eigen aangepaste ontwerpen maken. Zie [Een ontwerp](../../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) maken en een ontwerp [](../../c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59)aanpassen voor meer informatie.

   ![Ontwerp selecteren, dialoogvenster](/help/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Elk ontwerp toont een grafische voorstelling van hoe het eruit zal zien, en pictogrammen die tonen hoeveel van uw levende en inactieve activiteiten momenteel dat ontwerp gebruiken.

   * Als u een of meer bestaande ontwerpen wilt selecteren, klikt u op de ontwerpen en vervolgens op **[!UICONTROL Next]**.

      Als u meerdere criteria hebt geselecteerd, kunt u slechts één ontwerp selecteren.

   * Als u een aangepast ontwerp wilt maken, klikt u **[!UICONTROL Create Design]** en vult u vervolgens de naam en code voor het nieuwe ontwerp in. Klik **[!UICONTROL Next]**, selecteer of upload een beeld en klik **[!UICONTROL Done]** > **[!UICONTROL Done]**. Zie Een ontwerp [maken voor informatie over het maken van een nieuw ontwerp](../../c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klik op **[!UICONTROL Next]**.

   U kunt speciale acties toevoegen aan uw aanbevelingen. Zie Promoties [toevoegen voor meer informatie over het toevoegen van promoties](../../c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14)aan voor- en achterzijde.
1. Klik op **[!UICONTROL Save]**.

   In het VEC-scherm wordt het aanbevolen ontwerp op de pagina weergegeven.

1. (Optioneel) Klik **[!UICONTROL Preview]** om te zien hoe de activiteit eruit zal zien voor bezoekers.

   [!UICONTROL Preview] in de modus kunt u op dezelfde manier werken met uw aanbevelingen als een bezoeker.

   Klik wanneer u klaar bent met het voorvertonen van uw aanbevelingen. **[!UICONTROL Compose]**

1. Herzie uw aanbeveling in VEC, dan klik **[!UICONTROL Next]**.

1. Controleer uw [!DNL Recommendations] activiteit in het stroomdiagram en breng de noodzakelijke veranderingen aan.

   ![Recommendations-stroomdiagram](/help/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen, opstellingservaringen, en succesmetriek te specificeren.

   Vanuit het stroomdiagram kunt u het volgende doen:

   * Wijzig het publiek dat de aanbevelingen zal zien

      >[!NOTE]
      >
      >Naast het selecteren van een bestaand publiek, kunt u een activiteit-slechts publiek [](../../c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) tot stand brengen of veelvoudige publiek [](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) combineren om ad hoc publiek tot stand te brengen eerder dan het creëren van een nieuw publiek.

      Standaard zien alle gebruikers de aanbevelingen. U kunt de aanbeveling echter richten op een specifiek publiek.

      Voor een [!DNL Recommendations] activiteit, ziet de controlegroep de pagina zonder enige aanbevelingen.

   * De criteria weergeven
   * De verzameling wijzigen (naast het [!UICONTROL Criteria] label)
   * Wijzig het percentage gegadigden dat de controleervaring ziet
   * De ontwerpcode weergeven
   * Een ontwerp wijzigen of verwijderen

1. Klik **[!UICONTROL Next]** wanneer gebeëindigd.
1. Geef de activiteitinstellingen op.

   Typ bijvoorbeeld een naam (vereist) en een doelstelling (optioneel) voor de activiteit. Zie [Recommendations Activity Settings](../../c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)voor informatie over de instellingen.

   >[!NOTE]
   >
   >Als u een [!DNL Recommendation] activiteitennaam opgeeft die al bestaat voor een andere activiteit in [!DNL Recommendations Classic], wordt de nieuwe activiteit opnieuw gesynchroniseerd met een nieuwe naam. De nieuwe naam is de oorspronkelijke naam die met een tijdstempel is toegevoegd om deze uniek te maken. Deze nieuwe naam wordt zowel in [!DNL Target Standard/Premium] als [!DNL Recommendations Classic].

1. Klik wanneer u klaar bent op **[!UICONTROL Save & Close]**.

   Er wordt een overzicht van uw activiteiten weergegeven.

   Op de [!UICONTROL Overview] pagina kunt u:

   * De activiteit activeren
   * De activiteit bewerken
   * De activiteit vastzetten op het Experience Cloud-bord
   * Ervings-URL&#39;s weergeven
   * Gegevens downloaden
   * Wijzig het percentage deelnemers aan de activiteit die de controleervaring zien
   * Criteria-details tonen of verbergen
   * De code voor uw ontwerpen weergeven

1. (Optioneel) Open de [!UICONTROL Reports] pagina om het rapport weer te geven met de prestaties van uw [!DNL Recommendations] activiteit.
1. (Optioneel) Open de [!UICONTROL Collisions] pagina om eventuele [activiteitenconflicten](/help/c-experiences/c-visual-experience-composer/activity-collisions.md) weer te geven.

   Er treden conflicten op wanneer meerdere activiteiten zijn ingesteld om inhoud te leveren aan dezelfde pagina. Hierdoor kan onverwachte inhoud worden weergegeven.

## Trainingsvideo: Een ![zelfstudie met een Recommendations-activiteit maken (7:15)](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)