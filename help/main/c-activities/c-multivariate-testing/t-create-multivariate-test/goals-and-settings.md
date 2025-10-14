---
keywords: activiteitinstellingen;doelen en instellingen;variëren;mvt
description: Leer hoe te om de [!UICONTROL Goals & Settings] pagina in  [!DNL Adobe Target]  te gebruiken om informatie over de doelstellingen van a [!UICONTROL Multivariate Test] (MVT) activiteit te specificeren.
title: Hoe kan ik doelen en instellingen opgeven in een [!UICONTROL Multivariate Test] (MVT)-activiteit?
feature: Multivariate Tests
exl-id: 823a1435-ccb9-4357-9c33-a0968d704b7a
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 0%

---

# Doelstellingen en instellingen ([!UICONTROL Multivariate Test])

Op de pagina [!UICONTROL Goals & Settings] in [!DNL Adobe Target] voert u informatie in over de doelen van uw [!UICONTROL Multivariate Test] -activiteiten (MVT).

De volgende secties zijn beschikbaar:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

De beschikbare instellingen in elke sectie zijn afhankelijk van het feit of u [!DNL Target] of [!DNL Analytics] als bron voor rapportage gebruikt.

## Activiteiteninstellingen {#section_DCBDC354261F420EBD4B43EA34947BAC}

De volgende instellingen zijn beschikbaar:

### Doelstelling

Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de campagne identificeren.

### Prioriteit

Afhankelijk van uw instellingen variëren de [!DNL Target] interface en de opties voor [!UICONTROL Priority] . U kunt de oudere instellingen van [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] gebruiken of u kunt fijngeoriënteerde prioriteiten van 0 tot en met 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.

Als deze optie niet is ingeschakeld in [!UICONTROL Administration] > [!UICONTROL Reporting] (de standaardinstelling), geeft u een prioriteit op: [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] .

Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op [!UICONTROL Administration] > [!UICONTROL Reporting] en schakelt u de optie [!UICONTROL Enable Fine-Grained Priorities] in op de positie &quot;Aan&quot;.

Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:

* 0 = Laag
* 999 = Hoog

Voor activiteiten die in vorige versies van [!DNL Target] zijn gemaakt, wordt [!UICONTROL Low] priority omgezet in 0, [!UICONTROL Medium] priority wordt omgezet in 5 en [!UICONTROL High] priority wordt omgezet in 10. U kunt deze waarden desgewenst aanpassen.

>[!NOTE]
>
>Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld.

### Duur

De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdplukker gebruikt een klok van 24 uur, met 00 :00 die middernacht zijn. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw.

## Rapportinstellingen {#section_13119392051044FBA6387D9B3B1C43CF}

De volgende instellingen zijn beschikbaar:

### Rapporterende Source

Geef op welke oplossingsgegevens worden verzameld:

* [!DNL Adobe Target]
* [!DNL Adobe Analytics]
* [!DNL Adobe Customer Journey Analytics]

Als een rapporteringsoplossing in uw [&#x200B; rekeningsmontages &#x200B;](/help/main/administrating-target/reporting.md) wordt gespecificeerd, wordt de gespecificeerde oplossing gebruikt en dit het plaatsen is niet zichtbaar.

U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.

**[!DNL Adobe Analytics]**: Zie [[!DNL Adobe Analytics]  als rapporteringsbron voor  [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) om over de verschillen tussen de het melden oplossingen en de voordelen van elk te leren.

Wanneer u [!DNL Analytics] selecteert als de rapportbron voor [!DNL Target] (A4T), selecteert u een [!DNL Analytics] -rapportsuite die [!DNL Target] activiteitsgegevens ontvangt. Hiervoor kiest u eerst een van de [!DNL Analytics] -bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportreeks nog van de lijst mist, contacteer [&#x200B; de Zorg van de Klant &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Er wordt een standaard traceringsserver weergegeven in het veld [!UICONTROL Tracking Server] . Als u meer dan één volgende server gebruikt, zorg ervoor u de correcte het volgen server in dit gebied omvat. Zie [&#x200B; Gebruikend een Analytics die Server &#x200B;](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) volgen voor meer informatie.

**[!DNL Adobe Customer Journey Analytics]**: Zie [[!DNL Target]  rapporterend in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) voor meer informatie over de integratie tussen [!DNL Adobe Customer Journey Analytics] en [!DNL Target].

### Goal Metric

Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een metrische waarde [!UICONTROL Conversion] en stel vervolgens de parameters in die bepalen wanneer succes wordt geboekt.

>[!NOTE]
>
>Als de rapportoplossing aan [!DNL Analytics] wordt geplaatst, is enige beschikbare doel metrisch [!UICONTROL Conversion]. [!DNL Analytics] metriek kan niet als doel worden geselecteerd.

Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de succesmetrische gegevens te kiezen.

Als deze optie is ingeschakeld, biedt het veld [!UICONTROL Estimated Value of the Conversion] (niet beschikbaar voor de [!UICONTROL Page Score] -meetgegevens) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan [!DNL Target] een geschatte lift in inkomsten berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), gebruikt de schatting [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency.

Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Dit gedrag is anders dan het standaardgedrag in [!DNL Target Classic] , dat bezoekers als nieuw beschouwt als ze de test opnieuw zien.

### Aanvullende cijfers

Maak aanvullende succeswaarden.

Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op [!DNL Analytics] . In dit geval worden de maatstaven die voor de rapportsuite [!DNL Analytics] zijn gedefinieerd, toegepast.

### Soorten publiek voor rapportage

Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportdoelgroepen toevoegen om alleen informatie over specifieke doelgroepen weer te geven.

### Geavanceerde instellingen {#section_E2FE441AFB324E498793ABB025ED9974}

Geavanceerde instellingen zijn beschikbaar voor [!UICONTROL Multivariate Test] -doelmeetgegevens.

![&#x200B; Geavanceerde het menu van Montages &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/Menu_AdvancedSettings.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron gebruikt, worden de instellingen beheerd door de [!DNL Analytics] -server. De optie Geavanceerde instellingen is niet beschikbaar.

#### Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen?

Gebruik deze optie om slechts iemand te tellen zoals het bereiken van metrisch succes als zij eerder een verschillend succes metrisch hebben bereikt. Een testconversie is bijvoorbeeld alleen geldig als de bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat de conversie plaatsvindt.

U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.

Definieer beide (of meerdere) succeswaarden voordat u de ene afhankelijk van de andere kunt maken.

Met de optie [!UICONTROL Add Dependency] kan de metrische waarde met succes worden verhoogd als een andere maatstaf met succes is bereikt of niet is bereikt.

Een afhankelijkheid toevoegen:

1. Klik op **[!UICONTROL Advanced Settings]** nadat u aanvullende metriek hebt toegevoegd.
2. Klik op de optie **[!UICONTROL Add Dependency]** :

   ![&#x200B; voeg Afhankelijkheid &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency.png) toe

3. Sleep de gewenste metriek van het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op **[!UICONTROL Reached]** om de instelling tussen Gehaald en Niet bereikt in te schakelen.

   ![&#x200B; Behaalde Afhankelijkheid &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency_reached.png)

U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.

### Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet?

Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:

* [!UICONTROL Select Increment Count & Keep User in Activity] om op te geven hoe het aantal wordt verhoogd.
* [!UICONTROL Select Increment Count, Release User & Allow Reentry] om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.
* [!UICONTROL Select Increment Count, Release User & Bar from Reentry] om op te geven wat de gebruiker ziet in plaats van de inhoud van de activiteit.

Zie [&#x200B; Metriek van het Succes &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde montages.

## Andere metagegevens {#section_2E8917BEFB954480A4206B9E9E917F80}

De volgende instelling is beschikbaar:

### Notities

Typ alle informatie over uw activiteiten die nuttig is voor uzelf of andere teamleden. U kunt het formaat van het deelvenster [!UICONTROL Notes] wijzigen.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Activiteitsinstellingen (3:02)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)

### Meervoudige tests maken (9 :25)

In deze video ziet u hoe u een multivariate test maakt met behulp van de [!DNL Target] driestapige geleide workflow. De doelstellingen en de montages worden besproken begin bij 7 :00.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
