---
keywords: add user;project;user group;properties;workspace;manage property;property;at_property;roles;permissions
description: Informatie over de taken die vereist zijn om gebruikers toe te voegen aan uw Adobe Target-implementatie. creëren werkruimten, gebruikersgroepen, en eigenschappen; werk uw implementatie van het Doel bij om de parameter te omvatten at_property; en geef rollen en machtigingen op.
title: Bedrijfsmachtigingen configureren
feature: user management
subtopic: Getting Started
uuid: 2f44ecd5-5c43-49c3-b1c3-58d28531c859
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '1443'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -bedrijfsmachtigingen configureren{#configure-enterprise-permissions}

Informatie over de taken die vereist zijn om gebruikers aan uw [!DNL Target] implementatie toe te voegen. creëren werkruimten, gebruikersgroepen, en eigenschappen; de [!DNL Target] implementatie bijwerken en de `at_property` parameter opnemen; en geef rollen en machtigingen op.

>[!NOTE]
>
>De eigenschappen en de Toestemmingsfunctionaliteit zijn beschikbaar als deel van de [Oplossing van de Premie](/help/c-intro/intro.md#premium) van het Doel. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.

De volgende lijst maakt een lijst van de taken u zou moeten uitvoeren om eigenschappen tot stand te brengen en gebruikersrollen en toestemmingen toe te wijzen. Raadpleeg de onderstaande secties voor meer informatie over elke taak.

| Taak | Uitgevoerd in |
|--- |--- |
| 1. Gebruikers toevoegen (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Een werkruimte maken (productprofiel) | [!DNL Adobe Admin Console for Enterprise] |
| 3. Gebruikersgroepen maken (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Eigenschappen maken | [!DNL Target] UI |
| 5: De implementatie bijwerken en de `at_property` parameter opnemen | [!DNL Target] UI, at.js-functies, [!DNL Adobe Launch]of [!DNL Dynamic Tag Management] |
| 6: Rollen en machtigingen opgeven | [!DNL Adobe Admin Console for Enterprise] |

Voor die taken die in [!DNL Adobe Admin Console for Enterprise]worden uitgevoerd, heb toegang tot de console door deze stappen te volgen:

1. Klik in Adobe Target op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** > **[!UICONTROL Assign Properties to Workspaces]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) > Meld u aan met uw Adobe ID, als u zich nog niet hebt aangemeld.


1. (Voorwaardelijk) Als u toegang hebt tot de sjabloon [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klikt u op de gebruikersavatar in de rechterhoek of op de bovenste navigatiebalk en selecteert u de gewenste organisatie.

## Stap 1. Gebruikers toevoegen (optioneel) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wanneer u de nieuwe [!UICONTROL Properties] functionaliteit gaat gebruiken, moet al gebruikersbeheer in [!DNL Adobe Admin Console for Enterprise]de toepassing worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter van [!DNL Target] naar [!DNL Admin Console for Enterprise].

1. [Klik in de Admin Console](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE)op het **[!UICONTROL Users]** tabblad boven aan de pagina > **[!UICONTROL Add Users]** om nieuwe gebruikers te maken of bestaande gebruikers te bewerken.
1. Volg de instructies in Gebruikers en groepen [beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in de gebruikershandleiding *van de* onderneming.

## Stap 2. Een werkruimte maken (productprofiel) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Met een werkruimte (productprofiel) kan een organisatie een specifieke set gebruikers toewijzen aan een specifieke set eigenschappen. In veel opzichten is een werkruimte vergelijkbaar met een rapportsuite in [!DNL Analytics].

Organisaties kunnen profiteren van de functionaliteit voor Enterprise-machtigingen door nieuwe werkruimten binnen te maken, [!DNL Admin Console][!DNL Target] eigenschappen toe te wijzen aan deze werkruimten en gebruikers van de configuratie &quot;Standaardwerkruimte&quot; over te brengen naar deze nieuwere werkruimten met beperkte toegang.

De klanten kunnen deze werkruimten gebruiken om toegang tot verschillende teams door gebied, door bedrijfseenheid, door plaatsctie, of via een andere methode te scheiden zij kiezen.

Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen zelfs verschillende rollen binnen elke werkruimte hebben.

1. Klik in het [!DNL Admin Console]dialoogvenster op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![werkruimte](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Maak de gewenste werkruimte (productprofiel):

   * **Standaardtoegang:** Alle bestaande activiteiten zullen in één enkel project worden samengevoegd genoemd &quot;StandaardToegang.&quot; Dit heeft geen invloed op klanten. Alle gebruikersrollen en functionaliteit zullen precies het zelfde blijven aangezien zij vóór deze verandering zijn.

      Alle activiteiten die zijn gemaakt via [!DNL Adobe Experience Manager] (AEM) [!DNL Adobe Mobile Services]en [!DNL Target Classic] maken ook deel uit van de werkruimte Standaardtoegang. U kunt momenteel geen projecten van &quot;Standaardtoegang&quot;aan een ander project bewegen.

   * **Nieuwe werkruimten (productprofielen):** U kunt beginnen uit de nieuwe toestemmingenfunctionaliteit voordeel te halen door het volgende te doen:

      * Nieuwe werkruimten maken in de [!DNL Admin Console for Enterprise]werkruimte.
      * Doeleigenschappen toewijzen aan de werkruimten.

   U kunt deze werkruimten gebruiken om toegang tot verschillende teams te verdelen door gebied, bedrijfseenheid, plaatssectie, of via een andere methode u kiest. Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen verschillende rollen binnen elke werkruimte hebben.

1. Volg de instructies in de [Create and Manage Product Configurations](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in de *Gids* van de Gebruiker van de Onderneming.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het configureren van werkruimten.

### Vraag uw werkruimte-id op {#workspace-id}

U moet de werkruimte-id doorgeven aan de Enterprise-machtigingen in [doel-API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md).

1. Klik in de [Adobe Admin Console](https://adminconsole.adobe.com)op het [!UICONTROL Products] tabblad en klik vervolgens op het product in het linkermenu om de lijst PLC (werkruimte) weer te geven.
1. Klik op de gewenste PLC (werkruimte) en zoek de id voor &quot;profielen&quot; in de URL, zoals hieronder wordt weergegeven.

   ![workspaceID](/help/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Stap 3. Gebruikersgroepen maken (optioneel) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid alle aangewezen voorrechten over verschillende producten van de Adobe kan zo gemakkelijk zijn zoals het toevoegen van hen aan een specifieke gebruikersgroep.

1. Klik in de Admin Console op het **[!UICONTROL Users]** tabblad boven aan de pagina > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of bestaande groepen te bewerken.
1. Volg de instructies in Gebruikers en groepen van een productconfiguratie [](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) beheren in de gebruikershandleiding *van de* onderneming.

## Stap 4. Eigenschappen maken {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschappen worden toegelaten door een specifiek naam/waardepaar als parameter met om het even welke vraag (de vraag van het Doel, api vraag, enz.) toe te voegen naar doel.

Eigenschappen behoren tot specifieke kanalen (Web, Mobiel, E-mail, en API/Overige).

**Tip**: Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

1. Klik [!DNL Target]in **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de [!UICONTROL Properties] lijst weer te geven.
1. Klik op Eigenschap **** maken.

   ![Nieuwe eigenschap, dialoogvenster](/help/administrating-target/c-user-management/property-channel/assets/new_property1.png)

   Vul de velden in:

   * **Naam eigenschap (vereist):** Geef een beschrijvende naam voor de eigenschap op.
   * **Omschrijving:** Geef een optionele beschrijving voor de eigenschap op.
   * **Kanaal:** Selecteer het gewenste kanaal voor de eigenschap: Web, Mobile App, Email of Other/API (bijvoorbeeld een set-top box of PlayStation-console).

1. Klik **[!UICONTROL Copy]** om de code naar uw klembord te kopiëren die u tijdens het uitvoeren van de stappen in [5 zult gebruiken: Werk uw Implementatie bij om de parameter](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8)at_property op te nemen.
1. Klik **[!UICONTROL Save]** wanneer gereed.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

## Stap 5: Werk uw implementatie bij om de parameter at_property op te nemen {#section_9B17A59807A94712BE642942442EBBC8}

Om de gebruiker-toestemmingsfunctionaliteit te gebruiken, moet u de [!DNL Target] parameter aan om het even welke vraag toevoegen die `at_property` [!DNL Target] (de vraag van het Doel, api vraag, enz.) aanslaat.

**U verkrijgt als volgt de`at_property`parametercode:**

1. (Voorwaardelijk) gebruik de implementatiecode u aan uw klembord produceerde en opsloeg terwijl het uitvoeren van de stappen in [4. Maak eigenschappen](../../../administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) en ga verder met stap 2.

   of

   Klik [!DNL Target]in **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de [!UICONTROL Properties] lijst weer te geven.

   1. Houd de muisaanwijzer boven de [!UICONTROL Last Updated] kolom zodat de gewenste eigenschap wordt weergegeven en klik op het [!UICONTROL Code] pictogram.

      ![Code voor aanwijzen van eigenschap](/help/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klik met de rechtermuisknop op de gemarkeerde implementatiecode om deze naar het klembord te kopiëren.

      ![Eigenschappencode](/help/administrating-target/c-user-management/property-channel/assets/code_property_2_new.png)

1. Werk uw [!DNL Target] implementatie bij met de implementatiecode die in de vorige stap is verkregen.

   Er zijn verschillende manieren om uw [!DNL Target] implementatie bij te werken. De volgende methoden kunnen bijvoorbeeld worden gebruikt voor webpagina&#39;s:

   * **Via een &quot;Algemene parameter in[!DNL Adobe Launch]:**

      Voor meer informatie, zie [Voeg Globale Params](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension#add-global-mbox-params) van het Doel in de documentatie van *Adobe Experience Platform Launch* toe.

   * **Via een &quot;globale parameter&quot; in[!DNL Dynamic Tag Management]:**

      ![](assets/property_token_2.png)

      Voor meer informatie, zie [Globale Parameters - Adobe Target](https://docs.adobe.com/content/help/en/dtm/using/tools-reference/target.html#global-parameters---adobe-target) in de *Dynamische Documentatie* van het Product van het Beheer van de Markering.

   * **Via de functie targetPageParams():** Plaats de volgende code in de <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"> -tags, boven de referentie at.js of mbox.js.

      ![](assets/property_token_1.png)

      Zie [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md)voor meer informatie over hoe u dit met at.js kunt doen.

   * **Via de functie mboxCreate():**

      ![](assets/property_token_3.png)

      Zie [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) en [mboxCreate(mbox,params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)voor meer informatie over hoe u dit met at.js kunt doen.

## Stap 6: Rollen en machtigingen opgeven {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klik in de Admin Console **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![Werkruimte](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de naam van het gewenste profiel (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Klik op **[!UICONTROL Users]**.

   Op het [!UICONTROL Users] tabblad worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste toestemmingenrol (Approver, Redacteur, Waarnemer, of Uitgever) door de drop-down lijst voor elke gebruiker in de [!UICONTROL Product Role] kolom te gebruiken.

   ![Vervolgkeuzelijst Productrol](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

   Zie [Productmachtigingen en -rollen beheren in de Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de gebruikershandleiding *van de* onderneming voor meer informatie.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] menu (voorheen [!UICONTROL Administration] [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video&#39;s is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

### Hoe te om de badge van de ![Zelfstudie van de Werkruimten van het Doel (6:55) te vormen](/help/assets/tutorial.png)

In deze video wordt uitgelegd hoe u werkruimten kunt maken.

* Toegang tot de Adobe Admin Console vanaf de Adobe Target-interface (3 manieren)
* Een werkruimte configureren in Adobe Admin Console

   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten

* Standaardwerkruimten begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Eigenschappen maken in Adobe Target (3:05), badge voor ![zelfstudie](/help/assets/tutorial.png)

* Hoe te om een bezit binnen de [!DNL Adobe Target] interface te creëren
* Hoe te om een bezitstoken te produceren om in uw bezitsimplementatie te omvatten
* Verken uzelf met de drie implementatiemethoden:

   * Web
   * Mobiele app
   * Aanroepen via e-mail, set top box of API

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
