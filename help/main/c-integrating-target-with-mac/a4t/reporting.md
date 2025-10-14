---
keywords: analytische gegevens voor doel;a4t;analytische gegevens als bron van de rapportage;analytische gegevens
description: Leer hoe te om Analytics voor  [!DNL Target]  (A4T) te gebruiken. A4T verleent toegang tot de rapporten van Analytics voor  [!DNL Target]  activiteiten die de metriek van de Analyse en publiekssegmenten gebruiken.
title: Hoe gebruik ik Rapportering in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---

# A4T-rapportage

Als u [!DNL Adobe Analytics] gebruikt als rapportagebron voor [!DNL Adobe Target] (A4T), hebt u toegang tot [!DNL Analytics] -rapporten voor uw [!DNL Target] -activiteiten.

U kunt rapporten voor uw activiteiten weergeven in zowel [!DNL Analytics] als [!DNL Target] .

Voor het melden van beste praktijken die [!DNL Analytics] voor [!DNL Target] gebruiken, [&#x200B; bezoek deze Pagina van de Vonk van Adobe &#x200B;](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Zowel in [!DNL Analytics] als in [!DNL Target] worden personen (de personen die de tests invoeren) gemeten in plaats van bezoekers van de site.

Telkens wanneer een bezoeker de inhoud van de activiteit op de pagina ziet, roept [!DNL Target] direct server-aan-server [!DNL Analytics] aan, met inbegrip van welke activiteit en ervaring de bezoeker zag. [!DNL Target] roept ook [!DNL Analytics] aan wanneer de conversie wordt uitgevoerd. [!DNL Analytics] voegt de conversie toe als een specifieke nieuwe [!DNL Analytics] -gebeurtenis met de naam &quot;Activity Conversion&quot;, die samen met andere gegevens die door [!DNL Analytics] worden verzameld, wordt bijgehouden.

Wanneer de [!UICONTROL Select] verrichting wordt gebruikt en u op *invoert* sorteert, dan slechts ervaringen die ingangen tijdens de geselecteerde tijdspanne ontvangen worden getoond in de rapporten.

>[!NOTE]
>
>Rapporten die door [!DNL Target] worden aangedreven, hebben een vertraging van vier minuten. Voor activiteiten die door A4T worden aangedreven, kan het in zowel de [!DNL Target] als [!DNL Analytics] rapporten tot 24 uur duren nadat de activiteit aanvankelijk wordt opgeslagen voordat de rapportgegevens kunnen worden uitgesplitst naar ervaringen. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#analytics}

In [!DNL Analytics] zijn er verschillende dimensies en metriek die beschikbaar worden gemaakt nadat de integratie A4T is ingeschakeld.

### Afmetingen

* [!UICONTROL Analytics for Target] - De bovenliggende id die door de integratie wordt doorgegeven. De indeling van deze dimensie is `Activity ID:Experience ID:3rd ID` . Onderstaande dimensies zijn classificaties van deze dimensie.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - kan worden genegeerd

### Metrisch

* [!UICONTROL Activity Impressions] - Komt overeen met het [!UICONTROL Entrants] -getal in het [!DNL Target] -rapport.
* [!UICONTROL Activity Conversions] - Komt overeen met het [!UICONTROL Custom Conversions] -getal in het [!DNL Target] -rapport.

In [!DNL Analysis Workspace] gebruikt u het deelvenster [!UICONTROL Analytics for Target] om uw [!DNL Target] -activiteiten en -ervaringen met optillen en vertrouwen te analyseren. Voor meer informatie, zie [&#x200B; Analytics voor het Comité van het Doel (A4T) &#x200B;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html?lang=nl-NL) in de *Gids van Hulpmiddelen van de Analyse*.

>[!IMPORTANT]
>
>Als uw [!UICONTROL Target Activities] -rapport in [!DNL Analytics] &#39;unspecified&#39; vermeldt in plaats van uw activiteiten aan te bieden, is een update vereist voor uw provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

Voor gedetailleerde informatie en voorbeelden, open [&#x200B; Analytics &amp; Doel: Beste praktijken voor Analyse &#x200B;](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) leerprogramma, dat door de Liga van de Ervaring van Adobe wordt verstrekt.

## Rapporten in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer [!DNL Analytics] wordt gebruikt als de rapportbron, worden in rapporten in [!DNL Target] de gegevens weergegeven die zijn verzameld van [!DNL Analytics] . Het rapport wijkt enigszins af van andere [!DNL Target] -rapporten:

* In de lijst [!UICONTROL Audiences] staan de soorten publiek die beschikbaar zijn voor uw [!DNL Analytics] -rapportenpakket.
* In de lijst [!UICONTROL Metric] worden alle metrische gegevens weergegeven die beschikbaar zijn via [!DNL Analytics] .

  Elke metrische waarde is beschikbaar, inclusief aangepaste of berekende meetwaarden die zijn ingebouwd in [!DNL Analytics] .

  Om het even welke aantallen die stijgen worden getoond als positieven in het rapport, zelfs wanneer een verhoging ongewenste is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt de metrische waarde of het publiek toepassen op het rapport in [!DNL Target] nadat de activiteit is gestart of zelfs nadat de test is voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om het volledige [!DNL Analytics] rapport rechtstreeks vanaf de pagina van het activiteitenrapport weer te geven.

## Activiteitenschepping {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op de [!UICONTROL Settings] pagina specificeren. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met [!DNL Analytics] gebruikt [!DNL Adobe Analytics] segmenten in plaats van [!DNL Target] soorten publiek.

## Offlineberekeningen uitvoeren voor Analytics voor Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

U kunt off-line berekeningen voor vertrouwen en betrouwbaarheidsintervallen voor A4T uitvoeren gebruikend het [!DNL Target] [&#x200B; Volledige dossier van de Rekenmachine van het Vertrouwen &#x200B;](/help/main/assets/complete_confidence_calculator.xlsx) Excel, maar het vereist een stap met gegevens die in [!DNL Analytics] uitvoeren.

Voor A4T, gebruiken wij t-test van a [&#x200B; Welch &#x200B;](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} berekening voor ononderbroken variabelen (eerder dan binaire metriek). In Analytics wordt een bezoeker altijd bijgehouden en wordt elke actie geteld. Daarom als de bezoeker veelvoudige tijden koopt of een succes metrisch veelvoudige tijden bezoekt, worden die extra treffers geteld. Dit maakt metrisch een ononderbroken variabele. Om de t-test-berekening van het Welch uit te voeren, is de &quot;som van de vierkanten&quot; vereist om de variantie te berekenen, die wordt gebruikt in de noemer van de t-statistiek. [&#x200B; Statistische berekeningen in tests A/Bn &#x200B;](/help/main/c-reports/statistical-methodology/statistical-calculations.md) verklaart de details van de gebruikte wiskundige formules. De som van de vierkanten kan worden opgehaald uit [!DNL Analytics] . Om de som gegevens van vierkanten te krijgen, moet u een bezoekersvlakke uitvoer voor metrisch uitvoeren u aan optimaliseert, voor een steekproeftijdspanne.

Bijvoorbeeld, als u aan paginameningen per bezoeker optimaliseert, zou u een steekproef van het totale aantal paginameningen op een per bezoekersbasis voor een gespecificeerd tijdkader uitvoeren, misschien een paar dagen (een paar duizend gegevenspunten is allen u nodig). Vervolgens vigeert u elke waarde en somt u de totalen op (de volgorde van de bewerkingen is hier van essentieel belang). Deze &quot;som van vierkanten&quot;waarde wordt dan gebruikt in de Volledige Berekening van het Vertrouwen. Gebruik de sectie &quot;opbrengst&quot; van dat spreadsheet voor deze waarden.

**om de [!DNL Analytics] eigenschap van de gegevensuitvoer te gebruiken om dit te doen:**

1. Meld u aan bij [!DNL Adobe Analytics] .
1. Klik op **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]** .
1. Vul op het tabblad **[!UICONTROL Data Warehouse Request]** de velden in.

   Voor meer informatie over elk gebied, zie &quot;beschrijvingen van Data Warehouse&quot;in [&#x200B; Data Warehouse &#x200B;](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html?lang=nl-NL).

   | Veld | Instructies |
   |--- |--- |
   | Naam aanvraag | Geef een naam op voor uw aanvraag. |
   | Datum van rapportage | Geef een tijdsperiode en granulariteit op.<br> als beste praktijken, kies niet meer dan een uur of één dag van gegevens voor uw eerste verzoek.  Het duurt langer om Data Warehouse-bestanden te verwerken met een langere periode. Het is daarom altijd aan te raden om eerst gegevens over een kleine periode aan te vragen om ervoor te zorgen dat het bestand het gewenste resultaat oplevert. Ga vervolgens naar de Request Manager, dupliceer uw verzoek en vraag de tweede keer om meer gegevens. Ook, als u granularity aan om het even wat buiten &quot;niets&quot;schakelt, zal de dossiergrootte drastisch stijgen.<br>![&#x200B; Data Warehouse &#x200B;](/help/main/c-reports/assets/datawarehouse.png) |
   | Beschikbare segmenten | Pas indien nodig een segment toe. |
   | Uitsplitsingen | Selecteer de gewenste afmetingen: Standaard is uit-van-de-doos (OOTB), terwijl de Douane eVars &amp; steunen omvat. Je kunt het beste &#39;Bezoeker-id&#39; gebruiken als je informatie op bezoekersidentiteitsniveau nodig hebt in plaats van &#39;Experience Cloud Bezoeker-id&#39;.<ul><li>Bezoeker-id is de laatste id die wordt gebruikt door Analytics. Het zal of identiteitskaart (als de klant erfenis is) of MID (als de klant nieuwe of ontruimde koekjes is sinds de dienst van bezoekersidentiteitskaart van MC werd gelanceerd) zijn.</li><li>De Experience Cloud Bezoeker-id wordt alleen ingesteld voor klanten die nieuwe of verwijderde cookies zijn sinds de service MC bezoeker-id is gestart.</li></ul> |
   | Metrisch | Selecteer de gewenste meetgegevens. Standaard is OOTB, terwijl Aangepast aangepaste gebeurtenissen bevat. |
   | Voorvertoning van rapport | Controleer uw instellingen voordat u het rapport plant.<br>![&#x200B; Data Warehouse 2 &#x200B;](/help/main/c-reports/assets/datawarehouse2.png) |
   | Levering plannen | Voer een e-mailadres in waarnaar het bestand moet worden verzonden, geef het bestand een naam en selecteer vervolgens [!UICONTROL Send Immediately] .<br> Nota: Het dossier kan via FTP onder [!UICONTROL Advanced Delivery Options]<br>![&#x200B; Levering van het Programma worden geleverd &#x200B;](/help/main/c-reports/assets/datawarehouse3.png). |

1. Klik op **[!UICONTROL Request this Report]**.

   De levering van het dossier kan tot 72 uren, afhankelijk van de gevraagde hoeveelheid gegevens vergen. U kunt de voortgang van uw verzoek op elk gewenst moment controleren door te klikken op [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager] .

   Als u gegevens die u in het verleden hebt aangevraagd opnieuw wilt aanvragen, kunt u zo nodig een oude aanvraag van [!UICONTROL Request Manager] dupliceren.

Raadpleeg de volgende koppelingen in de Help van [!DNL Data Warehouse] voor meer informatie over [!DNL Analytics] :

* [&#x200B; creeer een verzoek van Data Warehouse &#x200B;](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html?lang=nl-NL)
* [&#x200B; de beste praktijken van Data Warehouse &#x200B;](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html?lang=nl-NL)
