---
keywords: releaseopmerkingen;nieuwe functies;releases;updates;update;release;verbetering;verbeteringen;correcties;foutoplossingen;updates;huidige updates
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
landing-page-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Adobe Target].
short-description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de huidige versie van  [!DNL Target].
title: Wat is inbegrepen in de huidige Versie?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7d73870275c266055825c2fce90489ef82825fca
workflow-type: tm+mt
source-wordcount: '1700'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (huidig)

Ontdek de nieuwste functies, verbeteringen en oplossingen in [!DNL Adobe Target] . Deze releaseopmerkingen hebben ook betrekking op updates van [!DNL Target] API&#39;s, SDK&#39;s, de [!DNL Adobe Experience Platform Web SDK] , at.js en andere platformcomponenten, indien van toepassing.

(De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .)

## Tijdgevoelige updates die u moet weten {#time-sensitive}

[!BADGE &#x200B; Belangrijk &#x200B;]{type=Informative}

Voor tijdgevoelige updates die betrekking hebben op [!DNL Adobe Target] en uw implementatie, verschaft [!DNL Adobe] gedetailleerde opmerkingen en documentatie bij de release via [!UICONTROL Experience League] . Hier volgen enkele belangrijke punten die relevant zijn voor uw implementatie:

### Veroudering van interfaceversie [!DNL Target] in-/uitschakelen

Voor meer informatie, zie [[!DNL Target]  UI update FAQs &#x200B;](/help/main/c-intro/updated-ui-faq.md).

## [!DNL Target Standard/Premium] 25.10.1 (22 oktober 2025)

Deze release bevat de volgende updates en oplossingen:

**Activiteiten**

+++ Zie details
* **Oplossing een bruikbaarheidskwestie in bijgewerkte UI**. [!UICONTROL Observers] kan nu een voorbeeld van activiteiten weergeven met de optie [!UICONTROL View Activity] , net als in de oudere gebruikersinterface. (TGT-51741)
* **[!UICONTROL Observer]-gebruikers kunnen nu de inhoud van de activiteit weergeven in de bijgewerkte gebruikersinterface.** De zichtbaarheid van gebruikers met een observerrol in de bijgewerkte gebruikersinterface voor activiteiten is hersteld. Eerder konden waarnemers geen wijzigingen, aanbiedingen en wijzigingen in de inhoud weergeven, functionaliteit die beschikbaar was in de oudere gebruikersinterface. (TGT-53785)
* **[!UICONTROL Approver]-gebruikers kunnen nu activiteitendoelen bewerken zonder fout met bevoegdheden in de editor.** Oplossing voor een machtigingsprobleem in de interface Activiteit creëren die gebruikers op niveau van fiatteurs verhinderde wijzigingen in geavanceerde doelinstellingen op te slaan. Betrokken gebruikers hebben een `403 Forbidden.Resource` -fout ontvangen waarvoor editorrechten vereist zijn, ondanks dat ze voldoende toegangsrechten hebben. (TGT-53819)

+++

**Soorten publiek**

+++Zie details
* **de Selectie van het multi-publiek die in &quot;Deze activiteit slechts&quot;wordt teruggezet het Melden.** Oplossing voor een probleem in de interface Activiteit maken dat ervoor zorgde dat gebruikers niet meerdere soorten publiek konden selecteren onder de sectie [!UICONTROL This activity only] in [!UICONTROL Goals & Settings] . (TGT-53283)
* **op publiek-gebaseerde rapporteringsgrafieken tonen nu correct omzettingsgegevens.** Oplossing voor een probleem op het tabblad [!UICONTROL Reports] dat ertoe heeft geleid dat grafieken zijn mislukt bij het selecteren van niet-standaardsoorten publiek. Hoewel gegevens en betrouwbaarheidsmetriek beschikbaar waren, toonde de visuele grafiek slechts een stevige lijn, die analyse bemoeilijkt. (TGT-53769)
* **UI wijst nu duidelijk op uitgesloten publieksregels. [!UICONTROL Targeting]** Oplossing voor een probleem in de sectie [!UICONTROL Targeting] van de sectie Activity Create UI dat ertoe leidde dat de publieksregels die op [!UICONTROL Exclude] waren ingesteld, niet duidelijk werden weergegeven. Dit heeft tot verwarring geleid bij het controleren van de logica voor doelgroepen, met name voor doelgroepen die specifieke URL&#39;s uitsluiten. (TGT-53809)
* **de definitiewaarden van de Publiek nu selecteerbaar en copyable in [!UICONTROL Targeting] tabel.** Oplossing voor een probleem in de interface Activiteit maken dat ervoor zorgde dat gebruikers geen waarden voor de publieksregel konden selecteren en kopiëren op het tabblad [!UICONTROL Targeting] . Deze functionaliteit was beschikbaar in de oudere gebruikersinterface, maar ontbreekt in de bijgewerkte gebruikersinterface. (TGT-53856)

+++

**Localization**

+++Zie details
* **Correcteerde vertaling van &quot;citaat&quot;in de context van de zh_CN paginaredacteur.** Correctie van een contextuele vertaalfout in de landinstelling zh_CN waar de term &quot;quote&quot; onjuist is vertaald als &quot;报 价&quot;, wat een commercieel prijsopgave impliceert. In de sectie Typografie > Kopstijl > Blockquote verwijst de bedoelde betekenis naar een opmaakelement (prijsblok voor aanhalingstekens) en niet naar de prijs. (TGT-53841)
* **Correcteerde vertaling van &quot;geschrapt citaat&quot;in zh_CN context van de paginaredacteur.** Correctie van een vertaalfout in de landinstelling zh_CN waar &quot;quote verwijderd&quot; onjuist is weergegeven als &quot;移 除 报 价&quot;, wat een commercieel prijsopgave impliceert. In de sectie Typografie > Kopstijl > Blockquote verwijst de term naar een opmaakelement (prijsblok voor aanhalingstekens) en niet naar de prijsaanduiding. (TGT-53843)
* **Correcteerde vertaling van &quot;citaat herschikte&quot;in de context van de paginageditor zh_CN.** Correctie van een contextafhankelijke vertaalfout in de landinstelling zh_CN waarbij &quot;quote herschikt&quot; onjuist werd vertaald als &quot;重 排 列 了 价&quot;, wat een commerciële prijsopgave impliceert. In de sectie Typografie > Kopstijl > Blockquote verwijst de term naar een opmaakelement (prijsblok voor aanhalingstekens) en niet naar de prijsaanduiding. (TGT-53844)
* **Correcteerde vertaling van &quot;citaat veranderde&quot;in de context van de zh_CN paginaredacteur.** Correctie van een vertaalfout in de landinstelling zh_CN waar &quot;prijswijziging&quot; onjuist is weergegeven als &quot;更 改 报 价&quot;, wat een commerciële prijsopgave suggereert. In de sectie Typografie > Kopstijl > Blockquote verwijst de term naar een opmaakelement (prijsblok voor aanhalingstekens) en niet naar de prijsaanduiding. (TGT-53845)

+++

**Aanbevelingen**

+++Zie details
* **CSS selecteerveranderingen voor aanbevelingen bewaren nu correct.** Oplossing voor een probleem in de gebruikersinterface voor het maken van activiteiten dat ervoor zorgde dat gebruikers de CSS-kiezer niet konden bijwerken voor aanbevelingen. Wijzigingen zijn na het opslaan ongedaan gemaakt, zodat updates voor het aanwijzen van containers worden geblokkeerd. (TGT-53835)
* **de gebeurtenisselectie van de ladingsgebeurtenis van de Pagina blijft nu in aanbevelingen wijzigingen.** Oplossing voor een probleem in de gebruikersinterface voor het maken van activiteiten waardoor gebruikers geen wijzigingen konden opslaan wanneer ze het gebeurtenistype van een aanbeveling van [!UICONTROL View] naar [!UICONTROL Page Load] schakelden. Hoewel de selectie succesvol leek, werd deze hersteld nadat was genavigeerd en de publicatie van de activiteit werd geblokkeerd. (TGT-53957)

+++

**Rapporten**

+++Zie details
* **&quot;[!UICONTROL Export order details to CSV]&quot;downloadt nu volledige gegevens.** Oplossing voor een probleem in de bijgewerkte [!UICONTROL Overview] UI dat ertoe leidde dat de optie &quot;[!UICONTROL Export Order details to CSV]&quot; lege bestanden downloadde, zelfs als er geldige rapportgegevens aanwezig waren. (TGT-53787)

+++

**Veiligheid**

+++Zie details
* **IMS prefilter die wordt toegevoegd om GQL eindpunten tegen dwars-org gegevensblootstelling te beschermen.** Oplossing voor een beveiligingskwetsbaarheid op het tabblad Beheer die invloed heeft op de GraphQL-eindpunten licensegroups en targetProperties. Het probleem is ontstaan door het gebruik van de JIL API met een beheerdersclient-token dat kan worden gebruikt om toegang te krijgen tot productgegevens op verschillende platformen. (TGT-53837)

+++

**Visuele Composer van de Ervaring (VEC)**

+++Zie details
* **Authoring stabiliteit hersteld in Activiteit leidt UI.** Oplossing voor een periodiek probleem in VEC UI dat het ontwerpen veroorzaakte om te ontbreken en de verbindingen onverwacht klikbaar werden, die gebruikers buiten de pagina richten. (TGT-53153)
* **het uitgeven herstelde voor bewaarde activiteiten in Activiteit leidt UI.** Oplossing voor een probleem waardoor gebruikers hun activiteiten niet konden bewerken nadat ze wijzigingen hadden opgeslagen. Betrokken activiteiten bleven vastzitten in &quot;[!UICONTROL Applying initial modifications]&quot;, waardoor verdere updates worden geblokkeerd en de knop [!UICONTROL Cancel] wordt verborgen. (TGT-53631)
* **VEC blijft niet meer op &quot;[!UICONTROL Applying initial modifications].&quot;** Oplossing voor een prestatieprobleem in de VEC dat lange vertragingen veroorzaakte bij het laden van toepassingen met een groot aantal wijzigingen. Betrokken gebruikers zagen UI op &quot;[!UICONTROL Applying initial modifications]&quot;verscheidene notulen, vooral in de scenario&#39;s van de Ervaring B bleef. (TGT-53727)
* **VEC laadt nu wijzigingen zonder wortelelementen.**
Oplossing van een kwestie in VEC die ervaringen veroorzaakte om te blokkeren wanneer het laden van wijzigingen die een duidelijk wortelelement ontbraken. Deze wijzigingen veroorzaakten eerder UI om voor onbepaalde tijd op &quot;A [!UICONTROL pplying initial modifications] te hangen.&quot; (TGT-53799)
* **het Opslaan van veranderingen in activiteiten werkt nu zoals verwacht.** Oplossing voor een probleem met betrekking tot machtigingen in de interface Nieuwe interface maken dat gebruikers verhindert wijzigingen op te slaan bij het bewerken van doelen en geavanceerde instellingen in activiteiten. De betrokken gebruikers zagen een rood foutenlint en een &quot;Forbidden.Resource&quot;bericht, ondanks het hebben van aangewezen toegang. (TGT-53816)
* **VEC UI bewaart nu ervaringswijzigingen over meningen.** Oplossing voor meerdere problemen in de bijgewerkte VEC die invloed hadden op de ontwikkeling van de ervaring. Wijzigingen bleven niet goed doorgaan, vooral wanneer u HTML-aanbiedingen gebruikt of schakelt tussen weergaven. (TGT-53825)
* **Alle meningen tonen nu correct wanneer een wijziging veelvoudige ervaringen overspant.** Oplossing voor een probleem in de interface voor het maken van activiteiten waarbij slechts één weergave werd weergegeven toen een wijziging werd toegepast op meerdere weergaven. De knopinfo voor aanwijzen kan niet alle bijbehorende weergaven weergeven, ook al is de wijziging correct toegepast. (TGT-53827)
* **VEC blijft niet meer periodiek op &quot;[!UICONTROL Applying initial modifications].&quot;** Oplossing voor een periodiek probleem in VEC waarbij ervaringen niet konden worden geladen en vastbleven op &quot; [!UICONTROL Applying initial modifications]&quot;. Dit gedrag was inconsistent en leidde soms tot omleidingslijnen of vereiste handmatige cacheverwerking. (TGT-53916)
* **VEC ladingskwestie kon niet worden gereproduceerd.** Er is een probleem onderzocht waarbij de VEC tijdens het bewerken van bestaande activiteiten vastbleef op &quot;[!UICONTROL Applying initial modifications]&quot;. Het gedrag zou gerelateerd zijn aan HTML-inhoud zonder bovenliggend element. We zullen de controle op herhalingen voortzetten en het gebruik van gestructureerde containers voor HTML-aanbiedingen aanbevelen om de stabiliteit te garanderen. (TGT-53972)
* De modus **[!UICONTROL Design]in de VEC gedraagt zich niet meer als de modus [!UICONTROL Browse] .** Oplossing voor een probleem in de gebruikersinterface waarbij de [!UICONTROL Design] modus zich periodiek gedraagt als de [!UICONTROL Browse] -modus, zodat op klikbare `<a>` koppelingen kan worden geklikt en elementen niet kunnen worden geselecteerd. Hierdoor verdween het aanwijsvak en werden de wijzigingsworkflows geblokkeerd. (TGT-53136)
* **klikt de knoop op [!UICONTROL Composer] wijze niet meer teweegbrengt paginaomleiding.** Oplossing voor een probleem in de bijgewerkte VEC-gebruikersinterface dat er door het klikken op een knop in de modus [!UICONTROL Composer] een onverwachte omleiding naar de doel-URL van de knop veroorzaakte. Hierdoor konden gebruikers call-to-action (CTA)-elementen niet bewerken en werd de ontwerpworkflow verstoord. (TGT-53137)
* **de codeupdates van de aanbieding in geautomatiseerde verpersoonlijkingsactiviteiten sparen nu zonder fout.** Oplossing voor een probleem in de Nieuwe Create UI dat een fout &quot;[!UICONTROL Invalid user input]&quot; veroorzaakte bij het bijwerken van aanbiedingscode in [!UICONTROL Automated Personalization] -activiteiten. Door deze fout konden gebruikers geen wijzigingen opslaan, zelfs niet als de invoer geldig was. (TGT-53586)
* **[!UICONTROL Design]in de VEC blokkeert nu de koppelingsnavigatie voor bewerkbare componenten.** Oplossing voor een probleem in de bijgewerkte VEC waarbij klikbare elementen (zoals knoppen en koppelingen) paginareuchting hebben geactiveerd, zelfs in de modus [!UICONTROL Design] . Door dit gedrag werd de modus [!UICONTROL Browse] nagebootst en konden gebruikers geen sleutelcomponenten wijzigen. (TGT-53696)
* **&quot;[!UICONTROL Clicked an element]&quot;metrisch werkt nu zonder omleiding of fout.** Oplossing voor een probleem in Nieuwe Create UI dat onverwachte omleidingen en lege schermen veroorzaakte wanneer het selecteren van metrische conversie &quot;[!UICONTROL Clicked an element]&quot;. Het klikken van een knoop tijdens opstelling teweeggebrachte navigatie in plaats van het registreren van het element, resulterend in &quot;[!UICONTROL element not found]&quot;fout. (TGT-53817)
* **Bestaande activiteiten blijven niet meer vastzitten in oneindige ladingslijn tijdens uitgeven.** Oplossing voor een probleem in de Nieuwe Create UI waarbij het bewerken van een bestaande activiteit in de VEC ertoe leidde dat de pagina vastliep in een oneindige laadlus. Deze kwestie beïnvloedde pas gecreëerde activiteiten niet en werd teweeggebracht door reeds bestaande wijzigingen op de pagina. (TGT-53913)
* **Bestaande activiteitenpagina&#39;s met wijzigingen laden nu correct in VEC.** Oplossing voor een probleem in de bijgewerkte VEC dat ervoor zorgde dat pagina&#39;s vastzaten in de laadfase tijdens het bewerken van een bestaande activiteit met opgeslagen wijzigingen. De nieuwe activiteiten die zonder kwestie worden geladen, maar eerder gevormde activiteiten slaagden er niet in om terug te geven. (TGT-53967)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [&#x200B; de nota&#39;s van de Versie: De Ervaring van het Platform van Adobe Target Web SDK &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=nl-NL) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [&#x200B; at.js versiedetails &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Bron | Details |
|--- |--- |
| [&#x200B; Veranderingen van de Documentatie &#x200B;](/help/main/r-release-notes/doc-change.md) | Gedetailleerde informatie weergeven over updates van deze handleiding die niet zijn opgenomen in deze releaseopmerkingen. |
| [&#x200B; de nota&#39;s van de Versie voor vorige versies &#x200B;](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium. |
| [&#x200B; de Nota&#39;s van de Versie van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=nl-NL){target=_blank} | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen. |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Bron | Details |
|--- |--- |
| [&#x200B; de Prioritaire Update van het Product van Adobe &#x200B;](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Ontvang voorafgaande meldingen over aanstaande productverbeteringen voor [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen. |
| [&#x200B; de Nota&#39;s van de Versie van het Doel - preRelease &#x200B;](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informatie over de versies van het Doel van de huidige maand, met inbegrip van pre-releaseinformatie. |
