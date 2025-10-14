---
keywords: optimalisatie;personalisatie;adobe-reis optimizer;ajo;use cases;scenario's;content change/ab test;profile, kenmerk;image wijzigen;image wisselen
description: Ontgrendel de geheimen voor effectieve wijzigingen in A/B-testinhoud in Adobe Journey Optimizer
title: De inhoud verandert door het testen A/B in  [!DNL Adobe Journey Optimizer]
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#beta newtab=true" tooltip="Wat zijn de eigenschappen van Beta in  [!DNL Adobe Target]."
feature: Integrations
hide: true
hidefromtoc: true
exl-id: e5aed7cd-7701-4133-ac7c-98e528c8a763
source-git-commit: b66abe9649f8c257891c1cd8e5736b7f91501c13
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Inhoud verandert via A/B-tests in [!DNL Adobe Journey Optimizer]

Met dit gebruiksgeval kunt u de geheimen ontgrendelen zodat wijzigingen in de inhoud van A/B-tests in [!DNL Adobe Journey Optimizer] worden doorgevoerd.

Dit gebruiksgeval toont aan hoe te om vertrouwde taken uit te voeren, zoals het testen A/B met een [&#x200B; activiteit van de Test A/B &#x200B;](/help/main/c-activities/t-test-ab/test-ab.md) in [!DNL Adobe Target], gebruikend [!DNL Journey Optimizer] in plaats van [!DNL Adobe Target].

## Voordelen en waarde

* **optimaliseer inhoudsdoeltreffendheid**: Detecteer welke inhoudsvariaties en elementen het meest met uw klanten resoneren, die tot hogere betrokkenheid en omzettingen leiden.
* **gegevens-gedreven besluiten**: De gegevens van de hefboomwerking om geïnformeerde besluiten over uw inhoudsstrategie te nemen, die maximumeffect verzekeren.
* **Gepersonaliseerde gebruikerservaring**: Inhoud van de spoorstaaf om aan de unieke voorkeur en de behoeften van al uw publiekssegmenten te voldoen.

## Mogelijke scenario&#39;s

* Een merkwaardig bedrijf verhoogde omzettingen door diverse beelden te testen en campagne landende pagina&#39;s met de voornamen van gebruikers in de tekst van call-to-action te personaliseren.

* Een e-commercebedrijf stelde vast dat zijn leden van de Gold-loyaliteit hogere omrekeningskoersen hadden door verschillende productbeschrijvingen en afbeeldingen op een campagnelandingspagina te testen, wat leidde tot meer verkoop.

## Stappen

>[!NOTE]
>
>In de instructies in deze sectie wordt de nadruk gelegd op de stappen die nodig zijn om een afbeelding te wijzigen en om profielkenmerken te gebruiken om tekstberichten aan te passen. Voor meer informatie over beschikbare opties in de [!DNL Journey Optimizer] Webontwerper, zie [&#x200B; Werk met de Webontwerper &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in de *documentatie van Journey Optimizer*.
>
>De video onder aan de pagina is vooral handig.

Een webpagina optimaliseren door verschillende afbeeldingen te testen en berichten met de voornamen van gebruikers aan te passen met behulp van een profielscript:

1. In [!DNL Journey Optimizer], klik **Campagnes** in het linkerspoor om de [!UICONTROL Campaigns] pagina te tonen.

1. Klik op **[!UICONTROL Create Campaign]** in de rechterbovenhoek van de pagina [!UICONTROL Campaigns] .

1. Selecteer **[!UICONTROL Scheduled - Marketing]** (het gebrek), dan klik **creëren** om de [!UICONTROL Campaign] detailspagina te tonen.

1. Geef in de sectie **[!UICONTROL Properties]** een beschrijvende naam en een optionele beschrijving voor de campagne op.

1. (Voorwaardelijk) Klik in de sectie **[!UICONTROL Audience]** op **[!UICONTROL Select Audience]** en kies het gewenste publiek.

   Voor dit gebruik kunt u de campagne voor [!UICONTROL All Visitors] activeren (de standaardinstelling).

1. Kies in de sectie **[!UICONTROL Action]** de optie **[!UICONTROL Web]** in de vervolgkeuzelijst **[!UICONTROL Action]** en selecteer of maak een nieuwe webconfiguratie.

   Een Webconfiguratie, of kanaaloppervlakte, is een configuratie die door een systeembeheerder wordt bepaald. De webconfiguratie bevat alle technische parameters voor het verzenden van het bericht, zoals headerparameter, subdomein, mobiele apps enzovoort.

   Voor meer informatie, zie [&#x200B; de oppervlakken van het het kanaalkanaal van de Opstelling &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/configuration/channel-surfaces#set-up-channel-surfaces){target=_blank} in de *documentatie van Journey Optimizer*.

1. Klik in de sectie **[!UICONTROL Action]** op **[!UICONTROL Edit Content]** om uw website te openen in de webontwerper van [!DNL Journey Optimizer] .

   Voor A/B-tests zijn twee of meer experimenten nodig. U kunt uw bestaande homepage als eerste experiment gebruiken. In de volgende stappen wordt uitgelegd hoe u een tweede experiment instelt.

   ![&#x200B; Yoga landende pagina op de website LUMA &#x200B;](/help/main/c-integrating-target-with-mac/ajo/assets/luma-yoga-landing.png)

1. Klik op **[!UICONTROL Create Experiment]** als u een experiment wilt maken om te bepalen welke inhoud beter presteert.

   Met contentexperimenten kunt u de inhoud, het onderwerp of de afzender van berichten variëren om meerdere behandelingen te definiëren en de beste combinatie voor uw publiek te bepalen. Voor meer informatie, zie [&#x200B; een inhoudexperiment &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/content-management/content-experiment/content-experiment){target=_blank} in de *documentatie van Journey Optimizer* creëren.

1. Selecteer metrisch succes en klik actie.

   Klik op de Help-pictogrammen voor meer informatie en voor koppelingen naar relevante artikelen.

1. Klik op **[!UICONTROL Add Treatment]** en vervolgens op **[!UICONTROL Create]** .

   In dit geval kunt u de verdeling voor elk experiment op 50% laten staan.

1. Klik onder [!UICONTROL Campaign] onder **[!UICONTROL Action]** op de pagina met **[!UICONTROL Edit Content]** details.

1. Klik op Web onder Behandeling B.

   Voor dit gebruik moet u [!UICONTROL Treatment A] ongewijzigd laten om de oorspronkelijke ervaring te gebruiken als de eerste ervaring in de A/B-test.

1. Klik op **[!UICONTROL Edit Web Page]** in de rechtertrack.

   ![&#x200B; geef de pagina van de Inhoud op Yoga uit het landen pagina &#x200B;](/help/main/c-integrating-target-with-mac/ajo/assets/edit-yoga-page.png)

1. Als u de hoofdafbeelding wilt wijzigen, klikt u op de afbeelding die u wilt wijzigen en vervolgens op de knop **[!UICONTROL Choose Image]** .

   ![&#x200B; kies beeldknoop &#x200B;](/help/main/c-integrating-target-with-mac/ajo/assets/choose-image.png)

1. Blader naar de gewenste afbeelding en selecteer deze. Klik vervolgens op **[!UICONTROL Use This Image]** .

   ![&#x200B; Nieuwe heldenbeeld op Yoga pagina &#x200B;](/help/main/c-integrating-target-with-mac/ajo/assets/new-hero-image.png)

1. Als u het bericht wilt aanpassen met de voornamen van gebruikers met behulp van profielkenmerken, klikt u op de tekst die u wilt aanpassen en klikt u op **[!UICONTROL Add Personalization]** om de [!UICONTROL Add Personalization] -pagina weer te geven.

   ![&#x200B; voeg de knoop van Personalization toe.](/help/main/c-integrating-target-with-mac/ajo/assets/add-personalization-button.png)

   Voor meer informatie over profielattributen, zie [&#x200B; begonnen worden met de verpersoonlijkingsredacteur &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in de *documentatie van Journey Optimizer*.

1. Zoek en klik op het plusteken om het profielkenmerk &quot;voornaam&quot; toe te voegen, pas de tekst naar wens aan en klik op **[!UICONTROL Save]** .

   ![&#x200B; voeg profielattributen voor naam &#x200B;](/help/main/c-integrating-target-with-mac/ajo/assets/add-profile-attribute-for-name.png) toe

   Voor meer informatie, zie [&#x200B; begonnen worden met de verpersoonlijkingsredacteur &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/content-management/personalization/expression-editor/personalization-build-expressions){target=_blank} in de *documentatie van Journey Optimizer*.

1. Klik op de pijl Vorige in de linkerbovenhoek om terug te keren naar de webontwerper.

   ![&#x200B; de pijl van de Rug &#x200B;](/help/main/c-integrating-target-with-mac/ajo/assets/back-arrow.png)

1. Klik **[!UICONTROL Review to Activate]**, zorg ervoor dat alles zoals verwacht kijkt, dan klik **activeert**.

## Rapporten weergeven

Klik op de knop [!UICONTROL Reports] en klik vervolgens op de gewenste rapportageperiode:

* [!UICONTROL View all time report]
* [!UICONTROL View last 24hrs report]

Voor meer informatie, zie [&#x200B; begonnen worden met nieuwe Rapporterende interface &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/channel-report/report-gs-cja){target=_blank} in de *documentatie van Journey Optimizer*.

>[!MORELIKETHIS]
>
>[&#x200B; Werk met de Webontwerper &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/channels/web/author-web-pages/web-visual-editor){target=_blank} in de *documentatie van Journey Optimizer*
>&#x200B;>[Creeer een campagne &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/tutorials/create-campaigns/create-a-campaign){target=_blank} in *Zelfstudies van Journey Optimizer*
