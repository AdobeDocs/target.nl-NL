---
keywords: faq;veelgestelde vragen;analyses voor doel;a4T;opgeblazen;bezoek;bezoeker;gedeeltelijke hit;wees;wees;gedeeltelijk geraakt
description: Vind antwoorden op vragen over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics voor [!DNL Target] (A4T). Leer hoe u "gedeeltelijke gegevens" minimaliseert.
title: Waar kan ik Veelgestelde vragen over de Inflated Visit en de Tellingen van de Bezoeker met A4T vinden?
feature: Analyses voor doel (A4T)
exl-id: e936b1f6-dc72-4ab2-9bb5-169d1710edbe
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Opgeblazen bezoek en aantal bezoekers - A4T Veelgestelde vragen

Dit onderwerp bevat antwoorden op vragen die vaak over opgeblazen bezoek en bezoekersaantallen wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.

## Waarom tonen mijn gegevens van Analytics bezoeken die geen paginameningen of andere veranderlijke waarden hebben? {#section_4D8C2C2D766842E6B12F3ECC774A64D5}

Wanneer [!DNL Adobe Analytics] wordt gebruikt om [!DNL Target] activiteiten (genoemd A4T) te meten, [!DNL Analytics] gegevens verzamelt die niet beschikbaar zijn wanneer er geen [!DNL Target] activiteit op de pagina is. Dit is omdat de [!DNL Target] activiteit een vraag bij de bovenkant van de pagina in brand brengt, maar [!DNL Analytics] typisch zijn vraag van de gegevensinzameling bij de bodem van de pagina in brand. Bij de implementatie van A4T tot op heden, omvat Adobe deze extra gegevens wanneer een [!DNL Target] activiteit actief was.

Zie [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren voor meer informatie.

## Wat wordt een partiële-gegevenshit? {#section_59A203E289564576BF6821F96B0B9E11}

Er treden gedeeltelijke-gegevenshit op wanneer een [!DNL Target]-tag boven aan de pagina wordt geactiveerd maar een [!DNL Analytics]-tag onder aan de pagina niet wordt geactiveerd. Er zijn verschillende redenen waarom deze situatie zich voordoet. In de [!DNL A4T] implementatie tot op heden, omvat Adobe gedeeltelijke gegevens over deze resultaten wanneer een [!DNL Target] activiteit actief was. Als u doorgaat, neemt Adobe deze aanvullende gegevens alleen op wanneer zowel de tag [!DNL Target] als [!DNL Analytics] zijn geactiveerd.

Zie [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren voor meer informatie.

## Ik zie een piek in bezoeken. Hoe kan ik zeggen of deze bezoeken veroorzaakt worden door gedeeltelijke data-treffers? {#section_28506672C6224ED18AC74F6A02F6F811}

U kunt [Adobe de Zorg van de Klant ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) contacteren om een Gedeeltelijk Rapport van Gegevens terug te winnen. Deze informatie is niet direct beschikbaar in [!DNL Analytics] UI.

## Wat zijn de potentiële oorzaken van partieel-gegevens klappen? {#section_C4BB9925CE6444BE8CB9FBEFE5085546}

Gedeeltelijke-gegevenscontroles zijn vaak het resultaat van onjuiste implementatie, zoals onjuist uitgelijnde rapportsuite-id&#39;s. Er zijn ook legitieme oorzaken, zoals trage pagina&#39;s, paginafouten, omleidingsaanbiedingen in een activiteit of verouderde bibliotheekversies.

Voor meer informatie, zie &quot;wat tot Gedeeltelijke Gegevens&quot;in [Minimaliserend Geopend Bezoek en Tellingen van de Bezoeker in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) bijdraagt.

## Ik heb gedeeltelijke data-hits. Wat kan ik doen om mijn gegevens op te schonen? {#section_CBE778A9D07A469E8FF98F68BACC7124}

U kunt een virtuele rapportsuite maken om historische gedeeltelijke gegevens uit te sluiten van uw rapporten.

Voor meer informatie, zie &quot;hoe ik Historische trends zonder Gedeeltelijke gegevens kan bekijken?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

## Kan ik iets doen om te voorkomen dat mijn pagina&#39;s resultaten met gedeeltelijke gegevens genereren? {#section_4B00E7E618444BE98A0798DE98F08B21}

Na 14 november 2016 neemt Adobe alleen gegevens op wanneer zowel de tag [!DNL Target] als [!DNL Analytics] zijn geactiveerd. Deze wijziging is niet met terugwerkende kracht. Als uw historische rapporten opgeblazen aantallen tonen, kunt u hen van uw rapporten uitsluiten door een virtuele rapportreeks te creëren. Zie &quot;Hoe kan ik historische trends zonder gedeeltelijke gegevens bekijken?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

Er zijn ook stappen die u kunt uitvoeren om ongewenste resultaten met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

## Verlies ik dan geen waardevolle [!DNL Target]- of analysegegevens als gegevens die gedeeltelijk door gegevens zijn geraakt, uit de rapportage worden verwijderd? {#section_EBC39E8A0F6A40E58F51E776936F7D9E}

Het opnemen van gedeeltelijke gegevens in [!DNL Analytics]-rapportage biedt weliswaar aanvullende informatie, maar creëert ook inconsistentie met historische gegevens uit perioden waarin geen [!DNL Target]-activiteiten werden uitgevoerd. Het opnemen van gegevens die gedeeltelijk worden geraakt, kan problemen veroorzaken voor [!DNL Analytics] gebruikers die tendensen in tijd analyseren.

Er zijn stappen die u kunt uitvoeren om hits met gedeeltelijke gegevens te minimaliseren. Voor meer informatie, zie &quot;wat de Beste praktijken zijn om Gedeeltelijke Gegevens te verminderen?&quot; in [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren.

## Zijn er om het even welke specifieke soorten [!DNL Target] activiteiten die eerder gedeeltelijke-gegevensklappen zullen veroorzaken? {#section_69837442A9B84366BEFDA4588B31E574}

Met de omleidingsaanbiedingen wordt een gebruiker direct naar een andere pagina gestuurd. Dit betekent dat de [!DNL Analytics]-aanroep niet op de eerste pagina wordt afgespeeld.
