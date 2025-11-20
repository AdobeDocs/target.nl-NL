---
keywords: aanbevelingen maken;aanbevelingen, activiteit;nieuwe aanbevelingen;aanbevelingen, overzicht
description: Leer hoe te om  [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) te gebruiken om a  [!DNL Recommendations]  activiteit tot stand te brengen.
title: Hoe creeer ik a [!DNL Recommendations]  Activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: c83073d5-f852-4f09-8343-e4658fbf6f43
source-git-commit: 32b3a93b30c6ca6f7576be5dbb25b476167b33b7
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 0%

---

# Een [!DNL Recommendations] activiteit maken

Gebruik [!DNL Target] [!UICONTROL Visual Experience Composer] (VEC) om een [!DNL Recommendations] -activiteit rechtstreeks op een pagina met [!DNL Target] activering te maken en om delen van de pagina binnen [!DNL Target] te wijzigen.

1. Klik op **[!UICONTROL Activities]** > **[!UICONTROL Create Activity]** > **[!UICONTROL Recommendations]**.

1. Selecteer **[!UICONTROL Visual]**, indien nodig.

   Selecteer [!UICONTROL Form-Based Experience Composer] als u de [!UICONTROL Form] -toets liever wilt gebruiken. Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] ook de VEC. [!UICONTROL Single Page Application] Voor meer informatie over de diverse composers, zie [&#x200B; Ervaringen en Aanbiedingen &#x200B;](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [&#x200B; het Oplossen van problemen de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) kies a [&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef een activiteit-URL op en klik op **[!UICONTROL Create]** .

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http] ). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide overeen.

   De activiteit-URL is de pagina waarop de aanbevelingen worden weergegeven.

   Wanneer u [!UICONTROL Create] klikt, opent VEC en toont uw pagina. U kunt een huidig element met aanbevelingen, of tussenvoegselaanbevelingen vervangen.

1. Klik op een element op de pagina en klik op **[!UICONTROL Replace w/ Recommendations]** , **[!UICONTROL Insert Recommendations Before]** of **[!UICONTROL Insert Recommendations After]** als er aanbevelingen beschikbaar zijn op de locatie van dat element.

   >[!NOTE]
   >
   >[!UICONTROL Recommendations] -activiteiten ondersteunen slechts één wijziging/aanbeveling tegelijk. Voor meerdere aanbevelingen kunt u verschillende [!DNL Recommendations] -activiteiten maken of A/B- of XT-tests gebruiken.

   Bezoekers van uw site zien de aanbevolen inhoud alleen als ze in aanmerking komen voor de aanbeveling. Bezoekers die niet in aanmerking komen voor de aanbeveling, zien de standaardinhoud.

   ![&#x200B; de opties van Aanbevelingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_Replace-Insert.png)

   * **[!UICONTROL Replace w/ Recommendations]**: als u een element vervangt door aanbevelingen, wordt de huidige inhoud verwijderd en vervangen door uw aanbevelingen. Wanneer bezoekers uw site bezoeken en in aanmerking komen voor de aanbeveling, zien ze de aanbevolen items in het opgegeven gebied in plaats van de bestaande inhoud.
   * **[!UICONTROL Insert Recommendations Before]**: wanneer u aanbevelingen invoegt voordat het geselecteerde element de aanbevolen inhoud vóór dat element plaatst. Afhankelijk van de constructie van uw pagina wordt de aanbeveling boven of links van het geselecteerde element weergegeven.
   * **[!UICONTROL Insert Recommendations After]**: wanneer u aanbevelingen invoegt nadat het geselecteerde element de aanbevolen inhoud na dat element heeft geplaatst. Afhankelijk van de constructie van uw pagina wordt de aanbeveling onder of rechts van het geselecteerde element weergegeven.

   Met de optie **[!UICONTROL Expand Selection]** kunt u de geselecteerde locatie (de bovenliggende container) uitvouwen, zodat u de gewenste pagina-elementen gemakkelijker kunt herkennen en opnemen.

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

   ![&#x200B; Uitgezochte opties van het Type van Pagina &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/Menu_PageType.png)

1. Selecteer één of meerdere [&#x200B; criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md).

   De criteria worden getoond als kaarten die informatie over elke criteria tonen. Standaard worden in het scherm [!UICONTROL Select Criteria] criteria weergegeven die compatibel zijn met de verticale instellingen van uw bedrijf en het paginatype dat u in de vorige stap hebt geselecteerd. U kunt deze opties wijzigen en andere criteria weergeven.

   >[!NOTE]
   >
   >Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het selectievakje moet `entity.id` of `entity.categoryId` doorgeven om de huidige aanbevelingen voor het item of de huidige categorie compatibel te maken. Over het algemeen is het beter alleen compatibele criteria te laten zien. Als u echter incompatibele criteria voor de activiteit wilt gebruiken, schakelt u het selectievakje **[!UICONTROL Compatible]** uit. De optie [!UICONTROL Compatible] wordt mogelijk niet weergegeven, afhankelijk van de instellingen voor Aanbevelingen ( **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]** > **[!UICONTROL Filter Incompatible Criteria]** ). Voor meer informatie, zie [&#x200B; Montages &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html){target=_blank}.

   ![&#x200B; Uitgezochte de dialoogdoos van Criteria &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_SelectCriteria2.png)

   Als u meerdere criteria selecteert, wordt het verkeer gelijkmatig over de geselecteerde criteria verdeeld. Als u bijvoorbeeld twee criteria hebt geselecteerd en uw activiteit is ontworpen om standaardinhoud weer te geven voor 20% van de deelnemers aan de activiteit, dan zal 40% van de deelnemers aan de activiteit de aanbevelingen zien die door elke criteria worden gecontroleerd. Er is geen optie om de percentages voor elke criteria te wijzigen.

   * Als u naar bestaande criteria wilt zoeken (bijvoorbeeld als een groot aantal kaarten met criteria wordt weergegeven), typt u in het zoekveld totdat de gewenste criteria worden weergegeven, selecteert u de criteria en klikt u op **[!UICONTROL Next]** .

     Sommige criteria worden geleverd bij [!DNL Recommendations] . U en uw team kunnen ook uw eigen aangepaste criteria maken.

   * Als u nieuwe criteria wilt maken, klikt u op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** en vult u de gegevens voor de nieuwe criteria in. Voor informatie over het creëren van nieuwe criteria, zie [&#x200B; Creërend Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md).
   * U kunt criteria ook in reeksen groeperen. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]** om een nieuwe reeks criteria te maken. Zie [&#x200B; de Opeenvolging van Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-criteria-sequence.md) voor meer informatie creëren.

1. Klik op **[!UICONTROL Next]**.
1. Selecteer a [&#x200B; ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/design-overview.md).

   Een ontwerp is een sjabloon die het uiterlijk van de locaties op de pagina bepaalt. [!DNL Target] bevat verschillende vooraf geconfigureerde ontwerpen. U kunt ook uw eigen aangepaste ontwerpen maken. Voor meer informatie, zie [&#x200B; een Ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) creëren en [&#x200B; Aanpassen van een Ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/customizing-a-template.md#concept_94F1554C3F2E4CDB9A2C3D78F10EDA59).

   ![&#x200B; Uitgezochte de dialoogdoos van het Ontwerp &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/Card_SelectDesign.png)

   Elk ontwerp toont een grafische voorstelling van hoe het eruit zal zien, en pictogrammen die tonen hoeveel van uw levende en inactieve activiteiten momenteel dat ontwerp gebruiken.

   * Als u een of meer bestaande ontwerpen wilt selecteren, klikt u op de ontwerpen en vervolgens op **[!UICONTROL Next]** .

     Als u meerdere criteria hebt geselecteerd, kunt u slechts één ontwerp selecteren.

   * Als u een aangepast ontwerp wilt maken, klikt u op **[!UICONTROL Create Design]** en vult u vervolgens de naam en de code voor het nieuwe ontwerp in. Klik op **[!UICONTROL Next]**, selecteer of upload een afbeelding en klik op **[!UICONTROL Done]** > **[!UICONTROL Done]** . Voor informatie over het creëren van een nieuw ontwerp, zie [&#x200B; een Ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14) creëren.

1. Klik op **[!UICONTROL Next]**.

   U kunt speciale acties toevoegen aan uw aanbevelingen. Voor meer informatie over het toevoegen van voor en achter bevorderingen, zie [&#x200B; Toevoegend Bevorderingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/adding-promotions.md#task_CC5BD28C364742218C1ACAF0D45E0E14).

1. Klik op **[!UICONTROL Save]**.

   In het VEC-scherm wordt het aanbevolen ontwerp op de pagina weergegeven.

1. (Optioneel) Klik op **[!UICONTROL Preview]** om te zien hoe de activiteit eruit zal zien voor bezoekers.

   In de modus [!UICONTROL Preview] kunt u op dezelfde manier werken met uw aanbevelingen als een bezoeker.

   Klik op **[!UICONTROL Compose]** als u klaar bent met het voorvertonen van uw aanbevelingen.

1. Herzie uw aanbeveling in VEC, dan klik **[!UICONTROL Next]**.

1. Controleer uw [!DNL Recommendations] activiteit in het stroomdiagram en breng de noodzakelijke veranderingen aan.

   ![&#x200B; de stroomdiagram van de Aanbevelingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/SCRN_Workflow.png)

   Het stroomdiagram leidt u door de stappen om het publiek voor de activiteit te kiezen, opstellingservaringen, en succesmetriek te specificeren.

   Vanuit het stroomdiagram kunt u het volgende doen:

   * Wijzig het publiek dat de aanbevelingen zal zien

     >[!NOTE]
     >
     >Naast het selecteren van een bestaand publiek, kunt u [&#x200B; tot een activiteit-slechts publiek &#x200B;](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483) leiden of [&#x200B; veelvoudige publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) combineren om ad hoc publiek eerder dan het creëren van een nieuw publiek tot stand te brengen.

     Standaard zien alle gebruikers de aanbevelingen. U kunt de aanbeveling echter richten op een specifiek publiek.

     Voor een [!DNL Recommendations] activiteit, ziet de controlegroep de pagina zonder enige aanbevelingen.

   * De criteria weergeven
   * De verzameling wijzigen (naast het label [!UICONTROL Criteria] )
   * Wijzig het percentage gegadigden dat de controleervaring ziet
   * De ontwerpcode weergeven
   * Een ontwerp wijzigen of verwijderen

1. Klik op **[!UICONTROL Next]** als u klaar bent.
1. Geef de activiteitinstellingen op.

   Typ bijvoorbeeld een naam (vereist) en een doelstelling (optioneel) voor de activiteit. Voor informatie over de montages, zie {de Montages van de Activiteit van 0} Aanbevelingen [.](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md#reference_3FDA8388CEEC4159949151C1829E2FBB)

   >[!NOTE]
   >
   >Als u een [!DNL Recommendation] naam van een activiteit opgeeft die al bestaat voor een andere activiteit in [!DNL Recommendations Classic] , wordt de nieuwe activiteit opnieuw gesynchroniseerd met een nieuwe naam. De nieuwe naam is de oorspronkelijke naam die met een tijdstempel is toegevoegd om deze uniek te maken. Deze nieuwe naam wordt zowel in [!DNL Target Standard/Premium] als in [!DNL Recommendations Classic] weergegeven.

1. Klik op **[!UICONTROL Save & Close]** als u klaar bent.

   Er wordt een overzicht van uw activiteiten weergegeven.

   Op de pagina [!UICONTROL Overview] kunt u:

   * De activiteit activeren
   * De activiteit bewerken
   * De activiteit delen met uw Experience Cloud-feed
   * QA de activiteit
   * Ervings-URL&#39;s weergeven
   * Gegevens downloaden
   * Wijzig het percentage deelnemers aan de activiteit die de controleervaring zien
   * Criteria-details tonen of verbergen
   * De code voor uw ontwerpen weergeven

1. (Optioneel) Open de pagina [!UICONTROL Reports] om het rapport weer te geven met de prestaties van uw [!DNL Recommendations] -activiteit.

1. (Facultatief) open de [!UICONTROL Collisions] pagina om het even welke [&#x200B; activiteitenbotsingen &#x200B;](/help/main/c-experiences/c-visual-experience-composer/activity-collisions.md) te bekijken die zouden kunnen voorkomen.

   Er treden conflicten op wanneer meerdere activiteiten zijn ingesteld om inhoud te leveren aan dezelfde pagina. Hierdoor kan onverwachte inhoud worden weergegeven.

## De Video van de opleiding: Creeer een activiteit van Aanbevelingen (7 :15) &lbrace;het badge van 1&rbrace; Zelfstudie ![](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/27688)
