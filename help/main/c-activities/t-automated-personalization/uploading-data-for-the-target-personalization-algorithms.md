---
keywords: Automated Personalization;ap;upload gegevens;offline gegevens;personalisatiealgoritme;auto target;autoTarget;best practices
description: Leer hoe u offline gegevens kunt uploaden tijdens het samenstellen van verpersoonlijkingsmodellen in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] activiteiten.
title: Hoe kan ik gegevens voor de algoritmen van de Personalisatie uploaden?
feature: Automated Personalization, Auto-Target
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
exl-id: c750e0e5-8ebd-49a2-9705-05f593aaf0b9
source-git-commit: 3f64da1c9a1146e4d2d9389d6d5ce764764d2d9c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Gegevens uploaden voor de [!DNL Target] verpersoonlijkingsalgoritmen

Offlinegegevens, zoals CRM-informatie of klantchurn-concentratiescores, kunnen ongelooflijk waardevol zijn wanneer u modellen voor personalisatie ontwikkelt in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] activiteiten.

Er zijn verschillende manieren om gegevens in te voeren in [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] personalisatiealgoritmen. Naast de methoden in [Methoden om gegevens op te halen in doel](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}, [!DNL Experience Cloud] gedeeld publiek ([!UICONTROL Adobe Analytics], [!DNL Audience Manager]), en het publiek dat actief rapporteert, wordt ook gebruikt in [!DNL Target] algoritmen.

Voor informatie over automatisch verzamelde en gebruikte gegevens door [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] verpersoonlijkingsalgoritmen, zie [Automated Personalization-gegevensverzameling](/help/main/c-activities/t-automated-personalization/ap-data.md).

## Aanbevolen procedures {#section_DE96C7B7D114491DBB67FB5B7DA3D37B}

De volgende lijst bevat de aanbevolen procedures voor het uploaden van gegevens voor [!DNL Target] verpersoonlijkingsalgoritmen:

* De gegevens van hogere kwaliteit die beschikbaar zijn voor [!DNL Target] verpersoonlijkingsalgoritmen, hoe beter de kwaliteit de resulterende modellen in uw [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] activiteiten.
* Beperken met meerdere profielscripts of kenmerken die hetzelfde doel dienen.
* Geef geen unieke id door, zoals een sessie-id als dat niet nodig is.
* Controleren welke gegevens [!DNL Target] automatisch verzamelt ( [Gegevensverzameling voor persoonlijke algoritmen van het doel](/help/main/c-activities/t-automated-personalization/ap-data.md)), zodat u geen dubbele informatie verzendt. Bijvoorbeeld: [!DNL Target] gebruikt IP adressen om de codes van het ZIP van bezoekers te bepalen. Deze informatie hoeft niet als een afzonderlijke variabele te worden doorgegeven.
* Meerdere waarden in hetzelfde kenmerk of dezelfde variabele niet doorgeven. Wanneer meerdere variabelen worden samengevoegd, [!DNL Target] personaliseringsalgoritmen behandelen elk koord als unieke waarde, die de waarde van de informatie voor verpersoonlijking vermindert.
* Gebruik een gedenkwaardige en betekenisvolle naamgevingsconventie om uw [Persoonlijkheidsrapporten](/help/main/c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767) begrijpelijker.
