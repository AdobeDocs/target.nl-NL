---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release van Adobe Target (huidige) '
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 322b14629d420601b763fed7597c43a8458b7dbf
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---


# Opmerkingen bij de release van Target (huidige){#target-release-notes-current}

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke release van Target Standard en Target Premium. Daarnaast worden releaseopmerkingen voor Target API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020 zullen alle aanroepen van mbox.js op elegante wijze mislukken en van invloed zijn op uw pagina&#39;s waarop Target-activiteiten worden uitgevoerd door de standaardinhoud te bedienen. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.
   >
   >
* **Aankondigingen** van Target: Zie de Target-aankondigingspagina voor informatie over aanstaande gebeurtenissen, zoals Target Skill Builder-sessies, ontwikkelaarstekkers, webinars en Target Coffee Break-sessies. Zie [Target-aankondigingen](/help/r-release-notes/target-announcements.md)voor meer informatie.


De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

## Target Standard/Premium 20.5.1 (17 juni 2020)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Analytics for Target (A4T)-ondersteuning voor [!UICONTROL Auto-Allocate] activiteiten | [!UICONTROL Auto-Allocate] activiteiten ondersteunen nu [Analytics voor Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Deze integratie staat u toe om het [!UICONTROL Auto-Allocate] multi-gewapende bandit vermogen te gebruiken om verkeer aan het winnen van ervaringen te drijven, terwijl het gebruiken van een [!UICONTROL Adobe Analytics] doel metrisch en/of [!UICONTROL Adobe Analytics] rapporteringsen analysemogelijkheden.<br>Als u A4T [al hebt](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) geïmplementeerd voor gebruik met A/B Test and Experience Targeting-activiteiten, bent u klaar!<br>Zie [Analytics for Target (A4T)-ondersteuning voor Auto-Allocate-activiteiten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) in *Activity creation* voor meer informatie. |
| De tokens van de reactie voor de Methode van de Toewijzing van het Verkeer voor auto-Target en Geautomatiseerde Personalisatieactiviteiten | Er zijn twee [reactietokens](/help/administrating-target/response-tokens.md) toegevoegd aan [!UICONTROL Auto-Target] en [!UICONTROL Automated Personalization] activiteiten om te kunnen bepalen of een bezoeker een bepaalde ervaring heeft opgedaan als gevolg van zijn toewijzing aan &quot;controle&quot; of aan &quot;gericht&quot; verkeer.<ul><li>`experience.trafficAllocationId` 0 als een bezoeker ervaring heeft opgedaan met &quot;controle&quot;-verkeer en 1 als een bezoeker een ervaring heeft opgedaan met &quot;gerichte&quot; verkeersdistributie.</li><li>`experience.trafficAllocationType` retourneert &quot;control&quot; of &quot;target&quot;.</li></ul>Voor meer informatie over controle versus gericht verkeer, zie [Selecteer de controle voor uw Geautomatiseerde Personalisatie of auto-Target activiteit](/help/c-activities/t-automated-personalization/experience-as-control.md). |
| [!UICONTROL Publisher] rol | Deze nieuwe rol is vergelijkbaar met de huidige [!UICONTROL Observer] rol (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De [!UICONTROL Publisher] rol heeft echter de extra toestemming om activiteiten te activeren.<br>Zie voor meer informatie: <ul><li>**Target Standard-gebruikers**: [Geef rollen en machtigingen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) op in *Gebruikers*.</li><li>**Target Premium-gebruikers**: [Stap 6: Specificeer rollen en toestemmingen](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configure ondernemingstoestemmingen*.</li></ul> |
| A4T-ondersteuning op 25 [!DNL Analysis Workspace]<br>juni 2020 | [!UICONTROL Anaytics for Target] (A4T) wordt nu ondersteund in [!DNL Analysis Workspace]. Met [!UICONTROL Analytics for Target (A4T) panel] deze functie kunt u uw [!DNL Adobe Target] activiteiten en ervaringen analyseren in [!DNL Analysis Workspace].<br>Zie [Rapporten in Analytics](/help/c-integrating-target-with-mac/a4t/reporting.md) in *A4T-rapportage* en het deelvenster [Target (A4T) in de](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics Tools Guide ** voor meer informatie. |

### Verbeteringen, correcties en wijzigingen

* Probleem verholpen waarbij de metrische waarde &quot;bezoekers&quot; werd opgeslagen in de definitie van de activiteit in plaats van &quot;UniqueVisitors&quot;. (TGT-37098)
* Probleem verholpen in de [!DNL Target] gebruikersinterface die ervoor zorgde dat de verticale schuifbalk niet correct op de [!UICONTROL Audiences] pagina werkte. (TGT-36968)

## releases (15 juni 2020) om 1.js 1.8.2 en om 2.3.1.

De volgende verbeteringen en correcties zijn aangebracht in de bibliotheken [!DNL Target] at.js:

| Functie/verbetering | Beschrijving |
| --- | --- |
| om.js 1.8.2 | Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:<ul><li>Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 1.*x* zou tot het serverdomein verkeerd kunnen leiden, dat in het [!DNL Target] verzoek mislukte. (TNT-35064)</li></ul>Zie [de versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)at.js voor meer informatie. |
| om.js 2.3.1 | Deze versie van at.js is een onderhoudsrelease en bevat de volgende verbeteringen en oplossingen:<ul><li>De `deviceIdLifetime` instelling is overschreven via [targetGlobalSettings](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md). (TNT-36349)</li><li>Probleem verholpen bij gebruik van CNAME en randoverschrijving, op .js 2.*x* zou tot het serverdomein verkeerd kunnen leiden, dat in het [!DNL Target] verzoek mislukte. (TNT-35065)</li><li>Probleem verholpen bij het gebruik van de [!DNL Target] extensie v2 en de [!DNL Launch] [!DNL Adobe Analytics] extensie, [!DNL Launch] waarmee de [!DNL Target][!DNL Analytics] `sendBeacon` aanroep werd vertraagd. (TNT-36407, TNT-35990, TNT-36000)</li></ul>Zie [de versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)at.js voor meer informatie. |

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [Opmerkingen bij de release - Target server-side API&#39;s](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Opmerkingen bij de release met betrekking tot API&#39;s van de Adobe Target-server. |
| [Opmerkingen bij de release - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Release-aantekeningen met betrekking tot Adobe Target Node.js SDK. |
| [Opmerkingen bij de release - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Opmerkingen bij de release met betrekking tot de Adobe Target Java SDK. |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek van Adobe Target at.js. |
| [mbox.js, versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | Op deze pagina worden wijzigingen in elke versie van mbox.js weergegeven.<br>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten van mbox.js naar at.js migreren. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release van Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie [Documentatiewijzigingen](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C)voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in vorige versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de [Versie voor vorige versies](../r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release van [Experience Cloud voor meer informatie](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html). |

## Prerelease-informatie {#section_5D588F0415A2435B851A4D0113ACA3A0}

Met de volgende bronnen kunt u zien wat er in de volgende Target-release komt.

| Resource | Details |
|--- |--- |
| Update-lijst voor producten van Adobe Priority | Meld u aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de Target-releases van deze maand, waaronder pre-releasegegevens, raadpleegt u de [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
