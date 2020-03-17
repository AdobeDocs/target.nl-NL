---
keywords: activity settings;A/B goals and settings;reporting settings;goal metrics;success metrics;dependent success metrics;advanced settings;primary goal;additional metrics;objective;priority;duration;reporting solution;goal;audiences for reporting;Which success metric must be reached before incrementing this metric;What will happen after a user encounters this goal metric;notes
description: Op de pagina Doelstellingen en instellingen geeft u informatie op over de doelen van de test.
title: Doelstellingen en instellingen
uuid: 46d02e39-0c19-4da8-bdd8-48acb708831b
snippet: y
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Doelstellingen en instellingen {#goals-and-settings}

Op de pagina Doelstellingen en instellingen geeft u informatie op over de doelen van de test.

De beschikbare instellingen zijn afhankelijk van het feit of u Doel of [Analyse](/help/c-integrating-target-with-mac/a4t/a4t.md) als gegevensbron gebruikt.

![Activiteitsinstellingen, dialoogvenster](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

## Activiteiteninstellingen {#section_DCBDC354261F420EBD4B43EA34947BAC}

| Instellingen | Beschrijving |
|--- |--- |
| Doelstelling | Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de campagne identificeren. |
| Prioriteit | Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.<br>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<br>Als deze optie niet in Opstelling (het gebrek) wordt toegelaten, specificeer een prioriteit: Laag, Normaal of Hoog. <br>Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op Instellen en schakelt u de optie Fine-Grained Prioriteiten inschakelen in op de positie &quot;Aan&quot;. <br>Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999: 0 = Laag en 999 = Hoog. <br>Voor activiteiten die zijn gemaakt in eerdere versies van Target Standard/Premium wordt Lage prioriteit omgezet in 0, Normaal in 5 en Hoog in 10. U kunt deze waarden desgewenst aanpassen.<br>Opmerking:  Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld. |
| Duur | De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdkiezer gebruikt een 24-uurs klok, waarbij 00:00 middernacht is. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw. |

## Rapportinstellingen {#section_13119392051044FBA6387D9B3B1C43CF}

| Instellingen | Beschrijving |
|--- |--- |
| Bron rapporteren | Geef op of gegevens van Adobe Target of van Adobe Analytics worden verzameld. Zie [Adobe Analytics als Rapporterende Bron voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md) om over de verschillen tussen de rapporteringsoplossingen en de voordelen van elk te leren.  Wanneer u Analytics selecteert als de rapporteringsbron voor Target, selecteert u een Analytics-rapportsuite die doelactiviteitgegevens ontvangt.<br>Hiervoor kiest u eerst een van de Analytics-bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij Adobe Experience Cloud om het opnieuw te proberen. Neem contact op met de klantenservice als de rapportsuite nog steeds ontbreekt in de lijst.<br>Als een rapportbron is opgegeven in uw accountinstellingen, wordt de opgegeven bron gebruikt en is deze instelling niet zichtbaar.<br>Opmerking:  U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden. |
| Goal | Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een omzettingsmetrische waarde en stel vervolgens de parameters in die bepalen wanneer succes wordt behaald.  Zie Metriek [instellen voor meer informatie over het instellen van metriek](../../../c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<br>Opmerking:  Als de rapporteringsoplossing aan Analytics wordt geplaatst, is enige beschikbare doel metrisch Omzetting. Metrische gegevens voor analyse kunnen niet als doel worden geselecteerd.   Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de succesmetrische gegevens te kiezen.<br>Als deze optie is ingeschakeld, biedt de geschatte waarde van het veld Omzetting (niet beschikbaar voor de maatstaven van de paginascore) een waarde voor uw doel, maar niet voor andere meetwaarden. Met deze waarde kan Target een geschatte lift in inkomsten berekenen. Dit veld is facultatief; de incrementele inkomsten voor elke metrische waarde die geen inkomsten oplevert, kunnen echter niet zonder deze methode worden berekend. Voor alle inkomstenmaatstaven (opbrengsten per bezoeker, gemiddelde bestelwaarde, totale verkoop en bestellingen) gebruikt de schatting de opbrengsten per bezoeker. Het gegevenstype is currency.<br>Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een hogere prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Merk op dat dit verschillend is dan het standaardgedrag in Doel Klassiek, dat bezoekers als nieuw beschouwd als zij de test opnieuw zien. |
| Aanvullende cijfers | Maak aanvullende succesmaatstaven.  Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op Analytics. In dit geval worden de maatstaven die voor de rapportsuite Analytics zijn gedefinieerd, toegepast. |
| Soorten publiek voor rapportage | Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportdoelgroepen toevoegen om alleen informatie over specifieke doelgroepen weer te geven.  Deze instelling is niet beschikbaar als u Analytics kiest als uw rapportoplossing. Het publiek dat voor de het rapportreeks van Analytics wordt bepaald wordt toegepast. |

## Geavanceerde instellingen {#section_E2FE441AFB324E498793ABB025ED9974}

De geavanceerde montages zijn beschikbaar voor de doelstellingen van de Test van A/B metriek.

![Het menu Geavanceerde instellingen](/help/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Als u Adobe Analytics als rapportbron gebruikt, worden de instellingen beheerd door de Analytics-server. De optie Geavanceerde instellingen is niet beschikbaar.

![Geavanceerde instellingen](/help/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Instelling | Beschrijving |
|--- |--- |
| Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen? | Gebruik deze optie als u alleen wilt tellen dat iemand de maatstaf voor succes heeft bereikt als hij of zij eerder een andere maatstaf voor succes heeft bereikt. Een testconversie is bijvoorbeeld alleen geldig als de bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat deze wordt omgezet.  U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.  U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.  Met de optie Afhankelijkheid toevoegen kan metrisch met succes worden verhoogd als een andere succesmetrische waarde is bereikt of niet is bereikt.  Een afhankelijkheid toevoegen:<ul><li>Klik op Geavanceerde instellingen nadat u aanvullende gegevens hebt toegevoegd.</li><li>Klik op de optie Afhankelijkheid toevoegen:</li><li>Sleep de gewenste metriek van het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op Geëxisteerd om de instelling tussen Gehaald en Niet bereikt te wijzigen.</li><li>U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.</li></ul> |
| Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet? | Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:<ul><li>Selecteer Aantal verhogen en Gebruiker in activiteit houden om te specificeren hoe de telling wordt verhoogd.</li><li>Selecteer Aantal verhogen, Gebruiker vrijgeven &amp; Opnieuw invoeren toestaan om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.</li><li>Selecteer Aantal verhogen, Gebruiker vrijgeven &amp; Staaf van Opnieuw invoeren om op te geven wat de gebruiker ziet in plaats van de inhoud van de activiteit.</li></ul> |
| Hoe wordt het aantal verhoogd? | Er zijn drie opties voor de verhoging van het aantal:<ul><li>Eenmaal per Enter</li><li>Bij elke afdruk (met uitzondering van pagina-vernieuwingen)</li><li>Bij elke indrukking</li></ul> |

Zie [Succeswaarden](../../../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde instellingen.

## Andere metagegevens {#section_2E8917BEFB954480A4206B9E9E917F80}

| Instellingen | Beschrijving |
|---|---|
| Notities | Typ alle informatie over uw activiteiten die u voor uzelf of andere teamleden kunt gebruiken. U kunt het formaat van het deelvenster Notities wijzigen. |

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Activiteitsinstellingen (3:02) ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

(https://video.tv.adobe.com/v/17381)

### Een ![zelfstudie-badge voor A/B-tests maken (8:36)](/help/assets/tutorial.png)

In deze video ziet u hoe de instellingen voor activiteit passen in de driestappenworkflow met instructies bij het maken van een activiteit. De doelstellingen en de montages worden besproken beginnend bij 5:30.

* A/B-activiteit maken in Adobe Target
* Verkeer toewijzen met een handmatige splitsing of automatische verkeerstoewijzing

>[!VIDEO](https://video.tv.adobe.com/v/17391)
