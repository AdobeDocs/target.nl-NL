---
keywords: faq;vaak gestelde vragen;analyse voor doel;a4T;activiteitsinstelling
description: Dit onderwerp bevat antwoorden op vragen die vaak over activiteitenopstelling en het gebruiken van Analytics als rapporteringsbron voor Doel (A4T) worden gevraagd.
title: Activiteitsinstellingen - Veelgestelde vragen voor A4T
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# Activiteitsinstellingen - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak over activiteitenopstelling worden gevraagd en gebruikend [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

## Welke activiteitstypes steunen Analytics als rapporteringsbron (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Voor een volledige lijst, zie &quot;Gesteunde Types van Activiteit&quot;in [Adobe Analytics als Rapporterende Bron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Waarom heb ik tijdens het configureren van mijn Goal Metics geen toegang tot Geavanceerde instellingen?

Voor activiteiten die [!DNL Analytics] als rapporteringsbron (A4T) gebruiken, zal doel metrisch altijd &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages gebruiken. Dit is *niet* configureerbaar.

Voor meer informatie, zie &quot;terwijl het vormen van mijn doelmetica, waarom kan ik niet tot de Geavanceerde opties van Montages toegang hebben?&quot; in [Metrische definities - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ik heb net een activiteit gecreëerd. Waarom zie ik geen gegevens binnenkomen? {#section_9F8092BE4225442896F926540292F221}

Wanneer een activiteit wordt gecreeerd, [!DNL Target] verzendt een classificatiedossier naar [!DNL Analytics]. Hoewel [!DNL Analytics] de gegevens vastlegt en verwerkt, wordt deze pas in de rapporten weergegeven als het classificatiebestand is bijgewerkt. Dit kan tot 24 uur duren. Als u na 48 uur uw gegevens niet ziet, gelieve [de Zorg van de Cliënt ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) te contacteren. Als u weet dat u een activiteit start, kunt u de activiteit een paar dagen van tevoren maken en de classificaties worden verzonden wanneer de activiteit wordt opgeslagen. Op die manier worden gegevens weergegeven in de rapporten wanneer deze worden gestart. Houd er rekening mee dat het 45-90 minuten duurt voordat gegevens worden verwerkt in [!DNL Analytics].

## Waarom kan ik Analytics niet selecteren als mijn rapporteringsbron wanneer ik een nieuwe activiteit creeer? {#section_9F4F69C3085F4C2480AF439127EB27CD}

U kunt uw [!UICONTROL Reporting Settings] opties in [!UICONTROL Administration] veranderen.

1. Klik in [!DNL Target] op **[!UICONTROL Administration]**.
1. Klik in de vervolgkeuzelijst **[!UICONTROL Experience Cloud solution used for reporting]** op **[!UICONTROL Select per Activity]**.

![](assets/select-per-activity.png)

De vervolgkeuzelijst **[!UICONTROL Reporting Source]** is ingeschakeld in het **[!UICONTROL Goal & Settings]**-scherm voor het maken en bewerken van activiteiten.

Als u [!DNL Analytics] altijd als rapportagebron wilt gebruiken, selecteert u **[!UICONTROL Adobe Analytics]** in de vervolgkeuzelijst in [!UICONTROL Administration].

## Kan een bezoeker schakelen tussen gerichte en gecontroleerde ervaringen in verschillende bezoeken in een auto-Doelactiviteit die A4T gebruikt?

Het volgende is waar veronderstellend bezoekerId verandert niet voor een bezoeker tussen bezoeken.

Als het percentage voor de verkeerstoewijzing halverwege de activiteit wordt aangepast, is het mogelijk dat een bezoeker kan schakelen tussen doelgerichte en controleervaringen.

Als de percentages niet worden aangepast halverwege de activiteit, zal een bezoeker die aanvankelijk de controle ziet altijd naar controle worden verzonden. Een bezoeker die naar gerichte ervaringen wordt verzonden zal altijd naar gerichte ervaringen worden verzonden.

* Nadat de bezoeker zich in de beoogde &quot;emmer&quot; van het verkeer bevindt, kan hij naar een andere ervaring worden gestuurd dan een bezoek om te bezoeken als de modellen voor machinaal leren bepalen dat een andere ervaring relevant is voor het nieuwe bezoek.
* Nadat hij aan de controle &quot;emmer&quot;van verkeer wordt toegewezen, zal een bezoeker altijd de zelfde ervaring zien omdat de ervaringstaak op een deterministische pseudo-willekeurige hash van bezoekers bezoekerId gebaseerd is.
