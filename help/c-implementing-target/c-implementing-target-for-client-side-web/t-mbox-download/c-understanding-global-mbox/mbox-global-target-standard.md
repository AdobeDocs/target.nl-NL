---
keywords: global mbox;target classic;use global mbox from target classic
description: Door gebrek, leidt de Norm van het Doel tot globaal mbox genoemd target-global-mbox, die wordt gebruikt om activiteiten in werking te stellen die in de Standaard van het Doel worden gecreeerd. Nochtans, als u reeds een globale mbox op uw pagina's voor uw erfenisimplementaties hebt gecreeerd, kunt u die mbox voor uw Standaardactiviteiten van het Doel gebruiken.
title: Een globale box uit een verouderde implementatie gebruiken
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---


# Een globale box uit een verouderde implementatie gebruiken{#use-a-global-mbox-from-a-legacy-implementation}

Door gebrek, [!DNL Target] creeert een globale mbox genoemd target-global-mbox, die wordt gebruikt om activiteiten in in in werking te stellen die worden gecreeerd [!DNL Target]. Als u echter al een algemene mbox op uw pagina&#39;s hebt gemaakt voor uw oudere implementaties, kunt u die mbox gebruiken voor uw [!DNL Target] activiteiten.

>[!NOTE]
>
>Per account kunt u slechts één globale box gebruiken.

Om uw bestaande globale mbox voor zowel [!DNL Target] als uw erfenisimplementatie te gebruiken, moet u een paar parameters plaatsen.

1. Ga naar [!DNL Target], en klik dan **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   Standaard **[!UICONTROL Page load enabled (Auto-create global mbox]** is dit ingeschakeld en krijgt de aangepaste globale box een naam `target-global-mbox`.

1. Als u een bestaande mbox wilt gebruiken, maak onbruikbaar **[!UICONTROL Page load enabled (Auto-create global mbox]**, en specificeer de naam van eerder gecreeerd globaal mbox op het **[!UICONTROL Global Mbox]** gebied.

   In de [!UICONTROL Global Mbox] vervolgkeuzelijst worden alle vakken in uw account weergegeven. Als u een mbox wilt gebruiken die nog niet bestaat, maakt u de mbox.

1. Klik op **[!UICONTROL Save]**.

   De instellingen mbox.js voor uw account worden bijgewerkt.

1. Download het nieuwe bestand at.js en verwijs ernaar op uw site.

   Alle bestaande activiteiten worden bijgewerkt om de opgegeven global mbox te gebruiken, inclusief activiteiten die eerder zijn gemaakt en geïmplementeerd.

## Problemen met de globale mbox-implementatie oplossen

De volgende FAQs kan worden gebruikt om uw globale mbox implementatie problemen op te lossen:

### Waarom wordt het globale selectievakje niet geladen, of waarom is er latentie bij het laden van het globale selectievakje wanneer de pagina wordt geladen?

Zorg ervoor dat de verwijzing at.js de eerste JavaScript-aanroep op de pagina is. Voor andere oplossingen voor dit probleem, zie [Globale doos Veelgestelde Vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
