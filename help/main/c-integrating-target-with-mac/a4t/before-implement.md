---
keywords: Aanbevelingen
description: Leer de implementatievereisten voor Analytics voor  [!DNL Target]  (A4T) en wat te overwegen alvorens u deze integratie uitvoert.
title: Wat moet ik weten voordat ik A4T implementeer?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 656f728ba890f1f5afc0404e22f6acb1a2565fe6
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# Voordat u Analytics for Target (A4T) implementeert met at.js

Er treden verschillende wijzigingen op in het gegevensverzamelingsproces wanneer u [!DNL Adobe Analytics] als rapportbron voor [!DNL Adobe Target] (A4T) inschakelt.

Voordat u besluit om deze integratie te gebruiken, moet u de volgende secties doornemen en de gevolgen voor uw rapportageprocessen in overweging nemen.

>[!NOTE]
>
>Dit artikel is alleen van toepassing op at.js-implementaties. Voor informatie over het uitvoeren van [!UICONTROL Analytics for Target] (A4T) met [!DNL Adobe Experience Platform Web SDK], zie [&#x200B; Adobe Analytics voor Doel (A4T) het registreren in het Web SDK van Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/a4t/overview-a4t.html?lang=nl-NL){target=_blank}.

## Implementatievereisten {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen of uw account is ingericht voor de integratie. Gebruik de [&#x200B; Vorm van de Levering van de Integratie van Marketing Cloud &#x200B;](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} om te verzoeken om te worden provisioned.

Deze integratie A4T vereist dat u de volgende (of nieuwere) bibliotheekversies uitvoert, afhankelijk van of u redirect aanbiedingen met A4T of niet wilt gebruiken.

>[!NOTE]
>
>De volgende vereisten maken een lijst van de *minimum* versies van at.js nodig om A4T uit te voeren. Het team van [!DNL Target] onderhoudt slechts twee versies van [!DNL at.js]: de huidige versie en de tweede nieuwste versie. Voer indien nodig een upgrade uit op [!DNL at.js] om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie over wat in elke versie is, zie [&#x200B; at.js de Details van de Versie &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank}.

### Vereisten nodig als *niet* het gebruiken van redirect aanbiedingen met A4T

Deze integratie vereist dat u de volgende (of nieuwere) bibliotheekversies implementeert als u niet van plan bent om aanbiedingen om te leiden met A4T. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 1.8.0
* [!DNL Adobe Target]: at.js versie 0.9.1
* Adobe Analytics: appMeasurement.js versie 1.7.0

Voor informatie over het uitvoeren van A4T met [!DNL Platform Web SDK], zie [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

### Vereisten die nodig zijn bij het gebruik van omleidingsaanbiedingen met A4T

Als u omleidingsaanbiedingen met A4T wilt gebruiken, moet u de volgende (of nieuwere) bibliotheekversies implementeren. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 2.3.0

  >[!NOTE]
  >
  >at.js 1.8.0+ en at.js 2.x+ werken niet meer met Bezoeker-API-versies ouder dan 2.5.0 voor het doorgeven van Adobe Audience Manager (AAM)-parameters.

* [!DNL Adobe Target]: at.js versie 1.6.2

* Adobe Analytics: appMeasurement.js versie 2.1

De download en plaatsingsinstructies zijn vermeld in [&#x200B; Analytics voor de Implementatie van het Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Voor informatie over het uitvoeren van A4T met [!DNL Platform Web SDK], zie [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

## Wat u moet weten voordat u gaat implementeren {#section_50D49CC52E11414089C89FB67F9B88F5}

* Deze integratie is ingeschakeld voor nieuwe activiteiten wanneer u [!DNL Analytics] als rapportbron selecteert. Nadat u de implementatiewijzigingen hebt aangebracht die in dit document worden beschreven, heeft dit geen invloed op uw bestaande activiteiten.
* Het proces om [!DNL Analytics] in te stellen als de rapportbron voor [!DNL Target] bevat verschillende implementatiestappen, gevolgd door een inrichtingsstap. Het is een goed idee om het hieronder beschreven proces te doorlopen alvorens uit te voeren. Nadat u deze stappen hebt uitgevoerd, kunt u [!DNL Analytics] gebruiken als rapportbron wanneer deze voor u is ingeschakeld. Het inrichtingsproces kan maximaal vijf werkdagen duren.
* De [!DNL Visitor ID service] maakt een gedeelde [!DNL Visitor ID] over de [!DNL Adobe Experience Cloud] . Hoewel deze de id [!DNL Target] mboxPC of [!DNL Audience Manager] UUID niet vervangt, vervangt deze de manier waarop [!DNL Analytics] nieuwe bezoekers identificeert. Als de functie op de juiste wijze is ingesteld, kunnen terugkerende [!DNL Analytics] -bezoekers ook worden geïdentificeerd met hun oude [!DNL Analytics] -id. En omdat [!DNL Target] mboxPCid intact blijft, gaan er geen gegevens van het [!DNL Target] bezoekersprofiel verloren wanneer u een upgrade uitvoert naar de [!DNL Visitor ID service] .
* [!DNL Visitor ID service] moet vóór de paginacode [!DNL Analytics] en [!DNL Target] worden uitgevoerd. Zorg ervoor dat `VisitorAPI.js` boven de labels voor alle andere [!DNL Experience Cloud] -oplossingen wordt weergegeven.

## Latentie {#section_9489BE6FD21641A4844E591711E3F813}

Nadat deze integratie is ingeschakeld, hebt u een extra vertraging van 5 tot 10 minuten in [!DNL Analytics]. Door deze latentieverhoging kunnen gegevens uit [!DNL Analytics] en [!DNL Target] op dezelfde hit worden opgeslagen, zodat u activiteiten kunt onderverdelen op pagina en sitesectie.

Deze toename wordt weerspiegeld in alle [!DNL Analytics] -services en -gereedschappen, inclusief live streaming en realtime rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor de huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

De latentieverhoging begint nadat u de dienst van identiteitskaart van de Bezoeker [!DNL Experience Cloud] uitvoert, zelfs als u deze integratie niet volledig hebt uitgevoerd.

## Aanvullende id {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alle [!DNL Target] vraag die door een activiteit A4T wordt gebruikt om inhoud te leveren of doel metrisch te registreren moet overeenkomstige [!DNL Analytics] hebben die extra identiteitskaart voor A4T deelt om behoorlijk te werken.

Punten die gegevens van [!DNL Analytics] en [!DNL Target] bevatten bevatten een aanvullende gegevens-id. U kunt deze identiteitskaart in [&#x200B; Debugger van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=nl-NL) als `sdid` parameter zien. Bijvoorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0` . Deze id wordt op elk moment gegenereerd wanneer aan de volgende criteria wordt voldaan:

* De service voor bezoekersidentiteitskaart is geïmplementeerd

Wanneer [&#x200B; het oplossen van problemen &#x200B;](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md), ben zeker om te bevestigen dat supplementaire identiteitskaart op [!DNL Analytics] hits aanwezig is.

## Logboekregistratie voor clientanalyse {#client-side}

Als at.js, [!DNL Experience Cloud Visitor ID Service], en appMeturement.js op de pagina, [!DNL Analytics], en [!DNL Target] correct gebeurtenissen voor rapportering en analysedoeleinden in het achtereind vastmaakt zolang correcte supplementaire identiteitskaart van de pagina wordt omvat. U te hoeven om geen extra verrichtingen voor A4T te beheren en uit te voeren om correct te functioneren.

Er zijn gevallen waarin u meer controle wilt hebben over wanneer en hoe u analysegegevens met betrekking tot [!DNL Target] naar [!DNL Analytics] verzendt voor rapportagedoeleinden. Mogelijk hebt u een intern analyseprogramma dat u gebruikt voor interne doeleinden. U wilt de analysegegevens echter ook naar [!DNL Analytics] verzenden via uw interne analyseproduct, zodat andere leden van uw organisatie [!DNL Analytics] kunnen blijven gebruiken als visuele rapportbron. Zie [&#x200B; Stap 7: Verwijzing at.js op alle plaatspagina&#39;s &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analytics voor de Implementatie van het Doel* voor meer informatie.

## Gedeeld publiek

Terwijl het invullen van de [&#x200B; Vorm van de Levering van de Integratie van Marketing Cloud &#x200B;](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}, me bewust ben van de volgende belangrijke informatie betreffende de [!UICONTROL Shared Audiences] optie die onder &quot; [!UICONTROL For which capabilities are you requesting provisioning] wordt vermeld?&quot;

![&#x200B; vorm van het Verzoek &#x200B;](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wanneer u [!UICONTROL Shared Audiences] aanvraagt, schakelt u [!UICONTROL Target] en [!UICONTROL Adobe Audience Manager] (AAM) in om informatie te delen, in dit geval voor het publiek.

>[!IMPORTANT]
>
>Deze integratie tussen [!UICONTROL Target] en AAM heeft extra kosten. Voor elke [!UICONTROL Target] -aanroep in AAM worden kosten in rekening gebracht.
