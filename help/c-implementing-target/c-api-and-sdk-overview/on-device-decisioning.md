---
keywords: serverzijde;serverzijde;sdk;sdks;op apparaat;besluitvorming;op apparaat;op apparaat;nul latentie;latentie;dichtbij-nul;node.js
description: Leer hoe te om op-apparaat besluitvorming te gebruiken om uw  [!DNL Target] A/B en activiteiten MVT op uw server in het voorgeheugen op te slaan om in-geheugenbesluit bij bijna-nul latentie uit te voeren.
title: Wat is een apparaatbeslissing?
feature: Server-kant implementeren
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: fe70f357e2298f1656d713aae5fae800e6775d64
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Apparaatbeslissingen

Beslissing op het apparaat biedt de mogelijkheid om uw [!DNL Adobe Target] [!UICONTROL A/B Test]- en [!UICONTROL Experience Targeting] (XT)-activiteiten op uw server in het cachegeheugen op te slaan en de besluitvorming in het geheugen uit te voeren bij een bijna-nullatentie, zonder netwerkverzoeken aan [!DNL Adobe Target] Edge Network te blokkeren.

Zie [Inleiding tot apparaatbesluitvorming](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) in de documentatie van *[Adobe Target SDK&#39;s](https://adobetarget-sdks.gitbook.io/docs/)* voor meer informatie.

## Webinar: Personaliseer en test bij nul latentie met op apparaat besluiten van [!DNL Adobe Target]

Meer dan ooit, worden de marketers, de producteigenaars en de ontwikkelaars belast met het optimaliseren van de algemene klantenervaring op plaatsen, in apps, en overal anders zij met hun klanten verbinden. Meerdere gereedschappen met gegevenssilo&#39;s en ingewikkelde implementaties zijn ontoereikend.

In dit geregistreerde webinar bespreken productdeskundigen [!DNL Adobe Target] hoe het bewegen van kritieke ervaring optimaliseringsbesluiten op apparaat om plaatselijk met bijna-nul latentie uit te voeren deuren voor opwindende nieuwe gebruiksgevallen kan openen terwijl het verbeteren van plaatsprestaties voor uw klanten.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## Aanbevolen procedures

Adobe raadt de volgende aanbevolen procedures aan bij het gebruik van apparaatbeslissingen:

### Tips en trucs wanneer de beslissingsmethode &quot;op apparaat&quot; is {#best-practices-on-device}

Wanneer u &quot;op het apparaat&quot; gebruikt als beslissingsmethode, wordt het artefact gedownload wanneer de bezoeker de webpagina voor het eerst laadt. Om het even welke activiteitenkwalificatie die op de eerste paginading (geen geheim voorgeheugen) moet gebeuren gebeurt slechts nadat het artefact volledig wordt gedownload. Er zijn bepaalde beste praktijken u kunt volgen om ervoor te zorgen dat de activiteitenkwalificaties voor een nieuwe anonieme bezoeker snel gebeuren.

* Deactiveer &quot;Op apparaat&quot;geschikt activiteiten die niet bedoeld zijn om in het artefact te zijn.
* Als u [!DNL Target Premium] hebt, kunt u [eigenschappen/werkruimten](/help/administrating-target/c-user-management/property-channel/property-channel.md) gebruiken om verschillende artefactendossiers voor verschillende werkruimten tot stand te brengen.
* Als uw artefactbestanden om legitieme redenen erg groot worden, kunt u de &quot;hybride&quot; beslissingsmethode gebruiken. Deze methode staat u toe om het artefact in parallel te downloaden en alle [!DNL Target] API vraag gaat over de draad tot het artefact heeft gedownload. Lees de beste [praktijksectie over &quot;Hybride&quot;bepalingswijze](#best-practices-hybrid) hieronder om meer over deze benadering te leren.
* Als u een toepassing voor één pagina hebt (SPA), raadt [!DNL Adobe] u aan om 0.js te laden en te initialiseren voordat u het JavaScript-hoofdbestand van uw toepassing laadt tijdens het laden van de eerste pagina. Met deze methode wordt het downloaden van artefacten veel eerder gestart, waardoor rendering sneller verloopt.

### Aanbevolen procedures wanneer de beslissingsmethode &quot;hybride&quot; is {#best-practices-hybrid}

Wanneer u &quot;hybride&quot; gebruikt als beslissingsmethode, wordt het artefact parallel gedownload. Totdat het artefact wordt gedownload, gaan om het even welke [!DNL Target] API vraag over de draad zelfs als de &quot;plaatsen&quot;op apparaat geschikt zijn. Dit gedrag is het gebrek voor alle `getOffers()` vraag en verstrekt de beste prestaties in de meeste situaties. Als u het standaardgedrag van `getOffers()` door `decisioningMethod` aan `on-device` te plaatsen verandert, volg deze beste praktijken om fouten te vermijden en de beste prestaties te verzekeren.

* Als u `getOffers()` met `decisioningMethod` als `on-device` wanneer de pagina voor het eerst laadt, moet u dit binnen de &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot;bij.js gebeurtenismanager doen om fouten te vermijden. Als uw artefact zeer groot is, worden om het even welke &quot;plaatsen&quot;die deze benadering gebruiken teruggegeven slechts nadat het artefact volledig wordt gedownload, wat het teruggeven kan vertragen. [!DNL Adobe] Het verdient aanbeveling deze aanpak zelden te volgen. Volg de beste praktijken om artefactgrootte onder [ &quot;Op Apparaat&quot;beste praktijken sectie](#best-practices-on-device) hierboven te verminderen wanneer het gebruiken van deze benadering.

## Zelfstudie: Apparaatbeslissingen

[!DNL Adobe Target] De beslissing op het apparaat maakt de levering van content met bijna-nullatentie mogelijk.

Deze video van 7 minuten:

* Beschrijft op apparaat beslist, met inbegrip van hoe het met andere methodes van [!DNL Target] implementatie vergelijkt
* Toont aan hoe te om op apparatenbesluit in [!DNL Target] toe te laten
* Hiermee wordt een op een formulier gebaseerde componentactiviteit onderzocht die is geconfigureerd met JSON-inhoud
* Toont de code van steekproefNode.JS SDK die zeer belangrijke die configuratie bevat voor op-apparatenbesluit wordt vereist
* Toont resultaten in browser aan

>[!VIDEO](https://video.tv.adobe.com/v/329032)

Zie de handleiding [Adobe Target Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html) voor meer video&#39;s en zelfstudies.

## Adobe Tech Blog - Deel 1: [!DNL Adobe Target] NodeJS SDK uitvoeren voor experimenteren en personalisatie op Edge-platforms (Akamai Edge Workers)

[Klik hier om het blogbericht](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9) te openen.

## Adobe Tech Blog - Deel 2: [!DNL Adobe Target] NodeJS SDK uitvoeren voor experimenteren en personalisatie op randplatforms (AWS Lambda@Edge)

[Klik hier om het blogbericht](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563) te openen.