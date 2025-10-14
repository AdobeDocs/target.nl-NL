---
keywords: Doel;rapporten;rapport instellingen;extreme orden;extreme waarden
description: Leer hoe te om extreme waarden uit te sluiten van het beïnvloeden van rapporten in Adobe  [!DNL Target]  zodat beïnvloeden een paar ongebruikelijke orden uw activiteitenresultaten niet.
title: Hoe sluit ik extreme waarden uit in rapporten?
feature: Reports
exl-id: fd2d0c18-62c0-41e0-800c-b2ae123f0e74
source-git-commit: c1a71d1fb6fa9b5c14e22fa3199358a4594bb4a1
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Extreme waarden uitsluiten

U kunt extreme waarden uitsluiten van het beïnvloeden van rapporten in [!DNL Adobe Target] zodat beïnvloeden een paar ongebruikelijke orden niet uw activiteitenresultaten. Een voorbeeld van een ongebruikelijke bestelling zou een coach kunnen zijn die uniformen koopt voor een heel team in plaats van individuele kopers die individuele uniformen kopen.

>[!NOTE]
>
>De markering [!UICONTROL Exclude Extreme Values] is alleen van toepassing op activiteiten met metrische typen [!UICONTROL Revenue] en [!UICONTROL Engagement] .

Extreme waarden worden automatisch gemarkeerd op basis van de onderstaande regels. U kunt schakelen tussen het zien van en het uitsluiten van de extreme waarden van uw rapporten. De extreme waarden van een activiteit worden uitgesloten nadat de activiteit gedurende een uur of na 15 orders is uitgevoerd, afhankelijk van welke het eerst komt.

Een waarde wordt als extreem beschouwd als deze meer dan +/- 3 standaardafwijkingen van de gemiddelde orderwaarde is op basis van de laatste maand van gegevens (tot het tijdstip waarop de berekening is gemaakt).

Het filter voor extreme waarden is bijvoorbeeld vaak handig bij het gebruik van RPV. RPV combineert de omrekeningskoers en de gemiddelde orderwaarde, en stelt vaak de volatiliteit van die cijfers bloot. Als u RPV gebruikt en bepaalt dat orders niet normaal verdeeld lijken te zijn, ziet u wellicht meer normale resultaten als u het filter voor extreme volgorde toepast.

Wanneer een waarde als extreem wordt gemarkeerd, wordt de waarde van de volgorde vervangen door de gemiddelde waarde van de ervaring voor de laatste maand, exclusief de uiterste waarden. De volgorde wordt ook als extreem gemarkeerd in het [!UICONTROL Order Details] -rapport en in de CSV-download voor dagelijkse resultaten.

**om extreme waarden van uw rapporten uit te sluiten:**

1. Open een activiteit die [!UICONTROL Revenue] of [!UICONTROL Engagement] metrische types omvat, dan klik de **[!UICONTROL Reports]** tabel.
1. Klik het pictogram van de Montages van het Rapport ( ![&#x200B; pictogram van de Montages van het Rapport &#x200B;](/help/main/assets/icons/Setting.svg) ) om het **[!UICONTROL Settings]** dialoogvakje te tonen.

1. Sleep de schakeloptie **[!UICONTROL Exclude Extreme Values]** naar de positie &quot;aan&quot; of &quot;uit&quot;.
1. Klik op **[!UICONTROL Save]**.
