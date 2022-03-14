---
keywords: gericht;AP rapporten;geautomatiseerde verpersoonlijkingsrapporten;auto-doel;auto doel;auto doelrapport;auto-doel rapport;verpersoonlijking;inzichten;geautomatiseerde segmenten;vk;vaak gestelde vragen;belangrijke attributen
description: Leer hoe te om de gespecialiseerde rapporten voor Automated Personalization (AP) en auto-Doel (AT) activiteiten - Geautomatiseerde Segmenten en Belangrijke Attributen te gebruiken.
title: Hoe gebruik ik de rapporten over persoonlijke voorkeuren?
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Persoonlijkheidsrapporten

Gebruikers van [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] (AT) activiteiten: de [!UICONTROL Automated Segments] en [!UICONTROL Important Attributes] rapporten.

>[!NOTE]
>
>Houd rekening met het volgende wanneer u rapporten over persoonlijke voorkeuren gebruikt:
>
>* AP- en AT-activiteiten zijn beschikbaar als onderdeel van de [!DNL Target Premium] oplossing. Ze zijn niet inbegrepen bij [!DNL Target Standard] zonder [!DNL Target Premium] licentie.
>
>* [!UICONTROL Personalization Insights] rapporten zijn beschikbaar slechts voor AP en bij activiteiten die een doel van de omzetoptimalisering gebruiken. Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.
>
>* [!UICONTROL Personalization Insights] rapporten zijn alleen beschikbaar als de [!UICONTROL Primary Goal] is geselecteerd in het dialoogvenster [!UICONTROL Report Metric] vervolgkeuzelijst.
>
>* [!UICONTROL Personalization Insights] de rapporten worden gesteund in [standaardomgeving](/help/main/administrating-target/hosts.md) alleen.
>
>* [!UICONTROL Personalization Insights] rapporten worden alleen gegenereerd voor activiteiten in het [!UICONTROL Live] en ten minste 15 dagen in werking zijn gesteld en verkeer ontvangen.


## Overzicht van de rapportage van persoonlijke inzichten {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Het doel van het [!UICONTROL Personalization Insights] de verslagen moeten meer informatie verstrekken over de wijze waarop [!UICONTROL Target] personalisatiemodellen achter uw AP en de activiteiten van AT personaliseren bezoekersverkeer. De [Random Forest-algoritme](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) is de basis voor de [!DNL Target] personalisatiemodellen.

Omdat het doel van het [!UICONTROL Personalization Insights] verslagen moeten begrijpen hoe [!DNL Target] personalisatiemodellen hebben besloten om de bezoeker naar welk(e) stuk(ken) inhoud te sturen, de [!UICONTROL Personalization Insights] de rapporten wijzen slechts op een subsegment van al verkeer dat door uw AP of activiteit wordt gediend. Specifiek, zijn de twee rapporten weerspiegelend van al verkeer dat het verpersoonlijkingsmodel gebruikte. Met andere woorden: [!UICONTROL Personalization Insights] de rapporten overwegen geen controleverkeer of verkeer dat door het algemene winnersmodel wordt gediend.

Twee [!UICONTROL Personalization Insights] er zijn rapporten beschikbaar :

| Rapport | Details |
|--- |--- |
| [!UICONTROL Automated Segments] | Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport toont hoe de verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen reageerden op de aanbiedingen/ervaringen in de activiteit. |
| [!UICONTROL Important Attributes] | In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden. |

## Kenmerken interpreteren in de functie Persoonlijke inzichten {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Er zijn twee typen kenmerken die worden vertegenwoordigd in [!UICONTROL Personalization Insights] rapporten die in uw AP of AutoDoelmodellen worden gebruikt:

* **Kenmerken die automatisch door Target worden verzameld:** [!DNL Target] gebruikt een reeks basisgegevens om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen die in de Inzichten van de Personalisatie worden weerspiegeld. Zie [Gegevensverzameling voor personaliseringsalgoritmen van het Doel](/help/main/c-activities/t-automated-personalization/ap-data.md) voor gegevenstypen, voorbeeldkenmerken en hun [!UICONTROL Personalization Insights] naamgevingsconventie. Hoewel deze kenmerken in overweging worden genomen, gebruiken de modellen van een individuele activiteit mogelijk niet al deze kenmerken in het uiteindelijke model.
* **Attributen doorgegeven aan Doel:** Zie [Gegevens uploaden voor de algoritmen van de Personalisatie van het Doel](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] biedt u veel manieren om aanvullende gegevens door te geven aan [!DNL Target] om de reeks basisgegevens te verrijken die wordt gebruikt om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen:

| Gegevenstype | Beschrijving | Naamgevingsconventie voor gegevenstypen |
|--- |--- |--- |
| Profielkenmerken, waaronder profielscripts, API voor profielupdate en kenmerken van paginabereik | Alle informatie die u hebt besloten op te nemen in het gebruikersprofiel van Target.<br>Deze informatie kan afkomstig zijn van profielscripts, informatie die is geüpload met de API voor profielupdate of in-mbox-profielparameters die vooraf zijn ingesteld op &quot;profiel&quot;. | `Custom - Profile - [parameter name]` |
| Paginaparameters (ook wel &quot;parameters mbox&quot; genoemd) | Naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik. | `Custom - Mbox Parameter - [parameter name]` |
| Klantkenmerken | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gedeeld publiek (Adobe Audience Manager of Adobe Analytics) | Soorten publiek gemaakt via Adobe Audience Manager of Adobe Analytics en gedeeld met Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Activiteitenrapportage publiek/segmenten | Soorten publiek gedefinieerd in uw AP- of Auto Target-activiteit tijdens installatie in &quot;Doelen &amp; Metriek.&quot; | `Custom - Reporting Segment - [segment name]` |

## Veelgestelde vragen

Lijst met veelgestelde vragen over [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] [!UICONTROL Insights] rapporten.

### Hoelang gegevens [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] modellen blijven bestaan?

[!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] de modellen worden getraind op de laatste 45 dagen van gebruikersgedrag (gebruikersprofielen, impotentiegebeurtenissen, en omzettingsgebeurtenissen) voor de activiteit.

[!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] de modellen bewaren gebruikersgedrag, trainingsverslagen, en modelbeslissingsgegevens voor 90 dagen om te produceren [!UICONTROL Insights] rapporten. Na 90 dagen worden trainingsgegevens en modelbeslissingen genegeerd. [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] de modellen bewaren voor rapportagedoeleinden ook gedurende twee jaar de geaggregeerde gegevens over ervaring/aanbod en de conversie. Deze gegevens zijn alleen gegevens op geaggregeerd niveau en bevatten geen profielgegevens op individueel niveau.

## Trainingsvideo: De rapporten met informatie over personalisatie gebruiken ![Zelfstudie-badge](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Zie voor meer informatie [De rapporten met persoonlijke informatie in Adobe Target gebruiken](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe-blogs

* Deel 1: [De Mystery uit de Magic of AI-Driven Personalization halen](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Deel 2: [Een blik achter het gordijn van AI voor Personalisatie in Adobe Target](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Deel 3: [MAGIX — The Solution to the Black Box Issue of AI-Driven Personalization](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
