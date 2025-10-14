---
keywords: toevoegen gebruiker;project;gebruikersgroep;eigenschappen;werkruimte;beheren eigenschap;eigenschap;at_eigenschap;rollen;machtigingen
description: Leer hoe u gebruikers aan Adobe Target toevoegt, werkruimten, gebruikersgroepen en eigenschappen maakt, uw implementatie bijwerkt en rollen en machtigingen opgeeft.
title: Hoe kan ik bedrijfsmachtigingen configureren?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Administration & Configuration
role: Admin
exl-id: 6494fc86-d2d3-4382-9d2e-63be435ba935
source-git-commit: 0ab5b7d7cbfaef86b9a045883f597900dba72416
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 0%

---

# Bedrijfsmachtigingen configureren

Informatie over de taken die nodig zijn om gebruikers toe te voegen aan uw [!DNL Target] -implementatie, werkruimten, gebruikersgroepen en eigenschappen te maken, uw [!DNL Target] -implementatie bij te werken en de `at_property` -parameter op te nemen, en rollen en machtigingen op te geven.

>[!NOTE]
>
>De eigenschappen en de functionaliteit van Toestemmingen zijn beschikbaar als deel van de [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie.

De volgende lijst maakt een lijst van de taken u zou moeten uitvoeren om eigenschappen tot stand te brengen en gebruikersrollen en toestemmingen toe te wijzen. Raadpleeg de onderstaande secties voor meer informatie over elke taak.

| Taak | Uitgevoerd in |
|--- |--- |
| &#x200B;1. Gebruikers toevoegen (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| &#x200B;2. Een werkruimte maken (productprofiel) | [!DNL Adobe Admin Console for Enterprise] |
| &#x200B;3. Gebruikersgroepen maken (optioneel) | [!DNL Adobe Admin Console for Enterprise] |
| &#x200B;4. Eigenschappen maken | [!DNL Target] UI |
| 5: Werk uw implementatie bij om de parameter `at_property` op te nemen | [!DNL Target] UI, at.js-functies of -tags in [!DNL Adobe Experience Platform] |
| 6: Rollen en machtigingen opgeven | [!DNL Adobe Admin Console for Enterprise] |

Voor die taken die in [!DNL Adobe Admin Console for Enterprise] worden uitgevoerd, heb toegang tot de console door deze stappen te volgen:

1. Klik in Adobe Target op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** > **[!UICONTROL Assign Properties to Workspaces]** .

   of

   Ga naar [&#x200B; https://adminconsole.adobe.com/enterprise &#x200B;](https://adminconsole.adobe.com/enterprise/) > binnen het gebruiken van uw Adobe ID, als u nog niet hebt het programma geopend.


1. (Voorwaardelijk) Als u toegang hebt tot [!DNL Admin Console for Enterprise] voor meer dan één organisatie, klikt u op de gebruikersavatar in de rechterhoek of op de bovenste navigatiebalk en selecteert u de gewenste organisatie.

## Stap 1. Gebruikers toevoegen (optioneel) {#section_A92AF0F921B743FEB9E9033433BD816A}

Wanneer u de nieuwe [!UICONTROL Properties] -functionaliteit gaat gebruiken, moet al het gebruikersbeheer worden uitgevoerd in de [!DNL Adobe Admin Console for Enterprise] . Alle bestaande gebruikers in [!DNL Target] worden echter gemigreerd van [!DNL Target] naar [!DNL Admin Console for Enterprise] .

1. [&#x200B; in Admin Console &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_79796E0227D048F59BAE0AB02E544EBE), klik het **[!UICONTROL Users]** lusje bij de bovenkant van pagina > **[!UICONTROL Add Users]** om nieuwe gebruikers tot stand te brengen of bestaande gebruikers uit te geven.
1. Volg de instructies in [&#x200B; leiden Gebruikers en Groepen in Experience Cloud &#x200B;](https://helpx.adobe.com/nl/enterprise/help/users.html) in de *Gids van de Gebruiker van de Onderneming*.

## Stap 2. Een werkruimte maken (productprofiel) {#section_B82EB409B67C4D9D9D20CE30E48DB1DC}

Met een werkruimte (productprofiel) kan een organisatie een specifieke set gebruikers toewijzen aan een specifieke set eigenschappen. In veel opzichten is een werkruimte vergelijkbaar met een rapportsuite in [!DNL Analytics] .

Organisaties kunnen profiteren van de functionaliteit voor Enterprise-machtigingen door nieuwe werkruimten te maken in [!DNL Admin Console] , [!DNL Target] -eigenschappen toe te wijzen aan deze werkruimten en gebruikers van de configuratie &quot;Standaard Workspace&quot; te verplaatsen naar deze nieuwere werkruimten met beperkte toegang.

De klanten kunnen deze werkruimten gebruiken om toegang tot verschillende teams door gebied, door bedrijfseenheid, door plaatsctie, of via een andere methode te scheiden zij kiezen.

Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen zelfs verschillende rollen binnen elke werkruimte hebben.

1. Klik in [!DNL Admin Console] op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-new.png)

1. Maak de gewenste werkruimte (productprofiel):

   * **StandaardToegang:** Alle bestaande activiteiten zullen in één enkel project genoemd &quot;StandaardToegang worden samengevoegd.&quot; Dit heeft geen invloed op klanten. Alle gebruikersrollen en functionaliteit zullen precies het zelfde blijven aangezien zij vóór deze verandering zijn.

     Alle activiteiten die via [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services] en [!DNL Target Classic] worden gemaakt, maken ook deel uit van de werkruimte Standaardtoegang. U kunt momenteel geen projecten van &quot;Standaardtoegang&quot;aan een ander project bewegen.

   * **Nieuwe werkruimten (Profielen van het Product):** u kunt beginnen uit de nieuwe toestemmingenfunctionaliteit voordeel te halen door het volgende te doen:

      * Nieuwe werkruimten maken in de [!DNL Admin Console for Enterprise] .
      * Doeleigenschappen toewijzen aan de werkruimten.

   U kunt deze werkruimten gebruiken om toegang tot verschillende teams te verdelen door gebied, bedrijfseenheid, plaatssectie, of via een andere methode u kiest. Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen verschillende rollen binnen elke werkruimte hebben.

1. Volg de instructies in [&#x200B; creeer en beheer de Configuraties van het Product &#x200B;](https://helpx.adobe.com/nl/enterprise/help/manage-products-and-configurations.html) in de *Gids van de Gebruiker van de Onderneming*.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het configureren van werkruimten.

### Vraag uw werkruimte-id op {#workspace-id}

U zult werkruimtetoewijzing aan de Toestemmingen van de hefboomonderneming in [&#x200B; Doel APIs &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html?lang=nl-NL){target=_blank} moeten overgaan.

1. In [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com), klik het [!UICONTROL Products] lusje, dan klik het product in het linkermenu om PLC (werkruimte) lijst te tonen.
1. Klik op de gewenste PLC (werkruimte) en zoek de id voor &quot;profielen&quot; in de URL, zoals hieronder wordt weergegeven.

   ![&#x200B; workspaceID &#x200B;](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-id-newest.png)

## Stap 3. Gebruikersgroepen maken (optioneel) {#section_5F5CB9AA7A9F4D26953E22016DA59605}

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers, Executives, enz., en vervolgens rechten toewijzen voor meerdere Adobe-producten en -werkruimten. Het toewijzen van een nieuw teamlid aan alle juiste rechten voor verschillende Adobe-producten kan net zo eenvoudig zijn als het toevoegen van deze rechten aan een specifieke gebruikersgroep.

1. Klik in de Admin Console op de tab **[!UICONTROL Users]** boven aan de pagina > **[!UICONTROL User Groups]** om nieuwe gebruikersgroepen te maken of bestaande groepen te bewerken.
1. Volg de instructies in [&#x200B; leiden Gebruikers en Groepen van een Configuratie van het Product &#x200B;](https://helpx.adobe.com/nl/enterprise/help/manage-products-and-configurations.html) in de *Gids van de Gebruiker van de Onderneming*.

## Stap 4. Eigenschappen maken {#section_E8F2C92BE0F4466AB87604059C9CF3FD}

Eigenschappen worden ingeschakeld door een specifiek naam-/waardepaar als een parameter toe te voegen met een aanroep ([!DNL Target] aanroep, api-aanroep enz.) naar [!DNL Target] .

Eigenschappen behoren tot specifieke kanalen (Web, Mobiel, E-mail, en API/Overige).

**Uiteinde**: Zie de opleidingsvideo hieronder voor meer informatie over hoe te om eigenschappen tot stand te brengen.

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de lijst [!UICONTROL Properties] weer te geven.
1. Klik **creeer Bezit**.

   Vul de velden in:

   * **Naam van het Bezit (Vereist):** specificeer een beschrijvende naam voor het bezit.
   * **Beschrijving:** specificeer een facultatieve beschrijving voor het bezit.
   * **Kanaal:** selecteer het gewenste kanaal voor het bezit: Web, Mobiele App, E-mail, of Andere/API (bijvoorbeeld een reeks-hoogste doos of console PlayStation).

1. Klik **[!UICONTROL Copy]** om de code aan uw klembord te kopiëren die u terwijl het uitvoeren van de stappen in [&#x200B; 5 zult gebruiken: Werk Uw Implementatie bij om de parameter te omvatten at_property &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_9B17A59807A94712BE642942442EBBC8).
1. Klik op **[!UICONTROL Save]** als u klaar bent.

>[!NOTE]
>Zie de trainingsvideo hieronder voor meer informatie over het maken van eigenschappen.

## Stap 5: Werk uw implementatie bij om de parameter at_property op te nemen {#section_9B17A59807A94712BE642942442EBBC8}

Als u de functionaliteit voor [!DNL Target] gebruikersmachtigingen wilt gebruiken, moet u de parameter `at_property` toevoegen aan elke aanroep die [!DNL Target] aanroept (aanroep van doel, api enz.).

**om de `at_property` parametercode te verkrijgen:**

1. (Voorwaardelijk) Gebruik de implementatiecode u aan uw klembord produceerde en bewaarde terwijl het uitvoeren van de stappen in [&#x200B; . Creeer Eigenschappen &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_E8F2C92BE0F4466AB87604059C9CF3FD) en ga aan Stap 2 te werk.

   of

   Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Properties]** om de lijst [!UICONTROL Properties] weer te geven.

   1. Beweeg uw muiswijzer over de [!UICONTROL Last Updated] kolom voor het gewenste bezit aan vertoning en klik het [!UICONTROL Code] pictogram ( ![&#x200B; pictogram van de Code &#x200B;](/help/main/assets/icons/Code.svg)).

      ![&#x200B; de muiscode van het Bezit &#x200B;](/help/main/administrating-target/c-user-management/property-channel/assets/code_property_new.png)

   1. Klik met de rechtermuisknop op de gemarkeerde implementatiecode om deze naar het klembord te kopiëren.

1. Werk uw [!DNL Target] -implementatie bij met de implementatiecode die in de vorige stap is verkregen.

   Er zijn verschillende manieren om uw [!DNL Target] -implementatie bij te werken. De volgende methoden kunnen bijvoorbeeld worden gebruikt voor webpagina&#39;s:

   * **via een &quot;Parameter van de Douane&quot;in markeringen binnen [!DNL Adobe Experience Platform]:**

     Voor meer informatie, zie [&#x200B; Mbox Params &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html?lang=nl-NL#add-mbox-params) in de *het overzicht van Markeringen* documentatie toevoegen.

   * **via targetPageParamsAll () functie:** Plaats de volgende code in de `<head>` markeringen, boven de verwijzing at.js.

     ```javascript
     <script>
      function targetPageParamsAll() {
       return {
        "at_property": "5f8bd98b-1456-a84c-2a96-11s9b8e2b112"
       };
      }
     </script>
     ```

     Voor meer informatie over hoe te om dit met at.js te doen, zie [&#x200B; targetPageParamsAll &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetpageparamsall.html?lang=nl-NL){target=_blank}.

## Stap 6: Geef rollen en machtigingen op {#section_8C425E43E5DD4111BBFC734A2B7ABC80}

1. Klik in de Admin Console op **[!UICONTROL Products]** en selecteer vervolgens de naam van het gewenste product.

   ![&#x200B; Workspace &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/assets/workspace-publisher.png)

1. Klik op de naam van het gewenste profiel (bijvoorbeeld Standaard Workspace).

   ![&#x200B; Standaard Workspace &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/assets/default-workspace-new.png)

1. Klik op **[!UICONTROL Users]**.

   Op het tabblad [!UICONTROL Users] worden alle gebruikers in die werkruimte weergegeven.

   ![&#x200B; configuratiegebruikers &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/assets/configuration_users-new-publisher.png)

1. Selecteer de gewenste machtigingenrol (fiatteur, Editor, waarnemer of Uitgever) door de vervolgkeuzelijst voor elke gebruiker in de kolom [!UICONTROL Product Role] te gebruiken.

   ![&#x200B; drop-down lijst van de Rol van het Product &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/assets/product-role-new.png)

   | Rol | Beschrijving |
   |--- |--- |
   | Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
   | Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
   | Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
   | Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

   Voor meer informatie, zie [&#x200B; de Toestemmingen en Rollen van het Product in Admin Console &#x200B;](https://helpx.adobe.com/nl/enterprise/help/manage-permissions-and-roles.html) in de *Gids van de Gebruiker van de Onderneming* beheren.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

>[!NOTE]
>
>De gebruikersinterface van het [!DNL Target] [!UICONTROL Administration] menu (voorheen [!UICONTROL Setup] ) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video&#39;s is over het algemeen correct, maar de opties kunnen zich op een iets andere locatie bevinden. Bijgewerkte video&#39;s worden binnenkort gepost.

### Hoe te om de Werkruimten van Adobe Target (6 :55) te vormen ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

In deze video wordt uitgelegd hoe u werkruimten kunt maken.

* Toegang tot de Adobe Admin Console vanaf de Adobe Target-interface (3 manieren)
* Een werkruimte configureren in Adobe Admin Console

   * Gebruikers toevoegen aan werkruimten
   * Eigenschappen toevoegen aan werkruimten

* Standaardwerkruimten begrijpen

>[!VIDEO](https://video.tv.adobe.com/v/19463/)

### Hoe te om Eigenschappen in Adobe Target (3 :05) te creëren ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

* Hoe te om een bezit binnen de [!DNL Adobe Target] interface te creëren
* Hoe te om een bezitstoken te produceren om in uw bezitsimplementatie te omvatten
* Verken uzelf met de drie implementatiemethoden:

   * Web
   * Mobiele app
   * Aanroepen via e-mail, set top box of API

>[!VIDEO](https://video.tv.adobe.com/v/18990/)
