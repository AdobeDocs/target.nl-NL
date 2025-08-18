---
keywords: mbox;mbox3rdPartyId;profielsynchronisatie;profielsynchronisatie;PCID
description: Leer hoe u mbox3rdPartyId gebruikt. Dit is de bezoekersidentiteitskaart van uw organisatie, zoals lidmaatschap identiteitskaart of het loyaliteitsprogramma van uw organisatie.
title: Hoe gebruik ik Real-Time Profile Syncing voor mbox3rdPartyId?
feature: Audiences
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Real-time profielsynchronisatie voor mbox3rdPartyId

De `mbox3rdPartyId` in [!DNL Adobe Target] is de bezoekersidentiteitskaart van uw bedrijf, zoals lidmaatschapsidentiteitskaart voor het loyaliteitsprogramma van uw bedrijf.

Wanneer een bezoeker zich aanmeldt bij de site van een bedrijf, maakt het bedrijf doorgaans een id die is gekoppeld aan de account, de loyaliteitskaart, het lidmaatschapsnummer of andere toepasselijke id&#39;s voor dat bedrijf.

Wanneer een bezoeker toegang krijgt tot een pagina waarop [!DNL Target] is ingeschakeld, wordt aan die bezoeker een [!DNL Target] PCID toegewezen. Als de bezoeker zich vervolgens aanmeldt en de implementatie de eigenschap `mbox3rdPartyId` aan [!DNL Target] doorgeeft, maakt [!DNL Target] verbinding tussen de `mbox3rdPartyId` van die bezoeker en de [!DNL Target] PCID.

De updates worden gesynchroniseerd met de profielopslag om de 5-10 minuten. Wanneer de sessie van de bezoeker is beëindigd, vervangen de samengevoegde gegevens de vorige gegevens die aan de `mbox3rdPartyId` zijn gekoppeld, waardoor een volledige record van de handelingen van die bezoeker wordt gemaakt. Als hetzelfde kenmerk voorkomt in beide id&#39;s, bijvoorbeeld de PCID heeft category=hats en de `mbox3rdPartyId` has category=skis, of als de bezoeker A zag voordat hij zich aanmeldt, maar ervaring B wordt opgeslagen in `mbox3rdPartyId` , wordt het kenmerk dat is opgeslagen in de `mbox3rdPartyId` , gebruikt om het kenmerk van de PCID te overschrijven. Als de bezoeker één activiteit of ervaring had voordat hij zich aanmeldt, maar een andere activiteit en ervaring worden na het aanmelden in `mbox3rdPartyId` opgeslagen, wordt die bezoeker in de `mbox3rdPartyId` -activiteit en -ervaring geplaatst.

| PCID (niet aangemeld) | mbox3rdPartyId (aangemeld) | Samengevoegd en opgeslagen naar mbox3rdPartyId |
|---|---|---|
| category=hats | category=skis | category=skis |
|   | store=94103 | store=94103 |
| Activiteit 1, Ervaring A | Activiteit 1, ervaring B | Activiteit 1, ervaring B |
| Activiteit 1 |  | Activiteit 1 |

Wanneer de bezoeker zich afmeldt, blijft het samengevoegde profiel behouden.

>[!NOTE]
>
>Als u onderscheid wilt maken tussen geverifieerde (aangemelde) gebruikers en niet-geverifieerde gebruikers, gebruikt u de [!DNL Adobe Experience Cloud Identity Service] (ECID) in plaats van de mbox3rdPartyID. Nadat een gebruiker met mbox3rdPartyID wordt geassocieerd, blijft het verbonden met de gebruiker zelfs na het ondertekenen uit.

>[!NOTE]
>
>De doelstellingen van [!DNL Adobe Analytics] worden niet bijgehouden in gevallen waarin de [!DNL Adobe Experience Cloud] ID (ECID) verandert (bijvoorbeeld de bezoeker wijzigt apparaten), ook al wordt het [!DNL Target] -profiel mogelijk samengevoegd op basis van de mbox3rdPartyId en heeft het nog steeds activiteitsgegevens. Voor bezoekers die met dezelfde ECID zijn geïdentificeerd (bezoekers die de pagina met hetzelfde apparaat openen), werkt [!DNL Analytics for Target] (A4T) naar behoren.

## Overwegingen {#considerations}

* Als uw pagina meerdere vakken bevat en slechts voor een deel `3rdPartyID` gebruikt, heeft [!DNL Target] geen apart bezoekersprofiel/aparte context voor elke bezoekersaanvraag. De context `3rdPartyID` heeft voorrang op de context PCID. Het is voldoende dat één box `3rdPartyId` doorgeeft voordat de context prioriteit krijgt boven de PCID.

  Stel dat een bezoeker een pagina opent voordat hij of zij zich aanmeldt en een ervaring ziet. De algemene mbox maakt geen gebruik van `3rdPartyID` . Na het aanmelden ziet de bezoeker een van de drie ervaringen met onderliggende postvakken, waarvan er sommige `3rdPartyID` gebruiken. De bezoeker bezoekt verschillende pagina&#39;s op de site en gebruikt vervolgens de knop Terug om terug te keren naar de hoofdpagina die wordt geopend voordat hij zich aanmeldt. Er wordt een andere ervaring weergegeven. In dit scenario ging de algemene mbox niet door `3rdPartyID` , maar een of meer onderliggende mbox wel. `3rdPartyID` heeft voorrang op PCID.

* U kunt de klant-id&#39;s van bezoekers naar [!DNL Target] sturen op twee manieren:

   1. Gebruik `mbox3rdPartyId`/`thirdPartyId`.

      * `mbox3rdPartyId` is de parameternaam wanneer u `targetPageParams` of `targetPageParamsAll` gebruikt
      * `thirdPartyId` is de parameternaam die u rechtstreeks instelt in de payload van de bezorgings-API.
      * U kunt slechts één waarde in deze parameter verzenden.

   1. Gebruik de functie `setCustomerId`/`customerIds` van ECID Service.

      * `setCustomerId` is een functie die u kunt gebruiken op client-side (browser) implementaties wanneer VisitorAPI.js beschikbaar is op de pagina.
      * `customerIds` is de parameternaam die wordt gebruikt wanneer u deze rechtstreeks instelt in de payload van de API voor aflevering en die gewoonlijk wordt uitgevoerd op implementaties van de server-side of IOT (internet van dingen).
      * In tegenstelling tot `mbox3rdPartyId`/ `thirdPartyId`, kunt u veelvoudige IDs als lijst in deze benadering verzenden, maar omdat [!DNL Target] slechts één enkele klant identiteitskaart per identiteitskaart TnT steunt, gebruikt het eerste identiteitskaart in de lijst met een bekende alias (alias die in de UI van Attributen van de Klant wordt gevormd).

  U kunt `mbox3rdPartyId` gebruiken/`thirdPartyId` als [!DNL Target] uw enige [!DNL Adobe Experience Cloud] oplossing is en u geen Klantattributen wilt gebruiken. In alle andere gevallen raden we u aan `setCustomerId`/`customerIds` te gebruiken voor het verzenden van uw klant-id&#39;s.

  >[!IMPORTANT]
  >
  > Als u beide hierboven vermelde benaderingen verwisselbaar gebruikt voor één bezoeker, kan dit leiden tot onjuiste profielsamenvoegingen van de niet-geverifieerde en geverifieerde [!DNL Target] -profielen.
  >
  >Adobe raadt niet aan om zowel `mbox3rdPartyId`/`thirdPartyId` als `setCustomerID`/`customerIds` samen te gebruiken.
  >
  >Als u beide benaderingen moet gebruiken onderling verwisselbaar, zorg ervoor dat eerste identiteitskaart in de lijst die door `setCustomerID` wordt gebruikt/ `customerIds` is wat door `thirdPartyId` wordt gebruikt/ `mbox3rdPartyId` en vice versa.

