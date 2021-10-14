---
keywords: faq;vaak gestelde vragen;analyse voor doel;a4T;activiteitsinstelling
description: Vind antwoorden op vragen over activiteitenopstelling wanneer het gebruiken van Analytics voor  [!DNL Target] (A4T). A4T lets you use Analytics reporting for [!DNL Target] activiteiten.
title: Waar kan ik Veelgestelde vragen over activiteitenmontages met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 15ca5e92af5ebc66caa52ffc1dc04e1fbcbb2ed3
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Activiteitsinstellingen - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak over activiteitenopstelling worden gevraagd en gebruikend [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T).

## Welke activiteitstypes steunen Analytics als rapporteringsbron (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

Voor een volledige lijst, zie &quot;Gesteunde Types van Activiteit&quot;in [Adobe Analytics als Rapporterende Bron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

## Waarom heb ik tijdens het configureren van mijn Goal Metrics geen toegang tot Geavanceerde instellingen?

Voor activiteiten die [!DNL Analytics] als rapporteringsbron (A4T) gebruiken, het doel metrisch gebruikt &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages. Deze instellingen kunnen *niet* worden geconfigureerd.

Voor meer informatie, zie &quot;terwijl het vormen van mijn doelmetriek, waarom kan ik niet tot de Geavanceerde opties van Montages toegang hebben?&quot; in [Metrische definities - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

## Ik heb net een activiteit gecreëerd. Waarom zie ik geen gegevens binnenkomen? {#section_9F8092BE4225442896F926540292F221}

Wanneer een activiteit wordt gecreeerd, [!DNL Target] verzendt een classificatiedossier naar [!DNL Analytics]. Hoewel [!DNL Analytics] de gegevens vastlegt en verwerkt, toont het niet dat in de rapporten tot het classificatiedossier is bijgewerkt. Dit proces kan tot 24 uur duren. Als u na 48 uur uw gegevens niet ziet, gelieve [de Zorg van de Cliënt ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) te contacteren. Als u weet dat u een activiteit start, kunt u deze activiteit een paar dagen eerder maken en de classificaties worden verzonden wanneer de activiteit wordt opgeslagen. Op die manier worden gegevens weergegeven in de rapporten wanneer deze worden gestart. Houd er rekening mee dat het 45-90 minuten duurt voordat gegevens worden verwerkt in [!DNL Analytics].

## Waarom kan ik Analytics niet als mijn rapporteringsbron selecteren wanneer ik een activiteit creeer? {#section_9F4F69C3085F4C2480AF439127EB27CD}

U kunt uw [!UICONTROL Reporting Settings] opties in [!UICONTROL Administration] veranderen.

1. Klik in [!DNL Target] op **[!UICONTROL Administration]**.
1. Klik in de vervolgkeuzelijst **[!UICONTROL Experience Cloud solution used for reporting]** op **[!UICONTROL Select per Activity]**.

![](assets/select-per-activity.png)

De vervolgkeuzelijst **[!UICONTROL Reporting Source]** is ingeschakeld in het **[!UICONTROL Goal & Settings]**-scherm voor het maken en bewerken van activiteiten.

Als u [!DNL Analytics] altijd als rapportagebron wilt gebruiken, selecteert u **[!UICONTROL Adobe Analytics]** in de vervolgkeuzelijst in [!UICONTROL Administration].

## Kan een bezoeker schakelen tussen gerichte en gecontroleerde ervaringen in verschillende bezoeken in een auto-Doelactiviteit die A4T gebruikt?

Het volgende is waar veronderstellend bezoekerId verandert niet voor een bezoeker tussen bezoeken.

Als het percentage voor de verkeerstoewijzing halverwege de activiteit wordt aangepast, is het mogelijk dat een bezoeker kan schakelen tussen doelgerichte en controleervaringen.

Als de percentages niet worden aangepast halverwege de activiteit, wordt een bezoeker die aanvankelijk de controle ziet altijd verzonden naar controle. Een bezoeker die naar gerichte ervaringen wordt verzonden wordt altijd naar gerichte ervaringen verzonden.

* Nadat de bezoeker zich in de beoogde &quot;emmer&quot; van het verkeer bevindt, kan hij naar een andere ervaring worden gestuurd dan een bezoek om te bezoeken als de modellen voor machinaal leren bepalen dat een andere ervaring relevant is voor het nieuwe bezoek.
* Nadat hij aan de controle &quot;emmer&quot;van verkeer wordt toegewezen, zal een bezoeker altijd de zelfde ervaring zien omdat de ervaringstaak op een deterministische pseudo-willekeurige hash van bezoekers bezoekerId gebaseerd is.


## Kan ik een binomiale metrische [!DNL Analytics] met een segment gebruiken dat als optimaliserend doel in een [!UICONTROL Auto-Allocate] activiteit wordt toegepast? {#binomial}

U kunt geen [!DNL Analytics] metrisch met een segment gebruiken dat als optimaliserend doel in een [!UICONTROL Auto-Allocate] activiteit wordt toegepast. Als tussenoplossing kunt u een gebeurtenis van de Douane bepalen die het zelfde doel bereikt en gebruikt dat zoals optimaliserend doel metrisch.