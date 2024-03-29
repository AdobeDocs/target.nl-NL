---
keywords: geautomatiseerde personalisatie;ap
description: Leer hoe u een [!UICONTROL Automated Personalization] (AP) activiteit in [!DNL Adobe Target] met de [!UICONTROL Visual Experience Composer].
title: Hoe maak ik een [!UICONTROL Automated Personalization] Activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: d5b24f298ae405d57c2ba639082cbe99c4e358fd
workflow-type: tm+mt
source-wordcount: '1729'
ht-degree: 0%

---

# Een [!UICONTROL Automated Personalization] activiteit

Een [!UICONTROL Automated Personalization] (AP) activiteit in [!DNL Adobe Target] met de [!UICONTROL Visual Experience Composer] (VEC).

De [!UICONTROL Automated Personalization] (AP) werkstroom in [!DNL Target] varieert van het werkschema van de andere activiteitentypes.

1. Van de [!DNL Target] [!UICONTROL Activities] lijst, klik **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

   ![Activiteiten maken: Automated Personalization](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. Als u de opdracht [!UICONTROL Visual Experience Composer] (VEC) klikt u op **[!UICONTROL Visual]**.

   Als u de opdracht [!UICONTROL Form-Based Experience Composer], selecteert u [!UICONTROL Form]. Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor meer informatie .

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer], [!DNL Target] biedt de [!UICONTROL Single Page Application VEC]. Zie voor meer informatie over de verschillende composers [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, zie [Problemen oplossen met de composer voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) [Een werkruimte kiezen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verifieer of ga de activiteit URL in, dan klik **[!UICONTROL Create]**.

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ([!DNL https] en [!DNL http]). Dientengevolge, [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide komen overeen.

   De pagina met de opgegeven URL wordt geopend in de VEC.

1. Klik op de knop **[!UICONTROL Name]** en typ de naam van uw activiteit.

   ![Naamveld](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

   De naam van de activiteit mag geen van de volgende tekenreeksen bevatten:

   | Tekenreeks | Beschrijving |
   |--- |--- |
   | ;= | Semicolon, is gelijk aan |
   | ;+ | Puntkomma, plus |
   | ;- | Puntkomma, min |
   | ;@ | Puntkomma, bij teken |
   | ,= | Komma, is gelijk aan |
   | ,+ | Komma, plus |
   | ,- | Komma, min |
   | ,@ | Komma, bij teken |
   | `[`&quot; | Vierkante haak openen, dubbele aanhalingstekens |
   | &quot;`]` | Dubbele aanhalingstekens, vierkant haakje sluiten |

1. Pagina-elementen wijzigen zoals wordt uitgelegd in [Opties voor Visual Experience Composer](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   U kunt meerdere afbeeldingen tegelijk selecteren in het middelenbeheer. Zo kunt u snel de pagina weergeven met elk van de afbeeldingen die voor de activiteit zijn geconfigureerd. U kunt ook gemakkelijk tekstelementen in uw aanbiedingen bewerken. Wanneer u een element bewerkt, verschijnen er balken op dat element om aan te geven dat u het element hebt gewijzigd.

1. Klikken **[!UICONTROL Manage Content]** om de beschikbare combinaties te vormen.

   ![Inhoud beheren, optie](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Er wordt een dialoogvenster weergegeven met drie opties boven aan het scherm: [!UICONTROL Experiences], [!UICONTROL Offers], en [!UICONTROL Exclusion Groups].

   ![Inhoud beheren, dialoogvenster](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Hoewel u tot 30.000 ervaringen in een AP activiteit kunt tot stand brengen, presteert de activiteit het best wanneer minder dan 5.000 ervaringen worden gebruikt. Deze limiet wordt ook toegepast als de activiteit de optie [!UICONTROL Disalow Duplicates] -optie.

   De [!UICONTROL Experiences] in de lijst wordt elk stuk inhoud weergegeven dat is geselecteerd voor de activiteit en de locatie waaraan deze is toegewezen.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op de knop [!UICONTROL Exclude] pictogram.

   ![Pictogramaanwijs uitsluiten](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png)

   U kunt ervaringen in batch uitsluiten of opnemen door het selectievakje voor de relevante ervaringen in te schakelen en vervolgens op de knop [!UICONTROL Exclude] in de rechterbovenhoek van het dialoogvenster.

   ![Opties voor uitsluiten in batch](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png)

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de knop [!UICONTROL Status] vervolgkeuzelijst.

1. (Voorwaardelijk) Klik **[!UICONTROL Offers]** om stukken inhoud te selecteren en deze aan rapportagegroepen toe te wijzen, of alleen bepaalde bezoekers bepaalde aanbiedingen te laten zien waarvoor ze zich richten.

   Zie voor meer informatie over rapportagegroepen [Rapportagegroepen aanbieden in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

1. (Voorwaardelijk) Klik **[!UICONTROL Exclusion Groups]** om een willekeurige combinatie van elementen te kiezen die u van de activiteit wilt uitsluiten.

   ![Het tabblad Uitsluitingsgroepen van het dialoogvenster Inhoud beheren](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Hoewel u tot 30.000 ervaringen in een AP test kunt tot stand brengen, voert het algoritme zijn beste uit wanneer minder dan 10.000 verschillende ervaringen worden gebruikt. Deze limiet wordt ook toegepast als de activiteit de optie [!UICONTROL Disalow Duplicates] -optie.

   Als er momenteel geen uitsluitingsgroepen in uw activiteit zijn opgenomen, klikt u op **Uitsluitingsgroep maken**. U kunt filteren om een lijst te creëren die slechts de combinaties toont u wilt uitsluiten. Geef uw uitsluitingsgroep een naam en klik vervolgens op **Opslaan**.

   Als u een bestaande uitsluitingsgroep wilt bewerken, plaatst u de aanwijzer boven de groep die u wilt bewerken en klikt u op het potloodpictogram.

1. Klikken **[!UICONTROL Done]** als u klaar bent met het instellen van de inhoud van uw activiteit.

1. De **Targeting** de stap ziet er vertrouwd uit als u andere [!DNL Target] typen activiteiten. Hier kunt u een publiek selecteren en het percentage bezoekers opgeven dat de besturingservaring weergeeft door op de knop **[!UICONTROL Custom Allocation]** vervolgkeuzelijst en vervolgens op **Volgende**.

   De [!UICONTROL Custom Allocation] In de vervolgkeuzelijst kunt u de volgende opties kiezen:

   ![Verkeerstoewijzingsdoel, vervolgkeuzelijst](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** Als uw doel het algoritme is te testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** Als uw doel het creëren van &quot;altijd op&quot;activiteit is, zet 10% van de bezoekers in de controle. Deze optie zorgt ervoor dat er genoeg gegevens zijn voor de algoritmen om door te gaan met het leren in de tijd. De handel hier is dat in ruil voor het personaliseren van een groter deel van je verkeer, je minder nauwkeurigheid hebt in wat de exacte lift is. Geen kwestie uw doel, is deze optie de geadviseerde verkeerspleet wanneer het gebruiken van een specifieke ervaring als controle.
   * **[!UICONTROL Custom Allocation]:** Splits het percentage handmatig naar wens.

1. (Voorwaardelijk) Van de [!UICONTROL Control] vervolgkeuzelijst, [een specifieke ervaring selecteren die als controle moet worden gebruikt](/help/main/c-activities/t-automated-personalization/experience-as-control.md) of selecteer [!UICONTROL Random Experience.]

   De ervaring met het bedieningsorgaan levert een vergelijking op om te bepalen hoeveel lift door de geautomatiseerde test wordt geleverd.

   [!UICONTROL Automated Personalization] meet altijd prestaties tegen een controlegroep. De beste manier is om ten minste 10% van de deelnemers aan de controlegroep te plaatsen. Als uw doel is te testen als het verpersoonlijkingsalgoritme op het gegeven gegeven gegevens beter dan geen verpersoonlijking (bijvoorbeeld, de willekeurig gediende controle) presteert, is een 50/50 percenten die percenten verkeer tussen de controle en het verpersoonlijkingsalgoritme de snelste en meest nauwkeurige manier om dit doel te bereiken wordt verdeeld. Als u de hoeveelheid verkeer wilt maximaliseren dat gepersonaliseerd is en u minder met het begrijpen van de nauwkeurige lift uw activiteit produceert, is een 10/90 percenten die verkeer tussen de controle en het verpersoonlijkingsalgoritme wordt verdeeld de snelste en meest nauwkeurige manier om dit doel te bereiken.

   >[!NOTE]
   >
   >In [!UICONTROL Automated Personalization] de activiteiten, ingangscriteria (het richten van URL, malplaatjeregels, en publieksdoelstellingen) worden geëvalueerd voor elk verzoek. In vorige versies werden de entry criteria één keer per sessie geëvalueerd.

1. Klikken **[!UICONTROL Next]** om de **[!UICONTROL Goals & Settings]** pagina.
1. Vorm de activiteit met de volgende montages, dan klik **[!UICONTROL Save & Close]**.

   | Instelling | Beschrijving |
   |--- |--- |
   | [!UICONTROL Name] | Geef de activiteit een naam. Geef de activiteit een naam die beschrijvend genoeg is dat de teamleden het in de [!UICONTROL Activities] lijst. Raadpleeg de bovenstaande tabel om te zien welke tekens niet zijn toegestaan in een naam van een activiteit. |
   | [!UICONTROL Objective] | (Optioneel) Typ het doel van de test. Het doel helpt u het doel van de activiteit te herinneren. |
   | [!UICONTROL Priority] | Afhankelijk van uw instellingen worden [!DNL Target] UI en opties voor [!UICONTROL Priority] variëren. U kunt de oudere instellingen van [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High]of u kunt fijnkorrelige prioriteiten inschakelen van 0 tot en met 999.<P>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<P>Als deze optie niet is ingeschakeld in [!UICONTROL Administration] > [!UICONTROL Reporting] (standaard) geeft u een prioriteit op: [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High].<P>Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op [!UICONTROL Administration] > [!UICONTROL Reporting]en schakelt u vervolgens de [!UICONTROL Enable Fine-Grained Priorities] aan de positie &quot;Aan&quot;.<P>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:<ul><li>0 = Laag</li><li>999 = Hoog</li></ul>Voor activiteiten die in vorige versies van [!DNL Target Standard/Premium], [!UICONTROL Low] prioriteit wordt omgezet in 0, [!UICONTROL Medium] prioriteit wordt omgezet in 5, en [!UICONTROL High] prioriteit wordt omgezet in 10. U kunt deze waarden desgewenst aanpassen.<P>**Opmerking**: Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld. |
   | [!UICONTROL Duration] | Stel de begin- en einddatum voor de activiteit in. U kunt [!UICONTROL When Activated] of u kunt een specifieke datum en tijd opgeven. |
   | [!UICONTROL Optimization Goal] | Geef het optimalisatiedoel op, dat uit twee parameters bestaat:<ul><li>Wat u met de activiteit wilt meten</li><li>De actie van een deelnemer aan een activiteit die aantoont dat het doel is bereikt.</li></ul>U kunt het optimalisatiedoel een naam geven door de drie stippen rechts van [!UICONTROL My Primary Goal]. [!UICONTROL Automated Personalization] activiteiten kunnen [!UICONTROL Conversion] of [!UICONTROL Revenue]. Conversie is mogelijk door een pagina weer te geven of door een box te bekijken. Klik kan ook worden gevolgd.<P>Het primaire doel wordt ook de modelleringsmetrisch die door het modelleringssysteem wordt gebruikt om het succes van de ervaring te berekenen.<P>Bezoekers kunnen in de activiteit blijven voor traceringsdoeleinden nadat ze het modelleringsdoel hebben bereikt. Vaak worden bijvoorbeeld [!UICONTROL Automated Personalization] activiteit wordt gebruikt om kliktarieven te verbeteren, en dat wordt geplaatst als modelleringsdoel. Nochtans, is het belangrijk om te zien hoe de verhoogde klikkoersen tot definitieve omzetting leiden, zodat is het volgen door de definitieve omzetting essentieel.<P>U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.<P>U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.<P>De [!UICONTROL Add Dependency] optie staat succesmetrisch toe om te verhogen als een ander succes metrisch is bereikt of niet bereikt.<P>Een afhankelijkheid toevoegen:<ol><li>Klik op **[!UICONTROL Advanced Settings]** onder het menu met drie punten rechts van [!UICONTROL Additional Goal].</li><li>Klik op de knop **[!UICONTROL Add Dependency]** onder aan het dialoogvenster [!UICONTROL Reporting Settings] sectie.</li><li>Sleep de gewenste metriek vanuit het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op [!UICONTROL Reached] om de instelling tussen [!UICONTROL Reached] en [!UICONTROL Not Reached].</li></ol>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd. |
   | [!UICONTROL Conversion Metric] | Standaard is de metrische conversie hetzelfde als de metrische optimalisatiedoelstelling. U kunt echter wel een aparte omzettingsmaatstaf definiëren door de optie [!UICONTROL Same as Optimization Goal] -optie. |
   | [!UICONTROL Additional Metrics] | Voeg aanvullende rapportgegevens toe die u wilt gebruiken. U kunt conversie- of inkomstenwaarden toevoegen.<P>**Opmerking**: De [!UICONTROL Engagement] Metrisch wordt niet ondersteund als extra metrisch. De [!DNL Target] U kunt de interface selecteren [!UICONTROL Engagement] metrisch, maar de gegevens tonen correct niet in rapporten. |
   | [!UICONTROL Audiences for Reporting] | Voeg publiek toe om het filtreren door publiek in rapporten toe te laten. Standaard geeft het rapport resultaten weer voor alle gekwalificeerde bezoekers. Voeg publiek toe aan filterresultaten voor specifiekere subsets van bezoekers.<P>**Opmerking**: In tegenstelling tot andere activiteitstypen, [!UICONTROL Automated Personalization] kan niet gebruiken [!UICONTROL Adobe Analytics] als rapportagebron (A4T). |
   | [!UICONTROL Notes] | Typ alle informatie over uw activiteiten die nuttig is voor u of voor andere teamleden. De [!UICONTROL Notes] is resizable. |

   Wanneer u metrisch noemt of anders noemt, worden de volgende karakters niet toegestaan:

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

Nadat u op **[!UICONTROL Save & Close]**, de [!UICONTROL Overview] wordt weergegeven. Klikken **Voorvertoning van ervaringen** om te bekijken hoe je ervaringen eruit zien wanneer je wordt geleverd. Er verschijnt een pop-up die u kunt gebruiken om koppelingen naar uw AP-ervaringen op uw site weer te geven en te delen voor een &quot;echte voorvertoning&quot; van de ervaringen buiten het [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (VEC). U moet de koppelingen vanuit het bericht delen om de voorvertoning te kunnen delen. U kunt niet op een koppeling klikken en de URL rechtstreeks vanuit de browser kopiëren. Als u de koppeling kopieert, bevat de URL een parameter die de pagina alleen correct weergeeft wanneer u de pagina opent via de koppeling in het bericht.

Zie voor informatie over rapportage [Automated Personalization-rapporten](/help/main/c-reports/personalization-reports/reports-ap.md).
