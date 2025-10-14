---
keywords: activiteit montages;A/B doelstellingen en montages;het melden van montages;doel metriek;succesmetriek;afhankelijke succesmetriek;geavanceerde montages;primair doel;extra metriek;doelstelling;duur;het melden van oplossing;doel;publiek voor het melden;Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen;Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet;nota's
description: Leer hoe u de pagina [!UICONTROL Goals and Settings] gebruikt om informatie op te geven over de doelen van een A/B-activiteit.
title: Hoe specificeer ik Doelstellingen en Montages in a  [!DNL Target]  Activiteit A/B?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 0%

---

# Doelstellingen en instellingen

Op de pagina [!UICONTROL Goals & Settings] in [!DNL Adobe Target] geeft u informatie op over de doelen van de activiteit.

De beschikbare montages hangen af van of u Doel of [&#x200B; Analytics &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) als rapporteringsbron gebruikt.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

In het gedeelte [!UICONTROL Activity Settings] van de pagina [!UICONTROL Goals & Settings] kunt u de volgende opties configureren:

| Instellingen | Beschrijving |
|--- |--- |
| [!UICONTROL Objective] | Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de activiteit identificeren. |
| [!UICONTROL Priority] | Afhankelijk van uw instellingen variëren de [!DNL Target] interface en de opties voor [!UICONTROL Priority] . U kunt de oudere instellingen van [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] gebruiken of u kunt fijngeoriënteerde prioriteiten van 0 tot en met 999 inschakelen.<P>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<P>Als deze optie niet is ingeschakeld in [!UICONTROL Administration] (de standaardinstelling), geeft u een prioriteit op: [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] .<P>Om [&#x200B; fijnkorrelige prioriteiten &#x200B;](/help/main/administrating-target/reporting.md) toe te laten, klik [!UICONTROL Administration] > [!UICONTROL Reporting], dan knevel de [!UICONTROL Enable Fine-Grained Priorities] optie aan &quot;aan&quot;positie. <P>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999: 0 = [!UICONTROL Low] en 999 = [!UICONTROL High] . <P>Voor activiteiten die in vorige versies van [!DNL Target] zijn gemaakt, wordt [!UICONTROL Low] priority omgezet in 0, [!UICONTROL Medium] in 5 en wordt [!UICONTROL High] omgezet in 10. U kunt deze waarden desgewenst aanpassen.<P>Opmerking: voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld. |
| Duur | De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdplukker gebruikt een klok van 24 uur, met 00 :00 die middernacht zijn. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

In het gedeelte [!UICONTROL Reporting Settings] van de pagina [!UICONTROL Goals & Settings] kunt u de volgende opties configureren:

| Instellingen | Beschrijving |
|--- |--- |
| [!UICONTROL Reporting Source] | Geef op welke oplossingsgegevens worden verzameld:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Als een rapporteringsbron in uw [&#x200B; rekeningsmontages &#x200B;](/help/main/administrating-target/reporting.md) wordt gespecificeerd, wordt de gespecificeerde bron gebruikt en dit het plaatsen is niet zichtbaar.<P>U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.<P>**Adobe Analytics**: Zie [&#x200B; Adobe Analytics als Rapporterende Source voor Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) om over de verschillen tussen de rapporteringsoplossingen en de voordelen van elk te leren. Wanneer u [!DNL Analytics] selecteert als de rapportbron voor [!DNL Target] , selecteert u een [!DNL Analytics] -rapportsuite die [!DNL Target] activiteitsgegevens ontvangt.<P>Als u een rapportbron wilt opgeven, kiest u eerst een van de [!DNL Analytics] -bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Adobe Target] zijn beschikbaar voor selectie. Als u de rapportsuites niet ziet die u verwacht, probeer eerst het programma openen en opnieuw binnen aan [!DNL Adobe Experience Cloud] proberen opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met de klantenservice.<P><P>**Adobe Customer Journey Analytics**: Zie [[!DNL Target]  rapporterend in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) voor meer informatie over de integratie tussen [!DNL Adobe Customer Journey Analytics] en [!DNL Target].<P>[!DNL Target] reporting in [!DNL Customer Journey Analytics] wordt ondersteund in A/B-activiteiten met handmatige verkeerssplitsing. [!UICONTROL Auto-Target] en [!UICONTROL Auto-Allocate] A/B-activiteiten kunnen geen [!DNL Target] -rapportage gebruiken in [!DNL Customer Journey Analytics] . |
| [!UICONTROL Goal Metric] | Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een metrische waarde [!UICONTROL Conversion] en stel vervolgens de parameters in die bepalen wanneer succes wordt geboekt. Voor meer informatie over het plaatsen van metriek, zie [&#x200B; Reeks Metriek &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Opmerking: als de rapportoplossing is ingesteld op [!DNL Analytics] , is [!UICONTROL Conversion] de enige beschikbare meeteenheid voor het doel. [!DNL Analytics] metriek kan niet als doel worden geselecteerd. Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de succesmetrische gegevens te kiezen.<P>Als deze optie is ingeschakeld, biedt het veld [!UICONTROL Estimated Value of the Conversion] (niet beschikbaar voor de [!UICONTROL Page Score] -meetgegevens) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan [!DNL Target] een geschatte lift in inkomsten berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), gebruikt de schatting [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency.<P>Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Dit is anders dan het standaardgedrag in [!DNL Target Classic] , dat bezoekers als nieuw beschouwt als ze de activiteit opnieuw zien. |
| [!UICONTROL Additional Metrics] | Maak aanvullende succeswaarden. Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op [!DNL Analytics] . In dit geval worden de maatstaven die voor de rapportsuite [!DNL Analytics] zijn gedefinieerd, toegepast. |
| [!UICONTROL Audiences for Reporting] | Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportpubliek toevoegen om informatie over slechts specifieke doelgroepen te tonen. Deze instelling is niet beschikbaar als u [!DNL Analytics] als rapportoplossing kiest. Het publiek dat voor de [!DNL Analytics] rapportsuite is gedefinieerd, wordt toegepast. |

## Geavanceerde instellingen {#section_E2FE441AFB324E498793ABB025ED9974}

In het gedeelte [!UICONTROL Advanced Settings] van de pagina [!UICONTROL Goals & Settings] kunt u de volgende opties configureren:

Als u geavanceerde instellingen wilt opgeven, klikt u op het pictogram **[!UICONTROL More]** (de verticale ellips) en vervolgens op **[!UICONTROL Advanced Settings]** , zoals in de volgende afbeelding wordt getoond.

![&#x200B; Geavanceerde het menu van Montages &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron gebruikt, worden de instellingen beheerd door de [!DNL Analytics] -server. De optie Geavanceerde instellingen is niet beschikbaar.

![&#x200B; Geavanceerde Montages &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Instelling | Beschrijving |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | Gebruik deze optie om slechts iemand te tellen zoals het bereiken van metrisch succes als zij eerder een verschillend succes metrisch hebben bereikt. Een activiteitconversie is bijvoorbeeld alleen geldig als de bezoeker op het aanbod klikt of een bepaalde pagina bereikt voordat de conversie plaatsvindt. U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen. Definieer beide (of meerdere) succeswaarden voordat u de ene afhankelijk van de andere kunt maken. Met de optie [!UICONTROL Add Dependency] kan de metrische waarde met succes worden verhoogd als een andere maatstaf met succes is bereikt of niet is bereikt. Een afhankelijkheid toevoegen:<ul><li>Klik op [!UICONTROL Advanced Settings] nadat u aanvullende metriek hebt toegevoegd.</li><li>Klik op de optie [!UICONTROL Add Dependency] :</li><li>Sleep de gewenste metriek van de linkerruit in de juiste ruit, dan klik [!UICONTROL Reached] om het plaatsen tussen [!UICONTROL Reached] en [!UICONTROL &#x200B; Not Reached] van een knevel te voorzien.</li><li>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:<ul><li>Selecteer [!UICONTROL Increment Count & Keep User in Activity] om op te geven hoe het aantal wordt verhoogd.</li><li>Selecteer [!UICONTROL Increment Count, Release User & Allow Reentry] om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.</li><li>Selecteer [!UICONTROL Increment Count, Release User & Bar from Reentry] om op te geven wat de gebruiker ziet in plaats van de inhoud van de activiteit.</li></ul> |
| [!UICONTROL How will the count be incremented?] | Er zijn drie opties voor de verhoging van het aantal:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

Zie [&#x200B; Metriek van het Succes &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde montages.

## Andere metagegevens {#section_2E8917BEFB954480A4206B9E9E917F80}

In de sectie [!UICONTROL Other Metadata] van de pagina [!UICONTROL Goals & Settings] kunt u alle informatie over uw activiteiten opgeven die nuttig is om voor uzelf of andere teamleden beschikbaar te houden. U kunt het formaat van het deelvenster Notities wijzigen.|

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### De Montages van de activiteit (3 :02) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

https://video.tv.adobe.com/v/17381)

### Creërend A/B Tests (8 :36) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

In deze video ziet u hoe de instellingen voor activiteit passen in de driestappenworkflow met instructies bij het maken van een activiteit. De doelstellingen en de montages worden besproken begin bij 5 :30.

* A/B-activiteit maken in Adobe Target
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
