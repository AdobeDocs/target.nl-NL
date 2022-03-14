---
keywords: privacy;ip adres;geosegmentation;opt out;optout;opt-out;gegevensprivacy;overheidsverordeningen;gdpr;ccpa
description: Meer informatie over Adobe [!DNL Target] voldoet aan de toepasselijke wetgeving inzake gegevensprivacy, waaronder het verzamelen en afhandelen van IP-adressen, en instructies om te weigeren.
title: Hoe werkt [!DNL Target] Privacyproblemen verwerken?
feature: Privacy & Security
role: Developer
exl-id: fb632923-fa36-4553-88a6-f27860472eb6
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# Privacy

[!DNL Adobe Target] heeft processen en instellingen ingeschakeld waarmee u [!DNL Target] in overeenstemming met de toepasselijke wetgeving inzake gegevensbescherming.

## Verzameling van gebruiksgegevens

De individuele eigenschap-gebruik gegevens worden verzameld voor intern [!DNL Adobe] wordt nagegaan of [!DNL Target] functies worden uitgevoerd zoals bedoeld of om te bepalen welke functies onderbenut worden. Er worden verschillende metingen van de latentie verzameld om prestatieproblemen te verhelpen. Persoonlijke gegevens worden niet verzameld.

U kunt het rapporteren van gebruiksgegevens in onze SDK&#39;s uitschakelen door het instellen van `telemetryEnabled` naar false in de initialisatieopties voor de client. Zie voor meer informatie [telemetryEnabled in targetGlobalSettings](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#telemetry).

## Verzameling IP-adressen {#section_91BDB8105EBF4B85B7B8B8A14675AC85}

Het IP-adres van een bezoeker van uw website wordt naar een Adobe Data Processing Center (DPC) verzonden. Afhankelijk van de netwerkconfiguratie voor de bezoeker, vertegenwoordigt het IP adres niet noodzakelijk het IP adres van de computer van de bezoeker. Bijvoorbeeld, zou het IP adres het externe IP adres van een firewall van het Vertaal adres van het Netwerk (NATIONAAL), de volmacht van HTTP, of de gateway van Internet kunnen zijn. Het doel slaat geen IP adressen van de gebruiker of om het even welke Persoonlijk Identificeerbare Informatie (PII) op. IP de adressen worden gebruikt slechts door Doel tijdens de zitting (in geheugen, nooit voortgeduurd).

## Vervanging van laatste octet van IP adressen {#section_AE84EB0D7CE04E93B279B77732ADD61E}

Adobe heeft een nieuwe &quot;privacy-door-ontwerp&quot;instelling ontwikkeld die door de Zorg van de Cliënt van Adobe voor Adobe Target kan worden toegelaten. Wanneer dit het plaatsen wordt toegelaten, wordt het laatste octet (het laatste gedeelte) van het IP adres onmiddellijk verborgen wanneer het IP adres door Adobe wordt verzameld. Deze anonymization wordt uitgevoerd vóór om het even welke verwerking van het IP adres, met inbegrip van vóór een facultatieve geo-raadpleging van het IP adres.

Wanneer deze eigenschap wordt toegelaten, wordt het IP adres gemaakt voldoende anoniem zodat is het niet meer identificeerbaar als persoonlijke informatie. Als gevolg hiervan kan Adobe Target worden gebruikt in overeenstemming met de wetgeving inzake de privacy van gegevens in landen die het verzamelen van persoonsgegevens niet toestaan. Het verkrijgen van informatie op het niveau van de stad zal waarschijnlijk aanzienlijk worden beïnvloed door de verduistering van het IP-adres. Het verkrijgen van informatie op regionaal en nationaal niveau mag slechts enigszins worden beïnvloed.

De volgende instellingen zijn beschikbaar:

* Geen verwarring: Het doel verbergt geen deel van het IP adres.
* Laatste octet: Het doel verbergt het laatste octet van het IP adres.
* Volledige IP: Het doel verbergt het volledige IP adres.

Het doel ontvangt het volledige IP adres en verduistert het (als reeks aan Laatste octet of Volledige IP) zoals gespecificeerd. Het doel houdt dan het verduisterde IP adres in geheugen tijdens de zitting.

>[!NOTE]
>
>[Contact opnemen met de Adobe-klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om te bepalen welke het plaatsen u momenteel gebruikt of om de IP verduisteringseigenschap toe te laten.

## GeoSegmentation {#section_BB69F96559BD44BDA4177537C4A5345A}

Als u de vervanging van het laatste octet van het IP adres toelaat, kunnen de resterende waarden van het IP adres worden geanalyseerd gebruikend rapporten in Adobe Target. Als het laatste octet van het IP adres niet verduisterd is, dan kan het volledige IP adres in Adobe Target worden geanalyseerd. Met de functie GeoSegmentation kunt u de locatie van de bezoeker per geografisch gebied in kaart brengen. GeoSegmentation-gegevens zijn alleen granulair voor het niveau van de stad of postcode, en niet voor het individuele niveau.

Als IP de adressen volledig verduisterd zijn, is GeoSegmentation en geo het richten niet beschikbaar.

## Koppeling uitschakelen {#section_E7A62B7B99C94B3A806CB262D16E27FC}

U kunt een koppeling om te weigeren toevoegen aan uw sites zodat bezoekers zich kunnen afmelden voor alle aftellingen en de levering van inhoud.

1. Voeg de volgende koppeling toe aan uw site:

   `<a href="https://clientcode.tt.omtrdc.net/optout"> Your Opt Out Language Here</a>`

1. (Voorwaardelijk) als u CNAME gebruikt, zou de verbinding &quot;client= moeten bevatten`clientcode` parameter, bijvoorbeeld: https://my.cname.domain/optout?client=clientcode.

1. Vervangen `clientcode` met uw clientcode en voeg de tekst of afbeelding toe die u wilt koppelen aan de URL voor niet-deelname.

Elke bezoeker die op deze koppeling klikt, wordt niet opgenomen in een box-aanvraag die vanaf zijn browsersessies wordt aangeroepen totdat hij of zij zijn of haar cookies verwijdert, of gedurende twee jaar, afhankelijk van welke eerst aankomt. Dit werkt door een cookie in te stellen voor de bezoeker die wordt aangeroepen `disableClient` in de `clientcode.tt.omtrdc.net` domein.

Zelfs als u een eersteklas cookie-implementatie gebruikt, wordt de opgegeven opt-out ingesteld via een cookie van een andere fabrikant. Als de client alleen een eersteklas cookie gebruikt, controleert Target of een uitschakelcookie is ingesteld.

## Regels inzake privacy en gegevensbescherming

Zie [Regels inzake privacy en gegevensbescherming](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md) voor meer informatie over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten, en hoe deze regels van invloed zijn op uw organisatie en Adobe Target.
