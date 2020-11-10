---
keywords: criteria;algorithm;industry vertical;page type;recommendation key;recommendation logic;logic;data range;behavior data source;partial design;backup recommendations;inclusion rules;attribute weighting;current category;custom attribute;last purchased item;last viewed item;most viewed item;most viewed item;favorite category;popularity;recently viewed item;last purchased;last viewed;most viewed;favorite;recently viewed
description: Criteria bepalen de inhoud van je Adobe Recommendations-activiteiten. Maak criteria om de aanbevelingen weer te geven die het meest geschikt zijn voor uw activiteit.
title: Criteria maken
feature: criteria
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '2297'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) : criteria maken{#create-criteria}

Criteria in [!UICONTROL Adobe Target] het controleren van de inhoud van uw [!UICONTROL Recommendations] [!UICONTROL Recommendations] activiteiten. Maak criteria om de aanbevelingen weer te geven die het meest geschikt zijn voor uw activiteit. Deze criteria gebruiken de acties van de bezoeker om te bepalen welke inhoud of producten aan vertoning worden.

In de volgende secties wordt uitgelegd hoe u nieuwe criteria kunt maken.

## Het scherm Nieuwe criteria maken openen

Er zijn meerdere manieren om het [!UICONTROL Create New Criteria] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations] activiteiten.
* Wanneer u een [!DNL Recommendations] activiteit gebruikend [!UICONTROL Visual Experience Composer] (VEC) creeert, wordt u onmiddellijk genomen aan het [!UICONTROL Select Criteria] scherm nadat u een element op uw pagina selecteert en klikt [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], of [!UICONTROL Insert Recommendations After]. U kunt dan een beschikbare criteria selecteren of u kunt klikken **[!UICONTROL Create Criteria]**. Als u nieuwe criteria maakt, kunt u uw criteria opslaan voor gebruik met andere [!DNL Recommendations] activiteiten. Zie Een Recommendations-activiteit [maken voor meer informatie](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Als u een [!DNL Recommendations] activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] vak op de pagina en selecteert u **[!UICONTROL Change Criteria]**. Klik op het [!UICONTROL Select Criteria] scherm **[!UICONTROL Create Criteria]**. U kunt de nieuwe criteria opslaan voor gebruik met andere [!DNL Recommendations] activiteiten.

In de volgende stappen wordt ervan uitgegaan dat u het [!UICONTROL Create New Criteria] scherm opent met de eerste methode: het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

   ![Nieuwe criteria maken](/help/c-recommendations/c-algorithms/assets/CreateNewCriteria_full-new.png)

1. Configureer de informatie in de volgende secties.

## Basisinformatie {#info}

1. Typ een **[!UICONTROL Criteria Name]**.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de criteria te beschrijven. U kunt bijvoorbeeld uw criteria &quot;Hoogste margeproducten&quot; noemen, maar u wilt niet dat die titel openbaar wordt weergegeven. Zie de volgende stap om de naar buiten gerichte titel in te stellen.

   ![Sectie Basisinformatie](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Typ een openbare verwijzing die op de pagina wordt weergegeven voor alle aanbevelingen die gebruikmaken van deze criteria. **[!UICONTROL Display Title]**

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

1. Selecteer een **[!UICONTROL Page Type]**.

   U kunt meerdere paginatypen selecteren.

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde criteria te categoriseren, die het gemakkelijker maken om criteria voor andere [!DNL Recommendations] activiteiten opnieuw te gebruiken.

1. Selecteer een **[!UICONTROL Recommendation Key]**.

   Voor meer informatie over het baseren van criteria op een sleutel, zie de aanbeveling [baseren op een aanbeveling sleutel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. Selecteer de **[!UICONTROL Recommendation Logic]**.

   Zie [Criteria](/help/c-recommendations/c-algorithms/algorithms.md)voor meer informatie over de opties van de aanbevolen logica.

   >[!NOTE]
   >
   >Als u **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]** selecteert, kunt u regels [voor gelijkenis van de](#similarity)inhoud instellen.

## Gegevensbron {#data-source}

1. Plaats **[!UICONTROL Data Range]** om de tijdwaaier van beschikbare historische gegevens van het gebruikersgedrag te bepalen wanneer het bepalen van welke te tonen aanbevelingen.

   ![Schuifregelaar voor gegevensbereik](/help/c-recommendations/c-algorithms/assets/data-range.png)

   Als uw site veel verkeer heeft en het gedrag vaak verandert, kiest u een korter gegevensvenster. Een korter venster laat toe om ontvankelijker aan veranderingen in de markt en in uw zaken [!DNL Recommendations] te zijn. Een korter venster betekent bijvoorbeeld dat wijzigingen in het gedrag van de bezoeker [!DNL Recommendations] zullen worden gedetecteerd wanneer uw bezoekers seizoensgebonden winkelen beginnen, zoals &#39;back-to-school&#39;-winkelen of &#39;Kerstmis&#39;, en dat ze artikelen zullen aanbevelen die geschikt zijn voor die winkelseizoenen.

   Als u niet veel gegevens hebt of als het gedrag van de bezoeker niet vaak verandert, kunt u een langer venster selecteren. Nochtans, voor vele plaatsen, resulteert een korter venster in betere aanbevelingen.

   De beschikbare gegevensbereiken zijn:

   * Twee dagen
   * Eén week
   * Twee weken
   * Eén maand
   * Twee maanden

1. (Voorwaardelijk) Selecteer het gewenste **[!UICONTROL Behavioral Data Source]**: [!UICONTROL mboxes] of [!UICONTROL Analytics].

   >[!NOTE]
   >
   >De [!UICONTROL Behavioral Data Source] sectie wordt alleen weergegeven als uw implementatie [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt.

   ![Sectie Gedragsgegevensbron](/help/c-recommendations/c-algorithms/assets/behavioural-data-source.png)

   Als u kiest, selecteert u [!UICONTROL Analytics]de gewenste rapportsuite.

   Als de criteria als gedragsgegevensbron gebruiken, zodra gecreeerd, hangt de tijd voor criteria beschikbaarheid van af of de geselecteerde rapportreeks en het raadplegingsvenster voor een andere criteria, zoals hieronder verklaard is gebruikt: [!DNL Adobe Analytics]

   * **Eenmalige installatie** van rapportsuite: De eerste keer dat een rapportsuite wordt gebruikt met een bepaald terugzoekvenster voor gegevensbereik, [!DNL Target Recommendations] kan het twee tot zeven dagen duren voordat de gedragsgegevens voor de geselecteerde rapportsuite volledig zijn gedownload van [!DNL Analytics]. Dit tijdframe is afhankelijk van de [!DNL Analytics] systeembelasting.
   * **Nieuwe of bewerkte criteria met behulp van een reeds beschikbare rapportsuite**: Als bij het maken van nieuwe criteria of het bewerken van bestaande criteria de geselecteerde rapportsuite al is gebruikt met [!DNL Target Recommendations], met een gegevensbereik dat gelijk is aan of kleiner is dan het geselecteerde gegevensbereik, zijn de gegevens direct beschikbaar en is een eenmalige installatie niet vereist. In dit geval, of als de montages van een algoritme terwijl het wijzigen van de geselecteerde rapportreeks of gegevenswaaier worden uitgegeven, loopt het algoritme of herstelt binnen 12 uren.
   * **Doorlopende algoritme wordt uitgevoerd**: Gegevensstromen van [!DNL Analytics] naar [!DNL Target Recommendations] dagelijks. Bijvoorbeeld, voor de [!UICONTROL Viewed Affinity] aanbeveling, wanneer een gebruiker een product bekijkt, wordt een product-mening het volgen vraag overgegaan in dicht [!DNL Analytics] bij real time. De [!DNL Analytics] gegevens worden [!DNL Target] vroeg de volgende dag geduwd en het algoritme in minder dan 12 uren in werking [!DNL Target] gesteld.

   Zie Adobe Analytics [gebruiken met Target Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md)voor meer informatie.

## Inhoud {#content}

De regels van de inhoud bepalen wat gebeurt als het aantal geadviseerde punten uw [aanbevelingen ontwerp](/help/c-recommendations/c-design-overview/design-overview.md)niet vult. Het is mogelijk dat [!DNL Recommendations] criteria minder aanbevelingen teruggeven dan uw ontwerp vraagt. Als uw ontwerp bijvoorbeeld sleuven voor vier items bevat, maar uw criteria slechts twee items aanbevolen laten, kunt u de resterende sleuven leeg laten of back-upaanbevelingen gebruiken om de extra sleuven te vullen.

![Sectie Inhoud](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Optioneel) Sleep de **[!UICONTROL Partial Design Rendering]** schakeloptie naar de positie &quot;aan&quot;.

   Er worden zoveel mogelijk sleuven ingevuld, maar in de ontwerpsjabloon kan lege ruimte voor de resterende sleuven zijn opgenomen. Als deze optie is uitgeschakeld en er onvoldoende inhoud is om alle beschikbare sleuven te vullen, worden geen aanbevelingen gedaan en wordt in plaats daarvan standaardinhoud weergegeven.

   Schakel deze optie in als u wilt dat aanbevelingen worden gedaan met lege sleuven. Gebruik back-upaanbevelingen als u wilt dat de aanbevolen sleuven worden gevuld met inhoud op basis van uw criteria met lege sleuven die zijn gevuld met vergelijkbare of populaire inhoud van uw site, zoals in de volgende stap wordt uitgelegd.

1. (Optioneel) Sleep de **[!UICONTROL Show Backup Recommendations]** schakeloptie naar de positie &quot;aan&quot;.

   Vul eventueel resterende lege sleuven in het ontwerp met een willekeurige selectie van de meest bekeken producten van de hele site.

   Het gebruik van aanbevelingen voor back-ups zorgt ervoor dat het ontwerp van uw aanbeveling alle beschikbare sleuven vult. Stel dat u een ontwerp van 4 x 1 hebt, zoals hieronder wordt geïllustreerd:

   ![4 x 1 ontwerp](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Op basis van uw criteria worden slechts twee objecten aanbevolen. Als u de [!UICONTROL Partial Design Rendering] optie inschakelt, worden de eerste twee sleuven gevuld, maar blijven de resterende twee sleuven leeg. Als u de [!UICONTROL Show Backup Recommendations] optie echter inschakelt, worden de eerste twee sleuven gevuld op basis van uw opgegeven criteria en worden de resterende twee sleuven gevuld op basis van uw aanbevelingen voor back-up.

   De volgende matrix toont het resultaat dat u zult waarnemen wanneer u de opties [!UICONTROL Partial Design Rendering] en [!UICONTROL Backup Recommendations] opties gebruikt:

   | Gedeeltelijke rendering van ontwerp | Backup Recommendations | Resultaat |
   |--- |--- |--- |
   | Uitgeschakeld | Uitgeschakeld | Als er minder aanbevelingen worden geretourneerd dan door het ontwerp wordt gevraagd, wordt het ontwerp van de aanbevelingen vervangen door de standaardinhoud en worden er geen aanbevelingen weergegeven. |
   | Ingeschakeld | Uitgeschakeld | Het ontwerp wordt teruggegeven, maar kan lege ruimte omvatten als minder aanbevelingen zijn teruggekeerd dan het ontwerp verzoekt. |
   | Ingeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in.<br>Als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp gedeeltelijk teruggegeven.<br>Als de criteria geen aanbevelingen terugkeren, en de integratieregels reserveaanbevelingen tot nul beperken, wordt het ontwerp vervangen met standaardinhoud. |
   | Uitgeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in.<br>Als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp vervangen door standaardinhoud en geen aanbevelingen worden getoond. |

   Zie [Een back-upaanbeveling](/help/c-recommendations/c-algorithms/backup-recs.md)gebruiken voor meer informatie.

1. (Voorwaardelijk) Als u **[!UICONTROL Show Backup Recommendations]** in de vorige stap selecteerde, kunt u toelaten **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   In de insluitingsregels wordt bepaald welke items in uw aanbevelingen worden opgenomen. Welke opties beschikbaar zijn, is afhankelijk van de verticale situatie in uw branche.

   Zie [Opnameregels](#inclusion) hieronder opgeven voor meer informatie.

1. (Optioneel) Sleep de **[!UICONTROL Recommend Previously Purchased Items]** schakeloptie naar de positie &quot;aan&quot;.

   Deze instelling is gebaseerd op de `productPurchasedId`sjabloon. Standaard wordt eerder aangeschafte items niet aanbevolen. In de meeste gevallen wilt u geen objecten promoten die een klant onlangs heeft aangeschaft. Het is handig om objecten te verkopen die mensen doorgaans slechts eenmaal kopen, zoals kajaks. Als je objecten verkoopt die mensen herhaaldelijk kunnen kopen, zoals shampoo of andere persoonlijke objecten, moet je deze optie inschakelen.

## Vergelijkbare inhoud {#similarity}

Gebruik [!UICONTROL Content Similarity] regels om aanbevelingen te doen op basis van item- of mediakenmerken.

>[!NOTE]
>
>Als u **[!UICONTROL Items]**/ hebt geselecteerd **[!UICONTROL Media with Similar Attributes]** als uw [aanbevolen logica](#info), kunt u regels voor de gelijkenis van de inhoud instellen.

De gelijkenis van de inhoud vergelijkt de sleutelwoorden van puntattributen en doet aanbevelingen die op hoeveel sleutelwoorden verschillende punten in gemeenschappelijk hebben worden gebaseerd. Recommendations op basis van gelijkenis met inhoud vereist geen gegevens uit het verleden om sterke resultaten te bereiken.

Het gebruik van gelijkenis in de inhoud om aanbevelingen te genereren is vooral effectief voor nieuwe items. Deze worden waarschijnlijk niet weergegeven in aanbevelingen met *Personen die dit hebben bekeken, Bekeken dat* en andere logica die is gebaseerd op gedrag in het verleden. U kunt de gelijkenis van de inhoud ook gebruiken om nuttige aanbevelingen voor nieuwe bezoekers te produceren, die geen vroegere aankopen of andere historische gegevens hebben.

Wanneer u selecteert **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]**, hebt u de optie om regels tot stand te brengen om het belang van specifieke puntattributen in het bepalen van aanbevelingen te verhogen of te verminderen. Voor artikelen zoals boeken, zou u het belang van attributen zoals *genre*, *auteur*, *reeksen*, etc. kunnen willen verhogen, om gelijkaardige boeken aan te bevelen.

![](assets/ContentSimilarity.png)

Omdat bij gelijkenis met inhoud trefwoorden worden gebruikt om items te vergelijken, kunnen sommige kenmerken, zoals *bericht* of *beschrijving*, &#39;ruis&#39; in de vergelijking introduceren. U kunt regels maken om deze kenmerken te negeren.

Standaard zijn alle kenmerken ingesteld op *Basislijn*. U hoeft geen regel te maken, tenzij u deze instelling wilt wijzigen.

>[!NOTE]
>
>Het algoritme voor de gelijkenis van de inhoud kan gebruikmaken van willekeurige sampling bij het berekenen van gelijkenis tussen items. Hierdoor kunnen de overeenkomsten tussen items per algoritme verschillen.

## Opnameregels {#inclusion}

Met behulp van verschillende opties kunt u de items beperken die in uw aanbevelingen worden weergegeven. U kunt inclusieregels gebruiken terwijl het creëren van criteria of bevorderingen.

![Opnameregels](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Opnameregels zijn facultatief; nochtans, geeft het plaatsen van deze details u meer controle over de punten die in uw aanbevelingen verschijnen. Elk detail dat u vormt vernauwt verder de vertoningscriteria.

U kunt er bijvoorbeeld voor kiezen alleen vrouwenschoenen weer te geven met een voorraad van meer dan 50 en een prijs tussen 25 en 45 dollar. U kunt ook elk kenmerk van elkaar voorzien, zodat de items die voor uw bedrijf belangrijker zijn, meestal worden weergegeven.

U kunt er ook voor kiezen om vacatures weer te geven voor bezoekers die uw site alleen vanuit bepaalde steden bezoeken en die de vereiste universitaire graden hebben.

De opties voor de inclusieregel variëren per verticale branche. Standaard worden inclusieregels toegepast op back-upaanbevelingen.

>[!IMPORTANT]
>
>U moet opnemingsregels voorzichtig gebruiken. Ze zijn bijvoorbeeld handig als uw organisatie regels heeft die vereisen dat één merk niet wordt aanbevolen terwijl een ander merk wordt weergegeven. Er zijn echter alternatieve kosten voor deze functie. U kunt mogelijk een percentage aan lift verliezen door bepaalde items te beperken zodat ze niet kunnen worden weergegeven wanneer ze normaal gesproken aan de hand van de activiteitscriteria worden weergegeven.

De inclusieregels worden aangesloten bij EN. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

Voer de volgende stappen uit om een eenvoudige regel voor insluiting te maken, zoals eerder vermeld, om alleen vrouwenschoenen weer te geven met een voorraad van meer dan 50 en een prijs tussen 25 en 45 dollar:

1. Stel een prijsbereik in voor de producten die u wilt aanbevelen.
1. Stel het minimale voorraadbedrag in voor de producten die u wilt aanbevelen.
1. Vorm de aanbeveling om punten slechts te tonen wanneer zij aan bepaalde criteria voldoen.

   ![](assets/Recs_InclusionRules.png)

   U kunt opgeven dat items alleen worden opgenomen wanneer een van de kenmerken in de lijst voldoet aan een of meer opgegeven voorwaarden of niet overeenkomt.

   De beschikbare beoordelaars zijn afhankelijk van de waarde die u kiest in de eerste vervolgkeuzelijst. U kunt meerdere items weergeven. Deze items worden geëvalueerd met OR.

   De veelvoudige regels worden gecombineerd met EN.

   >[!NOTE]
   >
   >Met deze optie beperkt u de items die in de aanbeveling worden weergegeven. Het heeft geen invloed op de pagina&#39;s waarop de aanbeveling wordt weergegeven. Als u wilt beperken waar de aanbeveling wordt weergegeven, selecteert u de pagina&#39;s in de ervaringscomposer.

Zie [Dynamische en statische inclusieregels](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)gebruiken voor meer informatie.

## Kenmerkweging {#weighting}

U kunt veelvoudige regels toevoegen om het algoritme &quot;te &quot;verschuiven&quot;dat op belangrijke informatie of meta-gegevens over de inhoudscatalogus wordt gebaseerd zodat bepaalde punten waarschijnlijker om worden getoond.

U kunt bijvoorbeeld een hogere wegingsfactor toepassen op onverkochte objecten, zodat deze vaker in de aanbeveling voorkomen. Niet-verkochte objecten worden niet volledig uitgesloten, maar ze verschijnen minder vaak. Meerdere gewogen kenmerken kunnen op hetzelfde algoritme worden toegepast en de gewogen kenmerken kunnen in de aanbeveling op gesplitst verkeer worden getest.

1. Kies een waarde.

   De waarde bepaalt het type item dat vaker wordt weergegeven, op basis van een van de verschillende beschikbare criteria.

1. Kies een evaluator.

1. Typ het trefwoord om de regelkenmerken te voltooien.

   De volledige regel kan bijvoorbeeld &#39;Categorie bevat schoenen voor subreeksen&#39; zijn.

   ![](assets/Recs_AttributeWeighting.png)

1. Selecteer de dikte die u aan de regel wilt toewijzen.

   De opties variëren van 0 tot 100 in stappen van 25.

1. Voeg desgewenst aanvullende regels toe.

Klik wanneer u klaar bent op **[!UICONTROL Save]**.

Als u een nieuwe [!UICONTROL Recommendations] activiteit creeert of een bestaande uitgeeft, wordt de **[!UICONTROL Save criteria for later]** controledoos door gebrek geselecteerd. Als u de criteria niet wilt gebruiken in andere activiteiten, schakelt u het selectievakje uit voordat u het bestand opslaat.

## Trainingsvideo: Criteria maken in Recommendations (12:33) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
