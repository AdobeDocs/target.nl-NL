---
keywords: inclusion rules;inclusion criteria;recommendations;promotion;promotions;dynamic filtering;static;static filter
description: Voer handmatig een of meer statische waarden in om te filteren met behulp van insluitingsregels in Adobe Target Recommendations.
title: Filteren op statische waarden in inclusieregels in Adobe Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: b51c980d8e7db3ee574350a04f9056fe5b00a703
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# ![Statisch PREMIUM](/help/assets/premium.png) -filter

Voer handmatig een of meer statische waarden in om te filteren met behulp van insluitingsregels in Adobe Target Recommendations.

U kunt bijvoorbeeld alleen inhoud met een MPAA-score van &quot;G&quot; of &quot;PG&quot; aanbevelen.

Beschikbare operatoren:

* equals
* is niet gelijk aan
* contains
* bevat niet
* begint met
* eindigt met
* waarde is aanwezig
* waarde is niet aanwezig
* is groter dan of gelijk aan
* is kleiner dan of gelijk aan

>[!NOTE]
>
>Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen (&quot;overeenkomsten&quot; zijn nu &quot;gelijk&quot;), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig.

U kunt zo veel inclusieregels tot stand brengen zoals nodig. De inclusieregels worden verbonden met een exploitant AND. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.