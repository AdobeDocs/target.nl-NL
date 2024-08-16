---
keywords: optimalisatie;personalisatie;adobe-reis optimizer;ajo;use cases;scenario's;content change/ab test;profile, kenmerk;image wijzigen;image wisselen
description: Ontgrendel de geheimen voor effectieve wijzigingen in A/B-testinhoud in Adobe Journey Optimizer
title: De inhoud verandert door het testen A/B in  [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn de eigenschappen van Beta in  [!DNL Adobe Target]."
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: 9a9447b3067311ef203e91b186fff506e60bf590
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# Inhoud verandert via A/B-tests in [!DNL Adobe Journey Optimizer]

Met dit gebruiksgeval kunt u de geheimen ontgrendelen zodat wijzigingen in de inhoud van A/B-tests in [!DNL Adobe Journey Optimizer] worden doorgevoerd.

Dit gebruiksgeval wordt ontworpen om aan te tonen hoe te om een vertrouwde taak in [!DNL Adobe Target] uit te voeren, A/B het testen gebruikend een [ activiteit van de Test A/B ](/help/main/c-activities/t-test-ab/test-ab.md), maar het gebruiken [!DNL Journey Optimizer].

## Scenario

Een leerbedrijf verhoogde omzettingen door diverse beelden te testen en campagne landende pagina&#39;s met de voornamen van gebruikers van hun profielattributen te personaliseren.

## Voordelen en waarde

* **optimaliseer inhoudsdoeltreffendheid**: Detecteer welke inhoudsvariaties en elementen het meest met uw klanten resoneren, die tot hogere betrokkenheid en omzettingen leiden.
* **gegevens-gedreven besluiten**: De gegevens van de hefboomwerking om geïnformeerde besluiten over uw inhoudsstrategie te nemen, die maximumeffect verzekeren.
* **Gepersonaliseerde gebruikerservaring**: Inhoud van de spoorstaaf om aan de unieke voorkeur en de behoeften van al uw publiekssegmenten te voldoen.

## Stapsgewijze instructies

>[!NOTE]
>
>In de instructies in deze sectie wordt de nadruk gelegd op de stappen die nodig zijn om een afbeelding te wijzigen en om profielkenmerken te gebruiken om tekstberichten aan te passen. Voor meer informatie over beschikbare opties in de [!DNL Journey Optimizer] Webontwerper, zie [ Webinhoud ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content) {target=_blank} in de *documentatie van Journey Optimizer* uitgeven.

Voer de volgende stappen uit om een webpagina te optimaliseren door verschillende afbeeldingen te testen en berichten aan te passen aan de voornamen van gebruikers:

1. In [!DNL Adobe Journey Optimizer], klik **Campagnes** in het linkerspoor om de [!UICONTROL Campaigns] pagina te tonen.

   ![ Adobe Journey Optimizer het landen pagina met benadrukte het lusje van Campagnes.](/help/main/c-integrating-target-with-mac/ajo/assets/ajo-landing-page.png)

1. Klik op **[!UICONTROL Create Campaign]** in de rechterbovenhoek van de pagina [!UICONTROL Campaigns] .

1. Selecteer **[!UICONTROL Scheduled - Marketing]** (het gebrek), dan klik **creëren** om de [!UICONTROL Campaign] detailspagina te tonen.

   ![ pagina van de Details van de Campagne in Adobe Journey Optimizer ](/help/main/c-integrating-target-with-mac/ajo/assets/campaign-details.png)

1. Geef in de sectie **[!UICONTROL Properties]** een beschrijvende naam en een optionele beschrijving voor de campagne op.

1. (Voorwaardelijk) Klik in de sectie **[!UICONTROL Audience]** op **[!UICONTROL Select Audience]** en kies het gewenste publiek.

   In dit geval hebben we ervoor gekozen de campagne voor alle bezoekers te activeren (de standaardinstelling).

1. Kies in de sectie **[!UICONTROL Action]** de optie **[!UICONTROL Web]** in de vervolgkeuzelijst **[!UICONTROL Action]** en selecteer of maak een nieuwe webconfiguratie.

   Een Webconfiguratie, of kanaaloppervlakte, is een configuratie die door een Beheerder van het Systeem wordt bepaald. De webconfiguratie bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameter, subdomein, mobiele apps enzovoort.

   Voor meer informatie, zie [ de oppervlakken van het het kanaalkanaal van de Opstelling ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces) {target=_blank} in de *documentatie van Journey Optimizer*.

1. Klik in de sectie **[!UICONTROL Action]** op **[!UICONTROL Edit Content]** om uw website te openen in de webontwerper van [!DNL Journey Optimizer] .

   Voor A/B-tests zijn twee of meer experimenten nodig. U kunt uw bestaande homepage als eerste experiment gebruiken. In de volgende stappen wordt uitgelegd hoe u een tweede experiment instelt.

   ![ Yoga landende pagina op de website LUMA ](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Als u een experiment wilt maken om te testen welke inhoud het beste werkt, klikt u op **[!UICONTROL Create Experiment]** .

   Met contentexperimenten kunt u de inhoud, het onderwerp of de afzender van berichten variëren om meerdere behandelingen te definiëren en de beste combinatie voor uw publiek te bepalen. Voor meer informatie, zie [ een inhoudexperiment ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/content-experiment) {target=_blank} in de *documentatie van Journey Optimizer* creëren.

1. Klik op **[!UICONTROL Edit Web Page]** in de rechtertrack.

   ![ geef de pagina van de Inhoud op Yoga uit het landen pagina ](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Als u de hoofdafbeelding wilt wijzigen, klikt u op de afbeelding die u wilt wijzigen en vervolgens op de knop **[!UICONTROL Choose Image]** .

   ![ kies beeldknoop ](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Blader naar de gewenste afbeelding en selecteer deze. Klik vervolgens op **[!UICONTROL Use This Image]** .

   ![ Nieuwe heldenbeeld op Yoga pagina ](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Als u het bericht wilt aanpassen met de voornamen van gebruikers met behulp van profielkenmerken, klikt u op de tekst die u wilt aanpassen en klikt u op **[!UICONTROL Add Personalization]** om de [!UICONTROL Add Personalization] -pagina weer te geven.

   ![ voeg de knoop van Personalization toe.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Voor meer informatie over profielattributen, zie [ begonnen worden met de verpersoonlijkingsredacteur ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions) {target=_blank} in de *documentatie van Journey Optimizer*.

1. Zoek en selecteer het profielkenmerk &quot;first name&quot;, pas de tekst naar wens aan en klik op **[!UICONTROL Save]** .

   ![ voeg profielattributen voor naam ](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png) toe

   Voor meer informatie, zie [ begonnen worden met de verpersoonlijkingsredacteur ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions) {target=_blank} in de *documentatie van Journey Optimizer*.

1. Klik op de pijl Vorige in de linkerbovenhoek om terug te keren naar de webontwerper.

   ![ de pijl van de Rug ](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Klik **[!UICONTROL Review to Activate]**, zorg ervoor dat alles zoals verwacht kijkt, dan klik **activeert**.

## Rapporten weergeven

Klik op de knop Rapporten en klik vervolgens op de gewenste rapportageperiode:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Voor meer informatie, zie [ begonnen worden met nieuwe Rapporterende interface ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channel-report/report-gs-cja) {target=_blank} in de *documentatie van Journey Optimizer*.

>[!MORELIKETHIS]
>
>[ geef Webinhoud ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/edit-web-content) {target=_blank} in de *documentatie van Journey Optimizer* uit
>[Hoe te video ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/web/author-web-pages/web-spa#video) {target=_blank} in de *documentatie van Journey Optimizer*
>[Creeer een campagne ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign) {target=_blank} in *Tutorials van Journey Optimizer*

