---
keywords: publiek;publieksregels;publiek maken;publiek maken;alleen publiek maken;activiteit;alleen activiteit;adhoc
description: Leer hoe te om tot activiteit-slechts publiek in Adobe  [!DNL Target]  te leiden die voor eenmalig gebruik zijn.
title: Kan ik een publiek creëren om slechts één keer te gebruiken?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Een alleen-activiteitpubliek maken

Maak een publiek met alleen activiteit vanuit de [!DNL Adobe Target] driestapige geleide workflow terwijl u een activiteit maakt. Deze ad-hocdoelgroepen kunnen op andere plaatsen binnen dezelfde activiteit worden gebruikt, maar worden niet in [!UICONTROL Audiences Library] opgeslagen voor gebruik in andere activiteiten.

Alleen voor activiteiten bestemd publiek biedt de volgende voordelen:

* Met alleen activiteiten kunt u een publiek maken dat u maar één keer wilt gebruiken en niet in de [!UICONTROL Audiences Library] wilt opslaan. Met alleen activiteiten kunt u voorkomen dat het publiek in [!UICONTROL Audiences Library] wordt overspoeld met soorten publiek die u nooit meer wilt gebruiken.
* Activiteit-slechts publiek is niet zichtbaar in [!UICONTROL Audiences Library]. Omdat deze doelgroepen niet zichtbaar zijn in de bibliotheek, worden ze beschermd tegen ongewenste wijzigingen door anderen in uw organisatie.

1. Terwijl het creëren van een [&#x200B; activiteit &#x200B;](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op de **[!UICONTROL Targeting]** pagina, klik de drie verticale ellipsen, dan klik **[!UICONTROL Replace Audience]**.

   ![&#x200B; Resultaat van de Stap &#x200B;](assets/edit_audience.png)

1. Klik op **[!UICONTROL Create Audience]**.

1. Klik op **[!UICONTROL This activity only]**.

   ![&#x200B; activiteit-slechts-aud beeld &#x200B;](assets/activity-only-aud.png)

1. Typ een beschrijvende publieksnaam.
1. Sleep de gewenste kenmerken naar de builder van het publiek.

   Regels maken het mogelijk om uw publiek te beperken tot een subset van uw sitebezoekers. Elk regeltype heeft zijn eigen parameters. Zie [&#x200B; Categorieën voor Soorten publiek &#x200B;](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Klik op **[!UICONTROL Done]**.

## Overwegingen

Houd rekening met de volgende informatie wanneer u alleen werkt met activiteiten:

* U kunt alleen-activiteit publiek maken in [!UICONTROL Visual Experience Composer] (VEC) of in [!UICONTROL Form-Based Experience Composer] . Deze functie vervangt de verfijningsregels in eerdere versies van [!DNL Target] .
* U kunt een activiteit tot stand brengen om in [!UICONTROL Audience Library] voor hergebruik in andere activiteiten op te slaan of u creeert een activiteit-slechts publiek. Nadat u het publiek hebt opgeslagen, kunt u het type publiek niet meer wijzigen.
* Verfijningen voor bestaande activiteiten worden gemigreerd naar alleen-activiteiten-publiek.
* Toegankelijk publiek heeft de status [!UICONTROL Used] of [!UICONTROL Unused] . Ongebruikte publiek met alleen activiteit wordt weergegeven totdat de activiteit is opgeslagen. Als u de activiteit niet gebruikt en probeert op te slaan, wordt een waarschuwingsbericht weergegeven met de melding dat ongebruikte publiek met alleen de activiteit wordt verwijderd.
* U kunt de definitiedetails van het publiek op een pop-up kaart bekijken die van de publiekskiezer wordt betreden zonder het publiek te openen.
* U kunt [&#x200B; veelvoudige publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) combineren om tot activiteit-slechts publiek te leiden.
* Activiteits-slechts publiek steunt geen regels.

  U kunt de volgende alternatieven gebruiken om regels uit te sluiten:

   * [&#x200B; creeer en gebruik een bibliotheekpubliek &#x200B;](/help/main/c-target/c-audiences/create-audience.md) in plaats van een activiteit-slechts publiek.
   * [&#x200B; combineer veelvoudige &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (tot 20) bibliotheekpubliek in een activiteit-slechts publiek. Wanneer het combineren van publiek, omvat en sluit regels in individuele bibliotheekpubliek uit kan worden gebruikt zelfs wanneer het gecombineerde publiek als activiteit-slechts publiek wordt bewaard.
