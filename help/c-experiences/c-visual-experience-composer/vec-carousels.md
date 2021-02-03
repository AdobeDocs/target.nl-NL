---
keywords: Visual Experience Composer;VEC;carrousel
description: Dit onderwerp toont hoe te om een carrousel tot stand te brengen die in Adobe Target Visual Experience Composer (VEC) kan worden uitgegeven.
title: Carrousels maken die werken in de composer voor visuele ervaring
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Het creëren van Carrousels die in de Composer van de Visuele Ervaring werken

Dit onderwerp toont hoe te om een carrousel tot stand te brengen die in [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) kan worden uitgegeven.

Wanneer u de stappen hieronder gebruikt, [!DNL Target] weet altijd dat de geselecteerde dia &quot;selecteur&quot;voor de correcte dia zal hebben, zelfs als het in Visual Experience Composer na een paar seconden wordt veranderd.

1. Maak statische HTML-plaatsaanduidingen.

   ```html
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
   >De optie [!UICONTROL Render Using JavaScript] wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

1. Werk alleen classNames bij om andere namen te verbergen en de volgende met timer/animatie weer te geven.

   Werk de DOM-structuur nooit bij met JavaScript.