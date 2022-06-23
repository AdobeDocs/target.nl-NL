---
keywords: registerExtension;registerextension;register extension;at.js;functies;function;clientCode;serverDomain;globalMboxName;globalMboxAutoCreate;timeout
description: Gebruik de registerExtension() functie voor de Adobe [!DNL Target] at.js JavaScript-bibliotheek om een specifieke extensie te registreren. (om 1.js)
title: Hoe gebruik ik de functie registerExtension()?
feature: at.js
role: Developer
exl-id: 7f0898b4-ddd5-425c-99dc-94f9b30f8ba7
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---

# registerExtension() - at.js 1.x

Verstrekt een standaardmanier om een specifieke uitbreiding te registreren.

>[!NOTE]
>
>Deze functie is beschikbaar voor at.js versies 1.*x* alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x.

De parameter options is verplicht en heeft de volgende structuur:

| Sleutel | Type | Vereist | Beschrijving |
|--- |--- |--- |--- |
| name | String | Ja | Naam van extensie. |
| modules | Array[String] | Ja | Een array van tekenreeksen die opgevraagde modulenamen vertegenwoordigen. |
| registreren | -functie | Ja | Een functie die wordt gebruikt om de extensie te initialiseren en samen te stellen. Deze functie ontvangt argumenten die op modules serie worden gebaseerd. |

Opmerkingen:

* Als een van de parameters niet wordt opgegeven, wordt een uitzondering gegenereerd.
* Als de array modules leeg is, wordt een uitzondering gegenereerd.

Voor meer informatie en voorbeelden van hoe te om te gebruiken `registerExtension`, zie de [Adobe Experience Cloud Target-objectextensies](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions) pagina op GitHub.

## Methoden van de module Instellingen {#section_8501CDD4B0624FA2B10532C98C5F4328}

| Sleutel | Type | Beschrijving |
|--- |--- |--- |
| clientCode | String | Clientcode |
| serverDomain | String | Edge-serverdomein |
| globalMboxName | String | Globale naam van naamvak activeren |
| globalMboxAutoCreate | Boolean | Geeft aan of automatisch maken is ingeschakeld |
| timeout | Getal | Verzoek om time-out |

## Methoden van de module Logger {#section_10AF62B49AEF48F981E950D26E176138}

| Sleutel | Type | Beschrijving |
|--- |--- |--- |
| log | -functie | Logs de veranderlijke lijst van argumenten aan de browser console, als het bestaat. Het wordt alleen geactiveerd wanneer `mboxDebug=true` wordt doorgegeven aan de URL. |
| fout | -functie | Logs de veranderlijke lijst van argumenten aan de browser console. Het wordt geactiveerd slechts wanneer er ernstige fouten zijn, zoals netwerkonderbreking, HTML knoop niet gevonden, enz. |
