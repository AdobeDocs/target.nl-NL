---
keywords: problemen oplossen;veelgestelde vragen;Veelgestelde vragen;Veelgestelde vragen;Algemene vragen;globaal;globale mbox
description: Lees veelgestelde vragen (FAQs) en antwoorden over Adobe [!DNL Target] globale vakken.
title: Wat worden vaak gestelde vragen over Global mbox?
feature: at.js
role: Developer
exl-id: ec8399df-5222-44bd-9e61-dfce8fd1694d
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Algemene mbox Veelgestelde vragen

Lijst met veelgestelde vragen (FAQ&#39;s) over globale vakken.

## Kan ik meer dan één globale box hebben als mijn [!DNL Target] account is ingesteld op meerdere domeinen? {#section_B7252BA6C3BB4EF4AE9E53F47FD58ABD}

Er wordt slechts één globale box ondersteund voor uw account.

U kunt beperken waar uw activiteiten lopen door URL-regels aan uw activiteiten toe te voegen. Zie voor meer informatie [Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

U kunt ook een parameter op de pagina doorgeven met [targetPageParams](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/){target=_blank} en selecteer vervolgens de parameters in de sectie &quot;URL configureren&quot; in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC) of door de parameters toe te voegen als &quot;verfijningen&quot; in de Form-Based Experience Composer.

## Hoe kan ik inkomstengegevens doorgeven aan een [!DNL Target] globale mbox? {#section_17AEA933BADA4D169CCEDF5833C41306}

Om opbrengst en ordeinformatie over target-global-mbox te verzamelen, moeten de &quot;mbox parameters&quot;naar Doel worden verzonden. Deze parameters zijn naam/waardeparen die worden gebruikt om meer informatie naar Doel te verzenden. Het doel zoekt automatisch deze parameters (gereserveerde namen) om opbrengstgegevens te bevolken.

Voor de `orderConfirmPage`, moet u `orderTotal`, `orderId`, en `productPurchasedId`.

Deze parameters moeten via `targetPageParams()`. Zie voor meer informatie [Parameters doorgeven aan een globale box](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/).

U zult ook het richten aan het omzettingsstuk willen toevoegen zodat het Doel slechts omzettingen op doel-globaal-mbox telt wanneer de pagina van de ordesbevestiging is bekeken, zoals hieronder getoond:

![](assets/revenue1.png)

De sectie Site-pagina&#39;s die hierboven is weergegeven, bevat de volgende selecties: Huidige pagina, URL, bevat, ordende bevestiging.

![](assets/revenue2.png)

De opties in de bovenstaande afbeelding zijn onder andere:

* **Wat wilt u meten met deze activiteit?** Ontvangsten
* **Standaardweergave voor rapportage:** Opbrengst per bezoeker (RPV)
* **Welke actie heeft uw publiek ondernomen om aan te geven dat uw doel is bereikt?** Een mbox, target-global-mbox weergegeven
