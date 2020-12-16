---
keywords: Implementation;mbox.js non javascript;mbox;adbox
description: Gebruik een AdBox om afbeeldingen te leveren in een externe implementatie, met Adobe Target.
title: Een ADBox maken voor een afbeelding met Adobe Target
feature: email implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Adbox voor een afbeelding maken{#create-an-adbox-for-an-image}

Gebruik een AdBox om afbeeldingen te leveren in een externe implementatie met Adobe Target.

Een AdBox is vergelijkbaar met een box, maar wordt beheerd door een URL in plaats van JavaScript. AdBox wordt gemaakt met een speciale URL voor een advertentievak die een advertentievak (of advertentievak) in uw Adobe-account laadt. Gebruik deze AdBox in plaats van de box in uw activiteiten. Gebruik de URL van het AdBox in plaats van een verwijzing naar een directe afbeelding in e-mail of andere niet-JavaScript-implementaties.

Zie [Niet-JavaScript-gebaseerde implementaties](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) voor hulp bij het selecteren van de juiste setup.

1. Maak de URL van het advertentievak:

   ```
   https://myClientCode.tt.omtrdc.net/m2/myClientCode/ubox/
   image?mbox=emailHeroImage123_320x200&
   mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif
   ```

   * Waar `myClientCode` de cliëntcode van uw bedrijf is. De clientcode van uw bedrijf is helemaal in kleine letters en heeft geen speciale tekens.

      Uw clientcode is beschikbaar boven aan de pagina [!UICONTROL Administation > Implementation] van de interface [!DNL Target].

   * Waar `image` het vraagtype is. In dit geval is het een afbeelding.

   * Hierbij is `emailHeroImage123_320x200` de naam van de advertentievak.

   * Hierbij is `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fimg%2Flogo%2Egif` de standaardinhoud van de box. Dit moet een afbeelding zijn.

      Dit moet URL gecodeerd zijn en moet een absolute verwijzing zijn. Met de [HTML URL-coderingsreferentie](https://www.w3schools.com/tags/ref_urlencode.asp) kunt u snel URL&#39;s coderen.

1. Maak [Aanbiedingen omleiden](/help/c-experiences/c-manage-content/offer-redirect.md#task_33C80CD722564303B687948261484F94) voor elke alternatieve afbeelding.

   >[!NOTE]
   >
   >AdBox moet met een omleidingsvoorstel worden geladen of de standaardinhoudsaanbieding. Andere aanbiedingstypen werken niet. Omdat AdBox een URL is, kan het slechts URLs tonen het ontvangt, zodat werkt slechts de OmleidingsAanbieding.

1. Maak de activiteit.

   Zie [Niet-JavaScript-Gebaseerde Implementaties](/help/c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) voor de juiste opstelling om uw doelstellingen te ontmoeten.
1. Volledige kwaliteitscontrole op de activiteit.

   Als beste praktijken, creeer een dummypagina en verifieer dat alle ervaringen, standaardinhoud, en rapporten zoals verwacht op alle browser types, voor al uw milieu&#39;s handelen.

1. Start de activiteit.
