---
keywords: mbox.js faq;mbox.js veelgestelde vragen;document.write;tt.omtr dc.net;parser blocking
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Wat zijn een aantal veelgestelde vragen over target mbox.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---


# mbox.js Veelgestelde Vragen{#mbox-js-frequently-asked-questions}

Antwoorden op veelgestelde vragen over mbox.js.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Wat is het effect van mbox.js op pagina-lading tijden? {#section_90B3B94FE0BF4B369577FCB97B67F089}

Zie [Voordelen van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits) voor meer informatie.

## Waarom krijg ik &quot;Parser-blocking&quot;waarschuwingsberichten in Google Chrome wanneer het gebruiken van mbox.js en document.write? {#section_355A3A5BF02F42EEB8271C96EF41590A}

Dit consolebericht toont wanneer het gebruiken van Chrome in vele scenario&#39;s waarin de functie `document.write` binnen het mbox.js- dossier wordt gebruikt. Dit is een waarschuwingsbericht en heeft geen invloed op het installatieproces van uw activiteit.

De beste manier om deze situatie te verhinderen is [uw implementatie van het Doel aan de bibliotheek van at.js JavaScript ](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA) te migreren, die niet de `document.write` functie gebruikt. Het gebruik van at.js biedt veel voordelen ten opzichte van het gebruik van mbox.js. Zie [at.js Veelgestelde vragen](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769) voor meer informatie.

## Waarom worden mijn dozen niet op mijn webpagina&#39;s geactiveerd? {#section_4BA5DA424B734324AAB51E4588FA50F5}

Doelklanten gebruiken soms cloudgebaseerde instanties met [!DNL Target] voor testdoeleinden of eenvoudige concepttest-doeleinden. Deze domeinen, en vele anderen, maken deel uit van [Openbare Achtervoegsellijst](https://publicsuffix.org/list/public_suffix_list.dat).

Moderne browsers slaan cookies niet op als u deze domeinen gebruikt, tenzij u de instelling `cookieDomain` aanpast met targetGlobalSettings(). Zie [Op wolken gebaseerde instanties gebruiken met Doel](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566) voor meer informatie.

## Wat is het domein tt.omtr dc.net dat de servervraag van het Doel gaat? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] is de domeinnaam voor Adobe EDGE netwerk, dat wordt gebruikt om alle vraag naar Doel te ontvangen.

## Waarom gebruiken at.js en mbox.js geen vlag HttpOnly en Veilige koekjes? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly kan alleen worden ingesteld via code op de server. Doelcookies, zoals mbox, worden gemaakt en opgeslagen via JavaScript-code, zodat Target de Cookie-vlag HttpOnly niet kan gebruiken.

Beveiliging kan alleen via JavaScript worden ingesteld wanneer de pagina via HTTPS is geladen. Als de pagina voor het eerst wordt geladen via HTTP, kan JavaScript deze markering niet instellen. Als de markering Beveiligen wordt gebruikt, is de cookie bovendien alleen beschikbaar op HTTPS-pagina&#39;s.

Om ervoor te zorgen dat Doel gebruikers correct kan volgen, en omdat de koekjes cliënt-kant worden geproduceerd, gebruikt Target geen van beide vlaggen.
