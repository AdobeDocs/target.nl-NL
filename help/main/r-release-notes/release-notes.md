---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 6ecc59588b51da505b8f567a7e87ccef0f375477
workflow-type: tm+mt
source-wordcount: '1959'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Ontdek de nieuwste functies, verbeteringen en oplossingen in [!DNL Adobe Target] . Deze releaseopmerkingen hebben ook betrekking op updates van [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformcomponenten, indien van toepassing.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## Tijdgevoelige updates die u moet weten {#time-sensitive}

[!BADGE &#x200B; Belangrijk &#x200B;]{type=Informative}

Voor tijdgevoelige updates met betrekking tot [!DNL Adobe Target] en uw implementatie, [!DNL Adobe] verstrekt gedetailleerde versienota&#39;s en documentatie door [!UICONTROL Experience League]. Hier volgen enkele belangrijke punten die relevant zijn voor uw implementatie:

### Veroudering van interfaceversie [!DNL Target] in-/uitschakelen

+++Zie details
Het team van [!DNL Target] biedt een tijdelijke functie waarmee u met een schakelknop kunt schakelen tussen de bijgewerkte [!DNL Target] -gebruikersinterface en de oudere versie. Deze optie is beschikbaar slechts tijdens de definitieve fase van de rollout UI.

![ de versiesknevel van het Doel UI ](/help/main/r-release-notes/assets/toggle.png)

Zodra de rollout volledig is, zal de knevel worden verwijderd, en alle gebruikers overgang permanent aan bijgewerkte UI. [!DNL Adobe] raadt u aan vooruit te plannen, aangezien deze functie binnenkort wordt uitgeschakeld.

#### Tijdlijn van verdringing

Vanwege recente problemen die zijn vastgesteld, voornamelijk in verband met complexe klantaanpassingen, heeft het team van [!DNL Target] de tijdlijn voor de afschrijving aangepast:

* **17 Juni, 2025**: Alle organisaties IMS zijn toegelaten voor bijgewerkte [!DNL Target] UI, of voor specifieke gebruikers of organisatie-breed, beginnen het testen van de nieuwe ervaring.

* **Juni 30, 2025**: [ bijgewerkte  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md) werd de standaardervaring voor alle IMS Orgs die de UI versieknevel hebben toegelaten.

   * Klanten die momenteel de oudere UI zien, door gebrek, zien nu bijgewerkte UI bij login.
   * De UI versiesknevel blijft beschikbaar door eind Juli, die gebruikers toestaat om terug te schakelen indien nodig.

  >[!IMPORTANT]
  >
  > [!DNL Adobe] raadt u ten zeerste aan de bijgewerkte gebruikersinterface van [!DNL Target] te gebruiken. De schakelaar terug naar erfenis UI slechts als een blokkeerkwestie voorkomt, toe te schrijven aan [ beperkingen van het knevel schakelaargedrag ](#limitations).

* **15 juli tot 30 juli, 2025**: De de versiesknevel van UI zal permanent in fasen onbruikbaar worden gemaakt. Betrokken IMS-instellingen kunnen niet meer terugkeren naar de oudere gebruikersinterface.

   * Uitzonderingen worden per geval beoordeeld.
   * Vertragingen bij de tijdelijke verwijdering van de knevel worden slechts kort toegestaan (een paar dagen), terwijl problemen met blokkeringen worden opgelost.

De Zorg van de Klant van Adobe van het contact [ met om het even welke zorgen of als u kwesties tijdens deze overgang verwacht.](/help/main/cmp-resources-and-contact-information.md#/help/main/cmp-resources-and-contact-information.md)

#### Beperkingen van het gedrag van de UI-schakelfunctie {#limitations}

De volgende informatie beschrijft de beperkingen die u bewust zou moeten zijn wanneer het kiezen om de versiesknevel te gebruiken:

* **Zichtbaarheid van nieuwe activiteiten**: De activiteiten die in bijgewerkte UI worden gecreeerd zullen niet zichtbaar zijn als u terug naar erfenisUI schakelt.
* **het uitgeven van bestaande activiteiten**: De veranderingen die aan bestaande activiteiten (oorspronkelijk in erfenis UI) worden aangebracht terwijl het gebruiken van bijgewerkte UI worden gepubliceerd aan uw website. Nochtans, zijn deze updates niet zichtbaar in erfenis UI als u terug schakelt; slechts de laatste die updates van erfenisUI worden gemaakt verschijnen daar.
* **Consistentie van activiteitendetails**: De meest recente veranderingen, ongeacht welke UI u gebruikt, worden weerspiegeld op uw levende website. In de oudere gebruikersinterface worden echter alleen de meest recente wijzigingen weergegeven die in die versie zijn aangebracht. Deze situatie zou verwarring kunnen veroorzaken als de activiteiten die in bijgewerkte UI worden uitgegeven verschillend kijken dan wat u in erfenisUI ziet.

#### Meer bronnen voor meer informatie over de bijgewerkte gebruikersinterface

* [[!DNL Target]  UI update FAQs ](/help/main/c-intro/updated-ui-faq.md): Deze veelgestelde vragen behandelt gemeenschappelijke vragen over nieuwe [!DNL Target] UI en [!UICONTROL Visual Experience Composer] (VEC), met inbegrip van navigatieveranderingen, eigenschapplaatsen, en de veroudering van de tijdelijke UI versiesknevel. Of u nu een markeerteken, ontwikkelaar of beheerder bent, deze veelgestelde vragen helpen u een vloeiende overgang te maken en de bijgewerkte gebruikersinterface optimaal te benutten.
* [[!DNL Target Standard/Premium]  25.2.1 (17 februari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Activities], [!UICONTROL Recommendations], en [!UICONTROL Visual Experience Composer] (VEC).
* [[!DNL Target Standard/Premium]  25.1.1 (9 Januari, 2025) versienota&#39;s ](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-1): Verstrekt een samenvatting van de belangrijkste veranderingen UI in [!DNL Target] voor [!UICONTROL Offers Library].
* [ begrijp  [!DNL Target]  UI ](/help/main/c-intro/understand-the-target-ui.md): Verstrekt een kort overzicht om u te helpen vertrouwd worden met [!DNL Target] en verleent verbindingen voor meer diepgaande informatie en geleidelijke instructies.
* [[!UICONTROL Visual Experience Composer] changes ](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md) : In de release [!DNL Adobe Target Standard/Premium] 25.2.1 (17 februari 2015) wordt een bijgewerkte versie van [!UICONTROL Visual Experience Composer] (VEC) geïntroduceerd. Dit artikel verklaart de verschillen tussen de erfenis en bijgewerkte versies van VEC.
* [[!UICONTROL Visual Experience Composer] opties ](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md): Dit artikel verklaart bijgewerkte UI VEC en zijn opties.

+++

## [!DNL Target Standard/Premium] 25.8.1 (7 augustus 2025)

Deze release bevat de volgende verbeteringen en oplossingen:

**Activiteiten**

+++Zie details
* Oplossing voor verschillende problemen met de bijgewerkte interface, waaronder fouten bij het verwijderen van paginatypen als gevolg van de afstand in invoerwaarden, onbetrouwbare kopiëren van activiteiten tussen werkruimten en slecht functionerende regels voor het leveren van pagina&#39;s in QA-omgevingen. (TGT-52703)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] waar gebruikers met de [!UICONTROL Editor] -rol live activiteiten konden openen en proberen te bewerken. Dit probleem moet worden beperkt. De activiteitenlijst en overzichtsschermen onjuist weergegeven bewerkingsopties voor live activiteiten, wat tot mogelijk onbedoelde wijzigingen leidt. (TGT-53055)
* Probleem verholpen waarbij het selecteren van de operatoren &quot;value is present&quot; of &quot;value is not present&quot; in de gebruikersinterface van [!UICONTROL Advanced Search] ertoe leidde dat gebruikers een operand wilden invoeren die niet vereist was voor deze voorwaarden. (TGT-51961)
* Probleem verholpen in de bijgewerkte gebruikersinterface waarbij pogingen om activiteiten van de werkruimte van de testfase naar de productiewerkruimte consistent te kopiëren, zelfs in sandboxomgevingen, zijn mislukt. De klanten ontmoetten diverse foutenmeldingen, met inbegrip van &quot;Anoniem publiek dat reeds door de activiteit&quot;en &quot;Ongeldige publiek identiteitskaart,&quot;ondanks het gebruiken van geldige configuraties en het hebben van aangewezen werkruimtemachtigingen wordt gebruikt. (TGT-52394)

+++

**Fragmenten van de Ervaring (XFs)**

+++Zie details
* Probleem verholpen waarbij XF-inhoud (Experience Fragment) niet wordt gerenderd in de voorvertoning [!UICONTROL Visual Experience Composer] (VEC), ondanks het correct werken in de levering van inhoud. (TGT-53318)

+++

**Localization**

+++Zie details
* Probleem met lokalisatie verholpen waarbij de knop &quot;Promotie toevoegen&quot; in de sectie &quot;Promoties&quot; niet gelokaliseerd leek voor meerdere taalomgevingen in de QA-gebruiker. (TGT-53263)

+++

**Aanbiedingen**

+++Zie details
* Probleem verholpen waarbij tijdens het bewerken van een bestaand HTML-aanbod via Visual Experience Composer (VEC) alle wijzigingen werden verwijderd uit de levering van inhoud. De wijzigingen worden grijs weergegeven op het tabblad Wijzigen en worden niet weerspiegeld in QA-voorvertoningen, ondanks dat ze correct worden toegepast in de oudere gebruikersinterface. (TGT-52863)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] , waarbij HTML wijzigingen aanbiedt die in [!UICONTROL Visual Experience Composer] (VEC) zijn aangebracht, maar niet meer voorkomen nadat u van de tab [!UICONTROL Targeting] terug naar [!UICONTROL Experiences] bent genavigeerd. (TGT-52874)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] waarbij het invoegen van één HTML-aanbieding voor en een ander na dezelfde kiezer tot onjuiste locatiegeneratie leidde. Wanneer klanten van het tabblad [!UICONTROL Targeting] naar het tabblad [!UICONTROL Experience] zijn teruggekeerd, is slechts één kiezer behouden gebleven, wat heeft geleid tot verloren wijzigingen en een verbroken levering van inhoud. Dit gedrag verschilde van erfenis UI, die correct beide wijzigingen met verschillende plaatsherkenningstekens handhaaft. (TGT-52891)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] , waarbij het klikken op een toegevoegde aanbieding in de [!UICONTROL Modifications] rail ertoe leidde dat het rechterdeelvenster [!UICONTROL Configuration] af en toe werd weergegeven en verdwijnt, waardoor interactie met de aanbiedingsinstellingen moeilijk werd. (TGT-53288)
* Probleem verholpen waarbij HTML-aanbiedingen die binnen een activiteit aan publiekspecifieke variaties zijn toegevoegd, niet consistent werden opgeslagen of in de wijzigingssectie werden weergegeven. Nadat tijdens het bewerken is geschakeld tussen het publiek, zijn eerder toegepaste aanbiedingen soms verdwenen of zijn ze niet weergegeven, waardoor de validatie wordt verstoord en de gereedheid van de activiteit wordt vertraagd. (TGT-53440)
* Probleem verholpen waarbij door het kopiëren van een activiteit die aanbiedingen bevatte, dubbele aanbiedingen werden gemaakt in de nieuwe activiteit. Dit gedrag veroorzaakte onnodige verwarring en verwarring, vooral wanneer het bewegen van activiteiten tussen werkruimten. De oplossing zorgt ervoor dat [!DNL Target] -aanbiedingen nu correct en zonder duplicatie naar de doelwerkruimte worden gekopieerd, zodat het activiteitsbeheer wordt gestroomlijnd en de efficiëntie van de workflow wordt verbeterd. (TGT-53454)

+++

**Enige Toepassingen van de Pagina (SPAs)**

+++Zie details
* Oplossing voor een probleem in de bijgewerkte VEC dat ervoor zorgde dat klanten geen wijzigingen konden toepassen op [!UICONTROL Single Page Application] (SPA)-weergaven. Terwijl de activiteiten die in oude UI werden gecreeerd mening-specifiek het richten steunden, nieuwe UI niet om te ontdekken of toe te staan uitgeeft aan die meningen, met de mening-omschakeling controles die gehandicapt lijken. (TGT-52556)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* Correctie van een probleem waarbij wijzigingen in ervaringen binnen [!UICONTROL Visual Experience Composer] niet zichtbaar waren of inconsistent optraden in de gebruikersinterface. (TGT-TGT-53381)
* Probleem verholpen in de bijgewerkte VEC waarbij de sectie [!UICONTROL Manage Content] geen alternatieve tekst kon weergeven voor ervaringsminiaturen. Hierdoor konden gebruikers documenten moeilijk herkennen, vooral als bestandsnamen lang of ingekort waren. (TGT-52291)
* Probleem verholpen waarbij klanten onjuiste validatiefouten tegenkwamen bij het configureren van [!UICONTROL page delivery] -regels in VEC-activiteiten. Operatoren als &quot;is gelijk aan een van de items&quot; en &quot;is niet gelijk aan een van de items&quot; die worden geactiveerd &quot;Ongeldige invoer voor het operatortype&quot; bij het invoeren van tekstwaarden, ook al moet tekst worden ondersteund. (TGT-52629)
* Oplossing voor verschillende problemen die een inconsistent gedrag veroorzaakten in het deelvenster [!UICONTROL Modifications] van de bijgewerkte gebruikersinterface bij het selecteren van aanbiedingen met de knop &quot;Een aanbieding selecteren&quot;. In plaats van de bestaande aanbieding te vervangen, heeft de gebruikersinterface een duplicaat toegevoegd en geprobeerd om met een van beide aanbiedingen te communiceren, heeft dit geleid tot consolefouten zoals `selectorNotFound` . Bovendien wordt in sommige aanbiedingen de knop &quot;Een aanbieding selecteren&quot; niet weergegeven en worden alleen bewerkbare eigenschappen weergegeven. (TGT-53321)
* Probleem verholpen in de bijgewerkte gebruikersinterface van [!DNL Target] waarbij wijzigingen in de HTML-code die tijdens het instellen van de activiteit zijn aangebracht, niet meer voorkomen op variatiepagina&#39;s, ook al zijn deze op de juiste wijze opgeslagen voor controlegroepen. Ondanks meerdere pogingen en het opnieuw maken van tests zonder paginagroepen, konden de variatiepagina&#39;s voortdurend geen wijzigingen behouden, wat invloed had op de levering van inhoud en de validatie van de kwaliteitscontrole. (TGT-53436)
* Probleem verholpen in de bijgewerkte VEC waarbij de operator &quot;equals of&quot; in de leveringsregels voor pagina&#39;s geen invoerwaarden accepteerde. Wanneer het vormen van klantenparameters over alle dozen, resulteerde het selecteren van deze exploitant in een &quot;Ongeldige Input&quot;fout, verhinderend regelverwezenlijking. (TGT-52623)

+++

**Werkruimten**

+++Zie details
* Verbeterde workflow bij het kopiëren van activiteiten tussen werkruimten. De activiteiten van het exemplaar tussen werkruimten leidden eerder tot synchronisatiefouten toe te schrijven aan ontbrekend publiek en niet toegewezen eigenschappen. Deze update introduceert een slimmere, intuïtievere workflow die ervoor zorgt dat gekopieerde activiteiten correct zijn geconfigureerd en klaar zijn voor publicatie. (TGT-47094)
* Probleem verholpen waarbij klanten geen activiteiten konden kopiëren tussen werkruimten vanwege een fout in de mutatie `copyActivityBatchOperations` . Pogingen om activiteiten te dupliceren resulteerden in een serverfout (500) en een lege antwoordlading. (TGT-52405)
* Probleem verholpen waarbij activiteiten niet konden worden gesynchroniseerd wanneer aanbiedingen waarnaar in de configuratie wordt verwezen niet toegankelijk waren binnen de geselecteerde werkruimte. Hierdoor zijn publicatiefouten en linkactiviteiten mislukt. (TGT-52535)
* Meerdere problemen verholpen tijdens het kopiëren van activiteiten tussen werkruimten in de bijgewerkte gebruikersinterface van [!DNL Target] . De klanten ontmoetten fouten met betrekking tot publiekstoegang, met name met levende activiteiten, en onjuiste voorrechtbevestiging, zelfs wanneer de gebruiker &quot;[!UICONTROL Approver]&quot;rollen in zowel bron als bestemmingswerkruimten had. (TGT-53002)
* Probleem verholpen in de bijgewerkte gebruikersinterface waarbij het kopiëren van activiteiten binnen dezelfde werkruimte nodeloos gekoppelde aanbiedingen en soorten publiek dupliceerde. (TGT-53457)
* Probleem verholpen waarbij ad-hocpubliek (anoniem) niet correct werd gekopieerd tussen niet-standaardwerkruimten of van niet-standaard naar standaardwerkruimten. Terwijl de vroegere updates correcte duplicatie voor gebrek-aan-niet gebrek en zelfde-werkruimtescenario&#39;s zorgden, concentreerde deze verbetering zich op het bewaren van gecombineerde publieksconfiguraties die veelvoudige werkruimten overspannen. Deze oplossing zorgt voor consistent gedrag van het publiek en een nauwkeurige afstemming op alle overgangen in de werkruimte. (TGT-53268)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK ](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=en) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [ Veranderingen van de Documentatie ](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [ de nota&#39;s van de Versie voor vorige versies ](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [ de Nota&#39;s van de Versie van Adobe Experience Cloud ](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [ de Prioritaire Update van het Product van Adobe ](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [ de Nota&#39;s van de Versie van het Doel - preRelease ](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
