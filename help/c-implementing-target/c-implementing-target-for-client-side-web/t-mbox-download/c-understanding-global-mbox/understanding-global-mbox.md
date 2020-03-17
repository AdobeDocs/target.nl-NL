---
keywords: global mbox;implement mbox.js;implement at.js
description: Informatie over globale mbox, een naam die wordt gebruikt om naar de enige servervraag te verwijzen die bij de bovenkant van elke Web-pagina in uw implementatie van het Doel van Adobe wordt gemaakt.
title: De globale box begrijpen
subtopic: Getting Started
topic: Standard
uuid: d8f48c94-6487-437b-828f-f9be7da58f48
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# De globale box begrijpen{#understand-the-global-mbox}

Informatie over globale mbox, een naam die wordt gebruikt om naar de enige servervraag te verwijzen die bij de bovenkant van elke Web-pagina in uw implementatie van het Doel van Adobe wordt gemaakt.

Standaard krijgt de algemene naam mbox de naam [!DNL target-global-mbox]. U kunt de naam van uw account desgewenst wijzigen.

Er zijn verschillende verschillen tussen een standaard mbox (non-global mbox) en de globale mbox, waaronder:

| Standaardbox | Globale mbox |
|--- |--- |
| Een standaardkader loopt gewoonlijk rond de inhoud door een `<DIV>` label. | Het algemene mbox is &quot;leeg&quot; en loopt niet rond inhoud. |
| Inhoud van slechts één activiteit kan in een normale doos worden geleverd. | Inhoud uit meerdere activiteiten kan in één reactie op een global box worden geleverd. |

Als er meerdere activiteiten via de globale box of via meerdere gewone vakjes worden geleverd, [!DNL Target] bepaalt u de prioriteit [](../../../../c-activities/priority.md#concept_1780C11FEA57440499F0047DD6900E0F) waarmee de activiteit (of activiteiten) aan een webpagina wordt geleverd.

Met behulp van de functie kunnen aanvullende gegevens op paginaniveau [!DNL Target] `targetPageParams` samen met het globale vak worden verzonden. Dit is vergelijkbaar met de functionaliteit van de mbox-parameter. Voor meer informatie, zie het [overgaan van Parameters tot Globale mbox](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).
