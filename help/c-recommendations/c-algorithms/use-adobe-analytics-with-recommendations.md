---
keywords: gedragsgegevensbron;analyse;aanbevelingen;criteria;productvariabelen
description: Leren gebruiken [!DNL Adobe Analytics] as the behavioral data source to use the view-based and/or purchase-based behavioral data from [!DNL Analytics] in [!DNL Target Recommendations].
title: Hoe gebruikt u [!DNL Adobe Analytics] with [!DNL Target Recommendations]?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 2dc134d064b0707bcc8a24a08e9831e1cfa0b08e
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# ![PREMIUM](/help/assets/premium.png) Gebruiken [!DNL Adobe Analytics] with [!DNL Recommendations]

Gebruiken [!DNL Adobe Analytics] als de gegevensbron voor gedragsgegevens clients de op weergave en/of aankoop gebaseerde gedragsgegevens van [!DNL Analytics] in [!DNL Adobe Target] [!DNL Recommendations] activiteiten. Deze functie is vooral handig in situaties waarin de [!DNL Target Recommendations] de installatie is nieuw en [!DNL Analytics] beschikt over veel historische gegevens die moeten worden gebruikt.

Gebruiken [!DNL Analytics] aangezien de gegevensbron van het gedrag als rijke bron van informatie over gebruikersgedrag kan dienst doen. Deze informatie kan gegevens bevatten van een bron of feed van een derde die alleen wordt gedeeld met [!DNL Analytics].

while [criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in [!DNL Recommendations]Er zijn twee keuzerondjes waarmee u kunt kiezen welke gegevensbron moet worden gebruikt: [!UICONTROL mboxes] of [!UICONTROL Analytics]. Als u criteria wilt maken, klikt u op [!UICONTROL Recommendations] > [!UICONTROL Criteria] > [!UICONTROL Create Criteria] > [!UICONTROL Create Criteria]. Zie voor meer informatie [Criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md).

![Knoppen voor gegevensbron van gedrag](assets/behavioral-data-source.png)

>[!NOTE]
>
>Als deze twee knoppen niet worden weergegeven in uw account, kunt u het beste [Klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Gevallen gebruiken voor analysegegevens in Doel

Gebruiken [!DNL Analytics] als gegevensbron voor gedragsgegevens voor aanbevelingen laat u ook specifieke gebruiksgevallen zonder het vereiste van het etiketteren van entiteitspagina&#39;s met alle [!DNL Target] entiteitsparameters. Hoewel daarvoor bepaalde voorwaarden moeten gelden, is de beschikbaarheid van &quot;Productvariabelen&quot; voor die functionaliteit van essentieel belang om naadloos te kunnen werken. Reguliere eVars en Props zijn niet voldoende voor deze handshake om automatisch tussen te komen [!DNL Analytics] en [!DNL Target].

U kunt [!DNL Analytics] als gegevensbron voor gedragsgegevens:

* Geef op een detailhandelssite aanbevelingen weer voor gebruikers op een pagina met productdetails, gebaseerd op wat andere gebruikers in de laatste maand van dezelfde categorie hebben gekocht. Gebruik hiervoor [!DNL Analytics] gegevens.
* Geef inhoud op het beginscherm van een mediasite weer voor de populairste inhoud in een bepaalde categorie die momenteel wordt overgeschakeld, op basis van [!DNL Analytics] gegevens.

## Implementatie in [!DNL Analytics]

In de volgende secties kunt u deze functie implementeren op het tabblad [!DNL Analytics] zijde.

### Vereisten: productvariabelen instellen in [!DNL Analytics]

Productvariabelen implementeren in [!DNL Analytics] met de vereiste kenmerken waarvoor [!DNL Target Recommendations].

A [!DNL Target Recommendations] de voorbeeldvoederindeling dient als leidraad voor de definitie van alle kenmerken in de productvariabelen . Later moeten deze waarden worden &quot;toegewezen&quot; binnen de [!DNL Target] UI voor de respectieve [!DNL Target] entiteitswaarden.

>[!NOTE]
>
>Als het een inhoudssite is, moeten de respectievelijke inhoudsonderdelen worden behandeld als &quot;producten&quot; en de bijbehorende kenmerken over die inhoud worden doorgegeven als kenmerken. Dergelijke kenmerken kunnen de auteursnaam, publicatiedatum, inhoudstitel, maand van versie, enzovoort omvatten. Het bedrijf moet op basis van de gebruiksaanwijzing beslissen over de mate waarin een categorie of categorie in aanmerking komt.

Voor meer informatie over het instellen van productvariabelen raadpleegt u [producten](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) in de *Adobe Analytics implementeren* hulplijn. Sommige nota&#39;s in die documentatie hebben discretie van het team nodig dat het opstelt (voorbeeld: Categorie). Het wordt altijd aangeraden om [!DNL Adobe] voordat u deze activiteit uitvoert.

### Overwegingen

[!DNL Analytics] gegevens worden via een dagelijkse feed verzonden. Het kan 24 uur duren voordat de resultaten van het gedrag worden weergegeven in de resultaten van de aanbevelingen op uw site. Zoals bij alles [!DNL Recommendations] Deze gegevensbron kan en moet worden getest op criteria-instellingen.

Voor snelle besluitvorming over welke gegevensbron moet worden gebruikt, als er veel organische gegevens zijn die elke dag door gebruikers worden gegenereerd, en niet veel afhankelijkheid van historische gegevens, dan gebruikt u een [!DNL Target] mbox als gegevensbron voor gedrag kan een goede pasvorm zijn. In gevallen waarin de biologische gegevens die onlangs zijn gegenereerd, minder beschikbaar zijn, kunt u zich afvragen [!DNL Analytics] gegevens, dan het gebruiken [!DNL Analytics] aangezien de gegevensbron over gedrag een goede pasvorm is.

Nu is het tijd om deze variabelen toe te wijzen [!DNL Target] zijde voor continue levering van gedragsgegevens.

## Implementeren in [!DNL Target]

1. In [!DNL Target], klikt u op **[!UICONTROL Recommendations]** klikt u op de knop **[!UICONTROL Feeds]** tab.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klik op **[!UICONTROL Create Feed]**.

1. Selecteren **[!UICONTROL Analytics Classifications]** en geeft u vervolgens de rapportsuite op.

   ![Klassificaties voor analyse, optie](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klikken **[!UICONTROL Next]** aan **[!UICONTROL Schedule]** de instellingen, selecteert u een frequentieperiode voor de feed:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 weeks]
   * [!UICONTROL Never]

   U kunt ook de tijd van de dag selecteren waarop de feed moet worden verwerkt.

1. Klikken **[!UICONTROL Next]** aan  **[!UICONTROL Mapping]** instellingen, en wijs vervolgens de kolomkoppen van het veld toe aan de juiste [!UICONTROL Recommendations] veldnamen.

   ![Sectie Toewijzing](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klik op **[!UICONTROL Save]**.

## Veelgestelde vragen

Houd rekening met de volgende veelgestelde vragen wanneer u deze gebruikt [!DNL Analytics] with [!DNL Target]:

### zijn `entity.id` en `entity.categoryId` waarden die moeten worden doorgegeven binnen de [!DNL Target] mbox call?

Ja, die twee waarden zijn nog steeds vereist. De overige kenmerken kunnen worden doorgegeven via een [!DNL Analytics] feed, zoals beschreven in dit document.

### Kan ik dynamische inclusieregels gebruiken, zoals entiteitparameter past profielattributen gebruikend [!DNL Analytics] voederaanpak?

Ja, dat kan. De methode is vergelijkbaar bij gebruik [!DNL Target] zelfstandig. In dit geval moet u echter goed letten op de tijdsfactor. De entiteitvariabelen die met de profielvariabelen moeten aanpassen hangen van de gegevenslaag af die veel later op de pagina zou kunnen verschijnen.
