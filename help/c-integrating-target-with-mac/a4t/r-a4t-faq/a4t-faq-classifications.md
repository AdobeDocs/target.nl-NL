---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;classificaties;classificatie;classificaties importeur;post-tnt-action
description: Vind antwoorden op vragen over classificaties en het gebruiken van Analytics voor  [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] activiteiten.
title: Waar kan ik informatie over classificaties met A4T vinden?
feature: Analyses voor doel (A4T)
exl-id: 875f6c1c-1bda-40a9-96f2-d58c00d91d20
source-git-commit: cdb79c82fe1e7158a2f2014df661bd6fa852df92
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Classificaties - A4T Veelgestelde vragen

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
* Gebeurtenis -1 of 65535 vertegenwoordigt dat de gebruiker uit de activiteit of de ervaring wordt verwijderd. Dit gebeurt vaak wanneer de bezoeker de site omslaat. De bezoeker wordt losgelaten uit de ervaring en is nu beschikbaar om in aanmerking te komen voor een andere ervaring.

U kunt het classificatiebestand regelmatig vanuit de gebruikersinterface importeren met een [browser-import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/browser-import.html?lang=en) of een [FTP-import](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/import-file.html?lang=en). U kunt met de Diensten van de Techniek ook in dienst nemen om het dossier als raadplegingslijst samen met een klikstroomgegevens te verkrijgen.
