---
keywords: inclusieregels;inclusiecriteria;aanbevelingen;bevordering;bevordering;dynamische filtratie;statisch;statische filter
description: Leer hoe te om één of meerdere statische waarden manueel in te gaan om inclusieregels in Adobe  [!DNL Target]  Recommendations te gebruiken.
title: Hoe filtert ik op statische waarden in Recommendations-activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: b6a55260fd49e07e2b217f6becfbc778251a5d0d
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# [!UICONTROL Static Filter]

Voer handmatig een of meer statische waarden in om te filteren met behulp van insluitingsregels in [!DNL Adobe Target Recommendations] .

U kunt bijvoorbeeld alleen inhoud aanbevelen met de MPA-score (Motion Picture Association) van &quot;G&quot; of &quot;PG&quot;.

U kunt zo veel inclusieregels tot stand brengen zoals nodig. De inclusieregels worden verbonden met een exploitant AND. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

>[!NOTE]
>
>Als u vertrouwd met bent hoe de inclusieregels voorafgaand aan Doel 17.6.1 versie (Juni 2017) werden gevormd, zult u merken dat sommige opties en exploitanten zijn veranderd. Alleen de operatoren die van toepassing zijn op de geselecteerde optieweergave en sommige operatoren hebben een andere naam gekregen (&quot;overeenkomsten&quot; zijn nu &quot;gelijk&quot;), zodat ze consistenter en intuïtiever zijn. Alle bestaande uitsluitingsregels die vóór deze release zijn gemaakt, zijn automatisch naar de nieuwe structuur gemigreerd. Van uw kant is geen herstructurering nodig.

## Aanbevolen inhoud met G of PG

Om een inclusieregel met statische waarden tot stand te brengen om inhoud met een classificatie MPA van &quot;G&quot;of &quot;PG&quot;slechts (exclusief &quot;R&quot;en &quot;NC17&quot;inhoud) aan te bevelen, kon u de volgende het filtreren regels &quot;film-rating evenaart om het even welk van g-geschat&quot;en &quot;film-classificatie evenaart om het even welk van pg-geschat&quot;tot stand brengen.
