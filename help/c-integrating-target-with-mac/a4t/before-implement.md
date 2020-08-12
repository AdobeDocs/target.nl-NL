---
keywords: Recommendations
description: Verscheidene veranderingen komen in uw proces van de gegevensinzameling voor wanneer het toelaten van Analytics als rapporteringsbron voor Doel (A4T).
title: Voordat u Adobe Analytics implementeert als rapportagebron voor Adobe Target (A4T)
feature: null
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---


# Voordat u implementeert{#before-you-implement}

Verscheidene veranderingen komen in uw proces van de gegevensinzameling voor wanneer het toelaten [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

Voordat u besluit om deze integratie te gebruiken, moet u de volgende secties doornemen en de gevolgen voor uw rapportageprocessen in overweging nemen:

## Implementatievereisten {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen dat uw account wordt ingericht voor de integratie. Gebruik [dit formulier](https://www.adobe.com/go/audiences) om provisioning aan te vragen.

Deze integratie A4T vereist dat u de volgende (of nieuwere) bibliotheekversies uitvoert, afhankelijk van of u redirect aanbiedingen met A4T of niet wilt gebruiken:

### Vereisten indien *geen* omleidingsaanbiedingen met A4T worden gebruikt

Deze integratie vereist dat u de volgende (of nieuwere) bibliotheekversies implementeert als u niet van plan bent om aanbiedingen om te leiden met A4T. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 1.8.0
* [!DNL Adobe Target] (afhankelijk van uw implementatie): at.js versie 0.9.1 of mbox.js versie 61
* Adobe Analytics: appMeasurement.js versie 1.7.0

### Vereisten die nodig zijn bij het gebruik van omleidingsaanbiedingen met A4T

Als u omleidingsaanbiedingen met A4T wilt gebruiken, moet u de volgende (of nieuwere) bibliotheekversies implementeren. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 2.3.0
* [!DNL Adobe Target]: at.js versie 1.6.2

   **Opmerking:** De bibliotheek mbox.js ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet at.js gebruiken.

* Adobe Analytics: appMeasurement.js versie 2.1

Download- en implementatieinstructies worden vermeld in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Wat u moet weten voordat u gaat implementeren {#section_50D49CC52E11414089C89FB67F9B88F5}

* Deze integratie wordt toegelaten op nieuwe activiteiten wanneer u om als rapporteringsbron selecteert te gebruiken [!DNL Analytics] . Nadat u de implementatiewijzigingen hebt aangebracht die in dit document worden beschreven, heeft dit geen invloed op uw bestaande activiteiten.
* Het proces van vestiging [!DNL Analytics] als rapporteringsbron voor [!DNL Target] omvat verscheidene implementatiestappen, die door een leveringsstap worden gevolgd. Het is een goed idee om het hieronder beschreven proces te doorlopen alvorens uit te voeren. Nadat u deze stappen hebt uitgevoerd, kunt u deze gebruiken [!DNL Analytics] als rapportbron zodra deze voor u is ingeschakeld. Het inrichtingsproces kan maximaal vijf werkdagen in beslag nemen.
* De [!DNL Visitor ID service] server maakt een gedeelde [!DNL Visitor ID] over de [!DNL Adobe Experience Cloud]. Hoewel deze de id [!DNL Target] mboxPC of [!DNL Audience Manager] UUID niet vervangt, vervangt deze de manier waarop nieuwe bezoekers worden [!DNL Analytics] geïdentificeerd. Als de site op de juiste wijze is ingesteld, moeten de terugkerende [!DNL Analytics] bezoekers ook met hun oude [!DNL Analytics] id worden geïdentificeerd om te voorkomen dat bezoekers worden geknipt. En omdat de [!DNL Target] mboxPCid intact blijft, gaan er geen gegevens van het [!DNL Target] bezoekersprofiel verloren wanneer u een upgrade uitvoert naar de [!DNL Visitor ID service].
* Het [!DNL Visitor ID service] moet vóór uw [!DNL Analytics] en [!DNL Target] paginacode worden uitgevoerd. Zorg ervoor dat dit boven de labels voor alle andere `VisitorAPI.js` [!DNL Experience Cloud] oplossingen wordt weergegeven.

## Latentie {#section_9489BE6FD21641A4844E591711E3F813}

Nadat deze integratie is ingeschakeld, hebt u nog 5 tot 10 minuten vertraging nodig [!DNL Analytics]. Door deze latentieverhoging kunnen gegevens van [!DNL Analytics] en [!DNL Target] worden opgeslagen op dezelfde hit, zodat u activiteiten kunt onderverdelen op pagina en sitesectie.

Deze stijging wordt weerspiegeld in alle [!DNL Analytics] diensten en hulpmiddelen, met inbegrip van live-stream en real-time rapportering, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentieverhoging begint nadat u de service [!DNL Experience Cloud] bezoekersidentiteitskaart hebt geïmplementeerd, zelfs als u deze integratie niet volledig hebt geïmplementeerd.

## Aanvullende id {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] vraag die door een activiteit A4T wordt gebruikt om inhoud te leveren of het doel te registreren metrisch moet een overeenkomstige [!DNL Analytics] slag hebben die zelfde supplementaire identiteitskaart voor A4T deelt om behoorlijk te werken.

Hits die gegevens van bevatten [!DNL Analytics] en een extra gegevens-identiteitskaart [!DNL Target] bevatten. U kunt deze id in Foutopsporing [van](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) Adobe Experience Cloud zien als de `sdid` parameter. Bijvoorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Deze id wordt op elk moment gegenereerd wanneer aan de volgende criteria wordt voldaan:

* De service voor bezoekersidentiteitskaart is geïmplementeerd
* Er wordt een versie geïmplementeerd van [!DNL mbox.js] die deze integratie ondersteunt.

Zorg er bij het oplossen van problemen voor dat de aanvullende id aanwezig is bij [!DNL Analytics] treffers.

## Logboekregistratie voor clientanalyse {#client-side}

Wanneer at.js, de [!DNL Experience Cloud Visitor ID Service], en appMeasurement.js op de pagina staan, [!DNL Analytics] en [!DNL Target] sluit gebeurtenissen voor rapportage- en analysedoeleinden standaard correct op de achtergrond zolang de juiste aanvullende id van de pagina is opgenomen, zoals hierboven vermeld. U hoeft geen extra bewerkingen te beheren en uit te voeren om A4T correct te laten werken.

Er zijn echter gevallen waarin u meer controle wilt hebben over wanneer en hoe u analysegegevens wilt verzenden die betrekking hebben [!DNL Target] op [!DNL Analytics] rapportagedoeleinden. U hebt mogelijk een intern analyseprogramma dat u gebruikt voor interne doeleinden, maar u wilt de analysegegevens ook [!DNL Analytics] via uw interne analyseproduct verzenden, zodat andere leden van uw organisatie [!DNL Analytics] als visuele rapportbron kunnen blijven gebruiken. Zie [stap 7: Verwijzing om.js of mbox.js op alle plaatspagina](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) &#39;s in *Analytics voor de Implementatie* van het Doel voor meer informatie.
