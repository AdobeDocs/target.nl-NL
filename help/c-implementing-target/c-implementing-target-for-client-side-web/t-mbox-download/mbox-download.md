---
keywords: implementation;mbox;download mbox.js;download api;mbox.js api
description: Als u Adobe Target Standard of Target Premium wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.
title: mbox.js-implementatie
feature: null
translation-type: tm+mt
source-git-commit: a85a5c10c31fb0d7eb00c21ff03b2012d044de45
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---


# mbox.js-implementatie

Als u [!DNL Adobe Target Standard] of [!DNL Target Premium] wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.

U kunt twee bibliotheekverwijzingen gebruiken: de [!DNL Adobe Experience Platform Web SDK] of [!DNL at.js]. [De voordelen van at.](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) jslegt de verschillen tussen de bibliotheken mbox.js en at.js uit.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd. We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen.
>
>* **Adobe Experience Platform Web SDK**: Met dit  [!UICONTROL Adobe Experience Platform Web SDK] programma kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in de  [!DNL Experience Cloud] (inclusief  [!DNL Target]). Als u ervoor kiest om naar [!DNL Adobe Experience Platform Web SDK] te migreren, zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Web SDK Guide*.
   >
   >
* **at.js**: De JavaScript-bibliotheek at.js biedt veel voordelen ten opzichte van mbox.js. Het bestand at.js verbetert onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert de beveiliging en biedt betere implementatieopties voor toepassingen op één pagina. Als u verkiest om aan at.js te migreren, zie [How At.js werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) en [Adobe Target Skill Builder: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Hoewel mbox.js momenteel wordt ondersteund (tot 31 maart 2021), hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Door alle klanten naar [!UICONTROL Adobe Experience Platform Web SDK] of at.js te verplaatsen, zullen onze technici en ondersteunend personeel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.

De enige verwijzing naar [!DNL mbox.js] op elke pagina verstrekt de bibliotheken nodig voor al uw activiteiten. [!DNL mbox.js] roept  [!DNL Target] van elke pagina die naar het  [!DNL mbox.js] dossier verwijst. Hierdoor kan [!DNL Target] het volgende doen:

* Doelactiviteiten leveren
* Klikken bijhouden
* De meeste succescijfers bijhouden

>[!TIP]
>
>Om implementatie te vereenvoudigen, kon u [!DNL mbox.js] in uw globale kopbal van verwijzingen voorzien.

U hoeft geen verschillende activiteitspecifieke versies van het bestand te onderhouden.

1. Verwijzing [!DNL mbox.js] in `<head>` sectie van elke pagina op uw plaats.

   `<script src="/ *``*/ *`directoryscripts`*/mbox.js"></script>`

   Hierbij is ` *`directory`*/ *`scripts`*` de map waarin u het [!DNL mbox.js]-bestand hebt opgeslagen nadat u het hebt gedownload.
Als er al vakken op uw pagina staan van een oudere implementatie, kunnen deze vakken nog steeds worden gebruikt in de nieuwe interface. Het bijgewerkte [!DNL mbox.js]-bestand is nog steeds vereist, maar deze vakken kunnen worden geselecteerd voor activiteiten en bewerkt met [!UICONTROL Visual Experience Composer].