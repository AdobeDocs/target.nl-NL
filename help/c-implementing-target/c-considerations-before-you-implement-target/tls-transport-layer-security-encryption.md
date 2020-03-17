---
keywords: tls;tls 1.0;transport layer security;encryption;tls 1.1;tls 1.2
description: Informatie over veranderingen in hoe Adobe en het Doel TLS (de Veiligheid van de Laag van het Vervoer) gebruiken om de hoogste veiligheidsnormen te handhaven en de veiligheid van klantengegevens te bevorderen.
title: De encryptieveranderingen van TLS (de Veiligheid van de Laag van het Vervoer)
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
translation-type: tm+mt
source-git-commit: 5b13ad02691a685dd76db2b390e030f8aef30dd9

---


# De encryptieveranderingen van TLS (de Veiligheid van de Laag van het Vervoer){#tls-transport-layer-security-encryption-changes}

Informatie over veranderingen in hoe Adobe en het Doel van Adobe TLS (de Veiligheid van de Laag van het Vervoer) gebruiken om de hoogste veiligheidsnormen te handhaven en de veiligheid van klantengegevens te bevorderen.

De Veiligheid van de Laag van het vervoer (TLS) is het wijdst opgestelde veiligheidsprotocol dat vandaag voor Webbrowsers en andere toepassingen wordt gebruikt die gegevens vereisen om veilig over een netwerk worden geruild. Adobe heeft normen voor beveiligingscompatibiliteit die het einde van de levensduur van oudere protocollen vereisen en die het gebruik van TLS 1.2 verplicht stellen om de meest actuele en veilige versie in gebruik te hebben.

>[!IMPORTANT]
>
>Na 1 maart 2020 biedt Adobe Target geen ondersteuning meer voor TLS 1.1-codering voor Visual Experience Composer (VEC), Enhanced Experience Composer (EEC), activity delivery, API&#39;s, enz. Upgrade vóór 1 maart 2020 naar TLS 1.2 om problemen te voorkomen.

We verwachten niet dat dit een aanzienlijke invloed zal hebben op klantgegevens of rapportage.

## Visual Experience Composer (VEC) met Enhanced Experience Composer (EEC) Enabled {#section_B374B62DEC3344C194AC7BECC2EE0AA0}

TLS 1.2 is de standaard vanaf 1 maart 2020 en TLS 1.1 wordt niet meer ondersteund.

Adobe verplaatst klanten geleidelijk naar TLS 1.2. Voor degenen, wier domeinen reeds 1.2 volgzaam zijn, zullen wij hen naar TLS 1.2 zonder enige veranderingen verplaatsen nodig van u. De meeste klantdomeinen ondersteunen reeds TLS 1.2; als uw domein echter geen TLS 1.2 ondersteunt, behouden we deze domeinen op TLS 1.1 zoals vandaag (tot maart 2020).

Tijdens deze migratiefase mag u geen enkel probleem tegenkomen. Als VEC ophoudt ladend een plaats die vroeger werkte, [open een kaartje](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) van de Zorg van de Cliënt die deze migratie als mogelijke oorzaak citeert.

Als u echter een van deze klanten bent die op TSL 1.1 werken zonder TLS 1.2 te ondersteunen, moet u plannen voor het verplaatsen van uw domeinen/infrastructuur naar TLS 1.2. We zullen het TLS 1.1-protocol blijven ondersteunen tot 1 maart 2020. Vanaf 1 maart 2020 biedt Target geen ondersteuning voor het TLS 1.1-protocol dat via de Enhanced Experience Composer-functie voor de VEC moet worden gebruikt.

Hoewel wij iedereen ten zeerste adviseren om op TLS 1.2 vooruit te zijn, als u een nieuwe klant bent maar *GEEN* steun TLS 1.2 steunt, te contacteren aan de Zorg van de Klant die hen meedeelt dat u op TLS 1.1 voor de Verbeterde Composer van de Ervaring moet zijn. Overstappen naar TLS 1.2 is echter niet mogelijk, aangezien u ook na 1 maart 2020 geen ondersteuning meer krijgt.

## Levering van activiteiten {#section_46CA5943E4354B259014C2BF340AECD6}

Vanaf 1 maart 2020 ondersteunen doelservers TLS 1.1 niet meer. Met deze wijziging accepteren de doelservers geen aanvragen meer van bezoekers met oudere apparaten of webbrowsers die geen TLS 1.2 (of hoger) ondersteunen. Als gevolg hiervan ontvangen oudere apparaten en browsers die alleen TLS 1.1 ondersteunen (of standaard TLS 1.1 ondersteunen) geen activity-inhoud van Adobe Target. De standaardinhoud van de site wordt weergegeven.

Tot de oudere apparaten en browsers die worden beïnvloed behoren:

* Google Chrome (Chrome voor Android) versie 29 en lager
* Opera Browser (Opera Mobile) versie 12.17 en eerdere versies
* Mozilla Firefox (Firefox voor mobiele apparaten) versie 26 en lager
* Android 4.3 en eerdere versies
* Internet Explorer 8-10 in Windows 7 en eerdere versies
* Internet Explorer 10 op Windows Phone 8.0
* Safari 6.0.4/OS X10.8.4 en eerdere versies

Overweeg het volgende terwijl u deze wijziging wilt uitvoeren (de deadline van 1 maart 2020 beïnvloedt al deze items):

* U moet ervoor zorgen dat uw standaardsite gereed is op een manier die geschikt is voor compatibele apparaten en browsers.
* Houd er rekening mee dat het aantal bezoekers in uw doelrapporten mogelijk een onbeduidende daling van het aantal bezoekers kan zien.
* Mogelijk moet u het publiek wijzigen dat specifiek is gemaakt voor oudere apparaten of browsers die geen TLS 1.2 ondersteunen. Levering aan deze apparaten en browsers werkt niet meer.

Zie [Ondersteunde browsers](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100)voor meer informatie over ondersteunde browsers en hun versies.

## Adobe Target-API&#39;s {#section_88797FA5434049EC89F908853CC76903}

Vanaf 1 maart 2020 bieden doel-API&#39;s geen ondersteuning meer voor TLS 1.1-codering. Klanten die toegang hebben tot de API moeten controleren of dit geen gevolgen heeft.

* API-clients die Java 7 met standaardinstellingen gebruiken, moeten worden gewijzigd om TLS 1.2 te ondersteunen. Zie &#39;&#39;Standaardversie van TLS-protocol voor eindpunten van clients [wijzigen&#39;&#39; voor meer informatie: TLS 1.0 tot TLS 1.2](https://www.java.com/en/configure_crypto.html)&quot; op de Java-website.
* API-clients die Java 8 gebruiken, moeten niet worden beïnvloed omdat de standaardinstelling TLS 1.2 is.
* API-clients die andere frameworks gebruiken, moeten contact opnemen met hun leveranciers voor meer informatie over TLS 1.2-ondersteuning.

## Toegang tot de interfaces van de Oplossingen van de Wolk {#section_748870ADE77B4CBEB18518DC784E64E5}

Omdat voor de interface Target Standard/Premium al een [moderne webbrowser](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100)is vereist, zijn er geen problemen te verwachten. Als u geen verbinding kunt maken met Target, moet u de browser upgraden naar de meest recente versie.

## Controleren welke TLS-versie uw browser gebruikt {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

U kunt als volgt de TLS-versie op uw website controleren met Google Chrome:

1. Open de desbetreffende website in Chrome.
1. Klik in het menu Chrome (de drie verticale ovalen) op Meer gereedschappen > Gereedschappen voor ontwikkelaars.

   ![Chrome Developer Tools](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-developer-tools.png)

1. Open het tabblad Beveiliging en bekijk vervolgens de TLS-versiegegevens onder Verbinding:

   ![TLS-versiedetails](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/chrome-tls-version.png)

>[!NOTE]
>
>Deze instructies zijn actueel vanaf de publicatie en kunnen worden gewijzigd. Een snelle internetzoekactie moet helpen als deze instructies veranderen.  Andere browsers hebben vergelijkbare stappen.

## Verwacht gedrag bij browsers die TLS-versies onder 1.2 ondersteunen {#section_B5DA97A34EF248EB927610A5DA71EF2F}

In deze sectie wordt beschreven wat u alleen kunt verwachten bij browsers die TLS-versies onder 1.2 ondersteunen bij het gebruik van een at.js- of mbox.js-implementatie. Ter vergelijking wordt in deze sectie ook beschreven wat u kunt verwachten bij browsers die TLS 1.2 ondersteunen.

### Centrale eindpunten

| Doel JavaScript-implementatie | Details |
|--- |--- |
| at.js | Als TLS 1.0 of TLS 1.1 is ingeschakeld:<ul><li>Gebruikend browser ontwikkelt hulpmiddelen, op het lusje van het Netwerk, zult u &quot;200 O.K.&quot;zien. Dit betekent dat het verzoek is ingewilligd.</li><li>De gebruiker ziet een bericht &quot;Kan niet veilig met deze pagina verbinden&quot;. In het bericht wordt uitgelegd dat dit kan worden veroorzaakt omdat de site verouderde of onveilige TLS-beveiligingsinstellingen gebruikt.</li><li>Er worden geen consolefouten weergegeven.</li></ul>Met TLS 1.2 ingeschakeld:<ul><li>bestand at.js wordt gedownload.</li></ul> |
| mbox.js | Als TLS 1.0 of TLS 1.1 is ingeschakeld:<ul><li>Gebruikend browser ontwikkelt hulpmiddelen, op het lusje van het Netwerk, zult u &quot;200 O.K.&quot;zien. Dit betekent dat het verzoek is ingewilligd.</li><li>De gebruiker ziet een bericht &quot;Kan niet veilig met deze pagina verbinden&quot;. In het bericht wordt uitgelegd dat dit kan worden veroorzaakt omdat de site verouderde of onveilige TLS-beveiligingsinstellingen gebruikt.</li><li>Er worden geen consolefouten weergegeven.</li></ul>Met TLS 1.2 ingeschakeld:<ul><li>het bestand mbox.js wordt gedownload.</li></ul> |

### Eindpunten rand

| Doel JavaScript-implementatie | Details |
|--- |--- |
| at.js | Als TLS 1.0 of TLS 1.1 is ingeschakeld:<ul><li>Gebruikend browser ontwikkelt hulpmiddelen, op het lusje van het Netwerk, zult u &quot;200 O.K.&quot;zien. Dit betekent dat het verzoek is ingewilligd.</li><li>De gebruiker ziet een bericht &quot;Kan niet veilig met deze pagina verbinden&quot;. In het bericht wordt uitgelegd dat dit kan worden veroorzaakt omdat de site verouderde of onveilige TLS-beveiligingsinstellingen gebruikt.</li><li>Er worden geen consolefouten weergegeven.</li><li>De standaardinhoud wordt weergegeven.</li></ul>Met TLS 1.2 ingeschakeld:<ul><li>Inhoud van voorstel wordt weergegeven.</li></ul> |
| mbox.js | Als TLS 1.0 of TLS 1.1 is ingeschakeld:<ul><li>Gebruikend browser ontwikkelt hulpmiddelen, op het lusje van het Netwerk, zult u &quot;200 O.K.&quot;zien. Dit betekent dat het verzoek is ingewilligd.</li><li>De gebruiker ziet een bericht &quot;Kan niet veilig met deze pagina verbinden&quot;. In het bericht wordt uitgelegd dat dit kan worden veroorzaakt omdat de site verouderde of onveilige TLS-beveiligingsinstellingen gebruikt.</li><li>Er worden geen consolefouten weergegeven.</li><li>De standaardinhoud wordt weergegeven.</li></ul>Met TLS 1.2 ingeschakeld:<ul><li>Aanbiedingsinhoud is verzonden</li></ul> |

### Activiteit gericht met browser-versie publiek (Internet Explorer, Versies 6, 7, of 8)

>[!NOTE]
>
>Het publiek werkt niet meer.

| Doel JavaScript-implementatie | Details |
|--- |--- |
| at.js | at.js wordt niet ondersteund in versies van Internet Explorer ouder dan versie 10. |
| mbox.js | Als TLS 1.0 of TLS 1.1 is ingeschakeld:<ul><li>De standaardinhoud wordt weergegeven.</li><li>Geen doelverzoeken worden geactiveerd.</li><li>Er wordt geen consolefout weergegeven.</li><li>Gebruikend browser ontwikkelt hulpmiddelen, op het lusje van het Netwerk, zult u &quot;200 O.K.&quot;zien. Dit betekent dat het verzoek is ingewilligd.</li></ul>Met TLS 1.2 ingeschakeld:<ul><li>Inhoud van voorstel wordt weergegeven.</li></ul> |