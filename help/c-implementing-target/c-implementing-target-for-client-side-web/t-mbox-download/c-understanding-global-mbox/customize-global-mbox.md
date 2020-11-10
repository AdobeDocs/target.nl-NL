---
keywords: global mbox;customize global mbox;edit at.js;at.js;implement at.js
description: Informatie om u te helpen een globale mbox voor at.js aanpassen.
title: Een globale box aanpassen
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Een globale box aanpassen{#customize-a-global-mbox}

Informatie om u te helpen een globale mbox voor at.js aanpassen.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. Schakel deze optie uit **[!UICONTROL Page load enabled (Auto create global mbox)]** en voeg vervolgens de naam toe van de aangepaste globale box die u wilt gebruiken om activiteiten van [!DNL Target]te leveren.

   Dit aangepaste globale vakje wordt ook gebruikt voor klik het volgen.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Klik **[!UICONTROL Save]** wanneer u klaar bent.

1. Implementeer de [!DNL at.js] bibliotheek op uw site.

   Zie [hoe te om at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) voor meer informatie op te stellen.

1. Tijd de overgang met uw versie.

   Zodra u klaar bent om uw globale mbox voor alle activiteiten [!DNL Target] te beginnen te gebruiken die zich voortbewegen, kunt u met deze stap verdergaan.

   Werk de naam van de aangepaste globale box bij zodat deze overeenkomt met de naam die in Stap 2, hierboven, wordt gebruikt.

   >[!IMPORTANT]
   >
   >Wanneer u het bestand opslaat, worden alle activiteiten in uw account gesynchroniseerd met dit selectievakje. Als deze box niet op uw site staat, werken alle activiteiten niet meer.

