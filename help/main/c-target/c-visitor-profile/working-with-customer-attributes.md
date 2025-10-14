---
keywords: klantenrelatiebeheer;de dienst van het klantenverslag;crs;crm;mbox3rdpartyid;klantenattributen;het richten;csv;crm;adobe ervaren wolken
description: Leer hoe te om de gegevens van de ondernemingsklant van een gegevensbestand van de klantenverhouding (CRM) voor inhoud te gebruiken richtend in  [!DNL Adobe Target].
title: Wat zijn klantkenmerken en hoe gebruik ik deze?
feature: Audiences
exl-id: 4a36230a-ae86-42a2-b6fe-60e7ab45e1a8
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 0%

---

# Klantkenmerken

Informatie over het gebruik van bedrijfsklantgegevens uit CRM-databases (Customer Relationship Management) voor het aanwijzen van inhoud in [!DNL Adobe Target] door gebruik te maken van klantkenmerken in de [!DNL Adobe Enterprise Cloud People] -service.

Gegevens van bedrijfsklanten die via meerdere bronnen zijn verzameld en in CRM-databases zijn opgeslagen, kunnen in [!DNL Target] worden gebruikt om strategisch de meest relevante inhoud aan klanten te leveren, waarbij de nadruk met name ligt op terugkerende klanten. Soorten publiek en klantkenmerken in de [!DNL People] -service (voorheen Profielen en Soorten publiek) brengen gegevensverzameling en -analyse samen met testen en optimaliseren, waardoor gegevens en inzichten actioneel worden.

## Overzicht van klantkenmerken {#section_B4099971FA4B48598294C56EAE86B45A}

[&#x200B; de Attributen van de Klant &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html?lang=nl-NL) in de [!DNL People] dienst maakt deel uit van [!DNL Adobe Experience Cloud] en verstrekt ondernemingen een hulpmiddel om hun klantengegevens aan het [!DNL Experience Cloud] platform te duwen.

Gegevens die aan de [!DNL Experience Cloud] zijn toegevoegd, zijn beschikbaar voor alle [!DNL Experience Cloud] -workflows. [!DNL Target] gebruikt deze gegevens voor het activeren van geretourneerde klanten op basis van kenmerken. [!DNL Adobe Analytics] verbruikt deze kenmerken en ze kunnen worden gebruikt voor analyse en segmentatie.

![&#x200B; crs voorbeeld &#x200B;](/help/main/c-target/c-visitor-profile/assets/crs.png)

Houd rekening met de volgende informatie als uw werk met klantkenmerken en [!DNL Target] :

* Er zijn enkele voorwaarden waaraan u moet voldoen voordat u de functie [!UICONTROL Customer attributes] in de service [!DNL People] kunt gebruiken. Voor meer informatie, zie &quot;Eerste vereisten voor het uploaden van de Attributen van de Klant&quot;in [&#x200B; attributen van de Klant &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html?lang=nl-NL#section_BD38693AFBF34926BA28E964963B4EA0) in de *Diensten van Experience Cloud en de documentatie van het Beleid*.
* Ben zich bewust van de beperkingen betreffende dossieruploads, zoals die in [&#x200B; over gegevensdossier en gegevensbronnen voor de Attributen van de Klant &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=nl-NL) in de *Centrale Gids van de Componenten van de Interface van Experience Cloud* worden gedocumenteerd. Als beste praktijken:

   * Upload enige grote dossiers (binnen de [&#x200B; gespecificeerde grenzen &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/crs-data-file.html?lang=nl-NL)). Enkelvoudige grote bestanden hebben de voorkeur boven meerdere kleinere bestanden.
   * Als u de upload in verscheidene dossiers moet verdelen, zorg ervoor dat de dossiers volledig worden verwerkt alvorens nieuwe dossiers voor te leggen. Zorg ervoor dat elk bestand in een batch volledig is verwerkt voordat u het volgende bestand in de batch verzendt.

* [!DNL Adobe] garandeert niet dat 100% van klantkenmerkgegevens (bezoekersprofiel) uit CRM-databases wordt opgenomen in de [!DNL Experience Cloud] en dus beschikbaar is voor gebruik in [!DNL Target] . In het huidige ontwerp bestaat de mogelijkheid dat een klein percentage gegevens (tot 0,1% van de grote productiepartijen) niet wordt ingecheckt.
* De levensduur van klantspecifieke gegevens die worden geïmporteerd van [!DNL Experience Cloud] naar [!DNL Target] , is afhankelijk van de levensduur van het bezoekersprofiel, standaard 14 dagen. Voor meer informatie, zie {het Leven van het Profiel van 0} Bezoeker [.](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD)
* Als de parameters `vst.*` het enige identificatiemiddel van de bezoeker zijn, wordt het bestaande &quot;geverifieerde&quot; profiel niet opgehaald zolang `authState` ONGEAUTHENTIFICEERD is (0). Het profiel wordt alleen afgespeeld als `authState` is gewijzigd in AUTHENTICATED (1).

  Als de parameter `vst.myDataSource.id` bijvoorbeeld wordt gebruikt om de bezoeker te identificeren (waarbij `myDataSource` de gegevensbronalias is) en er geen MCID of een id van een derde is, haalt het gebruik van de parameter `vst.myDataSource.authState=0` niet het profiel op dat mogelijk is gemaakt via het importeren van klantkenmerken. Als het gewenste gedrag het geverifieerde profiel moet ophalen, moet `vst.myDataSource.authState` de waarde 1 (GEAUTHENTIFICEERD) hebben.

* U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plusteken (+) en slash (/).

## De Attributen van de Klant van de toegang in de dienst van Mensen

1. In [!DNL Adobe Experience Cloud], klik het menupictogram ( ![&#x200B; menupictogram &#x200B;](/help/main/c-target/c-visitor-profile/assets/menu-icon.png) ) dan klik **[!UICONTROL People]**.

   ![&#x200B; Mensen &#x200B;](/help/main/c-target/c-visitor-profile/assets/people.png)

1. Klik op de tab **[!UICONTROL Customer Attributes]** .

   ![&#x200B; de Attributen tabel van de Klant &#x200B;](/help/main/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Workflow voor klantkenmerken voor [!DNL Target] {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Voer de volgende stappen uit om CRM-gegevens te gebruiken in [!DNL Target], zoals hieronder wordt geïllustreerd:

![&#x200B; crm werkschema &#x200B;](/help/main/c-target/c-visitor-profile/assets/crm_workflow.png)

De gedetailleerde instructies voor de voltooiing van elk van de volgende taken kunnen in [&#x200B; worden gevonden creeer een bron van de klantenattributen en upload het gegevensbestand &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/t-crs-usecase.html?lang=nl-NL) in *de Diensten en documentatie van het Beleid van Experience Cloud*.

1. Maak een gegevensbestand.

   De klantengegevens van de uitvoer van uw CRM aan formaat CSV om een .csv- dossier tot stand te brengen. Er kan ook een zip- of gzip-bestand worden gemaakt om te uploaden. Zorg ervoor dat de eerste rij van het CSV-bestand de koptekst is en dat alle rijen (klantgegevens) hetzelfde aantal vermeldingen hebben.

   In de volgende afbeelding ziet u een voorbeeld van een bestand met klantgegevens voor de onderneming:

   ![&#x200B; crs steekproef &#x200B;](/help/main/c-target/c-visitor-profile/assets/CRS_sample.png)

   In de volgende afbeelding ziet u een voorbeeld van een klant-CSV-bestand voor bedrijven:

   ![&#x200B; csv steekproef &#x200B;](/help/main/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Maak de kenmerkbron en upload het gegevensbestand.

   Geef een naam en beschrijving op van de gegevensbron en de alias-id. De alias-id is een unieke id die in de kenmerkcode van de klant in `VisitorAPI.js` moet worden gebruikt.

   >[!IMPORTANT]
   >
   >De naam van de gegevensbron en de kenmerknaam mogen geen punt bevatten.

   Het gegevensbestand moet voldoen aan de vereisten voor het uploaden van het bestand en mag niet groter zijn dan 100 MB. Als uw bestand te groot is of als u gegevens hebt die op terugkerende basis moeten worden geüpload, kunt u in plaats daarvan FTP op uw bestanden toepassen.

   * **HTTPS:** u kunt het .csv- gegevensdossier slepen-en-daling of klikken **[!UICONTROL Browse]** om van uw dossiersysteem te uploaden.
   * **FTP:** klik de verbinding van FTP aan [&#x200B; uploadt het dossier door FTP &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html?lang=nl-NL). De eerste stap bestaat uit het opgeven van een wachtwoord voor de door Adobe verschafte FTP-server. Geef het wachtwoord op en klik op **[!UICONTROL Done]** .

   Breng nu uw CSV/ZIP/GZIP-bestand over naar de FTP-server. Nadat deze bestandsoverdracht is gelukt, maakt u een bestand met dezelfde naam en met een extensie `.fin` . Breng dit lege bestand over naar de server. Dit geeft een einde aan de gegevensoverdracht aan en de [!DNL Experience Cloud] begint het gegevensbestand te verwerken.

1. Valideer het schema.

   Met het validatieproces kunt u weergavenamen en beschrijvingen toewijzen aan geüploade kenmerken (tekenreeksen, gehele getallen, getallen, enzovoort). Wijs elk attribuut aan zijn correct gegevenstype, vertoningsnaam, en beschrijving toe.

   Klik op **[!UICONTROL Save]** nadat de schemavalidatie is voltooid. De uploadtijd van het bestand is afhankelijk van de grootte.

   ![&#x200B; bevestigt schema &#x200B;](/help/main/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![&#x200B; uploadschema &#x200B;](/help/main/c-target/c-visitor-profile/assets/upload1.png)

1. Configureer abonnementen en activeer de kenmerkbron.

   Klik op **[!UICONTROL Add Subscription]** en selecteer vervolgens de oplossing om deze kenmerken in te schrijven. [&#x200B; vorm abonnementen &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html?lang=nl-NL) plaatsen omhoog de gegevensstroom tussen [!DNL Experience Cloud] en oplossingen. Door de kenmerkbron te activeren, kunnen de gegevens naar ingetekende oplossingen stromen. De klantrecords die u hebt geüpload, komen overeen met binnenkomende id-signalen van uw website of toepassing.

   ![&#x200B; vorm oplossing &#x200B;](/help/main/c-target/c-visitor-profile/assets/solution.png)

   ![&#x200B; activeer &#x200B;](/help/main/c-target/c-visitor-profile/assets/activate.png)

   Houd bij het uitvoeren van deze stap rekening met de volgende beperkingen:

   * De maximale bestandsgrootte voor elke upload met de HTTP-methode is 100 MB.
   * De maximale bestandsgrootte voor elke upload met de FTP-methode is 4 GB.
   * Het aantal kenmerken dat mag worden geabonneerd: 5 voor [!DNL Target Standard] en 200 voor [!DNL Target Premium] .

## Kenmerken van klant gebruiken in [!DNL Target] {#section_107E3A0F0EC7478E82E6DBD17B30B756}

U kunt klantkenmerken in [!DNL Target] op de volgende manieren gebruiken:

### Doelgroepen maken

In [!DNL Target], kunt u een klantenattribuut van de [!UICONTROL Visitor Profile] sectie selecteren wanneer het creëren van een publiek. Alle klantkenmerken hebben het voorvoegsel &lt; data_source_name > in de lijst. U kunt deze kenmerken desgewenst combineren met andere gegevenskenmerken om een publiek te maken.

![&#x200B; Doelpubliek van het Doel &#x200B;](/help/main/c-target/c-visitor-profile/assets/TargetAudience.png)

### Profielscripts maken met behulp van tokens

In profielscripts kan met de indeling `crs.get('<Datasource Name>.<Attribute name>')` naar de kenmerken van de klant worden verwezen.

Dit profielscript kan rechtstreeks worden gebruikt in aanbiedingen voor het leveren van kenmerken die bij de huidige bezoeker horen.

### Mbox3rdPartyID in uw website gebruiken voor een geslaagde implementatie en gebruik

Geef `mbox3rdPartyId` als een parameter door aan de algemene box binnen de methode `targetPageParams()` . De waarde van `mbox3rdPartyId` moet worden ingesteld op de klant-id die aanwezig was in het CSV-gegevensbestand.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### De Experience Cloud-id-service gebruiken

Als u de Experience Cloud-id-service gebruikt, moet u een klant-id en verificatiestatus instellen om klantkenmerken te gebruiken voor het opgeven van doelen. Voor meer informatie, zie [&#x200B; identiteitskaarts van de Klant en de Staat van de Authentificatie &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=nl-NL) in de *Hulp van de Dienst van identiteitskaart van Experience Cloud*.

Zie de volgende bronnen voor meer informatie over het gebruik van klantkenmerken in [!DNL Target] :

* [&#x200B; creeer een bron van het klantenattribuut en upload het gegevensbestand &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html?lang=nl-NL) in de *Diensten van Experience Cloud en de documentatie van het Beleid*

## Problemen die klanten vaak tegenkomen {#section_BE0F70E563F64294B17087DE2BC1E74C}

Als u met klantkenmerken en [!DNL Target] werkt, kunnen de volgende problemen optreden.

>[!NOTE]
>
>Kwesties 1 en 2 veroorzaken ongeveer 60% van de problemen op dit gebied. Probleem 3 veroorzaakt ongeveer 30% van de problemen. Probleem 4 veroorzaakt ongeveer 5% van de problemen. De resterende 5% is te wijten aan diverse problemen.

### Probleem 1: Klantkenmerken worden verwijderd omdat het profiel te groot is

Er is geen tekenlimiet voor een bepaald veld in het gebruikersprofiel, maar als het profiel groter is dan 64 kB, wordt het afgebroken door de oudste kenmerken te verwijderen totdat het profiel weer lager is dan 64 kB.

### Uitgave 2: Attributen die niet worden vermeld in de Audience Library in [!DNL Target], zelfs na enkele dagen

Dit is meestal een verbindingsprobleem met de pijplijn. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Versie 3: levering werkt niet op basis van het kenmerk

Het profiel is nog niet bijgewerkt op de rand. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Probleem 4: Implementatieproblemen

Houd rekening met de volgende implementatiekwesties:

* De bezoeker-id is niet correct doorgegeven. De id is doorgegeven in `mboxMCGVID` in plaats van `setCustomerId` .
* De bezoekersidentiteitskaart werd correct overgegaan, maar de staat van de VERIFICATIE werd niet geplaatst aan voor authentiek verklaard.
* `mbox3rdPartyId` is niet correct doorgegeven.

### Uitgave 5: `mboxUpdate` wordt niet correct uitgevoerd

`mboxUpdate` is niet correct uitgevoerd met `mbox3rdPartyId` .

### Versie 6: kenmerken van klanten worden niet geïmporteerd in [!DNL Target]

Als u de gegevens van de Attributen van de Klant in Doel niet kunt vinden, zorg ervoor dat de invoer binnen de laatste *x* dagen voorkwam waar *x* de waarde van het Levensduur van het Profiel van de Bezoeker [&#128279;](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) (14 dagen door gebrek) is.

## De video van de opleiding: Upload Off-line Gegevens gebruikend de badge van de Attributen van de Klant ![&#x200B; Zelfstudie &#x200B;](/help/main/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In deze video ziet u hoe u offline CRM, helpdesk, verkooppunt en andere marketinggegevens kunt importeren in de [!DNL Experience Cloud People] -service en deze kunt koppelen aan bezoekers die hun bekende id&#39;s gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
