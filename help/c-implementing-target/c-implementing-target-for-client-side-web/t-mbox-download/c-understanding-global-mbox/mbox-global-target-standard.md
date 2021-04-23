---
keywords: global mbox;target classic;use global mbox from target classic
description: Leer hoe te om een erfenis globale mbox voor uw Adobe te gebruiken  [!DNL Target] activiteiten als u reeds een globale mbox op uw pagina's voor uw erfenisimplementaties hebt gecreeerd.
title: Kan ik een globale box van een Verouderde implementatie gebruiken?
feature: at.js
role: Developer
exl-id: 1eb6836b-6b3c-4494-af67-cd72a4f357e2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Een globale box uit een oudere implementatie gebruiken

Standaard maakt [!DNL Target] een globale box met de naam target-global-mbox, die wordt gebruikt om activiteiten uit te voeren die zijn gemaakt in [!DNL Target]. Nochtans, als u reeds een globaal mbox op uw pagina&#39;s voor uw erfenisimplementaties hebt gecreeerd, kunt u dat mbox voor uw [!DNL Target] activiteiten gebruiken.

>[!NOTE]
>
>Per account kunt u slechts één globale box gebruiken.

Om uw bestaande globale mbox voor zowel [!DNL Target] als uw erfenisimplementatie te gebruiken, moet u een paar parameters plaatsen.

1. Ga naar [!DNL Target] en klik vervolgens op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   Standaard is **[!UICONTROL Page load enabled (Auto-create global mbox]** ingeschakeld en krijgt de aangepaste globale box de naam `target-global-mbox`.

1. Als u een bestaande mbox wilt gebruiken, maak **[!UICONTROL Page load enabled (Auto-create global mbox]** onbruikbaar, en specificeer de naam van eerder gecreeerd globaal mbox op het **[!UICONTROL Global Mbox]** gebied.

   In de vervolgkeuzelijst [!UICONTROL Global Mbox] worden alle vakken in uw account weergegeven. Als u een mbox wilt gebruiken die nog niet bestaat, maakt u de mbox.

1. Klik op **[!UICONTROL Save]**.

   De instellingen mbox.js voor uw account worden bijgewerkt.

1. Download het nieuwe bestand at.js en verwijs ernaar op uw site.

   Alle bestaande activiteiten worden bijgewerkt om de opgegeven global mbox te gebruiken, inclusief activiteiten die eerder zijn gemaakt en geïmplementeerd.

## Problemen met de globale mbox-implementatie oplossen

De volgende FAQs kan worden gebruikt om uw globale mbox implementatie problemen op te lossen:

### Waarom wordt het globale selectievakje niet geladen, of waarom is er latentie bij het laden van het globale selectievakje wanneer de pagina wordt geladen?

Zorg ervoor dat de verwijzing at.js de eerste JavaScript-aanroep op de pagina is. Voor andere oplossingen voor dit probleem, zie [Globale mbox vaak Gestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
