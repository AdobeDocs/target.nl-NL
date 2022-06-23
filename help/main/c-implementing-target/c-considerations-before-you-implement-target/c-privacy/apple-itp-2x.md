---
keywords: appel;ITP;Intelligente traceringspreventie;Ervaar wolk id;ecid;itp
description: Meer informatie over Adobe [!DNL Target] en de gevolgen van het Apple Intelligent Tracking Prevention (ITP)-initiatief ter bescherming van de privacy van Safari-gebruikers.
title: Hoe werkt [!DNL Target] Apple ITP-ondersteuning afhandelen?
feature: Privacy & Security
role: Developer
exl-id: 05a62be5-ccfb-4d5c-b511-35023b95e567
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) is het initiatief van Apple om de privacy van Safari-gebruikers te beschermen. De eerste release van ITP, die in 2017 plaatsvond, was gericht op het gebruik van cookies van derden. Apple heeft namelijk alle cookies van derden geblokkeerd, wat op zijn beurt weer ernstige hoofdpijn heeft veroorzaakt voor technische en technische bedrijven, omdat cookies van derden over het algemeen worden gebruikt voor het bijhouden van bezoekers en het verzamelen van bezoekersgegevens. Apple is nu op weg om beperkingen en beperkingen in te stellen voor het gebruik van cookies van eerste partijen in Safari.

Deze versies van ITP bevatten de volgende beperkingen:

| Versie | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Gekoppelde clientcookies die met de `document.cookie` API tot een vervaldatum van zeven dagen.<br>Release van 21 februari 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Verminderde de 7-daagse vervalsingsdop drastisch tot één dag.<br>Release van 24 april 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Verschillende hindernissen zijn geëlimineerd, zoals het gebruik van localStorage of het gebruik van JavaScript `Document.referrer property`.<br>Release van 23 september 2019.<br>De CNAME-camouflage-verdedigingsfunctie van ITP, uitgebracht in Safari 14, macOS Big Sur, Catalina, Mojave, iOS 14 en iPad OS 14. Alle cookies die door een derde CNAME-camouflage HTTP-respons worden gemaakt, verlopen over zeven dagen.<br>Aankondigd op 12 november 2020. |

## Wat is de impact voor mij als Adobe? [!DNL Target] klant? {#impact}

[!DNL Target] biedt JavaScript-bibliotheken die u op uw pagina&#39;s kunt implementeren, zodat [!DNL Target] kan uw bezoekers in real time personaliseren. Er zijn drie Target JavaScript-bibliotheken in .js 1.x, at.js 2.x die client-side plaatsen [!DNL Target] cookies in de browsers van uw bezoekers via de `document.cookie` API. Dientengevolge [!DNL Target] cookies worden beïnvloed door ITP 2.1, 2.2 en 2.3 van Apple en verlopen na zeven dagen (met ITP 2.1) en na één dag (met ITP 2.2 en ITP 2.3).

Apple ITP 2.x-effecten [!DNL Target] op de volgende gebieden:

| Gevolgen | Details |
| --- | --- |
| Mogelijke toename van het aantal unieke bezoekers | Omdat het afloopvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), kan het zijn dat er een toename is van unieke bezoekers die uit Safari-browsers komen. Als uw bezoekers uw domein na zeven dagen (ITP 2.1) of één dag (ITP 2.2 en ITP 2.3) terugkeren, [!DNL Target] is gedwongen een nieuwe [!DNL Target] cookie op uw domein in plaats van de verlopen cookie. De nieuwe [!DNL Target] cookie wordt omgezet naar een nieuwe unieke bezoeker, ook al is de gebruiker hetzelfde. |
| Verlaagde terugzoekperiodes voor [!DNL Target] activiteiten | Bezoekersprofielen voor [!DNL Target] de activiteiten kunnen een kortere terugkijkperiode voor besluitvorming hebben. [!DNL Target] cookies worden gebruikt om een bezoeker te identificeren en gebruikersprofielkenmerken op te slaan voor personalisatie. Aangezien [!DNL Target] cookies kunnen op Safari verlopen na zeven dagen (ITP 2.1) of één dag (ITP 2.2 en 2.3), de gebruikersprofielgegevens die aan het leeggemaakte product waren gekoppeld [!DNL Target] cookie kan niet worden gebruikt voor de besluitvorming. |
| Profielscripts gebaseerd op 3rdPartyID | Aangezien het vervalvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), [profielscripts](/help/main/c-target/c-visitor-profile/profile-parameters.md) op basis van het cookie 3rdPartyID werkt niet meer na afloop. |
| URL&#39;s met kwaliteitscontrole/voorvertoning op iOS-apparaten | Aangezien het vervalvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), [URL&#39;s voor kwaliteitscontrole/voorvertoning](/help/main/c-activities/c-activity-qa/activity-qa.md) werkt niet meer nadat de URL is verlopen omdat de URL&#39;s zijn gebaseerd op het cookie 3rdPartyID. |

## Is mijn huidige implementatie van [!DNL Target] beïnvloed?

Als u naast de Experience Cloud-id (ECID) ook de bibliotheek gebruikt [!DNL Target] JavaScript-bibliotheek, wordt uw implementatie beïnvloed op de manieren die in dit artikel worden vermeld: [Safari ITP 2.1 Impact op klanten van Adobe Experience Cloud en Experience Platform](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).
