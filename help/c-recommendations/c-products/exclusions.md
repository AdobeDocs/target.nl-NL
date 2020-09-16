---
keywords: exclusions
description: Maak een uitsluitingslijst in Adobe Target om te voorkomen dat objecten worden aanbevolen.
title: Uitsluitingen in Adobe Target
feature: entities
uuid: 1970846e-37d8-4b69-a0d9-ff45bb840bef
translation-type: tm+mt
source-git-commit: 421168f34bffe1f5f90d90f4af9b28940d0b8010
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---


# Uitsluitingen{#exclusions}

Maak een uitsluiting in [!DNL Adobe Target Recommendations] om te voorkomen dat producten of inhoud aan bezoekers worden aanbevolen.

Een uitsluiting is een subset van producten of inhoud die niet aan uw bezoekers mag worden aanbevolen. U kunt uitsluitingen bijvoorbeeld gebruiken om te voorkomen dat producten of inhoud worden weergegeven in aanbevelingen die zijn stopgezet of die gevoelig zijn in de natuur (zoals films met een classificatie die niet geschikt is voor alle leeftijden).

>[!IMPORTANT]
>
>Statische en dynamische uitsluitingsregels zijn krachtige functies die u kunnen helpen bij uw marketinginspanningen. Voor gedetailleerde informatie, voorbeelden, en gebruik-case scenario&#39;s, zie de Dynamische en Statische Regels [van de Insluiting van het](../../c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md#concept_4CB5C0FA705D4E449BD0B37B3D987F9F)Gebruik.

## Een uitsluiting maken

1. Klik **[!UICONTROL Recommendations]** > **[!UICONTROL Exclusions]** om de lijst met bestaande uitsluitingen weer te geven.

   ![](assets/exclusions_list.png)

   Het &quot;Aantal Punten&quot;voor elke uitsluiting op de [!UICONTROL Exclusions] lijstmening wordt gemeld is het aantal producten die de regels voor die uitsluiting binnen de gevormde standaardRecommendations [gastheergroep](/help/administrating-target/hosts.md) (milieu) aanpassen die. Zie [Instellingen](../../c-recommendations/plan-implement.md#concept_C1E1E2351413468692D6C21145EF0B84) om de standaardhostgroep te wijzigen.

1. Klik op **[!UICONTROL Create Exclusion]**.

1. (Voorwaardelijk) Kies een omgeving van het **[!UICONTROL Environment]** filter wanneer u een uitsluiting maakt (of bijwerkt) om een voorvertoning van de inhoud van de uitsluiting in die omgeving weer te geven. Standaard worden de resultaten van de standaardhostgroep weergegeven.

   ![Uitsluiting maken](/help/c-recommendations/c-products/assets/CreateExclusion.png)

1. Typ een uitsluiting **[!UICONTROL Name]** en voer een optionele beschrijving in.

1. Gebruik de regelbouwer om uw uitsluitingen te maken.

   Selecteer een parameter in de lijst Regels, selecteer een operator en voer een of meer waarden in om de producten te identificeren. Scheid meerdere waarden met komma&#39;s.

1. Klik op **[!UICONTROL Save]**.

## Een uitsluiting maken met Geavanceerd zoeken

U kunt uitsluitingen ook maken met Geavanceerd zoeken op de pagina Cataloguszoekopdracht ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]).

![Opslaan als](/help/c-recommendations/c-products/assets/save-as-dialog.png)

Nadat u een zoekopdracht hebt gemaakt met &#39;id > contains&#39;, kunt u bijvoorbeeld op [!UICONTROL Save As] > [!UICONTROL Exclusion]klikken. Zie [Cataloguszoekopdracht](/help/c-recommendations/c-products/catalog-search.md#save-as)voor meer informatie.

>[!IMPORTANT]
>
>De functie Geavanceerd zoeken is niet hoofdlettergevoelig. producten die op het tijdstip van levering worden geretourneerd, zijn echter gebaseerd op hoofdlettergevoelige zoekopdrachten. Deze wanverhouding kan tot verwarring leiden. Zorg ervoor dat u rekening houdt met hoofdlettergevoeligheid wanneer u uitsluitingen maakt op basis van resultaten met de functie Geavanceerd zoeken. Als u bijvoorbeeld zoekt naar &#39;Vakantie&#39;, worden in de eerste zoekopdracht resultaten weergegeven die &#39;Vakantie&#39; en &#39;Vakantie&#39; bevatten. Als u vervolgens een uitzondering maakt met de bedoeling producten die vakantie bevatten, uit te sluiten, worden alleen producten die vakantie bevatten, uitgesloten. Producten die &quot;vakantie&quot; bevatten, zijn niet uitgesloten.

## Trainingsvideo: Verzamelingen en uitsluitingen maken in Recommendations (7:05) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie:

* Een verzameling maken
* Een uitsluiting maken

>[!VIDEO](https://video.tv.adobe.com/v/27689)