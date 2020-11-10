---
keywords: faq;frequently asked questions;analytics for target;a4T;inflated;visit;visitor;partial hit;orphaned;orphan;partial-hit
description: Dit onderwerp bevat antwoorden op vragen die vaak over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.
title: Opgeblazen bezoek en aantal bezoekers - A4T Veelgestelde vragen
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---


# Opgeblazen bezoek en aantal bezoekers - A4T Veelgestelde vragen{#inflated-visit-and-visitor-counts-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.

## Waarom tonen mijn gegevens van Analytics bezoeken die geen paginameningen of andere veranderlijke waarden hebben? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Wanneer [!DNL Adobe Analytics] wordt gebruikt om [!DNL Target] activiteiten (genoemd A4T) te meten, [!DNL Analytics] verzamelt extra gegevens die niet beschikbaar zijn wanneer er geen [!DNL Target] activiteit op de pagina is. Dit is omdat de [!DNL Target] activiteit een vraag bij de bovenkant van de pagina in brand brengt, maar [!DNL Analytics] typisch zijn vraag van de gegevensinzameling bij de bodem van de pagina in brand. Bij de implementatie van A4T tot op heden, hebben wij deze extra gegevens opgenomen wanneer een [!DNL Target] activiteit actief was.

Voor meer informatie, zie het [Minimaliseren van de Inflated Tellingen van het Bezoek en van de Bezoeker in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Wat wordt een partiële-gegevenshit? {#section_59A203E289564576BF6821F96B0B9E11}

Er treedt een fout op met betrekking tot gedeeltelijke gegevens wanneer een [!DNL Target] tag boven aan de pagina wordt geactiveerd, maar er geen [!DNL Analytics] tag onder aan de pagina wordt geactiveerd. Er zijn verschillende redenen waarom dit gebeurt. In de [!DNL A4T] implementatie tot nu toe hebben we gedeeltelijke gegevens over deze resultaten opgenomen wanneer een [!DNL Target] activiteit actief was. Deze aanvullende gegevens worden alleen opgenomen wanneer de [!DNL Target] tags en de [!DNL Analytics] tags zijn geactiveerd.

Voor meer informatie, zie het [Minimaliseren van de Inflated Tellingen van het Bezoek en van de Bezoeker in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Ik zie een piek in bezoeken. Hoe kan ik zien of dit veroorzaakt werd door partieel-data-hits? {#section_28506672C6224ED18AC74F6A02F6F811}

U kunt contact opnemen met de klantenservice [van](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Adobe om een gedeeltelijk gegevensrapport op te halen. Deze informatie is niet rechtstreeks beschikbaar in de [!DNL Analytics] gebruikersinterface.

## Wat zijn de potentiële oorzaken van partieel-gegevens klappen? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Gedeeltelijke-gegevenscontroles zijn vaak het resultaat van onjuiste implementatie, zoals onjuist uitgelijnde rapportsuite-id&#39;s. Er zijn ook legitieme oorzaken, zoals trage pagina&#39;s, paginafouten, omleidingsaanbiedingen in een activiteit of verouderde bibliotheekversies.

Voor meer informatie, zie &quot;wat tot Gedeeltelijke Gegevens&quot;in het [Minimaliseren van Geinflateerde Bezoek en de Tellingen van de Bezoeker in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235)bijdraagt.

## Ik heb gedeeltelijke data-hits. Wat kan ik doen om mijn gegevens op te schonen? {#section_CBE778A9D07A469E8FF98F68BACC7124}

U kunt een virtuele rapportsuite maken om historische gedeeltelijke gegevens uit te sluiten van uw rapporten.

Voor meer informatie, zie &quot;hoe ik Historische trends zonder Gedeeltelijke gegevens kan bekijken?&quot; in [Minimizing Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Kan ik iets doen om te voorkomen dat mijn pagina&#39;s resultaten met gedeeltelijke gegevens genereren? {#section_4B00E7E618444BE98A0798DE98F08B21}

Na 14 november 2016 nemen we alleen gegevens op wanneer zowel de [!DNL Target] tag als de [!DNL Analytics] tag zijn geactiveerd. Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, en u hen van uw rapporten zou willen uitsluiten, kunt u een virtuele rapportreeks tot stand brengen, zoals die in &quot;hoe kan ik Historische Trends zonder Gedeeltelijke Gegevens bekijken?&quot;wordt verklaard in [Minimizing Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

Er zijn ook stappen die u kunt uitvoeren om ongewenste resultaten met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Minimizing Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Als gegevens die gedeeltelijk door gegevens worden geraakt, uit de rapportage worden verwijderd, verliezen we dan geen waardevolle doel- of analysegegevens? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Het opnemen van gedeeltelijke gegevens in de [!DNL Analytics] rapportage levert wel aanvullende informatie op, maar leidt ook tot inconsistentie met historische gegevens uit perioden waarin geen [!DNL Target] activiteiten werden uitgevoerd. Dit kan problemen veroorzaken voor [!DNL Analytics] gebruikers die tendensen in tijd analyseren.

Er zijn stappen die u kunt uitvoeren om hits met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Minimizing Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235).

## Zijn er om het even welke specifieke soorten activiteiten van het Doel die eerder gedeeltelijk-gegevensklappen zullen veroorzaken? {#section_69837442A9B84366BEFDA4588B31E574}

Met de optie Omleiden stuurt u aanbiedingen direct een gebruiker naar een andere pagina, wat betekent dat de [!DNL Analytics] oproep niet op de eerste pagina wordt afgespeeld.
