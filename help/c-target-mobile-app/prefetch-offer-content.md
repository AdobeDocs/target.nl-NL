---
keywords: offer;prefetch;iOS;android;sdk;mobile;mobile sdk
description: De Adobe Target-prefetch-functie gebruikt de iOS- en Android Mobile-SDK's om inhoud van de aanbieding zo weinig mogelijk op te halen door de serverreacties in cache te plaatsen.
title: Prefetaanbiedingsinhoud
feature: null
topic: Advanced,Standard,Classic
uuid: 715e0e77-bfd9-437b-b42c-899d66f2890c
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Prefetaanbiedingsinhoud{#prefetch-offer-content}

De [!DNL Target] prefetch-functie gebruikt de iOS- en Android Mobile-SDK&#39;s om inhoud van de aanbieding zo weinig mogelijk op te halen door de serverreacties in cache te plaatsen.

Dit proces verkort de laadtijd, verhindert veelvoudige netwerkvraag, en staat toe om op de hoogte [!DNL Target] te worden gebracht die mbox door de mobiele toepassingsgebruiker werd bezocht. Alle inhoud wordt teruggewonnen en in het voorgeheugen ondergebracht tijdens de prefetch vraag, en deze inhoud wordt teruggewonnen van het geheime voorgeheugen voor alle toekomstige vraag die caching inhoud voor de gespecificeerde mbox naam bevat.

Houd rekening met de volgende beperkingen wanneer u de prefetch-methode gebruikt met de iOS- en Android Mobile-SDK&#39;s:

* Prefetch-inhoud blijft niet behouden bij alle opstarters. De inhoud van de prefetch wordt in de cache geplaatst zolang de toepassing leeft of totdat de `clearPrefetchCache()` methode wordt aangeroepen.
* De functionaliteit van de prefetch wordt niet gesteund voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] verkeerstoewijzingsmethodes, voor [!UICONTROL Automated Personalization] of [!UICONTROL Recommendations] activiteitstypes, of voor [aanbevelingen biedt binnen A/B of XT activiteit](/help/c-recommendations/recommendations-as-an-offer.md)aan.

Voor meer informatie, met inbegrip van prefetch methodes, openbare klassen, en codesteekproeven, zie:

* **iOS:**  [Prefetch biedt inhoud aan in iOS](https://docs.adobe.com/content/help/en/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) in de Help bij *de iOS SDK van* Mobile Services.
* **Android:**  [Prefetch biedt inhoud aan in Android](https://docs.adobe.com/content/help/en/mobile-services/android/target-android/c-mob-target-prefetch-android.html) in de Help bij *de Android-SDK van* Mobile Services.
