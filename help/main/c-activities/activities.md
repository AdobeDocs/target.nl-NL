---
keywords: activiteitenlijst;activiteiten;activiteit;activiteitstypen;activiteit bewerken;activiteit;activiteit, acties;activiteitskenmerk;activiteitlijstfilter;activiteitsbeperkingen;personaliseren;personalisatie
description: Personaliseer inhoud en test paginaontwerpen voor specifiek publiek met  [!DNL Adobe Target]  activiteiten.
title: Hoe kan ik inhoud en de Ontwerpen van de Pagina van de Test aanpassen met  [!DNL Target]?
feature: Activities
exl-id: 7e61525d-b2db-44f6-a7c2-df5a8d28eca2
source-git-commit: 5012c2b849d6b415f08fcaa3be85508637e30481
workflow-type: tm+mt
source-wordcount: '2292'
ht-degree: 0%

---

# Overzicht van activiteiten

Inhoud aanpassen en paginaontwerpen testen voor specifieke doelgroepen met [!DNL Adobe Target] -activiteiten.

U kunt bijvoorbeeld een activiteit ontwerpen die twee verschillende landingspagina&#39;s test, een die informatie over dameszomerschoenen markeert, en een andere landingspagina die meer algemene zomerkleding markeert. De activiteit bepaalt de voorwaarden die controleren wanneer elk van deze het landen pagina&#39;s toont, en de metriek die bepalen welke pagina succesvoller is. De activiteit wordt gevormd om te beginnen en te beëindigen wanneer de specifieke voorwaarden, zoals tussen specifieke data worden voldaan. Of u kunt kiezen om te beginnen wanneer de activiteit wordt goedgekeurd en te beëindigen wanneer het wordt gedeactiveerd.

Wanneer het ontwerpen van een activiteit, zou u zorgvuldig moeten plannen. Bepaal wanneer de activiteit begint en hoe lang het duurt. Geef vervolgens een lijst met uw aanbiedingen en wijs een doelgroep toe aan elk aanbod.

## Activiteitenlijst {#section_DE8E2DB30D534962A931EF8BB48240F5}

De lijst [!UICONTROL Activities] is de standaardweergave wanneer u [!DNL Target] opent. U kunt activiteiten maken op deze pagina en bestaande activiteiten beheren.

U kunt de lijst [!UICONTROL Activities] ook weergeven door op de tab [!UICONTROL Activities] boven aan de gebruikersinterface van [!DNL Target] te klikken.

De lijst [!UICONTROL Activities] biedt een overzicht van alle activiteiten in uw [!DNL Target] -implementatie en biedt u de mogelijkheid verschillende handelingen uit te voeren.

In de volgende tabel vindt u informatie over verschillende elementen in de lijst [!UICONTROL Activities] in de gebruikersinterface van [!DNL Target] :

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL Show filters] pictogram<P>![&#x200B; toon Filters pictogram &#x200B;](/help/main/assets/icons/Filter.svg) | U kunt filters openen door op het pictogram **[!UICONTROL Show Filters]** boven aan de lijst te klikken om activiteiten van [!UICONTROL Type] , [!UICONTROL Status] , [!UICONTROL Reporting Source] , [!UICONTROL Experience Composer] , [!UICONTROL Metrics Type] , [!UICONTROL Decisioning Source] , [!UICONTROL Activity Source] en [!UICONTROL Properties] te filteren.<P>Filters die u configureert, blijven blijvend in de huidige sessie.<P>Voor meer informatie, zie [&#x200B; filters op de [!UICONTROL Activities] lijst &#x200B;](#filters) hieronder toepassen. |
| Zoeken in velden | Zoek snel een activiteit of verminder het aantal activiteiten dat in de [!UICONTROL Activity] lijst wordt getoond. U kunt zoeken op [!UICONTROL Activity Name] , [!UICONTROL URL] of [!UICONTROL ID] met behulp van de vervolgkeuzelijst.<P>De zoekopties die u configureert, blijven geldig in de huidige sessie. |
| [!UICONTROL Create Activity] | Maak een activiteit.<P>Zie voor meer informatie over het maken van de verschillende typen activiteiten: <ul><li>[&#x200B; creeer een [!UICONTROL A/B Test] activiteit &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)</li><li>[&#x200B; creeer een [!UICONTROL Auto-Allocate] activiteit &#x200B;](/help/main/c-activities/automated-traffic-allocation/create-auto-allocate-activity.md)</li><li>[&#x200B; creeer een [!UICONTROL Auto-Target] activiteit &#x200B;](/help/main/c-activities/auto-target/create-auto-target.md)</li><li>[&#x200B; creeer een [!UICONTROL Automated Personalization] activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)</li><li>[&#x200B; creeer een [!UICONTROL Experience Targeting] activiteit &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md)</li><li>[&#x200B; creeer een activiteit &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md)</li><li>[&#x200B; creeer a [!UICONTROL Recommendations] activiteit &#x200B;](/help/main/c-recommendations/recommendations.md)</li></ul>Voor meer informatie over elk type, zie [&#x200B; types van Activiteit &#x200B;](#types) hieronder. |
| [!UICONTROL Create mobile preview link]<P>![&#x200B; Meer actiemenu &#x200B;](/help/main/assets/icons/MoreVertical.svg) | Het gebruik [&#x200B; mobiele voorproefverbindingen &#x200B;](https://experienceleague.adobe.com/nl/docs/target-dev/developer/mobile-apps/target-mobile-preview) om gemakkelijke QA van begin tot eind voor mobiele toepassingsactiviteiten uit te voeren.<P>Klik het **Meer optiepictogram**, selecteer **creëren de Mobiele Verbinding van de Voorproef**, dan de activiteiten kiezen u op mobiel wilt testen. |
| Tabel aanpassen<P>![&#x200B; pas het pictogram van de Lijst &#x200B;](/help/main/assets/icons/ColumnSetting.svg) aan | U kunt de kolommen in de lijst van [!UICONTROL Activity] wijzigen door op het pictogram **[!UICONTROL Customize Table]** rechtsboven op de pagina te klikken en vervolgens de gewenste kolommen te selecteren of de selectie ervan op te heffen.<P>De wijzigingen worden toegepast op uw account en blijven actief, zelfs nadat u zich hebt afgemeld bij [!DNL Target] . |
| Selectievakjes voor bulkbewerkingen<P>![&#x200B; het pictogram van Verrichtingen van het Bulk &#x200B;](/help/main/assets/icons/Rectangle.svg) | bulktransacties uitvoeren op alle activiteiten of op geselecteerde activiteiten.<P>Voor een lijst van acties die (afhankelijk van uw toestemmingen en de activiteitenstatus) beschikbaar zijn, zie [&#x200B; snelle acties &#x200B;](#quick-actions) hieronder uitvoeren. |
| [!UICONTROL Type] | Het type activiteit. Met de kolom [!UICONTROL Type] kunt u snel elke activiteit op type identificeren. <ul><li>**AB-M**: hand [!UICONTROL A/B Test]</li><li>**ab-a**: [!UICONTROL Auto-Allocate]</li><li>**AB-AT**: [!UICONTROL Auto-Target]</li><li>**AP**: [!UICONTROL Automated Personalization]</li><li>**XT**: [!UICONTROL Experience Targeting]</li><li>**MVT**: [!UICONTROL Multivariate Test]</li><li>**REC**: [!UICONTROL Recommendations]</li></ul>Voor meer informatie over elk type, zie [&#x200B; types van Activiteit &#x200B;](#types) hieronder. |
| [!UICONTROL Name] | De naam van de activiteit. Klik het **[!UICONTROL Quick Info]** pictogram ( ![&#x200B; Snelle pictogram van Info &#x200B;](/help/main/assets/icons/InfoOutline.svg)) naast elke activiteitennaam om meer informatie over die activiteit in een pop-up kaart, met inbegrip van [!UICONTROL Activity ID], [!UICONTROL Activity Objective], [!UICONTROL Activity Location], [!UICONTROL Goal], en [!UICONTROL Status] te bekijken.<P>Klik het **[!UICONTROL More actions]** pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) naast elke activiteitennaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren. De volgende handelingen zijn beschikbaar (afhankelijk van uw machtigingen en de activiteitsstatus): [!UICONTROL Edit], [!UICONTROL Activate], [!UICONTROL Deactivate], [!UICONTROL Copy], [!UICONTROL Delete] en [!UICONTROL Archive] .<P>Voor meer informatie over elke actie, zie [&#x200B; snelle acties &#x200B;](#quick-actions) hieronder uitvoeren.<P>Klik op de tabelkop om de lijst alfabetisch te sorteren in oplopende of aflopende volgorde op naam. |
| [!UICONTROL Status] | De status van de activiteit kan een van de volgende zijn:<ul><li>**[!UICONTROL Live]**: De activiteit wordt momenteel uitgevoerd.</li><li>**[!UICONTROL Scheduled]**: De activiteit kan worden geactiveerd wanneer de opgegeven begindatum en -tijd aankomen.</li><li>**[!UICONTROL Inactive]**: De activiteit is gepauzeerd of gedeactiveerd.</li><li>**[!UICONTROL Ended]**: De opgegeven einddatum en -tijd van de activiteit zijn bereikt en de activiteit wordt niet meer uitgevoerd.</li><li>**[!UICONTROL Archived]**: De activiteit is gearchiveerd. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.</li></ul>**Nota**: Wanneer u bepaalde acties, zoals het activeren van een activiteit buiten [!DNL Target] UI gebruikend API methodes uitvoert, kan de update tot tien minuten nemen om aan [!DNL Target] UI te verspreiden. |
| [!UICONTROL Last Updated] | De datum en het tijdstip waarop de activiteit voor het laatst is bijgewerkt en door wie.<P>Klik op de tabelkop om de lijst op datum in oplopende of aflopende volgorde te sorteren. |
| [!UICONTROL Priority] | De prioriteit van de activiteit.<P>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.<P>Afhankelijk van uw [&#x200B; montages &#x200B;](/help/main/administrating-target/reporting.md), variëren [!DNL Target] UI en de opties voor [!UICONTROL Priority]. U kunt de oudere instellingen van [!UICONTROL Low] , [!UICONTROL Medium] of [!UICONTROL High] gebruiken of u kunt fijngeoriënteerde prioriteiten van 0 tot en met 999 inschakelen.<P>Voor meer informatie over prioritaire montages, zie [&#x200B; Prioriteit &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#section_DCBDC354261F420EBD4B43EA34947BAC) onder *Montages van de Activiteit* in *Doelen en montages*. |
| [!UICONTROL Property] | Toont het [&#x200B; bezit &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) voor de activiteit.<P>De gebruikerstoestemmingen van de onderneming zijn a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) eigenschap. |
| [!UICONTROL Estimated Lift in Revenue] | Toont de voorspelde toename van inkomsten als 100% van het publiek de winnende ervaring ziet.<P>Berekend met de volgende formule:<P>`(<winning experience> - <control experience>)*<total number of visitors>`<P>Dit getal wordt afgerond tot op één decimaal (maximaal) als het versmalde formulier slechts één cijfer voor het decimaalteken heeft. Bijvoorbeeld: $1,6M, $60K, $900, $8,5K, $205K<P>Deze kolom toont &quot;—&quot; voor activiteiten die niet genoeg gegevens hebben om een winnaar te roepen of geen kostenraming hebben.<P>Zie [&#x200B; Schatting Lift in Inkomsten &#x200B;](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor meer informatie. |
| [!UICONTROL Source] | Toont waar de activiteit werd gecreeerd: [!DNL Adobe Target], [&#x200B; Adobe Target API &#x200B;](https://experienceleague.adobe.com/nl/docs/target-dev/developer/overview), [&#x200B; Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform.html?lang=nl-NL), [&#x200B; Adobe Experience Manager &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=nl-NL), of [&#x200B; Adobe Mobiele Diensten &#x200B;](https://developer.adobe.com/client-sdks/documentation/). |
| [!UICONTROL Author] | De naam van de persoon die de activiteit heeft gemaakt. |
| [!UICONTROL Decisioning Method] | De besluitvormingsmethode die in elke activiteit wordt gebruikt: [&#x200B; server-Kant &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=nl-NL) of [&#x200B; cliënt-Kant &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html?lang=nl-NL). |

<!--|[!UICONTROL Location]|The URL for the activity identifies where the activity is displayed. This column helps you quickly identify an activity and determine whether a particular page already has an activity running on it.<P>If an activity runs on multiple URLs, a link shows how many more URLs are used. Click the link to view the complete list of URLs for that activity.<P>You can search based on the URL. Use the drop-down list next to the search box and select [!UICONTROL URL].|-->

## Typen activiteiten {#types}

[!DNL Target] bevat verschillende typen activiteiten. In de volgende tabel vindt u een overzicht van elk type activiteit met koppelingen voor meer informatie. Om u beter te helpen het beste activiteitstype voor uw doeleinden kiezen, gebruik de [&#x200B; Gids van de Activiteiten van Adobe Target &#x200B;](/help/main/c-activities/target-activities-guide.md).

| Type activiteit | Beschrijving |
|--- |--- |
| [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md) | Bij een A/B-test worden twee of meer versies van uw website-inhoud vergeleken om te zien welke versie uw conversies het beste verbetert tijdens een vooraf opgegeven testperiode. |
| [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | [!UICONTROL Auto-Allocate], een type van test A/B, identificeert een winnaar onder twee of meer ervaringen en wijst automatisch meer verkeer aan de winnaar toe om omzettingen te verhogen terwijl de test blijft lopen en leren. |
| [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)<P>![&#x200B; Target Premium &#x200B;](/help/main/assets/premium.png) | Auto-Target, een type A/B test, gebruikt geavanceerd machine leren om veelvoudige high-performance marketer-bepaalde ervaringen te identificeren, en dient de meest op maat gemaakte ervaring aan elke bezoeker die op het profiel van de individuele klant en het gedrag van vorige bezoekers met gelijkaardige profielen wordt gebaseerd, om inhoud en aandrijvingsomzettingen te personaliseren. |
| [[!UICONTROL Multivariate Test]](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | [!UICONTROL Multivariate Testing] (MVT) vergelijkt combinaties aanbiedingen in elementen op een pagina om te bepalen welke combinatie het beste voor een specifiek publiek presteert, en identificeert welk element het meest van invloed is op het succes van de activiteit. |
| [[!UICONTROL Experience Targeting]](/help/main/c-activities/t-experience-target/experience-target.md) | [!UICONTROL Experience Targeting] (XT) levert inhoud aan een specifiek publiek dat op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd. |
| [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<P>![&#x200B; Target Premium &#x200B;](/help/main/assets/premium.png) | [!UICONTROL Automated Personalization] (AP) combineert aanbiedingen of berichten en maakt gebruik van geavanceerd computerleren om verschillende verschillen met elke bezoeker op basis van hun individuele klantprofiel met elkaar in overeenstemming te brengen, om inhoud en schijfconversies aan te passen. |
| [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)<P>![&#x200B; Target Premium &#x200B;](/help/main/assets/premium.png) | Een aanbeveling bepaalt hoe een product aan een websitebezoeker wordt voorgesteld, afhankelijk van de activiteiten van die bezoeker op de plaats.<P>U kunt bijvoorbeeld mensen die een rugzak kopen aanmoedigen om wandelschoenen en wandelstokken te kopen. U kunt een aanbeveling maken die items toont die vaak samen worden aangeschaft met het algoritme &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. U kunt bezoekers ook aanmoedigen om meer tijd te besteden aan uw mediasite door vergelijkbare video&#39;s aan te bevelen als de video die ze bekijken. Gebruik hiervoor het algoritme &quot;Personen die dit hebben bekeken&quot;.<P>**NOTA**: U kunt aanbevelingen binnen [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Experience Targeting] (XT) activiteiten ook omvatten. Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md). Deze functionaliteit vereist dat u de vergunning van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt. |

## Filters toepassen op de lijst Activiteiten {#filters}

De filters van de toegang door het **[!UICONTROL Show Filters]** pictogram ( ![&#x200B; te klikken tonen het pictogram van Filters &#x200B;](/help/main/assets/icons/Filter.svg)) dichtbij de bovenkant van de lijst.

In het menu kunt u activiteiten filteren op de volgende kenmerken:

| Kenmerk | Details |
| --- | --- |
| [!UICONTROL Type] | Filter door [&#x200B; type van activiteit &#x200B;](#types). |
| [!UICONTROL Status] | Filteren op activiteitsstatus.<ul><li>**[!UICONTROL Live]**: De activiteit wordt momenteel uitgevoerd.</li><li>**[!UICONTROL Scheduled]**: De activiteit kan worden geactiveerd wanneer de opgegeven begindatum en -tijd aankomen.</li><li>**[!UICONTROL Inactive]**: De activiteit is gepauzeerd of gedeactiveerd.</li><li>**[!UICONTROL Ended]**: De opgegeven einddatum en -tijd van de activiteit zijn bereikt en de activiteit wordt niet meer uitgevoerd.</li><li>**[!UICONTROL Archived]**: De activiteit is gearchiveerd. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.</li></ul>Zie de opmerking onder deze tabel voor meer informatie over de afgekeurde statussen [!UICONTROL Save as Draft] en [!UICONTROL Syncing] . |
| [!UICONTROL Reporting Source] | Filteren op bron rapporteren.<ul><li>[[!DNL Analytics]](/help/main/c-integrating-target-with-mac/a4t/a4t.md): activiteiten weergeven die [!UICONTROL Analytics for Target] (A4T) als rapportagebron gebruiken.</li><li>[[!DNL Target]](/help/main/c-reports/reports.md): activiteiten weergeven die [!DNL Target] als bron voor rapportage gebruiken.</li><li>[[!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md): activiteiten weergeven die [!DNL Adobe Customer Analytics] als bron voor rapportage gebruiken.</li></ul> |
| [!UICONTROL Experience Composer] | Filter op basis waarvan de ervaring met composer is gebruikt tijdens het maken van activiteiten:<ul><li>[&#x200B; Visueel &#x200B;](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md): De activiteiten van vertoningen die gebruikend [!UICONTROL Visual Experience Composer] (VEC) werden gecreeerd.</li><li>[&#x200B; Gebaseerde Vorm &#x200B;](/help/main/c-experiences/form-experience-composer.md): De activiteiten van de vertoning die gebruikend [!UICONTROL Form-Based Experience Composer] werden gecreeerd.</li></ul> |
| [!UICONTROL Metrics Type] | Filter waardoor [&#x200B; metrisch succes &#x200B;](/help/main/c-activities/r-success-metrics/success-metrics.md) tijdens activiteitenverwezenlijking werd gekozen.<ul><li>[!UICONTROL Conversion]</li><li>[!UICONTROL Revenue]</li><li>[!UICONTROL Engagement]</li><li>[!UICONTROL Use an Analytics metric]</lI></ul> |
| [!UICONTROL Decisioning Method] | Filter op de beslissingsmethode die in elke activiteit wordt gebruikt.<ul><li>[&#x200B; server-kant &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/on-device-decisioning/overview.html?lang=nl-NL): De activiteiten van de vertoning die server-zijbeslissing gebruiken.</li><li>[&#x200B; cliënt-Kant &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/on-device-decisioning/on-device-decisioning.html?lang=nl-NL): De activiteiten van de vertoning die cliënt-zijbeslissing gebruiken.</li></ul> |
| [!UICONTROL Activity Source] | Filteren op de activiteitsbron die wordt gebruikt om elke activiteit te maken.<ul><li>[!DNL Adobe Target]</li><li>[[!DNL Adobe Target]  API &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/overview.html?lang=nl-NL)</li><li>[[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=nl-NL)</li><li>[[!DNL Adobe Experience Manager]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=nl-NL)</li><li>[[!DNL Adobe Mobile Services]](https://developer.adobe.com/client-sdks/home/)</li></ul> |
| [!UICONTROL Property] | Filter door het [&#x200B; bezit &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) waarin de activiteit werd gecreeerd. |


>[!NOTE]
>
>**Update op activiteitenstaten in bijgewerkte UI**: Met de recentste updates aan het gebruikersinterface, zijn de [!UICONTROL Save as Draft] en [!UICONTROL Syncing] staten niet meer beschikbaar. Dit komt omdat alle activiteiten nu direct in het back-end [!DNL Target] leveringssysteem worden gemaakt en bewerkt met de GraphQL-laag, waardoor een gestroomlijnder en efficiënter proces wordt gegarandeerd.
>
>Eerder werden activiteiten eerst opgeslagen in de [!DNL Target] frontend en vervolgens gesynchroniseerd met het back-end [!DNL Target] -leveringssysteem, waarvoor deze tussenliggende staten vereist waren. Aangezien dit niet langer het geval is, zijn deze staten geschrapt.
>
>[!DNL Adobe] begrijpt dat sommige klanten belangstelling hebben getoond voor de functie [!UICONTROL Save as Draft] . Deze feedback wordt momenteel niet ondersteund.

## Snelle handelingen uitvoeren {#quick-actions}

Klik het **[!UICONTROL More actions]** pictogram ( ![&#x200B; Meer actiemenu &#x200B;](/help/main/assets/icons/MoreVertical.svg)) naast elke activiteitennaam om een menu te openen dat u snelle acties op een activiteit laat uitvoeren.

De volgende acties zijn beschikbaar (afhankelijk van uw machtigingen en de activiteitsstatus):

| Handeling | Beschrijving |
| --- | --- |
| [!UICONTROL Edit] | Wijzig de activiteit. Elke activiteit kan worden bewerkt.<P>Voor meer informatie over de diverse manieren kunt u activiteiten uitgeven, zie [&#x200B; een activiteit uitgeven of sparen als ontwerp &#x200B;](/help/main/c-activities/edit-activity.md). |
| [!UICONTROL Deactivate] | Stop een live of geplande activiteit. Een gedeactiveerde activiteit kan opnieuw worden geactiveerd of worden gearchiveerd.<P>Als u een activiteit deactiveert of archiveert en deze later opnieuw activeert, blijft een bezoeker deel uitmaken van die activiteit nadat de activiteit opnieuw is geactiveerd, als hij of zij zich daarin bevond voordat de activiteit werd gedeactiveerd of gearchiveerd. Alle conversiemetriek die tijdens de tijd tussen de twee gebeurtenissen is vastgelegd, worden niet aan die activiteit toegewezen. |
| [!UICONTROL Activate] | Start een inactieve activiteit of een activiteit die klaar is om te worden geactiveerd. |
| [!UICONTROL Archive] | Verzend de activiteit naar het archief. Gearchiveerde activiteiten worden standaard niet meer weergegeven in de lijst [!UICONTROL Activities] . Wijzig het filter voor de lijst [!UICONTROL Activities] om gearchiveerde activiteiten op te nemen om deze weer te geven. U kunt een gearchiveerde activiteit activeren om deze opnieuw te gebruiken.<P>Als u een activiteit deactiveert of archiveert en deze later opnieuw activeert, blijft een bezoeker deel uitmaken van die activiteit na de reactivering als hij of zij die activiteit had voordat deze werd gedeactiveerd of gearchiveerd. Alle conversiemetriek die tijdens de tijd tussen de twee gebeurtenissen is vastgelegd, worden niet aan die activiteit toegewezen. |
| [!UICONTROL Copy] | Kopieer een activiteit. Elke activiteit kan worden gekopieerd. Wanneer u een activiteit kopieert, wordt er een nieuwe activiteit met dezelfde naam gemaakt, die wordt toegevoegd met &quot;Copy&quot;. Een test met de naam &quot;Browser Offers&quot; wordt bijvoorbeeld gekopieerd naar &quot;Browser Offers Copy&quot;.<P>Visuele aanbiedingen worden gekopieerd met de activiteit. U kunt de voorstellen in de kopie veilig bewerken zonder dat dit invloed heeft op de oorspronkelijke activiteit. De enige uitzondering hierop vormen de opgeslagen aanbiedingen en afbeeldingen in de map Content/Assets. |
| [!UICONTROL Delete] | Een concept of activiteit verwijderen.<P>**NOTA**: De geschrapte activiteiten kunnen niet worden teruggekregen. Gebruik de handeling [!UICONTROL Archive] , tenzij u zeker weet dat u deze activiteit nooit meer nodig hebt. U kunt de activiteit dan opnieuw activeren indien nodig. |

## Overwegingen

Let op het volgende over de [!UICONTROL Activity] lijst:

* [!UICONTROL Archived] - en [!UICONTROL Ended] -activiteiten worden niet weergegeven in de lijst [!UICONTROL Activities] . Om deze activiteiten te bekijken, filter hen gebruikend het [&#x200B; pictogram van Filters &#x200B;](#filters) ( ![&#x200B; toon het pictogram van Filters &#x200B;](/help/main/assets/icons/Filter.svg)) bij de bovenkant van de lijst.
* Wanneer een activiteit die oorspronkelijk in [!DNL Target Classic] is gemaakt, wordt gedeactiveerd of verwijderd, wordt deze verwijderd uit [!DNL Target Standard/Premium] . Verwijderde activiteiten die oorspronkelijk in [!DNL Target Classic] zijn gemaakt, worden niet verzonden naar de map [!UICONTROL Archive] in [!DNL Target Standard/Premium] . De functionaliteit voor gearchiveerde mappen is alleen van toepassing op activiteiten die zijn gemaakt in [!DNL Target Standard/Premium] .
* Alle andere activiteitstypen dan [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] geven u de keuze om [!DNL Target] of [!DNL Adobe Analytics] als gegevensbron te gebruiken. [!UICONTROL Automated Personalization], [!UICONTROL Auto-Allocate], en [!UICONTROL Auto-Target] *gebruiken altijd* [!DNL Target] gegevens.
* De activiteiten zijn beschikbaar voor verschillende kanalen:

   * Websites en mobiele sites
   * Schermen en apparaten met internetverbinding, waaronder kiosken en geldautomaten
   * E-mail en andere verwervingskanalen of partnerplaatsen
   * Mobiele apps
   * Overal waar u gecodeerde inhoud kunt leveren

## Beperkingen {#section_049D4684403A4E07B998067EB8E9BE56}

Elke [!DNL Target] -activiteit heeft de volgende inhoudsbeperkingen:

| Item | Limiet |
|--- |--- |
| Unieke kiezers | 300 wanneer een kiezer in een andere ervaring wordt herhaald, wordt deze eenmaal meegeteld. Als het echter in dezelfde ervaring wordt herhaald, wordt het opnieuw geteld. |
| Aanbiedingen in elke ervaring | 350 |
| Klik op kiezers bijhouden in metriek | 50 |
| Mboxen in metriek | 50 |
| Soorten publiek en locaties | 50 combinaties van soorten publiek en locaties (mbox) mogen niet meer dan 50 zijn. |

De activiteit kan niet worden bewaard als u om het even welk van deze grenzen overschrijdt.

Als u het aantal van deze items in uw activiteit vergroot, neemt ook de tijd toe die nodig is om de activiteit in [!DNL Target] te synchroniseren.

Voor extra grenzen van [!UICONTROL Visual Experience Composer] (VEC), zie [&#x200B; de Beperkingen van de Composer van de Visuele Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/experience-composer-best-practices.md#section_F33C2EA27F2E417AA036BC199DD6C721).

## Attributen geïmporteerd in [!DNL Target] voor activiteiten bijgewerkt buiten [!DNL Target] {#section_802B0D174E6A44E1A96F404CA81AAE44}

Als in [!DNL Target] gemaakte activiteiten van buiten [!DNL Target] (bijvoorbeeld via API) worden bijgewerkt, worden de volgende activiteitskenmerken weer geïmporteerd in [!DNL Target] : `thirdpartyId` , `startDate` , `endDate` , `status` , `priority` en `marketingCloudMetadata(remoteModifiedBy)` .

Deze importtaak wordt uitgevoerd wanneer de lijst [!UICONTROL Activities] wordt geopend, met een maximale vertraging van tien minuten.

