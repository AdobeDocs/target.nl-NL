---
keywords: uitsluitingen
description: Leer hoe te om tot uitsluitingen in Adobe  [!DNL Target]  Aanbevelingen te leiden om producten of inhoud te verhinderen aan bezoekers worden geadviseerd.
title: Hoe gebruik ik uitsluitingen in activiteiten met aanbevelingen?
feature: Recommendations
exl-id: e41487c7-6d47-4958-8e4b-616a2ad56b3c
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# Uitsluitingen

Maak een uitsluiting in [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen. Een uitsluiting is een subset van producten of inhoud die niet aan bezoekers mag worden aanbevolen.

De uitsluitingen zijn beschikbaar over de volledige rekening. In tegenstelling tot verzamelingen waarin u voor elke ervaring een specifieke verzameling opgeeft terwijl u een [!UICONTROL Recommendations] -activiteit maakt, zijn uitsluitingen van toepassing op alle activiteiten in de account. Er is geen optie om een uitsluitingsgroep toe te wijzen tijdens het maken van activiteiten.

Enkele voorbeelden van de tijden u uitsluitingen zou gebruiken omvatten:

* Producten die zijn stopgezet
* De catalogus Herfst/Winter is nu de enige catalogus die online aanwezig moet zijn. Elk item uit de zomercatalogus kan niet meer worden aangeschaft.
* Items die op de meeste pagina&#39;s/schermen niet kunnen worden aanbevolen (volwassen producten, NC-17-films, enz.)
* Producten met onvolledige metagegevensvelden (ontbrekende miniatuur, prijs of andere belangrijke metagegevens)
* Producten die nooit zouden moeten worden geadviseerd (misschien bestaat SKU in het systeem voor iets maar het is geen koopbaar voorwerp, of misschien is het een nep SKU voor het team van QA om een aankoop te simuleren zonder eigenlijk iets te bestellen, enz.)

>[!IMPORTANT]
>
>Uitsluitingsregels worden globaal toegepast op alle omgevingen.
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruik-case scenario&#39;s, zie [&#x200B; Dynamische en Statische Regels van de Opname van het Gebruik &#x200B;](/help/main/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F).

## Een uitsluiting maken

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** om de lijst met bestaande uitsluitingen weer te geven.

   ![&#x200B; exclusion_list beeld &#x200B;](assets/exclusions_list.png)

   Het &quot;Aantal Punten&quot;voor elke uitsluiting op de [!UICONTROL Exclusions] lijstmening wordt gemeld is het aantal producten die de regels voor die uitsluiting aanpassen binnen de gevormde standaardgroep van Aanbevelingen [&#128279;](/help/main/administrating-target/hosts.md) (milieu). Zie [&#x200B; Montages &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=nl-NL){target=_blank} om de standaardgastheergroep te veranderen.

1. Klik op **[!UICONTROL Create Exclusion]**.

1. (Voorwaardelijk) Kies een omgeving van het filter **[!UICONTROL Environment]** wanneer u een uitsluiting maakt (of bijwerkt) om een voorvertoning van de inhoud van de uitsluiting in die omgeving weer te geven. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![&#x200B; creeer Uitsluiting &#x200B;](/help/main/c-recommendations/c-products/assets/CreateExclusion.png)

1. Typ een uitsluiting **[!UICONTROL Name]** en voer een optionele beschrijving in.

1. Gebruik de regelbouwer om uw uitsluitingen te maken.

   Selecteer een parameter in de lijst Regels, selecteer een operator en voer een of meer waarden in om de producten te identificeren. Scheid meerdere waarden met komma&#39;s.

1. Klik op **[!UICONTROL Save]**.

## Een uitsluiting maken met Geavanceerd zoeken

U kunt uitsluitingen ook tot stand brengen gebruikend [!UICONTROL Advanced Search] op de [&#x200B; pagina van het Onderzoek van de Catalogus &#x200B;](/help/main/c-recommendations/c-products/catalog-search.md#save-as) ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![&#x200B; sparen als dialoog &#x200B;](/help/main/c-recommendations/c-products/assets/save-as.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Exclusion] klikken.

>[!IMPORTANT]
>
>De functie [!UICONTROL Advanced Search] is niet hoofdlettergevoelig. Producten die op het moment van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u uitsluitingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een uitzondering maakt met de bedoeling producten die vakantie bevatten, uit te sluiten, worden alleen producten die vakantie bevatten, uitgesloten. Producten die &quot;vakantie&quot; bevatten, zijn niet uitgesloten.

## Een uitsluiting bewerken, kopiëren of verwijderen

Houd de muisaanwijzer boven de gewenste uitsluiting in de lijst en klik op het juiste pictogram: bewerken, kopiëren of verwijderen.

![&#x200B; pictogrammen van de Bedekking voor een uitsluiting &#x200B;](/help/main/c-recommendations/c-products/assets/hover-exclusions.png)

U kunt een bestaande uitsluiting kopiëren om een dubbele uitsluiting te maken die u vervolgens kunt wijzigen. Hierdoor kunt u een vergelijkbare uitsluiting maken met minder moeite.

Houd er rekening mee dat uitsluitingen beschikbaar zijn voor de gehele account. Zorg ervoor dat u hiermee rekening houdt voordat u een uitsluiting verwijdert. Verwijderde uitsluitingen kunnen niet worden hersteld.

## De video van de opleiding: Creeer inzamelingen en uitsluitingen in Aanbevelingen (7 :05) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)
