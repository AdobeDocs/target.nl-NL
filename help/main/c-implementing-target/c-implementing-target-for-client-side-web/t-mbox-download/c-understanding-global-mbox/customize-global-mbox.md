---
keywords: global mbox;customize global mbox;edit at.js;at.js;implement at.js
description: Learn how to customize a global mbox for at.js on the Administration-Implementation page in Adobe Target.
title: Hoe kan ik een globale box aanpassen?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Een globale box aanpassen

Informatie die u helpt bij het aanpassen van een [!DNL Adobe Target] global mbox for at.js.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. Uitschakelen **[!UICONTROL Page load enabled (Auto create global mbox)]** Voeg vervolgens de naam toe van het aangepaste globale selectievakje dat u wilt gebruiken om activiteiten te leveren van [!DNL Target].

   >[!IMPORTANT]
   >
   >The change is automatically saved when you select a different global mbox.

   This custom global mbox is also used for click tracking.

   ![custom-global-mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementeer de [!DNL at.js] bibliotheek op uw site.

   See [How to deploy at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) for more information.

1. Tijd de overgang met uw versie.

   Wanneer u klaar bent voor [!DNL Target] om uw globale mbox voor alle activiteiten in de toekomst te beginnen gebruiken, kunt u met deze stap te werk gaan.

   Update the name of the custom global mbox to match the name used in Step 2, above.

   >[!IMPORTANT]
   >
   >All activities in your account sync with this mbox. Ensure that the global mbox is present on your site so that activities continue functioning. Ben zeker om beïnvloede activiteiten uit te geven en opnieuw op te slaan die met Visual Experience Composer (VEC) werden gecreeerd die synchronisatie met dit mbox. Het is niet nodig om activiteiten die zijn gemaakt in de Form-Based Experience Composer of via API opnieuw op te slaan.

