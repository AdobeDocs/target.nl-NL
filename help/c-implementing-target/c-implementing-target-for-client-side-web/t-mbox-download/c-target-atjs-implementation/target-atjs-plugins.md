---
keywords: at.js plugins;supported plugins;unsupported plugins;ttMeta;ttmeta;mboxTrack
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Welke verouderde plug-ins worden niet ondersteund in [!DNL Target] at.js?
feature: at.js
role: Developer
exl-id: 1d858f5b-58dc-4181-9cb5-aa6b22011abc
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# at.js plug-ins

Informatie over ondersteunde en niet-ondersteunde insteekmodules van het type at.js in Adobe Target.

Veel mensen hebben aangepaste plug-ins en responsplug-ins voor [!DNL mbox.js] gemaakt. Deze aangepaste plug-ins worden mogelijk niet ondersteund door [!DNL at.js] zonder te worden bijgewerkt.

Neem contact op met uw accountvertegenwoordiger als u een plug-in gebruikt die hier niet wordt vermeld en u de status wilt weten.

Hier is de huidige status van enkele plug-ins die door veel klanten worden gebruikt bij gebruik met [!DNL at.js]:

| Insteekmodule | Details |
|--- |--- |
| mboxTrack | Niet ondersteund.<br>Deze wordt vervangen door de  [functie adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) . Werk de plug-ins bij om de nieuwe functie toe te passen.<br>Zie de  [](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md) integratiepagina. |
| Plug-in voor continue profielback-up | Niet ondersteund.<br>Deze plug-in is afgekeurd toen de levensduur van het doelprofiel werd verlengd van twee weken tot 90 dagen. Controleer de vervaldatum van het cookie van uw box om de instelling voor de levensduur van het profiel op uw account te zien.<br>Neem contact op met ClientCare als u de levensduur van het profiel wilt verlengen tot 90 dagen. |
| ttMeta | Oude SiteCatalyst-plug-ins moeten worden uitgeschakeld en vervangen door [Adobe Analytics als rapportagebron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). De ttMeta-plug-in moet worden uitgeschakeld en vervangen door de [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). |
