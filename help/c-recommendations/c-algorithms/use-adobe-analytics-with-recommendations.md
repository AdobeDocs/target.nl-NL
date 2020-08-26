---
keywords: behavioral data source;analytics;recommendations;criteria;product variables
description: Als u Adobe Analytics gebruikt als gegevensbron voor gedragsgegevens, kunnen clients de op weergaven gebaseerde en/of op aanschaf gebaseerde gedragsgegevens van Analytics in Adobe Recommendations gebruiken.
title: Adobe Analytics gebruiken met Target Recommendations
feature: criteria
translation-type: tm+mt
source-git-commit: abe28722199c74c8b57dbfd0ca893dbf2e862cad
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# Adobe Analytics gebruiken met Recommendations

Als u [!DNL Adobe Analytics] de gegevensbron voor gedrag gebruikt, kunnen clients de op weergave gebaseerde en/of op aankoop gebaseerde gedragsgegevens uit [!DNL Analytics] in [!DNL Adobe Target] aanbevolen activiteiten gebruiken. Deze functie is vooral handig in situaties waarin de [!DNL Target Recommendations] installatie nieuw is en veel historische gegevens [!DNL Analytics] bevat die u kunt gebruiken.

Het gebruiken [!DNL Analytics] als gedragsgegevensbron kan als rijke bron van informatie over gebruikersgedrag dienst doen. Dit kunnen gegevens bevatten van een bron of feed van een derde die alleen met [!DNL Analytics]wordt gedeeld.

Bij het [maken van criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md) in Recommendations zijn er twee keuzerondjes waarmee u kunt kiezen welke gegevensbron moet worden gebruikt: [!UICONTROL mboxes] of [!UICONTROL Analytics].

![Knoppen voor gegevensbron van gedrag](/help/c-recommendations/c-algorithms/assets/behavioral-data-source.png)

>[!NOTE]
>
>Als deze twee knoppen niet worden weergegeven in uw account, neemt u contact op met de [klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Gevallen gebruiken

Het gebruiken [!DNL Analytics] als gedragsgegevensbron voor aanbevelingen verstrekt ook de capaciteit om specifieke gebruiksgevallen zonder het vereiste van het etiketteren van entiteitpagina&#39;s van alle [!DNL Target] entiteitsparameters op te stellen. Hoewel daarvoor bepaalde voorwaarden moeten gelden, is de beschikbaarheid van &quot;Productvariabelen&quot; voor die functionaliteit van essentieel belang om naadloos te kunnen werken. Reguliere eVars en Props zijn niet voldoende voor deze handdruk om automatisch tussen [!DNL Analytics] en [!DNL Target]te gebeuren.

U kunt als gegevensbron voor gedrag gebruiken [!DNL Analytics] :

* Geef met behulp van analysegegevens op een detailhandelssite aanbevelingen weer voor gebruikers op een PDP-pagina op basis van de gegevens die andere gebruikers in de laatste maand van dezelfde categorie hebben gekocht.
* Geef op het beginscherm van een mediasite inhoud weer voor de populairste inhoud in een bepaalde categorie die momenteel wordt doorlopen, op basis van [!DNL Analytics] gegevens.

## Implementatie in Analytics

De volgende secties zullen u helpen deze eigenschap op de [!DNL Analytics] kant uitvoeren.

### Vereisten: productvariabelen in Analytics

U moet productvariabelen in [!DNL Analytics] met de noodzakelijke attributen uitvoeren die voor worden vereist [!DNL Target Recommendations].

Een [!DNL Target Recommendations] voorbeeldvoederindeling zal dienen als leidraad voor de definitie van alle kenmerken in de productvariabelen. Later moeten deze waarden binnen de [!DNL Target] gebruikersinterface worden &quot;toegewezen&quot; voor de respectieve [!DNL Target] entiteitwaarden.

>[!NOTE]
>
>Als het een inhoudssite is, moeten de respectievelijke inhoudsonderdelen worden behandeld als &quot;producten&quot; en de bijbehorende kenmerken voor die inhoud (bijvoorbeeld: naam van auteur, publicatiedatum, titel van inhoud, maand van release, enz.) moet worden doorgegeven als kenmerken. Het bedrijf moet op basis van de gebruiksaanwijzing beslissen over de mate waarin een categorie of categorie in aanmerking komt.

Raadpleeg de [producten](https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/products.html) in de *handleiding* Analytics Implementation voor meer informatie over het instellen van productvariabelen. Sommige nota&#39;s in die documentatie hebben discretie van het team nodig dat het opstelt (voorbeeld: Categorie). Het wordt altijd aangeraden om met Adobe te overleggen voordat u deze activiteit uitvoert.

### Overwegingen

[!DNL Analytics] gegevens worden via een dagelijkse feed verzonden. Gedragresultaten nemen tot 24 uur in beslag om te worden weergegeven in de resultaten van de aanbevelingen op uw site. Net als bij alle [!DNL Recommendations] criteria kan en moet deze gegevensbron worden getest.

Voor snelle besluitvorming over welke gegevensbron moet worden gebruikt, als er veel organische gegevens zijn die elke dag door gebruikers worden gegenereerd, en niet veel afhankelijkheid van historische gegevens, dan kan het gebruiken van een [!DNL Target] box als gedragsgegevensbron een goede pasvorm zijn. In gevallen van minder beschikbaarheid van onlangs gegenereerde organische gegevens, als u op [!DNL Analytics] gegevens wilt bankieren, dan is het gebruiken [!DNL Analytics] als gedragsgegevensbron een goed pasvorm.

### Stappen om te implementeren

Ervan uitgaande dat alle voorwaarden aanwezig zijn, voert u de volgende taken uit:

1. Klik [!DNL Target]in **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** om uw [!DNL Target] clientcode aan te schaffen.

   ![Clientcode](/help/c-recommendations/c-algorithms/assets/client-code.png)

1. Verkrijg uw [!DNL Analytics] rapportsuite.

   Gebruik de rapportsuite van uw [!DNL Analytics] productiesite. Dit is de rapportsuite die de site bijhoudt waarin u de site hebt [!DNL Recommendations] geïmplementeerd.

1. Klik [!DNL Analytics]in **[!UICONTROL Admin]** > **[!UICONTROL Data Feeds]**.

   ![Setup > Data feeds](/help/c-recommendations/c-algorithms/assets/data-feed.png)

1. Klik **[!UICONTROL Add]** om een nieuwe feed te maken.

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
   >Raadpleeg het [!DNL Adobe Analytics] team voordat u deze stap uitvoert.

   * **Type**: VFTP
   * **Host**: xxx.yyy.com
   * **Pad**: Uw doelclientcode
   * **Gebruikersnaam**: xxxyy
   * **Wachtwoord**: xxxxxxxxxxx

   Screenshot is alleen ter referentie. Uw implementatie heeft andere referenties. Raadpleeg het [!DNL Adobe Analytics] team of de klantenservice tijdens deze stap.

   ![Doelsectie](/help/c-recommendations/c-algorithms/assets/destination.png)

1. Vul de **[!UICONTROL Data Column]** definities in:

   * **Compressie-indeling**: Gzip
   * **Verpakkingstype**:  Eén bestand
   * **Manifest:** Bestand voltooien

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

Met dit, is de opstelling aan [!DNL Analytics] kant volledig. Nu is het tijd om deze variabelen [!DNL Target] naast elkaar toe te wijzen voor continue levering van gedragsgegevens.

## Implementatie in doel

1. Klik in Doel **[!UICONTROL Recommendations]** en klik vervolgens op het **[!UICONTROL Feeds]** tabblad.

   ![Feeds](/help/c-recommendations/c-algorithms/assets/feeds-tab.png)

1. Klik op **[!UICONTROL Create Feed]**.

1. Selecteer **[!UICONTROL Analytics Classifications]**, dan specificeer de rapportreeks.

   ![Klassificaties voor analyse, optie](/help/c-recommendations/c-algorithms/assets/analytics-classifications.png)

1. Klik **[!UICONTROL Mapping]** en wijs de kolomkoppen van het veld toe aan de juiste [!UICONTROL Recommendations] veldnamen.

   ![Sectie Toewijzing](/help/c-recommendations/c-algorithms/assets/mapping.png)

1. Klik op **[!UICONTROL Save]**.