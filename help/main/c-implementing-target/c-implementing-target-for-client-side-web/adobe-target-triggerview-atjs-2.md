---
keywords: adobe.target.triggerView;triggerView;triggerview;triggerweergave;at.js;functies;function;viewName;viewname;view name
description: Gebruik de functie adobe.target.triggerView() voor de Adobe [!DNL Target] at.js JavaScript-bibliotheek voor gebruik in toepassingen voor één pagina (SPA). (om 2.x.js)
title: Hoe gebruik ik de functie adobe.target.triggerView()?
feature: at.js
role: Developer
exl-id: 619d5166-d1d9-49a6-9807-338544782e66
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# adobe.target.triggerView (viewName, options) - at.js 2.x

Deze functie kan worden aangeroepen wanneer een nieuwe pagina wordt geladen of wanneer een component op een pagina opnieuw wordt weergegeven. `adobe.target.triggerView()` moet worden geïmplementeerd voor toepassingen van één pagina (SPA) om de Visual Experience Composer (VEC) te gebruiken voor het maken van A/B Tests en Experience Targeting (XT)-activiteiten. Indien `adobe.target.triggerView()` niet op de locatie wordt geïmplementeerd, kan de VEC niet voor SPA worden gebruikt. Zie voor meer informatie [Toepassing van één pagina](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/target-atjs-single-page-application/).

>[!NOTE]
>
>Deze functie is geïntroduceerd met at.js 2.x. Deze functie is niet beschikbaar voor versie 1 van at.js.*x*.

| Parameter | Type | Vereist? | Beschrijving |
| --- | --- | --- | --- |
| viewName | String | Ja | Geef elke naam door als een type tekenreeks dat u de weergave wilt vertegenwoordigen. Deze weergavenaam wordt weergegeven in het dialoogvenster [!UICONTROL Modifications] paneel van VEC voor marketers om acties tot stand te brengen en hun activiteiten A/B en XT in werking te stellen. |
| opties | Object | Nee |  |
| opties > pagina | Boolean | Nee | **TRUE:** De standaardwaarde van de pagina is true. Als page=true is, worden meldingen verzonden naar de [!DNL Target] voor het verhogen van het aantal imkers.<br>Een bericht wordt altijd standaard verzonden wanneer een `triggerView` wordt aangeroepen, behalve wanneer opties > pagina is ingesteld op false.<br>**FALSE:** Wanneer page=false, worden geen meldingen verzonden voor het verhogen van het aantal impressies. Dit zou moeten worden gebruikt wanneer u een component op een pagina met een aanbieding slechts opnieuw wilt teruggeven. |

## Voorbeeld: Waar

`triggerView()` vraag om een bericht naar de achtergrond van het Doel voor het verhogen van activiteitenindrukkingen en andere metriek te verzenden.

```javascript
adobe.target.triggerView("homeView")
```

## Voorbeeld: Onwaar

`triggerView()` oproep om geen meldingen naar de Target-backend te laten verzenden voor het tellen van de indruk.

```javascript
adobe.target.triggerView("homeView", {page: false})
```
