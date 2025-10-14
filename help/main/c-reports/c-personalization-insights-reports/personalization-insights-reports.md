---
keywords: gericht;AP rapporten;geautomatiseerde verpersoonlijkingsrapporten;auto-doel;auto doel;auto doelrapport;auto-doel rapport;verpersoonlijking;inzichten;geautomatiseerde segmenten;vk;vaak gestelde vragen;belangrijke attributen
description: Leer hoe te om de gespecialiseerde rapporten voor Automated Personalization (AP) en auto-Doel (AT) activiteiten - Geautomatiseerde Segmenten en Belangrijke Attributen te gebruiken.
title: Hoe gebruik ik de Personalization Insights-rapporten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Reports
exl-id: 89295d95-f179-4277-ae63-453350e1bba8
source-git-commit: 6c8f042acb257fc908349c679bf745e477f94af4
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# [!UICONTROL Personalization Insights] rapporten

Er zijn twee gespecialiseerde rapporten beschikbaar voor gebruikers van [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] (AT)-activiteiten: de [!UICONTROL Automated Segments] - en [!UICONTROL Important Attributes] -rapporten.

## Overwegingen

Houd rekening met het volgende wanneer u [!UICONTROL Personalization Insights] -rapporten gebruikt:

* AP en de activiteiten van AT zijn beschikbaar als deel van de [[!DNL Target Premium]  oplossing &#x200B;](/help/main/c-intro/intro.md#premium). Ze worden niet zonder [!DNL Target Standard] -licentie opgenomen in [!DNL Target Premium] .

* [!UICONTROL Personalization Insights] -rapporten zijn alleen beschikbaar voor AP- en AT-activiteiten die als volgt zijn geconfigureerd:

   * [!DNL Target] reporting > [!UICONTROL Conversion]

     Bijvoorbeeld:

     ![&#x200B; het Rapport van het Doel > Omzetting &#x200B;](/help/main/c-reports/assets/conversion.png)

   * [!DNL Analytics] reporting > [!DNL Conversion]

     Bijvoorbeeld:

     ![&#x200B; Analytische Rapportering > Omzetting &#x200B;](/help/main/c-reports/assets/analytics-reporting-conversion.png)

   * [!DNL Analytics] reporting > [!UICONTROL Use an Analytics metric] > [!UICONTROL Maximize Visit Conversion Rate]

     Bijvoorbeeld:

     ![&#x200B; gebruik metrische Analytics > Maximize het Tarief van de Omzetting van het Bezoek &#x200B;](/help/main/c-reports/assets/maximize-visit-conversion-rate.png)

* Activiteiten waarbij de optimalisatiedoelstelling werd gewijzigd in een omrekening van inkomsten nadat de activiteit al actief was, worden ook niet ondersteund.

* [!UICONTROL Personalization Insights] -rapporten zijn alleen beschikbaar als [!UICONTROL Primary Goal] is geselecteerd in de vervolgkeuzelijst [!UICONTROL Report Metric] .

* [!UICONTROL Personalization Insights] de rapporten worden gesteund in het [&#x200B; standaardmilieu &#x200B;](/help/main/administrating-target/hosts.md) slechts.

* [!UICONTROL Personalization Insights] -rapporten worden alleen gegenereerd voor activiteiten die de status [!UICONTROL Live] hebben en die gedurende ten minste 15 dagen zijn geactiveerd en verzonden.

## Overzicht Personalization Insights Reporting {#section_B47CD4A50FEB43D587F9FACD9FFD6D9D}

Het doel van de [!UICONTROL Personalization Insights] rapporten is meer informatie te verstrekken over hoe de [!UICONTROL Target] verpersoonlijkingsmodellen achter uw AP en de activiteiten van AT bezoekersverkeer verpersoonlijken. Het [&#x200B; Willekeurige Bosalgoritme &#x200B;](/help/main/c-activities/t-automated-personalization/algo-random-forest.md) is de basis voor de [!DNL Target] verpersoonlijkingsmodellen.

Omdat het doel van de [!UICONTROL Personalization Insights] -rapporten is te begrijpen hoe de [!DNL Target] personalisatiemodellen hebben besloten om de bezoeker naar welk(e) stuk(ken) inhoud te sturen, weerspiegelen de [!UICONTROL Personalization Insights] -rapporten slechts een subsegment van alle verkeer dat door uw AP of AT-activiteit wordt bediend. Specifiek, zijn de twee rapporten weerspiegelend van al verkeer dat het verpersoonlijkingsmodel gebruikte. Met andere woorden, in [!UICONTROL Personalization Insights] -rapporten wordt geen rekening gehouden met het beheer van het verkeer of het verkeer dat wordt bediend door het algemene winnersmodel.

Er zijn twee [!UICONTROL Personalization Insights] -rapporten beschikbaar:

| Rapport | Details |
|--- |--- |
| [!UICONTROL Automated Segments] | Verschillende bezoekers reageren anders op de aanbiedingen/ervaringen in uw AP/AT-activiteit. Dit rapport laat zien hoe verschillende geautomatiseerde segmenten die door de [!DNL Target] personalisatiemodellen worden gedefinieerd, op de aanbiedingen/ervaringen in de activiteit hebben gereageerd. |
| [!UICONTROL Important Attributes] | In verschillende activiteiten zijn verschillende kenmerken meer of minder belangrijk voor de manier waarop het model beslist om zich aan te passen. Dit rapport toont de belangrijkste kenmerken die het model en hun relatieve belang beïnvloedden. |

## Kenmerken interpreteren in Personalization Insights {#section_B5C45E723EC941BDA2A7A642EEB30E4D}

Er zijn twee typen kenmerken in [!UICONTROL Personalization Insights] -rapporten die worden gebruikt in uw AP- of Auto Target-modellen:

* **Attributen die automatisch door Doel worden verzameld:** [!DNL Target] gebruikt een reeks van basisgegevens om zijn verpersoonlijkingsalgoritmen in AP en bij activiteiten te bouwen die in de Inzichten van Personalization worden weerspiegeld. Zie [&#x200B; Inzameling van Gegevens voor de Algoritmen van Personalization van het Doel &#x200B;](/help/main/c-activities/t-automated-personalization/ap-data.md) voor gegevenstypes, voorbeeldattributen, en hun [!UICONTROL Personalization Insights] noemende overeenkomst. Hoewel deze kenmerken in overweging worden genomen, gebruiken de modellen van een individuele activiteit mogelijk niet al deze kenmerken in het uiteindelijke model.
* **Attributen die tot Doel worden overgegaan:** zie [&#x200B; Uploadend Gegevens voor de Algoritmen van Personalization van het Doel &#x200B;](/help/main/c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md).

[!DNL Target] biedt verschillende manieren waarop u aanvullende gegevens aan [!DNL Target] kunt doorgeven om de set met basisgegevens die wordt gebruikt voor het maken van de aanpassingsalgoritmen van de gegevensset in AP- en AT-activiteiten te verrijken:

| Gegevenstype | Beschrijving | Naamgevingsconventie voor gegevenstypen |
|--- |--- |--- |
| Profielkenmerken, waaronder profielscripts, API voor profielupdate en kenmerken van paginabereik | Alle informatie die u hebt besloten op te nemen in het gebruikersprofiel van Target.<br> deze informatie kon uit profielmanuscripten, informatie komen die gebruikend de Update API van het Profiel, of in-mbox profielparameters vooraf bepaald met &quot;profiel wordt geupload.&quot; | `Custom - Profile - [parameter name]` |
| Paginaparameters (ook wel &quot;parameters mbox&quot; genoemd) | Naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik. | `Custom - Mbox Parameter - [parameter name]` |
| Klantkenmerken | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target. | `Custom - Customer Attributes - [parameter name]` |
| Gedeeld publiek (Adobe Audience Manager of Adobe Analytics) | Soorten publiek gemaakt via Adobe Audience Manager of Adobe Analytics en gedeeld met Target. | `Custom - Experience Cloud Segment - [segment name]` |
| Gedeeld publiek (Adobe Experience Platform/Real-Time CDP) | Publiek dat door Adobe Experience Platform/Real-time CDP wordt gecreeerd en met Doel via Doelen wordt gedeeld. | `Custom - Adobe Experience Platform Segment - [segment name]` |
| Gedeelde kenmerken (Adobe Experience Platform/Real-Time CDP) | Attributen die door Adobe Experience Platform/Real-Time CDP worden gecreeerd en met Doel via Doelen worden gedeeld. Deze functie is momenteel in Beta. | `Custom - Adobe Experience Platform Attribute - [attribute name]]` |
| Activiteitenrapportage publiek/segmenten | Soorten publiek gedefinieerd in uw AP- of Auto Target-activiteit tijdens installatie in &quot;Doelen &amp; Metriek.&quot; | `Custom - Reporting Segment - [segment name]` |

## Veelgestelde vragen

Lijst met veelgestelde vragen over [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] [!UICONTROL Insights] -rapporten.

### Hoe lang blijven de gegevens voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] modellen behouden?

[!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] -modellen worden getraind op de laatste 45 dagen van het gebruikersgedrag (gebruikersprofielen, impliciete gebeurtenissen en conversiegebeurtenissen) voor de activiteit.

[!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] -modellen behouden het gebruikersgedrag, de trainingsrecords en de modelbeslissingsgegevens gedurende 90 dagen om [!UICONTROL Insights] -rapporten te produceren. Na 90 dagen worden trainingsgegevens en modelbeslissingen genegeerd. [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Auto-Target] -modellen behouden voor rapportagedoeleinden ook gedurende twee jaar samengevoegde gegevens over ervaring/aanbod en conversie. Deze gegevens zijn alleen gegevens op geaggregeerd niveau en bevatten geen profielgegevens op individueel niveau.

## De video van de opleiding: Het gebruiken van de rapporten van de Inzichten van Personalization ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/25601/)

Voor meer informatie, zie [&#x200B; Gebruikend de Rapporten van de Inzichten van Personalization in Adobe Target &#x200B;](https://helpx.adobe.com/target/kt/using/personalization-insights-report-feature-video-use.html).

## Adobe-blogs

* Deel 1: [&#x200B; Gebruikend het Mysterie uit Magisch van AI-Gedreven Personalization &#x200B;](https://theblog.adobe.com/taking-mystery-magic-ai-driven-personalization-part-1/)
* Deel 2: [&#x200B; Een blik achter het Gordijn van AI voor Personalization in Adobe Target &#x200B;](https://theblog.adobe.com/a-peek-behind-the-curtain-of-ai-for-personalization-in-adobe-target/)
* Deel 3: [&#x200B; MAGIX — de Oplossing aan de Zwarte Doos Uitgave van AI-Gedreven Personalization &#x200B;](https://theblog.adobe.com/magix-the-solution-to-the-black-box-issue-of-ai-driven-personalization/)
