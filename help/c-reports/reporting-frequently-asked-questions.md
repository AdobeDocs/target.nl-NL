---
keywords: troubleshooting;metric discrepancies;FAQ;reports;new visitor;new visitors;returning visitor;returning visitors;return visit;new visit
description: Lijst met veelgestelde vragen over rapportage in Adobe Target.
title: Veelgestelde vragen over rapportage voor Adobe Target
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---


# Veelgestelde vragen over rapportage{#reporting-faq}

Lijst met veelgestelde vragen over rapportage in [!DNL Target].

## Hoe worden de metriek Nieuwe Bezoekers en Terugkerende Bezoekers geteld?

De volgende informatie verklaart hoe de Nieuwe Bezoekers en Terugkerende Bezoekers worden geteld en verstrekt voorbeelden van waarom de som van deze twee segmenten niet altijd aan het aantal totale bezoekers optellen.

### Nieuwe bezoekers

Een bezoeker wordt opgenomen in het segment Nieuwe bezoekers als aan een van de volgende voorwaarden is voldaan:

* Het is de eerste keer dat de bezoeker de site bezoekt.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds hij cookies wist.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds de levensduur [van het](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) bezoekersprofiel is verstreken.

### Bezoekers terugsturen

De bezoeker wordt opgenomen in het segment Terugkerende bezoekers als de gebruiker de site eerder heeft bezocht, ten minste 30 minuten heeft verlaten en opnieuw met dezelfde cookies naar de site is teruggekeerd. Zolang een bezoeker binnen zijn profielleven terugkeert, zullen zij een terugkerende bezoeker zijn.

Stel dat de levensduur van uw profiel 14 dagen is ingesteld (de standaardwaarde). Een bezoeker wordt opgenomen in het segment Terugkerende bezoekers als aan de volgende voorwaarden wordt voldaan:

* Een bezoeker bezoekt de site voor het eerst en wordt opgenomen als nieuwe bezoeker.
* De bezoeker verlaat de site, maar keert zes dagen later terug.

Aangezien de levensduur van het profiel veertien dagen is ingesteld, wordt deze bezoeker opgenomen in het segment Terugkerende bezoekers. Als de bezoeker binnen die periode van zes dagen cookies heeft verwijderd, wordt die bezoeker opgenomen in het segment Nieuwe bezoekers.

### Voorbeelden die verschillen tussen metrische aantallen verklaren

**Voorbeeld 1**: Als deze twee segmenten worden toegepast op een activiteit, vormen het segment Nieuwe bezoekers en het segment Terugkerende bezoekers niet altijd het totale aantal bezoekers.

Neem bijvoorbeeld het volgende voorbeeld, waarbij u de hierboven vermelde voorwaarden voor Nieuwe Bezoekers en Terugkerende Bezoekers in acht neemt:

* Een bezoeker bezoekt de site voor de eerste keer en wordt geteld als een nieuwe bezoeker.
* De bezoeker keert terug naar de site nadat aan de voorwaarden voor het terugsturen van bezoekers is voldaan en wordt geteld als een terugkerende bezoeker.

Deze bezoeker wordt geteld als één bezoeker in het totale aantal bezoekers van de activiteit, ook al wordt het geteld in zowel het segment Nieuwe bezoekers als het segment Terugkerende bezoekers.

**Voorbeeld 2**: De discrepanties tussen de tellingen voor Nieuwe Bezoekers en Terugkerende Bezoekers hangen ook van af hoe u de de [succesmetriek](/help/c-activities/r-success-metrics/success-metrics.md)van de activiteit vormt.

Bijvoorbeeld:

Een aantal nieuwe bezoekers bezoekt uw site en is gekwalificeerd voor een activiteit. Deze nieuwe bezoekers worden meegerekend in het segment Nieuwe Bezoekers. Al deze bezoekers namen ook een bezoek aan die activiteit.

Sommige bezoekers raakten de metrische conversie, die als &quot;Aantal van de Toename &amp; houdt Gebruiker in Activiteit.&quot;werd gevormd Stel dat sommige van deze gebruikers de metrische conversie meerdere keren hebben bereikt, de metrische conversie zal niet toenemen. Gezien die opstelling, echter, zouden sommige gebruikers omzettings metrisch kunnen raken en dan terug naar de homepage navigeren, die in de activiteit opnieuw kwalificeert om een nieuw bezoek te registreren.

## Waarom bevatten mijn [!UICONTROL Experience Targeting] (XT) rapporten metriek voor controleervaringen?

XT-activiteiten moeten altijd een beheerervaring hebben. Als u een activiteit XT op een gelijkaardige manier aan een [!UICONTROL A/B Test] activiteit gebruikt, die een vrij algemeen scenario is, zijn de gegevens van de controleervaring nuttig. U kunt de gegevens van de controleervaring negeren als u het niet nuttig in uw rapporten vindt.

## Waarom is het aantal bezoeken lager in [!DNL Target] dan in andere [!DNL Adobe Experience Cloud] oplossingen? {#section_7E626FDB417E41B8B58BBF30FB207409}

De metrische aantallen, bijvoorbeeld bezoeken, door [!DNL Target] zullen altijd lager zijn dan de gemelde aantallen in andere [!DNL Experience Cloud] oplossingen om een aantal redenen:

* [!DNL Target] telt alleen bezoeken voor bezoekers die voor de activiteit in aanmerking kwamen. Andere oplossingen tellen bezoeken voor bezoekers die de pagina tonen, ongeacht welke activiteit hen aan de pagina bracht.
* Er kunnen situaties zijn waarin verschillende activiteiten op dezelfde locatie concurreren (wederzijds exclusief). Dit heeft tot gevolg dat bezoekers verschillende inhoud op een webpagina zien die van invloed is op de metrische nummers die door [!DNL Target]worden gerapporteerd.

## Waarom zijn er geen gegevens beschikbaar voor mijn activiteitenverslag? {#section_E4722F6445884130951DF79981C8289B}

Als de inhoud van een activiteit met succes aan gebruikers werd geleverd maar zijn rapport bevat geen gegevens, zorg ervoor dat u het correcte milieu ([gastheergroep](/help/administrating-target/hosts.md)) hebt die in de montages van het rapport wordt geselecteerd.

Als u een ontwikkelomgeving hebt geselecteerd, wordt mogelijk het volgende foutbericht weergegeven: &quot;Er zijn geen gegevens beschikbaar voor de geselecteerde rapportinstellingen.&quot;

Om het milieu voor het rapport van een activiteit te veranderen:

1. Klik **[!UICONTROL Activities]**, klik de gewenste activiteit van de lijst, dan klik de **[!UICONTROL Reports]** tabel.
1. Klik op het tandwielpictogram om de rapportinstellingen te configureren.

   ![A/B-instellingen, dialoogvenster](/help/c-reports/c-report-settings/assets/ab_settings_dialog.png)

   >[!NOTE]
   >
   >Het tandwielpictogram is niet beschikbaar voor [!UICONTROL Automated Personalization] (AP)-rapporten.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Environment]** de optie **[!UICONTROL Production]**.

   Rapportgegevens zijn mogelijk niet beschikbaar als u een ontwikkelomgeving hebt geselecteerd.

1. Klik op **[!UICONTROL Save]**.

Zie [Gastheren](/help/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)voor meer informatie over omgevingen.

## Waarom is het verkeer verdeeld tussen mijn ervaringen ongelijk in mijn activiteit A/B of MVT? {#uneven}

Bijvoorbeeld, plaatste ik de verkeersverdeling aan 50/50 of 25/25/25/25 maar ik zie een zeer verschillende verdeling tussen ervaringen in de rapportering. Er zijn een aantal verklaarbare redenen voor ongelijke aantallen bezoekers in het [!DNL Target] melden:

* Wanneer een [!DNL Target] activiteit eerst wordt gelanceerd, zou de verkeersdistributie wegens de architectuur van de randknoop ongelijk kunnen zijn die [!DNL Target] gebruikt om ervaringslevering te optimaliseren. De beste praktijk is een activiteit wat tijd te geven om extra gegevens te verzamelen en de distributie zal normaliseren. Voor meer informatie over [!DNL Adobe Target] architectuur en de knopen van de Rand, zie [hoe Adobe Target werkt](/help/c-intro/how-target-works.md).
* Als u binnen bent [!DNL Target] of [!DNL Analytics] en u **[!UICONTROL Visits]** metrisch gebruikt, herinner dat [!DNL Target] een op bezoeker-gebaseerd systeem is en de verkeersdistributie voor een test A/B of MVT wordt toegewezen op het bezoekersniveau. Aldus, als u activiteitenresultaten gebruikend **[!UICONTROL Visits]** metrisch onderzoekt, kan de verkeersdistributie ongelijk lijken omdat bepaalde bezoekers veelvoudige bezoeken zouden kunnen hebben. Bezoekers zijn de standaard die metrische gegevens normaliseren bij het evalueren van de prestaties van de activiteit.
* De beste praktijk voor A/B- en MVT-tests is het gelijkmatig verdelen van het verkeer. Het wijzigen van de verkeersverdeling tussen ervaringen (bijvoorbeeld van 90/10 naar 50/50) tijdens een test kan leiden tot ongelijke ervaringen tussen bezoekers. De lagere verkeerservaring kan nooit &quot;inhalen.&quot;
* Als u de bovenstaande beste praktijken volgt en de verkeerssplitsing niet in tijd normaliseert, zou u het volgende moeten controleren:

   * Gebruikt u de nieuwste bibliotheek van at.js? Raadpleeg de versiedetails [at.js voor meer informatie over de huidige versie en de bijbehorende opmerkingen bij de release](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * Is het een omleidingstest? Onjuiste timing van tags die op de pagina worden afgevuurd, kan leiden tot ongelijke verkeerspleten, vooral wanneer u deze gebruikt [!DNL Analytics] als gegevensbron voor een [!DNL Target] activiteit. Voor details om ongelijke verkeersdistributie op een omleidingsactiviteit met Analytics voor Doel (A4T) te verhelpen, zie [Redirect aanbiedingen - Veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)A4T.
