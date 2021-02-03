---
keywords: Recommendations
description: Verscheidene veranderingen komen in uw proces van de gegevensinzameling voor wanneer het toelaten van Analytics als rapporteringsbron voor Doel (A4T).
title: Voordat u Analyses implementeert als rapportbron (A4T)
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---


# Voordat u{#before-you-implement} implementeert

Er vinden verschillende wijzigingen plaats in het gegevensverzamelingsproces wanneer [!DNL Analytics] wordt ingeschakeld als rapportagebron voor [!DNL Target] (A4T).

Voordat u besluit om deze integratie te gebruiken, moet u de volgende secties doornemen en de gevolgen voor uw rapportageprocessen in overweging nemen:

## Implementatievereisten {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen dat uw account wordt ingericht voor de integratie. Gebruik [Marketing Cloud Integations Provisioning Form](https://www.adobe.com/go/audiences) om provisioned te verzoeken.

Deze integratie A4T vereist dat u de volgende (of nieuwere) bibliotheekversies uitvoert, afhankelijk van of u redirect aanbiedingen met A4T of niet wilt gebruiken:

### Vereisten indien *niet* omleidingsaanbiedingen met A4T gebruikt

Deze integratie vereist dat u de volgende (of nieuwere) bibliotheekversies implementeert als u niet van plan bent om aanbiedingen om te leiden met A4T. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 1.8.0
* [!DNL Adobe Target] (afhankelijk van uw implementatie): at.js versie 0.9.1 of mbox.js versie 61
* Adobe Analytics: appMeasurement.js versie 1.7.0

### Vereisten die nodig zijn bij het gebruik van omleidingsaanbiedingen met A4T

Als u omleidingsaanbiedingen met A4T wilt gebruiken, moet u de volgende (of nieuwere) bibliotheekversies implementeren. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 2.3.0
* [!DNL Adobe Target]: at.js versie 1.6.2

   **Opmerking:** de bibliotheek mbox.js ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet at.js gebruiken.

* Adobe Analytics: appMeasurement.js versie 2.1

Download- en implementatieinstructies worden vermeld in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Te weten dingen voordat u {#section_50D49CC52E11414089C89FB67F9B88F5} implementeert

* Deze integratie wordt toegelaten op nieuwe activiteiten wanneer u om [!DNL Analytics] als rapporteringsbron selecteert te gebruiken. Nadat u de implementatiewijzigingen hebt aangebracht die in dit document worden beschreven, heeft dit geen invloed op uw bestaande activiteiten.
* Het proces om [!DNL Analytics] als rapporteringsbron voor [!DNL Target] te vestigen omvat verscheidene implementatiestappen, die door een leveringsstap worden gevolgd. Het is een goed idee om het hieronder beschreven proces te doorlopen alvorens uit te voeren. Nadat u deze stappen hebt voltooid, bent u klaar om [!DNL Analytics] als uw rapporteringsbron te gebruiken zodra het voor u wordt toegelaten. Het inrichtingsproces kan maximaal vijf werkdagen in beslag nemen.
* [!DNL Visitor ID service] leidt tot gedeelde [!DNL Visitor ID] over [!DNL Adobe Experience Cloud]. Hoewel deze de [!DNL Target] mboxPC id of [!DNL Audience Manager] UUID niet vervangt, vervangt deze de manier waarop [!DNL Analytics] nieuwe bezoekers identificeert. Indien correct ingesteld, dienen terugkerende [!DNL Analytics] bezoekers ook te worden geïdentificeerd via hun oude [!DNL Analytics]-id om te voorkomen dat bezoekers knippen. Op dezelfde manier, omdat [!DNL Target] mboxPCid intact blijft, worden geen [!DNL Target] gegevens van het bezoekersprofiel verloren wanneer u aan [!DNL Visitor ID service] bevordert.
* De [!DNL Visitor ID service] moet vóór uw [!DNL Analytics] en [!DNL Target] paginacode uitvoeren. Zorg ervoor dat `VisitorAPI.js` boven de markeringen voor alle andere [!DNL Experience Cloud] oplossingen verschijnt.

## Latentie {#section_9489BE6FD21641A4844E591711E3F813}

Nadat deze integratie is ingeschakeld, hebt u nog 5-10 minuten vertraging in [!DNL Analytics]. Door deze latentieverhoging kunnen gegevens van [!DNL Analytics] en [!DNL Target] op dezelfde hit worden opgeslagen, zodat u activiteiten kunt onderverdelen op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle [!DNL Analytics] diensten en hulpmiddelen, met inbegrip van live-stream en real-time rapportering, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

Vergeet niet dat de latentieverhoging begint nadat u de [!DNL Experience Cloud] bezoekersidentiteitsservice implementeert, zelfs als u deze integratie niet volledig hebt geïmplementeerd.

## Aanvullende id {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] vraag die door een activiteit A4T wordt gebruikt om inhoud te leveren of het doel metrisch te registreren moet overeenkomstige [!DNL Analytics] hebben die zelfde supplementaire identiteitskaart voor A4T deelt om behoorlijk te werken.

Punten die gegevens van [!DNL Analytics] en [!DNL Target] bevatten bevatten een extra gegevens-id. U kunt deze id in [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als `sdid` parameter zien. Bijvoorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Deze id wordt op elk moment gegenereerd wanneer aan de volgende criteria wordt voldaan:

* De service voor bezoekersidentiteitskaart is geïmplementeerd
* Een versie van [!DNL mbox.js] die deze integratie steunt wordt uitgevoerd.

Als [problemen oplossen](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), moet u bevestigen dat de aanvullende id aanwezig is bij [!DNL Analytics]-treffers.

## Logboekregistratie voor clientanalyse {#client-side}

Wanneer [!DNL Experience Cloud Visitor ID Service], en appMeasurement.js zich standaard op de pagina bevinden, [!DNL Analytics] en [!DNL Target] naaien gebeurtenissen correct voor rapportage- en analysedoeleinden op de achtergrond zolang de juiste aanvullende id van de pagina is opgenomen, zoals hierboven vermeld. U hoeft geen extra bewerkingen te beheren en uit te voeren om A4T correct te laten werken.

Er zijn echter gevallen waarin u meer controle wilt hebben over wanneer en hoe u analysegegevens wilt verzenden die betrekking hebben op [!DNL Target] naar [!DNL Analytics] voor rapportagedoeleinden. U hebt mogelijk een intern analyseprogramma dat u gebruikt voor interne doeleinden, maar u wilt de analysegegevens ook naar [!DNL Analytics] verzenden via uw interne analyseproduct, zodat andere leden van uw organisatie [!DNL Analytics] kunnen blijven gebruiken als visuele rapportbron. Zie [Stap 7: Verwijzing om.js of mbox.js op alle plaatspagina&#39;s](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics voor de Implementatie van het Doel* voor meer informatie.

## Gedeeld publiek

Let bij het invullen van het [Integations Provisioning Form](https://www.adobe.com/go/audiences) op de volgende belangrijke informatie met betrekking tot de optie [!UICONTROL Shared Audiences] die onder &quot;[!UICONTROL For which capabilities are you requesting provisioning]?&quot; wordt vermeld

![Formulier aanvragen](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wanneer u [!UICONTROL Shared Audiences] vraagt, laat u [!UICONTROL Target] en [!UICONTROL Adobe Audience Manager] (AAM) toe om informatie, in dit geval publiek te delen.

>[!IMPORTANT]
>
>Deze integratie tussen [!UICONTROL Target] en AAM komt met extra kosten. U zult voor elke [!UICONTROL Target] vraag in AAM worden gefactureerd.
