---
keywords: gedragsgegevensbron;analyse;aanbevelingen;criteria;productvariabelen
description: Leer hoe u Adobe Analytics kunt gebruiken als gegevensbron voor gedragingen om de op weergave gebaseerde en/of op aankoop gebaseerde gedragsgegevens van Analytics te gebruiken in [!DNL Target] Recommendations.
title: Hoe gebruik ik Adobe Analytics met [!DNL Target] Recommendations?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 2a4cae206bf634bf3fbec65c5c4b289aadefede1
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Adobe Analytics gebruiken met Recommendations

Gebruiken [!DNL Adobe Analytics] als de gegevensbron voor gedragsgegevens clients de op weergave en/of aankoop gebaseerde gedragsgegevens van [!DNL Analytics] in [!DNL Adobe Target] aanbevelingen. Deze functie is vooral handig in situaties waarin de [!DNL Target Recommendations] de installatie is nieuw en [!DNL Analytics] heeft veel historische gegevens om te gebruiken.

Gebruiken [!DNL Analytics] aangezien de gegevensbron van het gedrag als rijke bron van informatie over gebruikersgedrag kan dienst doen. Dit kunnen gegevens zijn van een bron of feed van een derde die alleen met [!DNL Analytics].

while [criteria maken](/help/c-recommendations/c-algorithms/create-new-algorithm.md) In Recommendations zijn er twee keuzerondjes waarmee u kunt kiezen welke gegevensbron u wilt gebruiken: [!UICONTROL mboxes] of [!UICONTROL Analytics].

![Knoppen voor gegevensbron van gedrag](assets/behavioral-data-source.png)

>[!NOTE]
>
>Als deze twee knoppen niet worden weergegeven in uw account, kunt u het beste [Klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Gevallen gebruiken voor analysegegevens in Doel

Gebruiken [!DNL Analytics] als gedragsgegevensbron voor aanbevelingen ook de capaciteit verstrekt om specifieke gebruiksgevallen zonder het vereiste van het etiketteren van entiteitspagina&#39;s van alle te gebruiken [!DNL Target] entiteitsparameters. Hoewel daarvoor bepaalde voorwaarden moeten gelden, is de beschikbaarheid van &quot;Productvariabelen&quot; voor die functionaliteit van essentieel belang om naadloos te kunnen werken. Reguliere eVars en Props zijn niet voldoende voor deze handshake om automatisch tussen te komen [!DNL Analytics] en [!DNL Target].

U kunt [!DNL Analytics] als gegevensbron voor gedragsgegevens:

* Geef met behulp van analysegegevens op een detailhandelssite aanbevelingen weer voor gebruikers op een PDP-pagina op basis van de gegevens die andere gebruikers in de laatste maand van dezelfde categorie hebben gekocht.
* Geef inhoud op het beginscherm van een mediasite weer voor de populairste inhoud in een bepaalde categorie die momenteel wordt overgeschakeld, op basis van [!DNL Analytics] gegevens.

## Implementatie in Analytics

In de volgende secties kunt u deze functie implementeren op het tabblad [!DNL Analytics] zijde.

### Vereisten: productvariabelen instellen in Analytics

U moet productvariabelen implementeren in [!DNL Analytics] met de vereiste kenmerken waarvoor [!DNL Target Recommendations].

A [!DNL Target Recommendations] de voorbeeldvoederindeling zal als leidraad dienen voor de definitie van alle kenmerken in de productvariabelen . Later moeten deze waarden worden &quot;toegewezen&quot; binnen de [!DNL Target] UI voor de respectieve [!DNL Target] entiteitswaarden.

>[!NOTE]
>
>Als het een inhoudssite is, moeten de respectievelijke inhoudsonderdelen worden behandeld als &quot;producten&quot; en de bijbehorende kenmerken voor die inhoud (bijvoorbeeld: naam van auteur, publicatiedatum, titel van inhoud, maand van release, enz.) moet worden doorgegeven als kenmerken. Het bedrijf moet op basis van de gebruiksaanwijzing beslissen over de mate waarin een categorie of categorie in aanmerking komt.

Voor meer informatie over het instellen van productvariabelen raadpleegt u [producten](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) in de *Handleiding voor analytische implementatie*. Sommige nota&#39;s in die documentatie hebben discretie van het team nodig dat het opstelt (voorbeeld: Categorie). Het wordt altijd aangeraden om met Adobe te overleggen voordat u deze activiteit uitvoert.

### Overwegingen

[!DNL Analytics] gegevens worden via een dagelijkse feed verzonden. Gedragresultaten nemen tot 24 uur in beslag om weerspiegeld te worden in de resultaten van de aanbevelingen op uw site. Zoals bij alles [!DNL Recommendations] Deze gegevensbron kan en moet worden getest op criteria-instellingen.

Voor snelle besluitvorming over welke gegevensbron moet worden gebruikt, als er veel biologische gegevens zijn die dagelijks door gebruikers worden gegenereerd, en niet veel afhankelijkheid van historische gegevens, dan gebruikt u een [!DNL Target] mbox als gegevensbron voor gedrag kan een goede pasvorm zijn. In gevallen waarin de biologische gegevens die onlangs zijn gegenereerd, minder beschikbaar zijn, kunt u zich afvragen [!DNL Analytics] gegevens, dan het gebruiken [!DNL Analytics] aangezien de gegevensbron over gedrag een goede pasvorm is.

Nu is het tijd om deze variabelen toe te wijzen [!DNL Target] zijde voor continue levering van gedragsgegevens.

## Implementeren in doel

1. Klik in Doel op **[!UICONTROL Recommendations]** klikt u op de knop **[!UICONTROL Feeds]** tab.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klik op **[!UICONTROL Create Feed]**.

1. Selecteren **[!UICONTROL Analytics Classifications]** en geeft u vervolgens de rapportsuite op.

   ![Klassificaties voor analyse, optie](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klikken **[!UICONTROL Mapping]** en geeft u vervolgens de kolomkoppen van het veld toe aan de juiste kolomkoppen [!UICONTROL Recommendations] veldnamen.

   ![Sectie Toewijzing](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klik op **[!UICONTROL Save]**.

## Veelgestelde vragen

Houd rekening met de volgende veelgestelde vragen wanneer u deze gebruikt [!DNL Analytics] with [!DNL Target]:

### zijn `entity.id` en `entity.categoryId` waarden die moeten worden doorgegeven binnen de [!DNL Target] mbox call?

Ja, die twee waarden zijn nog steeds vereist. De overige kenmerken kunnen worden doorgegeven via een [!DNL Analytics] feed, zoals beschreven in dit document.

### Kan ik dynamische inclusieregels gebruiken, zoals entiteitparameter past profielattributen gebruikend [!DNL Analytics] voederaanpak?

Ja, dat kan. De methode is vergelijkbaar bij gebruik [!DNL Target] zelfstandig. In dit geval moet u echter rekening houden met de tijdsfactor. De entiteitvariabelen die met de profielvariabelen zouden moeten aanpassen zijn afhankelijk van de gegevenslaag die veel later op de pagina zou kunnen verschijnen.
