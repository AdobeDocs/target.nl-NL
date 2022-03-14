---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;bevordering;bevordering;dynamische filtratie;statisch;statische filter
description: Leer hoe u handmatig een of meer statische waarden invoert om te filteren met behulp van insluitingsregels in Adobe [!DNL Target] Recommendations.
title: Hoe filtert ik op statische waarden in Recommendations-activiteiten?
feature: Recommendations
exl-id: 217e19bf-521f-4913-9b41-099c9af8b393
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Statisch filter

Voer handmatig een of meer statische waarden in om te filteren met behulp van insluitingsregels in [!DNL Adobe Target] [!DNL Recommendations].

U kunt bijvoorbeeld alleen inhoud aanbevelen met de MPA-score (Motion Picture Association) van &quot;G&quot; of &quot;PG&quot;.

U kunt zo veel inclusieregels tot stand brengen zoals nodig. De inclusieregels worden verbonden met een exploitant AND. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

>[!NOTE]
>
>Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen (&quot;overeenkomsten&quot; zijn nu &quot;gelijk&quot;), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig.

## Aanbevolen inhoud met G of PG

Om een inclusieregel met statische waarden tot stand te brengen om inhoud met een classificatie MPA van &quot;G&quot;of &quot;PG&quot;slechts (exclusief &quot;R&quot;en &quot;NC17&quot;inhoud) aan te bevelen, kon u de volgende het filtreren regels &quot;film-rating evenaart g-rating&quot;en &quot;film-rating gelijk pg-schatten&quot;, zoals hieronder getoond.

![voorbeeld voor filmbeoordeling](/help/main/c-recommendations/c-algorithms/assets/movies.png)
