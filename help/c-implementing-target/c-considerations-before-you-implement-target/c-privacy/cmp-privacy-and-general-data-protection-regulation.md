---
keywords: gdpr;eu;europese unie;privacy;faq;vaak gestelde vragen;cccpa;privacy;gegevensbescherming;opt-out;opt out;regering;regulering
description: Leer over [!DNL Target] en de Algemene Verordening van de Europese Unie van de Bescherming van Gegevens (GDPR), de Wet van de Consumentenprivacy van Californië (CCPA), en andere privacyvereisten.
title: Hoe behandelt  [!DNL Target] Privacy en gegevensbeschermingsverordeningen?
feature: Privacy en beveiliging
role: Developer
exl-id: 5013a9d2-a463-4787-90ee-3248d9cb02b2
source-git-commit: cf65cfb6641ce837717658e6fd5d0013e65f7875
workflow-type: tm+mt
source-wordcount: '2189'
ht-degree: 0%

---

# Regels inzake privacy en gegevensbescherming

Informatie over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten. Leer hoe deze verordeningen uw organisatie en [!DNL Adobe Target] beïnvloeden.

## Overzicht van privacy en algemene gegevensbeschermingsverordening (GDPR) {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Op 25 mei 2018 is de GDPR van de Europese Unie van kracht geworden. Voor meer informatie over wat deze verordening voor u betekent, zie [GDPR en Uw Zaken](https://business.adobe.com/privacy/general-data-protection-regulation.html).

Als [!DNL Adobe] software en services levert aan een onderneming, werkt [!DNL Adobe] als gegevensverwerker voor persoonlijke gegevens die het verwerkt en opslaat als onderdeel van het aanbieden van deze services. Als gegevensverwerker verwerkt [!DNL Adobe] persoonlijke gegevens conform de toestemming en instructies van uw bedrijf (bijvoorbeeld zoals uiteengezet in uw overeenkomst met [!DNL Adobe]).

Als Controlemechanisme van Gegevens, bepaalt u de persoonlijke gegevens die [!DNL Adobe] in uw naam verwerkt en opslaat. Als u [!DNL Adobe Experience Cloud] oplossingen gebruikt, [!DNL Adobe] zou persoonlijke gegevens voor u kunnen ontvangen, afhankelijk van de oplossingen u gebruikt en de informatie u verkiest om naar uw [!DNL Adobe Experience Cloud] rekening te verzenden. Zie [Adobe Experience Cloud Privacy](https://www.adobe.com/privacy/experience-cloud.html#collect) voor een gedetailleerde lijst met voorbeelden.

[!DNL Adobe Experience Cloud] biedt API&#39;s die geschikt zijn voor GDPR voor gegevenscontrollers waarmee ze de volgende taken kunnen uitvoeren:

* Toegang krijgen tot onderwerpgegevens die zijn opgeslagen in [!DNL Target]
* Gegevens van gegevensonderwerp verwijderen die zijn opgeslagen in [!DNL Target]

Zie voor meer informatie:

* [API-website van Adobe General Data Protection Regulation](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [GDPR-documentatie](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en)

## Overzicht van de California Consumer Privacy Act (CCPA)

De California Consumer Privacy Act (CCPA) biedt Californische consumenten nieuwe rechten met betrekking tot hun persoonlijke gegevens en legt gegevensbeschermingsverantwoordelijkheden op aan bepaalde entiteiten die zaken in Californië leiden. De CCPA is op 1 januari 2020 in werking getreden.

Op hoog niveau verleent de wet Californië verschillende belangrijke rechten, waaronder rechten op:

* Verzoek om informatie (gegevenstoegang)
* Afzien van de verkoop van persoonlijke informatie (een breed gedefinieerd recht om af te zien van het delen van informatie met derden)
* Persoonlijke gegevens verwijderen
* ervan in kennis worden gesteld dat persoonsgegevens openbaar worden gemaakt of worden verkocht

Als u zich vorig jaar zou voorbereiden op de Europese privacywetgeving (GDPR), zouden sommige van deze rechten bekend kunnen zijn en zou veel van het werk dat u hebt gedaan, kunnen worden hergebruikt.

>[!NOTE]
>
>De toegang tot en het schrappen van gegevens zoals die op CCPA van toepassing zijn volgt het zelfde proces zoals voor GDPR.

## Adobe [!DNL Target] en [!DNL Adobe Experience Platform] opt-in {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] biedt ondersteuning voor aanmeldingsfuncties via tags  [!DNL Adobe Experience Platform] om uw strategie voor het beheer van machtigingen te ondersteunen. Met de functie Inschakelen kunnen klanten bepalen hoe en wanneer de tag [!DNL Target] wordt geactiveerd. Er is ook een optie via [!DNL Adobe Experience Platform] om de tag [!DNL Target] vooraf goed te keuren. Als u de mogelijkheid wilt inschakelen om Opt-In te gebruiken in de bibliotheek [!DNL Target] at.js, moet u `targetGlobalSettings` gebruiken en de instelling `optinEnabled=true` toevoegen. Selecteer in [!DNL Adobe ExperiencePlatform] &quot;enable&quot; in de vervolgkeuzelijst [!UICONTROL GDPR Opt-In] in de installatieweergave van de extensie. Zie [Implementeren [!DNL Target] met [!DNL Adobe Experience Platform]](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) voor meer informatie.

Het volgende codefragment toont u hoe te om `optinEnabled=true` het plaatsen toe te laten:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>De aanmeldingsfunctionaliteit wordt ondersteund in at.js versie 1.7.0 en at.js 2.1.0 of hoger. Inschakelen wordt niet ondersteund in at.js versie 2.0.0 en 2.0.1.
>
>Het gebruik van [!DNL Adobe Experience Platform] voor het beheer van opt-in is de aanbevolen aanpak. Er is nog meer korrelige controle in [!DNL Adobe Experience Platform] om geselecteerde elementen van uw pagina te verbergen voordat [!DNL Target] wordt geactiveerd die nuttig zijn om als onderdeel van uw toestemmingsstrategie te gebruiken.

Er zijn drie scenario&#39;s om te overwegen wanneer het gebruiken van Opt-binnen:

1. **De  [!DNL Target] tag wordt vooraf goedgekeurd via  [!DNL Adobe Experience Platform] (of de betrokkene heeft eerder goedgekeurd  [!DNL Target]):** De  [!DNL Target] tag wordt niet bewaard voor toestemming en functies zoals verwacht.
1. **De  [!DNL Target] tag is NIET vooraf goedgekeurd en  `bodyHidingEnabled` is FALSE:** De  [!DNL Target] tag wordt pas geactiveerd nadat de toestemming van de klant is verzameld. Voordat toestemming wordt verzameld, is alleen de standaardinhoud beschikbaar. Nadat de toestemming is ontvangen, wordt [!DNL Target] geroepen en de gepersonaliseerde inhoud is beschikbaar aan de betrokkene (bezoeker). Omdat alleen de standaardinhoud beschikbaar is vóór de toestemming, is het belangrijk om een geschikte strategie te gebruiken, zoals een welkomstpagina die een gedeelte van de pagina of inhoud beslaat die kan worden aangepast. Dit proces zorgt ervoor dat de ervaring voor de betrokkene (bezoeker) consistent blijft.
1. **De  [!DNL Target] tag is NIET vooraf goedgekeurd en  `bodyHidingEnabled` is TRUE:** de  [!DNL Target] tag wordt alleen geactiveerd nadat toestemming van de klant is verzameld. Voordat toestemming wordt verzameld, is alleen de standaardinhoud beschikbaar. Omdat `bodyHidingEnabled` is ingesteld op true, bepaalt `bodyHiddenStyle` echter welke inhoud op de pagina wordt verborgen totdat de tag [!DNL Target] wordt geactiveerd (of de betrokkene de aanmeldingsnaam weigert, in welk geval standaardinhoud wordt weergegeven). Standaard is `bodyHiddenStyle` ingesteld op `body { opacity:0;}`, waardoor de HTML-body-tag wordt verborgen. Aanbevolen pagina-configuratie bevindt zich hieronder zodat de gehele hoofdtekst van de pagina, behalve het dialoogvenster voor het beheer van de Adobe, wordt verborgen door de inhoud van de pagina in één container te plaatsen en het dialoogvenster voor het beheer van de toestemming in een aparte container. Met deze setup wordt [!DNL Target] zo geconfigureerd dat alleen de container van de pagina-inhoud wordt verborgen. Zie [Overzicht van de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en).

   De geadviseerde pagina opstelling voor scenario 3 is:

   ```
   <html> 
   <head> 
   //visitor, at.js 
   </head> 
   
   <body> 
   <div id = "consentManagerDialog"> 
   
   //consent manager html dialog goes here 
   </div> 
   
   <div id="pageContent"> 
   // page content goes here 
   </div> 
   
   </body> 
   </html> 
   ```

   Veronderstellend `bodyHiddenStyle` van:

   ```
   #pageContent { opacity:0;}
   ```

## Privacy- en gegevensbeschermingsregels Veelgestelde vragen {#concept_41F88DE95D2943178BEC382736B5C038}

Veelgestelde vragen over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere specifieke internationale privacyvereisten voor [!DNL Target].

### Wat is het [!DNL Adobe] beleid voor deze verordeningen? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] of voldoet al aan zijn verplichtingen als gegevensverwerker of voert deze uit. Adobe heeft een sterke basis voor gecertificeerde beveiliging en privacycontroles door ontwerp en heeft productverbeteringen aangebracht vóór de deadline van mei 2018. De klanten van de onderneming hebben de verantwoordelijkheid om deze verhogingen uit te voeren en om het even welk noodzakelijk beleid en procedures bij te werken.

### Moet mijn bedrijf, het Controlemechanisme van Gegevens, een GDPR of CPA- verzoek aan elke [!DNL Adobe Experience Cloud] oplossing voorleggen die het gebruikt? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

Nee, [!DNL Adobe] biedt een centrale manier om gegevenscontrollers te helpen voldoen aan hun GDPR- en CCPA-vereisten. Gegevenscontrollers hoeven niet rechtstreeks naar elke oplossing te gaan.

Alle GDPR- en CCPA-aanvragen voor [!DNL Experience Cloud]-oplossingen, inclusief [!DNL Target], worden uitgevoerd via een centrale [!DNL Adobe]-API, die momenteel de GDPR-API wordt genoemd. De API voltooit dan het verzoek over de [!DNL Experience Cloud] oplossingsreeks van het Controlemechanisme van Gegevens.

### Met welke informatie kunnen klanten [!DNL Adobe] gegevens verwijderen als reactie op een verzoek van een gegevenssubject/gebruiker? {#section_4B51D00924EC4166B2442218B69214F0}

De informatie met betrekking tot een individuele bezoeker binnen [!DNL Target] is bevat binnen [!DNL Target] het Profiel van de Bezoeker. [!DNL Target] Hiermee kunnen klanten alle gegevens verwijderen die aan een id zijn gekoppeld in hun bezoekersprofiel. Zie [Bezoekersprofiel](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E) voor voorbeelden van de profielgegevens [!DNL Target].

Geaggregeerde of geanonimiseerde gegevens (bijvoorbeeld gegevens die een bepaalde persoon niet identificeren) of gegevens die geen verband houden met een specifieke persoon (bijvoorbeeld inhoudsgegevens), vallen buiten het bereik van een verzoek tot verwijdering van een gebruiker.

[!DNL Target] Bezoekerprofielen die 90 dagen inactief zijn, worden standaard verwijderd, zonder dat enige actie vereist is.

### Welke id&#39;s worden ondersteund om klanten te helpen een aanvraag voor toegang en verwijdering van een GDPR- of CCPA-bestand voor [!DNL Target] te voltooien? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] ondersteunt de volgende id-typen om een klantprofiel te zoeken:

| Gebruikersnaam | Naam ruimte-id-type | Naamruimte-id | Definitie |
|--- |--- |--- |--- |
| Experience Cloud-ID (ECID) | Standaard | 4 | [!UICONTROL Adobe Experience Cloud ID], voorheen bekend als bezoeker-id of Experience Cloud-id. U kunt de JavaScript-API gebruiken om deze id te zoeken (zie onderstaande details). |
| TnT-id / Cookie-id (TNTID) | Standaard | 9 | [!DNL Target] id is ingesteld als een cookie in de browser van de bezoeker. U kunt de JavaScript-API gebruiken om deze id te zoeken (zie onderstaande details). |
| ID/CRM-ID van derden (DERDE PARTYID) | [!DNL Target]-Specifiek | N.v.t. | Als u [!DNL Target] van uw CRM of andere unieke herkenningstekeninformatie voor uw klanten verstrekt. |

>[!NOTE]
>
>Hoewel [!DNL Target] zowel first-party als derde dwars-domeinkoekjes steunt, worden de eerste - partij [!DNL Target] koekjes slechts geadviseerd voor GDPR en CCPA.

### Hoe omgaat [!DNL Target] met beheer van toestemming? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR en CCPA veranderen niet wanneer u toestemming moet krijgen, maar hoe u het krijgt. De toestemmingsstrategie van elke klant hangt van zijn gegevensinzameling en gebruikspraktijken en zijn privacybeleid af. Goedkeuringsbeheer wordt niet ondersteund door en moet niet worden bereikt via [!DNL Target] voor GDPR en CCPA.

[!DNL Adobe] biedt momenteel geen oplossing voor het beheer van instemming, maar er zijn verschillende hulpmiddelen die zich op de markt ontwikkelen om aan enkele nieuwe vereisten te voldoen. Zie het [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) op de *International Association of Privacy Professionals (iaap)*-website voor meer informatie over privacy-instrumenten in het algemeen, inclusief machtigingsmanagers.

[!DNL Target] biedt ondersteuning voor aanmeldingsfuncties via  [!DNL Adobe Experience Platform] de ondersteuning van uw toestemmingsbeheerstrategie. Met de functie Inschakelen kunnen klanten bepalen hoe en wanneer de tag [!DNL Target] wordt geactiveerd. Er is ook een optie via [!DNL Adobe Experience Platform] om de tag [!DNL Target] vooraf goed te keuren. Het gebruik van [!DNL Adobe Experience Platform] voor het beheer van opt-in is de aanbevolen aanpak. Er is meer korrelige controle in [!DNL Adobe Experience Platform] om geselecteerde elementen van uw pagina vóór het [!DNL Target] branden te verbergen die nuttig zouden kunnen zijn om als deel van uw toestemmingsstrategie te gebruiken.

Voor meer informatie over GDPR, CCPA, en [!DNL Adobe Experience Platform], zie [De Bibliotheek van JavaScript van de Privacy van de Adobe en GDPR](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en). Zie ook de sectie *Adobe Target en Adobe Experience Platform opt-in* hierboven.

### Verzendt `AdobePrivacy.js` informatie naar de GDPR API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] verzendt deze informatie  ** niet naar de API. De klant moet dat doen. Deze bibliotheek bevat alleen de id&#39;s die in de browser voor die specifieke bezoeker zijn opgeslagen.

### Wat verwijdert `removeIdentities`? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL `removeIdentities`] *verwijdert* alleen die identiteiten uit de browser en dat hangt alleen af van het feit of de  [!DNL Adobe] oplossing de id heeft geïmplementeerd.

[!DNL Target] verwijdert bijvoorbeeld de cookies waarin de id&#39;s worden opgeslagen, maar [!DNL Adobe Audience Manager] (AAM) verwijdert niet de demdex-id die is opgeslagen in een cookie van een andere fabrikant.

### Welke informatie moet in een [!DNL Target] verzoek van GDPR of CCPA worden omvat? {#section_D29A4744AE6344E68AD7710B185FD6D0}

Naast de vereisten van de centrale Privacy Service bevat een geldig GDPR- of CCPA-bericht voor [!DNL Target]:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            "namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            "namespace":"TNTID", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"THIRDPARTYID", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
}
```

### Welke soorten reacties kan ik verwachten van [!DNL Target] via de GDPR API? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Aanvraagstatus | [!DNL Target] Antwoordbericht | Scenario |
|--- |--- |--- |
| Verwerking | Verwerking | [!DNL Target] heeft het verzoek van de GDPR of de CCPA ontvangen en wordt verwerkt. |
| Voltooid | Niet van toepassing - bedrijfcontext niet van toepassing | De IMS-id in het GDPR- of CCPA-verzoek wordt niet toegewezen aan een [!DNL Target]-client.<br>Sommige bedrijven hebben meerdere IMS-id&#39;s. Verzend de IMS-id waarin [!DNL Target] is ingericht. |
| Voltooid | Niet van toepassing - gebruikerscontext niet gevonden | De id die in het verzoek van de GDPR of de CCPA voor de specifieke bezoeker of betrokkene wordt verstrekt, is niet aanwezig in het [!DNL Target] profielarchief.<br>Dit resultaat wordt ook geretourneerd wanneer u probeert een naamruimte-id-type te verzenden dat niet wordt ondersteund door  [!DNL Target] (zie hierboven voor ondersteunde id&#39;s). |
| Fout | Foutbericht (details zijn afhankelijk van het type fout) | Fout bij het ophalen of verwijderen van het gewenste gegevensonderwerpprofiel.<br>Fout bij uploaden naar Azure voor toegangsaanvraag. |

### Welk antwoord verzendt [!DNL Target] naar GDPR API voor een toegangsverzoek? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Reacties op verzoeken om toegang tot gegevens bevatten een overzicht van het [!DNL Target]-profiel voor de betrokken bezoeker. Deze terugkeer wordt verzonden naar [!DNL Experience Cloud] GDPR API, die op zijn beurt de Controllers van Gegevens een reactie verzendt.

Een voorbeeld [!DNL Target] API-respons voor toegang kan er als volgt uitzien:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            ~"namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            ~"namespace":"tntId", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"thirdPartyId", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
} 
```

| Veld | Beschrijving |
|--- |--- |
| jobId | Hiermee wordt de GDPR- of CCPA-taak-id van de centrale GDPR-API aangegeven. |
| imsOrgID | Verstrekt een uniek herkenningsteken voor uw bedrijf. |
| namespace | Wordt ook wel gegevensbron genoemd. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voor [!DNL Target] voltooien?&quot; in dit onderwerp. |
| type | Het type van identiteitskaart waarvoor u GDPR of CCPA gegevenstoegang vroeg. [!DNL Target] Hiermee accepteert u verschillende id-typen, waarvan sommige standaard zijn en sommige specifiek voor  [!DNL Target]. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voor [!DNL Target] voltooien?&quot; in dit onderwerp. |
| value | De id van de naamruimte/gegevensbron. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voor [!DNL Target] voltooien?&quot; voor geaccepteerde waarden. |
| integratiecode | De codes van de integratie zijn vriendschappelijke namen voor uw gegevensbronnen en helpen u uw gegevensbronnen volgen gemakkelijker dan het gebruiken van gegevensbron IDs. |

Als er meerdere waarden zijn opgegeven om profielen te identificeren, heeft elke geldige id één profielbestand. Een of meer profielbestanden worden via de GDPR Central API naar het centrale GDPR Azure-blok verzonden, in de notatie van [!DNL Target] Profile JSON response.

Een voorbeeld [!DNL Target] profiel JSON zou als het volgende voorbeeld kunnen kijken:

```
{"profileAttributes": 
 
"Sample_Parameter":{"value":"Gold Loyalty Status","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"user.ReturnTimeOfDay":{"value":"44.0","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"firstSessionStart":{"value":"1523497450602","modifiedAt":"2018-04-11T21:44:10.000-04:00"}, 
 
"user.sessionCountScript":{"value":"1","modifiedAt":"2018-04-11T21:44:14.000-04:00"} 
   } 
} 
```

De volgende tabel bevat een beschrijving van de JSON-velden voor het illustratieve profiel:

| Veld | Beschrijving |
|--- |--- |
| sample_parameter | Veel gegevens in het profiel [!DNL Target] worden geüpload of rechtstreeks geleverd door de gegevenscontroller. In dit voorbeeld is een parameter geüpload naar het profiel [!DNL Target] met behulp van de API voor het bijwerken van profielen. Voor meer informatie, zie [Methoden om Gegevens in  [!DNL Target]](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md) te krijgen. |
| user.ReturnTimeOfDay | Dit standaardveld bevat de tijd van de dag van het meest recente retourbezoek van een gebruiker. |
| firstSessionStart | Dit standaardveld bevat de tijd van de dag waarop de eerste sessie van de gebruiker is gestart. |
| user.sessionCountScript | Veel gegevens in het profiel [!DNL Target] worden geüpload of rechtstreeks geleverd door de gegevenscontroller. In dit voorbeeld verhoogt een profielscript het aantal sessies dat deze bezoeker op de site van de Data Controller heeft uitgevoerd. Zie [Scriptkenmerken profiel](/help/c-target/c-visitor-profile/profile-parameters.md) voor meer informatie. |

>[!NOTE]
>
>Dit codevoorbeeld is een verkorte versie van een [!DNL Target] profiel JSON voor illustratie. Veel velden van het profiel [!DNL Target] zijn niet standaard. Wat wordt geretourneerd, is afhankelijk van de informatie in dat specifieke bezoekersprofiel.

### Ondersteunt [!DNL Target] IP-verduistering? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] steunt IP verwarring als u verkiest om het als deel van uw GDPR of CCPA implementatiestrategie te gebruiken. Zie [Privacy](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0) voor meer informatie.

### Moet ik iets doen om te voorkomen dat mijn gegevens worden gedeeld of verkocht aan derden?

[!DNL Target] klanten niet toestaat gegevens rechtstreeks van  [!DNL Target] naar derden te delen of te verkopen, zodat er geen sprake is van een opt-out voor verkoop  [!DNL Target].
