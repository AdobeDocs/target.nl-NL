---
keywords: a4t;analytics;analytics for target;analytics reporting source;adobe analytics as the reporting source for target
description: Adobe "Analytics for Target" (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van metriek en publiekssegmenten voor analytische conversie. Dankzij deze integratie kunt u analyserapporten gebruiken om uw resultaten te bekijken. Als u Analytics als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op de gegevensinzameling van de Analyse.
title: Adobe Analytics als bron van rapportage voor Adobe Target (A4T)
feature: a4t general
translation-type: tm+mt
source-git-commit: fe6826e25b2d7c66ab245492f610585d0f5b3d69
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 0%

---


# Adobe Analytics als bron van rapportage voor Adobe Target (A4T)

[!DNL Adobe Analytics for Target] (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van  [!DNL Analytics] conversiemetriek en publiekssegmenten. Met de integratie A4T kunt u [!DNL Analytics]-rapporten gebruiken om uw resultaten te bekijken. Als u [!DNL Analytics] als rapporteringsbron voor een activiteit gebruikt, is al rapportering en segmentatie voor die activiteit gebaseerd op [!DNL Analytics] gegevensinzameling.

## A4T-overzicht {#section_92B66069210C40DBA937790E8CC596CF}

De [!DNL Analytics for Target]-integratie tussen [!DNL Analytics] en [!DNL Target] biedt krachtige analyse- en tijdbesparingsgereedschappen voor uw optimalisatieprogramma.

De drie belangrijkste voordelen van het gebruik van [!DNL Analytics]-gegevens in [!DNL Target] zijn:

* Marktdeelnemers kunnen [!DNL Analytics] succesmaatstaven of rapportagesegmenten op elk gewenst moment dynamisch toepassen op activiteitenrapporten [!DNL Target]. U hoeft niet alles op te geven voordat u de activiteit uitvoert.
* Eén gegevensbron voorkomt de variantie die optreedt wanneer gegevens in twee afzonderlijke systemen worden verzameld.
* Uw bestaande [!DNL Analytics]-implementatie verzamelt alle vereiste gegevens. Het is niet nodig vakken op pagina&#39;s te implementeren om alleen gegevens voor rapporten te verzamelen. Hoewel, wordt het nog geadviseerd dat u een doos van de orderbevestiging voor [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten uitvoert.

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen dat uw account wordt ingericht voor de integratie. Gebruik [dit formulier](https://www.adobe.com/go/audiences) om provisioned te vragen.
>
>De integratie die [!DNL Analytics] als gegevensbron voor [!DNL Target] (A4T) toelaat vertegenwoordigt de volgende generatie van Test&amp;Target aan stop-in SiteCatalyst. Deze plug-in is vervangen, maar wordt nog steeds ondersteund door klanten die deze al gebruiken.

Als u [!DNL Analytics] als rapportagebron voor een activiteit gebruikt, is alle rapportage en segmentatie voor die activiteit gebaseerd op [!DNL Analytics].

Alle [!DNL Analytics] metriek, met inbegrip van berekende metriek, zijn beschikbaar in [!DNL Target] en [!UICONTROL Target Activities] rapport in [!DNL Analytics]. Evenzo kan elk segment dat beschikbaar is in [!DNL Analytics], worden toegepast op beide oplossingen. U kunt metrisch of publiek op het rapport in [!DNL Target] toepassen nadat de activiteit is begonnen, of zelfs nadat de activiteit heeft voltooid.

Elke maatstaf is inbegrepen, met inbegrip van om het even welke klant of berekende metriek die ingebouwde [!DNL Analytics] zijn.

Na de rubriceringsperiode worden in deze rapporten ongeveer een uur na de verzameling gegevens van de website weergegeven. Alle metriek, segmenten, en waarden in de rapporten komen uit de rapportreeks u selecteerde toen u opstelling de activiteit.

Houd rekening met de volgende punten wanneer u overweegt A4T te gebruiken:

* Als u [!DNL Analytics] als rapportagebron voor [!DNL Target] wilt gebruiken, moeten zowel u als uw bedrijf toegang hebben tot [!DNL Analytics] en [!DNL Target]. [Neem contact op met uw ](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) accountvertegenwoordiger als u een van beide oplossingen nodig hebt.
* De bron van de rapportage wordt voor elke activiteit ingesteld. [!DNL Target] gegevens blijven verzamelen die kunnen worden gebruikt voor rapportage en  [!DNL Target] gegevens zijn nog steeds beschikbaar als u een activiteit liever baseert op gegevens die zijn verzameld door  [!DNL Target].
* U moet de ene of de andere rapportbron gebruiken. U kunt geen gegevens verzamelen voor één activiteit uit beide bronnen.
* Wanneer het gebruiken van A4T, zijn alle succesmetriek beschikbaar aan uw activiteiten [!DNL Analytics] metriek. Nochtans, kan uw doel metrisch op een mbox vraag worden gebaseerd. Bijvoorbeeld, kunt u de uit-van-de-doos klik-volgende mogelijkheden van het Doel met A4T in plaats van het moeten [!DNL Analytics] klikvolgende code uitvoeren.
* Wanneer het bekijken van rapportering van een activiteit A4T in [!DNL Target] UI, bekijkt u [!DNL Analytics] gegevens. Als u bijvoorbeeld [!UICONTROL Visitor] metrisch in [!DNL Target] gebruikt, gebruikt u [!DNL Analytics] [!UICONTROL Visitor] metrisch, niet [!DNL Target] [!UICONTROL Visitors] metrisch, die nu [!UICONTROL Entrants] wordt genoemd. Dit verschil is vooral belangrijk voor elementaire verkeersmetriek ([!UICONTROL Visitors], [!UICONTROL Visits], [!UICONTROL Page Views]) en omzettingsmetriek.
* Eventuele bestaande [!DNL Target] activiteiten blijven gebruikmaken van [!DNL Target] gegevensverzameling en worden niet beïnvloed door het inschakelen van A4T.
* Bij het gebruik van [!DNL Analytics] als rapportagebron is slechts één metrische waarde op basis van een box toegestaan.
* Een server-aan-server vraag van [!DNL Target] aan [!DNL Analytics] verzendt activiteit en ervaringsinformatie naar [!DNL Analytics]. Deze integratie leidt niet tot extra serveraanroepen voor [!DNL Target] of [!DNL Analytics].

   In sommige situaties, zou de classificatievraag van [!DNL Target] aan [!DNL Analytics] kunnen ontbreken en de activiteiten tonen geen gegevens in [!DNL Analytics]. Als dit gebeurt, zie [Problemen met de integratie van Analytics en Target oplossen (A4T)](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md). U kunt ook [contact opnemen met de klantenservice](/help/cmp-resources-and-contact-information.md#concept_34A1CA16F2244D42930BB77846A5ABBB) voor verdere ondersteuning.

## Ondersteunde activiteitstypen {#section_F487896214BF4803AF78C552EF1669AA}

In de volgende tabel wordt aangegeven welke activiteitstypen [!DNL Analytics] als rapportagebron ondersteunen in [!DNL Target] (A4T):

| Activiteitstypen | A4T-compatibel? | Opmerkingen, indien van toepassing |
|--- |--- |--- |
| A/B-activiteit met handmatige verkeersverdeling | Ja |  |
| A/B-activiteit met automatisch toewijzen | Ja | Zie [Analytics for Target (A4T) support for Auto-Allocate and Auto-Target activities](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| A/B activiteit met AutoTarget | Ja | Zie [Analytics for Target (A4T) support for Auto-Allocate and Auto-Target activities](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa). |
| Gericht op ervaring (XT) | Ja |  |
| MVT (Multivariate Test) | Ja | Vereist op doos-gebaseerde doel metrische doelstelling om het [!UICONTROL Element Contribution] rapport te krijgen.  Het [!UICONTROL Element Contribution]-rapport biedt momenteel geen ondersteuning voor [!DNL Analytics]-meetgegevens. |
| Automated Personalization (AP)-activiteit | Nee |  |
| Recommendations-activiteit | Ja |  |
| Mobiele app | Ja | Ondersteund met de SDK voor mobiele services, versie 4.13.1 of hoger.  Raadpleeg de [documentatie over mobiele services](https://experienceleague.adobe.com/docs/mobile-services/using/home.html) voor meer informatie. |
| E-mail | Nee |  |
| Server Side Delivery-API | Ja | Zie [Server-zijde voor meer informatie: Doel implementeren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| NodeJS SDK | Ja | Zie [Server-zijde voor meer informatie: Doel implementeren](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md). |
| AEM 6.1 (of vroeger) de Integratie van de Cloud Service | Nee |  |
| AEM 6.2 (of later) de Integratie van de Cloud Service | Ja | Zie [Integreren met Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) in de [!DNL Adobe Experience Manager] 6.2-documentatie voor meer informatie. |
| Elke activiteit die een omleidingsaanbieding gebruikt | Ja | Er zijn strengere minimumeisen voor het gebruik van omleidingsaanbiedingen met A4T. Zie [Aanbiedingen omleiden - A4T veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) voor meer informatie. |
| Node.JS | Ja | Zie [Node.js SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/nodejs-sdk) in de handleiding *Adobe Target SDKs* voor meer informatie. |
| Java SDK | Ja | Zie [Java SDK](https://adobetarget-sdks.gitbook.io/docs/sdk-reference-guides/java-sdk) in de handleiding *Adobe Target* SDK&#39;s voor meer informatie. |

Omdat alle activiteitstypen A4T nog niet ondersteunen, wordt u aangeraden belangrijke conversievakken, zoals de mbox `orderConfirmPage`, te behouden of te implementeren.

## Voorbeelden van A4T-rapporten {#section_F0A43A1CB2F04E8282B909E4D7034361}

Om A4T rapporten in [!DNL Target] te bekijken, klik **[!UICONTROL Activities]**, klik de gewenste activiteit van de lijst die [!DNL Analytics] als zijn rapporteringsbron gebruikt, dan klik **[!UICONTROL Reports]** tabel.

>[!NOTE]
>
>U kunt de [!UICONTROL Reporting Source] drop-down lijst bij de bovenkant van [!UICONTROL Activities] pagina gebruiken om slechts activiteiten te tonen die [!DNL Analytics] als rapporteringsbron gebruiken.

U kunt tussen [!UICONTROL Table View] en [!UICONTROL Graph View] van het rapport van een knevel voorzien door het aangewezen pictogram bij de hoogste juiste kant van het rapport te klikken.

In de volgende afbeelding ziet u de [!UICONTROL Graph View] van een A4T-rapport met de vervolgkeuzelijst [!UICONTROL Report Metric] waarin de beschikbare [!DNL Analytics]-doelmeetgegevens worden weergegeven:

![](assets/a4t_report_graph1.png)

In de volgende afbeelding ziet u de [!UICONTROL Graph View] van een A4T-rapport met de vervolgkeuzelijst [!UICONTROL Audience] waarin het beschikbare [!DNL Analytics] publiek wordt weergegeven:

![](assets/a4t_report_graph2.png)

In de volgende afbeelding ziet u de [!UICONTROL Table View] van een A4T-rapport:

![](assets/a4t_report_table.png)

Als u het rapport wilt weergeven in [!DNL Analytics] in plaats van in [!DNL Target], klikt u op **[!UICONTROL View in Analytics]** boven aan het rapport.

## Analyse en doel: Best practices voor zelfstudie analyse {#section_3438E6E77A464424B717A4FD333B84B2}

Open [Analytics &amp; Target: Beste praktijken voor Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) zelfstudie, die door [!DNL Adobe Experience League] wordt verstrekt.

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit onderwerp worden besproken.

### Analytics for Target (A4T) (4:32) ![Overview badge](/help/assets/overview.png)

In deze video wordt uitgelegd hoe u [!DNL Analytics] kunt gebruiken als rapporteringsbron in [!DNL Target] om de analyse van uw optimalisatieprogramma te stimuleren.

* Verklaar wat A4T is en waarom u het zou gebruiken
* Uitleggen hoe A4T werkt
* Begrijp de eerste vereisten nodig alvorens A4T te gebruiken

>[!VIDEO](https://video.tv.adobe.com/v/17384)

### Analytics / Target Integration (A4T) (40:33) ![Tutorial badge](/help/assets/tutorial.png)

Deze video is een opname van &quot; [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot;, een initiatief onder leiding van het team van de klantenservice van Adobe.

* Hoe te opstelling en te bevestigen dat de integratie werkt
* Hoe de integratie werkt
* Meer informatie over de ideale rapporten die u kunt gebruiken in Analytics
* Antwoorden op algemene vragen over A4T

[Kantooruren voor Analytics/Target Integration (A4T)](https://helpx.adobe.com/customer-care-office-hours/target/analytics-target-A4T-integration.html)