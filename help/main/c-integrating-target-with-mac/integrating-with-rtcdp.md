---
keywords: Real-time Customer Data Platform;rtcdp;personalisatie;publiek in het publiek;publiek in het Adobe-ervaringsplatform
description: Leer hoe u de [!DNL Target]/[!DNL Real-time Customer Data Platform] (RTCDP) integratie om rijkere klantgegevens en een nog grotere personalisatie te bieden.
title: Hoe integreer ik [!DNL Target] met de [!DNL Real-time Customer Data Platform]?
feature: Integrations
exl-id: 1c066b62-91a2-4b8c-807a-3cc56fca7778
source-git-commit: 9bc31a2de295cdc5ea29dfb5ebf60fdf36705e98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Integreren met Real-time Customer Data Platform

Gebaseerd op [!DNL Adobe Experience Platform], [!DNL Real-time Customer Data Platform] (RTCDP) helpt bedrijven bekende en anonieme gegevens van veelvoudige ondernemingsbronnen samenbrengen om klantenprofielen tot stand te brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in real time te verstrekken.

Voor meer informatie over RTCDP raadpleegt u [Real-time Customer Data Platform-overzicht](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank}.

## Gebruik publiek van [!DNL Adobe Experience Platform] {#aep}

Gebruiken [publiek](/help/main/c-target/c-audiences/audiences.md) gemaakt in [!DNL Adobe Experience Platform] Verstrek rijkere klantengegevens die tot uitvoerigere verpersoonlijking leiden. De [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html){target=_blank} (RTCDP), gebaseerd op [!DNL Adobe Experience Platform]helpt bedrijven bekende en anonieme gegevens uit meerdere bedrijfsbronnen bij elkaar te brengen. Dit proces laat u klantenprofielen tot stand brengen die kunnen worden gebruikt om gepersonaliseerde klantenervaringen over alle kanalen en apparaten in real time te verstrekken.

Door verbinding te maken [!DNL Target] aan de [!DNL Real-time Customer Data Platform]kunnen klanten hun webpersonalisatie verrijken door nieuwe segmenten te ontsluiten die eerder niet toegankelijk waren voor [!DNL Target] om realtime millisecondenpersonalisatie in te schakelen op de eerste pagina van het webbezoek van een klant. Soorten publiek en profielkenmerken gebruiken die zijn gemaakt in [!DNL Adobe Experience Platform] Hiermee kunt u de beschikbare gegevenspunten uitbreiden voor een rijkere personalisatie.

Deze integratie ontgrendelt zeer belangrijke gebruiksgevallen met CDP in real time:

* Zelfde pagina/volgende hoogte-personalisatie
* Eerste/onbekende gebruikerspersonalisatie

### Belangrijkste kenmerken

Belangrijke functies zijn:

* Direct [!DNL Target] integratie met Real-Time CDP/[!DNL Adobe Experience Platform] op de rand (afhankelijkheid van [!DNL Audience Core services] - AAM)
* [!UICONTROL Target Edge Destinations Card] met governance en beleidshandhaving
* CDP-segmenten en gedeelde profielkenmerken in realtime

### Beperkingen en overwegingen met betrekking tot de eigenschapseigenschappen van CDP-profielen in realtime

Overweeg het volgende:

* Kenmerken binnen een gegeven aanbod moeten afkomstig zijn van dezelfde AEP-sandbox. (Met andere woorden, een aanbieding mag geen kenmerken van verschillende AEP-sandboxen bevatten.)
* Kenmerken binnen een bepaalde aanbieding kunnen uit verschillende bronnen afkomstig zijn; namelijk de [!DNL Target] profiel en het AEP-profiel. (Met andere woorden, u kunt kenmerken combineren, ongeacht of ze afkomstig zijn [!DNL Target] of uit het AEP-profiel.)
* Wanneer u een aanbieding definieert, kunt u standaardwaarden toewijzen voor CDP-profielkenmerken in realtime, voor het geval het kenmerk geen expliciete waarde heeft. Als een toestemmings- of governancebeleid bijvoorbeeld blokkeert dat het kenmerk wordt gebruikt in de verpersoonlijkingsservice, kan in plaats daarvan de standaardwaarde worden gebruikt.
* Wanneer gedeeld, worden de Attributen van het Profiel in real time CDP gebruikt in de Kunstmatige Intelligence/het Leren van de Machine verpersoonlijkingsmodellen voor [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] activiteiten.

>[!NOTE]
>
>De eigenschap van de Attributen van het Profiel in real time CDP is momenteel beschikbaar in Bèta voor HTML Aanbiedingen en [JSON-aanbiedingen](/help/main/c-experiences/c-manage-content/create-json-offer.md).

### Koppelingen naar meer informatie

Raadpleeg de volgende onderwerpen voor meer informatie:

* [Opmerkingen bij de release Doelen](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=en#destinations){target=_blank} in de *Opmerkingen bij de release van Adobe Experience Platform*
* [Vorm verpersoonlijkingsbestemmingen voor zelfde-pagina en volgende-pagina verpersoonlijking](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/configure-personalization-destinations.html){target=_blank} in de *Overzicht van doelen* hulplijn.
* [Aangepaste aanpassingsverbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html){target=_blank} in de *Overzicht van doelen* hulplijn
* [Adobe Target-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-target-connection.html){target=_blank} in de *Overzicht van doelen* hulplijn
* [Vorm verpersoonlijkingsbestemmingen voor de zelfde pagina en volgende de gebruiksgevallen van de paginagrootte](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} in de *Overzicht van doelen* hulplijn

### Aanvullende gegevens

Houd rekening met de volgende informatie wanneer u publiek gebruikt van [!DNL Adobe Experience Platform]:

#### Gebruikszaken aanpassen

In de volgende tabel wordt aangegeven welk type gebruiksscenario voor personalisatie (volgende sessie of dezelfde pagina) beschikbaar is wanneer u de [!DNL Adobe Experience Platform Web SDK] versus het gebruik van at.js:

| Implementatie | Oplossingen/Hoofdletters gebruiken ingeschakeld |
| --- | --- |
| at.js | **Oplossingen**:<ul><li>[!DNL Adobe Audience Manager] (AAM) en [!DNL Target]</li><li>[!DNL RTCDP] (Premium of Ultimate) en [!DNL Target]</li><li>[!DNL RTCDP] (alle SKU&#39;s), [!DNL AAM], en [!DNL Target]</li></ul>**Hoofdletters gebruiken**:<ul><li>Aanpassing van volgende sessie</li></ul> |
| [!DNL Platform Web SDK] of [!DNL AEP Server-Side API] | **Oplossingen**:<ul><li>[!DNL RTCDP] (elke SKU) en [!DNL Target]</li></ul>**Hoofdletters gebruiken**:<ul><li>Aanpassing van volgende sessie</li><li>Dezelfde pagina aanpassen via Edge</li><li>Bestuur afgedwongen bij het delen van segmenten</li></ul>**Oplossingen**:<ul><li>[!DNL RTCDP] (alle SKU&#39;s), [!DNL AAM], en [!DNL Target]</li></ul>**Hoofdletters gebruiken**:<ul><li>Aanpassing van volgende sessie</li><ul><li>[!DNL AAM] segmenten</li><li>Segmenten van derden via [!DNL AAM]</li></ul><li>Dezelfde pagina aanpassen via Edge</li><ul><li>[!DNL RTCDP] segmenten</li><li>Bestuur afgedwongen bij het delen van segmenten</li></ul> |
| Mix van [!UICONTROL at.js] en [!DNL Platform Web SDK] | **Oplossingen**:<ul><li>[!DNL RTCDP] (elke SKU) en [!DNL Target]</li></ul>**Hoofdletters gebruiken**:<ul><li>Aanpassing van volgende sessie</li><ul><li>Voor alle pagina&#39;s met [!UICONTROL at.js]</li></ul><li>Zelfde paginagrootte</li><ul><li>Voor alle pagina&#39;s met [!DNL Platform Web SDK]</li></ul></ul>**Oplossingen**:<ul><li>[!DNL RTCDP] (alle SKU&#39;s), [!DNL AAM], en [!DNL Target]</li></ul>**Hoofdletters gebruiken**:<ul><li>Aanpassing van volgende sessie</li><ul><li>Voor alle pagina&#39;s met [!UICONTROL at.js]</li><li>[!DNL AAM] segmenten</li><li>Segmenten van derden via [!DNL AAM]</li></ul> |

#### Evaluatietijd segment

De volgende lijst toont de tijd van de segmentevaluatie voor gebeurtenissen die uit verschillende implementatiescenario&#39;s komen:

| Scenario | Edge-segment (millisecondenevaluatie) | Streaming segment (mindevaluatie) | Evaluatie van batchsegment |
| --- | --- | --- | --- |
| Gebeurtenissen/gegevens van [!DNL Adobe Experience Platform] SDK&#39;s | Ja | Ja | N.v.t. |
| Gebeurtenissen van [!UICONTROL at.js] | Nee | Ja | N.v.t. |
| Gebeurtenissen van [!DNL Target Mobile] SDK&#39;s | Nee | Ja | N.v.t. |
| Gebeurtenissen van geüpload item | Nee | Nee | Ja |
| Gebeurtenissen van offlinegegevens (stroom) | Nee | Ja | Ja |

## CDP-profielkenmerken in realtime delen met [!DNL Target] {#rtcdp-profile-attributes}

CDP-profielkenmerken in realtime kunnen worden gedeeld met [!DNL Target] voor gebruik in HTML-aanbiedingen en [JSON-aanbiedingen](/help/main/c-experiences/c-manage-content/create-json-offer.md). (Merk op dat deze functie momenteel in Bèta is.)

Voorbeeld van gebruik: Als online telleraar, wilt u het AEP/Verenigde Profiel kenmerkwaarden met delen [!DNL Target] om realtime personalisatie mogelijk te maken. Door de Attributen van het Profiel in real time te gebruiken CDP, kunt u de waarde van het attribuut AEP in een [!DNL Target] aanbieden met gebruik van token replace. U kunt bijvoorbeeld personaliseren op basis van de favoriete kleur van een klant `${aep.profile.favoriteColor}`, of hun loyaliteitsrij en loyaliteitspuntwaarde die tokens gebruiken `${aep.loyalty.tier}` en `${aep.loyalty.points}`.

![aanbiedingsjson-aep-shared-attribute image](/help/main/c-experiences/c-manage-content/assets/offer-json-aep-shared-attribute.png)

Het toewijzen van standaardwaarden is optioneel.

## Video: Volgend-raakpersonalisatie met Real-time CDP en [!DNL Adobe Target]{#RTCDP}

Leer hoe u een persoonlijke voorstelling kunt maken bij de volgende hit met [!DNL Real-time Customer Data Platform] en [!DNL Adobe Target]. De [!DNL Adobe Target] bestemming in [!DNL Real-time CDP] staat u toe te gebruiken [!DNL Experience Platform] segmenten in [!DNL Adobe Target] voor dezelfde paginagropersonalisatie en paginagrootte personalisatie met beheer en privacyondersteuning.

Zie voor meer informatie [Volgend-klare verpersoonlijking met Real-Time CDP en Adobe Target](https://experienceleague.adobe.com/docs/platform-learn/tutorials/experience-cloud/next-hit-personalization.html){target=_blank} in de *Platform Tutorials* hulplijn.

>[!VIDEO](https://video.tv.adobe.com/v/340091?quality=12&learn=on)

## Adobe Target-blog en -video:

[[!DNL Adobe] announces Same Page Enhanced Personalization with [!DNL Adobe Target] en [!DNL Real-time Customer Data Platform]](https://blog.adobe.com/en/publish/2021/10/05/adobe-announces-same-page-enhanced-personalization-with-adobe-target-real-time-customer-data-platform){target=_blank}
