---
keywords: doel;a4t;geo;geotargeting;geotargeting nauwkeurigheid;land;land;land;plaats;zip-code;dma;mobiele carrier-codes;regio-codes;landcodes;metro-codes;profielscripts;geotargeting profielscripts;geotargeting mobile
description: Leer hoe u een publiek kunt maken in [!DNL Adobe Target] op basis van hun geografische locatie.
title: Kan ik bezoekers richten op basis van locatie?
feature: Audiences
solution: Target,Analytics
exl-id: e4a71a4d-e8f3-4f94-a1a7-fd250f4d5095
source-git-commit: 195028613dec0294c816703b9145e720e3209d74
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 1%

---

# Geo

Soorten publiek gebruiken in [!DNL Adobe Target] op basis van hun geografische locatie.

De parameters van de plaats van de geoplaats laten u activiteiten en ervaringen richten die op de aardrijkskunde van uw bezoekers worden gebaseerd. U kunt bezoekers opnemen of uitsluiten op basis van hun land, provincie, provincie, stad, postcode, breedte, lengte, DMA of mobiele provider. Deze gegevens worden met elk verzonden [!DNL Target] en is gebaseerd op het IP-adres van de bezoeker. Selecteer deze parameters net als alle doelwaarden.

## Een publiek maken met geofocus {#section_49CBFFAAC8694C4AAD3DE4B2DB7B05DE}

1. In de [!DNL Target] interface, klik **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Slepen en neerzetten **[!UICONTROL Geo]** in het deelvenster voor publieksopbouw.

1. Klikken **[!UICONTROL Select]** Selecteer vervolgens een van de volgende opties:

   * [!UICONTROL Country/Region]
   * [!UICONTROL State]
   * [!UICONTROL City]
   * [!UICONTROL Zip Code]
   * [!UICONTROL Longitude]
   * [!UICONTROL Latitude]
   * [!UICONTROL DMA]
   * [!UICONTROL Mobile Carrier]

   De geo-informatie van een bezoeker wordt bepaald aan de hand van het IP-adres van oorsprong van een [!DNL Target] locatieverzoek (mbox-verzoek). De IP-aan-geo resolutie wordt gedaan voor de eerste vraag van een nieuwe zitting. Dit betekent, als het IP adres van een bezoeker middenzitting van een bezoek verandert, is de geo informatie nog gebaseerd op het IP adres van de eerste vraag.

   Voor [!UICONTROL Mobile Carrier], [!DNL Target] gebruikt de IP gegevens van de adresregistratie (die het blok van IP adressen) bezit om de aangewezen mobiele drager te bepalen gebruikend [Mobiele landcodes (MCC) en Mobiele netwerkcodes (MNC)](https://www.mcc-mnc.com).

1. Geef een operator en de juiste waarde op.
1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

In de volgende afbeelding ziet u een publiek dat gericht is op gebruikers die de activiteit betreden vanaf een breedte van meer dan 44° en een lengte van minder dan 22°.

![target_geo, afbeelding](assets/target_geo.png)

## Nauwkeurigheid {#section_D63D5FFCB49C42F9933AFD0BD7C79DF1}

De nauwkeurigheid van geo-gerichtheid hangt af van verschillende factoren. WiFi-verbindingen zijn nauwkeuriger dan mobiele netwerken. Wanneer een bezoeker een cellulaire gegevensverbinding gebruikt, kan de nauwkeurigheid van geo-raadpleging door plaats worden beïnvloed, de gegevensverhouding van de leverancier met [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester)en andere factoren. Netwerkverbindingen die zijn gebaseerd op mobiele tower, zijn mogelijk minder nauwkeurig dan bekabelde of WiFi-verbindingen. Ook, zou het IP van een bezoeker adres aan de ISP plaats van de bezoeker kunnen worden in kaart gebracht, die niet het zelfde als de daadwerkelijke plaats van de bezoeker zou kunnen zijn. Bepaalde problemen met mobiele geolocatie kunnen worden opgelost met de [Geolocatie-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API).

De volgende lijst toont de nauwkeurigheid van op IP-Gebaseerde geografische informatie van [DigitalEnvoy](https://www.digitalelement.com/solutions/) voor bekabelde of WiFi-internetverbindingen. DigitalEnvoy biedt de meest nauwkeurige gegevens in de branche. De wereldwijde nauwkeurigheid is meer dan 99,9 procent op landniveau en is tot 97 procent nauwkeurig op stadsniveau. Nauwkeurigheidsinformatie is niet van toepassing op netwerken op basis van mobiele towers.

| Land | Staat | Plaats | Regio |
|--- |--- |--- |--- |
| VS | 99.99% | 96% | 94% |
| Canada | 99.99% | 96% | 94% |
| Europa | 99.99% |  |  |
| VK | 99.99% |  | 87% |
| Duitsland | 99.99% | 95% | 93% |
| Scandinavië | 99% | Laag 90 s | Midden 80 |
| Spanje | 99.99% | Ongeveer 90% | Midden tot hoog, 90 seconden |
| Azië | 99% | Midden 90 | Laag 90 s |
| Japan | 99.99% | Midden 90 | Laag 90 s |
| Australië | 99.99% | 94% | 91% |

## Geo-targeting gebruiken in profielscripts {#section_92C93138542C4A94997E3F4BE3F5DA28}

U kunt geo-informatie gebruiken voor profielscripts.

Gebruik bijvoorbeeld:

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`

U kunt dus een doelexpressie met de naam &#39;Uit Noord-Amerika&#39; schrijven met de volgende code:

`return profile.geolocation.country == 'united states' || profile.geolocation.country == 'canada' || profile.geolocation.country == 'mexico';`

## Geo-richtingswaarden gebruiken als tokens {#section_E7F7FDF62C3B4934A6565D04B24655F6}

U kunt `profile.geolocation` worden rechtstreeks als tokens gebruikt in aanbiedingen, plug-ins enzovoort.

Gebruik bijvoorbeeld:

* `${profile.geolocation.country}`
* `${profile.geolocation.state}`
* `${profile.geolocation.city}`
* `${profile.geolocation.zip}`
* `${profile.geolocation.dma}`
* `${profile.geolocation.domainName}`
* `${profile.geolocation.ispName}`
* `${profile.geolocation.connectionSpeed}`
* `${profile.geolocation.mobileCarrier}`
* `${profile.geolocation.latitude}`
* `${profile.geolocation.longitude}`

## Veelgestelde vragen over geo-targeting {#section_DD308A53AF0F48FA8C81423580561FE7}

De volgende vragen worden vaak gesteld over geo-targeting:

### Hoe kan ik breedte- en lengtegraad opgeven?

+++Zie details
* De waarde voor breedte en lengte moet een numerieke waarde in graden zijn.
* De waarde voor breedte en lengte kan een maximale precisie van vijf decimalen hebben.
* De waarde voor latitude moet liggen tussen -90 en 90.
* De waarde voor longitude moet liggen tussen -180 en 180.

+++

### Hoe werkt geo-targeting voor mobiele apparaten?

+++Zie details De meeste gebruikers van mobiele apparaten hebben toegang tot inhoud via WiFi, wat betekent [!DNL Target]IP-based geo het richten is zo nauwkeurig als op een Desktop. De op toren-gebaseerde verbindingen van de cel kunnen minder nauwkeurig zijn omdat het IP van de bezoeker adres op de toren gebaseerd is waar het signaal wordt opgepikt. Bepaalde problemen met mobiele geolocatie kunnen worden opgelost met de [Geolocatie-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API).

+++

### Hoe behandelt de functie van geo bezoekers van AOL?

+++Zie details Wegens de manier waarop AOL zijn verkeer verrijkt, [!DNL Target] zij kunnen alleen op nationaal niveau worden gericht. Zo is een campagne gericht op Frankrijk succesvol gericht op gebruikers van AOL in Frankrijk. Maar een campagne gericht op Parijs is niet succesvol gericht op AOL-gebruikers in Parijs. Als u specifiek op AOL-gebruikers wilt gericht, kunt u het gebiedveld instellen op &quot;aol&quot;. In feite kunt u de gebruikers van AOL van de V.S. door twee te specificeren richten voorwaarden richten: het land komt precies overeen met &quot; verenigde staten &quot; en de regio komt precies overeen met &quot; aol &quot; .

+++

### Welke plaatsgranulariteit verstrekt geo-richt?

+++Zie details
* Land - wereldwijd
* Staat/provincie/regio - wereldwijd
* Plaats - wereldwijd
* Postcode - VS, Duitsland, Canada
* DMA/ITV (VK) - VS, VK
* Mobiele provider - wereldwijd

+++

### Hoe kan ik mijn activiteiten testen alsof ik een gebruiker ben die van een verschillende plaats komt?

+++Zie details
* **te.js 1.*x***: U kunt uw IP adres met een IP adres van een verschillende plaats met voeten treden en gebruiken `mboxOverride.browserIp url` parameter. Als uw bedrijf bijvoorbeeld in het Verenigd Koninkrijk is, maar uw wereldwijde campagne gericht is op bezoekers in Auckland, Nieuw-Zeeland, gebruikt u deze URL in de veronderstelling dat `60.234.0.39` is een IP adres in Auckland:

   `https://www.mycompany.com?mboxOverride.browserIp=60.234.0.39`

   Wis uw cookies voordat u de activiteit test.

   >[!NOTE]
   >
   >`mboxOverride.browserIp` wordt ondersteund in at.js 1.*x* alleen. Deze functionaliteit wordt niet ondersteund in at.js 2.*x*.

* **te.js 2.*x***: Om uw IP adres met at.js 2 met voeten te treden.*x*, installeert u een browserextensie/plug-in (zoals X-Forwarded-For-header voor Chrome of Firefox). Met deze extensie kunt u de x-door:sturen-voor-header doorgeven in uw paginaaanvragen.

+++

### Hoe worden gebieden, zoals Puerto Rico en Hongkong, in de geo-gerichte structuur ondergebracht?

+++Zie de details Puerto Rico, Hong Kong, en andere gebieden worden behandeld als afzonderlijke &quot;Land&quot;waarden.

+++

### doet [!DNL Target] vastleggen (en opslaan) van informatie zoals ZIP-code wanneer de activiteit wordt gericht op de doelgerichte geolocatie?

+++Zie details nr., [!DNL Target] gebruikt alleen geo-gegevens tijdens de sessie, dan worden de gegevens verwijderd.

+++

## Trainingsvideo: Soorten publiek maken ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
