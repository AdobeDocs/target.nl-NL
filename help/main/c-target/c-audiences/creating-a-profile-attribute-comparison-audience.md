---
keywords: publiek;prioriteit;profielkenmerk;vergelijken;vergelijken;publiek maken;publiek maken;publiek maken
description: Leer hoe u een publiek definieert om twee profielkenmerken te vergelijken.
title: Kan ik twee profielkenmerken vergelijken voor gebruik bij het publiek?
feature: Audiences
exl-id: 033e90f1-5a05-4fce-a520-68826860a908
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Een vergelijkingspubliek voor profielkenmerken maken

Een publiek definiëren in [!DNL Adobe Target] twee profielkenmerken voor uw [Auditiebibliotheek](/help/main/c-target/c-audiences/audiences.md) of in een [alleen voor activiteiten](/help/main/c-target/creating-activity-only-audience.md). Met operatoren, zoals groter dan, kleiner dan of gelijk aan, definieert u een publiek om de waarden van twee verschillende profielkenmerken dynamisch te vergelijken.

>[!NOTE]
>
>Deze functionaliteit is beschikbaar voor de [[!UICONTROL Visitor Profile]](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E) alleen categorie.

## Overzicht {#section_303CBC78194D49A2A004945D425441E1}

Het publiek wordt gedefinieerd door regels die bepalen wie van een [!DNL Target] activiteit. Een publieksdefinitie kan veelvoudige regels omvatten, en elke regel kan veelvoudige parameters omvatten. Als één van de regels u omvat gebruikt [!UICONTROL Visitor Profile] categorie, kunt u een regel definiëren die is gebaseerd op de specifieke waarde van een kenmerk van een bezoekersprofiel of de waarde van dat kenmerk vergelijken met een ander kenmerk van het bezoekersprofiel.

Stel bijvoorbeeld dat u voor een meubelbedrijf werkt en twee scores voor klantvriendelijkheid in [!DNL Target]:

* Mogelijkheid om in de komende 90 dagen dinerruimmeubilair te kopen
* Mogelijkheid om in de komende 90 dagen huiskamermeubilair te kopen

Je zou een publiek kunnen maken dat gedefinieerd wordt als de neiging om eetkamermeubilair te kopen groter is dan de neiging om meubilair van woonkamertjes te kopen. [!DNL Target] Vervolgens worden de scores voor de eetruimte en de neiging tot woonkamer dynamisch met elkaar vergeleken om te bepalen of de bezoeker voor dit publiek in aanmerking komt.

Zie voor meer informatie [Methoden om gegevens op te halen in doel](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/).

## Een vergelijkingspubliek voor profielkenmerken maken {#section_7A62FD47D5C74C3EBC3417ACDBB85013}

1. Klik op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Slepen en neerzetten **[!UICONTROL Visitor Profile]** in het deelvenster voor publieksopbouw.
1. Van de **[!UICONTROL Visitor Profile]** kiest u een kenmerk in de vervolgkeuzelijst:

   ![Propensatiescore 1](assets/propensity_score_1.png)

1. Kies uw evaluator:

   ![Propensatiescore 2](assets/propensity_score_2.png)

1. Van de **[!UICONTROL Choose Comparison Type]** vervolgkeuzelijst kiest u **[!UICONTROL Attribute]**.

   Met het vergelijkingstype &quot;statische waarde&quot; kunt u het kenmerk &quot;profiel van de bezoeker&quot; vergelijken met specifieke waarden.

   ![Propensatiescore 3](assets/propensity_score_3.png)

   >[!NOTE]
   >
   >Als u een van de standaardcategorieën voor bezoekersprofielen gebruikt (bijvoorbeeld Nieuwe bezoeker of Bezoeker terugsturen), kunt u alleen de optie voor statische waarden kiezen. De opties voor dynamische vergelijking zijn niet beschikbaar voor standaardcategorieën. Andere voorbeelden waarbij de dynamische vergelijkingsopties niet beschikbaar zijn, zijn &quot;Eerste pagina van sessie&quot;, &quot;Niet in andere tests&quot;, &quot;Niet eerste pagina van sessie&quot; en &quot;Categorie-affiniteit&quot;.

1. Kies het extra kenmerk dat u met het oorspronkelijke kenmerk wilt vergelijken.

   ![](assets/propensity_score_4.png)

1. Klik op **[!UICONTROL Done]**.

## Video over training ![Overzicht badge](/help/main/assets/overview.png) {#section_3BB8DBF3418F4520B3E274B6F40AF8F3}

Bekijk de volgende video voor meer informatie en een scenario waarin u deze functie kunt gebruiken:

>[!VIDEO](https://video.tv.adobe.com/v/23218/)
