---
keywords: criteria sequence;multiple criteria;algorithms;criteria;recommendations criteria
description: Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw activiteiten met aanbevelingen worden weergegeven.
title: Criteria-reeksen maken
uuid: 9a5ca86b-fc79-4c24-b86f-e333b0c63088
translation-type: tm+mt
source-git-commit: 0ba817898366e9d18fec6cc0fc75013c78a136e9

---


# ![PREMIUM](/help/assets/premium.png) : Criteria maken{#create-criteria-sequences}

Gebruik reeksen van maximaal vijf criteria om meer controle uit te oefenen over de items die in uw activiteiten met aanbevelingen worden weergegeven.

>[!NOTE]
>
>Criteria sequences kunnen niet worden gebruikt met [!UICONTROL Aanbevelingen] activiteiten die vóór de release van oktober 2016 zijn gemaakt [!DNL Target Premium].

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

Er zijn meerdere manieren om het scherm [!UICONTROL Criteria Sequence] maken te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Wanneer u een [!UICONTROL activiteit van Aanbevelingen] creeert, klik **[!UICONTROL Create Nieuw]** > **[!UICONTROL creeer de Opeenvolging]** van Criteria op het [!UICONTROL Uitgezochte scherm] . U kunt de nieuwe reeks criteria opslaan voor gebruik met andere activiteiten voor [!UICONTROL Aanbevelingen] .
* Wanneer u een activiteit van [!UICONTROL Aanbevelingen] uitgeeft, klik in een vakje van de Plaats [!UICONTROL van] Aanbevelingen op uw pagina, en selecteer de Criteria **[!UICONTROL van de]** Verandering. Klik in het scherm [!UICONTROL Criteria] selecteren op **[!UICONTROL Nieuw]** maken > **[!UICONTROL Criteria-reeks]** maken. U kunt uw nieuwe criteria opslaan voor gebruik met andere [!UICONTROL activiteiten voor Aanbevelingen] .
* Klik in het scherm **[!UICONTROL Aanbevelingen]** > **[!UICONTROL Criteria]** bibliotheek op **[!UICONTROL Criteria]** maken > **[!UICONTROL Criteria-reeks]** maken. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL activiteiten met aanbevelingen] .

1. Klik op **[!UICONTROL Criteria]** maken of **[!UICONTROL Nieuw]** maken.

   ![Nieuwe criteria maken](/help/c-recommendations/c-algorithms/assets/button_CreateCriteria_new.png)

1. Selecteer **[!UICONTROL Criteria-reeks]** maken.

   ![](assets/CreateCriteriaSequence.png)

1. Typ een **[!UICONTROL naam]** voor de reeks.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de opeenvolging van criteria te beschrijven. Bezoekers van uw site krijgen deze naam niet te zien.
1. Typ een openbare-onder ogen ziet Titel **[!UICONTROL van de]** Algemene Vertoning om op de pagina te verschijnen als de veelvoudige criteria in de opeenvolging worden gebruikt om het ontwerp van [!UICONTROL Aanbevelingen] te vullen.

   U wilt bijvoorbeeld &quot;Klanten die dit ook hebben bekeken&quot; vervangen. met &quot;Aanbevolen voor u&quot; als het ontwerp items kan bevatten die zijn gebaseerd op meerdere [!UICONTROL Aanbevelingen] .
1. Typ een korte **[!UICONTROL beschrijving]** van de reeks criteria.

   De beschrijving zou u moeten helpen de opeenvolging van criteria identificeren, en zou informatie over zijn doel kunnen omvatten.
1. Selecteer een **[!UICONTROL industrie verticaal]**.

   De standaardverticale weergave in de branche wordt automatisch weergegeven.
1. Selecteer een **[!UICONTROL paginatype]**.

   U kunt meerdere paginatypen selecteren.

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde opeenvolging van criteria te categoriseren, die het gemakkelijker maken om opeenvolgingen voor andere activiteiten van [!UICONTROL Aanbevelingen] opnieuw te gebruiken.
1. Stel de regels voor de **[!UICONTROL inhoud]** in.

   Wanneer u een reeks criteria maakt, worden back-upaanbevelingen en renderinstellingen voor gedeeltelijk ontwerp genegeerd voor de afzonderlijke criteria waaruit de reeks bestaat. Als u back-upaanbevelingen en gedeeltelijke ontwerprendering wilt gebruiken, moet u deze voor de reeks inschakelen. Selecteer de juiste gereedschappen. Als u ervoor kiest om back-upaanbevelingen toe te staan, kunt u ook kiezen of u inclusieregels wilt toepassen op de back-ups.
1. Stel de volgorde van de volgreeksen in.

1. Klik op **[!UICONTROL Criteria]** toevoegen.
1. Selecteer een criterium in het scherm Criteria toevoegen.
1. Klik op **[!UICONTROL Toevoegen]**.

   U kunt maximaal vijf criteria toevoegen aan een reeks.
1. Klik op **[!UICONTROL Opslaan]**.

   De opeenvolging van criteria zal in de lijst van Criteria verschijnen.

   ![](assets/CriteriaSequenceCard.png)

   Zie [Criteria](../../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750)voor meer informatie over de opties van de aanbevolen logica.

## Trainingsvideo: Criteria maken in ![zelfstudie voor aanbevelingen (12:33)](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
