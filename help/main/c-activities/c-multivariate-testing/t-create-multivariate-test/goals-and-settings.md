---
keywords: activiteitinstellingen;doelen en instellingen;variëren;mvt
description: Leer hoe u de [!UICONTROL Goals & Settings] pagina in [!DNL Adobe Target] om informatie over de doelstellingen van een [!UICONTROL Multivariate Test] (MVT) activiteit.
title: Hoe kan ik doelen en instellingen opgeven in een [!UICONTROL Multivariate Test] (MVT) Activiteit?
feature: Multivariate Tests
exl-id: 823a1435-ccb9-4357-9c33-a0968d704b7a
source-git-commit: ba4eb936a0fcf3a8ec7ed7ca87625a9829deb901
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 0%

---

# Doelstellingen en instellingen ([!UICONTROL Multivariate Test])

De [!UICONTROL Goals & Settings] pagina in [!DNL Adobe Target] Hier voert u informatie in over de doelen van uw [!UICONTROL Multivariate Test] (MVT) activiteiten.

De volgende secties zijn beschikbaar:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

De beschikbare instellingen in elke sectie zijn afhankelijk van het gebruik [!DNL Target] of [!DNL Analytics] als de bron van de rapportage.

## Activiteiteninstellingen {#section_DCBDC354261F420EBD4B43EA34947BAC}

De volgende instellingen zijn beschikbaar:

### Doelstelling

Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de campagne identificeren.

### Prioriteit

Afhankelijk van uw instellingen worden [!DNL Target] UI en opties voor [!UICONTROL Priority] variëren. U kunt de oudere instellingen van [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High]of u kunt fijnkorrelige prioriteiten inschakelen van 0 tot en met 999.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.

Als deze optie niet is ingeschakeld in [!UICONTROL Administration] > [!UICONTROL Reporting] (standaard) geeft u een prioriteit op: [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High].

Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op [!UICONTROL Administration] > [!UICONTROL Reporting]en schakelt u vervolgens de [!UICONTROL Enable Fine-Grained Priorities] aan de positie &quot;Aan&quot;.

Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:

* 0 = Laag
* 999 = Hoog

Voor activiteiten die in vorige versies van [!DNL Target], [!UICONTROL Low] prioriteit wordt omgezet in 0, [!UICONTROL Medium] prioriteit wordt omgezet in 5, en [!UICONTROL High] prioriteit wordt omgezet in 10. U kunt deze waarden desgewenst aanpassen.

>[!NOTE]
>
>Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld.

### Duur

De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdkiezer gebruikt een 24-uurs klok, waarbij 00:00 middernacht is. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw.

## Rapportinstellingen {#section_13119392051044FBA6387D9B3B1C43CF}

De volgende instellingen zijn beschikbaar:

### Rapportagebron

Opgeven of gegevens moeten worden verzameld [!DNL Adobe Target] of van [!DNL Adobe Analytics]. Zie [Adobe Analytics als rapportbron voor Doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) voor meer informatie over de verschillen tussen de rapporteringsoplossingen en de voordelen van beide.

Als u [!DNL Analytics] als bron van rapportage voor [!DNL Target]selecteert u een [!DNL Analytics] te ontvangen rapportsuite [!DNL Target] activiteitsgegevens. Kies eerst een van de opties [!DNL Analytics] bedrijven waaraan uw account is gekoppeld, en selecteer vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich weer aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!UICONTROL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Een standaard volgende server wordt weergegeven in het dialoogvenster [!UICONTROL Tracking Server] veld. Als u meer dan één volgende server gebruikt, zorg ervoor dat u de correcte het volgen server in dit gebied omvat. Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) voor meer informatie .

Als er een rapportoplossing is opgegeven in uw accountinstellingen, wordt de opgegeven oplossing gebruikt en is deze instelling niet zichtbaar.

>[!NOTE]
>
>U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.

### Goal Metric

Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] metrisch, dan plaats de parameters die bepalen wanneer het succes wordt bereikt.

>[!NOTE]
>
>Als de rapporteringsoplossing wordt geplaatst aan [!DNL Analytics], de enige beschikbare doelstelling metrisch is [!UICONTROL Conversion]. [!DNL Analytics] metriek kan niet als doel worden geselecteerd.

Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de succesmetrische gegevens te kiezen.

Indien ingeschakeld, wordt de [!UICONTROL Estimated Value of the Conversion] veld (niet beschikbaar voor de [!UICONTROL Page Score] metriek) verstrekt een waarde voor uw doel, maar niet voor andere metriek. Deze waarde schakelt [!DNL Target] een geraamde verhoging van de inkomsten te berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency.

Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Dit gedrag verschilt van het standaardgedrag in [!DNL Target Classic], die bezoekers als nieuw beschouwt als ze de test opnieuw zien.

### Aanvullende cijfers

Maak aanvullende succeswaarden.

Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op [!DNL Analytics]. In dit geval worden de maatstaven voor de [!DNL Analytics] rapportsuite wordt toegepast.

### Soorten publiek voor rapportage

Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportdoelgroepen toevoegen om alleen informatie over specifieke doelgroepen weer te geven.

### Geavanceerde instellingen {#section_E2FE441AFB324E498793ABB025ED9974}

Geavanceerde instellingen zijn beschikbaar voor [!UICONTROL Multivariate Test] maatstaven van het doel.

![Het menu Geavanceerde instellingen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/Menu_AdvancedSettings.png)

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als uw rapporteringsbron, worden de montages beheerd door [!DNL Analytics] server. De optie Geavanceerde instellingen is niet beschikbaar.

#### Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen?

Gebruik deze optie om slechts iemand te tellen zoals het bereiken van metrisch succes als zij eerder een verschillend succes metrisch hebben bereikt. Een testconversie is bijvoorbeeld alleen geldig als de bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat de conversie plaatsvindt.

U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.

Definieer beide (of meerdere) succeswaarden voordat u de ene afhankelijk van de andere kunt maken.

De [!UICONTROL Add Dependency] optie staat succesmetrisch toe om te verhogen als een ander succes metrisch is bereikt of niet bereikt.

Een afhankelijkheid toevoegen:

1. Klik op **[!UICONTROL Advanced Settings]**.
2. Klik op de knop **[!UICONTROL Add Dependency]** optie:

   ![Afhankelijkheid toevoegen](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency.png)

3. Sleep de gewenste metriek vanuit het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op **[!UICONTROL Reached]** om de instelling tussen Gehaald en Niet bereikt in te schakelen.

   ![Afhankelijkheid bereikt](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency_reached.png)

U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.

### Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet?

Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:

* [!UICONTROL Select Increment Count & Keep User in Activity] om op te geven hoe het aantal wordt verhoogd.
* [!UICONTROL Select Increment Count, Release User & Allow Reentry] om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.
* [!UICONTROL Select Increment Count, Release User & Bar from Reentry] om op te geven wat de gebruiker te zien krijgt in plaats van de inhoud van de activiteit.

Zie [Succeswaarden](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde instellingen.

## Andere metagegevens {#section_2E8917BEFB954480A4206B9E9E917F80}

De volgende instelling is beschikbaar:

### Notities

Typ alle informatie over uw activiteiten die nuttig is voor uzelf of andere teamleden. De [!UICONTROL Notes] is resizable.

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

### Multivariate tests maken (9:25)

In deze video wordt getoond hoe u een multivariatietest kunt maken met de opdracht [!DNL Target] driestapsgerichte workflow. De doelstellingen en de montages worden besproken begin om 7:00.

* Een multivariatietest definiëren en ontwerpen
* Een multivariatietest maken

>[!VIDEO](https://video.tv.adobe.com/v/17395)
