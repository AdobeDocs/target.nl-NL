---
keywords: apple;ITP;intelligent tracking prevention
description: Informatie over Adobe Target-ondersteuning voor ITP 2.x van Apple via de Experience Cloud ID-bibliotheek 4.3.
title: Adobe Target- en Apple ITP-ondersteuning
feature: privacy and security
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) is het initiatief van Apple om de privacy van Safari-gebruikers te beschermen. De eerste release van ITP, die in 2017 plaatsvond, was gericht op het gebruik van cookies van derden. In feite heeft Apple alle cookies van derden geblokkeerd, wat op zijn beurt weer ernstige hoofdpijn heeft veroorzaakt voor technische en technische bedrijven, omdat cookies van derden doorgaans worden gebruikt voor het bijhouden van bezoekers en het verzamelen van bezoekersgegevens. Apple is nu onderweg om beperkingen en beperkingen in te stellen voor het gebruik van cookies van eerste partijen in Safari.

Deze versies van ITP bevatten de volgende beperkingen:

| Versie | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Er zijn gemaximeerde clientcookies die met de API `document.cookie` op de browser worden geplaatst bij een vervaldatum van zeven dagen.<br>Release van 21 februari 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Verminderde de 7-daagse vervalsingsdop drastisch tot één dag.<br>Release van 24 april 2019. |
| [ITP 2.3](https://webkit.org/blog/9521/intelligent-tracking-prevention-2-3/) | Er zijn verschillende tijdelijke oplossingen verwijderd, zoals het gebruik van localStorage of het gebruik van JavaScript `Document.referrer property`.<br>Release van 23 september 2019. |

## Wat is de impact voor mij als Adobe Target-klant? {#impact}

[!DNL Target] biedt JavaScript-bibliotheken waarmee u inhoud op uw pagina&#39;s kunt implementeren zodat u uw bezoekers in real-time kunt personaliseren.  [!DNL Target] Er zijn drie JavaScript-doelbibliotheken ([at.js 1.x, at.js 2.x](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) en [mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) die cookies aan de clientzijde [!DNL Target] via de `document.cookie`-API in de browsers van uw bezoekers plaatsen. Als gevolg hiervan worden [!DNL Target] cookies beïnvloed door ITP 2.x van Apple en verlopen deze na zeven dagen (met ITP 2.1) en na één dag (met ITP 2.2 en ITP 2.3).

Apple ITP 2.x beïnvloedt [!DNL Target] op de volgende gebieden:

| Gevolgen | Details |
| --- | --- |
| Mogelijke toename van het aantal unieke bezoekers | Omdat het afloopvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), kan het zijn dat er een toename is van unieke bezoekers die uit Safari-browsers komen. Als uw bezoekers uw domein na zeven dagen (ITP 2.1) of één dag (ITP 2.2 en ITP 2.3) terugkeren, [!DNL Target] wordt gedwongen om een nieuw [!DNL Target] koekje op uw domein in plaats van het verlopen koekje te plaatsen. Het nieuwe [!DNL Target] koekje vertaalt aan een nieuwe unieke bezoeker alhoewel de gebruiker het zelfde is. |
| Verlaagde terugzoekperiodes voor [!DNL Target] activiteiten | Bezoekersprofielen voor [!DNL Target] activiteiten kunnen een kortere terugzoekperiode voor beslissing hebben. [!DNL Target] cookies worden gebruikt om een bezoeker te identificeren en gebruikersprofielkenmerken op te slaan voor personalisatie. Aangezien [!DNL Target] cookies na zeven dagen (ITP 2.1) of één dag (ITP 2.2 en 2.3) in Safari kunnen worden verlopen, kunnen de gegevens van het gebruikersprofiel die aan het leeggemaakte [!DNL Target] cookie waren gekoppeld, niet worden gebruikt voor besluitvorming. |
| Profielscripts gebaseerd op 3rdPartyID | Aangezien het verloopvenster wordt ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), zullen [profielscripts](/help/c-target/c-visitor-profile/profile-parameters.md) op basis van het cookie 3rdPartyID niet meer werken bij het verlopen. |
| URL&#39;s met kwaliteitscontrole/voorvertoning op iOS-apparaten | Omdat het vervalvenster wordt geplaatst aan zeven dagen (met ITP 2.1) en één dag (met ITP 2.2 en ITP 2.3), [QA/Voorproef URLs](/help/c-activities/c-activity-qa/activity-qa.md) zal ophouden werkend bij afloop omdat URLs op het cookie 3rdPartyID gebaseerd is. |

## Heeft mijn huidige implementatie van [!DNL Target] gevolgen?

Navigeer in een Safari-browser naar de website waarop u een JavaScript-bibliotheek hebt. [!DNL Target] Als u een [!DNL Target] koekje ziet dat in de context van een CNAME, zoals `analytics.company.com` wordt geplaatst, dan wordt u niet beïnvloed door ITP 2.x.

Als u de Experience Cloud-id (ECID)-bibliotheek gebruikt in aanvulling op de JavaScript-doelbibliotheek, wordt de implementatie beïnvloed op de manieren die in dit artikel worden vermeld: [Safari ITP 2.1 Impact op klanten van Adobe Experience Cloud en Experience Platform](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac).

## Hoe kan ik het effect van toekomstige versies ITP 2.x aan Doel verlichten?

Om het effect van toekomstige versies ITP 2.x aan Doel te verlichten, voltooi de volgende taken:

1. Implementeer de Experience Cloud-id (ECID)-bibliotheek op uw pagina&#39;s.

   Met de ECID-bibliotheek kunnen mensen identificeren met Experience Cloud Core-oplossingen. Met de ECID-bibliotheek kunt u dezelfde sitebezoekers en hun gegevens identificeren in verschillende Experience Cloud-oplossingen door permanente en unieke id&#39;s toe te wijzen. De ECID-bibliotheek wordt regelmatig bijgewerkt om u te helpen eventuele ITP-gerelateerde wijzigingen die van invloed zijn op uw implementatie, te beperken.

   Voor ITP 2.x moet [ECID-bibliotheek 4.3.0+](https://experienceleague.adobe.com/docs/id-service/using/release-notes/release-notes.html) worden gebruikt voor mitigatie.

1. CNAME van Adobe en Inschrijven van het gebruik in het Beheerde Programma van het Certificaat van Adobe Analytics.

   Nadat u de ECID-bibliotheek 4.3.0+ hebt geïnstalleerd, kunt u de CNAME van Adobe Analytics en het Beheerde Certificaatprogramma gebruiken. Met dit programma kunt u gratis een eersteklas certificaat voor cookies van andere bedrijven implementeren. De hefboomwerking CNAME zal klanten [!DNL Target] helpen de gevolgen van ITP 2.x verlichten.

   Als u geen gebruik maakt van CNAME, kunt u het proces starten door met uw accountvertegenwoordiger te spreken en u in te schrijven in het [Adobe Beheerde certificaatprogramma](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Nadat u een bibliotheek van het Doel JavaScript samen met de bibliotheek ECID v4.3.0+ opstelt en in het Adobe Beheerde Programma van het Certificaat aan hefboomwerking CNAME inschrijft, zult u een robuust en op lange termijn matigingsplan voor op ITP betrekking hebbende veranderingen hebben.

Aangezien de branche vooruitgang boekt bij het creëren van een veiliger web voor consumenten, is [!DNL Adobe Target] absoluut gecommitteerd aan het bieden van persoonlijke ervaringen terwijl het voldoen aan en het overtreffen van de privacyverwachtingen van bezoekers. [!DNL Adobe Target] heeft al steun aangekondigd voor het SameSite Chrome- [beleid van ](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Google naast ondersteuning voor het ITP 2.x van Apple.

Aangezien het beleid zich blijft ontwikkelen om onze consumenten te beschermen, zal [!DNL Adobe] deze initiatieven ook blijven steunen in [!DNL Target], terwijl het helpen van onze klanten de best-in-klasse gepersonaliseerde ervaringen verstrekken.
