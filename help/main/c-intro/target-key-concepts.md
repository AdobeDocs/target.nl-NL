---
keywords: Overzicht en verwijzing;soorten activiteit;inleiding
description: Leer de basisbeginselen van Adobe Target. Dit artikel introduceert u aan Doel, zijn activiteitstypes, en andere eigenschappen.
title: Hoe gebruik ik Target?
feature: Overview
exl-id: c9555d79-d505-41ff-ba4b-ab94793f9efa
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 2%

---

# Doelsleutelbegrippen

Informatie over de belangrijkste concepten die u helpen de eigenschappen en de mogelijkheden begrijpen [!DNL Adobe Target].

## Activiteiten en tests {#section_BEA0A0C51A8847579B566060206DE7E8}

Een activiteit bepaalt de ervaringen een plaatsbezoeker zou kunnen ontmoeten.

U kunt bijvoorbeeld een activiteit ontwerpen die twee verschillende landingspagina&#39;s test, een die informatie over dameszomerschoenen belicht, en een die meer algemene zomerkleding benadrukt. De activiteit bepaalt de voorwaarden die controleren wanneer elk van deze landingspagina&#39;s verschijnt, en de metriek die bepalen welke pagina succesvoller is. De activiteit wordt gevormd om te beginnen en te beëindigen wanneer de specifieke voorwaarden worden voldaan. Deze voorwaarden kunnen het begin en einde van de activiteit tussen bepaalde data omvatten, of het begin wanneer de activiteit wordt goedgekeurd en het einde wanneer deze wordt gedeactiveerd.

Plan zorgvuldig wanneer het ontwerpen van een activiteit. Bepaal wanneer de activiteit begint en hoe lang het duurt. Geef vervolgens een lijst met uw aanbiedingen en wijs een doelgroep toe aan elk aanbod.

Doel bevat verschillende typen activiteit. In de volgende tabel vindt u een overzicht van elk type activiteit met koppelingen voor meer informatie. Om u beter te helpen het beste activiteitstype voor uw doeleinden kiezen, heeft het team van het Doel ook gecreeerd [Adobe Target Activity Guide](/help/main/c-activities/target-activities-guide.md).

| Type activiteit | Beschrijving |
|--- |--- |
| [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) | Bij het testen van A/B worden twee of meer versies van de inhoud van uw website vergeleken om te zien welke versie het beste uw omzettingen tijdens een vooraf gespecificeerde testperiode verbetert.<br>**Opmerking:** U kunt nu [aanbevelingen binnen de testactiviteiten A/B](/help/main/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit hebt u een [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium). |
| [Automatisch toewijzen](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Met Automatisch toewijzen wordt een winnaar geïdentificeerd aan de hand van twee of meer ervaringen en wordt automatisch meer verkeer toegewezen aan de winnaar, zodat de conversie toeneemt terwijl de test nog steeds wordt uitgevoerd en opgedaan.<br>**Opmerking:** U kunt nu [aanbevelingen in Auto-Allocate activiteiten](/help/main/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit hebt u een [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium). |
| [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<br>![Doelpremie](/help/main/assets/premium.png) | AutoDoel gebruikt geavanceerd machine leren om veelvoudige hoog presterende tellers-bepaalde ervaringen te identificeren. Auto-Target activiteiten dienen voor elke bezoeker de meest toegesneden ervaring op basis van hun individuele klantprofiel en het gedrag van vorige bezoekers met vergelijkbare profielen, om inhoud en aandrijvingsomzettingen aan te passen.<br>**Opmerking:** U kunt nu [aanbevelingen in Auto-Target activiteiten](/help/main/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit hebt u een [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium). |
| [Analysegegevens gebruiken](/help/main/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A4T) | U kunt een activiteit vormen om te gebruiken [!DNL Adobe Analytics] als bron van de rapportage. Voor dit type activiteit is een koppeling vereist tussen uw  [!DNL Adobe Experience Cloud] account met beide [!DNL Analytics] en [!DNL Target]. |
| [Multivariatietest](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | MVT (Multivariate Testing) vergelijkt combinaties van aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifieke doelgroep presteert, en identificeert welk element de meeste invloed op het succes van de activiteit heeft. |
| [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) | Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.<br>**Opmerking:** U kunt nu [aanbevelingen binnen de ervaring gerichte activiteiten](/help/main/c-recommendations/recommendations-as-an-offer.md). Voor deze functionaliteit hebt u een [Licentie voor doelpremie](/help/main/c-intro/intro.md#premium). |
| [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>![Doelpremie](/help/main/assets/premium.png) | Automated Personalization (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende verschillen met elke bezoeker op basis van hun individuele klantprofiel met elkaar in overeenstemming te brengen, om inhoud en schijfconversies aan te passen. |
| [Recommendations](/help/main/c-recommendations/recommendations.md)<br>![Doelpremie](/help/main/assets/premium.png) | Een aanbeveling bepaalt hoe een product aan een websitegebruiker wordt voorgesteld, afhankelijk van de activiteiten van die gebruiker op de plaats.<br>U kunt bijvoorbeeld mensen die een rugzak kopen aanmoedigen om wandelschoenen en wandelstokken te kopen. U kunt een aanbeveling maken die items toont die vaak samen worden aangeschaft met het algoritme &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. U kunt bezoekers ook aanmoedigen om meer tijd te besteden aan uw mediasite door dezelfde video aan te bevelen als de video die ze bekijken. Gebruik hiervoor het algoritme &quot;Personen die dit hebben bekeken&quot;.<br>**Opmerking:** U kunt nu aanbevelingen opnemen in de A/B-test (inclusief Automatische toewijzing en Auto-Target) en de Experience Targeting-activiteiten (XT). Zie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## Locaties {#section_F18FBF1ED23340ED9F39C51971A4E874}

Een locatie is voornamelijk een pagina op uw website. Het kan ook verwijzen naar een plaats in een mobiele app, een e-mail of een andere plaats waar u een optimalisatie uitvoert.

Locaties zijn essentieel voor activiteiten en ervaringen. U bepaalt of een locatie een van de volgende handelingen kan uitvoeren, beide of geen van de volgende handelingen:

* Inhoud voor bezoekers weergeven en wisselen.
* Het gedrag van de bezoeker van het logboek.

In [!DNL Target Standard], kan een locatie elk element op een pagina zijn, zolang de pagina maar één coderegel bevat die [!DNL Target] in de `<head>` van elke pagina die u wilt bijhouden. Deze coderegel roept de JavaScript-bibliotheken aan die nodig zijn om informatie te verzamelen en uw bezoekers gerichte ervaringen te bieden.

Locaties worden gecombineerd met het publiek om een bijna oneindig aantal opties te bieden waarmee uw klanten informatie kunnen zoeken. Als een bezoeker bijvoorbeeld nog niet eerder naar de site is geweest, kunt u een kortingscoupon weergeven voor nieuwe klanten. Op dezelfde manier kan de pagina worden gewijzigd in weergaveaanbiedingen die beter zijn geoptimaliseerd voor terugkerende klanten.

U kunt plaatsen ook gebruiken om de vooruitgang van een bezoeker door uw Website te volgen. U kunt locaties ook gebruiken om bij te houden of de bezoeker een bepaalde maatstaf voor succes heeft voltooid, zoals het toevoegen van een artikel aan het winkelwagentje of het voltooien van een aankoop.

## Ervaringen en paginaontwerpen {#section_B806FB752EC1470784755C1EB3D4AC70}

Een ervaring, ook wel een recept genoemd, definieert de inhoud die op uw pagina wordt weergegeven, en andere pagina-elementen, zoals koppelingen.

Een ervaring bepaalt welke aanbiedingsvertoningen op een bepaalde plaats wanneer specifieke het richten voorwaarden worden voldaan aan. De ervaring bepaalt bijvoorbeeld dat, wanneer een retourbezoeker uw site bezoekt, boven aan de pagina een aanbieding voor verzending over twee dagen wordt weergegeven. De ervaring bepaalt ook dat wanneer een eerste bezoeker de pagina bekijkt, een korting van 10% op dezelfde locatie wordt weergegeven.

Een ervaring bestaat uit de aanbiedingen, afbeeldingselementen of andere HTML-elementen (zoals koppelingen) die op de pagina worden weergegeven om de bezoeker naar het gewenste resultaat te sturen. [!DNL Target] combineert locaties, aanbiedingen en ervaringen om te bepalen welke inhoud tijdens een specifieke test op uw site wordt weergegeven.

Een ervaring kan ook een ander paginaontwerp zijn. Een ervaring kan bijvoorbeeld een set koppelingen boven aan de pagina bevatten, waarbij een andere ervaring andere koppelingen heeft of dezelfde koppelingen in een andere volgorde. Mogelijk wilt u testen of de ene afbeelding meer optilt dan de andere, of op een advertentie eerder boven aan de pagina of op een andere locatie wordt geklikt.

[!DNL Target] optimaliseert ervaringen voor elk van uw bezoekers over uw digitale aanraakpunten en om verschillende ervaringen te testen om te bepalen welke het meest succesvol zal zijn. Door uw ervaringen zorgvuldig te richten, kunt u ervoor zorgen dat uw bezoekers van de site de meest relevante aanbiedingen op de juiste locaties op uw pagina zien, waardoor uw kans op een succesvol bezoek groter wordt.

## Aanbiedingen {#section_973D4CC4CEB44711BBB9A21BF74B89E9}

Een aanbieding is de inhoud die tijdens campagnes of activiteiten op uw webpagina&#39;s wordt weergegeven.

Wanneer u uw webpagina&#39;s test, meet u het succes van elke ervaring met verschillende aanbiedingen op uw locaties.

Een aanbieding kan verschillende typen inhoud bevatten, zoals:

* Afbeelding
* Tekst
* HTML
* Koppeling
* Knop

Op een webpagina kunnen bijvoorbeeld twee aanbiedingen worden weergegeven, afhankelijk van of de bezoeker al eerder naar uw site is geweest.

An *ervaring* bepaalt welke inhoud wordt weergegeven wanneer aan bepaalde voorwaarden wordt voldaan.

## Soorten publiek {#section_3F32DA46BDF947878DD79DBB97040D01}

Optimaliseer uw gerichte inhoud aan activiteiteningangen die aan specifieke criteria voldoen.

Het publiek bepaalt het doel voor uw activiteit en wordt gebruikt overal waar het richten beschikbaar is.

[!DNL Target] het publiek is een bepaalde reeks bezoekerscriteria . Aanbiedingen kunnen worden gericht op specifieke doelgroepen (of segmenten). Alleen bezoekers die bij dat publiek horen, zien de ervaring die voor hen is bedoeld.

U kunt een activiteit bijvoorbeeld richten op een publiek dat bestaat uit bezoekers die een bepaalde browser of een bepaald besturingssysteem gebruiken.

Uw activiteit kan ook gericht zijn op bezoekers uit een bepaald geografisch gebied of op personen die uw pagina openen vanuit een bepaald zoekprogramma.

Soorten publiek kan worden opgeslagen voor hergebruik in meerdere activiteiten, of ze kunnen worden gemaakt voor een bepaalde activiteit.

| Type publiek | Beschrijving |
|--- |--- |
| Herbruikbaar publiek | Herbruikbare doelgroepen kunnen voor elke activiteit worden geselecteerd. Als u een van deze soorten publiek wijzigt, verandert dit voor alle activiteiten die het gebruiken. |
| Aangepaste segmenten | De segmenten van de douane (die ook als campagne-specifieke segmenten worden bekend) zijn specifiek voor een campagne in Klassiek van het Doel. Ze worden gemaakt als onderdeel van de campagne en kunnen niet opnieuw worden gebruikt in andere campagnes. |
| Gedeeld publiek | Soorten publiek kan worden gedeeld [!DNL Adobe Experience Cloud] oplossingen. Zie [Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=nl-NL) voor voorbeelden. |

Voor informatie over hoe het bezoekersprofiel informatie over bezoekers van uw site bijhoudt, raadpleegt u [Bezoekerprofielen](/help/main/c-target/c-visitor-profile/visitor-profile.md#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1).

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Typen activiteiten (9:03) ![Overzicht badge](/help/main/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium].

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Soorten publiek gebruiken in Adobe Target (6:21) ![Overzicht badge](/help/main/assets/overview.png)

In deze video wordt uitgelegd hoe u het publiek kunt gebruiken in [!DNL Target Standard/Premium].

* Verklaar de term &quot;Publiek&quot;
* Verklaar de twee manieren waarop het publiek voor optimalisering wordt gebruikt
* Soorten publiek zoeken in de lijst Soorten publiek
* Een activiteit toewijzen aan een publiek
* Gebruik publiek voor passieve rapportage in een activiteit

>[!VIDEO](https://video.tv.adobe.com/v/17398)
