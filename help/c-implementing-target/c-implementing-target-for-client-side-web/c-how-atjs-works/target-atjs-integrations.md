---
keywords: at.js integratie;ondersteunde integratie;niet-ondersteunde integratie;integratie van derden
description: Zie de integratie die door Adobe [!DNL Target] at.js, including Analytics for [!DNL Target]  (A4T), de Dienst van Experience Cloud identiteitskaart, en meer wordt gesteund.
title: Welke integraties worden door at.js ondersteund?
feature: at.js
role: Developer
exl-id: 148c744d-2a2b-40f8-964b-c51283ae7d1c
source-git-commit: eddde1bae345e2e28ca866662ba9664722dedecd
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# at.js-integratie

Informatie over gemeenschappelijke integratie met [!DNL Target] en hun steunstatus met at.js.

Neem contact op met uw accountvertegenwoordiger of consultant als u een dwingende behoefte hebt aan integratie die hier niet wordt ondersteund of vermeld.

## Ondersteunde integratie {#section_3B44A970D3FB42D1973701452C868B55}

| Integratie | Details |
|--- |--- |
| Analyses voor doel (A4T) | Zie [Adobe Analytics als de rapportbron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE). |
| Profielen en soorten publiek (P&amp;A) | Zie [Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) in de *Gebruikershandleiding voor kernservices*. |
| Experience Cloud ID-service | Zie de [Adobe Experience Cloud ID Service documentation](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| Tags in [!DNL Adobe Experience Platform] | Tags in [!DNL Adobe Experience Platform] zijn de volgende generatie mogelijkheden voor tagbeheer van [!DNL Adobe]. Met labels kunnen klanten op eenvoudige wijze de analytische, marketing- en advertentietags implementeren en beheren die nodig zijn om relevante klantervaringen mogelijk te maken. Zie [Implementeren [!DNL Target] met [!DNL Adobe Experience Platform]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#topic_5234DDAEB0834333BD6BA1B05892FC25). |
| Adobe Experience Manager (AEM) Cloud Service | De AEM Cloud Service maakt het mogelijk om A/B-tests en activiteiten op het gebied van ervaring te maken binnen de AEM workflow. Ondersteunt at.js met Adobe Experience Manager 6.2 met FP-11577 (of later). Zie [Integreren met Adobe Target](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/target.html) en selecteer uw AEM versie voor meer informatie. |
| Fragmenten voor AEM | Met de fragmenten van de ervaring die in AEM in de activiteiten van het Doel worden gecreeerd, kunt u het gebruiksgemak en de kracht van AEM combineren met de krachtige mogelijkheden van de Automated Intelligence (AI) en het Leren van de Machine (ML) in Doel om ervaringen bij schaal te testen en te personaliseren.  AEM brengt al uw inhoud en middelen in een centrale plaats samen om uw verpersoonlijkingsstrategie te voeden. Met AEM kunt u eenvoudig inhoud voor desktops, tablets en mobiele apparaten op één locatie maken zonder dat u code hoeft te schrijven. Het is niet nodig om pagina&#39;s te maken voor elk apparaat. AEM past automatisch elke ervaring aan met uw inhoud.  Zie [AEM ervaren fragmenten](/help/c-experiences/c-manage-content/aem-experience-fragments.md#topic_1E1E4EA01F074349B2CF8785387B5FE8). |

## Niet-ondersteunde integratie {#section_8EFCAED418DC42E0B07F95924819EAC2}

| Integratie | Details |
|--- |--- |
| [!DNL Legacy Target to SiteCatalyst Integration] | Dit was de integratie die campagne en recept ids naar [!DNL SiteCatalyst] via de paginavraag verzendt zodat kon u rapportering in [!DNL SiteCatalyst] UI doen. Deze functionaliteit wordt vervangen door A4T. |
| [!DNL Legacy Target to SiteCatalyst Integration] | Dit was de integratie die mbox vraag genoemd `"SiteCatalyst: Event"` en `"SiteCatalyst: Purchase"` maakte zodat kon u succesmetriek en gebruikersprofielen bouwen die op gebeurtenissen en steunen worden gebaseerd. Deze functionaliteit wordt vervangen door A4T en P&amp;A. |
| [!DNL Legacy Audience Manager (AAM) to Target Integration] | Dit was de integratie die een front-end API vraag maakte om AAM segmenten terug te winnen en hen toen als mbox parameters op elke mbox vraag op de pagina verzond. |

## Integraties van derden {#section_EE599839CCAD49DD97640E5EDAD9082E}

| Integratie | Details |
|--- |--- |
| Andere tagmanagers | at.js zou met niet-Adobe markeringsbeheerplatforms moeten werken, maar ben zorgvuldig het gebruiken van de eigenschappen van de douaneintegratie die andere verkopers hebben ontwikkeld. Hun integratie zou van interne mbox.js functies afhankelijk kunnen zijn die niet meer in at.js bestaan. |
| Externe gegevensleveranciers (bv. Demandbase, Bluekai, weer-API&#39;s) | Veel gegevensproviders van derden die worden gebruikt als aanvulling op de gebruikerprofilering van Target, kunnen worden geïntegreerd met de functie at.js [Data Providers](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md#data-providers). |
