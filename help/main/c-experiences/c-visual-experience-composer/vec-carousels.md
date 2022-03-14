---
keywords: Visual Experience Composer;VEC;carrousel
description: Leer hoe u een carrousel maakt die in de Adobe kan worden bewerkt [!DNL Target] Visual Experience Composer (VEC).
title: Hoe maak ik carrousels in de Visual Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 50bc11d2-c9fc-4b53-8218-49842b59269a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Het creëren van Carrousels die in de Composer van de Visuele Ervaring werken

Dit onderwerp laat zien hoe u een carrousel maakt die in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC).

Wanneer u de onderstaande stappen gebruikt: [!DNL Target] weet altijd dat de geselecteerde dia &quot;selecteur&quot;voor de correcte dia zal hebben, zelfs als het in Composer van de Visuele Ervaring na een paar seconden wordt veranderd.

1. Maak statische plaatsaanduidingen voor HTML.

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
   >De [!UICONTROL Render Using JavaScript] optie wordt momenteel niet gesteund als het samen met douanecode in de Visuele Composer van de Ervaring wordt gebruikt.

1. Werk alleen classNames bij om andere namen te verbergen en de volgende met timer/animatie weer te geven.

   Werk de DOM-structuur nooit bij met JavaScript.
