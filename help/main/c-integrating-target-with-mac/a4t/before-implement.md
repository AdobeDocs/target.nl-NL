---
keywords: Recommendations
description: Leer de implementatievereisten voor Analytics voor [!DNL Target] (A4T) en wat te overwegen alvorens u deze integratie uitvoert.
title: Wat moet ik weten voordat ik A4T implementeer?
feature: Analytics for Target (A4T)
exl-id: 1c98b20b-4dd1-4011-b0cd-5096471af095
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 0%

---

# Voordat u Analytics for Target (A4T) implementeert met at.js

Bij het inschakelen van gegevensverzamelingen worden verschillende wijzigingen aangebracht [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T).

Voordat u besluit om deze integratie te gebruiken, moet u de volgende secties doornemen en de gevolgen voor uw rapportageprocessen in overweging nemen.

>[!NOTE]
>
>Dit artikel is alleen van toepassing op at.js-implementaties.

## Implementatievereisten {#section_A0D2EF18033D4C3997B08A6EBB34C17A}

>[!IMPORTANT]
>
>Voordat u kunt beginnen met het gebruik van A4T, moet u vragen of uw account is ingericht voor de integratie. Gebruik de [Integraal leveringsformulier voor Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank} om provisioning aan te vragen.

Deze integratie A4T vereist dat u de volgende (of nieuwere) bibliotheekversies uitvoert, afhankelijk van of u redirect aanbiedingen met A4T of niet wilt gebruiken.

>[!NOTE]
>
>De volgende vereisten zijn *minimum* versies van at.js nodig om A4T uit te voeren. De [!DNL Target] team handhaaft slechts twee versies [!DNL at.js]—de huidige versie en de tweede nieuwste versie. Voer een upgrade uit [!DNL at.js] om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie over wat in elke versie is, zie [at.js - Versiedetails](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank}.

### Vereisten indien nodig *niet* het gebruiken van omleidingsaanbiedingen met A4T

Deze integratie vereist dat u de volgende (of nieuwere) bibliotheekversies implementeert als u niet van plan bent om aanbiedingen om te leiden met A4T. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 1.8.0
* [!DNL Adobe Target]: at.js versie 0.9.1
* Adobe Analytics: appMeasurement.js versie 1.7.0

Voor informatie over het implementeren van A4T met de [!DNL Platform Web SDK], zie [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=nl-NL){target=_blank}.

### Vereisten die nodig zijn bij het gebruik van omleidingsaanbiedingen met A4T

Als u omleidingsaanbiedingen met A4T wilt gebruiken, moet u de volgende (of nieuwere) bibliotheekversies implementeren. De vermelde volgorde is de volgorde van de bewerkingen.

* [!DNL Experience Cloud Visitor ID Service]: bezoekerAPI.js versie 2.3.0

   >[!NOTE]
   >
   >at.js 1.8.0+ en at.js 2.x+ werken niet meer met Bezoeker-API-versies ouder dan 2.5.0 voor het doorgeven van Adobe Audience Manager-parameters (AAM).

* [!DNL Adobe Target]: at.js versie 1.6.2

* Adobe Analytics: appMeasurement.js versie 2.1

Download- en implementatieinstructies worden vermeld in [Analyses voor doelimplementatie](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md).

Voor informatie over het implementeren van A4T met de [!DNL Platform Web SDK], zie [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=nl-NL){target=_blank}.

## Wat u moet weten voordat u gaat implementeren {#section_50D49CC52E11414089C89FB67F9B88F5}

* Deze integratie is ingeschakeld voor nieuwe activiteiten wanneer u ervoor kiest deze te gebruiken [!DNL Analytics] als bron van de rapportage. Nadat u de implementatiewijzigingen hebt aangebracht die in dit document worden beschreven, heeft dit geen invloed op uw bestaande activiteiten.
* Het proces van oprichting [!DNL Analytics] als bron van rapportage voor [!DNL Target] bevat diverse implementatiestappen, gevolgd door een inrichtingsstap. Het is een goed idee om het hieronder beschreven proces te doorlopen alvorens uit te voeren. Nadat u deze stappen hebt voltooid, kunt u [!DNL Analytics] als uw rapporteringsbron wanneer het voor u wordt toegelaten. Het inrichtingsproces kan maximaal vijf werkdagen in beslag nemen.
* De [!DNL Visitor ID service] maakt een gedeelde [!DNL Visitor ID] in de hele [!DNL Adobe Experience Cloud]. Hoewel het de [!DNL Target] mboxPC id of [!DNL Audience Manager] UUID, deze vervangt de manier [!DNL Analytics] identificeert nieuwe bezoekers. Indien correct ingesteld, wordt [!DNL Analytics] bezoekers moeten ook via hun oude [!DNL Analytics] ID. Op dezelfde manier omdat [!DNL Target] mboxPCid blijft intact, geen [!DNL Target] bezoekersprofielgegevens gaan verloren wanneer u een upgrade uitvoert naar het dialoogvenster [!DNL Visitor ID service].
* De [!DNL Visitor ID service] moet worden uitgevoerd voordat uw [!DNL Analytics] en [!DNL Target] paginacode. Controleer of `VisitorAPI.js` verschijnt boven de tags voor alle andere [!DNL Experience Cloud] oplossingen.

## Latentie {#section_9489BE6FD21641A4844E591711E3F813}

Nadat deze integratie is ingeschakeld, zult u een extra vertraging van 5 tot 10 minuten ervaren in [!DNL Analytics]. Deze latentieverhoging staat gegevens van toe [!DNL Analytics] en [!DNL Target] om op de zelfde klap worden opgeslagen, die u toestaat om activiteiten door pagina en plaatssectie te verdelen.

Deze stijging komt in het geheel tot uiting [!DNL Analytics] diensten en instrumenten, met inbegrip van de live stream en real-time rapportage, en is van toepassing in de volgende scenario&#39;s:

* Voor live stream, real-time rapporten en API-aanvragen en huidige gegevens voor verkeersvariabelen worden alleen hits met een aanvullende gegevens-id vertraagd.
* Voor de huidige gegevens over conversiemetriek, voltooide gegevens, en gegevensvoer, worden alle klappen een extra 5-7 minuten vertraagd.

De latentieverhoging begint nadat u uitvoert [!DNL Experience Cloud] de bezoekersidentiteitsdienst, zelfs als u deze integratie niet volledig hebt uitgevoerd.

## Aanvullende id {#section_2C1F745A2B7D41FE9E30915539226E3A}

Alles [!DNL Target] vraag die door een A4T activiteit wordt gebruikt om inhoud te leveren of het doel te registreren metrisch moet overeenkomstige hebben [!DNL Analytics] hit die de aanvullende id voor A4T deelt om correct te werken.

Hits die gegevens bevatten van [!DNL Analytics] en [!DNL Target] bevat een aanvullende gegevens-id. U kunt deze id zien in het dialoogvenster [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=nl-NL) als de `sdid` parameter. Bijvoorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`. Deze id wordt op elk moment gegenereerd wanneer aan de volgende criteria wordt voldaan:

* De service voor bezoekersidentiteitskaart is geïmplementeerd

Wanneer [problemen oplossen](/help/main/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/a4t-troubleshooting.md)moet u bevestigen dat de aanvullende id aanwezig is op [!DNL Analytics] treffers.

## Logboekregistratie voor clientanalyse {#client-side}

Indien om.js, [!DNL Experience Cloud Visitor ID Service], en appMeasurement.js bevindt zich op de pagina, [!DNL Analytics], en [!DNL Target] stift gebeurtenissen correct voor rapportage- en analysedoeleinden op de achtergrond zolang de juiste aanvullende id van de pagina wordt opgenomen. U te hoeven om geen extra verrichtingen voor A4T te beheren en uit te voeren om correct te functioneren.

Er zijn gevallen waarin u meer controle wilt hebben over wanneer en hoe u analysegegevens wilt verzenden die betrekking hebben op [!DNL Target] tot [!DNL Analytics] voor rapportagedoeleinden. Mogelijk hebt u een intern analyseprogramma dat u gebruikt voor interne doeleinden. U wilt de analysegegevens echter ook naar [!DNL Analytics] via uw interne analyseproduct zodat andere leden van uw organisatie kunnen blijven gebruiken [!DNL Analytics] als een visuele bron voor rapportage. Zie [Stap 7: Referentie om.js op alle sitepagina&#39;s](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#step7) in *Analyses voor doelimplementatie* voor meer informatie .

## Gedeeld publiek

Als u de [Integraal leveringsformulier voor Marketing Cloud](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}is op de hoogte van de volgende belangrijke informatie over de [!UICONTROL Shared Audiences] optie vermeld onder &quot;[!UICONTROL For which capabilities are you requesting provisioning]?&quot;

![Formulier aanvragen](/help/main/c-integrating-target-with-mac/a4t/assets/request-form.png)

Wanneer u [!UICONTROL Shared Audiences], kunt u [!UICONTROL Target] en [!UICONTROL Adobe Audience Manager] (AAM) informatie te delen, in dit geval publiek.

>[!IMPORTANT]
>
>Deze integratie tussen [!UICONTROL Target] en AAM komt met extra kosten. Voor elk object worden kosten in rekening gebracht [!UICONTROL Target] AAM.
