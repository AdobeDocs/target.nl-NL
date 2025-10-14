---
keywords: Automated Personalization;ap;upload gegevens;offline gegevens;personalisatiealgoritme;auto target;autoTarget;best practices
description: Leer hoe te om off-line gegevens te uploaden wanneer het bouwen van verpersoonlijkingsmodellen in  [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] activiteiten.
title: Hoe kan ik gegevens uploaden voor Personalization-algoritmen?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Gegevens uploaden voor de [!DNL Target] verpersoonlijkingsalgoritmen

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescore, kunnen ongelooflijk waardevol zijn bij het maken van personalisatiemodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] -activiteiten.

Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] personalisatiealgoritmen. Naast de methodes in [&#x200B; Methoden om Gegevens in Doel &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html?lang=nl-NL){target=_blank} te krijgen, [!DNL Experience Cloud] wordt het gedeelde publiek ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]), en het in-activiteit rapporterend publiek ook gebruikt in [!DNL Target] algoritmen.

Voor informatie over de gegevens die automatisch door [!UICONTROL Automated Personalization] worden verzameld en worden gebruikt en [!UICONTROL Auto-Target] verpersoonlijkingsalgoritmen, zie [&#x200B; de Inzameling van Gegevens van Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Aanbevolen procedures {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

In de volgende lijst vindt u de aanbevolen procedures voor het uploaden van gegevens voor [!DNL Target] personalisatiealgoritmen:

* Hoe hoger de kwaliteit van de gegevens die beschikbaar zijn voor [!DNL Target] verpersoonlijkingsalgoritmen, hoe beter de kwaliteit van de resulterende modellen in uw [!UICONTROL Automated Personalization] - en [!UICONTROL Auto-Target] -activiteiten.
* Beperken met meerdere profielscripts of kenmerken die hetzelfde doel dienen.
* Geef geen unieke id door, zoals een sessie-id als dat niet nodig is.
* Herzie welke gegevens [!DNL Target] automatisch verzamelt ( [&#x200B; de Inzameling van Gegevens voor de Algoritmen van Personalization van het Doel &#x200B;](/help/main/c-activities/t-automated-personalization/ap-data.md)) zodat u geen dubbele informatie verzendt. [!DNL Target] gebruikt bijvoorbeeld IP-adressen om ZIP-codes van bezoekers te bepalen. Deze informatie hoeft niet als een afzonderlijke variabele te worden doorgegeven.
* Meerdere waarden in hetzelfde kenmerk of dezelfde variabele niet doorgeven. Wanneer meerdere variabelen worden samengevoegd, behandelen [!DNL Target] verpersoonlijkingsalgoritmen elke tekenreeks als een unieke waarde, waardoor de waarde van de informatie voor verpersoonlijking afneemt.
* Gebruik een memorabele en zinvolle noemende overeenkomst om uw [&#x200B; Rapporten van de Inzichten van Personalization &#x200B;](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) begrijpelijker te maken.
