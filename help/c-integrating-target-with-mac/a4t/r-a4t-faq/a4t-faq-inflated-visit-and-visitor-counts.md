---
keywords: faq;veelgestelde vragen;analyses voor doel;a4T;opgeblazen;bezoek;bezoeker;gedeeltelijke hit;wees;wees;gedeeltelijk geraakt
description: Dit onderwerp bevat antwoorden op vragen die vaak over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.
title: Opgeblazen aantal bezoekers en bezoekers - A4T veelgestelde vragen
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---


# Opgeblazen bezoek en aantal bezoekers - A4T veelgestelde vragen{#inflated-visit-and-visitor-counts-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.

## Waarom tonen mijn gegevens van Analytics bezoeken die geen paginameningen of andere veranderlijke waarden hebben? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Wanneer [!DNL Adobe Analytics] wordt gebruikt om [!DNL Target] activiteiten (genoemd A4T) te meten, [!DNL Analytics] verzamelt extra gegevens die niet beschikbaar zijn wanneer er geen [!DNL Target] activiteit op de pagina is. Dit is omdat de [!DNL Target] activiteit een vraag bij de bovenkant van de pagina in brand brengt, maar [!DNL Analytics] typisch zijn vraag van de gegevensinzameling bij de bodem van de pagina in brand. Bij de implementatie van A4T tot op heden, omvatten wij deze extra gegevens wanneer een [!DNL Target] activiteit actief was.

Zie [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren voor meer informatie.

## Wat wordt een partiële-gegevenshit? {#section_59A203E289564576BF6821F96B0B9E11}

Er treden gedeeltelijke-gegevenshit op wanneer een [!DNL Target]-tag boven aan de pagina wordt geactiveerd maar een [!DNL Analytics]-tag onder aan de pagina niet wordt geactiveerd. Er zijn verschillende redenen waarom dit gebeurt. In de [!DNL A4T] implementatie tot op heden, omvatten wij gedeeltelijke gegevens over deze resultaten wanneer een [!DNL Target] activiteit actief was. In de toekomst worden deze aanvullende gegevens alleen opgenomen wanneer zowel de [!DNL Target]- als [!DNL Analytics]-tag zijn geactiveerd.

Zie [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren voor meer informatie.

## Ik zie een piek in bezoeken. Hoe kan ik zien of dit veroorzaakt werd door partieel-data-hits? {#section_28506672C6224ED18AC74F6A02F6F811}

U kunt [Adobe de Zorg van de Klant ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) contacteren om een Gedeeltelijk Rapport van Gegevens terug te winnen. Deze informatie is niet direct beschikbaar in [!DNL Analytics] UI.

## Wat zijn de potentiële oorzaken van partieel-gegevens klappen? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Gedeeltelijke-gegevenscontroles zijn vaak het resultaat van onjuiste implementatie, zoals onjuist uitgelijnde rapportsuite-id&#39;s. Er zijn ook legitieme oorzaken, zoals trage pagina&#39;s, paginafouten, omleidingsaanbiedingen in een activiteit of verouderde bibliotheekversies.

Voor meer informatie, zie &quot;wat tot Gedeeltelijke Gegevens&quot;in [Minimaliserend Geopend Bezoek en Tellingen van de Bezoeker in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) bijdraagt.

## Ik heb gedeeltelijke data-hits. Wat kan ik doen om mijn gegevens op te schonen? {#section_CBE778A9D07A469E8FF98F68BACC7124}

U kunt een virtuele rapportsuite maken om historische gedeeltelijke gegevens uit te sluiten van uw rapporten.

Voor meer informatie, zie &quot;hoe ik Historische trends zonder Gedeeltelijke gegevens kan bekijken?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

## Kan ik iets doen om te voorkomen dat mijn pagina&#39;s resultaten met gedeeltelijke gegevens genereren? {#section_4B00E7E618444BE98A0798DE98F08B21}

Na 14 november 2016 nemen we alleen gegevens op wanneer zowel de tag [!DNL Target] als [!DNL Analytics] zijn geactiveerd. Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, en u hen van uw rapporten zou willen uitsluiten, kunt u een virtuele rapportreeks tot stand brengen, zoals die in &quot;hoe kan ik Historische Trends zonder Gedeeltelijke Gegevens bekijken?&quot;wordt verklaard in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

Er zijn ook stappen die u kunt uitvoeren om ongewenste resultaten met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

## Als gegevens die gedeeltelijk door gegevens worden geraakt, uit de rapportage worden verwijderd, verliezen we dan geen waardevolle doel- of analysegegevens? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Door gedeeltelijke gegevens op te nemen in [!DNL Analytics]-rapportage wordt aanvullende informatie verschaft, wat ook inconsistentie creëert met historische gegevens uit perioden waarin geen [!DNL Target]-activiteiten werden uitgevoerd. Dit kan problemen veroorzaken voor [!DNL Analytics] gebruikers die tendensen in tijd analyseren.

Er zijn stappen die u kunt uitvoeren om hits met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

## Zijn er om het even welke specifieke soorten activiteiten van het Doel die eerder gedeeltelijk-gegevensklappen zullen veroorzaken? {#section_69837442A9B84366BEFDA4588B31E574}

Met de omleidingsaanbiedingen wordt een gebruiker direct naar een andere pagina gestuurd. Dit betekent dat de [!DNL Analytics]-aanroep niet op de eerste pagina wordt afgespeeld.
