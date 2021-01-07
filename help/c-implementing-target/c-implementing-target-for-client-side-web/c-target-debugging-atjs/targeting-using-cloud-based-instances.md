---
keywords: cloud instances;public suffix list;public suffix;cookie;first-party cookie;1st-party cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Informatie over problemen waarmee klanten worden geconfronteerd wanneer ze op cloud gebaseerde instanties gebruiken om Adobe Target te testen.
title: Gebruik cloudgebaseerde instanties met Doel
feature: at.js
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '143'
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
