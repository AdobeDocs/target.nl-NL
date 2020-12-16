---
keywords: audience;audience rules;combine audiences;exclusion;add exclusion;exclude;combining audiences;adhoc audience;ad hoc audience
description: Combineer meerdere soorten publiek (inclusief Adobe Experience Cloud-publiek en doelpubliek) om een ad-hocpubliek te maken. U kunt ook uitsluitingsregels maken en het publiek uitsluiten van een regel.
title: Meerdere doelgroepen combineren in Adobe Target
feature: audiences
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---


# Meerdere soorten publiek combineren{#combine-multiple-audiences}

Combineer meerdere soorten publiek (inclusief Adobe Experience Cloud-publiek en doelpubliek) om een ad-hocpubliek te maken. U kunt ook uitsluitingsregels maken en het publiek uitsluiten van een regel.

Stel dat u een publiek hebt met de doelgroep &quot;Nieuwe bezoekers&quot; en een publiek met de doelgroep &quot;Chrome-gebruikers&quot;. Voor een specifieke activiteit, zou u deze bestaande publiek aan doelnieuwe bezoekers kunnen willen combineren gebruikend browsers van Chrome. In plaats van een derde publiek te maken en dit op te slaan in de [!UICONTROL Audiences]-bibliotheek, kunt u deze twee soorten publiek combineren tijdens het maken van activiteiten of tijdens het bewerken van een bestaande activiteit.

Als ander voorbeeld, kunt u alle loyaliteitklanten richten door een specifiek [!DNL Audience Manager] segment voor loyaliteitsstatus op te nemen en het te combineren met een [!DNL Target] segment dat uit mensen bestaat die voor uw loyaliteitsprogramma tijdens de huidige zitting, in plaats van het creëren van een derde, permanent publiek hebben aangemeld.

U kunt maximaal tien soorten publiek combineren met AND en OR.

U kunt een gecombineerd publiek op verschillende plaatsen door [!DNL Target] UI tot stand brengen en gebruiken.

## Een gecombineerd publiek maken tijdens het maken van een activiteit {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

U kunt een ad hoc gecombineerd publiek op de pagina van [!UICONTROL Target] van de activiteit tijdens de drie-stap geleide werkschema tot stand brengen.

1. Tijdens het creëren van [activity](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op **[!UICONTROL Target]** pagina, klik de drie verticale ellipsen, dan klik **[!UICONTROL Replace Audience]**.

   ![Stap resultaat](assets/edit_audience.png)

1. Selecteer op de pagina [!UICONTROL Choose Audience] de selectievakjes naast het gewenste publiek dat u als bouwstenen voor uw gecombineerde publiek wilt gebruiken.

   ![Stap resultaat](assets/combine_multiple_audiences1.png)

1. Klik op **[!UICONTROL Combine Multiple Audiences]** in de rechterbovenhoek.

   ![Stap resultaat](assets/combine_multiple_audiences2.png)

1. (Voorwaardelijk) Bewerk het nieuwe gecombineerde publiek naar wens.

   Met het dialoogvenster [!UICONTROL Edit Audience] kunt u extra elementen voor publieksopbouw van links naar het nieuwe gecombineerde publiek slepen en neerzetten, en uitsluitingsregels toevoegen en het publiek uitsluiten.

   1. U kunt slepen-en-neerzetten functionaliteit gebruiken om publiek binnen een bestaande sectie als niveau 2 bouwsteen toe te voegen. Als u een bouwsteen van niveau 1 wilt toevoegen, schakelt u het selectievakje naast het gewenste publiek in en klikt u op **[!UICONTROL Add to Rules]**.

      Stel dat u in het vorige voorbeeld nu Safari-gebruikers wilt opnemen in het gecombineerde publiek. Zoek naar en sleep het publiek &quot;Safari Browser&quot;in de Browser van Firefox&quot;doos op de rechterkant, zoals in het volgende voorbeeld:

      ![](assets/combine_multiple_audiences3.png)

      De operator tussen het twee publiek van het browsertype is AND. Selecteer de vervolgkeuzelijst En en wijzig deze in &quot;OR&quot; om een nieuw, gecombineerd publiek te maken voor nieuwe bezoekers met Firefox of Safari. Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Het is bijvoorbeeld niet mogelijk dat iemand een pagina gelijktijdig bezoekt met Firefox en Safari.

      >[!NOTE]
      >
      >De operator (AND of OR) moet hetzelfde blijven als het publiek dat u combineert. U kunt operatoren niet mixen en koppelen.

   1. Als u een uitsluiting aan een regel wilt toevoegen, klikt u op **[!UICONTROL Exclusion]** > **[!UICONTROL Add Exclusion]**.

      ![](assets/combine_multiple_audiences3a.png)

      Sleep een publiek naar het vak:

      ![](assets/combine_multiple_audiences3b.png)

      Als u bijvoorbeeld Amerikaanse bezoekers wilt uitsluiten van nieuwe bezoekers, versleept u de Market: Amerikaanse publiek in de doos, zoals hieronder getoond:

      ![](assets/combine_multiple_audiences3b2.png)

      Dit gecombineerde publiek omvat alle nieuwe bezoekers aan uw plaats (met uitzondering van die van San Francisco) gebruikend Safari of Firefox.

   1. Als u een publiek wilt uitsluiten van een regel, klikt u op **[!UICONTROL Exclusion]** > **[!UICONTROL Exclude this Audience.]**.

      U kunt bijvoorbeeld een gecombineerd publiek maken dat alle nieuwe bezoekers van uw site omvat, met uitzondering van bezoekers die Firefox gebruiken. Het uitsluiten van bezoekers die Firefox gebruiken is eenvoudiger en sneller dan het maken van een gecombineerd publiek dat expliciet meerdere browsers (Safari, Chrome en Internet Explorer) bevat, maar Firefox is niet inbegrepen.

1. Geef een beschrijvende naam op voor het gecombineerde publiek en klik op **[!UICONTROL Save]**.

## Een gecombineerd publiek maken voor gebruik bij het meten van {#section_A42E795AFCBD4575809C5942039910F0}

U kunt een ad hoc gecombineerd publiek op de pagina van [!UICONTROL Goals & Settings] van de activiteit tot stand brengen om in metrisch richten te gebruiken. Bijvoorbeeld om het richten tot stand te brengen die op omzetting gebruikend een gecombineerd publiek wordt gebaseerd:

1. Tijdens het uitgeven of het creëren van [activiteit](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op **[!UICONTROL Goals & Settings]** pagina, selecteer **[!UICONTROL Conversion]** voor succesmetrisch, dan uitgezocht **[!UICONTROL Viewed an Mbox]** als actie.
1. Selecteer de gewenste mbox in het **[!UICONTROL Search mbox]** gebied.

   ![](assets/combine_multiple_audiences4.png)

1. Klik op het tandwielpictogram en klik vervolgens op **[!UICONTROL Add Audience Targeting]**.
1. Klik op de koppeling **[!UICONTROL Add Audience/Targeting Condition]** om het dialoogvenster [!UICONTROL Choose Audience] weer te geven.

   ![](assets/combine_multiple_audiences5.png)

1. Ga met [Stap 2](/help/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;creeer een Gecombineerde Publiek terwijl het Creëren van een Activiteit&quot;om het gecombineerde publiek tot stand te brengen.

## Creeer een Gecombineerd Publiek voor Gebruik in het Melden {#section_4682D342EFBB43C38E54B99B3A1E14CD}

U kunt een ad hoc gecombineerd publiek op de pagina [!UICONTROL Goals & Settings] van de activiteit tot stand brengen in het melden.

1. Tijdens het bewerken of maken van een [activiteit](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) klikt u op de **[!UICONTROL Goals & Settings]**-pagina onder **[!UICONTROL Add Audience]** om de [!UICONTROL Choose Audience]-pagina weer te geven.[!UICONTROL Audiences for Reporting]

   ![](assets/combine_multiple_audiences6.png)

1. Ga met [Stap 2](/help/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;creeer een Gecombineerde Publiek terwijl het Creëren van een Activiteit&quot;om het gecombineerde publiek tot stand te brengen.

## Een gecombineerd publiek maken tijdens het bewerken van een activiteit {#section_364A12CE96E04B61B7C18113AA586C2C}

U kunt een gecombineerd ad-hocpubliek maken terwijl u een bestaande activiteit bewerkt.

1. Houd de muisaanwijzer boven de gewenste activiteit op de pagina [!UICONTROL Activities] en klik op het pictogram **[!UICONTROL Edit]**.

   of

   Klik op de gewenste activiteit om deze te openen en klik vervolgens op **[!UICONTROL Edit Activity]**.

1. Klik op **[!UICONTROL Configure]** > **[!UICONTROL Audiences]** > **[!UICONTROL Multiple Audiences]**.

   ![Configureren > Soorten publiek > Meerdere soorten publiek](/help/c-target/assets/combine_multiple_audiences7.png)

1. Klik op het pictogram Meer opties (drie verticale ellipsen) naast het huidige publiek van de activiteit en klik vervolgens op **[!UICONTROL Change Audience]**.

   ![Publiek wijzigen](/help/c-target/assets/combine_multiple_audiences8.png)

1. Ga met [Stap 2](/help/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;creeer een Gecombineerde Publiek terwijl het Creëren van een Activiteit&quot;om het gecombineerde publiek tot stand te brengen.