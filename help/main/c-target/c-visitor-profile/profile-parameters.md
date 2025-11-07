---
keywords: Profielscript;profielscriptkenmerken;profielscript, aanbevolen methoden;foutopsporing;scripts;profielscripts;kenmerken;kenmerk;parameter
description: Leer over bezoeker-specifieke attributen die in het profiel van de bezoeker worden opgeslagen om informatie over te verstrekken die in uw Adobe  [!DNL Target]  activiteiten kan worden gebruikt.
title: Wat zijn profielkenmerken?
feature: Audiences
exl-id: 6c689629-bbd3-461e-9a68-5b16d4eb4250
source-git-commit: e45ac15a60c83e35b8b2b2ba29a42727faf746df
workflow-type: tm+mt
source-wordcount: '2426'
ht-degree: 0%

---

# Profielkenmerken

Profielkenmerken in [!DNL Adobe Target] zijn parameters die specifiek zijn voor een bezoeker. Deze kenmerken worden opgeslagen in het profiel van de bezoeker om informatie over de bezoeker te verstrekken die in uw activiteiten kan worden gebruikt.

Een gebruikersprofiel bevat demografische en gedragsinformatie van een bezoeker van een webpagina. Deze informatie kan leeftijd, geslacht, aangekochte producten, laatste tijd van bezoek omvatten, etc. [!DNL Target] gebruikt deze gegevens om de inhoud die deze bezoeker aanbiedt, aan te passen.

Wanneer een bezoeker door uw website bladert of wanneer de bezoeker voor een andere sessie terugkeert, kunnen de opgeslagen profielkenmerken in het profiel worden gebruikt om inhoud of logboekinformatie voor segmentfiltering als doel in te stellen.

Profielkenmerken instellen:

1. Klik op **[!UICONTROL Audiences]** > **[!UICONTROL Profile Scripts.]**

   ![ Scripts tabel van het Profiel ](/help/main/c-target/c-visitor-profile/assets/create-script.png)

1. Klik op **[!UICONTROL Create Script]**.

   ![ creeer de dialoogdoos van het Manuscript van het Profiel ](/help/main/c-target/c-visitor-profile/assets/profile-script.png)

   De volgende typen profielkenmerken zijn beschikbaar:

   | Type parameter | Beschrijving |
   |--- |--- |
   | mbox | Direct door paginacode doorgegeven tijdens het maken van het mbox. Zie {de Parameters van 0} overgaan tot een Globale Mbox [ in de ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html){target=_blank} Gids van de Ontwikkelaar van het Doel *.*<P>**Nota**: [!DNL Target] heeft een grens van 50 unieke profielattributen per mbox vraag. Als u meer dan 50 profielkenmerken moet doorgeven aan [!DNL Target] , geeft u deze door met de methode [!UICONTROL Profile Update API] . Voor meer informatie, zie [ profielen van de Update ](https://experienceleague.adobe.com/docs/target-dev/developer/api/profile-apis/profile-api-overview.html){target=_blank} in de *Gids van de Ontwikkelaar van het Doel*. |
   | Profiel | Direct gedefinieerd met een JavaScript-codefragment. Deze fragmenten kunnen lopende totalen opslaan, zoals het totale geld dat de consument besteedt, en worden uitgevoerd op elke mbox-aanvraag. Zie *het manuscriptattributen van het Profiel* hieronder. |

## Profielscriptkenmerken {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}

Definieer een profielscriptkenmerk met het bijbehorende JavaScript-codefragment.

U kunt profielscripts gebruiken om bezoekerskenmerken voor meerdere bezoeken vast te leggen. Profielscripts zijn codefragmenten die binnen [!DNL Target] worden gedefinieerd met behulp van een vorm van JavaScript op de server. U kunt bijvoorbeeld een profielscript gebruiken om vast te leggen hoe vaak een bezoeker uw site bezoekt en wanneer die bezoeker het laatst is bezocht.

Profielscripts zijn niet hetzelfde als profielparameters. Profielparameters leggen informatie over bezoekers vast met behulp van de mbox-code-implementatie van [!DNL Target] .

## Profielscripts maken {#section_CB02F8B97CAF407DA84F7591A7504810}

Profielscripts zijn beschikbaar op het tabblad [!UICONTROL Audiences] in de interface van [!DNL Target] .

Als u een profielscript wilt toevoegen, klikt u op de tab **[!UICONTROL Profile Scripts]** **[!UICONTROL Create Script]** en schrijft u vervolgens uw script.

of

Als u een bestaand profielscript wilt kopiëren, klikt u in de lijst [!UICONTROL Profile Scripts] op het pictogram van de ovaal voor het gewenste script en klikt u vervolgens op **[!UICONTROL Duplicate]** .

Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

Profielscripts voeren profielkenmerk &#39;catchers&#39; uit op elke locatieaanvraag. Wanneer een locatieverzoek wordt ontvangen, bepaalt [!DNL Target] welke activiteit zou moeten lopen en toont inhoud die voor die activiteit en die ervaring aangewezen is. [!DNL Target] houdt ook het succes van de activiteit bij en voert relevante profielmanuscripten uit. Met dit proces kunt u informatie bijhouden over het bezoek, zoals de locatie, het tijdstip van de bezoeker, het aantal keren dat de bezoeker naar de site is geweest, als hij of zij eerder heeft gekocht, enzovoort. Deze informatie wordt vervolgens toegevoegd aan het profiel van de bezoeker, zodat u de activiteiten van die bezoeker op uw site beter kunt bijhouden.

Bij profielscriptkenmerken wordt de tag `user.` ingevoegd vóór de kenmerknaam. Bijvoorbeeld:

```
if (mbox.name == 'Track_Interest') { 
    if (profile.get('model') == "A5" &&; profile.get('subcat') == "KS6") { 
        return (user.get('A5KS6') || 0) + 1; 
    } 
}
```

Houd rekening met het volgende:

* Raadpleeg scriptkenmerken voor profielen (ook zichzelf) in de code met `user.get('parameterName')` .
* Sla variabelen op die de volgende keer dat het script wordt uitgevoerd (bij de volgende aanvraag van het mbox) met `user.setLocal('variable_name', 'value')` kunnen worden geopend. Verwijs naar de variabele met `user.getLocal('variable_name')`. Dit proces is handig voor situaties waarin u naar de datum en het tijdstip van het laatste verzoek wilt verwijzen.

  Deze waarden blijven bestaan als een profielscript, maar u hebt er alleen toegang tot binnen het script dat ze zijn ingesteld.

* Parameters en waarden zijn hoofdlettergevoelig. Komt overeen met het geval van de parameters en waarden die u ontvangt tijdens de activiteit of test.
* Zie de sectie &quot;JavaScript reference for script profile parameters&quot; hieronder voor meer JavaScript syntaxis.
* De parameter blijft in het profiel nadat het script is uitgeschakeld. Gebruikers waarvan de profielen al een parameter bevatten die in het publiek van een activiteit wordt gebruikt, kwalificeren in die activiteit.
* Profielscripts kunnen niet worden verwijderd terwijl ze in een activiteit worden gebruikt.
* Het wordt niet aanbevolen afhankelijke profielscripts te maken die het resultaat van een profielscript in een ander profielscript gebruiken. De volgorde waarin profielscripts worden uitgevoerd, is niet gegarandeerd.

## Informatiekaarten voor profielscripts weergeven {#section_18EA3B919A8E49BBB09AA9215E1E3F17}

U kunt pop-upkaarten met profielscriptinformatie weergeven, vergelijkbaar met informatiekaarten. Met deze informatiekaarten voor profielscripts kunt u een lijst weergeven met activiteiten die verwijzen naar het geselecteerde profielscript, samen met andere nuttige metagegevens.

De volgende profielscriptinformatiekaart is bijvoorbeeld toegankelijk door te klikken op het pictogram [!UICONTROL Info] voor het gewenste profielscript in de lijst ( [!UICONTROL Audiences] > [!UICONTROL Profile Scripts] ).

Het tabblad [!UICONTROL Script Info] bevat de volgende informatie: Naam, Beschrijving en scriptcode.

![ de infokaart van het Manuscript van het Profiel ](assets/profile_script_info_card.png)

Klik op **[!UICONTROL View full details]** om het publiek en de activiteiten te zien die naar het geselecteerde profielscript verwijzen.

![ de infokaart van het Manuscript van het Profiel > lusje van het Gebruik van het Manuscript ](assets/profile_script_info_card_usage_tab.png)

>[!NOTE]
>
>Op het tabblad [!UICONTROL Script Usage] worden in de volgende situaties geen activiteiten weergegeven die verwijzen naar het geselecteerde profielscript:
>
> * De activiteit bevindt zich in de status [!UICONTROL Draft] .
> * De inhoud of de aanbieding die in de activiteit wordt gebruikt gebruikt manuscriptvariabelen (of een gealigneerde aanbieding binnen de activiteit of een aanbieding binnen de bibliotheek van de Aanbieding).

## Doel schakelt profielscripts in bepaalde situaties uit {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

In [!DNL Target] worden profielscripts in bepaalde situaties automatisch uitgeschakeld, bijvoorbeeld wanneer de uitvoering te lang duurt of wanneer er te veel instructies zijn.

Wanneer een profielscript is uitgeschakeld, wordt een geel waarschuwingspictogram weergegeven naast het profielscript in de doelinterface, zoals hieronder wordt geïllustreerd:

![ profile_script_invalid beeld ](assets/profile_script_invalid.png)

Bij aanwijzen worden details op de foutweergave weergegeven, zoals hieronder wordt geïllustreerd:

![ profile_script_hover beeld ](assets/profile_script_hover.png)

De meest gangbare redenen voor het uitschakelen van profielscripts zijn:

* Een niet-gedefinieerde variabele waarnaar wordt verwezen.
* Er wordt verwezen naar een ongeldige waarde. Deze fout wordt vaak veroorzaakt door naar URL-waarden en andere door de gebruiker ingevoerde gegevens te verwijzen zonder juiste validatie.
* Er worden te veel JavaScript-instructies gebruikt. [!DNL Target] heeft een limiet van 2.000 JavaScript instructies per script, maar deze limiet kan niet eenvoudig worden berekend door de JavaScript handmatig te lezen. Rhino behandelt bijvoorbeeld alle functieaanroepen en &quot;nieuwe&quot; aanroepen als 100 instructies. Om het even welke vraag aan om het even welke functie verbruikt 100 instructies. Ook, kan de grootte van om het even welke ingangsgegevens, zoals waarden URL, de instructietelling beïnvloeden.
* Na punten niet die in de [ worden benadrukt beste praktijken ](/help/main/c-target/c-visitor-profile/profile-parameters.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) hieronder sectie.

## Aanbevolen procedures {#best}

De volgende richtlijnen zijn bedoeld om vereenvoudigde profielmanuscripten te schrijven die fout-falend-vrij zo mogelijk zijn door code te schrijven die zachtjes zakt zodat worden de manuscripten verwerkt zonder een systeem-manuscript-halt te dwingen. Deze richtsnoeren zijn het resultaat van goede praktijken die efficiënt zijn gebleken te werken. Deze richtsnoeren moeten worden toegepast in samenhang met de beginselen en aanbevelingen van de Rijnse ontwikkelingsgemeenschap.

* Stel de huidige scriptwaarde in op een lokale variabele in het gebruikersscript en stel een failover in op een lege tekenreeks.
* Valideer de lokale variabele door ervoor te zorgen dat deze geen lege tekenreeks is.
* Gebruik op tekenreeks gebaseerde manipulatiefuncties vs. Reguliere expressies.
* Gebruik limited for loops vs. open ended for or while loops.
* Gebruik niet meer dan 1.300 tekens of 50 lusherhalingen.
* Niet meer dan 2.000 JavaScript instructies. [!DNL Target] heeft een limiet van 2.000 JavaScript instructies per script, maar deze limiet kan niet eenvoudig worden berekend door de JavaScript handmatig te lezen. Rhino behandelt bijvoorbeeld alle functieaanroepen en &quot;nieuwe&quot; aanroepen als 100 instructies. Ook, kan de grootte van om het even welke ingangsgegevens, zoals waarden URL, de instructietelling beïnvloeden.
* Houd niet alleen rekening met de scriptprestaties, maar ook met de gecombineerde prestaties van alle scripts. [!DNL Adobe] raadt in totaal minder dan 5000 instructies aan. Het tellen van het aantal instructies is niet voor de hand liggend, maar het belangrijkste is dat scripts die hoger zijn dan 2000 instructies automatisch worden uitgeschakeld. Het aantal actieve profielscripts mag niet groter zijn dan 300. Elk manuscript wordt uitgevoerd met elke enige brievenbusvraag. Voer zo veel scripts uit als u nodig hebt.
* In een regex is het bijna nooit nodig om een puntster aan het begin te hebben (bijvoorbeeld: `/.*match/` , `/a|.*b/` ). De regex-zoekopdracht begint op alle posities in een tekenreeks (tenzij deze is gebonden met `^` ). Er wordt dus al een puntster gebruikt. De uitvoering van het script kan worden onderbroken als een dergelijke regex overeenkomt met een lang genoeg aantal invoergegevens (die kunnen oplopen tot honderden tekens).
* Als alles ontbreekt, verpak manuscript in probeer/vangst.
* De volgende aanbevelingen kunnen u helpen de ingewikkeldheid van het profielmanuscript beperken. Profielscripts kunnen een beperkt aantal instructies uitvoeren.

  Als beste praktijken:

   * Houd profielscripts klein en zo eenvoudig mogelijk.
   * Vermijd reguliere expressies of gebruik alleen eenvoudige reguliere expressies. Zelfs eenvoudige expressies kunnen veel instructies gebruiken om te evalueren.
   * Vermijd herhaling.
   * Profielscripts moeten op prestaties worden getest voordat ze aan [!DNL Target] worden toegevoegd. Alle profielscripts worden uitgevoerd op elke mbox-aanvraag. Als profielscripts niet correct worden uitgevoerd, duurt het langer om mbox-aanvragen uit te voeren, wat invloed kan hebben op verkeer en conversie.
   * Als de profielmanuscripten te complex worden, overweeg in plaats daarvan gebruikend [ reactietokens ](/help/main/administrating-target/response-tokens.md).

* Zie de documentatie van de JS Rhino-engine voor meer informatie.

## Fouten opsporen in profielscripts {#section_E9F933DE47EC4B4E9AF2463B181CE2DA}

De volgende methoden kunnen worden gebruikt om fouten op te sporen in profielscripts:

>[!NOTE]
>
>Als u [!DNL console.log] gebruikt in een profielscript, wordt de profielwaarde niet uitgevoerd, omdat profielscripts op de server worden uitgevoerd.

* **voeg profielmanuscripten als reactietokens toe om profielmanuscripten te zuiveren:**

  Klik in [!DNL Target] op **[!UICONTROL Administration]** , klik **[!UICONTROL Response Tokens]** en schakel vervolgens het profielscript in dat u wilt debuggen.

  Telkens wanneer u een pagina voor uw site laadt met [!DNL Target] erop, bevat een deel van de reactie van [!DNL Target] uw waarde voor het opgegeven profielscript, zoals hieronder wordt getoond:

  ![ debug_profile_script_1 beeld ](assets/debug_profile_script_1.png)

* **gebruik het mboxTrace het zuiveren hulpmiddel om profielmanuscripten te zuiveren.**

  Deze methode vereist een machtigingstoken dat u kunt genereren door te klikken op **[!UICONTROL Target]** > **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Generate Authorization Token]** in de sectie [!UICONTROL Debugger tools] .

  Vervolgens voegt u deze twee parameters toe aan de URL van de pagina na &quot;?&quot;: `mboxTrace=window&authorization=YOURTOKEN` .

  Het toevoegen van deze parameters is een weinig informatiefunctie dan het reactietoken omdat u een voor-uitgevoerde momentopname en een na-momentopname van uw profiel krijgt. Ook worden alle beschikbare profielen weergegeven.

  ![ debug_profile_script_2 beeld ](assets/debug_profile_script_2.png)

## Veelgestelde vragen over profielscript {#section_1389497BB6D84FC38958AE43AAA6E712}

**is het mogelijk om profielmanuscripten te gebruiken om informatie van een pagina te vangen die in een gegevenslaag verblijft?**

Profielscripts kunnen de pagina niet rechtstreeks lezen omdat ze aan de serverzijde worden uitgevoerd. De gegevens moeten binnen door een mbox verzoek of door andere [ methodes worden overgegaan om gegevens in Doel ](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank} te krijgen. Nadat de gegevens zich in [!DNL Target] bevinden, kunnen profielmanuscripten de gegevens als mbox parameter of profielparameter lezen.

## JavaScript-referentie voor scriptprofielparameters

Er is eenvoudige kennis van JavaScript vereist om het scriptprofiel effectief te kunnen gebruiken
parameters. Deze sectie dient als een snelle referentie om u binnen een paar minuten productief te maken met deze functionaliteit.

Parameters voor scriptprofielen vindt u onder het tabblad boxes/profielen. U kunt Javascript-programma&#39;s schrijven die elk Javascript-type (tekenreeks, geheel getal, array enzovoort) retourneren.

### Voorbeelden van scriptprofielparameters {#examples}

**Naam:** *user.recency*

```
var dayInMillis = 3600 * 24 * 1000;
if (mbox.name == 'orderThankyouPage') {
    user.setLocal('lastPurchaseTime', new Date().getTime());
}
var lastPurchaseTime = user.getLocal('lastPurchaseTime');
if (lastPurchaseTime) {
    return ((new Date()).getTime() - lastPurchaseTime) / dayInMillis;
}
```

Hiermee maakt u een variabele voor de dag, gemeten in milliseconden. Als de naam van het selectievakje `orderThankyouPage` is, stelt u een lokaal (onzichtbaar) gebruikersprofielkenmerk met de naam `lastPurchaseTime` in om de waarde van de huidige datum en tijd weer te geven. De waarde van de laatste aanschaftijd wordt gelezen en als deze is gedefinieerd, retourneert [!DNL Target] de tijd die is verstreken sinds de laatste aanschaftijd, gedeeld door het aantal milliseconden in een dag (wat resulteert in het aantal dagen sinds de laatste aanschaf).

**Naam:** *user.frequency*

```
var frequency = user.get('frequency') || 0;
if (mbox.name == 'orderThankyouPage') {
    return frequency + 1;
}
```

Maakt een variabele met de naam `frequency` en initialiseert deze naar de vorige waarde of 0 als er geen vorige waarde was. Als de naam van het selectievakje `orderThankyouPage` is, wordt de verhoogde waarde geretourneerd.

**Naam:** *user.monetaryValue*

```
var monetaryValue = user.get('monetaryValue') || 0;
if (mbox.name == 'orderThankyouPage') {
    return monetaryValue + parseInt(mbox.param('orderTotal'));
}
```

Maakt een variabele met de naam `monetaryValue` en zoekt de huidige waarde voor een bepaalde bezoeker op (of ingesteld op 0 als er geen vorige waarde was). Als de naam van het mbox `orderThankyouPage` is, wordt nieuwe monetaire waarde geretourneerd door de vorige waarde en de waarde van de parameter `orderTotal` toe te voegen die aan het mbox is doorgegeven.

**Naam:** adobeQA

```
if (page.param("adobeQA"))
     return page.param("adobeQA");
else if (page.param("adobeqa"))
     return page.param("adobeqa");
else if (mbox.param("adobeQA"))
     return mbox.param("adobeQA");
```

Creeert een geroepen variabele `adobeQA` om een gebruiker voor [ Activiteit QA ](/help/main/c-activities/c-activity-qa/activity-qa.md) te volgen.

### Objecten en methoden {#objects}

Naar de volgende objecten en methoden kan worden verwezen door scriptprofielparameters:

| Object of methode | Details |
| --- | --- |
| `page.url` | De huidige URL. |
| `page.protocol` | Het protocol dat wordt gebruikt voor de pagina (http of https). |
| `page.domain` | Het huidige URL-domein (alles vóór de eerste slash). Bijvoorbeeld `www.acme.com` in `http://www.acme.com/categories/men_jeans?color=blue&size=small` . |
| `page.query` | De queryreeks voor de huidige pagina. Alles na de &#39;?&#39;. Bijvoorbeeld `blue&size=small` in `http://www.acme.com/categories/mens_jeans?color=blue&size=small` . |
| `page.param('<par_name>')` | De waarde van de parameter die wordt aangegeven door `<par_name>` . Als de huidige URL een zoekpagina voor Google is en u `page.param('hl')` hebt ingevoerd, wordt &quot;en&quot; weergegeven voor de URL `http://www.google.com/search?hl=en& q=what+is+asdf&btnG=Google+Search` . |
| `page.referrer` | Dezelfde operaties als hierboven gelden voor referentie en landing (d.w.z. referentie.url is het URL-adres van de referentie). |
| `landing.url` , `landing.protocol` , `landing.query` en `landing.param` | Gelijkaardig aan dat van pagina, maar voor de landingspagina.<P>Als u wilt dat de URL van de bestemmingspagina naar behoren werkt, stelt u `context` > `browser` > `host` in. |
| `mbox.name` | De naam van de actieve box. |
| `mbox.param('<par_name>')` | Een mbox-parameter op basis van de opgegeven naam in het actieve mbox. |
| `profile.get('<par_name>')` | De door de client gemaakte parameter voor gebruikersprofielen krijgt de naam `<par_name>` . Als de gebruiker bijvoorbeeld een profielparameter met de naam &quot;gender&quot; instelt, kan de waarde worden geëxtraheerd met &quot;profile.gender&quot;. Retourneert de waarde van de set &quot;`profile.<par_name>`&quot; voor de huidige bezoeker; retourneert null als er geen waarde is ingesteld. `profile.get(<par_name>)` wordt gekwalificeerd als een functieaanroep. |
| `user.get('<par_name>')` | Retourneert de waarde van de set &quot;`user.<par_name>`&quot; voor de huidige bezoeker; retourneert null als er geen waarde is ingesteld. |
| `user.categoryAffinity` | Retourneert de naam van de beste categorie. |
| `user.categoryAffinities` | Retourneert een array met de beste categorieën. |
| `user.isFirstSession` | Retourneert true als het de eerste sessie van de bezoeker is. |
| `user.browser` | Retourneert de user-agent in de HTTP-header. U kunt bijvoorbeeld een expressiedoel maken dat alleen op Safari-gebruikers kan worden toegepast: `if (user.browser != null && user.browser.indexOf('Safari') != -1) { return true; }` |

### Algemene operatoren

Alle standaard JavaScript-operatoren zijn aanwezig en kunnen worden gebruikt. JavaScript-operatoren kunnen worden gebruikt voor tekenreeksen en getallen (en andere gegevenstypen). Een korte briefing:

| Operator | Beschrijving |
| --- | --- |
| `==` | Geeft gelijkheid aan. Houdt waar wanneer de operands aan beide kanten gelijk zijn. |
| `!=` | Geeft ongelijkheid aan. Houdt waar wanneer de operands aan beide kanten niet gelijk zijn. |
| `<` | Geeft aan dat de variabele aan de linkerkant kleiner is dan de variabele aan de rechterkant. Evalueert naar false als de variabelen gelijk zijn. |
| `>` | Geeft aan dat de variabele aan de linkerkant groter is dan de variabele aan de rechterkant. Evalueert naar false als de variabelen gelijk zijn. |
| `<=` | Hetzelfde als `<` , behalve als de variabelen gelijk zijn, wordt de waarde true weergegeven. |
| `>=` | Hetzelfde als `>` , behalve als de variabelen gelijk zijn, wordt de waarde true weergegeven. |
| `&&` | Logisch &quot;ENs&quot;de uitdrukkingen aan de linkerzijde en het recht van het - is slechts waar wanneer beide kanten waar (vals anders) zijn. |
| `\|\|` | Logisch &quot;ORs&quot;de uitdrukkingen aan de linkerzijde en het recht van het - is slechts waar als één van de kanten (vals anders) waar is. |
| `//` | Controleert of de bron alle elementen van doel boolean bevat (Array-bron, Array-doel).<br>`//` extraheert de subtekenreeks van het doel (overeenkomend met regexp) en decodeert deze `Array/*String*/ decode(String encoding, String regexp, String target)` .<br> de eigenschap steunt ook het gebruik van constante koordwaarden, groeperend (`condition1 \|\| condition2) && condition3`), en regelmatige uitdrukkingen (`/[^a-z]$/.test(landing.referring.url)`). |

## De video van de opleiding: De Manuscripten van het profiel ![ badge van het Leerprogramma ](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik en het maken van profielscripts.

* Uitleggen wat een profielscript is
* Uitleggen hoe een profielscript verschilt van een profielparameter
* Een eenvoudig profielscript maken
* Via het menu Beschikbaar token hebt u toegang tot beschikbare opties
* Profielscripts in- en uitschakelen

>[!VIDEO](https://video.tv.adobe.com/v/17394)
