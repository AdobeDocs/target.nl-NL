---
keywords: mbox.js faq;mbox.js veelgestelde vragen;document.write;tt.omtr dc.net;parser blocking
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Wat zijn een aantal veelgestelde vragen over  [!DNL Target] mbox.js?
feature: at.js
role: Developer
exl-id: 0e207896-d45b-45f9-8556-6532fda72a45
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# mbox.js Veelgestelde vragen

Antwoorden op veelgestelde vragen over mbox.js.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Waarom worden mijn dozen niet op mijn webpagina&#39;s geactiveerd? {#section_4BA5DA424B734324AAB51E4588FA50F5}

Doelklanten gebruiken soms cloudgebaseerde instanties met [!DNL Target] voor testdoeleinden of eenvoudige concepttest-doeleinden. Deze domeinen, en vele anderen, maken deel uit van [Openbare Achtervoegsellijst](https://publicsuffix.org/list/public_suffix_list.dat).

Moderne browsers slaan cookies niet op als u deze domeinen gebruikt, tenzij u de instelling `cookieDomain` aanpast met targetGlobalSettings(). Zie [Op wolken gebaseerde instanties gebruiken met Doel](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/targeting-using-cloud-based-instances.md#concept_A2077766948F4EA081CE592D8998F566) voor meer informatie.

## Wat is het domein tt.omtr dc.net dat de [!DNL Target] servervraag gaat naar? {#section_999C29940E8B4CAD8A957A6B1D440317}

[!DNL tt.omtrdc.net] is de domeinnaam voor Adobe EDGE netwerk, dat wordt gebruikt om alle vraag naar Doel te ontvangen.

## Waarom gebruiken at.js en mbox.js geen vlag HttpOnly en Veilige koekjes? {#section_74527E3B41B54B0A83F217C3E664ED1F}

HttpOnly kan alleen worden ingesteld via code op de server. Doelcookies, zoals mbox, worden gemaakt en opgeslagen via JavaScript-code, zodat Target de Cookie-vlag HttpOnly niet kan gebruiken.

Beveiliging kan alleen via JavaScript worden ingesteld wanneer de pagina via HTTPS is geladen. Als de pagina voor het eerst wordt geladen via HTTP, kan JavaScript deze markering niet instellen. Als de markering Beveiligen wordt gebruikt, is de cookie bovendien alleen beschikbaar op HTTPS-pagina&#39;s.

Om ervoor te zorgen dat Doel gebruikers correct kan volgen, en omdat de koekjes cliënt-kant worden geproduceerd, gebruikt Target geen van beide vlaggen.
