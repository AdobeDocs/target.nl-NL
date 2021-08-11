---
keywords: appel;ITP;Intelligente traceringspreventie;Ervaar wolk id;ecid;itp
description: Meer informatie over Adobe [!DNL Target] en de impact van het Apple Intelligent Tracking Prevention (ITP)-initiatief dat de privacy van Safari-gebruikers wil beschermen.
title: Hoe wordt  [!DNL Target] Apple ITP-ondersteuning verwerkt?
feature: Privacy en beveiliging
role: Developer
exl-id: 05a62be5-ccfb-4d5c-b511-35023b95e567
source-git-commit: 898a18cbd9c6f499f9e7b74078575bc149c9a292
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) is het initiatief van Apple om de privacy van Safari-gebruikers te beschermen. De eerste release van ITP, die in 2017 plaatsvond, was gericht op het gebruik van cookies van derden. In feite heeft Apple alle cookies van derden geblokkeerd, wat op zijn beurt weer ernstige hoofdpijn heeft veroorzaakt voor technische en technische bedrijven, omdat cookies van derden doorgaans worden gebruikt voor het bijhouden van bezoekers en het verzamelen van bezoekersgegevens. Apple is nu onderweg om beperkingen en beperkingen in te stellen voor het gebruik van cookies van eerste partijen in Safari.

Deze versies van ITP bevatten de volgende beperkingen:

| Versie | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Er zijn gemaximeerde clientcookies die met de API `document.cookie` op de browser worden geplaatst bij een vervaldatum van zeven dagen.<br>Release van 21 februari 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Verminderde de 7-daagse vervalsingsdop drastisch tot één dag.<br>Release van 24 april 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Er zijn verschillende tijdelijke oplossingen verwijderd, zoals het gebruik van localStorage of het gebruik van JavaScript `Document.referrer property`.<br>Release van 23 september 2019.<br>De CNAME-camouflage-verdedigingsfunctie van ITP die in Safari 14, macOS Big Sur, Catalina, Mojave, iOS 14 en iPadOS 14 is uitgebracht. Alle cookies die door een derde CNAME-camouflage HTTP-respons worden gemaakt, verlopen over zeven dagen.<br>Aankondigd op 12 november 2020. |

## Wat is de impact voor mij als Adobe [!DNL Target] klant? {#impact}

[!DNL Target] biedt JavaScript-bibliotheken waarmee u inhoud op uw pagina&#39;s kunt implementeren zodat u uw bezoekers in real-time kunt personaliseren.  [!DNL Target] Er zijn drie Target JavaScript-bibliotheken op .js 1.x, op.js 2.x die client-side [!DNL Target] cookies plaatsen in de browsers van uw bezoekers via de `document.cookie` API. Als gevolg hiervan worden cookies van [!DNL Target] beïnvloed door ITP 2.1, 2.2 en 2.3 van Apple en verlopen deze na zeven dagen (met ITP 2.1) en na één dag (met ITP 2.2 en ITP 2.3).

Apple ITP 2.x beïnvloedt [!DNL Target] op de volgende gebieden:

| Gevolgen | Details |
| --- | --- |
| Mogelijke toename van het aantal unieke bezoekers | Omdat het afloopvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), kan het zijn dat er een toename is van unieke bezoekers die uit Safari-browsers komen. Als uw bezoekers uw domein na zeven dagen (ITP 2.1) of één dag (ITP 2.2 en ITP 2.3) terugkeren, [!DNL Target] wordt gedwongen om een nieuw [!DNL Target] koekje op uw domein in plaats van het verlopen koekje te plaatsen. Het nieuwe [!DNL Target] koekje vertaalt aan een nieuwe unieke bezoeker alhoewel de gebruiker het zelfde is. |
| Verlaagde terugzoekperiodes voor [!DNL Target] activiteiten | Bezoekersprofielen voor [!DNL Target] activiteiten kunnen een kortere terugzoekperiode voor beslissing hebben. [!DNL Target] cookies worden gebruikt om een bezoeker te identificeren en gebruikersprofielkenmerken op te slaan voor personalisatie. Aangezien [!DNL Target] cookies na zeven dagen (ITP 2.1) of één dag (ITP 2.2 en 2.3) in Safari kunnen worden verlopen, kunnen de gegevens van het gebruikersprofiel die aan het leeggemaakte [!DNL Target] cookie waren gekoppeld, niet worden gebruikt voor besluitvorming. |
| Profielscripts gebaseerd op 3rdPartyID | Aangezien het verloopvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), zullen [profielscripts](/help/c-target/c-visitor-profile/profile-parameters.md) op basis van het cookie 3rdPartyID niet meer werken bij het verlopen. |
| URL&#39;s met kwaliteitscontrole/voorvertoning op iOS-apparaten | Omdat het vervalvenster wordt geplaatst aan zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), [QA/Voorproef URLs](/help/c-activities/c-activity-qa/activity-qa.md) zal ophouden werkend bij afloop omdat URLs op het cookie 3rdPartyID gebaseerd is. |

## Heeft mijn huidige implementatie van [!DNL Target] gevolgen?

Als u naast de JavaScript-bibliotheek [!DNL Target] ook de Experience Cloud-id (ECID) gebruikt, wordt de implementatie beïnvloed op de manieren die in dit artikel worden vermeld: [Safari ITP 2.1 Impact op klanten van Adobe Experience Cloud en Experience Platform](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).
