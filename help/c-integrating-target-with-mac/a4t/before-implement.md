---
keywords: Recommendations
description: Leer de implementatievereisten voor Analytics voor [!DNL Target] (A4T) en wat te overwegen alvorens u deze integratie implementeert.
title: Wat moet ik weten voordat ik A4T implementeer?
feature: Analyses voor doel (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 4c696f55f56a116cff61c2c307f750e72cc0107c
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Voordat u Analytics for Target (A4T) implementeert met at.js

Er vinden verschillende wijzigingen plaats in het gegevensverzamelingsproces wanneer [!DNL Adobe Analytics] wordt ingeschakeld als rapportagebron voor [!DNL Adobe Target] (A4T).

Voordat u besluit om deze integratie te gebruiken, moet u de volgende secties doornemen en de gevolgen voor uw rapportageprocessen in overweging nemen.

>[!NOTE]
>
>Dit artikel is alleen van toepassing op at.js-implementaties.

## Implementatievereisten {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen of uw account is ingericht voor de integratie. Gebruik het [Inrichtingsformulier voor integraties van Marketing Cloud](https://www.adobe.com/go/audiences) om provisioned te vragen.

Deze integratie A4T vereist dat u de volgende (of nieuwere) bibliotheekversies uitvoert, afhankelijk van of u redirect aanbiedingen met A4T of niet wilt gebruiken:

### Vereisten indien *niet* omleidingsaanbiedingen met A4T gebruikt

Deze integratie vereist dat u de volgende (of nieuwere) bibliotheekversies implementeert als u niet van plan bent om aanbiedingen om te leiden met A4T. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 1.8.0
* [!DNL Adobe Target] (afhankelijk van uw implementatie): at.js versie 0.9.1 of mbox.js versie 61
* Adobe Analytics: appMeasurement.js versie 1.7.0

### Vereisten die nodig zijn bij het gebruik van omleidingsaanbiedingen met A4T

Als u omleidingsaanbiedingen met A4T wilt gebruiken, moet u de volgende (of nieuwere) bibliotheekversies implementeren. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 2.3.0

   **Opmerking:**  at.js 1.8.0 of hoger werkt niet meer met versies van de bezoeker-API ouder dan 2.5.0 voor het doorgeven van parameters  [!DNL Adobe Audience Manager] (AAM).

* [!DNL Adobe Target]: at.js versie 1.6.2

   **Opmerking**: De bibliotheek mbox.js ondersteunt geen omleidingsaanbiedingen met A4T. Uw implementatie moet at.js gebruiken.

* Adobe Analytics: appMeasurement.js versie 2.1

Download- en implementatieinstructies worden vermeld in [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md).

## Wat u moet weten voordat u gaat implementeren {#section_50D49CC52E11414089C89FB67F9B88F5}

* Deze integratie wordt toegelaten op nieuwe activiteiten wanneer u om [!DNL Analytics] als rapporteringsbron selecteert te gebruiken. Nadat u de implementatiewijzigingen hebt aangebracht die in dit document worden beschreven, heeft dit geen invloed op uw bestaande activiteiten.
* Het proces om [!DNL Analytics] als rapporteringsbron voor [!DNL Target] te vestigen omvat verscheidene implementatiestappen, die door een leveringsstap worden gevolgd. Het is een goed idee om het hieronder beschreven proces te doorlopen alvorens uit te voeren. Nadat u deze stappen voltooit, bent u klaar om [!DNL Analytics] als uw rapporteringsbron te gebruiken wanneer het voor u wordt toegelaten. Het inrichtingsproces kan maximaal vijf werkdagen in beslag nemen.
* [!DNL Visitor ID service] leidt tot gedeelde [!DNL Visitor ID] over [!DNL Adobe Experience Cloud]. Hoewel deze de [!DNL Target] mboxPC id of [!DNL Audience Manager] UUID niet vervangt, vervangt deze de manier waarop [!DNL Analytics] nieuwe bezoekers identificeert. Indien correct ingesteld, moeten terugkerende [!DNL Analytics] bezoekers ook worden geïdentificeerd via hun oude [!DNL Analytics]-id. Op dezelfde manier, omdat [!DNL Target] mboxPCid intact blijft, worden geen [!DNL Target] gegevens van het bezoekersprofiel verloren wanneer u aan [!DNL Visitor ID service] bevordert.
* De [!DNL Visitor ID service] moet vóór uw [!DNL Analytics] en [!DNL Target] paginacode uitvoeren. Zorg ervoor dat `VisitorAPI.js` boven de markeringen voor alle andere [!DNL Experience Cloud] oplossingen verschijnt.

## Latentie {#section_9489BE6FD21641A4844E591711E3F813}

Nadat deze integratie is ingeschakeld, zult u een extra vertraging van 5 tot 10 minuten ervaren in [!DNL Analytics]. Door deze latentieverhoging kunnen gegevens van [!DNL Analytics] en [!DNL Target] op dezelfde hit worden opgeslagen, zodat u activiteiten kunt onderverdelen op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle [!DNL Analytics] diensten en hulpmiddelen, met inbegrip van live-stream en real-time rapportering, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor de huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

De latentieverhoging begint nadat u de [!DNL Experience Cloud] dienst van bezoekersidentiteitskaart uitvoert, zelfs als u deze integratie niet volledig hebt uitgevoerd.

## Aanvullende id {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] vraag die door een activiteit A4T wordt gebruikt om inhoud te leveren of doel te registreren metrisch moet overeenkomstige [!DNL Analytics] hebben die extra identiteitskaart voor A4T deelt om behoorlijk te werken.

Punten die gegevens van [!DNL Analytics] en [!DNL Target] bevatten bevatten een extra gegevens-id. U kunt deze id in [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) als `sdid` parameter zien. Bijvoorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Deze id wordt op elk moment gegenereerd wanneer aan de volgende criteria wordt voldaan:

* De service voor bezoekersidentiteitskaart is geïmplementeerd
* Een versie van [!DNL mbox.js] die deze integratie steunt wordt uitgevoerd.

Als [problemen oplossen](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), moet u bevestigen dat de aanvullende id aanwezig is bij [!DNL Analytics]-treffers.

## Logboekregistratie voor clientanalyse {#client-side}

Als at.js, [!DNL Experience Cloud Visitor ID Service], en appMeasurement.js op de pagina, [!DNL Analytics], en [!DNL Target] correct gebeurtenissen voor rapportering en analysedoeleinden in het achtereind vastmaakt zolang correcte supplementaire identiteitskaart van de pagina wordt omvat. U te hoeven om geen extra verrichtingen voor A4T te beheren en uit te voeren om correct te functioneren.

Er zijn gevallen waarin u meer controle wilt hebben over wanneer en hoe u analysegegevens met betrekking tot [!DNL Target] naar [!DNL Analytics] wilt verzenden voor rapportagedoeleinden. Mogelijk hebt u een intern analyseprogramma dat u gebruikt voor interne doeleinden. Nochtans, wilt u ook de analysegegevens naar [!DNL Analytics] via uw intern analyseproduct verzenden zodat andere leden van uw organisatie [!DNL Analytics] als visuele rapporteringsbron kunnen blijven gebruiken. Zie [Stap 7: Verwijzing om.js of mbox.js op alle plaatspagina&#39;s](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics voor de Implementatie van het Doel* voor meer informatie.

## Gedeeld publiek

Let bij het invullen van het [Integations Provisioning Form](https://www.adobe.com/go/audiences) op de volgende belangrijke informatie met betrekking tot de optie [!UICONTROL Shared Audiences] die onder &quot;[!UICONTROL For which capabilities are you requesting provisioning]?&quot; wordt vermeld

![Formulier aanvragen](/help/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wanneer u [!UICONTROL Shared Audiences] vraagt, laat u [!UICONTROL Target] en [!UICONTROL Adobe Audience Manager] (AAM) toe om informatie, in dit geval publiek te delen.

>[!IMPORTANT]
>
>Deze integratie tussen [!UICONTROL Target] en AAM komt met extra kosten. U wordt gefactureerd voor elke [!UICONTROL Target] vraag in AAM.
