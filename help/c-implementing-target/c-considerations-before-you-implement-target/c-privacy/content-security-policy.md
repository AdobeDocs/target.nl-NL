---
keywords: inhoudsbeveiligingsbeleid;csp;at.js;whitelist;lijst van gewenste personen;flicker;pre-hide;pre-hide;prehide
description: Meer informatie over de CSP-instructies (Content Security Policy) die u moet toevoegen wanneer u Adobe Target gebruikt.
title: Hoe behandelt het Doel het Beleid van de Veiligheid van de Inhoud (CSP)?
feature: Privacy & Security
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Inhoudsbeveiligingsbeleid (CSP)-instructies

Als u [Inhoudsveiligheidsbeleid](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) voor uw [!DNL Adobe Target] implementatie gebruikt, zou u de volgende CSP richtlijnen moeten toevoegen wanneer het gebruiken [at.js 2.1 of recenter](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` met  `*.tt.omtrdc.net` toegevoegd op lijst van gewenste personen. Noodzakelijk om het netwerkverzoek aan de [!DNL Target] rand toe te staan.
* `style-src unsafe-inline`. Vereist voor het voorbeverbergen en flikkeren van de besturing.
* `script-src unsafe-inline`.  Vereist om JavaScript-uitvoering toe te staan die deel kan uitmaken van een HTML-aanbieding.
