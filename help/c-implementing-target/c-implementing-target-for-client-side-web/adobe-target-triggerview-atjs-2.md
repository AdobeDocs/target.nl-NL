---
keywords: adobe.target.triggerView;triggerView;triggerview;trigger view;at.js;functions;function;viewName;viewname;view name
description: Informatie over de functie adobe.target.triggerView (viewName, options) voor de JavaScript-bibliotheek van Adobe Target at.js.
title: adobe.target.triggerView (viewName, options) - at.js 2.x
feature: client-side
translation-type: tm+mt
source-git-commit: 5c7ab4af3d4290ef8fa53ed51ed1c2e8336e02f9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# adobe.target.triggerView (viewName, options) - at.js 2.x

Deze functie kan worden aangeroepen wanneer een nieuwe pagina wordt geladen of wanneer een component op een pagina opnieuw wordt weergegeven. `adobe.target.triggerView()` moet worden geïmplementeerd voor toepassingen van één pagina (SPA) om de Visual Experience Composer (VEC) te gebruiken voor het maken van A/B Tests en Experience Targeting (XT)-activiteiten. Als `adobe.target.triggerView()` het niet op de plaats wordt uitgevoerd, kan VEC niet voor SPA worden gebruikt. Zie Toepassing [enkele pagina voor meer informatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).

>[!NOTE]
>
>Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*.

| Parameter | Type | Vereist? | Beschrijving |
| --- | --- | --- | --- |
| viewName | String | Ja | Geef elke naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze weergavenaam wordt in het [!UICONTROL Modifications] deelvenster VEC weergegeven, zodat marketers handelingen kunnen maken en hun A/B- en XT-activiteiten kunnen uitvoeren. |
| opties | Object | Nee |  |
| opties > pagina | Boolean | Nee | **TRUE:** De standaardwaarde van de pagina is true. Wanneer page=true, worden de berichten verzonden naar het [!DNL Target] achterste voor het verhogen van het aantal impressies.<br>Een bericht wordt altijd standaard verzonden wanneer een bericht `triggerView` wordt aangeroepen, behalve wanneer de opties > pagina op false zijn ingesteld.<br>**FALSE:** Wanneer page=false, worden geen meldingen verzonden voor het verhogen van het aantal impressies. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

## Voorbeeld: Waar

`triggerView()` vraag om een bericht naar de achtergrond van het Doel voor het verhogen van activiteitenindrukkingen en andere metriek te verzenden.

```
adobe.target.triggerView("homeView")
```

## Voorbeeld: Onwaar

`triggerView()` oproep om geen meldingen naar de Target-backend te laten verzenden voor het tellen van de indruk.

```
adobe.target.triggerView("homeView", {page: false})
```
