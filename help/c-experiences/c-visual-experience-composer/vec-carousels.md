---
keywords: Visual Experience Composer;VEC;carrousel
description: Leer hoe u een carrousel maakt die kan worden bewerkt in de Adobe Target Visual Experience Composer (VEC).
title: Hoe maak ik carrousels in de Visual Experience Composer?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '148'
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