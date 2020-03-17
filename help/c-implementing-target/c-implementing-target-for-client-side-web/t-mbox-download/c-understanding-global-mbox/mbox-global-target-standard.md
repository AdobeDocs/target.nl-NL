---
keywords: global mbox;target classic;use global mbox from target classic
description: Door gebrek, leidt de Norm van het Doel tot globaal mbox genoemd target-global-mbox, die wordt gebruikt om activiteiten in werking te stellen die in de Standaard van het Doel worden gecreeerd. Nochtans, als u reeds een globale mbox op uw pagina's voor uw erfenisimplementaties hebt gecreeerd, kunt u die mbox voor uw Standaardactiviteiten van het Doel gebruiken.
title: Een globale box uit een verouderde implementatie gebruiken
subtopic: Getting Started
topic: Standard
uuid: 31b03dab-99da-4040-bab6-4f5cb452ffdc
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Een globale box uit een verouderde implementatie gebruiken{#use-a-global-mbox-from-a-legacy-implementation}

Door gebrek, leidt de Norm van het Doel tot globaal mbox genoemd target-global-mbox, die wordt gebruikt om activiteiten in werking te stellen die in de Standaard van het Doel worden gecreeerd. Nochtans, als u reeds een globale mbox op uw pagina&#39;s voor uw erfenisimplementaties hebt gecreeerd, kunt u die mbox voor uw Standaardactiviteiten van het Doel gebruiken.

>[!NOTE]
>
>Per account kunt u slechts één globale box gebruiken.

Om uw bestaande globale mbox voor zowel [!DNL Target Standard] als uw erfenisimplementatie te gebruiken, moet u een paar parameters plaatsen.

1. Ga naar [!DNL Target Standard], en klik dan **[!UICONTROL Setup]** > **[!UICONTROL Implementation]**.

   Standaard [!UICONTROL Auto Create Global Mbox] is dit ingeschakeld en krijgt de aangepaste globale box een naam `target-global-mbox`.
1. Als u een bestaande mbox wilt gebruiken, maak onbruikbaar [!UICONTROL Auto Create Global Mbox], en specificeer de naam van eerder gecreeerd globaal mbox op het [!UICONTROL Custom Global Mbox] gebied.

   In de [!UICONTROL Custom Global Mbox] vervolgkeuzelijst worden alle vakken in uw account weergegeven. Als u een box wilt gebruiken die nog niet bestaat, creeer de mbox in Klassiek van het Doel.
1. Klik op **[!UICONTROL Save]**.

   De instellingen mbox.js voor uw account worden bijgewerkt.
1. Download het nieuwe bestand mbox.js en verwijs ernaar op uw site.

   Nadat u de productiesite hebt bijgewerkt met het nieuwe bestand mbox.js, kunt u uw voorkeuren instellen.
1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Preferences]**.
1. Geef in het [!UICONTROL Custom Global Mbox] veld de naam op van het globale selectievakje dat u op de pagina Implementatie hebt geselecteerd.
1. Klik op **[!UICONTROL Submit]**.

   Alle bestaande activiteiten worden bijgewerkt om de opgegeven global mbox te gebruiken, inclusief activiteiten die eerder zijn gemaakt en geïmplementeerd.
   **Problemen met de globale Mbox-implementatie** oplossen *Waarom wordt de globale box niet geladen of waarom wordt er vertraging opgetreden bij het laden van de globale mbox wanneer de pagina wordt geladen?*

Zorg ervoor dat de verwijzing mbox.js de eerste JavaScript-aanroep op de pagina is. Voor andere oplossingen voor dit probleem, zie [Implementatie](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420)Mbox.js.
