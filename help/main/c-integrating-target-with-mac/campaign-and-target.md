---
keywords: Overzicht en referentie
description: Leer hoe te om Adobe  [!DNL Target]  met Adobe Campaign te gebruiken om e-mailinhoud te optimaliseren.
title: Hoe integreer ik  [!DNL Target]  met Adobe Campaign?
feature: Integrations
exl-id: 605b8fe4-e32f-43bc-9131-245008b655e1
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# [!DNL Target] integreren met Adobe Campaign

Gebruik [!DNL Target] met [!DNL Adobe Campaign] om e-mailinhoud te optimaliseren.

Als u uw e-mailinhoud wilt optimaliseren, kunt u een omleidingsvoorstel maken in [!DNL Target] en vervolgens [!DNL Adobe Campaign] gebruiken om de e-mailaanbiedingen te beheren. U kunt bijvoorbeeld verschillende aanbiedingen voor mannelijke en vrouwelijke ontvangers weergeven.

De integratie vindt plaats wanneer de e-mail wordt geopend. Wanneer de klant het e-mailbericht opent, wordt [!DNL Target] aangeroepen en wordt een dynamische versie van de inhoud weergegeven. De inhoud bestaat uit een statische afbeelding die door alle browsers wordt ondersteund. [!DNL Target] volgt de reactie op de aanbieding op publiek- of sessieniveau en die gegevens zijn beschikbaar in [!DNL Target] -rapporten.

[!DNL Target] kan de volgende gegevens bijhouden:

* Gebruikersagent
* IP-adres
* Geografische locatie
* Segment dat is gekoppeld aan de id van de bezoeker in [!DNL Target] (mits deze wettelijk is goedgekeurd)
* Gegevens uit [!DNL Campaign] Datamart

Er zijn verschillende beperkingen:

* Omdat alleen een afbeelding kan worden gebruikt, kan de inhoud niet worden gepersonaliseerd.
* Tekstspatiëring wordt niet geconsolideerd in [!DNL Adobe Campaign] .
* Geen uniforme gebruikerservaring.

Gebruik zowel [!DNL Target] als [!DNL Campaign] om verschillende onderdelen van de integratie in te stellen:

* De onbewerkte doos en de ervaring in [!DNL Target]

>[!NOTE]
>
>Wanneer het gebruiken van een rawbox en [!DNL Target], zie de belangrijke veiligheidskennisgeving onder [&#x200B; lijsten van gewenste personen creëren die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel &#x200B;](/help/main/administrating-target/hosts.md#allowlist) te verzenden.

* De levering in [!DNL Campaign]

## Voordat u begint {#section_FF19BF1BCA064260930BF6C141313B0E}

Voordat u [!DNL Adobe Campaign] gebruikt om uw beoogde e-mailaanbiedingen in te stellen, stelt u het volgende in [!DNL Target] in:

* Twee of meer [!DNL Target] omleidingsvoorstellen

  Zie [&#x200B; opnieuw richten aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/offer-redirect.md).

* A [!DNL Target] activiteit met een ervaring voor elke aanbieding en het gewenste [&#x200B; metrische succes &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md).

  Zie [&#x200B; opnieuw richten aan een URL &#x200B;](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

Start de activiteit in [!DNL Target] voordat u het gedeelte [!DNL Campaign] van de integratie instelt.

## Een [!DNL Target] -aanbieding opnemen in een [!DNL Adobe Campaign] -e-mail {#section_B201BBE27A704E18AF0D553F35695837}

1. Maak een e-mail in [!DNL Adobe Campaign] .
1. Klik in de e-maileigenschappen op **[!UICONTROL Include]** > **[!UICONTROL Dynamic image served by Adobe Target]** .
1. Selecteer de standaardafbeelding in de gedeelde elementen.
1. Geef de locatie op (rawbox).
1. Voeg andere beslissingsparameters toe, zoals het geslacht van de ontvanger.
1. Geef een voorvertoning van de e-mail weer en selecteer ten minste één ontvanger voor elke aanbieding (in dit geval een man en een vrouw).
1. Definieer in [!DNL Campaign] de [!DNL Target] Edge-server die u gebruikt om de activiteit en de naam van de huurder te beheren.
1. Geef de externe account op die voor de [!DNL Adobe Experience Cloud] wordt gebruikt, zodat u toegang kunt krijgen tot de bronnen in de [!DNL Experience Cloud] .

Raadpleeg de documentatie van [!DNL Adobe Campaign] voor meer informatie.

## Video: [!DNL Target] integreren met [!DNL Campaign]

>[!VIDEO](https://video.tv.adobe.com/v/35149)
