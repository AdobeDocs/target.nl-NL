---
keywords: criteria;algoritme;industrie verticaal;paginatype;aanbeveling sleutel;logica;gegevenswaaier;gegevenswaaier;lookback venster;gedraggegevensbron;gedeeltelijk ontwerp;steun aanbevelingen;opnameregels;opnameregels;attribuut weging;huidige categorie;laatst gekocht punt;laatst bekeken punt;het meest bekeken punt;meest bekeken punt;favoriete categorie;populariteit;onlangs bekeken punt;laatst bekeken punt;laatst bekeken punt;laatst bekeken;meest bekeken;favoriet;onlangs bekeken
description: Leer hoe u criteria maakt die de inhoud van uw Adobe Recommendations-activiteiten bepalen om de aanbevelingen weer te geven die het meest geschikt zijn voor uw activiteiten.
title: Hoe maak ik criteria in aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 3f4f59b2-6637-4c33-bf17-bff11bef7173
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '2694'
ht-degree: 0%

---

# Criteria maken

Criteria in [!UICONTROL Adobe Target] [!UICONTROL Recommendations] bepalen de inhoud van uw [!UICONTROL Recommendations] -activiteiten. Maak criteria om de aanbevelingen weer te geven die het meest geschikt zijn voor uw activiteit. Deze criteria gebruiken de acties van de bezoeker om te bepalen welke inhoud of producten aan vertoning worden.

In de volgende secties wordt uitgelegd hoe u nieuwe criteria kunt maken.

## Het scherm Nieuwe criteria maken openen

Er zijn meerdere manieren om het [!UICONTROL Create New Criteria] -scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** . De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations] -activiteiten.
* Wanneer u een [!DNL Recommendations] -activiteit maakt met behulp van [!UICONTROL Visual Experience Composer] (VEC), wordt u direct naar het [!UICONTROL Select Criteria] -scherm geleid nadat u een element op de pagina hebt geselecteerd en op [!UICONTROL Replace w/ Recommendations] , [!UICONTROL Insert Recommendations Before] of [!UICONTROL Insert Recommendations After] hebt geklikt. U kunt vervolgens een beschikbare criteria selecteren of op **[!UICONTROL Create Criteria]** klikken. Als u nieuwe criteria maakt, kunt u uw criteria opslaan voor gebruik met andere [!DNL Recommendations] -activiteiten. Voor meer informatie, zie [&#x200B; een activiteit van Aanbevelingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md) creëren.
* Wanneer u een [!DNL Recommendations] -activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] -vak op de pagina en selecteert u **[!UICONTROL Change Criteria]** . Klik op [!UICONTROL Select Criteria] in het **[!UICONTROL Create Criteria]** -scherm. U kunt de nieuwe criteria opslaan voor gebruik met andere [!DNL Recommendations] -activiteiten.

In de volgende stappen wordt ervan uitgegaan dat u het [!UICONTROL Create New Criteria] -scherm opent via de eerste methode: het **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** -bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** .

   ![&#x200B; creeer Nieuwe Criteria &#x200B;](assets/CreateNewCriteria_full-new.png)

1. Configureer de informatie in de volgende secties.

## [!UICONTROL Basic Information] {#info}

1. Typ een **[!UICONTROL Criteria Name]** .

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de criteria te beschrijven. U kunt bijvoorbeeld uw criteria &quot;Hoogste margeproducten&quot; noemen, maar u wilt niet dat die titel openbaar wordt weergegeven. Zie de volgende stap om de openbare-gerichte titel te plaatsen.

   ![&#x200B; Basissectie van de Informatie &#x200B;](assets/basic-information.png)

1. Typ een publiekelijk gericht **[!UICONTROL Display Title]** om op de pagina te verschijnen voor alle aanbevelingen die van deze criteria gebruikmaken.

   U kunt bijvoorbeeld &quot;Personen die dit hebben bekeken, hebben dit weergegeven&quot; of &quot;Gelijksoortige producten&quot; weergeven wanneer u deze criteria gebruikt om aanbevelingen weer te geven.

1. Typ een korte **[!UICONTROL Description]** van de criteria.

   Aan de hand van deze beschrijving kunt u de criteria vaststellen en informatie over het doel van de criteria toevoegen.

1. Selecteer de industrie verticaal die op de doelstellingen van uw aanbevelingen activiteit wordt gebaseerd.

   | Verticale industrie | Goal |
   |--- |--- |
   | Detailhandel/e-handel | Conversie die tot aankoop leidt |
   | Genereren van leads/B2B/Financiële services | Omzetten zonder aankoop |
   | Media/Publiceren | Betrokkenheid |

   Andere criteria worden gewijzigd op basis van de verticale industriestandaard die u selecteert.

1. Selecteer een **[!UICONTROL Page Type]** .

   U kunt meerdere paginatypen selecteren.

   Samen worden de verticale en paginatypen van de branche gebruikt om uw bewaarde criteria te categoriseren, die het gemakkelijker maken om criteria voor andere [!DNL Recommendations] activiteiten opnieuw te gebruiken.

## [!UICONTROL Recommendations Algorithm] {#rec-algo}

1. Selecteer een **[!UICONTROL Algorithm Type]** en **[!UICONTROL Algorithm]** :

   ![&#x200B; Geadviseerde sectie van het Algoritme &#x200B;](assets/recommended-algorithm.png)

   | Het type Algorithm | Wanneer gebruiken | Beschikbare algoritmen |
   | --- | --- | --- |
   | [!UICONTROL Cart-Based] | Aanbevelingen doen op basis van de inhoud van het winkelwagentje. | <ul><li>Personen die ze bekeken, bekeken ze</li><li>Mensen die ze bekeken, kochten hen</li><li>Mensen die deze hebben gekocht, hebben de</li></ul> |
   | [!UICONTROL Popularity-Based] | Aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker. | <ul><li>Meest bekeken op de site</li><li>Meest bekeken op rubriek</li><li>Meest bekeken door kenmerk Item</li><li>Topverkopers op de hele site</li><li>Topverkopers op rubriek</li><li>Topverkopers op objectkenmerk</li><li>Metrisch, boven op Analytics</li></ul> |
   | [!UICONTROL Item-Based] | Aanbevelingen doen op basis van het zoeken naar objecten die vergelijkbaar zijn met een item dat de gebruiker momenteel bekijkt of onlangs heeft bekeken. | <ul><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Mensen die dit bekeken hebben, hebben het volgende gekocht</li><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Objecten met vergelijkbare kenmerken</li></ul> |
   | [!UICONTROL User-Based] | Aanbevelingen doen op basis van het gedrag van de gebruiker. | <ul><li>Onlangs bekeken objecten</li><li>Aanbevolen voor u</li></ul> |
   | [!UICONTROL Custom Criteria] | Aanbevelingen doen op basis van een aangepast bestand dat u uploadt. | <ul><li>Aangepast algoritme</li></ul> |

   >[!NOTE]
   >
   >Als u **[!UICONTROL Items]** selecteert/ **[!UICONTROL Media with Similar Attributes]**, zult u de optie hebben om [&#x200B; de regels van de inhoudsgelijkenis &#x200B;](#similarity) te plaatsen.

1. Zoals vereist, selecteer het Attribuut van het Punt **en** Profiel om **, Sleutel van de Aanbeveling van a** **,** Filtrerend Zeer belangrijk **, en/of** Metrische Analytics **aan te passen om het algoritme te vormen.**

De resterende opties van de algoritmeconfiguratie variëren afhankelijk van het geselecteerde algoritme. Als u de configuratie van het algoritme wilt voltooien, selecteert u een [!UICONTROL Recommendation Key], [!UICONTROL Filtering Key], [!UICONTROL Co-Occurrence Basis], [!UICONTROL Analytics Metric] en/of [!UICONTROL Item Attribute] en [!UICONTROL Profile Attribute to Match] .

Voor meer informatie over het kiezen van a [!UICONTROL Recommendation Key], zie [&#x200B; Baseer de aanbeveling op een aanbeveling sleutel &#x200B;](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## [!UICONTROL Data Source] {#data-source}

1. Selecteer het gewenste **[!UICONTROL Behavioral Data Source]**: [!UICONTROL Adobe Target] of [!UICONTROL Analytics] .

   >[!NOTE]
   >
   >De [!UICONTROL Behavioral Data Source] sectie toont slechts als uw implementatie [&#x200B; Analytics voor Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt.

   ![&#x200B; de sectie van Source van de Gegevens van het Gedrag &#x200B;](assets/data-source.png)

   Als u [!UICONTROL Analytics] kiest, selecteert u de gewenste rapportsuite.

   Als de criteria [!DNL Adobe Analytics] als gegevensbron voor gedrag, zodra gecreeerd gebruiken, hangt de tijd voor criteria beschikbaarheid af van of de geselecteerde rapportreeks en het raadplegingsvenster voor een andere criteria, zoals hieronder verklaard is gebruikt:

   * **Eenmalige opstelling van de rapportreeks**: De eerste keer wordt een rapportreeks gebruikt met een bepaald venster van de gegevenswaaierraadpleging, [!DNL Target Recommendations] kan van twee tot zeven dagen nemen om de gedragsgegevens voor de geselecteerde rapportreeks van [!DNL Analytics] volledig te downloaden. Dit tijdframe is afhankelijk van het laden van het [!DNL Analytics] -systeem.
   * **Nieuwe of uitgegeven criteria die een reeds beschikbare rapportreeks** gebruiken: Wanneer het creëren van nieuwe criteria of het uitgeven van een bestaande criteria, als de geselecteerde rapportreeks reeds met [!DNL Target Recommendations], met een gegevenswaaier gelijk aan of minder dan de geselecteerde gegevenswaaier is gebruikt, dan zijn de gegevens onmiddellijk beschikbaar en geen eenmalig opstelling wordt vereist. In dit geval, of als de montages van een algoritme terwijl het wijzigen van de geselecteerde rapportreeks of gegevenswaaier worden uitgegeven, loopt het algoritme of herstelt binnen 12 uren.
   * **Doorlopende algoritmelooppas**: De stromen van gegevens van [!DNL Analytics] aan [!DNL Target Recommendations] op een dagelijkse basis. Voor de aanbeveling [!UICONTROL Viewed Affinity] geldt dat wanneer een gebruiker bijvoorbeeld een product bekijkt, een aanroep voor het bijhouden van de productweergave wordt doorgegeven aan [!DNL Analytics] dicht bij real-time. De [!DNL Analytics] -gegevens worden [!DNL Target] vroeg op de volgende dag weergegeven en [!DNL Target] voert het algoritme uit binnen 12 uur.

   Voor meer informatie, zie [&#x200B; Gebruik Adobe Analytics met de Aanbevelingen van het Doel &#x200B;](/help/main/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

1. Stel de **[!UICONTROL Lookback Window]** in om het tijdbereik te bepalen van de beschikbare gegevens over historisch gebruikersgedrag die moeten worden gebruikt om te bepalen welke aanbevelingen moeten worden weergegeven. Deze optie is beschikbaar voor alle algoritmes, met uitzondering van Items met vergelijkbare kenmerken en aangepaste algoritmen.

   ![&#x200B; de schuif van het Venster van de Opzoeken &#x200B;](assets/data-range.png)

   Als uw site veel verkeer heeft en het gedrag vaak verandert, kiest u een korter gegevensvenster. Met een korter venster kan [!DNL Recommendations] beter reageren op veranderingen in de markt en in uw bedrijf. Een korter venster betekent bijvoorbeeld dat [!DNL Recommendations] wijzigingen in het gedrag van bezoekers detecteert wanneer uw bezoekers seizoensgebonden winkelen beginnen, zoals winkelen op school of Kerstmis, en dat  artikelen aanbeveelt die geschikt zijn voor die winkelseizoenen.

   Als u niet veel gegevens hebt of als het gedrag van de bezoeker niet vaak verandert, kunt u een langer venster selecteren. Voor veel sites leidt een korter venster echter tot aanbevelingen van hogere kwaliteit.

   De beschikbare gegevensbereiken zijn:

   | Venster opzoeken, optie | Bijgewerkte frequentie (weergegeven bij aanwijzen) | Ondersteunde algoritmen |
   | --- | --- | --- |
   | Zes uur | Algorithm wordt elke 3-6 uur uitgevoerd | [!UICONTROL Popularity-Based] algoritmen wanneer de geselecteerde [!UICONTROL Behavioral Data Source] is [!DNL Adobe Target] |
   | Eén dag | Algorithm wordt elke 12-24 uur uitgevoerd | [!UICONTROL Popularity-Based] algoritmen |
   | Twee dagen | Algorithm wordt elke 12-24 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Eén week | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Twee weken | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>Alle [!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Eén maand (30 dagen) | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Twee maanden (61 dagen) | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |

## [!UICONTROL Backup Content] {#content}

[!UICONTROL Backup Content] de regels bepalen wat gebeurt als het aantal geadviseerde punten uw [&#x200B; aanbevelingen ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/design-overview.md) niet vult. Het is mogelijk dat [!DNL Recommendations] -criteria minder aanbevelingen opleveren dan uw ontwerp vraagt. Als uw ontwerp bijvoorbeeld sleuven voor vier items bevat, maar uw criteria slechts twee items aanbevolen laten, kunt u de resterende sleuven leeg laten, back-upaanbevelingen gebruiken om de extra sleuven te vullen, of u kunt ervoor kiezen geen aanbevelingen weer te geven.

![&#x200B; sectie van de Inhoud &#x200B;](assets/content.png)

1. (Optioneel) Sleep de schakeloptie **[!UICONTROL Partial Design Rendering]** naar de positie &quot;aan&quot;.

   Er worden zoveel mogelijk sleuven ingevuld, maar in de ontwerpsjabloon kan lege ruimte voor de resterende sleuven zijn opgenomen. Als deze optie is uitgeschakeld en er onvoldoende inhoud is om alle beschikbare sleuven te vullen, worden geen aanbevelingen gedaan en wordt in plaats daarvan standaardinhoud weergegeven.

   Schakel deze optie in als u wilt dat aanbevelingen worden gedaan met lege sleuven. Gebruik back-upaanbevelingen als u wilt dat de aanbevolen sleuven worden gevuld met inhoud op basis van uw criteria met lege sleuven die zijn gevuld met vergelijkbare of populaire inhoud van uw site, zoals in de volgende stap wordt uitgelegd.

1. (Optioneel) Sleep de schakeloptie **[!UICONTROL Show Backup Content]** naar de positie &quot;aan&quot;.

   Vul eventueel resterende lege sleuven in het ontwerp met een willekeurige selectie van de meest bekeken producten van de hele site.

   Het gebruik van aanbevelingen voor back-ups zorgt ervoor dat het ontwerp van uw aanbeveling alle beschikbare sleuven vult. Stel dat u een ontwerp van 4 x 1 hebt, zoals hieronder wordt geïllustreerd:

   ![&#x200B; 4 x 1 ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/assets/velocity_example.png)

   Op basis van uw criteria worden slechts twee objecten aanbevolen. Als u de optie [!UICONTROL Partial Design Rendering] inschakelt, worden de eerste twee sleuven gevuld, maar blijven de resterende twee sleuven leeg. Als u echter de optie [!UICONTROL Show Backup Recommendations] inschakelt, worden de eerste twee sleuven gevuld op basis van de opgegeven criteria en worden de resterende twee sleuven gevuld op basis van uw aanbevelingen voor back-ups.

   De volgende matrix toont het resultaat dat u zult waarnemen wanneer u de opties [!UICONTROL Partial Design Rendering] en [!UICONTROL Backup Content] gebruikt:

   | Gedeeltelijke rendering van ontwerp | Back-upinhoud | Resultaat |
   |--- |--- |--- |
   | Uitgeschakeld | Uitgeschakeld | Als er minder aanbevelingen worden geretourneerd dan door het ontwerp wordt gevraagd, wordt het ontwerp van de aanbevelingen vervangen door de standaardinhoud en worden er geen aanbevelingen weergegeven. |
   | Ingeschakeld | Uitgeschakeld | Het ontwerp wordt teruggegeven, maar kan lege ruimte omvatten als minder aanbevelingen zijn teruggekeerd dan het ontwerp verzoekt. |
   | Ingeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in, waardoor het ontwerp volledig wordt gerenderd.<br> als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp gedeeltelijk teruggegeven.<br> als de criteria geen aanbevelingen terugkeren, en de integratieregels reserveaanbevelingen tot nul beperken, wordt het ontwerp vervangen met standaardinhoud. |
   | Uitgeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in, waardoor het ontwerp volledig wordt gerenderd.<br> als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp vervangen door standaardinhoud en geen aanbevelingen worden getoond. |

   Voor meer informatie, zie [&#x200B; Gebruik een reserveaanbeveling &#x200B;](/help/main/c-recommendations/c-algorithms/backup-recs.md).

1. (Voorwaardelijk) Als u **[!UICONTROL Show Backup Content]** in de vorige stap hebt geselecteerd, kunt u **[!UICONTROL Apply inclusion rules to backup recommendations]** inschakelen.

   In de insluitingsregels wordt bepaald welke items in uw aanbevelingen worden opgenomen. Welke opties beschikbaar zijn, is afhankelijk van de verticale situatie in uw branche.

   Voor meer details, zie [&#x200B; Specificeer inbegrepen regels &#x200B;](#inclusion) hieronder.

## Vergelijkbare inhoud {#similarity}

Gebruik [!UICONTROL Content Similarity] -regels om aanbevelingen te doen op basis van item- of mediakenmerken.

>[!NOTE]
>
>Als u **[!UICONTROL Item-Based]**/ **[!UICONTROL Media with Similar Attributes]** hebt geselecteerd als type algoritme en algoritme, kunt u regels voor gelijkenis van inhoud instellen.

De gelijkenis van de inhoud vergelijkt de sleutelwoorden van puntattributen en doet aanbevelingen die op hoeveel sleutelwoorden verschillende punten in gemeenschappelijk hebben worden gebaseerd. Aanbevelingen op basis van gelijkenis van inhoud vereisen geen gegevens uit het verleden om sterke resultaten te bereiken.

Het gebruiken van inhoudsgelijkenis om aanbevelingen te produceren is vooral efficiënt voor nieuwe punten, die niet waarschijnlijk in aanbevelingen zullen tonen gebruikend *Mensen die dit bekeken, Bekeken dat* en andere logica die op verleden gedrag wordt gebaseerd. U kunt de gelijkenis van de inhoud ook gebruiken om nuttige aanbevelingen voor nieuwe bezoekers te produceren, die geen vroegere aankopen of andere historische gegevens hebben.

Wanneer u **[!UICONTROL Item-Based]**/ **[!UICONTROL Media with Similar Attributes]** selecteert, kunt u regels maken om het belang van specifieke itemkenmerken bij het bepalen van aanbevelingen te vergroten of te verkleinen. Voor punten zoals boeken, zou u het belang van attributen zoals *genre*, *auteur*, *reeksen*, etc. kunnen willen opvoeren, om gelijkaardige boeken aan te bevelen.

![&#x200B; beeld ContentGelijksheid &#x200B;](assets/ContentSimilarity.png)

Omdat de inhoudsgelijkenis sleutelwoorden gebruikt om punten te vergelijken, kunnen sommige attributen, zoals *bericht* of *beschrijving*, &quot;lawaai&quot;in de vergelijking introduceren. U kunt regels maken om deze kenmerken te negeren.

Door gebrek, worden alle attributen geplaatst aan *Basislijn*. U hoeft geen regel te maken, tenzij u deze instelling wilt wijzigen.

>[!NOTE]
>
>Het algoritme voor de gelijkenis van de inhoud kan gebruikmaken van willekeurige sampling bij het berekenen van gelijkenis tussen items. Hierdoor kunnen de overeenkomsten tussen items per algoritme verschillen.

## Opnameregels {#inclusion}

Met behulp van verschillende opties kunt u de items beperken die in uw aanbevelingen worden weergegeven. U kunt inclusieregels gebruiken terwijl het creëren van criteria of bevorderingen.

![&#x200B; Regels van de Opsluiting &#x200B;](/help/main/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Opnameregels zijn optioneel. Als u deze details instelt, hebt u echter meer controle over de items die in uw aanbevelingen worden weergegeven. Elk detail dat u vormt vernauwt verder de vertoningscriteria.

U kunt er bijvoorbeeld voor kiezen alleen vrouwenschoenen weer te geven met een voorraad van meer dan 50 en een prijs tussen 25 en 45 dollar. U kunt ook elk kenmerk van elkaar voorzien, zodat de items die voor uw bedrijf belangrijker zijn, meestal worden weergegeven.

U kunt er ook voor kiezen om vacatures weer te geven voor bezoekers die uw site alleen vanuit bepaalde steden bezoeken en die de vereiste universitaire graden hebben.

De opties voor de inclusieregel variëren per verticale branche. Standaard worden inclusieregels toegepast op back-upaanbevelingen.

>[!IMPORTANT]
>
>U moet opnemingsregels voorzichtig gebruiken. Ze zijn bijvoorbeeld handig als uw organisatie regels heeft die vereisen dat één merk niet wordt aanbevolen terwijl een ander merk wordt weergegeven. Er zijn echter alternatieve kosten voor deze functie. U kunt mogelijk een percentage aan lift verliezen door bepaalde items te beperken zodat ze niet kunnen worden weergegeven wanneer ze normaal gesproken aan de hand van de activiteitscriteria worden weergegeven.

De inclusieregels worden aangesloten bij EN. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

Voer de volgende stappen uit om een eenvoudige regel voor insluiting te maken, zoals eerder vermeld, om alleen vrouwenschoenen weer te geven met een voorraad van meer dan 50 en een prijs tussen 25 en 45 dollar:

1. (Voorwaardelijk) Schuif de schakeloptie **[!UICONTROL Allow recently purchased items to be recommended?]** naar de positie &quot;aan&quot;.

   Deze instelling is gebaseerd op de instructie `productPurchasedId` . Standaard wordt eerder aangeschafte items niet aanbevolen. In de meeste gevallen wilt u geen objecten promoten die een klant onlangs heeft aangeschaft. Het is handig om objecten te verkopen die mensen doorgaans slechts eenmaal kopen, zoals kajaks. Als je objecten verkoopt die mensen herhaaldelijk kunnen kopen, zoals shampoo of andere persoonlijke objecten, moet je deze optie inschakelen.

1. Stel een prijsbereik in voor de producten die u wilt aanbevelen.
1. Stel het minimale voorraadbedrag in voor de producten die u wilt aanbevelen.
1. Vorm de aanbeveling om punten slechts te tonen wanneer zij aan bepaalde criteria voldoen.

   ![&#x200B; Recs_InclusionRules beeld &#x200B;](assets/Recs_InclusionRules.png)

   U kunt opgeven dat items alleen worden opgenomen wanneer een van de kenmerken in de lijst voldoet aan een of meer opgegeven voorwaarden of niet overeenkomt.

   De beschikbare beoordelaars zijn afhankelijk van de waarde die u kiest in de eerste vervolgkeuzelijst. U kunt meerdere items weergeven. Deze items worden geëvalueerd met OR.

   De veelvoudige regels worden gecombineerd met EN.

   >[!NOTE]
   >
   >Met deze optie beperkt u de items die in de aanbeveling worden weergegeven. Het heeft geen invloed op de pagina&#39;s waarop de aanbeveling wordt weergegeven. Als u wilt beperken waar de aanbeveling wordt weergegeven, selecteert u de pagina&#39;s in de ervaringscomposer.

Voor meer informatie, zie [&#x200B; Dynamische en statische opnemingsregels van het Gebruik &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

## Kenmerkweging {#weighting}

U kunt veelvoudige regels toevoegen om het algoritme &quot;te &quot;verschuiven&quot;dat op belangrijke informatie of meta-gegevens over de inhoudscatalogus wordt gebaseerd zodat bepaalde punten waarschijnlijker om worden getoond.

U kunt bijvoorbeeld een hogere wegingsfactor toepassen op onverkochte objecten, zodat deze vaker in de aanbeveling voorkomen. Niet-verkochte objecten worden niet volledig uitgesloten, maar ze verschijnen minder vaak. Meerdere gewogen kenmerken kunnen op hetzelfde algoritme worden toegepast en de gewogen kenmerken kunnen in de aanbeveling op gesplitst verkeer worden getest.

1. Kies een waarde.

   De waarde bepaalt het type item dat vaker wordt weergegeven, op basis van een van de verschillende beschikbare criteria.

1. Kies een evaluator.

1. Typ het trefwoord om de regelkenmerken te voltooien.

   De volledige regel kan bijvoorbeeld &#39;Categorie bevat schoenen voor subreeksen&#39; zijn.

   ![&#x200B; Recs_AttributeWeighting beeld &#x200B;](assets/Recs_AttributeWeighting.png)

1. Selecteer de dikte die u aan de regel wilt toewijzen.

   De opties variëren van 0 tot 100 in stappen van 25.

1. Voeg desgewenst aanvullende regels toe.

Klik op **[!UICONTROL Save]** als u klaar bent.

Als u een nieuwe [!UICONTROL Recommendations] -activiteit maakt of een bestaande activiteit bewerkt, is het selectievakje **[!UICONTROL Save criteria for later]** standaard ingeschakeld. Als u de criteria niet wilt gebruiken in andere activiteiten, schakelt u het selectievakje uit voordat u het bestand opslaat.

## De video van de opleiding: Creeer criteria in Aanbevelingen (12 :33) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
