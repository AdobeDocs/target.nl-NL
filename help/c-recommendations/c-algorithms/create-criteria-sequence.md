---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria
description: Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw Recommendations-activiteiten worden weergegeven.
title: Criteria-reeksen maken
feature: criteria
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) : Criteria maken{#create-criteria-sequences}

Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw Recommendations-activiteiten worden weergegeven.

>[!NOTE]
>
>Criteria sequenties kunnen niet worden gebruikt met [!UICONTROL Recommendations] activiteiten die vóór de release van oktober 2016 zijn gecreëerd [!DNL Target Premium].

Als u een reeks criteria wilt maken, moet u eerst de criteria maken die u in de reeks wilt opnemen. Zie [Criteria](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_8A9CB465F28D44899F69F38AD27352FE) maken voor meer informatie.

Door een criteria opeenvolging te gebruiken, kunt u extra gerichte aanbevelingen verstrekken, in plaats van het gebruiken van generischere reserveaanbevelingen, wanneer een criteria niet genoeg resultaten terugkeren om uw ontwerp te vullen. Doorgaans wordt een reeks criteria uitgevoerd van een meer specifieke doelverwijzing, die mogelijk minder resultaten oplevert, naar een meer algemene doelgerichtheid, die meestal meer resultaten oplevert.

Een reeks criteria voor productpagina&#39;s kan bijvoorbeeld deze volgorde volgen:

1. Gebaseerd op huidig item, van hetzelfde merk
1. Gebaseerd op huidige item, van alle merken
1. Gebaseerd op gelijkenis van inhoud
1. Gebaseerd op topverkopers
1. Gebaseerd op de meeste weergegeven items op de hele site

Deze volgorde kan worden gevolgd door een reeks criteria voor de homepage:

1. Gebaseerd op laatste aankoop van bezoeker
1. Gebaseerd op het favoriete object van de bezoeker
1. Gebaseerd op de favoriete rubriek van de bezoeker
1. Gebaseerd op topverkopers
1. Gebaseerd op de meest bekeken website

Er zijn meerdere manieren om het [!UICONTROL Create Criteria Sequence] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Wanneer u een [!UICONTROL Recommendations] activiteit creeert, klik **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]** op het [!UICONTROL Select Criteria] scherm. U kunt de nieuwe reeks criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Als u een [!UICONTROL Recommendations] activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] vak op de pagina en selecteert u **[!UICONTROL Change Criteria]**. Klik in het [!UICONTROL Select Criteria] scherm op **[!UICONTROL Create New]** > **[!UICONTROL Create Criteria Sequence]**. U kunt de nieuwe criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria Sequence]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations] activiteiten.

1. Klik **[!UICONTROL Create Criteria]** of **[!UICONTROL Create New]**.

   ![Nieuwe criteria maken](/help/c-recommendations/c-algorithms/assets/button_CreateCriteria_new.png)

1. Selecteer **[!UICONTROL Create Criteria Sequence]**.

   ![](assets/CreateCriteriaSequence.png)

1. Typ een **[!UICONTROL Name]** voor de reeks.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de opeenvolging van criteria te beschrijven. Bezoekers van uw site krijgen deze naam niet te zien.
1. Typ een openbare-onder ogen ziet **[!UICONTROL Generic Display Title]** om op de pagina te verschijnen als de veelvoudige criteria in de opeenvolging worden gebruikt om het [!UICONTROL Recommendations] ontwerp te vullen.

   U wilt bijvoorbeeld &quot;Klanten die dit ook hebben bekeken&quot; vervangen. met &quot;Aanbevolen voor u&quot; als het ontwerp items kan bevatten die op meer dan één [!UICONTROL Recommendations] toets zijn gebaseerd.
1. Typ een korte reeks criteria. **[!UICONTROL Description]**

   De beschrijving zou u moeten helpen de opeenvolging van criteria identificeren, en zou informatie over zijn doel kunnen omvatten.
1. Selecteer een **[!UICONTROL Industry Vertical]**.

   De standaardverticale weergave in de branche wordt automatisch weergegeven.
1. Selecteer een **[!UICONTROL Page Type]**.

   U kunt meerdere paginatypen selecteren.

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde opeenvolging van criteria te categoriseren, die het gemakkelijker maken om opeenvolgingen voor andere [!UICONTROL Recommendations] activiteiten opnieuw te gebruiken.
1. Stel uw **[!UICONTROL Content]** regels in.

   Wanneer u een reeks criteria maakt, worden back-upaanbevelingen en renderinstellingen voor gedeeltelijk ontwerp genegeerd voor de afzonderlijke criteria waaruit de reeks bestaat. Als u back-upaanbevelingen en gedeeltelijke ontwerprendering wilt gebruiken, moet u deze voor de reeks inschakelen. Selecteer de juiste gereedschappen. Als u ervoor kiest om back-upaanbevelingen toe te staan, kunt u ook kiezen of u inclusieregels wilt toepassen op de back-ups.
1. Stel de volgorde van de volgreeksen in.

1. Klik op **[!UICONTROL Add Criteria]**.
1. Selecteer een criterium in het scherm Criteria toevoegen.
1. Klik op **[!UICONTROL Add]**.

   U kunt maximaal vijf criteria toevoegen aan een reeks.
1. Klik op **[!UICONTROL Save]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   ![](assets/CriteriaSequenceCard.png)

   Zie [Criteria](../../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750)voor meer informatie over de opties van de aanbevolen logica.

## Trainingsvideo: Criteria maken in Recommendations (12:33) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
