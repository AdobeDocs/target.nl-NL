---
keywords: faq;vaak gestelde vragen;analyses voor doel;a4T;metrisch;metrische definities
description: Vind antwoorden op vragen over metrische definities en het gebruiken van Analytics voor [!DNL Target] (A4T). Met A4T kunt u Analyses melden met Adobe [!DNL Target] activiteiten.
title: Waar kan ik informatie over metrische definities met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 97442622-ba6d-46f8-bfac-72638875d889
source-git-commit: aff96eca1380f4274dba0c1567f6e41d42f4b5ab
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---

# Metrische definities - Veelgestelde vragen A4T

Dit onderwerp bevat antwoorden op vragen die vaak over metrische definities en het gebruiken worden gevraagd [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T).

## Wat is de vervaldatum voor het lidmaatschap van activiteiten? Hoe lang nadat bezoekers de activiteit betreden worden hun acties geteld in de activiteit als zij het niet meer zien? {#section_41B4958F33534E4B96DEE0C981227A79}

++ Antwoord De standaardvervaldatum voor de activiteit is 90 dagen na de laatste interactie van een bezoeker met de activiteit. Deze instelling kan indien nodig door ClientCare worden aangepast. Deze instelling is echter algemeen voor alle activiteiten, zodat ze niet voor één geval hoeft te worden aangepast.

+++

## Waarom heb ik tijdens het configureren van mijn doelmeetgegevens geen toegang tot de opties voor Geavanceerde instellingen? {#adv-settings}

++ beantwoord [!UICONTROL Advanced Settings] opties zijn niet beschikbaar voor activiteiten die [!DNL Analytics] als bron van rapportage (A4T).

Voor activiteiten die A4T gebruiken, het doel metrisch gebruikt altijd &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; en &quot;[!UICONTROL On Every Impression]&quot;. Deze instellingen zijn *niet* configureerbaar.

Voor niet-A4T-activiteiten kunt u de opdracht [Geavanceerde opties voor instellingen](/help/main/c-activities/r-success-metrics/success-metrics.md#section_7CE95A2FA8F5438E936C365A6D43BC5B) om te beheren hoe u succes meet. De opties omvatten het toevoegen van gebiedsdelen, het kiezen of om de gebruiker in de activiteit te houden of hen te verwijderen, en of om metrisch één keer per ingang of op elke indruk te tellen. U opent de [!UICONTROL Advanced Settings] opties in een niet-A4T activiteit door de verticale ellips te klikken > [!UICONTROL Advanced Settings], zoals hieronder weergegeven:

![Geavanceerde instellingen](/help/main/c-activities/r-success-metrics/assets/advanced-settings.png)

+++

## Wat worden berekende metriek en hoe vervangen zij SiteCatalyst:Gebeurtenis mbox ik gebruikte om te gebruiken? {#section_D59F4719E6B94758A2187427C17F8EF3}

+++Antwoord Berekende metriek laten u douanemetriek tot stand brengen die uit segmenten of wiskundige berekeningen worden afgeleid. In het verleden, wanneer u zou kunnen gebruiken `SiteCatlayst:Event` mbox waarbij `evar27=shoes` en de gebeurtenis `purchase`Nu maakt u een segment waarin `evar27=shoes` en maak vervolgens een berekende metrische waarde waar de gebeurtenis plaatsvindt `purchase` waarop het segment is toegepast. Deze metriek kan op elk ogenblik worden gecreeerd, zelfs nadat de activiteit lopend is. Deze kunnen vervolgens voor elk rapport in Analytics worden gebruikt.

+++

## Worden A4T-kenmerken omgezet in meerdere campagnes? {#section_7F15C727206440CD86B3A8CE77087DF9}

++ Antwoord ja, gebruikend het &quot;Volledige plaatsen van de Toewijzing&quot;.

+++