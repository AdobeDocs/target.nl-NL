---
keywords: Overview and Reference
description: Gebruik Target met Adobe Campaign om e-mailinhoud te optimaliseren.
title: Target integreren met Adobe Campaign
topic: Standard
uuid: 1a5b70e6-d501-4b52-bec8-4ae2c419d331
translation-type: tm+mt
source-git-commit: c652be30b0dfede94457f402a8b540a35096bdb4
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---


# Target integreren met Adobe Campaign{#integrate-target-with-adobe-campaign}

Gebruik [!DNL Target] met [!DNL Adobe Campaign] om e-mailinhoud te optimaliseren.

Als u uw e-mailinhoud wilt optimaliseren, bijvoorbeeld om verschillende aanbiedingen voor mannelijke en vrouwelijke ontvangers weer te geven, kunt u een omleidingsvoorstel maken in [!DNL Target], en vervolgens de e-mailaanbiedingen [!DNL Adobe Campaign] beheren.

De integratie vindt plaats wanneer de e-mail wordt geopend. Wanneer de klant de e-mail opent, wordt een vraag gemaakt aan [!DNL Target] en een dynamische versie van de inhoud verschijnt. De inhoud bestaat uit een statische afbeelding die door alle browsers wordt ondersteund. [!DNL Target] volgt de reactie op het aanbod op publiek of sessieniveau en dat gegevens beschikbaar zijn in [!DNL Target] rapporten.

Target kan de volgende gegevens bijhouden:

* Gebruikersagent
* IP-adres
* Geografische locatie
* Segment dat is gekoppeld aan de ID van de bezoeker in Target (onderworpen aan wettelijke goedkeuring)
* Gegevens van [!DNL Campaign] Datamart

Er zijn verschillende beperkingen:

* Omdat alleen een afbeelding kan worden gebruikt, kan de inhoud niet worden gepersonaliseerd.
* Tekstspatiëring wordt niet geconsolideerd in [!DNL Adobe Campaign].
* Geen uniforme gebruikerservaring.

   U moet zowel [!DNL Target] als [!DNL Campaign] aan opstelling verschillende delen van de integratie gebruiken:

   * De doos en de ervaring in [!DNL Target]
   >[!NOTE]
   >
   >Wanneer het gebruiken van een doos en [!DNL Target], zie de belangrijke veiligheidsmededeling onder [Create allowlists die gastheren specificeren die worden gemachtigd om mbox vraag naar Target](/help/administrating-target/hosts.md#allowlist)te verzenden.

   * De levering in [!DNL Campaign]



## Voordat u begint {#section_FF19BF1BCA064260930BF6C141313B0E}

Voordat u uw beoogde e-mailaanbiedingen instelt, stelt u het volgende in [!DNL Adobe Campaign] [!DNL Target]:

* Twee of meer [!DNL Target] omleidingsaanbiedingen

   Zie [Omleidingsvoorstel](/help/c-experiences/c-manage-content/offer-redirect.md)maken.
* Een Target-activiteit met een ervaring voor elk aanbod en de gewenste [succesmaatstaf](/help/c-activities/r-success-metrics/success-metrics.md).

   Zie [Omleiden naar een URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Start de activiteit in [!DNL Target] voordat u het [!DNL Campaign] gedeelte van de integratie instelt.

## Een Target-voorstel opnemen in een Adobe Campaign-e-mail {#section_B201BBE27A704E18AF0D553F35695837}

1. Maak een e-mail in [!DNL Adobe Campaign].
1. Klik in de e-maileigenschappen op **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]**.
1. Selecteer de standaardafbeelding in de gedeelde elementen.
1. Geef de locatie op (rawbox).
1. Voeg andere beslissingsparameters toe, zoals het geslacht van de ontvanger.
1. Geef een voorvertoning van de e-mail weer en selecteer ten minste één ontvanger voor elke aanbieding (in dit geval een man en een vrouw).
1. In [!DNL Campaign], bepaal de server van de [!DNL Target] Rand u gebruikt om de activiteit en de naam van de huurder te controleren.
1. Geef de externe account op die voor de account wordt gebruikt, [!DNL Adobe Experience Cloud] zodat u toegang kunt krijgen tot de bronnen in de [!DNL Experience Cloud]account.

Raadpleeg de [!DNL Adobe Campaign] documentatie voor meer informatie.
