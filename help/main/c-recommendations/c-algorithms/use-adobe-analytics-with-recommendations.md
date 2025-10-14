---
keywords: gedragsgegevensbron;analyse;aanbevelingen;criteria;productvariabelen
description: Leer hoe te om  [!DNL Adobe Analytics]  als gedragsgegevensbron in  [!DNL Target Recommendations] te gebruiken.
title: Hoe gebruik ik  [!DNL Adobe Analytics]  met  [!DNL Target Recommendations]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: d2b7e840-9546-4a8e-bec4-1ebea5a79672
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# [!DNL Adobe Analytics] gebruiken met [!DNL Recommendations]

Als u [!DNL Adobe Analytics] gebruikt als gegevensbron voor gedragingen, kunnen clients de op weergave gebaseerde en op aankoop gebaseerde gedragsgegevens uit [!DNL Analytics] in [!DNL Adobe Target Recommendations] -activiteiten gebruiken. Deze functie is vooral handig in situaties waarin de [!DNL Target Recommendations] -instelling nieuw is en [!DNL Analytics] veel historische gegevens kan gebruiken.

Het gebruik van [!DNL Analytics] als de gegevensbron voor gedragingen kan fungeren als een rijke bron van informatie over het gedrag van gebruikers. Deze informatie kan gegevens bevatten van een bron of feed van een derde die alleen met [!DNL Analytics] wordt gedeeld.

Terwijl [&#x200B; creërend criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) in [!DNL Recommendations], zijn er twee radioknopen die u laten kiezen welke gegevensbron moet worden gebruikt: [!UICONTROL mboxes] of [!UICONTROL Analytics]. Klik op [!UICONTROL Recommendations] > [!UICONTROL Criteria] > [!UICONTROL Create Criteria] > [!UICONTROL Create Criteria] om criteria te maken. Voor meer informatie, zie [&#x200B; criteria &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md) creëren.

>[!NOTE]
>
>Als deze twee knopen niet in uw rekening tonen, reik uit aan [&#x200B; de Zorg van de Klant &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Gevallen gebruiken voor [!DNL Analytics] -gegevens in [!DNL Target]

Als u [!DNL Analytics] gebruikt als gegevensbron voor gedragsgegevens voor aanbevelingen, kunt u ook specifieke gebruiksgevallen implementeren zonder dat u entiteitspagina&#39;s met alle parameters van [!DNL Target] moet coderen. Hoewel daarvoor bepaalde voorwaarden moeten gelden, is de beschikbaarheid van &quot;Productvariabelen&quot; voor die functionaliteit van essentieel belang om naadloos te kunnen werken. Deze handdruk kan alleen automatisch plaatsvinden tussen [!DNL Analytics] en [!DNL Target] als Reguliere eVars en Props beschikbaar zijn.

U kunt [!DNL Analytics] als gegevensbron voor gedrag gebruiken:

* Geef op een detailhandelssite aanbevelingen weer voor gebruikers op een productdetailpagina, gebaseerd op wat andere gebruikers de laatste maand van dezelfde categorie hebben gekocht, met behulp van [!DNL Analytics] -gegevens.
* Geef op het beginscherm van een mediasite inhoud weer voor de populairste inhoud in een bepaalde categorie die momenteel wordt doorlopen, op basis van [!DNL Analytics] -gegevens.

## Implementatie in [!DNL Analytics]

In de volgende secties vindt u informatie over het implementeren van deze functie aan de [!DNL Analytics] zijde.

### Vereisten: productvariabelen instellen in [!DNL Analytics]

Productvariabelen implementeren in [!DNL Analytics] met de benodigde kenmerken die vereist zijn voor [!DNL Target Recommendations] .

Een [!DNL Target Recommendations] -voorbeeldvoederindeling fungeert als leidraad voor het definiëren van alle kenmerken in de productvariabelen. Later moeten deze waarden binnen de gebruikersinterface van [!DNL Target] worden &quot;toegewezen&quot; voor de respectievelijke entiteitswaarden van [!DNL Target] .

>[!NOTE]
>
>Als het een inhoudssite is, moeten de respectievelijke inhoudsonderdelen worden behandeld als &quot;producten&quot; en de bijbehorende kenmerken over die inhoud worden doorgegeven als kenmerken. Dergelijke kenmerken kunnen de auteursnaam, publicatiedatum, inhoudstitel, maand van versie, enzovoort omvatten. Het bedrijf moet op basis van de gebruiksaanwijzing beslissen over de mate waarin een categorie of categorie in aanmerking komt.

Voor meer details op hoe te opstellings productvariabelen, zie [&#x200B; producten &#x200B;](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/products.html?lang=nl-NL) in *Adobe Analytics* gids uitvoeren. Sommige nota&#39;s in die documentatie hebben behoefte aan discretie van het team dat het opstelt (voorbeeld: Categorie). Het wordt altijd aangeraden [!DNL Adobe] te raadplegen voordat u deze activiteit uitvoert.

### Overwegingen

[!DNL Analytics] -gegevens worden verzonden via een dagelijkse feed. Het kan 24 uur duren voordat de resultaten van het gedrag worden weerspiegeld in de resultaten van de aanbevelingen op uw site. Net als bij alle criteria-instellingen van [!DNL Recommendations] , kan en moet deze gegevensbron worden getest.

Voor snelle besluitvorming over welke gegevensbron moet worden gebruikt, als er veel organische gegevens zijn die elke dag door gebruikers worden gegenereerd, en niet veel afhankelijkheid van historische gegevens, dan kan het gebruiken van een [!DNL Target] box als gedragsgegevensbron een goede pasvorm zijn. Als er minder biologische gegevens beschikbaar zijn die onlangs zijn gegenereerd, en u wilt [!DNL Analytics] -gegevens gebruiken, is het gebruik van [!DNL Analytics] als gegevensbron voor gedrag een goede oplossing.

Nu is het tijd om deze variabelen aan de [!DNL Target] kant in kaart te brengen voor ononderbroken levering van gedragsgegevens.

## Implementeren in [!DNL Target]

1. Klik in [!DNL Target] op **[!UICONTROL Recommendations]** en klik vervolgens op de tab **[!UICONTROL Feeds]** .

1. Klik op **[!UICONTROL Create Feed]**.

1. Selecteer **[!UICONTROL Analytics Classifications]** en geef vervolgens de rapportsuite op.

1. Klik op **[!UICONTROL Next]** om naar de instellingen van **[!UICONTROL Schedule]** te gaan en selecteer een frequentieperiode voor de feed:

   * [!UICONTROL Daily]
   * [!UICONTROL Weekly]
   * [!UICONTROL Every 2 weeks]
   * [!UICONTROL Never]

   U kunt ook de tijd van de dag selecteren waarop de feed moet worden verwerkt.

1. Klik op **[!UICONTROL Next]** om naar de **[!UICONTROL Mapping]** -instellingen te gaan en wijs vervolgens de kolomkoppen van het veld toe aan de desbetreffende [!UICONTROL Recommendations] -veldnamen.

1. Klik op **[!UICONTROL Save]**.

## Veelgestelde vragen

Houd rekening met de volgende veelgestelde vragen wanneer u [!DNL Analytics] gebruikt met [!DNL Target] :

### Zijn de waarden `entity.id` en `entity.categoryId` vereist om binnen de [!DNL Target] mbox vraag worden overgegaan?

Ja, die twee waarden zijn nog steeds vereist. De overige kenmerken kunnen via een [!DNL Analytics] -feed worden doorgegeven, zoals in dit document wordt beschreven.

### Kan ik dynamische inclusieregels gebruiken, zoals de parameter van de entiteit past profielattributen gebruikend de [!DNL Analytics] voederbenadering aan?

Ja, dat kan. De methode is vergelijkbaar wanneer u [!DNL Target] op zichzelf gebruikt. In dit geval moet u echter goed letten op de tijdsfactor. De entiteitvariabelen die met de profielvariabelen moeten aanpassen hangen van de gegevenslaag af die veel later op de pagina zou kunnen verschijnen.
