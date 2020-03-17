---
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
description: Als u Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.
title: mbox.js-implementatie
subtopic: Getting Started
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# mbox.js-implementatie{#mbox-js-implementation}

Als u Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.

U kunt twee bibliotheekverwijzingen gebruiken: [!DNL mbox.js] of [!DNL at.js]. [De voordelen van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) verklaren de verschillen tussen de twee bibliotheken.

>[!NOTE]
>
>De bibliotheek mbox.js wordt nog steeds ondersteund, maar er zijn geen functie-updates. Alle klanten moeten naar om.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA).

De enige verwijzing naar [!DNL mbox.js] op elke pagina verstrekt de bibliotheken nodig voor al uw activiteiten. [!DNL mbox.js] roept [!DNL Target] van elke pagina die naar het [!DNL mbox.js] dossier verwijst. Dit laat toe [!DNL Target] om het volgende te doen:

* Doelactiviteiten leveren
* Klikken bijhouden
* De meeste succescijfers bijhouden

>[!TIP]
>
>Om de implementatie te vereenvoudigen, kunt u verwijzen naar [!DNL mbox.js] de algemene koptekst.

U hoeft geen verschillende activiteitspecifieke versies van het bestand te onderhouden.

1. Verwijzing [!DNL mbox.js] in de `<head>` sectie van elke pagina op uw plaats.

   `<script src="/ *``*/ *`directoryscripts`*/mbox.js"></script>`

   Waar ` *``*/ *`directoryscripts`*` de map zijn waarin u het [!DNL mbox.js] bestand hebt opgeslagen nadat u het hebt gedownload.
Als er al vakken op uw pagina staan van een oudere implementatie, kunnen deze vakken nog steeds worden gebruikt in de nieuwe interface. Het bijgewerkte [!DNL mbox.js] bestand is nog steeds vereist, maar u kunt deze vakken selecteren voor activiteiten en bewerken met het [!UICONTROL Visual Experience Composer]bestand.