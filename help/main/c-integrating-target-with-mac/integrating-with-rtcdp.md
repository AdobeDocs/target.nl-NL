---
keywords: Real-Time Customer Data Platform;rtcdp;personalisatie;publiek in het publiek;adobe Experience platform publiek;profielkenmerken
description: Leer hoe te om  [!DNL Target]/[!DNL Real-Time Customer Data Platform]  (RTCDP) integratie te gebruiken om rijkere klantengegevens en meer impactful personalisatie te verstrekken.
title: Hoe integreer ik  [!DNL Target]  met  [!DNL Real-Time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 4104b6cb67347205c0143c9dea46dd483a8266ce
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# Integreren met [!DNL Real-Time Customer Data Platform]

Dankzij [!DNL Adobe Experience Platform] [!DNL Real-Time Customer Data Platform] (RTCDP) kunnen bedrijven bekende en anonieme gegevens uit meerdere bedrijfsbronnen samenbrengen. Met RTCDP kunt u klantprofielen maken die kunnen worden gebruikt om in real-time persoonlijke klantenervaringen op te doen op alle kanalen en apparaten.

Voor meer informatie over RTCDP, zie [&#x200B; overzicht van Real-Time Customer Data Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=nl-NL){target=_blank}.

## Belangrijkste kenmerken

Belangrijkste kenmerken zijn:

* Directe [!DNL Target] integratie met Real-Time CDP/[!DNL Adobe Experience Platform] op de Edge (afhankelijkheid van [!DNL Audience Core services] - AAM wordt verwijderd)
* [!UICONTROL Target Edge Destinations Card] met governance en beleidshandhaving
* CDP-segmenten en gedeelde profielkenmerken in realtime

## Uitvoeringsscenario&#39;s

In de volgende secties wordt aangegeven welk type gebruiksscenario voor personalisatie (volgende sessie of dezelfde pagina) beschikbaar is wanneer u verschillende implementatiemethoden gebruikt:

### at.js-implementatie

| Oplossingen | Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] (AAM) en [!DNL Target]</li><li>[!DNL RTCDP] (Premium of Ultimate) en [!DNL Target]</li><li>[!DNL RTCDP] (any SKU), [!DNL AAM] en [!DNL Target]</li></ul> | Aanpassing van volgende sessie |

### [!DNL Adobe Experience Platform Web SDK] of [!DNL Experience Platform Server-Side API] -implementatie

| Oplossingen | Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| <ul><li>[!DNL RTCDP] (elke SKU) en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><li>Zelfstandige personalisatie via Edge</li><li>Bestuur afgedwongen bij het delen van segmenten</li></ul> |
| <ul><li>[!DNL RTCDP] (any SKU), [!DNL AAM] en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><ul><li>[!DNL AAM] segmenten</li><li>Segmenten van derden via [!DNL AAM]</li></ul><li>Zelfstandige personalisatie via Edge</li><ul><li>[!DNL RTCDP] segmenten</li><li>Bestuur afgedwongen bij het delen van segmenten</li></ul> |

### Mix van [!UICONTROL at.js] - en [!DNL Platform Web SDK] -implementatie

| Oplossingen | Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| <ul><li>[!DNL RTCDP] (elke SKU) en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><ul><li>Voor alle pagina&#39;s met [!UICONTROL at.js]</li></ul><li>Zelfde paginagrootte</li><ul><li>Voor alle pagina&#39;s met [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (any SKU), [!DNL AAM] en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><ul><li>Voor alle pagina&#39;s met [!UICONTROL at.js]</li><li>[!DNL AAM] segmenten</li><li>Segmenten van derden via [!DNL AAM]</li></ul> |

## Evaluatietijd segment

De volgende lijst toont de tijd van de segmentevaluatie voor gebeurtenissen die uit verschillende implementatiescenario&#39;s komen:

| Scenario | Edge-segment (millisecondenevaluatie) | Streaming segment (mindevaluatie) | Evaluatie van batchsegment |
| --- | --- | --- | --- |
| Gebeurtenissen/gegevens van [!DNL Adobe Experience Platform] SDK&#39;s | Ja | Ja | NVT |
| Gebeurtenissen van [!UICONTROL at.js] | Nee | Ja | NVT |
| Gebeurtenissen van [!DNL Target Mobile] SDKs | Nee | Ja | NVT |
| Gebeurtenissen van geüpload item | Nee | Nee | Ja |
| Gebeurtenissen van offlinegegevens (stroom) | Nee | Ja | Ja |

## Gebruik soorten publiek van [!DNL Adobe Experience Platform] {#aep}

Het gebruiken van [&#x200B; publiek &#x200B;](/help/main/c-target/c-audiences/audiences.md) gecreeerd in [!DNL Adobe Experience Platform] verstrekt rijkere klantengegevens die tot uitvoerigere verpersoonlijking leiden. [&#x200B; Real-Time Customer Data Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=nl-NL){target=_blank} (RTCDP), die op [!DNL Adobe Experience Platform] wordt voortgebouwd, helpt bedrijven bekende en anonieme gegevens van veelvoudige ondernemingsbronnen samenbrengen. Dit proces laat u klantenprofielen tot stand brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in real time te verstrekken.

Door [!DNL Target] aan [!DNL Real-Time Customer Data Platform] te verbinden, kunnen klanten hun Webverpersoonlijking verrijken. Dankzij deze integratie kunt u nieuwe segmenten ontgrendelen die voorheen mogelijk niet toegankelijk waren voor [!DNL Target] , zodat u in real-time milliseconde kunt aanpassen op de eerste pagina van het webbezoek van een klant. Door het gebruik van publiek- en profielkenmerken die in [!DNL Adobe Experience Platform] zijn gemaakt, kunt u de beschikbare gegevenspunten uitbreiden voor een rijkere personalisatie.

Deze integratie ontgrendelt belangrijke gebruiksgevallen met Real-Time CDP:

* Zelfde pagina/volgende hoogte-personalisatie
* Eerste/onbekende gebruikerspersonalisatie

## Real-Time CDP-profielkenmerken delen met [!DNL Target] {#rtcdp-profile-attributes}

De Attributen van het Profiel van Real-Time CDP kunnen met [!DNL Target] voor gebruik in de aanbiedingen van HTML worden gedeeld en [&#x200B; aanbiedingen JSON &#x200B;](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Beperkingen en overwegingen met betrekking tot de Real-Time CDP-profielkenmerken {#limitations}

Overweeg het volgende:

* Kenmerken binnen een bepaalde aanbieding moeten afkomstig zijn uit dezelfde [!UICONTROL Experience Platform] -sandbox. (Met andere woorden, een aanbieding mag geen kenmerken van verschillende [!UICONTROL Experience Platform] -sandboxen bevatten.)
* Kenmerken binnen een bepaalde aanbieding kunnen uit verschillende bronnen afkomstig zijn, namelijk het [!DNL Target] -profiel en het [!UICONTROL Experience Platform] -profiel. (Met andere woorden, u kunt kenmerken combineren, ongeacht of ze afkomstig zijn uit [!DNL Target] of uit het [!UICONTROL Experience Platform] -profiel.)
* Wanneer u een aanbieding definieert, kunt u standaardwaarden toewijzen voor [!UICONTROL Real-Time CDP Profile Attributes] voor het geval het kenmerk geen expliciete waarde heeft. Als een toestemmings- of governancebeleid bijvoorbeeld blokkeert dat het kenmerk wordt gebruikt in de verpersoonlijkingsservice, kan in plaats daarvan de standaardwaarde worden gebruikt.
* [!DNL Target] ondersteunt alleen het gegevenstype &quot;tekenreeks&quot; voor [!DNL Adobe Experience Platform] -profielkenmerken die in aanbiedingen moeten worden gebruikt. Kenmerken van het type &#39;Map&#39; en &#39;Array&#39; worden nog niet ondersteund.

### JSON-voorbeeldgebruikcase

Als onlinemarkering wilt u dat het AEP/Unified Profile-profiel kenmerkwaarden deelt met [!DNL Target] voor realtime personalisatie. Als u [!UICONTROL Real-Time CDP Profile Attributes] gebruikt, kunt u de waarde van het kenmerk [!UICONTROL Experience Platform] in een aanbieding [!DNL Target] weergeven met gebruik van token replace. U kunt bijvoorbeeld personaliseren op basis van de favoriete kleur van een klant met `${aep.profile.favoriteColor}` , of op basis van de waarde van de loyaliteitslaag en het loyaliteitspunt met de tokens `${aep.loyalty.tier}` en `${aep.loyalty.points}` .

Een JSON-aanbieding maken om AEP/Unified Profile-kenmerken te delen met [!DNL Target] :

1. Terwijl [&#x200B; creërend een aanbieding JSON &#x200B;](/help/main/c-experiences/c-manage-content/create-json-offer.md), van de **[!UICONTROL Select a source]** lijst, uitgezochte **[!UICONTROL Adobe Experience Platform]**.
1. Selecteer in de lijst **[!UICONTROL Select a profile sandbox name]** de gewenste sandbox.
1. Selecteer in de lijst **[!UICONTROL Select a profile attribute]** de gewenste kenmerken.
1. (Optioneel) Selecteer in de lijst **[!UICONTROL Insert a default value]** de gewenste waarden.
1. Klik op **[!UICONTROL Add]**.

In de volgende afbeelding ziet u dat twee profielkenmerken: `loyalty.tier` en `loyalty.points` zijn toegevoegd aan de JSON-aanbieding.

![&#x200B; aanbieding-json-aap-gedeeld-attributenbeeld &#x200B;](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Koppelingen naar meer informatie

Raadpleeg de volgende onderwerpen voor meer informatie:

* [&#x200B; de versienota&#39;s van Doelen &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=nl-NL#destinations){target=_blank} in de *de versienota&#39;s van Adobe Experience Platform*
* [&#x200B; vorm verpersoonlijkingsbestemmingen voor zelfde-pagina en volgende-pagina verpersoonlijking &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html?lang=nl-NL){target=_blank} in de *gids van het overzicht van Doelen*.
* [&#x200B; verbinding van Adobe Target &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html?lang=nl-NL){target=_blank} in de *overzichtsgids van Doelen*
* [&#x200B; de attributen van de Kaart &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=nl-NL#map-attributes){target=_blank} in de *overzichtsgids van Doelen*.
* [&#x200B; activeer publiek aan de bestemmingen van de randverpersoonlijking &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html?lang=nl-NL){target=_blank} in de *gids van het overzicht van Doelen*.
* [&#x200B; Zelfpagina en volgende-pagina verpersoonlijking door de  [!DNL Adobe Target]  en bestemmingen van Personalization van de Douane &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/destinations-faq.html?lang=nl-NL#same-next-page-personalization){target=_blank} onder &quot;Veelgestelde vragen&quot;in de *gids van het Overzicht van Doelen*.

## Video&#39;s en blogberichten {#videos-blogs}

In de volgende video&#39;s en blogberichten vindt u meer informatie over verbeterde personalisatie met Target en RTCDP:

### Video: Next-hit personalization with Real-Time CDP and [!DNL Adobe Target]{#RTCDP}

Leer hoe u bij de volgende druk [!DNL Real-Time Customer Data Platform] en [!DNL Adobe Target] personaliseert. Met de [!DNL Adobe Target] -bestemming in [!DNL Real-Time CDP] kunt u [!DNL Experience Platform] -segmenten in [!DNL Adobe Target] gebruiken voor dezelfde paginagrootte en paginagrootte aanpassen met ondersteuning voor beheer en privacy.

Voor meer informatie, zie [&#x200B; Volgend-raakpersonalisatie met Real-Time CDP en Adobe Target &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html?lang=nl-NL){target=_blank} in de *gids van de Leerprogramma&#39;s van het Platform*.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Video: het doel [!DNL Adobe Target] configureren in [!DNL Real-Time Customer Data Platform]

Leer hoe u de [!DNL Adobe Target] bestemming in [!DNL Real-Time Customer Data Platform] configureert voor het verzenden van segmenten en profielkenmerken van [!DNL Real-Time CDP] naar [!DNL Target] .

>[!VIDEO](https://video.tv.adobe.com/v/3449799/?learn=on&captions=dut)

### Video: segmenten en profielkenmerken activeren

Leer hoe u segmenten en profielkenmerken van [!DNL Adobe Real-Time Customer Data Platform] tot [!DNL Adobe Target] activeert om realtime gepersonaliseerde inhoud weer te geven in uw websites, mobiele apps en andere digitale eigenschappen.

>[!VIDEO](https://video.tv.adobe.com/v/3447361/?learn=on&captions=dut)

### Video: [!DNL Real-Time CDP] segmenten gebruiken in [!DNL Target]

Leer hoe u met [!DNL Real-Time Customer Data Platform] -segmenten in [!DNL Adobe Target] persoonlijke ervaringen kunt opdoen op uw website en mobiele apps.

>[!VIDEO](https://video.tv.adobe.com/v/3446833/?learn=on&captions=dut)

### Video: gebruik [!DNL Real-Time CDP] -profielkenmerken in [!DNL Adobe Target]

Leer hoe u met [!DNL Adobe Real-Time Customer Data Platform] profielkenmerken in [!DNL Adobe Target] persoonlijke ervaringen kunt opdoen op uw website en mobiele apps.

>[!VIDEO](https://video.tv.adobe.com/v/3451899/?learn=on&captions=dut)

### [!DNL Adobe Target] blog en video: uitgebreide personalisatie op dezelfde pagina

[[!DNL Adobe]  aankondigt Gelijke-Pagina Verbeterde Personalization met  [!DNL Adobe Target]  en  [!DNL Real-time Customer Data Platform] &#x200B;](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
