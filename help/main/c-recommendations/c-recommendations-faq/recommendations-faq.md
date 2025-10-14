---
keywords: problemen oplossen;veelgestelde vragen;Veelgestelde vragen;Veelgestelde vragen;aanbevelingen;speciale tekens;weging van kenmerken;gelijkenis van inhoud
description: Bekijk een lijst van vaak gestelde vragen en antwoorden over  [!DNL Target Recommendations]  activiteiten.
title: Waar kan ik Vragen en Antwoorden over  [!DNL Recommendations] vinden?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: aaa52923-1c2d-44ae-bd89-671329222077
source-git-commit: 18f6c06aa06e9526ee65bd3cc0f9b552c91c10e7
workflow-type: tm+mt
source-wordcount: '3444'
ht-degree: 0%

---

# Veelgestelde vragen over aanbevelingen

Lijst met veelgestelde vragen (FAQ&#39;s) over [!DNL Adobe Target] [!DNL Recommendations] -activiteiten.

## Weergeven [!DNL Recommendations] -objecten die via API zijn gemaakt in de [!DNL Target] -gebruikersinterface?

Ja, [!UICONTROL Recommendations] -objecten ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections] en [!UICONTROL Exclusions]) die via de API zijn gemaakt, zijn beschikbaar in de gebruikersinterface en kunnen worden bewerkt via de API of de [!DNL Target] gebruikersinterface.

## Kan ik met de API&#39;s van [!DNL Target] visuele aanbiedingen beheren die door [!DNL Target] in de gebruikersinterface zijn gemaakt?

Nee. [!DNL Recommendations] -activiteiten met visuele aanbiedingen die zijn gemaakt in de [!DNL Target] -gebruikersinterface, kunnen niet worden beheerd met de [!DNL Target] -API&#39;s. Hoewel deze activiteiten worden weergegeven in de lijst van [!UICONTROL Activities] , kunt u ze niet lezen of bijwerken (met GET/PUT).

## Waarom geeft [!UICONTROL Catalog Search] niet de juiste resultaten weer wanneer ik zoek naar een aangepast kenmerk met een numerieke waarde?

Wanneer u een cataloguszoekopdracht uitvoert op een aangepast kenmerk met een numerieke waarde, wordt het aangepaste kenmerk in de resultaten behandeld als een tekenreeks in plaats van een numerieke waarde.

Er is momenteel geen functionaliteit beschikbaar waarmee klanten het type van een kenmerk kunnen wijzigen. Om een verandering aan te brengen, [&#x200B; open een klantenkwestie &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) van verwijzingen voorzien van de attributen die het type vereisen dat van koord in numeriek wordt veranderd.

## Hoe lang duurt het voordat updates van items in mijn catalogus op mijn site worden weergegeven?

Het tijdkader en de resultaten variëren, afhankelijk van hoe de items worden bijgewerkt.

| Source | Details |
| --- | --- |
| Itemkenmerken bijgewerkt via mbox of API | <ul><li>Aanbevelingen worden binnen 15 minuten bijgewerkt.</li><li>Bestaande aanbevelingen en itemkenmerken worden weergegeven totdat updates beschikbaar zijn.</li><li>Zoekopdracht in catalogus wordt bijgewerkt na catalogusindex (3-8 uur).</li></ul> |
| Itemkenmerken bijgewerkt via feed | <ul><li>Aanbevelingen worden bijgewerkt na inname van het voer (2-8 uur).</li><li>Bestaande aanbevelingen en itemkenmerken worden weergegeven totdat updates beschikbaar zijn.</li><li>Zoekopdracht in catalogus wordt bijgewerkt na invoer (2-8 uur) en na volgende catalogusindex (3-8 uur). Zoekopdrachten voor catalogi worden binnen 5-16 uur bijgewerkt.</li></ul> |
| Item dat via de gebruikersinterface of API van [!DNL Target] uit de catalogus is verwijderd | <ul><li>Aanbevelingen worden binnen 15 minuten bijgewerkt.</li><li>Bestaande aanbevelingen en itemkenmerken worden weergegeven totdat updates beschikbaar zijn.</li><li>Zoekopdracht in catalogus wordt bijgewerkt na catalogusindex (3-8 uur).</li></ul> |
| Item dat via mbox of API aan de catalogus is toegevoegd | <ul><li>Aanbevelingen worden bijgewerkt nadat het algoritme is uitgevoerd. Algorithm-run is elke 12 uur gepland voor algoritmes van 1 tot 2 dagen en elke 24 uur voor algoritmen van 7 of meer dagen.</li><li>Bestaande aanbevelingen worden weergegeven totdat updates beschikbaar zijn als het toegevoegde item geen gevraagde sleutel is.</li><li>Back-upaanbevelingen worden weergegeven totdat updates beschikbaar zijn als het toegevoegde item een gevraagde sleutel is.</li><li>Zoekopdracht in catalogus wordt bijgewerkt na catalogusindex (3-8 uur).</li></ul> |
| Item dat via feed aan de catalogus is toegevoegd | <ul><li>Aanbevelingen worden bijgewerkt na inname van het voer (2-8 uur). De volgende algoritmelooppas wordt gepland om de 12 uur voor 1-2 dagalgoritmen en om de 24 uur voor 7+ dagalgoritmen. Aanbevelingen worden binnen 2-32 uur in totaal bijgewerkt.</li><li>Bestaande aanbevelingen worden weergegeven totdat updates beschikbaar zijn als het toegevoegde item geen gevraagde sleutel is.</li><li>Back-upaanbevelingen worden weergegeven totdat updates beschikbaar zijn als het toegevoegde item een gevraagde sleutel is.</li><li>Zoekopdracht in catalogus wordt bijgewerkt na invoer (2-8 uur) en na catalogusindex (3-8 uur). Zoekopdrachten voor catalogi worden binnen 5-16 uur bijgewerkt.</li></ul> |

Nadat u een feed-bestand hebt geïmporteerd of nadat u eenheidupdates hebt ontvangen via API of mbox, worden de volgende wijzigingen in minder dan 60 minuten doorgevoerd:

* Als een item eerder was uitgesloten maar nu moet worden opgenomen, wordt het item opgenomen in de volgende reeks algoritmen (12-24 uur).

  Deze situatie doet zich voor omdat [!DNL Target] zowel online als offline uitsluitingen toepast. Wanneer een item pas wordt uitgesloten, wordt de online uitsluiting snel toegepast. Wanneer een item pas wordt opgenomen, gaat de onlineuitsluiting snel weg, maar de offline uitsluiting gaat pas weg als het volgende algoritme wordt uitgevoerd.

* Als een item eerder was opgenomen, maar nu moet worden uitgesloten, wordt het item uitgesloten volgens de tijdlijn die hierboven wordt besproken op basis van de voederbron (15 minuten via mbox/API of 12-24 uur via feed).

De volgende wijzigingen worden pas doorgevoerd wanneer het volgende algoritme wordt uitgevoerd (binnen 12-24 uur):

* Itemkenmerken die worden gebruikt in de regels voor verzamelingen die worden gebruikt voor de activiteit.
* Objectkenmerken die worden gebruikt in een speciale actie die is gebaseerd op een kenmerk of verzameling dat aan de activiteit is gekoppeld.
* Objectcategorie waarin het item wordt weergegeven voor &quot;Huidige rubriek&quot; of &quot;Favoriete rubriek&quot; in de hoogste verkopers of het meest bekeken algoritme.
* Het rangschikken van geadviseerde punten wanneer het attribuut veranderde is een douaneattribuut dat als douanetoets voor een algoritme wordt gebruikt.
* Rangschikking van aanbevolen items op basis van een of meer gewijzigde kenmerken wanneer de logica van de aanbeveling &quot;Items met vergelijkbare kenmerken&quot; is, wanneer de wegingsfactoren &quot;Gelijksoortigheid van inhoud&quot; worden gebruikt of wanneer de factoren &quot;Afweging van kenmerken&quot; worden gebruikt.

>[!NOTE]
>
>Een voederdossier wordt beschouwd als ingevoerd wanneer zijn status van &quot;het Importeren van Punten&quot;in &quot;het Voorbereiden van de Updates van de Index van het Onderzoek&quot; verandert. Het kan meer dan 60 minuten duren voordat updates worden weergegeven in de gebruikersinterface van Cataloguszoekopdracht. Het zoeken naar catalogi is bijgewerkt wanneer de status van de feed verandert in &quot;Updates voltooid&quot;. Zelfs als Catalog Search nog niet bijgewerkt is, geeft uw site updates van de hierboven vermelde tijdframes weer. De meest recente update van de index van het Onderzoek van de Catalogus wordt getoond op de pagina van het Onderzoek van de Catalogus.

## Hoe lang duurt het voordat een wijziging in de configuratie van mijn [!UICONTROL Recommendations] activiteit, aanbieding, promoties of criteria op mijn site wordt weerspiegeld?

* Een wijziging in de instellingen voor speciale acties kan maximaal vijf uur duren voordat deze op de site worden weergegeven.
* Een wijziging in andere criteria wordt mogelijk pas doorgevoerd bij de volgende uitvoering van het algoritme:

   * Bepaalde criteria-instellingen (bijvoorbeeld &#39;toevoeging van een regel voor dynamische insluiting&#39;) worden direct weerspiegeld.
   * Andere criteria kunnen de montages (bijvoorbeeld &quot;verwijdering van een dynamische inclusieregel&quot;, verandering van raadplegingsvenster, etc.) niet tot de volgende algoritmelooppas worden opgenomen.
   * De looppas van het algoritme wordt teweeggebracht door deze veranderingen maar kan tot 24 uren vergen om worden voltooid. Algoritmen lopen ook op een geplande basis om de 12-24 uur.

## Hoe lang neemt het voor het gedrag van een gebruiker (bijvoorbeeld, klikkend product A en het kopen product B) om in de aanbevelingen *worden weerspiegeld dat* gebruiker ontvangt?

* Momenteel bekeken/gekochte product/inhoud beïnvloeden de aanbevelingen de gebruiker op de zelfde pagina/ [!DNL Target] inhoudverzoek ontvangt.
* Historisch gebruikersgedrag, zoals &quot;laatst bekeken product,&quot;het meest bekeken product,&quot;en algemene het bekijken/het kopen geschiedenis wordt bijgewerkt met dat verzoek en beïnvloedt de aanbevelingen die de gebruiker op het volgende pagina ontvangt [!DNL Target] inhoudsverzoek. De algoritmen &quot;Recent bekeken items&quot; en &quot;Aanbevolen voor u&quot; werken bijvoorbeeld bij met elke productweergave/aankoop en worden weergegeven in de volgende inhoudsaanvraag.

## Hoe lang duurt het voor het gedrag van een gebruiker (bijvoorbeeld, klikkend product A en het kopen product B) om in de aanbevelingen *worden weerspiegeld andere* gebruikers ontvangen?

Het gedrag van geaggregeerde gebruikers wordt opgenomen in de verwerking van offlinealgoritmen, waarbij elk algoritme elke 12-24 uur wordt uitgevoerd.

## Wat moet ik doen als speciale karakters mijn serie breken? {#section_D27214116EE443638A60887C7D1C534E}

Gebruik beschermde waarden in JavaScript. Aanhalingstekens ( &quot; ) kunnen de array afbreken. Het volgende codefragment is een voorbeeld van beschermde waarden:

```
#set($String='') 
#set($escaper=$String.class.forName('org.apache.commons.lang.StringEscapeUtils')) 
<script type="text/javascript"> 
console.log("$escaper.escapeJavaScript($entity1.name)") 
console.log("$escaper.escapeJavaScript($entity2.name)") 
console.log('$escaper.escapeJavaScript($entity3.name)') 
names.push("$escaper.escapeJavaScript($entity4.name)") 
</script>
```

## Waarom zijn niet alle criteria, met inbegrip van douanecriteria, beschikbaar voor selectie wanneer het creëren van een activiteit van Aanbevelingen? {#section_B2265AC8B8A94E0298D495A05C5D817F}

De beschikbare criteria zijn gebaseerd op de huidige categorie. Wanneer u aanbevelingen aanbiedt, geeft de algoritmekiezer criteria weer op basis van categorie-id.

Als de plaats waarop u deze criteria toepast niet de categorie ID bevat, zijn bepaalde criteria niet beschikbaar in de algoritmekiezer.

Als u een locatie gebruikt waar categorie-id aanwezig is in het vak, bevat de kiezer voor criteria alle toepasselijke criteria.

[!DNL Target] heeft a [&#x200B; Incompatibele Criteria van de Filter &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/recommendations.html?lang=nl-NL){target=_blank} plaatsen om intelligent filtreren van de algoritmekiezer te controleren.

>[!NOTE]
>
>Deze instelling is alleen van toepassing op activiteiten die zijn gemaakt in de map [!UICONTROL Visual Experience Composer] (VEC). Deze instelling is niet van toepassing op activiteiten die zijn gemaakt in de Form-Based Experience Composer ([!DNL Target] heeft geen locatiecontext).

Klik op [!UICONTROL Filter Incompatible Criteria] > [!UICONTROL Recommendations] om de instelling [!UICONTROL Settings] te openen:

![&#x200B; recs_settings_filter beeld &#x200B;](assets/recs_settings_filter.png)

Als de instelling [!UICONTROL Filter Incompatible Criteria] NIET is ingeschakeld, filtert [!DNL Target] geen algoritmen in de Algorituurkiezer en worden alle algoritmen weergegeven.

Als de instelling [!UICONTROL Filter Incompatible Criteria] is ingeschakeld, leest [!DNL Target] in VEC-activiteiten entiteit-id en categorie-id van de geselecteerde locatie en worden vervolgens algoritmen weergegeven op basis van `currentItem|currentCategory` (als er respectievelijke waarden aanwezig zijn op die locatie). Hierdoor worden standaard alleen compatibele algoritmen voor de geselecteerde locatie weergegeven in de algoritmekiezer.

Als de instelling [!UICONTROL Filter Incompatible Criteria] is ingeschakeld, kunt u nog steeds niet-compatibele algoritmen weergeven door het selectievakje [!UICONTROL Compatible] uit te schakelen terwijl u criteria selecteert.

![&#x200B; compatible_checkbox beeld &#x200B;](assets/compatible_checkbox.png)

De volgende lijst bevat speciale gevallen waarin [!DNL Target] het selectievakje [!UICONTROL Compatible] niet weergeeft:

* Zowel entiteitskaart als categorie ID zijn aanwezig op de plaats, dan niets wordt gefilterd.
* U gebruikt [!DNL mbox.js] versie 55 of eerder.
* Geen mbox vraag wordt in brand gestoken van de pagina (!config.isAutoCreateGlobalMbox &amp;&amp; !config.isRegionalMbox)
* [!DNL Target] -parameters zijn niet gedefinieerd.

## Wat moet ik doen als een verzameling in Aanbevelingen naar nul (0) gaat? {#section_E2DB2FE67CF24EEC81412BFF3FA6385D}

Overweeg de volgende informatie als u een inzameling ziet gaan naar nul die eerder niet bij nul was:

* U kunt de verzameling opnieuw opslaan en zien of het nummer wordt bijgewerkt. Door op te slaan, herstelt de inzameling alle algoritmen die die inzameling gebruiken.
* Kijk je naar de juiste omgeving? Ga naar [!DNL /target/products.html#recsSettings] om te dubbelklikken (zoals hieronder wordt weergegeven).

  ![&#x200B; product_catalog beeld &#x200B;](assets/product_catalog.png)

* Is uw index up-to-date? Ga naar [!DNL /target/products.html#productSearch] en controleer hoeveel uren de index is (bijvoorbeeld &quot;Geïndexeerde 3 uur geleden&quot;). U kunt de index naar wens vernieuwen.
* Heeft u iets in de feed of de gegevenslaag gewijzigd waardoor de entiteiten niet meer overeenkomen met de verzamelingsregels? Zorg ervoor dat uw HOOFDLETTERS overeenkomen (hoofdlettergevoelig).
* Is uw feed gelukt? Heeft iemand de FTP-map, het wachtwoord enzovoort gewijzigd?
* [!DNL Target] doet zijn best om updates voor de levering (op de pagina/app van de klant) zo snel mogelijk uit te voeren. Toch moet [!DNL Target] ook een representatie in de gebruikersinterface bieden voor de markeerteken. [!DNL Target] zorgt ervoor dat de leveringsupdates niet worden vertraagd totdat de UI-updates gesynchroniseerd zijn. U kunt [&#x200B; mboxTrace &#x200B;](/help/main/c-activities/c-troubleshooting-activities/content-trouble.md) gebruiken om te zien wat in het systeem op het tijdstip is een verzoek binnen komt.

## Wat is het verschil tussen de algemene weging van de Waarden van Attributen en Inhoud gelijksoortig-specifieke attributen? {#section_FCD96598CBB44B16A4C6C084649928FF}

Kenmerkweging bestaat in twee vormen: &quot;weging van standaardkenmerken&quot; en &quot;weging van gelijkenis van inhoud&quot;.

De &quot;Standaard kenmerkenweging&quot; is van toepassing op de meeste, zo niet alle, definitietypen (niet alleen de Gelijksoortigheid van de Inhoud). Dit type weging geeft meer gewicht aan bepaalde kenmerkwaarden. In het volgende voorbeeld krijgen Nike-producten een reliëf in de aanbevelingen voor uitvoer.

![&#x200B; attribute_weight_example beeld &#x200B;](assets/attribute_weighting_example.png)

De &quot;weging van de gelijksoortige eigenschappen van de inhoud&quot;is slechts op de criteria van de Gelijksoortigheid van de Inhoud van toepassing.

Dit type weging is dynamischer en is gebaseerd op de huidige &quot;aanbeveling key&quot; (het momenteel bekeken item). In het volgende voorbeeld (merk x 16), als een bezoeker Nike sneakers zou bekijken, zal die bezoeker eerder andere Nike-producten (niet noodzakelijkerwijs alleen sneakers) dan concurrenten-sneakers aanraden. Als een bezoeker Adidas sneakers bekijkt, zal die bezoeker eerder Adidas producten worden geadviseerd.

![&#x200B; content_similarity_example beeld &#x200B;](assets/content_similarity_example.png)

## Waarom kan [!DNL Target] soms geen aanbevelingen weergeven? {#section_DB3F40673AED42228E407C05437D99E9}

[!DNL Target] kan soms geen aanbevelingen weergeven vanwege het lage aantal beschikbare aanbevelingen.

Het aantal waarden dat per criterium wordt gegenereerd, is driemaal zo groot als het aantal entiteiten dat in het ontwerp is opgegeven. Het filtreren van runtime (bijvoorbeeld, inventaris, mbox kenmerkenaanpassing) wordt toegepast nadat de 3x waarden worden geproduceerd, zodat is het mogelijk met minder dan 3x waarden bij leveringstijd beëindigen. Om deze situatie te verzachten, vergroot u het aantal entiteiten in het ontwerp door andere entiteiten te verbergen.

De volgende JavaScript kan aan het begin van het ontwerp worden gebruikt om het aantal gevraagde entiteiten te verhogen. In dit voorbeeld is het aantal aangevraagde entiteiten 30 (3x10).

```
#foreach($entity in $entities) 
 #if( $foreach.count > 10 ) 
  #break 
 #end 
 #set ($foo = $entity.id) 
#end 
```

## Wat is de formaatgrens van een API vraag voor tussenvoegsel/updateproducten? Kan ik 50.000 producten in één vraag bijwerken gebruikend API in plaats van een voer? {#section_434FE1F187B7436AA39B7C14C7895168}

[!DNL Target] legt een postlimiet van 50 MB op toepassingsniveau op. Dit is echter alleen wanneer u de header van het inhoudstype `application/x-www-form-urlencoded` doorgeeft.

Je zou zeker kunnen proberen om 50.000 producten in één enkele vraag te verzenden. Als het ontbreekt, kunt u het in partijen verdelen. Adobe raadt aan dat klanten hun aanroepen opsplitsen in 5.000 of 10.000 productbatches om de kans op een time-out door systeembelasting te verkleinen.

## Moet ik de naam van de box specificeren wanneer het creëren van de criteria van Aanbevelingen, bevorderingen, of malplaatje testende regels? {#section_FFA42ABCC5954B48A46526E32A3A88A2}

Wanneer u criteria, promoties of testregels voor sjablonen maakt op basis van een mbox-parameter, vraagt `mboxParameter` u niet langer om `mboxName` . mbox name is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen.

De gewenste parameter selecteren:

* Selecteer een parameternaam in de lijst wanneer u criteria, promoties of testregels voor sjablonen maakt. Typ de eerste tekens van de gewenste parameternaam of typ de volledige naam van de gewenste parameternaam.
* Als u de naam van het selectievakje, maar niet de naam van de parameter, onthoudt, gebruikt u het selectievakje om te filteren op een bekend selectievakje dat de gewenste parameter doorgeeft.

Bij beide methoden is er geen koppeling tussen de mbox en de parameter. De criteria, de bevordering, of de malplaatje testende regel werken die op parameter over alle vakjes worden gebaseerd die die parameter overgaan.

Als u bestaande criteria, bevordering, of malplaatje het testen regel uitgeeft, tonen de het filtreren criteria met de mbox naam die tijdens verwezenlijking werd verstrekt.

## Waarom kan ik mijn activiteit van de Aanbevelingen van de erfenis niet bewaren na het bepalen van een nieuw publiek? {#section_1E47C40B1FE7479BAC3EE0F50CE7C2C4}

Zorg ervoor dat het publiek een unieke naam heeft. Als u het publiek de zelfde naam zoals een bestaand publiek gaf, kunt u niet uw activiteit van de erfenisAanbevelingen opslaan (een activiteit van Aanbevelingen die vóór Oktober 2016 wordt gecreeerd).

## Wat is de maximumgrootte van een CSV-bestand voor een feed-upload? {#section_20F1AF4839A447B9889B246D6E873538}

Het aantal rijen of de bestandsgrootte voor het uploaden van een CSV-bestand van een feed is niet hard beperkt. Adobe raadt echter aan om de CSV-bestandsgrootte te beperken tot 1 GB om fouten tijdens het uploaden van bestanden te voorkomen. Als de grootte van het bestand groter is dan 1 GB, kan het bestand idealiter in meerdere feed-bestanden worden gesplitst. Het maximumaantal kolommen voor aangepaste kenmerken is 100 en de aangepaste kenmerken zijn beperkt tot 4096 tekens. Andere grenzen op de lengte van vereiste kolommen zijn beschikbaar op de [[!DNL Target]  pagina van Beperkingen &#x200B;](/help/main/r-troubleshooting-target/target-limits.md#reference_BEFE60C3AAA442FF94D4EBFB9D3CC9B1).

## Kan ik een entiteit dynamisch uitsluiten? {#exclude}

In het vraagkoord, kunt u entiteit IDs voor entiteiten overgaan die u van uw aanbevelingen wilt uitsluiten. U kunt bijvoorbeeld items uitsluiten die zich al in het winkelwagentje bevinden.

Gebruik de parameter `excludedIds` mbox om de uitsluitingsfunctionaliteit in te schakelen. Deze parameter verwijst naar een lijst met door komma&#39;s gescheiden id&#39;s. Bijvoorbeeld `mboxCreate(..., "excludedIds=1,2,3,4,5")` . De waarde wordt verzonden wanneer het verzoeken van om aanbevelingen.

De uitsluiting wordt alleen uitgevoerd voor de huidige [!DNL Target] -aanroep; items worden niet uitgesloten bij volgende [!DNL Target] -aanroepen, tenzij de waarde `excludedIds` opnieuw wordt doorgegeven. Als u items in het winkelwagentje wilt uitsluiten van aanbevelingen op elke pagina, blijft u de waarde `excludedIds` op elke pagina doorgeven.

>[!NOTE]
>
>Als te veel entiteiten zijn uitgesloten, gedragen de aanbevelingen zich alsof er niet genoeg entiteiten zijn om het advisemalplaatje te vullen.

Als u `entityIds` wilt uitsluiten, voegt u de token `&excludes=${mbox.excludedIds}` toe aan de inhoud-URL van de aanbieding. Wanneer de inhoud-URL wordt geëxtraheerd, worden de vereiste parameters vervangen door de huidige parameters voor mbox-aanvragen.

Deze functie is standaard ingeschakeld voor nieuwe aanbevelingen. Bestaande aanbevelingen moeten worden opgeslagen om dynamisch uitgesloten entiteiten te ondersteunen.

## Wat betekent de reactie NO_CONTENT soms teruggekeerd in de inhoud van Aanbevelingen spoor?

NO_CONTENT wordt geretourneerd wanneer aanbevelingen niet beschikbaar zijn voor het gevraagde algoritme en de toetsencombinatie. Over het algemeen, komt deze situatie voor wanneer de steunen voor het algoritme en één of meerdere van het volgende ook waar zijn onbruikbaar gemaakt:

* De resultaten zijn nog niet gereed.

  Deze situatie komt typisch voor wanneer eerst het bewaren van een pas gecreëerde activiteit of nadat de configuratieveranderingen in de inzameling, de criteria, of de bevorderingen worden aangebracht die in de activiteit worden gebruikt.

* De resultaten zijn klaar, maar zijn nog niet in het voorgeheugen ondergebracht bij de dichtstbijzijnde randserver, voor de gevraagde algoritme/toetsencombinatie.

  De aanvraag start een cachebewerking. Dit probleem moet dus worden opgelost nadat de pagina enkele keren opnieuw is geladen en/of een paar minuten is verstreken.

* De resultaten zijn gereed, maar niet beschikbaar voor de opgegeven sleutelwaarde.

  Deze situatie komt typisch voor wanneer het verzoeken van om aanbevelingen voor een punt dat aan de catalogus na de meest recente looppas van het algoritme werd toegevoegd en zal na de volgende algoritmelooppas oplossen.

* Gedeeltelijke sjabloonrendering is uitgeschakeld en er zijn onvoldoende resultaten beschikbaar om de sjabloon te vullen.

  Deze situatie komt typisch voor wanneer u een dynamische integratieregel hebt, die veel punten van de mogelijke resultaten agressief filtert. Om situatie te vermijden, laat steunen toe en pas niet de inclusieregel op steunen toe, of gebruik achtereenvolgens de criteria met minder-agressief gefilterde criteria.

## Blijven aanbevelingen op basis van onlangs weergegeven items op meerdere apparaten voor één bezoeker? {#persist-across-devices}

Wanneer een bezoeker een sessie start, is de sessie-id gekoppeld aan één Edge-computer en wordt een cache met een tijdelijk profiel opgeslagen op deze Edge-computer. De volgende verzoeken van de zelfde zitting lezen dit profielgeheime voorgeheugen, met inbegrip van onlangs bekeken punten.

Wanneer de sessie wordt beëindigd (doorgaans wanneer deze verloopt na 30 minuten zonder activiteit), wordt de sessiestatus, inclusief onlangs weergegeven items, voortgezet naar een meer permanente profielopslag in dezelfde geografische rand.

De volgende zittingen van verschillende apparaten kunnen dan tot deze onlangs bekeken punten toegang hebben zolang de nieuwe zitting met het klantenprofiel via zelfde Marketing Cloud identiteitskaart (MCID), identiteitskaart van Experience Cloud (ECID), of CustomerID/mbox3rdPartyId wordt verbonden.

Als een bezoeker twee actieve zittingen tezelfdertijd heeft, onlangs bekeken punten op één apparaat niet de onlangs bekeken punten op het andere apparaat bijwerken, tenzij de apparaten worden gedwongen om zittingsidentiteitskaart te delen. Er is een mogelijke oplossing voor het probleem, maar [!DNL Target] biedt geen directe ondersteuning voor het delen van een sessie-id op meerdere apparaten. De klant moet deze id zelf delen.

Dit gedrag treedt nog steeds op als een bezoeker actief is op het ene apparaat en vervolgens een paar minuten later actief wordt op het andere apparaat. De sessie van het eerste apparaat verloopt niet gedurende 30 minuten en er kan maximaal vijf minuten vertraging optreden voordat de profielstatus naar de permanente status wordt geschreven en wordt verwerkt. 35 minuten laten verlopen voordat de sessie verloopt en het profiel moet worden opgeslagen wanneer dit gedrag wordt getest.

Als de bezoeker niet tegelijkertijd twee actieve sessies heeft, worden onlangs bekeken items op het ene apparaat bijgewerkt met de onlangs weergegeven items op het andere apparaat zolang de sessie is beëindigd. Laat 35 minuten verlopen voor de sessie wanneer u dit gedrag test.

## Kan ik een algoritme gebruiken dat is gemaakt in [!DNL Adobe Recommendations Classic] in [!DNL Recommendations Premium] ?

Een algoritme dat is gemaakt in [!DNL Recommendations Classic] , wordt niet ondersteund in [!DNL Recommendations Premium] . U kunt het oude algoritme wellicht gebruiken in [!DNL Target Premium] , maar het algoritme kan synchronisatieproblemen veroorzaken wanneer u de activiteit in de [!DNL Target Premium] -gebruikersinterface deactiveert of verwijdert. Voor meer informatie over de verschillen tussen de twee oplossingen, zie [[!DNL Recommendations Classic]  tegenover  [!DNL Recommendations]  activiteiten in  [!DNL Target Premium]](/help/main/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md).

## Hoe kan ik alleen nieuwe artikelen of video&#39;s aanbevelen? {#recommend-new-articles}

Sommige klanten in media en uitgevers willen ervoor zorgen dat de aanbevolen items alleen de nieuwste artikelen of video&#39;s bevatten. Een [!DNL Target] -klant heeft bijvoorbeeld de volgende aanpak gebruikt om artikelen van minder dan 60 dagen aan te bevelen:

1. Geef de publicatiedatum van het artikel in de notatie JJMMDDD door als een attribuut van de douaneentiteit.
1. Maak een profielscript dat de datum minus 60 dagen van vandaag is, ook in de notatie JJJMMDD.
1. Gebruik een dynamisch inclusiefilter in de criteria zodat `publish date > today's date minus 60 days`.

### Geef de publicatiedatum door als een aangepast entiteitskenmerk:

| Entiteitskenmerk | Voorbeeld |
| --- | --- |
| issueDate | 2021218 |
| lastViewDate | 2021701 |
| parentCategory | commentaar |
| publishDate | 20210113 |
| publishDateDisplay | 13 jan. 2021 |

### Configureer het profielscript:

![&#x200B; het profielmanuscript van de Steekproef &#x200B;](/help/main/c-recommendations/c-recommendations-faq/assets/sample-profile-script.png)

### Configureer de insluitingsregel:

![&#x200B; de integratieregel van de Steekproef &#x200B;](/help/main/c-recommendations/c-recommendations-faq/assets/sample-inclusion-rule.png)

>[!NOTE]
>
>Dit voorbeeld kan ook worden uitgevoerd door parameter-overeenkomsten te gebruiken en de waarde `priorDate60` door te geven als een mbox-parameter.

### Wat zijn enkele bekende problemen bij het gebruik van [!DNL Recommendations] -activiteiten?

Hier volgen bekende problemen met [!UICONTROL Recommendations] -activiteiten:

* Wanneer [!DNL Target] een JSON-aanbieding met getOffer() retourneert, retourneert deze met het type JSON. Als u echter een ontwerp met JSON-aanbevelingen retourneert, retourneert dit met een type HTML.
* Verlopen entiteiten zijn na 60 dagen na ontvangst van geen updates via feed of API correct verlopen. De verlopen entiteiten worden echter na afloop niet uit de zoekindex van catalogus verwijderd. Entiteiten die via feed of API zijn verwijderd, worden momenteel ook niet verwijderd uit de zoekindex van de catalogus. (IRI-857)
* Aanbevelingen Aanbiedingen in A/B en Ervaring gerichte activiteiten tonen geen visuele voorvertoning van de bak met aanbevelingen (TGT-33426)
* Activiteiten van aanbevelingen die via API zijn gemaakt, kunnen in de gebruikersinterface worden weergegeven, maar kunnen alleen via API worden bewerkt.
* De voedingsstatus van de aangepaste criteria die wordt weergegeven in de weergave Criteria (kaart), wordt elke tien minuten vernieuwd en kan in zeldzame gevallen meer dan tien minuten verouderd zijn. De status die wordt weergegeven in de bewerkingsweergave Aangepaste criteria wordt opgehaald in real-time en is altijd up-to-date. (TGT-35896, TGT-36173)
