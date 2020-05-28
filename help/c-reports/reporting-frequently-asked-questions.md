---
keywords: troubleshooting;metric discrepancies;FAQ;reports;new visitor;new visitors;returning visitor;returning visitors;return visit;new visit
description: Lijst met veelgestelde vragen over rapportage in Adobe Target.
title: Veelgestelde vragen over rapportage voor Adobe Target
topic: Standard
uuid: 0be40d3f-3274-493d-899b-cb7bb3612baf
translation-type: tm+mt
source-git-commit: c22f2c375c15c5827f5c9884fbf948b99424c760
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---


# Veelgestelde vragen over rapportage{#reporting-faq}

Lijst met veelgestelde vragen over rapportage in [!DNL Target].

## Hoe worden de metriek Nieuwe Bezoekers en Terugkerende Bezoekers geteld?

Overweeg het volgende:

**Nieuwe bezoekers**: Een bezoeker wordt opgenomen in het segment Nieuwe bezoekers als aan een van de volgende voorwaarden is voldaan:

* Het is de eerste keer dat de bezoeker de site bezoekt.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds hij cookies wist.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds de levensduur [van het](/help/c-target/c-visitor-profile/visitor-profile-lifetime.md) bezoekersprofiel is verstreken.

**Bezoekers** terugsturen: De bezoeker wordt opgenomen in het segment Terugkerende bezoekers als de gebruiker de site eerder heeft bezocht, ten minste 30 minuten heeft verlaten en opnieuw met dezelfde cookies naar de site is teruggekeerd. Zolang een bezoeker binnen zijn profielleven terugkeert, zullen zij een terugkerende bezoeker zijn.

Als deze twee segmenten worden toegepast op een activiteit, vormen het segment Nieuwe bezoekers en het segment Terugkerende bezoekers niet altijd het totale aantal bezoekers.

Bekijk het volgende voorbeeld, gezien de voorwaarden hierboven voor Nieuwe Bezoekers en Terugkerende Bezoekers:

* Een bezoeker bezoekt de site voor de eerste keer en wordt geteld als een nieuwe bezoeker.
* De bezoeker keert terug naar de site nadat aan de voorwaarden voor het terugsturen van bezoekers is voldaan en wordt geteld als een terugkerende bezoeker.

Deze bezoeker wordt geteld als één bezoeker in het totale aantal bezoekers van de activiteit, ook al wordt het geteld in zowel het segment Nieuwe bezoekers als het segment Terugkerende bezoekers.

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

Zie [Gastheren](../administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E)voor meer informatie over omgevingen.

## Waarom is het verkeer verdeeld tussen mijn ervaringen ongelijk in mijn activiteit A/B of MVT? {#uneven}

Bijvoorbeeld, plaatste ik de verkeersverdeling aan 50/50 of 25/25/25/25 maar ik zie een zeer verschillende verdeling tussen ervaringen in de rapportering. Er zijn een aantal verklaarbare redenen voor ongelijke aantallen bezoekers in het [!DNL Target] melden:

* Wanneer een [!DNL Target] activiteit eerst wordt gelanceerd, zou de verkeersdistributie wegens de architectuur van de randknoop ongelijk kunnen zijn die [!DNL Target] gebruikt om ervaringslevering te optimaliseren. De beste praktijk is een activiteit wat tijd te geven om extra gegevens te verzamelen en de distributie zal normaliseren. Zie [!DNL Adobe Target] Hoe werkt [Adobe Target voor meer informatie over](/help/c-intro/how-target-works.md)architectuur en Edge-knooppunten.
* Als u binnen bent [!DNL Target] of [!DNL Analytics] en u **[!UICONTROL Visits]** metrisch gebruikt, herinner dat [!DNL Target] een op bezoeker-gebaseerd systeem is en de verkeersdistributie voor een test A/B of MVT wordt toegewezen op het bezoekersniveau. Aldus, als u activiteitenresultaten gebruikend **[!UICONTROL Visits]** metrisch onderzoekt, kan de verkeersdistributie ongelijk lijken omdat bepaalde bezoekers veelvoudige bezoeken zouden kunnen hebben. Bezoekers zijn de standaard die metrische gegevens normaliseren bij het evalueren van de prestaties van de activiteit.
* De beste praktijk voor A/B- en MVT-tests is het gelijkmatig verdelen van het verkeer. Het wijzigen van de verkeersverdeling tussen ervaringen (bijvoorbeeld van 90/10 naar 50/50) tijdens een test kan leiden tot ongelijke ervaringen tussen bezoekers. De lagere verkeerservaring kan nooit &quot;inhalen.&quot;
* Als u de bovenstaande beste praktijken volgt en de verkeerssplitsing niet in tijd normaliseert, zou u het volgende moeten controleren:

   * Gebruikt u de nieuwste bibliotheek van at.js? Raadpleeg de versiedetails [at.js voor meer informatie over de huidige versie en de bijbehorende opmerkingen bij de release](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

   * Is het een omleidingstest? Onjuiste timing van tags die op de pagina worden afgevuurd, kan leiden tot ongelijke verkeerspleten, vooral wanneer u deze gebruikt [!DNL Analytics] als gegevensbron voor een [!DNL Target] activiteit. Voor details om ongelijke verkeersdistributie op een omleidingsactiviteit met Analytics voor Doel (A4T) te verhelpen, zie [Redirect aanbiedingen - Veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md)A4T.
