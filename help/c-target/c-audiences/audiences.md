---
keywords: publiek;publieksregels;publiek maken;publiek maken;publiek instellen;publiek rapporteren;publiek rapporteren;segment;aangepaste profielparameters;publieksdefinitie;publiekslijst
description: Leer hoe u het publiek kunt gebruiken in [!DNL Adobe Target].
title: Hoe gebruik ik de Audience List?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: 62c17b5a4bce2cf9a2412b2bbe1aff064b8c6b17
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 0%

---

# Soorten publiek maken

Soorten publiek in [!DNL Adobe Target] bepalen wie inhoud en ervaringen in een gerichte activiteit ziet.

Het publiek wordt gebruikt overal waar het richten beschikbaar is. Wanneer u een activiteit als doel instelt, hebt u de volgende opties:

* Selecteer een herbruikbaar publiek in het menu [!UICONTROL Audiences] list
* [Een activiteitspecifiek publiek maken](/help/c-target/creating-activity-only-audience.md) en als doel instellen
* [Meerdere doelgroepen combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) om een ad-hocpubliek te maken

U kunt ook publieksgegevens gebruiken die zijn verzameld door [!DNL Adobe Analytics] voor realtime gericht werken en personalisatie in [!DNL Target] en andere [!DNL Adobe Experience Cloud] toepassingen. Zie [Experience Cloud publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) in de *Experience Cloud Central-interfacecomponenten* hulplijn.

Er zijn twee soorten publiek in [!DNL Target]:

* **Doelgroepen:** Wordt gebruikt om verschillende inhoud aan verschillende typen bezoekers te leveren.
* **Volwassenen rapporteren:** Hiermee bepaalt u hoe verschillende typen bezoekers op dezelfde inhoud reageren, zodat u de testresultaten kunt analyseren.

   In [!DNL Target], kunt u rapportpubliek slechts vormen als u gebruikt [!DNL Target] als rapportagebron. Als u [Adobe Analytics als rapportagebron](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T), moet u uw rapporteringspubliek binnen vormen [!DNL Analytics].

## Gebruik de [!UICONTROL Audiences] list {#use-list}

Om toegang te krijgen tot [!UICONTROL Audiences] lijst, klikt u op **[!UICONTROL Audiences]** in de bovenste menubalk:

![[!UICONTROL Audiences] list](assets/audiences_list.png)

De [!UICONTROL Audiences] Deze lijst bevat het publiek dat u in uw activiteiten kunt gebruiken. Gebruik de [!UICONTROL Audiences] om een publiek te maken, te bewerken, te dupliceren, te kopiëren of te combineren. De lijst toont ook de bron waar het publiek werd gecreeerd:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >De [!DNL Adobe Experience Platform] bron is beschikbaar voor iedereen [!DNL Target] klanten die [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md). Publiek beschikbaar bij de [!DNL Adobe Experience Platform] kan worden gebruikt zoals is of [gecombineerd met bestaand publiek](/help/c-target/combining-multiple-audiences.md).
   >
   >Gebruikers moeten beschikken over [!UICONTROL Approver] of hoger [!DNL Target] om te vormen [!DNL Target] [!UICONTROL Destinations] kaarten in AEP/RTCDP ([!DNL Real-time Customer Data Platform]).
   >
   >Zie voor meer informatie [Soorten publiek uit Adobe Experience Platform gebruiken](#aep).

Vooraf gedefinieerde doelgroepen, zoals &quot;[!UICONTROL New Visitors]&quot; en &quot;[!UICONTROL Returning Visitors],&quot; kan niet worden hernoemd.

Wanneer u werkt met soorten publiek die oorspronkelijk zijn gemaakt in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform], [!DNL Target] waarschuwt u als u een publiek in [!DNL Target] activiteiten die later zijn verwijderd in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform].

* Als een publiek is verwijderd in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform], een waarschuwingspictogram in beide [!UICONTROL Audience] wordt weergegeven. Knopinfo in de [!DNL Target] De gebruikersinterface geeft ook aan dat het publiek is verwijderd in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform].
* Als u meerdere soorten publiek probeert te combineren met een verwijderd publiek of als u een activiteit probeert op te slaan die verwijst naar een verwijderd publiek, wordt een waarschuwingsbericht weergegeven.

U kunt ook aangepaste profielparameters en `user.` parameters. Wanneer het creëren van een publiek, sleep de attributen u wilt gebruiken om uw activiteit in het venster van de publieksbouwer te richten. Als het gewenste kenmerk niet wordt weergegeven, is het kenmerk niet geactiveerd door een mbox. Andere aangepaste mbox-parameters zijn beschikbaar in het dialoogvenster [!UICONTROL Custom Parameters] vervolgkeuzelijst.

Gebruik de [!UICONTROL Filters] om het filter [!UICONTROL Audiences] lijst op bron: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud], en [!DNL Adobe Experience Platform].

![De optie Filters in het dialoogvenster [!UICONTROL Audiences] list](assets/filters.png)

Gebruik de [!UICONTROL Search audiences] vak waarin u kunt zoeken [!UICONTROL Audiences] lijst. U kunt zoeken naar een willekeurig deel van een publieksnaam of u kunt een specifieke tekenreeks tussen aanhalingstekens plaatsen.

U kunt de [!UICONTROL Audiences] lijst op publieksnaam of op de datum waarop deze voor het laatst is gewijzigd. Als u op naam of datum wilt sorteren, klikt u op de kolomkop en selecteert u deze om het publiek in oplopende of aflopende volgorde weer te geven.

## Scherptedefinities weergeven {#section_11B9C4A777E14D36BA1E925021945780}

U kunt de definitiedetails van het publiek op een pop-up kaart op diverse plaatsen in bekijken [!DNL Target] UI zonder het publiek te openen. Deze functionaliteit is van toepassing op publiek dat is gemaakt in [!DNL Target Standard/Premium] en publiek geïmporteerd uit [!DNL Target Classic] of gemaakt via API.

De volgende publieksdefinitiekaart is bijvoorbeeld toegankelijk door op de knop [!UICONTROL View Details] pictogram voor het gewenste publiek:

![Activiteiten > Definitie van publiek](assets/audience_definition_list.png)

U kunt de volgende publieksdefinitiekaart openen door op de knop [!UICONTROL View Details] pictogram op een activiteit [!UICONTROL Overview] pagina:

![Activiteiten > Definitie van publiek](assets/view-details-activity-overview.png)

De publieksdefinitiekaart toont zij het type, de bron, en de attributen van het publiek. Klikken **[!UICONTROL View full details]** andere activiteiten te bekijken die naar dat publiek verwijzen, indien van toepassing. Als u een publieksdefinitiekaart van een activiteit bekijkt [!UICONTROL Overview] pagina, klikt u op **[!UICONTROL Audience Usage]**.

De informatie over het gebruik van het publiek kan u helpen onbedoelde gevolgen voor andere activiteiten te vermijden terwijl het uitgeven van publiek. Informatie omvat [!UICONTROL Live Activities], [!UICONTROL Inactive Activities], [!UICONTROL Archived Activities], en [!UICONTROL Syncing Activities]. Deze functie is beschikbaar voor alle soorten publiek (publiek in de bibliotheek en [alleen-activiteitstoepassingen](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Als een publiek [gecombineerd met een ander publiek](/help/c-target/combining-multiple-audiences.md) en het gecombineerde publiek wordt gebruikt om een activiteit tot stand te brengen, maakt de gebruiksinformatie voor beide publiek een lijst van die pas gecreëerde activiteit.

![](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## Gebruik publiek van [!DNL Adobe Experience Platform] {#aep}

Het publiek gebruiken dat is gemaakt in [!DNL Adobe Experience Platform] Verstrek rijkere klantengegevens die tot uitvoerigere verpersoonlijking leiden. De [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), gebouwd op [!DNL Adobe Experience Platform]helpt bedrijven bekende en anonieme gegevens uit meerdere bedrijfsbronnen bij elkaar te brengen. Dit proces laat u klantenprofielen tot stand brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in real time te verstrekken.

Door verbinding te maken [!DNL Target] aan de [!DNL Real-time Customer Data Platform]kunnen klanten hun webpersonalisatie verrijken door nieuwe segmenten te ontsluiten die eerder niet toegankelijk waren voor [!DNL Target] om realtime millisecondenpersonalisatie in te schakelen op de eerste pagina van het webbezoek van een klant. Het publiek gebruiken dat is gemaakt in [!DNL Adobe Experience Platform] Hiermee kunt u de beschikbare gegevenspunten uitbreiden voor een rijkere personalisatie.

Deze integratie ontgrendelt belangrijke gebruiksgevallen met RTCDP:

* Zelfde pagina/volgende hoogte-personalisatie
* Eerste/onbekende gebruikerspersonalisatie

Belangrijke functies zijn:

* Directe doelintegratie met RTCDP/[!DNL Adobe Experience Platform] op de rand (afhankelijkheid van [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations Card] met toezicht
* Randsegmentatie en randprofiel met verenigd profiel

Raadpleeg de volgende onderwerpen voor meer informatie:

* [Opmerkingen bij de release Doelen](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank}
* [Vorm verpersoonlijkingsbestemmingen voor zelfde-pagina en volgende-pagina verpersoonlijking](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank}
* [Aangepaste aanpassingsverbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} in het dialoogvenster *Overzicht van doelen* hulplijn
* [Adobe Target-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in het dialoogvenster *Overzicht van doelen* hulplijn
* [Vorm verpersoonlijkingsbestemmingen voor de zelfde pagina en volgende de gebruiksgevallen van de paginagrootte](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank}

### Aanvullende informatie

De volgende lijst toont de tijd van de segmentevaluatie voor gebeurtenissen die uit verschillende implementatiescenario&#39;s komen:

| Scenario | Edge-segment (millisecondenevaluatie) | Streaming segment (mindevaluatie) | Evaluatie van batchsegment |
| --- | --- | --- | --- |
| Gebeurtenissen/gegevens van SDK&#39;s van Adobe Experience Platform | Ja | Ja | N.v.t. |
| Gebeurtenissen van at.js | Nee | Ja | N.v.t. |
| Gebeurtenissen van mobiele SDK&#39;s van doel | Nee | Ja | N.v.t. |
| Gebeurtenissen van geüpload item | Nee | Nee | Ja |
| Gebeurtenissen van offlinegegevens (stroom) | Nee | Ja | Ja |

### Video: Volgend-raakpersonalisatie met Real-time CDP en [!DNL Adobe Target]{#RTCDP}

Leer hoe u een persoonlijke voorstelling kunt maken bij de volgende hit met [!DNL Real-time Customer Data Platform] en [!DNL Adobe Target]. De [!DNL Adobe Target] bestemming in [!DNL Real-time CDP] staat u toe te gebruiken [!DNL Experience Platform] segmenten in [!DNL Adobe Target] voor dezelfde pagina en paginagrootte personalisatie met beheer en privacyondersteuning.

Zie voor meer informatie [Volgend-klare verpersoonlijking met Real-Time CDP en Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in het dialoogvenster *Platform Tutorials* hulplijn.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Adobe Target-blog en -video:

[[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] en [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}

## Trainingsvideo: Soorten publiek gebruiken ![Zelfstudie-badge](/help/assets/tutorial.png)

Deze video bevat informatie over het gebruik van soorten publiek.

* Verklaar de term &quot;publiek&quot;
* Verklaar de twee manieren waarop het publiek voor optimalisering wordt gebruikt
* Soorten publiek zoeken in de lijst Soorten publiek
* Een activiteit toewijzen aan een publiek
* Gebruik publiek voor passieve rapportage in een activiteit

>[!VIDEO](https://video.tv.adobe.com/v/17398)
