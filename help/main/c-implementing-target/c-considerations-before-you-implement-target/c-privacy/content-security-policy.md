---
keywords: inhoudsbeveiligingsbeleid;csp;at.js;whitelist;lijst van gewenste personen;flicker;pre-hide;pre-hide;prehide
description: Meer informatie over de CSP-instructies (Content Security Policy) die u moet toevoegen wanneer u Adobe Target gebruikt.
title: Hoe werkt [!DNL Target] Beveiligingsbeleid voor inhoud (CSP) verwerken?
feature: Privacy & Security
role: Developer
exl-id: 31457b16-ed21-4540-8d0c-abfb49d1fbe9
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Inhoudsbeveiligingsbeleid (CSP)-instructies

Als u [Beveiligingsbeleid voor inhoud](https://en.wikipedia.org/wiki/Content_Security_Policy) (CSP) voor uw [!DNL Adobe Target] implementatie, moet u de volgende CSP-instructies toevoegen bij het gebruik [at.js 2.1 of hoger](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank}:

* `connect-src` with `*.tt.omtrdc.net` gevoegd op lijst van gewenste personen. Noodzakelijk om het netwerkverzoek toe te staan aan [!DNL Target] rand.
* `style-src unsafe-inline`. Vereist voor het voorbeverbergen en flikkeren van de besturing.
* `script-src unsafe-inline`.  Vereist om JavaScript-uitvoering toe te staan die deel kan uitmaken van een HTML-aanbieding.

## Veelgestelde vragen

Raadpleeg de volgende veelgestelde vragen over beveiligingsbeleid:

### Zijn de het Delen van Middelen van het Middel van de Oorsprong (CORS) en het beleid van de Flash dwars-domein veiligheidskwesties?

De geadviseerde manier om het beleid van CORS uit te voeren is toegang tot slechts vertrouwde op oorsprong toe te staan die het via een lijst van gewenste personen van vertrouwde op domeinen vereisen. Hetzelfde kan gezegd worden van het Flash-interdomeinbeleid. Sommige [!DNL Adobe Target] klanten maken zich zorgen over het gebruik van jokertekens voor domeinen in [!DNL Target]. De zorg is dat als een gebruiker aan een toepassing het programma wordt geopend, en een domein bezoekt dat door het beleid wordt toegestaan, om het even welke kwaadwillige inhoud die op dat domein loopt gevoelige inhoud van de toepassing kan terugwinnen en acties binnen de veiligheidscontext van de het programma geopende gebruiker uitvoeren. Dit wordt algemeen bedoeld als Cross-Site Request Smederij (CSRF).

In een [!DNL Adobe Target] de uitvoering van dit beleid mag echter geen veiligheidskwestie zijn .

&quot;adobe.tt.omtrdc.net&quot; is een domein dat eigendom is van Adobe. [!DNL Adobe Target] is een test- en personalisatiehulpmiddel en verwacht wordt dat [!DNL Target] kan verzoeken van overal ontvangen en verwerken zonder enige authentificatie te vereisen. Deze verzoeken bevatten sleutel/waardeparen die voor het testen A/B, aanbevelingen, of inhoudspartnerij worden gebruikt.

[!DNL Adobe] slaat persoonlijk identificeerbare informatie (PII) of andere gevoelige informatie niet op [!DNL Adobe Target] Edge-servers, waarnaar &quot;adobe.tt.omtrdc.net&quot; wijst.

Verwacht wordt dat [!DNL Target] vanuit elk domein toegankelijk zijn via JavaScript-aanroepen. De enige manier om deze toegang toe te staan is door &quot;toegang-controle-toe:staan-Oorsprong&quot;met een vervanging te bedienen.
