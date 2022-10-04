---
keywords: geautomatiseerde personalisatie;ap;publiek;ensemble;random forest;restvariantie;foutvariantie;levenswaarde
description: Leer hoe u een [!UICONTROL Automated Personalization] (AP) activiteit in [!DNL Adobe Target] het gebruiken van Visual Experience Composer.
title: Hoe maak ik een [!UICONTROL Automated Personalization] Activiteit?
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: d90e541588f51e16dd9b11ead1ece77e9ca1408b
workflow-type: tm+mt
source-wordcount: '1967'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Een [!UICONTROL Automated Personalization] activiteit

De [!UICONTROL Automated Personalization] (AP) werkstroom in [!DNL Adobe Target] varieert van het werkschema van de andere activiteitentypes.

1. Van de [!DNL Target] [!UICONTROL Activities] lijst, klikt u op **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

   ![Activiteit maken: Automated Personalization](/help/main/c-activities/t-automated-personalization/assets/ap_create-new.png)

1. Als u de opdracht [!UICONTROL Visual Experience Composer] (VEC) klikt u op **[!UICONTROL Visual (Default)]**.

   ![Automated Personalization-activiteit maken, dialoogvenster](/help/main/c-activities/t-automated-personalization/assets/ap_url-new.png)

   Als u liever het [!UICONTROL Form-Based Experience Composer], selecteert u [!UICONTROL Form]. Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor meer informatie .

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer], [!DNL Target] biedt de [!UICONTROL Single Page Application VEC] en de VEC voor mobiele apps. Voor meer informatie over de verschillende composers raadpleegt u [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Het oplossen van problemen de Visuele Composer van de Ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >De [!UICONTROL Choose Workplace] optie in de voorgaande illustratie is een [Doelpremie](/help/main/c-intro/intro.md) gebruiken. Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een [!DNL Target] Premium-klant, [een werkruimte kiezen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verifieer of ga de activiteit URL in, dan klik **[!UICONTROL Next]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ( [!DNL https] en [!DNL http]). Dientengevolge [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide komen overeen.

   De pagina met gespecificeerde URL opent in de Visuele Composer van de Ervaring.

1. Als u de activiteit een naam wilt geven, klikt u op de knop **[!UICONTROL Name]** en typ de naam van uw activiteit.

   ![Naamveld](/help/main/c-activities/t-automated-personalization/assets/ab_newname-new.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Pagina-elementen wijzigen zoals wordt uitgelegd in [Opties voor Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   U kunt meerdere afbeeldingen tegelijk selecteren in het middelenbeheer. Hierdoor kunt u snel de pagina weergeven met elk van de afbeeldingen die voor de activiteit zijn geconfigureerd. U kunt ook gemakkelijk tekstelementen in uw aanbiedingen bewerken. Wanneer u een element bewerkt, verschijnen er balken op dat element om aan te geven dat u het element hebt gewijzigd.

1. Klikken **[!UICONTROL Manage Content]** om de beschikbare combinaties te vormen.

   ![Inhoud beheren, optie](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Er verschijnt een dialoogvenster met drie opties boven aan het scherm: Ervaringen, aanbiedingen en uitsluitingsgroepen.

   ![Inhoud beheren, dialoogvenster](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Hoewel u tot 30.000 ervaringen in een AP activiteit kunt tot stand brengen, presteert de activiteit het best wanneer minder dan 5.000 ervaringen worden gebruikt.

   De [!UICONTROL Experiences] in de lijst worden alle inhoud weergegeven die is geselecteerd voor de activiteit en de locatie waaraan deze is toegewezen.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![Pictogramaanwijs uitsluiten](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   U kunt ervaringen in batch uitsluiten of opnemen door het selectievakje voor relevante ervaringen in te schakelen en vervolgens op het pictogram Uitsluiten in de rechterbovenhoek van het dialoogvenster te klikken.

   ![Opties voor uitsluiten in batch](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de knop **Status** vervolgkeuzelijst.

1. (Voorwaardelijk) Klik **[!UICONTROL Offers]** om stukken inhoud te selecteren en deze aan rapportagegroepen toe te wijzen, of alleen bepaalde bezoekers bepaalde aanbiedingen te laten zien waarvoor ze zich richten.

   Zie voor meer informatie [Rapportagegroepen aanbieden in Automated Personalization](/help/main/c-reports/personalization-reports/offer-reporting-groups-in-automated-personalization.md).

   Gebruik de [!UICONTROL Location] lijst om aanbiedingen te filteren op locatie. Gebruik de [!UICONTROL Report Group] lijst aan filteraanbiedingen door rapporterende groepen. U kunt ook de opdracht [!UICONTROL Report Group] lijst die moet worden gefilterd voor [!UICONTROL Unassigned Offers] zodat kunt u een rapportgroep aan een aanbieding toewijzen die momenteel niet aan om het even welke rapporteringsgroep wordt toegewezen.

   U kunt specifieke ervaringen toevoegen aan een rapportgroep door de muis boven de gewenste aanbieding te houden en vervolgens op het mappictogram te klikken.

   ![Mappictogram aanwijzen](/help/main/c-activities/t-automated-personalization/assets/icon-folder.png)

   U kunt ervaringen in een rapportgroep in batch opnemen door checkbox voor de relevante ervaringen te selecteren en dan de de omslagknoop van de Groep van de Rapportering in de hoogste juiste hoek van de dialoogdoos te klikken.

   ![Opties voor rapportgroep](/help/main/c-activities/t-automated-personalization/assets/report-group-options.png)

   Het is belangrijk te begrijpen dat rapportagegroepen van invloed zijn op de manier waarop Target zijn modellen bouwt. Dientengevolge, adviseren wij dat u rapportgroepen slechts gebruikt als u van plan bent om nieuwe aanbiedingen te vervangen of toe te voegen terwijl de activiteit levend is. Als een nieuwe aanbieding wordt geïntroduceerd in een live-activiteit, kan de machine de gegevens die reeds voor de andere aanbiedingen in haar groep zijn verzameld, gebruiken om meer te weten te komen over de nieuwe aanbieding. Je mag niet alle voorstellen in één rapportagegroep plaatsen.

   Voor informatie over het richten van een aanbieding aan specifiek publiek, zie [AP-doelaanbiedingen](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

1. (Voorwaardelijk) Klik **[!UICONTROL Exclusion Groups]** om combinaties van elementen te kiezen die u van de activiteit wilt uitsluiten.

   ![Het tabblad Uitsluitingsgroepen van het dialoogvenster Inhoud beheren](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Hoewel u tot 30.000 ervaringen in een AP test kunt tot stand brengen, voert het algoritme zijn beste uit wanneer minder dan 10.000 verschillende ervaringen worden gebruikt.

   Als er momenteel geen uitsluitingsgroepen in uw activiteit zijn opgenomen, klikt u op **Uitsluitingsgroep maken**. U kunt filteren om een lijst te creëren die slechts de combinaties toont u wilt uitsluiten. Geef uw uitsluitingsgroep een naam en klik op **Opslaan**.

   Als u een bestaande uitsluitingsgroep wilt bewerken, plaatst u de aanwijzer boven de groep die u wilt bewerken en klikt u op het potloodpictogram.

1. Klikken **[!UICONTROL Done]** als u klaar bent met het instellen van de inhoud van uw activiteit.

1. De **Doelstelling** De stap zal vertrouwd kijken als u andere types van activiteit van het Doel hebt gebruikt. Hier kunt u een publiek selecteren en het percentage bezoekers opgeven dat de besturingservaring zal zien door op de knop **[!UICONTROL Custom Allocation]** vervolgkeuzelijst en vervolgens op **Volgende**.

   De [!UICONTROL Custom Allocation] In de vervolgkeuzelijst kunt u de volgende opties kiezen:

   ![Verkeerstoewijzingsdoel, vervolgkeuzelijst](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **Evalueer het Algoritme van de Personalisatie (50/50):** Als uw doel het algoritme is te testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle.
   * **Maximaliserend Verkeer van de Personalisering (90/10):** Als uw doel het creëren van &quot;altijd op&quot;activiteit is, zet 10% van de bezoekers in de controle om ervoor te zorgen dat er genoeg gegevens voor de algoritmen zijn om in tijd te blijven leren. Merk op de handel hier is dat in ruil voor het personaliseren van een groter deel van uw verkeer, u minder precisie in wat de nauwkeurige lift is zult hebben. Wat u ook wilt, dit is de aanbevolen verkeerssplitsing wanneer u een specifieke ervaring als besturingselement gebruikt.
   * **Aangepaste toewijzing** Splits het percentage handmatig naar wens.

1. (Voorwaardelijk) Van de [!UICONTROL Control] vervolgkeuzelijst, [een specifieke ervaring selecteren die als controle moet worden gebruikt](/help/main/c-activities/t-automated-personalization/experience-as-control.md) of selecteer [!UICONTROL Random Experience.]

   De ervaring met het bedieningsorgaan levert een vergelijking op om te bepalen hoeveel lift door de geautomatiseerde test wordt geleverd.

   Automated Personalization meet prestaties altijd ten opzichte van een controlegroep. De beste manier is om ten minste 10% van de deelnemers aan de controlegroep te plaatsen. Als uw doel is te testen als het verpersoonlijkingsalgoritme op de gegevens het wordt gegeven beter dan geen verpersoonlijking (d.w.z. de willekeurig gediende controle) presteert, dan zou een 50/50 percenten die percenten tussen de controle en het verpersoonlijkingsalgoritme de snelste en meest nauwkeurige manier zijn om dit doel te bereiken. Als u de hoeveelheid verkeer wilt maximaliseren dat gepersonaliseerd is en u minder met het begrijpen van de nauwkeurige lift uw activiteit produceert, dan zou een 10/90 percenten verkeer die tussen de controle en het verpersoonlijkingsalgoritme wordt verdeeld de snelste en meest nauwkeurige manier zijn om dit doel te bereiken.

   >[!NOTE]
   >
   >In Automated Personalization-activiteiten worden entry-criteria (URL-adressering, sjabloonregels en doelgroep) geëvalueerd voor elke aanvraag. In vorige versies werden de entry criteria één keer per sessie geëvalueerd.

1. Klikken **[!UICONTROL Next]** om de **[!UICONTROL Goals & Settings]** pagina.
1. Configureer de activiteit met de volgende instellingen en klik vervolgens op **[!UICONTROL Save & Close]**.

   | Instelling | Beschrijving |
   |--- |--- |
   | Naam | Geef de activiteit een naam. Geef de activiteit een naam die beschrijvend genoeg is dat de teamleden het in de lijst van Activiteiten kunnen erkennen.  Raadpleeg de bovenstaande tabel om te zien welke tekens niet zijn toegestaan in een naam van een activiteit. |
   | Doelstelling | (Optioneel) Typ het doel van de test. Het doel helpt u het doel van de activiteit te herinneren. |
   | Prioriteit | Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.<br>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<br>Als deze optie niet is ingeschakeld in [!UICONTROL Administration] > [!UICONTROL Reporting] (standaard) geeft u een prioriteit op: Laag, Normaal of Hoog.<br>Klik op [!UICONTROL Administration] > [!UICONTROL Reporting]en schakelt u vervolgens de [!UICONTROL Enable Fine-Grained Priorities] aan de positie &quot;Aan&quot;.<br>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:<ul><li>0 = Laag</li><li>999 = Hoog</li></ul>Voor activiteiten die zijn gemaakt in eerdere versies van Target Standard/Premium wordt Lage prioriteit omgezet in 0, Normaal in 5 en Hoog in 10. U kunt deze waarden desgewenst aanpassen.<br>**Opmerking**: Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld. |
   | Duur | Stel de begin- en einddatum voor de activiteit in. |
   | Optimalisatiedoelstelling | Geef het optimalisatiedoel op, dat uit twee parameters bestaat:<ul><li>Wat u met de activiteit wilt meten</li><li>De actie van een deelnemer aan een activiteit die aantoont dat het doel is bereikt.</li></ul>U kunt het optimalisatiedoel een naam geven door de drie stippen rechts van Mijn primaire doel te selecteren. Automated Personalization-activiteiten kunnen conversie, RPV en AOV meten. Conversie is mogelijk door een pagina weer te geven of een box weer te geven. Klik kan ook worden gevolgd.<br>Het primaire doel wordt ook de modelleringsmetrische methode, die door het modelleringssysteem wordt gebruikt om het succes van de ervaring te berekenen.<br>Bezoekers kunnen in de activiteit blijven voor traceringsdoeleinden nadat ze het modelleringsdoel hebben bereikt. Bijvoorbeeld, vaak wordt een activiteit van Automated Personalization gebruikt om kliktarieven te verbeteren, en dat wordt geplaatst als modelleringsdoel. Nochtans, is het belangrijk om te zien hoe de verhoogde klikkoersen tot definitieve omzetting leiden, zodat is het volgen door de definitieve omzetting essentieel.<br>U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.<br>U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.<br>Met de optie Afhankelijkheid toevoegen kan metrisch met succes worden verhoogd als een andere succesmetrische waarde is bereikt of niet is bereikt.<br>Een afhankelijkheid toevoegen:<ol><li>Klik op [!UICONTROL Advanced Settings] onder het menu met drie punten rechts van Extra doelstelling.</li><li>Klik op de knop [!UICONTROL Add Dependency] onder aan het dialoogvenster [!UICONTROL Reporting Settings] sectie.</li><li>Sleep de gewenste metriek vanuit het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op [!UICONTROL Reached] om de instelling tussen [!UICONTROL Reached] en [!UICONTROL Not Reached]</li></ol>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd. |
   | Omzettingsmetrisch | Standaard is de metrische conversie hetzelfde als de metrische optimalisatiedoelstelling. U kunt echter wel een aparte omzettingsmaatstaf definiëren door de optie [!UICONTROL Same as Optimization Goal] optie. |
   | Aanvullende cijfers | Voeg aanvullende rapportgegevens toe die u wilt gebruiken. U kunt conversie- of inkomstenmetriek toevoegen.<br>**Opmerking**: Metrisch van de Betrokkenheid wordt niet ook gesteund als extra metrisch. In de UI kunt u de metrische betrokkenheid selecteren, maar de gegevens worden niet correct weergegeven in rapporten. |
   | Soorten publiek voor rapportage | Voeg publiek toe om het filtreren door publiek in rapporten toe te laten. Standaard toont het rapport resultaten voor alle gekwalificeerde bezoekers. Voeg publiek toe aan filterresultaten voor specifiekere subsets van bezoekers.<br>**Opmerking**: In tegenstelling tot andere soorten activiteiten kan Automated Personalization Adobe Analytics niet als rapportagebron gebruiken. |
   | Notities | Typ alle informatie over uw activiteiten die u voor uzelf of andere teamleden kunt gebruiken. Het deelvenster Notities kan opnieuw worden geschaald. |

   Wanneer u metrische gegevens een naam geeft of de naam ervan wijzigt, zijn de volgende tekens niet toegestaan:

   | Teken | Beschrijving |
   |--- |--- |
   | / | slash |
   | ? | Vraagteken |
   | Aantal | Nummerteken |
   | : | Colon |
   | = | Gelijk aan |
   | + | Plus |
   | - | Min |
   | @ | Bij ondertekenen |

Nadat u op **[!UICONTROL Create]**, wordt het Activiteitenoverzicht weergegeven. Klikken **Voorvertoning van ervaringen** om te bekijken hoe je ervaringen eruit zien wanneer je wordt geleverd. Er wordt een pop-up weergegeven die u kunt gebruiken om koppelingen naar uw AP-ervaringen op uw site weer te geven en te delen voor een &quot;echte voorvertoning&quot; van de ervaringen buiten de Visual Experience Composer van Target. U moet de koppelingen vanuit het bericht delen om de voorvertoning te kunnen delen. Wanneer u op een koppeling klikt en vervolgens de URL rechtstreeks vanaf de pagina kopieert, werkt de URL niet omdat de URL een parameter bevat die de pagina alleen correct weergeeft wanneer u de pagina opent via de koppeling in het bericht.

Voor informatie over rapportage raadpleegt u [Automated Personalization-rapporten](/help/main/c-reports/personalization-reports/reports-ap.md).
