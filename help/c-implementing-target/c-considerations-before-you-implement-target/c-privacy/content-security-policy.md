---
keywords: inhoudsbeveiligingsbeleid;csp;at.js;whitelist;lijst van gewenste personen;flicker;pre-hide;pre-hide;prehide
description: Meer informatie over de CSP-instructies (Content Security Policy) die u moet toevoegen wanneer u Adobe Target gebruikt.
title: Hoe behandelt  [!DNL Target] het Beleid van de Veiligheid van de Inhoud (CSP)?
feature: Privacy en beveiliging
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Inhoudsbeveiligingsbeleid (CSP)-instructies

Als u [Inhoudsveiligheidsbeleid](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) voor uw [!DNL Adobe Target] implementatie gebruikt, zou u de volgende CSP richtlijnen moeten toevoegen wanneer het gebruiken [at.js 2.1 of recenter](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` met  `*.tt.omtrdc.net` gevoegd op lijst van gewenste personen. Noodzakelijk om het netwerkverzoek aan de [!DNL Target] rand toe te staan.
* `style-src unsafe-inline`. Vereist voor het voorbeverbergen en flikkeren van de besturing.
* `script-src unsafe-inline`.  Vereist om JavaScript-uitvoering toe te staan die deel kan uitmaken van een HTML-aanbieding.
