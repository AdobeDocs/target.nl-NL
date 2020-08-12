---
keywords: mobile app;mobile app sdk;target mobile app;mobile target sdk;mobile app sdk;enable target in sdk
description: Voeg de SDK van Adobe Mobile Services toe aan uw app.
title: Doel inschakelen in de SDK
feature: null
topic: Target
uuid: 673dd5c7-9c09-4a6e-bc41-c6ad27cf269c
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Doel inschakelen in de SDK{#enable-target-in-the-sdk}

Voeg de SDK van Adobe Mobile Services toe aan uw app.

1. Als u de SDK van Adobe Mobile Services niet in uw app hebt geïnstalleerd, gebruikt u de Analytics- of Experience Cloud-gegevens en downloadt u de SDK van de website [Adobe Mobile Services](https://mobilemarketing.adobe.com) .

1. Voeg de SDK van Adobe Mobile Services toe aan uw app.

   U vindt de instructies onder [Core Implementation en Lifecycle](https://docs.adobe.com/content/help/en/mobile-services/ios/getting-started-ios/dev-qs.html).

1. Voeg cliëntcode toe, onderbreking en laat SSL toe.

   Open Mobiele services in de Experience Cloud en ga vervolgens naar **[!UICONTROL Manage App Settings]** > **[!UICONTROL SDK Target Options]**.

   Voeg uw clientcode van het Doel en onderbreking toe. De clientcode is uniek voor uw account of bedrijf. De onderbreking is de tijd in aantal seconden tot welk Doel op een reactie zal wachten alvorens de standaardinhoud te tonen. Controleer of de **[!UICONTROL Use HTTPS]** optie is ingeschakeld op de pagina Toepassingsinstellingen beheren in Adobe Mobile Services. Als HTTPS niet wordt toegelaten, zullen alle vraag in iOS9+ worden geblokkeerd tenzij u de server van het Doel toe_voegt op lijst van gewenste personen.

   ![](assets/mobile-clientcode.png)

1. Nadat u de app hebt gemaakt of gevonden, zoekt u de app-instellingen en downloadt u de gewenste SDK.

   ![](assets/download-sdk.png)

>[!IMPORTANT]
>
> Als u geen toegang hebt tot de mobiele marketinginterface, kunt u wijzigingen rechtstreeks doorvoeren in het configuratiebestand in uw toepassingscode. deze pagina is echter niet synchroon met de instellingenpagina in de gebruikersinterface.

