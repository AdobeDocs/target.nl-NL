---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe "Analytics for Target" (A4T) is een integratie tussen oplossingen waarmee u activiteiten kunt maken op basis van de gegevens van de conversie van Analytics en publiekssegmenten. Dankzij deze integratie kunt u analyserapporten gebruiken om uw resultaten te bekijken. Als u Analytics als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op de gegevensinzameling van de Analyse.
title: Adobe Analytics als de rapportbron voor Adobe Target (A4T)
subtopic: Integrating
topic: Standard
uuid: 616798a6-1587-410f-9ac6-473beb39e3fc
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Adobe Analytics als de rapportbron voor Adobe Target (A4T){#adobe-analytics-as-the-reporting-source-for-adobe-target-a-t}

Adobe &quot;Analytics for Target&quot; (A4T) is een integratie tussen oplossingen waarmee u activiteiten kunt maken op basis van de gegevens van de conversie van Analytics en publiekssegmenten. Met de integratie A4T kunt u analyserapporten gebruiken om uw resultaten te bekijken. Als u Analytics als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op de gegevensinzameling van de Analyse.

## A4T-overzicht {#section_92B66069210C40DBA937790E8CC596CF}

De Analytics voor de integratie van het Doel tussen Analytics en Target verstrekt krachtige analyse en tijdbesparende hulpmiddelen voor uw optimaliseringsprogramma.

De drie belangrijkste voordelen van het gebruik van analysegegevens in Doel zijn:

* De handelaars kunnen Analytics succesmetriek of het melden van segmenten dynamisch toepassen op de activiteitenrapporten van het Doel op elk ogenblik. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Een enkele gegevensbron voorkomt de variantie die optreedt wanneer gegevens in twee afzonderlijke systemen worden verzameld.
* Met de bestaande Adobe Analytics-implementatie worden alle vereiste gegevens verzameld. Het is niet nodig vakken op pagina&#39;s te implementeren om alleen gegevens voor rapporten te verzamelen. Hoewel, wordt het nog geadviseerd dat u een doos van de orderbevestiging voor de Geautomatiseerde activiteiten van de Personalisatie (AP) uitvoert.

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen dat uw account wordt ingericht voor de integratie. Gebruik [dit formulier](https://www.adobe.com/go/audiences) om provisioning aan te vragen.
>
>De integratie die Adobe Analytics als gegevensbron voor Adobe Target (A4T) toelaat vertegenwoordigt de volgende generatie van de stop van Test&amp;Target aan SiteCatalyst. Deze plug-in is vervangen, maar wordt nog steeds ondersteund door klanten die deze al gebruiken.

Als u Analytics als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op Analytics.

Alle metriek van Analytics, met inbegrip van berekende metriek, zijn beschikbaar in Standaard/Premium van het Doel en het rapport van Activiteiten van het Doel in Analytics. Evenzo, kan om het even welk segment beschikbaar in Analytics op beide oplossingen worden toegepast. U kunt metrisch of publiek op het rapport in Standaard/Premium van het Doel toepassen nadat de test is begonnen, of zelfs nadat de test heeft voltooid.

Elke metrische waarde is inbegrepen, met inbegrip van om het even welke klant of berekende metriek die ingebouwde in Analytics zijn.

Na de rubriceringsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

Houd rekening met de volgende punten wanneer u overweegt A4T te gebruiken:

* Als u Adobe Analytics wilt gebruiken als rapportagebron voor Adobe Target, moeten zowel u als uw bedrijf toegang hebben tot Adobe Analytics en Adobe Target. [Neem contact op met uw accountvertegenwoordiger](../../cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) als u een van beide oplossingen nodig hebt.
* De bron van de rapportage wordt voor elke activiteit ingesteld. Doel blijft gegevens verzamelen die u wilt gebruiken in rapportage en doelgegevens zijn nog steeds beschikbaar als u een activiteit liever baseert op gegevens die door Doel zijn verzameld.
* U moet de ene of de andere rapportbron gebruiken. U kunt geen gegevens verzamelen voor één activiteit uit beide bronnen.
* Wanneer het gebruiken van A4T, zijn alle succesmetriek beschikbaar aan uw activiteiten Analytische metriek. Nochtans, kan uw doel metrisch op een mbox vraag worden gebaseerd. Bijvoorbeeld, kunt u de uit-van-de-doos klikvolgende mogelijkheden van het Doel met A4T in plaats van het moeten Analytics uitvoeren klik-volgende code.
* Wanneer het bekijken van het melden van een activiteit A4T in het Doel UI, bekijkt u de gegevens van Analytics. Bijvoorbeeld, als u metrisch van de Bezoeker in Doel gebruikt, gebruikt u metrisch van de Bezoeker van de Analyse, niet metrisch van de Bezoeker van het Doel, die nu wordt genoemd Entrants. Dit verschil is vooral belangrijk voor elementaire verkeersmetriek (Bezoekers, Bezoekingen, Paginaweergaven) en conversiemetriek.
* Eventuele bestaande doelactiviteiten blijven gebruikmaken van de gegevensverzameling Target en worden niet beïnvloed door het inschakelen van A4T.
* Slechts één op doos-gebaseerde metrisch wordt toegestaan wanneer het gebruiken van Analytics als rapporteringsbron.
* Een server-aan-server vraag van Doel naar Analytics verzendt activiteit en ervaringsinformatie naar Analytics. Deze integratie resulteert niet in extra servervraag naar of Doel of Analytics.

   In sommige situaties, zou de classificatievraag van Doel aan Analytics kunnen ontbreken en de activiteiten tonen geen gegevens in Analytics. Als dit gebeurt, zie [Problemen oplossen met de integratie Analytics en Target (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). U kunt ook [contact opnemen met de klantenservice](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) voor verdere hulp.

## Ondersteunde activiteitstypen {#section_F487896214BF4803AF78C552EF1669AA}

In de volgende tabel wordt aangegeven welke activiteitstypen Analytics als rapportbron ondersteunen (A4T):

| Activiteitstypen | A4T-compatibel? | Opmerkingen, indien van toepassing |
|--- |--- |--- |
| A/B-activiteit met handmatige verkeersverdeling | Ja |  |
| A/B-activiteit met automatisch toewijzen | Nee |  |
| A/B activiteit met AutoTarget | Nee |  |
| Gericht op ervaring (XT) | Ja |  |
| MVT (Multivariate Test) | Ja | Vereist op box-Gebaseerd doel metrisch doel om het rapport van de Bijdrage van het Element te krijgen.  Het Rapport Element Contribution biedt momenteel geen ondersteuning voor analytische gegevens. |
| Actie voor geautomatiseerde personalisatie (AP) | Nee |  |
| Activiteit aanbevelingen | Ja |  |
| Mobiele app | Ja | Ondersteund met de SDK voor mobiele services, versie 4.13.1 of hoger.  Raadpleeg de documentatie bij [Mobiele services voor meer informatie](https://docs.adobe.com/content/help/en/mobile-services/using/home.html). |
| E-mail | Nee |  |
| Server Side Delivery-API | Ja | Zie [Serverzijde voor meer informatie: Doel](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)implementeren. |
| NodeJS SDK | Ja | Zie [Serverzijde voor meer informatie: Doel](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md)implementeren. |
| AEM 6.1 (of eerder) Cloud Service Integration | Nee |  |
| AEM 6.2 (of hoger) Cloud Service Integration | Ja | Zie [Integratie met Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in de documentatie van Adobe Experience Manager 6.2 voor meer informatie. |
| Alle activiteiten via een omleidingsaanbieding | Ja | Er zijn strengere minimumeisen voor het gebruik van omleidingsaanbiedingen met A4T. Zie Aanbiedingen [omleiden - A4T Veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)voor meer informatie. |
| Node.JS | Ja |  |

Omdat alle activiteitstypen A4T nog niet ondersteunen, wordt u aangeraden belangrijke conversievakken te behouden of te implementeren, zoals het vak &quot;orderConfirmPage&quot;.

## Voorbeelden van A4T-rapporten {#section_F0A43A1CB2F04E8282B909E4D7034361}

Als u A4T-rapporten wilt weergeven in [!DNL Target], klikt u op **[!UICONTROL Activities]** de gewenste activiteit in de lijst die [!DNL Analytics] als rapportbron wordt gebruikt > en klikt u vervolgens op het **[!UICONTROL Reports]** tabblad.

>[!NOTE]
>
>U kunt de [!UICONTROL Reporting Source] drop-down lijst bij de bovenkant van de [!UICONTROL Activities] pagina gebruiken om slechts activiteiten te tonen die [!DNL Analytics] als rapporteringsbron gebruiken.

U kunt tussen de Mening van de Lijst en [!UICONTROL Graph View] van het rapport van een knevel voorzien door het aangewezen pictogram bij de hoogste juiste kant van het rapport te klikken.

De volgende illustratie toont de [!UICONTROL Graph View] van een rapport A4T met de [!UICONTROL Report Metric] drop-down lijst die de beschikbare [!DNL Analytics] doelmetriek toont:

![](assets/a4t_report_graph1.png)

De volgende afbeelding toont de [!UICONTROL Graph View] vorm van een A4T-rapport met de [!UICONTROL Audience] vervolgkeuzelijst waarin het beschikbare [!DNL Analytics] publiek wordt weergegeven:

![](assets/a4t_report_graph2.png)

In de volgende afbeelding wordt de [!UICONTROL Table View] vorm van een A4T-rapport getoond:

![](assets/a4t_report_table.png)

Als u het rapport wilt weergeven in [!DNL Analytics] plaats van in [!DNL Target], klikt u **[!UICONTROL View in Analytics]** boven aan het rapport.

## Analyse en doel: Best practices voor zelfstudie analyse {#section_3438E6E77A464424B717A4FD333B84B2}

Open de [Analytics &amp; Target: Best Practices for Analysis](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) tutorial, geleverd door Adobe Experience League.

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Analytics for Target (A4T) (4:32) ![Overview badge](/help/assets/overview.png)

In deze video wordt uitgelegd hoe u Adobe Analytics kunt gebruiken als rapporteringsbron in Adobe Target voor de analyse van uw optimalisatieprogramma.

* Verklaar wat A4T is en waarom u het zou gebruiken
* Uitleggen hoe A4T werkt
* Begrijp de eerste vereisten nodig alvorens A4T te gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics / Target Integration (A4T) (40:33) !![Tutorial badge](/help/assets/tutorial.png

Deze video is een opname van &quot; [Office Hours](../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot;, een initiatief van het team van de klantenservice van Adobe.

* Hoe te opstelling en te bevestigen dat de integratie werkt
* Hoe de integratie werkt
* Meer informatie over de ideale rapporten die u kunt gebruiken in Analytics
* Antwoorden op algemene vragen over A4T

[Kantooruren voor Analytics/Target Integration (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)