---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;classificaties;classificatie;classificaties importeur;post-tnt-action;gebeurteniscodes
description: Zoek antwoorden op vragen over classificaties en gebruik [!UICONTROL Analytics for Target] (A4T).
title: Waar kan ik informatie over classificaties met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: e81a27bc321fa83cc1b2449e5df32edfa37d5198
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Classificaties - A4T Veelgestelde vragen

Dit onderwerp bevat antwoorden op vragen die vaak over classificaties worden gevraagd en gebruikend [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

## Hoe kan ik, nadat ik de [!UICONTROL Classifications Importer] heb gebruikt om classificaties te downloaden, de waarde voor post-tnt-action afstemmen op de naam van een activiteit? {#section_6045DAC488B248418F430E663C38D001}

U kunt de classificaties voor de tekenreeks A4T/TNT downloaden van de Admin Tools [Classification Importer](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html). De variabele wordt &quot;TNT&quot; genoemd in de exportlijst. De gedownloade gegevens bevatten de vriendelijke namen voor activiteiten, ervaringen enzovoort.

Dit opzoekbestand is handig voor klanten die [!DNL Adobe]&#39;s clickstream-gegevensfeed ontvangen. Het bestand bevat vriendelijke namen voor de kolommen `post_tnt` en `post_tnt_action`.

Voor standaard [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten, is het formaat van het TNT koord:

```
activityID:experienceID:targettype|event
```

Voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten, is het formaat van het TNT koord:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` =  `targettype` en  `algorithmId` zijn interne identificatoren die door  [!UICONTROL Auto-Allocate] en  [!UICONTROL Auto-Target] activiteiten worden gebruikt.
* Event = 0 staat voor een ervaringstoegang.
* Gebeurtenis = 1 vertegenwoordigt een ervaringsbezoek.
* Event = 2 is een activiteitsindruk.
* Event = 3-32766 vertegenwoordigt metrische id van het analyseresultaat.
* Gebeurtenis = 32767 vertegenwoordigt een activiteitconversie.
* Gebeurtenis -1 of 65535 vertegenwoordigt dat de gebruiker uit de activiteit of de ervaring wordt verwijderd. Dit gebeurt vaak wanneer de bezoeker de site omslaat. De bezoeker wordt losgelaten uit de ervaring en is nu beschikbaar om in aanmerking te komen voor een andere ervaring.

U kunt het classificatiebestand regelmatig vanuit de gebruikersinterface importeren met een [browser-import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) of een [FTP-import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en). U kunt met de Diensten van de Techniek ook in dienst nemen om het dossier als raadplegingslijst samen met een klikstroomgegevens te verkrijgen.
