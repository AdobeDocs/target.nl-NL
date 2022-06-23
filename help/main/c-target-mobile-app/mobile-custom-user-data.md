---
keywords: mobiele app;mobiele app verzendt gegevens;doel mobiele app;mobiele aangepaste gebruikersgegevens;mobiele app, aangepaste gegevens
description: Leer hoe u aanvullende informatie over de locatie of de gebruiker naar Adobe kunt sturen [!DNL Target] als naam-waardeparen om u te helpen douanepubliek bouwen.
title: Hoe kan ik aangepaste gebruikersgegevens verzenden in een iOS-app?
feature: Implement Mobile
role: Developer
exl-id: c64219ec-8d60-4d05-b2b8-103e8ffcaefc
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# iOS - aangepaste gebruikersgegevens verzenden

U kunt aanvullende informatie over de locatie of de gebruiker als naam-waardeparen naar Target sturen.

Deze informatie kan worden gebruikt om aangepaste soorten publiek (bijvoorbeeld gebruikers met een lengte van meer dan 25000 mijl) en rapportage te maken.

Er zijn twee soorten parameters die u met een vraag van het Doel kunt verzenden:

* mbox-parameters

   Mbox-parameters zijn niet blijvend in sessies.
* Profielparameters

   Profielparameters worden opgeslagen in de opslag van het bezoekersprofiel en zijn tijdens verschillende sessies blijvend. Mbox-parameters blijven niet bestaan. Terwijl sommige toetsen zijn gereserveerd, kunnen zowel profiel- als mbox-parameters aangepaste sleutel-waardeparen zijn.

Hoewel er enkele gereserveerde toetsen zijn, kunnen zowel profiel- als mapoparameters aangepaste sleutel-waardeparen bevatten.

1. Woordenboek maken.

   Maak eerst een woordenboek met de waarden die u naar Doel verzendt. Voor het gemak kunt u dit toevoegen in het `welcomeMessageCampaign` methode zodat moet u zich niet over werkingsgebied ongerust maken.

   Hier volgt een voorbeeldwoordenboek. U kunt deze plakken in `(void)welcomeMessageCampaign`. De waarden voor toetsen als `userLevel` en `userMiles` zijn hard-gecodeerd in dit voorbeeld. Over het algemeen geeft u de bijbehorende variabelen door.

   ```
   NSDictionary *targetParams = [[NSDictionary alloc] initWithObjectsAndKeys: 
                                 @"platinum",@"userLevel", 
                                 @26500,@"userMiles", 
                                 @"1067007",@"entity.id", 
                                 @"dealsapp.qa", @"host", 
                                 @"fashion",@"entity.categoryId", 
                                 @"millenial", @"profile.persona", 
                                 @"cohort_5", @"profile.cohort", 
                                 nil];
   ```

   * Toetsen met het voorvoegselprofiel (bijvoorbeeld `profile.persona`) worden opgeslagen in het gebruikersprofiel.

      Deze profielkenmerken kunnen op verschillende activiteiten en kanalen worden gebruikt.

   * Toetsen die geen voorvoegsel hebben (bijvoorbeeld `userMiles`) zijn mbox-parameters.

      Deze parameters zijn alleen beschikbaar tijdens de sessie.

   * Toetsen met het voorvoegsel (bijvoorbeeld `entity.category.id`) worden gebruikt voor productaanbevelingen.

1. Controleer de gegevens.
   1. In toepassing `didFinishLaunchingWithOptions`, verwijderen of toevoegen `[ADBMobile setDebugLogging:YES];`.

      Hiermee worden gedetailleerde foutopsporingslogbestanden afgedrukt.
   1. Maak de app.
   1. Verifieer dat de parameters in de doelvraag worden overgegaan.

      Zoek naar uw naam van de doelplaats in uw zuivert console. U zult een vraag zien aan `YOUR-CLIENT-CODE.tt.omtrdc.net`met alle parameters die u net hebt doorgegeven.

      ![](assets/mobile-debug.png)
   U kunt een publiek maken en de weergave van inhoud beperken of als doel instellen met deze parameters in de doelstandaard.
