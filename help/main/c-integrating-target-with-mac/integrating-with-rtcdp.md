---
keywords: Real-time Customer Data Platform;rtcdp;personalisatie;publiek in het publiek;adobe Experience platform publiek;profielkenmerken
description: Leer hoe u de [!DNL Target]/[!DNL Real-Time Customer Data Platform] (RTCDP) integratie om rijkere klantgegevens en een nog grotere personalisatie te bieden.
title: Hoe integreer ik [!DNL Target] met de [!DNL Real-Time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 210e9de954dba813972b0da9a7db5b9383d3e303
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Integreren met [!DNL Real-Time Customer Data Platform]

Gebaseerd op [!DNL Adobe Experience Platform], [!DNL Real-Time Customer Data Platform] (RTCDP) helpt bedrijven bekende en anonieme gegevens uit meerdere bedrijfsbronnen bij elkaar te brengen. RTCDP laat u klantenprofielen tot stand brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in echt te verstrekken - tijd.

Voor meer informatie over RTCDP raadpleegt u [Real-time Customer Data Platform-overzicht](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}.

## Belangrijkste kenmerken

Belangrijke functies zijn:

* Direct [!DNL Target] integratie met Real-Time CDP/[!DNL Adobe Experience Platform] op de rand (afhankelijkheid van [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations Card] met governance en beleidshandhaving
* CDP-segmenten en gedeelde profielkenmerken in realtime

## Uitvoeringsscenario&#39;s

In de volgende secties wordt aangegeven welk type gebruiksscenario voor personalisatie (volgende sessie of dezelfde pagina) beschikbaar is wanneer u verschillende implementatiemethoden gebruikt:

### at.js-implementatie

| Oplossingen | Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| <ul><li>[!DNL Adobe Audience Manager] (AAM) en [!DNL Target]</li><li>[!DNL RTCDP] (Premium of Ultimate) en [!DNL Target]</li><li>[!DNL RTCDP] (alle SKU&#39;s), [!DNL AAM], en [!DNL Target]</li></ul> | Aanpassing van volgende sessie |

### [!DNL Adobe Experience Platform Web SDK] of [!DNL Experience Platform Server-Side API] uitvoering

| Oplossingen | Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| <ul><li>[!DNL RTCDP] (elke SKU) en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><li>Dezelfde pagina aanpassen via Edge</li><li>Bestuur afgedwongen bij het delen van segmenten</li></ul> |
| <ul><li>[!DNL RTCDP] (alle SKU&#39;s), [!DNL AAM], en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><ul><li>[!DNL AAM] segmenten</li><li>Segmenten van derden via [!DNL AAM]</li></ul><li>Dezelfde pagina aanpassen via Edge</li><ul><li>[!DNL RTCDP] segmenten</li><li>Bestuur afgedwongen bij het delen van segmenten</li></ul> |

### Mix van [!UICONTROL at.js] en [!DNL Platform Web SDK] uitvoering

| Oplossingen | Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| <ul><li>[!DNL RTCDP] (elke SKU) en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><ul><li>Voor alle pagina&#39;s met [!UICONTROL at.js]</li></ul><li>Zelfde paginagrootte</li><ul><li>Voor alle pagina&#39;s met [!DNL Platform Web SDK]</li></ul> |
| <ul><li>[!DNL RTCDP] (alle SKU&#39;s), [!DNL AAM], en [!DNL Target]</li></ul> | <ul><li>Aanpassing van volgende sessie</li><ul><li>Voor alle pagina&#39;s met [!UICONTROL at.js]</li><li>[!DNL AAM] segmenten</li><li>Segmenten van derden via [!DNL AAM]</li></ul> |

## Evaluatietijd segment

De volgende lijst toont de tijd van de segmentevaluatie voor gebeurtenissen die uit verschillende implementatiescenario&#39;s komen:

| Scenario | Edge-segment (millisecondenevaluatie) | Streaming segment (mindevaluatie) | Evaluatie van batchsegment |
| --- | --- | --- | --- |
| Gebeurtenissen/gegevens van [!DNL Adobe Experience Platform] SDK&#39;s | Ja | Ja | N.v.t. |
| Gebeurtenissen van [!UICONTROL at.js] | Nee | Ja | N.v.t. |
| Gebeurtenissen van [!DNL Target Mobile] SDK&#39;s | Nee | Ja | N.v.t. |
| Gebeurtenissen van geüpload item | Nee | Nee | Ja |
| Gebeurtenissen van offlinegegevens (stroom) | Nee | Ja | Ja |

## Gebruik publiek van [!DNL Adobe Experience Platform] {#aep}

Gebruiken [publiek](/help/main/c-target/c-audiences/audiences.md) gemaakt in [!DNL Adobe Experience Platform] Verstrek rijkere klantengegevens die tot uitvoerigere verpersoonlijking leiden. De [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), gebaseerd op [!DNL Adobe Experience Platform]helpt bedrijven bekende en anonieme gegevens uit meerdere bedrijfsbronnen bij elkaar te brengen. Dit proces laat u klantenprofielen tot stand brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in real time te verstrekken.

Door verbinding te maken [!DNL Target] aan de [!DNL Real-Time Customer Data Platform], kunnen klanten hun webpersonalisatie verrijken. Dankzij deze integratie kunt u nieuwe segmenten ontgrendelen die eerder niet toegankelijk waren voor [!DNL Target] om realtime millisecondenpersonalisatie in te schakelen op de eerste pagina van het webbezoek van een klant. Soorten publiek en profielkenmerken gebruiken die zijn gemaakt in [!DNL Adobe Experience Platform] Hiermee kunt u de beschikbare gegevenspunten uitbreiden voor een rijkere personalisatie.

Deze integratie ontgrendelt belangrijke gebruiksgevallen met Real-Time CDP:

* Zelfde pagina/volgende hoogte-personalisatie
* Eerste/onbekende gebruikerspersonalisatie

## Real-Time CDP-profielkenmerken delen met [!DNL Target] {#rtcdp-profile-attributes}

Real-Time CDP-profielkenmerken kunnen worden gedeeld met [!DNL Target] voor gebruik in HTML-aanbiedingen en [JSON-aanbiedingen](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Beperkingen en overwegingen met betrekking tot de Real-Time CDP-profielkenmerken

Overweeg het volgende:

* Kenmerken binnen een bepaalde aanbieding moeten van hetzelfde [!UICONTROL Experience Platform] sandbox. (Met andere woorden, een aanbieding mag geen kenmerken van verschillende [!UICONTROL Experience Platform] sandboxen.)
* Kenmerken binnen een bepaalde aanbieding kunnen uit verschillende bronnen afkomstig zijn; namelijk de [!DNL Target] en de [!UICONTROL Experience Platform] profiel. (Met andere woorden, u kunt kenmerken combineren, ongeacht of ze afkomstig zijn [!DNL Target] of van de [!UICONTROL Experience Platform] profiel.)
* Wanneer u een aanbieding definieert, kunt u standaardwaarden toewijzen voor [!UICONTROL Real-Time CDP Profile Attributes], als het kenmerk geen expliciete waarde heeft. Als een toestemmings- of governancebeleid bijvoorbeeld blokkeert dat het kenmerk wordt gebruikt in de verpersoonlijkingsservice, kan in plaats daarvan de standaardwaarde worden gebruikt.

### JSON-voorbeeldcase

Als online telleraar, wilt u het AEP/Verenigde Profiel kenmerkwaarden met delen [!DNL Target] zorgen voor realtime personalisatie. Met [!UICONTROL Real-Time CDP Profile Attributes]kunt u de waarde van de optie [!UICONTROL Experience Platform] kenmerk in een [!DNL Target] aanbieden met gebruik van token replace. U kunt bijvoorbeeld personaliseren op basis van de favoriete kleur van een klant `${aep.profile.favoriteColor}`, of hun loyaliteitsrij en loyaliteitspuntwaarde die tokens gebruiken `${aep.loyalty.tier}` en `${aep.loyalty.points}`.

Een JSON-aanbieding maken om AEP/Unified Profile-kenmerken te delen met [!DNL Target]:

1. while [een JSON-aanbieding maken](/help/main/c-experiences/c-manage-content/create-json-offer.md)van de **[!UICONTROL Select a source]** list, selecteer **[!UICONTROL Adobe Experience Platform]**.
1. Van de **[!UICONTROL Select a profile sandbox name]** selecteert u de gewenste sandbox.
1. Van de **[!UICONTROL Select a profile attribute]** selecteert u de gewenste kenmerken.
1. (Optioneel) Van de **[!UICONTROL Insert a default value]** selecteert u de gewenste waarden.
1. Klik op **[!UICONTROL Add]**.

In de volgende afbeelding ziet u twee profielkenmerken: `loyalty.tier` en `loyalty.points` zijn toegevoegd aan het JSON-aanbod.

![aanbiedingsjson-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

## Koppelingen naar meer informatie

Raadpleeg de volgende onderwerpen voor meer informatie:

* [Opmerkingen bij de release Doelen](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} in de *Opmerkingen bij de release van Adobe Experience Platform*
* [Vorm verpersoonlijkingsbestemmingen voor zelfde-pagina en volgende-pagina verpersoonlijking](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} in de *Overzicht van doelen* hulplijn.
* [Adobe Target-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in de *Overzicht van doelen* hulplijn
* [Kenmerken Kaart](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-profile-request-destinations.html?lang=en#map-attributes){target=_blank} in de *Overzicht van doelen* hulplijn.
* [Het publiek activeren voor verpersoonlijkingsdoelen van randen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html){target=_blank} in de *Overzicht van doelen* hulplijn.
* [Gelijke pagina en volgende pagina personalisatie door [!DNL Adobe Target] en Aangepaste aanpassingsdoelen](https://experienceleague.adobe.com/docs/experience-platform/destinations/destinations-faq.html?lang=en#same-next-page-personalization){target=_blank} onder &quot;Veelgestelde vragen&quot; in de *Overzicht van doelen* hulplijn.

## Video&#39;s en blogberichten {#videos-blogs}

De volgende video&#39;s en blogberichten bevatten meer informatie over verbeterde personalisatie met Target en RTCDP:

### Video: Volgend-klare personalisatie met Real-Time CDP en [!DNL Adobe Target]{#RTCDP}

Leer hoe u een persoonlijke voorstelling kunt maken bij de volgende hit met [!DNL Real-Time Customer Data Platform] en [!DNL Adobe Target]. De [!DNL Adobe Target] bestemming in [!DNL Real-Time CDP] staat u toe te gebruiken [!DNL Experience Platform] segmenten in [!DNL Adobe Target] voor dezelfde paginagropersonalisatie en paginagrootte personalisatie met beheer en privacyondersteuning.

Zie voor meer informatie [Volgend-klare personalisatie met Real-Time CDP en Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in de *Platform Tutorials* hulplijn.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

### Video: Configureer de [!DNL Adobe Target] bestemming in [!DNL Real-Time Customer Data Platform]

Leer hoe u de [!DNL Adobe Target] bestemming in [!DNL Real-Time Customer Data Platform] om segmenten en profielkenmerken te verzenden vanaf [!DNL Real-Time CDP] tot [!DNL Target].

>[!VIDEO](https://video.tv.adobe.com/v/3418799/?learn=on)

### Video: Segmenten en profielkenmerken activeren

Leer hoe u segmenten en profielkenmerken activeert vanuit [!DNL Adobe Real-Time Customer Data Platform] tot [!DNL Adobe Target] om realtime gepersonaliseerde inhoud weer te geven op uw websites, mobiele apps en andere digitale eigenschappen.

>[!VIDEO](https://video.tv.adobe.com/v/3419036/?learn=on)

### Video: Gebruiken [!DNL Real-Time CDP] segmenten in [!DNL Target]

Leren gebruiken [!DNL Real-Time Customer Data Platform] segmenten in [!DNL Adobe Target] voor persoonlijke ervaringen op uw website en mobiele apps.

>[!VIDEO](https://video.tv.adobe.com/v/3419149/?learn=on)

### Video: Gebruiken [!DNL Real-Time CDP] profielkenmerken in [!DNL Adobe Target]

Leren gebruiken [!DNL Adobe Real-Time Customer Data Platform] profielkenmerken in [!DNL Adobe Target] voor persoonlijke ervaringen op uw website en mobiele apps.

>[!VIDEO](https://video.tv.adobe.com/v/3419318/?learn=on)

### [!DNL Adobe Target] blog en video: Verbeterde personalisatie met dezelfde pagina

[[!DNL Adobe] announces Same-Page Enhanced Personalization with [!DNL Adobe Target] en [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
