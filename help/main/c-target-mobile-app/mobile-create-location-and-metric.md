---
keywords: mobiele app;mobiele toepassingslocatie;doel mobiele app;mobiele doellocaties;mobiele app, succesgegevens
description: Voorbeeldcode weergeven voor meer informatie over het maken van locaties en succeswaarden in iOS-toepassingen, zodat u Adobe kunt gebruiken [!DNL Target] om uw app aan te passen en te optimaliseren.
title: Hoe maak ik [!DNL Target] Locaties en gegevens over succes in een iOS-app?
feature: Implement Mobile
role: Developer
exl-id: c2f05478-b019-47a7-b1a5-3783929e6732
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# iOS - maak een [!DNL Target] plaats en succes metrisch

Als u Doel wilt gebruiken in uw mobiele app, maakt u een locatie en een succesmaatstaf.

Deze sectie bevat voorbeeldcode die als sjabloon voor uw app kan worden gebruikt. De voorbeelden in deze sectie bevatten code voor iOS. Dezelfde patronen gelden voor Android. Specifieke Android-syntaxis vindt u in het gedeelte [Android SDK 4.x voor Experience Cloud-oplossingen](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/target-main.html) hulplijn.

>[!NOTE]
>
>Zie de [Mobiele documentatie](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-target-methods.html) voor een lijst van alle beschikbare methodes van het Doel.

Er zijn twee primaire methoden om een doellocatie in uw app te maken en een aanvraag in te dienen:

* `targetCreateRequestWithName`
* `targetLoadRequest`

1. Maak een doellocatie.

   Hier is een steekproefvraag om een verzoek tot stand te brengen:

   ```
   // make your request 
   ADBTargetLocationRequest *myRequest = [ADBMobile targetCreateRequestWithName:@"heroBanner" 
                                                    defaultContent:@"default.png" 
                                                    parameters:nil];
   ```

   | Parameter | Beschrijving |
   |---|---|
   | `ADBTargetLocationRequest *myRequest` | Vervangen `myRequest` met de naam van uw `targetLocation` in de app. |
   | `targetCreateRequestWithName:@"heroBanner"` | Vervangen `heroBanner` met de naam van uw `targetLocation` in Doel. Dit is het zelfde als de mbox naam. Deze hoofdbanner wordt weergegeven in de interface Doel. |
   | `defaultContent:@"default.png"` | Vervangen `default.png` met de waarde die de app gebruikt als Target niet reageert. |
   | `parameters:nil` | Geef de profiel- of mbox-parameters op. Zie meer informatie in de sectie &#39;Aangepaste gegevens doorgeven&#39;. |

   Hier is een steekproefvraag om het verzoek te laden:

   ```
   // load your request 
   [ADBMobile targetLoadRequest:myRequest callback:^(NSString *content) { 
                                        // do something with content 
                                        heroImage.image = [UIImage imageNamed:content]; 
   }];
   ```

   | Parameter | Beschrijving |
   |---|---|
   | `targetLoadRequest:myRequest` | Vervangen `myRequest` met de naam van uw `targetLocation` in de app. |
   | `NSString *content` | Inhoud vervangen door de inhoud die daadwerkelijk terugkomt van Adobe. De tekenreeks kan XML, JSON of een onbewerkte tekenreeks zijn. Gebruik dit gedeelte van de code om variabelen te definiëren, afbeeldingspaden in te stellen, controllerstromen, transactiepunten of andere elementen weer te geven die u wilt gebruiken. Doel retourneert de inhoud die in de gebruikersinterface is ingevoerd in exact dezelfde indeling. |
   | `heroImage.image = [UIImage imageNamed:content];` | Bijvoorbeeld: Neem inhoud en stel het pad in voor een hoofdafbeelding. |

1. Maak een succesmetrische methode.

   De methode `targetCreateOrderConfirmRequestWithName` kan worden gebruikt om een metrische waarde voor conversie/succes in uw app bij te houden.

   ```
   ADBTargetLocationRequest *req = [ADBMobile targetCreateOrderConfirmRequestWithName: "orderConfirm" 
                                              orderId: orderId 
                                              orderTotal: @"39.95" 
                                              productPurchasedId: _galleryItem.title 
                                              parameters: nil]; 
   [ADBMobile targetLoadRequest: req callback: nil];
   ```

   | Parameter | Beschrijving |
   |---|---|
   | `orderId` | Vervangen door een dynamische variabele die een unieke orde-id vertegenwoordigt. |
   | `@"39.95"` | Vervangen door een dynamische variabele die een uniek ordertotaal vertegenwoordigt. |
   | `_galleryItem.title` | Vervangen door een dynamische variabele die een door komma&#39;s gescheiden lijst van gekochte producten vertegenwoordigt. |
   | `parameters: nil` | Optioneel woordenboek van aanvullende parameters. |

1. Maak de app.

   Het Resultaat van de stap nadat u met succes een doelplaats en geëtiketteerd metrisch hebt gecreeerd, creeert een test A/B. De activiteit kan worden gemaakt met behulp van de op formulieren gebaseerde ervaringscomposer.