---
keywords: gdpr;eu;european union;privacy;faq;frequently asked questions;california consumer privacy act;ccpa;privacy;data protection;opt-out;opt out;government;regulation
description: Informatie over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten, en hoe deze regels van invloed zijn op uw organisatie en Adobe Target.
title: Informatie over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten, en hoe deze regels van invloed zijn op uw organisatie en Adobe Target.
feature: privacy and security
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '2274'
ht-degree: 0%

---


# Regels inzake privacy en gegevensbescherming {#privacy-and-general-data-protection-regulation-gdpr}

Informatie over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten, en hoe deze regels van invloed zijn op uw organisatie en Adobe Target.

## Overzicht van privacy en algemene gegevensbeschermingsverordening (GDPR) {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Op 25 mei 2018 is de GDPR van de Europese Unie van kracht geworden. Zie [GDPR en Uw bedrijf](https://www.adobe.com/privacy/general-data-protection-regulation.html)voor meer informatie over wat dit voor u betekent.

Wanneer [!DNL Adobe] software en de diensten aan een onderneming verleent, [!DNL Adobe] handelt als Bewerker van Gegevens voor om het even welke persoonlijke gegevens het verwerkt en opslaat als deel van het verlenen van deze diensten. Als gegevensverwerker, [!DNL Adobe] verwerkt persoonlijke gegevens in overeenstemming met de toestemming en de instructies van uw bedrijf (bijvoorbeeld, zoals die in uw overeenkomst met [!DNL Adobe]) worden vermeld.

Als Controlemechanisme van Gegevens, bepaalt u de persoonlijke gegevens die [!DNL Adobe] en namens u verwerken opslaan. Als u [!DNL Adobe Experience Cloud] oplossingen gebruikt, [!DNL Adobe] zouden de persoonlijke gegevens voor u, afhankelijk van de oplossingen kunnen ontvangen u gebruikt en de informatie u verkiest om naar uw [!DNL Adobe Experience Cloud] rekening te verzenden. Zie [Adobe Experience Cloud Privacy](https://www.adobe.com/privacy/marketing-cloud.html#collect)voor een gedetailleerde lijst met voorbeelden.

[!DNL Adobe Experience Cloud] API&#39;s die geschikt zijn voor GDPR, leveren voor gegevenscontrollers waarmee ze de volgende taken kunnen uitvoeren:

* Toegang tot informatie over betrokkenen die is opgeslagen binnen [!DNL Target]
* Gegevens van gegevensonderwerp verwijderen die zijn opgeslagen in [!DNL Target]

Zie voor meer informatie:

* [API-website van Adobe General Data Protection Regulation](https://www.adobe.io/apis/cloudplatform/gdpr.html)
* [GDPR-documentatie](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## Overzicht van de California Consumer Privacy Act (CCPA)

De California Consumer Privacy Act (CCPA) biedt Californische consumenten nieuwe rechten met betrekking tot hun persoonlijke gegevens en legt gegevensbeschermingsverantwoordelijkheden op aan bepaalde entiteiten die zaken in Californië leiden. De CCPA treedt in werking op 1 januari 2020.

Op hoog niveau verleent de wet Californië verschillende belangrijke rechten, waaronder rechten op:

* Verzoek om informatie (gegevenstoegang)
* Weigeren van verkoop van persoonlijke informatie (een zeer ruim gedefinieerd recht om af te zien van het delen van informatie met derden)
* Persoonlijke gegevens verwijderen
* ervan in kennis worden gesteld dat persoonsgegevens openbaar worden gemaakt of worden verkocht

Als u zich vorig jaar zou voorbereiden op de Europese privacywetgeving (GDPR), zouden sommige van deze rechten bekend kunnen zijn en zou veel van het werk dat u hebt gedaan, opnieuw kunnen worden uitgevoerd.

>[!NOTE]
>
>De toegang tot en het schrappen van gegevens tot zoals het op CCPA van toepassing is volgt het zelfde proces zoals voor GDPR.

## Adobe Target en [!DNL Experience Platform Launch] opt-in {#section_6F7B53F5E40C4425934627B653E831B0}

[!DNL Target] biedt ondersteuning voor aanmeldingsfuncties via [!DNL Launch] om uw strategie voor het beheer van uw toestemming te ondersteunen. Met de functie Inschakelen kunnen klanten bepalen hoe en wanneer de [!DNL Target] tag wordt geactiveerd. Er is ook een optie via [!DNL Launch] om de [!DNL Target] tag vooraf goed te keuren. Als u de mogelijkheid wilt inschakelen om Opt-In te gebruiken in de bibliotheek [!DNL Target] at.js, moet u de `targetGlobalSettings` instelling gebruiken `optinEnabled=true` en toevoegen. In [!DNL Launch] zult u &quot;toelaten&quot;van de [!UICONTROL GDPR Opt-In] drop-down lijst in de mening van de [!DNL Launch] uitbreidingsinstallatie moeten selecteren. Raadpleeg de documentatie [bij](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) Starten voor meer informatie.

Het volgende codefragment toont u hoe te om het `optinEnabled=true` plaatsen toe te laten:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>De aanmeldingsfunctionaliteit wordt ondersteund in at.js versie 1.7.0 en at.js 2.1.0 of hoger. Inschakelen wordt niet ondersteund in at.js versie 2.0.0 en 2.0.1.
>
>De aanbevolen aanpak is [!DNL Experience Platform Launch] om opt-in te beheren. Er is nog meer korrelige controle over [!DNL Launch] het verbergen van geselecteerde elementen van uw pagina voordat deze worden [!DNL Target] geactiveerd. Deze elementen zijn handig voor het maken van een acceptatiestrategie.

Er zijn drie scenario&#39;s om te overwegen wanneer het gebruiken van Opt-binnen:

1. **De[!DNL Target]tag wordt vooraf goedgekeurd via[!DNL Launch](of de betrokkene is eerder goedgekeurd[!DNL Target]):** De [!DNL Target] tag wordt niet bewaard voor toestemming en functies zoals verwacht.
1. **De[!DNL Target]tag is NIET vooraf goedgekeurd en`bodyHidingEnabled`is FALSE:** De [!DNL Target] tag wordt pas geactiveerd nadat de toestemming van de klant is verzameld. Voordat toestemming wordt verzameld, is alleen de standaardinhoud beschikbaar. Nadat de toestemming is ontvangen, [!DNL Target] wordt geroepen en de gepersonaliseerde inhoud is beschikbaar aan de betrokkene (bezoeker). Omdat alleen de standaardinhoud beschikbaar is voordat u toestemming geeft, is het belangrijk een geschikte strategie te gebruiken, zoals een welkomstpagina die een gedeelte van de pagina beslaat of inhoud die u kunt aanpassen. Dit zorgt ervoor dat de ervaring consistent blijft voor de betrokkene (bezoeker).
1. **De[!DNL Target]tag is NIET vooraf goedgekeurd en`bodyHidingEnabled`is TRUE:** De [!DNL Target] tag wordt pas geactiveerd nadat de toestemming van de klant is verzameld. Voordat toestemming wordt verzameld, is alleen de standaardinhoud beschikbaar. Omdat `bodyHidingEnabled` deze waarde is ingesteld op true, `bodyHiddenStyle` bepaalt u echter welke inhoud op de pagina wordt verborgen totdat de [!DNL Target] tag wordt geactiveerd (of de betrokkene de aanmeldingsnaam weigert, in welk geval de standaardinhoud wordt weergegeven). Standaard `bodyHiddenStyle` is deze ingesteld op `body { opacity:0;`} , waardoor de HTML-body-tag wordt verborgen. Onze aanbevolen paginaconfiguratie is hieronder weergegeven, zodat de volledige hoofdtekst van de pagina, behalve het dialoogvenster voor het beheer van de toestemming, wordt verborgen door de inhoud van de pagina in één container te plaatsen en het dialoogvenster voor het beheer van de toestemming in een aparte container. Deze opstelling vormt [!DNL Target] zodat het de container van de paginacontent slechts. Zie de documentatie van de [Lancering voor meer informatie over hoe te om deze montages](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html)te vormen.

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

   Ervan uitgaande dat `bodyHiddenStyle` :

   ```
   #pageContent { opacity:0;}
   ```

## Privacy- en gegevensbeschermingsregels Veelgestelde vragen {#concept_41F88DE95D2943178BEC382736B5C038}

Veelgestelde vragen over de algemene gegevensbeschermingsverordening (GDPR) van de Europese Unie, de California Consumer Privacy Act (CCPA) en andere specifieke internationale privacyvereisten voor Target.

### Wat is het beleid van de Adobe voor deze regelgeving? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] of voldoet al of voert onze verplichtingen als Bewerker van Gegevens uit. We hebben een sterke basis voor gecertificeerde controle op veiligheid en privacy door het ontwerp en hebben productverbeteringen doorgevoerd vóór de deadline van mei 2018. De klanten van de onderneming zullen de verantwoordelijkheid hebben om deze verhogingen uit te voeren, evenals om het even welk noodzakelijk beleid en procedures bij te werken.

### Moet mijn bedrijf, de Data Controller, een GDPR- of CCPA-verzoek indienen bij elke [!DNL Adobe Experience Cloud] oplossing die het gebruikt? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

Nee, [!DNL Adobe] biedt een centrale manier om gegevenscontrollers te helpen voldoen aan hun GDPR- en CCPA-vereisten. Gegevenscontrollers hoeven niet rechtstreeks naar elke oplossing te gaan.

Alle GDPR- en CCPA-aanvragen voor alle [!DNL Experience Cloud] oplossingen, inclusief [!DNL Target], worden gemaakt via een centrale Adobe API, die momenteel de GDPR API wordt genoemd. De API zal dan het verzoek over de de oplossingsreeks van het Controlemechanisme van Gegevens voltooien. [!DNL Experience Cloud]

### Welke informatie zal onze klanten [!DNL Adobe] toelaten om in antwoord op een gegevenssubject/een gebruikersverzoek te schrappen? {#section_4B51D00924EC4166B2442218B69214F0}

De informatie met betrekking tot een individuele bezoeker binnen [!DNL Target] is vermeld binnen het Profiel van de [!DNL Target] Bezoeker. [!DNL Target] onze klanten in staat stellen alle gegevens te verwijderen die aan een id zijn gekoppeld in hun bezoekersprofiel. Zie [!DNL Target] Bezoekersprofiel [voor voorbeelden van de](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)opslag van profielgegevens.

Geaggregeerde of geanonimiseerde gegevens (bijvoorbeeld gegevens die een bepaalde persoon niet identificeren) of gegevens die geen verband houden met een specifieke persoon (bijvoorbeeld inhoudsgegevens), vallen buiten het bereik van een verzoek tot verwijdering van een gebruiker.

[!DNL Target] Bezoekerprofielen die 90 dagen inactief zijn, worden standaard verwijderd, zonder dat enige actie vereist is.

### Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek tot voltooien [!DNL Target]? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] ondersteunt de volgende id-typen om een klantprofiel te zoeken:

| Gebruikersnaam | Naam ruimte-id-type | Naamruimte-id | Definitie |
|--- |--- |--- |--- |
| Experience Cloud-ID (ECID) | Standaard | 4 | Adobe Experience Cloud ID, voorheen bekend als bezoeker-ID of Marketing Cloud-ID. U kunt de JavaScript-API gebruiken om deze id te zoeken (zie onderstaande details). |
| TnT-id / Cookie-id (TNTID) | Standaard | 9 | Doel-id ingesteld als een cookie in de browser van de bezoeker. U kunt de JavaScript-API gebruiken om deze id te zoeken (zie onderstaande details). |
| ID/CRM-ID van derden (DERDE PARTYID) | Doelspecifiek | N.v.t. | Als u Target van uw CRM of andere unieke herkenningstekeninformatie voor uw klanten voorziet. |

>[!NOTE]
>
>Hoewel [!DNL Target] [!DNL Target] zowel first-party als derdedomeincookies ondersteunt, worden cookies van de eerste partij alleen aanbevolen voor GDPR en CCPA.

### Hoe gaat [!DNL Target] het beheer van toestemming? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR en CCPA veranderen niet wanneer u toestemming moet krijgen, maar hoe u het krijgt. De toestemmingsstrategie van elke klant hangt van zijn gegevensinzameling en gebruikspraktijken evenals zijn privacybeleid af. Het beheer van toestemming wordt niet ondersteund door en mag niet worden uitgevoerd via [!DNL Target] de GDPR en de CCPA.

[!DNL Adobe] biedt momenteel geen oplossing voor het beheer van instemming, maar er zijn verschillende hulpmiddelen die zich op de markt ontwikkelen om aan enkele nieuwe vereisten te voldoen. Zie voor meer informatie over privacy-instrumenten in het algemeen, waaronder toestemmingsmanagers, het [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) op de website van de *International Association of Privacy Professionals (iaap)* .

[!DNL Target] biedt ondersteuning voor de aanmeldingsfunctionaliteit via [!DNL Launch] ondersteuning voor uw toestemmingsbeheerstrategie. Met de functie Inschakelen kunnen klanten bepalen hoe en wanneer de [!DNL Target] tag wordt geactiveerd. Er is ook een optie via [!DNL Launch] om de [!DNL Target] tag vooraf goed te keuren. De aanbevolen aanpak is [!DNL Launch] om opt-in te beheren. Er is nog meer korrelige controle over het verbergen van geselecteerde elementen van uw pagina vóór het [!DNL Launch] [!DNL Target] vuren. Dit kan handig zijn als onderdeel van uw toestemmingsstrategie.

Voor meer informatie over GDPR, CCPA, en [!DNL Launch], zie [de Bibliotheek van JavaScript van de Privacy van de Adobe en GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). Zie ook de bovenstaande sectie *Adobe Target en Experience Platform Launch opt-in* .

### Verzendt AdobePrivacy.js informatie naar de GDPR API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] Deze informatie wordt *niet* naar de API verzonden. De klant moet dat doen. Deze bibliotheek bevat alleen de id&#39;s die in de browser voor die specifieke bezoeker zijn opgeslagen.

### Wat verwijdert removeIdentities? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities] *alleen* verwijdert deze identiteiten uit de browser en dat hangt alleen af van het feit of de [!DNL Adobe] oplossing de id heeft geïmplementeerd.

De cookies waarin de id&#39;s worden opgeslagen, worden bijvoorbeeld [!DNL Target] verwijderd, maar [!DNL Adobe Audience Manager] (AAM) verwijdert de index-id die is opgeslagen in een cookie van een derde niet.

### Welke informatie moet in een GDPR- of CCPA-aanvraag van Target worden opgenomen? {#section_D29A4744AE6344E68AD7710B185FD6D0}

Naast de vereisten van de centrale Privacy Service, [!DNL Target] bevat een geldig GDPR- of CCPA-bericht voor:

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

### Welke soorten reacties kan ik verwachten van Target via de GDPR API? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Aanvraagstatus | Doelresponsbericht | Scenario |
|--- |--- |--- |
| Verwerking | Verwerking | Doel heeft het verzoek van GDPR of CCPA ontvangen en verwerkt dit. |
| Voltooid | Niet van toepassing - bedrijfcontext niet van toepassing | De IMS-id in het GDPR- of CCPA-verzoek wordt niet toegewezen aan een doelclient.<br>Sommige bedrijven hebben meerdere IMS-id&#39;s. U moet de IMS-id verzenden waarin Target is ingericht. |
| Voltooid | Niet van toepassing - gebruikerscontext niet gevonden | De in het verzoek van de GDPR of de CCPA voor de specifieke bezoeker of betrokkene verstrekte id is niet aanwezig in de Target profile store.<br>Dit resultaat wordt ook geretourneerd wanneer u een naamruimte-id-type probeert te verzenden dat niet door Doel wordt ondersteund (zie hierboven voor ondersteunde id&#39;s). |
| Fout | Foutbericht (details zijn afhankelijk van het type fout) | Fout bij het ophalen of verwijderen van het gewenste gegevensonderwerpprofiel.<br>Fout bij uploaden naar Azure voor toegangsaanvraag. |

### Welke reactie verzendt Target naar de GDPR API voor een toegangsverzoek? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

De antwoorden op verzoeken om toegang tot gegevens bevatten een samenvatting van het [!DNL Target] profiel voor de betrokken bezoeker. Merk op dat deze terugkeer naar [!DNL Experience Cloud] GDPR API wordt verzonden, die op zijn beurt de Controllers van Gegevens een reactie verzendt.

Een voorbeeld van de API-respons voor [!DNL Target] toegang kan er als volgt uitzien:

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
| namespace | Wordt ook wel gegevensbron genoemd. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voor Doel voltooien?&quot; in dit onderwerp. |
| type | Het type van identiteitskaart waarvoor u GDPR of CCPA gegevenstoegang vroeg. Het doel keurt verscheidene types van identiteitskaart goed, waarvan sommige standaard zijn en wat doelspecifiek zijn. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voor Doel voltooien?&quot; in dit onderwerp. |
| value | De id van de naamruimte/gegevensbron. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voor Doel voltooien?&quot; voor geaccepteerde waarden. |
| integratiecode | De codes van de integratie zijn vriendschappelijke namen voor uw gegevensbronnen en helpen u uw gegevensbronnen volgen gemakkelijker dan het gebruiken van gegevensbron IDs. |

Als er meerdere waarden zijn opgegeven om profielen te identificeren, heeft elke geldige id één profielbestand. Het profielbestand of de profielbestanden worden via de GDPR Central API naar de centrale GDPR Azure Blob verzonden, in de indeling Profile JSON response. [!DNL Target]

Een voorbeeldprofiel [!DNL Target] JSON kan er als volgt uitzien:

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
| sample_parameter | Veel gegevens in het [!DNL Target] profiel worden geüpload of rechtstreeks geleverd door de gegevenscontroller. In dit voorbeeld is een parameter geüpload naar het [!DNL Target] profiel met de API voor profielupdate. Voor meer informatie, zie [Methoden om Gegevens in Doel](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md)te krijgen. |
| user.ReturnTimeOfDay | Dit standaardveld bevat de tijd van de dag van het meest recente retourbezoek van een gebruiker. |
| firstSessionStart | Dit standaardveld bevat de tijd van de dag waarop de eerste sessie van de gebruiker is gestart. |
| user.sessionCountScript | Veel gegevens in het [!DNL Target] profiel worden geüpload of rechtstreeks geleverd door de gegevenscontroller. In dit voorbeeld verhoogt een profielscript het aantal sessies dat deze bezoeker op de site van de Data Controller heeft uitgevoerd. Zie [Profielscriptkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md)voor meer informatie. |

>[!NOTE]
>
>Dit is een verkorte versie van een [!DNL Target] profiel JSON ter illustratie. Veel velden van het [!DNL Target] profiel zijn niet standaard. Wat wordt geretourneerd, is afhankelijk van de informatie in dat specifieke bezoekersprofiel.

### Steunt het Doel IP verduistering? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] steunt IP verwarring als u verkiest om het als deel van uw GDPR of CCPA implementatiestrategie te gebruiken. Zie [Privacy](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0)voor meer informatie.

### Moet ik iets doen om te voorkomen dat mijn gegevens worden gedeeld of verkocht aan derden?

Target kan klanten niet toestaan gegevens rechtstreeks van Target aan derden te delen of te verkopen, zodat er geen sprake is van een opt-out voor Target.
