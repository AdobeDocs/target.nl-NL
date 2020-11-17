---
keywords: faq;frequently asked questions;analytics for target;a4T;activity setup
description: Dit onderwerp bevat antwoorden op vragen die vaak over activiteitenopstelling en het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.
title: Activiteitsinstellingen - Veelgestelde vragen voor A4T
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: 208196b8c0cf11367ad37121c4792a015b396dc7
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Activiteitsinstellingen - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak over activiteitenopstelling en het gebruiken [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T) worden gevraagd.

## Welke activiteitstypes steunen Analytics als rapporteringsbron (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Voor een volledige lijst, zie &quot;Gesteunde Types van Activiteit&quot;in [Adobe Analytics als Rapporterende Bron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Ik heb net een activiteit gecreëerd. Waarom zie ik geen gegevens binnenkomen? {#section_9F8092BE4225442896F926540292F221}

Wanneer een activiteit wordt gecreeerd, [!DNL Target] verzendt een classificatiedossier naar [!DNL Analytics]. Hoewel de gegevens worden vastgelegd en verwerkt, worden deze pas in de rapporten weergegeven als het classificatiebestand is bijgewerkt. [!DNL Analytics] Dit kan tot 24 uur duren. Als u na 48 uur uw gegevens niet ziet, neemt u [contact op met de klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C). Als u weet dat u een activiteit start, kunt u de activiteit een paar dagen van tevoren maken en de classificaties worden verzonden wanneer de activiteit wordt opgeslagen. Op die manier worden gegevens weergegeven in de rapporten wanneer deze worden gestart. Houd er rekening mee dat het 45 tot 90 minuten duurt voordat gegevens worden verwerkt in [!DNL Analytics].

## Waarom kan ik Analytics niet selecteren als mijn rapporteringsbron wanneer ik een nieuwe activiteit creeer? {#section_9F4F69C3085F4C2480AF439127EB27CD}

U kunt de [!UICONTROL Reporting Settings] opties wijzigen in [!UICONTROL Administration].

1. Klik [!DNL Target]in **[!UICONTROL Administration]**.
1. In the **[!UICONTROL Experience Cloud solution used for reporting]** drop-down list, click **[!UICONTROL Select per Activity]**.

![](assets/select-per-activity.png)

De **[!UICONTROL Reporting Source]** vervolgkeuzelijst is in het **[!UICONTROL Goal & Settings]** scherm ingeschakeld voor het maken en bewerken van activiteiten.

Selecteer een optie in de vervolgkeuzelijst in als u deze altijd wilt gebruiken [!DNL Analytics] als rapportagebron **[!UICONTROL Adobe Analytics]** [!UICONTROL Administration].

## Kan een bezoeker schakelen tussen gerichte en gecontroleerde ervaringen in verschillende bezoeken in een auto-Doelactiviteit die A4T gebruikt?

Het volgende is waar veronderstellend bezoekerId verandert niet voor een bezoeker tussen bezoeken.

Als het percentage voor de verkeerstoewijzing halverwege de activiteit wordt aangepast, is het mogelijk dat een bezoeker kan schakelen tussen doelgerichte en controleervaringen.

Als de percentages niet worden aangepast halverwege de activiteit, zal een bezoeker die aanvankelijk de controle ziet altijd naar controle worden verzonden. Een bezoeker die naar gerichte ervaringen wordt verzonden zal altijd naar gerichte ervaringen worden verzonden.

* Nadat de bezoeker zich in de beoogde &quot;emmer&quot; van het verkeer bevindt, kan hij naar een andere ervaring worden gestuurd dan een bezoek om te bezoeken als de modellen voor machinaal leren bepalen dat een andere ervaring relevant is voor het nieuwe bezoek.
* Nadat hij aan de controle &quot;emmer&quot;van verkeer wordt toegewezen, zal een bezoeker altijd de zelfde ervaring zien omdat de ervaringstaak op een deterministische pseudo-willekeurige hash van bezoekers bezoekerId gebaseerd is.

## Is het raadzaam het aangepaste model voor AutoDoel en A4T te gebruiken met een 90 (Controle)/10 (Gericht) spleet tot de modellen bouwen?

Uw optimale verdeling van de verkeerstoewijzing hangt af van wat u wilt verwezenlijken.

Als uw doel is zoveel mogelijk verkeer te personaliseren, kunt u met 90% gerichte en 10% controle voor het leven van de activiteit blijven. Als je een experiment wilt uitvoeren waarin je vergelijkt hoe goed gepersonaliseerde algoritmen werken ten opzichte van het besturingselement, dan is een 50/50-splitsing het beste.

