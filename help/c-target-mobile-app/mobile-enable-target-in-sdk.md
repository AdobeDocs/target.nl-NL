---
keywords: mobiele app;mobiele app sdk;doel mobiele app;mobiele doel sdk;mobiele app sdk;doel inschakelen in sdk
description: Leer hoe u de Adobe Mobile Services SDK toevoegt aan uw mobiele app.
title: Hoe laat ik Doel in de Adobe Mobile SDK toe?
feature: Implement Mobile
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Doel inschakelen in de SDK{#enable-target-in-the-sdk}

Voeg de SDK van Adobe Mobile Services toe aan uw app.

1. Als u de SDK van Adobe Mobile Services niet hebt geïnstalleerd in uw app, gebruikt u uw Analytics- of Experience Cloud-gegevens en downloadt u de SDK van de [Adobe Mobile Services](https://mobilemarketing.adobe.com)-website.

1. Voeg de SDK van Adobe Mobile Services toe aan uw app.

   U vindt de instructies onder [Core Implementation en Lifecycle](https://experienceleague.adobe.com/docs/mobile-services/ios/getting-started-ios/dev-qs.html).

1. Voeg cliëntcode toe, onderbreking en laat SSL toe.

   Open Mobiele services in de Experience Cloud en ga vervolgens naar **[!UICONTROL Manage App Settings]** > **[!UICONTROL SDK Target Options]**.

   Voeg uw clientcode van het Doel en onderbreking toe. De clientcode is uniek voor uw account of bedrijf. De onderbreking is de tijd in aantal seconden tot welk Doel op een reactie zal wachten alvorens de standaardinhoud te tonen. Controleer of de optie **[!UICONTROL Use HTTPS]** is ingeschakeld op de pagina Toepassingsinstellingen beheren in Adobe Mobile Services. Als HTTPS niet wordt toegelaten, zullen alle vraag in iOS9+ worden geblokkeerd tenzij u de server van het Doel toe_voegt op lijst van gewenste personen.

   ![](assets/mobile-clientcode.png)

1. Nadat u de app hebt gemaakt of gevonden, zoekt u de app-instellingen en downloadt u de gewenste SDK.

   ![](assets/download-sdk.png)

>[!IMPORTANT]
>
> Als u geen toegang hebt tot de mobiele marketinginterface, kunt u wijzigingen rechtstreeks doorvoeren in het configuratiebestand in uw toepassingscode. deze pagina is echter niet synchroon met de instellingenpagina in de gebruikersinterface.

