---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 29ddf23b41531e5fab80fe7d0f6bc913e778d839
workflow-type: tm+mt
source-wordcount: '1670'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Ontdek de nieuwste functies, verbeteringen en oplossingen in [!DNL Adobe Target] . Deze releaseopmerkingen hebben ook betrekking op updates van [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformcomponenten, indien van toepassing.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## Tijdgevoelige updates die u moet weten {#time-sensitive}

[!BADGE  Belangrijk ]{type=Informative}

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

## [!DNL Target Standard/Premium] 25.9.1 (5 september 2025)

Deze release bevat de volgende updates en oplossingen:

**[!UICONTROL Experience Fragments]**

+++Zie details
* **Verbeterde gebruikerstoewijzing voor [!UICONTROL AEM Experience Fragment] aanbiedingen.** Oplossing voor een probleem in VEC waarbij het veld [!UICONTROL Last updated] voor [!UICONTROL AEM Experience Fragment] (XF) een code-id onjuist weergeeft in plaats van de gebruikersnaam. Deze discrepantie kwam tijdens aanbiedingsselectie in bijgewerkte UI voor, die tot inconsistentie met de erfenis UI en aanbiedingen van HTML leidt, die correct de naam van de laatste redacteur toonde. Deze correctie zorgt voor consistente toewijzing van gebruikers over aanbiedingstypen, waardoor de transparantie en de uitlijning met het verwachte gedrag worden verbeterd. (TGT-52880 &amp; TGT-52898)

+++

**Offer Decisioning**

+++Zie details
* **de fout van het Besluit van de Aanbieding wordt opgelost voor de aanbiedingen van ODE.** Oplossing voor een probleem waarbij ODE-aanbiedingen (Offer Decision Engine) die via [!DNL Target] zijn geïnjecteerd, een fout van 400 hebben geretourneerd omdat metagegevens over indelingen ontbreken. Het foutbericht geeft aan dat het MIME-type null is, waardoor succesvolle verwerking van biedingsbesluiten wordt voorkomen. Deze oplossing zorgt voor een juiste verwerking van de metagegevens van de aanbieding, herstelt functionaliteit voor levering van gepersonaliseerde inhoud en maakt het mogelijk dat marketingcampagnes zonder onderbreking worden uitgevoerd. (TGT-53635)
* **ODS biedt het teruggeven probleem opgelost aan.** Het volgende probleem is opgelost: [!DNL Offer Decision Service] (ODS)-aanbiedingen die via [!DNL Adobe Journey Optimizer] (AJO) zijn gemaakt, worden niet gerenderd wanneer activiteiten met behulp van de VEC in de bijgewerkte gebruikersinterface zijn gemaakt. Dezelfde configuratie werkte correct in de oudere gebruikersinterface, wat tot verwarring en een geblokkeerde uitvoering van de campagne leidde. Deze oplossing zorgt voor een consistente levering van de aanbieding in beide gebruikersinterfaceversies en herstelt het verwachte gedrag voor AJO-gedreven personalisatie.

+++

**Rapporten**

+++Zie details
* **optie van de Download wordt hersteld in rapportensectie van de bijgewerkte overzichtsUI van Rapporten.** Oplossing voor een probleem in de nieuwe interface voor het overzicht waarin de knop [!UICONTROL Download] ontbreekt in de sectie Rapporten, zodat gebruikers geen scores voor kenmerkbelang kunnen exporteren. Deze update herstelt de volledige exportfunctionaliteit, waardoor gestroomlijnde toegang tot downloadbare gegevens voor analyse en rapportage mogelijk is. (TGT-53222)
* **[!UICONTROL Download full CSV report]wordt hersteld in de weergave [!UICONTROL Important attributes] .** Oplossing voor een probleem in de bijgewerkte interface voor het maken van activiteiten waarbij de knop [!UICONTROL Download full CSV report] ontbreekt in de sectie [!UICONTROL Important Attributes] in de rapportweergave. Met deze oplossing herstelt u de toegang tot downloadbare inzichten en zorgt u voor consistente functionaliteit voor zowel de bijgewerkte als de verouderde gebruikersinterface. (TGT-53238)
* **Opgeloste kwesties UI die [!UICONTROL Auto Target] rapportering in bijgewerkte overzichtsUI beïnvloeden.** Oplossing voor meerdere problemen met de gebruikersinterface in de bijgewerkte interface die gevolgen hebben voor de [!UICONTROL Auto Target] -rapportage. Deze correcties zijn onder andere:

   * Ontbrekende cijfers over lift en betrouwbaarheid in samenvattingsrapporten
   * Onjuiste kleurindicator voor het selectievakje &quot;Modellen gebouwd&quot;
   * Niet-functioneel grafiekrapport ondanks verschillen in gegevens [!DNL Analytics]
   * Ontbrekende downloadkoppeling voor [!UICONTROL Automated Segments] - en [!UICONTROL Important Attributes] -rapporten
   * Verbroken [!UICONTROL Automated Segments] rapportweergave

  Met deze correcties wordt het verwachte rapportgedrag hersteld en wordt de zichtbaarheid van [!UICONTROL Auto Target] -prestaties in de bijgewerkte gebruikersinterface verbeterd. (TGT-53484)

+++

**[!UICONTROL Visual Experience Composer]**

+++Zie details
* **Bevestiging van de Vorm die voor de voorwaarden van de parameteraanwezigheid in bijgewerkte UI wordt verbeterd.** Oplossing voor een probleem in bijgewerkte UI waar het selecteren van &quot; [!UICONTROL Custom mbox parameter value is present]&quot;of &quot;[!UICONTROL Parameter is present]&quot;klanten verkeerd vereiste om een waarde in te gaan. Dit gedrag was in strijd met de bedoelde logica, die eenvoudig controleert of een parameter bestaat, ongeacht de waarde ervan. Met deze correctie wordt formuliervalidatie uitgelijnd op het verwachte gedrag, waardoor de activiteiten vloeiender kunnen worden ingesteld en de bijgewerkte gebruikersinterface volledig kan worden toegepast. (TGT-53638)
* **logica van de Vorm die voor de regels van de parameteraanwezigheid in paginalevering wordt verbeterd.&quot;** Oplossing een kwestie in bijgewerkte UI waar het selecteren van de regels van de paginalevering zoals &quot;[!UICONTROL Parameter is present],&quot;[!UICONTROL Parameter is not present],&quot;[!UICONTROL Parameter value is present],&quot; of &quot;[!UICONTROL Parameter value is not present]&quot;verkeerd vereiste gebruikers om een extra parameterwaarde in te gaan. Dit gedrag was inconsistent met de oudere UI en drukte de voorgenomen logica tegen om parameteraanwezigheid te ontdekken zonder een waarde te specificeren. Deze moeilijke situatie herstelt het verwachte gedrag van de regelconfiguratie, stroomlijnt activiteitenopstelling en verbetert bruikbaarheid. (TGT-53640)
* **de logica van de Bevestiging verbeterde voor multi-page regelbouwer in bijgewerkte UI.** Meerdere validatieproblemen in de builder van meerdere pagina&#39;s in de bijgewerkte gebruikersinterface opgelost. Deze correcties zijn onder andere:

   * Het voorkomen van het maken van regels wanneer de parameter mbox leeg is
   * De juiste foutberichten voor ongeldige regelstatussen weergeven
   * Validatielogica corrigeren voor unaire operatoren en operatoren op basis van parameters die geen operandwaarden vereisen
   * Hash-fragmentregels inschakelen met unaire operatoren door functie voor opslaan te herstellen

  Deze updates verzekeren nauwkeurige regelconfiguratie en verbeteren bruikbaarheid over de complexe scenario&#39;s van de paginalevering. (TGT-53722)
* **het anders noemen van plaats probleem dat in A/B en activiteiten MVT wordt opgelost.** Oplossing voor een fout in de bijgewerkte gebruikersinterface waarbij de naam van een locatie in een [!UICONTROL A/B Test] - of [!UICONTROL Multivariate Test] -activiteit (MVT) niet werd gewijzigd nadat was genavigeerd tussen de lijst met locaties, de locatie van de doellocatie en de locatie van de gebruiker. Deze update zorgt ervoor dat wijzigingen in de locatienaam worden opgeslagen en consistent worden weerspiegeld in de gehele werkstroom. (TGT-52367)
* **de naampersistentie van de Plaats die voor activiteiten MVT en AP in bijgewerkte UI wordt bevestigd.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij locatienamen die werden bewerkt in [!UICONTROL Multivariate Test] (MVT)- en [!UICONTROL Automated Personalization] (AP)-activiteiten niet correct werden opgeslagen. Nadat de naam van een locatie was gewijzigd, werd door navigatie tussen tabbladen, zoals [!UICONTROL Targeting] en [!UICONTROL Experiences] , de vorige status van de namen hersteld. Deze moeilijke situatie verzekert verenigbare plaats het noemen over lusjes en verbetert betrouwbaarheid tijdens activiteitenopstelling. (TGT-52927)
* **het etiketteren van de Plaats die in het beheer ervaringspaneel voor MVT activiteiten wordt verbeterd.** Oplossing voor een probleem in de bijgewerkte gebruikersinterface waarbij in het deelvenster [!UICONTROL Manage Experiences] in [!UICONTROL Multivariate Test] -activiteiten (MVT) inconsistente plaatsnummering werd weergegeven. Deze correctie zorgt ervoor dat locatielabels opeenvolgend zijn en correct zijn uitgelijnd met door de gebruiker gedefinieerde wijzigingen, waardoor de helderheid en bruikbaarheid tijdens het instellen van de ervaring worden verbeterd. (TGT-52929)

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
