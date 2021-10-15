---
keywords: doel;mobiel;doel mobiele;apparaten;apparaten;iphone;iphone modellen;apparatenatlas;display breedte;display breedte;display hoogte;type apparaat;displayheight;phone;tablet;device model
description: Leer hoe u een publiek kunt maken in [!DNL Adobe Target] om mobiele apparaten als doel in te stellen.
title: Kan ik bezoekers richten op basis van mobiele opties?
feature: Audiences
exl-id: 73d5c80c-bfa2-4806-8c04-652781b70bf2
source-git-commit: 05619301a4cd145d07abb4bf5fbe9fd44bb3d65f
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Mobiel

Maak een publiek in [!DNL Adobe Target] om mobiele apparaten als doel in te stellen op basis van parameters zoals mobiel apparaat, type apparaat, leverancier van apparaat, schermafmetingen en meer.

U kunt bijvoorbeeld andere inhoud weergeven aan gebruikers die uw pagina via een telefoon bezoeken dan u zou laten zien als zij de pagina met een computer bezoeken. In dat geval kunt u het [!UICONTROL Mobile]-publiek selecteren en vervolgens de optie **[!UICONTROL Is Mobile Phone]** selecteren. Vervolgens kunt u specifieke details toevoegen die voor u van belang zijn, zoals het type telefoon, de grootte van het scherm (in pixels), enzovoort.

Mobiel richten wordt geleverd door [DeviceAtlas](https://deviceatlas.com/device-data/user-agent-tester), een dienst van DotMobi. DeviceAtlas is een uitgebreide database van mobiele apparaten die is gebaseerd op gegevens die zijn gecompileerd uit verschillende bronnen, waaronder fabrikanten en netwerkoperatoren. Deze gegevens worden vervolgens geverifieerd, waarnaar wordt verwezen en gevalideerd om een grote en nauwkeurige database voor mobiele apparaten samen te stellen.

De opsporing van het apparaat wordt verwezenlijkt door user-Agent koorden te analyseren. Sommige apparaatfabrikanten, zoals Apple, schakelen deze functionaliteit uit door onvoldoende informatie in de UA op te geven.

Bijvoorbeeld, delen de apparaten van Apple geen apparaat model-specifieke tokens in UA. Het resultaat is dat het niet mogelijk is om iPhone-modellen (zoals iPhone 12 Pro, iPhone 12, iPhone 11 Pro Max enzovoort) te detecteren met behulp van een eenvoudige methode op basis van trefwoorden.

[!DNL Target] verzamelt aanvullende gegevens om iPhones en andere Apple-apparaten nauwkeurig te detecteren met behulp van de volgende parameters om dit probleem op te lossen:

| Parameter | Type | Beschrijving |
|--- |--- |--- |
| devicePixelRatio | String | Verhouding tussen fysieke pixels en apparaatonafhankelijke pixels (dips) in de browser. Bijvoorbeeld &quot;1.5&quot; of &quot;2&quot; |
| screenOrientation | String | Het apparaat en de JavaScript-engine van de browser ondersteunen apparaatoriëntatie. Kan liggend of staand zijn. |
| webGLRenderer | String | Browserrenderer van het grafische stuurprogramma. |

>[!NOTE]
>
>Klanten die de SDK voor mobiele apparaten gebruiken, hoeven niets te doen om deze functionaliteit toe te passen. Klanten die at.js gebruiken moeten [een upgrade uitvoeren naar at.js versie 1.5.0](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md#reference_DBB5EDB79EC44E558F9E08D4774A0F7A) (of hoger).

U kunt meerdere eigenschappen voor mobiele apparaten kiezen. Meerdere selecties worden verbonden met een operator OR.

Klanten die een aangepaste integratie gebruiken (zonder at.js of de Mobile SDK), kunnen deze parameters zelf verzamelen en deze als mbox-parameters doorgeven.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Mobile]** in de ruit van de publieksbouwer.
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
   >U kunt zich richten door mobiele apparatendrager gebruikend [Geo montages](/help/c-target/c-audiences/c-target-rules/geo.md#concept_5B4D99DE685348FB877929EE0F942670).

1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

In de volgende afbeelding ziet u een publiek dat gericht is op bezoekers die apparaten gebruiken die door Google zijn gemaakt en die mobiele apparaten zijn.

![Doelmobiele apparaten](assets/target_mobile.png)

## Overwegingen

Houd rekening met de volgende informatie wanneer u zich richt op mobiele apparaten:

### Doelapparaten met iOS 12.2 of hoger

Als gevolg van de nieuwe wijzigingen die in iOS 12.2 zijn geïntroduceerd, heeft dit gevolgen voor het maken van een publiek met regels die worden gedefinieerd door [!UICONTROL Device Marketing Name] en [!UICONTROL Device Model] die iPhone Models opgeven. [!DNL Target] kan zich niet meer richten op gebruikers die iPhones met iOS 12.2 (of later) hebben geïnstalleerd op hen. Als deze gebruikers echter geen iOS 12.2 (of hoger) hebben, werkt het iPhone-model nog steeds correct.

De iOS 12.2-update (of hoger) heeft geen invloed op de identificatie van de volgende modellen omdat deze modellen geen upgrade naar iOS 12.2 ondersteunen: iPhone, iPhone 3G, iPhone 3GS, iPhone 4, iPhone 4s, iPhone 5, iPhone 5c, iPad, iPad 2, iPad / Retina display, iPad Retina (vierde generatie), iPod Touch 4 en iPod Touch 5.

### Doelapparaten met Safari 14.0.2 (of hoger)

Wanneer u mobiele regels gebruikt om apparaten met Safari versie 14.0.2 (of hoger) op macOS te activeren, wordt Safari op Mac- en iPad-apparaten onjuist geïdentificeerd door een probleem waarbij Apple-gebruikersagents en DeviceAtlas betrokken zijn. [!DNL Target] Deze kwestie zal in de toekomst worden aangepakt.

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
