---
keywords: gedragsgegevensbron;analyse;aanbevelingen;criteria;productvariabelen
description: Leer hoe u Adobe Analytics gebruikt als gegevensbron voor gedragsgegevens om de op weergave gebaseerde en/of op aankoop gebaseerde gedragsgegevens van Analytics in [!DNL Target] Recommendations te gebruiken.
title: Hoe gebruik ik Adobe Analytics met [!DNL Target] Recommendations?
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 0%

---

# Adobe Analytics gebruiken met Recommendations

Door [!DNL Adobe Analytics] als gegevensbron voor gedrag te gebruiken, kunnen clients de op weergave gebaseerde en/of op aankoop gebaseerde gedragsgegevens van [!DNL Analytics] gebruiken in [!DNL Adobe Target]-aanbevelingen. Deze functie is vooral handig in situaties waarin de [!DNL Target Recommendations]-instelling nieuw is en [!DNL Analytics] veel historische gegevens heeft om te gebruiken.

Het gebruik van [!DNL Analytics] als gegevensbron voor gedrag kan als rijke bron van informatie over gebruikersgedrag dienst doen. Dit kunnen gegevens bevatten van een bron of feed van een derde die alleen met [!DNL Analytics] wordt gedeeld.

Terwijl [criteria creëren](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations, zijn er twee radioknopen die u laten kiezen welke gegevensbron moet worden gebruikt: [!UICONTROL mboxes] of [!UICONTROL Analytics].

![Knoppen voor gegevensbron van gedrag](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Als deze twee knoppen niet worden weergegeven in uw account, kunt u [Klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) raadplegen.

## Gevallen gebruiken voor analysegegevens in Doel

Als u [!DNL Analytics] gebruikt als gegevensbron voor gedragsgegevens voor aanbevelingen, kunt u ook specifieke gebruiksgevallen implementeren zonder dat u entiteitspagina&#39;s moet coderen met alle parameters van [!DNL Target]. Hoewel daarvoor bepaalde voorwaarden moeten gelden, is de beschikbaarheid van &quot;Productvariabelen&quot; voor die functionaliteit van essentieel belang om naadloos te kunnen werken. Reguliere eVars en Props zijn onvoldoende voor deze handshake om automatisch tussen [!DNL Analytics] en [!DNL Target] te gebeuren.

U kunt [!DNL Analytics] gebruiken als gegevensbron voor gedrag aan:

* Geef met behulp van analysegegevens op een detailhandelssite aanbevelingen weer voor gebruikers op een PDP-pagina op basis van de gegevens die andere gebruikers in de laatste maand van dezelfde categorie hebben gekocht.
* Geef op het beginscherm van een mediasite inhoud weer voor de populairste inhoud in een bepaalde categorie die momenteel wordt doorlopen, op basis van [!DNL Analytics]-gegevens.

## Implementatie in Analytics

De volgende secties zullen u helpen deze eigenschap op de [!DNL Analytics] kant uitvoeren.

### Vereisten: productvariabelen instellen in Analytics

U moet productvariabelen in [!DNL Analytics] met de noodzakelijke attributen uitvoeren die voor [!DNL Target Recommendations] worden vereist.

Een [!DNL Target Recommendations]-voorbeeldvoederindeling fungeert als leidraad voor het definiëren van alle kenmerken in de productvariabelen. Later moeten deze waarden worden &quot;toegewezen&quot; binnen de interface [!DNL Target] voor de respectievelijke entiteitswaarden [!DNL Target].

>[!NOTE]
>
>Als het een inhoudssite is, moeten de respectievelijke inhoudsonderdelen worden behandeld als &quot;producten&quot; en de bijbehorende kenmerken voor die inhoud (bijvoorbeeld: naam van auteur, publicatiedatum, titel van inhoud, maand van release, enz.) moet worden doorgegeven als kenmerken. Het bedrijf moet op basis van de gebruiksaanwijzing beslissen over de mate waarin een categorie of categorie in aanmerking komt.

Zie [products](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html) in de *Implementatiegids voor Analytics* voor meer informatie over het instellen van productvariabelen. Sommige nota&#39;s in die documentatie hebben discretie van het team nodig dat het opstelt (voorbeeld: Categorie). Het wordt altijd aangeraden om met Adobe te overleggen voordat u deze activiteit uitvoert.

### Overwegingen

[!DNL Analytics] gegevens worden via een dagelijkse feed verzonden. Gedragresultaten nemen tot 24 uur in beslag om te worden weergegeven in de resultaten van de aanbevelingen op uw site. Zoals bij alle [!DNL Recommendations] criteria montages, kan en zou deze gegevensbron moeten worden getest.

Voor snelle besluitvorming over welke gegevensbron moet worden gebruikt, als er veel organische gegevens zijn die elke dag door gebruikers worden geproduceerd, en niet veel afhankelijkheid die op historische gegevens wordt vereist, dan kan het gebruiken van een [!DNL Target] mbox als gedragsgegevensbron een goede pasvorm zijn. In gevallen van minder beschikbaarheid van onlangs gegenereerde organische gegevens, als u op [!DNL Analytics] gegevens wilt registreren, dan is het gebruiken [!DNL Analytics] als gedragsgegevensbron een goede pasvorm.

Nu is het tijd om deze variabelen aan de zijde [!DNL Target] in kaart te brengen voor ononderbroken levering van gedragsgegevens.

## Implementeren in doel

1. Klik in Doel op **[!UICONTROL Recommendations]** en klik vervolgens op het tabblad **[!UICONTROL Feeds]**.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klik op **[!UICONTROL Create Feed]**.

1. Selecteer **[!UICONTROL Analytics Classifications]**, dan specificeer de rapportreeks.

   ![Klassificaties voor analyse, optie](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klik **[!UICONTROL Mapping]**, dan kaart de kopballen van de gebiedskolom aan de aangewezen [!UICONTROL Recommendations] gebiedsnamen.

   ![Sectie Toewijzing](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klik op **[!UICONTROL Save]**.

## Veelgestelde vragen

Overweeg de volgende FAQs aangezien u [!DNL Analytics] met [!DNL Target] gebruikt:

### Zijn de `entity.id` en `entity.categoryId` waarden vereist om binnen [!DNL Target] mbox vraag worden overgegaan?

Ja, die twee waarden zijn nog steeds vereist. De overige kenmerken kunnen worden doorgegeven via een [!DNL Analytics]-feed, zoals in dit document wordt beschreven.

### Kan ik dynamische inclusieregels, zoals de attributen van de entiteitparameter gebruiken profielattributen gebruikend de [!DNL Analytics] voederbenadering?

Ja, dat kan. De methode is vergelijkbaar bij gebruik van [!DNL Target] op zelfstandige basis. In dit geval moet u echter rekening houden met de tijdsfactor. De entiteitvariabelen die met de profielvariabelen zouden moeten aanpassen zijn afhankelijk van de gegevenslaag die veel later op de pagina zou kunnen verschijnen.
