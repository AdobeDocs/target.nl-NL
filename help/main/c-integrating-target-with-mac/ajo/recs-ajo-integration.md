---
keywords: ajo;adobe road optimizer;adobe trip optimizer target integration;aanbevelingen;target recommendations;integration
description: Gebruiken [!DNL Adobe Target Recommendations] with [!DNL Adobe Journey Optimizer].
title: Hoe wordt ik gebruikt [!DNL Target Recommendations] bij reizen van klanten met [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn bètafuncties in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: bb6c83ff393656a634e1e8ddcb02b14dc8d4c8d2
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# [!DNL Adobe Target Recommendations] en [!DNL Adobe Journey Optimizer] integratie

In dit artikel worden gebruiksgevallen en informatie uitgelegd die u helpen bij het instellen van de integratie tussen [!DNL Adobe Target Recommendation] en [!DNL Adobe Journey Optimizer] om u te helpen verbonden, contextafhankelijke en gepersonaliseerde ervaringen aan uw klanten te leveren.

## Vereisten

Als u de opdracht [!DNL Target Recommendations] en [!DNL Adobe Journey Optimizer] voor integratie hebt u het volgende nodig:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) geïmplementeerd met behulp van de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

  De functie is niet beschikbaar bij een [!DNL Target Standard] vergunning of bij de tenuitvoerlegging [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Gebruiksscenario&#39;s

Het volgende is slechts twee mogelijke gebruiksgevallen voor integratie [!DNL Target Recommendations] with [!DNL Adobe Journey Optimizer]:

* **[!DNL Customer Journey Optimizer]een persoonlijke e-mail verzenden na het verlaten van het winkelwagentje**: Dit gebruiksgeval is gebaseerd op een klant die een website bezoekt, artikelen in het winkelwagentje plaatst en de site vervolgens verlaat zonder het aankoopproces te voltooien.

  Stel bijvoorbeeld dat een bezoeker de website van een kledingbedrijf bezoekt en twee winterjassen en een sweatshirt in het winkelwagentje plaatst. De bezoeker wordt dan afgeleid en verlaat de website of is niet zeker van de aankopen en sluit de browser of app.

  Na een bepaalde periode, misschien een paar uur of een dag, een aangepaste handeling in [!DNL Adobe Journey Optimizer] roept om [!DNL Target Recommendations] om de inhoud van het verlaten winkelwagentje te bepalen. [!DNL Adobe Journey Optimizer] verstuurt deze bezoeker vervolgens een persoonlijke e-mail als herinnering dat het aankoopproces niet is voltooid, samen met afbeeldingen en koppelingen naar de verlaten items.

* **[!DNL Customer Journey Optimizer]verzendt een e-mail na het sitebezoek met behulp van het gebruikersprofiel**: Dit gebruiksgeval is gebaseerd op een klant die een website bezoekt, verschillende items weergeeft en vervolgens de site verlaat zonder items in het winkelwagentje te plaatsen.

  Na een bepaalde tijdsperiode kunt u een aangepaste handeling uitvoeren in [!DNL Adobe Journey Optimizer] roept om [!DNL Target Recommendations] om te bepalen welke items deze bezoeker heeft weergegeven met de [!DNL Adobe Experience Cloud Identifier] (EDID). [!DNL Adobe Journey Optimizer] verstuurt deze bezoeker vervolgens een persoonlijke e-mail als herinnering dat het aankoopproces niet is voltooid, samen met afbeeldingen en koppelingen naar de verlaten items.

