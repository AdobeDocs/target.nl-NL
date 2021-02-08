---
keywords: wolkeninstanties;openbare achtervoegsellijst;openbaar achtervoegsel;cookie;cookie van eerste partij;cookie van eerste partij;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Verken problemen (met oplossingen) waar klanten mee te maken krijgen wanneer ze cloudgebaseerde instanties gebruiken om Adobe Target te testen of voor concepttest-doeleinden.
title: Kan ik Doel gebruiken met instanties op basis van cloud?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# Gebruik cloudgebaseerde instanties met Doel{#use-cloud-based-instances-with-target}

Informatie over problemen waarmee klanten worden geconfronteerd wanneer ze cloudgebaseerde instanties gebruiken om [!DNL Adobe Target] te testen.

Doelklanten gebruiken soms cloudgebaseerde instanties met [!DNL Target] voor testdoeleinden of eenvoudige concepttest-doeleinden. Deze instanties kunnen de volgende domeinen omvatten:

`azurewebsites.net`,  `cloudapp.net`,  `amazonaws.com`,  `cloudfront.net`,  `herokuapp.com`of  `firebaseapp.com`

Deze domeinen, en vele anderen, maken deel uit van [Openbare Achtervoegsellijst](https://publicsuffix.org/list/public_suffix_list.dat).

**Probleem:** moderne browsers slaan geen cookies op als u deze domeinen gebruikt.

De JavaScript-bibliotheken [!DNL at.js] en [!DNL mbox.js] gebruiken cookies om gebruikers bij te houden om ervoor te zorgen dat [!DNL Target] altijd een consistente ervaring biedt. Als de [!DNL Target] JavaScript-bibliotheken geen cookies kunnen opslaan, worden [!DNL Target]-aanvragen uitgeschakeld.

**Oplossing:** Als beste praktijken, als u op wolk-gebaseerde instanties met domeinen inbegrepen op de Openbare Lijst van het Achtervoegsel van het Hoogtepunt wilt gebruiken, zorg ervoor dat u het  `cookieDomain` plaatsen aanpast. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) voor meer informatie.
