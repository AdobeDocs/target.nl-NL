---
keywords: Profielscript;profielscriptkenmerken;profielscript, aanbevolen methoden;foutopsporing;scripts;profielscripts;kenmerken;kenmerk;parameter
description: Meer informatie over bezoekersspecifieke kenmerken die zijn opgeslagen in het profiel van de bezoeker voor informatie over de kenmerken die kunnen worden gebruikt in uw Adobe [!DNL Target] activiteiten.
title: Wat zijn profielkenmerken?
feature: Audiences
exl-id: 6c689629-bbd3-461e-9a68-5b16d4eb4250
source-git-commit: 341b57a91dac8f948e9d7767999411118c0e0562
workflow-type: tm+mt
source-wordcount: '2430'
ht-degree: 0%

---

# Profielkenmerken

Profielkenmerken in [!DNL Adobe Target] zijn parameters die specifiek zijn voor een bezoeker. Deze kenmerken worden opgeslagen in het profiel van de bezoeker om informatie over de bezoeker te verstrekken die in uw activiteiten kan worden gebruikt.

Een gebruikersprofiel bevat demografische en gedragsinformatie van een bezoeker van een webpagina. Deze informatie kan leeftijd, geslacht, aangekochte producten, laatste tijd van bezoek omvatten, etc. dat [!DNL Target] gebruikt om de inhoud aan de bezoeker aan te passen.

Wanneer een bezoeker door uw website bladert of wanneer de bezoeker voor een andere sessie terugkeert, kunnen de opgeslagen profielkenmerken in het profiel worden gebruikt om inhoud of logboekinformatie voor segmentfiltering als doel in te stellen.

Profielkenmerken instellen:

1. Klik op **[!UICONTROL Audiences]** > **[!UICONTROL Profile Scripts.]**

   ![Profielscripts, tabblad](/help/main/c-target/c-visitor-profile/assets/create-script.png)

1. Klik op **[!UICONTROL Create Script]**.

   ![Profielscript maken, dialoogvenster](/help/main/c-target/c-visitor-profile/assets/profile-script.png)

   De volgende typen profielkenmerken zijn beschikbaar:

   | Type parameter | Beschrijving |
   |--- |--- |
   | mbox | Direct door paginacode doorgegeven tijdens het maken van het mbox. Zie [Parameters doorgeven aan een globale box](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html){target=_blank}.<br>**Opmerking**: [!DNL Target] heeft een limiet van 50 unieke profielkenmerken per mbox-aanroep. Als u meer dan 50 profielkenmerken moet doorgeven aan [!DNL Target], geeft u deze door met de API-methode voor het bijwerken van profielen. Zie voor meer informatie [Profielupdate in het dialoogvenster [!DNL Adobe Target] API-documentatie](https://developers.adobetarget.com/api/#updating-profiles). |
   | Profiel | Direct gedefinieerd met een JavaScript-codefragment. Deze fragmenten kunnen lopende totalen opslaan zoals het totale geld dat de consument besteedt en worden uitgevoerd op elke mbox-aanvraag. Zie Profielscriptkenmerken hieronder. |

## Profielscriptkenmerken {#concept_8C07AEAB0A144FECA8B4FEB091AED4D2}

Definieer een profielscriptkenmerk met het bijbehorende JavaScript-codefragment.

U kunt profielscripts gebruiken om bezoekerskenmerken voor meerdere bezoeken vast te leggen. Profielscripts zijn codefragmenten die binnen [!DNL Target] met behulp van een vorm van JavaScript op de server. U kunt bijvoorbeeld een profielscript gebruiken om vast te leggen hoe vaak een bezoeker uw site bezoekt en wanneer die bezoeker het laatst is bezocht.

Profielscripts zijn niet hetzelfde als profielparameters. Profielparameters leggen informatie over bezoekers vast met behulp van de mbox-code-implementatie [!DNL Target].

## Profielscripts maken {#section_CB02F8B97CAF407DA84F7591A7504810}

Profielscripts zijn beschikbaar onder [!UICONTROL Audiences] in de [!DNL Target] interface.

Als u een profielscript wilt toevoegen, klikt u op de knop **[!UICONTROL Profile Scripts]** tab, **[!UICONTROL Create Script]**, dan schrijf uw manuscript.

of

Als u een bestaand profielscript wilt kopiëren, kiest u [!UICONTROL Profile Scripts] lijst, klikt u op het ellipspictogram voor het gewenste script en klikt u vervolgens op **[!UICONTROL Duplicate]**.

Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

Profielscripts voeren profielkenmerk &#39;catchers&#39; uit op elke locatieaanvraag. Wanneer een locatieverzoek wordt ontvangen, [!DNL Target] bepaalt welke activiteit moet worden uitgevoerd en geeft inhoud weer die geschikt is voor die activiteit en die ervaring. [!DNL Target] volgt ook het succes van de activiteit en stelt om het even welke relevante profielmanuscripten in werking. Met dit proces kunt u informatie bijhouden over het bezoek, zoals de locatie, het tijdstip van de bezoeker, het aantal keren dat de bezoeker naar de site is geweest, als hij of zij eerder heeft gekocht, enzovoort. Deze informatie wordt vervolgens toegevoegd aan het profiel van de bezoeker, zodat u de activiteiten van die bezoeker op uw site beter kunt bijhouden.

Profielscriptkenmerken hebben de `user.` tag ingevoegd vóór de kenmerknaam. Bijvoorbeeld:

```
if (mbox.name == 'Track_Interest') { 
    if (profile.get('model') == "A5" &&; profile.get('subcat') == "KS6") { 
        return (user.get('A5KS6') || 0) + 1; 
    } 
}
```

Houd rekening met het volgende:

* Raadpleeg scriptkenmerken voor profielen (ook zichzelf) in de code met `user.get('parameterName')`.
* Variabelen opslaan die de volgende keer kunnen worden geopend dat het script wordt uitgevoerd (op de volgende mbox-aanvraag) met `user.setLocal('variable_name', 'value')`. Verwijs met de variabele `user.getLocal('variable_name')`. Dit proces is handig voor situaties waarin u naar de datum en het tijdstip van het laatste verzoek wilt verwijzen.

   Deze waarden blijven bestaan als een profielscript, maar u hebt er alleen toegang tot binnen het script dat ze zijn ingesteld.

* Parameters en waarden zijn hoofdlettergevoelig. Komt overeen met het geval van de parameters en waarden die u ontvangt tijdens de activiteit of test.
* Zie de sectie &quot;JavaScript reference for script profile parameters&quot; hieronder voor meer JavaScript-syntaxis.
* De parameter blijft in het profiel nadat het script is uitgeschakeld. Gebruikers waarvan de profielen al een parameter bevatten die in het publiek van een activiteit wordt gebruikt, kwalificeren in die activiteit.
* Profielscripts kunnen niet worden verwijderd terwijl ze in een activiteit worden gebruikt.
* Het wordt niet aanbevolen afhankelijke profielscripts te maken die het resultaat van een profielscript in een ander profielscript gebruiken. De volgorde waarin profielscripts worden uitgevoerd, is niet gegarandeerd.

## Informatiekaarten voor profielscripts weergeven {#section_18EA3B919A8E49BBB09AA9215E1E3F17}

U kunt pop-upkaarten met profielscriptinformatie weergeven, vergelijkbaar met informatiekaarten. Met deze informatiekaarten voor profielscripts kunt u een lijst weergeven met activiteiten die verwijzen naar het geselecteerde profielscript, samen met andere nuttige metagegevens.

U kunt bijvoorbeeld de volgende profielscriptinformatiekaart openen door op de knop [!UICONTROL Info] pictogram voor het gewenste profielscript in de lijst ([!UICONTROL Audiences] > [!UICONTROL Profile Scripts]).

De [!UICONTROL Script Info] bevat de volgende informatie: Naam, Beschrijving en scriptcode.

![Profielscript-infokaart](assets/profile_script_info_card.png)

Klikken **[!UICONTROL View full details]** om het publiek en de activiteiten te zien die van het geselecteerde profielmanuscript van verwijzingen voorzien.

![Profile Script info card > Script Usage, tabblad](assets/profile_script_info_card_usage_tab.png)

>[!NOTE]
>
>De [!UICONTROL Script Usage] worden in de volgende situaties geen activiteiten weergegeven die verwijzen naar het geselecteerde profielscript:
>
> * De activiteit bevindt zich in de [!UICONTROL Draft] status.
> * De inhoud of de aanbieding die in de activiteit wordt gebruikt gebruikt manuscriptvariabelen (of een gealigneerde aanbieding binnen de activiteit of een aanbieding binnen de bibliotheek van de Aanbieding).


## Doel schakelt profielscripts in bepaalde situaties uit {#section_C0FCB702E60D4576AD1174D39FBBE1A7}

[!DNL Target] Hiermee worden profielscripts in bepaalde situaties automatisch uitgeschakeld, bijvoorbeeld wanneer de uitvoering te lang duurt of wanneer er te veel instructies zijn.

Wanneer een profielscript is uitgeschakeld, wordt een geel waarschuwingspictogram weergegeven naast het profielscript in de doelinterface, zoals hieronder wordt geïllustreerd:

![profile_script_invalid image](assets/profile_script_invalid.png)

Bij aanwijzen worden details op de foutweergave weergegeven, zoals hieronder wordt geïllustreerd:

![profile_script_hover, afbeelding](assets/profile_script_hover.png)

De meest gangbare redenen voor het uitschakelen van profielscripts zijn:

* Een niet-gedefinieerde variabele waarnaar wordt verwezen.
* Er wordt verwezen naar een ongeldige waarde. Deze fout wordt vaak veroorzaakt door naar URL-waarden en andere door de gebruiker ingevoerde gegevens te verwijzen zonder juiste validatie.
* Er worden te veel JavaScript-instructies gebruikt. [!DNL Target] heeft een limiet van 2.000 JavaScript-instructies per script, maar deze limiet kan niet eenvoudig worden berekend door het JavaScript handmatig te lezen. Rhino behandelt bijvoorbeeld alle functieaanroepen en &quot;nieuwe&quot; aanroepen als 100 instructies. Om het even welke vraag aan om het even welke functie verbruikt 100 instructies. Ook, kan de grootte van om het even welke ingangsgegevens, zoals waarden URL, de instructietelling beïnvloeden.
* Niet volgende items die zijn gemarkeerd in het dialoogvenster [best practices](/help/main/c-target/c-visitor-profile/profile-parameters.md#section_64AFE5D2B0C8408A912FC2A832B3AAE0) hieronder.

## Aanbevolen procedures {#best}

De volgende richtlijnen zijn bedoeld om vereenvoudigde profielmanuscripten te schrijven die fout-falend-vrij zo mogelijk zijn door code te schrijven die zachtjes zakt zodat worden de manuscripten verwerkt zonder een systeem-manuscript-halt te dwingen. Deze richtsnoeren zijn het resultaat van goede praktijken die efficiënt zijn gebleken te werken. Deze richtsnoeren moeten worden toegepast in samenhang met de beginselen en aanbevelingen van de Rijnse ontwikkelingsgemeenschap.

* Stel de huidige scriptwaarde in op een lokale variabele in het gebruikersscript en stel een failover in op een lege tekenreeks.
* Valideer de lokale variabele door ervoor te zorgen dat deze geen lege tekenreeks is.
* Gebruik op tekenreeks gebaseerde manipulatiefuncties vs. Reguliere expressies.
* Gebruik limited for loops vs. open ended for or while loops.
* Gebruik niet meer dan 1.300 tekens of 50 lusherhalingen.
* Gebruik niet meer dan 2.000 JavaScript-instructies. [!DNL Target] heeft een limiet van 2.000 JavaScript-instructies per script, maar deze limiet kan niet eenvoudig worden berekend door het JavaScript handmatig te lezen. Rhino behandelt bijvoorbeeld alle functieaanroepen en &quot;nieuwe&quot; aanroepen als 100 instructies. Ook, kan de grootte van om het even welke ingangsgegevens, zoals waarden URL, de instructietelling beïnvloeden.
* Houd niet alleen rekening met de scriptprestaties, maar ook met de gecombineerde prestaties van alle scripts. Als beste praktijken, [!DNL Adobe] beveelt in totaal minder dan 5.000 instructies aan. Het tellen van het aantal instructies is niet voor de hand liggend, maar het belangrijkste is dat scripts die hoger zijn dan 2000 instructies automatisch worden uitgeschakeld. Het aantal actieve profielscripts mag niet groter zijn dan 300. Elk manuscript wordt uitgevoerd met elke enige brievenbusvraag. Voer zo veel scripts uit als u nodig hebt.
* In een regex met een puntster in het begin (bijvoorbeeld: `/.*match/`, `/a|.*b/`) is bijna nooit nodig. De regex-zoekopdracht begint op alle posities in een tekenreeks (tenzij gebonden aan `^`), dus er wordt al een puntster aangenomen. De uitvoering van het script kan worden onderbroken als een dergelijke regex overeenkomt met een lang genoeg aantal invoergegevens (die wel honderden tekens kunnen bevatten).
* Als alles ontbreekt, verpak manuscript in probeer/vangst.
* De volgende aanbevelingen kunnen u helpen de ingewikkeldheid van het profielmanuscript beperken. Profielscripts kunnen een beperkt aantal instructies uitvoeren.

   Als beste praktijken:

   * Houd profielscripts klein en zo eenvoudig mogelijk.
   * Vermijd reguliere expressies of gebruik alleen eenvoudige reguliere expressies. Zelfs eenvoudige expressies kunnen veel instructies gebruiken om te evalueren.
   * Vermijd herhaling.
   * Profielscripts moeten op prestaties worden getest voordat ze worden toegevoegd aan [!DNL Target]. Alle profielscripts worden uitgevoerd op elke mbox-aanvraag. Als profielscripts niet correct worden uitgevoerd, duurt het langer om mbox-aanvragen uit te voeren, wat invloed kan hebben op verkeer en conversie.
   * Als profielscripts te complex worden, kunt u het volgende gebruiken [reactietokens](/help/main/administrating-target/response-tokens.md) in plaats daarvan.

* Zie de documentatie van de JS Rhino-engine voor meer informatie.

## Fouten opsporen in profielscripts {#section_E9F933DE47EC4B4E9AF2463B181CE2DA}

De volgende methoden kunnen worden gebruikt om fouten op te sporen in profielscripts:

>[!NOTE]
>
>Gebruiken [!DNL console.log] in een profielscript wordt de profielwaarde niet uitgevoerd, omdat profielscripts op de server worden uitgevoerd.

* **Profielscripts toevoegen als reactietokens voor foutopsporing in profielscripts:**

   In [!DNL Target], klikt u op **[!UICONTROL Administration]**, klikt u op **[!UICONTROL Response Tokens]** Schakel vervolgens het profielscript in dat u wilt debuggen.

   Telkens wanneer u een pagina voor uw site laadt met [!DNL Target] een deel van het antwoord van [!DNL Target] bevat uw waarde voor het opgegeven profielscript, zoals hieronder wordt getoond:

   ![debug_profile_script_1 afbeelding](assets/debug_profile_script_1.png)

* **Gebruik het foutopsporingsprogramma mboxTrace om fouten in profielscripts op te sporen.**

   Deze methode vereist een toestemmingstoken dat u kunt produceren door te klikken **[!UICONTROL Target]** > **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Generate Authorization Token]** in de [!UICONTROL Debugger tools] sectie.

   Vervolgens voegt u deze twee parameters toe aan de URL van de pagina na &quot;?&quot;: `mboxTrace=window&authorization=YOURTOKEN`.

   Het toevoegen van deze parameters is een weinig informatiefunctie dan het reactietoken omdat u een voor-uitgevoerde momentopname en een na-momentopname van uw profiel krijgt. Ook worden alle beschikbare profielen weergegeven.

   ![afbeelding debug_profile_script_2](assets/debug_profile_script_2.png)

## Veelgestelde vragen over profielscript {#section_1389497BB6D84FC38958AE43AAA6E712}

**Is het mogelijk om profielmanuscripten te gebruiken om informatie van een pagina te vangen die in een gegevenslaag verblijft?**

Profielscripts kunnen de pagina niet rechtstreeks lezen omdat ze aan de serverzijde worden uitgevoerd. De gegevens moeten binnen door een mbox verzoek of door andere worden overgegaan [methoden om gegevens in het doel op te halen](https://experienceleague.corp.adobe.com/docs/target-dev/developer/implementation/methods/methods-to-get-data-into-target.html){target=_blank}. Nadat de gegevens zijn ingevoerd [!DNL Target]profielscripts kunnen de gegevens lezen als een parameter mbox of profielparameter.

## JavaScript-referentie voor scriptprofielparameters

De eenvoudige kennis JavaScript wordt vereist om manuscriptprofielparameters effectief te gebruiken. Deze sectie dient als een snelle referentie om u binnen een paar minuten productief te maken met deze functionaliteit.

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

Hiermee maakt u een variabele voor de dag, gemeten in milliseconden. Als de naam van het selectievakje `orderThankyouPage`, stelt u een lokaal (onzichtbaar) gebruikersprofielkenmerk genaamd `lastPurchaseTime` om de waarde van de huidige datum en tijd weer te geven. De waarde van de laatste aankooptijd wordt gelezen en, indien gedefinieerd, [!DNL Target] retourneert de tijd die is verstreken sinds de laatste aankooptijd, gedeeld door het aantal milliseconden in een dag (wat resulteert in het aantal dagen sinds de laatste aankoop).

**Naam:** *user.frequency*

```
var frequency = user.get('frequency') || 0;
if (mbox.name == 'orderThankyouPage') {
    return frequency + 1;
}
```

Maakt een variabele met de naam `frequency`, initialiseert u de vorige waarde of 0 als er geen vorige waarde was. Als de naam van het selectievakje `orderThankyouPage`, wordt de verhoogde waarde geretourneerd.

**Naam:** *user.monetaryValue*

```
var monetaryValue = user.get('monetaryValue') || 0;
if (mbox.name == 'orderThankyouPage') {
    return monetaryValue + parseInt(mbox.param('orderTotal'));
}
```

Maakt een variabele met de naam `monetaryValue`, waarbij de huidige waarde voor een bepaalde bezoeker wordt opgezocht (of op 0 wordt ingesteld als er geen vorige waarde was). Als de naam van het selectievakje `orderThankyouPage`, wordt nieuwe monetaire waarde geretourneerd door de vorige waarde en de waarde van de `orderTotal` parameter die aan mbox wordt overgegaan.

**Naam:** adobeQA

```
if (page.param("adobeQA"))
     return page.param("adobeQA");
else if (page.param("adobeqa"))
     return page.param("adobeqa");
else if (mbox.param("adobeQA"))
     return mbox.param("adobeQA");
```

Maakt een variabele met de naam `adobeQA` om een gebruiker bij te houden voor [Activiteit QA](/help/main/c-activities/c-activity-qa/activity-qa.md).

### Objecten en methoden {#objects}

Naar de volgende objecten en methoden kan worden verwezen door scriptprofielparameters:

| Object of methode | Details |
| --- | --- |
| `page.url` | De huidige URL. |
| `page.protocol` | Het protocol dat wordt gebruikt voor de pagina (http of https). |
| `page.domain` | Het huidige URL-domein (alles vóór de eerste schuine streep). Bijvoorbeeld: `www.acme.com` in `http://www.acme.com/categories/men_jeans?color=blue&size=small`. |
| `page.query` | De queryreeks voor de huidige pagina. Alles na de &#39;?&#39;. Bijvoorbeeld: `blue&size=small` in `http://www.acme.com/categories/mens_jeans?color=blue&size=small`. |
| `page.param('<par_name>')` | De waarde van de parameter die wordt aangegeven door `<par_name>`. Als je huidige URL een zoekpagina voor Google is en je hebt opgegeven `page.param('hl')`, krijgt u &quot;en&quot; voor de URL `http://www.google.com/search?hl=en& q=what+is+asdf&btnG=Google+Search`. |
| `page.referrer` | Dezelfde operaties als hierboven gelden voor referentie en landing (d.w.z. referentie.url is het URL-adres van de referentie). |
| `landing.url`, `landing.protocol`, `landing.query`, en `landing.param` | Gelijkaardig aan dat van pagina, maar voor de landingspagina.<P>Als u de URL van de bestemmingspagina wilt laten werken zoals u had verwacht, stelt u de optie `context` > `browser` > `host`. |
| `mbox.name` | De naam van de actieve box. |
| `mbox.param('<par_name>')` | Een mbox-parameter op basis van de opgegeven naam in het actieve mbox. |
| `profile.get('<par_name>')` | De door de client gemaakte parameter voor gebruikersprofielen krijgt de naam `<par_name>`. Als de gebruiker bijvoorbeeld een profielparameter met de naam &quot;gender&quot; instelt, kan de waarde worden geëxtraheerd met &quot;profile.gender&quot;. Hiermee wordt de waarde van de waarde &quot;`profile.<par_name>`&quot; vastgesteld voor de huidige bezoeker; retourneert null als er geen waarde is ingesteld. Let op: `profile.get(<par_name>)` wordt gekwalificeerd als een functieaanroep. |
| `user.get('<par_name>')` | Hiermee wordt de waarde van de waarde &quot;`user.<par_name>`&quot; vastgesteld voor de huidige bezoeker; retourneert null als er geen waarde is ingesteld. |
| `user.categoryAffinity` | Retourneert de naam van de beste categorie. |
| `user.categoryAffinities` | Retourneert een array met de beste categorieën. |
| `user.isFirstSession` | Retourneert true als het de eerste sessie van de bezoeker is. |
| `user.browser` | Retourneert de user-agent in de HTTP-header. Als voorbeeld kunt u een expressiedoel maken om alleen Safari-gebruikers als doel in te stellen: `if (user.browser != null && user.browser.indexOf('Safari') != -1) { return true; }` |

### Algemene operatoren

Alle standaard JavaScript-operatoren zijn aanwezig en kunnen worden gebruikt. JavaScript-operatoren kunnen worden gebruikt voor tekenreeksen en getallen (en andere gegevenstypen). Een korte briefing:

| Operator | Beschrijving |
| --- | --- |
| `==` | Geeft gelijkheid aan. Houdt waar wanneer de operands aan beide kanten gelijk zijn. |
| `!=` | Geeft ongelijkheid aan. Houdt waar wanneer de operands aan beide kanten niet gelijk zijn. |
| `<` | Geeft aan dat de variabele aan de linkerkant kleiner is dan de variabele aan de rechterkant. Evalueert naar false als de variabelen gelijk zijn. |
| `>` | Geeft aan dat de variabele aan de linkerkant groter is dan de variabele aan de rechterkant. Evalueert naar false als de variabelen gelijk zijn. |
| `<=` | Gelijk aan `<` behalve als de variabelen gelijk zijn , wordt het geëvalueerd naar true . |
| `>=` | Gelijk aan `>` behalve als de variabelen gelijk zijn , wordt het geëvalueerd naar true . |
| `&&` | Logisch &quot;ENs&quot;de uitdrukkingen aan de linkerzijde en het recht van het - is slechts waar wanneer beide kanten waar (vals anders) zijn. |
| `||` | Logisch &quot;ORs&quot;de uitdrukkingen aan de linkerzijde en het recht van het - is slechts waar als één van de kanten (vals anders) waar is. |
| `//` | Controleert of de bron alle elementen van doel boolean bevat (Array-bron, Array-doel).<br>`//` extraheert substring uit target (overeenkomend met regexp) en decodeert deze `Array/*String*/ decode(String encoding, String regexp, String target)`.<br>De functie ondersteunt ook het gebruik van constante tekenreekswaarden, groeperen (`condition1 || condition2) && condition3`, en reguliere expressies (`/[^a-z]$/.test(landing.referring.url)`. |

## Trainingsvideo: Profielscripts ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik en het maken van profielscripts.

* Uitleggen wat een profielscript is
* Uitleggen hoe een profielscript verschilt van een profielparameter
* Een eenvoudig profielscript maken
* Via het menu Beschikbaar token hebt u toegang tot beschikbare opties
* Profielscripts in- en uitschakelen

>[!VIDEO](https://video.tv.adobe.com/v/17394)
