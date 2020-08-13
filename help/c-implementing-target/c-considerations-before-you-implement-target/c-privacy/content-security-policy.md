---
keywords: content security policy;csp;at.js;whitelist;allowlist;flicker;pre-hide;pre-hiding;prehiding
description: Informatie over CSP-instructies (Content Security Policy) die u moet toevoegen wanneer u Adobe Target at.js 2.1 of hoger gebruikt.
title: Beleid voor inhoudsbeveiliging (CSP)
feature: privacy and security
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Inhoudsbeveiligingsbeleid (CSP)-instructies

Als u het Beleid [van de Veiligheid van de](https://en.wikipedia.org/wiki/Content_Security_Policy) Inhoud (CSP) voor uw implementatie van het Doel gebruikt, zou u de volgende CSP richtlijnen moeten toevoegen wanneer het gebruiken [bij.js 2.1 of later](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` met `*.tt.omtrdc.net` toegevoegd op lijst van gewenste personen. Nodig om het netwerkverzoek aan de [!DNL Target] rand toe te staan.
* `style-src unsafe-inline`. Vereist voor het voorbeverbergen en flikkeren van de besturing.
* `script-src unsafe-inline`.  Vereist om JavaScript-uitvoering toe te staan die deel kan uitmaken van een HTML-aanbieding.
