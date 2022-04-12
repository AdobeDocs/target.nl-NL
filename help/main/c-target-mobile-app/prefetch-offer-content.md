---
keywords: aanbieding;prefetch;iOS;android;sdk;mobile;mobile sdk
description: De Adobe gebruiken [!DNL Target] Prefetch-functie in de SDK's van iOS en Android Mobile om inhoud van aanbiedingen zo weinig mogelijk op te halen door de serverreacties in cache te plaatsen.
title: Kan ik inhoud voor mobiele apps vooraf aanbieden?
feature: Implement Mobile
role: Developer
exl-id: 83a96a41-cf27-4ed8-8169-277f3ef3f249
source-git-commit: e152d3d68eede9c7606e546e30bd3e65bb8bcb9a
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Prefetaanbiedingsinhoud

De [!DNL Target] De prefetch-functie gebruikt de SDK&#39;s van iOS en Android Mobile om inhoud van de aanbieding zo weinig mogelijk op te halen door de serverreacties in cache te plaatsen.

Dit proces verkort de ladingstijd, verhindert veelvoudige netwerkvraag, en staat toe [!DNL Target] om op de hoogte te worden gebracht van de mbox die door de gebruiker van de mobiele app is bezocht. Alle inhoud wordt teruggewonnen en in het voorgeheugen ondergebracht tijdens de prefetch vraag, en deze inhoud wordt teruggewonnen van het geheime voorgeheugen voor alle toekomstige vraag die caching inhoud voor de gespecificeerde mbox naam bevat.

Houd rekening met de volgende beperkingen wanneer u de prefetch-methode gebruikt met de iOS en Android Mobile SDK&#39;s:

* Prefetch-inhoud blijft niet behouden bij alle opstarters. De prefetch-inhoud wordt in de cache geplaatst zolang de toepassing actief is of totdat de `clearPrefetchCache()` wordt aangeroepen.

Voor meer informatie, met inbegrip van prefetch methodes, openbare klassen, en codesteekproeven, zie:

* **iOS:**  [Inhoud van voorkeursaanbieding in iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/target-ios/c-mob-target-prefetch-ios.html) in de *Help bij Mobile Services iOS SDK*.
* **Android:**  [Inhoud van Prefetch-aanbieding in Android](https://experienceleague.adobe.com/docs/mobile-services/android/target-android/c-mob-target-prefetch-android.html) in de *Help bij Mobile Services Android SDK*.
