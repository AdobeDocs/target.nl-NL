---
keywords: automated personalization;Audiences;ensemble;random forest;residual variance;error variance;lifetime value
description: De Automated Personalization-activiteitenworkflow verschilt van de workflow van de andere typen activiteiten.
title: Een Automated Personalization-activiteit maken
feature: null
topic: Advanced
uuid: 7d301dc3-6076-4e05-8abc-4978075a881e
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Een Automated Personalization-activiteit maken{#create-an-automated-personalization-activity}

De Automated Personalization-activiteitenworkflow verschilt van de workflow van de andere typen activiteiten.

1. Klik in de lijst Standaardactiviteiten doel op **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

   ![Activiteit maken: Automated Personalization](/help/c-activities/t-automated-personalization/assets/ap_create-new.png)

1. Om Visual Experience Composer (VEC) te gebruiken, klik **[!UICONTROL Visual (Default)]**.

   ![Automated Personalization-activiteit maken, dialoogvenster](/help/c-activities/t-automated-personalization/assets/ap_url-new.png)

   Selecteer [!UICONTROL Form]Formulier-based Experience Composer als u liever wilt gebruiken. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Zie [Ervaringen en Aanbiedingen](/help/c-experiences/experiences.md)voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.
   >
   >De [!UICONTROL Choose Workplace] optie in de voorgaande illustratie is een [doelpremiumfunctie](/help/c-intro/intro.md) . Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.]

1. (Voorwaardelijk) Als u een klant van de Premium van het Doel bent, [kies een werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verifieer of ga de activiteit URL in, dan klik **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide overeen.

   De pagina met gespecificeerde URL opent in de Visuele Composer van de Ervaring.

1. Als u de activiteit een naam wilt geven, klikt u op het veld Naam en typt u de naam van de activiteit.

   ![Naamveld](/help/c-activities/t-automated-personalization/assets/ab_newname-new.png)

   De volgende tekens zijn niet toegestaan in een naam van een activiteit:

   | Teken | Beschrijving |
   |--- |--- |
   | / | slash |
   | ? | Vraagteken |
   | # | Nummerteken |
   | : | Colon |
   | = | Gelijk aan |
   | + | Plus |
   | - | Min |
   | @ | Bij ondertekenen |

1. Wijzig pagina-elementen zoals wordt uitgelegd in de opties [](/help/c-experiences/c-visual-experience-composer/viztarget-options.md)Visual Experience Composer.

   U kunt meerdere afbeeldingen tegelijk selecteren in het middelenbeheer. Hierdoor kunt u snel de pagina weergeven met elk van de afbeeldingen die voor de activiteit zijn geconfigureerd. U kunt ook gemakkelijk tekstelementen in uw aanbiedingen bewerken. Wanneer u een element bewerkt, verschijnen er balken op dat element om aan te geven dat u het element hebt gewijzigd.

1. Klik **[!UICONTROL Manage Content]** om de beschikbare combinaties te vormen.

   ![Inhoud beheren, optie](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Er verschijnt een dialoogvenster met drie opties boven aan het scherm: Ervaringen, aanbiedingen en uitsluitingsgroepen.

   ![Inhoud beheren, dialoogvenster](/help/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Hoewel u tot 30.000 ervaringen in een AP activiteit kunt tot stand brengen, presteert de activiteit het best wanneer minder dan 5.000 ervaringen worden gebruikt.

   In de [!UICONTROL Experiences] lijst wordt elk stuk inhoud weergegeven dat is geselecteerd voor de activiteit en de locatie die eraan is toegewezen.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![Pictogramaanwijs uitsluiten](/help/c-activities/t-automated-personalization/assets/icon-exclude.png)

   U kunt ervaringen in batch uitsluiten of opnemen door het selectievakje voor relevante ervaringen in te schakelen en vervolgens op het pictogram Uitsluiten in de rechterbovenhoek van het dialoogvenster te klikken.

   ![Opties voor uitsluiten in batch](/help/c-activities/t-automated-personalization/assets/batch-exclude.png)

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de vervolgkeuzelijst **Status** te klikken.

1. (Voorwaardelijk) Klik **[!UICONTROL Offers]** om stukken inhoud te selecteren en deze toe te wijzen aan rapportagegroepen of om alleen bepaalde bezoekers toe te staan bepaalde aanbiedingen te zien waarvoor ze zich richten.

   Zie [Rapportgroepen aanbieden in Automated Personalization](../../c-reports/offer-reporting-groups-in-automated-personalization.md#concept_194128C0B56B4B26AAB57DB49892960C)voor meer informatie.

   Gebruik de [!UICONTROL Location] lijst om aanbiedingen op locatie te filteren. Gebruik de [!UICONTROL Report Group] lijst aan filteraanbiedingen door rapportgroepen. U kunt de [!UICONTROL Report Group] lijst ook gebruiken om voor te filtreren [!UICONTROL Unassigned Offers] zodat kunt u een rapporteringsgroep aan een aanbieding toewijzen die momenteel niet aan om het even welke rapportgroep wordt toegewezen.

   U kunt specifieke ervaringen toevoegen aan een rapportgroep door de muis boven de gewenste aanbieding te houden en vervolgens op het mappictogram te klikken.

   ![Mappictogram aanwijzen](/help/c-activities/t-automated-personalization/assets/icon-folder.png)

   U kunt ervaringen in een rapportgroep in batch opnemen door checkbox voor de relevante ervaringen te selecteren en dan de de omslagknoop van de Groep van de Rapportering in de hoogste juiste hoek van de dialoogdoos te klikken.

   ![Opties voor rapportgroep](/help/c-activities/t-automated-personalization/assets/report-group-options.png)

   Het is belangrijk te begrijpen dat rapportagegroepen van invloed zijn op de manier waarop Target zijn modellen bouwt. Dientengevolge, adviseren wij dat u rapportgroepen slechts gebruikt als u van plan bent om nieuwe aanbiedingen te vervangen of toe te voegen terwijl de activiteit levend is. Als een nieuwe aanbieding wordt geïntroduceerd in een live-activiteit, kan de machine de gegevens die reeds voor de andere aanbiedingen in haar groep zijn verzameld, gebruiken om meer te weten te komen over de nieuwe aanbieding. Je mag niet alle voorstellen in één rapportagegroep plaatsen.

   Voor informatie over het richten van een aanbieding aan specifiek publiek, zie AP van het [Doel Aanbiedingen](../../c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

1. (Voorwaardelijk) Klik **[!UICONTROL Exclusion Groups]** om combinaties van elementen te kiezen die u van de activiteit wilt uitsluiten.

   ![Het tabblad Uitsluitingsgroepen van het dialoogvenster Inhoud beheren](/help/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Hoewel u tot 30.000 ervaringen in een AP test kunt tot stand brengen, voert het algoritme zijn beste uit wanneer minder dan 10.000 verschillende ervaringen worden gebruikt.

   Als er momenteel geen uitsluitingsgroepen zijn opgenomen in uw activiteit, klikt u op **Uitsluitingsgroep** maken. U kunt filteren om een lijst te creëren die slechts de combinaties toont u wilt uitsluiten. Geef een naam op voor de uitsluitingsgroep en klik op **Opslaan**.

   Als u een bestaande uitsluitingsgroep wilt bewerken, plaatst u de aanwijzer boven de groep die u wilt bewerken en klikt u op het potloodpictogram.

1. Klik **[!UICONTROL Done]** wanneer u klaar bent met het instellen van de inhoud van uw activiteit.

1. De **het richten** stap zal vertrouwd kijken als u andere types van de activiteit van het Doel hebt gebruikt. Hier kunt u een publiek selecteren en het percentage bezoekers specificeren die de controleervaring zullen zien door de **[!UICONTROL Custom Allocation]** drop-down lijst te klikken, dan **daarna** te klikken.

   In de [!UICONTROL Custom Allocation] vervolgkeuzelijst kunt u de volgende opties kiezen:

   ![Verkeerstoewijzingsdoel, vervolgkeuzelijst](/help/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **Evalueer het Algoritme van de Personalisatie (50/50):** Als uw doel het algoritme is te testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle.
   * **Maximaliserend Verkeer van de Personalisering (90/10):** Als uw doel het creëren van &quot;altijd op&quot;activiteit is, zet 10% van de bezoekers in de controle om ervoor te zorgen dat er genoeg gegevens voor de algoritmen zijn om in tijd te blijven leren. Merk op de handel hier is dat in ruil voor het personaliseren van een groter deel van uw verkeer, u minder precisie in wat de nauwkeurige lift is zult hebben. Wat u ook wilt, dit is de aanbevolen verkeerssplitsing wanneer u een specifieke ervaring als besturingselement gebruikt.
   * **Met Aangepaste toewijzing** wordt het percentage handmatig gesplitst.

1. (Voorwaardelijk) Van de [!UICONTROL Control] drop-down lijst, [selecteer een specifieke ervaring die als controle](/help/c-activities/t-automated-personalization/experience-as-control.md) moet worden gebruikt of selecteer [!UICONTROL Random Experience.]

   De ervaring met het bedieningsorgaan levert een vergelijking op om te bepalen hoeveel lift door de geautomatiseerde test wordt geleverd.

   Automated Personalization meet prestaties altijd ten opzichte van een controlegroep. De beste manier is om ten minste 10% van de deelnemers aan de controlegroep te plaatsen. Als uw doel is te testen als het verpersoonlijkingsalgoritme op de gegevens het wordt gegeven beter dan geen verpersoonlijking (d.w.z. de willekeurig gediende controle) presteert, dan zou een 50/50 percenten die percenten tussen de controle en het verpersoonlijkingsalgoritme de snelste en meest nauwkeurige manier zijn om dit doel te bereiken. Als u de hoeveelheid verkeer wilt maximaliseren dat gepersonaliseerd is en u minder met het begrijpen van de nauwkeurige lift uw activiteit produceert, dan zou een 10/90 percenten verkeer die tussen de controle en het verpersoonlijkingsalgoritme wordt verdeeld de snelste en meest nauwkeurige manier zijn om dit doel te bereiken.

   >[!NOTE]
   >
   >In Automated Personalization-activiteiten worden entry-criteria (URL-adressering, sjabloonregels en doelgroep) geëvalueerd voor elke aanvraag. In vorige versies werden de entry criteria één keer per sessie geëvalueerd.

1. Klik **[!UICONTROL Next]** om de **[!UICONTROL Goals & Settings]** pagina weer te geven.
1. Vorm de activiteit met de volgende montages, dan klik **[!UICONTROL Save & Close]**.

   | Instelling | Beschrijving |
   |--- |--- |
   | Naam | Geef de activiteit een naam. Geef de activiteit een naam die beschrijvend genoeg is dat de teamleden het in de lijst van Activiteiten kunnen erkennen.  Raadpleeg de bovenstaande tabel om te zien welke tekens niet zijn toegestaan in een naam van een activiteit. |
   | Doelstelling | (Optioneel) Typ het doel van de test. Het doel helpt u het doel van de activiteit te herinneren. |
   | Prioriteit | Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.<br>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<br>Als deze optie niet is ingeschakeld in [!UICONTROL Administration] > [!UICONTROL Reporting] (de standaardinstelling), geeft u een prioriteit op: Laag, Normaal of Hoog.<br>Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op [!UICONTROL Administration] > [!UICONTROL Reporting]en schakelt u de [!UICONTROL Enable Fine-Grained Priorities] optie in op de positie &quot;Aan&quot;.<br>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:<ul><li>0 = Laag</li><li>999 = Hoog</li></ul>Voor activiteiten die zijn gemaakt in eerdere versies van Target Standard/Premium wordt Lage prioriteit omgezet in 0, Normaal in 5 en Hoog in 10. U kunt deze waarden desgewenst aanpassen.<br>**Opmerking **: Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld. |
   | Duur | Stel de begin- en einddatum voor de activiteit in. |
   | Optimalisatiedoelstelling | Geef het optimalisatiedoel op, dat uit twee parameters bestaat:<ul><li>Wat u met de activiteit wilt meten</li><li>De actie van een deelnemer aan een activiteit die aantoont dat het doel is bereikt.</li></ul>U kunt het optimalisatiedoel een naam geven door de drie stippen rechts van Mijn primaire doel te selecteren. Automated Personalization-activiteiten kunnen conversie, RPV en AOV meten. Conversie is mogelijk door een pagina weer te geven of een box weer te geven. Klik kan ook worden gevolgd.<br>Het primaire doel wordt ook de modelleringsmetrische methode, die door het modelleringssysteem wordt gebruikt om het succes van de ervaring te berekenen.<br>Bezoekers kunnen in de activiteit blijven voor traceringsdoeleinden nadat ze het modelleringsdoel hebben bereikt. Bijvoorbeeld, vaak wordt een activiteit van Automated Personalization gebruikt om kliktarieven te verbeteren, en dat wordt geplaatst als modelleringsdoel. Nochtans, is het belangrijk om te zien hoe de verhoogde klikkoersen tot definitieve omzetting leiden, zodat is het volgen door de definitieve omzetting essentieel.<br>U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.<br>U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.<br>Met de optie Afhankelijkheid toevoegen kan metrisch met succes worden verhoogd als een andere succesmetrische waarde is bereikt of niet is bereikt.<br>Een afhankelijkheid toevoegen:<ol><li>Nadat u aanvullende metriek hebt toegevoegd, klikt u [!UICONTROL Advanced Settings] onder het menu met drie punten rechts van Extra doel.</li><li>Klik op de [!UICONTROL Add Dependency] optie onder aan de [!UICONTROL Reporting Settings] sectie.</li><li>Sleep de gewenste metriek van het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens [!UICONTROL Reached] om de instelling tussen [!UICONTROL Reached] en [!UICONTROL Not Reached]</li></ol>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd. |
   | Omzettingsmetrisch | Standaard is de metrische conversie hetzelfde als de metrische optimalisatiedoelstelling. U kunt echter wel een aparte omzettingsmaatstaf definiëren door de [!UICONTROL Same as Optimization Goal] optie uit te schakelen. |
   | Aanvullende cijfers | Voeg aanvullende rapportgegevens toe die u wilt gebruiken. U kunt conversie- of inkomstenmetriek toevoegen.<br>**Opmerking **: Metrisch van de Betrokkenheid wordt niet ook gesteund als extra metrisch. In de UI kunt u de metrische betrokkenheid selecteren, maar de gegevens worden niet correct weergegeven in rapporten. |
   | Soorten publiek voor rapportage | Voeg publiek toe om het filtreren door publiek in rapporten toe te laten. Standaard toont het rapport resultaten voor alle gekwalificeerde bezoekers. Voeg publiek toe aan filterresultaten voor specifiekere subsets van bezoekers.<br>**Opmerking **: In tegenstelling tot andere soorten activiteiten kan Automated Personalization Adobe Analytics niet als rapportagebron gebruiken. |
   | Notities | Typ alle informatie over uw activiteiten die u voor uzelf of andere teamleden kunt gebruiken. Het deelvenster Notities kan opnieuw worden geschaald. |

   Wanneer u metrische gegevens een naam geeft of de naam ervan wijzigt, zijn de volgende tekens niet toegestaan:

   | Teken | Beschrijving |
   |--- |--- |
   | / | slash |
   | ? | Vraagteken |
   | # | Nummerteken |
   | : | Colon |
   | = | Gelijk aan |
   | + | Plus |
   | - | Min |
   | @ | Bij ondertekenen |

Nadat u hebt geklikt, wordt het Activiteitenoverzicht weergegeven. **[!UICONTROL Create]** Klik op Ervaringen **** voorvertonen om een voorvertoning weer te geven van hoe uw ervaringen eruit zullen zien wanneer ze worden geleverd. Er wordt een pop-up weergegeven die u kunt gebruiken om koppelingen naar uw AP-ervaringen op uw site weer te geven en te delen voor een &quot;echte voorvertoning&quot; van de ervaringen buiten de Visual Experience Composer van Target. U moet de koppelingen vanuit het bericht delen om de voorvertoning te kunnen delen. Wanneer u op een koppeling klikt en vervolgens de URL rechtstreeks vanaf de pagina kopieert, werkt de URL niet omdat de URL een parameter bevat die de pagina alleen correct weergeeft wanneer u de pagina opent via de koppeling in het bericht.

Zie Rapporten [van](../../c-reports/reports-ap.md#concept_C02BAFC922114A44846998FD956E345A)Automated Personalization voor informatie over rapporten.
