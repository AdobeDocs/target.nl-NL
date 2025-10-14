---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;metrisch;metrische definities
description: Vind antwoorden aan vragen over metrische definities en het gebruiken van Analytics voor  [!DNL Target]  (A4T). A4T laat u Analytics gebruiken die met Adobe  [!DNL Target]  activiteiten melden.
title: Waar kan ik informatie over metrische definities met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Metrische definities - Veelgestelde vragen A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over metrische definities en [!DNL Adobe Analytics] als rapporteringsbron voor [!DNL Adobe Target] (A4T) gebruiken.

## Wat is de vervaldatum voor het lidmaatschap van activiteiten? Hoe lang nadat bezoekers de activiteit betreden worden hun acties geteld in de activiteit als zij het niet meer zien? {#section_41B4958F33534E4B96DEE0C981227A79}

+++Antwoord
De standaardvervaldatum voor de activiteit is 90 dagen na de laatste interactie van een bezoeker met de activiteit. Deze instelling kan indien nodig door ClientCare worden aangepast. Deze instelling is echter algemeen voor alle activiteiten, zodat ze niet voor één geval hoeft te worden aangepast.

+++

## Waarom heb ik tijdens het configureren van mijn doelmeetgegevens geen toegang tot de opties voor Geavanceerde instellingen? {#adv-settings}

+++Antwoord
De [!UICONTROL Advanced Settings] -opties zijn niet beschikbaar voor activiteiten die [!DNL Analytics] als rapportagebron (A4T) gebruiken.

Voor activiteiten die A4T gebruiken, het doel metrisch gebruikt altijd &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages. Deze montages zijn *niet* configureerbaar.

Voor activiteiten niet-A4T, kunt u de [&#x200B; Geavanceerde opties van Montages &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) gebruiken om te beheren hoe u succes meet. De opties omvatten het toevoegen van gebiedsdelen, het kiezen of om de gebruiker in de activiteit te houden of hen te verwijderen, en of om metrisch één keer per ingang of op elke indruk te tellen. U opent de opties voor [!UICONTROL Advanced Settings] in een niet-A4T-activiteit door op de verticale ellipsen > [!UICONTROL Advanced Settings] te klikken, zoals hieronder wordt weergegeven:

![&#x200B; Geavanceerde Montages &#x200B;](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## Wat zijn berekende metriek en hoe vervangen zij SiteCatalyst :Event mbox ik gebruikte om te gebruiken? {#section_D59F4719E6B94758A2187427C17F8EF3}

+++Antwoord
Met berekende metriek kunt u aangepaste metriek maken die is afgeleid van segmenten of wiskundige berekeningen. In het verleden, wanneer u de `SiteCatlayst:Event` mbox waar `evar27=shoes` en de gebeurtenis `purchase` zou kunnen gebruiken, zou u nu een segment creëren waar `evar27=shoes` en dan berekende metrisch waar de gebeurtenis `purchase` met het toegepaste segment is. Deze metriek kan op elk ogenblik worden gecreeerd, zelfs nadat de activiteit aan de gang is. Deze kunnen vervolgens voor elk rapport in Analytics worden gebruikt.

+++

## Worden A4T-kenmerken omgezet in meerdere campagnes? {#section_7F15C727206440CD86B3A8CE77087DF9}

+++Antwoord
Ja, met de instelling Volledige toewijzing.

+++
