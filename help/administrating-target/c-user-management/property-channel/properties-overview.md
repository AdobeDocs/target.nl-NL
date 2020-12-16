---
keywords: add user;project;user group;properties;workspace;manage property;property;at_property;roles;permissions
description: Informatie over de taken die vereist zijn om gebruikers toe te voegen aan uw Adobe Target-implementatie. creëren werkruimten, gebruikersgroepen, en eigenschappen; werk uw implementatie van het Doel bij om de parameter te omvatten at_property; en geef rollen en machtigingen op.
title: Bedrijfsmachtigingen configureren
feature: user management
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1441'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMConfigureren bedrijfsmachtigingen{#configure-enterprise-permissions}

Informatie over de taken die worden vereist om gebruikers aan uw [!DNL Target] implementatie toe te voegen; creëren werkruimten, gebruikersgroepen, en eigenschappen; uw [!DNL Target]-implementatie bijwerken en de `at_property`-parameter opnemen; en geef rollen en machtigingen op.

>[!NOTE]
>
>Eigenschappen en de functionaliteit van Toestemmingen is beschikbaar als deel van [de Oplossing van de Premium ](/help/c-intro/intro.md#premium) van het Doel. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.

De volgende lijst maakt een lijst van de taken u zou moeten uitvoeren om eigenschappen tot stand te brengen en gebruikersrollen en toestemmingen toe te wijzen. Raadpleeg de onderstaande secties voor meer informatie over elke taak.

| Taak | Uitgevoerd in |
|--- |--- |
| 1. Gebruikers toevoegen (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| 2. Een werkruimte maken (productprofiel) | [!DNL Adobe Admin Console for Enterprise] |
| 3. Gebruikersgroepen maken (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| 4. Eigenschappen maken | [!DNL Target] UI |
| 5: Werk uw implementatie bij om de parameter `at_property` op te nemen | [!DNL Target] UI, at.js-functies,  [!DNL Adobe Launch]of  [!DNL Dynamic Tag Management] |
| 6: Rollen en machtigingen opgeven | [!DNL Adobe Admin Console for Enterprise] |

Voor die taken die in [!DNL Adobe Admin Console for Enterprise] worden uitgevoerd, toegang tot de console door deze stappen te volgen:

1. Klik in Adobe Target op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** > **[!UICONTROL Assign Properties to Workspaces]**.

   of

   Ga naar [https://adminconsole.adobe.com/enterprise](https://adminconsole.adobe.com/enterprise/) > aanmelden met uw Adobe ID, als u zich nog niet hebt aangemeld.


1. (Voorwaardelijk) als u toegang tot [!DNL Admin Console for Enterprise] voor meer dan één organisatie hebt, klik de gebruikersavatar in de juiste hoek of de hoogste navigatiebar, dan selecteer de gewenste organisatie.

## Stap 1. Gebruikers toevoegen (optioneel) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wanneer u de nieuwe [!UICONTROL Properties] functionaliteit gaat gebruiken, moet al gebruikersbeheer in [!DNL Adobe Admin Console for Enterprise] worden uitgevoerd. Alle bestaande gebruikers in [!DNL Target] worden echter gemigreerd van [!DNL Target] naar [!DNL Admin Console for Enterprise].

1. [Klik in de Admin Console](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE) op de  **[!UICONTROL Users]** tab boven aan de pagina >  **[!UICONTROL Add Users]** om nieuwe gebruikers te maken of om bestaande gebruikers te bewerken.
1. Volg de instructies in [Gebruikers en groepen beheren in de Experience Cloud](https://helpx.adobe.com/enterprise/help/users.html) in *Handleiding voor gebruikers in de onderneming*.

## Stap 2. Een werkruimte maken (productprofiel) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Met een werkruimte (productprofiel) kan een organisatie een specifieke set gebruikers toewijzen aan een specifieke set eigenschappen. In veel opzichten is een werkruimte vergelijkbaar met een rapportsuite in [!DNL Analytics].

Organisaties kunnen profiteren van de functionaliteit voor Enterprise-machtigingen door nieuwe werkruimten te maken binnen [!DNL Admin Console], eigenschappen [!DNL Target] toe te wijzen aan deze werkruimten en gebruikers van de configuratie &quot;Standaardwerkruimte&quot; te verplaatsen naar deze nieuwere werkruimten met beperkte toegang.

De klanten kunnen deze werkruimten gebruiken om toegang tot verschillende teams door gebied, door bedrijfseenheid, door plaatsctie, of via een andere methode te scheiden zij kiezen.

Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen zelfs verschillende rollen binnen elke werkruimte hebben.

1. Klik in [!DNL Admin Console] op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![werkruimte](/help/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Maak de gewenste werkruimte (productprofiel):

   * **Standaardtoegang:** alle bestaande activiteiten worden samengevoegd in één project dat &quot;Standaardtoegang&quot; wordt genoemd. Dit heeft geen invloed op klanten. Alle gebruikersrollen en functionaliteit zullen precies het zelfde blijven aangezien zij vóór deze verandering zijn.

      Alle activiteiten die worden gemaakt via [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] en [!DNL Target Classic] maken ook deel uit van de werkruimte Standaardtoegang. U kunt momenteel geen projecten van &quot;Standaardtoegang&quot;aan een ander project bewegen.

   * **Nieuwe werkruimten (Productprofielen):** u kunt de nieuwe functionaliteit voor machtigingen als volgt benutten:

      * Nieuwe werkruimten maken in de [!DNL Admin Console for Enterprise].
      * Doeleigenschappen toewijzen aan de werkruimten.

   U kunt deze werkruimten gebruiken om toegang tot verschillende teams te verdelen door gebied, bedrijfseenheid, plaatssectie, of via een andere methode u kiest. Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen verschillende rollen binnen elke werkruimte hebben.

1. Volg de instructies in [Productconfiguraties maken en beheren](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in de *Handleiding voor Enterprise*.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het configureren van werkruimten.

### Verkrijg uw werkruimte-id {#workspace-id}

U moet de werkruimte-id doorgeven aan Enterprise-machtigingen in [Doel-API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md).

1. Klik in [Adobe Admin Console](https://adminconsole.adobe.com) op het tabblad [!UICONTROL Products] en klik vervolgens op het product in het linkermenu om de lijst PLC(werkruimte) weer te geven.
1. Klik op de gewenste PLC (werkruimte) en zoek de id voor &quot;profielen&quot; in de URL, zoals hieronder wordt weergegeven.

   ![workspaceID](/help/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Stap 3. Gebruikersgroepen maken (optioneel) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid alle aangewezen voorrechten over verschillende producten van de Adobe kan zo gemakkelijk zijn zoals het toevoegen van hen aan een specifieke gebruikersgroep.

1. Klik in de Admin Console op de tab **[!UICONTROL Users]** boven aan de pagina > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of om bestaande groepen te bewerken.
1. Volg de instructies in [Gebruikers en groepen van een productconfiguratie beheren](https://helpx.adobe.com/enterprise/help/manage-products-and-configurations.html) in *Handleiding voor Enterprise*.

## Stap 4. Eigenschappen maken {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschappen worden toegelaten door een specifiek naam/waardepaar als parameter met om het even welke vraag (de vraag van het Doel, api vraag, enz.) toe te voegen naar doel.

Eigenschappen behoren tot specifieke kanalen (Web, Mobiel, E-mail, en API/Overige).

**Tip**: Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de lijst [!UICONTROL Properties] weer te geven.
1. Klik **Eigenschap maken**.

   ![Nieuwe eigenschap, dialoogvenster](/help/administrating-target/c-user-management/property-channel/assets/new_property1.png)

   Vul de velden in:

   * **Eigenschapnaam (vereist):** geef een beschrijvende naam voor de eigenschap op.
   * **Beschrijving:** geef een optionele beschrijving voor de eigenschap op.
   * **Kanaal:** selecteer het gewenste kanaal voor het bezit: Web, Mobile App, Email of Other/API (bijvoorbeeld een set-top box of PlayStation-console).

1. Klik **[!UICONTROL Copy]** om de code aan uw klembord te kopiëren die u tijdens het uitvoeren van de stappen in [5 zult gebruiken: Werk Uw Implementatie bij om de parameter at_property](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8) op te nemen.
1. Klik **[!UICONTROL Save]** wanneer gereed.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

## Stap 5: Werk uw implementatie bij om de parameter at_property {#section_9B17A59807A94712BE642942442EBBC8} op te nemen

Om [!DNL Target] gebruiker-toestemmingsfunctionaliteit te gebruiken, moet u de `at_property` parameter aan om het even welke vraag toevoegen die [!DNL Target] (de vraag van het Doel, api vraag, enz.) raakt.

**U verkrijgt als volgt de  `at_property` parametercode:**

1. (Voorwaardelijk) gebruik de implementatiecode u aan uw klembord produceerde en opsloeg terwijl het uitvoeren van de stappen in [4. Creeer Eigenschappen](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) en ga aan Stap 2 te werk.

   of

   Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de lijst [!UICONTROL Properties] weer te geven.

   1. Houd de muisaanwijzer boven de kolom [!UICONTROL Last Updated] om de gewenste eigenschap weer te geven en klik op het pictogram [!UICONTROL Code].

      ![Code voor aanwijzen van eigenschap](/help/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klik met de rechtermuisknop op de gemarkeerde implementatiecode om deze naar het klembord te kopiëren.

      ![Eigenschappencode](/help/administrating-target/c-user-management/property-channel/assets/code_property_2_new.png)

1. Werk uw [!DNL Target] implementatie met de implementatiecode bij die in de vorige stap wordt verkregen.

   Er zijn verschillende manieren om uw [!DNL Target]-implementatie bij te werken. De volgende methoden kunnen bijvoorbeeld worden gebruikt voor webpagina&#39;s:

   * **Via een &quot;Algemene parameter in  [!DNL Adobe Launch]:**

      Zie [Globale doelparameters toevoegen](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension#add-global-mbox-params) in de documentatie *Adobe Experience Platform Launch* voor meer informatie.

   * **Via een &quot;globale parameter&quot; in  [!DNL Dynamic Tag Management]:**

      ![](assets/property_token_2.png)

      Voor meer informatie, zie [Globale Parameters - Adobe Target](https://experienceleague.adobe.com/docs/dtm/using/tools-reference/target.html#global-parameters---adobe-target) in *Dynamische Document van het Product van het Beheer van de Markering*.

   * **Via de functie targetPageParams():** Plaats de volgende code in de  `<head>` tags, boven de verwijzing at.js of mbox.js.

      ![](assets/property_token_1.png)

      Zie [targetPageParams()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) voor meer informatie over hoe u dit met at.js kunt doen.

   * **Via de functie mboxCreate():**

      ![](assets/property_token_3.png)

      Voor meer informatie over hoe te om dit met at.js te doen, zie [targetPageParams ()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) en [mboxCreate(mbox,params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md).

## Stap 6: Rollen en machtigingen opgeven {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klik in de Admin Console op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![Werkruimte](/help/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de naam van het gewenste profiel (bijvoorbeeld Standaardwerkruimte).

   ![Standaardwerkruimte](/help/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Klik op **[!UICONTROL Users]**.

   Op het tabblad [!UICONTROL Users] worden alle gebruikers in die werkruimte weergegeven.

   ![configuratiegebruikers](/help/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste toestemmingenrol (Approver, Redacteur, Waarnemer, of Uitgever) door de drop-down lijst voor elke gebruiker in [!UICONTROL Product Role] kolom te gebruiken.

   ![Vervolgkeuzelijst Productrol](/help/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

   Zie [Productmachtigingen en -rollen beheren in de Admin Console](https://helpx.adobe.com/enterprise/help/manage-permissions-and-roles.html) in de *Handleiding voor bedrijven* voor meer informatie.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video&#39;s is over het algemeen correct. de opties kunnen zich echter op iets andere locaties bevinden . Bijgewerkte video&#39;s worden binnenkort gepost.

### Hoe te om de Werkruimten van het Doel (6:55) ![badge van het Leerprogramma](/help/assets/tutorial.png) te vormen

In deze video wordt uitgelegd hoe u werkruimten kunt maken.

* Toegang tot de Adobe Admin Console vanaf de Adobe Target-interface (3 manieren)
* Een werkruimte configureren in Adobe Admin Console

   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten

* Standaardwerkruimten begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Eigenschappen maken in Adobe Target (3:05) ![Zelfstudie-badge](/help/assets/tutorial.png)

* Hoe te om een bezit binnen de [!DNL Adobe Target] interface tot stand te brengen
* Hoe te om een bezitstoken te produceren om in uw bezitsimplementatie te omvatten
* Verken uzelf met de drie implementatiemethoden:

   * Web
   * Mobiele app
   * Aanroepen via e-mail, set top box of API

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
