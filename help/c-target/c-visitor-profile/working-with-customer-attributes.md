---
keywords: klantenrelatiebeheer;de dienst van het klantenverslag;crs;crm;mbox3rdpartyid;klantenattributen;het richten;csv;crm;adobe ervaren wolken
description: Leer hoe te om de gegevens van ondernemingsklanten van een gegevensbestand van het de relatiebeheer van de klant (CRM) voor inhoud te gebruiken richtend in [!DNL Adobe Target].
title: Wat zijn klantkenmerken en hoe gebruik ik deze?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: 19b012a0fcbf5195b12990f0a634a90597850899
workflow-type: tm+mt
source-wordcount: '1559'
ht-degree: 0%

---

# [ongedefinieerd](/help/c-target/c-visitor-profile/working-with-customer-attributes.md)

Informatie over het gebruik van bedrijfsklantgegevens uit CRM-databases (Customer Relationship Management) voor inhoud die zich richt op [!DNL Adobe Target] door klantkenmerken te gebruiken in de [!DNL Adobe Enterprise Cloud People] service.

De gegevens van de de klantenklant van de onderneming die door veelvoudige bronnen worden verzameld en binnen de gegevensbestanden van CRM worden opgeslagen kunnen in worden gebruikt [!DNL Target] om strategisch de meest relevante inhoud aan klanten te leveren, met name gericht op het terugsturen van klanten. Soorten publiek en klantkenmerken in de [!DNL People] de dienst (vroeger Profielen en Publiek) brengt gegevensinzameling en analyse met het testen en optimaliseren samen, die gegevens en inzichten actionable maken.

## Overzicht van klantkenmerken {#section_B4099971FA4B48598294C56EAE86B45A}

[Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html) in de [!DNL People] de dienst maakt deel uit van [!DNL Adobe Experience Cloud] en biedt bedrijven een hulpmiddel om hun klantgegevens naar de [!DNL Experience Cloud] platform.

Gegevens aan boord van de [!DNL Experience Cloud] is beschikbaar voor iedereen [!DNL Experience Cloud] workflows. [!DNL Target] gebruikt deze gegevens voor het richten van terugkerende klant die op attributen wordt gebaseerd. [!DNL Adobe Analytics] verbruikt deze kenmerken en kunnen worden gebruikt voor analyse en segmentatie.

![crs-voorbeeld](/help/c-target/c-visitor-profile/assets/crs.png)

Overweeg de volgende informatie als uw werk met klantenattributen en [!DNL Target]:

* Er zijn enkele voorwaarden waaraan u moet voldoen voordat u de opdracht [!UICONTROL Customer attributes] in de [!DNL People] service. Zie &quot;Vereisten voor het uploaden van klantkenmerken&quot; in [Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in de *Experience Cloud Services- en beheerdocumentatie*.
* Houd rekening met de beperkingen met betrekking tot het uploaden van bestanden, zoals beschreven in [Gegevensbestand en gegevensbronnen voor klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en) in de *Experience Cloud Central Interface Components Guide*. Als beste praktijken:

   * Enkelvoudige grote bestanden uploaden (binnen de [gespecificeerde limieten](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en)). Enkelvoudige grote bestanden hebben de voorkeur boven meerdere kleinere bestanden.
   * Als u de upload in verscheidene dossiers moet verdelen, zorg ervoor dat de dossiers volledig worden verwerkt alvorens nieuwe dossiers voor te leggen. Zorg ervoor dat elk bestand in een batch volledig is verwerkt voordat u de volgende batch verzendt.

* [!DNL Adobe] garandeert niet dat 100% van gegevens van klantkenmerken (bezoekersprofiel) uit CRM-databases aan de [!DNL Experience Cloud] en dus beschikbaar zijn voor gebruik bij [!DNL Target]. In het huidige ontwerp bestaat de mogelijkheid dat een klein percentage gegevens (tot 0,1% van de grote productiepartijen) niet wordt ingecheckt.
* De levensduur van klantkenmerkgegevens die zijn geïmporteerd uit de [!DNL Experience Cloud] tot [!DNL Target] is afhankelijk van de levensduur van het bezoekersprofiel, dat standaard 14 dagen is. Zie voor meer informatie [Levensduur bezoekersprofiel](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* Als de `vst.*` parameters zijn het enige dat de bezoeker identificeert; het bestaande &quot;geverifieerde&quot; profiel wordt niet opgehaald zolang `authState` is NIET VERIFIEERD (0). Het profiel wordt alleen in werking gesteld als `authState` wordt gewijzigd in AUTHENTICATED (1).

   Als de `vst.myDataSource.id` parameter wordt gebruikt om de bezoeker te identificeren (waarbij `myDataSource` is de alias van de gegevensbron) en er is geen MCID of derde identiteitskaart, gebruikend de parameter `vst.myDataSource.authState=0` haalt niet het profiel dat door de invoer van Attributen van de Klant zou kunnen zijn gecreeerd. Als u het geverifieerde profiel wilt ophalen, wordt het `vst.myDataSource.authState` moet de waarde 1 (GEAUTHENTIFICEERD) hebben.

* U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plus-teken (+) en slash (/).

## De Attributen van de Klant van de toegang in de dienst van Mensen

1. In de [!DNL Adobe Experience Cloud], klikt u op het menupictogram ( ![menupictogram](/help/c-target/c-visitor-profile/assets/menu-icon.png) ) en klik vervolgens op **[!UICONTROL People]**.

   ![Mensen](/help/c-target/c-visitor-profile/assets/people.png)

1. Klik op de knop **[!UICONTROL Customer Attributes]** tab.

   ![Klantkenmerken, tabblad](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Workflow voor klantkenmerken voor [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Voer de volgende stappen uit om CRM-gegevens te gebruiken in [!DNL Target], zoals hieronder wordt geïllustreerd:

![crm-workflow](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Gedetailleerde instructies voor het uitvoeren van elk van de volgende taken vindt u in [Een bron voor klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html) in de *Experience Cloud Services- en beheerdocumentatie*.

1. Maak een gegevensbestand.

   De klantengegevens van de uitvoer van uw CRM aan formaat CSV om een .csv- dossier tot stand te brengen. Er kan ook een zip- of gzip-bestand worden gemaakt om te uploaden. Zorg ervoor dat de eerste rij van het CSV-bestand de koptekst is en dat alle rijen (klantgegevens) hetzelfde aantal vermeldingen hebben.

   In de volgende afbeelding ziet u een voorbeeld van een bestand met klantgegevens voor de onderneming:

   ![crs-monster](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   In de volgende afbeelding ziet u een voorbeeld van een klant-CSV-bestand voor bedrijven:

   ![csv-monster](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Maak de kenmerkbron en upload het gegevensbestand.

   Geef een naam en beschrijving op van de gegevensbron en de alias-id. De alias-id is een unieke id die moet worden gebruikt in de kenmerkcode van uw klant in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >De naam van de gegevensbron en de kenmerknaam mogen geen punt bevatten.

   Het gegevensbestand moet voldoen aan de vereisten voor het uploaden van het bestand en mag niet groter zijn dan 100 MB. Als uw bestand te groot is of als u gegevens hebt die op terugkerende basis moeten worden geüpload, kunt u in plaats daarvan FTP op uw bestanden toepassen.

   * **HTTPS:** U kunt het CSV-gegevensbestand slepen en neerzetten of klikken **[!UICONTROL Browse]** om te uploaden vanaf uw bestandssysteem.
   * **FTP:** Klik op de FTP-koppeling naar [het bestand uploaden via FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). De eerste stap bestaat uit het opgeven van een wachtwoord voor de door Adobe verschafte FTP-server. Geef het wachtwoord op en klik vervolgens op **[!UICONTROL Done]**.

   Breng nu uw CSV/ZIP/GZIP-bestand over naar de FTP-server. Nadat deze bestandsoverdracht is gelukt, maakt u een bestand met dezelfde naam en een `.fin` extensie. Breng dit lege bestand over naar de server. Dit wijst op een eind van overdracht en [!DNL Experience Cloud] begint het gegevensbestand te verwerken.

1. Valideer het schema.

   Met het validatieproces kunt u weergavenamen en beschrijvingen toewijzen aan geüploade kenmerken (tekenreeksen, gehele getallen, getallen, enzovoort). Wijs elk attribuut aan zijn correct gegevenstype, vertoningsnaam, en beschrijving toe.

   Klikken **[!UICONTROL Save]** nadat de schemavalidatie volledig is. De uploadtijd van het bestand is afhankelijk van de grootte.

   ![Schema valideren](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema uploaden](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Configureer abonnementen en activeer de kenmerkbron.

   Klikken **[!UICONTROL Add Subscription]** Selecteer vervolgens de oplossing om deze kenmerken in te schrijven. [Abonnementen configureren](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) stelt de gegevensstroom in tussen de [!DNL Experience Cloud] en oplossingen. Door de kenmerkbron te activeren, kunnen de gegevens naar ingetekende oplossingen stromen. De klantrecords die u hebt geüpload, komen overeen met binnenkomende id-signalen van uw website of toepassing.

   ![Oplossing configureren](/help/c-target/c-visitor-profile/assets/solution.png)

   ![Activeren](/help/c-target/c-visitor-profile/assets/activate.png)

   Houd bij het uitvoeren van deze stap rekening met de volgende beperkingen:

   * De maximale bestandsgrootte voor elke upload met de HTTP-methode is 100 MB.
   * De maximale bestandsgrootte voor elke upload met de FTP-methode is 4 GB.
   * Het aantal kenmerken dat mag worden geabonneerd: 5 voor [!DNL Target Standard] en 200 voor [!DNL Target Premium].

## Klantkenmerken gebruiken in [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

U kunt klantkenmerken gebruiken in [!DNL Target] op de volgende manieren:

### Doelgroepen maken

In [!DNL Target], kunt u een klantkenmerk selecteren in het menu [!UICONTROL Visitor Profile] bij het maken van een publiek. Alle klantkenmerken hebben het voorvoegsel &lt; data_source_name > in de lijst. U kunt deze kenmerken desgewenst combineren met andere gegevenskenmerken om een publiek te maken.

![Doelpubliek](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### Profielscripts maken met behulp van tokens

In profielscripts kan met de indeling naar de kenmerken van de klant worden verwezen `crs.get('<Datasource Name>.<Attribute name>')`.

Dit profielscript kan rechtstreeks worden gebruikt in aanbiedingen voor het leveren van kenmerken die bij de huidige bezoeker horen.

### Mbox3rdPartyID in uw website gebruiken voor een geslaagde implementatie en gebruik

Voldoende `mbox3rdPartyId` als een parameter voor de algemene mbox in de `targetPageParams()` methode. De waarde van `mbox3rdPartyId` moet worden ingesteld op de klant-id die aanwezig was in het CSV-gegevensbestand.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### De Experience Cloud ID-service gebruiken

Als u de Experience Cloud-id-service gebruikt, moet u een klant-id en verificatiestatus instellen om klantkenmerken te gebruiken voor het opgeven van doelen. Zie voor meer informatie [Klant-id&#39;s en verificatiestatus](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in de *Help bij Experience Cloud ID-service*.

Voor meer informatie over het gebruik van klantkenmerken in [!DNL Target], zie de volgende middelen:

* [Een bron voor klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in de *Experience Cloud Services- en beheerdocumentatie*

## Problemen die klanten vaak tegenkomen {#section_BE0F70E563F64294B17087DE2BC1E74C}

U zou de volgende kwesties kunnen ontmoeten wanneer het werken met klantenattributen en [!DNL Target].

>[!NOTE]
>
>Kwesties 1 en 2 veroorzaken ongeveer 60% van de problemen op dit gebied. Probleem 3 veroorzaakt ongeveer 30% van de problemen. Probleem 4 veroorzaakt ongeveer 5% van de problemen. De resterende 5% is te wijten aan diverse problemen.

### Uitgave 1: Klantkenmerken worden verwijderd omdat het profiel te groot is

Er is geen tekenlimiet voor een bepaald veld in het gebruikersprofiel, maar als het profiel groter is dan 64 kB, wordt het afgebroken door de oudste kenmerken te verwijderen totdat het profiel weer lager is dan 64 kB.

### Uitgave 2: Kenmerken die niet worden vermeld in de Audience Library in [!DNL Target], zelfs na enkele dagen

Dit is meestal een verbindingsprobleem met de pijplijn. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Versie 3: Aflevering werkt niet op basis van het kenmerk

Het profiel is nog niet bijgewerkt op de rand. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Versie 4: Implementatievraagstukken

Houd rekening met de volgende implementatiekwesties:

* De bezoeker-id is niet correct doorgegeven. De id is doorgegeven `mboxMCGVID` in plaats van `setCustomerId`.
* De bezoekersidentiteitskaart werd correct overgegaan, maar de staat van de VERIFICATIE werd niet geplaatst aan voor authentiek verklaard.
* `mbox3rdPartyId` is niet correct doorgegeven.

### Uitgave 5: `mboxUpdate` niet correct uitgevoerd

`mboxUpdate`  is niet correct uitgevoerd met `mbox3rdPartyId`.

### Uitgave 6: Klantkenmerken worden niet geïmporteerd in [!DNL Target]

Als u de klantkenmerkgegevens niet kunt vinden in Target, dient u ervoor te zorgen dat de import heeft plaatsgevonden binnen de laatste *x* dagen *x* is het doel [Levensduur bezoekersprofiel](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) waarde (standaard 14 dagen).

## Trainingsvideo: Offlinegegevens uploaden met behulp van klantkenmerken ![Zelfstudie-badge](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In deze video ziet u hoe u offline CRM, helpdesk, verkooppunt en andere marketinggegevens kunt importeren in de [!DNL Experience Cloud People] en deze koppelen aan bezoekers met behulp van hun bekende id&#39;s.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
