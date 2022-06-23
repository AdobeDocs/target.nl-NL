---
keywords: global mbox;target classic;use global mbox from target classic
description: Leer hoe u een verouderde globale box voor uw Adobe gebruikt [!DNL Target] activiteiten als u al een global mbox op uw pagina's hebt gemaakt voor uw oudere implementaties.
title: Kan ik een globale box van een Verouderde implementatie gebruiken?
feature: at.js
role: Developer
exl-id: 1eb6836b-6b3c-4494-af67-cd72a4f357e2
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# Een globale box uit een oudere implementatie gebruiken

Standaard, [!DNL Target] maakt een globale mbox met de naam target-global-mbox, die wordt gebruikt voor het uitvoeren van activiteiten die zijn gemaakt in [!DNL Target]. Als u echter al een algemeen mbox op uw pagina&#39;s hebt gemaakt voor uw oudere implementaties, kunt u dat mbox gebruiken voor uw [!DNL Target] activiteiten.

>[!NOTE]
>
>Per account kunt u slechts één globale box gebruiken.

Om uw bestaande globale mbox voor allebei te gebruiken [!DNL Target] en uw oudere implementatie, moet u een paar parameters plaatsen.

1. Ga naar [!DNL Target]en klik vervolgens op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   Standaard, **[!UICONTROL Page load enabled (Auto-create global mbox]** is ingeschakeld en krijgt de aangepaste algemene mbox een naam `target-global-mbox`.

1. Als u een bestaande mbox wilt gebruiken, maak onbruikbaar **[!UICONTROL Page load enabled (Auto-create global mbox]** en geeft u de naam op van een eerder gemaakt algemeen naamvak in het dialoogvenster **[!UICONTROL Global Mbox]** veld.

   De [!UICONTROL Global Mbox] worden alle vakken in uw account weergegeven. Als u een mbox wilt gebruiken die nog niet bestaat, maakt u de mbox.

1. Klik op **[!UICONTROL Save]**.

   De instellingen voor uw account worden bijgewerkt.

1. Download het nieuwe bestand at.js en verwijs ernaar op uw site.

   Alle bestaande activiteiten worden bijgewerkt om de opgegeven global mbox te gebruiken, inclusief activiteiten die eerder zijn gemaakt en geïmplementeerd.

## Problemen met de globale mbox-implementatie oplossen

De volgende FAQs kan worden gebruikt om uw globale mbox implementatie problemen op te lossen:

### Waarom wordt het globale selectievakje niet geladen, of waarom is er latentie bij het laden van het globale selectievakje wanneer de pagina wordt geladen?

Zorg ervoor dat de verwijzing at.js de eerste JavaScript-aanroep op de pagina is. Voor andere oplossingen voor dit probleem raadpleegt u [Algemene mbox Veelgestelde vragen](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/global-mbox-faq/).
