---
keywords: mbox.js faq;mbox.js frequently asked questions;document.write;tt.omtrdc.net;parser blocking
description: Antwoorden op veelgestelde vragen over mbox.js.
title: mbox.js Veelgestelde vragen
feature: null
subtopic: Getting Started
uuid: af3105ab-87d9-4dbf-a380-b72788928958
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# mbox.js Veelgestelde vragen{#mbox-js-frequently-asked-questions}

Antwoorden op veelgestelde vragen over mbox.js.

## Wat is het effect van mbox.js op pagina-lading tijden? {#section_90B3B94FE0BF4B369577FCB97B67F089}

Voor meer informatie, zie [Voordelen van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits).

## Waarom krijg ik &quot;Parser-blocking&quot;waarschuwingsberichten in Google Chrome wanneer het gebruiken van mbox.js en document.write? {#section_355A3A5BF02F42EEB8271C96EF41590A}

Dit consolebericht toont wanneer het gebruiken van Chrome in vele scenario&#39;s waarin de `document.write` functie binnen het mbox.js- dossier wordt gebruikt. Dit is een waarschuwingsbericht en heeft geen invloed op het installatieproces van uw activiteit.

De beste manier om deze situatie te voorkomen is uw doelimplementatie te [migreren naar de JavaScript-bibliotheek](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md#task_DE55DCE9AC2F49728395665DE1B1E6EA)at.js, die de `document.write` functie niet gebruikt. Het gebruik van at.js biedt veel voordelen ten opzichte van het gebruik van mbox.js. Voor meer informatie, zie [bij.js Veelgestelde Vragen](../../../c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md#concept_D6EFE8D84A06476DB5ABD494D7E8C769).

## Waarom worden mijn dozen niet op mijn webpagina&#39;s geactiveerd? {#section_4BA5DA424B734324AAB51E4588FA50F5}

De doelklanten gebruiken soms op wolk-gebaseerde instanties met [!DNL Target] voor het testen of eenvoudige proef-van-concept doeleinden. Deze domeinen, en vele anderen, maken deel uit van de [Openbare Lijst](https://publicsuffix.org/list/public_suffix_list.dat)van het Achtervoegsel.

Moderne browsers slaan cookies niet op als u deze domeinen gebruikt, tenzij u de `cookieDomain` instelling aanpast met targetGlobalSettings(). Zie Op cloud gebaseerde instanties [gebruiken met Doel](../../../c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566)voor meer informatie.

## Wat is het domein tt.omtr dc.net dat de servervraag van het Doel gaat? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] is de domeinnaam voor Adobe EDGE netwerk, dat wordt gebruikt om alle vraag naar Doel te ontvangen.

## Waarom gebruiken at.js en mbox.js geen vlag HttpOnly en Veilige koekjes? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly kan alleen worden ingesteld via code op de server. Doelcookies, zoals mbox, worden gemaakt en opgeslagen via JavaScript-code, zodat Target de Cookie-vlag HttpOnly niet kan gebruiken.

Beveiliging kan alleen via JavaScript worden ingesteld wanneer de pagina via HTTPS is geladen. Als de pagina voor het eerst wordt geladen via HTTP, kan JavaScript deze markering niet instellen. Als de markering Beveiligen wordt gebruikt, is de cookie bovendien alleen beschikbaar op HTTPS-pagina&#39;s.

Om ervoor te zorgen dat Doel gebruikers correct kan volgen, en omdat de koekjes cliënt-kant worden geproduceerd, gebruikt Target geen van beide vlaggen.
