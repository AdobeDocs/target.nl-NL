---
keywords: qa;server side;server-side;preview;preview links
description: Gebruik Adobe Target QA URLs met server-zijlevering om gemakkelijke activiteit QA met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.
title: Activiteit QA met levering aan de serverzijde gebruiken
feature: Activities
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# Activiteit QA gebruiken met levering aan de serverzijde{#use-activity-qa-with-server-side-delivery}

Gebruik QA URLs met server-zijlevering om gemakkelijke activiteit QA met voorproefverbindingen uit te voeren die nooit veranderen, facultatieve publiek richten, en QA rapportering die van levende activiteitengegevens gesegmenteerd blijft.

De standaardimplementatie van Activiteit QA steunt het overgaan van `qa_mode` parameters via `pageUrl` parameters. Deze benadering is geschikt voor standaard/ajax [!DNL Target] vraag. Voor server-naar-server aanroepen is dit echter niet de beste aanpak voor een geval van Mobile SDK als `pageUrl` niet beschikbaar is.

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
| token | Versleuteld token | Geen.<br>Het mag niet leeg zijn. | Een gecodeerde entiteit die de lijst met activiteit-id&#39;s bevat die mogen worden uitgevoerd in activiteit QA.<br>Validatieregels: Dit moet een gecodeerde token zijn die hoort bij de client die in de  [!DNL Target] aanvraag is opgegeven. Alle activiteiten die in het token worden opgegeven, moeten bij de client horen. |
| bypassEntryAudience | Boolean | Onwaar | Geeft aan of invoerstapdoelstellingen voor kwaliteitskwaliteitskwaliteitsbeoordelingen moeten worden geëvalueerd of dat deze als overeenkomend moeten worden beschouwd. |
| listActivityOnly | Boolean | Onwaar | Geeft aan of QA-activiteiten afzonderlijk moeten worden uitgevoerd of als ze moeten worden beoordeeld als actieve activiteiten voor de huidige omgeving. |
| evaluateAsTrueAudienceIds | Lijst met id&#39;s | Lege lijst. | Lijst van publiek IDs die altijd als waar in het werkingsgebied van [!DNL Target] verzoek zou moeten worden geëvalueerd. |
| evaluateAsFalseAudienceIds | Lijst met id&#39;s | Lege lijst. | Lijst van publiek IDs die altijd als vals in het werkingsgebied van [!DNL Target] verzoek zou moeten worden geëvalueerd. |
| activityIndex | Geheel | Null.<br>Het mag niet leeg zijn. | Index van de activiteit in het gecodeerde token. Als activityIndex zich buiten de grenzen van de activiteit in het token bevindt of als deze null is, wordt deze genegeerd. Index begint met 1.<br>Validatieregels: Moet ten minste één activiteitenindex zijn en moet verwijzen naar een activiteit die in de token is opgegeven. |
| experienceIndex | Geheel | Null. | Wanneer opgegeven, wordt een ervaring op index geselecteerd in de activiteitdefinitie. Als deze optie niet wordt opgegeven of buiten de grenzen valt, wordt de selectiestrategie van de activiteit hersteld. Index begint met 1 validatieregels: Kan null zijn of moet verwijzen naar een ervaring in de activiteit. |