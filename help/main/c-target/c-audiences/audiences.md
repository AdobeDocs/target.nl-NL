---
keywords: publiek;publieksregels;publiek maken;publiek maken;publiek instellen;publiek rapporteren;publiek rapporteren;segment;aangepaste profielparameters;publieksdefinitie;publiekslijst
description: Leer hoe te om publiek in  [!DNL Adobe Target] te gebruiken.
title: Hoe gebruik ik de Audience List?
feature: Audiences
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Soorten publiek maken

Soorten publiek in [!DNL Adobe Target] bepalen wie inhoud en ervaringen in een doelactiviteit ziet.

Het publiek wordt gebruikt overal waar het richten beschikbaar is. Wanneer u een activiteit als doel instelt, hebt u de volgende opties:

* Selecteer een herbruikbaar publiek in de lijst [!UICONTROL Audiences]
* [&#x200B; creeer een activiteit-specifiek publiek &#x200B;](/help/main/c-target/creating-activity-only-audience.md) en richt het
* [&#x200B; combineer veelvoudige publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) om een ad hoc publiek tot stand te brengen

U kunt ook publieksgegevens gebruiken die door [!DNL Adobe Analytics] zijn verzameld voor realtime doelen en personalisatie in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -toepassingen. Zie [&#x200B; het Soorten publiek van Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=nl-NL) in de *3&rbrace; gids van de Componenten van de Interface van Experience Cloud Centrale.*

Er zijn twee soorten publiek in [!DNL Target]:

* **richtend publiek:** Gebruikt om verschillende inhoud aan verschillende soorten bezoekers te leveren.
* **Meldend publiek:** gebruikt om te bepalen hoe de verschillende types van bezoekers aan de zelfde inhoud antwoorden zodat kunt u uw testresultaten analyseren.

  In [!DNL Target] kunt u het rapportpubliek alleen configureren als u [!DNL Target] als rapportbron gebruikt. Als u [&#x200B; Adobe Analytics als uw rapporteringsbron &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt, moet u uw rapporterend publiek binnen vormen [!DNL Analytics].

## De lijst [!UICONTROL Audiences] gebruiken {#use-list}

Als u de lijst [!UICONTROL Audiences] wilt openen, klikt u op **[!UICONTROL Audiences]** in de bovenste menubalk:

![[!UICONTROL Audiences] list &#x200B;](assets/audiences_list.png)

De lijst [!UICONTROL Audiences] bevat het publiek dat u kunt gebruiken in uw activiteiten. Met de lijst [!UICONTROL Audiences] kunt u soorten publiek maken, bewerken, dupliceren, kopiëren of combineren. De lijst toont ook de bron waar het publiek werd gecreeerd:

* [!DNL Adobe Target]
* [!DNL Adobe Target Classic]
* [!DNL Experience Cloud]
* [!DNL Adobe Experience Platform]

  >[!NOTE]
  >
  >De [!DNL Adobe Experience Platform] bron is beschikbaar aan alle [!DNL Target] klanten die [&#x200B; SDK van het Web van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} gebruiken. Het publiek beschikbaar van [!DNL Adobe Experience Platform] kan worden gebruikt zoals is of [&#x200B; gecombineerd met bestaand publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md).
  >
  >Gebruikers moeten de status [!UICONTROL Approver] of hoger in [!DNL Target] hebben om [!DNL Target] [!UICONTROL Destinations] -kaarten in AEP/RTCDP ([!DNL Real-time Customer Data Platform]) te configureren.
  >
  >Voor meer informatie zie [&#x200B; publiek van het Gebruik van Adobe Experience Platform &#x200B;](#aep).

Vooraf gedefinieerde soorten publiek, zoals &quot;[!UICONTROL New Visitors]&quot; en &quot;[!UICONTROL Returning Visitors]&quot;, kunnen niet worden hernoemd.

Wanneer u werkt met soorten publiek die oorspronkelijk zijn gemaakt in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform] , geeft [!DNL Target] een waarschuwing als u verwijst naar een publiek in [!DNL Target] -activiteiten die later zijn verwijderd in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform] .

* Als een publiek in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform] is verwijderd, wordt een waarschuwingspictogram weergegeven in zowel de [!UICONTROL Audience] -lijst als de publiekskiezer. Een knopinfo in de gebruikersinterface van [!DNL Target] geeft ook aan dat het publiek is verwijderd in [!DNL Experience Cloud] of [!DNL Adobe Experience Platform] .
* Als u meerdere soorten publiek probeert te combineren met een verwijderd publiek of als u een activiteit probeert op te slaan die verwijst naar een verwijderd publiek, wordt een waarschuwingsbericht weergegeven.

U kunt ook aangepaste profielparameters en `user.` -parameters als doel instellen. Wanneer het creëren van een publiek, sleep de attributen u wilt gebruiken om uw activiteit in het venster van de publieksbouwer te richten. Als het gewenste kenmerk niet wordt weergegeven, is het kenmerk niet geactiveerd door een mbox. De vervolgkeuzelijst [!UICONTROL Custom Parameters] bevat andere aangepaste parameters voor de box.

Gebruik de knop [!UICONTROL Filters] om de [!UICONTROL Audiences] -lijst te filteren op bron: [!DNL Adobe Target] , [!DNL Adobe Target Classic] , [!DNL Experience Cloud] en [!DNL Adobe Experience Platform] .

![&#x200B; optie van Filters in de [!UICONTROL Audiences] lijst &#x200B;](assets/filters.png)

Gebruik het vak [!UICONTROL Search audiences] om te zoeken in de lijst van [!UICONTROL Audiences] . U kunt zoeken naar een willekeurig deel van een publieksnaam of u kunt een specifieke tekenreeks tussen aanhalingstekens plaatsen.

U kunt de [!UICONTROL Audiences] lijst sorteren op publieksnaam of op de datum waarop deze voor het laatst is gewijzigd. Als u op naam of datum wilt sorteren, klikt u op de kolomkop en selecteert u deze om het publiek in oplopende of aflopende volgorde weer te geven.

## Scherptedefinities weergeven {#section_11B9C4A777E14D36BA1E925021945780}

U kunt de definitiedetails van het publiek op een pop-up kaart op diverse plaatsen in [!DNL Target] UI bekijken zonder het publiek te openen. Deze functionaliteit is van toepassing op publiek dat is gemaakt in [!DNL Target Standard/Premium] en publiek dat is geïmporteerd uit [!DNL Target Classic] of gemaakt via API.

De volgende publieksdefinitiekaart is bijvoorbeeld toegankelijk door op het pictogram [!UICONTROL View Details] voor het gewenste publiek te klikken:

![&#x200B; Activiteiten > de definitie van het Publiek &#x200B;](assets/audience_definition_list.png)

De volgende publieksdefinitiekaart wordt benaderd door op het pictogram [!UICONTROL View Details] op de pagina van een activiteit [!UICONTROL Overview] te klikken:

![&#x200B; Activiteiten > de definitie van het Publiek &#x200B;](assets/view-details-activity-overview.png)

De publieksdefinitiekaart toont zij het type, de bron, en de attributen van het publiek. Klik op **[!UICONTROL View full details]** om andere activiteiten weer te geven die naar dat publiek verwijzen, indien van toepassing. Als u een publieksdefinitiekaart van de pagina van een activiteit [!UICONTROL Overview] bekijkt, klik **[!UICONTROL Audience Usage]**.

De informatie over het gebruik van het publiek kan u helpen onbedoelde gevolgen voor andere activiteiten te vermijden terwijl het uitgeven van publiek. Voorbeelden van informatie zijn [!UICONTROL Live Activities] , [!UICONTROL Inactive Activities] , [!UICONTROL Archived Activities] en [!UICONTROL Syncing Activities] . Deze eigenschap is beschikbaar voor alle publiek (het publiek van de Bibliotheek en [&#x200B; activiteit-slechts publiek &#x200B;](/help/main/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Als een publiek [&#x200B; met een ander publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md) wordt gecombineerd en het gecombineerde publiek wordt gebruikt om een activiteit tot stand te brengen, maakt de gebruiksinformatie voor beide publiek een lijst dat de pas gecreëerde activiteit.

![&#x200B; publiek_definition_list_usage beeld &#x200B;](assets/audience_definition_list_usage.png)

<!--The following audience definition card is for an audience imported from the Adobe Experience Cloud. In this instance, the audience was imported from Adobe Audience Manager (AAM).

![Usage tab on Audience Definition card](assets/audience_definition_mc.png)

The following details are available for these imported audience types:

| Audience Type | Details |
|--- |--- |
|Mobile audience|Marketing Name, Vendor, and Model.<br>The `matches | does not match` operator displays instead of `equals | does not equal`<br>![Imported Mobile Audience](/help/main/c-target/c-audiences/assets/imported_mobile_audience.png).|
|Visitor-behavior audience|**user.categoryAffinity:** `categoryAffinity` with `FAVORITE` parameter.<br>![Imported Category Affinity](/help/main/c-target/c-audiences/assets/imported_category_affinity.png)<br>**Monitoring:** Monitoring service equals true.<br>**No Monitoring Service:** Monitoring service equals false.<br>![Imported Monitoring](/help/main/c-target/c-audiences/assets/imported_monitoring.png)|
|Audiences using the NOT operator|**Single Rule:** Target displays the audience in the format `[All Visitor AND [NOT [rule]`. Single NOT rule displays with AND with `AllVisitor` audience.<br>![Imported Not Audience](/help/main/c-target/c-audiences/assets/imported_not_audience.png)|

Keep the following points in mind as you work with imported audiences:

* Expression target audiences are no longer supported in Target Standard/Premium. 
* Target Standard/Premium does not support some deprecated audiences or has improved operators for ease of use. Because of this, the definition of an imported audience, although working as per definition, does not mean that same is now available for creation in the Standard/Premium interface. For example, Social Audiences are visible with their rules but Target Standard/Premium does not allow social audiences to be created.-->

## Gebruik soorten publiek van [!DNL Adobe Experience Platform] {#aep}

Het gebruik van publiek dat in [!DNL Adobe Experience Platform] is gemaakt, levert rijkere klantgegevens die tot een onuitvoerbaardere personalisatie leiden.

Voor meer informatie, zie [&#x200B; publiek van het Gebruik van  [!DNL Adobe Experience Platform]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#aep).

## De video van de opleiding: Het gebruiken van de badge van het publiek ![&#x200B; Zelfstudie &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik van soorten publiek.

* Verklaar de term &quot;publiek&quot;
* Verklaar de twee manieren waarop het publiek voor optimalisering wordt gebruikt
* Soorten publiek zoeken in de lijst Soorten publiek
* Een activiteit toewijzen aan een publiek
* Gebruik publiek voor passieve rapportage in een activiteit

>[!VIDEO](https://video.tv.adobe.com/v/17398)
