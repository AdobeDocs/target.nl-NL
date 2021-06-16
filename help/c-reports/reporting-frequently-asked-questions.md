---
keywords: problemen oplossen;metrische verschillen;Veelgestelde vragen;rapporten;nieuwe bezoeker;nieuwe bezoekers;terugkerende bezoeker;terugkerende bezoekers;terugkeer bezoek;nieuw bezoek
description: Ontdek een lijst met veelgestelde vragen en antwoorden over Adobe [!DNL Target] rapportering.
title: Waar kan ik antwoorden op vragen over  [!DNL Target] Rapportering vinden?
feature: Rapporten
exl-id: 1a345a67-5050-4bd3-858d-99731d2c1dd3
source-git-commit: bdf8fdc0c7d92cb59270518861693ec22eb596f2
workflow-type: tm+mt
source-wordcount: '1294'
ht-degree: 0%

---

# Veelgestelde vragen over rapportage

Lijst met veelgestelde vragen over rapportage in [!DNL Adobe Target].

## Hoe lang blijven de gegevens voor [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Auto-Target] modellen bestaan?

[!UICONTROL Automated Personalization] (AP) en  [!UICONTROL Auto-Target] modellen worden getraind op de laatste 45 dagen van gebruikersgedrag (gebruikersprofielen, impliciete gebeurtenissen en conversiegebeurtenissen) voor de activiteit.

[!UICONTROL Automated Personalization] (AP) en  [!UICONTROL Auto-Target] modellen behouden het gebruikersgedrag, de trainingsverslagen, en de modelbeslissingsgegevens gedurende 90 dagen om  [!UICONTROL Insights] rapporten te produceren. Na 90 dagen worden trainingsgegevens en modelbeslissingen genegeerd. [!UICONTROL Automated Personalization] (AP) en  [!UICONTROL Auto-Target] modellen bewaren voor rapportagedoeleinden ook geaggregeerde gegevens over ervaring/aanbod en de conversie gedurende twee jaar. Deze gegevens zijn alleen gegevens op geaggregeerd niveau en bevatten geen profielgegevens op individueel niveau.

## Hoe worden de metriek Nieuwe Bezoekers en Terugkerende Bezoekers geteld? {#methodology}

Het eerste bezoek van een nieuwe bezoeker duurt zolang de bezoeker actief is op de site.
Als de gebruiker 30 minuten of langer inactief is, wordt de sessie opnieuw ingesteld. Als u de sessie herstelt, wordt deze bezoeker een Return Visitor bij het volgende bezoek of wordt hij weer actief na 30 minuten inactiviteit.
Als de bezoeker om de 29 minuten de hele dag door de site beweegt, wordt deze bezoeker die hele dag geteld als een nieuwe bezoeker. De sessie is nooit opnieuw ingesteld omdat de bezoeker de drempel van 30 minuten nooit heeft overschreden.

De volgende informatie verklaart meer in detail hoe de Nieuwe Bezoekers en Terugkerende Bezoekers worden geteld. De voorbeelden zijn ook inbegrepen verklarend waarom de som van deze twee segmenten niet altijd aan het aantal totale bezoekers optellen.

### Nieuwe bezoekers

Een bezoeker wordt opgenomen in het segment Nieuwe bezoekers als aan een van de volgende voorwaarden is voldaan:

* Het is de eerste keer dat de bezoeker de site bezoekt.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds hij cookies wist.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds de levensduur van het [bezoekersprofiel](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) is verlopen.

### Bezoekers terugsturen

De bezoeker wordt opgenomen in het segment Terugkerende bezoekers als de gebruiker de site eerder heeft bezocht, ten minste 30 minuten heeft verlaten en opnieuw met dezelfde cookies naar de site is teruggekeerd. Zolang een bezoeker binnen zijn profielleven terugkeert, deze bezoeker een terugkerende bezoeker.

Stel dat de levensduur van uw profiel is ingesteld op 14 dagen (de standaardwaarde). Een bezoeker wordt opgenomen in het segment Terugkerende bezoekers als aan de volgende voorwaarden wordt voldaan:

* Een bezoeker bezoekt de site voor het eerst en wordt opgenomen als nieuwe bezoeker.
* De bezoeker verlaat de site, maar keert zes dagen later terug.

Aangezien de levensduur van het profiel veertien dagen is ingesteld, wordt deze bezoeker opgenomen in het segment Terugkerende bezoekers. Als de bezoeker binnen die periode van zes dagen cookies heeft verwijderd, wordt die bezoeker opgenomen in het segment Nieuwe bezoekers.

### Voorbeelden die verschillen tussen metrische aantallen verklaren

**Voorbeeld 1**: Als deze twee segmenten worden toegepast op een activiteit, vormen het segment Nieuwe bezoekers en het segment Terugkerende bezoekers niet altijd het totale aantal bezoekers.

Neem bijvoorbeeld het volgende voorbeeld, waarbij u de hierboven vermelde voorwaarden voor Nieuwe Bezoekers en Terugkerende Bezoekers in acht neemt:

* Een bezoeker bezoekt de site voor de eerste keer en wordt geteld als een nieuwe bezoeker.
* De bezoeker keert terug naar de site nadat aan de voorwaarden voor het terugsturen van bezoekers is voldaan en wordt geteld als een terugkerende bezoeker.

Deze bezoeker wordt geteld als één bezoeker in het totale aantal bezoekers van de activiteit, ook al wordt het geteld in zowel het segment Nieuwe bezoekers als het segment Terugkerende bezoekers.

**Voorbeeld 2**: De discrepanties tussen de tellingen voor Nieuwe Bezoekers en Terugkerende Bezoekers hangen ook van af hoe u de de  [succesmetriek](/help/c-activities/r-success-metrics/success-metrics.md) van de activiteit vormt.

Bijvoorbeeld:

Verschillende nieuwe bezoekers bezoeken uw site en zijn gekwalificeerd voor een activiteit. Deze nieuwe bezoekers worden meegerekend in het segment Nieuwe Bezoekers. Al deze bezoekers namen ook een bezoek aan die activiteit.

Sommige bezoekers raakten de metrische conversie, die als &quot;Aantal van de Toename &amp; houdt Gebruiker in Activiteit.&quot;werd gevormd Veronderstel sommige van deze gebruikers de omzettings metrisch veelvoudige tijden bereiken, verhoogt omzettings metrisch niet. Gezien die opstelling, echter, zouden sommige gebruikers omzettings metrisch kunnen raken en dan terug naar de homepage navigeren, die in de activiteit opnieuw kwalificeert om een nieuw bezoek te registreren.

## Waarom bevatten mijn [!UICONTROL Experience Targeting] (XT) rapporten metriek voor controleervaringen?

XT-activiteiten moeten altijd een beheerervaring hebben. Als u een XT activiteit op een gelijkaardige manier aan [!UICONTROL A/B Test] activiteit gebruikt, die een vrij algemeen scenario is, zijn de gegevens van de controleervaring nuttig. U kunt de gegevens van de controleervaring negeren als u het niet nuttig in uw rapporten vindt.

## Waarom is het aantal bezoeken lager in [!DNL Target] dan in andere [!DNL Adobe Experience Cloud] oplossingen? {#section_7E626FDB417E41B8B58BBF30FB207409}

De metrische aantallen, bijvoorbeeld bezoeken, die door [!DNL Target] worden gemeld zijn altijd lager dan de gemelde aantallen in andere [!DNL Experience Cloud] oplossingen om verscheidene redenen:

* [!DNL Target] telt alleen bezoeken voor bezoekers die voor de activiteit in aanmerking kwamen. Andere oplossingen tellen bezoeken voor bezoekers die de pagina tonen, ongeacht welke activiteit hen aan de pagina bracht.
* Er kunnen situaties zijn waarin verschillende activiteiten op dezelfde locatie concurreren (wederzijds exclusief). Dit heeft tot gevolg dat bezoekers verschillende inhoud op een webpagina zien die van invloed is op de metrische nummers die worden gerapporteerd door [!DNL Target].

## Waarom zijn er geen gegevens beschikbaar voor mijn activiteitenverslag? {#section_E4722F6445884130951DF79981C8289B}

Als de inhoud van een activiteit met succes aan gebruikers werd geleverd maar zijn rapport bevat geen gegevens, zorg ervoor dat u het correcte milieu ([gastheergroep](/help/administrating-target/hosts.md)) hebt die in de montages van het rapport wordt geselecteerd.

Als u een ontwikkelomgeving hebt geselecteerd, wordt mogelijk het volgende foutbericht weergegeven: &quot;Er zijn geen gegevens beschikbaar voor de geselecteerde rapportinstellingen.&quot;

Om het milieu voor het rapport van een activiteit te veranderen:

1. Klik **[!UICONTROL Activities]**, klik de gewenste activiteit van de lijst, dan klik **[!UICONTROL Reports]** tabel.
1. Klik op het tandwielpictogram om de rapportinstellingen te configureren.

   ![A/B-instellingen, dialoogvenster](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >Het tandwielpictogram is niet beschikbaar voor [!UICONTROL Automated Personalization] (AP)-rapporten.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Environment]** de optie **[!UICONTROL Production]**.

   Rapportgegevens zijn mogelijk niet beschikbaar als u een ontwikkelomgeving hebt geselecteerd.

1. Klik op **[!UICONTROL Save]**.

Zie [Gastheren](/help/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E) voor meer informatie over omgevingen.

## Waarom is het verkeer verdeeld tussen mijn ervaringen ongelijk in mijn activiteit A/B of MVT? {#uneven}

Bijvoorbeeld, plaatste ik de verkeersverdeling aan 50/50 of 25/25/25/25 maar ik zie een zeer verschillende verdeling tussen ervaringen in de rapportering. Er zijn verscheidene verklaarbare redenen voor ongelijke bezoekersaantallen in [!DNL Target] rapportering:

* Wanneer een [!DNL Target] activiteit eerst wordt gelanceerd, kan de verkeersdistributie ongelijk wegens de architectuur van de randknoop zijn die [!DNL Target] gebruikt om ervaringslevering te optimaliseren. De beste praktijk is een activiteit wat tijd te geven om meer gegevens te verzamelen en de distributie zal normaliseren. Voor meer informatie over [!DNL Adobe Target] architectuur en de knopen van de Rand, zie [Hoe werkt Adobe Target](/help/c-intro/how-target-works.md).
* Als u in [!DNL Target] of [!DNL Analytics] bent en u **[!UICONTROL Visits]** metrisch gebruikt, herinner dat [!DNL Target] een op bezoeker-gebaseerd systeem is en de verkeersdistributie voor een test A/B of MVT wordt toegewezen op het bezoekersniveau. Aldus, als u activiteitenresultaten gebruikend **[!UICONTROL Visits]** metrisch onderzoekt, zou de verkeersdistributie ongelijk kunnen lijken omdat bepaalde bezoekers veelvoudige bezoeken zouden kunnen hebben. Bezoekers zijn de standaard die metrische gegevens normaliseren bij het evalueren van de prestaties van de activiteit.
* De beste praktijk voor A/B- en MVT-tests is het gelijkmatig verdelen van het verkeer. Het wijzigen van de verkeersverdeling tussen ervaringen (bijvoorbeeld van 90/10 naar 50/50) tijdens een test kan leiden tot ongelijke ervaringen tussen bezoekers. De lagere verkeerservaring zou nooit &quot;inhalen.&quot;
* Als u de bovenstaande beste praktijken volgt en de verkeerssplitsing niet in tijd normaliseert, zou u het volgende moeten controleren:

   * Gebruikt u de nieuwste bibliotheek van at.js? Voor meer informatie over de huidige versie en bijbehorende versienota&#39;s, zie [at.js versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * Is het een omleidingstest? Onjuiste timing van het vuren van markeringen op de pagina kan tot ongelijkmatige verkeerspleten leiden, vooral wanneer het gebruiken van [!DNL Analytics] als gegevensbron voor een [!DNL Target] activiteit. Voor details om ongelijke verkeersdistributie op een omleidingsactiviteit met Analytics voor Doel (A4T) te verhelpen, zie [Aanbiedingen omleiden - A4T FAQ](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
