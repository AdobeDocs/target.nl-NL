---
keywords: doel;mobiel;doel mobiele;apparaten;apparaten;iphone;iphone modellen;apparatenatlas;display breedte;display breedte;display hoogte;type apparaat;displayheight;phone;tablet;device model
description: Leer hoe te om publiek in  [!DNL Adobe Target]  tot stand te brengen om mobiele apparaten te richten.
title: Kan ik bezoekers richten op basis van mobiele opties?
feature: Audiences
exl-id: 73d5c80c-bfa2-4806-8c04-652781b70bf2
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Mobiel

Maak een publiek in [!DNL Adobe Target] voor mobiele apparaten op basis van parameters zoals mobiel apparaat, type apparaat, leverancier van apparaten, schermafmetingen en meer.

U kunt bijvoorbeeld andere inhoud weergeven aan gebruikers die uw pagina via een telefoon bezoeken dan u zou laten zien als zij de pagina met een computer bezoeken. In dat geval kunt u het publiek van [!UICONTROL Mobile] selecteren en vervolgens de optie **[!UICONTROL Is Mobile Phone]** selecteren. Vervolgens kunt u specifieke details toevoegen die voor u van belang zijn, zoals het type telefoon, de grootte van het scherm (in pixels), enzovoort.

Het mobiele richten wordt geleverd door [&#x200B; DeviceAtlas &#x200B;](https://deviceatlas.com/device-data/user-agent-tester), de dienst van DotMobi. DeviceAtlas is een uitgebreide database van mobiele apparaten die is gebaseerd op gegevens die zijn gecompileerd uit verschillende bronnen, waaronder fabrikanten en netwerkoperatoren. Deze gegevens worden vervolgens geverifieerd, waarnaar wordt verwezen en gevalideerd om een grote en nauwkeurige database voor mobiele apparaten samen te stellen.

De opsporing van het apparaat wordt verwezenlijkt door user-Agent koorden te analyseren. Sommige apparaatfabrikanten, zoals Apple, schakelen deze functionaliteit uit door onvoldoende informatie in de UA op te geven.

Bijvoorbeeld, delen de apparaten van Apple geen apparaat model-specifieke tokens in UA. Het resultaat is dat het niet mogelijk is om iPhone-modellen (zoals iPhone 12 Pro, iPhone 12, iPhone 11 Pro Max enzovoort) te detecteren met behulp van een eenvoudige methode op basis van trefwoorden.

Om dit probleem op te lossen, verzamelt [!DNL Target] aanvullende gegevens om iPhones en andere Apple-apparaten op nauwkeurige wijze te detecteren aan de hand van de volgende parameters:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| devicePixelRatio | String | Verhouding tussen fysieke pixels en apparaatonafhankelijke pixels (dips) in de browser. Bijvoorbeeld &quot;1.5&quot; of &quot;2&quot; |
| screenOrientation | String | Het apparaat en de JavaScript-engine van de browser ondersteunen apparaatoriëntatie. Kan liggend of staand zijn. |
| webGLRenderer | String | Browserrenderer van het grafische stuurprogramma. |

>[!NOTE]
>
>Klanten die de Mobile SDK gebruiken, hoeven niets te doen om deze functionaliteit toe te passen. De klanten die at.js gebruiken moeten [&#x200B; bevorderen aan versie 1.5.0 van at.js &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} (of recenter).

U kunt meerdere eigenschappen voor mobiele apparaten kiezen. Meerdere selecties worden verbonden met een operator OR.

Klanten die een aangepaste integratie gebruiken (geen gebruik maken van at.js of de Mobile SDK) kunnen deze parameters zelf verzamelen en deze als mbox-parameters doorgeven.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]** .
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Mobile]** naar het deelvenster van de publieksbuilder.
1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

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
   >U kunt door mobiele apparatendrager richten gebruikend de [&#x200B; montages van Geo &#x200B;](/help/main/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670).

1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

In de volgende afbeelding ziet u een publiek dat gericht is op bezoekers die apparaten gebruiken die door Google zijn gemaakt en die mobiele apparaten zijn.

![&#x200B; mobiele apparaten van het Doel &#x200B;](assets/target_mobile.png)

## Overwegingen

Houd rekening met de volgende informatie wanneer u zich richt op mobiele apparaten:

### Doelapparaten met iOS 12.2 of hoger

Als gevolg van de nieuwe wijzigingen die in iOS 12.2 zijn geïntroduceerd, heeft dit gevolgen voor het maken van een publiek met regels die door [!UICONTROL Device Marketing Name] en [!UICONTROL Device Model] worden gedefinieerd en die iPhone Models opgeven. [!DNL Target] kan niet langer als doel instellen voor gebruikers die iPhones met iOS 12.2 (of hoger) op hen hebben geïnstalleerd. Als deze gebruikers echter geen iOS 12.2 (of hoger) hebben, werkt het iPhone-model nog steeds correct.

De iOS 12.2-update (of hoger) heeft geen invloed op de identificatie van de volgende modellen omdat deze modellen geen ondersteuning bieden voor de upgrade naar iOS 12.2: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad 2, iPad/Retina display, iPad Retina (vierde generatie), iPod Touch 4 en iPod Touch 5.

### Doelapparaten met Safari 14.0.2 (of hoger)

Wanneer u mobiele regels gebruikt om apparaten met Safari versie 14.0.2 (of hoger) op macOS te activeren, wordt Safari op Mac- en iPad-apparaten onjuist geïdentificeerd door [!DNL Target] wanneer u mobiele regels gebruikt voor het activeren van apparaten met Apple-gebruikersagents en DeviceAtlas. Deze kwestie zal in de toekomst worden aangepakt.

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
