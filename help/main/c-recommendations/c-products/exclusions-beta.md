---
keywords: uitsluitingen
description: Leer hoe u uitsluitingen kunt maken in [!DNL Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen.
title: Hoe gebruik ik uitsluitingen in [!UICONTROL Recommendations] Activiteiten?
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 31cf23a52c331eabad0e5f6423eeeca84df87625
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Uitsluitingen

Een uitsluiting maken in [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen. Een uitsluiting is een subset van producten of inhoud die niet aan bezoekers mag worden aanbevolen.

De uitsluitingen zijn beschikbaar over de volledige rekening. In tegenstelling tot verzamelingen, waarin u een specifieke verzameling opgeeft voor elke ervaring terwijl u een [!UICONTROL Recommendations] activiteiten, zijn uitsluitingen van toepassing op alle activiteiten over de gehele rekening. Er is geen optie om een uitsluitingsgroep toe te wijzen tijdens het maken van activiteiten.

Enkele voorbeelden van de tijden u uitsluitingen zou gebruiken omvatten:

* Producten die zijn stopgezet.
* De catalogus Herfst en Winter is nu de enige catalogus die online aanwezig moet zijn. Elk item uit de zomercatalogus kan niet meer worden aangeschaft.
* Items die op de meeste pagina&#39;s of schermen (volwassen producten, NC-17-films enzovoort) niet kunnen worden aanbevolen.
* Producten met onvolledige metagegevensvelden (ontbrekende miniatuur, prijs of andere belangrijke metagegevens).
* Producten die nooit zouden moeten worden geadviseerd (misschien bestaat SKU in het systeem voor iets maar het is geen koopbaar voorwerp. Of misschien is het een nepSKU voor het QA-team om een aankoop te simuleren zonder iets te bestellen, enzovoort).

>[!IMPORTANT]
>
>Uitsluitingsregels worden globaal toegepast op alle [omgevingen](/help/main/administrating-target/environments.md).
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruiksscenario&#39;s, zie [Dynamische en statische insluitingsregels gebruiken](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Een uitsluiting maken

1. Klikken **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** de lijst van bestaande uitsluitingen weer te geven.

   ![exclusies_list-afbeelding](assets/exclusions-list.png)

   Het gerapporteerde &quot;Aantal posten&quot; voor elke uitsluiting op de [!UICONTROL Exclusions] lijstmening is het aantal producten die de regels voor die uitsluiting binnen de gevormde standaardRecommendations aanpassen [hostgroep](/help/main/administrating-target/hosts.md) (milieu). Zie [Plan en implementeer [!DNL Recommendations]](https://experienceleague.adobe.com/en/docs/target-dev/developer/recommendations){target=_blank} in de *Adobe Target Developer Guide* voor informatie over hoe te om de standaardgastheergroep te veranderen.

1. (Voorwaardelijk) Klik op de knop [!UICONTROL Filter] pictogram, kies dan het gewenste [milieu](/help/main/administrating-target/environments.md) van de **[!UICONTROL Environment]** vervolgkeuzelijst tijdens het maken (of bijwerken) van een uitsluiting om de inhoud van de uitsluiting in die omgeving voor te vertonen. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Uitsluiting maken](/help/main/c-recommendations/c-products/assets/choose-environment.png)

1. Klik op **[!UICONTROL Create Exclusion]**.

   ![Dialoogvenster Uitsluiting maken](/help/main/c-recommendations/c-products/assets/create-exclusion.png)

1. Een uitsluiting typen **[!UICONTROL Name]** en voert u een optionele beschrijving in.

1. Gebruik de regelbouwer om uw uitsluitingen te maken.

   Selecteer een parameter in de lijst Regels, selecteer een operator en voer een of meer waarden in om de producten te identificeren. Scheid meerdere waarden met komma&#39;s.

1. Klik op **[!UICONTROL Create]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

## Een uitsluiting bewerken, kopiëren of verwijderen

Klik op de knop **weglatingsteken** klikt u op het betreffende pictogram naast de gewenste uitsluiting in de lijst: bewerken, kopiëren of verwijderen.

![Opties: bewerken, kopiëren en verwijderen](/help/main/c-recommendations/c-products/assets/edit-copy-delete.png)

U kunt een bestaande uitsluiting kopiëren om een dubbele uitsluiting te maken die u vervolgens kunt wijzigen. Met deze optie kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat uitsluitingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u rekening houdt met dit voorbehoud voordat u een uitsluiting verwijdert. Verwijderde uitsluitingen kunnen niet worden hersteld.

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)