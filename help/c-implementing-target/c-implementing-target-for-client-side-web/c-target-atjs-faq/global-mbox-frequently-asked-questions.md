---
keywords: troubleshooting;frequently asked questions;FAQ;FAQs;global;global mbox
description: Lijst met veelgestelde vragen (FAQ's) over globale vakken.
title: Algemene mbox Veelgestelde vragen
feature: client-side
topic: Standard
uuid: f8eb0331-bc2b-4be9-9b35-c764ac091ef4
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# Algemene mbox Veelgestelde vragen{#global-mbox-frequently-asked-questions}

Lijst met veelgestelde vragen (FAQ&#39;s) over globale vakken.

## Kan ik meer dan één globale mbox hebben als mijn rekening van het Doel over veelvoudige domeinen wordt geplaatst? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Er wordt slechts één globale box ondersteund voor uw account.

U kunt beperken waar uw activiteiten lopen door URL-regels aan uw activiteiten toe te voegen. Zie Gelijke ervaring [opnemen op vergelijkbare pagina&#39;s](/help/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781)voor meer informatie.

U zou een parameter op de pagina ook kunnen overgaan gebruikend [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) en dan die parameters in de &quot;vorm URL&quot;sectie in de [!UICONTROL Visual Experience Composer] (VEC) selecteren of door de parameters als &quot;verfijningen&quot;in de vorm-Gebaseerde Composer van de Ervaring toe te voegen.

## Hoe geef ik opbrengstgegevens over een Globaal doel door mbox? {#section_17AEA933BADA4D169CCEDF5833C41306}

Om opbrengst en ordeinformatie over target-global-mbox te verzamelen, moeten de &quot;mbox parameters&quot;naar Doel worden verzonden. Deze parameters zijn naam/waardeparen die worden gebruikt om meer informatie naar Doel te verzenden. Het doel zoekt automatisch deze parameters (gereserveerde namen) om opbrengstgegevens te bevolken.

Voor de `orderConfirmPage`, zou u binnen moeten overgaan `orderTotal`, `orderId`, en `productPurchasedId`. Zie [Een bevestigingsbox voor bestellingen maken - mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md#task_0036D5F6C062442788BB55E872816D82)voor meer informatie.

Dezelfde parameters moeten via `targetPageParams()`de methode target-global-mbox worden verzonden. Voor meer informatie, zie het [overgaan van Parameters tot Globale mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).

U zult ook het richten aan het omzettingsstuk willen toevoegen zodat het Doel slechts omzettingen op doel-globaal-mbox telt wanneer de pagina van de ordesbevestiging is bekeken, zoals hieronder getoond:

![](assets/revenue1.png)

De sectie Site-pagina&#39;s die hierboven is weergegeven, bevat de volgende selecties: Huidige pagina, URL, bevat, ordende bevestiging.

![](assets/revenue2.png)

De opties in de bovenstaande afbeelding zijn onder andere:

* **Wat wilt u meten met deze activiteit?** Ontvangsten
* **Standaardweergave voor rapportage:** Opbrengst per bezoeker (RPV)
* **Welke actie heeft uw publiek ondernomen om aan te geven dat uw doel is bereikt?** Een mbox, target-global-mbox weergegeven