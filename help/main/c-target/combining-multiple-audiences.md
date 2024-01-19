---
keywords: publiek;publieksregels;samenvoegen publiek;uitsluiting;toevoegen uitsluiting;uitsluiten;combineren publiek;ad-hocpubliek
description: Leer hoe u meerdere soorten publiek combineert (inclusief Adobe Experience Cloud-publiek en [!DNL Target] publiek) op de vlucht om ad hoc publiek tot stand te brengen.
title: Kan ik Meerdere soorten publiek combineren om een nieuw publiek te maken?
feature: Audiences
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 0%

---

# Meerdere doelgroepen combineren

Meerdere soorten publiek combineren (inclusief [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform], en [!DNL Target] publiek) op de vlucht om ad hoc publiek tot stand te brengen. U kunt ook uitsluitingsregels maken en het publiek uitsluiten van een regel.

>[!NOTE]
>
>De [!DNL Adobe Experience Platform] bron is beschikbaar voor iedereen [!DNL Target] klanten die [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=en){target=_blank}. Publiek beschikbaar bij de [!DNL Adobe Experience Platform] kan worden gebruikt zoals het is of gecombineerd met bestaande doelgroepen, zoals in dit onderwerp wordt uitgelegd.
>
>Zie voor meer informatie [Soorten publiek uit Adobe Experience Platform gebruiken](/help/main/c-target/c-audiences/audiences.md#aep).

Stel dat u een publiek hebt met de doelgroep Nieuwe bezoekers en een publiek met de doelgroep Chrome-gebruikers. Voor een specifieke activiteit, zou u deze bestaande publiek aan doelnieuwe bezoekers kunnen willen combineren gebruikend browsers van Chrome. In plaats van een derde publiek te maken en het op te slaan in de [!UICONTROL Audiences] kunt u deze twee soorten publiek combineren tijdens het maken van activiteiten of tijdens het bewerken van een bestaande activiteit.

Als een ander voorbeeld, kunt u alle loyaliteitklanten richten. U kunt bijvoorbeeld een specifieke [!DNL Audience Manager] publiek voor loyaliteitsstatus en combineer deze met een [!DNL Target] publiek dat bestaat uit mensen die zich tijdens de huidige sessie hebben aangemeld voor uw loyaliteitsprogramma . Het combineren van deze twee soorten publiek is eenvoudiger dan het creëren van een derde, permanent publiek.

U kunt maximaal 20 soorten publiek combineren met AND en OR.

U kunt een gecombineerd publiek maken en gebruiken op verschillende plaatsen in de [!DNL Target] UI.

## Een gecombineerd publiek maken tijdens het maken van een activiteit {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

U kunt een ad hoc gecombineerd publiek op de activiteit tot stand brengen [!UICONTROL Target] pagina tijdens de driestappenworkflow met instructies.

1. Terwijl u een [activiteit](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), over de **[!UICONTROL Targeting]** pagina, klikt u op de drie verticale ovalen en klikt u vervolgens op **[!UICONTROL Replace Audience]**.

   ![Stapresultaat](assets/edit_audience.png)

1. Op de **[!UICONTROL Choose Audience]** , selecteert u de selectievakjes naast het gewenste publiek dat u als bouwstenen voor uw gecombineerde publiek wilt gebruiken.

   Gebruik de [!UICONTROL Search Audiences] om uw zoekopdracht naar het gewenste publiek te beperken.

   ![Stapresultaat](assets/combine_multiple_audiences1.png)

1. Klikken **[!UICONTROL Combine Multiple Audiences]** in de rechterbovenhoek.

   ![Stapresultaat](assets/combine_multiple_audiences2.png)

1. (Voorwaardelijk) Bewerk het nieuwe gecombineerde publiek naar wens.

   De [!UICONTROL Edit Audience] in dit dialoogvenster kunt u extra elementen voor publieksopbouw vanaf de linkerkant naar het nieuwe gecombineerde publiek slepen. U kunt ook uitsluitingsregels toevoegen en soorten publiek uitsluiten.

   1. Gebruik de functie slepen en neerzetten om een publiek binnen een bestaande sectie toe te voegen als bouwsteen van niveau 2.

      Stel dat u in het vorige voorbeeld nu Safari-gebruikers wilt opnemen in het gecombineerde publiek. Zoek naar en sleep het publiek &quot;Safari Browser&quot;in de Browser van Firefox&quot;doos op de rechterkant, zoals in het volgende voorbeeld:

      ![afbeelding combine_multiple_audiences3](assets/combine_multiple_audiences3.png)

      De operator tussen het twee publiek van het browsertype is AND. Selecteer de [!UICONTROL And] vervolgkeuzelijst en wijzig deze in &quot;OR&quot; om een nieuw, gecombineerd publiek te maken voor nieuwe bezoekers met Firefox of Safari. Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Het is bijvoorbeeld niet mogelijk dat iemand een pagina gelijktijdig bezoekt met Firefox en Safari.

      >[!NOTE]
      >
      >De operator (AND of OR) moet hetzelfde blijven als het publiek dat u combineert. U kunt operatoren niet mixen en koppelen.

   1. Als u een uitsluiting aan een regel wilt toevoegen, klikt u op **[!UICONTROL Exclude]**.

      ![afbeelding combine_multiple_audiences3a](assets/combine_multiple_audiences3a.png)

      Sleep een publiek.

      Als u bijvoorbeeld bezoekers uit de Verenigde Staten wilt uitsluiten van nieuwe bezoekers, kunt u het publiek Market: United States naar de doos slepen.

      Dit gecombineerde publiek omvat alle nieuwe bezoekers aan uw plaats (met uitzondering van die van San Francisco) gebruikend Safari of Firefox.

   1. Om een publiek van een regel uit te sluiten, klik **[!UICONTROL Exclusion]** > **[!UICONTROL Exclude this Audience.]**.

      U kunt bijvoorbeeld een gecombineerd publiek maken dat alle nieuwe bezoekers van uw site omvat, met uitzondering van bezoekers die Firefox gebruiken. Het uitsluiten van bezoekers die Firefox gebruiken is eenvoudiger en sneller dan het maken van een gecombineerd publiek dat expliciet meerdere browsers (Safari, Chrome en Internet Explorer) bevat, maar Firefox is niet inbegrepen.

1. Geef een beschrijvende naam op voor het gecombineerde publiek en klik vervolgens op **[!UICONTROL Done]**.

## Een gecombineerd publiek maken voor gebruik bij metrische doelen {#section_A42E795AFCBD4575809C5942039910F0}

U kunt een ad hoc gecombineerd publiek op de activiteit tot stand brengen [!UICONTROL Goals & Settings] pagina die moet worden gebruikt voor metrische doelen. Bijvoorbeeld om het richten tot stand te brengen die op omzetting gebruikend een gecombineerd publiek wordt gebaseerd:

1. Tijdens het bewerken of maken van een [activiteit](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), over de **[!UICONTROL Goals & Settings]** pagina, selecteert u **[!UICONTROL Conversion]** voor succesmetrisch, dan uitgezocht **[!UICONTROL Viewed an Mbox]** als de handeling.
1. Selecteer de gewenste mbox in het dialoogvenster **[!UICONTROL Search mbox]** veld.

   ![afbeelding combine_multiple_audiences4](assets/combine_multiple_audiences4.png)

1. Klik op het tandwielpictogram en klik vervolgens op **[!UICONTROL Add Audience Targeting]**.
1. Klik op de knop **[!UICONTROL Add Audience/Targeting Condition]** koppeling om de [!UICONTROL Choose Audience] in.

   ![afbeelding combine_multiple_publiek5](assets/combine_multiple_audiences5.png)

1. Doorgaan met [Stap 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;Een gecombineerd publiek maken tijdens het maken van een activiteit&quot; om het gecombineerde publiek te maken.

## Een gecombineerd publiek maken voor rapportage {#section_4682D342EFBB43C38E54B99B3A1E14CD}

U kunt een ad hoc gecombineerd publiek op de activiteit tot stand brengen [!UICONTROL Goals & Settings] pagina voor rapportage.

1. Tijdens het bewerken of maken van een [activiteit](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), over de **[!UICONTROL Goals & Settings]** pagina, klikt u op de **[!UICONTROL Add Audience]** pictogram onder [!UICONTROL Audiences for Reporting] om de [!UICONTROL Choose Audience] pagina.

   ![afbeelding combine_multiple_audiences6](assets/combine_multiple_audiences6.png)

1. Doorgaan met [Stap 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;Een gecombineerd publiek maken tijdens het maken van een activiteit&quot; om het gecombineerde publiek te maken.

## Een gecombineerd publiek maken tijdens het bewerken van een activiteit {#section_364A12CE96E04B61B7C18113AA586C2C}

U kunt een gecombineerd ad-hocpubliek maken terwijl u een bestaande activiteit bewerkt.

1. Van de [!UICONTROL Activities] pagina, houd de muisaanwijzer boven de gewenste activiteit en klik vervolgens op de knop **[!UICONTROL Edit]** pictogram.

   of

   Klik op de gewenste activiteit om deze te openen en klik vervolgens op **[!UICONTROL Edit Activity]**.

1. Klik op de knop **[!UICONTROL Configure]** > **[!UICONTROL Audiences]** > **[!UICONTROL Multiple Audiences]**.

   ![Configureren > Soorten publiek > Meerdere soorten publiek](assets/combine_multiple_audiences7.png)

1. Klik op het pictogram Meer opties (drie verticale ellipsen) naast het huidige publiek van de activiteit en klik vervolgens op **[!UICONTROL Change Audience]**.

   ![Publiek wijzigen](assets/combine_multiple_audiences8.png)

1. Doorgaan met [Stap 2](/help/main/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;Een gecombineerd publiek maken tijdens het maken van een activiteit&quot; om het gecombineerde publiek te maken.
