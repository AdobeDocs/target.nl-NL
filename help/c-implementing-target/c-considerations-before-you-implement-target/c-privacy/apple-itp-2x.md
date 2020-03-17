---
keywords: apple;ITP;intelligent tracking prevention
description: Informatie over ondersteuning van Adobe Target voor ITP 2.1 en ITP 2.2 van Apple via de Experience Cloud ID-bibliotheek 4.3.
title: Ondersteuning voor Adobe Target en Apple ITP
subtopic: Getting Started
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Apple Intelligent Tracking Prevention (ITP) 2.x

Intelligent Tracking Prevention (ITP) is het initiatief van Apple om de privacy van Safari-gebruikers te beschermen. De eerste release van ITP, die in 2017 plaatsvond, was gericht op het gebruik van cookies van derden. In feite heeft Apple alle cookies van derden geblokkeerd, wat op zijn beurt weer ernstige hoofdpijn heeft veroorzaakt voor technische en technische bedrijven, omdat cookies van derden doorgaans worden gebruikt voor het bijhouden van bezoekers en het verzamelen van bezoekersgegevens. Apple is nu onderweg om beperkingen en beperkingen in te stellen voor het gebruik van cookies van eerste partijen in Safari.

Deze versies van ITP bevatten de volgende beperkingen:

| Versie | Details |
| --- | --- |
| [ITP 2.1](https://webkit.org/blog/8613/intelligent-tracking-prevention-2-1/) | Aangewezen cliënt-zijkoekjes die op browser gebruikend `document.cookie` API aan een vervaldatum van zeven dagen worden geplaatst.<br>Release van 21 februari 2019. |
| [ITP 2.2](https://webkit.org/blog/8828/intelligent-tracking-prevention-2-2/) | Verminderde de 7-daagse vervalsingsdop drastisch tot één dag.<br>Release van 24 april 2019. |

## Wat is de invloed op mij als Adobe Target-klant?

[!DNL Target] biedt JavaScript-bibliotheken waarmee u inhoud op uw pagina&#39;s kunt implementeren, zodat uw bezoekers in real-time een persoonlijk tintje [!DNL Target] kunnen geven. Er zijn drie Target JavaScript-bibliotheken ([at.js 1.*x* en at.js 2.*x *](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)en[mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)) die[!DNL Target]cookies aan de clientzijde via de`document.cookie`API in de browsers van uw bezoekers plaatsen. Als gevolg hiervan worden[!DNL Target]cookies beïnvloed door ITP 2.1 en 2.2 van Apple en verlopen ze na zeven dagen (met ITP 2.1) en na één dag (met ITP 2.2).

De invloed van Apple ITP 2.1 en 2.1 [!DNL Target] op de volgende gebieden:

| Gevolgen | Details |
| --- | --- |
| Mogelijke toename van het aantal unieke bezoekers | Aangezien het verloopvenster is ingesteld op zeven dagen (met ITP 2.1) en één dag (met ITP 2.2), kan het zijn dat er een toename is van unieke bezoekers die uit Safari-browsers komen. Als uw bezoekers uw domein na zeven dagen (ITP 2.1) of één dag (ITP 2.2) terugkeren, [!DNL Target] wordt gedwongen om een nieuwe [!DNL Target] koekje op uw domein in plaats van het verlopen koekje te plaatsen. Het nieuwe [!DNL Target] cookie wordt omgezet naar een nieuwe unieke bezoeker, ook al is de gebruiker hetzelfde. |
| Verlaagde terugzoektijden voor [!DNL Target] activiteiten | Bezoekersprofielen voor [!DNL Target] activiteiten hebben mogelijk een kortere terugzoekperiode voor beslissingen. [!DNL Target] cookies worden gebruikt om een bezoeker te identificeren en gebruikersprofielkenmerken op te slaan voor personalisatie. Aangezien [!DNL Target] cookies na zeven dagen (ITP 2.1) of één dag (ITP 2.2) in Safari kunnen verlopen, kunnen de gegevens van het gebruikersprofiel die aan het gezuiverde [!DNL Target] cookie waren gekoppeld, niet worden gebruikt voor de besluitvorming. |

## Is mijn huidige implementatie van [!DNL Target] invloed?

Navigeer in een Safari-browser naar uw website waarop u een [!DNL Target] JavaScript-bibliotheek hebt. Als u een [!DNL Target] koekjesreeks in de context van een CNAME ziet, zoals `analytics.company.com`, dan wordt u niet beïnvloed door ITP 2.1 of 2.2.

Als u naast de doelJavaScript-bibliotheek ook de ECID-bibliotheek (Experience Cloud ID) gebruikt, wordt de implementatie beïnvloed op de manieren die in dit artikel worden vermeld: [Safari ITP 2.1 Impact op klanten](https://medium.com/adobetech/safari-itp-2-1-impact-on-adobe-experience-cloud-customers-9439cecb55ac)van het Adobe Experience Cloud en Experience Platform.

## Hoe kan ik het effect van ITP 2.1, ITP 2.2, en toekomstige versies ITP aan [!DNL Target]verlichten?

Om het effect van ITP 2.1, ITP 2.2, en toekomstige versies ITP te verlichten aan [!DNL Target], voltooi de volgende taken:

1. Gebruik de ECID-bibliotheek (Experience Cloud ID) op uw pagina&#39;s.

   Met de ECID-bibliotheek kunnen mensen identificeren op basis van Cloud Core-oplossingen. Met de ECID-bibliotheek kunt u dezelfde sitebezoekers en hun gegevens identificeren in verschillende Experience Cloud-oplossingen door permanente en unieke id&#39;s toe te wijzen. De ECID-bibliotheek wordt regelmatig bijgewerkt om u te helpen eventuele ITP-gerelateerde wijzigingen die van invloed zijn op uw implementatie, te beperken.

   Voor ITP 2.1 en ITP 2.2, [ECID bibliotheek 4.3.0+](https://docs.adobe.com/content/help/en/id-service/using/release-notes/release-notes.html) moet voor matiging worden gebruikt.

1. Gebruik de NAAM en de Inschrijving van Adobe in het Beheerde CertificaatProgramma van de Analyse van Adobe.

   Nadat u de ECID-bibliotheek 4.3.0+ hebt geïnstalleerd, kunt u de CNAME en het Beheerde certificaatprogramma van Adobe Analytics gebruiken. Met dit programma kunt u gratis een eersteklas certificaat voor cookies van andere bedrijven implementeren. Leveraging CNAME zal [!DNL Target] klanten helpen het effect van ITP 2.1 en ITP 2.2 verlichten.

   Als u CNAME niet gebruikt, kunt u het proces starten door met uw accountvertegenwoordiger te spreken en u in te schrijven voor het [Adobe Managed Certificate Program](https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-first-party.html#adobe-managed-certificate-program).

Nadat u een JavaScript-bibliotheek van het Doel in combinatie met de ECID-bibliotheek v4.3.0+ hebt geïmplementeerd en u in het door Adobe beheerde certificaatprogramma hebt ingeschreven om gebruik te maken van CNAME, beschikt u over een robuust en langetermijnplan voor mitigatie van ITP-gerelateerde wijzigingen.

Aangezien de industrie zich inzet voor het creëren van een veiliger web voor consumenten, [!DNL Adobe Target] is zij absoluut gecommitteerd aan het aanbieden van persoonlijke ervaringen en het overtreffen van de privacyverwachtingen van bezoekers. [!DNL Adobe Target] heeft al steun aangekondigd voor het SameSite Chrome-beleid [van](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md) Google naast ondersteuning voor ITP 2.1 en ITP 2.2 van Apple.

Naarmate het beleid zich blijft ontwikkelen om onze consumenten te beschermen, [!DNL Adobe] zullen deze initiatieven ook in de toekomst worden ondersteund [!DNL Target], terwijl onze klanten tegelijkertijd de best-in-class gepersonaliseerde ervaringen kunnen bieden.
