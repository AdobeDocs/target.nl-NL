---
keywords: Targeting;AP reports;automated personalization reports;auto-target;auto target;auto target report;auto-target report;personalization;insights;automated segments;faq;frequently asked questions;important attributes
description: Er zijn twee gespecialiseerde rapporten beschikbaar voor gebruikers van Automated Personalization (AP)- en Auto-Target (AT)-activiteiten in de rapporten Geautomatiseerde segmenten en Belangrijke kenmerken.
title: Persoonlijkheidsrapporten
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) -rapporten over persoonlijke gegevens{#personalization-insights-reports}

Er zijn twee gespecialiseerde rapporten beschikbaar voor gebruikers van [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] (AT)-activiteiten: de [!UICONTROL Automated Segments] en de [!UICONTROL Important Attributes] verslagen.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u rapporten over persoonlijke voorkeuren gebruikt:
>
>* AP en de activiteiten van AT zijn beschikbaar als deel van de [!DNL Target Premium] oplossing. Zij worden niet opgenomen bij [!DNL Target Standard] zonder een [!DNL Target Premium] vergunning.
   >
   >
* [!UICONTROL Personalization Insights] rapporten zijn beschikbaar slechts voor AP en bij activiteiten die een doel van de omzetoptimalisering gebruiken. Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.
   >
   >
* [!UICONTROL Personalization Insights] rapporten zijn alleen beschikbaar als de optie [!UICONTROL Primary Goal] is geselecteerd in de [!UICONTROL Report Metric] vervolgkeuzelijst.
   >
   >
* [!UICONTROL Personalization Insights] rapporten worden alleen ondersteund in de [standaardomgeving](/help/administrating-target/hosts.md) .
   >
   >
* [!UICONTROL Personalization Insights] rapporten worden alleen gegenereerd voor activiteiten die zich in de [!UICONTROL Live] status bevinden en die gedurende ten minste 15 dagen zijn geactiveerd en ontvangen.


## Overzicht van de rapportage van persoonlijke inzichten {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Het doel van de [!UICONTROL Personalization Insights] rapporten is meer informatie te verstrekken over hoe de [!UICONTROL Target] verpersoonlijkingsmodellen achter uw AP en de activiteiten van AT bezoekersverkeer verpersoonlijken. Het algoritme [Willekeurig bos is de basis voor de](/help/c-activities/t-automated-personalization/algo-random-forest.md) [!DNL Target] verpersoonlijkingsmodellen.

Omdat het doel van de [!UICONTROL Personalization Insights] rapporten is te begrijpen hoe de [!DNL Target] personalisatiemodellen besloten om te verzenden welke bezoeker naar welk(e) stuk(ken) van inhoud, de [!UICONTROL Personalization Insights] rapporten slechts op een subsegment van al verkeer wijzen dat door uw AP of activiteit wordt gediend. Specifiek, zijn de twee rapporten weerspiegelend van al verkeer dat het verpersoonlijkingsmodel gebruikte. Met andere woorden, [!UICONTROL Personalization Insights] de rapporten houden geen rekening met controleverkeer of verkeer dat door het algemene winnersmodel wordt gediend.

Er zijn twee [!UICONTROL Personalization Insights] rapporten beschikbaar:

| Rapport | Details |
|--- |--- |
| [!UICONTROL Automated Segments] | Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport toont hoe de verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden bepaald op de aanbiedingen/ervaringen in de activiteit reageerden. |
| [!UICONTROL Important Attributes] | In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden. |

## Kenmerken interpreteren in de functie Persoonlijke inzichten {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Er zijn twee soorten attributen die in rapporten worden vertegenwoordigd die in uw AP of Auto modellen van het Doel worden gebruikt: [!UICONTROL Personalization Insights]

* **Kenmerken die automatisch door Target worden verzameld:** [!DNL Target] gebruikt een reeks basisgegevens om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen die in de Inzichten van de Personalisatie worden weerspiegeld. Zie de Inzameling van [Gegevens voor de Algoritmen](/help/c-activities/t-automated-personalization/ap-data.md) van de Personalisering van het Doel voor gegevenstypes, voorbeeldattributen, en hun [!UICONTROL Personalization Insights] noemende overeenkomst. Hoewel deze kenmerken in overweging worden genomen, gebruiken de modellen van een individuele activiteit mogelijk niet al deze kenmerken in het uiteindelijke model.
* **Attributen doorgegeven aan Doel:** Zie Gegevens [uploaden voor de Algoritmen](/help/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md)van de Aanpassing van het Doel.

[!DNL Target] verstrekt vele manieren voor u om in extra gegevens over te gaan om de reeks van basisgegevens [!DNL Target] te verrijken die wordt gebruikt om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen:

| Gegevenstype | Beschrijving | Naamgevingsconventie voor gegevenstypen |
|--- |--- |--- |
| Profielkenmerken, waaronder profielscripts, API voor profielupdate en kenmerken van paginabereik | Alle informatie die u hebt besloten op te nemen in het gebruikersprofiel van Target.<br>Deze informatie kan afkomstig zijn van profielscripts, informatie die is geüpload met de API voor profielupdate of in-mbox-profielparameters die vooraf zijn ingesteld op &quot;profile&quot;. | `Custom - Profile - [parameter name]` |
| Paginaparameters (ook wel &quot;parameters mbox&quot; genoemd) | Naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik. | `Custom - Mbox Parameter - [parameter name]` |
| Klantkenmerken | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gedeeld publiek (Adobe Audience Manager of Adobe Analytics) | Soorten publiek gemaakt via Adobe Audience Manager of Adobe Analytics en gedeeld met Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Activiteitenrapportage publiek/segmenten | Soorten publiek gedefinieerd in uw AP- of Auto Target-activiteit tijdens installatie in &quot;Doelen &amp; Metriek.&quot; | `Custom - Reporting Segment - [segment name]` |

## Trainingsvideo: De ![zelfstudie met de rapporten Persoonlijke inzichten gebruiken](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Voor meer informatie, zie het [Gebruiken van de Rapporten van de Inzichten van de Personalisatie in Adobe Target](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe-blogs

* Deel 1: [De Mystery uit de Magic of AI-Driven Personalization halen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Deel 2: [Een blik achter het gordijn van AI voor Personalisatie in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Deel 3: [MAGIX — The Solution to the Black Box Issue of AI-Driven Personalization](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
