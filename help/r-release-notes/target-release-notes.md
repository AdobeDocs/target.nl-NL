---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-releases.
title: Voorlopige Adobe Target-opmerkingen
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 8ef5b9c09cc016aad08c75d62f361b22630a7a56
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---


# Opmerkingen bij de release van Target (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 15 juni 2020**

Zie Opmerkingen bij de release van [Target voor informatie over de huidige release](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020 zullen alle oproepen van mbox.js mislukken en gevolgen hebben voor uw pagina&#39;s waarop Target-activiteiten worden uitgevoerd. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.
   >
   >
* **Aankondigingen** van Target: Zie de Target-aankondigingspagina voor informatie over aanstaande gebeurtenissen, zoals Target Skill Builder-sessies, ontwikkelaarstekkers, webinars en Target Coffee Break-sessies. Zie [Target-aankondigingen](/help/r-release-notes/target-announcements.md)voor meer informatie.


## releases (15 juni 2020) om 1.js 1.8.2 en om 2.3.1.

De volgende verbeteringen en correcties zijn aangebracht in de bibliotheken [!DNL Target] at.js:

### om.js 1.8.2

* Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 1.*x* zou tot het serverdomein verkeerd kunnen leiden, dat in het [!DNL Target] verzoek mislukte. (TNT-35064)

### om.js 2.3.1

* De `deviceIdLifetime` instelling is overschreven via [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)
* Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 2.*x* zou tot het serverdomein verkeerd kunnen leiden, dat in het [!DNL Target] verzoek mislukte. (TNT-35065)
* Probleem verholpen bij het gebruik van de [!DNL Target] extensie v2 en de [!DNL Launch] [!DNL Adobe Analytics] extensie, [!DNL Launch] waarmee de [!DNL Target][!DNL Analytics] `sendBeacon` aanroep werd vertraagd. (TNT-36407, TNT-35990, TNT-36000)

## Target Standard/Premium 20.5.1 (17 juni 2020)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Analytics for Target (A4T)-ondersteuning voor activiteiten voor automatisch toewijzen | Met de release van juni ondersteunen Auto-Allocate-tests [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md). Dankzij deze integratie kunt u de multi-gewapende bandeigenschappen van Auto-Allocate gebruiken om het verkeer naar het winnen van ervaringen te sturen, terwijl u tegelijkertijd een Adobe Analytics-doelstelling gebruikt voor metrische en/of Adobe Analytics-rapportage en -analyse. Als u A4T [al hebt](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) geïmplementeerd voor gebruik met A/B Test and Experience Targeting-activiteiten, bent u klaar! |
| Uitgever | Deze nieuwe rol is vergelijkbaar met de huidige rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |
| A4T-ondersteuning op 25 [!DNL Analysis Workspace]<br>juni 2020 | [!UICONTROL Anaytics for Target] (A4T) wordt nu ondersteund in [!DNL Analysis Workspace]. Met [!UICONTROL Analytics for Target (A4T) panel] deze functie kunt u uw [!DNL Adobe Target] activiteiten en ervaringen analyseren in [!DNL Analysis Workspace].<br>Zie het deelvenster [Analytics for Target (A4T) in de](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics Tools Guide ** voor meer informatie. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Meld u aan voor de Adobe Priority Product Update als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
