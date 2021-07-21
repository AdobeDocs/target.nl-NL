---
keywords: publiek;publieksregels;samenvoegen publiek;uitsluiten;toevoegen uitsluiting;uitsluiten;combineren publiek;ad-hocpubliek
description: Leer hoe u meerdere soorten publiek (inclusief Adobe Experience Cloud-publiek en [!DNL Target] publiek) tegelijk kunt combineren om een ad-hocpubliek te maken.
title: Kan ik Meerdere soorten publiek combineren om een nieuw publiek te maken?
feature: Soorten publiek
exl-id: 1d9bff9c-f63b-4e15-9809-71b046158b71
source-git-commit: 20a5201b5c05b1f083252ac73b3b4bbc91e97aaa
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Meerdere soorten publiek combineren

Combineer meerdere soorten publiek (inclusief [!DNL Adobe Experience Cloud], [!DNL Adobe Experience Platform] en [!DNL Target] publiek) tegelijk om een ad-hocpubliek te maken. U kunt ook uitsluitingsregels maken en het publiek uitsluiten van een regel.

>[!NOTE]
>
>De [!DNL Adobe Experience Platform]-bron bevindt zich in een bètatestprogramma, maar is beschikbaar voor alle [!DNL Target]-klanten die de [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) gebruiken. Publiek beschikbaar bij [!DNL Adobe Experience Platform] kan worden gebruikt zoals is of [gecombineerd met bestaand publiek](/help/c-target/combining-multiple-audiences.md).

Stel dat u een publiek hebt met de doelgroep &quot;Nieuwe bezoekers&quot; en een publiek met de doelgroep &quot;Chrome-gebruikers&quot;. Voor een specifieke activiteit, zou u deze bestaande publiek aan doelnieuwe bezoekers kunnen willen combineren gebruikend browsers van Chrome. In plaats van een derde publiek te maken en dit op te slaan in de [!UICONTROL Audiences]-bibliotheek, kunt u deze twee soorten publiek combineren tijdens het maken van activiteiten of tijdens het bewerken van een bestaande activiteit.

Als een ander voorbeeld, kunt u alle loyaliteitklanten richten. Bijvoorbeeld, kunt u een specifiek [!DNL Audience Manager] publiek voor loyaliteitsstatus omvatten en het combineren met een [!DNL Target] publiek dat uit mensen wordt samengesteld die voor uw loyaliteitsprogramma tijdens de huidige zitting hebben geregistreerd. Het combineren van deze twee soorten publiek is eenvoudiger dan het creëren van een derde, permanent publiek.

U kunt maximaal tien soorten publiek combineren met AND en OR.

U kunt een gecombineerd publiek op verschillende plaatsen door [!DNL Target] UI tot stand brengen en gebruiken.

## Een gecombineerd publiek maken tijdens het maken van een activiteit {#section_2F1CE9434CC04174B4BA2BFC89B85D77}

U kunt een ad hoc gecombineerd publiek op de pagina van [!UICONTROL Target] van de activiteit tijdens de drie-stap geleide werkschema tot stand brengen.

1. Tijdens het creëren van [activity](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op **[!UICONTROL Targeting]** pagina, klik de drie verticale ellipsen, dan klik **[!UICONTROL Replace Audience]**.

   ![Stap resultaat](assets/edit_audience.png)

1. Selecteer op de pagina [!UICONTROL Choose Audience] de selectievakjes naast het gewenste publiek dat u als bouwstenen voor uw gecombineerde publiek wilt gebruiken.

   Klik op de knop [!UICONTROL Filters] om uw zoekopdracht naar het gewenste publiek te verfijnen. U kunt het publiek filteren op de bron: ([!DNL Adobe Target], [!DNL Adobe Target Classic], [!DNL Experience Cloud], [!DNL Adobe Experience Platform] (bèta)).

   ![Stap resultaat](assets/combine_multiple_audiences1.png)

1. Klik op **[!UICONTROL Combine Audiences]** in de rechterbovenhoek.

   ![Stap resultaat](assets/combine_multiple_audiences2.png)

1. (Voorwaardelijk) Bewerk het nieuwe gecombineerde publiek naar wens.

   Met het dialoogvenster [!UICONTROL Edit Audience] kunt u extra elementen voor publieksopbouw vanaf de linkerkant naar het nieuwe gecombineerde publiek slepen. U kunt ook uitsluitingsregels toevoegen en soorten publiek uitsluiten.

   1. Gebruik de functie slepen en neerzetten om een publiek binnen een bestaande sectie toe te voegen als bouwsteen van niveau 2.

      Stel dat u in het vorige voorbeeld nu Safari-gebruikers wilt opnemen in het gecombineerde publiek. Zoek naar en sleep het publiek &quot;Safari Browser&quot;in de Browser van Firefox&quot;doos op de rechterkant, zoals in het volgende voorbeeld:

      ![](assets/combine_multiple_audiences3.png)

      De operator tussen het twee publiek van het browsertype is AND. Selecteer de vervolgkeuzelijst En en wijzig deze in &quot;OR&quot; om een nieuw, gecombineerd publiek te maken voor nieuwe bezoekers met Firefox of Safari. Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Het is bijvoorbeeld niet mogelijk dat iemand een pagina gelijktijdig bezoekt met Firefox en Safari.

      >[!NOTE]
      >
      >De operator (AND of OR) moet hetzelfde blijven als het publiek dat u combineert. U kunt operatoren niet mixen en koppelen.

   1. Als u een uitsluiting aan een regel wilt toevoegen, klikt u op **[!UICONTROL Exclude]**.

      ![](assets/combine_multiple_audiences3a.png)

      Sleep een publiek.

      Als u bijvoorbeeld Amerikaanse bezoekers wilt uitsluiten van nieuwe bezoekers, versleept u de Market: Amerikaanse publiek in de doos.

      Dit gecombineerde publiek omvat alle nieuwe bezoekers aan uw plaats (met uitzondering van die van San Francisco) gebruikend Safari of Firefox.

   1. Als u een publiek wilt uitsluiten van een regel, klikt u op **[!UICONTROL Exclusion]** > **[!UICONTROL Exclude this Audience.]**.

      U kunt bijvoorbeeld een gecombineerd publiek maken dat alle nieuwe bezoekers van uw site omvat, met uitzondering van bezoekers die Firefox gebruiken. Het uitsluiten van bezoekers die Firefox gebruiken is eenvoudiger en sneller dan het maken van een gecombineerd publiek dat expliciet meerdere browsers (Safari, Chrome en Internet Explorer) bevat, maar Firefox is niet inbegrepen.

1. Geef een beschrijvende naam op voor het gecombineerde publiek en klik op **[!UICONTROL Done]**.

## Een gecombineerd publiek maken voor gebruik bij metrische doelen {#section_A42E795AFCBD4575809C5942039910F0}

U kunt een ad hoc gecombineerd publiek op de pagina van [!UICONTROL Goals & Settings] van de activiteit tot stand brengen om in metrisch richten te gebruiken. Bijvoorbeeld om het richten tot stand te brengen die op omzetting gebruikend een gecombineerd publiek wordt gebaseerd:

1. Tijdens het uitgeven of het creëren van [activiteit](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03), op **[!UICONTROL Goals & Settings]** pagina, selecteer **[!UICONTROL Conversion]** voor succesmetrisch, dan uitgezocht **[!UICONTROL Viewed an Mbox]** als actie.
1. Selecteer de gewenste mbox in het **[!UICONTROL Search mbox]** gebied.

   ![](assets/combine_multiple_audiences4.png)

1. Klik op het tandwielpictogram en klik vervolgens op **[!UICONTROL Add Audience Targeting]**.
1. Klik op de koppeling **[!UICONTROL Add Audience/Targeting Condition]** om het dialoogvenster [!UICONTROL Choose Audience] weer te geven.

   ![](assets/combine_multiple_audiences5.png)

1. Ga met [Stap 2](/help/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;creeer een Gecombineerde Publiek terwijl het Creëren van een Activiteit&quot;om het gecombineerde publiek tot stand te brengen.

## Een gecombineerd publiek maken voor rapportage {#section_4682D342EFBB43C38E54B99B3A1E14CD}

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

   ![Configureren > Soorten publiek > Meerdere soorten publiek](assets/combine_multiple_audiences7.png)

1. Klik op het pictogram Meer opties (drie verticale ellipsen) naast het huidige publiek van de activiteit en klik vervolgens op **[!UICONTROL Change Audience]**.

   ![Publiek wijzigen](assets/combine_multiple_audiences8.png)

1. Ga met [Stap 2](/help/c-target/combining-multiple-audiences.md#section_2F1CE9434CC04174B4BA2BFC89B85D77) onder &quot;creeer een Gecombineerde Publiek terwijl het Creëren van een Activiteit&quot;om het gecombineerde publiek tot stand te brengen.
