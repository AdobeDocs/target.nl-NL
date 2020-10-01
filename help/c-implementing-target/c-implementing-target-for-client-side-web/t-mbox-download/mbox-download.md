---
keywords: Implementation;Mbox;download mbox.js;download api;mbox.js api
description: Als u Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.
title: mbox.js-implementatie
feature: null
subtopic: Getting Started
topic: Standard
uuid: aa53dfd4-db42-4a33-b561-7e84ca7e4497
translation-type: tm+mt
source-git-commit: 1397891d4451d9e66a25e018e6bd7078e70cfd3f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---


# mbox.js-implementatie{#mbox-js-implementation}

Als u Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.

U kunt twee bibliotheekverwijzingen gebruiken: [!DNL mbox.js] of [!DNL at.js]. [De voordelen van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) verklaren de verschillen tussen de twee bibliotheken.

>[!NOTE]
>
>**mbox.js-verwijdering**: Op 18 januari 2021 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 18 januari 2021, zullen alle vraag die van mbox.js wordt gemaakt zachtjes ontbreken en zullen uw pagina&#39;s beïnvloeden die de activiteiten van het Doel hebben die door standaardinhoud te dienen lopen. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)At.js voor meer informatie.
>
>Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
>
>Door alle klanten naar at.js te verplaatsen, zullen onze ingenieurs en steunpersoneel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.

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