---
keywords: klantenrelatiebeheer;de dienst van het klantenverslag;crs;crm;mbox3rdpartyid;klantenattributen;het richten;csv;crm;adobe ervaren wolken
description: Leer hoe te om de gegevens van ondernemingsklanten van een gegevensbestand van het de relatiebeheer van de klant (CRM) voor inhoud te gebruiken richtend in [!DNL Adobe Target].
title: Wat zijn klantkenmerken en hoe gebruik ik deze?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1563'
ht-degree: 0%

---

# Klantkenmerken

Informatie over het gebruik van bedrijfsklantgegevens uit CRM-databases (Customer Relationship Management) voor inhoud die zich richt op [!DNL Adobe Target] door klantkenmerken te gebruiken in de [!DNL Adobe Enterprise Cloud People] service.

De gegevens van de de klantenklant van de onderneming die door veelvoudige bronnen worden verzameld en binnen de gegevensbestanden van CRM worden opgeslagen kunnen in worden gebruikt [!DNL Target] om strategisch de meest relevante inhoud aan klanten te leveren, met name gericht op het terugsturen van klanten. Soorten publiek en klantkenmerken in de [!DNL People] de dienst (vroeger Profielen en Publiek) brengt gegevensinzameling en analyse met het testen en optimaliseren samen, die gegevens en inzichten actionable maken.

## Overzicht van klantkenmerken {#section_B4099971FA4B48598294C56EAE86B45A}

[Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html) in de [!DNL People] de dienst maakt deel uit van [!DNL Adobe Experience Cloud] en biedt bedrijven een hulpmiddel om hun klantgegevens naar de [!DNL Experience Cloud] platform.

Gegevens aan boord van de [!DNL Experience Cloud] is beschikbaar voor iedereen [!DNL Experience Cloud] workflows. [!DNL Target] gebruikt deze gegevens voor het richten van terugkerende klant die op attributen wordt gebaseerd. [!DNL Adobe Analytics] verbruikt deze kenmerken en kunnen worden gebruikt voor analyse en segmentatie.

![crs-voorbeeld](/help/main/c-target/c-visitor-profile/assets/crs.png)

Overweeg de volgende informatie als uw werk met klantenattributen en [!DNL Target]:

* Er zijn enkele voorwaarden waaraan u moet voldoen voordat u de opdracht [!UICONTROL Customer attributes] in de [!DNL People] service. Zie &quot;Vereisten voor het uploaden van klantkenmerken&quot; in [Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in de *Experience Cloud Services- en beheerdocumentatie*.
* Houd rekening met de beperkingen met betrekking tot het uploaden van bestanden, zoals beschreven in [Gegevensbestand en gegevensbronnen voor klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en) in de *Experience Cloud Central Interface Components Guide*. As best practice:

   * Upload single large files (within the [limits specified](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=en)). Single large files are preferred over multiple smaller files.
   * If you must split the upload into several files, ensure that files are fully processed before submitting new files. Ensure that each file in a batch is fully processed prior to submitting the next file in the batch.

* [!DNL Adobe] garandeert niet dat 100% van gegevens van klantkenmerken (bezoekersprofiel) uit CRM-databases aan de [!DNL Experience Cloud] en dus beschikbaar zijn voor gebruik bij [!DNL Target]. In het huidige ontwerp bestaat de mogelijkheid dat een klein percentage gegevens (tot 0,1% van de grote productiepartijen) niet wordt ingecheckt.
* The lifetime of customer attributes data imported from the [!DNL Experience Cloud] to [!DNL Target] depends on the lifetime of the visitor profile, which is 14 days by default. For more information, see [Visitor Profile Lifetime](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD).
* If the `vst.*` parameters are the only thing identifying the visitor, the existing &quot;authenticated&quot; profile will not be fetched as long as `authState` is UNAUTHENTICATED (0). Het profiel wordt alleen in werking gesteld als `authState` wordt gewijzigd in AUTHENTICATED (1).

   Als de `vst.myDataSource.id` parameter wordt gebruikt om de bezoeker te identificeren (waarbij `myDataSource` is de alias van de gegevensbron) en er is geen MCID of derde identiteitskaart, gebruikend de parameter `vst.myDataSource.authState=0` haalt niet het profiel dat door de invoer van Attributen van de Klant zou kunnen zijn gecreeerd. Als u het geverifieerde profiel wilt ophalen, wordt het `vst.myDataSource.authState` moet de waarde 1 (GEAUTHENTIFICEERD) hebben.

* U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plus-teken (+) en slash (/).

## De Attributen van de Klant van de toegang in de dienst van Mensen

1. In de [!DNL Adobe Experience Cloud], klikt u op het menupictogram ( ![menupictogram](/help/main/c-target/c-visitor-profile/assets/menu-icon.png) ) en klik vervolgens op **[!UICONTROL People]**.

   ![Mensen](/help/main/c-target/c-visitor-profile/assets/people.png)

1. Klik op de knop **[!UICONTROL Customer Attributes]** tab.

   ![Klantkenmerken, tabblad](/help/main/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Workflow voor klantkenmerken voor [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Voer de volgende stappen uit om CRM-gegevens te gebruiken in [!DNL Target], zoals hieronder wordt geïllustreerd:

![crm-workflow](/help/main/c-target/c-visitor-profile/assets/crm_workflow.png)

Gedetailleerde instructies voor het uitvoeren van elk van de volgende taken vindt u in [Een bron voor klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html) in de *Experience Cloud Services- en beheerdocumentatie*.

1. Maak een gegevensbestand.

   De klantengegevens van de uitvoer van uw CRM aan formaat CSV om een .csv- dossier tot stand te brengen. Er kan ook een zip- of gzip-bestand worden gemaakt om te uploaden. Zorg ervoor dat de eerste rij van het CSV-bestand de koptekst is en dat alle rijen (klantgegevens) hetzelfde aantal vermeldingen hebben.

   In de volgende afbeelding ziet u een voorbeeld van een bestand met klantgegevens voor de onderneming:

   ![crs-monster](/help/main/c-target/c-visitor-profile/assets/CRS_sample.png)

   In de volgende afbeelding ziet u een voorbeeld van een klant-CSV-bestand voor bedrijven:

   ![csv-monster](/help/main/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Maak de kenmerkbron en upload het gegevensbestand.

   Geef een naam en beschrijving op van de gegevensbron en de alias-id. De alias-id is een unieke id die moet worden gebruikt in de kenmerkcode van uw klant in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >De naam van de gegevensbron en de kenmerknaam mogen geen punt bevatten.

   Het gegevensbestand moet voldoen aan de vereisten voor het uploaden van het bestand en mag niet groter zijn dan 100 MB. Als uw bestand te groot is of als u gegevens hebt die op terugkerende basis moeten worden geüpload, kunt u in plaats daarvan FTP op uw bestanden toepassen.

   * **HTTPS:** You can drag-and-drop the .csv data file or click **[!UICONTROL Browse]** to upload from your file system.
   * **FTP:** Klik op de FTP-koppeling naar [het bestand uploaden via FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). First step is to provide a password for the Adobe-provided FTP server. Geef het wachtwoord op en klik vervolgens op **[!UICONTROL Done]**.

   Breng nu uw CSV/ZIP/GZIP-bestand over naar de FTP-server. Nadat deze bestandsoverdracht is gelukt, maakt u een bestand met dezelfde naam en een `.fin` extensie. Breng dit lege bestand over naar de server. Dit wijst op een eind van overdracht en [!DNL Experience Cloud] begint het gegevensbestand te verwerken.

1. Valideer het schema.

   Met het validatieproces kunt u weergavenamen en beschrijvingen toewijzen aan geüploade kenmerken (tekenreeksen, gehele getallen, getallen, enzovoort). Wijs elk attribuut aan zijn correct gegevenstype, vertoningsnaam, en beschrijving toe.

   Klikken **[!UICONTROL Save]** nadat de schemavalidatie volledig is. De uploadtijd van het bestand is afhankelijk van de grootte.

   ![Schema valideren](/help/main/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema uploaden](/help/main/c-target/c-visitor-profile/assets/upload1.png)

1. Configureer abonnementen en activeer de kenmerkbron.

   Klikken **[!UICONTROL Add Subscription]** Selecteer vervolgens de oplossing om deze kenmerken in te schrijven. [Abonnementen configureren](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) stelt de gegevensstroom in tussen de [!DNL Experience Cloud] en oplossingen. Door de kenmerkbron te activeren, kunnen de gegevens naar ingetekende oplossingen stromen. De klantrecords die u hebt geüpload, komen overeen met binnenkomende id-signalen van uw website of toepassing.

   ![Oplossing configureren](/help/main/c-target/c-visitor-profile/assets/solution.png)

   ![Activeren](/help/main/c-target/c-visitor-profile/assets/activate.png)

   Houd bij het uitvoeren van deze stap rekening met de volgende beperkingen:

   * De maximale bestandsgrootte voor elke upload met de HTTP-methode is 100 MB.
   * De maximale bestandsgrootte voor elke upload met de FTP-methode is 4 GB.
   * Het aantal kenmerken dat mag worden geabonneerd: 5 voor [!DNL Target Standard] en 200 voor [!DNL Target Premium].

## Klantkenmerken gebruiken in [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

U kunt klantkenmerken gebruiken in [!DNL Target] op de volgende manieren:

### Doelgroepen maken

In [!DNL Target], kunt u een klantkenmerk selecteren in het menu [!UICONTROL Visitor Profile] bij het maken van een publiek. Alle klantkenmerken hebben het voorvoegsel &lt; data_source_name > in de lijst. U kunt deze kenmerken desgewenst combineren met andere gegevenskenmerken om een publiek te maken.

![Target Audience](/help/main/c-target/c-visitor-profile/assets/TargetAudience.png)

### Profielscripts maken met behulp van tokens

Customer attributes can be referenced in profile scripts using format `crs.get('<Datasource Name>.<Attribute name>')`.

Dit profielscript kan rechtstreeks worden gebruikt in aanbiedingen voor het leveren van kenmerken die bij de huidige bezoeker horen.

### Using mbox3rdPartyID in your website for a successful implementation and usage

Voldoende `mbox3rdPartyId` als een parameter voor de algemene mbox in de `targetPageParams()` methode. De waarde van `mbox3rdPartyId` moet worden ingesteld op de klant-id die aanwezig was in het CSV-gegevensbestand.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### Using the Experience Cloud ID Service

If you are using the Experience Cloud ID service, you must set a Customer ID and Authentication State to use customer attributes in targeting. Zie voor meer informatie [Klant-id&#39;s en verificatiestatus](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in de *Help bij Experience Cloud ID-service*.

For more information about using customer attributes in [!DNL Target], see the following resources:

* [Create a customer attribute source and upload the data file](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in the *Experience Cloud Services and Administration documentation*

## Problemen die klanten vaak tegenkomen {#section_BE0F70E563F64294B17087DE2BC1E74C}

U zou de volgende kwesties kunnen ontmoeten wanneer het werken met klantenattributen en [!DNL Target].

>[!NOTE]
>
>Kwesties 1 en 2 veroorzaken ongeveer 60% van de problemen op dit gebied. Probleem 3 veroorzaakt ongeveer 30% van de problemen. Probleem 4 veroorzaakt ongeveer 5% van de problemen. De resterende 5% is te wijten aan diverse problemen.

### Uitgave 1: Klantkenmerken worden verwijderd omdat het profiel te groot is

There is no character limit on a particular field in the user&#39;s profile, but if the profile gets larger than 64 K, it is truncated by removing the oldest attributes until the profile is below 64 K again.

### Uitgave 2: Kenmerken die niet worden vermeld in de Audience Library in [!DNL Target], zelfs na enkele dagen

Dit is meestal een verbindingsprobleem met de pijplijn. As a resolution, ask your Customer Attributes team to republish the feed.

### Issue 3: Delivery not working based on the attribute

Het profiel is nog niet bijgewerkt op de rand. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Versie 4: Implementatievraagstukken

Houd rekening met de volgende implementatiekwesties:

* De bezoeker-id is niet correct doorgegeven. De id is doorgegeven `mboxMCGVID` in plaats van `setCustomerId`.
* De bezoekersidentiteitskaart werd correct overgegaan, maar de staat van de VERIFICATIE werd niet geplaatst aan voor authentiek verklaard.
* `mbox3rdPartyId` is niet correct doorgegeven.

### Uitgave 5: `mboxUpdate` niet correct uitgevoerd

`mboxUpdate`  is niet correct uitgevoerd met `mbox3rdPartyId`.

### Uitgave 6: Klantkenmerken worden niet geïmporteerd in [!DNL Target]

Als u de klantkenmerkgegevens niet kunt vinden in Target, dient u ervoor te zorgen dat de import heeft plaatsgevonden binnen de laatste *x* dagen *x* is het doel [Levensduur bezoekersprofiel](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) waarde (standaard 14 dagen).

## Trainingsvideo: Offlinegegevens uploaden met behulp van klantkenmerken ![Zelfstudie-badge](/help/main/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

This video shows you how to import offline CRM, help desk, point-of-sale, and other marketing data into the [!DNL Experience Cloud People] service and associate it with visitors using their known IDs.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
