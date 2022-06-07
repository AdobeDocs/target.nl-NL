---
keywords: toevoegen gebruiker;project;gebruikersgroep;eigenschappen;werkruimte;beheren eigenschap;eigenschap;at_eigenschap;rollen;machtigingen
description: Leer hoe u gebruikers aan Adobe Target kunt toevoegen. creëren werkruimten, gebruikersgroepen, en eigenschappen; de implementatie bij te werken; en geef rollen en machtigingen op.
title: Hoe kan ik bedrijfsmachtigingen configureren?
feature: Administration & Configuration
role: Admin
exl-id: 6494fc86-d2d3-4382-9d2e-63be435ba935
source-git-commit: 4251832a5983ea8950e54d52df5d27bf395894e0
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Bedrijfsmachtigingen configureren

Informatie over de taken die nodig zijn om gebruikers toe te voegen aan uw [!DNL Target] uitvoering; creëren werkruimten, gebruikersgroepen, en eigenschappen; update uw [!DNL Target] de tenuitvoerlegging `at_property` parameter; en geef rollen en machtigingen op.

>[!NOTE]
>
>Eigenschappen en machtigingen zijn beschikbaar als onderdeel van de [Doelpremie](/help/main/c-intro/intro.md#premium) oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder [!DNL Target Premium] licentie.

De volgende lijst maakt een lijst van de taken u zou moeten uitvoeren om eigenschappen tot stand te brengen en gebruikersrollen en toestemmingen toe te wijzen. Raadpleeg de onderstaande secties voor meer informatie over elke taak.

| Taak | Uitgevoerd in |
|--- |--- |
| 1. Gebruikers toevoegen (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Een werkruimte maken (productprofiel) | [!DNL Adobe Admin Console for Enterprise] |
| 3. Gebruikersgroepen maken (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Eigenschappen maken | [!DNL Target] UI |
| 5: Werk uw implementatie bij om de `at_property` parameter | [!DNL Target] UI, at.js-functies of -tags in [!DNL Adobe Experience Platform] |
| 6: Rollen en machtigingen opgeven | [!DNL Adobe Admin Console for Enterprise] |

Voor de taken die worden uitgevoerd in de [!DNL Adobe Admin Console for Enterprise], toegang tot de console door deze stappen te volgen:

1. Klik in Adobe Target op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** > **[!UICONTROL Assign Properties to Workspaces]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) > Meld u aan met uw Adobe ID als u zich nog niet hebt aangemeld.


1. (Voorwaardelijk) Als u toegang hebt tot de [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klik de gebruikersavatar in de juiste hoek of de hoogste navigatiebar, dan selecteer de gewenste organisatie.

## Stap 1. Gebruikers toevoegen (optioneel) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wanneer u de nieuwe [!UICONTROL Properties] functionaliteit, moet al gebruikersbeheer in [!DNL Adobe Admin Console for Enterprise]. Alle bestaande gebruikers in [!DNL Target] wordt gemigreerd van [!DNL Target] aan de [!DNL Admin Console for Enterprise].

1. [In de Admin Console](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE)klikt u op de knop **[!UICONTROL Users]** tab boven aan de pagina > **[!UICONTROL Add Users]** om nieuwe gebruikers te maken of om bestaande gebruikers te bewerken.
1. Volg de instructies in [Gebruikers en groepen beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de *Handleiding voor bedrijven*.

## Stap 2. Een werkruimte maken (productprofiel) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Met een werkruimte (productprofiel) kan een organisatie een specifieke set gebruikers toewijzen aan een specifieke set eigenschappen. In veel opzichten is een werkruimte vergelijkbaar met een rapportsuite in [!DNL Analytics].

Organisaties kunnen nu profiteren van de functionaliteit voor Enterprise-machtigingen door nieuwe werkruimten te maken binnen [!DNL Admin Console], toewijzen [!DNL Target] eigenschappen aan deze werkruimten, en het bewegen van gebruikers van de &quot;StandaardWerkruimte&quot;configuratie aan deze nieuwere, beperkte toegangswerkruimten.

De klanten kunnen deze werkruimten gebruiken om toegang tot verschillende teams door gebied, door bedrijfseenheid, door plaatsctie, of via een andere methode te scheiden zij kiezen.

Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen zelfs verschillende rollen binnen elke werkruimte hebben.

1. In de [!DNL Admin Console], klikt u op **[!UICONTROL Products]** en selecteert u vervolgens de naam van het gewenste product.

   ![werkruimte](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Maak de gewenste werkruimte (productprofiel):

   * **Standaardtoegang:** Alle bestaande activiteiten zullen in één enkel project worden samengevoegd genoemd &quot;StandaardToegang.&quot; Dit heeft geen invloed op klanten. Alle gebruikersrollen en functionaliteit zullen precies het zelfde blijven aangezien zij vóór deze verandering zijn.

      Alle activiteiten die via [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services], en [!DNL Target Classic] maakt ook deel uit van de werkruimte Standaardtoegang. U kunt momenteel geen projecten van &quot;Standaardtoegang&quot;aan een ander project bewegen.

   * **Nieuwe werkruimten (productprofielen):** U kunt beginnen uit de nieuwe toestemmingenfunctionaliteit voordeel te halen door het volgende te doen:

      * Nieuwe werkruimten maken in het dialoogvenster [!DNL Admin Console for Enterprise].
      * Doeleigenschappen toewijzen aan de werkruimten.

   U kunt deze werkruimten gebruiken om toegang tot verschillende teams te verdelen door gebied, bedrijfseenheid, plaatssectie, of via een andere methode u kiest. Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen verschillende rollen binnen elke werkruimte hebben.

1. Volg de instructies in [Productconfiguraties maken en beheren](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in de *Handleiding voor bedrijven*.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het configureren van werkruimten.

### Vraag uw werkruimte-id op {#workspace-id}

U moet de werkruimte-id doorgeven aan Enterprise-machtigingen in [Doel-API&#39;s](/help/main/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md).

1. In de [Adobe Admin Console](https://adminconsole.adobe.com)klikt u op de knop [!UICONTROL Products] klikt u op het product in het linkermenu om de lijst PLC (werkruimte) weer te geven.
1. Klik op de gewenste PLC (werkruimte) en zoek de id voor &quot;profielen&quot; in de URL, zoals hieronder wordt weergegeven.

   ![workspaceID](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Stap 3. Gebruikersgroepen maken (optioneel) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid alle aangewezen voorrechten over verschillende producten van de Adobe kan zo gemakkelijk zijn zoals het toevoegen van hen aan een specifieke gebruikersgroep.

1. Klik in de Admin Console op de knop **[!UICONTROL Users]** tab boven aan de pagina > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of om bestaande groepen te bewerken.
1. Volg de instructies in [Gebruikers en groepen van een productconfiguratie beheren](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in de *Handleiding voor bedrijven*.

## Stap 4. Eigenschappen maken {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschappen worden toegelaten door een specifiek naam/waardepaar als parameter met om het even welke vraag (de vraag van het Doel, api vraag, enz.) toe te voegen naar doel.

Eigenschappen behoren tot specifieke kanalen (Web, Mobiel, E-mail, en API/Overige).

**Tip**: Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

1. In [!DNL Target], klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de [!UICONTROL Properties] lijst.
1. Klikken **Eigenschap maken**.

   Vul de velden in:

   * **Naam eigenschap (vereist):** Geef een beschrijvende naam voor de eigenschap op.
   * **Omschrijving:** Geef een optionele beschrijving voor de eigenschap op.
   * **Kanaal:** Selecteer het gewenste kanaal voor de eigenschap: Web, Mobile App, Email of Other/API (bijvoorbeeld een set-top box of PlayStation-console).

1. Klikken **[!UICONTROL Copy]** om de code naar het klembord te kopiëren die u tijdens het uitvoeren van de stappen in [5: Werk Uw Implementatie bij om de parameter at_property op te nemen](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8).
1. Klikken **[!UICONTROL Save]** wanneer gereed.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

## Stap 5: Werk uw implementatie bij om de parameter at_property op te nemen {#section_9B17A59807A94712BE642942442EBBC8}

Als u de opdracht [!DNL Target] gebruiker-toestemmingenfunctionaliteit, moet u toevoegen `at_property` parameter aan om het even welke vraag die aanslaat [!DNL Target] (Aanroep van doel, api-aanroep, enz.).

**Om de `at_property` parametercode:**

1. (Voorwaardelijk) Gebruik de implementatiecode die u hebt gegenereerd en opgeslagen op het klembord tijdens het uitvoeren van de stappen in [4. Eigenschappen maken](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) en ga verder met stap 2.

   of

   In [!DNL Target], klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de [!UICONTROL Properties] lijst.

   1. Plaats de muisaanwijzer op de knop [!UICONTROL Last Updated] kolom voor de gewenste eigenschap die moet worden weergegeven en klik op de knop [!UICONTROL Code] pictogram.

      ![Code voor aanwijzen van eigenschap](/help/main/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klik met de rechtermuisknop op de gemarkeerde implementatiecode om deze naar het klembord te kopiëren.

1. Werk uw [!DNL Target] uitvoering met de in de vorige stap verkregen uitvoeringscode.

   Er zijn verschillende manieren om uw [!DNL Target] uitvoering. De volgende methoden kunnen bijvoorbeeld worden gebruikt voor webpagina&#39;s:

   * **Via een &quot;Aangepaste parameter&quot; in tags binnen [!DNL Adobe Experience Platform]:**

      Zie voor meer informatie [Mbox-parameters toevoegen](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=en#add-mbox-params) in de *Overzicht van codes* documentatie.

   * **Via de functie targetPageParamsAll():** Plaats de volgende code in de `<head>` -tags, boven de referentie at.js.

      ```javascript
      <script>
       function targetPageParamsAll() {
        return {
         "at_property": "5f8bd98b-1456-a84c-2a96-11s9b8e2b112"
        };
       }
      </script>
      ```

      Ga voor meer informatie over hoe u dit kunt doen met at.js naar [targetPageParamsAll](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md).

## Stap 6: Rollen en machtigingen opgeven {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klik in de Admin Console op **[!UICONTROL Products]** en selecteert u vervolgens de naam van het gewenste product.

   ![Werkruimte](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de naam van het gewenste profiel (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Klik op **[!UICONTROL Users]**.

   De [!UICONTROL Users] worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste machtigingenrol (fiatteur, Editor, waarnemer of uitgever) door de vervolgkeuzelijst voor elke gebruiker in het dialoogvenster [!UICONTROL Product Role] kolom.

   ![Vervolgkeuzelijst Productrol](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

   Zie voor meer informatie [Productmachtigingen en -rollen beheren in de Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de *Handleiding voor bedrijven*.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video&#39;s is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

### Adobe Target-werkruimten configureren (6:55) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

In deze video wordt uitgelegd hoe u werkruimten kunt maken.

* Toegang tot de Adobe Admin Console vanaf de Adobe Target-interface (3 manieren)
* Een werkruimte configureren in Adobe Admin Console

   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten

* Standaardwerkruimten begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Eigenschappen maken in Adobe Target (3:05) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

* Hoe te om een bezit binnen te creëren [!DNL Adobe Target] interface
* Hoe te om een bezitstoken te produceren om in uw bezitsimplementatie te omvatten
* Verken uzelf met de drie implementatiemethoden:

   * Web
   * Mobiele app
   * Aanroepen via e-mail, set top box of API

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
