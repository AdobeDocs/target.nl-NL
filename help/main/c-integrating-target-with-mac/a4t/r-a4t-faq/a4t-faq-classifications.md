---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;classificaties;classificatie;classificaties importeur;post-tnt-action;gebeurteniscodes
description: Zoek antwoorden op vragen over classificaties en gebruik [!UICONTROL Analytics for Target] (A4T).
title: Waar kan ik informatie over classificaties met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# Classificaties - A4T Veelgestelde vragen

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over classificaties en waarbij [!DNL Analytics] wordt gebruikt als rapportagebron voor [!DNL Target] (A4T).

## Nadat u classificaties hebt gedownload met [!UICONTROL Classifications Importer] , hoe moet ik de waarde voor post-tnt-action afstemmen op de naam van een activiteit? {#section_6045DAC488B248418F430E663C38D001}

+++Antwoord
U kunt de classificaties voor het koord A4T/TNT van Admin Hulpmiddelen [&#x200B; Importer van de Classificatie &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html?lang=nl-NL) downloaden. De variabele wordt &quot;TNT&quot; genoemd in de exportlijst. De gedownloade gegevens bevatten de vriendelijke namen voor activiteiten, ervaringen enzovoort.

Dit opzoekbestand is handig voor klanten die de [!DNL Adobe] -feed clickStream-gegevens ontvangen. Het bestand bevat vriendelijke namen voor de kolommen `post_tnt` en `post_tnt_action` .

Voor standaard [!UICONTROL A/B Test] - en [!UICONTROL Experience Targeting] (XT) -activiteiten is de indeling van de TNT-tekenreeks:

```
activityID:experienceID:targettype|event
```

Voor [!UICONTROL Auto-Allocate] - en [!UICONTROL Auto-Target] -activiteiten is de indeling van de TNT-tekenreeks:

```
activityId:experienceId:targettype:algorithmId|event
```

* `targettype` = `targettype` en `algorithmId` zijn interne id&#39;s die worden gebruikt door [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] -activiteiten.
* Event = 0 staat voor een ervaringstoegang.
* Gebeurtenis = 1 vertegenwoordigt een ervaringsbezoek.
* Event = 2 is een activiteitsindruk.
* Event = 3-32766 vertegenwoordigt metrische id van het analyseresultaat.
* Gebeurtenis = 32767 vertegenwoordigt een activiteitconversie.
* Gebeurtenis -1 of 65535 vertegenwoordigt dat de gebruiker uit de activiteit of de ervaring wordt verwijderd. Dit gebeurt vaak wanneer de bezoeker de site omslaat. De bezoeker wordt losgelaten uit de ervaring en is nu beschikbaar om in aanmerking te komen voor een andere ervaring.

U kunt het classificatiedossier op een regelmatige basis van UI invoeren gebruikend de invoer van de browser van a [&#128279;](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=nl-NL) of de invoer van FTP van a [&#128279;](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=nl-NL). U kunt met de Diensten van de Techniek ook in dienst nemen om het dossier als raadplegingslijst samen met een klikstroomgegevens te verkrijgen.

+++
