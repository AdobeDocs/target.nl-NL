---
keywords: Recommendations
description: Verscheidene veranderingen komen in uw proces van de gegevensinzameling voor wanneer het toelaten van Analytics als rapporteringsbron voor Doel (A4T).
title: Voordat u Adobe Analytics implementeert als de rapportbron voor Adobe Target (A4T)
uuid: fe603a4b-bd61-49f4-b1b7-a0329aa905f5
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Voordat u implementeert{#before-you-implement}

Verscheidene veranderingen komen in uw proces van de gegevensinzameling voor wanneer het toelaten van Analytics als rapporteringsbron voor Doel (A4T).

Voordat u besluit om deze integratie te gebruiken, moet u de volgende secties doornemen en de gevolgen voor uw rapportageprocessen in overweging nemen:

## Implementatievereisten {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen dat uw account wordt ingericht voor de integratie. Gebruik [dit formulier](https://www.adobe.com/go/audiences) om provisioning aan te vragen.

Deze integratie A4T vereist dat u de volgende (of nieuwere) bibliotheekversies uitvoert, afhankelijk van of u redirect aanbiedingen met A4T of niet wilt gebruiken:

### Vereisten indien *geen* omleidingsaanbiedingen met A4T worden gebruikt

Deze integratie vereist dat u de volgende (of nieuwere) bibliotheekversies implementeert als u niet van plan bent om aanbiedingen om te leiden met A4T. De vermelde volgorde is de volgorde van de bewerkingen.

* Experience Cloud Visitor ID Service: bezoekerAPI.js versie 1.8.0
* Adobe Target (afhankelijk van uw implementatie): at.js versie 0.9.1 of mbox.js versie 61
* Adobe Analytics: appMeasurement.js versie 1.7.0

### Vereisten die nodig zijn bij het gebruik van omleidingsaanbiedingen met A4T

Als u omleidingsaanbiedingen met A4T wilt gebruiken, moet u de volgende (of nieuwere) bibliotheekversies implementeren. De vermelde volgorde is de volgorde van de bewerkingen.

* Experience Cloud Visitor ID Service: bezoekerAPI.js versie 2.3.0
* Adobe-doel: at.js versie 1.6.2

   **Opmerking:** De bibliotheek mbox.js ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet at.js gebruiken.

* Adobe Analytics: appMeasurement.js versie 2.1

Download- en implementatieinstructies worden vermeld in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Wat u moet weten voordat u gaat implementeren {#section_50D49CC52E11414089C89FB67F9B88F5}

* Deze integratie wordt toegelaten op nieuwe activiteiten wanneer u om Analytics als rapporteringsbron selecteert te gebruiken. Nadat u de implementatiewijzigingen hebt aangebracht die in dit document worden beschreven, heeft dit geen invloed op uw bestaande activiteiten.
* Het proces om Analytics als rapportbron voor Doel op te zetten omvat verscheidene implementatiestappen, die door een leveringsstap worden gevolgd. Het is een goed idee om het hieronder beschreven proces te doorlopen alvorens uit te voeren. Nadat u deze stappen hebt uitgevoerd, kunt u Analytics gebruiken als de rapportbron zodra dit voor u is ingeschakeld. Het inrichtingsproces kan maximaal vijf werkdagen in beslag nemen.
* Met de service Bezoeker-id maakt u een gedeelde bezoeker-id in de Experience Cloud. Hoewel deze de Target mboxPC-id of Audience Manager UUID niet vervangt, vervangt deze de manier waarop Analytics nieuwe bezoekers identificeert. Indien correct ingesteld, moeten terugkerende Analytics-bezoekers ook worden geïdentificeerd met hun oude Analytics-id om te voorkomen dat bezoekers worden geknipt. Op dezelfde manier, omdat het Doel mboxPCid intact blijft, worden geen gegevens van het het bezoekersprofiel van het Doel verloren wanneer u aan de dienst van identiteitskaart van de Bezoeker bevordert.
* De service voor bezoekersidentiteitskaart moet worden uitgevoerd voordat de code van de pagina Analytics en Target wordt uitgevoerd. Zorg ervoor dat dit boven de labels voor alle andere Experience Cloud-producten `VisitorAPI.js` wordt weergegeven.

## Latentie {#section_9489BE6FD21641A4844E591711E3F813}

Nadat deze integratie is ingeschakeld, wordt er een extra vertraging van 5 tot 10 minuten waargenomen in Adobe Analytics. Door deze latentieverhoging kunnen gegevens van Analytics en Target op dezelfde hit worden opgeslagen, zodat u tests kunt onderbreken op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle Adobe Analytics-services en -hulpprogramma&#39;s, inclusief de live stream en realtime rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Houd er rekening mee dat de latentie toeneemt wanneer u de Experience Cloud-bezoekersidentiteitsservice implementeert, zelfs als u deze integratie niet volledig hebt geïmplementeerd.

## Aanvullende id {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle vraag van het Doel die door een activiteit A4T wordt gebruikt om inhoud te leveren of het doel metrisch te registreren moet een overeenkomstige treffer hebben Analytics die zelfde supplementaire identiteitskaart voor A4T deelt om behoorlijk te werken.

Hits die gegevens van Analytics en Doel bevatten bevatten een extra gegevens-ID. U kunt deze id in de [Adobe Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html) zien als de `sdid` parameter. Bijvoorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Deze id wordt op elk moment gegenereerd wanneer aan de volgende criteria wordt voldaan:

* De service voor bezoekersidentiteitskaart is geïmplementeerd
* Er wordt een versie geïmplementeerd van [!DNL mbox.js] die deze integratie ondersteunt.

Wanneer het oplossen van problemen, ben zeker om te bevestigen dat supplementaire identiteitskaart op Analytics treffers aanwezig is.

## Logboekregistratie voor clientanalyse {#client-side}

Wanneer at.js, de [!DNL Experience Cloud Visitor ID Service], en appMeasurement.js op de pagina staan, [!DNL Adobe Analytics] en [!DNL Target] sluit gebeurtenissen voor rapportage- en analysedoeleinden standaard correct op de achtergrond zolang de juiste aanvullende id van de pagina is opgenomen, zoals hierboven vermeld. U hoeft geen extra bewerkingen te beheren en uit te voeren om A4T correct te laten werken.

Er zijn echter gevallen waarin u meer controle wilt hebben over wanneer en hoe u analysegegevens wilt verzenden die betrekking hebben [!DNL Target] op [!DNL Analytics] rapportagedoeleinden. U hebt mogelijk een intern analyseprogramma dat u gebruikt voor interne doeleinden, maar u wilt de analysegegevens ook [!DNL Analytics] via uw interne analyseproduct verzenden, zodat andere leden van uw organisatie [!DNL Analytics] als visuele rapportbron kunnen blijven gebruiken. Zie [stap 7: Verwijzing om.js of mbox.js op alle plaatspagina](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) &#39;s in *Analytics voor de Implementatie* van het Doel voor meer informatie.
