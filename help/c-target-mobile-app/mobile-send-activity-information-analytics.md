---
keywords: mobile;tntVal;analytics;adobe analytics;integration;sdk;mobile sdk;
description: In deze sectie wordt beschreven hoe u informatie over activiteiten in de mobiele app van Adobe Target naar Adobe Analytics verzendt voor postAhoc-segmentatie.
title: Informatie over Adobe Target-activiteiten naar Adobe Analytics verzenden
feature: mobile implementation
uuid: 2ca1ebfe-5008-4a73-a032-1ad81f062925
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# Activiteitsgegevens naar Adobe Analytics verzenden{#send-activity-information-to-adobe-analytics}

In deze sectie wordt beschreven hoe u informatie over activiteiten in [!DNL Target] mobiele apps naar Adobe verzendt [!DNL Analytics] voor posthosegmentatie.

**Vereisten**

* Deze integratie vereist dat [!DNL Analytics] en [!DNL Target] worden geïmplementeerd met de mobiele SDK.
* Zorg ervoor dat uw rapportsuite is ingeschakeld voor het ontvangen van activiteitengegevens van [!DNL Target].

   Dit wordt gewoonlijk gedaan door de [!DNL Target] cliëntcode aan de [!DNL Analytics] rapportreeks toe te voegen. Dit is mogelijk al ingeschakeld als u de SiteCatalyst-Test&amp;Target-integratie gebruikt voor webactiviteiten. Neem contact op met de klantenservice van Adobe als u vragen hebt over deze stap.

1. Verkrijg de activiteiteninformatie.

   Als u een tekenreeks als deze in uw ervaringsinhoud opneemt, [!DNL Target] worden de activiteitengegevens geretourneerd die u kunt verzenden naar [!DNL Analytics]:

   ```
   ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}
   ```

   Vervang de tekst in uw ervaringsJson code met iets als het volgende voorbeeld:

   ```
   { 
     "tntVal": ${campaign.id}:${campaign.recipe.id}:${campaign.recipe.trafficType}", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

   In dit voorbeeld `tntVal` wordt een knooppunt met de variabele toegevoegd om de activiteiteninformatie te verkrijgen. Voeg vergelijkbare code toe voor de andere ervaringen, met een juiste titel en bericht.

   Deze tekenreeks levert een getal (zoals 115110:0:0) in de reactie van [!DNL Target]. Dit wijst op activiteitenidentiteitskaart, ervaring identiteitskaart, en verkeerstype. Hieronder volgt een voorbeeldreactie van [!DNL Target]:

   ```
   { 
     "tntVal": 115110:0:0", 
     "title":"Welcome Message", 
     "message":"Get Free Shipping Today!" 
   }
   ```

1. Analyseer het JSON-object.

   Parseer de reactie die terugkwam [!DNL Target] in de callback. U kunt deze reactie parseren `NSJSONSerialization` en opslaan in een woordenboek of een array.

   Verwijs naar de documentatie [van](https://developer.apple.com/library/ios/documentation/Foundation/Reference/NSJSONSerialization_Class/#//apple_ref/occ/clm/NSJSONSerialization/JSONObjectWithData:options:error) NSJSONSerialization voor meer informatie.

1. Verzend de gegevens naar [!DNL Analytics].

   Voeg de geparseerde activiteiteninformatie (zoals `tntVal` in de bovenstaande reactie) aan uw voorwerp van contextgegevens in een [!DNL Analytics] vraag toe. Deze [!DNL Analytics] vraag die de contextgegevens bevat kan onmiddellijk worden in brand gestoken of het kan wachten tot de volgende [!DNL Analytics] vraag wordt in brand gestoken.

   Bijvoorbeeld, kan deze vraag in callback van de `targetLoadRequest` vraag worden in brand gestoken:

   ```
   [ADBMobile trackAction:@"Welcome Screen"  
         data:@{@"&&tnt" : tntVal from response}];
   ```

   >[!NOTE]
   >
   >`&&tnt`is een gereserveerde gebeurtenissleutel in de mobiele SDK. De post-classificatie van de `tntVal` variabele [!DNL Analytics] werkt in de mobiele SDK op dezelfde manier als op het web (JavaScript). Nadat de informatie binnen wordt verwerkt, zou u activiteit en ervaringsnamen in de [!DNL Analytics][!DNL Analytics] interface moeten zien.

