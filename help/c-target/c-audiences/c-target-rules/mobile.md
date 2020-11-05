---
keywords: targeting;mobile;target mobile;deviceatlas;iphone;iphone models;device atlas;displaywidth;display width;display height;type of device;displayheight;phone;tablet;device model
description: Maak in Adobe Target publiek voor mobiele apparaten op basis van parameters zoals mobiel apparaat, type apparaat, leverancier van apparaten, schermafmetingen (per pixel) en meer.
title: Mobiele opties in Adobe Target-publiek
feature: audiences
topic: Standard
uuid: a731e8c0-e9c1-4971-95b7-882cefcabfc7
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---


# Mobiel{#mobile}

Maak een publiek voor mobiele doelapparaten op basis van parameters zoals mobiel apparaat, type apparaat, leverancier van apparaat, schermafmetingen (per pixel) en meer.

U kunt bijvoorbeeld andere inhoud weergeven voor gebruikers die uw pagina invoeren via een telefoon dan voor gebruikers die een pagina bezoeken vanaf een computer. In dat geval kunt u het mobiele publiek selecteren en vervolgens de **[!UICONTROL Is Mobile Phone]** optie selecteren en vervolgens specifieke details toevoegen die voor u van belang zijn, zoals het type telefoon, de schermgrootte (in pixels), enzovoort.

Mobiel richten wordt geleverd door [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), een service van DotMobi. DeviceAtlas is een uitgebreide database van mobiele apparaten die is gebaseerd op gegevens die zijn gecompileerd uit verschillende bronnen, waaronder fabrikanten en netwerkoperatoren. Deze gegevens worden vervolgens geverifieerd, waarnaar wordt verwezen en gevalideerd om een grote en nauwkeurige database voor mobiele apparaten samen te stellen.

De opsporing van het apparaat wordt verwezenlijkt door user-Agent koorden te analyseren. Sommige apparaatfabrikanten, zoals Apple, schakelen deze functionaliteit uit door onvoldoende informatie in de UA op te geven.

Bijvoorbeeld, delen de apparaten van Apple geen apparaat model-specifieke tokens in UA. Het resultaat is dat het niet mogelijk is om iPhone-modellen (zoals iPhone 5S, iPhone SE, iPhone 6 enzovoort) te detecteren met behulp van een eenvoudige op trefwoorden gebaseerde methode.

Om dit op te lossen, verzamelt Target extra gegevens om iPhones en andere apparaten van Apple nauwkeurig te ontdekken gebruikend de volgende parameters:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| devicePixelRatio | String | Verhouding tussen fysieke pixels en apparaatonafhankelijke pixels (dips) in de browser.  bijv. &quot;1.5&quot; of &quot;2&quot; |
| screenOrientation | String | Het apparaat en de JavaScript-engine van de browser ondersteunen apparaatoriëntatie. Kan liggend of staand zijn. |
| webGLRenderer | String | Browserrenderer van het grafische stuurprogramma. |

>[!NOTE]
>
>Klanten die de SDK voor mobiele apparaten gebruiken, hoeven niets te doen om deze functionaliteit te benutten. Klanten die at.js gebruiken, moeten [upgraden naar at.js versie 1.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (of hoger).

U kunt meerdere eigenschappen voor mobiele apparaten kiezen. Meerdere selecties worden gekoppeld aan een OR.

Klanten die een aangepaste integratie gebruiken (zonder at.js of de Mobile SDK), kunnen deze parameters zelf verzamelen en deze als mbox-parameters doorgeven.

1. Klik in de [!DNL Target] interface op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Mobile]**.
1. Klik **[!UICONTROL Select]** en selecteer een van de volgende opties:

   * Marketingnaam apparaat
   * Apparaatmodel
   * Leverancier van apparaat
   * Is een mobiel apparaat
   * Is mobiele telefoon
   * Is tablet
   * OS
   * Schermhoogte (px)
   * Schermbreedte (px)

   >[!NOTE]
   >
   >Als gevolg van de nieuwe wijzigingen die in iOS 12.2 zijn geïntroduceerd, heeft dit gevolgen voor het maken van een publiek met regels die zijn gedefinieerd door de naam van het apparaat en het apparaatmodel die iPhone-modellen opgeven. We kunnen ons niet langer richten op gebruikers die iPhones met iOS 12.2 op hen hebben geïnstalleerd. Als deze gebruikers echter geen iOS 12.2 hebben, werkt het iPhone-model dat als doel is ingesteld, nog steeds correct.
   >
   >De iOS 12.2-update heeft geen invloed op de identificatie van de volgende modellen omdat deze modellen geen upgrade naar iOS 12.2 ondersteunen: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad, iPad 2, iPad / Retina display, iPad Retina (4e generatie), iPod Touch 4 en iPod Touch 5.

   >[!NOTE]
   >
   >Met de [Geo-instellingen](/help/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670)kunt u zich richten op een mobiele provider.

1. (Optioneel) Klik op aanvullende regels voor het publiek **[!UICONTROL Add Rule]** en stel deze in.
1. Klik op **[!UICONTROL Save]**.

In de volgende afbeelding wordt een publiek getoond dat doelt op bezoekers met apparaten die door Google zijn gemaakt en die een mobiel apparaat zijn.

![Doelmobiele apparaten](assets/target_mobile.png)

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
