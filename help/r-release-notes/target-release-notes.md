---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-releases.
title: Voorlopige Adobe Target-opmerkingen
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---


# Opmerkingen bij de release van Target (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 17 juni 2020**

Zie Opmerkingen bij de release van [Target voor informatie over de huidige release](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020 zullen alle oproepen van mbox.js mislukken en gevolgen hebben voor uw pagina&#39;s waarop Target-activiteiten worden uitgevoerd. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.
   >
   >
* **Aankondigingen** van Target: Zie de Target-aankondigingspagina voor informatie over aanstaande gebeurtenissen, zoals Target Skill Builder-sessies, ontwikkelaarstekkers, webinars en Target Coffee Break-sessies. Zie [Target-aankondigingen](/help/r-release-notes/target-announcements.md)voor meer informatie.


## Target Standard/Premium 20.5.1 (17 juni 2020)

| Functie/verbetering | Beschrijving |
| --- | --- |
| Analytics for Target (A4T)-ondersteuning voor [!UICONTROL Auto-Allocate] activiteiten | [!UICONTROL Auto-Allocate] activiteiten ondersteunen nu [Analytics voor Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Deze integratie staat u toe om het [!UICONTROL Auto-Allocate] multi-gewapende bandit vermogen te gebruiken om verkeer aan het winnen van ervaringen te drijven, terwijl het gebruiken van een [!UICONTROL Adobe Analytics] doel metrisch en/of [!UICONTROL Adobe Analytics] rapporteringsen analysemogelijkheden.<br>Als u A4T [al hebt](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) geïmplementeerd voor gebruik met A/B Test and Experience Targeting-activiteiten, bent u klaar!<br>Zie [Analytics for Target (A4T)-ondersteuning voor Auto-Allocate-activiteiten](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) in *Activity creation* voor meer informatie. |
| [!UICONTROL Publisher] rol | Deze nieuwe rol is vergelijkbaar met de huidige [!UICONTROL Observer] rol (kan activiteiten weergeven, maar kan deze niet maken of bewerken). De [!UICONTROL Publisher] rol heeft echter de extra toestemming om activiteiten te activeren.<br>Zie voor meer informatie: <ul><li>**Target Standard-gebruikers**: [Geef rollen en machtigingen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) op in *Gebruikers*.</li><li>**Target Premium-gebruikers**: [Stap 6: Specificeer rollen en toestemmingen](/help/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configure ondernemingstoestemmingen*.</li></ul> |
| A4T-ondersteuning op 25 [!DNL Analysis Workspace]<br>juni 2020 | [!UICONTROL Anaytics for Target] (A4T) wordt nu ondersteund in [!DNL Analysis Workspace]. Met [!UICONTROL Analytics for Target (A4T) panel] deze functie kunt u uw [!DNL Adobe Target] activiteiten en ervaringen analyseren in [!DNL Analysis Workspace].<br>Zie [Rapporten in Analytics](/help/c-integrating-target-with-mac/a4t/reporting.md) in *A4T-rapportage* en het deelvenster [Target (A4T) in de](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics Tools Guide ** voor meer informatie. |

### Verbeteringen, correcties en wijzigingen

* Probleem verholpen waarbij de metrische waarde &quot;bezoekers&quot; werd opgeslagen in de definitie van de activiteit in plaats van &quot;UniqueVisitors&quot;. (TGT-37098)
* Probleem verholpen in de [!DNL Target] gebruikersinterface die ervoor zorgde dat de verticale schuifbalk niet correct op de [!UICONTROL Audiences] pagina werkte. (TGT-36968)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Meld u aan voor de Adobe Priority Product Update als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
