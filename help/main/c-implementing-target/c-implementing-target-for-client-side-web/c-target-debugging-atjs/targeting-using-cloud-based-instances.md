---
keywords: wolkeninstanties;openbare achtervoegsellijst;openbaar achtervoegsel;cookie;cookie van eerste partij;cookie van eerste partij;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Problemen verkennen (met oplossingen) waarmee klanten worden geconfronteerd wanneer ze cloudgebaseerde instanties gebruiken om Adobe te testen [!DNL Target] of voor conceptuele doeleinden.
title: Kan ik gebruiken [!DNL Target] met op cloud gebaseerde instanties?
feature: at.js
role: Developer
exl-id: 220371a9-ba57-4e67-b82f-8fec6f9d2833
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Gebruik cloudgebaseerde instanties met Doel

Informatie over problemen waarmee klanten worden geconfronteerd wanneer ze cloudgebaseerde instanties gebruiken om te testen [!DNL Adobe Target].

Doelklanten gebruiken soms cloudgebaseerde instanties met [!DNL Target] voor tests of eenvoudige concepttest. Deze instanties kunnen de volgende domeinen omvatten:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com`, of `firebaseapp.com`

Deze en vele andere domeinen maken deel uit van de [Lijst met openbare achtervoegsels](https://publicsuffix.org/list/public_suffix_list.dat).

**Probleem:** Moderne browsers slaan geen cookies op als u deze domeinen gebruikt.

De [!DNL at.js] JavaScript-bibliotheek gebruikt cookies om gebruikers bij te houden om ervoor te zorgen dat [!DNL Target] biedt altijd een consistente ervaring. Als de [!DNL Target] JavaScript-bibliotheek kan cookies niet opslaan, [!DNL Target] aanvragen zijn uitgeschakeld.

**Oplossing:** Als beste praktijken, als u op wolk-gebaseerde instanties met domeinen inbegrepen op de Openbare Lijst van het Achtervoegsel van het Hoogtepunt wilt gebruiken, zorg ervoor dat u aanpast `cookieDomain` instellen. Zie voor meer informatie [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.
