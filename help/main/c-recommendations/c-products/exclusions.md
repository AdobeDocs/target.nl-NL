---
keywords: uitsluitingen
description: Leer hoe te om uitsluitingen in  [!DNL Target Recommendations]  tot stand te brengen om producten of inhoud te verhinderen aan bezoekers worden geadviseerd.
title: Hoe gebruik ik uitsluitingen in [!UICONTROL Recommendations] -activiteiten?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Uitsluitingen

Maak een uitsluiting in [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen. Een uitsluiting is een subset van producten of inhoud die niet aan bezoekers mag worden aanbevolen.

De uitsluitingen zijn beschikbaar over de volledige rekening. In tegenstelling tot verzamelingen waarin u voor elke ervaring een specifieke verzameling opgeeft terwijl u een [!UICONTROL Recommendations] -activiteit maakt, zijn uitsluitingen van toepassing op alle activiteiten in de account. Er is geen optie om een uitsluitingsgroep toe te wijzen tijdens het maken van activiteiten.

Enkele voorbeelden van de tijden u uitsluitingen zou gebruiken omvatten:

* Producten die zijn stopgezet.
* De catalogus Herfst en Winter is nu de enige catalogus die online aanwezig moet zijn. Elk item uit de zomercatalogus kan niet meer worden aangeschaft.
* Items die op de meeste pagina&#39;s of schermen (volwassen producten, NC-17-films enzovoort) niet kunnen worden aanbevolen.
* Producten met onvolledige metagegevensvelden (ontbrekende miniatuur, prijs of andere belangrijke metagegevens).
* Producten die nooit zouden moeten worden geadviseerd (misschien bestaat SKU in het systeem voor iets maar het is geen koopbaar voorwerp. Of misschien is het een nepSKU voor het QA-team om een aankoop te simuleren zonder iets te bestellen, enzovoort).

>[!IMPORTANT]
>
>De regels van de uitsluiting worden globaal toegepast op alle [&#x200B; milieu&#39;s &#x200B;](/help/main/administrating-target/environments.md).
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruik-case scenario&#39;s, zie [&#x200B; Dynamische en Statische Regels van de Opname van het Gebruik &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Een uitsluiting maken

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** om de lijst met bestaande uitsluitingen weer te geven.

   Het &quot;Aantal Punten&quot;voor elke uitsluiting op de [!UICONTROL Exclusions] lijstmening wordt gemeld is het aantal producten die de regels voor die uitsluiting aanpassen binnen de gevormde standaardgroep van Aanbevelingen [&#128279;](/help/main/administrating-target/hosts.md) (milieu). Zie [&#x200B; Plan en voer  [!DNL Recommendations] uit &#x200B;](https://experienceleague.adobe.com/nl/docs/target-dev/developer/recommendations){target=_blank} in de *Gids van de Ontwikkelaar van Adobe Target* voor informatie over uit hoe te om de standaardgastheergroep te veranderen.

1. (Voorwaardelijk) klik het **[!UICONTROL Show Filters]** pictogram ( ![&#x200B; toon het pictogram van Filters &#x200B;](/help/main/assets/icons/Filter.svg)), dan kies het gewenste [&#x200B; milieu &#x200B;](/help/main/administrating-target/environments.md) van de **[!UICONTROL Environment]** drop-down lijst terwijl het creëren van (of het bijwerken) een uitsluiting om de inhoud van de uitsluiting in dat milieu voor te vertonen. Standaard worden de resultaten van de standaardhostgroep weergegeven.

1. Klik op **[!UICONTROL Create Exclusion]**.

1. Typ een uitsluiting **[!UICONTROL Name]** en voer een optionele beschrijving in.

1. Gebruik de regelbouwer om uw uitsluitingen te maken.

   Selecteer een parameter in de lijst [!UICONTROL Rules] , selecteer een operator en voer een of meer waarden in om de producten te identificeren. Scheid meerdere waarden met komma&#39;s.

1. Klik op **[!UICONTROL Create]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

## Een uitsluiting bewerken, kopiëren of verwijderen

Klik het Meer pictogram van Acties ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) naast de gewenste uitsluiting in de lijst, dan klik het aangewezen pictogram: [!UICONTROL Edit], [!UICONTROL Copy], of [!UICONTROL Delete].

U kunt een bestaande uitsluiting kopiëren om een dubbele uitsluiting te maken die u vervolgens kunt wijzigen. Met deze optie kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat uitsluitingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u rekening houdt met dit voorbehoud voordat u een uitsluiting verwijdert. Verwijderde uitsluitingen kunnen niet worden hersteld.

## De video van de opleiding: Creeer inzamelingen en uitsluitingen in Aanbevelingen (7 :05) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)
