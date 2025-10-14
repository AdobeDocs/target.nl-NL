---
keywords: faq;veelgestelde vragen;analyses voor doel;a4T;activity setup
description: Vind antwoorden op vragen over activiteitenopstelling wanneer het gebruiken van Analytics voor  [!DNL Target]  (A4T). A4T laat u Analytics gebruiken die voor  [!DNL Target]  activiteiten rapporteert.
title: Waar kan ik Veelgestelde vragen over activiteitenmontages met A4T vinden?
feature: Analytics for Target (A4T)
exl-id: 8a8cdbb9-89f6-4e4a-a53e-8f33adab4d61
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Activiteitsinstellingen - Veelgestelde vragen voor A4T

Dit onderwerp bevat antwoorden op vragen die vaak worden gesteld over het instellen van activiteiten en het gebruik van [!DNL Analytics] als rapportagebron voor [!DNL Target] (A4T).

## Welke activiteitstypen worden ondersteund [!DNL Analytics] als de rapportagebron (A4T)? {#section_5E4F58CD25A5424E869E6FE0803968EF}

+++Antwoord
Voor een volledige lijst, zie &quot;Ondersteunde Types van Activiteit&quot;in [&#x200B; Adobe Analytics als Rapporterende Source voor Adobe Target (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md#concept_7540C8C04259434AB6EE33B09F47A1DE).

+++

## Kan ik de zelfde activiteitennaam voor twee activiteiten van afzonderlijke werkruimten gebruiken wanneer het gebruiken van A4T het melden?

+++Antwoord

Gebruik niet de zelfde activiteitennaam voor twee activiteiten van afzonderlijke [&#x200B; werkruimten &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) die A4T het melden gebruiken.

Hoewel dit wordt ondersteund wanneer [!DNL Target] als rapportagebron wordt gebruikt, wordt het gebruik van dezelfde naam voor twee activiteiten niet ondersteund wanneer [!UICONTROL Analytics for Target] als rapportagebron wordt gebruikt.

+++

## Waarom heb ik tijdens het configureren van mijn Goal Metrics geen toegang tot Geavanceerde instellingen?

+++Antwoord
Voor activiteiten die [!DNL Analytics] als rapporteringsbron (A4T) gebruiken, metrische doel gebruikt &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot;en &quot;[!UICONTROL On Every Impression]&quot;montages. Deze montages zijn *niet* configureerbaar.

Voor meer informatie, zie &quot;terwijl het vormen van mijn doelmetriek, waarom kan ik niet tot de Geavanceerde opties van Montages toegang hebben?&quot; in [&#x200B; Metrische definities - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-metric-definition.md).

+++

## Ik heb net een activiteit gecreëerd. Waarom zie ik geen gegevens binnenkomen? {#section_9F8092BE4225442896F926540292F221}


+++Antwoord
Wanneer een activiteit wordt gecreeerd, verzendt [!DNL Target] een classificatiedossier naar [!DNL Analytics]. Hoewel [!DNL Analytics] de gegevens vastlegt en verwerkt, toont dit niet in de rapporten tot het classificatiebestand is bijgewerkt. Dit proces kan 24 tot 72 uur duren. Als na 72 uren u uw gegevens niet ziet, {de Zorg van de Cliënt van 0} contact [. &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) Als u weet dat u een activiteit start, kunt u deze activiteit een paar dagen eerder maken en de classificaties worden verzonden wanneer de activiteit wordt opgeslagen. Op die manier worden gegevens weergegeven in de rapporten wanneer deze worden gestart. Houd er rekening mee dat het 45-90 minuten duurt voordat gegevens worden verwerkt in [!DNL Analytics] .

+++

## Waarom kan ik Analytics niet als mijn rapporteringsbron selecteren wanneer ik een activiteit creeer? {#section_9F4F69C3085F4C2480AF439127EB27CD}

+++Antwoord
U kunt de [!UICONTROL Reporting Settings] -opties wijzigen in [!UICONTROL Administration] .

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** .
1. Klik in de vervolgkeuzelijst **[!UICONTROL Experience Cloud solution used for reporting]** op **[!UICONTROL Select per Activity]** .

![&#x200B; uitgezocht-per-activiteit beeld &#x200B;](assets/select-per-activity.png)

De vervolgkeuzelijst **[!UICONTROL Reporting Source]** wordt in het **[!UICONTROL Goal & Settings]** -scherm ingeschakeld voor het maken en bewerken van activiteiten.

Selecteer [!DNL Analytics] in de vervolgkeuzelijst in **[!UICONTROL Adobe Analytics]** als u [!UICONTROL Administration] altijd als rapportagebron wilt gebruiken.

+++

## Kan een bezoeker schakelen tussen gerichte en gecontroleerde ervaringen in verschillende bezoeken in een auto-Doelactiviteit die A4T gebruikt?

+++Antwoord
Het volgende is waar veronderstellend bezoekerId verandert niet voor een bezoeker tussen bezoeken.

Als het verkeerstoewijzingspercentage wordt aangepast halverwege de activiteit, is het mogelijk dat een bezoeker tussen gerichte en controleervaringen kan bewegen.

Als de percentages niet worden aangepast halverwege de activiteit, wordt een bezoeker die aanvankelijk de controle ziet altijd verzonden naar controle. Een bezoeker die naar gerichte ervaringen wordt verzonden wordt altijd naar gerichte ervaringen verzonden.

* Nadat de bezoeker zich in de beoogde &quot;emmer&quot; van het verkeer bevindt, kan hij naar een andere ervaring worden gestuurd dan een bezoek om te bezoeken als de modellen voor machinaal leren bepalen dat een andere ervaring relevant is voor het nieuwe bezoek.
* Nadat hij aan de controle &quot;emmer&quot;van verkeer wordt toegewezen, zal een bezoeker altijd de zelfde ervaring zien omdat de ervaringstaak op een deterministische pseudo-willekeurige hash van bezoekers bezoekerId gebaseerd is.

+++

## Kan ik een binomiale [!DNL Analytics] metrisch gebruiken met een segment dat als optimaliserend doel in een [!UICONTROL Auto-Allocate] activiteit wordt toegepast? {#binomial}

+++Antwoord
U kunt geen [!DNL Analytics] metrisch met een segment gebruiken dat als optimaliserend doel in een [!UICONTROL Auto-Allocate] activiteit wordt toegepast. Als tussenoplossing kunt u een gebeurtenis van de Douane bepalen die het zelfde doel bereikt en gebruikt dat zoals optimaliserend doel metrisch.

+++
