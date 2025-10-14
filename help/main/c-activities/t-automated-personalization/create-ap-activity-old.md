---
keywords: geautomatiseerde personalisatie;ap
description: Leer hoe te om een [!UICONTROL Automated Personalization] (AP) activiteit in  [!DNL Adobe Target]  tot stand te brengen gebruikend [!UICONTROL Visual Experience Composer].
title: Hoe maak ik een [!UICONTROL Automated Personalization] -activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '1743'
ht-degree: 0%

---

# Een [!UICONTROL Automated Personalization] activiteit maken

Maak een [!UICONTROL Automated Personalization] (AP)-activiteit in [!DNL Adobe Target] met behulp van [!UICONTROL Visual Experience Composer] (VEC).

De werkstroom [!UICONTROL Automated Personalization] (AP) activiteit in [!DNL Target] varieert van het werkschema van de andere activiteitstypen.

1. Klik in de lijst [!DNL Target] [!UICONTROL Activities] op **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]** .

   ![&#x200B; creeer Activiteit: Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/assets/ap-create-new.png)

1. Klik op [!UICONTROL Visual Experience Composer] als u **[!UICONTROL Visual]** (VEC) wilt gebruiken.

   Selecteer [!UICONTROL Form-Based Experience Composer] als u [!UICONTROL Form] wilt gebruiken. Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] de [!UICONTROL Single Page Application VEC] . Voor meer informatie over de diverse composers, zie [&#x200B; Ervaringen en Aanbiedingen &#x200B;](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, zie [&#x200B; het Oplossen van problemen de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) [&#x200B; kies een werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Verifieer of voer de activiteit-URL in en klik vervolgens op **[!UICONTROL Create]** .

   >[!NOTE]
   >
   >[!DNL Target] maakt geen onderscheid tussen URL-protocollen ([!DNL https] en [!DNL http]). Hierdoor komen [!DNL `http://www.adobe.com`] en [!DNL `https://wwww.adobe.com`] beide overeen.

   De pagina met de opgegeven URL wordt geopend in de VEC.

1. Klik op het veld **[!UICONTROL Name]** en typ de naam van uw activiteit.

   ![&#x200B; het gebied van de Naam &#x200B;](/help/main/c-activities/t-automated-personalization/assets/ap-new-name.png)

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

1. Wijzig paginaelementen zoals die in [&#x200B; de opties van Composer van de Ervaring worden verklaard Visuele &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   U kunt meerdere afbeeldingen tegelijk selecteren in het middelenbeheer. Zo kunt u snel de pagina weergeven met elk van de afbeeldingen die voor de activiteit zijn geconfigureerd. U kunt ook gemakkelijk tekstelementen in uw aanbiedingen bewerken. Wanneer u een element bewerkt, verschijnen er balken op dat element om aan te geven dat u het element hebt gewijzigd.

1. Klik op **[!UICONTROL Manage Content]** om de beschikbare combinaties te configureren.

   ![&#x200B; beheert de optie van de Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Er wordt een dialoogvenster weergegeven met drie opties boven aan het scherm: [!UICONTROL Experiences], [!UICONTROL Offers] en [!UICONTROL Exclusion Groups] .

   ![&#x200B; beheert de dialoogdoos van de Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/ap_content-new.png)

   >[!NOTE]
   >
   >Hoewel u tot 30.000 ervaringen in een AP activiteit kunt tot stand brengen, presteert de activiteit het best wanneer minder dan 5.000 ervaringen worden gebruikt. Deze limiet wordt ook toegepast wanneer de activiteit de optie [!UICONTROL Disalow Duplicates] heeft ingeschakeld.

   In de lijst [!UICONTROL Experiences] wordt elk stuk inhoud weergegeven dat is geselecteerd voor de activiteit en de locatie waaraan deze is toegewezen.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram [!UICONTROL Exclude] te klikken.

   ![&#x200B; sluit pictogramaanwijzer &#x200B;](/help/main/c-activities/t-automated-personalization/assets/icon-exclude.png) uit

   U kunt ervaringen in batch uitsluiten of opnemen door het selectievakje voor relevante ervaringen in te schakelen en vervolgens op het pictogram [!UICONTROL Exclude] rechtsboven in het dialoogvenster te klikken.

   ![&#x200B; Partij sluit opties &#x200B;](/help/main/c-activities/t-automated-personalization/assets/batch-exclude.png) uit

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de vervolgkeuzelijst [!UICONTROL Status] te klikken.

1. (Voorwaardelijk) Klik **[!UICONTROL Offers]** om stukken inhoud te selecteren en deze toe te wijzen aan rapportagegroepen of om alleen bepaalde bezoekers toe te staan bepaalde aanbiedingen te zien waarvoor ze zich richten.

   Voor meer informatie over het melden van groepen, zie [&#x200B; Aanbieding die groepen in Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md) melden.

1. (Voorwaardelijk) Klik **[!UICONTROL Exclusion Groups]** om een willekeurige combinatie van elementen te kiezen die u van de activiteit wilt uitsluiten.

   ![&#x200B; het lusje van de Groepen van de Uitsluiting van Manage de dialoogdoos van de Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Hoewel u tot 30.000 ervaringen in een AP test kunt tot stand brengen, voert het algoritme zijn beste uit wanneer minder dan 10.000 verschillende ervaringen worden gebruikt. Deze limiet wordt ook toegepast wanneer de activiteit de optie [!UICONTROL Disalow Duplicates] heeft ingeschakeld.

   Als u momenteel geen uitsluitingsgroepen inbegrepen in uw activiteit hebt, klik **creeer de Groep van de Uitsluiting**. U kunt filteren om een lijst te creëren die slechts de combinaties toont u wilt uitsluiten. Noem uw uitsluitingsgroep, dan klik **sparen**.

   Als u een bestaande uitsluitingsgroep wilt bewerken, plaatst u de aanwijzer boven de groep die u wilt bewerken en klikt u op het potloodpictogram.

1. Klik op **[!UICONTROL Done]** als u de inhoud van uw activiteit hebt ingesteld.

1. De **het richten** stap kijkt vertrouwd als u andere [!DNL Target] activiteitstypes hebt gebruikt. Hier kunt u een publiek selecteren en het percentage bezoekers specificeren die de controleervaring zien door de **[!UICONTROL Custom Allocation]** drop-down lijst te klikken, dan **daarna** klikken.

   In de vervolgkeuzelijst [!UICONTROL Custom Allocation] kunt u uit de volgende opties kiezen:

   ![&#x200B; drop-down lijst van het Doel van de Toewijzing van het Verkeer &#x200B;](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** als uw doel het algoritme moet testen, gebruik een 50/50 percenten verdeling van bezoekers tussen de controle en het gerichte algoritme. Deze splitsing geeft de meest nauwkeurige schatting van de lift. Voorgesteld voor gebruik met &quot;willekeurige ervaringen&quot; als controle.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** Als uw doel &quot;altijd op&quot;activiteit is tot stand te brengen, zet 10% van de bezoekers in de controle. Deze optie zorgt ervoor dat er genoeg gegevens zijn voor de algoritmen om door te gaan met het leren in de tijd. De handel hier is dat in ruil voor het personaliseren van een groter deel van je verkeer, je minder nauwkeurigheid hebt in wat de exacte lift is. Geen kwestie uw doel, is deze optie de geadviseerde verkeerspleet wanneer het gebruiken van een specifieke ervaring als controle.
   * **[!UICONTROL Custom Allocation]:** verdeel manueel het percentage zoals gewenst.

1. (Voorwaardelijk) van de [!UICONTROL Control] drop-down lijst, [&#x200B; selecteer een specifieke ervaring die als controle &#x200B;](/help/main/c-activities/t-automated-personalization/experience-as-control.md) moet worden gebruikt of [!UICONTROL Random Experience.] selecteren

   De ervaring met het bedieningsorgaan levert een vergelijking op om te bepalen hoeveel lift door de geautomatiseerde test wordt geleverd.

   [!UICONTROL Automated Personalization] meet de prestaties altijd ten opzichte van een controlegroep. De beste manier is om ten minste 10% van de deelnemers aan de controlegroep te plaatsen. Als uw doel is te testen als het verpersoonlijkingsalgoritme op het gegeven gegeven gegevens beter dan geen verpersoonlijking (bijvoorbeeld, de willekeurig gediende controle) presteert, is een 50/50 percenten die percenten verkeer tussen de controle en het verpersoonlijkingsalgoritme de snelste en meest nauwkeurige manier om dit doel te bereiken wordt verdeeld. Als u de hoeveelheid verkeer wilt maximaliseren dat gepersonaliseerd is en u minder met het begrijpen van de nauwkeurige lift uw activiteit produceert, is een 10/90 percenten die verkeer tussen de controle en het verpersoonlijkingsalgoritme wordt verdeeld de snelste en meest nauwkeurige manier om dit doel te bereiken.

   >[!NOTE]
   >
   >Bij [!UICONTROL Automated Personalization] -activiteiten worden de entry-criteria (URL-adressering, sjabloonregels en doelgroepen) voor elke aanvraag geëvalueerd. In vorige versies werden de entry criteria één keer per sessie geëvalueerd.

1. Klik op **[!UICONTROL Next]** om de pagina **[!UICONTROL Goals & Settings]** weer te geven.
1. Configureer de activiteit met de volgende instellingen en klik vervolgens op **[!UICONTROL Save & Close]** .

   | Instelling | Beschrijving |
   |--- |--- |
   | [!UICONTROL Name] | Geef de activiteit een naam. Geef de activiteit een naam die beschrijvend genoeg is dat de teamleden het in de [!UICONTROL Activities] lijst kunnen erkennen. Raadpleeg de bovenstaande tabel om te zien welke tekens niet zijn toegestaan in een naam van een activiteit. |
   | [!UICONTROL Objective] | (Optioneel) Typ het doel van de test. Het doel helpt u het doel van de activiteit te herinneren. |
   | [!UICONTROL Priority] | Afhankelijk van uw instellingen variëren de [!DNL Target] interface en de opties voor [!UICONTROL Priority] . U kunt de oudere instellingen van [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] gebruiken of u kunt fijngeoriënteerde prioriteiten van 0 tot en met 999 inschakelen.<P>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<P>Als deze optie niet is ingeschakeld in [!UICONTROL Administration] > [!UICONTROL Reporting] (de standaardinstelling), geeft u een prioriteit op: [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] .<P>Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op [!UICONTROL Administration] > [!UICONTROL Reporting] en schakelt u de optie [!UICONTROL Enable Fine-Grained Priorities] in op de positie &quot;Aan&quot;.<P>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:<ul><li>0 = Laag</li><li>999 = Hoog</li></ul>Voor activiteiten die in vorige versies van [!DNL Target Standard/Premium] zijn gemaakt, wordt [!UICONTROL Low] priority omgezet in 0, [!UICONTROL Medium] priority wordt omgezet in 5 en [!UICONTROL High] priority wordt omgezet in 10. U kunt deze waarden desgewenst aanpassen.<P>**Nota**: Alvorens u deze optie na het gebruiken van fijn-gegrainde prioriteiten kunt onbruikbaar maken, moeten alle prioriteiten terug naar 0, 5, en 10 worden geplaatst. |
   | [!UICONTROL Duration] | Stel de begin- en einddatum voor de activiteit in. U kunt [!UICONTROL When Activated] selecteren of u kunt een specifieke datum en tijd opgeven. |
   | [!UICONTROL Optimization Goal] | Geef het optimalisatiedoel op, dat uit twee parameters bestaat:<ul><li>Wat u met de activiteit wilt meten</li><li>De actie van een deelnemer aan een activiteit die aantoont dat het doel is bereikt.</li></ul>U kunt het optimalisatiedoel een naam geven door de drie stippen rechts van [!UICONTROL My Primary Goal] te selecteren. [!UICONTROL Automated Personalization] -activiteiten kunnen [!UICONTROL Conversion] of [!UICONTROL Revenue] meten. Conversie is mogelijk door een pagina weer te geven of door een box te bekijken. Klik kan ook worden gevolgd.<P>Het primaire doel wordt ook de modelleringsmetrisch die door het modelleringssysteem wordt gebruikt om het succes van de ervaring te berekenen.<P>Bezoekers kunnen in de activiteit blijven voor traceringsdoeleinden nadat ze het modelleringsdoel hebben bereikt. Een [!UICONTROL Automated Personalization] -activiteit wordt bijvoorbeeld vaak gebruikt om kliksnelheden te verbeteren. Dit wordt ingesteld als modelleringsdoel. Nochtans, is het belangrijk om te zien hoe de verhoogde klikkoersen tot definitieve omzetting leiden, zodat is het volgen door de definitieve omzetting essentieel.<P>U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.<P>U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.<P>Met de optie [!UICONTROL Add Dependency] kan de metrische waarde met succes worden verhoogd als een andere maatstaf met succes is bereikt of niet is bereikt.<P>Een afhankelijkheid toevoegen:<ol><li>Nadat u aanvullende metriek hebt toegevoegd, klikt u op **[!UICONTROL Advanced Settings]** onder het menu met drie punten rechts van [!UICONTROL Additional Goal] .</li><li>Klik op de optie **[!UICONTROL Add Dependency]** onder aan de sectie [!UICONTROL Reporting Settings] .</li><li>Sleep de gewenste metriek van het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op [!UICONTROL Reached] om de instelling tussen [!UICONTROL Reached] en [!UICONTROL Not Reached] te schakelen.</li></ol>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd. |
   | [!UICONTROL Conversion Metric] | Standaard is de metrische conversie hetzelfde als de metrische optimalisatiedoelstelling. U kunt echter een aparte omzettingsmaatstaf definiëren door de optie [!UICONTROL Same as Optimization Goal] uit te schakelen. |
   | [!UICONTROL Additional Metrics] | Voeg aanvullende rapportgegevens toe die u wilt gebruiken. U kunt conversie- of inkomstenwaarden toevoegen.<P>**Nota**: [!UICONTROL Engagement] metrisch wordt niet gesteund als extra metrisch. In de gebruikersinterface van [!DNL Target] kunt u mogelijk de [!UICONTROL Engagement] -methode selecteren, maar de gegevens worden niet correct weergegeven in rapporten. |
   | [!UICONTROL Audiences for Reporting] | Voeg publiek toe om het filtreren door publiek in rapporten toe te laten. Standaard geeft het rapport resultaten weer voor alle gekwalificeerde bezoekers. Voeg publiek toe aan filterresultaten voor specifiekere subsets van bezoekers.<P>**Nota**: In tegenstelling tot andere activiteitstypes, [!UICONTROL Automated Personalization] kan niet [!UICONTROL Adobe Analytics] als zijn rapporteringsbron (A4T) gebruiken. |
   | [!UICONTROL Notes] | Typ alle informatie over uw activiteiten die nuttig is voor u of voor andere teamleden. U kunt het formaat van het deelvenster [!UICONTROL Notes] wijzigen. |

   Wanneer u metrisch noemt of anders noemt, worden de volgende karakters niet toegestaan:

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

Nadat u op **[!UICONTROL Save & Close]** hebt geklikt, wordt de [!UICONTROL Overview] -pagina van de activiteit weergegeven. Klik **Ervaringen van de Voorproef** aan voorproef hoe uw ervaringen wanneer geleverd kijken. Er wordt een pop-up weergegeven die u kunt gebruiken om koppelingen naar uw AP-ervaringen op uw site weer te geven en te delen voor een &quot;echte voorvertoning&quot; van de ervaringen buiten de [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (VEC). U moet de koppelingen vanuit het bericht delen om de voorvertoning te kunnen delen. U kunt niet op een koppeling klikken en de URL rechtstreeks vanuit de browser kopiëren. Als u de koppeling kopieert, bevat de URL een parameter die de pagina alleen correct weergeeft wanneer u de pagina opent via de koppeling in het bericht.

Voor informatie over het melden, zie [&#x200B; Rapporten van Automated Personalization &#x200B;](/help/main/c-reports/personalization-reports/reports-ap.md).
