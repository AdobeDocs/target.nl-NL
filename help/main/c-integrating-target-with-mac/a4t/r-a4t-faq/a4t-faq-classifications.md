---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;classificaties;classificatie;classificaties importeur;post-tnt-action;gebeurteniscodes
description: Antwoorden zoeken op vragen over classificaties en het gebruik [!UICONTROL Analytics for Target] (A4T).
title: Waar kan ik informatie over classificaties met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Classificaties - A4T Veelgestelde vragen

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over classificaties en het gebruiken [!DNL Analytics] als bron van rapportage voor [!DNL Target] (A4T).

## Nadat u de [!UICONTROL Classifications Importer] Hoe kan ik de waarde voor post-tnt-action afstemmen op een naam van een activiteit om classificaties te downloaden? {#section_6045DAC488B248418F430E663C38D001}

+++Antwoord U kunt de classificaties voor de tekenreeks A4T/TNT downloaden via de beheerhulpprogramma&#39;s [Classificatieimportmodule](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html). De variabele wordt &quot;TNT&quot; genoemd in de exportlijst. De gedownloade gegevens bevatten de vriendelijke namen voor activiteiten, ervaringen enzovoort.

Dit opzoekbestand is handig voor klanten die [!DNL Adobe]s clickStream data feed. Het bestand bevat vriendelijke namen voor de `post_tnt` en `post_tnt_action` kolommen.

Voor standaard [!UICONTROL A/B Test] en [!UICONTROL Experience Targeting] (XT) activiteiten, is het formaat van het TNT koord:

```
activityID:experienceID:targettype|event
```

Voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten, is het formaat van het TNT koord:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` en `algorithmId` zijn interne id&#39;s die worden gebruikt door [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten.
* Event = 0 staat voor een ervaringstoegang.
* Gebeurtenis = 1 vertegenwoordigt een ervaringsbezoek.
* Event = 2 is een activiteitsindruk.
* Event = 3-32766 vertegenwoordigt metrische id van het analyseresultaat.
* Gebeurtenis = 32767 vertegenwoordigt een activiteitconversie.
* Gebeurtenis -1 of 65535 vertegenwoordigt dat de gebruiker uit de activiteit of de ervaring wordt verwijderd. Dit gebeurt vaak wanneer de bezoeker de site omslaat. De bezoeker wordt losgelaten uit de ervaring en is nu beschikbaar om in aanmerking te komen voor een andere ervaring.

U kunt het classificatiebestand regelmatig vanuit de gebruikersinterface importeren met een [browserimport](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) of [FTP importeren](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en). U kunt met de Diensten van de Techniek ook in dienst nemen om het dossier als raadplegingslijst samen met een klikstroomgegevens te verkrijgen.

+++
