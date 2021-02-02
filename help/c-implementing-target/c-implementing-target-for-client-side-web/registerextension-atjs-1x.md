---
keywords: registerExtension;registerextension;register extension;at.js;functies;function;clientCode;serverDomain;globalMboxName;globalMboxAutoCreate;timeout
description: Informatie over de functie registerExtension() voor de Adobe Target at.js JavaScript-bibliotheek.
title: Registerextension() - at.js 1.x
feature: at.js
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 1%

---


# registerExtension() - at.js 1.x

Verstrekt een standaardmanier om een specifieke uitbreiding te registreren.

>[!NOTE]
>
>Deze functie is beschikbaar voor at.js versies 1.** Alleen. Deze functie is vervangen door de release van at.js 2.x. Deze functie retourneert standaardinhoud als deze wordt gebruikt met at.js 2.x.

De parameter options is verplicht en heeft de volgende structuur:

| Sleutel | Type | Vereist | Beschrijving |
|--- |--- |--- |--- |
| name | String | Ja | Naam van extensie. |
| modules | Array[String] | Ja | Een array van tekenreeksen die opgevraagde modulenamen vertegenwoordigen. |
| registreren | -functie | Ja | Een functie die wordt gebruikt om de extensie te initialiseren en samen te stellen. Deze functie ontvangt argumenten die op modules serie worden gebaseerd. |

Opmerkingen:

* Als een van de parameters niet wordt opgegeven, wordt een uitzondering gegenereerd.
* Als de array modules leeg is, wordt een uitzondering gegenereerd.

Voor meer informatie en voorbeelden van hoe te om `registerExtension` te gebruiken, zie [Adobe Experience Cloud het Doelen van de Doelen Extensions](https://github.com/Adobe-Marketing-Cloud/target-atjs-extensions) pagina op GitHub.

## Methoden van de module Settings {#section_8501CDD4B0624FA2B10532C98C5F4328}

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
| log | -functie | Logs de veranderlijke lijst van argumenten aan de browser console, als het bestaat. Deze wordt alleen geactiveerd wanneer `mboxDebug=true` wordt doorgegeven aan de URL. |
| fout | -functie | Logs de veranderlijke lijst van argumenten aan de browser console. Deze wordt alleen geactiveerd wanneer er ernstige fouten zijn, zoals time-out van netwerk, niet gevonden HTML-knooppunt, enzovoort. |
