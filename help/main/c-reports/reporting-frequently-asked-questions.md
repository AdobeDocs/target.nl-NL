---
keywords: problemen oplossen;metrische verschillen;Veelgestelde vragen;rapporten;nieuwe bezoeker;nieuwe bezoekers;terugkerende bezoeker;terugkerende bezoekers;terugkeer bezoek;nieuw bezoek
description: Onderzoek een lijst van vaak gestelde vragen en antwoorden over Adobe  [!DNL Target]  rapporterend.
title: Waar kan ik antwoorden aan Vragen over  [!DNL Target]  het Melden vinden?
feature: Reports
exl-id: 1a345a67-5050-4bd3-858d-99731d2c1dd3
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 0%

---

# Veelgestelde vragen over rapportage

Lijst met veelgestelde vragen over rapportage in [!DNL Adobe Target] .

## Hoe worden de metriek Nieuwe Bezoekers en Terugkerende Bezoekers geteld? {#methodology}

Het eerste bezoek van een nieuwe bezoeker duurt zolang de bezoeker actief is op de site.
Als de gebruiker 30 minuten of langer inactief is, wordt de sessie opnieuw ingesteld. Als u de sessie herstelt, wordt deze bezoeker een Return Visitor bij het volgende bezoek of wordt hij weer actief na 30 minuten inactiviteit.
Als de bezoeker om de 29 minuten de hele dag door de site beweegt, wordt deze bezoeker die hele dag geteld als een nieuwe bezoeker. De sessie is nooit opnieuw ingesteld omdat de bezoeker de drempel van 30 minuten nooit heeft overschreden.

De volgende informatie verklaart meer in detail hoe de Nieuwe Bezoekers en Terugkerende Bezoekers worden geteld. De voorbeelden zijn ook inbegrepen verklarend waarom de som van deze twee segmenten niet altijd aan het aantal totale bezoekers optellen.

### Nieuwe bezoekers

Een bezoeker wordt opgenomen in het segment Nieuwe bezoekers als aan een van de volgende voorwaarden is voldaan:

* Het is de eerste keer dat de bezoeker de site bezoekt.
* Het is de eerste keer dat de bezoeker de site bezoekt sinds hij cookies wist.
* Het is de eerste keer die van de bezoeker de plaats bezoekt aangezien het [&#x200B; leven van het het profielleven van de Bezoeker &#x200B;](/help/main/c-target/c-visitor-profile/visitor-profile-lifetime.md) is verlopen.

### Bezoekers terugsturen

De bezoeker wordt opgenomen in het segment Terugkerende bezoekers als de gebruiker de site eerder heeft bezocht, ten minste 30 minuten heeft verlaten en opnieuw met dezelfde cookies naar de site is teruggekeerd. Zolang een bezoeker binnen zijn profielleven terugkeert, deze bezoeker een terugkerende bezoeker.

Stel dat de levensduur van uw profiel is ingesteld op 14 dagen (de standaardwaarde). Een bezoeker wordt opgenomen in het segment Terugkerende bezoekers als aan de volgende voorwaarden wordt voldaan:

* Een bezoeker bezoekt de site voor het eerst en wordt opgenomen als een nieuwe bezoeker.
* De bezoeker verlaat de site, maar keert zes dagen later terug.

Aangezien de levensduur van het profiel veertien dagen is ingesteld, wordt deze bezoeker opgenomen in het segment Terugkerende bezoekers. Als de bezoeker binnen die periode van zes dagen cookies heeft verwijderd, wordt die bezoeker opgenomen in het segment Nieuwe bezoekers.

### Voorbeelden die verschillen tussen metrische aantallen verklaren

**Voorbeeld 1**: Als deze twee segmenten op een activiteit worden toegepast, voegen het Nieuwe segment van Bezoekers en het Terugkerende segment van Bezoekers niet altijd tot het totale aantal bezoekers toe.

Neem bijvoorbeeld het volgende voorbeeld, waarbij u de hierboven vermelde voorwaarden voor Nieuwe Bezoekers en Terugkerende Bezoekers in acht neemt:

* Een bezoeker bezoekt de site voor de eerste keer en wordt geteld als een nieuwe bezoeker.
* De bezoeker keert terug naar de site nadat aan de voorwaarden voor het terugsturen van bezoekers is voldaan en wordt geteld als een terugkerende bezoeker.

Deze bezoeker wordt geteld als één enkele bezoeker in het totale aantal bezoekers van de activiteit, ook al wordt het geteld in zowel de segmenten Nieuwe Bezoekers als Terugkerende Bezoekers.

**Voorbeeld 2**: De discrepanties tussen de tellingen voor Nieuwe Bezoekers en Terugkerende Bezoekers hangen ook van af hoe u de 2&rbrace; succesmetriek van de activiteit [&#x200B; vormt.](/help/main/c-activities/r-success-metrics/success-metrics.md)

Bijvoorbeeld:

Verschillende nieuwe bezoekers bezoeken uw site en zijn gekwalificeerd voor een activiteit. Deze nieuwe bezoekers worden meegerekend in het segment Nieuwe Bezoekers. Al deze bezoekers namen ook een bezoek aan die activiteit.

Sommige bezoekers raakten de metrische conversie, die als &quot;Aantal van de Toename &amp; houdt Gebruiker in Activiteit.&quot;werd gevormd Veronderstel sommige van deze gebruikers de omzettings metrisch veelvoudige tijden bereiken, verhoogt omzettings metrisch niet. Gezien die opstelling, echter, zouden sommige gebruikers omzettings metrisch kunnen raken en dan terug naar de homepage navigeren, die in de activiteit opnieuw kwalificeert om een nieuw bezoek te registreren.

## Waarom bevatten mijn [!UICONTROL Experience Targeting] (XT) rapporten metriek voor controleervaringen?

XT-activiteiten moeten altijd een beheerervaring hebben. Als u een activiteit XT op een gelijkaardige manier aan een [!UICONTROL A/B Test] activiteit gebruikt, die een vrij algemeen scenario is, zijn de gegevens van de controleervaring nuttig. U kunt de gegevens van de controleervaring negeren als u het niet nuttig in uw rapporten vindt.

## Waarom is het aantal bezoeken lager in [!DNL Target] dan in andere [!DNL Adobe Experience Cloud] oplossingen? {#section_7E626FDB417E41B8B58BBF30FB207409}

De metrische aantallen, bijvoorbeeld bezoeken, die door [!DNL Target] worden gemeld zijn altijd lager dan de gemelde aantallen in andere [!DNL Experience Cloud] oplossingen om verscheidene redenen:

* [!DNL Target] telt alleen bezoeken voor bezoekers die voor de activiteit in aanmerking kwamen. Andere oplossingen tellen bezoeken voor bezoekers die de pagina tonen, ongeacht welke activiteit hen aan de pagina bracht.
* Er kunnen situaties zijn waarin verschillende activiteiten op dezelfde locatie concurreren (wederzijds exclusief). Dit heeft tot gevolg dat bezoekers verschillende inhoud op een webpagina zien die van invloed is op de metrische nummers die door [!DNL Target] worden gerapporteerd.

## Waarom zijn er geen gegevens beschikbaar voor mijn activiteitenverslag? {#section_E4722F6445884130951DF79981C8289B}

Als de inhoud van een activiteit met succes aan bezoekers werd geleverd maar zijn rapport bevat geen gegevens, zou u met het volgende foutenbericht kunnen worden voorgesteld: &quot;Er zijn geen gegevens beschikbaar voor de geselecteerde rapportmontages.&quot;

Er zijn een paar mogelijke redenen waarom gegevens ontbreken in activiteitenverslagen:

* U hebt niet het correcte milieu geselecteerd in de montages van het rapport
* U hebt geen verkeer dat aan de controleervaring wordt toegewezen

### U hebt niet het correcte milieu geselecteerd in de montages van het rapport:

Als de inhoud van een activiteit met succes aan gebruikers werd geleverd maar zijn rapport bevat geen gegevens, zorg ervoor dat u het correcte milieu ([&#x200B; die gastheergroep &#x200B;](/help/main/administrating-target/hosts.md)) in de montages van het rapport wordt geselecteerd hebt.

Om het milieu voor het rapport van een activiteit te veranderen:

1. Klik op **[!UICONTROL Activities]** , klik in de lijst op de gewenste activiteit en klik vervolgens op de tab **[!UICONTROL Reports]** .
1. Klik op het tandwielpictogram om de rapportinstellingen te configureren.

   ![&#x200B; de dialoogdoos van Montages A/B &#x200B;](/help/main/c-reports/c-report-settings/assets/ab_settings_dialog.png)

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Environment]** de optie **[!UICONTROL Production]**.

   Rapportgegevens zijn mogelijk niet beschikbaar als u een ontwikkelomgeving hebt geselecteerd.

1. Klik op **[!UICONTROL Save]**.

Voor meer informatie over milieu&#39;s, zie [&#x200B; Gastheren &#x200B;](/help/main/administrating-target/hosts.md#concept_516BB01EBFBD4449AB03940D31AEB66E).

### U hebt geen verkeer dat aan de controleervaring wordt toegewezen

Als de inhoud van een activiteit met succes aan gebruikers werd geleverd maar zijn rapport bevat geen gegevens, zorg ervoor dat u een ervaring met verkeer als controleervaring gebruikt.

1. Klik op **[!UICONTROL Activities]** , klik in de lijst op de gewenste activiteit en klik vervolgens op de tab **[!UICONTROL Reports]** .
1. Klik op het tandwielpictogram om de rapportinstellingen te configureren.

1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Control]** een ervaring die verkeer ontvangt.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Voor meer informatie over hoe te om een [!UICONTROL Automated Personalization] (AP) activiteit bij te werken en de controleervaring in een ervaring te veranderen die verkeer ontvangt, zie [&#x200B; de controle voor uw activiteit van Automated Personalization of Auto-Doel &#x200B;](/help/main/c-activities/t-automated-personalization/experience-as-control.md) selecteren.


## Waarom is het verkeer verdeeld tussen mijn ervaringen ongelijk in mijn activiteit A/B of MVT? {#uneven}

Bijvoorbeeld, plaatste ik de verkeersverdeling aan 50/50 of 25/25/25/25 maar ik zie een zeer verschillende verdeling tussen ervaringen in de rapportering. Er zijn verschillende oorzaken die kunnen worden verklaard door het feit dat een bezoeker in [!DNL Target] -rapporten een ongelijk aantal bezoekers telt:

* Wanneer een [!DNL Target] -activiteit voor het eerst wordt gestart, kan de verkeersdistributie ongelijk zijn vanwege de architectuur van het randknooppunt die [!DNL Target] gebruikt om de levering van de ervaring te optimaliseren. De beste praktijk is een activiteit wat tijd te geven om meer gegevens te verzamelen en de distributie zal normaliseren. Voor meer informatie over [!DNL Adobe Target] architectuur en de knopen van Edge, zie [&#x200B; hoe Adobe Target &#x200B;](/help/main/c-intro/how-target-works.md) werkt.
* Als u in [!DNL Target] of [!DNL Analytics] bent en u **[!UICONTROL Visits]** metrisch gebruikt, herinner me dat [!DNL Target] een op bezoekers-gebaseerd systeem is en de verkeersdistributie voor een test A/B of MVT wordt toegewezen op het bezoekersniveau. Als u dus de resultaten van de activiteit bekijkt met de **[!UICONTROL Visits]** -meting, kan de verkeersdistributie ongelijk lijken, omdat bepaalde bezoekers mogelijk meerdere bezoeken hebben. Bezoekers zijn de standaard die metrische gegevens normaliseren bij het evalueren van de prestaties van de activiteit.
* De beste praktijk voor A/B- en MVT-tests is het gelijkmatig verdelen van het verkeer. Het wijzigen van de verkeersverdeling tussen ervaringen (bijvoorbeeld van 90/10 naar 50/50) tijdens een test kan leiden tot ongelijke ervaringen tussen bezoekers. De lagere verkeerservaring zou nooit &quot;inhalen.&quot;
* Als u de bovenstaande beste praktijken volgt en de verkeerssplitsing niet in tijd normaliseert, zou u het volgende moeten controleren:

   * Gebruikt u de nieuwste bibliotheek van at.js? Voor meer informatie over de huidige versie en de bijbehorende versiedetails, zie [&#x200B; at.js versiedetails &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank}.

   * Is het een omleidingstest? Onjuiste timing van het afvuren van tags op de pagina kan leiden tot ongelijke verkeerspleten, vooral wanneer [!DNL Analytics] als gegevensbron voor een [!DNL Target] -activiteit wordt gebruikt. Voor details om ongelijkmatige verkeersdistributie op een omleidingsactiviteit met Analytics voor Doel (A4T) te verhelpen, zie [&#x200B; Redirect aanbiedingen - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md).
