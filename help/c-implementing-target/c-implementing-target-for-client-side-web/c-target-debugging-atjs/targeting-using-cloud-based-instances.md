---
keywords: wolkeninstanties;openbare achtervoegsellijst;openbaar achtervoegsel;cookie;cookie van eerste partij;cookie van eerste partij;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Verken problemen (met oplossingen) waar klanten mee te maken krijgen wanneer ze cloudgebaseerde instanties gebruiken om Adobe [!DNL Target] of voor concepttest-doeleinden te testen.
title: Kan ik [!DNL Target] met op wolken gebaseerde instanties gebruiken?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: 3c79b2ce70e456275ddf6774a35ae5c36f0ae99d
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Gebruik cloudgebaseerde instanties met Doel

Informatie over problemen waarmee klanten worden geconfronteerd wanneer ze cloudgebaseerde instanties gebruiken om [!DNL Adobe Target] te testen.

Doelklanten gebruiken soms cloudgebaseerde instanties met [!DNL Target] voor testdoeleinden of eenvoudige concepttest-doeleinden. Deze instanties kunnen de volgende domeinen omvatten:

`azurewebsites.net`,  `cloudapp.net`,  `amazonaws.com`,  `cloudfront.net`,  `herokuapp.com`of  `firebaseapp.com`

Deze domeinen, en vele anderen, maken deel uit van [Openbare Achtervoegsellijst](https://publicsuffix.org/list/public_suffix_list.dat).

**Probleem:** moderne browsers slaan geen cookies op als u deze domeinen gebruikt.

In de JavaScript-bibliotheek [!DNL at.js] worden cookies gebruikt om gebruikers bij te houden, zodat [!DNL Target] altijd een consistente ervaring biedt. Als de JavaScript-bibliotheek [!DNL Target] geen cookies kan opslaan, worden [!DNL Target]-aanvragen uitgeschakeld.

**Oplossing:** Als beste praktijken, als u op wolk-gebaseerde instanties met domeinen inbegrepen op de Openbare Lijst van het Achtervoegsel van het Hoogtepunt wilt gebruiken, zorg ervoor dat u het  `cookieDomain` plaatsen aanpast. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) voor meer informatie.
