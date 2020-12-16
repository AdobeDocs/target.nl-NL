---
keywords: offer;prefetch;iOS;android;sdk;mobile;mobile sdk
description: De Adobe Target-prefetch-functie gebruikt de iOS- en Android Mobile-SDK's om inhoud van de aanbieding zo weinig mogelijk op te halen door de serverreacties in cache te plaatsen.
title: Prefetaanbiedingsinhoud
feature: mobile implementation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# Inhoud van voorkeursaanbieding{#prefetch-offer-content}

De prefetch [!DNL Target] gebruikt de iOS- en Android Mobile-SDK&#39;s om inhoud van de aanbieding zo weinig mogelijk op te halen door de serverreacties in cache te plaatsen.

Dit proces verkort de laadtijd, verhindert veelvoudige netwerkvraag, en staat [!DNL Target] toe om op de hoogte te worden gebracht die mbox door de mobiele toepassingsgebruiker werd bezocht. Alle inhoud wordt teruggewonnen en in het voorgeheugen ondergebracht tijdens de prefetch vraag, en deze inhoud wordt teruggewonnen van het geheime voorgeheugen voor alle toekomstige vraag die caching inhoud voor de gespecificeerde mbox naam bevat.

Houd rekening met de volgende beperkingen wanneer u de prefetch-methode gebruikt met de iOS- en Android Mobile-SDK&#39;s:

* Prefetch-inhoud blijft niet behouden bij alle opstarters. De prefetch-inhoud wordt in de cache geplaatst zolang de toepassing leeft of totdat de methode `clearPrefetchCache()` wordt aangeroepen.
* Prefetch-functionaliteit wordt niet ondersteund voor verkeerstoewijzingsmethoden [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target], voor activiteitstypen [!UICONTROL Automated Personalization] of [!UICONTROL Recommendations] of voor [aanbevelingen binnen een A/B- of XT-activiteit](/help/c-recommendations/recommendations-as-an-offer.md).

Voor meer informatie, met inbegrip van prefetch methodes, openbare klassen, en codesteekproeven, zie:

* **iOS:**  [Prefetch biedt inhoud aan in ](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) iOS in de Help bij  *Mobile Services iOS SDK*.
* **Android:**  [Prefetch biedt inhoud aan in ](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) Android in de Help bij  *Mobile Services Android SDK*.
