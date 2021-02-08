---
keywords: global mbox;mbox.js implementeren;at.js implementeren
description: Leer over globale mbox in Adobe Target, een naam die wordt gebruikt om naar de enige servervraag te verwijzen die bij de bovenkant van elke Web-pagina in uw implementatie van het Doel wordt gemaakt.
title: Wat is een globale box?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---


# De globale box begrijpen

Informatie over globale mbox, een naam die wordt gebruikt om naar de enige servervraag te verwijzen die bij de bovenkant van elke Web-pagina in uw [!DNL Adobe Target] implementatie wordt gemaakt.

Standaard krijgt de globale box de naam `target-global-mbox`. U kunt de naam van uw account desgewenst wijzigen.

Er zijn verschillende verschillen tussen een standaard mbox (non-global mbox) en de globale mbox, waaronder:

| Standaardbox | Globale mbox |
|--- |--- |
| Een gewone box loopt gewoonlijk rond inhoud met een `<DIV>`-tag. | Het algemene mbox is &quot;leeg&quot; en loopt niet rond inhoud. |
| Inhoud van slechts één activiteit kan in een normale doos worden geleverd. | Inhoud uit meerdere activiteiten kan in één reactie op een global box worden geleverd. |

Als er meerdere activiteiten via de globale box of via meerdere gewone vakjes worden geleverd, bepaalt [!DNL Target] [de prioriteit](/help/c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) waarmee de activiteit (of activiteiten) aan een webpagina wordt geleverd.

Met de functie `targetPageParams` kunt u extra gegevens op paginaniveau samen met het globale vakje verzenden naar [!DNL Target]. Dit is vergelijkbaar met de functionaliteit van de mbox-parameter. Voor meer informatie, zie [Het overgaan van Parameters tot Globale mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).
