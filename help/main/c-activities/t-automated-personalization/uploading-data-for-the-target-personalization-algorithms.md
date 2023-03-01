---
keywords: Automated Personalization;ap;upload gegevens;offline gegevens;personalisatiealgoritme;auto target;autoTarget;best practices
description: Leer hoe te om off-line gegevens, zoals de informatie van CRM te uploaden wanneer het bouwen van verpersoonlijkingsmodellen in Adobe [!DNL Target] Automated Personalization (AP)-activiteiten.
title: Hoe kan ik gegevens voor de algoritmen van de Personalisatie uploaden?
feature: Automated Personalization
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3ac61272ee1ccd72a8670966f181e7798cbe9f76
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Gegevens uploaden voor de [!DNL Target] verpersoonlijkingsalgoritmen

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescores, kunnen ongelooflijk waardevol zijn wanneer u modellen voor personalisatie ontwikkelt in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) activiteiten.

Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] personalisatiealgoritmen. Naast de methoden in [Methoden om gegevens op te halen in doel](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/){target=_blank}, Experience Cloud shared audiences (Adobe Analytics, Audience Management){target=_blank} en rapporteringspubliek in de activiteit wordt ook gebruikt in onze algoritmen.

Voor informatie over de gegevens die automatisch worden verzameld en gebruikt door Automated Personalization en Auto-Target verpersoonlijkingsalgoritmen, zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Aanbevolen werkwijzen {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In de volgende lijst vindt u de aanbevolen procedures voor het uploaden van gegevens voor de personalisatiealgoritmen van Target:

* Hoe hoger de gegevens van hoge kwaliteit die beschikbaar zijn voor de verpersoonlijkingsalgoritmen van Target, hoe beter de kwaliteit van de resulterende modellen in uw AP- en AutoTarget-activiteiten.
* Beperken met meerdere profielscripts of kenmerken die hetzelfde doel dienen.
* Geef geen unieke id door, zoals een sessie-id, als dat niet nodig is.
* Controleren welke gegevens Doel automatisch verzamelt ( [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md)), zodat u geen dubbele gegevens verzendt. Bijvoorbeeld, gebruikt het Doel IP adressen om de codes van het ZIP van bezoekers te bepalen. Deze informatie hoeft niet als een afzonderlijke variabele te worden doorgegeven.
* Meerdere waarden in hetzelfde kenmerk/dezelfde variabele niet doorgeven. Als er meerdere variabelen zijn samengevoegd, behandelen de personalisatiealgoritmen van Target elke tekenreeks als een unieke waarde, waardoor de waarde van de informatie voor personalisatie wordt verminderd.
* Gebruik een gedenkwaardige en betekenisvolle naamgevingsconventie om uw [Persoonlijkheidsrapporten](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) begrijpelijker.
