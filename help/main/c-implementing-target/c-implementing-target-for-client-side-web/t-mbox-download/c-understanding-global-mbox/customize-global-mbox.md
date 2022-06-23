---
keywords: global mbox;aanpassen global mbox;bewerken at.js;at.js;implementeren at.js
description: Leer hoe u een globale mbox voor at.js op de pagina Beheer-Implementatie in Adobe Target aanpast.
title: Hoe kan ik een globale box aanpassen?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Een globale box aanpassen

Informatie die u helpt bij het aanpassen van een [!DNL Adobe Target] global mbox for at.js.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. Uitschakelen **[!UICONTROL Page load enabled (Auto create global mbox)]** Voeg vervolgens de naam toe van het aangepaste globale selectievakje dat u wilt gebruiken om activiteiten te leveren van [!DNL Target].

   >[!IMPORTANT]
   >
   >De wijziging wordt automatisch opgeslagen wanneer u een ander algemeen vakje selecteert.

   Dit aangepaste globale vakje wordt ook gebruikt voor klik het volgen.

   ![custom-global-mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementeer de [!DNL at.js] bibliotheek op uw site.

   Zie [Hoe te opstellen bij.js](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/how-to-deployatjs/){target=_blank} voor meer informatie.

1. Tijd de overgang met uw versie.

   Wanneer u klaar bent voor [!DNL Target] om uw globale mbox voor alle activiteiten in de toekomst te beginnen gebruiken, kunt u met deze stap te werk gaan.

   Werk de naam van de aangepaste globale box bij zodat deze overeenkomt met de naam die in Stap 2, hierboven, wordt gebruikt.

   >[!IMPORTANT]
   >
   >Alle activiteiten in uw account worden gesynchroniseerd met dit selectievakje. Zorg ervoor dat de globale box op uw plaats aanwezig is zodat de activiteiten blijven functioneren. Ben zeker om beïnvloede activiteiten uit te geven en opnieuw op te slaan die met Visual Experience Composer (VEC) werden gecreeerd die synchronisatie met dit mbox. Het is niet nodig om activiteiten die zijn gemaakt in de Form-Based Experience Composer of via API opnieuw op te slaan.

