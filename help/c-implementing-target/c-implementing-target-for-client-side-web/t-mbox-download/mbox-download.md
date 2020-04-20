---
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
description: Als u Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.
title: mbox.js-implementatie
subtopic: Getting Started
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: e5948d70eff9a3ec8205eb69591325bd55e37855

---


# mbox.js-implementatie{#mbox-js-implementation}

Als u Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.

U kunt twee bibliotheekverwijzingen gebruiken: [!DNL mbox.js] of [!DNL at.js]. [De voordelen van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) verklaren de verschillen tussen de twee bibliotheken.

>[!NOTE]
>
>**afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020, zullen alle vraag die van mbox.js wordt gemaakt ontbreken en zullen uw pagina&#39;s beïnvloeden die de actieve activiteiten van het Doel hebben. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)At.js voor meer informatie.
>
>Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
>
>Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.

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
Als er al vakken op uw pagina staan van een oudere implementatie, kunnen deze vakken nog steeds worden gebruikt in de nieuwe interface. Het bijgewerkte [!DNL mbox.js] dossier wordt nog vereist, maar deze dozen kunnen voor activiteiten worden geselecteerd en worden uitgegeven gebruikend Composer [!UICONTROL van de]Visuele Ervaring.