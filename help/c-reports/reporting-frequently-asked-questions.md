---
keywords: troubleshooting;metric discrepancies;FAQ;reports
description: Lijst met veelgestelde vragen over rapportage in Adobe Target.
title: Veelgestelde vragen over rapportage voor Adobe Target
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Veelgestelde vragen over rapportage{#reporting-faq}

Lijst met veelgestelde vragen over rapportage in [!DNL Target].

## Waarom bevatten mijn [!UICONTROL Experience Targeting] (XT) rapporten metriek voor controleervaringen?

XT-activiteiten moeten altijd een beheerervaring hebben. Als u een activiteit XT op een gelijkaardige manier aan een [!UICONTROL A/B Test] activiteit gebruikt, die een vrij algemeen scenario is, zijn de gegevens van de controleervaring nuttig. U kunt de gegevens van de controleervaring negeren als u het niet nuttig in uw rapporten vindt.

## Waarom is het aantal bezoeken lager in [!DNL Target] dan in andere [!DNL Adobe Experience Cloud] oplossingen? {#section_7E626FDB417E41B8B58BBF30FB207409}

De metrische aantallen, bijvoorbeeld bezoeken, door [!DNL Target] zullen altijd lager zijn dan de gemelde aantallen in andere [!DNL Experience Cloud] oplossingen om een aantal redenen:

* [!DNL Target] telt alleen bezoeken voor bezoekers die voor de activiteit in aanmerking kwamen. Andere oplossingen tellen bezoeken voor bezoekers die de pagina tonen, ongeacht welke activiteit hen aan de pagina bracht.
* Er kunnen situaties zijn waarin verschillende activiteiten op dezelfde locatie concurreren (wederzijds exclusief). Dit heeft tot gevolg dat bezoekers verschillende inhoud op een webpagina zien die van invloed is op de metrische nummers die door [!DNL Target]worden gerapporteerd.

## Waarom zijn er geen gegevens beschikbaar voor mijn activiteitenverslag? {#section_E4722F6445884130951DF79981C8289B}

Als de inhoud van een activiteit met succes aan gebruikers werd geleverd maar zijn rapport bevat geen gegevens, zorg ervoor dat u het correcte milieu ([gastheergroep](/help/administrating-target/hosts.md)) hebt die in de montages van het rapport wordt geselecteerd.

Als u een ontwikkelomgeving hebt geselecteerd, wordt mogelijk het volgende foutbericht weergegeven: &quot;Er zijn geen gegevens beschikbaar voor de geselecteerde rapportinstellingen.&quot;

Om het milieu voor het rapport van een activiteit te veranderen:

1. Klik **[!UICONTROL Activities]**, klik de gewenste activiteit van de lijst, dan klik de **[!UICONTROL Reports]** tabel.
1. Klik op het tandwielpictogram om de rapportinstellingen te configureren.

   ![A/B-instellingen, dialoogvenster](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >Het tandwielpictogram is niet beschikbaar voor [!UICONTROL Automated Personalization] (AP)-rapporten.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Environment]** de optie **[!UICONTROL Production]**.

   Rapportgegevens zijn mogelijk niet beschikbaar als u een ontwikkelomgeving hebt geselecteerd.

1. Klik op **[!UICONTROL Save]**.

Zie [Gastheren](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)voor meer informatie over omgevingen.
