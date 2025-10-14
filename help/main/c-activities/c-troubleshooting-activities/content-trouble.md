---
keywords: debug mbox;troubleshoot mbox;mbox issues;flicker;mboxDebug;mboxTrace;token;debugger;priority;activity priority;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst purchase mbox;top-selling;top-verkoper
description: Zoek naar suggesties om problemen op te lossen als de pagina de verwachte inhoud niet weergeeft. Leer hoe u fouten kunt opsporen in de levering van inhoud in Adobe Target.
title: Hoe kan ik problemen met de levering van inhoud oplossen?
feature: Activities
exl-id: 887b7956-1d61-439a-8339-c150deb9a378
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Problemen met de levering van inhoud oplossen

Als op de pagina de verwachte inhoud niet wordt weergegeven, zijn er een paar stappen die u kunt uitvoeren om de levering van inhoud op fouten te controleren.

* Controleer uw activiteit of campagnecode zorgvuldig. Een typefout of andere fout kan ertoe leiden dat de verwachte inhoud niet wordt weergegeven.
* Gebruik mboxTrace of mboxDebug om de [!DNL Target] aanvraag problemen op te lossen.
* Gebruik Foutopsporing van Adobe Experience Cloud, een makkelijk te gebruiken hulpmiddel dat veel van de zelfde informatie zoals mboxDebug verstrekt, om het [!DNL Target] verzoek problemen op te lossen.

mboxDebug is vooral handig wanneer u [!DNL Target] op de pagina instelt om er zeker van te zijn dat de aanvraag Doel wordt geactiveerd en het cookie wordt ingesteld. Nochtans, gaat het niet in het soort detail dat wanneer het zuiveren van inhoudslevering nuttig is. Als uw activiteit niet op uw pagina verschijnt of ongewenste inhoud verschijnt, gebruik mboxTrace om de pagina in detail te onderzoeken en te zuiveren.

## Haal het toestemmingstoken terug om met het zuiveren hulpmiddelen te gebruiken {#section_BED130298E794D1FA229DB7C3358BA54}

Omdat mboxTrace en mboxDebug campagnegegevens en profielgegevens aan externe partijen kunnen blootstellen, wordt een toestemmingstoken vereist. Het machtigingstoken kan in [!DNL Target] UI worden teruggewonnen. De token is zes uur geldig.

U moet een van de volgende gebruikersmachtigingen hebben om een verificatietoken te genereren:

* Minstens [!UICONTROL Editor] machtiging (of [!UICONTROL Approver])

  Voor meer informatie voor [!DNL Target Standard] klanten, zie [&#x200B; rollen en Toestemmingen &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers* specificeren. Voor meer informatie voor [!DNL Target Premium] klanten, zie [&#x200B; ondernemingstoestemmingen &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) vormen.

* Beheerdersrol op het niveau van de werkruimte/het productprofiel

  De werkruimten zijn alleen beschikbaar voor [!DNL Target Premium] klanten. Voor meer informatie, zie [&#x200B; ondernemingstoestemmingen &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md) vormen.

* Beheerdersrechten (machtiging Sysadmin) op productniveau van [!DNL Adobe Target]

Om het toestemmingstoken terug te winnen:

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** .
1. Klik in de sectie Foutopsporingsgereedschappen op **[!UICONTROL Generate New Authentication Token]** .

   ![&#x200B; produceer Nieuwe Token van de Authentificatie &#x200B;](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

1. Voeg het gegenereerde token als parameter toe aan uw URL om een van de geavanceerde foutopsporingsprogramma&#39;s in te schakelen.

   ![&#x200B; teken van de Token van de Toestemming &#x200B;](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace stelt u in staat traceerinformatie te ontvangen die is gekoppeld aan [!DNL Target] reacties. Traceergegevens weerspiegelen het resultaat van een [!DNL Target] -aanroep (bijvoorbeeld een conversie of een indruk) en eventuele aanvullende gegevens die kunnen helpen bepalen waarom dit specifieke resultaat is opgetreden, zoals een set beschikbare vertakkingen waaronder de selectie is gemaakt in een campagne. Gebruik deze informatie om de levering van inhoud te zuiveren.

De volgende parameters zijn beschikbaar:

| mboxTrace-opties | Resultaat |
|--- |--- |
| `?mboxTrace=console` | Hiermee wordt het logboek als objecten afgedrukt in het logbestand van de console.<br> voor at.js, in plaats van het popping een nieuw browser venster of output aan de console zoals in mbox.js (nu afgekeurd) was, moet u het verzoek van het Netwerk inspecteren en onder Voorproef (Chrome) of Reactie (Firefox) kijken. |
| `?mboxTrace=json` | Drukt in consolelogboek als letterlijke JSON-tekenreeks af |
| `?mboxTrace=window` | Drukt in een pop-upvenster af als een JSON-tekenreeks |
| `?mboxTrace=disable` | Hiermee schakelt u de overtreksessiemodus uit |

**de vraag mboxTrace van het Voorbeeld**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

In de uitvoer wordt gedetailleerde informatie over de inhoud weergegeven. mboxTrace geeft details over uw campagne of activiteit en profiel. Het biedt ook een momentopname van het profiel vóór de uitvoering en een momentopname van wat na de uitvoering is gewijzigd. Het toont ook welke campagnes of activiteiten voor elke plaats werden geëvalueerd.

Sommige informatie omvat overeenkomende en niet-overeenkomende segment- en doel-id&#39;s:

* **SegmentId**: IDs van segmenten, of van de herbruikbare segmentbibliotheek of anonieme die voor de bijzondere campagne worden gecreeerd.
* **TargetId**: IDs van doelstellingen, of van de bibliotheek van de doeluitdrukking of anonieme doelstellingen voor om het even welke segmenten van campagne.
* **Niet overtroffen**: Het verzoek kwalificeerde niet in deze vraag voor die segmenten of doelstellingen.
* **Gelijke**: Het verzoek kwalificeerde voor de gespecificeerde segmenten of de doelstellingen.

**Gebruikend mboxTrace op aanbevelingen pagina&#39;s**: Het toevoegen van mboxTrace als vraagparameter op pagina&#39;s met aanbevelingen vervangt het ontwerp van Aanbevelingen op de pagina met een mboxTrace detailsvenster, dat diepgaande informatie over uw aanbevelingen, die omvat:

* Geretourneerde aanbevelingen versus gevraagde aanbevelingen
* De gebruikte sleutel en of het aanbevelingen produceert
* Door criteria gegenereerde aanbevelingen versus aanbevelingen voor back-ups
* Criteria configureren
* Uitgesloten en toegepaste insluitingen
* Verzamelingsregels

U hoeft `=console` , `=json` of `=window` niet op te nemen in de queryparameter. Wanneer u klaar bent met de details mboxTrace, voegt u `=disable` toe en drukt u op **[!UICONTROL Enter]** om terug te keren naar de normale weergavemodus.

Het normale functioneren en de vormgeving van uw site worden niet beïnvloed door mboxTrace. Bezoekers zien het ontwerp van uw gebruikelijke aanbevelingen.

## mboxDebug {#mboxdebug}

Als u mboxDebug wilt gebruiken, voegt u een parameter mboxDebug toe aan het einde van de URL. De volgende tabel bevat informatie over [!DNL Target] aan reacties gerelateerde URL-parameters.

>[!NOTE]
>
>Sommige parameters mboxDebug zijn beschikbaar met of zonder authentificatie.

| URL-parameters | Doel |
|--- |--- |
| `mboxDebug=1` | Debugger <br> die deze parameter aan om het even welke URL met bepaalde verzoeken van het Doel toevoegt opent een pop-up venster met waardevolle het zuiveren details. De informatie van het cookie, de waarden van PCid en van identiteitskaart van de Zitting worden weggeschreven, en alle URLs zijn zichtbaar. Klik op een aanvraag-URL van het doel om het antwoord voor die [!DNL Target] -aanvraag weer te geven. Meer details zijn beschikbaar in [&#x200B; mbox_debug.pdf &#x200B;](/help/main/assets/mbox_debug.pdf). |
| `mboxDisable=1` | Vakken op de pagina uitschakelen |
| `mboxOverride.browserIp=<Insert IP address>` | Het in werking stellen van de test <br> het in werking stellen van de Test die met deze parameter URL werkt. Typ een IP adres als waarde voor dit attribuut, en het groeperen van Test&amp;Target evalueert dat IP adres tegen om het even welke geotargeting of segmentatie die in een campagne wordt geplaatst. |

>[!NOTE]
>
>Controleer of het URL-fragment zich na parameters van queryreeksen bevindt. Alles na de eerste `#` is een fragment-id en zorgt ervoor dat foutopsporingsparameters niet correct werken.

## Adobe Experience Cloud Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

Met de Adobe Experience Cloud Debugger kunt u snel en gemakkelijk uw doelimplementatie begrijpen. U kunt uw bibliotheekconfiguratie snel bekijken, verzoeken onderzoeken om ervoor te zorgen uw douaneparameters correct worden overgegaan, console het registreren inschakelen, en alle verzoeken van het Doel onbruikbaar maken. Verifieer in de Experience Cloud en u kunt het krachtige hulpmiddel MboxTrace gebruiken om uw activiteit en publiekskwalificaties evenals uw bezoekersprofiel te inspecteren.

Zie de volgende trainingsvideo&#39;s voor meer informatie:

Voor meer gedetailleerde informatie, zie [&#x200B; zuiveren at.js gebruikend debugger van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/target-debugging-atjs.html?lang=nl-NL){target=_blank}.

## Topverkopers worden niet weergegeven in Aanbevelingen {#section_3920C857270A406C80BE6CBAC8221ECD}

De aanroep van *`SiteCatalyst: purchase`* kan niet worden gebruikt voor verkeersgegevens van het inkoopalgoritme. Gebruik in plaats hiervan de aanroep *`orderConfirmPage`* .

## Prioriteit activiteit controleren {#section_3D0DD07240F0465BAF655D0804100AED}

Activiteiten die op formulieren zijn gebaseerd en met [!DNL Target Standard/Premium] zijn gemaakt, kunnen botsen met activiteiten die zijn gemaakt in de [!DNL Target Classic] -gebruikersinterface en die dezelfde prioriteit hebben en dezelfde [!DNL Target] -aanvraag gebruiken.

## De code van de douane veroorzaakt niet de verwachte resultaten in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Doel ondersteunt IE 8 niet meer.

## Doelcookie wordt niet ingesteld {#section_77AFEB541C0B495EB67E29A4475DF960}

Als uw site een subdomein heeft, zoals [!DNL us.domain.com] , maar u hebt de doelcookie ingesteld op [!DNL domain.com] (in plaats van [!DNL us.domain.com] ), moet u de instelling `cookieDomain` overschrijven. Voor meer informatie, zie [&#x200B; targetGlobalSettings () &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html?lang=nl-NL){target=_blank}.

## De doelinhoud flikkert of wordt niet weergegeven als een element ook deel uitmaakt van Adobe Experience Manager-personalisatie. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Als een DOM-element onderdeel is van Adobe Experience Manager (AEM) voor personalisatie en een doelactiviteit, kan de doelinhoud flikkeren of niet worden weergegeven.

U verhelpt deze situatie door AEM-personalisatie uit te schakelen op pagina&#39;s waarop Target wordt uitgevoerd.

## Omleiding en aanbiedingen op afstand kunnen niet worden geleverd vanwege een ongeldige URL. {#section_7D09043B687F43B39DAEDF17D00375AC}

Als de omleiding of de aanbieding op afstand een ongeldige URL gebruikt, kan het zijn dat deze niet wordt geleverd.

Voor omleidingsvoorstellen kan het [!DNL Target] -antwoord `/* invalid redirect offer URL */` bevatten

of

Voor externe aanbiedingen kan de reactie [!DNL Target] `/* invalid remote offer URL */` bevatten

U kunt de [!DNL Target] reactie controleren in browser of mboxTrace gebruiken. Zie [&#x200B; https://tools.ietf.org/html/std66 &#x200B;](https://tools.ietf.org/html/std66) voor meer informatie over geldige URLs.

## [!DNL Target] -aanvragen worden niet op mijn site geactiveerd.

at.js leidt geen verzoeken van het Doel in brand als u een ongeldig documenttype gebruikt. at.js vereist het HTML 5-documenttype.

## Zorg ervoor dat [!DNL Target] activiteiten URLs met vraagkoordparameters correct behandelen. {#query-strings}

[!UICONTROL Activity URL] bepaalt de pagina die bezoekers voor de activiteit kwalificeert en geeft de activiteitenervaringen aan gebruikers terug. Wanneer u hierom wordt gevraagd tijdens het maken van activiteiten, zorgt het typen van de volledige URL niet altijd ervoor dat de inhoud op die sitepagina wordt geleverd, vooral niet met URL&#39;s die querytekenreeksparameters bevatten.

Door gebrek, opent [!UICONTROL Visual Experience Composer] (VEC) de pagina die in uw [&#x200B; Visuele montages van Composer van de Ervaring wordt gespecificeerd &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md). U kunt ook een andere pagina opgeven tijdens het maken van activiteiten.

Als u een andere pagina wilt weergeven nadat de VEC is geopend, klikt u op **[!UICONTROL Configure gear icon]** > Selecteren **[!UICONTROL Page Delivery]** > en geeft u vervolgens de gewenste URL op in het veld [!UICONTROL Activity URL] .

![&#x200B; vorm de montages UI van de Levering van de Pagina &#x200B;](assets/configure-page-delivery.png)

Maar wat als URL vraagkoordparameters bevat? Werkt het en toont het gepersonaliseerde inhoud? In dit scenario, ongeacht uw doelpubliek, kunt u malplaatjeregels naast basis URL omvatten om uw vraagparameters te bepalen.

U kunt de volgende opties gebruiken om aanvullende sjabloonregels op te nemen:

### Optie 1: Herhaal de URL en zorg dat deze in de sjabloonregel blijft staan met de optie &quot;contains&quot;.

Deze optie zorgt ervoor dat deze URL in aanmerking komt voor de activiteit, maar houd er rekening mee dat er hoekgevallen aan zijn gekoppeld die uw rapportgegevens kunnen beïnvloeden met extra records aan URL&#39;s die de basis-URL bevatten.

In dit scenario is de URL `https://shopping.mycart.com?type=Summers%20Offers` en bevatten aanvullende sjabloonregels dezelfde URL, gescheiden door een OR-operator:

![&#x200B; Herhaal URL in malplaatjeregels &#x200B;](assets/option1.png)

### Optie 2: Beperk de voorwaarde &quot;bevat&quot; van de URL met alleen de queryreeks.

Het geval in hoeken dat in de vorige optie wordt besproken wordt toegepast in deze optie, maar hier is de voorwaardelijke opstelling beperkt tot het vraagkoord slechts.

In dit scenario is de URL `https://shopping.mycart.com?type=Summers%20Offers` en bevat de aanvullende sjabloonregels alleen de querytekenreeks, gescheiden door een OR-operator:

![&#x200B; de regel van het Malplaatje bevat slechts het vraagkoord &#x200B;](assets/option2.png)

### Optie 3: Gebruik in plaats van de volledige URL een specifiek gedeelte van de URL.

In dit scenario is de URL `https://shopping.mycart.com?type=Summers%20Offers` en geven de aanvullende sjabloonregels een [!UICONTROL Query] met [!UICONTROL type] > [!UICONTROL is (case sensitive)] > type=Summers%20Offers op, gescheiden door een OR-operator:

![&#x200B; regel die van het Malplaatje een specifiek deel van URL leveraging &#x200B;](assets/option3.png)

## Het verwijderen van dubbele aanhalingstekens in de kenmerkwaarde van het profiel [!DNL Target] werkt niet zoals verwacht. {#escape}

Wanneer u waarden verzendt die dubbele aanhalingstekens bevatten in een [!DNL Target] -profielkenmerk, moet u de waarde opnieuw opgeven zoals hieronder wordt weergegeven.

```
adobe.target.trackEvent({
    "mbox": "data-collection",
    "params":    {
        "profile.tagLine": "Escape \\\"Double Quotes\\\" like this."
    }
});
```

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Voeg de badge van de Uitbreiding ![&#x200B; Zelfstudie &#x200B;](/help/main/assets/tutorial.png) toe

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Basis Adobe Target het Zuiveren ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### De badge van het Spoor van het Mbox ![&#x200B; Zelfstudie &#x200B;](/help/main/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)
