---
keywords: targeting;a4t;geo;geotargeting;geotargeting accuracy;country;state;city;zip code;dma;mobile carrier;city codes;region codes;country codes;metro codes;profile scripts;geotargeting profile scripts;geotargeting mobile
description: Gebruik een Adobe Target-publiek voor doelgebruikers op basis van hun geografische locatie, waaronder hun land, land/provincie, stad, postcode, DMA of mobiele luchtvaartmaatschappij.
title: Geo-opties in Adobe Target-publiek
feature: audiences
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 2%

---


# Geo{#geo}

Gebruik doelgroepen voor gebruikers op basis van hun geografische locatie, waaronder hun land, land/provincie, stad, postcode/postcode, DMA of mobiele luchtvaartmaatschappij.

De parameters van de plaats van de geoplaats staan u toe om activiteiten en ervaringen te richten die op de aardrijkskunde van uw bezoekers worden gebaseerd. U kunt bezoekers opnemen of uitsluiten op basis van hun land, provincie, provincie, stad, postcode, breedte, lengte, DMA of mobiele provider. Dit gegeven wordt verzonden met elk verzoek van het Doel en is gebaseerd op het IP van de bezoeker adres. Selecteer deze parameters net als alle doelwaarden.

## Een publiek maken met Geo-doelen {#section_49CBFFAAC8694C4AAD3DE4B2DB7B05DE}

1. Klik in de [!DNL Target] interface op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Geo]**.

1. Klik **[!UICONTROL Select]** en selecteer een van de volgende opties:

   * Land
   * Staat
   * Plaats
   * Postcode
   * Breedte
   * Lengtegraad
   * DMA
   * Mobiele vervoerder

   IP van een bezoeker adres wordt overgegaan met een brievenbusverzoek, eens per bezoek (zitting), om geo richtende parameters voor die bezoeker op te lossen.

   Voor Mobiele Drager, [!DNL Target] gebruikt de IP gegevens van de adresregistratie (die het blok van IP adressen) bezit om de aangewezen mobiele drager te bepalen gebruikend de [Mobiele Codes van het Land (MCC) en Mobiele Codes MNC van het Netwerk)](https://www.mcc-mnc.com).

1. Geef een operator en de juiste waarde op.
1. (Optioneel) Klik op aanvullende regels voor het publiek **[!UICONTROL Add Rule]** en stel deze in.
1. Klik op **[!UICONTROL Save]**.

In de volgende afbeelding ziet u een publiek dat gericht is op gebruikers die de activiteit betreden vanaf een breedte van meer dan 44 graden en een lengte van minder dan 22 graden.

![](assets/target_geo.png)

## Nauwkeurigheid {#section_D63D5FFCB49C42F9933AFD0BD7C79DF1}

De nauwkeurigheid van geo-gerichtheid hangt af van verschillende factoren. WiFi-verbindingen zijn nauwkeuriger dan mobiele netwerken. Wanneer de bezoeker een cellulaire gegevensverbinding gebruikt, kan de nauwkeurigheid van geo-raadpleging door plaats, de gegevensverhouding van de leverancier met [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), en andere factoren worden beïnvloed. Netwerkverbindingen die zijn gebaseerd op mobiele tower, zijn mogelijk minder nauwkeurig dan bekabelde of WiFi-verbindingen. Ook, zou het IP van een bezoeker adres aan zijn of haar ISP plaats kunnen worden in kaart gebracht, die niet het zelfde als de daadwerkelijke plaats van de bezoeker zou kunnen zijn. Sommige problemen met mobiele geolocatie kunnen worden opgelost met de [Geolocation-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API).

In de volgende tabel wordt de nauwkeurigheid van op IP gebaseerde geografische informatie van [DigitalEnvoy](https://www.digitalelement.com/solutions/) voor bekabelde of WiFi-internetverbindingen weergegeven. DigitalEnvoy biedt de meest nauwkeurige gegevens in de branche. De wereldwijde nauwkeurigheid is meer dan 99,9 procent op landniveau en is tot 97 procent nauwkeurig op stadsniveau. Nauwkeurigheidsinformatie is niet van toepassing op netwerken op basis van mobiele towers.

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

## Geo-gericht gebruiken in profielscripts {#section_92C93138542C4A94997E3F4BE3F5DA28}

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

## Geo-gerichte waarden als tokens gebruiken {#section_E7F7FDF62C3B4934A6565D04B24655F6}

U kunt waarden nu rechtstreeks als tokens gebruiken in aanbiedingen, plug-ins enzovoort. `profile.geolocation`

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

## Veelgestelde vragen over Geotargeting {#section_DD308A53AF0F48FA8C81423580561FE7}

**Hoe kan ik breedte- en lengtegraad opgeven?**

* De waarde voor breedte/lengte moet een numerieke waarde in graden zijn.
* De waarde voor latitude/longitude kan een maximale precisie van vijf decimalen hebben.
* De waarde voor latitude moet liggen tussen -90 en 90.
* De waarde voor longitude moet liggen tussen -180 en 180.

**Hoe richt geo zich op het werk voor mobiele apparaten?**

Het overgrote deel van de gebruikers van mobiele apparaten heeft toegang tot inhoud via WiFi, wat betekent dat de op IP-Gebaseerde geo van Target net zo nauwkeurig is als op een Desktop. De op toren-gebaseerde verbindingen van de cel kunnen minder nauwkeurig zijn omdat het IP van de bezoeker adres op de toren gebaseerd is waar het signaal wordt opgepikt. Sommige problemen met mobiele geolocatie kunnen worden opgelost met de [Geolocation-API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API).

**Hoe behandelt de functie van geo bezoekers van AOL?**

Door de manier waarop AOL zijn verkeer verrijkt, kunnen we ze alleen op nationaal niveau aanpakken. Zo zal een campagne voor Frankrijk met succes gericht zijn op AOL-gebruikers in Frankrijk. Maar een campagne gericht op Parijs zal niet succesvol zijn tegen AOL-gebruikers in Parijs. Als u specifiek op AOL-gebruikers wilt gericht, kunt u het gebiedveld instellen op &quot;aol&quot;. In feite kunt u de gebruikers van AOL van de V.S. door twee te specificeren richten voorwaarden richten: het land komt precies overeen met &quot; verenigde staten &quot; en de regio komt precies overeen met &quot; aol &quot; .

**Welke plaatsgranulariteit verstrekt geo richt?**

* Land - wereldwijd
* Staat/provincie/regio - wereldwijd
* Plaats - wereldwijd
* Postcode - VS, Duitsland, Canada
* DMA/ITV (VK) - VS, VK
* Mobiele provider - wereldwijd

**Hoe kan ik mijn activiteiten testen alsof ik een gebruiker ben die van een verschillende plaats komt?**

U kunt uw IP adres met een IP adres van een verschillende plaats met voeten treden en de `mboxOverride.browserIp url` parameter gebruiken. Dus als uw bedrijf zich in het Verenigd Koninkrijk bevindt, maar uw wereldwijde campagne gericht is op bezoekers in Aukland, Nieuw-Zeeland, gebruikt u deze URL, ervan uitgaande dat dat een IP-adres `60.234.0.39` is in Auckland:

`https://www.mycompany.com?mboxOverride.browserIp=60.234.0.39`

Je moet je cookies wissen voordat je dit doet.

>[!NOTE]
>
>`mboxOverride.browserIp` wordt alleen ondersteund in at.js 1.*jx* . Deze functionaliteit wordt niet ondersteund in at.js 2.*x*.

**Hoe worden gebieden, zoals Puerto Rico en Hongkong, in de geo-gerichte structuur ondergebracht?**

Puerto Rico, Hong Kong en andere gebieden worden behandeld als afzonderlijke &quot;Land&quot;-waarden.

**Vangt (en slaat) informatie zoals de Codes van het PIT op wanneer de activiteit met geo-plaats gerichte mogelijkheden wordt gericht? [!DNL Target]**

Nr, [!DNL Target] gebruikt geo gegevens voor de duur van de zitting slechts, dan worden de gegevens verworpen.

## Trainingsvideo: Zelfstudie- ![badge voor soorten publiek maken](/help/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
