---
keywords: Overview and Reference
description: Gebruik Doel met Adobe Campagne om e-mailinhoud te optimaliseren.
title: Doel integreren met Adobe-campagne
topic: Standard
uuid: 1a5b70e6-d501-4b52-bec8-4ae2c419d331
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Doel integreren met Adobe-campagne{#integrate-target-with-adobe-campaign}

Gebruik Doel met Adobe Campagne om e-mailinhoud te optimaliseren.

Als u uw e-mailinhoud wilt optimaliseren, bijvoorbeeld om verschillende aanbiedingen voor mannelijke en vrouwelijke ontvangers weer te geven, kunt u een omleidingsaanbieding maken in Target en vervolgens de e-mailaanbiedingen beheren met Adobe Campaign.

De integratie vindt plaats wanneer de e-mail wordt geopend. Wanneer de klant de e-mail opent, wordt een vraag gemaakt aan Target en een dynamische versie van de inhoud verschijnt. De inhoud bestaat uit een statische afbeelding die door alle browsers wordt ondersteund. Het doel volgt de reactie op de aanbieding op het publiek of zittingsniveau en dat de gegevens in de rapporten van het Doel beschikbaar zijn.

Doel kan de volgende gegevens bijhouden:

* Gebruikersagent
* IP-adres
* Geografische locatie
* Segment dat aan de bezoekersidentiteitskaart in Doel (onderworpen aan wettelijke goedkeuring) wordt geassocieerd
* Gegevens van campagne Datamart

Er zijn verschillende beperkingen:

* Omdat alleen een afbeelding kan worden gebruikt, kan de inhoud niet worden gepersonaliseerd.
* Tekstspatiëring is niet geconsolideerd in Adobe-campagne.
* Geen uniforme gebruikerservaring.

   U moet zowel Doel als Campagne gebruiken om verschillende delen van de integratie te plaatsen:

   * De box en de ervaring in Doel
   * De levering in Campagne

## Voordat u begint {#section_FF19BF1BCA064260930BF6C141313B0E}

Voordat u Adobe Campaign gebruikt om uw beoogde e-mailaanbiedingen in te stellen, stelt u het volgende in Target in:

* Twee of meer aanbiedingen voor omleiding van Target

   Zie [Omleidingsvoorstel](/help/c-experiences/c-manage-content/offer-redirect.md)maken.
* Een activiteit van het Doel met een ervaring voor elke aanbieding en gewenste [succes metrisch](/help/c-activities/r-success-metrics/success-metrics.md).

   Zie [Omleiden naar een URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Start de activiteit in Doel voordat u het onderdeel Campagne van de integratie instelt.

## Een doelaanbieding opnemen in een e-mailbericht voor een Adobe-campagne {#section_B201BBE27A704E18AF0D553F35695837}

1. Maak een e-mail in Adobe Campaign.
1. Klik in de e-maileigenschappen op **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]**.
1. Selecteer de standaardafbeelding in de gedeelde elementen.
1. Geef de locatie op (rawbox).
1. Voeg andere beslissingsparameters toe, zoals het geslacht van de ontvanger.
1. Geef een voorvertoning van de e-mail weer en selecteer ten minste één ontvanger voor elke aanbieding (in dit geval een man en een vrouw).
1. In Campagne, bepaal de server van de Rand van het Doel u gebruikt om de activiteit en de naam van de huurder te controleren.
1. Geef het externe account op dat wordt gebruikt voor de Experience Cloud, zodat u toegang kunt krijgen tot de bronnen in de Experience Cloud.

Raadpleeg de documentatie bij Adobe Campagne voor meer informatie.
