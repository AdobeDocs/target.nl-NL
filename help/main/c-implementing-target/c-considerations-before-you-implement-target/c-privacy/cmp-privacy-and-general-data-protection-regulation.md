---
keywords: gdpr;eu;europese unie;privacy;faq;vaak gestelde vragen;cccpa;privacy;gegevensbescherming;opt-out;opt out;regering;regulering
description: Meer informatie over [!DNL Target] en de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere privacyvereisten.
title: Hoe werkt [!DNL Target] Regels voor privacy en gegevensbescherming afhandelen?
feature: Privacy & Security
role: Developer
exl-id: 5013a9d2-a463-4787-90ee-3248d9cb02b2
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '2223'
ht-degree: 0%

---

# Regels inzake privacy en gegevensbescherming

Informatie over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten. Leer hoe deze regels van invloed zijn op uw organisatie en [!DNL Adobe Target].

## Overzicht van privacy en algemene gegevensbeschermingsverordening (GDPR) {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Op 25 mei 2018 is de GDPR van de Europese Unie van kracht geworden. Voor meer informatie over wat deze verordening voor u betekent, zie [GDPR en uw bedrijf](https://business.adobe.com/privacy/general-data-protection-regulation.html).

Wanneer [!DNL Adobe] software en diensten levert aan een onderneming; [!DNL Adobe] handelt als Bewerker van Gegevens voor om het even welke persoonlijke gegevens het verwerkt en opslaat als deel van het verlenen van deze diensten. Als gegevensprocessor, [!DNL Adobe] verwerkt persoonlijke gegevens in overeenstemming met de toestemming en instructies van uw bedrijf (bijvoorbeeld zoals in uw overeenkomst met [!DNL Adobe]).

Als Controlemechanisme van Gegevens, bepaalt u de persoonlijke gegevens die [!DNL Adobe] processen en slaat namens u op. Als u [!DNL Adobe Experience Cloud] oplossingen, [!DNL Adobe] kan persoonlijke gegevens voor u ontvangen, afhankelijk van de oplossingen die u gebruikt en de informatie die u kiest om naar uw [!DNL Adobe Experience Cloud] account. Voor een gedetailleerde lijst met voorbeelden raadpleegt u [Adobe Experience Cloud Privacy](https://www.adobe.com/privacy/experience-cloud.html#collect).

[!DNL Adobe Experience Cloud] biedt API&#39;s die geschikt zijn voor GDPR voor gegevenscontrollers waarmee ze de volgende taken kunnen uitvoeren:

* Toegang tot informatie over betrokkenen die is opgeslagen binnen [!DNL Target]
* Gegevens van gegevensonderwerp verwijderen die zijn opgeslagen in [!DNL Target]

Zie voor meer informatie:

* [Overzicht Adobe Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target=-blank}
* [Handleiding Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html){target=_blank}
* [Overzicht van de gebruikersinterface voor Privacys Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/overview.html){target=_blank}

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

[!DNL Target] biedt ondersteuning voor aanmeldingsfunctionaliteit via tags in [!DNL Adobe Experience Platform] om u te helpen uw toestemmingsbeheerstrategie steunen. De opt-in functionaliteit laat klanten controleren hoe en wanneer [!DNL Target] -tag wordt geactiveerd. Er is ook een optie via [!DNL Adobe Experience Platform] om de [!DNL Target] tag. De mogelijkheid om Opt-In te gebruiken in het dialoogvenster [!DNL Target] at.js bibliotheek, zou u moeten gebruiken `targetGlobalSettings` en voeg de `optinEnabled=true` instellen. In [!DNL Adobe ExperiencePlatform], selecteert u &quot;inschakelen&quot; in het menu [!UICONTROL GDPR Opt-In] vervolgkeuzelijst in de installatieweergave van de extensie. Zie [Implementeren [!DNL Target] gebruiken [!DNL Adobe Experience Platform]](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/implement-target-using-adobe-launch/) voor meer informatie .

In het volgende codefragment wordt getoond hoe u het `optinEnabled=true` instellen:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>De aanmeldingsfunctionaliteit wordt ondersteund in at.js versie 1.7.0 en at.js 2.1.0 of hoger. Inschakelen wordt niet ondersteund in at.js versie 2.0.0 en 2.0.1.
>
>Gebruiken [!DNL Adobe Experience Platform] het beheer van de opt-in is de aanbevolen aanpak. Verdere korrelcontrole is beschikbaar bij: [!DNL Adobe Experience Platform] geselecteerde elementen van de pagina vóór verbergen [!DNL Target] het branden die nuttig zijn om als deel van uw toestemmingsstrategie te gebruiken.

Er zijn drie scenario&#39;s om te overwegen wanneer het gebruiken van Opt-binnen:

1. **De [!DNL Target] -tag is vooraf goedgekeurd via [!DNL Adobe Experience Platform] (of de eerder goedgekeurde betrokkene [!DNL Target]):** De [!DNL Target] tag wordt niet bewaard voor toestemming en functies zoals verwacht.
1. **De [!DNL Target] -tag is NIET vooraf goedgekeurd en `bodyHidingEnabled` is FALSE:** De [!DNL Target] tag wordt pas geactiveerd nadat de toestemming van de klant is verzameld. Voordat toestemming wordt verzameld, is alleen de standaardinhoud beschikbaar. Na ontvangst van de toestemming [!DNL Target] wordt aangeroepen en gepersonaliseerde inhoud beschikbaar is voor de betrokkene (bezoeker). Omdat alleen de standaardinhoud beschikbaar is vóór de toestemming, is het belangrijk om een geschikte strategie te gebruiken, zoals een welkomstpagina die een gedeelte van de pagina of inhoud beslaat die kan worden aangepast. Dit proces zorgt ervoor dat de ervaring voor de betrokkene (bezoeker) consistent blijft.
1. **De [!DNL Target] -tag is NIET vooraf goedgekeurd en `bodyHidingEnabled` is WAAR:** De [!DNL Target] tag wordt pas geactiveerd nadat de toestemming van de klant is verzameld. Voordat toestemming wordt verzameld, is alleen de standaardinhoud beschikbaar. Maar omdat `bodyHidingEnabled` is ingesteld op true, `bodyHiddenStyle` dicteert welke inhoud op de pagina wordt verborgen tot de [!DNL Target] -tag wordt geactiveerd (of de betrokkene weigert de aanmeldingsnaam, in welk geval de standaardinhoud wordt weergegeven). Standaard, `bodyHiddenStyle` is ingesteld op `body { opacity:0;}`, die de body-tag HTML verbergt. Aanbevolen pagina-configuratie bevindt zich hieronder zodat de gehele hoofdtekst van de pagina, behalve het dialoogvenster voor het beheer van de Adobe, wordt verborgen door de inhoud van de pagina in één container te plaatsen en het dialoogvenster voor het beheer van de toestemming in een aparte container. Deze setup configureert [!DNL Target] zodat alleen de container van de pagina-inhoud wordt verborgen. Zie de [Overzicht van Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en).

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

   Ervan uitgaande dat de `bodyHiddenStyle` van:

   ```
   #pageContent { opacity:0;}
   ```

## Privacy- en gegevensbeschermingsregels Veelgestelde vragen {#concept_41F88DE95D2943178BEC382736B5C038}

Veelgestelde vragen over de algemene gegevensbeschermingsverordening van de Europese Unie (GDPR), de California Consumer Privacy Act (CCPA) en andere internationale privacyvereisten die specifiek zijn voor [!DNL Target].

### Wat is de [!DNL Adobe] beleid voor deze verordeningen? {#section_A6849628D6524C80A6E16946DC5D25A9}

[!DNL Adobe] of voldoet al aan zijn verplichtingen als gegevensverwerker of voert deze uit. Adobe heeft een sterke basis voor gecertificeerde beveiliging en privacycontroles door ontwerp en heeft productverbeteringen aangebracht vóór de deadline van mei 2018. De klanten van de onderneming hebben de verantwoordelijkheid om deze verhogingen uit te voeren en om het even welk noodzakelijk beleid en procedures bij te werken.

### Moet mijn bedrijf, de Data Controller, een GDPR- of CCPA-verzoek indienen bij elke [!DNL Adobe Experience Cloud] de oplossing die zij gebruikt? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

Nee, [!DNL Adobe] biedt een centrale manier om gegevenscontrollers te helpen voldoen aan hun GDPR- en CCPA-vereisten. Gegevenscontrollers hoeven niet rechtstreeks naar elke oplossing te gaan.

Alle GDPR- en CCPA-verzoeken [!DNL Experience Cloud] oplossingen, waaronder [!DNL Target], door een centraal [!DNL Adobe] API, momenteel de GDPR-API genoemd. De API voltooit dan het verzoek over het Controlemechanisme van Gegevens [!DNL Experience Cloud] oplossingssuite.

### Welke informatie [!DNL Adobe] klanten in staat stellen om in antwoord op een verzoek van een betrokkene/gebruiker te schrappen? {#section_4B51D00924EC4166B2442218B69214F0}

De informatie over een individuele bezoeker binnen [!DNL Target] bevindt zich in de [!DNL Target] Bezoekersprofiel. [!DNL Target] Hiermee kunnen klanten alle gegevens verwijderen die aan een id zijn gekoppeld in hun bezoekersprofiel. Voorbeelden van de profielgegevens [!DNL Target] winkels, zie [Bezoekerprofiel](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

Geaggregeerde of geanonimiseerde gegevens (bijvoorbeeld gegevens die een bepaalde persoon niet identificeren) of gegevens die geen verband houden met een specifieke persoon (bijvoorbeeld inhoudsgegevens), vallen buiten het bereik van een verzoek tot verwijdering van een gebruiker.

[!DNL Target] Bezoekerprofielen die 90 dagen inactief zijn, worden standaard verwijderd, zonder dat enige actie vereist is.

### Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voltooien [!DNL Target]? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

[!DNL Target] ondersteunt de volgende id-typen om een klantprofiel te zoeken:

| Gebruikersnaam | Naam ruimte-id-type | Naamruimte-id | Definitie |
|--- |--- |--- |--- |
| Experience Cloud-ID (ECID) | Standaard | 4 | [!UICONTROL Adobe Experience Cloud ID], voorheen bekend als bezoeker-id of Experience Cloud-id. U kunt de JavaScript-API gebruiken om deze id te zoeken (zie onderstaande details). |
| TnT-id / Cookie-id (TNTID) | Standaard | 9 | [!DNL Target] id is ingesteld als een cookie in de browser van de bezoeker. U kunt de JavaScript-API gebruiken om deze id te zoeken (zie onderstaande details). |
| ID/CRM-ID van derden (DERDE PARTYID) | [!DNL Target]-Specifiek | N.v.t. | Als u [!DNL Target] met uw CRM of andere unieke id-informatie voor uw klanten. |

>[!NOTE]
>
>Hoewel [!DNL Target] biedt ondersteuning voor cookies van zowel eerste als externe leveranciers [!DNL Target] cookies worden alleen aanbevolen voor GDPR en CCPA.

### Hoe werkt [!DNL Target] beheer van toestemming afhandelen? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR en CCPA veranderen niet wanneer u toestemming moet krijgen, maar hoe u het krijgt. De toestemmingsstrategie van elke klant hangt van zijn gegevensinzameling en gebruikspraktijken en zijn privacybeleid af. Goedkeuringsbeheer wordt niet ondersteund door en kan niet worden bereikt via [!DNL Target] voor GDPR en CCPA.

[!DNL Adobe] biedt momenteel geen oplossing voor het beheer van instemming, maar er zijn verschillende hulpmiddelen die zich op de markt ontwikkelen om aan enkele nieuwe vereisten te voldoen. Voor meer informatie over privacyinstrumenten in het algemeen, waaronder toestemmingsmanagers, raadpleegt u de [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) op de *International Association of Privacy Professionals (iaap)* website.

[!DNL Target] biedt ondersteuning voor aanmeldingsfunctionaliteit via [!DNL Adobe Experience Platform] om uw toestemmingsbeheersstrategie te steunen. De opt-in functionaliteit laat klanten controleren hoe en wanneer [!DNL Target] -tag wordt geactiveerd. Er is ook een optie via [!DNL Adobe Experience Platform] om de [!DNL Target] tag. Gebruiken [!DNL Adobe Experience Platform] het beheer van de opt-in is de aanbevolen aanpak. Verdere korrelcontrole is beschikbaar bij: [!DNL Adobe Experience Platform] om geselecteerde elementen van uw pagina vóór te verbergen [!DNL Target] afvuren kan nuttig zijn om te gebruiken als onderdeel van uw toestemmingsstrategie.

Voor meer informatie over GDPR, CCPA, en [!DNL Adobe Experience Platform], zie [De Adobe Privacy JavaScript-bibliotheek en GDPR](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en). Zie ook de *Adobe Target- en Adobe Experience Platform-opt-in* hierboven.

### doet `AdobePrivacy.js` informatie aan de GDPR-API verstrekken? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] doet *niet* deze informatie naar de API verzenden. De klant moet dat doen. Deze bibliotheek bevat alleen de id&#39;s die in de browser voor die specifieke bezoeker zijn opgeslagen.

### Wat doet `removeIdentities` verwijderen? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL `removeIdentities`] *alleen* verwijdert die identiteiten uit browser, en dat hangt slechts af van of [!DNL Adobe] de oplossing heeft deze ten uitvoer gelegd .

Bijvoorbeeld: [!DNL Target] verwijdert de cookies waarin de id&#39;s worden opgeslagen, maar [!DNL Adobe Audience Manager] (AAM) verwijdert de index-id die is opgeslagen in een cookie van een derde niet.

### Welke informatie moet in een [!DNL Target] GDPR- of CCPA-verzoek? {#section_D29A4744AE6344E68AD7710B185FD6D0}

Naast de eisen van de centrale Privacy Service, een geldig GDPR- of CCPA-bericht voor [!DNL Target] bevat:

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

### Welke soorten reacties kan ik verwachten? [!DNL Target] via de GDPR-API? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Aanvraagstatus | [!DNL Target] Antwoordbericht | Scenario |
|--- |--- |--- |
| Verwerking | Verwerking | [!DNL Target] heeft het verzoek van de GDPR of de CCPA ontvangen en wordt verwerkt. |
| Voltooid | Niet van toepassing - bedrijfcontext niet van toepassing | De IMS-id in de GDPR- of CCPA-aanvraag is niet toegewezen aan [!DNL Target] client.<br>Sommige bedrijven hebben meerdere IMS-id&#39;s. De IMS-id verzenden waar [!DNL Target] is provisioned. |
| Voltooid | Niet van toepassing - gebruikerscontext niet gevonden | De in het verzoek van de GDPR of de CCPA voor de specifieke bezoeker of betrokkene verstrekte identiteitskaart is niet aanwezig in de [!DNL Target] profielopslag.<br>Dit resultaat wordt ook geretourneerd wanneer u een naamruimte-id-type probeert te verzenden dat niet wordt ondersteund door [!DNL Target] (zie hierboven voor ondersteunde id&#39;s). |
| Fout | Foutbericht (details zijn afhankelijk van het type fout) | Fout bij het ophalen of verwijderen van het gewenste gegevensonderwerpprofiel.<br>Fout bij uploaden naar Azure voor toegangsaanvraag. |

### Welke reactie doet [!DNL Target] de GDPR-API voor een toegangsaanvraag sturen? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

De reacties op verzoeken om toegang bevatten een samenvatting van [!DNL Target] profiel voor de betrokken bezoeker. Deze return wordt naar de [!DNL Experience Cloud] GDPR-API, die op zijn beurt gegevenscontrollers een reactie stuurt.

Een monster [!DNL Target] API-reactie voor toegang kan er als volgt uitzien:

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
| namespace | Wordt ook wel gegevensbron genoemd. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voltooien [!DNL Target]?&quot; in dit onderwerp. |
| type | Het type van identiteitskaart waarvoor u GDPR of CCPA gegevenstoegang vroeg. [!DNL Target] accepteert verschillende ID-typen, waarvan sommige standaard zijn en sommige specifiek zijn voor [!DNL Target]. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voltooien [!DNL Target]?&quot; in dit onderwerp. |
| value | De id van de naamruimte/gegevensbron. Zie &quot;Welke IDs wordt gesteund om klanten te helpen een GDPR of CCPA toegang en schrappingsverzoek voltooien [!DNL Target]?&quot; voor geaccepteerde waarden. |
| integratiecode | De codes van de integratie zijn vriendschappelijke namen voor uw gegevensbronnen en helpen u uw gegevensbronnen volgen gemakkelijker dan het gebruiken van gegevensbron IDs. |

Als er meerdere waarden zijn opgegeven om profielen te identificeren, heeft elke geldige id één profielbestand. Een of meer profielbestanden worden via de GDPR Central API naar de centrale GDPR Azure Blob verzonden, in de vorm van [!DNL Target] JSON-reactie profiel.

Een monster [!DNL Target] Profiel-JSON kan er als volgt uitzien:

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
| sample_parameter | Veel informatie in de [!DNL Target] worden geüpload of rechtstreeks geleverd door de Data Controller. In dit voorbeeld is een parameter geüpload naar de [!DNL Target] profiel gebruiken met de API voor het bijwerken van profielen. Zie voor meer informatie [Methoden om gegevens in te voeren [!DNL Target]](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/methods-to-get-data-into-target/). |
| user.ReturnTimeOfDay | Dit standaardveld bevat de tijd van de dag van het meest recente retourbezoek van een gebruiker. |
| firstSessionStart | Dit standaardveld bevat de tijd van de dag waarop de eerste sessie van de gebruiker is gestart. |
| user.sessionCountScript | Veel informatie in de [!DNL Target] worden geüpload of rechtstreeks geleverd door de Data Controller. In dit voorbeeld verhoogt een profielscript het aantal sessies dat deze bezoeker op de site van de Data Controller heeft uitgevoerd. Zie voor meer informatie [Profielscriptkenmerken](/help/main/c-target/c-visitor-profile/profile-parameters.md). |

>[!NOTE]
>
>Dit codevoorbeeld is een verkorte versie van een [!DNL Target] profiel JSON ter illustratie. Veel van de gebieden van [!DNL Target] is niet standaard. Wat wordt geretourneerd, is afhankelijk van de informatie in dat specifieke bezoekersprofiel.

### doet [!DNL Target] steun IP verduistering? {#section_428907B0CD9842D9B245B38C66A53C6A}

[!DNL Target] steunt IP verwarring als u verkiest om het als deel van uw GDPR of CCPA implementatiestrategie te gebruiken. Zie voor meer informatie [Privacy](https://developer.adobe.com/target/before-implement/privacy/privacy/).

### Moet ik iets doen om te voorkomen dat mijn gegevens worden gedeeld of verkocht aan derden?

[!DNL Target] staat klanten niet toe gegevens rechtstreeks te delen of te verkopen van [!DNL Target] aan derden, zodat er geen opt-out is voor [!DNL Target].
