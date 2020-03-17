---
description: Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen.
title: Gegevens uploaden voor de personalisatiealgoritmen van Target
uuid: eb0938b9-7f35-4bb5-ac4b-260b2144db5b
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Gegevens uploaden voor de Target personalization-algoritmen{#upload-data-for-target-s-personalization-algorithms}

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen.

Er zijn verscheidene manieren om gegevens in Geautomatiseerde Persoonlijke (AP) en auto-Doel verpersoonlijkingsalgoritmen in te voeren. Naast de methoden in [Methoden om gegevens in Doel](../../c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md#concept_0069C0EFB56C4700BB33F2F35C2B9B17)te krijgen, worden ook de gedeelde benaderingen van Experience Cloud (Adobe Analytics, Audience Management) en de rapporteringsdoelgroepen in de praktijk gebruikt in onze algoritmen.

Voor informatie over de gegevens die automatisch door Geautomatiseerde Persoonlijke en Auto-Doel verpersoonlijkingsalgoritmen worden verzameld en worden gebruikt, zie de [Geautomatiseerde Gegevensverzameling](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)van de Aanpassing van de Aanpassing.

## Aanbevolen werkwijzen {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In de volgende lijst vindt u de aanbevolen procedures voor het uploaden van gegevens voor de personalisatiealgoritmen van Target:

* Hoe hoger de gegevens van hoge kwaliteit die beschikbaar zijn voor de verpersoonlijkingsalgoritmen van Target, hoe beter de kwaliteit van de resulterende modellen in uw AP- en AutoTarget-activiteiten.
* Beperken met meerdere profielscripts of kenmerken die hetzelfde doel dienen.
* Geef geen unieke id door, zoals een sessie-id, als dat niet nodig is.
* Controleren welke gegevens door Doel automatisch worden verzameld ( [gegevensverzameling voor de Persoonlijke Algoritmen](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058)van het Doel), zodat u geen dubbele informatie verzendt. Bijvoorbeeld, gebruikt het Doel IP adressen om de codes van het ZIP van bezoekers te bepalen. Deze informatie hoeft niet als een afzonderlijke variabele te worden doorgegeven.
* Meerdere waarden in hetzelfde kenmerk/dezelfde variabele niet doorgeven. Als er meerdere variabelen zijn samengevoegd, behandelen de personalisatiealgoritmen van Target elke tekenreeks als een unieke waarde, waardoor de waarde van de informatie voor personalisatie wordt verminderd.
* Gebruik een gedenkwaardige en zinvolle naamgevingsconventie om uw rapporten over [persoonlijke voorkeuren](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) begrijpelijker te maken.

