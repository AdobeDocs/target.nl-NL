---
keywords: Recommendations;settings;preferences;industry vertical;filter incompatible criteria;default host group;thumb base url;recommendations api token
description: Wat je moet weten voordat je een Recommendations-activiteit maakt.
title: Recommendations plannen en implementeren
feature: recommendations general
uuid: 37be7fb3-3686-4dec-9cca-478d28191985
translation-type: tm+mt
source-git-commit: 00749d54d0416c57364ff648bd0911e636c84bc7
workflow-type: tm+mt
source-wordcount: '1567'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Plan en implementeer Recommendations {#plan-and-implement-recommendations}

Wat je moet weten voordat je een Recommendations-activiteit maakt.

## Recommendations plannen en implementeren {#concept_02AA644A4C7D4D5CB1D9CADA208CF8D1}

Wat u moet weten voordat u een [!DNL Recommendations] activiteit maakt.

[!DNL Recommendations] vereist dat u de volgende hiërarchie van informatie instelt:

| Stap | Informatie | Details |
|--- |--- |--- |
| ![Stap 1](/help/c-recommendations/assets/step1_red.png) | JavaScript-bibliotheek | Voor elke pagina is een verwijzing naar versie 0.js 0.9.1 (of hoger) of versie 55 (of hoger) van mbox.js vereist. Deze implementatiestap is vereist op alle pagina&#39;s waar een doelactiviteit wordt gebruikt en kan sleutels zoals een product of een categorie ID omvatten.<BR>Zie [at.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md)voor meer informatie over at.js.<br>Zie [Mbox.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)voor meer informatie over mbox.js. |
| ![Stap 2](/help/c-recommendations/assets/step2_red.png) | Toetsen | De sleutel bepaalt het type product of inhoud dat in uw aanbevelingen wordt weergegeven. De sleutel kan bijvoorbeeld een productcategorie zijn. Zie [De aanbeveling baseren op een toets](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)voor aanbevelingen. |
| ![Stap 3](/help/c-recommendations/assets/step3_red.png) | Attributen | Kenmerken bieden specifiekere informatie over de producten die u wilt weergeven. U kunt bijvoorbeeld producten weergeven binnen een bepaald prijsbereik of objecten die aan een voorraaddrempel voldoen. Kenmerken kunnen worden opgegeven in de mbox of via een [feed](/help/c-recommendations/c-products/feeds.md).<br>Zie [[Opnameregels](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion)opgeven. |
| ![Stap 4](/help/c-recommendations/assets/step4_red.png) | Uitsluitingen | De uitsluitingen bepalen welke specifieke punten niet in uw aanbevelingen verschijnen.<br>Zie [Uitsluitingen](/help/c-recommendations/c-products/exclusions.md). |
| ![Stap 5](/help/c-recommendations/assets/step5_red.png) | Aankoopgegevens | De koopgegevens bevatten informatie over de aangeschafte objecten en de order wanneer de aankoop is voltooid. |

## Basisimplementatie {#concept_D1154A3FB0FB4467A29AD2BDD21C82D5}

De basisimplementatie vereist dat u parameters aan uw pagina doorgeeft die bepalen welke producten of de diensten in uw aanbevelingen verschijnen.

Voordat u begint met het instellen van een [!DNL Recommendations] activiteit, moet u begrijpen hoe productgegevens worden verschaft [!DNL Recommendations]en bepalen welke methode het beste geschikt is voor uw behoeften.

Er zijn twee methoden om informatie te verstrekken over producten en services aan [!DNL Recommendations]:

| Methode | Beschrijving |
|--- |--- |
| Parameters rechtstreeks aan de pagina doorgeven | Deze methode werkt goed voor items die vaak veranderen. Omdat het echter vereist dat wijzigingen rechtstreeks op de pagina worden aangebracht, moet deze methode in veel organisaties worden toegepast door de IT-afdeling en de personen die de pagina&#39;s implementeren. |
| Parameters doorgeven via een Google- of CSV-feed | Deze methode werkt goed voor verzamelingen die niet vaak worden gewijzigd. Het is gewoonlijk niet nodig om uw implementatie of andere paginacode te veranderen om productinformatie door een voer te verstrekken. De productlijst blijft echter statisch, dus snelle wijzigingen zijn moeilijker. Zie [Feeds](/help/c-recommendations/c-products/feeds.md)voor meer informatie. |

Deze methoden kunnen afzonderlijk of samen worden gebruikt, zoals in de volgende voorbeelden.

## Voorbeeld één: Pagina en feeds combineren {#section_DF6BAE4BF11548BD9C44D0A426BCF5A7}

Bij één veelgebruikte [!DNL Recommendations] implementatieoptie worden zowel de paginaparameters als de feeds gebruikt.

Deze methode kan de voorkeur krijgen van een detailhandelaar die een relatief vastgestelde productcatalogus heeft, maar die wellicht specifieke seizoensgebonden artikelen of objecten die te koop zijn, wil benadrukken. De meeste klanten kunnen hun informatie hoofdzakelijk door het voer, met slechts af en toe aanpassingen op de pagina verstrekken.

Gebruik een feed om informatie te geven die niet vaak verandert. Gebruik de volgende parameters, of u nu een CSV-bestand of een Google-feed gebruikt:

* Vereiste parameters

   * `entity.id`

* Nuttige parameters

   * `entity.name`
   * `entity.categoryId`
   * `entity.brand`
   * `entity.pageUrl`
   * `entity.thumbnailUrl`
   * `entity.message`
   * Alle aangepaste kenmerken

Wanneer de feed is ingesteld en doorgegeven aan [!DNL Recommendations], geeft u op de pagina parameters door voor kenmerken die vaak veranderen, d.w.z. vaker dan dagelijks.

* Vereiste parameters

   * `entity.id`
   * `entity.categoryId`

* Nuttige parameters

   * `entity.inventory`
   * `entity.value`

Prioriteit wordt gegeven aan welke reeks gegevens het laatst wordt uitgevoerd. Als u eerst de feed doorgeeft en vervolgens de paginaparameters bijwerkt, worden de wijzigingen die in de paginaparameters zijn aangebracht, weergegeven ter vervanging van de iteminformatie die in de feed is doorgegeven.

## Voorbeeld twee: Geef alle parameters op de pagina met productdetails (of inhoudsgegevens) door {#section_D5A4F69457604CA7AACFD7BFF79B58A9}

Als u alle parameters op de pagina doorgeeft, kunt u snel updates uitvoeren door de pagina bij te werken. In sommige organisaties vereist dit de betrokkenheid van IT of uw team van het Ontwerp van het Web.

Dit voorbeeld is vooral handig voor een mediabedrijf, met inhoud die voortdurend verandert.

* Vereiste parameters

   * `entity.id`
   * `entity.categoryId`
   * Alle andere kenmerken

## Voorbeeldcode {#section_6E8A73376F30468BB549F337C4C220B1}

U kunt bijvoorbeeld de volgende code gebruiken in de koptekstsectie van uw product- of inhoudspagina&#39;s:

```
function targetPageParams() {
 return {
    "entity": {
       "id": "32323",
       "categoryId": "My Category",
       "value": 105.56,
       "inventory": 329
    }
 }
}
```

Zie [Implementatie volgens paginatype](../c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)voor meer voorbeelden van de code die u op verschillende typen pagina&#39;s kunt gebruiken.

## Implementatie volgens paginatype {#reference_DE38BB07BD3C4511B176CDAB45E126FC}

Paginatype beïnvloedt uw [!DNL Recommendations] implementatie.

De typen aanbevelingen die u bijvoorbeeld op een productpagina wilt presenteren, kunnen anders zijn dan op een categoriepagina of uw homepage. Voor elke pagina, kunt u specifieke functies in werking stellen voorafgaand aan de mbox vraag om de aangewezen aanbevelingen te tonen.

Zie [Entiteitskenmerken](../c-recommendations/c-products/entity-attributes.md#reference_3BCC1383FB3F44F4A2120BB36270387F)voor informatie over de kenmerken in de voorbeelden.

Geldige JSON-opmaak is vereist.

De hieronder weergegeven `targetPageParams` functie is vooral handig als u een oplossing voor tagbeheer gebruikt om uw pagina&#39;s te implementeren. [!DNL Adobe Launch] of [!DNL Adobe Dynamic Tag Manager] (DTM) plaatst de verwijzing at.js/mbox.js en de `targetPageParams` functie op uw pagina en staat u toe om de waarden te vormen. Plaats die functie voor uw aanroep naar at.js/mbox.js of plaats deze in de sectie Extra JavaScript van uw at.js/mbox.js.

## Alle pagina&#39;s {#section_A22061788BAB42BB82BA087DEC3AA4AD}

Voor alle pagina&#39;s die aanbevelingen bevatten, is een verwijzing [!DNL at.js] of een [!DNL mbox.js] verwijzing op de pagina vereist. Voeg een van de volgende verwijzingen naar alle pagina&#39;s met aanbevelingen toe:

```
<script src="../at.js /></script>
```

```
<script src="../mbox.js /></script>
```

Deze implementatie vereist:

* [!DNL at.js] versie 0.9.2 (of hoger) of [!DNL mbox.js] versie 55 (of hoger)

* [!DNL mbox.js] moet de verwijzing naar [!DNL target.js] ( [!DNL at.js] geen verwijzing naar [!DNL target.js]) bevatten

Voor meer informatie over het uitvoeren [!DNL at.js], zie [hoe te at.js opstellen](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md#topic_ECF2D3D1F3384E2386593A582A978556).

Voor meer informatie over het uitvoeren [!DNL mbox.js], zie [Implementatie](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420)Mbox.js.

Voor meer informatie over de verschillen tussen de twee bibliotheken van het Doel Javascript, zie [Voordelen van at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#benefits).

## Categoriepagina {#section_F51A1AAEAC0E4B788582BBE1FEC3ABDC}

Op een categoriepagina wilt u waarschijnlijk uw aanbevelingen beperken tot producten of inhoud binnen die categorie. Als u een categoriepagina wilt instellen, stelt u de sleutels in die door de pagina worden gebruikt. Voor meer informatie over sleutels, zie [Baseer de Aanbeveling op een Sleutel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md)van de Aanbeveling.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "categoryId": "My Category" 
      } 
   } 
}
```

## Productpagina {#section_205B3953C9664125A17CA8574FA6B2A3}

Op een productpagina kun je bepaalde objecten of objecten met een bepaalde prijs of voorraad aanbevelen. Voor een productpagina moet u mogelijk veelvoorkomende veranderende kenmerken instellen (zoals waarde en voorraad), naast de sleutels die vereist zijn voor een categoriepagina.

```
function targetPageParams() { 
   return { 
      "entity": { 
         "id": "32323", 
         "categoryId": "My Category", 
         "value": 105.56, 
         "inventory": 329 
      } 
   } 
}
```

## Winkelpagina {#section_D37E48700F074556B925D0CA0291405E}

Op een winkelwagentje wilt u waarschijnlijk bepaalde items uitsluiten van uw aanbevelingen, zoals de items die al in het winkelwagentje staan.

```
<script type="text/javascript">
function targetPageParams() {
   return {
      "excludedIds": [352, 223, 23432, 432, 553]
      }
}
</script>
```

## Dankbriefje {#section_C6126A4517A1478693AB7EC2A1D4ACCA}

Op de pagina Hartelijk dank kunt u het totaal van de bestellingen en de bestellings-id weergeven en de aangekochte producten weergeven zonder extra objecten aan te raden. U kunt een tweede box uitvoeren om de ordeinformatie te vangen.

* Zie Conversies [bijhouden als u at.js gebruikt](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053).
* Als u mbox.js gebruikt, zie [Create een doos van de Bevestiging van de Orde - mbox.js](../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md#task_0036D5F6C062442788BB55E872816D82).

## Instellingen {#concept_C1E1E2351413468692D6C21145EF0B84}

Gebruik instellingen om uw [!DNL Recommendations] implementatie te beheren.

Als u de [!UICONTROL Recommendations Settings] opties wilt openen, opent u [!DNL Target] in het dialoogvenster [!DNL Adobe Experience Cloud]en klikt u op **[!UICONTROL Recommendations]** > **[!UICONTROL Settings]**.

![](assets/recs_settings.png)

De volgende opties zijn beschikbaar:

| Instelling | Beschrijving |
|--- |--- |
| Aangepaste globale mabox | (Optioneel) Geef de aangepaste globale box op die wordt gebruikt voor [!DNL Target] activiteiten. Standaard [!DNL Target] wordt de algemene mbox gebruikt door [!DNL Recommendations].<br>Opmerking: Deze optie is ingesteld op de [!DNL Target] [!UICONTROL Administration] pagina. Open [!DNL Target], klik dan [!UICONTROL Administration] > [!UICONTROL Visual Experience Composer]. |
| Verticale industrie | De industrie verticaal wordt gebruikt helpen uw aanbevelingen criteria categoriseren. Hierdoor kunnen leden van uw team criteria vinden die voor een bepaalde pagina zinnig zijn, zoals criteria die het beste bij de winkelwagentje of een mediagina horen. |
| Niet-compatibele criteria filteren | Schakel deze optie in om alleen die criteria weer te geven waarbij de geselecteerde pagina de vereiste gegevens doorgeeft. Niet alle criteria worden op elke pagina correct uitgevoerd. De pagina of het kader moet worden doorgegeven `entity.id` `entity.categoryId` of de huidige aanbevelingen voor het item of de huidige categorie moeten compatibel zijn. Over het algemeen is het beter alleen compatibele criteria te laten zien. Schakel deze optie echter uit als u incompatibele criteria voor de activiteit wilt gebruiken.<br>U wordt aangeraden deze optie uit te schakelen als u een oplossing voor tagbeheer gebruikt.<br>Zie Veelgestelde vragen over [Recommendations voor meer informatie over deze optie](/help/c-recommendations/c-recommendations-faq/recommendations-faq.md). |
| Standaardhostgroep | Selecteer de standaardhostgroep.<br>U kunt de hostgroep gebruiken om de beschikbare items in uw catalogus te scheiden voor verschillende toepassingen. U kunt bijvoorbeeld hostgroepen gebruiken voor ontwikkelings- en productieomgevingen, verschillende merken of verschillende geografische locaties. Standaard zijn de voorvertoningsresultaten in Cataloguszoekopdrachten, Verzamelingen en Uitsluitingen gebaseerd op de standaardhostgroep. (U kunt ook een andere hostgroep selecteren om een voorvertoning van de resultaten weer te geven met behulp van het filter Omgeving.) Nieuwe toegevoegde items zijn standaard beschikbaar in alle hostgroepen, tenzij een milieu-id is opgegeven bij het maken of bijwerken van het item. De geleverde aanbevelingen hangen van de gastheergroep af die in het verzoek wordt gespecificeerd.<br>Als u uw producten niet ziet, zorg ervoor dat u de correcte gastheergroep gebruikt. Bijvoorbeeld, als u opstelling uw aanbeveling om een het opvoeren milieu te gebruiken en u uw gastheergroep aan het Opvoeren plaatst, zou u uw inzamelingen in het opvoeren milieu voor de te tonen producten kunnen moeten opnieuw creëren. Om te zien welke producten in elke milieu beschikbaar zijn, gebruik CatalogusOnderzoek met elke milieu. U kunt ook een voorvertoning weergeven van de inhoud van Recommendations-verzamelingen en -uitsluitingen voor een geselecteerde omgeving (hostgroep).<br>**Opmerking:** Nadat u de geselecteerde omgeving hebt gewijzigd, moet u op Zoeken klikken om de geretourneerde resultaten bij te werken.<br>Het [!UICONTROL Environment] filter is beschikbaar op de volgende plaatsen in [!DNL Target] UI:<ul><li>Catalogus zoeken ([!UICONTROL Recommendations] > Cataloguszoekopdracht)</li><li>Verzameling maken, dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])</li><li>Dialoogvenster Verzameling bijwerken ([!UICONTROL Recommendations > Collections > Edit])</li><li>Dialoogvenster Uitsluiting maken ([!UICONTROL Recommendations > Exclusions > Create New])</li><li>Dialoogvenster Uitsluiting bijwerken ([!UICONTROL Recommendations > Exclusions > Edit])</li></ul>Zie [Gastheren](/help/administrating-target/hosts.md)voor meer informatie. |
| Basis-URL miniatuur | Als u een basis-URL instelt voor uw productcatalogus, kunt u relatieve URL&#39;s gebruiken wanneer u miniaturen van uw producten opgeeft wanneer u de URL van de miniatuur doorgeeft.<br>Bijvoorbeeld: hiermee<br>`"entity.thumbnailURL=/Images/Homepage/product1.jpg"`<br>stelt u een URL in ten opzichte van de basis-URL van de miniatuur. |
| Recommendations API Token | Gebruik dit token in Recommendations API-aanroepen, zoals de Download API. |
