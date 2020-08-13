---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: Dit onderwerp bevat antwoorden op vragen die vaak over classificaties worden gevraagd en het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Classificaties - A4T Veelgestelde vragen
feature: a4t troubleshooting
topic: Standard
uuid: 4b42adbc-4fa8-4b62-86c8-bb8f8bec7e54
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Classificaties - A4T Veelgestelde vragen{#classifications-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over classificaties worden gevraagd en gebruikt [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

## Hoe kan ik, nadat ik de Classificatieimportmodule heb gebruikt om classificaties te downloaden, de waarde voor post-tnt-action afstemmen op de naam van een activiteit? {#section_6045DAC488B248418F430E663C38D001}

U kunt de classificaties voor de A4T/TNT-tekenreeks downloaden van de Admin Tools [Classification Importer](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html). De variabele wordt &quot;TNT&quot; genoemd in de exportlijst. De gedownloade gegevens bevatten de vriendelijke namen voor activiteiten, ervaringen enzovoort.

Dit opzoekbestand is handig voor klanten die de gegevens van de clickstream van Adobe ontvangen. Het bestand bevat vriendelijke namen voor de `post_tnt` kolommen en de `post_tnt_action` kolommen.

De tekenreeksindeling van de TNT-variabele is `activityID:experienceID:targettype|event`.

* doelsoort = 0 (controle/willekeurig) of 1 (doelwit) voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.
* Event = 0 staat voor een ervaringstoegang.
* Gebeurtenis = 1 vertegenwoordigt een ervaringsbezoek.
* Event = 2 is een activiteitsindruk.
* Gebeurtenis = 32767 vertegenwoordigt een activiteitconversie.

U kunt het classificatiebestand regelmatig vanuit de gebruikersinterface importeren met behulp van een [browserimport](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) of een [FTP-import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). U kunt met de Diensten van de Techniek ook in dienst nemen om het dossier als raadplegingslijst samen met een klikstroomgegevens te verkrijgen.
