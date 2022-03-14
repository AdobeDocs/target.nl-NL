---
keywords: inhoudsbeveiligingsbeleid;csp;at.js;whitelist;lijst van gewenste personen;flicker;pre-hide;pre-hide;prehide
description: Meer informatie over de CSP-instructies (Content Security Policy) die u moet toevoegen wanneer u Adobe Target gebruikt.
title: Hoe werkt [!DNL Target] Beveiligingsbeleid voor inhoud (CSP) verwerken?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Inhoudsbeveiligingsbeleid (CSP)-instructies

Als u [Beveiligingsbeleid voor inhoud](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) voor uw [!DNL Adobe Target] implementatie, moet u de volgende CSP-instructies toevoegen bij het gebruik [at.js 2.1 of hoger](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md):

* `connect-src` with `*.tt.omtrdc.net` gevoegd op lijst van gewenste personen. Noodzakelijk om het netwerkverzoek toe te staan aan [!DNL Target] rand.
* `style-src unsafe-inline`. Vereist voor het voorbeverbergen en flikkeren van de besturing.
* `script-src unsafe-inline`.  Vereist om JavaScript-uitvoering toe te staan die deel kan uitmaken van een HTML-aanbieding.
