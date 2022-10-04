---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target;atjs;at.js;adobe Experience platform web sdk;platform web sdk;platform sdk
description: Gebruiken [!DNL Analytics] for [!DNL Target] (A4T) om activiteiten te creëren op basis van [!DNL Analytics] conversiemetriek en publiekssegmenten en gebruik [!DNL Analytics] verslagen om de resultaten te onderzoeken.
title: Wat is [!DNL Analytics] for [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: 5bb80b03-8209-4932-a838-0e11c5865133
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 0%

---

# [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T)

[!DNL Adobe Analytics for Target] (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van [!DNL Analytics] conversiemetriek en publiekssegmenten. De integratie A4T laat u gebruiken [!DNL Analytics] rapporten om uw resultaten te onderzoeken. Als u [!DNL Analytics] als bron van rapportage voor een activiteit, alle rapportage en segmentering voor die activiteit is gebaseerd op [!DNL Analytics] gegevensverzameling.

## Overzicht {#section_92B66069210C40DBA937790E8CC596CF}

De [!DNL Analytics for Target] integratie tussen [!DNL Analytics] en [!DNL Target] biedt krachtige hulpmiddelen voor analyse en tijdbesparend maken voor uw optimalisatieprogramma.

De drie belangrijkste voordelen van het gebruik [!DNL Analytics] gegevens in [!DNL Target] zijn:

* Marketers kunnen dynamisch toepassen [!DNL Analytics] succesmetriek of het melden van segmenten aan [!DNL Target] activiteitenverslagen op elk moment. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Eén gegevensbron voorkomt de variantie die optreedt wanneer gegevens in twee afzonderlijke systemen worden verzameld.
* Uw bestaande [!DNL Analytics] alle vereiste gegevens worden verzameld. Het is niet nodig vakken op pagina&#39;s te implementeren om alleen gegevens voor rapporten te verzamelen.

Als u [!DNL Analytics] als bron van rapportage voor een activiteit, alle rapportage en segmentering voor die activiteit is gebaseerd op [!DNL Analytics].

Alles [!DNL Analytics] metriek, inclusief berekende metriek, zijn beschikbaar in [!DNL Target] en de [!UICONTROL Target Activities] rapporteren in [!DNL Analytics], met één uitzondering. De berekende maatstaven voor [!UICONTROL Lift & Confidence] worden niet ondersteund. Ook elk segment dat beschikbaar is in [!DNL Analytics] kan op beide oplossingen worden toegepast. U kunt metrisch of publiek op het rapport in toepassen [!DNL Target] nadat de activiteit is gestart of zelfs nadat de activiteit is voltooid.

Elke metrisch is inbegrepen, met inbegrip van om het even welke douane of berekende metriek die ingebouwde zijn [!DNL Analytics].

Na de indelingsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

Houd rekening met de volgende punten wanneer u overweegt A4T te gebruiken:

* Te gebruiken [!DNL Analytics] als bron van rapportage voor [!DNL Target], zowel u als uw bedrijf moeten toegang hebben tot [!DNL Analytics] en [!DNL Target]. [Neem contact op met uw accountvertegenwoordiger](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) als u een van beide oplossingen nodig hebt.
* De bron van de rapportage wordt voor elke activiteit ingesteld. [!DNL Target] blijft gegevens verzamelen die bij de rapportage moeten worden gebruikt, en [!DNL Target] gegevens zijn nog steeds beschikbaar als u een activiteit liever baseert op gegevens die zijn verzameld door [!DNL Target].
* Gebruik één rapporteringsbron of andere. U kunt geen gegevens verzamelen voor één activiteit uit beide bronnen.
* Wanneer u A4T gebruikt, zijn alle succesmeetgegevens die beschikbaar zijn voor uw activiteiten [!DNL Analytics] metriek. Nochtans, kan uw doel metrisch worden gebaseerd op een mbox vraag als het gebruiken van at.js. Bijvoorbeeld, kunt u de uit-van-de-doos klikvolgende mogelijkheden van het Doel met A4T in plaats van het moeten uitvoeren [!DNL Analytics] code voor het bijhouden van klikken.
* Bij het weergeven van rapporten over een A4T-activiteit in de [!DNL Target] UI, u bekijkt [!DNL Analytics] gegevens. Als u bijvoorbeeld de opdracht [!UICONTROL Visitor] metrisch in [!DNL Target], gebruikt u de [!DNL Analytics] [!UICONTROL Visitor] metrisch, niet [!DNL Target] [!UICONTROL Visitors] metrisch, die nu wordt genoemd [!UICONTROL Entrants]. Dit verschil is vooral belangrijk voor basisverkeersmetriek ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) en conversiemetriek.
* Bestaande [!DNL Target] activiteiten blijven [!DNL Target] gegevensverzameling en worden niet beïnvloed door het inschakelen van A4T.
* Bij het gebruik van A4T is slechts één metrische waarde op basis van een doos toegestaan.
* Een server-aan-server vraag van [!DNL Target] tot [!DNL Analytics] verzendt activiteit en ervaringsinformatie naar [!DNL Analytics]. Deze integratie leidt niet tot extra serveraanroepen voor [!DNL Target] of [!DNL Analytics].

   In sommige gevallen worden de classificaties van [!DNL Target] tot [!DNL Analytics] mislukken en activiteiten geven geen gegevens weer in [!DNL Analytics]. Zie [Los de Analytics en integratie van het Doel (A4T) problemen op](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). U kunt ook [Contact opnemen met de klantenservice](/help/main/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) voor verdere bijstand.

## A4T implementeren

Voor informatie over het implementeren van A4T met at.js en de [!DNL Adobe Experience Platform Web SDK], zie [Analyses voor [!DNL Target] uitvoering](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Ondersteunde activiteitstypen {#section_F487896214BF4803AF78C552EF1669AA}

De volgende secties bevatten informatie over ondersteunde activiteitstypen wanneer u de [!DNL Adobe Experience Platform Web SDK] of at.js:

| Activiteitstypen | A4T-compatibel? | Opmerkingen, indien van toepassing |
|--- |--- |--- |
| [A/B-activiteit met handmatige verkeersverdeling](/help/main/c-activities/t-test-ab/test-ab.md) | Ja |  |
| [A/B-activiteit met automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Ja | Zie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) |
| [A/B activiteit met AutoTarget](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | Ja | Zie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md). |
| [Gericht op ervaring (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Ja |  |
| [MVT (Multivariate Test)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Ja | Vereist op mbox-Gebaseerd doel metrisch doel om te krijgen [!UICONTROL Element Contribution] verslag. De [!UICONTROL Element Contribution] rapport wordt momenteel niet ondersteund [!DNL Analytics] metriek. |
| [Automated Personalization (AP)-activiteit](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | Nee |  |
| [Recommendations-activiteit](/help/main/c-recommendations/recommendations.md) | Ja |  |
| [Elke activiteit die een omleidingsaanbieding gebruikt](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Ja |

Omdat alle activatypen nog geen A4T steunen, wordt het geadviseerd dat u belangrijke omzetvakjes houdt of uitvoert, zoals `orderConfirmPage` mbox.

## Voorbeelden van A4T-rapporten {#section_F0A43A1CB2F04E8282B909E4D7034361}

A4T-rapporten weergeven in [!DNL Target], klikt u op **[!UICONTROL Activities]**, klikt u op de gewenste activiteit in de lijst die [!DNL Analytics] als rapportbron klikt u op de knop **[!UICONTROL Reports]** tab.

>[!NOTE]
>
>U kunt de [!UICONTROL Reporting Source] vervolgkeuzelijst boven aan [!UICONTROL Activities] pagina om alleen activiteiten weer te geven die gebruikmaken van A4T.

U kunt schakelen tussen de [!UICONTROL Table View] en [!UICONTROL Graph View] van het rapport door op het juiste pictogram in de rechterbovenhoek van het rapport te klikken.

In de volgende afbeelding ziet u de [!UICONTROL Graph View] van een A4T-rapport met de [!UICONTROL Report Metric] vervolgkeuzelijst met de beschikbare [!DNL Analytics] meetgegevens doel:

![a4t_report_graph1-afbeelding](assets/a4t_report_graph1.png)

In de volgende afbeelding ziet u de [!UICONTROL Graph View] van een A4T-rapport met de [!UICONTROL Audience] vervolgkeuzelijst met de beschikbare [!DNL Analytics] publiek:

![a4t_report_graph2-afbeelding](assets/a4t_report_graph2.png)

In de volgende afbeelding ziet u de [!UICONTROL Table View] van een A4T-rapport:

![a4t_report_table-afbeelding](assets/a4t_report_table.png)

Als u het rapport wilt weergeven in [!DNL Analytics] eerder dan in [!DNL Target], klikt u op **[!UICONTROL View in Analytics]** boven aan het rapport.

## Analyse en doel: Best practices voor zelfstudie analyse {#section_3438E6E77A464424B717A4FD333B84B2}

Open de [Analyse en doel: Beste praktijken voor Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) zelfstudie, verstrekt door [!DNL Adobe Experience League].

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit onderwerp worden besproken.

### Analyses voor Adobe Target (A4T) (4:32) ![Overzicht badge](/help/main/assets/overview.png)

In deze video wordt uitgelegd hoe u deze video kunt gebruiken [!DNL Analytics] als bron van rapportage in [!DNL Target] om de analyse van uw optimalisatieprogramma te sturen.

* Verklaar wat A4T is en waarom u het zou gebruiken
* Uitleggen hoe A4T werkt
* Begrijp de eerste vereisten nodig alvorens A4T te gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics / Adobe Target Integration (A4T) (40:33) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video is een opname van &quot; [Kantooruren](/help/main/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7),&quot; een initiatief dat wordt geleid door het Adobe-team van de klantenservice.

* Hoe te opstelling en te bevestigen dat de integratie werkt
* Hoe de integratie werkt
* Meer informatie over de ideale rapporten die u kunt gebruiken in Analytics
* Antwoorden op algemene vragen over A4T

[Kantooruren voor Analytics/Target Integration (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)

>[!MORELIKETHIS]
>
>* [Analyses voor [!DNL Target] uitvoering](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md): Bevat implementatieinformatie voor at.js en het Web SDK van het Platform.
>* [Aanbiedingen omleiden - Veelgestelde vragen A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)
>* [Wat is Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html): Bevat overzichtsinformatie over het Web SDK van het Platform.
>* [Doeloverzicht](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html): Bevat specifieke informatie voor [!DNL Target] en de [!DNL Platform Web SDK].

