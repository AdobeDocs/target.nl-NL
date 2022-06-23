---
keywords: aanbevelingen maken;aanbevelingen, activiteit;nieuwe aanbevelingen;aanbevelingen, overzicht
description: Leer hoe u de Adobe gebruikt [!DNL Target] Visual Experience Composer (VEC) om een Recommendations-activiteit rechtstreeks op een [!DNL Target]-enabled pagina.
title: Hoe maak ik een Recommendations-activiteit?
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Een Recommendations-activiteit maken

Gebruik de Composer van de Ervaring van het Doel Visuele (VEC) om een activiteit van Recommendations direct op een Doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen Doel te wijzigen.

1. Klik op **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

   ![Recommendations-activiteit maken](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_CreateActivity.png)

1. Selecteren **[!UICONTROL Visual (Default)]**, indien nodig.

   ![Recommendations-activiteit maken, dialoogvenster](/help/main/c-recommendations/t-create-recs-activity/assets/DB_NewRecAct.png)

   Selecteer [!UICONTROL Form]. Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor meer informatie .

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Voor meer informatie over de verschillende composers raadpleegt u [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Het oplossen van problemen de Visuele Composer van de Ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >De [!UICONTROL [Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) optie in de voorgaande illustratie is een [Doelpremie](/help/main/c-intro/intro.md) gebruiken. Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een [De klant van de Premium van het doel](/help/main/c-intro/intro.md#premium), kiest u een [werkruimte](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef een activiteit-URL op en klik vervolgens op **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Dientengevolge [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide komen overeen.

   De activiteiten-URL is de pagina waarop de aanbevelingen worden weergegeven.

   Wanneer u op [!UICONTROL Next], opent VEC en toont uw pagina. U kunt een huidig element met aanbevelingen, of tussenvoegselaanbevelingen vervangen.

1. Klik op een element op de pagina en klik vervolgens op **[!UICONTROL Replace w/ Recommendations]**, **[!UICONTROL Insert Recommendations Before]**, of **[!UICONTROL Insert Recommendations After]**.

   Bezoekers van uw site zien de aanbevolen inhoud alleen als ze in aanmerking komen voor de aanbeveling. Bezoekers die niet in aanmerking komen voor de aanbeveling, zien de standaardinhoud.

   ![Recommendations-opties](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: Als u een element vervangt door aanbevelingen, wordt de huidige inhoud verwijderd en vervangen door uw aanbevelingen. Wanneer bezoekers uw site bezoeken en in aanmerking komen voor de aanbeveling, zien ze de aanbevolen items in het opgegeven gebied in plaats van de bestaande inhoud.
   * **[!UICONTROL Insert Recommendations Before]**: Als u aanbevelingen invoegt voordat het geselecteerde element de aanbevolen inhoud vóór dat element plaatst. Afhankelijk van de constructie van uw pagina wordt de aanbeveling boven of links van het geselecteerde element weergegeven.
   * **[!UICONTROL Insert Recommendations After]**: Als u aanbevelingen invoegt nadat het geselecteerde element de aanbevolen inhoud na dat element heeft geplaatst. Afhankelijk van de constructie van uw pagina wordt de aanbeveling onder of rechts van het geselecteerde element weergegeven.

   De **[!UICONTROL Expand Selection]** Met deze optie kunt u de geselecteerde locatie (de bovenliggende container) uitbreiden, zodat u de gewenste pagina-elementen gemakkelijker kunt herkennen en opnemen.

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

   ![Opties voor paginatype selecteren](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. Selecteer een of meer [criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).

   De criteria worden getoond als kaarten die informatie over elke criteria tonen. Standaard worden de [!UICONTROL Select Criteria] op het scherm worden criteria weergegeven die compatibel zijn met de verticale instellingen van uw bedrijf en het paginatype dat u in de vorige stap hebt geselecteerd. U kunt deze opties wijzigen om andere criteria weer te geven.

   >[!NOTE]
   >
   >Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het selectievakje moet worden ingeschakeld `entity.id` of `entity.categoryId` voor het huidige item of de huidige categorie. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, wist u de optie **[!UICONTROL Compatible]** selectievakje. De [!UICONTROL Compatible] deze optie wordt mogelijk niet weergegeven, afhankelijk van uw Recommendations-instellingen ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]**). Zie voor meer informatie [Instellingen](https://developer.adobe.com/target/implement/recommendations/).

   ![Selectiecriteria, dialoogvenster](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

   * Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als een groot aantal kaarten met criteria wordt weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u op **[!UICONTROL Next]**.

      Sommige criteria worden verstrekt [!DNL Recommendations]. U en uw team kunnen ook uw eigen aangepaste criteria maken.

   * Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult vervolgens de informatie voor de nieuwe criteria in. Voor informatie over het creëren van nieuwe criteria, zie [Criteria maken](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * U kunt criteria ook in reeksen groeperen. Als u een nieuwe reeks criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. Zie [Criteria-reeks maken](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md) voor meer informatie .

1. Klik op **[!UICONTROL Next]**.
1. Selecteer een [ontwerp](/help/main/c-recommendations/c-design-overview/design-overview.md).

   Een ontwerp is een sjabloon die het uiterlijk van de locaties op de pagina bepaalt. [!DNL Target] bevat verschillende vooraf geconfigureerde ontwerpen. U kunt ook uw eigen aangepaste ontwerpen maken. Zie voor meer informatie [Een ontwerp maken](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) en [Een ontwerp aanpassen](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![Ontwerp selecteren, dialoogvenster](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Elk ontwerp toont een grafische voorstelling van hoe het eruit zal zien, en pictogrammen die tonen hoeveel van uw levende en inactieve activiteiten momenteel dat ontwerp gebruiken.

   * Als u een of meer bestaande ontwerpen wilt selecteren, klikt u op de ontwerpen en vervolgens op **[!UICONTROL Next]**.

      Als u meerdere criteria hebt geselecteerd, kunt u slechts één ontwerp selecteren.

   * Als u een aangepast ontwerp wilt maken, klikt u op **[!UICONTROL Create Design]** en vult vervolgens de naam en de code voor het nieuwe ontwerp in. Klikken **[!UICONTROL Next]** selecteert of uploadt u vervolgens een afbeelding en klikt u op **[!UICONTROL Done]** > **[!UICONTROL Done]**. Voor informatie over het maken van een nieuw ontwerp raadpleegt u [Een ontwerp maken](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klik op **[!UICONTROL Next]**.

   U kunt speciale acties toevoegen aan uw aanbevelingen. Voor meer informatie over het toevoegen van voor- en achterpromoties raadpleegt u [Promoties toevoegen](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klik op **[!UICONTROL Save]**.

   In het VEC-scherm wordt het aanbevolen ontwerp op de pagina weergegeven.

1. (Optioneel) Klik op **[!UICONTROL Preview]** om te zien hoe de activiteit voor bezoekers wordt weergegeven.

   [!UICONTROL Preview] in de modus kunt u op dezelfde manier werken met uw aanbevelingen als een bezoeker.

   Wanneer u klaar bent met het voorvertonen van uw aanbevelingen, klikt u op **[!UICONTROL Compose]**.

1. Controleer uw aanbeveling in VEC, dan klik **[!UICONTROL Next]**.

1. Controleer uw [!DNL Recommendations] activiteit in het stroomdiagram en breng de noodzakelijke veranderingen aan.

   ![Recommendations-stroomdiagram](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen, opstellingservaringen, en succesmetriek te specificeren.

   Vanuit het stroomdiagram kunt u het volgende doen:

   * Wijzig het publiek dat de aanbevelingen zal zien

      >[!NOTE]
      >
      >Naast het selecteren van een bestaand publiek, kunt u [een alleen-actief publiek maken](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) of [meerdere soorten publiek combineren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) ad-hocdoelgroepen maken in plaats van een nieuw publiek te creëren.

      Standaard zien alle gebruikers de aanbevelingen. U kunt de aanbeveling echter richten op een specifiek publiek.

      Voor een [!DNL Recommendations] activiteit, ziet de controlegroep de pagina zonder enige aanbevelingen.

   * De criteria weergeven
   * De verzameling wijzigen (naast de [!UICONTROL Criteria] label)
   * Wijzig het percentage gegadigden dat de controleervaring ziet
   * De ontwerpcode weergeven
   * Een ontwerp wijzigen of verwijderen

1. Klikken **[!UICONTROL Next]** wanneer gereed.
1. Geef de activiteitinstellingen op.

   Typ bijvoorbeeld een naam (vereist) en een doelstelling (optioneel) voor de activiteit. Voor informatie over de instellingen raadpleegt u [Recommendations Activity Settings](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB).

   >[!NOTE]
   >
   >Als u een [!DNL Recommendation] naam van activiteit die al bestaat voor een andere activiteit in [!DNL Recommendations Classic], wordt de nieuwe activiteit opnieuw gesynchroniseerd met een nieuwe naam. De nieuwe naam is de oorspronkelijke naam die met een tijdstempel is toegevoegd om deze uniek te maken. Deze nieuwe naam wordt in beide weergegeven [!DNL Target Standard/Premium] en [!DNL Recommendations Classic].

1. Als u klaar bent, klikt u op **[!UICONTROL Save & Close]**.

   Er wordt een overzicht van uw activiteiten weergegeven.

   Van de [!UICONTROL Overview] pagina, kunt u:

   * De activiteit activeren
   * De activiteit bewerken
   * De activiteit delen met uw Experience Cloud-feed
   * QA de activiteit
   * Ervings-URL&#39;s weergeven
   * Gegevens downloaden
   * Wijzig het percentage deelnemers aan de activiteit die de controleervaring zien
   * Criteria-details tonen of verbergen
   * De code voor uw ontwerpen weergeven

1. (Optioneel) Open het dialoogvenster [!UICONTROL Reports] pagina om het rapport te bekijken dat de prestaties van uw [!DNL Recommendations] activiteit.

1. (Optioneel) Open het dialoogvenster [!UICONTROL Collisions] pagina om het even welke te bekijken [activiteitenbotsingen](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) dat kan gebeuren .

   Er treden conflicten op wanneer meerdere activiteiten zijn ingesteld om inhoud te leveren aan dezelfde pagina. Hierdoor kan onverwachte inhoud worden weergegeven.

## Trainingsvideo: Een Recommendations-activiteit maken (7:15) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
