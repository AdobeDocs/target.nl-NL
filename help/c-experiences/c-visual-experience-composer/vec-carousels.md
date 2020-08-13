---
keywords: Visual Experience Composer;VEC;carousel
description: Dit onderwerp toont hoe te om een carrousel tot stand te brengen die in Visual Experience Composer (VEC) kan worden uitgegeven.
title: Het creëren van Carrousels die in de Composer van de Visuele Ervaring werken
feature: vec
subtopic: Multivariate Test
topic: Standard
uuid: 19538f6e-445c-49ca-9f0d-b49fc330b721
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Het creëren van Carrousels die in de Composer van de Visuele Ervaring werken{#creating-carousels-that-work-in-the-visual-experience-composer}

Dit onderwerp toont hoe te om een carrousel tot stand te brengen die in Visual Experience Composer (VEC) kan worden uitgegeven.

Wanneer u de stappen hieronder gebruikt, weet [!DNL Target] altijd dat de geselecteerde dia &quot;selecteur&quot;voor de correcte dia zal hebben, zelfs als het in Visual Experience Composer na een paar seconden wordt veranderd.

1. Maak statische HTML-plaatsaanduidingen.

   ```
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Voeg CSS toe om het uiterlijk te ontwerpen.

   Gebruik hiervoor geen JavaScript.

   >[!NOTE]
   >
   >De [!UICONTROL Render Using JavaScript] optie wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

1. Werk alleen classNames bij om andere namen te verbergen en de volgende met timer/animatie weer te geven.

   Werk de DOM-structuur nooit bij met JavaScript.