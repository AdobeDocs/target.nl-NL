---
keywords: publiek;publieksregels;publiek maken;publiek maken;publiek instellen;publiek rapporteren;publiek rapporteren;segment;aangepaste profielparameters;publieksdefinitie;publiekslijst
description: Leer hoe te om de [!UICONTROL Audiences] lijst in Adobe te gebruiken [!DNL Target] en hoe te om de kaarten van de Definitie van het publiek te bekijken die publieksdetails en gebruiksinformatie bevatten.
title: Hoe gebruik ik de Audience List?
feature: Soorten publiek
exl-id: 7af7f101-f550-4fdc-bcd9-90e4107b0415
source-git-commit: 06a5fda72a649c4037cb78d3e670747cd297a64d
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Soorten publiek maken

Het publiek in [!DNL Adobe Target] bepaalt wie inhoud en ervaringen in een gerichte activiteit ziet.

Het publiek wordt gebruikt overal waar het richten beschikbaar is. Wanneer u zich richt op een activiteit, kunt u de volgende opties hebben:

* Selecteer een herbruikbaar publiek in de lijst [!UICONTROL Audiences]
* [Een activiteitspecifiek ](/help/c-target/creating-activity-only-audience.md) publiek maken en dit als doel instellen
* [Meerdere ](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) doelgroepen combineren om een ad-hocpubliek te maken

U kunt publieksgegevens ook gebruiken die door [!DNL Adobe Analytics] voor het in real time richten en verpersoonlijken in [!DNL Target] en andere [!DNL Adobe Experience Cloud] toepassingen worden verzameld. Zie [Experience Cloud Soorten publiek](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) in de handleiding *Experience Cloud Central Interface Components*.

[!DNL Target] definieert twee soorten publiek:

* **Doelgroepen:** gebruikt voor het leveren van verschillende inhoud aan verschillende typen bezoekers.
* **Meldend publiek:** gebruikt om te bepalen hoe de verschillende types bezoekers aan de zelfde inhoud antwoorden zodat kunt u uw testresultaten analyseren.

   In [!DNL Target], kunt u rapportpubliek vormen slechts als u [!DNL Target] als uw rapporteringsbron gebruikt. Als u [Adobe Analytics als rapportbron](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruikt, moet u uw rapporteringspubliek binnen [!DNL Analytics] vormen.

## De lijst [!UICONTROL Audiences] gebruiken

Als u de lijst [!UICONTROL Audiences] wilt openen, klikt u op **[!UICONTROL Audiences]** in de bovenste menubalk:

![[!UICONTROL Audiences] list](/help/c-target/c-audiences/assets/audiences_list.png)

De lijst [!UICONTROL Audiences] bevat alle soorten publiek die u in uw activiteiten kunt gebruiken. Met de lijst [!UICONTROL Audiences] kunt u soorten publiek maken, bewerken, verwijderen, kopiëren of combineren. De lijst toont ook de bron waar het publiek werd gecreeerd ([!DNL Target], [!DNL Target Classic], en [!DNL Experience Cloud]. Vooraf gedefinieerde doelgroepen, zoals &quot;[!UICONTROL New Visitors]&quot; en &quot;[!UICONTROL Returning Visitors]&quot;, kunnen niet worden hernoemd.

Wanneer het werken met publiek dat oorspronkelijk in [!DNL Experience Cloud] werd gecreeerd, het alarm van het Doel u als u een publiek in [!DNL Target] activiteiten van verwijzingen voorziet die later in [!DNL Experience Cloud] zijn geschrapt.

* Als een publiek in [!DNL Experience Cloud] werd geschrapt, toont een waarschuwingspictogram in zowel [!UICONTROL Audience] lijst als de publieksplukker. Een hulpmiddel-uiteinde in UI wijst ook erop dat het publiek in [!DNL Experience Cloud] werd geschrapt.
* Als u meerdere soorten publiek probeert te combineren met een verwijderd publiek of als u een activiteit probeert op te slaan die verwijst naar een verwijderd publiek, wordt een waarschuwingsbericht weergegeven.

U kunt ook aangepaste profielparameters en `user.` parameters als doel instellen. Wanneer u een publiek toevoegt, klikt u op het kenmerk dat u wilt gebruiken om uw activiteit als doel in te stellen. Als het gewenste kenmerk niet wordt weergegeven, is het kenmerk niet geactiveerd door een mbox. Andere aangepaste mbox-parameters zijn beschikbaar in de vervolgkeuzelijst [!UICONTROL Custom Parameters].

Met de knop [!UICONTROL Filters] kunt u de lijst [!UICONTROL Audiences] filteren op bron: [!DNL Adobe Target], [!DNL Adobe Target Classic] en [!DNL Experience Cloud].

![De optie Filters in de  [!UICONTROL Audiences] lijst](/help/c-target/c-audiences/assets/filters.png)

Gebruik het vakje [!UICONTROL Search audiences] om uw [!UICONTROL Audiences] lijst te zoeken. U kunt zoeken naar een willekeurig deel van een publieksnaam of u kunt een specifieke tekenreeks tussen aanhalingstekens plaatsen.

U kunt de lijst [!UICONTROL Audiences] sorteren op publieksnaam of op de datum waarop het voor het laatst werd gewijzigd. Als u op naam of datum wilt sorteren, klikt u op de kolomkop en selecteert u deze om het publiek in oplopende of aflopende volgorde weer te geven.

## Scherptedefinities weergeven {#section_11B9C4A777E14D36BA1E925021945780}

U kunt de details van de publieksdefinitie op een pop-up kaart op diverse plaatsen in het Doel UI bekijken zonder het publiek te openen. Deze functionaliteit is van toepassing op publiek dat is gemaakt in [!DNL Target Standard/Premium] en publiek dat is geïmporteerd uit [!DNL Target Classic] of gemaakt via API.

De volgende publieksdefinitiekaart is bijvoorbeeld toegankelijk door op het pictogram [!UICONTROL View Details] voor het gewenste publiek te klikken:

![Activiteiten > Definitie van publiek](assets/audience_definition_list.png)

De volgende publieksdefinitiekaart wordt betreden door het [!UICONTROL View Details] pictogram op de pagina [!UICONTROL Overview] van een activiteit te klikken:

![Activiteiten > Definitie van publiek](/help/c-target/c-audiences/assets/view-details-activity-overview.png)

De publieksdefinitiekaart toont zij het type, de bron, en de attributen van het publiek. Klik **[!UICONTROL View full details]** om andere activiteiten te zien die van dat publiek, als toepasselijk verwijzen. Als u een publieksdefinitiekaart van een activiteit [!UICONTROL Overview] pagina bekijkt, klik **[!UICONTROL Audience Usage]**.

De informatie over het gebruik van het publiek kan u helpen onbedoelde gevolgen voor andere activiteiten te vermijden terwijl het uitgeven van publiek. De informatie omvat Live-activiteiten, inactieve activiteiten, gearchiveerde activiteiten en synchronisatieactiviteiten. Deze functie is beschikbaar voor alle soorten publiek (bibliotheekpubliek en [alleen-activiteit](/help/c-target/creating-activity-only-audience.md#concept_A6BADCF530ED4AE1852E677FEBE68483)).

Als een publiek met een ander publiek wordt gecombineerd en het gecombineerde publiek wordt gebruikt om een activiteit tot stand te brengen, maakt de gebruiksinformatie voor beide publiek een lijst van die pas gecreëerde activiteit.

![](assets/audience_definition_list_usage.png)

De volgende publieksdefinitiekaart is voor een publiek dat uit Adobe Experience Cloud wordt ingevoerd. In dit geval is het publiek geïmporteerd uit Adobe Audience Manager (AAM).

![Het lusje van het gebruik op de kaart van de Definitie van het Publiek](assets/audience_definition_mc.png)

De volgende details zijn beschikbaar voor deze geïmporteerde publiekstypen:

| Type publiek | Details |
|--- |--- |
| Mobiel publiek | Marketingnaam, leverancier en model.<br>De  `matches | does not match` operator wordt weergegeven in plaats van  `equals | does not equal`<br>![Geïmporteerd mobiel publiek](/help/c-target/c-audiences/assets/imported_mobile_audience.png). |
| Bezoekersgedrag publiek | **user.categoryAffinity:** `categoryAffinity` met  `FAVORITE` parameter.<br>![Geïmporteerde Categorie ](/help/c-target/c-audiences/assets/imported_category_affinity.png)<br>**AffinityMonitoring:** Monitoring-service is waar.<br>**Geen bewakingsservice:** bewakingsservice is false.<br>![Geïmporteerde controle](/help/c-target/c-audiences/assets/imported_monitoring.png) |
| Soorten publiek met de operator NOT | **Eén regel:** doel geeft het publiek weer in de indeling  `[All Visitor AND [NOT [rule]`. De enige regel NOT toont met EN met `AllVisitor` publiek.<br>![Geïmporteerd niet publiek](/help/c-target/c-audiences/assets/imported_not_audience.png) |

Houd bij het werken met geïmporteerde soorten publiek rekening met de volgende punten:

* Doelpubliek van expressie wordt niet meer ondersteund in Target Standard/Premium.
* De Standaard/Premium van het doel steunt sommige verouderde doelgroepen niet of heeft betere exploitanten voor gebruiksgemak. Daarom betekent de definitie van een geïmporteerd publiek, hoewel het volgens definitie werkt, niet dat dit nu beschikbaar is voor ontwerpen in de Standard/Premium-interface. Sociale doelgroepen zijn bijvoorbeeld zichtbaar met hun regels, maar met Target Standard/Premium kunnen geen sociale doelgroepen worden gecreëerd.

## Trainingsvideo: Soorten publiek ![Zelfstudie-badge](/help/assets/tutorial.png) gebruiken

Deze video bevat informatie over het gebruik van soorten publiek.

* Verklaar de term &quot;publiek&quot;
* Verklaar de twee manieren waarop het publiek voor optimalisering wordt gebruikt
* Soorten publiek zoeken in de lijst Soorten publiek
* Een activiteit toewijzen aan een publiek
* Gebruik publiek voor passieve rapportage in een activiteit

>[!VIDEO](https://video.tv.adobe.com/v/17398)
