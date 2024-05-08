---
keywords: werkruimten;beheren eigenschap;machtigingen;productconfiguratie;productprofiel;rollen;project;waarnemer;editor;fiatteur;uitgever
description: Leer hoe u afzonderlijke werkruimten (productprofielen) maakt en gebruikers vervolgens verschillende rollen en machtigingen toewijst voor afzonderlijke pagina's, eigenschappen of websites.
title: Wat zijn de toestemmingen van de Gebruiker van de Onderneming en hoe gebruik ik hen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Administration & Configuration
role: Admin
exl-id: 838abe87-dba7-4274-97b4-31a7905846dc
source-git-commit: 5e86d3a95dad291f6c876f126568ba685ff32670
workflow-type: tm+mt
source-wordcount: '3171'
ht-degree: 0%

---

# Machtigingen voor Enterprise-gebruikers

De gebruikerstoestemmingen van de onderneming zijn een middel formeel om gebruikers op bedrijfsniveau toegang tot te beheren [!DNL Adobe Target]. Gebruikers toevoegen aan [!DNL Target], wijs toestemmingen toe die op hun rollen worden gebaseerd, en creeer werkruimten voor teams die op verschillende afdelingen, globale plaatsen, kanalen, en andere logische groeperingen worden gebaseerd. U kunt gebruikers de rollen toewijzen van [!UICONTROL Observer], [!UICONTROL Editor], [!UICONTROL Approver], of [!UICONTROL Publisher].

## Bepaal of u toegang hebt tot bedrijfsgebruikersmachtigingen

>[!NOTE]
>
>[!UICONTROL Properties and Permissions] is beschikbaar als onderdeel van de [!DNL Target] Hoogwaardige oplossing. Ze zijn niet beschikbaar in [!DNL Target] Standaard zonder een [!DNL Target] Premium-licentie.
>
>Uw [!DNL Target] de implementatie kan elke versie van at.js of [!DNL Adobe Experience Platform Web SDK].

Als u wilt weten of uw organisatie een Standard- of Premium-licentie heeft, klikt u op de knop [!UICONTROL Administration] koppeling boven aan [!DNL Target] UI.

* **[!DNL Target Standard]Klanten**: Als u de [!UICONTROL Users] tab ([!UICONTROL Administration > Users]) (en niet de [!UICONTROL Properties] tab), heeft uw organisatie een [!DNL Target Standard] licentie. [!DNL Target Standard] klanten moeten de instructies in [Gebruikers](/help/main/administrating-target/c-user-management/c-user-management/user-management.md) om gebruikers toe te voegen en toestemmingen toe te wijzen in [!DNL Adobe Admin Console].

* **[!DNL Target Premium]Klanten**: Als u de [!UICONTROL Properties] tab ([!UICONTROL Administration > Properties]) en de [!UICONTROL Users] tab, heeft uw organisatie een [!DNL Target Premium] licentie. [!DNL Target Premium] klanten moeten de instructies in dit artikel en in [Bedrijfsmachtigingen configureren](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

## Voordat u aan de slag gaat met bedrijfsmachtigingen

>[!IMPORTANT]
>
>Zorg ervoor dat u de [Caveats](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#section_9714311B1CD9497A86F4910F8AE635E2) hieronder voor u verder gaat met bedrijfsmachtigingen.

## In deze sectie gebruikte termen en definities {#section_F8D229544FEA41C3BC2EFD1F95AA0116}

De volgende termen worden gebruikt in deze sectie en zijn mogelijk nieuw voor gebruikers die de eigenschappen en de machtigingsfunctionaliteit willen gebruiken in [!DNL Target] Premium.

### Eigenschap

Eigenschappen zijn van nature vergelijkbaar met eigenschappen binnen [!DNL Adobe Experience Platform] in die zin dat zij een uniek codefragment gebruiken om hen te onderscheiden.

Een webeigenschap is een bibliotheek met regels en één insluitcode. Een webeigenschap kan elke groepering van een of meer domeinen en subdomeinen zijn.

Eigenschappen worden toegelaten door een specifiek naam/waardepaar als parameter met om het even welke vraag (de vraag van het Doel, api vraag, etc.) toe te voegen aan [!DNL Target].

Eigenschappen behoren tot specifieke kanalen (Web, Mobiel, E-mail, of API/Overige).

### Werkruimte (productprofiel) {#workspace}

Met een werkruimte kan een organisatie een specifieke set gebruikers toewijzen aan een specifieke set eigenschappen. In veel opzichten is een werkruimte vergelijkbaar met een rapportsuite in [!DNL Adobe Analytics].

Opmerking: werkruimten worden ook wel [!UICONTROL Product Profiles] in de [!DNL Adobe Admin Console for Enterprise].

Als u deel uitmaakt van een multinationale organisatie, hebt u mogelijk een werkruimte voor uw Europese webpagina&#39;s, eigenschappen of sites en een andere werkruimte voor uw Amerikaanse webpagina&#39;s, eigenschappen of sites. Als u deel uitmaakt van een organisatie met meerdere merken, hebt u mogelijk een aparte werkruimte voor elk van uw merken.

Gebruikers kunnen deel uitmaken van meerdere werkruimten en kunnen zelfs verschillende rollen binnen elke werkruimte hebben.

Gebruikers kunnen verschillende weergaven van [!DNL Adobe Target] door te schakelen tussen werkruimten, vergelijkbaar met [!DNL Analytics] gebruikers hebben verschillende weergaven van [!DNL Analytics] door tussen de Geschikten van het Rapport te bewegen.

De werkruimten kunnen volledig verschillend publiek, codeaanbiedingen, en activiteiten omvatten.

Alle publiek en activiteiten die vóór de nieuwe modelmigratie van de Toestemmingen van de Onderneming worden gecreeerd worden gegroepeerd in &quot;StandaardWerkruimte,&quot;hieronder besproken.

Alle activiteiten die via [!DNL Adobe Experience Manager] (AEM), [!DNL Adobe Mobile Services], en [!DNL Adobe Target Classic] maakt deel uit van de standaardwerkruimte.

### Standaardwerkruimte

Alle bestaande werkruimten (productprofielen) in [!DNL Admin Console] tijdens de migratie van uw organisatie naar het nieuwe model voor bedrijfsmachtigingen worden samengevoegd in één werkruimte met de naam &quot;Standaardwerkruimte&quot;.

>[!IMPORTANT]
>
>Verwijder de standaardwerkruimte niet.

Alle gebruikersrollen en toegang tot alle [!DNL Target] de functionaliteit blijft hetzelfde als vóór de migratie naar het nieuwe model voor Enterprise-machtigingen.

### Gebruikersgroepen

U kunt gebruikersgroepen maken, zoals Ontwikkelaars, Analysten, Marketers en Managers. U kunt dan voorrechten over veelvoudige producten en werkruimten van de Adobe toewijzen. Het toewijzen van een nieuw teamlid kan alle aangewezen voorrechten over verschillende producten van de Adobe zo gemakkelijk zijn zoals het toevoegen van hen aan een specifieke gebruikersgroep.

### Rollen en machtigingen {#roles-permissions}

De rollen en de toestemmingen bepalen de toegangsniveaus die de gebruikers activiteiten in uw moeten creëren en beheren [!DNL Target] uitvoering. In [!DNL Target], omvatten rollen het volgende:

| Rol | Beschrijving |
|--- |--- |
| [!UICONTROL Approver] | Kan activiteiten maken, bewerken en activeren of stoppen. |
| [!UICONTROL Editor] | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
| [!UICONTROL Observer] | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
| [!UICONTROL Publisher] | Vergelijkbaar met de [!UICONTROL Observer] rol (kan activiteiten bekijken, maar kan niet hen creëren of uitgeven). De [!UICONTROL Publisher] de rol heeft de extra toestemming om activiteiten te activeren. |

### Kanaal

Het kanaal verwijst naar het inhoudstype van waar uw [!DNL Target] activiteiten worden geleverd: webpagina&#39;s, mobiele apps, e-mailberichten enzovoort.

Wanneer u een activiteit creeert, wordt het gecreeerd in de momenteel geselecteerde werkruimte. U ziet de opties voor kanaalselectie in het eerste dialoogvenster waarin u het gewenste kanaal voor de activiteit kunt kiezen: Web, Mobiele app, E-mail of Overige/API.

## Overzicht van machtigingen {#section_DC2172520DA84605B218A5E9FB6D187A}

De volgende informatie verklaart hoe de toestemmingen eerder in werden afgedwongen [!DNL Target] en de wijze waarop deze worden afgedwongen met behulp van de [!UICONTROL Properties] en [!UICONTROL Permissions] functionaliteit.

De nieuwe [!UICONTROL Permissions] Met de functionaliteit kunt u verschillende projecten maken (de zogenaamde &quot;Productprofielen&quot; in het dialoogvenster [!DNL Adobe Admin Console for Enterprise]). De projecten staan u toe om verschillende toestemmingen voor één enkele gebruiker toe te wijzen die de toegangsrechten van die gebruiker voor elk project dicteren. Deze afzonderlijke projecten kunnen worden vergeleken met de manier waarop de reeksen in [!DNL Adobe Analytics]. Elk project kan specifieke gebruikers met specifieke rollen hebben die op een reeks eigenschappen van toepassing zijn. Het resultaat is dat klanten de weergave, bewerking en goedkeuringstoegang kunnen beperken tot hun gebruikers op basis van regio, omgeving (dvd/stage/prod), kanaal of andere aangepaste criteria, zoals hieronder wordt getoond:

![machtigingsafbeelding](assets/permissions.png)

Een specifieke gebruiker kan bijvoorbeeld toegang tot goedkeuring hebben op de Amerikaanse websites, maar alleen toegang tot de Europese mobiele app bekijken. Dezelfde gebruiker heeft mogelijk geen toegang om zelfs maar de activiteiten te bekijken die op het web en mobiele eigenschappen in de APAC-regio worden aangeboden.

De [!DNL Target] [!UICONTROL Permissions] het model heeft de volgende toestemmingsrollen (Waarnemer, Redacteur, Approver, en Waarnemer). De rol van waarnemer wordt niet weergegeven in illustraties in dit artikel.

![permissions_1 afbeelding](assets/permissions_1.png)

Elke rol heeft verschillende machtigingsniveaus:

| Rol | Beschrijving |
|--- |--- |
| Fiatteur | Kan activiteiten maken, bewerken en activeren of stoppen. |
| Editor | Kan activiteiten maken en bewerken voordat deze live zijn, maar kan het starten van een activiteit niet goedkeuren. |
| Waarnemer | Kan activiteiten weergeven, maar kan deze niet maken of bewerken. |
| Uitgever | Lijkt op de rol van waarnemer (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De rol Publisher heeft echter de extra machtiging om activiteiten te activeren. |

Het is belangrijk om op te merken dat de rol van elke gebruiker op elke pagina, bezit, of plaats in uw rekening van toepassing is die omvat [!DNL Target] -tags, zoals hieronder wordt weergegeven:

![permissions_2 beeld](assets/permissions_2.png)

De nieuwe [!DNL Target] [!UICONTROL Permissions] Het model heeft de zelfde drie toestemmingsrollen (de Waarnemer, de Redacteur, en de fiatteur); nochtans kunt u de toestemmingsrollen van een gebruiker afzonderlijk voor individuele pagina&#39;s, eigenschappen, of plaatsen, zoals hieronder getoond toewijzen:

![permissions_3 beeld](assets/permissions_3.png)

In dit voorbeeld heeft Jan de toestemmingen van de fiatteur aan de Homepage van de V.S. en de Plaats en de toestemmingen van de Waarnemer aan de Plaats van Frankrijk.

Bovendien kan Jan geen pagina&#39;s, eigenschappen of sites weergeven in [!DNL Target] dat ze geen toestemming heeft om te zien, zoals hieronder wordt getoond:

![permissions_4 beeld](assets/permissions_4.png)

In dit voorbeeld ziet Jan de Productpagina&#39;s, de Russische Site en de Careers Site niet.

## Gebruiksscenario&#39;s {#section_F3CE8576959E4F4CB13BEEED38311DD8}

De volgende gebruiksgevallen kunnen nuttig zijn om te begrijpen hoe eigenschappen, projecten, rollen, en toestemmingen u kunnen helpen uw marketing doelstellingen bereiken met [!DNL Target]:

### Meernationale organisatie

Als u deel uitmaakt van een multinationale organisatie, hebt u mogelijk een werkruimte voor uw Europese webpagina&#39;s, eigenschappen of sites en een andere werkruimte voor uw Amerikaanse webpagina&#39;s, eigenschappen of sites.
Na een reorganisatie, gebruikend de karakters in de illustraties hierboven, zou u opstelling werkruimten en toestemmingen gelijkend op het volgende kunnen:

* **Jan**: Jan is het hoofd Optimalisatie in het Center of Excellence voor de webpagina&#39;s, eigenschappen en sites van haar organisatie in de Verenigde Staten. Ze heeft waarschijnlijk rechten voor Systeembeheer in de Adobe Experience Cloud.

  In haar rol, heeft zij de toestemmingen van Approver voor de Homepage van de V.S. en de Plaats van de V.S. Met de machtiging fiatteur kunt u activiteiten maken, bewerken en activeren of stoppen.

  Jan raadpleegt ook het optimalisatieteam in Frankrijk en heeft daarom waarnemersmachtigingen voor de site van Frankrijk die haar alleen-lezen toegang tot activiteiten geven. Jan kan activiteiten weergeven, maar kan deze niet maken of bewerken.

  Omdat Jan geen rol heeft die haar het zien van de Pagina&#39;s van het Product, de Plaats van Rusland, of de Plaats van Careers vereist, kan zij geen activiteiten voor die plaatsen zien.

* **Ernie**: Ernie is een marketingmanager van de organisatie die in de Verenigde Staten verantwoordelijk is voor marketing.

  Omdat Ernie vrij nieuw aan de organisatie en onervaren met Doel is, heeft hij de toestemmingen van de Redacteur voor de Homepage van de V.S., Plaats, en de Pagina&#39;s van het Product van de V.S. Met de toestemmingen van de Redacteur, kan Ernie activiteiten tot stand brengen en uitgeven alvorens zij levend zijn. Hij kan niet de lancering van activiteit-iemand met de toestemming van de Goedkeuring, zoals Jan goedkeuren, moet de activiteit goedkeuren alvorens het in productie kan worden gezet.

  Omdat Ernie geen rol heeft die hem vereist om de Russische Site, de Plaats van Frankrijk, of de Plaats van Careers te zien, kan hij geen activiteiten voor die plaatsen zien.

* **Diana**: Diana is nu een analist voor de organisatie en heeft waarnemersmachtigingen gekregen voor de US Homepage US Site, Product Pages, Russisch Site en de website van Frankrijk, die haar alleen-lezen toegang geven tot activiteiten. Diana kan activiteiten bekijken, maar kan ze niet maken of bewerken.

  Omdat Diana geen rol heeft die haar nodig heeft om de website van Careers te zien, kan ze geen activiteiten voor die sites zien.

### Meermerkorganisatie

Als u deel uitmaakt van een organisatie met meerdere merken, hebt u mogelijk een aparte werkruimte voor de webpagina&#39;s, eigenschappen of sites van elk merk.

Na een reorganisatie, gebruikend de karakters in de illustraties hierboven, zou u opstellingsprojecten en toestemmingen gelijkend op het volgende kunnen:

* **Jan**: Jan is het hoofd van de optimalisatie in het excellentiecentrum voor een organisatie voor gezondheidszorg die actief is in de ruimten voor ziekenhuisproducten en consumentenproducten. Ze heeft waarschijnlijk rechten voor Systeembeheer in de Adobe Experience Cloud.

  In haar rol, heeft zij de toestemmingen van de fiatteur voor de Ziekenhuis. Met de machtiging fiatteur kunt u activiteiten maken, bewerken en activeren of stoppen.

  Jan raadpleegt ook het optimalisatieteam in de ruimte voor consumentenproducten en beschikt daarom over de machtiging Waarnemer voor die site die haar alleen-lezen toegang geeft tot activiteiten. Jan kan activiteiten weergeven, maar kan deze niet maken of bewerken.

* **Ernie**: Ernie is een marketingmanager voor de organisatie die verantwoordelijk is voor marketing in de ruimte tussen consument en product.

  Omdat Ernie vrij nieuw aan de organisatie en onervaren met Doel is, heeft hij de toestemming van de Redacteur voor de Plaats van de Consumenten. Met de toestemmingen van de Redacteur, kan Ernie activiteiten tot stand brengen en uitgeven alvorens zij levend zijn. Hij kan niet de lancering van activiteit-iemand met de toestemmingen van de Goedkeuring voor de Plaats van de Consumenten goedkeuren, maar niet Jan in dit scenario, moet de activiteit goedkeuren alvorens het in productie kan worden gezet.

  Omdat Ernie geen rol heeft die hem ertoe noopt de Ziekenhuis te zien, kan hij geen activiteiten voor die plaats zien.

* **Diana**: Diana is nu een analist voor de organisatie en heeft waarnemersmachtigingen gekregen voor de ziekenhuissite en de consumentensite die haar alleen-lezen toegang geven tot activiteiten. Diana kan activiteiten bekijken, maar kan ze niet maken of bewerken.

## Eigenschap voor doel-UI en aanraakpunten voor machtigingen {#section_3414371393BB42999A268628B5456EC9}

De nieuwe machtigingsfunctionaliteit is op verschillende plaatsen te zien in de [!DNL Target] UI.

* **Vervolgkeuzelijst Werkruimte (Productprofiel):** De vervolgkeuzelijst Werkruimte wordt boven aan het dialoogvenster [!UICONTROL Activities], [!UICONTROL Audiences], en [!UICONTROL Offers] pagina&#39;s. Selecteer de gewenste werkruimte om de lijst te filteren zodat alleen de items in de geselecteerde werkruimte worden weergegeven.

  ![workspace_drop-down image](assets/workspace_drop-down.png)

* **Activiteiten maken:** Wanneer u een activiteit creeert, wordt het gecreeerd in de momenteel geselecteerde werkruimte. U ziet de opties voor kanaalselectie in het eerste dialoogvenster waarin u het gewenste kanaal voor de activiteit kunt kiezen: Web, Mobiele app, E-mail of Overige/API.

  ![channel_options-afbeelding](assets/channel_options.png)

* **Aanmaken publiek:** Wanneer u een publiek maakt, wordt dit gemaakt in de momenteel geselecteerde werkruimte.
* **Poortlijst:** U kunt een publiek tussen werkruimten verplaatsen met de opdracht [!UICONTROL More Actions] > [!DNL Move] de optie [!UICONTROL Audiences] pagina.
* **Aanbieding maken:** Wanneer u een aanbieding creeert, wordt het gecreeerd in de momenteel geselecteerde werkruimte.
* **Pagina Eigenschappen (Beheer > Eigenschappen):** U kunt de [!UICONTROL Search] vak waarin u kunt zoeken [!UICONTROL Property] lijst.

  ![properties_list, afbeelding](assets/properties_list.png)

## Caveats {#section_9714311B1CD9497A86F4910F8AE635E2}

Overweeg het volgende wanneer het gebruiken van of het vormen van eigenschappen en toestemmingen in [!DNL Target] Premium:

* **Belangrijk**: Verwijder geen werkruimten met activiteiten. Als u een werkruimte met activiteiten schrapt, werk met de Zorg van de Cliënt om die activiteiten terug te krijgen.
* Wanneer het gebruiken van Al Mijn mening van Werkruimten:

   * U kunt activiteiten, publiek, en aanbiedingen voor alle werkruimten zien die u de juiste rollen en toestemmingen hebt om toegang te hebben.
   * Wanneer u [!UICONTROL All My Workspaces] wordt een nieuwe kolom toegevoegd aan de pagina Activiteiten, Soorten publiek en Aanbiedingen. Deze kolom maakt een lijst van de werkruimte van het punt en uw gebruikerstoestemming verbonden aan dat punt (Observer, Redacteur, of Approver),
   * Wanneer u een activiteit, publiek of aanbieding maakt in de weergave Al mijn werkruimten, moet u de werkruimte selecteren waar het item moet worden gemaakt. Alleen die werkruimten kunnen worden geselecteerd waarvoor u de machtiging Editor of fiatteur hebt.
   * Wanneer u een activiteit, een publiek of een aanbieding kopieert in de weergave Al mijn werkruimten, moet u de werkruimte selecteren waar het item moet worden gekopieerd. Alleen die werkruimten kunnen worden geselecteerd waarvoor u de machtiging Editor of fiatteur hebt.

* Willekeurige instelling op het volgende [!UICONTROL Administration] pagina&#39;s kunnen door elke [!UICONTROL Approver] in elke werkruimte:

   * Visual Experience Composer
   * Rapportage
   * Scene7-configuratie
   * Implementatie
   * Eigenschappen
   * Gastheren
   * Omgevingen
   * Reactiepunten
   * Gebruikers

* Gebruikers kunnen bronnen niet van de ene werkruimte (productprofiel) naar de andere verplaatsen. Kopiëren wordt echter ondersteund.
* Bij het weergeven van soorten publiek vanuit het deelvenster [!DNL Audiences] pagina, wordt de pagina langzamer geladen dan u had verwacht. Als u op een of andere manier met de zoekbalk werkt, worden de doelgroepen sneller weergegeven. Dit probleem is bekend en wordt in een volgende update opgelost. Dit probleem heeft geen invloed op het selecteren van doelgroepen tijdens de workflow voor het maken van activiteiten.
* De volgende middelen maken deel uit van het nieuwe model van de Toestemmingen van de Onderneming:

   * Activiteiten, publiek en codeaanbieding binnen [!DNL Target Standard/Premium] zijn beschikbaar voor gebruik nadat de klant voor toestemmingen wordt toegelaten. (Opmerking: klanten moeten het recht hebben om [!DNL Target Premium].)
   * Eigenschappen kunnen worden toegevoegd aan bestaande activiteiten in de standaardwerkruimte, maar deze aanpak kan worden gewijzigd.
   * Alleen nieuwe bronnen (zoals activiteiten, codeaanbiedingen en publiek) die zijn gemaakt in Target Premium (nadat Enterprise-machtigingen zijn ingeschakeld) zijn beschikbaar om te worden beperkt door machtigingen.
   * Externe bronnen zijn alleen beschikbaar voor gebruikers in de standaardwerkruimte. De rol van een gebruiker in de Standaardwerkruimte wordt globaal toegepast (op alle doelverzoeken en alle doelbronnen).

* De volgende bronnen zijn *niet* onderdeel van het nieuwe model voor Enterprise-machtigingen:

   * Afbeeldingsaanbiedingen
   * Alle Recommendations-bronnen, inclusief Criteria Library, Design Library, Catalog en Recommendations Setup.
   * Bestaande bronnen (zoals activiteiten, codeaanbiedingen en publiek) die zijn gemaakt in Target Premium voordat u Enterprise-machtigingen inschakelt, kunnen worden gekopieerd, maar kunnen niet naar andere werkruimten worden verplaatst.
   * Activiteiten, publiek, codeaanbiedingen, beeldaanbiedingen, of om het even welke andere die middelen worden gecreeerd gebruikend de volgende oplossingen of de methodes kunnen niet door het model van de Toestemmingen van de Onderneming worden gecontroleerd, maar maken deel uit van de StandaardWerkruimte: Klassiek van het doel, Adobe Experience Manager (AEM), de Mobiele Diensten van de Adobe, en middelen die via API worden gecreeerd. De middelen die via API worden gecreeerd omvatten activiteiten, publiek, codeaanbiedingen, en beeldaanbiedingen).
   * Aanbiedingen voor afbeeldingen (elementen die zijn opgeslagen onder `https://[tenantName].marketing.adobe.com/content/mac/[tenantName]/target/offers.html#image-library` kan momenteel niet worden gecontroleerd door het model van de Toestemmingen van de Onderneming.
   * clickTracking en richt werk opnieuw wanneer de bestemmingsverbinding of bestemmingspagina deel van een bezit uitmaken dat in de activiteit inbegrepen is. Klik opTracking werkt mogelijk niet wanneer u de opdracht `targetPageParams()` functie. De `targetPageParamsAll()` is de aanbevolen functie.

  [!DNL Target] momenteel is een `at_property` om aanwezig te zijn op om het even welke pagina waar het volgen voorkomt. Als het teken (1) niet aanwezig is, (2) niet op het tijdstip van activiteitenopstelling (binnen VEC) wordt ontdekt, of (3) niet overgegaan tot de clickTracking vraag van het Doel via `targetPageParamsAll()` , wordt de metrische waarde niet verhoogd en wordt weergegeven als &quot;0.&quot;

  Hetzelfde geldt voor activiteiten die omleidingen gebruiken. De doelpagina moet een `at_property` en worden erkend op het tijdstip van opstelling binnen VEC.

  In een toekomstige release werkt Target op pagina&#39;s waar geen `at_property` token aanwezig is of pagina&#39;s waarop een ander token aanwezig is `at_property` token is aanwezig.

* De functionaliteit voor gebruikersmachtigingen voor Enterprise wordt niet ondersteund in Adobe Developer API-aanroepen.

## Veelgestelde vragen {#faqs}

Veelgestelde vragen over bedrijfsmachtigingen zijn onder andere:

### Wat gebeurt er als een gebruiker meerdere rollen en machtigingen heeft? {#multiple-roles}

Als een gebruiker veelvoudige rollen en toestemmingen heeft, wordt de rol met de hogere toestemmingen toegepast. Als een gebruiker bijvoorbeeld [!UICONTROL Observer] en [!UICONTROL Approver] rollen, de [!UICONTROL Approver] rol wordt toegepast.

### Kan ik een activiteit van één werkruimte naar een andere verplaatsen?

Helaas kunt u activiteiten niet van de ene werkruimte naar de andere verplaatsen. U kunt een activiteit echter naar elke werkruimte kopiëren in de wetenschap dat de rapportgegevens niet worden overgedragen. Zie &quot;Een activiteit kopiëren/bewerken bij het gebruik van werkruimten&quot; voor meer informatie in [Activiteit kopiëren/bewerken bij gebruik van werkruimten](/help/main/c-activities/edit-activity.md#section_45A92E1DD3934523B07E71EF90C4F8B6).

Activiteiten die vóór de migratie zijn gemaakt, worden in de standaardwerkruimte op dezelfde manier uitgevoerd, tenzij ze worden bewerkt en toegewezen eigenschappen. Activiteiten die onder een specifieke werkruimte vallen, respecteren de eigenschap die aan die werkruimte is toegewezen. Daarom is het mogelijk dat gedrag niet hetzelfde blijft als vóór de migratie.

### Kan ik een publiek van de ene werkruimte naar de andere verplaatsen? {#move-audience}

Ja, u kunt een publiek tussen werkruimten verplaatsen met de opdracht [!UICONTROL More Actions] de optie [!UICONTROL Audiences] pagina.

1. Klik op de knop **[!UICONTROL More Actions]** (de drie ellipsen), en klik dan **[!UICONTROL Move]**.

   ![Meer handelingen > Verplaatsen](/help/main/administrating-target/c-user-management/property-channel/assets/move-audience.png)

1. Selecteer de gewenste werkruimte in het menu **[!UICONTROL Workspace]** vervolgkeuzelijst en vervolgens op **[!UICONTROL Move]**.

   ![Selecteer het gewenste publiek om naar de nieuwe werkruimte te gaan](/help/main/administrating-target/c-user-management/property-channel/assets/workspace-move.png)

>[!NOTE]
>
>U moet de juiste rechten hebben om een publiek te bewerken. Bovendien mag het publiek niet bij andere activiteiten worden gebruikt. Als het publiek in andere activiteiten wordt gebruikt en u wilt het publiek naar een andere werkplaats verplaatsen, verwijdert u het publiek uit de andere activiteiten waar zij worden gebruikt.

### Waarom krijg ik een foutenmelding erop wijst die dat geen bezit aan deze activiteit wordt geassocieerd, alhoewel er een toegewezen bezit is?

Als u [!DNL Target] met tags in [!DNL Adobe Experience Platform] en krijg een foutbericht dat aangeeft dat er geen eigenschap is die aan de activiteit is gekoppeld, geeft u door `at_property` met de `targetPageParams` functie.

### Zijn klikspooromzettingen geregistreerd als een omgeleide pagina en activiteit URL tot verschillende eigenschappen behoren?

Klik op Tekstspatiëring wordt niet opgenomen op pagina&#39;s waarvan de pagina en activiteit-URL tot verschillende eigenschappen behoren.

Overweeg het volgende scenario:

* Pagina1 behoort tot Eigenschap1.
* Pagina2 behoort tot Eigenschap2.
* In de activiteit, richt Pagina1 zich aan Pagina2, die kliksporen bevat.

Wanneer een bezoeker Pagina1 in browser opent, wordt de bezoeker opnieuw gericht aan Pagina2. Omdat Page2 niet kwalificeert om de activiteit te leveren, bevat zijn vraag van het Doel geen kliksporen in zijn reactie.

Als de omleidingspagina en de activiteit-URL tot dezelfde eigenschap behoren, werkt het klikken op de tracks zoals verwacht. Zie voor meer informatie [Klikken bijhouden](/help/main/c-activities/r-success-metrics/click-tracking.md).

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Trainingsvideo: Trainingsvideo voor bedrijfsmachtigingen ![Overzicht badge](/help/main/assets/overview.png)

Leerdoelstellingen:

* De drie rolniveaus die de gebruikers van Adobe Target kunnen houden
* De concepten Eigenschappen en Werkruimten, en hoe deze grenzen en groeperingen werken om voor controle over de toegangsniveaus van gebruikers toe te staan
* Verschillende eigenschappenvoorbeelden voor uw organisatie

>[!VIDEO](https://video.tv.adobe.com/v/19042/)

### Kantooruren: [!DNL Target] Hoogwaardige werkruimten

Deze video is een opname van &quot;Office Hours&quot;, een initiatief van het team van de klantenservice van de Adobe.

* Een werkruimte maken (productprofiel)
* Eigenschappen maken
* Gebruikers toevoegen
* Implementatie bijwerken

>[!NOTE]
>
>De [!DNL Target] [!UICONTROL Administration] menu-interface (voorheen [!UICONTROL Setup]) is opnieuw ontworpen om betere prestaties te bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De informatie in de volgende video is correct, maar de opties kunnen zich op iets verschillende locaties bevinden.

>[!VIDEO](https://video.tv.adobe.com/v/23643/)
