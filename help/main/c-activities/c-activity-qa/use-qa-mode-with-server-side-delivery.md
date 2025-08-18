---
keywords: qa;serverzijde;server-kant;voorvertoning;voorvertoning van koppelingen
description: Leer hoe te om Adobe  [!DNL Target]  QA URLs met server-zijlevering te gebruiken om gemakkelijke activiteitQA van begin tot eind met voorproefverbindingen uit te voeren die nooit veranderen, facultatief publiek richtend, en QA rapporterend die van levende activiteitengegevens gesegmenteerd blijft.
title: Kan ik activiteit QA met Server-kant levering uitvoeren?
feature: Activities
exl-id: eb6965be-92a6-452d-ac01-7ae1533239cc
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Activiteit QA met levering aan de serverzijde gebruiken

Gebruik QA URLs met server-zijlevering in [!DNL Adobe Target] om gemakkelijke activiteit QA met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.

De standaardimplementatie van Activity QA ondersteunt het doorgeven van `qa_mode` -parameters via `pageUrl` -parameters. Deze aanpak is handig voor standaard/ajax [!DNL Target] -aanroepen. Voor server-naar-server aanroepen is dit echter niet de beste aanpak voor een geval van Mobile SDK als `pageUrl` niet beschikbaar is.

Het volgende codevoorbeeld toont Activiteit QA in een server-zijvraag:

```json
{
  "mbox" : "orderConfirmPage",
  "clientSideAnalyticsLogging": true,
  "clicked" : true,
  "tntId" : "12121212.17_01",
  "order" : {
    ...
  },
  "profileParameters" : {
    ...
  },
  "mboxParameters" : {
    ...
  },
  "requestLocation" : {
    ...
  },
  "qaMode" : {
    "token" : "<encrypted token string>",
    "bypassEntryAudience" : true,
    "listedActivitiesOnly" : true,
    "evaluateAsTrueAudienceIds" : [audienceId1, audienceId2...],
    "evaluateAsFalseAudienceIds" : [audienceId3, audienceId4...],
    "previewIndexes" : [
       {
         "activityIndex" : 1,
         "experienceIndex" : 1
       }
     ],
  },
  "mboxTrace" : true
}
```

In de volgende tabel worden de details van een verzoek op de server uitgelegd:

| Parameter | Type | Standaardwaarde | Beschrijving |
|--- |--- |--- |--- |
| token | Versleuteld token | Geen.<br> het kan niet leeg zijn. | Een gecodeerde entiteit die de lijst met activiteit-id&#39;s bevat die mogen worden uitgevoerd in activiteit-QA.<br> de regels van de Bevestiging: zou een gecodeerd teken moeten zijn dat tot de cliënt behoort die in het [!DNL Target] verzoek wordt gespecificeerd. Alle activiteiten die in het token worden opgegeven, moeten bij de client horen. |
| bypassEntryAudience | Boolean | Onwaar | Geeft aan of invoerstapdoelstellingen voor kwaliteitskwaliteitskwaliteitsbeoordelingen moeten worden geëvalueerd of dat deze als overeenkomend moeten worden beschouwd. |
| listActivityOnly | Boolean | Onwaar | Geeft aan of QA-activiteiten afzonderlijk moeten worden uitgevoerd of als ze moeten worden beoordeeld als actieve activiteiten voor de huidige omgeving. |
| evaluateAsTrueAudienceIds | Lijst met id&#39;s | Lege lijst. | Lijst met publiek-id&#39;s die altijd als true moeten worden beoordeeld in het bereik van de aanvraag [!DNL Target] . |
| evaluateAsFalseAudienceIds | Lijst met id&#39;s | Lege lijst. | Lijst met publiek-id&#39;s die altijd als onwaar moeten worden beschouwd in het bereik van de aanvraag [!DNL Target] . |
| activityIndex | Geheel | Null.<br> het kan niet leeg zijn. | Index van de activiteit in het gecodeerde token. Als activityIndex zich buiten de grenzen van de activiteit in het token bevindt of als deze null is, wordt deze genegeerd. Index begint met 1.<br> de regels van de Bevestiging: zou minstens één activiteitenindex moeten zijn, en zou een activiteit moeten van verwijzingen voorzien die in het teken wordt gespecificeerd. |
| experienceIndex | Geheel | Null. | Wanneer opgegeven, wordt een ervaring op index geselecteerd in de activiteitdefinitie. Als deze optie niet wordt opgegeven of buiten de grenzen valt, wordt de selectiestrategie van de activiteit hersteld. Index begint met 1 validatieregels: kan null zijn of moet verwijzen naar een ervaring in de activiteit. |
