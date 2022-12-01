---
keywords: faq;veelgestelde vragen;analyses voor doel;a4T;opgepompt;bezoek;bezoeker;gedeeltelijke hit;wees;wees;gedeeltelijk geraakt
description: Vind antwoorden op vragen over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics voor [!DNL Target] (A4T). Leer hoe u "gedeeltelijke gegevens" minimaliseert.
title: Waar kan ik Veelgestelde vragen over de Inflated Visit en de Tellingen van de Bezoeker met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Opgeblazen bezoek en aantal bezoekers - A4T Veelgestelde vragen

Dit onderwerp bevat antwoorden op vragen die vaak over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.

## Waarom tonen mijn gegevens van Analytics bezoeken die geen paginameningen of andere veranderlijke waarden hebben? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

+++Antwoord wanneer [!DNL Adobe Analytics] wordt gebruikt om te meten [!DNL Target] activiteiten (genaamd A4T); [!DNL Analytics] verzamelt gegevens die niet beschikbaar zijn wanneer er geen [!DNL Target] activiteit op de pagina. Dit komt omdat de [!DNL Target] activiteit brengt een vraag bij de bovenkant van de pagina in brand, maar [!DNL Analytics] worden doorgaans onder aan de pagina aanroepen van de gegevensverzameling geactiveerd. Bij de implementatie van A4T tot op heden, omvat Adobe deze extra gegevens wanneer een [!DNL Target] activiteit was actief.

Zie voor meer informatie [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

+++

## Wat wordt een partiële-gegevenshit? {#section_59A203E289564576BF6821F96B0B9E11}

++ + Antwoord Een gedeeltelijk-gegevenshit komt voor wanneer een [!DNL Target] boven aan de pagina wordt de tag geactiveerd, maar een [!DNL Analytics] -tag onder aan de pagina wordt niet geactiveerd. Er zijn verschillende redenen waarom deze situatie zich voordoet. In de [!DNL A4T] tot op heden bevat Adobe gedeeltelijke gegevens over deze resultaten wanneer een [!DNL Target] activiteit was actief. Als u doorgaat, neemt Adobe deze aanvullende gegevens alleen op wanneer beide [!DNL Target] en [!DNL Analytics] tags zijn afgegaan.

Zie voor meer informatie [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

+++

## Ik zie een piek in bezoeken. Hoe kan ik zeggen of deze bezoeken veroorzaakt worden door gedeeltelijke data-treffers? {#section_28506672C6224ED18AC74F6A02F6F811}

++ + Antwoord U kunt contact opnemen [Adobe Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om een rapport van Gedeeltelijke Gegevens terug te winnen. Deze informatie is niet rechtstreeks beschikbaar in de [!DNL Analytics] UI.

+++

## Wat zijn de potentiële oorzaken van partieel-gegevens klappen? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

+++Antwoord Gedeeltelijke-gegevensklappen zijn vaak het resultaat van onjuiste implementatie, zoals onjuist uitgelijnde rapportsuite-id&#39;s. Er zijn ook legitieme oorzaken, zoals trage pagina&#39;s, paginafouten, omleidingsaanbiedingen in een activiteit of verouderde bibliotheekversies.

Voor meer informatie, zie &quot;wat tot Gedeeltelijke Gegevens&quot;bijdraagt in [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

+++

## Ik heb gedeeltelijke data-hits. Wat kan ik doen om mijn gegevens op te schonen? {#section_CBE778A9D07A469E8FF98F68BACC7124}

+++Antwoord U kunt een virtuele rapportreeks tot stand brengen om historische gedeeltelijke gegevens van uw rapporten uit te sluiten.

Voor meer informatie, zie &quot;hoe ik Historische trends zonder Gedeeltelijke gegevens kan bekijken?&quot; in [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

+++

## Kan ik iets doen om te voorkomen dat mijn pagina&#39;s resultaten met gedeeltelijke gegevens genereren? {#section_4B00E7E618444BE98A0798DE98F08B21}

+++Antwoord Na 14 november 2016, zal Adobe gegevens slechts omvatten wanneer allebei [!DNL Target] en [!DNL Analytics] tags zijn afgegaan. Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, kunt u hen van uw rapporten uitsluiten door een virtuele rapportreeks te creëren. Zie &quot;Hoe kan ik historische trends zonder gedeeltelijke gegevens bekijken?&quot; in [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

Er zijn ook stappen die u kunt uitvoeren om ongewenste resultaten met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

+++

## Als delen-gegeven-raakgegevens uit rapportering worden verwijderd, verlies ik waardevol niet [!DNL Target] of analysegegevens? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

+++Antwoord inclusief gedeeltelijke gegevens in [!DNL Analytics] rapportage verschaft wel aanvullende informatie, maar creëert ook inconsistentie met historische gegevens uit perioden waarin er geen [!DNL Target] activiteiten die worden uitgevoerd. Het opnemen van gegevens die gedeeltelijk worden geraakt, kan problemen veroorzaken voor [!DNL Analytics] gebruikers die trends in de loop der tijd analyseren.

Er zijn stappen die u kunt uitvoeren om hits met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Inflated Visit and Visitor Counts in A4T minimaliseren](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

+++

## Zijn er bepaalde soorten [!DNL Target] activiteiten die eerder gedeeltelijk-gegevensklappen zullen veroorzaken? {#section_69837442A9B84366BEFDA4588B31E574}

+++Aanbiedingen van Redirect Antwoord verzenden een gebruiker onmiddellijk naar een verschillende pagina, wat betekent [!DNL Analytics] de vraag niet op de eerste pagina brandt.

+++