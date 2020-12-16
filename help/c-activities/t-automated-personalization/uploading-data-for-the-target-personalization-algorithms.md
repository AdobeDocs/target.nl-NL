---
description: Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen.
title: Gegevens uploaden voor de personalisatiealgoritmen van Target
feature: ap
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---


# Gegevens uploaden voor de Target personalization-algoritmen{#upload-data-for-target-s-personalization-algorithms}

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen.

Er zijn verschillende manieren om gegevens in te voeren in Automated Personalization (AP) en Auto-Target verpersoonlijkingsalgoritmen. Naast de methodes in [Methoden om Gegevens in Doel ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17) te krijgen, worden de Experience Cloud gedeelde publiek (Adobe Analytics, het Beheer van het Publiek) en het in-activiteit rapporteringspubliek ook gebruikt in onze algoritmen.

Zie [Automated Personalization Data Collection](/help/c-activities/t-automated-personalization/ap-data.md) voor informatie over de gegevens die automatisch worden verzameld en gebruikt door Automated Personalization- en Auto-Target-verpersoonlijkingsalgoritmen.

## Aanbevolen procedures {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In de volgende lijst vindt u de aanbevolen procedures voor het uploaden van gegevens voor de personalisatiealgoritmen van Target:

* Hoe hoger de gegevens van hoge kwaliteit die beschikbaar zijn voor de verpersoonlijkingsalgoritmen van Target, hoe beter de kwaliteit van de resulterende modellen in uw AP- en AutoTarget-activiteiten.
* Beperken met meerdere profielscripts of kenmerken die hetzelfde doel dienen.
* Geef geen unieke id door, zoals een sessie-id, als dat niet nodig is.
* Controleer welke gegevens Doel automatisch verzamelt ( [Gegevensverzameling voor de Verpersoonlijkingsalgoritmen van het Doel](/help/c-activities/t-automated-personalization/ap-data.md)) zodat u geen dubbele informatie verzendt. Bijvoorbeeld, gebruikt het Doel IP adressen om de codes van het ZIP van bezoekers te bepalen. Deze informatie hoeft niet als een afzonderlijke variabele te worden doorgegeven.
* Meerdere waarden in hetzelfde kenmerk/dezelfde variabele niet doorgeven. Als er meerdere variabelen zijn samengevoegd, behandelen de personalisatiealgoritmen van Target elke tekenreeks als een unieke waarde, waardoor de waarde van de informatie voor personalisatie wordt verminderd.
* Gebruik een gedenkwaardige en zinvolle naamgevingsconventie om uw [Persoonlijke inzichten > Rapporten](/help/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) begrijpelijker te maken.

