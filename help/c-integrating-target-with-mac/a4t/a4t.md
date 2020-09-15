---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe "Analytics for Target" (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van metriek en publiekssegmenten voor analytische conversie. Dankzij deze integratie kunt u analyserapporten gebruiken om uw resultaten te bekijken. Als u Analytics als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op de gegevensinzameling van de Analyse.
title: Adobe Analytics als bron van rapportage voor Adobe Target (A4T)
feature: a4t general
subtopic: Integrating
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: b69a34023466fa2e348ed77ee41bc1cfdeb4e6ab
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---


# Adobe Analytics als bron van rapportage voor Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

[!DNL Adobe Analytics for Target] (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van [!DNL Analytics] conversiemetriek en publiekssegmenten. Met de integratie A4T kunt u rapporten gebruiken om uw resultaten te bekijken. [!DNL Analytics] Als u [!DNL Analytics] als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op [!DNL Analytics] gegevensinzameling.

## A4T-overzicht {#section_92B66069210C40DBA937790E8CC596CF}

De [!DNL Analytics for Target] integratie tussen [!DNL Analytics] en [!DNL Target] verstrekt krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma.

De drie belangrijkste voordelen van het gebruik van [!DNL Analytics] gegevens in [!DNL Target] zijn:

* Marketers kunnen op elk gewenst moment dynamisch [!DNL Analytics] succesmaatstaven of rapportsegmenten toepassen op [!DNL Target] activiteitenrapporten. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Eén gegevensbron voorkomt de variantie die optreedt wanneer gegevens in twee afzonderlijke systemen worden verzameld.
* Met uw bestaande [!DNL Analytics] implementatie worden alle vereiste gegevens verzameld. Het is niet nodig vakken op pagina&#39;s te implementeren om alleen gegevens voor rapporten te verzamelen. Hoewel, wordt het nog geadviseerd dat u een doos van de orderbevestiging voor de activiteiten van [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) uitvoert.

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen dat uw account wordt ingericht voor de integratie. Gebruik [dit formulier](https://www.adobe.com/go/audiences) om provisioning aan te vragen.
>
>De integratie die [!DNL Analytics] als gegevensbron voor [!DNL Target] (A4T) toelaat vertegenwoordigt de volgende generatie van Test&amp;Target aan stop-in SiteCatalyst. Deze plug-in is vervangen, maar wordt nog steeds ondersteund door klanten die deze al gebruiken.

Als u [!DNL Analytics] als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op [!DNL Analytics].

Alle [!DNL Analytics] metriek, met inbegrip van berekende metriek, zijn beschikbaar in [!DNL Target] en het [!UICONTROL Target Activities] rapport in [!DNL Analytics]. Evenzo, kan om het even welk segment beschikbaar in [!DNL Analytics] worden toegepast op beide oplossingen. U kunt metrisch of publiek op het rapport binnen toepassen [!DNL Target] nadat de activiteit is begonnen, of zelfs nadat de activiteit heeft voltooid.

Elke metrische waarde is inbegrepen, met inbegrip van om het even welke klant of berekende metriek die ingebouwde [!DNL Analytics].

Na de rubriceringsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

Houd rekening met de volgende punten wanneer u overweegt A4T te gebruiken:

* Om als rapporteringsbron voor te gebruiken [!DNL Analytics] , zowel moet u als uw bedrijf toegang tot [!DNL Target]en tot [!DNL Analytics] [!DNL Target]. [Neem contact op met uw accountvertegenwoordiger](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) als u een van beide oplossingen nodig hebt.
* De bron van de rapportage wordt voor elke activiteit ingesteld. [!DNL Target] gegevens blijven verzamelen die kunnen worden gebruikt voor rapportage en [!DNL Target] gegevens zijn nog steeds beschikbaar als u een activiteit liever baseert op gegevens die zijn verzameld door [!DNL Target].
* U moet de ene of de andere rapportbron gebruiken. U kunt geen gegevens verzamelen voor één activiteit uit beide bronnen.
* Wanneer het gebruiken van A4T, zijn alle succesmetriek beschikbaar aan uw activiteiten [!DNL Analytics] metriek. Nochtans, kan uw doel metrisch op een mbox vraag worden gebaseerd. Bijvoorbeeld, kunt u de uit-van-de-doos klikvolgende mogelijkheden van het Doel met A4T in plaats van het moeten [!DNL Analytics] klik-volgcode uitvoeren.
* Wanneer het bekijken van het melden van een activiteit A4T in [!DNL Target] UI, bekijkt u [!DNL Analytics] gegevens. Bijvoorbeeld, als u [!UICONTROL Visitor] metrisch binnen gebruikt [!DNL Target], gebruikt u [!DNL Analytics] [!UICONTROL Visitor] metrisch, niet [!DNL Target] metrisch, die nu wordt genoemd [!UICONTROL Visitors] [!UICONTROL Entrants]. Dit verschil is vooral belangrijk voor basisverkeersmetriek ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) en omzettingsmetriek.
* Bestaande [!DNL Target] activiteiten blijven gebruikmaken van [!DNL Target] gegevensverzameling en worden niet beïnvloed door het inschakelen van A4T.
* Slechts één op doos-gebaseerde metrisch wordt toegestaan wanneer het gebruiken [!DNL Analytics] als rapporteringsbron.
* Een server-aan-server vraag van [!DNL Target] naar [!DNL Analytics] verzendt activiteit en ervaringsinformatie naar [!DNL Analytics]. Deze integratie resulteert niet in extra servervraag naar of [!DNL Target] of [!DNL Analytics].

   In sommige situaties, zou de classificatievraag van [!DNL Target] aan [!DNL Analytics] kunnen ontbreken en de activiteiten tonen geen gegevens in [!DNL Analytics]. Als dit gebeurt, zie [Problemen oplossen met de integratie Analytics en Target (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). U kunt ook [contact opnemen met de klantenservice](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) voor verdere hulp.

## Ondersteunde activiteitstypen {#section_F487896214BF4803AF78C552EF1669AA}

In de volgende tabel wordt aangegeven welke typen activiteiten worden ondersteund [!DNL Analytics] als de rapportbron in [!DNL Target] (A4T):

| Activiteitstypen | A4T-compatibel? | Opmerkingen, indien van toepassing |
|--- |--- |--- |
| A/B-activiteit met handmatige verkeersverdeling | Ja |  |
| A/B-activiteit met automatisch toewijzen | Ja | Zie [Analytics voor de steun van het Doel (A4T) voor auto-Wijs en auto-Doel activiteiten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| A/B activiteit met AutoTarget | Ja | Zie [Analytics voor de steun van het Doel (A4T) voor auto-Wijs en auto-Doel activiteiten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| Gericht op ervaring (XT) | Ja |  |
| MVT (Multivariate Test) | Ja | Vereist op box-Gebaseerd doel metrisch doel om het [!UICONTROL Element Contribution] rapport te krijgen.  Het [!UICONTROL Element Contribution] rapport ondersteunt momenteel geen [!DNL Analytics] metriek. |
| Automated Personalization (AP)-activiteit | Nee |  |
| Recommendations-activiteit | Ja |  |
| Mobiele app | Ja | Ondersteund met de SDK voor mobiele services, versie 4.13.1 of hoger.  Raadpleeg de documentatie bij [Mobiele services voor meer informatie](https://docs.adobe.com/content/help/en/mobile-services/using/home.html). |
| E-mail | Nee |  |
| Server Side Delivery-API | Ja | Zie [Serverzijde voor meer informatie: Doel](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)implementeren. |
| NodeJS SDK | Ja | Zie [Serverzijde voor meer informatie: Doel](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)implementeren. |
| AEM 6.1 (of vroeger) de Integratie van de Cloud Service | Nee |  |
| AEM 6.2 (of later) de Integratie van de Cloud Service | Ja | Zie [Integratie met Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in de documentatie van [!DNL Adobe Experience Manager] 6.2 voor meer informatie. |
| Elke activiteit die een omleidingsaanbieding gebruikt | Ja | Er zijn strengere minimumeisen voor het gebruik van omleidingsaanbiedingen met A4T. Zie Aanbiedingen [omleiden - A4T Veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)voor meer informatie. |
| Node.JS | Ja |  |

Omdat alle activiteitstypen A4T nog niet ondersteunen, wordt u aangeraden belangrijke conversievakken, zoals het `orderConfirmPage` mbox, te behouden of te implementeren.

## Voorbeelden van A4T-rapporten {#section_F0A43A1CB2F04E8282B909E4D7034361}

Om A4T rapporten binnen te bekijken [!DNL Target], klik **[!UICONTROL Activities]**, klik de gewenste activiteit van de lijst die [!DNL Analytics] als zijn rapporteringsbron gebruikt, dan klik de **[!UICONTROL Reports]** tabel.

>[!NOTE]
>
>U kunt de [!UICONTROL Reporting Source] drop-down lijst bij de bovenkant van de [!UICONTROL Activities] pagina gebruiken om slechts activiteiten te tonen die [!DNL Analytics] als rapporteringsbron gebruiken.

U kunt tussen de [!UICONTROL Table View] en [!UICONTROL Graph View] van het rapport schakelen door op het juiste pictogram rechtsboven in het rapport te klikken.

De volgende illustratie toont de [!UICONTROL Graph View] van een rapport A4T met de [!UICONTROL Report Metric] drop-down lijst die de beschikbare [!DNL Analytics] doelmetriek toont:

![](assets/a4t_report_graph1.png)

De volgende afbeelding toont de [!UICONTROL Graph View] vorm van een A4T-rapport met de [!UICONTROL Audience] vervolgkeuzelijst waarin het beschikbare [!DNL Analytics] publiek wordt weergegeven:

![](assets/a4t_report_graph2.png)

In de volgende afbeelding wordt de [!UICONTROL Table View] vorm van een A4T-rapport getoond:

![](assets/a4t_report_table.png)

Als u het rapport wilt weergeven in [!DNL Analytics] plaats van in [!DNL Target], klikt u **[!UICONTROL View in Analytics]** boven aan het rapport.

## Analyse en doel: Best practices voor zelfstudie analyse {#section_3438E6E77A464424B717A4FD333B84B2}

Open de [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, verstrekt door [!DNL Adobe Experience League].

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit onderwerp worden besproken.

### Analytics for Target (A4T) (4:32) ![Overview badge](/help/assets/overview.png)

In deze video wordt uitgelegd hoe u [!DNL Analytics] als rapporteringsbron kunt gebruiken [!DNL Target] om de analyse van uw optimalisatieprogramma te bepalen.

* Verklaar wat A4T is en waarom u het zou gebruiken
* Uitleggen hoe A4T werkt
* Begrijp de eerste vereisten nodig alvorens A4T te gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Zelfstudie voor Analytics / Target Integration (A4T) (40:33) ![](/help/assets/tutorial.png)

Deze video is een opname van &quot; [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot;, een initiatief van het team van de klantenservice van Adobe.

* Hoe te opstelling en te bevestigen dat de integratie werkt
* Hoe de integratie werkt
* Meer informatie over de ideale rapporten die u kunt gebruiken in Analytics
* Antwoorden op algemene vragen over A4T

[Kantooruren voor Analytics/Target Integration (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)