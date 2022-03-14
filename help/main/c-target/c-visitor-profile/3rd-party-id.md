---
keywords: mbox;mbox3rdPartyId;profielsynchronisatie;profielsynchronisatie;PCID
description: Leer hoe u mbox3rdPartyId gebruikt. Dit is de bezoekersidentiteitskaart van uw organisatie, zoals lidmaatschap identiteitskaart of het loyaliteitsprogramma van uw organisatie.
title: Hoe gebruik ik Real-Time Profile Syncing voor mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Real-time profielsynchronisatie voor mbox3rdPartyId

De `mbox3rdPartyId` in [!DNL Adobe Target] is de bezoeker-id van uw bedrijf, zoals de lidmaatschaps-id voor het loyaliteitsprogramma van uw bedrijf.

Wanneer een bezoeker zich aanmeldt bij de site van een bedrijf, maakt het bedrijf doorgaans een id die is gekoppeld aan de account, de loyaliteitskaart, het lidmaatschapsnummer of andere toepasselijke id&#39;s voor dat bedrijf.

Wanneer een bezoeker een pagina opent waarop [!DNL Target] is ingeschakeld, wordt aan die bezoeker een [!DNL Target] PCID. Als de bezoeker zich vervolgens aanmeldt en de implementatie de `mbox3rdPartyId` tot [!DNL Target], [!DNL Target] verbindt de `mbox3rdPartyId` met de [!DNL Target] PCID.

De updates worden gesynchroniseerd met de profielopslag om de 5-10 minuten. Wanneer de sessie van de bezoeker is beëindigd, vervangen de samengevoegde gegevens de vorige gegevens die aan de `mbox3rdPartyId`, een volledige record te maken van de acties van die bezoeker. Als hetzelfde kenmerk voorkomt in beide id&#39;s, heeft de PCID bijvoorbeeld category=hats en de id `mbox3rdPartyId` heeft category=skis, of als de bezoeker A vóór het programma openen zag, maar ervaring B wordt opgeslagen in `mbox3rdPartyId`—het kenmerk dat is opgeslagen in het dialoogvenster `mbox3rdPartyId` Hiermee overschrijft u het kenmerk van de PCID. Als de bezoeker een activiteit of ervaring had voordat hij zich aanmeldt, maar een andere activiteit en ervaring zijn opgeslagen in het dialoogvenster `mbox3rdPartyId`, na het aanmelden, wordt die bezoeker in de `mbox3rdPartyId` activiteit en ervaring.

| PCID (niet aangemeld) | mbox3rdPartyId (aangemeld) | Samengevoegd en opgeslagen naar mbox3rdPartyId |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Activiteit 1, Ervaring A | Activiteit 1, ervaring B | Activiteit 1, ervaring B |
| Activiteit 1 |  | Activiteit 1 |

Wanneer de bezoeker zich afmeldt, blijft het samengevoegde profiel behouden.

>[!NOTE]
>
>Als u onderscheid wilt maken tussen geverifieerde (aangemelde) gebruikers en niet-geverifieerde gebruikers, gebruikt u de optie [!DNL Adobe Experience Cloud Identity Service] (ECID) in plaats van mbox3rdPartyID. Nadat een gebruiker met mbox3rdPartyID wordt geassocieerd, blijft het verbonden met de gebruiker zelfs na het ondertekenen uit.

>[!NOTE]
>
>[!DNL Adobe Analytics] doelstellingen worden niet bijgehouden in gevallen waarin de [!DNL Adobe Experience Cloud] ID (ECID) verandert (bijvoorbeeld de bezoeker wijzigt apparaten), ook als de [!DNL Target] profiel kan worden samengevoegd op basis van de mbox3rdPartyId en heeft nog steeds activiteitsgegevens. Voor bezoekers met dezelfde ECID (personen die de pagina met hetzelfde apparaat openen): [!DNL Analytics for Target] (A4T) zou moeten werken zoals verwacht.

## Overwegingen {#considerations}

* Als uw pagina meerdere vakken bevat en slechts voor een deel `3rdPartyID`, [!DNL Target] heeft geen afzonderlijk bezoekersprofiel/aparte context voor elke bezoekersaanvraag. De `3rdPartyID` context heeft voorrang op de PCID-context. Het is voldoende dat één box wordt doorgegeven `3rdPartyId` voor zijn context voorrang te geven boven PCID.

   Stel dat een bezoeker een pagina opent voordat hij of zij zich aanmeldt en een ervaring ziet. De algemene box wordt niet gebruikt `3rdPartyID`. Na het aanmelden ziet de bezoeker een van de drie ervaringen met onderliggende postvakken, waarvan er enkele worden gebruikt `3rdPartyID`. De bezoeker bezoekt verschillende pagina&#39;s op de site en gebruikt vervolgens de knop Terug om terug te keren naar de hoofdpagina die wordt geopend voordat hij zich aanmeldt. Er wordt een andere ervaring weergegeven. In dit scenario ging de globale box niet voorbij `3rdPartyID`, maar een of meer van de onderliggende dozen wel. `3rdPartyID` heeft voorrang op PCID.

* U kunt klanten-id&#39;s van bezoekers verzenden naar [!DNL Target] twee methoden gebruiken:

   1. Gebruiken `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` is de parameternaam wanneer u `targetPageParams` of `targetPageParamsAll`
      * `thirdPartyId` Dit is de parameternaam die u rechtstreeks instelt in de payload van de API voor levering.
      * U kunt slechts één waarde in deze parameter verzenden.
   1. Gebruik de `setCustomerId`/`customerIds` functie van ECID Service.

      * `setCustomerId` is een functie die u kunt gebruiken op client-side (browser) implementaties wanneer VisitorAPI.js beschikbaar is op de pagina.
      * `customerIds` Dit is de parameternaam die wordt gebruikt wanneer u deze rechtstreeks instelt in de payload van de API voor levering en die gewoonlijk wordt uitgevoerd in implementaties op de server of in de IOT-indeling (internet van dingen).
      * Anders `mbox3rdPartyId`/`thirdPartyId`, kunt u meerdere id&#39;s als een lijst verzenden in deze aanpak, maar omdat [!DNL Target] steunt slechts één enkele klant identiteitskaart per identiteitskaart TnT, gebruikt het eerste identiteitskaart in de lijst met een bekende alias (alias die in de UI van de Attributen van de Klant wordt gevormd).

   U kunt `mbox3rdPartyId`/`thirdPartyId` indien [!DNL Target] is uw enige [!DNL Adobe Experience Cloud] en u wilt geen Klantkenmerken gebruiken. Voor alle andere gevallen raden we u aan `setCustomerId`/`customerIds` voor het verzenden van je klant-id&#39;s.

   >[!IMPORTANT]
   >
   > Het gebruik van beide hierboven vermelde benaderingen voor één bezoeker kan leiden tot onjuiste profielsamenvoegingen van de niet-geverifieerde en geverifieerde [!DNL Target] profielen.
   >
   >Adobe adviseert niet beide te gebruiken `mbox3rdPartyId`/`thirdPartyId` en `setCustomerID`/`customerIds` samen.
   >
   >Als u beide methoden onderling moet gebruiken, moet u ervoor zorgen dat de eerste id in de lijst die wordt gebruikt door `setCustomerID`/`customerIds` is wat wordt gebruikt door `thirdPartyId`/`mbox3rdPartyId` en omgekeerd.

