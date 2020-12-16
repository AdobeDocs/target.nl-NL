---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Als u Adobe Analytics gebruikt als gegevensbron voor gedragsgegevens, kunnen clients de op weergaven gebaseerde en/of op aanschaf gebaseerde gedragsgegevens van Analytics in Adobe Recommendations gebruiken.
title: Adobe Analytics gebruiken met Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '1000'
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

### Stappen om te implementeren

Ervan uitgaande dat aan alle voorwaarden is voldaan, moeten de volgende taken door het team van [!DNL Adobe Target Recommendations] worden uitgevoerd:

>[!IMPORTANT]
>
>De onderstaande stappen dienen slechts ter illustratie. Een lid van het [!DNL Recommendations] team moet deze stappen momenteel uitvoeren. [Neem contact op met de ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) klantenservice voor meer informatie.

1. Klik in [!DNL Target] op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** om uw [!DNL Target]-clientcode aan te schaffen.

   ![Clientcode](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. Verkrijg uw [!DNL Analytics] rapportsuite.

   Gebruik uw [!DNL Analytics] rapportenpakket van de productiesite. Dit is de rapportsuite die de site bijhoudt waarin u [!DNL Recommendations] hebt geïmplementeerd.

1. Klik in [!DNL Analytics] op **[!UICONTROL Admin]** > **[!UICONTROL Data Feeds]**.

   ![Setup > Data feeds](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Klik **[!UICONTROL Add]** om een nieuwe voer tot stand te brengen.

   ![Feed toevoegen](/help/c-recommendations/c-algorithms/assets/add-feed.png)

1. Voer de gegevens in:

   * **Naam**: Recs Prod Feed
   * **Rapportsuite**: Uw vooraf bepaalde rapportsuite
   * **E-mail**: Geef een geschikt adres voor een Admin-gebruiker op
   * **Diervoederinterval**: Selecteer het gewenste interval
   * **Vertraging**: Geen vertraging.
   * **Begin- en einddatum**: Doorlopende diervoeders

   ![Sectie met informatie over diervoeders](/help/c-recommendations/c-algorithms/assets/feed-information.png)

1. Vul de details in de **[!UICONTROL Destination]** sectie in:

   >[!NOTE]
   > 
   >Raadpleeg het [!DNL Adobe Analytics]-team voordat u deze stap uitvoert.

   * **Type**: FTP
   * **Host**:  `xxx.yyy.com`
   * **Pad**: Uw  [!DNL Target] clientcode
   * **Gebruikersnaam**: Geef uw gebruikersnaam op
   * **Wachtwoord**: Geef uw wachtwoord op

   Screenshot is alleen ter referentie. Uw implementatie heeft andere referenties. Raadpleeg het [!DNL Adobe Analytics]-team of de klantenservice tijdens deze stap.

   ![Doelsectie](/help/c-recommendations/c-algorithms/assets/destination.png)

1. Vul de **[!UICONTROL Data Column]** definities in:

   * **Compressie-indeling**: Gzip
   * **Verpakkingstype**: Eén bestand
   * **manifest:bestand** voltooien

      ![Compressie-indeling, Type pakket en Manifest-instellingen](/help/c-recommendations/c-algorithms/assets/compression.png)

   * **Opgenomen kolommen**:

      >[!IMPORTANT]
      >
      >De kolommen moeten worden toegevoegd in dezelfde volgorde die hier wordt beschreven. Selecteer de kolommen in de volgende volgorde en klik **[!UICONTROL Add]** voor elke kolom.

      * hit_time_gmt
      * visid_high
      * visid_low
      * event_list
      * product_list
      * visit_num

1. Klik op **[!UICONTROL Save]**.

   ![Sectie met definities van gegevenskolommen](/help/c-recommendations/c-algorithms/assets/data-column-definitions.png)

Hierdoor is de installatie aan de zijde [!DNL Analytics] voltooid. Nu is het tijd om deze variabelen aan de zijde [!DNL Target] in kaart te brengen voor ononderbroken levering van gedragsgegevens.

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

