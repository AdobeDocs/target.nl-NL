---
keywords: Target;reports;report settings;extreme orders;extreme values
description: U kunt extreme waarden uitsluiten van het beïnvloeden van rapporten in Adobe Target zodat een paar ongebruikelijke orden niet uw activiteitenresultaten beïnvloeden. Een voorbeeld van een ongebruikelijke bestelling zou een coach kunnen zijn die uniformen koopt voor een heel team in plaats van individuele kopers die individuele uniformen kopen.
title: Extreme waarden uitsluiten in Adobe Target-rapporten
feature: report settings
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Extreme waarden uitsluiten

U kunt extreme waarden uitsluiten van het beïnvloeden van rapporten in [!DNL Adobe Target] zodat beïnvloeden een paar ongebruikelijke orden niet uw activiteitenresultaten. Een voorbeeld van een ongebruikelijke bestelling zou een coach kunnen zijn die uniformen koopt voor een heel team in plaats van individuele kopers die individuele uniformen kopen.

>[!NOTE]
>
>De [!UICONTROL Exclude Extreme Values] vlag is alleen van toepassing op activiteiten met [!UICONTROL Revenue] en [!UICONTROL Engagement] metrische typen.

Extreme waarden worden automatisch gemarkeerd op basis van de onderstaande regels. U kunt schakelen tussen het zien van en het uitsluiten van de extreme waarden van uw rapporten. De extreme waarden van een activiteit worden uitgesloten nadat de activiteit gedurende een uur of na 15 orders is uitgevoerd, afhankelijk van welke het eerst komt.

Een waarde wordt als extreem beschouwd als deze meer dan +/- 3 standaardafwijkingen van de gemiddelde orderwaarde is op basis van de laatste maand van gegevens (tot het tijdstip waarop de berekening is gemaakt).

Het filter voor extreme waarden is bijvoorbeeld vaak handig bij het gebruik van RPV. RPV combineert de omrekeningskoers en de gemiddelde orderwaarde, en stelt vaak de volatiliteit van die cijfers bloot. Als u RPV gebruikt en bepaalt dat orders niet normaal verdeeld lijken te zijn, ziet u wellicht meer normale resultaten als u het filter voor extreme volgorde toepast.

Wanneer een waarde als extreem wordt gemarkeerd, wordt de waarde van de volgorde vervangen door de gemiddelde waarde van de ervaring voor de laatste maand, exclusief de uiterste waarden. De volgorde wordt ook als extreem gemarkeerd in het [!UICONTROL Order Details] rapport en in de CSV-download voor dagelijkse resultaten.

**Extreme waarden uitsluiten van uw rapporten:**

1. Open een activiteit die de metrische types van Inkomsten of van de Betrokkenheid omvat, dan klik de **[!UICONTROL Reports]** tabel.
1. Klik op het tandwielpictogram om het **[!UICONTROL Settings]** dialoogvenster weer te geven.

   ![Stap resultaat](assets/exclude_extreme_values.png)

1. Sleep de **[!UICONTROL Exclude Extreme Values]** schakeloptie naar de positie &quot;aan&quot; of &quot;uit&quot;.
1. Klik op **[!UICONTROL Save]**.
