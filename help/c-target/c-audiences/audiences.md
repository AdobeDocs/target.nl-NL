---
keywords: publiek;publieksregels;publiek maken;publiek maken;publiek instellen;publiek rapporteren;publiek rapporteren;segment;aangepaste profielparameters;publieksdefinitie;publiekslijst
description: Leer hoe te om [!UICONTROL Audiences] lijst in  [!DNL Adobe Target] te gebruiken.
title: Hoe gebruik ik de Audience List?
feature: Soorten publiek
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: a2b3bf75e8b14c3068b8dba59f31d2577d9cec29
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 0%

---

# Soorten publiek maken

Het publiek in [!DNL Adobe Target] bepaalt wie inhoud en ervaringen in een gerichte activiteit ziet.

Het publiek wordt gebruikt overal waar het richten beschikbaar is. Wanneer u een activiteit als doel instelt, hebt u de volgende opties:

* Selecteer een herbruikbaar publiek in de lijst [!UICONTROL Audiences]
* [Een activiteitspecifiek ](/help/c-target/creating-activity-only-audience.md) publiek maken en dit als doel instellen
* [Meerdere ](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) doelgroepen combineren om een ad-hocpubliek te maken

U kunt publieksgegevens ook gebruiken die door [!DNL Adobe Analytics] voor het in real time richten en verpersoonlijken in [!DNL Target] en andere [!DNL Adobe Experience Cloud] toepassingen worden verzameld. Zie [Experience Cloud Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) in de handleiding *Experience Cloud Central Interface Components*.

Er zijn twee soorten publiek in [!DNL Target]:

* **Doelgroepen:** gebruikt voor het leveren van verschillende inhoud aan verschillende typen bezoekers.
* **Meldend publiek:** gebruikt om te bepalen hoe de verschillende types bezoekers aan de zelfde inhoud antwoorden zodat kunt u uw testresultaten analyseren.

   In [!DNL Target], kunt u rapportpubliek vormen slechts als u [!DNL Target] als uw rapporteringsbron gebruikt. Als u [Adobe Analytics als rapportbron](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt, moet u uw rapporteringspubliek binnen [!DNL Analytics] vormen.

## De lijst [!UICONTROL Audiences] gebruiken {#use-list}

Als u de lijst [!UICONTROL Audiences] wilt openen, klikt u op **[!UICONTROL Audiences]** in de bovenste menubalk:

![[!UICONTROL Audiences] list](assets/audiences_list.png)

De lijst [!UICONTROL Audiences] bevat het publiek dat u in uw activiteiten kunt gebruiken. Met de lijst [!UICONTROL Audiences] kunt u soorten publiek maken, bewerken, dupliceren, kopiëren of combineren. De lijst toont ook de bron waar het publiek werd gecreeerd:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

   >[!NOTE]
   >
   >De [!DNL Adobe Experience Platform]-bron bevindt zich in een bètatestprogramma, maar is beschikbaar voor alle [!DNL Target]-klanten die de [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) gebruiken. Publiek beschikbaar bij [!DNL Adobe Experience Platform] kan worden gebruikt zoals is of [gecombineerd met bestaand publiek](/help/c-target/combining-multiple-audiences.md).

Vooraf gedefinieerde doelgroepen, zoals &quot;[!UICONTROL New Visitors]&quot; en &quot;[!UICONTROL Returning Visitors]&quot;, kunnen niet worden hernoemd.

Als u werkt met soorten publiek die oorspronkelijk zijn gemaakt in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform], [!DNL Target], wordt u gewaarschuwd als u verwijst naar een publiek in [!DNL Target]-activiteiten die later zijn verwijderd in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform].

* Als een publiek in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform] werd geschrapt, toont een waarschuwingspictogram in zowel [!UICONTROL Audience] lijst als de publieksplukker. Een tooltip in [!DNL Target] UI wijst ook erop dat het publiek in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform] werd geschrapt.
* Als u meerdere soorten publiek probeert te combineren met een verwijderd publiek of als u een activiteit probeert op te slaan die verwijst naar een verwijderd publiek, wordt een waarschuwingsbericht weergegeven.

U kunt ook aangepaste profielparameters en `user.` parameters als doel instellen. Wanneer het creëren van een publiek, sleep de attributen u wilt gebruiken om uw activiteit in het venster van de publieksbouwer te richten. Als het gewenste kenmerk niet wordt weergegeven, is het kenmerk niet geactiveerd door een mbox. Andere aangepaste mbox-parameters zijn beschikbaar in de vervolgkeuzelijst [!UICONTROL Custom Parameters].

Met de knop [!UICONTROL Filters] kunt u de lijst [!UICONTROL Audiences] filteren op bron: [!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud] en [!DNL Adobe Experience Platform].

![De optie Filters in de  [!UICONTROL Audiences] lijst](assets/filters.png)

Gebruik het vakje [!UICONTROL Search audiences] om uw [!UICONTROL Audiences] lijst te zoeken. U kunt zoeken naar een willekeurig deel van een publieksnaam of u kunt een specifieke tekenreeks tussen aanhalingstekens plaatsen.

U kunt de lijst [!UICONTROL Audiences] sorteren op publieksnaam of op de datum waarop het voor het laatst werd gewijzigd. Als u op naam of datum wilt sorteren, klikt u op de kolomkop en selecteert u deze om het publiek in oplopende of aflopende volgorde weer te geven.

## Scherptedefinities weergeven {#section_11B9C4A777E14D36BA1E925021945780}

U kunt de details van de publieksdefinitie op een pop-up kaart op diverse plaatsen in [!DNL Target] UI bekijken zonder het publiek te openen. Deze functionaliteit is van toepassing op publiek dat is gemaakt in [!DNL Target Standard/Premium] en publiek dat is geïmporteerd uit [!DNL Target Classic] of gemaakt via API.

De volgende publieksdefinitiekaart is bijvoorbeeld toegankelijk door op het pictogram [!UICONTROL View Details] voor het gewenste publiek te klikken:

![Activiteiten > Definitie van publiek](assets/audience_definition_list.png)

De volgende publieksdefinitiekaart wordt betreden door het [!UICONTROL View Details] pictogram op de pagina [!UICONTROL Overview] van een activiteit te klikken:

![Activiteiten > Definitie van publiek](assets/view-details-activity-overview.png)

De publieksdefinitiekaart toont zij het type, de bron, en de attributen van het publiek. Klik **[!UICONTROL View full details]** om andere activiteiten te zien die van dat publiek, als toepasselijk verwijzen. Als u een publieksdefinitiekaart van een activiteit [!UICONTROL Overview] pagina bekijkt, klik **[!UICONTROL Audience Usage]**.

De informatie over het gebruik van het publiek kan u helpen onbedoelde gevolgen voor andere activiteiten te vermijden terwijl het uitgeven van publiek. De informatie omvat [!UICONTROL Live Activities], [!UICONTROL Inactive Activities], [!UICONTROL Archived Activities], en [!UICONTROL Syncing Activities]. Deze functie is beschikbaar voor alle soorten publiek (bibliotheekpubliek en [alleen-activiteit](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Als een publiek [met een ander publiek](/help/c-target/combining-multiple-audiences.md) wordt gecombineerd en het gecombineerde publiek wordt gebruikt om een activiteit tot stand te brengen, maakt de gebruiksinformatie voor beide publiek een lijst van die pas gecreëerde activiteit.

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

## Trainingsvideo: Soorten publiek ![Zelfstudie-badge](/help/assets/tutorial.png) gebruiken

Deze video bevat informatie over het gebruik van soorten publiek.

* Verklaar de term &quot;publiek&quot;
* Verklaar de twee manieren waarop het publiek voor optimalisering wordt gebruikt
* Soorten publiek zoeken in de lijst Soorten publiek
* Een activiteit toewijzen aan een publiek
* Gebruik publiek voor passieve rapportage in een activiteit

>[!VIDEO](https://video.tv.adobe.com/v/17398)
