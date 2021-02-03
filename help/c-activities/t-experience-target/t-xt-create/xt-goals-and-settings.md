---
keywords: activiteit montages;ervaring richtend doelstellingen en montages;xt doelstellingen en montages;ervaring richtend;rapporteringsmontages;doel metriek;afhankelijke succesmetriek;afhankelijke succesmetriek;primair doel;extra metriek;prioriteit;duur;rapporteringsoplossing;doel;publiek voor het melden;Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen;Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet;nota's
description: Op de pagina Doelstellingen en instellingen geeft u informatie op over de doelen van de test.
title: Doelstellingen en instellingen
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 0%

---


# Doelstellingen en instellingen in Experience Targeting (XT)-activiteiten

Op de pagina Doelstellingen en instellingen geeft u informatie op over de doelen van de test.

* Activiteiteninstellingen
* Rapportinstellingen
* Andere metagegevens

De beschikbare instellingen zijn afhankelijk van het feit of u [!DNL Target] of [!DNL Analytics] als gegevensbron gebruikt.

![pagina Instellingen activiteit](/help/c-activities/t-experience-target/t-xt-create/assets/ab_settings-new.png)

## Activiteitsinstellingen {#section_DCBDC354261F420EBD4B43EA34947BAC}

De volgende instellingen zijn beschikbaar

### Doelstelling

Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de campagne identificeren.

### Prioriteit

Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.

Als deze optie niet is ingeschakeld in Beheer (de standaardinstelling), geeft u een prioriteit op: Laag, Normaal of Hoog.

Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Reporting]** en schakelt u vervolgens de optie Fine-Grained prioriteiten inschakelen in op de positie &quot;Aan&quot;.

Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:

* 0 = Laag
* 999 = Hoog

Voor activiteiten die zijn gemaakt in eerdere versies van Target Standard/Premium wordt Lage prioriteit omgezet in 0, Normaal in 5 en Hoog in 10. U kunt deze waarden desgewenst aanpassen.

>[!NOTE]
>
>Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld.

### Duur

De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdkiezer gebruikt een 24-uurs klok, waarbij 00:00 middernacht is. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw.

## Rapportinstellingen {#section_13119392051044FBA6387D9B3B1C43CF}

De volgende instellingen zijn beschikbaar:

### Oplossing voor rapportage

Geef op of gegevens uit Adobe Target of Adobe Analytics worden verzameld. Zie [Adobe Analytics als Rapporterende Bron voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md) om over de verschillen tussen de rapporteringsoplossingen en de voordelen van elk te leren.

Wanneer u Analytics selecteert als de rapporteringsbron voor Target, selecteert u een Analytics-rapportsuite die doelactiviteitgegevens ontvangt. Hiervoor kiest u eerst een van de Analytics-bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target, zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de Adobe Experience Cloud om het opnieuw te proberen. Neem contact op met de klantenservice als de rapportsuite nog steeds ontbreekt in de lijst.

Analytics for Target vereist een trackingserver om de resultaten correct te rapporteren. In het veld Trackingserver wordt een standaard traceringsserver weergegeven. Als u meerdere trackingservers gebruikt, moet u controleren of u de juiste trackingserver in dit veld opneemt. Zie [Een Analytics Tracking Server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) gebruiken voor meer informatie.

Als er een rapportoplossing is opgegeven in uw accountinstellingen, wordt de opgegeven oplossing gebruikt en is deze instelling niet zichtbaar.

>[!NOTE]
>
>U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.

### Goal Metric

Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een omzettingsmetrische waarde en stel vervolgens de parameters in die bepalen wanneer succes wordt behaald.

Zie [Metriek instellen](/help/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB) voor meer informatie over het instellen van metriek.

>[!NOTE]
>
>Als de rapporteringsoplossing aan Analytics wordt geplaatst, is enige beschikbare doel metrisch Omzetting. Metrische gegevens voor analyse kunnen niet als doel worden geselecteerd.

Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de metrische succesmethode te kiezen.

Als deze optie is ingeschakeld, biedt de geschatte waarde van het veld Omzetting (niet beschikbaar voor de maatstaven van de paginascore) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan Target een geschatte lift in inkomsten berekenen. Dit veld is facultatief; de incrementele inkomsten voor elke metrische waarde die geen inkomsten oplevert, kunnen echter niet zonder deze methode worden berekend. Voor alle inkomstenmaatstaven (opbrengsten per bezoeker, gemiddelde bestelwaarde, totale verkoop en bestellingen) gebruikt de schatting de opbrengsten per bezoeker. Het gegevenstype is currency.

Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een hogere prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Merk op dat dit verschillend is dan het standaardgedrag in Doel Klassiek, dat bezoekers als nieuw beschouwd als zij de test opnieuw zien.

### Aanvullende cijfers

Maak aanvullende succesmaatstaven.

Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op Analytics. In dit geval worden de maatstaven die voor de rapportsuite Analytics zijn gedefinieerd, toegepast.

### Soorten publiek voor rapportage

Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportdoelgroepen toevoegen om alleen informatie over specifieke doelgroepen weer te geven.

Deze instelling is niet beschikbaar als u Analytics kiest als uw rapportoplossing. Het publiek dat voor de het rapportreeks van Analytics wordt bepaald wordt toegepast.

## Overige metagegevens

Typ alle informatie over uw activiteiten die u voor uzelf of andere teamleden kunt gebruiken. U kunt het formaat van het deelvenster Notities wijzigen.

## Geavanceerde instellingen {#section_E2FE441AFB324E498793ABB025ED9974}

De geavanceerde montages zijn beschikbaar voor Ervaring richtend doelmetriek.

![Geavanceerde instellingen](/help/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Als u Adobe Analytics als rapportbron gebruikt, worden de instellingen beheerd door de Analyseserver. De optie Geavanceerde instellingen is niet beschikbaar.

De volgende instellingen zijn beschikbaar:

### Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen?

Gebruik deze optie als u alleen wilt tellen dat iemand de maatstaf voor succes heeft bereikt als hij of zij eerder een andere maatstaf voor succes heeft bereikt. Een testconversie is bijvoorbeeld alleen geldig als de bezoeker op het aanbod klikt of een bepaalde pagina bereikt voordat de conversie plaatsvindt.

U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.

U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.

Met de optie Afhankelijkheid toevoegen kan metrisch met succes worden verhoogd als een andere succesmetrische waarde is bereikt of niet is bereikt.

Een afhankelijkheid toevoegen:

1. Klik op **[!UICONTROL Advanced Settings]** nadat u extra metriek hebt toegevoegd.
2. Klik op **[!UICONTROL Add Dependency]**:

   ![Koppeling voor afhankelijkheid toevoegen](/help/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Sleep de gewenste metriek van het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op Geëxisteerd om de instelling tussen Gehaald en Niet bereikt te wijzigen.

   ![Dialoogvenster Metrische afhankelijkheid toevoegen](/help/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.

### Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet?

Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:

* Selecteer Aantal verhogen en Gebruiker in activiteit houden om te specificeren hoe de telling wordt verhoogd.
* Selecteer Aantal verhogen, Gebruiker vrijgeven &amp; Opnieuw invoeren toestaan om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.
* Selecteer Aantal verhogen, Gebruiker vrijgeven &amp; Staaf van Opnieuw invoeren om op te geven wat de gebruiker ziet in plaats van de inhoud van de activiteit.

Zie [Succeswaarden](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde instellingen.

## Trainingsvideo: Activiteitsinstellingen (3:02)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)