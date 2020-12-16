---
keywords: faq;frequently asked questions;analytics for target;a4T;classifications;classification;classifications importer;post-tnt-action
description: Dit onderwerp bevat antwoorden op vragen die vaak over classificaties worden gevraagd en het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Classificaties - A4T Veelgestelde vragen
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 403a56da912fa143cf6c20b078c0bba63c6f4420
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Classificaties - A4T Veelgestelde vragen{#classifications-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over classificaties worden gevraagd en gebruikend [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

## Hoe kan ik, nadat ik de Classificatieimportmodule heb gebruikt om classificaties te downloaden, de waarde voor post-tnt-action afstemmen op de naam van een activiteit? {#section_6045DAC488B248418F430E663C38D001}

U kunt de classificaties voor de tekenreeks A4T/TNT downloaden van de Admin Tools [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html). De variabele wordt &quot;TNT&quot; genoemd in de exportlijst. De gedownloade gegevens bevatten de vriendelijke namen voor activiteiten, ervaringen enzovoort.

Dit opzoekbestand is handig voor klanten die de gegevens van de clickstream van Adobe ontvangen. Het bestand bevat vriendelijke namen voor de kolommen `post_tnt` en `post_tnt_action`.

De tekenreeksindeling van de TNT-variabele is `activityID:experienceID:targettype|event`.

* targetType = 0 (controle/willekeurig) of 1 (gericht) voor [!UICONTROL Auto-Allocate]- en [!UICONTROL Auto-Target]-activiteiten.
* Event = 0 staat voor een ervaringstoegang.
* Gebeurtenis = 1 vertegenwoordigt een ervaringsbezoek.
* Event = 2 is een activiteitsindruk.
* Event = 3-32766 vertegenwoordigt metrische id van het analyseresultaat.
* Gebeurtenis = 32767 vertegenwoordigt een activiteitconversie.

U kunt het classificatiebestand regelmatig vanuit de gebruikersinterface importeren met een [browser-import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/browser-import.html) of een [FTP-import](https://docs.adobe.com/help/en/analytics/components/classifications/classifications-importer/import-file.html). U kunt met de Diensten van de Techniek ook in dienst nemen om het dossier als raadplegingslijst samen met een klikstroomgegevens te verkrijgen.
