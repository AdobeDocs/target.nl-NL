---
keywords: at.js plugins;supported plugins;unsupported plugins;ttMeta;ttmeta;mboxTrack
description: Informatie over ondersteunde en niet-ondersteunde insteekmodules voor Adobe Target.
title: at.js plug-ins voor Adobe Target
topic: Standard
uuid: ef36b2b2-bf6d-497e-b3f5-2b572a1b8a8d
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# at.js plug-ins{#at-js-plug-ins}

Informatie over ondersteunde en niet-ondersteunde insteekmodules van het type at.js in Adobe Target.

Veel mensen hebben aangepaste plug-ins en responsplug-ins voor [!DNL mbox.js]. Deze aangepaste plug-ins worden mogelijk niet ondersteund door [!DNL at.js] het bijwerken.

Neem contact op met uw accountvertegenwoordiger als u een plug-in gebruikt die hier niet wordt vermeld en u de status wilt weten.

Hier is de huidige status van enkele plug-ins die door veel klanten worden gebruikt bij gebruik met [!DNL at.js]:

| Insteekmodule | Details |
|--- |--- |
| mboxTrack | Niet ondersteund.<br>Deze wordt vervangen door de functie [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) . Werk de plug-ins bij om de nieuwe functie toe te passen.<br>Zie de pagina [Integrations](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md) . |
| Plug-in voor continue profielback-up | Niet ondersteund.<br>Deze plug-in is afgekeurd toen de levensduur van het doelprofiel werd verlengd van twee weken tot 90 dagen. Controleer de vervaldatum van het cookie van uw box om de instelling voor de levensduur van het profiel op uw account te zien.<br>Neem contact op met ClientCare als u de levensduur van het profiel wilt verlengen tot 90 dagen. |
| ttMeta | Oude SiteCatalyst-plug-ins moeten worden uitgeschakeld en vervangen door [Adobe Analytics als rapportagebron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). De ttMeta-plug-in moet worden uitgeschakeld en vervangen door [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). |