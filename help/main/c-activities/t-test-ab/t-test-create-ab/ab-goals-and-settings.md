---
keywords: activiteit montages;A/B doelstellingen en montages;het melden van montages;doel metriek;succesmetriek;afhankelijke succesmetriek;geavanceerde montages;primair doel;extra metriek;doelstelling;duur;het melden van oplossing;doel;publiek voor het melden;Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen;Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet;nota's
description: Leer hoe u de [!UICONTROL Goals and Settings] pagina in [!DNL Adobe Target] om informatie over de doelstellingen van een A/B-activiteit te specificeren.
title: Hoe kan ik doelen en instellingen opgeven in een [!DNL Target] A/B-activiteit?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 0%

---

# Doelstellingen en instellingen

De [!UICONTROL Goals & Settings] pagina in [!DNL Adobe Target] Hier geeft u informatie op over de doelen van de activiteit.

Welke instellingen beschikbaar zijn, is afhankelijk van het feit of u Target gebruikt of [Analyse](/help/main/c-integrating-target-with-mac/a4t/a4t.md) als de bron van de rapportage.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

De [!UICONTROL Activity Settings] van de [!UICONTROL Goals & Settings] Met deze pagina kunt u de volgende opties configureren:

| Instellingen | Beschrijving |
|--- |--- |
| [!UICONTROL Objective] | Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de activiteit identificeren. |
| [!UICONTROL Priority] | Afhankelijk van uw instellingen worden [!DNL Target] UI en opties voor [!UICONTROL Priority] variëren. U kunt de oudere instellingen van [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High]of u kunt fijnkorrelige prioriteiten inschakelen van 0 tot en met 999.<P>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<P>Als deze optie niet is ingeschakeld in [!UICONTROL Administration] (standaard) geeft u een prioriteit op: [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High].<P>Inschakelen [fijnkorrelige prioriteiten](/help/main/administrating-target/reporting.md), klikt u op [!UICONTROL Administration] > [!UICONTROL Reporting]en schakelt u vervolgens de [!UICONTROL Enable Fine-Grained Priorities] aan de positie &quot;Aan&quot;. <P>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999: 0 = [!UICONTROL Low] en 999 = [!UICONTROL High]. <P>Voor activiteiten die in vorige versies van [!DNL Target], [!UICONTROL Low] prioriteit wordt omgezet in 0, [!UICONTROL Medium] wordt omgezet in 5, en [!UICONTROL High] wordt omgezet in 10. U kunt deze waarden desgewenst aanpassen.<P>Opmerking: voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld. |
| Duur | De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdkiezer gebruikt een 24-uurs klok, waarbij 00:00 middernacht is. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

De [!UICONTROL Reporting Settings] van de [!UICONTROL Goals & Settings] Met deze pagina kunt u de volgende opties configureren:

| Instellingen | Beschrijving |
|--- |--- |
| [!UICONTROL Reporting Source] | Opgeven of gegevens moeten worden verzameld [!DNL Adobe Target] of van [!DNL Adobe Analytics]. Zie [Adobe Analytics als rapportbron voor Doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) kennis te nemen van de verschillen tussen de rapporteringsoplossingen en de voordelen van beide. Als u [!DNL Analytics] als bron van rapportage voor [!DNL Target]selecteert u een [!DNL Analytics] te ontvangen rapportsuite [!DNL Target] activiteitsgegevens.<P>Als u een rapportbron wilt opgeven, kiest u eerst een van de volgende opties [!DNL Analytics] bedrijven waaraan uw account is gekoppeld, en selecteer vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Adobe Target] zijn beschikbaar voor selectie. Als u niet de rapportsuites ziet die u verwacht, probeer eerst het registreren uit en het registreren terug aan [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met de klantenservice.<P>Als een rapportbron is opgegeven in uw accountinstellingen, wordt de opgegeven bron gebruikt en is deze instelling niet zichtbaar.<P>Opmerking: u kunt de rapportbron niet wijzigen nadat de activiteit actief is geworden om rapporten consistent te houden. |
| [!UICONTROL Goal Metric] | Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] metrisch, dan plaats de parameters die bepalen wanneer het succes wordt bereikt. Voor meer informatie over het plaatsen van metriek, zie [Metrisch instellen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Opmerking: als de rapportoplossing is ingesteld op [!DNL Analytics], de enige beschikbare doelstelling metrisch is [!UICONTROL Conversion]. [!DNL Analytics] metriek kan niet als doel worden geselecteerd. Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de succesmetrische gegevens te kiezen.<P>Indien ingeschakeld, wordt de [!UICONTROL Estimated Value of the Conversion] veld (niet beschikbaar voor de [!UICONTROL Page Score] metriek) verstrekt een waarde voor uw doel, maar niet voor andere metriek. Deze waarde schakelt [!DNL Target] een geraamde verhoging van de inkomsten te berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency.<P>Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Dit verschilt van het standaardgedrag in [!DNL Target Classic], die bezoekers als nieuw beschouwt als ze de activiteit weer zien. |
| [!UICONTROL Additional Metrics] | Maak aanvullende succeswaarden. Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op [!DNL Analytics]. In dit geval worden de maatstaven voor de [!DNL Analytics] rapportsuite wordt toegepast. |
| [!UICONTROL Audiences for Reporting] | Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportpubliek toevoegen om informatie over slechts specifieke doelgroepen te tonen. Deze instelling is niet beschikbaar als u [!DNL Analytics] als uw rapportoplossing. Het publiek dat is gedefinieerd voor de [!DNL Analytics] rapportsuite is toegepast. |

## Geavanceerde instellingen {#section_E2FE441AFB324E498793ABB025ED9974}

De [!UICONTROL Advanced Settings] van de [!UICONTROL Goals & Settings] Met deze pagina kunt u de volgende opties configureren:

Klik op de knop **[!UICONTROL More]** pictogram (de verticale ellips) en klik vervolgens op **[!UICONTROL Advanced Settings]**, zoals in de volgende afbeelding wordt getoond.

![Het menu Geavanceerde instellingen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als uw rapporteringsbron, worden de montages beheerd door [!DNL Analytics] server. De optie Geavanceerde instellingen is niet beschikbaar.

![Geavanceerde instellingen](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Instelling | Beschrijving |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | Gebruik deze optie om slechts iemand te tellen zoals het bereiken van metrisch succes als zij eerder een verschillend succes metrisch hebben bereikt. Een activiteitconversie is bijvoorbeeld alleen geldig als de bezoeker op het aanbod klikt of een bepaalde pagina bereikt voordat de conversie plaatsvindt. U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen. Definieer beide (of meerdere) succeswaarden voordat u de ene afhankelijk van de andere kunt maken. De [!UICONTROL Add Dependency] optie staat succesmetrisch toe om te verhogen als een ander succes metrisch is bereikt of niet bereikt. Een afhankelijkheid toevoegen:<ul><li>Klik op [!UICONTROL Advanced Settings].</li><li>Klik op de knop [!UICONTROL Add Dependency] optie:</li><li>Sleep de gewenste metriek vanuit het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op [!UICONTROL Reached] om de instelling tussen [!UICONTROL Reached] en[!UICONTROL  Not Reached].</li><li>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:<ul><li>Selecteren [!UICONTROL Increment Count & Keep User in Activity] om op te geven hoe het aantal wordt verhoogd.</li><li>Selecteren [!UICONTROL Increment Count, Release User & Allow Reentry] om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.</li><li>Selecteren [!UICONTROL Increment Count, Release User & Bar from Reentry] om op te geven wat de gebruiker te zien krijgt in plaats van de inhoud van de activiteit.</li></ul> |
| [!UICONTROL How will the count be incremented?] | Er zijn drie opties voor de verhoging van het aantal:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

Zie [Succeswaarden](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde instellingen.

## Andere metagegevens {#section_2E8917BEFB954480A4206B9E9E917F80}

De [!UICONTROL Other Metadata] van de [!UICONTROL Goals & Settings] op de pagina kunt u alle informatie over uw activiteiten opgeven die nuttig is om voor uzelf of andere teamleden beschikbaar te houden. U kunt het formaat van het deelvenster Notities wijzigen.|

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Activiteitsinstellingen (3:02) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

https://video.tv.adobe.com/v/17381)

### A/B-tests maken (8:36) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

In deze video ziet u hoe de instellingen voor activiteit passen in de driestappenworkflow met instructies bij het maken van een activiteit. De doelstellingen en de montages worden besproken beginnend bij 5:30.

* A/B-activiteit maken in Adobe Target
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
