---
keywords: privacy;ip address;geosegmentation;opt out;optout;opt-out;data privacy;government regulations;regulations;gdpr;ccpa
description: Adobe Target heeft processen en instellingen ingeschakeld waarmee u Target kunt gebruiken in overeenstemming met de toepasselijke wetgeving inzake privacy van gegevens.
title: Privacy
feature: privacy and security
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---


# Privacy{#privacy}

Adobe Target heeft processen en instellingen ingeschakeld waarmee u Target kunt gebruiken in overeenstemming met de toepasselijke wetgeving inzake privacy van gegevens.

## Verzameling van IP-adressen {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

Het IP-adres van een bezoeker van uw website wordt naar een Adobe Data Processing Center (DPC) verzonden. Afhankelijk van de netwerkconfiguratie voor de bezoeker, vertegenwoordigt het IP adres niet noodzakelijk het IP adres van de computer van de bezoeker. Bijvoorbeeld, zou het IP adres het externe IP adres van een firewall van het Vertaal adres van het Netwerk (NATIONAAL), de volmacht van HTTP, of de gateway van Internet kunnen zijn. Het doel slaat geen IP adressen van de gebruiker of om het even welke Persoonlijk Identificeerbare Informatie (PII) op. IP de adressen worden gebruikt slechts door Doel voor de duur van de zitting (in geheugen, nooit voortgeduurd).

## Vervanging van laatste octet van IP adressen {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe heeft een nieuwe &quot;privacy-door-ontwerp&quot;instelling ontwikkeld die door de Zorg van de Cliënt van Adobe voor Adobe Target kan worden toegelaten. Wanneer dit het plaatsen wordt toegelaten, wordt het laatste octet (het laatste gedeelte) van het IP adres onmiddellijk verborgen wanneer het IP adres door Adobe wordt verzameld. Deze anonymization wordt uitgevoerd voorafgaand aan om het even welke verwerking van het IP adres, met inbegrip van vóór een facultatieve geo-raadpleging van het IP adres.

Wanneer deze eigenschap wordt toegelaten, wordt het IP adres gemaakt voldoende anoniem zodat is het niet meer identificeerbaar als persoonlijke informatie. Als gevolg hiervan kan Adobe Target worden gebruikt in overeenstemming met de wetgeving inzake de privacy van gegevens in landen die het verzamelen van persoonsgegevens niet toestaan. Het verkrijgen van informatie op het niveau van de stad zal waarschijnlijk aanzienlijk worden beïnvloed door de verduistering van het IP-adres. Het verkrijgen van informatie op regionaal en nationaal niveau mag slechts enigszins worden beïnvloed.

De volgende instellingen zijn beschikbaar:

* Geen verwarring: Het doel verbergt geen deel van het IP adres.
* Laatste octet: Het doel verbergt het laatste octet van het IP adres.
* Volledige IP: Het doel verbergt het volledige IP adres.

Het doel ontvangt het volledige IP adres en verduistert het (als reeks aan Laatste octet of Volledige IP) zoals gespecificeerd. Het doel houdt dan het verduisterde IP adres in geheugen voor de duur van de zitting.

>[!NOTE]
>
>[De Cliënt van de Adobe van het contact ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Caret om te bepalen welke het plaatsen u momenteel gebruikt of om de IP verduisteringseigenschap toe te laten.

## GeoSegmentation {#section_BB69F96559BD44BDA4177537C4A5345A}

Als u de vervanging van het laatste octet van het IP adres toelaat, kunnen de resterende waarden van het IP adres worden geanalyseerd gebruikend rapporten in Adobe Target. Als het laatste octet van het IP adres niet verduisterd is, dan kan het volledige IP adres in Adobe Target worden geanalyseerd. Met de functie GeoSegmentation kunt u de locatie van de bezoeker per geografisch gebied in kaart brengen. GeoSegmentation-gegevens zijn alleen granulair voor het niveau van de stad of postcode, en niet voor het individuele niveau.

Als IP de adressen volledig verduisterd zijn, is GeoSegmentation en geo het richten niet beschikbaar.

## Koppeling {#section_E7A62B7B99C94B3A806CB262D16E27FC} uitschakelen

U kunt een koppeling om te weigeren toevoegen aan uw sites zodat bezoekers zich kunnen afmelden voor alle aftellingen en de levering van inhoud.

1. Voeg de volgende koppeling toe aan uw site:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`
1. Vervang de `clientcode`-tekst met uw clientcode en voeg de tekst of afbeelding toe die u wilt koppelen aan de URL voor niet-deelname.

Elke bezoeker die op deze koppeling klikt, wordt niet opgenomen in een box-aanvraag die vanaf zijn browsersessies wordt aangeroepen totdat hij of zij zijn of haar cookies verwijdert, of gedurende twee jaar, afhankelijk van welke eerst aankomt. Dit werkt door een koekje voor de bezoeker te plaatsen genoemd `disableClient` in `clientcode.tt.omtrdc.net` domein.

Zelfs als u een eersteklas cookie-implementatie gebruikt, wordt de opgegeven opt-out ingesteld via een cookie van een andere fabrikant. Als de client alleen een eersteklas cookie gebruikt, controleert Target of een uitschakelcookie is ingesteld.

## Regels inzake privacy en gegevensbescherming

Zie [Privacy- en gegevensbeschermingsregels](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) voor informatie over de algemene gegevensbeschermingsverordening (GDPR) van de Europese Unie, de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten, en hoe deze regels van invloed zijn op uw organisatie en Adobe Target.
