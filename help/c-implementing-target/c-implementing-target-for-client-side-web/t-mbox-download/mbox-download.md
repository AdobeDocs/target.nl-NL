---
keywords: implementatie;mbox;download mbox.js;download api;mbox.js api
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Hoe implementeer ik [!DNL Target] met mbox.js?
feature: at.js
role: Developer
exl-id: 105095d7-8e29-413b-a7f4-e46e2e30e91f
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# mbox.js-implementatie

Als u [!DNL Adobe Target Standard] of [!DNL Target Premium] wilt gebruiken, voegt u één coderegel toe om mbox.js aan te roepen.

U kunt twee bibliotheekverwijzingen gebruiken: de [!DNL Adobe Experience Platform Web SDK] of [!DNL at.js]. [De voordelen van at.](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) jslegt de verschillen tussen de bibliotheken mbox.js en at.js uit.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

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
