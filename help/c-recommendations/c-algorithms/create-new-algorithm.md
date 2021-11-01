---
keywords: criteria;algoritme;industrie verticaal;paginatype;aanbeveling sleutel;logica;gegevenswaaier;gegevenswaaier;lookback venster;gedraggegevensbron;gedeeltelijk ontwerp;steun aanbevelingen;opnameregels;opnameregels;attribuut weging;huidige categorie;laatst gekocht punt;laatst bekeken punt;het meest bekeken punt;meest bekeken punt;favoriete categorie;populariteit;onlangs bekeken punt;laatst bekeken punt;laatst bekeken punt;laatst bekeken;meest bekeken;favoriet;onlangs bekeken
description: Leer hoe u criteria maakt die de inhoud van uw Adobe Recommendations-activiteiten bepalen om de aanbevelingen weer te geven die het meest geschikt zijn voor uw activiteiten.
title: Hoe maak ik criteria in Recommendations?
feature: Recommendations
exl-id: 3f4f59b2-6637-4c33-bf17-bff11bef7173
source-git-commit: cc260620cf87feebcd4c43f45f05406ac845cf5b
workflow-type: tm+mt
source-wordcount: '2644'
ht-degree: 0%

---

# ![PREMIUM](/help/assets/premium.png) Criteria maken

Criteria in [!UICONTROL Adobe Target] [!UICONTROL Recommendations] de inhoud van uw [!UICONTROL Recommendations] activiteiten. Maak criteria om de aanbevelingen weer te geven die het meest geschikt zijn voor uw activiteit. Deze criteria gebruiken de acties van de bezoeker om te bepalen welke inhoud of producten aan vertoning worden.

In de volgende secties wordt uitgelegd hoe u nieuwe criteria kunt maken.

## Het scherm Nieuwe criteria maken openen

Er zijn meerdere manieren om de [!UICONTROL Create New Criteria] scherm. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Op de **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm, klik **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations] activiteiten.
* Wanneer u een [!DNL Recommendations] activiteit met behulp van de [!UICONTROL Visual Experience Composer] (VEC), wordt u onmiddellijk naar de [!UICONTROL Select Criteria] het scherm nadat u een element op uw pagina selecteert en klikt [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], of [!UICONTROL Insert Recommendations After]. U kunt vervolgens een van de beschikbare criteria selecteren of op **[!UICONTROL Create Criteria]**. Als u nieuwe criteria maakt, kunt u de criteria opslaan zodat u deze samen met andere criteria kunt gebruiken [!DNL Recommendations] activiteiten. Zie voor meer informatie [Een Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Wanneer u een [!DNL Recommendations] activiteit, klik in [!UICONTROL Recommendations Location] op de pagina en selecteer **[!UICONTROL Change Criteria]**. Op de [!UICONTROL Select Criteria] scherm, klikken **[!UICONTROL Create Criteria]**. U hebt de optie om uw nieuwe criteria op te slaan voor gebruik met andere [!DNL Recommendations] activiteiten.

De volgende stappen veronderstellen u tot [!UICONTROL Create New Criteria] scherm met de eerste methode: de **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

   ![Nieuwe criteria maken](assets/CreateNewCriteria_full-new.png)

1. Configureer de informatie in de volgende secties.

## [!UICONTROL Basic Information] {#info}

1. Typ a **[!UICONTROL Criteria Name]**.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de criteria te beschrijven. U kunt bijvoorbeeld uw criteria &quot;Hoogste margeproducten&quot; noemen, maar u wilt niet dat die titel openbaar wordt weergegeven. Zie de volgende stap om de naar buiten gerichte titel in te stellen.

   ![Sectie Basisinformatie](assets/basic-information.png)

1. Typ een publiekelijk gericht **[!UICONTROL Display Title]** om op de pagina te worden weergegeven voor aanbevelingen die gebruikmaken van deze criteria.

   U kunt bijvoorbeeld &quot;Personen die dit hebben bekeken, hebben dit weergegeven&quot; of &quot;Gelijksoortige producten&quot; weergeven wanneer u deze criteria gebruikt om aanbevelingen weer te geven.

1. Typ een korte tekst **[!UICONTROL Description]** van de criteria.

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

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde criteria te categoriseren, die het gemakkelijker maken om criteria voor andere te hergebruiken [!DNL Recommendations] activiteiten.

## [!UICONTROL Recommendations Algorithm] {#rec-algo}

1. Selecteer een **[!UICONTROL Algorithm Type]** en **[!UICONTROL Algorithm]**:

   ![Aanbevolen Algoritmesectie](assets/recommended-algorithm.png)

   | Het type Algorithm | Wanneer gebruiken | Beschikbare algoritmen |
   | --- | --- | --- |
   | [!UICONTROL Cart-Based] | Aanbevelingen doen op basis van de inhoud van het winkelwagentje van de gebruiker. | <ul><li>Personen die ze bekeken, bekeken ze</li><li>Mensen die ze bekeken, kochten hen</li><li>Mensen die deze hebben gekocht, hebben de</li></ul>Zie voor meer informatie [Op basis van winkelwagentje](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *De aanbeveling baseren op een aanbevelingen*. |
   | [!UICONTROL Popularity-Based] | Aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker. | <ul><li>Meest bekeken op de site</li><li>Meest bekeken op rubriek</li><li>Meest bekeken door kenmerk Item</li><li>Topverkopers op de hele site</li><li>Topverkopers op rubriek</li><li>Topverkopers op objectkenmerk</li><li>Metrisch, boven op Analytics</li></ul> |
   | [!UICONTROL Item-Based] | Aanbevelingen doen op basis van het zoeken naar objecten die vergelijkbaar zijn met een item dat de gebruiker momenteel bekijkt of onlangs heeft bekeken. | <ul><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Mensen die dit bekeken hebben, hebben het volgende gekocht</li><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Objecten met vergelijkbare kenmerken</li></ul> |
   | [!UICONTROL User-Based] | Aanbevelingen doen op basis van het gedrag van de gebruiker. | <ul><li>Onlangs bekeken objecten</li><li>Aanbevolen voor u</li></ul> |

   |[!UICONTROL Custom Criteria]|Aanbevelingen doen op basis van een aangepast bestand dat u uploadt.|<ul><li>Aangepast algoritme</li></ul>|


   >[!NOTE]
   >
   >Als u **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]** kunt u instellen [regels voor gelijkenis met inhoud](#similarity).

1. Selecteer zo nodig een **Itemkenmerk** en **Profielkenmerk dat moet overeenkomen**, **Aanbevelingssleutel**, **Filtersleutel**, en/of **Metrisch** om het algoritme te vormen.

Voor meer informatie over het kiezen van een Sleutel van de Aanbeveling, zie [De aanbeveling baseren op een aanbevelingen](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## [!UICONTROL Data Source] {#data-source}

1. Selecteer het gewenste **[!UICONTROL Behavioral Data Source]**: [!UICONTROL Adobe Target] of [!UICONTROL Analytics].

   >[!NOTE]
   >
   >De [!UICONTROL Behavioral Data Source] de sectie toont slechts als uw implementatie gebruikt [Analyses voor doel](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).

   ![Sectie Gedragsgegevensbron](assets/data-source.png)

   Als u [!UICONTROL Analytics]selecteert u de gewenste rapportsuite.

   Indien de criteria worden gebruikt [!DNL Adobe Analytics] als gedragsgegevensbron, zodra gecreeerd, hangt de tijd voor criteria beschikbaarheid af van of de geselecteerde rapportreeks en het raadplegingsvenster voor een andere criteria, zoals hieronder verklaard is gebruikt:

   * **Installatie van een eenmalige rapportsuite**: De eerste keer wordt een rapportreeks gebruikt met een bepaald venster van de gegevenswaaierraadpleging, [!DNL Target Recommendations] kan twee tot zeven dagen duren om de gedragsgegevens voor de geselecteerde rapportsuite volledig te downloaden van [!DNL Analytics]. Dit tijdframe is afhankelijk van het [!DNL Analytics] systeembelasting.
   * **Nieuwe of bewerkte criteria met behulp van een reeds beschikbare rapportsuite**: Als de geselecteerde rapportsuite al is gebruikt bij het maken van nieuwe criteria of het bewerken van bestaande criteria [!DNL Target Recommendations]Met een gegevensbereik dat gelijk is aan of kleiner is dan het geselecteerde gegevensbereik, zijn de gegevens direct beschikbaar en is er geen eenmalige installatie vereist. In dit geval, of als de montages van een algoritme terwijl het wijzigen van de geselecteerde rapportreeks of gegevenswaaier worden uitgegeven, loopt het algoritme of herstelt binnen 12 uren.
   * **Doorlopende algoritmeuitvoering**: Gegevensstromen uit [!DNL Analytics] tot [!DNL Target Recommendations] dagelijks. Bijvoorbeeld voor [!UICONTROL Viewed Affinity] aanbeveling, wanneer een gebruiker een product bekijkt, wordt een product-mening het volgen vraag overgegaan in [!DNL Analytics] dicht bij real-time. De [!DNL Analytics] gegevens worden doorgegeven aan [!DNL Target] vroeg de volgende dag en [!DNL Target] voert het algoritme uit binnen minder dan 12 uur.

   Zie voor meer informatie [Adobe Analytics gebruiken met Target Recommendations](/help/c-recommendations/c-algorithms/use-adobe-analytics-with-recommendations.md).

1. Stel de **[!UICONTROL Lookback Window]** om de tijdwaaier van beschikbare historische gegevens van het gebruikersgedrag te bepalen om te gebruiken wanneer het bepalen welke aanbevelingen te tonen. Deze optie is beschikbaar voor alle algoritmes, met uitzondering van Items met vergelijkbare kenmerken en aangepaste algoritmen.

   ![Schuifregelaar voor Venster opzoeken](assets/data-range.png)

   Als uw site veel verkeer heeft en het gedrag vaak verandert, kiest u een korter gegevensvenster. Een korter venster schakelt [!DNL Recommendations] om beter op veranderingen in de markt en in uw zaken te reageren. Een korter venster betekent bijvoorbeeld dat [!DNL Recommendations] wijzigingen in het gedrag van bezoekers detecteren wanneer uw bezoekers seizoensgebonden winkelen beginnen, zoals &#39;back-to-school&#39;-winkelen of &#39;Kerstmis&#39;, en artikelen aanbevelen die geschikt zijn voor deze winkelseizoenen.

   Als u niet veel gegevens hebt of als het gedrag van de bezoeker niet vaak verandert, kunt u een langer venster selecteren. Voor veel sites leidt een korter venster echter tot aanbevelingen van hogere kwaliteit.

   De beschikbare gegevensbereiken zijn:

   | Venster opzoeken, optie | Bijgewerkte frequentie (weergegeven bij aanwijzen) | Ondersteunde algoritmen |
   | --- | --- | --- |
   | Zes uur | Algorithm wordt elke 3-6 uur uitgevoerd | [!UICONTROL Popularity-Based] algoritmen wanneer de geselecteerde [!UICONTROL Behavioral Data Source] is [!DNL Adobe Target] |
   | Eén dag | Algorithm wordt elke 12-24 uur uitgevoerd | [!UICONTROL Popularity-Based] algoritmen |
   | Twee dagen | Algorithm wordt elke 12-24 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Eén week | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Twee weken | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>Alles [!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Eén maand (30 dagen) | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |
   | Twee maanden (61 dagen) | Algorithm wordt elke 24-48 uur uitgevoerd | <ul><li>[!UICONTROL Popularity-Based] algoritmen</li><li>[!UICONTROL Item-Based] algoritmen</li><li>[!UICONTROL User-Based] algoritmen</li><li>[!UICONTROL Cart-Based] algoritmen</li></ul> |

## [!UICONTROL Backup Content] {#content}

[!UICONTROL Backup Content] regels bepalen wat er gebeurt als het aantal aanbevolen items de [ontwerp van aanbevelingen](/help/c-recommendations/c-design-overview/design-overview.md). Het is mogelijk [!DNL Recommendations] criteria om minder aanbevelingen terug te keren dan uw ontwerp vraagt. Als uw ontwerp bijvoorbeeld sleuven voor vier items bevat, maar uw criteria slechts twee items aanbevolen laten, kunt u de resterende sleuven leeg laten, back-upaanbevelingen gebruiken om de extra sleuven te vullen, of u kunt ervoor kiezen geen aanbevelingen weer te geven.

![Sectie Inhoud](assets/content.png)

1. (Optioneel) Schuif de schuifregelaar **[!UICONTROL Partial Design Rendering]** schakelen naar de positie &quot;aan&quot;.

   Er worden zoveel mogelijk sleuven ingevuld, maar in de ontwerpsjabloon kan lege ruimte voor de resterende sleuven zijn opgenomen. Als deze optie is uitgeschakeld en er onvoldoende inhoud is om alle beschikbare sleuven te vullen, worden geen aanbevelingen gedaan en wordt in plaats daarvan standaardinhoud weergegeven.

   Schakel deze optie in als u wilt dat aanbevelingen worden gedaan met lege sleuven. Gebruik back-upaanbevelingen als u wilt dat de aanbevolen sleuven worden gevuld met inhoud op basis van uw criteria met lege sleuven die zijn gevuld met vergelijkbare of populaire inhoud van uw site, zoals in de volgende stap wordt uitgelegd.

1. (Optioneel) Schuif de schuifregelaar **[!UICONTROL Show Backup Content]** schakelen naar de positie &quot;aan&quot;.

   Vul eventueel resterende lege sleuven in het ontwerp met een willekeurige selectie van de meest bekeken producten van de hele site.

   Het gebruik van aanbevelingen voor back-ups zorgt ervoor dat het ontwerp van uw aanbeveling alle beschikbare sleuven vult. Stel dat u een ontwerp van 4 x 1 hebt, zoals hieronder wordt geïllustreerd:

   ![4 x 1 ontwerp](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Op basis van uw criteria worden slechts twee objecten aanbevolen. Als u de optie [!UICONTROL Partial Design Rendering] de eerste twee sleuven zijn ingevuld , maar de resterende twee sleuven blijven leeg . Als u echter de optie [!UICONTROL Show Backup Recommendations] de eerste twee sleuven worden gevuld op basis van de opgegeven criteria en de resterende twee sleuven worden ingevuld op basis van uw aanbevelingen voor back-up.

   De volgende matrix toont het resultaat dat u zult waarnemen bij het gebruik van de [!UICONTROL Partial Design Rendering] en [!UICONTROL Backup Content] opties:

   | Gedeeltelijke rendering van ontwerp | Back-upinhoud | Resultaat |
   |--- |--- |--- |
   | Uitgeschakeld | Uitgeschakeld | Als er minder aanbevelingen worden geretourneerd dan door het ontwerp wordt gevraagd, wordt het ontwerp van de aanbevelingen vervangen door de standaardinhoud en worden er geen aanbevelingen weergegeven. |
   | Ingeschakeld | Uitgeschakeld | Het ontwerp wordt teruggegeven, maar kan lege ruimte omvatten als minder aanbevelingen zijn teruggekeerd dan het ontwerp verzoekt. |
   | Ingeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in.<br>Als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp gedeeltelijk teruggegeven.<br>Als de criteria geen aanbevelingen terugkeren, en de integratieregels reserveaanbevelingen tot nul beperken, wordt het ontwerp vervangen met standaardinhoud. |
   | Uitgeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in.<br>Als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp vervangen door standaardinhoud en geen aanbevelingen worden getoond. |

   Zie voor meer informatie [Een back-upaanbeveling gebruiken](/help/c-recommendations/c-algorithms/backup-recs.md).

1. (Voorwaardelijk) Als u **[!UICONTROL Show Backup Content]** in de vorige stap kunt u **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   In de insluitingsregels wordt bepaald welke items in uw aanbevelingen worden opgenomen. Welke opties beschikbaar zijn, is afhankelijk van de verticale situatie in uw branche.

   Zie voor meer informatie [Opnameregels opgeven](#inclusion) hieronder.

1. (Optioneel) Schuif de schuifregelaar **[!UICONTROL Recommend Previously Purchased Items]** schakelen naar de positie &quot;aan&quot;.

   Deze instelling is gebaseerd op de `productPurchasedId`. Standaard wordt eerder aangeschafte items niet aanbevolen. In de meeste gevallen wilt u geen objecten promoten die een klant onlangs heeft aangeschaft. Het is handig om objecten te verkopen die mensen doorgaans slechts eenmaal kopen, zoals kajaks. Als je objecten verkoopt die mensen herhaaldelijk kunnen kopen, zoals shampoo of andere persoonlijke objecten, moet je deze optie inschakelen.

## Vergelijkbare inhoud {#similarity}

Gebruiken [!UICONTROL Content Similarity] regels om aanbevelingen te doen die op punt of media attributen worden gebaseerd.

>[!NOTE]
>
>Als u **[!UICONTROL Item-Based]**/ **[!UICONTROL Media with Similar Attributes]** als uw Type Algorithm en Algorithm, kunt u de regels voor de gelijkenis van de inhoud instellen.

De gelijkenis van de inhoud vergelijkt de sleutelwoorden van puntattributen en doet aanbevelingen die op hoeveel sleutelwoorden verschillende punten in gemeenschappelijk hebben worden gebaseerd. Recommendations op basis van gelijkenis met inhoud vereist geen gegevens uit het verleden om sterke resultaten te bereiken.

Het gebruiken van inhoudgelijkenis om aanbevelingen te produceren is vooral effectief voor nieuwe punten, die niet waarschijnlijk in aanbevelingen zullen tonen gebruikend *Personen die dit hebben bekeken, zagen het volgende* en andere logica gebaseerd op gedrag uit het verleden. U kunt de gelijkenis van de inhoud ook gebruiken om nuttige aanbevelingen voor nieuwe bezoekers te produceren, die geen vroegere aankopen of andere historische gegevens hebben.

Wanneer u **[!UICONTROL Item-Based]**/ **[!UICONTROL Media with Similar Attributes]**, hebt u de optie om regels tot stand te brengen om het belang van specifieke puntattributen in het bepalen van aanbevelingen te verhogen of te verminderen. Voor objecten zoals boeken kunt u het belang van kenmerken zoals *genre*, *auteur*, *serie*, enzovoort, om soortgelijke boeken aan te bevelen.

![](assets/ContentSimilarity.png)

Omdat bij gelijkenis met inhoud trefwoorden worden gebruikt om items te vergelijken, kunnen sommige kenmerken, zoals *message* of *beschrijving*, kan &quot;lawaai&quot;in de vergelijking introduceren. U kunt regels maken om deze kenmerken te negeren.

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

Zie voor meer informatie [Regels voor dynamische en statische integratie gebruiken](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md).

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

Als u klaar bent, klikt u op **[!UICONTROL Save]**.

Als u een nieuwe [!UICONTROL Recommendations] activiteit of het uitgeven van bestaande, **[!UICONTROL Save criteria for later]** selectievakje is standaard ingeschakeld. Als u de criteria niet wilt gebruiken in andere activiteiten, schakelt u het selectievakje uit voordat u het bestand opslaat.

## Trainingsvideo: Criteria maken in Recommendations (12:33) ![Zelfstudie-badge](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
