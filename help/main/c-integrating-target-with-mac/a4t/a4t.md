---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target;atjs;at.js;adobe Experience platform web sdk;platform web sdk;platform sdk
description: Gebruik  [!DNL Analytics]  voor  [!DNL Target]  (A4T) om activiteiten tot stand te brengen die op  [!DNL Analytics]  worden gebaseerd omzettingsmetriek en publiekssegmenten en gebruik  [!DNL Analytics]  rapporten om resultaten te onderzoeken.
title: Wat is  [!DNL Analytics]  voor  [!DNL Target]  (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: f7bb9b5d6e96095a31f50f1976b87d9ee7b7eb51
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# [!DNL Adobe Analytics] als de rapportbron voor [!DNL Adobe Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van [!DNL Analytics] -omzettingsmaatstaven en publiekssegmenten. Met de integratie A4T kunt u [!DNL Analytics] -rapporten gebruiken om uw resultaten te bekijken. Als u [!DNL Analytics] als rapportagebron voor een activiteit gebruikt, is alle rapportage en segmentatie voor die activiteit gebaseerd op [!DNL Analytics] -gegevensverzameling.

## Overzicht {#section_92B66069210C40DBA937790E8CC596CF}

De [!DNL Analytics for Target] integratie tussen [!DNL Analytics] en [!DNL Target] biedt krachtige gereedschappen voor analyse en tijdbesparing voor uw optimalisatieprogramma.

De drie belangrijkste voordelen van het gebruik van [!DNL Analytics] data in [!DNL Target] zijn:

* Marketers kunnen op elk gewenst moment dynamisch [!DNL Analytics] succeswaarden of rapportsegmenten toepassen op [!DNL Target] -activiteitenrapporten. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Een enkele gegevensbron voorkomt de variantie die optreedt wanneer gegevens in twee afzonderlijke systemen worden verzameld.
* Met de bestaande [!DNL Analytics] -implementatie worden alle vereiste gegevens verzameld. Het is niet nodig vakken op pagina&#39;s te implementeren om alleen gegevens voor rapporten te verzamelen.

Als u [!DNL Analytics] als rapportagebron voor een activiteit gebruikt, is alle rapportage en segmentatie voor die activiteit gebaseerd op [!DNL Analytics] .

Alle [!DNL Analytics] metriek, inclusief berekende metriek, zijn beschikbaar in [!DNL Target] en het [!UICONTROL Target Activities] rapport in [!DNL Analytics], met één uitzondering. De berekende metriek voor [!UICONTROL Lift & Confidence] worden niet gesteund. Op dezelfde manier kan elk segment dat beschikbaar is in [!DNL Analytics], worden toegepast op beide oplossingen. U kunt de metrische waarde of het publiek toepassen op het rapport in [!DNL Target] nadat de activiteit is gestart, of zelfs nadat de activiteit is voltooid.

Elke metrische waarde is inbegrepen, met inbegrip van om het even welke douane of berekende metriek die ingebouwde in [!DNL Analytics] zijn.

Na de rubriceringsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

Houd rekening met de volgende punten wanneer u overweegt A4T te gebruiken:

* Als u [!DNL Analytics] als rapportagebron voor [!DNL Target] wilt gebruiken, moeten zowel u als uw bedrijf toegang hebben tot [!DNL Analytics] en [!DNL Target] . [&#x200B; contacteer uw rekeningsvertegenwoordiger &#x200B;](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) als u één van beide oplossing nodig hebt.
* De bron van de rapportage wordt voor elke activiteit ingesteld. [!DNL Target] gaat door met het verzamelen van gegevens die worden gebruikt voor rapportage en [!DNL Target] -gegevens zijn nog steeds beschikbaar als u een activiteit liever baseert op gegevens die worden verzameld door [!DNL Target] .
* Gebruik één rapporteringsbron of andere. U kunt geen gegevens verzamelen voor één activiteit uit beide bronnen.
* Wanneer u A4T gebruikt, zijn alle succesmeetgegevens die beschikbaar zijn voor uw activiteiten [!DNL Analytics] metriek. Nochtans, kan uw doel metrisch worden gebaseerd op een mbox vraag als het gebruiken van at.js. U kunt bijvoorbeeld de uit-van-de-doos klikvolgende mogelijkheden van Doel met A4T in plaats van het moeten [!DNL Analytics] klik-volgende code uitvoeren.
* Wanneer u rapporten weergeeft van een A4T-activiteit in de [!DNL Target] -gebruikersinterface, bekijkt u [!DNL Analytics] -gegevens. Als u bijvoorbeeld de waarde [!UICONTROL Visitor] metrisch in [!DNL Target] gebruikt, gebruikt u de waarde [!DNL Analytics] [!UICONTROL Visitor] , niet de waarde [!DNL Target] [!UICONTROL Visitors] die nu [!UICONTROL Entrants] wordt genoemd. Dit verschil is met name van belang voor elementaire verkeersmetriek ([!UICONTROL Visitors] , [!UICONTROL Visits] , [!UICONTROL Page Views] ) en conversiemetriek.
* Bestaande [!DNL Target] -activiteiten blijven gebruikmaken van [!DNL Target] -gegevensverzameling en worden niet beïnvloed door het inschakelen van A4T.
* Bij het gebruik van A4T is slechts één metrische waarde op basis van een doos toegestaan.
* Een server-aan-server vraag van [!DNL Target] naar [!DNL Analytics] verzendt activiteit en ervaringsinformatie naar [!DNL Analytics]. Deze integratie leidt niet tot extra serveraanroepen voor [!DNL Target] of [!DNL Analytics] .

  In sommige situaties mislukken de classificaties van [!DNL Target] tot [!DNL Analytics] en geven activiteiten geen gegevens weer in [!DNL Analytics] . Zie [&#x200B; problemen oplossen Analytics en de integratie van het Doel (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). U kunt {de Zorg van de Cliënt van 0} ook [&#x200B; voor verdere hulp contacteren.](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB)

## A4T implementeren

Voor informatie over het uitvoeren van A4T met at.js en [!DNL Adobe Experience Platform Web SDK], zie [&#x200B; Analytics voor  [!DNL Target]  implementatie &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Ondersteunde activiteitstypen {#section_F487896214BF4803AF78C552EF1669AA}

De volgende secties bevatten informatie over ondersteunde activatietypen bij gebruik van [!DNL Adobe Experience Platform Web SDK] of at.js:

| Activiteitstypen | A4T-compatibel? | Opmerkingen, indien van toepassing |
|--- |--- |--- |
| [&#x200B; A/B activiteit met handverkeer spleet &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |  |
| [&#x200B; A/B activiteit met auto-Wijs &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) toe | Ja | Zie [&#x200B; steun A4T voor auto-Wijs en auto-Doel activiteiten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) toe. |
| [&#x200B; activiteit A/B met auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Ja | A4T-ondersteuning voor Auto-Target-activiteiten wordt nu ondersteund voor zowel [!DNL Platform Web SDK] als at.js. |
| [&#x200B; Ervaring die (XT) richt &#x200B;](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |  |
| [&#x200B; Multivariate test (MVT) &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja | Vereist op box-Gebaseerd doel metrisch doel om het [!UICONTROL Element Contribution] rapport te krijgen. Het [!UICONTROL Element Contribution] -rapport biedt momenteel geen ondersteuning voor [!DNL Analytics] -meetgegevens. |
| [&#x200B; Automated Personalization (AP) activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nee |  |
| [&#x200B; activiteit van Aanbevelingen &#x200B;](/help/main/c-recommendations/recommendations.md) | Ja |  |
| [&#x200B; Om het even welke activiteit die een herleidingsaanbieding &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) gebruikt | Ja |

Omdat alle activiteitstypen A4T nog niet ondersteunen, wordt u aangeraden belangrijke conversievakken, zoals de mbox `orderConfirmPage` , te behouden of te implementeren.

## Voorbeelden van A4T-rapporten {#section_F0A43A1CB2F04E8282B909E4D7034361}

Als u A4T-rapporten wilt weergeven in [!DNL Target] , klikt u op **[!UICONTROL Activities]** , klikt u op de gewenste activiteit in de lijst die [!DNL Analytics] als rapportbron gebruikt en klikt u vervolgens op het tabblad **[!UICONTROL Reports]** .

>[!NOTE]
>
>Met de vervolgkeuzelijst [!UICONTROL Reporting Source] boven aan de pagina [!UICONTROL Activities] kunt u alleen activiteiten weergeven die gebruikmaken van A4T.

U kunt schakelen tussen de [!UICONTROL Table View] en [!UICONTROL Graph View] van het rapport door op het juiste pictogram rechtsboven in het rapport te klikken.

In de volgende afbeelding ziet u de [!UICONTROL Graph View] van een A4T-rapport met de vervolgkeuzelijst [!UICONTROL Report Metric] waarin de beschikbare [!DNL Analytics] meetgegevens voor het doel worden weergegeven:

![&#x200B; a4t_report_graph1 beeld &#x200B;](assets/a4t_report_graph1.png)

In de volgende afbeelding ziet u de [!UICONTROL Graph View] van een A4T-rapport met de vervolgkeuzelijst [!UICONTROL Audience] waarin het beschikbare [!DNL Analytics] publiek wordt weergegeven:

![&#x200B; a4t_report_graph2 beeld &#x200B;](assets/a4t_report_graph2.png)

In de volgende afbeelding ziet u de [!UICONTROL Table View] van een A4T-rapport:

![&#x200B; a4t_report_table beeld &#x200B;](assets/a4t_report_table.png)

Als u het rapport wilt weergeven in [!DNL Analytics] in plaats van in [!DNL Target] , klikt u op **[!UICONTROL View in Analytics]** boven aan het rapport.

## Analyse en doel: Best practices voor zelfstudie analyse {#section_3438E6E77A464424B717A4FD333B84B2}

Open [&#x200B; Analytics &amp; Doel: Beste praktijken voor Analyse &#x200B;](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) leerprogramma, dat door [!DNL Adobe Experience League] wordt verstrekt.

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit onderwerp worden besproken.

### Analytics voor Adobe Target (A4T) (4 :32) ![&#x200B; de badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

In deze video wordt uitgelegd hoe u [!DNL Analytics] als rapporteringsbron in [!DNL Target] kunt gebruiken om de analyse van uw optimalisatieprogramma te bepalen.

* Verklaar wat A4T is en waarom u het zou gebruiken
* Uitleggen hoe A4T werkt
* Begrijp de eerste vereisten nodig alvorens A4T te gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics / de Integratie van Adobe Target (A4T) (40 :33) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video is een opname van &quot; [&#x200B; Uren van het Bureau &#x200B;](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7),&quot;een initiatief dat door het team van de Zorg van de Klant van Adobe wordt geleid.

* Hoe te opstelling en te bevestigen dat de integratie werkt
* Hoe de integratie werkt
* Meer informatie over de ideale rapporten die u kunt gebruiken in Analytics
* Antwoorden op algemene vragen over A4T

[&#x200B; de Uren van het Bureau van de Integratie van Analytics/van het Doel (A4T) &#x200B;](https://helpx.adobe.com/nl/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [&#x200B; Analytics voor  [!DNL Target]  implementatie &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md): Bevat implementatieinformatie voor at.js en het Web SDK van het Platform.
>* [&#x200B; Redirect aanbiedingen - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
>* [&#x200B; wat SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=nl-NL) is: Bevat overzichtsinformatie over het Web SDK van het Platform.
>* [&#x200B; overzicht van het Doel &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html?lang=nl-NL): Bevat informatie specifiek voor [!DNL Target] en [!DNL Platform Web SDK].
