---
keywords: mbox;mbox3rdPartyId;profielsynchronisatie;profielsynchronisatie;PCID
description: Leer hoe u mbox3rdPartyId gebruikt. Dit is de bezoekersidentiteitskaart van uw organisatie, zoals lidmaatschap identiteitskaart of het loyaliteitsprogramma van uw organisatie.
title: Hoe gebruik ik Real-Time Profile Syncing voor mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Real-time profielsynchronisatie voor mbox3rdPartyId

De `mbox3rdPartyId` in [!DNL Adobe Target] is de bezoekersidentiteitskaart van uw bedrijf, zoals lidmaatschapsidentiteitskaart voor het loyaliteitsprogramma van uw bedrijf.

Wanneer een bezoeker zich aanmeldt bij de site van een bedrijf, maakt het bedrijf doorgaans een id die is gekoppeld aan de account, de loyaliteitskaart, het lidmaatschapsnummer of andere toepasselijke id&#39;s voor dat bedrijf.

Wanneer een bezoeker tot een pagina toegang heeft waarop [!DNL Target] wordt toegelaten, wordt die bezoeker toegewezen een [!DNL Target] PCID. Als de bezoeker zich vervolgens aanmeldt en de implementatie `mbox3rdPartyId` doorgeeft aan [!DNL Target], maakt [!DNL Target] verbinding met de `mbox3rdPartyId`-PCID van die bezoeker.[!DNL Target]

Om de drie tot vijf minuten worden updates gesynchroniseerd met de database. Wanneer de bezoeker zich afmeldt, vervangen de samengevoegde gegevens de vorige gegevens verbonden aan `mbox3rdPartyId`, die tot een volledig verslag van de acties van die bezoeker leiden. Als hetzelfde kenmerk bestaat in beide id&#39;s, bijvoorbeeld de PCID heeft category=hats en de `mbox3rdPartyId` heeft category=skis, of als de bezoeker A zag voordat hij zich aanmeldt, maar ervaring B wordt opgeslagen in `mbox3rdPartyId`—het kenmerk dat is opgeslagen in `mbox3rdPartyId` overschrijft het kenmerk van de PCID. Als de bezoeker één activiteit of ervaring voordat het programma werd geopend had, maar een andere activiteit en ervaring worden opgeslagen in `mbox3rdPartyId`, na het aanmelden, wordt die bezoeker geplaatst in `mbox3rdPartyId` activiteit en ervaring.

| PCID (niet aangemeld) | mbox3rdPartyId (aangemeld) | Samengevoegd en opgeslagen naar mbox3rdPartyId |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Activiteit 1, Ervaring A | Activiteit 1, ervaring B | Activiteit 1, ervaring B |
| Activiteit 1 |  | Activiteit 1 |

Wanneer de bezoeker zich afmeldt, blijft het samengevoegde profiel behouden.

>[!NOTE]
>
>Als u onderscheid wilt maken tussen geverifieerde (aangemelde) gebruikers en niet-geverifieerde gebruikers, gebruikt u [!DNL Adobe Experience Cloud Identity Service] (ECID) in plaats van mbox3rdPartyID. Nadat een gebruiker met mbox3rdPartyID wordt geassocieerd, blijft het verbonden met de gebruiker zelfs na het ondertekenen uit.

>[!NOTE]
>
>[!DNL Adobe Analytics] De doelstellingen worden niet gevolgd in gevallen waar  [!DNL Adobe Experience Cloud] identiteitskaart (EDID) verandert (bijvoorbeeld, verandert de bezoeker apparaten), alhoewel het  [!DNL Target] profiel zou kunnen worden samengevoegd gebaseerd op mbox3rdPartyId en nog activiteitsinformatie heeft. Voor bezoekers die met dezelfde EDID zijn geïdentificeerd (bezoekers die de pagina met hetzelfde apparaat openen), zou [!DNL Analytics for Target] (A4T) moeten werken zoals verwacht.

## Overwegingen {#considerations}

* Als uw pagina meerdere vakken bevat en slechts voor een deel `3rdPartyID` wordt gebruikt, heeft [!DNL Target] geen apart bezoekersprofiel/context voor elke bezoekersaanvraag. De context `3rdPartyID` heeft voorrang op de context PCID. Het is voldoende dat één box `3rdPartyId` doorgeeft voordat de context prioriteit krijgt boven PCID.

   Stel dat een bezoeker een pagina opent voordat hij of zij zich aanmeldt en een ervaring ziet. De globale mbox gebruikt `3rdPartyID` niet. Na het aanmelden ziet de bezoeker een van de drie ervaringen met onderliggende postvakken, waarvan er sommige `3rdPartyID` gebruiken. De bezoeker bezoekt verschillende pagina&#39;s op de site en gebruikt vervolgens de knop Terug om terug te keren naar de hoofdpagina die wordt geopend voordat hij zich aanmeldt. Er wordt een andere ervaring weergegeven. In dit scenario ging de globale mbox niet `3rdPartyID` over, maar een of meer onderliggende mboxes wel. `3rdPartyID` heeft voorrang op PCID.

* U kunt de klant-id&#39;s van bezoekers naar [!DNL Target] sturen op twee manieren:

   1. Gebruik `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` is de parameternaam wanneer u  `targetPageParams` of  `targetPageParamsAll`
      * `thirdPartyId` Dit is de parameternaam die u rechtstreeks instelt in de payload van de API voor levering.
      * U kunt slechts één waarde in deze parameter verzenden.
   1. Gebruik de functie `setCustomerId`/`customerIds` van ECID Service.

      * `setCustomerId` is een functie die u kunt gebruiken op client-side (browser) implementaties wanneer VisitorAPI.js beschikbaar is op de pagina.
      * `customerIds` Dit is de parameternaam die wordt gebruikt wanneer u deze rechtstreeks instelt in de payload van de API voor levering en die gewoonlijk wordt uitgevoerd in implementaties op de server of in de IOT-indeling (internet van dingen).
      * In tegenstelling tot `mbox3rdPartyId`/`thirdPartyId`, kunt u veelvoudige IDs als lijst in deze benadering verzenden, maar omdat [!DNL Target] slechts één enkele klant ID per identiteitskaart TnT steunt, gebruikt het eerste identiteitskaart in de lijst met een bekende alias (alias die in de UI van Attributen van de Klant wordt gevormd).

   >[!IMPORTANT]
   >
   > Het gebruik van beide hierboven vermelde benaderingen voor één bezoeker kan leiden tot onjuiste profielsamenvoegingen van de niet-geverifieerde en geverifieerde [!DNL Target] profielen.
   >
   >Adobe adviseert niet dat u zowel `mbox3rdPartyId`/`thirdPartyId` als `setCustomerID`/`customerIds` samen gebruikt.
   >
   >Als u beide benaderingen moet gebruiken onderling verwisselbaar, zorg ervoor dat eerste identiteitskaart in de lijst die door `setCustomerID`/`customerIds` wordt gebruikt is wat door `thirdPartyId`/`mbox3rdPartyId` en vice versa wordt gebruikt.

