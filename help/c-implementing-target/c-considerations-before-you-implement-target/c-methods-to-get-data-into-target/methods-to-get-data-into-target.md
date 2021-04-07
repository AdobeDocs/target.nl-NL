---
keywords: implementeren;implementeren;instellen;instellen;pagina, parameter;tomcat;url gecodeerd;in-page profiel, kenmerk;mbox, parameter;in-page profiel, kenmerken;script, profielkenmerk;bulk profiel, update-API;single file, update-API;klantkenmerken;gegevensproviders;data provider;data provider
description: Gegevens ophalen in Doel (paginaparameters, profielkenmerken, scriptprofielkenmerken, gegevensproviders, update-API's met één profiel en bulkprofielen, klantkenmerken).
title: Hoe krijg ik gegevens in het doel?
feature: Implementatie
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: 70d4c5b4166081751246e867d90d43b67efa5469
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 0%

---

# Overzicht van methoden

Informatie over de verschillende methodes u kunt gebruiken om gegevens in [!DNL Adobe Target] te krijgen.

Beschikbare methoden zijn:

| Methode | Details |
| --- | --- |
| [Paginaparameters](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br> (ook wel &quot;parameters mbox&quot; genoemd) | Paginaparameters zijn naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik.<br>Paginaparameters zijn handig voor het verzenden van aanvullende paginagegevens naar Doel die niet met het profiel van de bezoeker hoeven te worden opgeslagen voor toekomstig doelgebruik. Deze waarden worden in plaats daarvan gebruikt om de pagina of de actie te beschrijven die de gebruiker op de specifieke pagina heeft ondernomen. |
| [Profielkenmerken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br> in pagina (ook wel &#39;profielkenmerken in de box&#39; genoemd) | Profielkenmerken in pagina zijn naam-/waardeparen die rechtstreeks door paginacode worden doorgegeven en die in het profiel van de bezoeker worden opgeslagen voor toekomstig gebruik.<br>Met profielkenmerken van pagina&#39;s kunnen gebruikersspecifieke gegevens in het doelprofiel worden opgeslagen, zodat deze later kunnen worden toegewezen en gesegmenteerd. |
| [Scriptprofielkenmerken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | Scriptprofielkenmerken zijn naam-/waardeparen die zijn gedefinieerd in de doeloplossing. De waarde wordt bepaald door het uitvoeren van een JavaScript-fragment op de server van Target per serveraanroep.<br>Gebruikers schrijven kleine codefragmenten die per mbox vraag uitvoeren, en alvorens een bezoeker voor publiek en activiteitenlidmaatschap wordt geëvalueerd. |
| [Gegevensleveranciers](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | Gegevensleveranciers zijn een mogelijkheid waarmee u eenvoudig gegevens van derden aan Target kunt doorgeven. |
| Bulkprofielupdate-API | Verzend via de API een CSV-bestand naar Target met updates van het bezoekersprofiel voor veel bezoekers. Elk bezoekersprofiel kan met veelvoudige in-pagina profielattributen in één vraag worden bijgewerkt. |
| API voor bijwerken van één profiel | Bijna identiek aan de API voor het bijwerken van het bulkprofiel, maar één bezoekersprofiel wordt tegelijk bijgewerkt, in lijn in de API-aanroep in plaats van met een .csv-bestand. |
| Klantkenmerken | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target. |







## API voor updates van bulkprofielen {#section_92AB4820A5624C669D9A1F1B6220D4FA}

Verzend via de API een CSV-bestand naar Target met updates van het bezoekersprofiel voor veel bezoekers. Elk bezoekersprofiel kan met veelvoudige in-pagina profielattributen in één vraag worden bijgewerkt.

Deze optie lijkt sterk op Customer Attributes met een paar verschillen:

* Klantkenmerken gebruiken een FTP-upload terwijl de API voor het bijwerken van het doelbulkprofiel een HTTP-POST-API gebruikt.
* De gegevens van de Attributen van de klant kunnen met Analytics worden gedeeld. Bulkprofielupdate kan alleen worden gebruikt in Doel.
* De steun van de Attributen van de klant die tot een profiel voor een gebruikersDoel leidt heeft nog niet gezien. De API voor het bijwerken van het bulkprofiel werkt alleen bestaande doelprofielen bij.
* Klantkenmerken vereisen het gebruik van de Experience Cloud-id (ECID). Voor de API voor het bijwerken van het bulkprofiel is de TNT-id of de `mbox3rdPartyId` vereist.
* U kunt de volgende tekens niet verzenden in `mbox3rdPartyID`: plus-teken (+) en slash (/).

### Indeling

Het .csv-bestand moet naar elke bezoeker verwijzen via zijn of haar doel-PCID of mboxThirdPartyId. De Experience Cloud-id (ECID) wordt niet ondersteund. Alle profielkenmerken/waarden worden gemaakt en bijgewerkt via de API. De indelingsgegevens zijn beschikbaar in de API-documentatie.

### Voorbeelden

Uw CRM of ander intern systeem slaat waardevolle gegevens over uw bezoekers op die u constant in Doel wilt bijwerken, zonder de profielgegevens in uw paginaimplementatie bloot te stellen.

### Voordelen van methode

Geen limiet voor het aantal profielkenmerken.

Profielkenmerken die via de site worden verzonden, kunnen via de API worden bijgewerkt en andersom.

### Caveats

Het batchbestand moet kleiner zijn dan 50 MB. Bovendien mag het totale aantal rijen niet groter zijn dan 500.000 rijen per upload.

Er geldt geen limiet voor het aantal rijen dat of de rijen die u kunt uploaden over een periode van 24 uur in volgende batches. Nochtans, zou het innameproces tijdens kantooruren kunnen worden vertraagd om ervoor te zorgen dat andere processen efficiënt lopen.

Opeenvolgende [V2 vraag van de partijupdate](https://developers.adobetarget.com/api/#updating-profiles) zonder mbox vraag binnen tussen voor zelfde thirdPartyIds treedt de eigenschappen met voeten die in de eerste vraag van de partijupdate worden bijgewerkt.

### Codevoorbeelden

Zie [Profielen bijwerken](https://developers.adobetarget.com/api/#updating-profiles).

### Koppelingen naar relevante informatie

[Profielen bijwerken](https://developers.adobetarget.com/api/#updating-profiles)

## API {#section_5D7A9DD7019F40E9AEF2F66F7F345A8D} voor bijwerken van één profiel

Bijna identiek aan de API voor het bijwerken van het bulkprofiel, maar één bezoekersprofiel wordt tegelijk bijgewerkt, in lijn in de API-aanroep in plaats van met een .csv-bestand.

### Indeling

De bezoeker moet via de waarde van Target mboxPC of de waarde mboxThirdPartyId worden geïdentificeerd. De Experience Cloud-id (ECID) wordt niet ondersteund.

### Voorbeelden

U wilt Doel in real time bijwerken wanneer een bezoeker één of andere off-line actie uitvoert, zoals het bereiken van een callcenter, wordt een lening gefinancierd, gebruikend een loyaliteitskaart in opslag, die tot een kiosk toegang hebben, etc.

### Voordelen van methode

Geen limiet voor het aantal profielkenmerken.

Profielkenmerken die via de site worden verzonden, kunnen via de API worden bijgewerkt en andersom.

### Caveats

Limiet van 1.000.000 API-aanroepen (1 miljoen) per periode van 24 uur

Alleen profielen worden bijgewerkt. Kan geen profiel maken voor een mogelijk gebruikersdoel dat nog niet is te zien.

### Codevoorbeelden

GET en POST ondersteund. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

### Koppelingen naar relevante informatie

[Profielen bijwerken](https://developers.adobetarget.com/api/#updating-profiles)

## Klantkenmerken {#section_C47FC7980A9A4608BD1A5F0BD900FA70}

Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik na het uploaden de gegevens in Adobe Analytics en Adobe Target.

Doelklanten van Standard kunnen 5 kenmerken gebruiken, doelklanten kunnen 200 kenmerken gebruiken.

### Indeling

Een .csv-bestand met Experience Cloud-id&#39;s (ECID&#39;s) en paren van kenmerknaam/waarde wordt geüpload via FTP of handmatig in de gebruikersinterface van de Experience Cloud.

### Voorbeelden

Uw CRM of ander intern systeem slaat waardevolle informatie op u met Adobe Experience Cloud, met inbegrip van Doel en Analytics wilt delen.

### Voordelen van methode

Als u klantgegevens uploadt, wordt voor die bezoeker in Target een profielvermelding gemaakt, zelfs als Target de bezoeker nog niet heeft kunnen zien.

Dezelfde gegevens zijn automatisch beschikbaar in Doel en Analyse.

FTP kan een eenvoudigere implementatiemethode zijn dan API.

### Caveats

Doelklanten van Standard kunnen 5 kenmerken benutten, doelklanten kunnen 200 kenmerken benutten

Kan waarden alleen bijwerken via Customer Attributes, niet op pagina.

Vereist Experience Cloud ID-implementatie (ECID).

### Codevoorbeelden

Details vindt u in [Een bron voor klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).

### Koppelingen naar relevante informatie

[Maak een bron voor klantkenmerken en upload het gegevensbestand](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
