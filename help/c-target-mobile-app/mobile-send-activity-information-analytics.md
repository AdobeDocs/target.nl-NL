---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: In deze sectie wordt beschreven hoe u informatie over activiteiten in de mobiele app van Adobe Target naar Adobe Analytics verzendt voor postAhoc-segmentatie.
title: Informatie over Adobe Target-activiteiten naar Adobe Analytics verzenden
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 6704ac2ec73361ad95e110e9182485537d0de642
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# Activiteitsgegevens verzenden naar Adobe Analytics{#send-activity-information-to-adobe-analytics}

In deze sectie wordt beschreven hoe u [!DNL Target] informatie over activiteiten in mobiele apps naar Adobe [!DNL Analytics] verzendt voor posthosegmentatie.

**Vereisten**

* Deze integratie vereist dat [!DNL Analytics] en [!DNL Target] worden uitgevoerd gebruikend mobiele SDK.
* Zorg ervoor dat uw rapportsuite is ingeschakeld om activiteiteninformatie van [!DNL Target] te ontvangen.

   Dit wordt gewoonlijk gedaan door [!DNL Target] cliëntcode aan [!DNL Analytics] rapportreeks toe te voegen. Dit is mogelijk al ingeschakeld als u de SiteCatalyst-Test&amp;Target-integratie gebruikt voor webactiviteiten. Neem contact op met de klantenservice van Adobe als u vragen hebt over deze stap.

1. Verkrijg de activiteiteninformatie.

   Als u een tekenreeks zoals deze in uw ervaringsinhoud opneemt, retourneert [!DNL Target] de activiteiteninformatie die u naar [!DNL Analytics] kunt verzenden:

   ```javascript
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   Vervang de tekst in uw ervaringsJson code met iets als het volgende voorbeeld:

   ```javascript
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In dit voorbeeld wordt een knooppunt met de variabele `tntVal` toegevoegd om de activiteiteninformatie te verkrijgen. Voeg vergelijkbare code toe voor de andere ervaringen, met een juiste titel en bericht.

   Deze tekenreeks levert een getal (zoals 115110:0:0) in de reactie van [!DNL Target]. Dit wijst op activiteitenidentiteitskaart, ervaring identiteitskaart, en verkeerstype. Hieronder volgt een voorbeeldreactie van [!DNL Target]:

   ```javascript
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analyseer het JSON-object.

   Analyseer de reactie die van [!DNL Target] in callback terugkwam. U kunt `NSJSONSerialization` gebruiken om deze reactie te ontleden en het op te slaan in een woordenboek of een serie.

   Verwijs naar [NSJSONSerialization documentatie](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) voor meer informatie.

1. Verzend de gegevens naar [!DNL Analytics].

   Voeg de geparseerde activiteiteninformatie (zoals `tntVal` in de bovenstaande reactie) aan uw voorwerp van contextgegevens in een [!DNL Analytics] vraag toe. Deze [!DNL Analytics] vraag die de contextgegevens bevat kan onmiddellijk worden in brand gestoken of het kan wachten tot de volgende [!DNL Analytics] vraag wordt in brand gestoken.

   Bijvoorbeeld, kan deze vraag in de callback van de `targetLoadRequest` vraag worden in brand gestoken:

   ```javascript
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`is een gereserveerde gebeurtenissleutel in de mobiele SDK. De post-classificatie van de `tntVal` variabele in [!DNL Analytics] werkt op dezelfde manier in de mobiele SDK als op het Web (JavaScript). Nadat de informatie in [!DNL Analytics] wordt verwerkt, zou u activiteit en ervaringsnamen in [!DNL Analytics] interface moeten zien.

