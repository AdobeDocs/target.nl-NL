---
keywords: publiek;publieksregels;publiek maken;publiek maken;alleen publiek maken;activiteit;alleen activiteit;adhoc
description: Maak een publiek met alleen activiteit vanuit de driestappenworkflow van Adobe Target wanneer u een activiteit maakt. Deze speciale doelgroepen kunnen op andere plaatsen binnen dezelfde activiteit worden gebruikt, maar worden niet opgeslagen in de Soortbibliotheek voor gebruik in andere activiteiten.
title: Een alleen-actief publiek maken
feature: Audiences
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---


# Creeer een activiteit-slechts publiek{#create-an-activity-only-audience}

Maak een alleen-activiteit publiek vanuit de driestappenworkflow met instructies bij het maken van een activiteit. Deze ad-hocdoelgroepen kunnen op andere plaatsen binnen dezelfde activiteit worden gebruikt, maar worden niet in [!UICONTROL Audiences Library] opgeslagen voor gebruik in andere activiteiten.

Alleen voor activiteiten bestemd publiek biedt de volgende voordelen:

* U kunt activiteit-slechts publiek gebruiken om een publiek tot stand te brengen dat u slechts één keer wilt gebruiken en u wilt niet het in [!UICONTROL Audiences Library] opslaan. Zo voorkomt u dat het publiek dat u nooit meer wilt gebruiken, wordt overspoeld met [!UICONTROL Audiences Library].
* Activiteits-slechts publiek is niet zichtbaar in [!UICONTROL Audiences Library]. Daarom zijn ze beschermd tegen ongewenste wijzigingen door anderen in uw organisatie.

1. Tijdens het creëren van [activity](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op **[!UICONTROL Target]** pagina, klik de drie verticale ellipsen, dan klik **[!UICONTROL Replace Audience]**.

   ![Stap resultaat](assets/edit_audience.png)

1. Klik op [!UICONTROL Choose Audience] op de pagina.**[!UICONTROL Activity Only Audience]**

   ![](assets/activity-only-aud.png)

1. Klik op **[!UICONTROL Create Audience]**.
1. Typ een beschrijvende publieksnaam.
1. Klik op **[!UICONTROL + Add Rule]**.

   Regels maken het mogelijk om uw publiek te beperken tot een subset van uw sitebezoekers.

1. Selecteer een regeltype.

   Elk regeltype heeft zijn eigen parameters. Zie [Categorieën voor Soorten publiek](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Definieer de regelparameters.
1. Klik op **[!UICONTROL Save]**.

## Overwegingen

Houd rekening met de volgende informatie wanneer u alleen werkt met activiteiten:

* U kunt activiteit-slechts publiek in de Visuele Composer van de Ervaring (VEC) of in Form-Based Composer van de Ervaring tot stand brengen. Deze functionaliteit vervangt verfijningsregels in vorige versies van Doel.
* U kunt een activiteit tot stand brengen om in [!UICONTROL Audience Library] voor hergebruik in andere activiteiten op te slaan of u creeert een activiteit-slechts publiek. Nadat u het publiek hebt opgeslagen, kunt u het type publiek niet meer wijzigen.
* Verfijningen voor bestaande activiteiten worden gemigreerd naar alleen-activiteiten-publiek.
* Toegankelijke doelgroepen hebben de status [!UICONTROL Used] of [!UICONTROL Unused]. Ongebruikte publiek met alleen activiteit wordt weergegeven totdat de activiteit is opgeslagen. Als u de activiteit niet gebruikt en probeert op te slaan, wordt een waarschuwingsbericht weergegeven met de melding dat ongebruikte publiek met alleen de activiteit wordt verwijderd.
* U kunt de definitiedetails van het publiek op een pop-up kaart bekijken die van de publiekskiezer wordt betreden zonder het publiek te openen.
* U kunt [meerdere soorten publiek combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) om alleen-activiteit publiek te maken.

