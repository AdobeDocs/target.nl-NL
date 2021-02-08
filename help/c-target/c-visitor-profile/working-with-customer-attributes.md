---
keywords: klantenrelatiebeheer;de dienst van het klantenverslag;crs;crm;mbox3rdpartyid;klantenattributen;het richten;csv;crm;adobe ervaren wolken
description: Leer hoe u bedrijfsklantgegevens uit een CRM-database (Customer relationship management) kunt gebruiken voor inhoud die op Adobe Target is gericht.
title: Wat zijn klantkenmerken en hoe gebruik ik deze?
feature: Audiences
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1490'
ht-degree: 0%

---


# Klantkenmerken

Informatie over het gebruik van bedrijfsklantgegevens uit databases van Customer Relationship Management (CRM) voor het aanwijzen van inhoud in [!DNL Adobe Target] door gebruik te maken van klantkenmerken in de [!DNL Adobe Enterprise Cloud People]-service.

Gegevens van bedrijfsklanten die via meerdere bronnen zijn verzameld en in CRM-databases zijn opgeslagen, kunnen in [!DNL Target] worden gebruikt om strategisch de meest relevante inhoud aan klanten te leveren, waarbij de nadruk met name ligt op terugkerende klanten. Soorten publiek en klantkenmerken in de [!DNL People]-service (voorheen Profielen en Soorten publiek) brengen gegevensverzameling en -analyse samen met testen en optimaliseren, waardoor gegevens en inzichten actioneel worden.

## Overzicht van klantkenmerken {#section_B4099971FA4B48598294C56EAE86B45A}

[Klantkenmerken ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html) in de  [!DNL People] service maken deel uit van de service  [!DNL Adobe Experience Cloud] en bieden bedrijven een tool om hun klantgegevens naar het  [!DNL Experience Cloud] platform te verzenden.

Gegevens die op [!DNL Experience Cloud] zijn ingevoerd, zijn beschikbaar voor alle [!DNL Experience Cloud]-workflows. [!DNL Target] gebruikt deze gegevens voor het richten van terugkerende klant die op attributen wordt gebaseerd. [!DNL Adobe Analytics] verbruikt deze kenmerken en kunnen worden gebruikt voor analyse en segmentatie.

![crs-voorbeeld](/help/c-target/c-visitor-profile/assets/crs.png)

Neem de volgende informatie in overweging als uw werk met klantkenmerken en [!DNL Target]:

* Er zijn enkele voorwaarden waaraan u moet voldoen voordat u de functie [!UICONTROL Customer attributes] in de service [!DNL People] kunt gebruiken. Zie &quot;Eerste vereisten voor het uploaden van klantkenmerken&quot; in [Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/attributes.html#section_BD38693AFBF34926BA28E964963B4EA0) in de *Experience Cloud Services and Administration documentatie* voor meer informatie.

   >[!NOTE]
   >
   >[!DNL at.js] (elke versie) of  [!DNL mbox.js] versie 58 of hoger is vereist.

* [!DNL Adobe] garandeert niet dat 100% van gegevens van klantkenmerken (bezoekersprofiel) uit CRM-databases aan de klant worden doorgegeven  [!DNL Experience Cloud] en dus beschikbaar zijn voor gebruik bij  [!DNL Target]de klant. In ons huidige ontwerp bestaat de mogelijkheid dat een klein percentage gegevens (tot 0,1% van de grote productiepartijen) niet wordt ingecheckt.
* De levensduur van klantgegevens die worden geïmporteerd van [!DNL Experience Cloud] naar [!DNL Target], is afhankelijk van de levensduur van het bezoekersprofiel, die standaard 14 dagen is. Zie [Levensduur bezoekersprofiel](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md#concept_D9F21B416F1F49159F03036BA2DD54FD) voor meer informatie.
* Als de parameters `vst.*` het enige element zijn dat de bezoeker identificeert, wordt het bestaande &quot;geverifieerde&quot; profiel niet opgehaald zolang `authState` ONGEAUTHENTIFICEERD is (0). Het profiel wordt alleen in werking gesteld als `authState` is gewijzigd in AUTHENTICATED (1).

   Als de parameter `vst.myDataSource.id` bijvoorbeeld wordt gebruikt om de bezoeker te identificeren (waarbij `myDataSource` de gegevensbronalias is) en er geen MCID of derde-id is, haalt het gebruik van de parameter `vst.myDataSource.authState=0` niet het profiel op dat mogelijk is gemaakt via het importeren van klantkenmerken. Als het gewenste gedrag het voor authentiek verklaarde profiel moet halen, `vst.myDataSource.authState` moet de waarde van 1 (GEAUTHENTIFICEERD) hebben.

* U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plus-teken (+) en slash (/).

## De Attributen van de Klant van de toegang in de dienst van Mensen

1. Klik in [!DNL Adobe Experience Cloud] op het menupictogram ( ![menupictogram](/help/c-target/c-visitor-profile/assets/menu-icon.png) ) en klik vervolgens op **[!UICONTROL People]**.

   ![Mensen](/help/c-target/c-visitor-profile/assets/people.png)

1. Klik op het tabblad **[!UICONTROL Customer Attributes]**.

   ![Klantkenmerken, tabblad](/help/c-target/c-visitor-profile/assets/customer-attributes-tab.png)

## Workflow voor klantkenmerken voor doel {#section_00DAE94DA9BA41398B6FD170BC7D38A3}

Voer de volgende stappen uit om CRM-gegevens te gebruiken in [!DNL Target], zoals hieronder wordt geïllustreerd:

![crm-workflow](/help/c-target/c-visitor-profile/assets/crm_workflow.png)

Gedetailleerde instructies voor het uitvoeren van elk van de volgende taken vindt u in [Een bron van klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in de *Experience Cloud Services and Administration documentation*.

1. Maak een gegevensbestand.

   De klantengegevens van de uitvoer van uw CRM aan formaat CSV om een .csv- dossier tot stand te brengen. Er kan ook een zip- of gzip-bestand worden gemaakt om te uploaden. Zorg ervoor dat de eerste rij van het CSV-bestand de koptekst is en dat alle rijen (klantgegevens) hetzelfde aantal vermeldingen hebben.

   In de volgende afbeelding ziet u een voorbeeld van een bestand met klantgegevens voor de onderneming:

   ![crs-monster](/help/c-target/c-visitor-profile/assets/CRS_sample.png)

   In de volgende afbeelding ziet u een voorbeeld van een klant-CSV-bestand voor bedrijven:

   ![csv-monster](/help/c-target/c-visitor-profile/assets/CRS_CSV_sample.png)

1. Maak de kenmerkbron en upload het gegevensbestand.

   Geef een naam en beschrijving op van de gegevensbron en de alias-id. De alias-id is een unieke id die moet worden gebruikt in de kenmerkcode van de klant in `VisitorAPI.js`.

   >[!IMPORTANT]
   >
   >De naam van de gegevensbron en de kenmerknaam mogen geen punt bevatten.

   Het gegevensbestand moet voldoen aan de vereisten voor het uploaden van bestanden en mag niet groter zijn dan 100 MB. Als het bestand te groot is of als u gegevens hebt die u regelmatig wilt uploaden, kunt u in plaats daarvan FTP op uw bestanden toepassen.

   * **HTTPS:** U kunt het CSV-gegevensbestand slepen en neerzetten of klikken  **[!UICONTROL Browse]** om te uploaden vanaf uw bestandssysteem.
   * **FTP:** klik op de FTP-koppeling om het bestand te  [uploaden via FTP](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-upload-attributes-ftp.html). De eerste stap bestaat uit het opgeven van een wachtwoord voor de door Adobe verschafte FTP-server. Geef het wachtwoord op en klik op **[!UICONTROL Done]**.

   Breng nu uw CSV/ZIP/GZIP-bestand over naar de FTP-server. Nadat deze bestandsoverdracht is gelukt, maakt u een nieuw bestand met dezelfde naam en extensie .fin. Breng dit lege bestand over naar de server. Dit geeft een einde aan de gegevensoverdracht aan en de [!DNL Experience Cloud] verwerkt het gegevensbestand.

1. Valideer het schema.

   Met het validatieproces kunt u weergavenamen en beschrijvingen toewijzen aan geüploade kenmerken (tekenreeksen, gehele getallen, getallen, enzovoort). Wijs elk attribuut aan zijn correct gegevenstype, vertoningsnaam, en beschrijving toe.

   Klik **[!UICONTROL Save]** nadat de schemabevestiging volledig is. De uploadtijd van het bestand is afhankelijk van de grootte.

   ![Schema valideren](/help/c-target/c-visitor-profile/assets/SchemaValidate.png)

   ![Schema uploaden](/help/c-target/c-visitor-profile/assets/upload1.png)

1. Configureer abonnementen en activeer de kenmerkbron.

   Klik **[!UICONTROL Add Subscription]**, dan selecteer de oplossing om deze attributen in te tekenen. [Vorm ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/subscription.html) abonnementen omhoog de gegevensstroom tussen de  [!DNL Experience Cloud] en oplossingen. Door de kenmerkbron te activeren, kunnen de gegevens naar ingetekende oplossingen stromen. De klantrecords die u hebt geüpload, komen overeen met binnenkomende id-signalen van uw website of toepassing.

   ![Oplossing configureren](/help/c-target/c-visitor-profile/assets/solution.png)

   ![Activeren](/help/c-target/c-visitor-profile/assets/activate.png)

   Houd bij het uitvoeren van deze stap rekening met de volgende beperkingen:

   * De maximale bestandsgrootte voor elke upload met de HTTP-methode is 100 MB.
   * De maximale bestandsgrootte voor elke upload met de FTP-methode is 4 GB.
   * Het aantal kenmerken dat mag worden geabonneerd: 5 voor [!DNL Target Standard] en 200 voor [!DNL Target Premium].

## Klantkenmerken gebruiken in doel {#section_107E3A0F0EC7478E82E6DBD17B30B756}

U kunt klantkenmerken op de volgende manieren gebruiken:[!DNL Target]

### Doelgroepen maken

In [!DNL Target], kunt u een klantenattribuut van &lt;a1 selecteren/> sectie wanneer het creëren van een publiek. [!UICONTROL Visitor Profile] Alle klantkenmerken hebben het voorvoegsel &lt; data_source_name > in de lijst. U kunt deze kenmerken desgewenst combineren met andere gegevenskenmerken om een publiek te maken.

![Doelpubliek](/help/c-target/c-visitor-profile/assets/TargetAudience.png)

### Profielscripts maken met behulp van tokens

In profielscripts kan met de notatie `crs.get('<Datasource Name>.<Attribute name>')` naar de kenmerken van de klant worden verwezen.

Dit profielscript kan rechtstreeks worden gebruikt in aanbiedingen voor het leveren van kenmerken die bij de huidige bezoeker horen.

### Mbox3rdPartyID in uw website gebruiken voor een geslaagde implementatie en gebruik

Geef `mbox3rdPartyId` als parameter aan globale mbox binnen de `targetPageParams()` methode door. De waarde van `mbox3rdPartyId` moet worden ingesteld op de klant-id die aanwezig was in het CSV-gegevensbestand.

```javascript
<script type="text/javascript">
            function targetPageParams() {
               return 'mbox3rdPartyId=2000578';
            }
</script>
```

### De Experience Cloud ID-service gebruiken

Als u de dienst van identiteitskaart van de Experience Cloud gebruikt, moet u een identiteitskaart van de Klant en de Staat van de Authentificatie plaatsen om klantenattributen in het richten te gebruiken. Voor meer informatie, zie [Klantidentiteitskaart en de Staat van de Authentificatie ](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html) in *Experience Cloud ID de Hulp van de Dienst*.

Zie de volgende bronnen voor meer informatie over het gebruik van klantkenmerken in [!DNL Target]:

* [Creeer een bron van de klantenattributen en upload het gegevensdossier ](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html) in de documentatie van de Diensten van  *Experience Cloud en van het Beleid*
* [Klantkenmerken: Hoe meer u weet, des te beter u ](https://blogs.adobe.com/digitalmarketing/analytics/customer-attributes-know-better-connect/) verbindt de  *Digitale Marketing Blog*

## Problemen die klanten vaak tegenkomen {#section_BE0F70E563F64294B17087DE2BC1E74C}

Als u met klantkenmerken en [!DNL Target] werkt, kunnen de volgende problemen optreden.

>[!NOTE]
>
>Kwesties 1 en 2 veroorzaken ongeveer 60% van de problemen op dit gebied. Probleem 3 veroorzaakt ongeveer 30% van de problemen. Probleem 4 veroorzaakt ongeveer 5% van de problemen. De resterende 5% is te wijten aan diverse problemen.

### Uitgave 1: Klantkenmerken worden verwijderd omdat het profiel te groot is

Er is geen tekenlimiet voor een bepaald veld in het gebruikersprofiel, maar als het profiel groter wordt dan 64 kB, wordt het afgebroken door de oudste kenmerken te verwijderen totdat het profiel weer lager is dan 64 kB.

### Uitgave 2: Kenmerken die niet worden vermeld in de Audience Library in [!DNL Target], zelfs na enkele dagen

Dit is meestal een verbindingsprobleem met de pijplijn. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Versie 3: Aflevering werkt niet op basis van het kenmerk

Het profiel is nog niet bijgewerkt op de rand. Vraag uw Customer Attributes-team dan om de feed opnieuw te publiceren.

### Versie 4: Implementatievraagstukken

Houd rekening met de volgende implementatiekwesties:

* De bezoeker-id is niet correct doorgegeven. De id is doorgegeven in `mboxMCGVID` in plaats van `setCustomerId`.
* De bezoekersidentiteitskaart werd correct overgegaan, maar de staat van de VERIFICATIE werd niet geplaatst aan voor authentiek verklaard.
* `mbox3rdPartyId` is niet correct doorgegeven.

### Uitgave 5: `mboxUpdate` is niet correct uitgevoerd

`mboxUpdate`  is niet correct uitgevoerd met  `mbox3rdPartyId`.

### Uitgave 6: Klantkenmerken worden niet geïmporteerd in [!DNL Target]

Als u de klantkenmerkgegevens niet kunt vinden in Target, dient u ervoor te zorgen dat de import heeft plaatsgevonden binnen de laatste *x* dagen waarbij *x* de waarde [Levensduur bezoekersprofiel](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) is (standaard ingesteld op 14 dagen).

## Trainingsvideo: Offlinegegevens uploaden met behulp van klantkenmerken ![Zelfstudie-badge](/help/assets/tutorial.png) {#section_9A4E0FA0D0934D06BD8D5BFA673E9BD8}

In deze video ziet u hoe u offline CRM, helpdesk, verkooppunt en andere marketinggegevens kunt importeren in de [!DNL Experience Cloud People]-service en deze kunt koppelen aan bezoekers die hun bekende id&#39;s gebruiken.

>[!VIDEO](https://video.tv.adobe.com/v/17802t1/)
