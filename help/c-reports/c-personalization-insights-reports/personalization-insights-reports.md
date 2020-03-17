---
keywords: Targeting;AP reports;automated personalization reports;auto-target;auto target;auto target report;auto-target report;personalization;insights;automated segments;faq;frequently asked questions;important attributes
description: Twee gespecialiseerde rapporten zijn beschikbaar aan gebruikers van Geautomatiseerde Personalisatie (AP) en auto-Doel (AT) activiteiten de Geautomatiseerde Segmenten en de Belangrijke rapporten van Attributen.
title: Persoonlijkheidsrapporten
uuid: 2507a7a6-d229-412a-a992-5777b45c80e7
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# ![PREMIUM](/help/assets/premium.png) -rapporten over persoonlijke gegevens{#personalization-insights-reports}

Er zijn twee gespecialiseerde rapporten beschikbaar voor gebruikers van de activiteiten Automated Personalization (AP) en Auto-Target (AT): de Geautomatiseerde Segmenten en Belangrijke rapporten van Attributen.

>[!NOTE]
>
>AP en de activiteiten van AT zijn beschikbaar als deel van de [!DNL Target Premium] oplossing. Zij worden niet opgenomen bij [!DNL Target Standard] zonder een [!DNL Target Premium] vergunning.
>
>De rapporten van de Inzichten van de Personalisatie zijn beschikbaar slechts voor AP en bij activiteiten die een doel van de omzetoptimalisering gebruiken. Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.
>
>Personalisatie-inzichten worden alleen in de [standaardomgeving](../../administrating-target/hosts.md) ondersteund.
>
>Personalisatie-inzichten worden alleen gerapporteerd voor activiteiten die de status Live hebben en die gedurende ten minste 15 dagen zijn geactiveerd en verhandeld.

## Overzicht van de rapportage van persoonlijke inzichten {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Het doel van de [!UICONTROL Personalization Insights] rapporten is meer informatie te verstrekken over hoe de de verpersoonlijkingsmodellen van het Doel achter uw AP en van AT activiteiten bezoekersverkeer personaliseren. Het [Random Forest-algoritme](/help/c-activities/t-automated-personalization/algo-random-forest.md) is de basis voor de personalisatiemodellen van Target.

Omdat het doel van de rapporten van de Inzichten van de Personalisatie is te begrijpen hoe de verpersoonlijkingsmodellen van Target besloten hebben om welke bezoeker naar welk(e) stuk(ken) van inhoud te verzenden, weerspiegelen de rapporten van de Inzichten van de Personalisatie slechts een subsegment van al verkeer dat door uw AP of activiteit wordt gediend. Specifiek, zijn de twee rapporten weerspiegelend van al verkeer dat het verpersoonlijkingsmodel gebruikte. Met andere woorden, in de rapporten van de Inzichten van de Personalisatie wordt geen controle van verkeer of verkeer overwogen dat door het algemene windenergiemodel wordt gediend.

Er zijn twee rapporten over persoonlijke inzichten beschikbaar:

| Rapport | Details |
|--- |--- |
| Geautomatiseerde segmenten | Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de personalisatiemodellen van Target worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd. |
| Belangrijke kenmerken | In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden. |

## Kenmerken interpreteren in de functie Persoonlijke inzichten {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Er zijn twee soorten attributen die in rapporten worden vertegenwoordigd die in uw AP of Auto modellen van het Doel worden gebruikt: [!UICONTROL Personalization Insights]

* **Kenmerken die automatisch door Target worden verzameld:** Het doel gebruikt een reeks van basisgegevens om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen die in de Inzichten van de Personalisatie worden weerspiegeld. Zie de Inzameling van [Gegevens voor de Algoritmen](../../c-activities/t-automated-personalization/ap-data.md#reference_255BD3DE7AD04DC9B766E0BC78961058) van de Personalisering van het Doel voor gegevenstypes, voorbeeldattributen, en hun [!UICONTROL Personalization Insights] noemende overeenkomst. Hoewel deze kenmerken in overweging worden genomen, gebruiken de modellen van een individuele activiteit mogelijk niet al deze kenmerken in het uiteindelijke model.
* **Attributen doorgegeven aan Doel:** Zie Gegevens [uploaden voor de Algoritmen](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6)van de Aanpassing van het Doel.

Het doel verstrekt vele manieren voor u om in extra gegevens tot Doel over te gaan om de reeks van basisgegevens te verrijken die wordt gebruikt om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen:

| Gegevenstype | Beschrijving | Naamgevingsconventie voor gegevenstypen |
|--- |--- |--- |
| Profielkenmerken, waaronder profielscripts, API voor profielupdate en kenmerken van paginabereik | Alle informatie die u hebt besloten op te nemen in het gebruikersprofiel van Target.<br>Deze informatie kan afkomstig zijn van profielscripts, informatie die is geüpload met de API voor profielupdate of in-mbox-profielparameters die vooraf zijn ingesteld op &quot;profile&quot;. | `Custom - Profile - [parameter name]` |
| Paginaparameters (ook wel &quot;parameters mbox&quot; genoemd) | Naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik. | `Custom - Mbox Parameter - [parameter name]` |
| Klantkenmerken | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gedeeld publiek (Adobe Audience Manager of Adobe Analytics) | Soorten publiek gemaakt via Adobe Audience Manager of Adobe Analytics en gedeeld met Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Activiteitenrapportage publiek/segmenten | Soorten publiek gedefinieerd in uw AP- of Auto Target-activiteit tijdens installatie in &quot;Doelen &amp; Metriek.&quot; | `Custom - Reporting Segment - [segment name]` |

## Trainingsvideo: De ![zelfstudie met de rapporten Persoonlijke inzichten gebruiken](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Zie [De rapporten met inzichten van persoonlijke instellingen gebruiken in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html)voor meer informatie.

## Adobe-blogs

* Deel 1: De [mysterie weghalen uit de Magic of AI-Driven Personalization](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Deel 2: Een blik achter het gordijn van AI voor Personalisatie in Adobe Target [](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Deel 3: [MAGIX — The Solution to the Black Box Issue of AI-Driven Personalization](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
