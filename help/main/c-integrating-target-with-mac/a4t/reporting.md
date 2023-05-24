---
keywords: analytische gegevens voor doel;a4t;analytische gegevens als bron van de rapportage;analytische gegevens
description: Meer informatie over het gebruik van Analytics voor [!DNL Target] (A4T). A4T biedt toegang tot analyserapporten voor [!DNL Target] activiteiten die de metriek van de Analyse en publiekssegmenten gebruiken.
title: Hoe gebruik ik Rapportering in A4T?
feature: Analytics for Target (A4T)
exl-id: cab5dc5f-166a-468e-8382-ae734684afdd
source-git-commit: 6857ba1a6410d3140a83a052efc50e9dd1776fd9
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# A4T-rapportage

Gebruiken [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T) geeft u toegang tot [!DNL Analytics] rapporten voor uw [!DNL Target] activiteiten.

U kunt rapporten voor uw activiteiten weergeven in beide [!DNL Analytics] en [!DNL Target].

Voor het rapporteren van beste praktijken die [!DNL Analytics] for [!DNL Target], [bezoek een Adobe Spark Page](https://spark.adobe.com/page/Lo3Spm4oBOvwF/).

## Overzicht {#section_035A62D65608423285D8A5A54731E2C5}

Beide [!DNL Analytics] en [!DNL Target] in rapporten worden nieuwkomers ( de personen die de tests uitvoeren ) gemeten in plaats van bezoekers van de site .

Telkens wanneer een bezoeker de inhoud van de activiteit op de pagina ziet, [!DNL Target] maakt een directe server-aan-server vraag aan [!DNL Analytics], met inbegrip van de activiteiten en ervaring die de bezoeker heeft gezien. [!DNL Target] ook oproepen [!DNL Analytics] wanneer de conversie plaatsvindt. [!DNL Analytics] voegt de conversie toe als een specifieke nieuwe [!DNL Analytics] gebeurtenis genaamd &quot;Activiteitenconversie&quot;, die wordt bijgehouden samen met andere gegevens die worden verzameld door [!DNL Analytics].

Wanneer de [!UICONTROL Select] bewerking wordt gebruikt en u sorteert op *Entranten* In dat geval worden in de rapporten alleen ervaringen weergegeven die tijdens de geselecteerde periode binnengekomen zijn.

>[!NOTE]
>
>Rapporten aangedreven door [!DNL Target] hebben een vertraging van vier minuten. Voor activiteiten die door A4T worden aangedreven, zowel in de [!DNL Target] en [!DNL Analytics] rapporten, kan het tot 24 uren vergen nadat de activiteit aanvankelijk wordt bewaard alvorens de rapportgegevens door ervaringen kunnen worden verdeeld. De gegevens die in die eerste 24 uur zijn verzameld, zijn nog steeds correct en worden toegewezen aan de juiste ervaring.

## Rapporten in Analytics {#analytics}

In [!DNL Analytics], zijn er verscheidene dimensies en metriek beschikbaar gemaakt nadat de integratie A4T wordt toegelaten.

### Dimension

* [!UICONTROL Analytics for Target] - De bovenliggende id die door de integratie wordt doorgegeven. De indeling van deze dimensie is `Activity ID:Experience ID:3rd ID`. Onderstaande dimensies zijn classificaties van deze dimensie.
* [!UICONTROL Target Activities]
* [!UICONTROL Target Experiences]
* [!UICONTROL Target Activity] > [!UICONTROL Experience]
* [!UICONTROL 3rd ID] - kan worden genegeerd

### Metrisch

* [!UICONTROL Activity Impressions] - Komt overeen met de [!UICONTROL Entrants] aantal in [!DNL Target] verslag.
* [!UICONTROL Activity Conversions] - Komt overeen met de [!UICONTROL Custom Conversions] aantal in [!DNL Target] verslag.

In [!DNL Analysis Workspace], gebruikt u de [!UICONTROL Analytics for Target] om uw [!DNL Target] activiteiten en ervaringen met liftmogelijkheden en vertrouwen. Zie voor meer informatie [Analyses voor doelvenster (A4T)](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/a4t-panel.html) in de *Handleiding Analysehulpmiddelen*.

>[!IMPORTANT]
>
>Als uw [!UICONTROL Target Activities] rapporteren in [!DNL Analytics] bevat de lijst &quot;niet opgegeven&quot; in plaats van je activiteiten aan te bieden. Er is een update vereist voor je provisioned account. Neem contact op met de klantenservice om dit probleem op te lossen.

Voor gedetailleerde informatie en voorbeelden opent u het dialoogvenster [Analyse en doel: Beste praktijken voor Analyse](https://spark.adobe.com/page/Lo3Spm4oBOvwF/) zelfstudie van Adobe Experience League.

## Rapporten in [!DNL Target] {#section_C0D1F17F88374B6690BF904D7B83B42E}

Wanneer [!DNL Analytics] wordt gebruikt als bron van rapportage, rapporten in [!DNL Target] tonen de gegevens die van worden verzameld [!DNL Analytics]. Het verslag wijkt enigszins af van het andere [!DNL Target] rapporten:

* De [!UICONTROL Audiences] de lijst toont de soorten publiek beschikbaar aan uw [!DNL Analytics] rapportsuite.
* De [!UICONTROL Metric] lijst toont elke metrische waarde beschikbaar door [!DNL Analytics].

   Elke metrisch is beschikbaar, met inbegrip van om het even welke douane of berekende metriek die ingebouwde zijn [!DNL Analytics].

   Om het even welke aantallen die stijgen worden getoond als positieven in het rapport, zelfs wanneer een verhoging ongewenste is. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

U kunt metrisch of publiek op het rapport in toepassen [!DNL Target] nadat de activiteit is gestart of zelfs nadat de test is voltooid. Je hoeft niet precies te weten wat je vooraf wilt meten.

Klik om de volledige [!DNL Analytics] rechtstreeks vanuit de pagina activiteitenrapport rapporteren.

## Activiteitenschepping {#section_311586E3FF5541E7A91D1A3CE5F9ACE3}

Tijdens het creëren van activiteit, moet u een doel voor de activiteit op specificeren [!UICONTROL Settings] pagina. Dit doel wordt standaard metrisch voor het rapport en is altijd vermeld als eerste optie in de metriekselecteur. U kunt geen segmenten voor rapportering selecteren zoals u voor een regelmatige activiteit van het Doel zou doen. Een test met [!DNL Analytics] gebruik [!DNL Adobe Analytics] segmenten in plaats van [!DNL Target] publiek.

## Offlineberekeningen uitvoeren voor analyses voor Adobe Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

U kunt offlineberekeningen voor betrouwbaarheid en betrouwbaarheidsintervallen voor A4T uitvoeren gebruikend [!DNL Target] [Complete betrouwbaarheidscalculator](/help/main/assets/complete_confidence_calculator.xlsx) Excel-bestand, maar vereist een stap met gegevens die worden geëxporteerd naar [!DNL Analytics].

Voor A4T gebruiken wij [T-test van Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test){target=_blank} berekening voor doorlopende variabelen (in plaats van binaire metriek). In Analytics wordt een bezoeker altijd bijgehouden en wordt elke actie geteld. Daarom als de bezoeker veelvoudige tijden koopt of een succes metrisch veelvoudige tijden bezoekt, worden die extra treffers geteld. Dit maakt metrisch een ononderbroken variabele. Om de t-test-berekening van het Welch uit te voeren, is de &quot;som van de vierkanten&quot; vereist om de variantie te berekenen, die wordt gebruikt in de noemer van de t-statistiek. [Statistische berekeningen voor A/Bn-tests](/help/main/c-reports/statistical-methodology/statistical-calculations.md) licht de details van de gebruikte wiskundige formules toe. De som van de vierkanten kan worden opgehaald [!DNL Analytics]. Om de som gegevens van vierkanten te krijgen, moet u een bezoekersvlakke uitvoer voor metrisch uitvoeren u aan optimaliseert, voor een steekproeftijdspanne.

Bijvoorbeeld, als u aan paginameningen per bezoeker optimaliseert, zou u een steekproef van het totale aantal paginameningen op een per bezoekersbasis voor een gespecificeerd tijdkader uitvoeren, misschien een paar dagen (een paar duizend gegevenspunten is allen u nodig). Vervolgens vigeert u elke waarde en somt u de totalen op (de volgorde van de bewerkingen is hier van essentieel belang). Deze &quot;som van vierkanten&quot;waarde wordt dan gebruikt in de Volledige Berekening van het Vertrouwen. Gebruik de sectie &quot;opbrengst&quot; van dat spreadsheet voor deze waarden.

**Als u de opdracht [!DNL Analytics] functie voor het exporteren van gegevens om dit te doen:**

1. Aanmelden bij [!DNL Adobe Analytics].
1. Klik op **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Op de **[!UICONTROL Data Warehouse Request]** , vult u de velden in.

   Voor meer informatie over elk gebied, zie &quot;Beschrijvingen van de Data Warehouse&quot;in [Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse.html).

   | Veld | Instructies |
   |--- |--- |
   | Naam aanvraag | Geef een naam op voor uw aanvraag. |
   | Datum van rapportage | Geef een tijdsperiode en granulariteit op.<br>Als beste praktijken, kies niet meer dan een uur of één dag van gegevens voor uw eerste verzoek.  De dossiers van de Data Warehouse nemen langer om de langere gevraagde tijdspanne te verwerken, zodat is het altijd beste om een kleine tijdspanne eerst om gegevens te verzoeken om ervoor te zorgen uw dossier het verwachte resultaat terugkeert. Ga vervolgens naar de Request Manager, dupliceer uw verzoek en vraag de tweede keer om meer gegevens. Ook, als u granularity aan om het even wat buiten &quot;niets&quot;schakelt, zal de dossiergrootte drastisch stijgen.<br>![Data Warehouse](/help/main/c-reports/assets/datawarehouse.png) |
   | Beschikbare segmenten | Pas indien nodig een segment toe. |
   | Uitsplitsingen | Selecteer de gewenste afmetingen: Standaard is OOTB (out-of-the-box) en Aangepast bevat Vars en props. U kunt het beste &quot;Bezoeker-id&quot; gebruiken als er gegevens op bezoekersidentiteitsniveau nodig zijn in plaats van &quot;Bezoeker-id Experience Cloud&quot;.<ul><li>Bezoeker-id is de laatste id die wordt gebruikt door Analytics. Het zal of HULP (als de klant erfenis is) of MID (als de klant nieuwe of ontruimde koekjes is sinds de dienst van bezoekersidentiteitskaart van MC werd gelanceerd) zijn.</li><li>De Experience Cloud Bezoeker-id wordt alleen ingesteld voor klanten die nieuwe of verwijderde cookies zijn sinds de service MC bezoeker-id is gestart.</li></ul> |
   | Metrisch | Selecteer de gewenste meetgegevens. Standaard is OOTB, terwijl Aangepast aangepaste gebeurtenissen bevat. |
   | Voorvertoning van rapport | Controleer uw instellingen voordat u het rapport plant.<br>![Data Warehouse 2](/help/main/c-reports/assets/datawarehouse2.png) |
   | Levering plannen | Voer een e-mailadres in waarnaar u het bestand wilt verzenden, geef het bestand een naam en selecteer vervolgens [!UICONTROL Send Immediately].<br>Opmerking: Het bestand kan via FTP worden geleverd onder [!UICONTROL Advanced Delivery Options]<br>![Levering plannen](/help/main/c-reports/assets/datawarehouse3.png). |

1. Klik op **[!UICONTROL Request this Report]**.

   De levering van het dossier kan tot 72 uren, afhankelijk van de gevraagde hoeveelheid gegevens vergen. U kunt de voortgang van uw verzoek op elk gewenst moment controleren door op [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager].

   Als u gegevens opnieuw wilt aanvragen die u in het verleden hebt aangevraagd, kunt u een oude aanvraag van de [!UICONTROL Request Manager] indien nodig.

Meer informatie over [!DNL Data Warehouse], zie de volgende koppelingen in de [!DNL Analytics] Help-documentatie:

* [Een Data Warehouse-aanvraag maken](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/t-dw-create-request.html)
* [Aanbevolen werkwijzen voor Data Warehouse](https://experienceleague.adobe.com/docs/analytics/export/data-warehouse/data-warehouse-bp.html)
