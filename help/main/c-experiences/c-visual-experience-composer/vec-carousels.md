---
keywords: Visual Experience Composer;VEC;carrousel
description: Leer hoe te om een carrousel tot stand te brengen die in Adobe  [!DNL Target]  Visuele Composer van de Ervaring (VEC) kan worden uitgegeven.
title: Hoe maak ik carrousels in de Visual Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Carrousels maken die werken in de composer voor visuele ervaring

In dit onderwerp ziet u hoe u een carrousel maakt die u kunt bewerken in de map [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).

Wanneer u de onderstaande stappen gebruikt, weet [!DNL Target] altijd dat de geselecteerde dia de &#39;kiezer&#39; voor de juiste dia heeft, zelfs als deze na een paar seconden wordt gewijzigd in de Visual Experience Composer.

1. Maak statische plaatsaanduidingen voor HTML.

   ```html
   <ul>
   <li class="show"> slide 1 </li>
   <li class="hidden"> slide 2 </li>
   <li class="hidden"> slide 3 </li>
   </ul>
   ```

1. Voeg CSS toe om het uiterlijk te ontwerpen.

   Gebruik hiervoor JavaScript niet.

   >[!NOTE]
   >
   >De optie [!UICONTROL Render Using JavaScript] wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

1. Werk alleen classNames bij om andere namen te verbergen en de volgende met timer/animatie weer te geven.

   Werk de DOM-structuur nooit bij met JavaScript.
