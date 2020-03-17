---
keywords: cloud instances;public suffix list;public suffix;cookie;first-party cookie;1st-party cookie;azurewebsites.net;cloudapp.net;amazonaws.com;cloudfront.net;herokuapp.com;firebaseapp.com;targetGlobalSettings;cookieDomain
description: Informatie over problemen waarmee klanten worden geconfronteerd wanneer ze op cloud gebaseerde instanties gebruiken om Adobe Target te testen.
title: Gebruik cloudgebaseerde instanties met Doel
uuid: dcaba49e-7567-4970-bb9a-19377aff7d38
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Gebruik cloudgebaseerde instanties met Doel{#use-cloud-based-instances-with-target}

Informatie over problemen waarmee klanten worden geconfronteerd wanneer ze cloudgebaseerde instanties gebruiken om te testen [!DNL Adobe Target].

De doelklanten gebruiken soms op wolk-gebaseerde instanties met [!DNL Target] voor het testen of eenvoudige proef-van-concept doeleinden. Deze instanties kunnen de volgende domeinen omvatten:

`azurewebsites.net`, `cloudapp.net`, `amazonaws.com`, `cloudfront.net`, `herokuapp.com`of `firebaseapp.com`

Deze domeinen, en vele anderen, maken deel uit van de [Openbare Lijst](https://publicsuffix.org/list/public_suffix_list.dat)van het Achtervoegsel.

**Probleem:** Moderne browsers slaan geen cookies op als u deze domeinen gebruikt.

De [!DNL at.js] JavaScript- en [!DNL mbox.js] JavaScript-bibliotheken gebruiken cookies om gebruikers bij te houden, zodat deze [!DNL Target] altijd een consistente ervaring hebben. Als de [!DNL Target] JavaScript-bibliotheken geen cookies kunnen opslaan, worden [!DNL Target] aanvragen uitgeschakeld.

**Oplossing:** Als beste praktijken, als u op wolk-gebaseerde instanties met domeinen wilt gebruiken inbegrepen op de Openbare Lijst van het Achtervoegsel, zorg ervoor dat u het `cookieDomain` plaatsen aanpast. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)voor meer informatie.
