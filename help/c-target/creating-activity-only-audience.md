---
keywords: publiek;publieksregels;publiek maken;publiek maken;alleen publiek maken;activiteit;alleen activiteit;adhoc
description: Leer hoe u een alleen-activiteitpubliek maakt in Adobe [!DNL Target] voor eenmalig gebruik.
title: Kan ik een publiek creëren om slechts één keer te gebruiken?
feature: Soorten publiek
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 20a5201b5c05b1f083252ac73b3b4bbc91e97aaa
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Een alleen-activiteitpubliek maken

Maak een publiek met alleen activiteit vanuit de driestappenworkflow met instructies in [!DNL Adobe Target] terwijl u een activiteit maakt. Deze ad-hocdoelgroepen kunnen op andere plaatsen binnen dezelfde activiteit worden gebruikt, maar worden niet in [!UICONTROL Audiences Library] opgeslagen voor gebruik in andere activiteiten.

Alleen voor activiteiten bestemd publiek biedt de volgende voordelen:

* U kunt activiteit-slechts publiek gebruiken om een publiek tot stand te brengen dat u slechts één keer wilt gebruiken en u wilt niet het in [!UICONTROL Audiences Library] opslaan. Activiteits-slechts publiek helpt [!UICONTROL Audiences Library] worden geklonterd met publiek dat u nooit meer wilt gebruiken.
* Activiteits-slechts publiek is niet zichtbaar in [!UICONTROL Audiences Library]. Omdat deze doelgroepen niet zichtbaar zijn in de bibliotheek, worden ze beschermd tegen ongewenste wijzigingen door anderen in uw organisatie.

1. Tijdens het creëren van [activity](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op **[!UICONTROL Targeting]** pagina, klik de drie verticale ellipsen, dan klik **[!UICONTROL Replace Audience]**.

   ![Stap resultaat](assets/edit_audience.png)

1. Klik op **[!UICONTROL Create Audience]**.

1. Klik op **[!UICONTROL This activity only]**.

   ![](assets/activity-only-aud.png)

1. Typ een beschrijvende publieksnaam.
1. Sleep de gewenste kenmerken naar de publieksbuilder.

   Regels maken het mogelijk om uw publiek te beperken tot een subset van uw sitebezoekers. Elk regeltype heeft zijn eigen parameters. Zie [Categorieën voor Soorten publiek](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Klik op **[!UICONTROL Done]**.

## Overwegingen

Houd rekening met de volgende informatie wanneer u alleen werkt met activiteiten:

* U kunt alleen-activiteit publiek in [!UICONTROL Visual Experience Composer] (VEC) of in [!UICONTROL Form-Based Experience Composer] tot stand brengen. Deze functionaliteit vervangt verfijningsregels in vorige versies van [!DNL Target].
* U kunt een activiteit tot stand brengen om in [!UICONTROL Audience Library] voor hergebruik in andere activiteiten op te slaan of u creeert een activiteit-slechts publiek. Nadat u het publiek hebt opgeslagen, kunt u het type publiek niet meer wijzigen.
* Verfijningen voor bestaande activiteiten worden gemigreerd naar alleen-activiteiten-publiek.
* Toegankelijke doelgroepen hebben de status [!UICONTROL Used] of [!UICONTROL Unused]. Ongebruikte publiek met alleen activiteit wordt weergegeven totdat de activiteit is opgeslagen. Als u de activiteit niet gebruikt en probeert op te slaan, wordt een waarschuwingsbericht weergegeven met de melding dat ongebruikte publiek met alleen de activiteit wordt verwijderd.
* U kunt de definitiedetails van het publiek op een pop-up kaart bekijken die van de publiekskiezer wordt betreden zonder het publiek te openen.
* U kunt [meerdere soorten publiek combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) om alleen-activiteit publiek te maken.
