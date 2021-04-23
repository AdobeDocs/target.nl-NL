---
keywords: problemen oplossen;veelgestelde vragen;Veelgestelde vragen;Veelgestelde vragen;Algemene vragen;globaal;globale mbox
description: Lees veelgestelde vragen (FAQs) en antwoorden over Adobe [!DNL Target] globale dozen.
title: Wat worden vaak gestelde vragen over Global mbox?
feature: at.js
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Algemene mbox Veelgestelde vragen

Lijst met veelgestelde vragen (FAQ&#39;s) over globale vakken.

## Kan ik meer dan één globale mbox hebben als mijn [!DNL Target] rekening over veelvoudige domeinen wordt geplaatst? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Er wordt slechts één globale box ondersteund voor uw account.

U kunt beperken waar uw activiteiten lopen door URL-regels aan uw activiteiten toe te voegen. Zie [Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s](/help/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781) voor meer informatie.

U kunt ook een parameter op de pagina doorgeven met [targetPageParams](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) en vervolgens die parameters selecteren in de sectie &quot;configure URL&quot; in de [!UICONTROL Visual Experience Composer] (VEC) of door de parameters toe te voegen als &quot;verfijningen&quot; in de Form-Based Experience Composer.

## Hoe kan ik inkomstengegevens doorgeven op een globale mbox van [!DNL Target]? {#section_17AEA933BADA4D169CCEDF5833C41306}

Om opbrengst en ordeinformatie over target-global-mbox te verzamelen, moeten de &quot;mbox parameters&quot;naar Doel worden verzonden. Deze parameters zijn naam/waardeparen die worden gebruikt om meer informatie naar Doel te verzenden. Het doel zoekt automatisch deze parameters (gereserveerde namen) om opbrengstgegevens te bevolken.

Voor `orderConfirmPage`, zou u binnen `orderTotal`, `orderId`, en `productPurchasedId` moeten overgaan. Zie [Een bevestigingsvak voor bestellingen maken - mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md#task_0036D5F6C062442788BB55E872816D82) voor meer informatie.

Dezelfde parameters moeten via `targetPageParams()` naar de target-global-mbox worden verzonden. Voor meer informatie, zie [Het overgaan van Parameters tot Globale mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md#concept_33362A04146C4E3C8E7089B65F38B5E5).

U zult ook het richten aan het omzettingsstuk willen toevoegen zodat het Doel slechts omzettingen op doel-globaal-mbox telt wanneer de pagina van de ordesbevestiging is bekeken, zoals hieronder getoond:

![](assets/revenue1.png)

De sectie Site-pagina&#39;s die hierboven is weergegeven, bevat de volgende selecties: Huidige pagina, URL, bevat, ordende bevestiging.

![](assets/revenue2.png)

De opties in de bovenstaande afbeelding zijn onder andere:

* **Wat wilt u met deze activiteit meten:** Inkomsten
* **Standaardweergave voor rapportage:** inkomsten per bezoeker (RPV)
* **Welke actie heeft uw publiek ondernomen om aan te geven dat uw doel is bereikt?** Een mbox, target-global-mbox weergegeven
