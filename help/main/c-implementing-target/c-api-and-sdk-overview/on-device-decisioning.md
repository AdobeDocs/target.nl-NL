---
keywords: serverzijde;serverzijde;sdk;sdks;op apparaat;besluitvorming;op apparaat;op apparaat;nul latentie;latentie;dichtbij-nul;node.js
description: Leer hoe u op het apparaat beslissingen kunt gebruiken om uw [!DNL Target] A/B en MVT activiteiten op uw server om in-geheugenbesluit bij bijna-nul latentie uit te voeren.
title: Wat is een apparaatbeslissing?
feature: Implement Server-side
role: Developer
exl-id: ae782511-6f32-4123-be76-838584e05b39
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Apparaatbeslissingen

De beslissing op het apparaat biedt de mogelijkheid om uw [!DNL Adobe Target] [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) de activiteiten op uw server en voeren in geheugenbesluit bij bijna-nul latentie uit, zonder netwerkverzoeken aan te blokkeren [!DNL Adobe Target] Edge Network.

Zie onderwerpen voor meer informatie:

* [Apparaatbeslissingen voor client-side](https://developer.adobe.com/target/implement/client-side/){target=_blank}
* [Apparaatbeslissingen voor server-side](https://developer.adobe.com/target/implement/server-side/sdk-guides/on-device-decisioning/){target=_blank}

## Webinar: Personaliseer en test bij nul latentie met op apparaat besluiten van [!DNL Adobe Target]

Meer dan ooit, worden de marketers, de producteigenaars en de ontwikkelaars belast met het optimaliseren van de algemene klantenervaring op plaatsen, in apps, en overal anders zij met hun klanten verbinden. Meerdere gereedschappen met gegevenssilo&#39;s en ingewikkelde implementaties zijn ontoereikend.

In dit geregistreerde webinar: [!DNL Adobe Target] productdeskundigen bespreken hoe u met behulp van beslissingen voor optimalisatie van kritieke ervaringen op apparaten, die lokaal kunnen worden uitgevoerd met bijna-nullatentie, deuren kunt openen voor spannende nieuwe gebruiksgevallen en de prestaties van de site voor uw klanten kunt verbeteren.

>[!VIDEO](https://video.tv.adobe.com/v/328148)

## Aanbevolen procedures

Adobe raadt de volgende aanbevolen procedures aan bij het gebruik van apparaatbeslissingen:

### Tips en trucs wanneer de beslissingsmethode &quot;op apparaat&quot; is {#best-practices-on-device}

Wanneer u &quot;op het apparaat&quot; gebruikt als beslissingsmethode, wordt het artefact gedownload wanneer de bezoeker de webpagina voor het eerst laadt. Om het even welke activiteitenkwalificatie die op de eerste paginading (geen geheim voorgeheugen) moet gebeuren gebeurt slechts nadat het artefact volledig wordt gedownload. Er zijn bepaalde beste praktijken u kunt volgen om ervoor te zorgen dat de activiteitenkwalificaties voor een nieuwe anonieme bezoeker snel gebeuren.

* Deactiveer &quot;Op apparaat&quot;geschikt activiteiten die niet bedoeld zijn om in het artefact te zijn.
* Als u [!DNL Target Premium]kunt u [eigenschappen/werkruimten](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) om verschillende artefactenbestanden te maken voor verschillende werkruimten.
* Als uw artefactbestanden om legitieme redenen erg groot worden, kunt u de &quot;hybride&quot; beslissingsmethode gebruiken. Met deze methode kunt u het artefact parallel en allemaal downloaden [!DNL Target] API de vraag gaat over de draad tot het artefact heeft gedownload. Het beste lezen [praktijkgedeelte over &quot;Hybride&quot;-beslissingsmodus](#best-practices-hybrid) hieronder voor meer informatie over deze aanpak.
* Als u een toepassing voor één pagina hebt (SPA), [!DNL Adobe] Het wordt aangeraden om .js te laden en te initialiseren voordat u het JavaScript-hoofdbestand van uw toepassing laadt tijdens het laden van de eerste pagina. Met deze methode wordt het downloaden van artefacten veel eerder gestart, waardoor rendering sneller verloopt.

### Aanbevolen procedures wanneer de beslissingsmethode &quot;hybride&quot; is {#best-practices-hybrid}

Wanneer u &quot;hybride&quot; gebruikt als beslissingsmethode, wordt het artefact parallel gedownload. Tot het artefact wordt gedownload, om het even welke [!DNL Target] API-aanroepen gaan over de kabel, zelfs als de &#39;locaties&#39; geschikt zijn voor het apparaat. Dit gedrag is de standaardinstelling voor alles `getOffers()` roept en verstrekt de beste prestaties in de meeste situaties. Als u het standaardgedrag wijzigt van `getOffers()` door de `decisioningMethod` tot `on-device`, deze beste praktijken volgen om fouten te vermijden en de beste prestaties te verzekeren.

* Als u besluit te roepen `getOffers()` with `decisioningMethod` als `on-device` wanneer de pagina voor het eerst wordt geladen, moet u dit binnen de gebeurtenishandler &quot;ARTIFACT_DOWNLOAD_SUCCEEDED&quot; at.js doen om fouten te voorkomen. Als uw artefact zeer groot is, worden om het even welke &quot;plaatsen&quot;die deze benadering gebruiken teruggegeven slechts nadat het artefact volledig wordt gedownload, wat het teruggeven kan vertragen. [!DNL Adobe] Het verdient aanbeveling deze aanpak zelden te volgen. Volg de beste praktijken om artefactgrootte onder te verminderen [&quot;Op apparaat&quot;, sectie met aanbevolen werkwijzen](#best-practices-on-device) bij deze aanpak.

## Zelfstudie: Apparaatbeslissingen

[!DNL Adobe Target] De beslissing op het apparaat maakt de levering van content met bijna-nullatentie mogelijk.

Deze video van 7 minuten:

* Beschrijft op apparaat beslist, met inbegrip van hoe het met andere methodes van vergelijkt [!DNL Target] uitvoering
* Toont aan hoe te om op apparaat het besluiten in toe te laten [!DNL Target]
* Hiermee wordt een op een formulier gebaseerde componentactiviteit onderzocht die is geconfigureerd met JSON-inhoud
* Toont de code van steekproefNode.JS SDK die zeer belangrijke die configuratie bevat voor op-apparatenbesluit wordt vereist
* Toont resultaten in browser aan

>[!VIDEO](https://video.tv.adobe.com/v/329032)

Zie de [Adobe Target Tutorials](https://experienceleague.adobe.com/docs/target-learn/tutorials/overview.html) hulplijn.

## Adobe Tech Blog - Deel 1: Uitvoeren [!DNL Adobe Target] NodeJS SDK voor experimenteren en personalisatie op Edge-platforms (Akamai Edge Workers)

[Klik hier om het blogbericht te openen](https://medium.com/adobetech/part-1-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-4d8660964ed9).

## Adobe Tech Blog - Deel 2: Uitvoeren [!DNL Adobe Target] NodeJS SDK voor experimenteren en personalisatie op Edge-platforms (AWS Lambda@Edge)

[Klik hier om het blogbericht te openen](https://medium.com/adobetech/part-2-run-adobe-target-nodejs-sdk-for-experimentation-and-personalization-on-edge-platforms-aws-4d6bdac24563).