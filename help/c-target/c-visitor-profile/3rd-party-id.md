---
keywords: mbox;mbox3rdPartyId;profielsynchronisatie;profielsynchronisatie;PCID
description: Leer hoe u mbox3rdPartyId gebruikt. Dit is de bezoekersidentiteitskaart van uw organisatie, zoals lidmaatschap identiteitskaart of het loyaliteitsprogramma van uw organisatie.
title: Hoe gebruik ik Real-Time Profile Syncing voor mbox3rdPartyId?
feature: Soorten publiek
exl-id: ed409225-fa35-49da-87d1-1770221f2ae0
source-git-commit: c19163020cdcb41a17ea6b65b5b500fadc9c7512
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Real-time profielsynchronisatie voor mbox3rdPartyId

De mbox3rdPartyId in [!DNL Adobe Target] is de bezoekersidentiteitskaart van uw bedrijf, zoals lidmaatschapsidentiteitskaart voor het loyaliteitsprogramma van uw bedrijf.

Wanneer een bezoeker zich aanmeldt bij de site van een bedrijf, maakt het bedrijf doorgaans een id die is gekoppeld aan de account, de loyaliteitskaart, het lidmaatschapsnummer of andere toepasselijke id&#39;s voor dat bedrijf.

Wanneer een bezoeker tot een pagina toegang heeft waarop [!DNL Target] wordt toegelaten, wordt die bezoeker toegewezen een [!DNL Target] PCID. Als de bezoeker zich dan binnen aanmeldt, en de implementatie mbox3rdPartyId tot [!DNL Target] overgaat, [!DNL Target] verbindt mbox3rdPartyId van die bezoeker met [!DNL Target] PCID.

Om de drie tot vijf minuten worden updates gesynchroniseerd met de database. Wanneer de bezoeker zich afmeldt, vervangen de samengevoegde gegevens de vorige gegevens verbonden aan mbox3rdPartyId, die tot een volledig verslag van de acties van die bezoeker leiden. Als het zelfde attribuut in beide IDs-bijvoorbeeld bestaat, heeft PCID category=hats en mbox3rdPartyId heeft category=skis, of als de bezoeker A vóór het programma opent zag, maar ervaring B wordt opgeslagen in mbox3rdPartyId-het attribuut dat in mbox3rdPartyId wordt opgeslagen beschrijft de attributen van PCID. Als de bezoeker in één activiteit of ervaring alvorens het programma te openen was, maar een verschillende activiteit en een ervaring worden opgeslagen in mbox3rdPartyId, nadat het programma openen die bezoeker in de mbox3rdPartyId activiteit en ervaring wordt geplaatst.

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

Als uw pagina verscheidene dozen bevat en slechts sommige gebruiken 3rdPartyID, [!DNL Target] heeft geen afzonderlijk bezoekersprofiel/context voor elke bezoekersverzoek. De context van de derde partijID heeft voorrang op de context PCID. Het is voldoende dat één box de voorkeur geeft aan de context van de derde partijId boven de PCID.

Stel dat een bezoeker een pagina opent voordat hij of zij zich aanmeldt en een ervaring ziet. De globale box gebruikt geen 3rdPartyID. Na het aanmelden ziet de bezoeker een van de drie ervaringen met onderliggende postvakken, waarvan er sommige gebruikmaken van de 3rdPartyID. De bezoeker bezoekt verschillende pagina&#39;s op de site en gebruikt vervolgens de knop Terug om terug te keren naar de hoofdpagina die wordt geopend voordat hij zich aanmeldt. Er wordt een andere ervaring weergegeven. In dit scenario, ging globale mbox 3rdID niet over, maar één of meerdere kinddozen deden. De prioriteit voor de derde partijID was groter dan PCID.
