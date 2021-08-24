---
keywords: Adobe Experience Platform Web SDK;aep web sdk;web sdk;sdk;adobe Experience cloud;platform edge network;adobe Experience platform edge network;edge network;aep edge network
description: Leer hoe u de SDK van Adobe Experience Platform Web kunt gebruiken om via het AEP Edge Network te communiceren met de verschillende services in de Adobe Experience Cloud.
title: Hoe voer ik met het Web SDK van het Experience Platform uit?
feature: AEP Web SDK
role: Developer
exl-id: afcd741f-bb7e-4bc2-b96c-ec10d5d6f4c5
source-git-commit: eddde1bae345e2e28ca866662ba9664722dedecd
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Adobe Experience Platform Web SDK

[!DNL Adobe Experience Platform Web SDK] (AEP Web SDK) is een client-side JavaScript-bibliotheek waarmee klanten kunnen communiceren  [!DNL Adobe Experience Cloud] met de verschillende services in de Experience Cloud (inclusief  [!DNL Target]) via de  [!UICONTROL Adobe Experience Platform Edge Network]. Naast de JavaScript-bibliotheek is er een extensie [!DNL Adobe Experience Platform] voor hulp bij uw Web SDK-configuraties.

Raadpleeg de volgende koppelingen in de Help van *Adobe Experience Platform Web SDK* voor meer informatie:

* Voor uitgebreide informatie: [Wat is Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)
* Voor specifieke informatie over [!DNL Target]: [Doeloverzicht](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html)

## Aanbevolen documentatie

Naast de bovenstaande [!DNL Platform Web SDK] documentatie, hebben onderwerpen in deze handleiding ook specifieke informatie over [!DNL Platform Web SDK] omdat deze betrekking heeft op [!DNL Target] functies en functionaliteit.

| Functie | Beschrijving/koppeling |
| --- | --- |
| [Activiteit QA](/help/c-activities/c-activity-qa/activity-qa.md) | Gebruik QA URLs in [!DNL Adobe Target] om gemakkelijke activiteit QA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft. [!UICONTROL Activity QA] Hiermee kunt u uw  [!DNL Target] activiteiten volledig testen voordat u ze live start.<br>Zie  [Doelcompatibiliteit met de JavaScript-bibliotheek in QA-modus en URL&#39;s met ](/help/c-activities/c-activity-qa/activity-qa.md#compatibility) voorvertoningen [ ](/help/c-activities/c-activity-qa/activity-qa.md#preview). |
| [[!UICONTROL Analytics for Target] (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) | [!DNL Adobe Analytics for Target] (A4T) is een integratie met meerdere oplossingen waarmee u activiteiten kunt maken op basis van  [!DNL Analytics] conversiemetriek en publiekssegmenten. Met de integratie A4T kunt u [!DNL Analytics]-rapporten gebruiken om uw resultaten te bekijken.<br>Zie  [Ondersteunde ](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) typen activiteiten en stappen voor  [implementatie voor een Adobe Experience Platform Web SDK-implementatie](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#platform). |
| [Soorten publiek](/help/c-target/target.md) | Het publiek in [!DNL Adobe Target] bepaalt wie inhoud en ervaringen in een gerichte activiteit ziet.<br>Zie  [De ](/help/c-target/c-audiences/audiences.md#use-list) lijst Soorten publiek gebruiken  [Meerdere soorten publiek](/help/c-target/combining-multiple-audiences.md) combineren. |
| [Aanbiedingen omleiden - Veelgestelde vragen A4T](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md) | Met omleidingsvoorstellen leiden bezoekersbrowsers om naar een nieuwe pagina.<br>Zie  [Verleidt  [!DNL Adobe Experience Platform Web SDK] de steun aanbiedingen voor A4T om?](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#platform) |
| [Reactietokens](/help/administrating-target/response-tokens.md) | Met responstokens kunt u doelgegevens verzenden naar Google Analytics en andere integratie van derden.<br>Zie het  [Verzenden van gegevens naar Google Analytics via het Web ](/help/administrating-target/response-tokens.md#platform-web-sdk) SDK van het Platform om een codesteekproef van te zien hoe te om deze taak te verwezenlijken. |
| [De ](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/spa-implementation.html?lang=en) implementatie van de enig-paginatoepassing in de  *Platform* overviewguide van SDK van het Web. | [!UICONTROL Adobe Experience Platform Web SDK] biedt rijke functies die uw bedrijf uitrusten om personalisatie uit te voeren op de volgende generatie, clienttechnologieën zoals single-page toepassingen (SPA). |
| [De encryptieveranderingen van TLS (de Veiligheid van de Laag van het Vervoer)](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md) | TLS (de Veiligheid van de Laag van het Vervoer) helpt u de hoogste veiligheidsnormen handhaven en de veiligheid van klantengegevens bevorderen. |
