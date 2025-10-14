---
keywords: ajo;adobe road optimizer;adobe trip optimizer target integration;aanbevelingen;target recommendations;integration
description: Integreer  [!DNL Adobe Target Recommendations]  met  [!DNL Adobe Journey Optimizer].
title: Hoe gebruik ik  [!DNL Target Recommendations]  in klantenreizen gebruikend  [!DNL Adobe Journey Optimizer]?
feature: Integrations
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#beta newtab=true" tooltip="Wat zijn de eigenschappen van Beta in  [!DNL Adobe Target]."
hide: true
hidefromtoc: true
exl-id: 81bbbd51-47fc-4e23-a1cb-7c18fea1c159
source-git-commit: b4f9e14f9dfa94f8648686e43e66eee7e0f7daa1
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Integeren [!DNL Adobe Target Recommendations] en [!DNL Adobe Journey Optimizer]

Dit artikel biedt gebruiksscenario&#39;s en richtlijnen voor de integratie van [!DNL Adobe Target Recommendations] met [!DNL Adobe Journey Optimizer] , zodat u verbonden, contextafhankelijke en persoonlijke ervaringen van klanten kunt bieden.

Dankzij deze integratie kunt u meer conversies aansturen en de impact van e-mailberichten met gepersonaliseerde aanbevelingen bekijken.

## Vereisten

Als u de integratie [!DNL Target Recommendations] en [!DNL Adobe Journey Optimizer] wilt gebruiken, hebt u het volgende nodig:

* [[!DNL Adobe Target Premium]](/help/main/c-intro/intro.md#premium) uitgevoerd gebruikend het [&#x200B; Web SDK van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}.

  Deze functie is niet beschikbaar met een [!DNL Target Standard] -licentie of bij de implementatie van [!DNL Target] met at.js of andere [!DNL Target] SDK&#39;s.

* [[!DNL Adobe Journey Optimizer] &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/ajo-home){target=_blank}.

## Gebruiksscenario&#39;s

Deze gebruiksgevallen zijn slechts een paar mogelijke gebruiksgevallen voor het integreren van [!DNL Target Recommendations] met [!DNL Adobe Journey Optimizer] :

* **[!DNL Adobe Journey Optimizer]verzendt een gepersonaliseerde e-mail na het verlaten van het winkelwagentje**: Dit gebruiksgeval is gebaseerd op een klant die een website bezoekt, die punten in het winkelwagentje plaatst, en dan de plaats verlaat zonder het aankoopproces te voltooien.

  Stel bijvoorbeeld dat een bezoeker de website van een kledingbedrijf bezoekt en twee winterjassen en een sweatshirt in het winkelwagentje plaatst. De bezoeker wordt dan afgeleid en verlaat de website of is niet zeker van de aankopen en sluit de browser of app.

  Na een gespecificeerde periode, misschien een paar uren of een dag, maakt een douaneactie in [!DNL Journey Optimizer] een vraag aan [!DNL Target Recommendations] om de inhoud van de verlaten het winkelwagentje te bepalen gebruikend a [&#x200B; op kar-gebaseerde aanbevelingen &#x200B;](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) algoritme. [!DNL Journey Optimizer] stuurt deze bezoeker vervolgens een gepersonaliseerde e-mail als herinnering dat het aankoopproces niet is voltooid, samen met afbeeldingen en koppelingen naar de verlaten items.

* **[!DNL Adobe Journey Optimizer]verzendt een grote e-mail na sitebezoeken om bezoekers eraan te herinneren welke items zijn weergegeven** : Deze kwestie is gebaseerd op bezoekers die een website bezoeken, verschillende items bekijken en vervolgens de site of de app verlaten zonder items in het winkelwagentje te plaatsen.

  Na een gespecificeerde periode, maakt een douaneactie in [!DNL Journey Optimizer] een vraag aan [!DNL Target Recommendations] om te bepalen welke punten elke bezoeker bekeken, gebruikend de 2&rbrace; van elke bezoeker (EDID), het profiel van de bezoeker [!DNL Adobe Experience Cloud Identifier], en a [!DNL Target] gebruiker-gebaseerd [&#x200B; algoritme. &#x200B;](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md) [!DNL Adobe Journey Optimizer] stuurt vervolgens een gepersonaliseerde e-mail naar elk lid van het gekwalificeerde publiek met afbeeldingen en koppelingen naar de weergegeven items van elke bezoeker om de bezoeker te laten terugkeren en een aankoop te doen.

  In dit scenario worden het profiel [!UICONTROL Experience Cloud Visitor ID] (ECID) en de inhoud van het profiel [!DNL Target] van elke bezoeker gebruikt om de aanbeveling te genereren op basis van het onlangs weergegeven algoritme.

  Stel dat een bezoeker bijvoorbeeld een website in de detailhandel bezoekt en verschillende stalen bekijkt. Het [!DNL Target] -profiel van deze bezoeker wordt bijgewerkt met een lijst van de weergegeven stalen. Met behulp van de ECID en het profiel [!DNL Target] van de bezoeker stuurt [!DNL Target] de aanbeveling naar [!DNL Journey Optimizer] . [!DNL Journey Optimizer] verzendt vervolgens via het onlangs weergegeven algoritme een e-mail met afbeeldingen en koppelingen naar de stalen die deze bezoeker heeft weergegeven. Een andere bezoeker ontvangt een persoonlijke e-mail met afbeeldingen en koppelingen naar de items die deze bezoeker heeft weergegeven. Elk e-mailbericht wordt gepersonaliseerd voor elke bezoeker.

* **[!DNL Adobe Journey Optimizer]stuurt na een bezoek aan de site een grote hoeveelheid e-mail naar gekwalificeerde bezoekers om veelgebruikte items voor te stellen.** : Deze kwestie is gebaseerd op een bezoeker die een website bezoekt, maar niet op bepaalde items. Het e-mailbericht wordt bulksgewijs verzonden naar alle bezoekers die voor een bepaald publiek in aanmerking komen, bijvoorbeeld:

  Stel dat de bezoeker geen bepaalde stalen ziet. Misschien heeft de bezoeker gewoon rond de site geklikt en rubriekpagina&#39;s of blogberichten weergegeven. Het resultaat is dat het profiel [!DNL Target] geen specifieke informatie bevat over onlangs weergegeven items. In deze situatie, [!DNL Target Recommendations] gebruikt a [&#x200B; reserveaanbeveling &#x200B;](/help/main/c-recommendations/c-algorithms/backup-recs.md) zodat [!DNL Journey Optimizer] een e-mail met beelden en verbindingen naar populaire punten op de website kan verzenden om de bezoeker te krijgen om terug te keren en misschien een aankoop te maken.
