---
keywords: ajo;adobe road optimizer;adobe trip optimizer target integration;aanbevelingen;target recommendations;integration
description: Integreren [!DNL Adobe Target Recommendations] with [!DNL Adobe Journey Optimizer].
title: Hoe wordt ik gebruikt [!DNL Target Recommendations] bij reizen van klanten met [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn bètafuncties in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: d93e58540568fb685bd18ee5e39ad2917323bce4
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Integreren [!DNL Adobe Target Recommendations] en [!DNL Adobe Journey Optimizer]

In dit artikel worden gebruiksgevallen en informatie uitgelegd die u helpen bij het instellen van de integratie tussen [!DNL Adobe Target Recommendations] en [!DNL Adobe Journey Optimizer] om u te helpen verbonden, contextafhankelijke en gepersonaliseerde ervaringen aan uw klanten te leveren.

Dankzij deze integratie kunt u meer conversies aansturen en de impact van e-mailberichten met gepersonaliseerde aanbevelingen bekijken.

## Vereisten

Als u de opdracht [!DNL Target Recommendations] en [!DNL Adobe Journey Optimizer] voor integratie hebt u het volgende nodig:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) geïmplementeerd met behulp van de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}.

  Deze functie is niet beschikbaar bij een [!DNL Target Standard] vergunning of bij de tenuitvoerlegging [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* [[!DNL Adobe Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/ajo-home.html){target=_blank}.

## Gebruiksscenario&#39;s

Dit zijn slechts een paar mogelijke toepassingen voor integratie [!DNL Target Recommendations] with [!DNL Adobe Journey Optimizer]:

* **[!DNL Adobe Journey Optimizer]een persoonlijke e-mail verzenden na het verlaten van het winkelwagentje**: Dit gebruiksgeval is gebaseerd op een klant die een website bezoekt, artikelen in het winkelwagentje plaatst en de site vervolgens verlaat zonder het aankoopproces te voltooien.

  Stel bijvoorbeeld dat een bezoeker de website van een kledingbedrijf bezoekt en twee winterjassen en een sweatshirt in het winkelwagentje plaatst. De bezoeker wordt dan afgeleid en verlaat de website of is niet zeker van de aankopen en sluit de browser of app.

  Na een bepaalde periode, misschien een paar uur of een dag, een aangepaste handeling in [!DNL Adobe Journey Optimizer] roept om [!DNL Target Recommendations] om de inhoud van het verlaten winkelwagentje te bepalen gebruikend een [aanbevelingen op basis van karretjes](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algoritme. [!DNL Adobe Journey Optimizer] verstuurt deze bezoeker vervolgens een persoonlijke e-mail als herinnering dat het aankoopproces niet is voltooid, samen met afbeeldingen en koppelingen naar de verlaten items.

* **[!DNL Adobe Journey Optimizer]stuurt een grote e-mail na bezoeken ter plaatse om bezoekers eraan te herinneren welke items zijn weergegeven**: Met dit gebruiksgeval kunnen bezoekers een website bezoeken, verschillende items weergeven en de site of app verlaten zonder items in het winkelwagentje te plaatsen.

  Na een opgegeven punt wordt een aangepaste handeling uitgevoerd in [!DNL Adobe Journey Optimizer] roept om [!DNL Target Recommendations] om te bepalen welke items elke bezoeker heeft weergegeven, met gebruik van de [!DNL Adobe Experience Cloud Identifier] (EDID), [!DNL Target] en een [op gebruiker gebaseerd](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algoritme. [!DNL Adobe Journey Optimizer] stuurt elk lid van het gekwalificeerde publiek vervolgens een persoonlijke e-mail met afbeeldingen en koppelingen naar de weergegeven items van elke bezoeker om de bezoeker te laten terugkeren en een aankoop te doen.

  In dit scenario wordt [!UICONTROL Experience Cloud Visitor ID] (ECID) en de inhoud van de [!DNL Target] wordt gebruikt om de aanbeveling te produceren die op het onlangs bekeken algoritme wordt gebaseerd.

  Stel dat een bezoeker bijvoorbeeld een website in de detailhandel bezoekt en verschillende stalen bekijkt. Deze bezoeker [!DNL Target] wordt bijgewerkt met een lijst met de weergegeven stalen. De ECID en de [!DNL Target] profiel, [!DNL Target] zendt de aanbeveling aan [!DNL Adobe Journey Optimizer]. [!DNL Adobe Journey Optimizer] verzendt vervolgens een e-mail met afbeeldingen en koppelingen naar de stalen die deze bezoeker heeft bekeken met het onlangs weergegeven algoritme. Een andere bezoeker ontvangt een persoonlijke e-mail met afbeeldingen en koppelingen naar de items die deze bezoeker heeft weergegeven. Elk e-mailbericht is gepersonaliseerd.

* **[!DNL Adobe Journey Optimizer]stuurt een grote hoeveelheid e-mail naar gekwalificeerde bezoekers na een bezoek om populaire objecten voor te stellen**: Deze kwestie van gebruik is gebaseerd op een bezoeker die een website bezoekt, maar geen bepaalde punten bekijkt. Het e-mailbericht wordt bulksgewijs verzonden naar iedereen die in aanmerking komt voor een bepaald publiek, bijvoorbeeld:

  Stel dat de bezoeker geen bepaalde stalen ziet. Misschien heeft de bezoeker gewoon rond de site geklikt en rubriekpagina&#39;s of blogberichten weergegeven. Dientengevolge, [!DNL Target] profiel bevat geen specifieke informatie over onlangs weergegeven items. In deze situatie [!DNL Target Recommendations] kan [aanbeveling voor back-up](/help/main/c-recommendations/c-algorithms/backup-recs.md) zodat [!DNL Adobe Journey Optimizer] U kunt een e-mail met afbeeldingen en koppelingen naar populaire items op de website verzenden om de bezoeker te laten terugkeren en eventueel een aankoop te doen.


