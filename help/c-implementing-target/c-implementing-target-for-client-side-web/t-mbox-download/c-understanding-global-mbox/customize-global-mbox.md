---
keywords: global mbox;aanpassen global mbox;bewerken at.js;at.js;implementeren at.js
description: Leer hoe u een globale mbox voor at.js op de pagina Beheer-Implementatie in Adobe Target aanpast.
title: Hoe kan ik een globale box aanpassen?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: fb0a62ecc5609e7b8ef5f6a4fb5a94f8ba025fec
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Een globale box aanpassen

Informatie om u te helpen een globale mbox voor at.js aanpassen.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

1. Schakel **[!UICONTROL Page load enabled (Auto create global mbox)]** uit en voeg vervolgens de naam toe van het aangepaste globale vakje dat u wilt gebruiken om activiteiten van [!DNL Target] te leveren.

   >[!IMPORTANT]
   >
   >De wijziging wordt automatisch opgeslagen wanneer u een ander algemeen vakje selecteert.

   Dit aangepaste globale vakje wordt ook gebruikt voor klik het volgen.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementeer de [!DNL at.js]-bibliotheek op uw site.

   Zie [Hoe te om at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) voor meer informatie op te stellen.

1. Tijd de overgang met uw versie.

   Wanneer u klaar bent voor [!DNL Target] om uw globale mbox voor alle activiteiten in de toekomst te beginnen te gebruiken, kunt u met deze stap te werk gaan.

   Werk de naam van de aangepaste globale box bij zodat deze overeenkomt met de naam die in Stap 2, hierboven, wordt gebruikt.

   >[!IMPORTANT]
   >
   >Alle activiteiten in uw account worden gesynchroniseerd met dit selectievakje. Als dit selectievakje niet op uw site staat, werken alle activiteiten niet meer.
