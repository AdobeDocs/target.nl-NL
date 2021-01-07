---
keywords: content security policy;csp;at.js;whitelist;allowlist;flicker;pre-hide;pre-hiding;prehiding
description: Informatie over CSP-instructies (Content Security Policy) die u moet toevoegen wanneer u Adobe Target at.js 2.1 of hoger gebruikt.
title: Beleid voor inhoudsbeveiliging (CSP)
feature: Privacy & Security
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# Inhoudsbeveiligingsbeleid (CSP)-instructies

Als u [Inhoudsveiligheidsbeleid](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) voor uw [!DNL Adobe Target] implementatie gebruikt, zou u de volgende CSP richtlijnen moeten toevoegen wanneer het gebruiken [at.js 2.1 of recenter](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` met  `*.tt.omtrdc.net` toegevoegd op lijst van gewenste personen. Noodzakelijk om het netwerkverzoek aan de [!DNL Target] rand toe te staan.
* `style-src unsafe-inline`. Vereist voor het voorbeverbergen en flikkeren van de besturing.
* `script-src unsafe-inline`.  Vereist om JavaScript-uitvoering toe te staan die deel kan uitmaken van een HTML-aanbieding.
