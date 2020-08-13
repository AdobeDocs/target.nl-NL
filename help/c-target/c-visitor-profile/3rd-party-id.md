---
keywords: mbox;mbox3rdPartyId;profile syncing;profile synch;PCID
description: 'Informatie over real-time profiel '
title: Real-time profielsynchronisatie voor mbox3rdPartyId in Adobe Target
feature: visitor profiles
topic: Standard
uuid: a88353d1-36e8-48b2-9b5e-71ed437c5b99
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---


# Real-time profielsynchronisatie voor mbox3rdPartyId{#real-time-profile-syncing-for-mbox-rdpartyid}

De mbox3rdPartyId is de bezoeker-id van uw bedrijf, zoals de lidmaatschap-id voor het loyaliteitsprogramma van uw bedrijf.

Wanneer een bezoeker zich aanmeldt bij de site van een bedrijf, maakt het bedrijf doorgaans een id die is gekoppeld aan de account, de loyaliteitskaart, het lidmaatschapsnummer of andere toepasselijke id&#39;s voor dat bedrijf.

Wanneer een bezoeker een pagina opent waarop [!DNL Target] wordt toegelaten, wordt die bezoeker toegewezen een [!DNL Target] PCID. Als de bezoeker zich dan aanmeldt en de implementatie de mbox3rdPartyId doorgeeft aan [!DNL Target], [!DNL Target] [!DNL Target] verbindt mbox3rdPartyId van die bezoeker met PCID.

Om de drie tot vijf minuten worden updates gesynchroniseerd met de database. Wanneer de bezoeker zich afmeldt, vervangen de samengevoegde gegevens de vorige gegevens verbonden aan mbox3rdPartyId, die tot een vollediger verslag van de acties van die bezoeker leiden. Als het zelfde attribuut in beide IDs-bijvoorbeeld bestaat, heeft PCID category=hats en mbox3rdPartyId heeft category=skis, of als de bezoeker A vóór het programma opent zag, maar ervaring B wordt opgeslagen in mbox3rdPartyId-het attribuut dat in mbox3rdPartyId wordt opgeslagen beschrijft de attributen van PCID. Als de bezoeker in één activiteit of ervaring alvorens het programma te openen was, maar een verschillende activiteit en een ervaring worden opgeslagen in mbox3rdPartyId, nadat het programma openen die bezoeker in de mbox3rdPartyId activiteit en ervaring wordt geplaatst.

| PCID (niet aangemeld) | mbox3rdPartyId (aangemeld) | Samengevoegd en opgeslagen naar mbox3rdPartyId |
|---|---|---|
| category=hats | category=skis | category=skis |
|  | store=94103 | store=94103 |
| Activiteit 1, Ervaring A | Activiteit 1, ervaring B | Activiteit 1, ervaring B |
| Activiteit 1 |  | Activiteit 1 |

Wanneer de bezoeker zich afmeldt, blijft het samengevoegde profiel behouden.

>[!NOTE]
>
>Als u onderscheid wilt maken tussen geverifieerde (aangemelde) gebruikers en niet-geverifieerde gebruikers, gebruikt u de Adobe Experience Cloud Identity Service (ECID) in plaats van mbox3rdPartyID. Nadat een gebruiker met mbox3rdPartyID wordt geassocieerd, blijft het verbonden met de gebruiker zelfs na het ondertekenen uit.

>[!NOTE]
>
>[!DNL Adobe Analytics] De doelen worden niet bijgehouden in gevallen waarin de [!DNL Adobe Experience Cloud] id (EDID) verandert (bijvoorbeeld wanneer de bezoeker apparaten wijzigt), ook al wordt het [!DNL Target] profiel mogelijk samengevoegd op basis van de mbox3rdPartyId en beschikt het nog steeds over informatie over de activiteit. Voor bezoekers die met dezelfde EDID zijn geïdentificeerd (bezoekers die de pagina met hetzelfde apparaat openen), [!DNL Analytics for Target] (A4T) zou moeten werken zoals verwacht.

## Overwegingen {#considerations}

Als uw pagina verscheidene dozen bevat en slechts sommige gebruiken 3rdID, heeft het Doel geen afzonderlijk bezoekersprofiel/context voor elke bezoekersverzoek. De context van de derde partijID heeft voorrang op de context PCID. Het is voldoende dat één box de voorkeur geeft aan de context van de derde partijId boven de PCID.

Stel dat een bezoeker een pagina opent voordat hij zich aanmeldt en een ervaring ziet. De globale box gebruikt geen 3rdPartyID. Na het aanmelden ziet de bezoeker een van de drie ervaringen met onderliggende postvakken, waarvan er sommige gebruikmaken van de 3rdPartyID. De bezoeker bezoekt verschillende pagina&#39;s op de site en gebruikt vervolgens de knop Terug om terug te keren naar de hoofdpagina die wordt geopend voordat hij zich aanmeldt. Er wordt een andere ervaring weergegeven. In dit scenario, ging globale mbox 3rdID niet over, maar één of meerdere kinddozen deden. De prioriteit voor de derde partijID was groter dan PCID.
