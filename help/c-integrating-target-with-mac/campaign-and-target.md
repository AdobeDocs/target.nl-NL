---
keywords: Overzicht en referentie
description: Leer hoe u Adobe Target met Adobe Campaign kunt gebruiken om e-mailinhoud te optimaliseren.
title: Hoe integreer ik Doel met Adobe Campaign?
feature: Integrations
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# Doel integreren met Adobe Campaign{#integrate-target-with-adobe-campaign}

Gebruik [!DNL Target] met [!DNL Adobe Campaign] om e-mailinhoud te optimaliseren.

Als u uw e-mailinhoud wilt optimaliseren, bijvoorbeeld om verschillende aanbiedingen voor mannelijke en vrouwelijke ontvangers weer te geven, kunt u een omleidingsaanbieding maken in [!DNL Target] en vervolgens [!DNL Adobe Campaign] gebruiken om de e-mailaanbiedingen te beheren.

De integratie vindt plaats wanneer de e-mail wordt geopend. Wanneer de klant het e-mailbericht opent, wordt [!DNL Target] aangeroepen en wordt een dynamische versie van de inhoud weergegeven. De inhoud bestaat uit een statische afbeelding die door alle browsers wordt ondersteund. [!DNL Target] volgt de reactie op het aanbod op publiek of sessieniveau en dat gegevens beschikbaar zijn in  [!DNL Target] rapporten.

Doel kan de volgende gegevens bijhouden:

* Gebruikersagent
* IP-adres
* Geografische locatie
* Segment dat aan de bezoekersidentiteitskaart in Doel (onderworpen aan wettelijke goedkeuring) wordt geassocieerd
* Gegevens van [!DNL Campaign] Datamart

Er zijn verschillende beperkingen:

* Omdat alleen een afbeelding kan worden gebruikt, kan de inhoud niet worden gepersonaliseerd.
* Tekstspatiëring wordt niet geconsolideerd in [!DNL Adobe Campaign].
* Geen uniforme gebruikerservaring.

   U moet zowel [!DNL Target] als [!DNL Campaign] gebruiken om verschillende delen van de integratie in te stellen:

   * De rawbox en de ervaring in [!DNL Target]
   >[!NOTE]
   >
   >Wanneer het gebruiken van een rawbox en [!DNL Target], zie de belangrijke veiligheidskennisgeving onder [creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel te verzenden](/help/administrating-target/hosts.md#allowlist).

   * De levering in [!DNL Campaign]



## Voordat u {#section_FF19BF1BCA064260930BF6C141313B0E} begint

Voordat u [!DNL Adobe Campaign] gebruikt om uw beoogde e-mailaanbiedingen in te stellen, stelt u het volgende in [!DNL Target] in:

* Twee of meer [!DNL Target] omleidingsaanbiedingen

   Zie [Omleidingsaanbieding maken](/help/c-experiences/c-manage-content/offer-redirect.md).
* Een activiteit van het Doel met een ervaring voor elke aanbieding en gewenste [succes metrisch](/help/c-activities/r-success-metrics/success-metrics.md).

   Zie [Omleiden naar een URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md).

Start de activiteit in [!DNL Target] voordat u het [!DNL Campaign]-gedeelte van de integratie instelt.

## Een doelaanbieding opnemen in een Adobe Campaign-e-mail {#section_B201BBE27A704E18AF0D553F35695837}

1. Maak een e-mailbericht in [!DNL Adobe Campaign].
1. Klik in de e-maileigenschappen op **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]**.
1. Selecteer de standaardafbeelding in de gedeelde elementen.
1. Geef de locatie op (rawbox).
1. Voeg andere beslissingsparameters toe, zoals het geslacht van de ontvanger.
1. Geef een voorvertoning van de e-mail weer en selecteer ten minste één ontvanger voor elke aanbieding (in dit geval een man en een vrouw).
1. Definieer in [!DNL Campaign] de [!DNL Target] Edge-server die u gebruikt om de activiteit en de naam van de huurder te beheren.
1. Geef de externe account op die wordt gebruikt voor de [!DNL Adobe Experience Cloud], zodat u toegang kunt krijgen tot de bronnen in [!DNL Experience Cloud].

Raadpleeg de documentatie [!DNL Adobe Campaign] voor meer informatie.
