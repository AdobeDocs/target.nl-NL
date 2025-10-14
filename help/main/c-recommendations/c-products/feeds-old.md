---
keywords: aanbevelingen feed;feed;SAINT;ftp;csv;classificaties;analytische classificaties
description: Leer hoe het voer de invoerentiteiten in  [!DNL Adobe Target] [!DNL Recommendations] gebruikend Csv- dossiers, het de voederformaat van het Onderzoek van het Product van Google, en  [!DNL Analytics]  productclassificaties invoert.
title: Hoe gebruik ik [!UICONTROL Feeds] in  [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 7b336a9e-23f4-4b09-9c8f-b9cb68162b1b
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '2463'
ht-degree: 0%

---

# Feeds

Gebruik feeds om entiteiten in te voeren in [!DNL Adobe Target] [!DNL Recommendations] . Entiteiten kunnen worden verzonden met gebruik van CSV-bestanden, de Google Product Search-feed-indeling en [!DNL Adobe Analytics] -productclassificaties.

## Overzicht van feeds {#concept_D1E9C7347C5D4583AA69B02E79607890}

Het voer laat u [&#x200B; Entiteiten &#x200B;](/help/main/c-recommendations/c-products/products.md) overgaan of uw brievenbusgegevens met informatie uitbreiden die of niet beschikbaar op de pagina is of onveilig om rechtstreeks van de pagina, zoals marge, COGS, etc. te verzenden.

Met feeds kunt u gedetailleerde itemgegevens doorgeven in [!DNL Recommendations] , zoals product-id, categorie, naam, bericht en andere kenmerken.

U kunt selecteren welke kolommen u naar de [!DNL Target] -server wilt verzenden in het [!DNL Recommendations] -bestand voor productclassificaties of in het zoekbestand voor Google-producten.

Deze gegevens over elk item kunnen vervolgens worden gebruikt om:

* Waarden weergeven in ontwerpen
* Criteria voor inclusie definiëren
* Items in verschillende verzamelingen sorteren
* Uitzonderingen op aanbevelingen toepassen

U kunt itembeschrijvingen doorgeven aan [!DNL Target] met feeds of selectievakjes. Als gegevens worden verzameld door zowel een entiteitsvoer als een box, wint de meest recente gegevens. Meestal komen de meest recente gegevens uit een box, omdat deze vaker worden weergegeven. In het zeldzame geval dat de entiteit gegevens invoert en tegelijkertijd de gegevens van de doos raken, worden de mbox gegevens gebruikt.

De [!UICONTROL Feeds] -lijst ( **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]** ) bevat informatie over alle feeds die u hebt gemaakt.

![&#x200B; de pagina van het voer &#x200B;](/help/main/c-recommendations/c-products/assets/feeds-page.png)

De pagina [!UICONTROL Feeds] bevat de volgende kolommen:

* **Naam**: De naam van het voer tijdens verwezenlijking wordt gespecificeerd die. Als u de naam van een feed wilt bewerken, moet u de feed zelf bewerken. Wanneer u de feed onder de nieuwe naam opslaat, wordt de feed vernieuwd.
* **Type**: De types omvatten [&#x200B; CSV &#x200B;](/help/main/c-recommendations/c-products/feeds.md#section_65CC1148C7DD448FB213FDF499D35FCA), [&#x200B; Diervoeders van het Product van Google &#x200B;](/help/main/c-recommendations/c-products/feeds.md#section_8EFA98B5BC064140B3F74534AA93AFFF), en [&#x200B; Classificaties van Analytics &#x200B;](/help/main/c-recommendations/c-products/feeds.md#section_79E430D2C75443BEBC9AA0916A337E0A).
* **Status**: De huidige status van de voer [&#128279;](/help/main/c-recommendations/c-products/feeds.md#concept_E475986720D1400999868B3DFD14A7A0).
* **Programma**: Toont het updateschema voor het voer: [!UICONTROL Daily], [!UICONTROL Weekly], [!DNL Every 2 Weeks], of [!UICONTROL Never].
* **Punten**: Toont het aantal punten in het voer.
* **Laatste Bijgewerkt**: Toont de datum en de tijd toen het voer en de naam van de persoon laatst werd bijgewerkt die het voer bijwerkte. Als de feed [!UICONTROL Last Updated] &#39;undefined&#39; zegt, komt de feed in vanuit [!DNL Recommendations Classic] en kan deze niet vanuit [!DNL Target Premium Recommendations] worden gewijzigd.

Klik op het pictogram Informatie om een kaart weer te geven waarop de laatste uploaddatum en de URL van de feed worden weergegeven.

Klik op het ellipspictogram om de volgende handelingen te openen: [!UICONTROL Deactivate] , [!DNL Edit] , [!UICONTROL Copy] en [!UICONTROL Delete] .

>[!IMPORTANT]
>
>Geüploade entiteiten en entiteitskenmerken verlopen na 61 dagen. Dit betekent:
>
>* Uw feed moet ten minste maandelijks worden uitgevoerd om ervoor te zorgen dat de inhoud van de catalogus niet verloopt.
>* Als u een item uit het voederbestand verwijdert, wordt dat item niet uit de catalogus verwijderd. Als u het item uit de catalogus wilt verwijderen, verwijdert u het handmatig via de gebruikersinterface of API van [!DNL Target] . Of wijzig de itemkenmerken (zoals voorraad) om ervoor te zorgen dat het item niet in aanmerking wordt genomen.

## Source-typen

Entiteiten kunnen worden verzonden met gebruik van CSV-bestanden, de Google Product Search-feed-indeling en [!DNL Adobe Analytics] -productclassificaties.

### CSV {#section_65CC1148C7DD448FB213FDF499D35FCA}

U kunt een .csv-bestand maken met de gedeponeerde CSV-uploadindeling van [!DNL Adobe] . Het bestand bevat weergaveinformatie over de gereserveerde en aangepaste kenmerken voor uw producten. Als u kenmerken wilt uploaden die specifiek zijn voor uw implementatie, vervangt u `CustomN` in de koptekstrij door de naam van het kenmerk dat u wilt gebruiken. In het onderstaande voorbeeld is `entity.Custom1` vervangen door: `entity.availability` . Vervolgens kunt u het bestand in bulk uploaden naar de [!DNL Recommendations] -server.

Het gebruik van de .csv-indeling heeft de volgende voordelen ten opzichte van de Google Feed-indeling:

* Voor de .csv-indeling zijn geen veldtoewijzingen vereist.
* De .csv-indeling ondersteunt kenmerken met meerdere waarden (zie het onderstaande voorbeeld).
* De .csv-indeling ondersteunt maximaal 100 aangepaste kenmerken. Als u meer dan 100 aangepaste kenmerken nodig hebt, kunt u een tweede feed-bestand maken met een andere set opgegeven aangepaste kenmerken.

Gebruik de methode voor het bulkuploaden om weergavegegevens te verzenden als u geen vakken op uw pagina hebt of als u uw weergavegegevens wilt aanvullen met items die niet op uw site beschikbaar zijn. Stel bijvoorbeeld dat u inventarisgegevens wilt verzenden die mogelijk niet op uw site worden gepubliceerd.

Alle gegevens die zijn geüpload met het CSV-bestand, de Google-productfeed of de [!DNL Analytics] Product Classification-feed, overschrijven de bestaande entiteitskenmerkwaarde in de database. Als u prijsinformatie via mbox-aanvragen verzendt en vervolgens andere prijswaarden in het bestand verzendt, overschrijven de waarden in het bestand de waarden die met de mbox-aanvraag zijn ingesteld. Een uitzondering hierop is het kenmerk entiteit van `categoryId` , waarbij de categoriewaarden worden toegevoegd in plaats van te worden overschreven tot de limiet van 250 tekens.

>[!IMPORTANT]
>
>Plaats geen waarden tussen dubbele aanhalingstekens ( &quot; ) in het CSV-bestand, tenzij deze opzettelijk zijn. Als u waarden tussen dubbele aanhalingstekens plaatst, moet u deze weglaten door ze in een andere set dubbele aanhalingstekens in te sluiten. Dubbele aanhalingstekens die niet worden genegeerd, verhinderen dat de aanbevolen feed correct wordt geladen.

De volgende syntaxis is bijvoorbeeld onjuist:

```
"Apples "Bananas" Grapes"",
```

De volgende syntaxis is correct:

```
"Apples ""Bananas"" Grapes""",
```

>[!NOTE]
>
>U kunt een bestaande waarde niet overschrijven met een lege waarde. Geef een andere waarde op de plaats door om deze te overschrijven. In het geval van een verkoopprijs is het een gemeenschappelijke oplossing om een werkelijk &quot;NULL&quot; of een ander bericht door te geven. Vervolgens kunt u een sjabloonregel schrijven om items met die waarde uit te sluiten.

Het product is ongeveer twee uur na het uploaden van de entiteit beschikbaar in de beheerinterface.

Hier volgt een voorbeeldcode voor een CSV-bestand:

```
## RECSRecommendations Upload File 
## RECS''## RECS'' indicates a Recommendations pre-process header. Please do not remove these lines. 
## RECS 
## RECSUse this file to upload product display information to Recommendations. Each product has its own row. Each line must contain 19 values and if not all are filled a space should be left. 
## RECSThe last 100 columns (entity.custom1 - entity.custom100) are custom. The name 'customN' can be replaced with a custom name such as 'onSale' or 'brand'. 
## RECSIf the products already exist in Recommendations then changes uploaded here will override the data in Recommendations. Any new attributes entered here will be added to the product''s entry in Recommendations. 
## RECSentity.id,entity.name,entity.categoryId,entity.message,entity.thumbnailUrl,entity.value,entity.pageUrl,entity.inventory,entity.margin,entity.last_updated_by,entity.multi_english,entity.availability,entity.tax_country,entity.tax_region,entity.tax_rate,entity.product_type,entity.item_group_id,entity.color,entity.size,entity.brand,entity.gtin 
na3456,RipCurl Watch with Titanium Dial,Watches & Sport,Cutting edge titanium with round case,https://example.com/s7/na3456_Viewer,425,https://example.com/shop/en-us/na3456_RipCurl,24,0.25,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Titanium,44mm,RipCurl,"075380 01050 5" 
na3457,RipCurl Watch with Black Dial,Watches & Sport,Cutting edge matte black with round case,https://example.com/s7/na3457_Viewer,275,https://example.com/shop/en-us/na3457_RipCurl,24,0.27,csv,"[""New"",""Web"",""Sales"",""[1,2,34,5]""]",in stock,US,CA,9.25,Shop by Category > Watches,dz1,Black,44mm,RipCurl,"075340 01060 7"
```

### Google {#section_8EFA98B5BC064140B3F74534AA93AFFF}

Voor het voedertype Google Product Search wordt de Google-indeling gebruikt. Dit is anders dan de gedeponeerde CSV-uploadindeling van [!DNL Adobe] .

Als u een bestaande Google-productfeed hebt, kunt u die gebruiken als importbestand.

>[!NOTE]
>
>Google-gegevens hoeven niet te worden gebruikt. [!DNL Recommendations] gebruikt dezelfde indeling als Google. U kunt deze methode gebruiken om alle gegevens te uploaden die u hebt en de beschikbare planningsfuncties te gebruiken. U moet echter wel de vooraf gedefinieerde Google-kenmerknamen behouden wanneer u het bestand instelt.

De meeste detailhandelaren uploaden producten naar Google, dus wanneer een bezoeker de Google-productzoekopdracht gebruikt, worden hun producten weergegeven. [!DNL Recommendations] volgt de Google-specificatie exact voor entiteitsfeeds. De voer van de entiteit kan naar [!DNL Recommendations] via .xml, .txt, of .tsv worden verzonden, en kan de [&#x200B; attributen gebruiken die door Google &#x200B;](https://support.google.com/merchants/answer/188494?hl=en&topic=2473824&ctx=topic#US) worden bepaald. De resultaten zijn doorzoekbaar op [&#x200B; Google die pagina&#39;s &#x200B;](https://www.google.com/prdhp) winkelen.

>[!NOTE]
>
>De POST-methode moet zijn toegestaan op de server die de Google-feedinhoud host.

Omdat [!DNL Recommendations] -gebruikers al .xml- of .txt-feeds configureren om deze via URL of FTP naar Google te verzenden, worden deze productgegevens door entiteitsfeeds geaccepteerd en worden deze gebruikt om de catalogus met aanbevelingen te maken. Geef op waar die feed bestaat en de aanbevelingen-server de gegevens ophaalt.

Als u Google Product Search gebruikt voor het uploaden van de eenheidfeed, moet er nog steeds een productpaginambox op de pagina staan als u daar aanbevelingen wilt weergeven of productweergaven wilt bijhouden voor levering op basis van weergaven.

Google feeds bieden geen ondersteuning voor meerdere waarden voor een aangepast kenmerk.

De feed wordt uitgevoerd op het moment dat u de feed opslaat en activeert. Het wordt uitgevoerd op het moment dat u de feed opslaat, en vervolgens elke dag en uur later.

Hieronder volgt een voorbeeldcode voor het XML-bestand met zoekgegevens voor Google-producten:

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
<feed xmlns="https://www.w3.org/2005/Atom" xmlns:ns2="https://base.google.com/ns/1.0" xmlns:ns3="https://base.google.com/cns/1.0"> 
    <title>Product Feed</title> 
    <link href="https://example.com"/> 
    <updated>2017-12-13T08:45:04.918-08:00</updated> 
    <author> 
        <name>Product Feed Author</name> 
    </author> 
    <id>https://example.com</id> 
    <entry> 
        <title>RipCurl Watch with Titanium Dial</title> 
        <description>Cutting edge Titanium with Round case</description> 
        <ns2:id>na3452</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3452_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 01050 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3452_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3452_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>425</ns2:price> 
        <ns2:product_review_average>5.0</ns2:product_review_average> 
        <ns2:product_review_count>30</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>375</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
    <entry> 
        <title>RipCurl Watch with Black Dial</title> 
        <description>Cutting edge matte black with Round case</description> 
        <ns2:id>na3453</ns2:id> 
        <ns2:link>https://example.com/shop/en-us/na3453_RipCurl</ns2:link> 
        <ns2:availability>in stock</ns2:availability> 
        <ns2:condition>NEW</ns2:condition> 
        <ns2:google_product_category>Watches &amp; Sport</ns2:google_product_category> 
        <ns2:gtin>075380 013450 5</ns2:gtin> 
        <ns2:image_link>https://example.com/s7/na3453_Viewer</ns2:image_link> 
        <ns2:mobile_link>https://m.example.com/s7/na3453_Viewer</ns2:mobile_link> 
        <ns2:mpn>71050</ns2:mpn> 
        <ns2:price>275</ns2:price> 
        <ns2:product_review_average>4.8</ns2:product_review_average> 
        <ns2:product_review_count>23</ns2:product_review_count> 
        <ns2:product_type>Shop by Category > Watches </ns2:product_type> 
        <ns2:brand>RipCurl</ns2:brand> 
        <ns2:sale_price>249</ns2:sale_price> 
        <ns2:tax> 
          <ns2:country>US</ns2:country> 
          <ns2:region>CA</ns2:region> 
          <ns2:rate>9.25</ns2:rate> 
          <ns2:tax_ship>y</ns2:tax_ship> 
        </ns2:tax> 
        <ns2:is_bundle>N</ns2:is_bundle> 
    </entry> 
</feed> 
```

Hieronder volgt een voorbeeldcode voor een Google-bestand met de zoekfunctie voor producten in het SWF-bestand:

```
id    title    description    link    price    condition    availability    image_link    tax    shipping_weight    shipping    google_product_category    product_type    item_group_id    color    size    gender    age_group    pattern    brand    gtin    mpn 
na3454    RipCurl Watch with Titanium Dial    Cutting edge titanium with round case    https://example.com/shop/en-us/na3454_RipCurl    425    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075380 01050 5    DZ1437 
na3455    RipCurl Watch with Black Dial    Cutting edge matte black with round case    https://example.com/shop/en-us/na3455_RipCurl    275    new    in stock    https://example.com/s7/na3452_Viewer    US:CA:9.25:y    1.5 oz    US:::0.00 USD    Watches & Sport    Shop by Category > Watches    dz1    Black    44mm    male    adult    Solid    RipCurl    075340 01060 7    DZ1446
```

### [!DNL Analytics] Productclassificaties {#section_79E430D2C75443BEBC9AA0916A337E0A}

De [!DNL Analytics] productclassificatie is de enige classificatie die beschikbaar is voor aanbevelingen. Voor meer informatie over dit classificatiedossier, zie [&#x200B; Ongeveer classificaties &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=nl-NL) in de *gids van de Componenten van Analytics*. Het is mogelijk dat niet alle informatie u voor aanbevelingen nodig hebt in uw huidige implementatie beschikbaar is, zo volg deze gebruikershandleiding als u aan uw classificatiedossier wilt toevoegen.

>[!IMPORTANT]
>
>Voordat u entiteitsgegevens importeert naar [!DNL Recommendations] met [!DNL Analytics] -productclassificaties, moet u er rekening mee houden dat dit niet de voorkeursmethode is.
>
> Let op het volgende:
>
>* Updates van entiteitskenmerken hebben een extra vertraging van maximaal 24 uur.
>* [!DNL Target] biedt alleen ondersteuning voor [!UICONTROL Product Classifications] . De SKU van het [!DNL Analytics] product moet aan het zelfde niveau in kaart brengen zoals [!DNL Recommendations] `entity.id`. Aangepaste [!DNL Analytics] classificaties kunnen worden ontwikkeld met [!UICONTROL Adobe Consulting Services] . Neem contact op met uw accountmanager voor vragen.

## Feed maken {#steps}

Maak een feed om informatie over uw producten of services in te voegen in [!DNL Recommendations] .

1. Klik in de doelinterface op **[!UICONTROL Recommendations]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]** .

   ![&#x200B; creeer de dialoogdoos van het Geëigenschap &#x200B;](assets/CreateFeed.png)

1. Geef een beschrijvende naam op voor uw feed.
1. Selecteer een **[!UICONTROL Source Type]** .

   * [!UICONTROL CSV]
   * [!UICONTROL Google Product Feed]
   * [!UICONTROL Analytics Classifications]

   Voor informatie over de [!UICONTROL CSV] en [!UICONTROL Google Product Feed] voedertypes, zie [&#x200B; Overzicht van het Beeld &#x200B;](/help/main/c-recommendations/c-products/feeds.md#concept_D1E9C7347C5D4583AA69B02E79607890). U kunt ook [&#x200B; een modelCSV gids &#x200B;](/help/main/c-recommendations/c-products/assets/EntityFileUploadTemplate.csv) downloaden om u te helpen de voer correct formatteren.

1. (Voorwaardelijk) Als u **[!UICONTROL CSV]** of **[!UICONTROL Google Product Feed]** hebt geselecteerd, geeft u de locatie op waar de feed kan worden geopend.

   * **FTP**: Als u FTP selecteerde, verstrek de de serverinformatie van FTP, de login geloofsbrieven, filename, en de folder van FTP. U kunt FTP met SSL (FTPS) gebruiken voor veiliger uploads.

     Ondersteunde FTP-serverinstellingen:

      * FTP en FTPS moeten zijn ingesteld op het gebruik van Passieve FTP.
      * Voor FTPS configureert u de server zodanig dat deze expliciete FTPS-verbindingen accepteert.
      * SFTP wordt niet ondersteund.
      * U kunt handmatig een poort opgeven waarop de verbinding moet worden gestart (bijvoorbeeld `ftp://ftp.yoursite.com:2121` ). Als u geen poort opgeeft, wordt de standaard-FTP- of FTPS-poort gebruikt.

   * **URL**: Als u [!UICONTROL URL] selecteert, specificeer URL.

1. (Voorwaardelijk) Als u **[!UICONTROL Analytics Classifications]** hebt geselecteerd, kiest u de rapportsuite in de vervolgkeuzelijst.

1. Klik op de pijl **[!UICONTROL Next]** om de opties van [!UICONTROL Schedule] weer te geven.

   ![&#x200B; Resultaat van de Stap &#x200B;](assets/CreateFeedSchedule.png)

1. Selecteer een updateoptie:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 Weeks]
   * [!UICONTROL Never]: plant geen update. Kies deze optie als u deze feed niet wilt uitvoeren.

1. Geef de tijd op waarop de feed moet worden uitgevoerd.

   Deze optie is gebaseerd op de tijdzone die in uw browser wordt gebruikt. Als u een tijd in een verschillende tijdzone wilt gebruiken, moet u die tijd volgens uw tijdzone berekenen.

1. Klik op de pijl **[!UICONTROL Next]** om de [!UICONTROL Mapping] -opties weer te geven en geef vervolgens op hoe u de gegevens wilt toewijzen aan [!DNL Target] -definities.

   ![&#x200B; Resultaat van de Stap &#x200B;](assets/CreatFeedMapping.png)

1. (Optioneel) Als u wilt dat de feed tot een omgeving (hostgroep) behoort, selecteert u de hostgroep.

   De feed behoort standaard tot alle hostgroepen. Dit zorgt ervoor dat de punten in dit voer in om het even welke milieu beschikbaar zijn. Voor meer informatie, zie [&#x200B; Gastheren &#x200B;](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

1. Klik op **[!UICONTROL Save]**.

Nadat u een feed hebt gemaakt of bewerkt, wordt de feed direct uitgevoerd. De feed wordt dan bijgewerkt volgens de parameters die u instelt. Het duurt enige tijd voordat de informatie beschikbaar is. Eerst moet de feed gesynchroniseerd worden, vervolgens moet deze worden verwerkt en geïndexeerd voordat deze kan worden gepubliceerd en beschikbaar gesteld. De huidige status verschijnt onder [&#x200B; Status van het Diervoer &#x200B;](/help/main/c-recommendations/c-products/feeds.md#status) in de lijst van het Beeld. U kunt [!DNL Target] sluiten voordat het proces is voltooid en het proces wordt voortgezet.

Terwijl het indexeren lopend is, verschijnen de producten en de voederkopballen alvorens de individuele waarden zijn geïndexeerd. Dit laat u zoeken en producten zien zodat kunt u inzamelingen, uitsluitingen, ontwerpen, en activiteiten tot stand brengen alvorens het indexeren is voltooid.

Wanneer in Status de tekst &#39;&#39;Voltooid&#39;&#39; wordt weergegeven, betekent dit dat het bestand is gevonden en correct is geparseerd. De informatie is niet beschikbaar voor gebruik binnen [!DNL Recommendations] totdat het bestand is geïndexeerd. Dit kan enige tijd in beslag nemen, afhankelijk van de grootte van het bestand. Als het proces mislukt, is het bestand niet gevonden. U hebt bijvoorbeeld een onjuiste URL gebruikt of de FTP-gegevens zijn onjuist of er is een parseringsfout opgetreden.

## Voederstatussen en indicatoren {#concept_E475986720D1400999868B3DFD14A7A0}

Informatie over de mogelijke voederstatussen en hun indicatoren.

### Voederstatussen {#status}

De volgende statussen zijn mogelijk voor een diervoeder:

| Status | Beschrijving |
|--- |--- |
| [!UICONTROL Syncing] | Gegevens over de instellingen van feed worden opgeslagen in [!DNL Target] . |
| [!UICONTROL Sync Failed] | Gegevens over instellingen van feed kunnen niet worden opgeslagen in [!DNL Target] . Probeer het opnieuw. |
| [!UICONTROL No Feed Run] | U hebt een feed gemaakt, maar deze is niet gepland (de frequentie is ingesteld op Nooit). |
| Gepland bij *datum en tijd* | De feed is niet uitgevoerd, maar moet op de opgegeven datum en tijd worden uitgevoerd. |
| [!UICONTROL Waiting for Download] | [!DNL Target] bereidt zich voor op het downloaden van het feed-bestand. |
| [!UICONTROL Downloading Feed File] | [!DNL Target] downloadt het feed-bestand. |
| [!UICONTROL Importing Items] | [!DNL Target] importeert items uit het feed-bestand. |
| Het voer met succes in *tijd* werd ingevoerd | [!DNL Target] heeft het feed-bestand geïmporteerd in het systeem voor de levering van inhoud. Wijzigingen in objectkenmerken zijn aangebracht in het systeem voor de levering van inhoud en zullen binnenkort worden weergegeven in de geleverde aanbevelingen. Als u de verwachte wijzigingen niet ziet, probeert u het opnieuw en vernieuwt u de pagina met aanbevelingen.<br> Nota&#39;s:<ul><li>Als wijzigingen in de kenmerken van een item ertoe leiden dat een item wordt uitgesloten van aanbevelingen, wordt de uitsluiting onmiddellijk weerspiegeld. Als een punt onlangs wordt toegevoegd, of de veranderingen in attributen in een punt resulteren dat *niet meer* van aanbevelingen wordt uitgesloten, wordt het niet weerspiegeld tot de volgende algoritmeupdate, die binnen 24 uren voorkomt.</li><li>Wanneer deze status wordt weergegeven, worden updates mogelijk nog niet weergegeven in de gebruikersinterface van [!UICONTROL Catalog Search] . In [!UICONTROL Catalog Search] wordt een aparte status weergegeven die de laatste keer aangeeft dat de doorzoekbare catalogus is bijgewerkt.</li></ul> |
| [!UICONTROL Failed to Index] | De indexbewerking is mislukt. Probeer het opnieuw. |
| [!UICONTROL Server Not Found] | FTP- of URL-locaties zijn ongeldig of anderszins onbereikbaar. |

Als u een feed wilt bijwerken (bijvoorbeeld om wijzigingen aan te brengen in de configuratie of het feed-bestand), opent u de feed, brengt u de gewenste wijzigingen aan en klikt u op **[!UICONTROL Save]** .

>[!IMPORTANT]
>
>Geüploade entiteiten verlopen na 61 dagen. Dit betekent dat uw voederdossier minstens om de 60 dagen moet worden geupload om een verstoring van uw aanbevelingen activiteiten te vermijden. Als een item niet ten minste om de 60 dagen in een feed-bestand (of een andere methode voor het bijwerken van entiteiten) wordt opgenomen, leidt [!DNL Target] tot de conclusie dat het item niet langer relevant is en wordt het uit de catalogus verwijderd.

### Indicatoren voor de voederstatus {#section_3C8A236C5CB84C769A9E9E36B8BFABA4}

De volgende statusindicatoren voor de feed worden weergegeven in de kolom [!UICONTROL Status] :

| Status-indicator | Beschrijving |
|--- |--- |
| Groene statusindicator | Wanneer een feed de indexering heeft voltooid, geeft een groene statuspunt aan dat de feed is geslaagd. |
| Gele statusindicator | Als een diervoeder- of voederindex wordt vertraagd met 25% van de voederfrequentie, wordt een gele statuspunt weergegeven. Bijvoorbeeld, toont een gele punt voor een voer dat wordt geplaatst om dagelijks te lopen als de index zes uur na de geplande tijd niet heeft voltooid. Opmerking: als de status van de feed &#39;Waiting for Index Queue&#39; is, zijn de nieuwe bijgewerkte waarden beschikbaar in de levering en verwerking van criteria. |
| Wit statussymbool | Als een feed niet is gepland, geeft een witte statuspunt aan dat de feed nog niet is gestart. |
| Indicator voor rode status | Als de feed er niet in slaagt gegevens naar de server te uploaden, wordt een rode statusindicator weergegeven. |

Neem de volgende voorbeelden:

**Voorbeeld 1:**

* Dag één: dagelijkse voederprocessen om 9.00 uur PST.:00
* Dag twee: het is 3 :30 p.m. en het voer is niet sinds gisteren om 9 :00 a.m. gelopen

De status moet geel zijn omdat de index ongeveer 6,5 uur geleden had moeten worden uitgevoerd. 6,5 uur +24 is 127% van het voedervenster.

**Voorbeeld 2:**

* 1 januari: maandelijkse voederprocessen om 9.00 uur PST.:00
* 3 februari: het is 10 :00 a.m. en het voer is niet één maand, één dag, en één uur geleden gelopen.

De status moet geel zijn omdat de index ongeveer een dag en een uur geleden had moeten lopen. Hoewel dit slechts is (31+(1/25))/30 = 1,03% van de frequentie-instelling, overschrijdt het het maximum van één dag vertraging.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Het begrip van voer in Aanbevelingen (3 :01) ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

Deze video bevat de volgende informatie:

* Begrijp het doel van voer
* De waarde van feeds begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/27695)

### Creeer een voer (6 :44) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een feed instellen
* Weet welk type diervoeder moet worden gebruikt

>[!VIDEO](https://video.tv.adobe.com/v/27696)
