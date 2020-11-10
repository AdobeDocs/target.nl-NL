---
keywords: exclusions
description: Maak een uitsluiting [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen.
title: Uitsluitingen in Adobe Target
feature: entities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---


# Uitsluitingen{#exclusions}

Maak een uitsluiting in [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen. Een uitsluiting is een subset van producten of inhoud die niet aan bezoekers mag worden aanbevolen.

De uitsluitingen zijn beschikbaar over de volledige rekening. In tegenstelling tot inzamelingen, waar u een specifieke inzameling voor elke ervaring specificeert aangezien u een [!UICONTROL Recommendations] activiteit creeert, zijn de uitsluitingen op alle activiteiten over de rekening van toepassing. Er is geen optie om een uitsluitingsgroep toe te wijzen tijdens het maken van activiteiten.

Enkele voorbeelden van de tijden u uitsluitingen zou gebruiken omvatten:

* Producten die zijn stopgezet
* De catalogus Herfst/Winter is nu de enige catalogus die online aanwezig moet zijn. Elk item uit de zomercatalogus kan niet meer worden aangeschaft.
* Items die op de meeste pagina&#39;s/schermen niet kunnen worden aanbevolen (volwassen producten, NC-17-films, enz.)
* Producten met onvolledige metagegevensvelden (ontbrekende miniatuur, prijs of andere belangrijke metagegevens)
* Producten die nooit mogen worden aanbevolen (misschien bestaat er een SKU in het systeem voor iets, maar het is geen aanschafbaar item, of misschien is het een nep-SKU voor het QA-team om een aankoop te simuleren zonder iets te bestellen, enz.)

>[!IMPORTANT]
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruik-case scenario&#39;s, zie de Dynamische en Statische Regels [van de Insluiting van het](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)Gebruik.

## Een uitsluiting maken

1. Klik **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** om de lijst met bestaande uitsluitingen weer te geven.

   ![](assets/exclusions_list.png)

   Het &quot;Aantal Punten&quot;voor elke uitsluiting op de [!UICONTROL Exclusions] lijstmening wordt gemeld is het aantal producten die de regels voor die uitsluiting binnen de gevormde standaardRecommendations [gastheergroep](/help/administrating-target/hosts.md) (milieu) aanpassen die. Zie [Instellingen](/help/c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) om de standaardhostgroep te wijzigen.

1. Klik op **[!UICONTROL Create Exclusion]**.

1. (Voorwaardelijk) Kies een omgeving van het **[!UICONTROL Environment]** filter wanneer u een uitsluiting maakt (of bijwerkt) om een voorvertoning van de inhoud van de uitsluiting in die omgeving weer te geven. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Uitsluiting maken](/help/c-recommendations/c-products/assets/CreateExclusion.png)

1. Typ een uitsluiting **[!UICONTROL Name]** en voer een optionele beschrijving in.

1. Gebruik de regelbouwer om uw uitsluitingen te maken.

   Selecteer een parameter in de lijst Regels, selecteer een operator en voer een of meer waarden in om de producten te identificeren. Scheid meerdere waarden met komma&#39;s.

1. Klik op **[!UICONTROL Save]**.

## Een uitsluiting maken met Geavanceerd zoeken

U kunt uitsluitingen ook maken [!UICONTROL Advanced Search] op de pagina [Catalog Search](/help/c-recommendations/c-products/catalog-search.md#save-as) ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als dialoogvenster](/help/c-recommendations/c-products/assets/save-as.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Exclusion]klikken.

>[!IMPORTANT]
>
>De [!UICONTROL Advanced Search] functionaliteit is niet hoofdlettergevoelig; producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u uitsluitingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een uitzondering maakt met de bedoeling producten die vakantie bevatten, uit te sluiten, worden alleen producten die vakantie bevatten, uitgesloten. Producten die &quot;vakantie&quot; bevatten, zijn niet uitgesloten.

## Een uitsluiting bewerken, kopiëren of verwijderen

Houd de muisaanwijzer boven de gewenste uitsluiting in de lijst en klik op het juiste pictogram: bewerken, kopiëren of verwijderen.

![Pictogrammen verbergen voor een uitsluiting](/help/c-recommendations/c-products/assets/hover-exclusions.png)

U kunt een bestaande uitsluiting kopiëren om een dubbele uitsluiting te maken die u vervolgens kunt wijzigen. Hierdoor kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat uitsluitingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een uitsluiting verwijdert. Verwijderde uitsluitingen kunnen niet worden hersteld.

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)