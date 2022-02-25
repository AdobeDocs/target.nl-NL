---
keywords: publiek;publieksregels;publiek maken;publiek maken;alleen publiek maken;activiteit;alleen activiteit;adhoc
description: Meer informatie over het maken van alleen-activiteit publiek in Adobe [!DNL Target] voor eenmalig gebruik.
title: Kan ik een publiek creëren om slechts één keer te gebruiken?
feature: Audiences
exl-id: 5fe0507a-75d1-47bc-a941-8c8eeeaf3b75
source-git-commit: 974b2093bc9ebc81acb64aa5df0c4c345e52383c
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Een alleen-activiteitpubliek maken

Een alleen-activiteitpubliek maken vanuit de [!DNL Adobe Target] driestapsgeleide workflow tijdens het maken van een activiteit. Deze ad-hocdoelgroepen kunnen op andere plaatsen binnen dezelfde activiteit worden gebruikt, maar worden niet in de [!UICONTROL Audiences Library] voor gebruik bij andere activiteiten.

Alleen voor activiteiten bestemd publiek biedt de volgende voordelen:

* U kunt alleen op activiteit gericht publiek gebruiken om een publiek te maken dat u maar één keer wilt gebruiken en u wilt het niet opslaan in het dialoogvenster [!UICONTROL Audiences Library]. Alleen-actief publiek voorkomt de [!UICONTROL Audiences Library] omdat je door allerlei soorten publiek wordt overspoeld die je nooit meer wilt gebruiken.
* Activiteitsgericht publiek is niet zichtbaar in de [!UICONTROL Audiences Library]. Omdat deze doelgroepen niet zichtbaar zijn in de bibliotheek, worden ze beschermd tegen ongewenste wijzigingen door anderen in uw organisatie.

1. Tijdens het maken van een [activiteit](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)over de **[!UICONTROL Targeting]** pagina, klikt u op de drie verticale ovalen en klikt u vervolgens op **[!UICONTROL Replace Audience]**.

   ![Stap resultaat](assets/edit_audience.png)

1. Klik op **[!UICONTROL Create Audience]**.

1. Klik op **[!UICONTROL This activity only]**.

   ![](assets/activity-only-aud.png)

1. Typ een beschrijvende publieksnaam.
1. Sleep de gewenste kenmerken naar de publieksbuilder.

   Regels maken het mogelijk om uw publiek te beperken tot een subset van uw sitebezoekers. Elk regeltype heeft zijn eigen parameters. Zie [Categorieën voor soorten publiek](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Klik op **[!UICONTROL Done]**.

## Overwegingen

Houd rekening met de volgende informatie wanneer u alleen werkt met activiteiten:

* U kunt alleen-activiteit publiek maken in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC) of in de [!UICONTROL Form-Based Experience Composer]. Deze functie vervangt verfijningsregels in vorige versies van [!DNL Target].
* U kunt een activiteit maken om op te slaan in het dialoogvenster [!UICONTROL Audience Library] voor hergebruik in andere activiteiten of u maakt een alleen-activiteitspubliek. Nadat u het publiek hebt opgeslagen, kunt u het type publiek niet meer wijzigen.
* Verfijningen voor bestaande activiteiten worden gemigreerd naar alleen-activiteiten-publiek.
* Toegankelijke doelgroepen hebben de status [!UICONTROL Used] of [!UICONTROL Unused]. Ongebruikte publiek met alleen activiteit wordt weergegeven totdat de activiteit is opgeslagen. Als u de activiteit niet gebruikt en probeert op te slaan, wordt een waarschuwingsbericht weergegeven met de melding dat ongebruikte publiek met alleen de activiteit wordt verwijderd.
* U kunt de definitiedetails van het publiek op een pop-up kaart bekijken die van de publiekskiezer wordt betreden zonder het publiek te openen.
* U kunt [meerdere soorten publiek combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) om alleen-activiteit publiek te maken.
* Activiteits-slechts publiek steunt geen regels.

   U kunt de volgende alternatieven gebruiken om regels uit te sluiten:

   * [Bibliotheekpubliek maken en gebruiken](/help/c-target/c-audiences/create-audience.md) in plaats van een alleen-activiteitspubliek.
   * [Meerdere combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) (maximaal 20) bibliotheekpubliek krijgt alleen toegang tot activiteiten. Wanneer het combineren van publiek, omvat en sluit regels in individuele bibliotheekpubliek uit kan worden gebruikt zelfs wanneer het gecombineerde publiek als activiteit-slechts publiek wordt bewaard.
