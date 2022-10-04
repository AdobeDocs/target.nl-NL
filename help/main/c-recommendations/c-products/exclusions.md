---
keywords: uitsluitingen
description: Leer hoe u uitsluitingen maakt in Adobe [!DNL Target] Recommendations om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen.
title: Hoe gebruik ik uitsluitingen in Recommendations-activiteiten?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Uitsluitingen

Een uitsluiting maken in [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen. Een uitsluiting is een subset van producten of inhoud die niet aan bezoekers mag worden aanbevolen.

De uitsluitingen zijn beschikbaar over de volledige rekening. In tegenstelling tot verzamelingen, waarin u een specifieke verzameling opgeeft voor elke ervaring terwijl u een [!UICONTROL Recommendations] activiteiten, zijn uitsluitingen van toepassing op alle activiteiten over de gehele rekening. Er is geen optie om een uitsluitingsgroep toe te wijzen tijdens het maken van activiteiten.

Enkele voorbeelden van de tijden u uitsluitingen zou gebruiken omvatten:

* Producten die zijn stopgezet
* De catalogus Herfst/Winter is nu de enige catalogus die online aanwezig moet zijn. Elk item uit de zomercatalogus kan niet meer worden aangeschaft.
* Items die op de meeste pagina&#39;s/schermen niet kunnen worden aanbevolen (volwassen producten, NC-17-films, enz.)
* Producten met onvolledige metagegevensvelden (ontbrekende miniatuur, prijs of andere belangrijke metagegevens)
* Producten die nooit mogen worden aanbevolen (misschien bestaat er een SKU in het systeem voor iets, maar het is geen aanschafbaar item, of misschien is het een nep-SKU voor het QA-team om een aankoop te simuleren zonder iets te bestellen, enz.)

>[!IMPORTANT]
>
>Uitsluitingsregels worden globaal toegepast op alle omgevingen.
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruiksscenario&#39;s, zie [Dynamische en statische insluitingsregels gebruiken](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Een uitsluiting maken

1. Klikken **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** de lijst van bestaande uitsluitingen weer te geven.

   ![exclusies_list-afbeelding](assets/exclusions_list.png)

   Het gerapporteerde &quot;Aantal posten&quot; voor elke uitsluiting op de [!UICONTROL Exclusions] lijstmening is het aantal producten die de regels voor die uitsluiting binnen de gevormde standaardRecommendations aanpassen [hostgroep](/help/main/administrating-target/hosts.md) (milieu). Zie [Instellingen](https://developer.adobe.com/target/implement/recommendations/){target=_blank} om de standaardhostgroep te wijzigen.

1. Klik op **[!UICONTROL Create Exclusion]**.

1. (Voorwaardelijk) Kies een omgeving in het menu **[!UICONTROL Environment]** filter tijdens het maken (of bijwerken) van een uitsluiting om de inhoud van de uitsluiting in die omgeving voor te vertonen. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Uitsluiting maken](/help/main/c-recommendations/c-products/assets/CreateExclusion.png)

1. Een uitsluiting typen **[!UICONTROL Name]** en voert u een optionele beschrijving in.

1. Gebruik de regelbouwer om uw uitsluitingen te maken.

   Selecteer een parameter in de lijst Regels, selecteer een operator en voer een of meer waarden in om de producten te identificeren. Scheid meerdere waarden met komma&#39;s.

1. Klik op **[!UICONTROL Save]**.

## Een uitsluiting maken met Geavanceerd zoeken

U kunt ook uitsluitingen maken met [!UICONTROL Advanced Search] op de [Catalogus zoeken](/help/main/c-recommendations/c-products/catalog-search.md#save-as) pagina ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als dialoogvenster](/help/main/c-recommendations/c-products/assets/save-as.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>De [!UICONTROL Advanced Search] de functionaliteit is niet hoofdlettergevoelig; producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u uitsluitingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een uitzondering maakt met de bedoeling producten die vakantie bevatten, uit te sluiten, worden alleen producten die vakantie bevatten, uitgesloten. Producten die &quot;vakantie&quot; bevatten, zijn niet uitgesloten.

## Een uitsluiting bewerken, kopiëren of verwijderen

Houd de muisaanwijzer boven de gewenste uitsluiting in de lijst en klik op het juiste pictogram: bewerken, kopiëren of verwijderen.

![Pictogrammen verbergen voor een uitsluiting](/help/main/c-recommendations/c-products/assets/hover-exclusions.png)

U kunt een bestaande uitsluiting kopiëren om een dubbele uitsluiting te maken die u vervolgens kunt wijzigen. Hierdoor kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat uitsluitingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een uitsluiting verwijdert. Verwijderde uitsluitingen kunnen niet worden hersteld.

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)
