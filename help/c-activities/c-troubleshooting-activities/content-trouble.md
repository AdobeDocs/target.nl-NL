---
keywords: debug mbox;troubleshoot mbox;mbox issues;flicker;mboxDebug;mboxTrace;token;debugger;priority;activity priority;Adobe Experience Cloud Debugger;orderConfirmPage mbox;SiteCatalyst purchase mbox;top selling;top-seller
description: Als op de pagina de verwachte inhoud niet wordt weergegeven, kunt u een aantal stappen uitvoeren om fouten op te sporen in de levering van inhoud in Adobe Target.
title: Problemen met levering van inhoud oplossen
feature: Activities
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 0%

---


# Problemen met de levering van inhoud oplossen

Als op de pagina de verwachte inhoud niet wordt weergegeven, zijn er een paar stappen die u kunt uitvoeren om de levering van inhoud te debuggen.

* Controleer uw activiteit of campagnecode zorgvuldig. Een typefout of andere fout kan ertoe leiden dat de verwachte inhoud niet wordt weergegeven.
* Gebruik mboxTrace of mboxDebug om het [!DNL Target] verzoek problemen op te lossen.
* Gebruik Foutopsporing van Adobe Experience Cloud, een makkelijk te gebruiken hulpmiddel dat veel van de zelfde informatie zoals mboxDebug verstrekt, om het [!DNL Target] verzoek problemen op te lossen.

mboxDebug is vooral handig wanneer u [!DNL Target] op uw pagina instelt om ervoor te zorgen dat het [!DNL Target]-verzoek wordt geactiveerd en het cookie wordt ingesteld. Nochtans, gaat het niet in het soort detail dat wanneer het zuiveren van inhoudslevering nuttig is. Als uw activiteit niet op uw pagina verschijnt of ongewenste inhoud verschijnt, gebruik mboxTrace om de pagina in detail te onderzoeken en te zuiveren.

## Hiermee wordt het machtigingstoken opgehaald dat moet worden gebruikt met foutopsporingsgereedschappen {#section_BED130298E794D1FA229DB7C3358BA54}

Omdat mboxTrace en mboxDebug campagnegegevens en profielgegevens aan externe partijen kunnen blootstellen, wordt een toestemmingstoken vereist. Het toestemmingstoken kan in [!DNL Target] UI worden teruggewonnen. De token is zes uur geldig.

U moet een van de volgende gebruikersmachtigingen hebben om een verificatietoken te genereren:

* Minstens [!UICONTROL Editor] toestemming (of [!UICONTROL Approver])

   Voor meer informatie voor [!DNL Target Standard] klanten, zie [Specificeer rollen en Toestemmingen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers*. Zie [Bedrijfsmachtigingen configureren](/help/administrating-target/c-user-management/property-channel/properties-overview.md) voor meer informatie voor [!DNL Target Premium]-klanten.

* Beheerdersrol op het niveau van de werkruimte/het productprofiel

   Werkruimten zijn alleen beschikbaar voor klanten van [!DNL Target Premium]. Zie [Bedrijfsmachtigingen configureren](/help/administrating-target/c-user-management/property-channel/properties-overview.md) voor meer informatie.

* Admin Rights (toestemming Sysadmin) op het [!DNL Adobe Target] productniveau

Om het toestemmingstoken terug te winnen:

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. Klik in de sectie Foutopsporingsgereedschappen op **[!UICONTROL Generate New Authentication Token]**.

   ![Nieuwe verificatietoken genereren](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/debugger-auth-token.png)

1. Voeg het gegenereerde token als parameter toe aan uw URL om een van de geavanceerde foutopsporingsprogramma&#39;s in te schakelen.

   ![Token voor autorisatie](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/assets/auth-token.png)

## mboxTrace {#section_256FCF7C14BB435BA2C68049EF0BA99E}

mboxTrace laat u toe om spoorinformatie te ontvangen in bijlage aan [!DNL Target] reacties. De spoorinformatie weerspiegelt het resultaat van een [!DNL Target] vraag (bijvoorbeeld, een omzetting of een indruk) en om het even welke extra gegevens die kunnen helpen om te bepalen waarom dit bepaalde resultaat, zoals een reeks beschikbare takken te bepalen waaronder de selectie in een campagne werd gemaakt. Gebruik deze informatie om de levering van inhoud te zuiveren.

De volgende parameters zijn beschikbaar:

| mboxTrace-opties | Resultaat |
|--- |--- |
| `?mboxTrace=console` | Hiermee wordt het logboek als objecten afgedrukt in het logbestand van de console.<br>Voor at.js, in plaats van een nieuw browser venster of output aan de console zoals in mbox.js te poppen, zult u het verzoek van het Netwerk moeten inspecteren en onder Voorproef (Chrome) of Reactie (Firefox) kijken. |
| `?mboxTrace=json` | Drukt in consolelogboek als letterlijke JSON-tekenreeks af |
| `?mboxTrace=window` | Drukt in een pop-upvenster af als een JSON-tekenreeks |
| `?mboxTrace=disable` | Hiermee schakelt u de overtreksessiemodus uit |

**Voorbeeld van aanroep van mboxTrace**

`https://www.mysite.com/page.html?mboxTrace=window&authorization=f543abf-0111-4061-9619-d41d665c59a6`

In de uitvoer wordt zeer gedetailleerde informatie over de inhoud weergegeven. mboxTrace geeft details over uw campagne of activiteit en profiel. Het biedt ook een momentopname van het profiel vóór uitvoering en een momentopname van wat na uitvoering is gewijzigd. Het toont ook welke campagnes of activiteiten voor elke plaats werden geëvalueerd.

Sommige informatie omvat overeenkomende en niet-overeenkomende segment- en doel-id&#39;s:

* **SegmentId**: Identiteitskaart van segmenten, of van de herbruikbare segmentbibliotheek of anonieme die voor de bepaalde campagne worden gecreeerd.
* **TargetId**: Ids van doelstellingen, of van de bibliotheek van de doeluitdrukking of anonieme doelstellingen voor om het even welke segmenten van campagne.
* **Niet-overeenkomend**: Het verzoek kwam in deze oproep niet in aanmerking voor die segmenten of doelstellingen.
* **Overeenkomend**: Het verzoek wordt gekwalificeerd voor de gespecificeerde segmenten of de doelstellingen.

**MboxTrace gebruiken op aanbevolen pagina**&#39;s: Als u mboxTrace toevoegt als een queryparameter op pagina&#39;s met aanbevelingen, wordt het Recommendations-ontwerp op de pagina vervangen door een venster met mboxTrace-details, dat uitgebreide informatie over uw aanbevelingen bevat, zoals:

* Recommendations heeft vs. aanbevelingen opgevraagd
* De gebruikte sleutel en of het aanbevelingen produceert
* Door criteria gegenereerde aanbevelingen versus aanbevelingen voor back-ups
* Criteria configureren
* Uitgesloten en toegepaste insluitingen
* Verzamelingsregels

U hoeft `=console`, `=json` of `=window` niet op te nemen in de queryparameter. Als u klaar bent met de mboxTrace-details, voegt u `=disable` toe en drukt u op **[!UICONTROL Enter]** om terug te keren naar de normale weergavemodus.

Het normale functioneren en de vormgeving van uw site worden niet beïnvloed door mboxTrace. Bezoekers zien je reguliere Recommendations-ontwerp.

## mboxDebug {#mboxdebug}

Als u mboxDebug wilt gebruiken, voegt u een parameter mboxDebug toe aan het einde van de URL. De volgende lijst bevat informatie over [!DNL Target] reactie-verwante URL parameters.

>[!NOTE]
>
>Sommige parameters mboxDebug zijn beschikbaar met of zonder authentificatie.

| URL-parameters | Doel |
|--- |--- |
| `mboxDebug=1` | Foutopsporing<br>Het toevoegen van deze parameter aan om het even welke URL met de bepaalde verzoeken van het Doel opent een pop-up venster met waardevolle het zuiveren details. De informatie van het cookie, de waarden van PCid en van identiteitskaart van de Zitting worden weggeschreven, en alle URLs zijn zichtbaar. Klik op een verzoek-URL van het Doel om de reactie voor dat [!DNL Target] verzoek te tonen. Meer details zijn beschikbaar in [mbox_debug.pdf](/help/assets/mbox_debug.pdf). |
| `mboxDebug=x-cookie` | Het cookie wijzigen |
| `mboxDisable=1` | Vakken op de pagina uitschakelen |
| `mboxDebug=x-profile` | Profielenset weergeven. |
| `mboxDebug=x-time` | Reactietijd voor elk [!DNL Target] verzoek tonen |
| `mboxOverride.browserIp=<Insert IP address>` | Test geoting<br>Test oriëntatie met deze URL-parameter. Typ een IP adres als waarde voor dit attribuut, en het groeperen van Test&amp;Target evalueert dat IP adres tegen om het even welke geotargeting of segmentatie die in een campagne wordt geplaatst aan te passen. |

>[!NOTE]
>
>Controleer of het URL-fragment zich na parameters van queryreeksen bevindt. Om het even wat na eerste `#` is een fragmentherkenningsteken en veroorzaakt het zuiveren parameters om niet correct te functioneren.

## Adobe Experience Cloud-foutopsporing {#section_A2798ED3A431409690A4BE08A1BFCF17}

Met de Adobe Experience Cloud Debugger kunt u snel en gemakkelijk uw doelimplementatie begrijpen. U kunt uw bibliotheekconfiguratie snel bekijken, verzoeken onderzoeken om ervoor te zorgen uw douaneparameters correct worden overgegaan, console het registreren inschakelen, en alle verzoeken van het Doel onbruikbaar maken. Verifieer in de Experience Cloud en u kunt het krachtige hulpmiddel MboxTrace gebruiken om uw activiteit en publiekskwalificaties evenals uw bezoekersprofiel te inspecteren.

Zie de volgende trainingsvideo&#39;s voor meer informatie:

Zie [Foutopsporing bij.js met Adobe Experience Cloud debugger](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md) voor meer informatie.

## Als target.js tijdens levering {#section_ABBA5EFDFFB749D8BEE172DB1F973058} niet kan laden

Mbox.js verzendt een koekje genoemd &quot;em-gehandicapt&quot;naar de bezoeker als target.js er niet in slaagt om tijdens levering te laden. Dit koekje verhindert aanbiedingen die gebruikend de Visuele Composer van de Ervaring worden gecreeerd op de plaats terug te geven. Bezoekers met dit cookie zien de testinhoud niet en worden niet meegeteld in die activiteitenrapporten. Alle andere aanbiedingsinhoud (bijvoorbeeld uit campagnes in Target Classic) wordt verder geladen. De cookie heeft een levensduur van 30 minuten vanaf het moment dat het laden mislukt.

## Topverkopers worden niet weergegeven in Recommendations {#section_3920C857270A406C80BE6CBAC8221ECD}

De *`SiteCatalyst: purchase`* vraag kan niet voor de gegevens van het het algoritmeverkeer van de Aankoop worden gebruikt. Gebruik in plaats hiervan de *`orderConfirmPage`*-aanroep.

## Prioriteit activiteit {#section_3D0DD07240F0465BAF655D0804100AED} controleren

Op vorm-gebaseerde activiteiten die met [!DNL Target Standard/Premium] worden gecreeerd zouden met activiteiten kunnen botsen die in [!DNL Target Classic] UI worden gecreeerd die de zelfde prioriteit hebben en het zelfde [!DNL Target] verzoek gebruiken.

## De code van de douane veroorzaakt niet de verwachte resultaten in Internet Explorer 8. {#section_FAC3651F19144D12A37A3E4F14C06945}

Doel biedt geen ondersteuning meer voor IE 8.

## JavaScript-inhoud die door de algemene [!DNL Target]-aanvraag wordt geleverd, wordt niet geladen wanneer u mbox.js gebruikt. {#section_03EC9B9C410B4F52A7FCD81840311709}

Voer een upgrade uit naar [!DNL mbox.js] versie 58 of hoger.

mbox.js versie 58 en hoger voert niet-JavaScript inhoud voor het globale [!DNL Target] verzoek onmiddellijk uit nadat de markering van HTML `BODY` aanwezig is. JavaScript-inhoud binnen `<script>`-tags voor de algemene [!DNL Target]-aanvraag wordt uitgevoerd nadat de gebeurtenis `DOMContentLoaded` is geactiveerd. Deze volgorde van de levering van inhoud zorgt ervoor dat JavaScript-inhoud voor het algemene [!DNL Target]-verzoek op de juiste wijze wordt geleverd en weergegeven.

## Doelcookie wordt niet ingesteld {#section_77AFEB541C0B495EB67E29A4475DF960}

Als uw site een subdomein heeft, zoals [!DNL us.domain.com], maar u de doelcookie moet instellen op [!DNL domain.com] (in plaats van [!DNL us.domain.com]), moet u de instelling `cookieDomain` overschrijven. Zie [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) voor meer informatie.

## De inhoud van het doel flikkert of wordt niet getoond als een element ook deel van AEM verpersoonlijking uitmaakt. {#section_9E1DABEB75AB431FB9F09887E6DD07D3}

Als een DOM-element onderdeel is van Adobe Experience Manager (AEM) personalization targeting en een doelactiviteit, kan de doelinhoud flikkeren of niet worden weergegeven.

U verhelpt dit door AEM personalisatie uit te schakelen op pagina&#39;s waarop Target wordt uitgevoerd.

## Omleiding en aanbiedingen op afstand kunnen niet worden geleverd vanwege een ongeldige URL. {#section_7D09043B687F43B39DAEDF17D00375AC}

Als de omleiding of de aanbieding op afstand een ongeldige URL gebruikt, kan het zijn dat deze niet wordt geleverd.

Voor omleidingsaanbiedingen kan het [!DNL Target]-antwoord `/* invalid redirect offer URL */` bevatten

of

Voor externe aanbiedingen kan de [!DNL Target]-reactie `/* invalid remote offer URL */` bevatten

U kunt de reactie [!DNL Target] in browser controleren of mboxTrace gebruiken. Zie [https://tools.ietf.org/html/std66](https://tools.ietf.org/html/std66) voor meer informatie over geldige URL&#39;s.

## Doelverzoeken worden niet op mijn site geactiveerd.

at.js leidt geen verzoeken van het Doel in brand als u een ongeldig documenttype gebruikt. at.js vereist het HTML 5-documenttype.

## Trainingsvideo&#39;s

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Voeg de extensie ![Zelfstudie-badge](/help/assets/tutorial.png) toe

>[!VIDEO](https://video.tv.adobe.com/v/23114t2/)

### Standaarddoelfoutopsporing ![Zelfstudie-badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23115t2/)

### Mbox Trace ![Zelfstudie badge](/help/assets/tutorial.png)

>[!VIDEO](https://video.tv.adobe.com/v/23113t2/)