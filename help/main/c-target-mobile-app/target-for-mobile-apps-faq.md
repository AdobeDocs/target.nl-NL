---
keywords: mobiele app;veelgestelde vragen;faq;mobiele app voor doel
description: Veelgestelde vragen en hun antwoorden op Adobe weergeven [!DNL Target] voor mobiele apps.
title: Veelgestelde vragen over [!DNL Target] voor mobiele apps?
feature: Implement Mobile
role: Developer
exl-id: 1ddd8345-e753-4608-9293-939e092cb16d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Veelgestelde vragen over het doel voor mobiele apps

Lijst met veelgestelde vragen over [!DNL Target] voor mobiele apps.

## Moet ik tags gebruiken in [!DNL Adobe Experience Platform] om SDK op te stellen, of kan ik SDK zonder gebruiken opstellen [!DNL Launch]?

De SDK is beschikbaar op de [Adobe Marketing Cloud git](https://github.com/Adobe-Marketing-Cloud/acp-sdks/). Als u het niet gebruikt [tags in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html), moet u uw eigen instellingenbestand beheren en dit beheren in uw app.

## Welke SDK&#39;s zijn momenteel beschikbaar?

The Adobe Experience Platform Mobile SDKs currently support iOS, Android, and React. For more information, see the [Adobe Experience Cloud Platform Mobile SDKs guide](https://aep-sdks.gitbook.io/docs/).

## Wat is de frequentie van de locatiegebaseerde functie, in termen van controle over de breedte en lengte?

Zie de [Documentatie voor Adobe-plaatsen](https://placesdocs.com/places-services-by-adobe-documentation/) voor meer informatie .

## Do I need at.js for the Adobe Experience Platform Mobile SDKs to work?

No, you don’t need at.js to use the mobile SDKs. at.js is de [!DNL Target] JavaScript-bibliotheek voor websites. De Adobe Experience Platform Mobile-SDK&#39;s zijn bedoeld voor mobiele apps.

## Is [!DNL Target] Mobiele Adobe [!DNL Target] Alleen SKU voor premiumproduct?

Nee. Voor [!DNL Adobe Target Standard] klanten, kunt u onze Mobiele SDKs voor A/B Test en Ervaring gerichte (XT) activiteiten slechts met de [!DNL Target Standard] Mobile App-invoegtoepassing. Als u Recommendations- of AI-functies wilt gebruiken in de mobiele app, hebt u een [Adobe Target Premium](/help/main/c-intro/intro.md#premium) licentie.

## Is there a mobile app integration between Adobe Experience Manager (AEM) and [!DNL Target] mobile activities?

It is on our roadmap but there is no timeline yet. Currently, you can share JSON [Experience Fragments](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) from AEM to Target and there might be potential to then use them in a mobile app activity.
