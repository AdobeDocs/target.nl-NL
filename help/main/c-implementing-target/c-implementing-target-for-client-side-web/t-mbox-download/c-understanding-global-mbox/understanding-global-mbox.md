---
keywords: global mbox;;implementeren at.js
description: Meer informatie over de globale mbox in Adobe Target, een naam die wordt gebruikt om te verwijzen naar de enige serveroproep die boven aan elke webpagina in uw [!DNL Target] uitvoering.
title: Wat is een globale box?
feature: at.js
role: Developer
exl-id: 84d15feb-f5df-4879-ae35-a7f455c1b20f
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# De globale box begrijpen

Informatie over globale mbox, een naam die wordt gebruikt om naar de enige servervraag te verwijzen die bij de bovenkant van elke Web-pagina in uw wordt gemaakt [!DNL Adobe Target] uitvoering.

Standaard krijgt het algemene mbox de naam `target-global-mbox`. U kunt de naam van uw account desgewenst wijzigen.

Er zijn verschillende verschillen tussen een standaard mbox (non-global mbox) en de globale mbox, waaronder:

| Standaardbox | Globale mbox |
|--- |--- |
| Een standaardkader loopt gewoonlijk rond inhoud met een `<DIV>` tag. | Het algemene mbox is &quot;leeg&quot; en loopt niet rond inhoud. |
| Inhoud van slechts één activiteit kan in een normale doos worden geleverd. | Inhoud uit meerdere activiteiten kan in één reactie op een global box worden geleverd. |

Als er meerdere activiteiten worden geleverd via de globale box of via meerdere gewone vakjes, [!DNL Target] [bepaalt de prioriteit](/help/main/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) waardoor de activiteit (of activiteiten) aan een webpagina wordt (worden) geleverd.

Er kunnen aanvullende gegevens op paginaniveau worden verzonden naar [!DNL Target] samen met de globale box door `targetPageParams` functie. Dit is vergelijkbaar met de functionaliteit van de mbox-parameter. Zie voor meer informatie [Parameters doorgeven aan een globale box](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/){target=_blank}.
