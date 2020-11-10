---
keywords: at.js integration;supported integrations;unsupported integrations;third party integrations
description: Informatie over gemeenschappelijke integratie met Doel en hun steunstatus met at.js.
title: at.js-integratie
feature: client-side
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---


# at.js-integratie{#at-js-integrations}

Informatie over gemeenschappelijke integratie met [!DNL Target] en hun steunstatus met at.js.

Neem contact op met uw accountvertegenwoordiger of consultant als u een dwingende behoefte hebt aan integratie die hier niet wordt ondersteund of vermeld.

## Ondersteunde integratie {#section_3B44A970D3FB42D1973701452C868B55}

| Integratie | Details |
|--- |--- |
| Analyses voor doel (A4T) | Zie [Adobe Analytics als de Rapportagebron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). |
| Profielen en soorten publiek (P&amp;A) | Zie [Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) in de Gebruikershandleiding *voor* Core Services. |
| Experience Cloud ID-service | Raadpleeg de documentatie [bij de](https://experienceleague.adobe.com/docs/id-service/using/home.html)Adobe Experience Cloud ID Service. |
| Adobe starten | Starten is het platform voor tagbeheer van de volgende generatie van Adobe en is de voorkeursmethode voor het implementeren van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.  Zie Doel [implementeren met Adobe starten](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25). |
| Dynamisch tagbeheer (DTM) | Zie de [Beste praktijken voor het Uitvoeren van Doel Gebruikend Dynamische gids](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html)van het Beheer van de Markering.   Belangrijk: [De Lancering](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25) van Adobe is de aangewezen, bijgewerkte methode voor het uitvoeren van Doel en de bibliotheek at.js. Gebruik Starten voor nieuwe doelimplementaties. De volgende handleiding is bedoeld voor bestaande clients die een DTM-implementatie gebruiken.   Houd rekening met het volgende wanneer u een DTM-integratie gebruikt: <ul><li>Bibliotheekbeheer: Gebruik de optie Aangepast als host om at.js te gebruiken. &quot;Automatisch&quot; beheer wordt momenteel niet ondersteund. </li></ul> |
| Adobe Experience Manager (AEM) Cloud Service | De AEM Cloud Service maakt het mogelijk om A/B-tests en activiteiten op het gebied van ervaring te maken binnen de AEM workflow. Ondersteunt at.js met Adobe Experience Manager 6.2 met FP-11577 (of later). Zie [Integreren met Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) en selecteer uw AEM versie voor meer informatie. |
| Fragmenten voor AEM | Met de fragmenten van de ervaring die in AEM in de activiteiten van het Doel worden gecreeerd, kunt u het gebruiksgemak en de kracht van AEM combineren met de krachtige mogelijkheden van de Automated Intelligence (AI) en het Leren van de Machine (ML) in Doel om ervaringen bij schaal te testen en te personaliseren.  AEM brengt al uw inhoud en middelen in een centrale plaats samen om uw verpersoonlijkingsstrategie te voeden. Met AEM kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder dat u code hoeft te schrijven. Het is niet nodig om pagina&#39;s te maken voor elk apparaat. AEM past automatisch elke ervaring aan met uw inhoud.  Zie [AEM ervaringsfragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8). |

## Niet-ondersteunde integratie {#section_8EFCAED418DC42E0B07F95924819EAC2}

| Integratie | Details |
|--- |--- |
| [!DNL Legacy Target to SiteCatalyst Integration] | Dit was de integratie die campagne- en recept-id&#39;s naar [!DNL SiteCatalyst] via de paginaoproep verstuurde zodat u rapportage in de [!DNL SiteCatalyst] gebruikersinterface kon doen. Deze functionaliteit wordt vervangen door A4T. |
| [!DNL Legacy Target to SiteCatalyst Integration] | Dit was de integratie die mbox genoemde vraag maakte `"SiteCatalyst: Event"` en `"SiteCatalyst: Purchase"` zodat kon u succesmetriek en gebruikersprofielen bouwen die op gebeurtenissen en steunen worden gebaseerd. Deze functionaliteit wordt vervangen door A4T en P&amp;A. |
| [!DNL Legacy Audience Manager (AAM) to Target Integration] | Dit was de integratie die een front-end API vraag maakte om AAM segmenten terug te winnen en hen toen als mbox parameters op elke mbox vraag op de pagina verzond. |

## Integraties van derden {#section_EE599839CCAD49DD97640E5EDAD9082E}

| Integratie | Details |
|--- |--- |
| Andere tagmanagers | at.js zou met niet-Adobe markeringsbeheerplatforms moeten werken, maar ben zorgvuldig het gebruiken van de eigenschappen van de douaneintegratie die andere verkopers hebben ontwikkeld. Hun integratie zou van interne mbox.js functies afhankelijk kunnen zijn die niet meer in at.js bestaan. |
| Externe gegevensleveranciers (bv. Demandbase, Bluekai, weer-API&#39;s) | Veel gegevensproviders van derden die worden gebruikt als aanvulling op de gebruikerprofilering van Target kunnen worden geïntegreerd met de functie [Data Providers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers) at.js. |