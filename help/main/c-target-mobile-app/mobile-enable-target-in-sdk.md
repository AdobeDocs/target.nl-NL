---
keywords: mobiele app;mobiele app sdk;doel mobiele app;mobiele doel sdk;mobiele app sdk;doel inschakelen in sdk
description: Leer hoe u de Adobe Mobile Services SDK toevoegt aan uw mobiele app.
title: Hoe kan ik inschakelen [!DNL Target] in de Adobe Mobile SDK?
feature: Implement Mobile
role: Developer
exl-id: c34bd50c-e17f-4dfb-8470-8f4c8639ee9f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Inschakelen [!DNL Target] in de SDK

Voeg de SDK van Adobe Mobile Services toe aan uw app.

1. Als u de SDK van Adobe Mobile Services niet hebt geïnstalleerd in uw app, gebruikt u uw Analytics- of Experience Cloud-gegevens en downloadt u de SDK via de [Adobe mobiele services](https://mobilemarketing.adobe.com/) website.

1. Voeg de SDK van Adobe Mobile Services toe aan uw app.

   U vindt de instructies onder [Core-implementatie en levenscyclus](https://experienceleague.adobe.com/docs/mobile-services/ios/getting-started-ios/dev-qs.html).

1. Voeg cliëntcode toe, onderbreking en laat SSL toe.

   Open Mobiele services in de Experience Cloud en ga vervolgens naar **[!UICONTROL Manage App Settings]** > **[!UICONTROL SDK Target Options]**.

   Voeg uw clientcode van het Doel en onderbreking toe. De clientcode is uniek voor uw account of bedrijf. De onderbreking is de tijd in aantal seconden tot welk Doel op een reactie zal wachten alvorens de standaardinhoud te tonen. Zorg ervoor dat de **[!UICONTROL Use HTTPS]** Deze optie is ingeschakeld op de pagina Toepassingsinstellingen beheren in Adobe Mobile Services. Als HTTPS niet wordt toegelaten, zullen alle vraag in iOS9+ worden geblokkeerd tenzij u de server van het Doel voegt op lijst van gewenste personen.

   ![](assets/mobile-clientcode.png)

1. Nadat u de app hebt gemaakt of gevonden, zoekt u de app-instellingen en downloadt u de gewenste SDK.

   ![](assets/download-sdk.png)

>[!IMPORTANT]
>
> Als u geen toegang hebt tot de mobiele marketinginterface, kunt u wijzigingen rechtstreeks doorvoeren in het configuratiebestand in uw toepassingscode. deze pagina is echter niet synchroon met de instellingenpagina in de gebruikersinterface.
