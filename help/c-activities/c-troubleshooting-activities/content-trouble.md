---
keywords: debug mbox;troubleshoot mbox;mbox issues;flicker;mboxDebug;mboxTrace;token;debugger;priority;activity priority;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst  purchase mbox;top selling;top seller
description: Als op de pagina de verwachte inhoud niet wordt weergegeven, kunt u een aantal stappen uitvoeren om fouten op te sporen in de levering van inhoud in Adobe Target.
title: Problemen met de levering van inhoud in Adobe Target oplossen
subtopic: Multivariate Test
topic: Standard
uuid: 8837d07a-f793-495e-a6c1-b9c35fbe18b1
translation-type: tm+mt
source-git-commit: c7664f9674234565a3657f453541095811fa5aa6
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---


# Problemen met de levering van inhoud oplossen{#troubleshoot-content-delivery}

Als op de pagina de verwachte inhoud niet wordt weergegeven, zijn er een paar stappen die u kunt uitvoeren om de levering van inhoud te debuggen.

* Controleer uw activiteit of campagnecode zorgvuldig. Een typefout of andere fout kan ertoe leiden dat de verwachte inhoud niet wordt weergegeven.
* Gebruik mboxTrace of mboxDebug om het [!DNL Target] verzoek problemen op te lossen.
* Gebruik Adobe Experience Cloud Debugger, een gebruiksvriendelijk hulpprogramma dat veel van dezelfde informatie biedt als mboxDebug, om problemen met de [!DNL Target] aanvraag op te lossen.

mboxDebug is vooral handig wanneer u [!DNL Target] op de pagina instelt om te controleren of de [!DNL Target] aanvraag wordt geactiveerd en het cookie wordt ingesteld. Nochtans, gaat het niet in het soort detail dat wanneer het zuiveren van inhoudslevering nuttig is. Als uw activiteit niet op uw pagina verschijnt of ongewenste inhoud verschijnt, gebruik mboxTrace om de pagina in detail te onderzoeken en te zuiveren.

## De machtigingstoken ophalen voor gebruik met de foutopsporingsgereedschappen {#section_BED130298E794D1FA229DB7C3358BA54}

Omdat mboxTrace en mboxDebug campagnegegevens en profielgegevens aan externe partijen kunnen blootstellen, wordt een toestemmingstoken vereist. Het toestemmingstoken kan in [!DNL Target] UI worden teruggewonnen. De token is zes uur geldig.

Om het toestemmingstoken terug te winnen:

1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Implementation]**.
1. Selecteer **[!UICONTROL mbox.js]** of **[!UICONTROL at.js]**.
1. Klik op **[!UICONTROL Generate Authentication Token]**.

   ![Token voor autorisatie genereren](/help/c-activities/c-troubleshooting-activities/assets/generate-auth-token.png)

1. Voeg het gegenereerde token als parameter toe aan uw URL om een van de geavanceerde foutopsporingsprogramma&#39;s in te schakelen.

   ![Token voor autorisatie](/help/c-activities/c-troubleshooting-activities/assets/gen-auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace laat u toe om spoorinformatie te ontvangen in bijlage aan [!DNL Target] reacties. Traceerinformatie weerspiegelt het resultaat van een [!DNL Target] oproep (bijvoorbeeld een conversie of een indruk) en eventuele aanvullende gegevens die kunnen helpen bepalen waarom dit specifieke resultaat heeft plaatsgevonden, zoals een reeks beschikbare vertakkingen waaronder de selectie in een campagne heeft plaatsgevonden. Gebruik deze informatie om de levering van inhoud te zuiveren.

De volgende parameters zijn beschikbaar:

| mboxTrace-opties | Resultaat |
|--- |--- |
| `?mboxTrace=console` | Hiermee wordt het logboek als objecten afgedrukt in het logbestand van de console.<br>Voor at.js, in plaats van een nieuw browser venster of output aan de console zoals in mbox.js te poppen, zult u het verzoek van het Netwerk moeten inspecteren en onder Voorproef (Chrome) of Reactie (Firefox) kijken. |
| `?mboxTrace=json` | Drukt in consolelogboek als letterlijke JSON-tekenreeks af |
| `?mboxTrace=window` | Drukt in een pop-upvenster af als een JSON-tekenreeks |
| `?mboxTrace=disable` | Hiermee schakelt u de overtreksessiemodus uit |

**Voorbeeld mboxTrace-aanroep**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

In de uitvoer wordt zeer gedetailleerde informatie over de inhoud weergegeven. mboxTrace geeft details over uw campagne of activiteit en profiel. Het biedt ook een momentopname van het profiel vóór uitvoering en een momentopname van wat na uitvoering is gewijzigd. Het toont ook welke campagnes of activiteiten voor elke plaats werden geëvalueerd.

Sommige informatie omvat overeenkomende en niet-overeenkomende segment- en doel-id&#39;s:

* **SegmentId**: Identiteitskaart van segmenten, of van de herbruikbare segmentbibliotheek of anonieme die voor de bepaalde campagne worden gecreeerd.
* **TargetId**: Ids van doelstellingen, of van de bibliotheek van de doeluitdrukking of anonieme doelstellingen voor om het even welke segmenten van campagne.
* **Niet-overeenkomend**: Het verzoek kwam in deze oproep niet in aanmerking voor die segmenten of doelstellingen.
* **Overeenkomend**: Het verzoek wordt gekwalificeerd voor de gespecificeerde segmenten of de doelstellingen.

**MboxTrace gebruiken op pagina**&#39;s met aanbevelingen: Als u mboxTrace toevoegt als een queryparameter op pagina&#39;s met aanbevelingen, wordt het ontwerp met aanbevelingen op de pagina vervangen door een venster met mboxTrace-details, dat uitgebreide informatie over uw aanbevelingen weergeeft, zoals:

* Geretourneerde aanbevelingen versus gevraagde aanbevelingen
* De gebruikte sleutel en of het aanbevelingen produceert
* Door criteria gegenereerde aanbevelingen versus aanbevelingen voor back-ups
* Criteria configureren
* Uitgesloten en toegepaste insluitingen
* Verzamelingsregels

U te hoeven niet om, `=console`of `=json``=window` in de vraagparameter op te nemen. Wanneer u met de details mboxTrace wordt gedaan, voeg toe `=disable` en druk **[!UICONTROL Enter]** om op de normale vertoningswijze terug te komen.

Het normale functioneren en de vormgeving van uw site worden niet beïnvloed door mboxTrace. Bezoekers zien het ontwerp van uw gebruikelijke aanbevelingen.

## mboxDebug {#mboxdebug}

Als u mboxDebug wilt gebruiken, voegt u een parameter mboxDebug toe aan het einde van de URL. De volgende tabel bevat informatie over URL-parameters die betrekking hebben op [!DNL Target] reacties.

>[!NOTE]
>
>Sommige parameters mboxDebug zijn beschikbaar met of zonder authentificatie.

| URL-parameters | Doel |
|--- |--- |
| `mboxDebug=1` | <br>FoutopsporingAls u deze parameter toevoegt aan een URL waarvoor Target-verzoeken zijn gedefinieerd, wordt een pop-upvenster geopend met waardevolle foutopsporingsgegevens. De informatie van het cookie, de waarden van PCid en van identiteitskaart van de Zitting worden weggeschreven, en alle URLs zijn zichtbaar. Klik op een Target request-URL om het antwoord voor die [!DNL Target] aanvraag weer te geven. Meer details zijn beschikbaar in [mbox_debug.pdf](/help/assets/mbox_debug.pdf). |
| `mboxDebug=x-cookie` | Het cookie wijzigen |
| `mboxDisable=1` | Vakken op de pagina uitschakelen |
| `mboxDebug=x-profile` | Profielenset weergeven. |
| `mboxDebug=x-time` | Responstijd voor elk [!DNL Target] verzoek tonen |
| `mboxOverride.browserIp=<Insert IP address>` | Test<br>geotargetingTest-oriëntatie met deze URL-parameter. Typ een IP adres als waarde voor dit attribuut, en test&amp;Target het groeperen evalueert dat IP adres aan gelijke tegen om het even welke geotargeting of segmentatie die in een campagne wordt geplaatst. |

>[!NOTE]
>
>Controleer of het URL-fragment zich na parameters van queryreeksen bevindt. Alles na de eerste `#` is een fragment-id en zorgt ervoor dat foutopsporingsparameters niet correct werken.

## Adobe Experience Cloud Debugger {#section_A2798ED3A431409690A4BE08A1BFCF17}

Met de Adobe Experience Cloud Debugger kunt u snel en gemakkelijk inzicht krijgen in uw Target-implementatie. U kunt uw bibliotheekconfiguratie snel bekijken, verzoeken onderzoeken om ervoor te zorgen uw douaneparameters correct worden overgegaan, console het registreren inschakelen, en alle verzoeken van Target onbruikbaar maken. Verifieer in de Experience Cloud en u kunt het krachtige hulpmiddel MboxTrace gebruiken om uw activiteit en publiekskwalificaties evenals uw bezoekersprofiel te inspecteren.

Zie de volgende trainingsvideo&#39;s voor meer informatie:

Zie [Foutopsporing in.js met Adobe Experience Cloud voor meer informatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md).

## Als target.js tijdens levering niet kan laden {#section_ABBA5EFDFFB749D8BEE172DB1F973058}

Mbox.js verzendt een koekje genoemd &quot;em-gehandicapt&quot;naar de bezoeker als target.js er niet in slaagt om tijdens levering te laden. Dit koekje verhindert aanbiedingen die gebruikend de Visuele Composer van de Ervaring worden gecreeerd op de plaats terug te geven. Bezoekers met dit cookie zien de testinhoud niet en worden niet meegeteld in die activiteitenrapporten. Alle andere aanbiedingsinhoud (bijvoorbeeld van campagnes in Target Classic) wordt verder geladen. De cookie heeft een levensduur van 30 minuten vanaf het moment dat het laden mislukt.

## Topverkopers worden niet weergegeven in Aanbevelingen {#section_3920C857270A406C80BE6CBAC8221ECD}

De *`SiteCatalyst: purchase`* vraag kan niet voor de gegevens van het het algoritmeverkeer van de Aankoop worden gebruikt. Gebruik in plaats hiervan de *`orderConfirmPage`* aanroep.

## Prioriteit activiteit controleren {#section_3D0DD07240F0465BAF655D0804100AED}

Op vorm-gebaseerde activiteiten die met worden gecreeerd [!DNL Target Standard/Premium] zouden met activiteiten in [!DNL Target Classic] UI kunnen botsen die de zelfde prioriteit hebben en het zelfde [!DNL Target] verzoek gebruiken.

## De code van de douane veroorzaakt niet de verwachte resultaten in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Target biedt geen ondersteuning meer voor IE 8.

## JavaScript-inhoud die door de algemene [!DNL Target] aanvraag wordt geleverd, wordt niet geladen wanneer u mbox.js gebruikt. {#section_03EC9B9C410B4F52A7FCD81840311709}

Voer een upgrade uit naar [!DNL mbox.js] versie 58 of hoger.

mbox.js versie 58 en hoger voert niet-JavaScript-inhoud voor de algemene [!DNL Target] aanvraag direct uit nadat de HTML- `BODY` tag aanwezig is. JavaScript-inhoud binnen `<script>` tags voor de algemene [!DNL Target] aanvraag wordt uitgevoerd nadat de `DOMContentLoaded` gebeurtenis is geactiveerd. Deze volgorde waarin de inhoud wordt geleverd, zorgt ervoor dat JavaScript-inhoud voor de algemene [!DNL Target] aanvraag op de juiste wijze wordt geleverd en weergegeven.

## Target Cookie wordt niet ingesteld {#section_77AFEB541C0B495EB67E29A4475DF960}

Als uw site een subdomein heeft, zoals [!DNL us.domain.com], maar u hebt de Target cookie ingesteld [!DNL domain.com] (in plaats van [!DNL us.domain.com]), moet u de `cookieDomain` instelling overschrijven. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md)voor meer informatie.

## Target-inhoud flikkert of wordt niet weergegeven als een element ook onderdeel is van AEM-personalisatie. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Als een DOM-element onderdeel is van een Adobe Experience Manager (AEM) voor personalisatie en een Target-activiteit, kan de Target-inhoud flikkeren of niet worden weergegeven.

Om dit te verhelpen, kunt u de personalisatie van AEM op pagina&#39;s onbruikbaar maken waarop Target loopt.

## Omleiding en aanbiedingen op afstand kunnen niet worden geleverd vanwege een ongeldige URL. {#section_7D09043B687F43B39DAEDF17D00375AC}

Als de omleiding of de aanbieding op afstand een ongeldige URL gebruikt, kan het zijn dat deze niet wordt geleverd.

Voor omleidingsvoorstellen kan de [!DNL Target] reactie bevatten `/* invalid redirect offer URL */`

of

Voor externe aanbiedingen kan de [!DNL Target] reactie `/* invalid remote offer URL */`

U kunt de [!DNL Target] reactie controleren in browser of mboxTrace gebruiken. Surf naar [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66) voor meer informatie over geldige URL&#39;s.

## Target-verzoeken vuren niet op mijn site.

at.js leidt geen Target-aanvragen in als u een ongeldig documenttype gebruikt. at.js vereist het HTML 5-documenttype.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Het ![zelfstudieginister voor extensies toevoegen](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Basic Target Debugging ![Tutorial badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### Mbox Trace ![Tutorial badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)