---
keywords: Overzicht en referentie
description: Leer hoe u Adobe gebruikt [!DNL Target] met Adobe Campaign om e-mailinhoud te optimaliseren.
title: Hoe integreer ik [!DNL Target] met Adobe Campaign?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Integreren [!DNL Target] met Adobe Campaign

Gebruiken [!DNL Target] with [!DNL Adobe Campaign] om e-mailinhoud te optimaliseren.

Als u uw e-mailinhoud wilt optimaliseren, kunt u een omleidingsvoorstel maken in [!DNL Target]en vervolgens gebruiken [!DNL Adobe Campaign] om de e-mailaanbiedingen te beheren. U kunt bijvoorbeeld verschillende aanbiedingen voor mannelijke en vrouwelijke ontvangers weergeven.

De integratie vindt plaats wanneer de e-mail wordt geopend. Wanneer de klant de e-mail opent, wordt een vraag gemaakt aan [!DNL Target] en wordt er een dynamische versie van de inhoud weergegeven. De inhoud bestaat uit een statische afbeelding die door alle browsers wordt ondersteund. [!DNL Target] volgt de reactie op het aanbod op publiek- of sessieniveau en dat gegevens beschikbaar zijn in [!DNL Target] rapporten.

[!DNL Target] U kunt de volgende gegevens bijhouden:

* Gebruikersagent
* IP-adres
* Geografische locatie
* Segment dat is gekoppeld aan de id van de bezoeker in [!DNL Target] (onder voorbehoud van wettelijke goedkeuring)
* Gegevens van [!DNL Campaign] Datamart

Er zijn verschillende beperkingen:

* Omdat alleen een afbeelding kan worden gebruikt, kan de inhoud niet worden gepersonaliseerd.
* Tekstspatiëring wordt niet geconsolideerd in [!DNL Adobe Campaign].
* Geen uniforme gebruikerservaring.

Beide gebruiken [!DNL Target] en [!DNL Campaign] verschillende onderdelen van de integratie instellen:

* De onbewerkte doos en de ervaring in [!DNL Target]

>[!NOTE]
>
>Bij gebruik van een rawbox en [!DNL Target], zie de belangrijke veiligheidskennisgeving onder [Creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel te verzenden](/help/main/administrating-target/hosts.md#allowlist).

* De levering in [!DNL Campaign]

## Voordat u begint {#section_FF19BF1BCA064260930BF6C141313B0E}

Wat u moet weten voordat u gaat gebruiken [!DNL Adobe Campaign] als u uw beoogde e-mailaanbiedingen wilt instellen, stelt u het volgende in [!DNL Target]:

* Twee of meer [!DNL Target] omleiding van aanbiedingen

   Zie [Omleidingsvoorstel maken](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* A [!DNL Target] activiteit met een ervaring voor elke aanbieding en de gewenste [succesmetrisch](/help/main/c-activities/r-success-metrics/success-metrics.md).

   Zie [Omleiden naar een URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

De activiteit starten in [!DNL Target] voordat u de [!DNL Campaign] deel van de integratie.

## Inclusief een [!DNL Target] aanbieden in een [!DNL Adobe Campaign] email {#section_B201BBE27A704E18AF0D553F35695837}

1. Een e-mail maken in [!DNL Adobe Campaign].
1. Klik in de e-maileigenschappen op **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]**.
1. Selecteer de standaardafbeelding in de gedeelde elementen.
1. Geef de locatie op (rawbox).
1. Voeg andere beslissingsparameters toe, zoals het geslacht van de ontvanger.
1. Geef een voorvertoning van de e-mail weer en selecteer ten minste één ontvanger voor elke aanbieding (in dit geval een man en een vrouw).
1. In [!DNL Campaign], de [!DNL Target] De server van de rand u gebruikt om de activiteit en de naam van de huurder te controleren.
1. Geef de externe account op die wordt gebruikt voor de [!DNL Adobe Experience Cloud] zodat u toegang hebt tot de bronnen in het dialoogvenster [!DNL Experience Cloud].

Raadpleeg voor meer informatie de [!DNL Adobe Campaign] documentatie.

## Video: Integreren [!DNL Target] with [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
