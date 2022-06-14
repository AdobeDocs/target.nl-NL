---
keywords: Recommendations;instellingen;voorkeuren;industrie verticaal;filter incompatibele criteria;standaard hostgroep;thumb basis url;aanbevelingen api token
description: 'Leer hoe u Recommendations-activiteiten implementeert in Adobe Target. '
title: Hoe kan ik Recommendations-activiteiten implementeren?
feature: Recommendations
exl-id: b6edb504-a8b6-4379-99c1-6907e71601f9
source-git-commit: fc2a9641b4b949b4d1308a5d17deff1754960bad
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Plan en implementeer [!DNL Recommendations]

Voordat u de eerste instelt [!DNL Recommendations] activiteit in [!DNL Adobe Target]Voer de volgende stappen uit:

1. [Implementeren [!DNL Target]](#implement-target) op het web en in mobiele apps die u wilt gebruiken voor het vastleggen van gebruikersgedrag en het doen van aanbevelingen.
1. [Stel uw [!DNL Recommendations] catalogus](#rec-catalog) van producten of inhoud die u aan uw gebruikers wilt aanbevelen.
1. [Gedragsinformatie en context doorgeven](#pass-behavioral) tot [!DNL Target Recommendations] om het in staat te stellen gepersonaliseerde aanbevelingen te doen.
1. [Algemene uitsluitingen configureren](#exclusions).
1. [Configureren [!DNL Recommendations] instellingen](#concept_C1E1E2351413468692D6C21145EF0B84).

## Implementeren [!DNL Target] {#implement-target}

[!DNL Target Recommendations] vereist dat u de [!DNL Adobe Experience Platform Web SDK] of om 0.js 0.9.2 (of later). Zie [Implementeren [!DNL Target]](/help/main/c-implementing-target/implementing-target.md) voor meer informatie .

## Een Recommendations-catalogus instellen {#rec-catalog}

Om aanbevelingen van hoge kwaliteit te doen, [!DNL Target] moet weten welke producten of inhoud u wilt aanbevelen. De catalogus bevat gewoonlijk drie soorten informatie over de items die u wilt aanbevelen. Stel dat u films aanbeveelt. Neem het volgende op:

1. Gegevens die u aan de gebruiker wilt tonen die de aanbeveling ontvangt. U kunt bijvoorbeeld de naam van de film en een URL voor een miniatuurafbeelding van de filmposter weergeven.
1. Gegevens die nuttig zijn voor het toepassen van marketing- en verkoopbesturingselementen. U kunt bijvoorbeeld de classificatie van de film weergeven, zodat u geen NC-17-films aanbeveelt.
1. Gegevens die nuttig zijn om de gelijkenis van items met andere items te bepalen. U kunt bijvoorbeeld het genre van de film en de filmdirecteur weergeven.

[!DNL Target] bevat meerdere integratieopties om uw catalogus te vullen. Deze opties kunnen in combinatie worden gebruikt om verschillende items in de catalogus bij te werken of om verschillende itemkenmerken op verschillende frequenties bij te werken.

| Methode | Wat het is | Wanneer gebruikt u het | Aanvullende informatie |
| --- | --- | --- | --- |
| Catalogusfeed | Een feed plannen (CSV, Google Product XML, of [!DNL Analytics Product Classifications]) die dagelijks worden geüpload en opgenomen. | Voor het verzenden van informatie over meerdere items tegelijk. Voor het verzenden van informatie die niet vaak wordt gewijzigd. | Zie [Feeds](/help/main/c-recommendations/c-products/feeds.md). |
| Entiteiten-API | Roep API aan om updates naar de minuut voor één enkel punt te verzenden. | Voor het verzenden van updates zoals deze over één item tegelijk plaatsvinden. Voor het verzenden van informatie die regelmatig verandert (bijvoorbeeld prijs, voorraad/voorraadniveau). | Zie de [Documentatie voor ontwikkelaars van Entiteiten-API](https://developers.adobetarget.com/api/recommendations/#tag/Entities). |
| Updates op de pagina doorgeven | Updates voor één item verzenden met JavaScript op de pagina of met de API voor levering. | Voor het verzenden van updates zoals deze over één item tegelijk plaatsvinden. Voor het verzenden van informatie die regelmatig verandert (bijvoorbeeld prijs, voorraad/voorraadniveau). | Zie [Objectweergaven/productpagina&#39;s](#items-product-pages) hieronder. |

De meeste klanten zouden minstens één voer moeten uitvoeren. Vervolgens kunt u ervoor kiezen om uw feed aan te vullen met updates voor vaak gewijzigde kenmerken of items met behulp van de Entities API of de on-the-page methode.

## Gedragsinformatie en context doorgeven {#pass-behavioral}

De gedragsinformatie en context die u moet doorgeven [!DNL Target] is afhankelijk van de actie die de bezoeker uitvoert. Dit is vaak afhankelijk van het type pagina waarmee de bezoeker communiceert.

### Objectweergaven/productpagina&#39;s {#items-product-pages}

Op pagina&#39;s waarop een bezoeker één item weergeeft, zoals een pagina met productdetails, moet u de identiteit doorgeven van het item dat de bezoeker bekijkt. U zou ook de korrelste categorie van het punt moeten overgaan dat de bezoeker bekijkt, om het filtreren aanbevelingen aan de huidige categorie toe te staan.

U kunt ook bepaalde snel veranderende kenmerken op de productpagina zelf doorgeven. U kunt bijvoorbeeld de prijs doorgeven (`value`) en voorraadniveau.

```
<script type="text/javascript">
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "running-shoes", 
         "value": 119.99, 
         "inventory": 329 
      } 
   } 
}
</script>
```

### Categorieweergaven/categoriepagina&#39;s

Op een categoriepagina wilt u waarschijnlijk uw aanbevelingen beperken tot producten of inhoud binnen die categorie. Hiervoor moet u de identiteit van de momenteel weergegeven categorie doorgeven.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "running-shoes" 
      } 
   } 
}
```

### Winkelwagentweergaven/winkelwagentjes/afhandelingspagina&#39;s {#cart}

Op een winkelwagentje kunt u objecten aanbevelen op basis van de inhoud van het huidige winkelwagentje van de bezoeker. Geef hiertoe de id&#39;s van alle items in het huidige winkelwagentje van de bezoeker door met behulp van de speciale parameter `cartIds`.

```
function targetPageParams() {
   return {
      "cartIds": "352,223,23432,432,553"
      }
}
```

Meer informatie over [!UICONTROL Cart-Based] aanbevelingen, zie [Op basis van winkelwagentje](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *De aanbeveling baseren op een aanbevelingen*.

### Objecten uitsluiten die al in de winkelwagentje van de bezoeker staan

Op pagina&#39;s op de hele site kunt u bepaalde items uitsluiten van aanbevelingen. U kunt bijvoorbeeld items die zich al in het huidige winkelwagentje van de bezoeker bevinden, niet aanbevelen. Geef daartoe de id&#39;s door van alle items die u wilt uitsluiten met behulp van de speciale parameter `excludedIds`.

```
function targetPageParams() {
   return {
      "excludedIds": "352,223,23432,432,553"
      }
}
```

### Pagina&#39;s voor kopen/bestellen bevestigen

Wanneer een aankoopgebeurtenis plaatsvindt, geeft u de identiteit door van het gekochte item of de gekochte items. Zie [Conversies bijhouden](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053) in *Implementeren [!DNL Target] zonder tagbeheer*.

## Algemene uitsluitingen configureren {#exclusions}

Sluit items op algemeen niveau uit die u nooit aan een bezoeker wilt aanbevelen. Zie [Uitsluitingen](/help/main/c-recommendations/c-products/exclusions.md).

## Configureren [!DNL Recommendations] instellingen {#concept_C1E1E2351413468692D6C21145EF0B84}

Instellingen gebruiken om uw [!DNL Recommendations] uitvoering.

Om toegang te krijgen tot [!UICONTROL Recommendations Settings] opties, openen [!DNL Target] in de [!DNL Adobe Experience Cloud]en klik vervolgens op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

![](assets/recs_settings.png)

De volgende opties zijn beschikbaar:

| Instelling | Beschrijving |
|--- |--- |
| Aangepaste globale mabox | (Optioneel) Geef de aangepaste globale box op die wordt gebruikt voor de server [!DNL Target] activiteiten. Standaard wordt de algemene box gebruikt door [!DNL Target] wordt gebruikt voor [!DNL Recommendations].<br>Opmerking: Deze optie is ingesteld op [!DNL Target] [!UICONTROL Administration] pagina. Openen [!DNL Target]en klik vervolgens op [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]. |
| Verticale industrie | De industrie verticaal wordt gebruikt helpen uw aanbevelingen criteria categoriseren. Deze informatie helpt leden van uw team criteria te vinden die voor een bepaalde pagina, zoals criteria zinvol zijn die voor de het winkelwagentje pagina of voor een media pagina het best zijn. |
| Niet-compatibele criteria filteren | Schakel deze optie in om alleen die criteria weer te geven waarbij de geselecteerde pagina de vereiste gegevens doorgeeft. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het selectievakje moet worden ingeschakeld `entity.id` of `entity.categoryId` voor het huidige item/de huidige categorie-aanbevelingen compatibel te maken. Over het algemeen is het beter alleen compatibele criteria te laten zien. Schakel deze optie echter uit als u incompatibele criteria voor de activiteit wilt gebruiken.<br>U wordt aangeraden deze optie uit te schakelen als u een oplossing voor tagbeheer gebruikt.<br>Zie voor meer informatie over deze optie [Veelgestelde vragen over Recommendations](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md). |
| Standaardhostgroep | Selecteer de standaardhostgroep.<br>U kunt de hostgroep gebruiken om de beschikbare items in uw catalogus te scheiden voor verschillende toepassingen. U kunt bijvoorbeeld hostgroepen gebruiken voor ontwikkelings- en productieomgevingen, verschillende merken of verschillende geografische locaties. Standaard zijn de voorvertoningsresultaten in Cataloguszoekopdrachten, Verzamelingen en Uitsluitingen gebaseerd op de standaardhostgroep. (U kunt ook een andere hostgroep selecteren om een voorvertoning van de resultaten weer te geven met behulp van het filter Omgeving.) Nieuwe toegevoegde items zijn standaard beschikbaar in alle hostgroepen, tenzij een milieu-id is opgegeven bij het maken of bijwerken van het item. De geleverde aanbevelingen hangen van de gastheergroep af die in het verzoek wordt gespecificeerd.<br>Als u uw producten niet ziet, zorg ervoor dat u de correcte gastheergroep gebruikt. Bijvoorbeeld, als u opstelling uw aanbeveling om een het opvoeren milieu te gebruiken en u uw gastheergroep aan het Opvoeren plaatst, zou u uw inzamelingen in het opvoeren milieu voor de te tonen producten kunnen moeten opnieuw creëren. Om te zien welke producten in elke milieu beschikbaar zijn, gebruik CatalogusOnderzoek met elke milieu. U kunt ook een voorvertoning weergeven van de inhoud van Recommendations-verzamelingen en -uitsluitingen voor een geselecteerde omgeving (hostgroep).<br>**Opmerking:** Nadat u de geselecteerde omgeving hebt gewijzigd, moet u op Zoeken klikken om de geretourneerde resultaten bij te werken.<br>De [!UICONTROL Environment] is beschikbaar op de volgende plaatsen in het dialoogvenster [!DNL Target] UI:<ul><li>Catalogus zoeken ([!UICONTROL Recommendations] > Catalogus zoeken)</li><li>Verzameling maken, dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])</li><li>Dialoogvenster Verzameling bijwerken ([!UICONTROL Recommendations > Collections > Edit])</li><li>Dialoogvenster Uitsluiting maken ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>Dialoogvenster Uitsluiting bijwerken ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul>Zie voor meer informatie [Gastheren](/help/main/administrating-target/hosts.md). |
| Basis-URL miniatuur | Als u een basis-URL instelt voor uw productcatalogus, kunt u relatieve URL&#39;s gebruiken wanneer u miniaturen van uw producten opgeeft wanneer u de URL van de miniatuur doorgeeft.<br>Bijvoorbeeld:<br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br>Hiermee stelt u een URL in ten opzichte van de basis-URL van de miniatuur. |
| Recommendations API Token | Gebruik dit token in Recommendations API-aanroepen, zoals de Download API. |
