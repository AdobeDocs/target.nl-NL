---
keywords: Overzicht en verwijzing;soorten activiteit;inleiding
description: Leer de basisbeginselen van Adobe Target. Dit artikel introduceert u aan Doel, zijn activiteitstypes, en andere eigenschappen.
title: Hoe gebruik ik Target?
feature: Overview
exl-id: c9555d79-d505-41ff-ba4b-ab94793f9efa
source-git-commit: 122484056e73f8f679312a3e776e623d905701d5
workflow-type: tm+mt
source-wordcount: '1524'
ht-degree: 2%

---

# Belangrijkste doelconcepten

Informatie over belangrijke concepten die u helpen de eigenschappen en mogelijkheden van [!DNL Adobe Target] begrijpen.

## Activiteiten en tests {#section_BEA0A0C51A8847579B566060206DE7E8}

Een activiteit bepaalt de ervaringen een plaatsbezoeker zou kunnen ontmoeten.

U kunt bijvoorbeeld een activiteit ontwerpen die twee verschillende landingspagina&#39;s test, een die informatie over dameszomerschoenen belicht, en een die meer algemene zomerkleding benadrukt. De activiteit bepaalt de voorwaarden die controleren wanneer elk van deze landingspagina&#39;s verschijnt, en de metriek die bepalen welke pagina succesvoller is. De activiteit wordt gevormd om te beginnen en te beëindigen wanneer de specifieke voorwaarden worden voldaan. Deze voorwaarden kunnen het begin en einde van de activiteit tussen bepaalde data omvatten, of het begin wanneer de activiteit wordt goedgekeurd en het einde wanneer deze wordt gedeactiveerd.

Plan zorgvuldig wanneer het ontwerpen van een activiteit. Bepaal wanneer de activiteit begint en hoe lang het duurt. Geef vervolgens een lijst met uw aanbiedingen en wijs een doelgroep toe aan elk aanbod.

Doel bevat verschillende typen activiteit. In de volgende tabel vindt u een overzicht van elk type activiteit met koppelingen voor meer informatie. Om u beter te helpen het beste activiteitstype voor uw doeleinden kiezen, heeft het team van het Doel ook de [&#x200B; Gids van de Activiteiten van Adobe Target &#x200B;](/help/main/c-activities/target-activities-guide.md) gecreeerd.

| Type activiteit | Beschrijving |
|--- |--- |
| [&#x200B; Test A/B &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) | Bij het testen van A/B worden twee of meer versies van de inhoud van uw website vergeleken om te zien welke versie het beste uw omzettingen tijdens een vooraf gespecificeerde testperiode verbetert.<br>**Nota:** u kunt [&#x200B; aanbevelingen binnen de activiteiten van de Test van A/B &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md) nu omvatten. Deze functionaliteit vereist dat u de vergunning van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt. |
| [&#x200B; automatisch-toewijst &#x200B;](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | Met Automatisch toewijzen wordt een winnaar geïdentificeerd aan de hand van twee of meer ervaringen en wordt automatisch meer verkeer toegewezen aan de winnaar, zodat de conversie toeneemt terwijl de test nog steeds wordt uitgevoerd en opgedaan.<br>**Nota:** u kunt [&#x200B; aanbevelingen binnen auto-toewijzen activiteiten &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md) nu omvatten. Deze functionaliteit vereist dat u de vergunning van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt. |
| [&#x200B; auto-Doel &#x200B;](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<br>![&#x200B; Target Premium &#x200B;](/help/main/assets/premium.png) | AutoDoel gebruikt geavanceerd machine leren om veelvoudige hoog presterende tellers-bepaalde ervaringen te identificeren. Auto-Target activiteiten dienen voor elke bezoeker de meest toegesneden ervaring op basis van hun individuele klantprofiel en het gedrag van vorige bezoekers met vergelijkbare profielen, om inhoud en aandrijvingsomzettingen aan te passen.<br>**Nota:** u kunt [&#x200B; aanbevelingen binnen activiteiten van het auto-Doel &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md) nu omvatten. Deze functionaliteit vereist dat u de vergunning van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt. |
| [&#x200B; Gebruikend de Gegevens van Analytics &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/create-a4t.md) (A4T) | U kunt een activiteit vormen om [!DNL Adobe Analytics] als rapporteringsbron te gebruiken. Voor dit type activiteit is het vereist dat u uw [!DNL Adobe Experience Cloud] -account koppelt aan zowel [!DNL Analytics] als [!DNL Target] . |
| [&#x200B; Multivariate Test &#x200B;](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | MVT (Multivariate Testing) vergelijkt combinaties van aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifieke doelgroep presteert, en identificeert welk element de meeste invloed op het succes van de activiteit heeft. |
| [&#x200B; Ervaring richtend &#x200B;](/help/main/c-activities/t-experience-target/experience-target.md) | Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.<br>**Nota:** u kunt [&#x200B; aanbevelingen binnen Ervaring nu omvatten richtend activiteiten &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md). Deze functionaliteit vereist dat u de vergunning van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt. |
| [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br>![&#x200B; Target Premium &#x200B;](/help/main/assets/premium.png) | Automated Personalization (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende verschillen met elke bezoeker op basis van hun individuele klantprofiel met elkaar in overeenstemming te brengen, om inhoud en schijfconversies aan te passen. |
| [&#x200B; Aanbevelingen &#x200B;](/help/main/c-recommendations/recommendations.md)<br>![&#x200B; Target Premium &#x200B;](/help/main/assets/premium.png) | Een aanbeveling bepaalt hoe een product aan een websitegebruiker wordt voorgesteld, afhankelijk van de activiteiten van die gebruiker op de plaats.<br> bijvoorbeeld, zou u mensen kunnen willen aanmoedigen die een backpack kopen om het kopen van wandelschoenen en trekrollen te overwegen. U kunt een aanbeveling maken die items toont die vaak samen worden aangeschaft met het algoritme &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. U kunt bezoekers ook aanmoedigen om meer tijd te besteden aan uw mediasite door dezelfde video aan te bevelen als de video die ze bekijken. Gebruik hiervoor het algoritme &quot;Personen die dit hebben bekeken&quot;.<br>**Nota:** u kunt aanbevelingen binnen A/B Test (met inbegrip van auto-Toewijzing en auto-Doel) en Ervaring nu omvatten richtend (XT) activiteiten. Zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## Locaties {#section_F18FBF1ED23340ED9F39C51971A4E874}

Een locatie is voornamelijk een pagina op uw website. Het kan ook verwijzen naar een plaats in een mobiele app, een e-mail of een andere plaats waar u een optimalisatie uitvoert.

Locaties zijn essentieel voor activiteiten en ervaringen. U bepaalt of een locatie een van de volgende handelingen kan uitvoeren, beide of geen van de volgende handelingen:

* Inhoud voor bezoekers weergeven en wisselen.
* Het gedrag van de bezoeker van het logboek.

In [!DNL Target Standard] kan een locatie elk element op een pagina zijn, zolang de pagina één coderegel bevat die [!DNL Target] in de `<head>` -sectie van elke pagina inschakelt die u wilt bijhouden. Deze coderegel roept de bibliotheken van JavaScript nodig om informatie te verzamelen en gerichte ervaringen aan uw bezoekers te leveren.

Locaties worden gecombineerd met het publiek om een bijna oneindig aantal opties te bieden waarmee uw klanten informatie kunnen zoeken. Als een bezoeker bijvoorbeeld nog niet eerder naar de site is geweest, kunt u een kortingscoupon weergeven voor nieuwe klanten. Op dezelfde manier kan de pagina worden gewijzigd in weergaveaanbiedingen die beter zijn geoptimaliseerd voor terugkerende klanten.

U kunt plaatsen ook gebruiken om de vooruitgang van een bezoeker door uw Website te volgen. U kunt locaties ook gebruiken om bij te houden of de bezoeker een bepaalde maatstaf voor succes heeft voltooid, zoals het toevoegen van een artikel aan het winkelwagentje of het voltooien van een aankoop.

## Ervaringen en paginaontwerpen {#section_B806FB752EC1470784755C1EB3D4AC70}

Een ervaring, ook wel een recept genoemd, definieert de inhoud die op uw pagina wordt weergegeven, en andere pagina-elementen, zoals koppelingen.

Een ervaring bepaalt welke aanbiedingen op een bepaalde plaats tonen wanneer de specifieke het richten voorwaarden worden voldaan. De ervaring bepaalt bijvoorbeeld dat, wanneer een retourbezoeker uw site bezoekt, boven aan de pagina een aanbieding voor verzending over twee dagen wordt weergegeven. De ervaring bepaalt ook dat wanneer een eerste bezoeker de pagina bekijkt, een korting van 10% op dezelfde locatie wordt weergegeven.

Een ervaring bestaat uit de aanbiedingen, afbeeldingselementen of andere HTML-elementen (zoals koppelingen) die op de pagina worden weergegeven om de bezoeker naar het gewenste resultaat te sturen. [!DNL Target] combineert locaties, aanbiedingen en ervaringen om te bepalen welke inhoud tijdens een specifieke test op uw site wordt weergegeven.

Een ervaring kan ook een ander paginaontwerp zijn. Een ervaring kan bijvoorbeeld een set koppelingen boven aan de pagina bevatten, waarbij een andere ervaring verschillende koppelingen heeft of dezelfde koppelingen in een andere volgorde. Mogelijk wilt u testen of de ene afbeelding meer optilt dan de andere, of op een advertentie eerder boven aan de pagina of op een andere locatie wordt geklikt.

[!DNL Target] optimaliseert de ervaringen voor elk van uw bezoekers via uw digitale aanraakpunten en test verschillende ervaringen om te bepalen welke het meest succesvol zullen zijn. Door uw ervaringen zorgvuldig te richten, kunt u ervoor zorgen dat uw bezoekers van de site de meest relevante aanbiedingen op de juiste locaties op uw pagina zien, waardoor uw kans op een succesvol bezoek groter wordt.

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

Een *ervaring* bepaalt welke inhoudsvertoningen wanneer de bijzondere voorwaarden worden voldaan.

## Soorten publiek {#section_3F32DA46BDF947878DD79DBB97040D01}

Optimaliseer uw gerichte inhoud aan activiteiteningangen die aan specifieke criteria voldoen.

Het publiek bepaalt het doel voor uw activiteit en wordt gebruikt overal waar het richten beschikbaar is.

[!DNL Target] publiek is een gedefinieerde set bezoekerscriteria. Aanbiedingen kunnen worden gericht op specifieke doelgroepen (of segmenten). Alleen bezoekers die bij dat publiek horen, zien de ervaring die voor hen is bedoeld.

U kunt een activiteit bijvoorbeeld richten op een publiek dat bestaat uit bezoekers die een bepaalde browser of een bepaald besturingssysteem gebruiken.

Uw activiteit kan ook gericht zijn op bezoekers uit een bepaald geografisch gebied of op personen die uw pagina openen vanuit een bepaald zoekprogramma.

Soorten publiek kan worden opgeslagen voor hergebruik in meerdere activiteiten, of ze kunnen worden gemaakt voor een bepaalde activiteit.

| Type publiek | Beschrijving |
|--- |--- |
| Herbruikbaar publiek | Herbruikbare doelgroepen kunnen voor elke activiteit worden geselecteerd. Als u een van deze soorten publiek wijzigt, verandert dit voor alle activiteiten die het gebruiken. |
| Aangepaste segmenten | De segmenten van de douane (die ook als campagne-specifieke segmenten worden bekend) zijn specifiek voor een campagne in Klassiek van het Doel. Ze worden gemaakt als onderdeel van de campagne en kunnen niet opnieuw worden gebruikt in andere campagnes. |
| Gedeeld publiek | Soorten publiek kan worden gedeeld door [!DNL Adobe Experience Cloud] -oplossingen. Zie [&#x200B; Soorten publiek &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=nl-NL) voor voorbeelden. |

Voor informatie over hoe het profiel van de bezoeker informatie over bezoekers aan uw plaats volgt, zie [&#x200B; Profielen van de Bezoeker &#x200B;](/help/main/c-target/c-visitor-profile/visitor-profile.md#concept_5E53D1A6DF224D7BAE76F4AE390B9DA1).

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### De Types van activiteit (9 :03) ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium] .

* Beschrijf de typen activiteiten die zijn opgenomen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Het gebruiken van Soorten publiek in Adobe Target (6 :21) ![&#x200B; de badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

In deze video wordt uitgelegd hoe u het publiek in [!DNL Target Standard/Premium] kunt gebruiken.

* Verklaar de term &quot;Publiek&quot;
* Verklaar de twee manieren waarop het publiek voor optimalisering wordt gebruikt
* Soorten publiek zoeken in de lijst Soorten publiek
* Een activiteit toewijzen aan een publiek
* Gebruik publiek voor passieve rapportage in een activiteit

>[!VIDEO](https://video.tv.adobe.com/v/17398)
