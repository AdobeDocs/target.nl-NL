---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Deze releaseopmerkingen bevatten informatie over functies, verbeteringen, oplossingen en bekende problemen voor elke release van Adobe Target Standard en Target Premium.
title: 'Opmerkingen bij de release van Adobe Target (huidige) '
feature: Release Notes
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---


# Opmerkingen bij de doelversie (huidig)

Deze releaseopmerkingen bevatten informatie over functies, verbeteringen en oplossingen voor elke doelstandaard- en doelpremiumversie. Daarnaast worden releaseopmerkingen voor doel-API&#39;s, SDK&#39;s, de JavaScript-bibliotheek (at.js) en andere platformwijzigingen, indien van toepassing, ook opgenomen.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd. We raden alle klanten aan vóór deze datum naar de meest recente versie van de bibliotheek at.js of de nieuwe [!DNL Adobe Experience Platform Web SDK] te migreren om mogelijke problemen met uw sites te voorkomen.
>
>* **at.js**: Als u verkiest om aan at.js te migreren, zie  [hoe de ](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) Werknemers van At.js en de Bouwer van de Vaardigheid van  [Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >
* **Adobe Experience Platform Web SDK**: Als u verkiest om aan te migreren  [!DNL Adobe Experience Platform Web SDK], zie  [wat Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) is, in de Gids *van* Web SDK. Zie [Overzicht van doel](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/adobe-target/target-overview.html) voor [!DNL Target]-specifieke informatie.
>
>
Hoewel mbox.js momenteel wordt ondersteund (tot 31 maart 2021), hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. De nieuwere bibliotheek at.js biedt veel voordelen ten opzichte van mbox.js. Het bestand at.js verbetert onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert de beveiliging en biedt betere implementatieopties voor toepassingen op één pagina. Met [!UICONTROL Adobe Experience Platform Web SDK] kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in [!DNL Experience Cloud] (inclusief [!DNL Target]).
>
>Door alle klanten naar at.js of [!UICONTROL Adobe Experience Platform Web SDK] te verplaatsen, zullen onze technici en ondersteunend personeel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.

De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

## om 2.3.3.2013 (13 november 2020)

Deze release van at.js is een onderhoudsrelease en bevat de volgende oplossing:

* Correctie van een probleem met betrekking tot het bijhouden van een postvak en A4T.

## Target Standard/Premium 20.10.1 (27 oktober 2020)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| [Apparaatbeslissingen](https://adobetarget-sdks.gitbook.io/docs/on-device-decisioning/introduction-to-on-device-decisioning) | Bij beslissingen op het apparaat kunnen zowel marketers als productontwikkelaars experimenteren en op machinaal leren gebaseerde personalisatie vanuit het apparaat van de gebruiker, via kanalen, met een bijna-nullatentie.<br>De snelheid en de prestaties zaken-in klanteninzichten en gebruikerstevredenheid.<br>Door op het apparaat te beslissen kunt u belangrijke personalisatie- en experimenteringsinstructies in A/B Test and Experience Targeting (XT) activiteitstypen compileren in &quot;optimalisatieartefacten:&quot;JSON voorwerpen die op klantenapparaten via CDN worden geladen. En omdat gebruikers van [!DNL Target] op-device beslissingen native verbinden met producten van [!DNL Adobe Experience Cloud], krijgen ze een snelle analyse en snellere ervaringherhalingen.<br>Voor meer informatie, zie *[Op-apparatenbesluit](/help/c-implementing-target/c-api-and-sdk-overview/on-device-decisioning.md). |

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waardoor [!UICONTROL Average Lift Confidence Interval] en [!UICONTROL Confidence] niet konden worden weergegeven in [!DNL Auto-Target]-rapportage voor de [!UICONTROL Total]-rij. De metingen worden correct weergegeven voor alle afzonderlijke ervaringen. (TGT-37301)
* [!DNL Adobe Target Premium] gebruikers&quot; [!UICONTROL Auto-Target] rapporteren vanaf 15 september om 14.30 uur. Dit probleem is nu opgelost. (PDT) tot 6 oktober, 9:25 (PDT). Wanneer het bekijken van rapporten voor de beïnvloede omzettingsmetriek (die of wordt gevormd gebruikend &quot;[!UICONTROL Viewed a page]&quot;of &quot;[!UICONTROL Clicked on mbox]&quot;optie) wordt gevormd, worden de omzettingspercentages verkeerd gerapporteerd. Er is momenteel geen bekend leveringsprobleem. Zie [Automatische rapportage](/help/r-release-notes/known-issues-resolved-issues.md#at-metrics) onder *Opgeloste problemen* in *Bekende problemen en opgeloste problemen* voor informatie over het opnieuw synchroniseren en corrigeren van uw rapportage.
* Er is een selecteerbare [!UICONTROL Last Updated At]-kolom toegevoegd in de tabel [!UICONTROL Catalog Search] en een [!UICONTROL Last Updated At]-filter. Deze verbetering bespaart tijd en inspanning omdat u niet elk individueel punt moet openen om te zien wanneer het laatst werd bijgewerkt en u kunt filtreren door datum de punten werden laatst bijgewerkt.

   ![Laatst bijgewerkt bij kolom- en filterillustratie](/help/r-release-notes/assets/column-and-filter.png)

* Er zijn updates uitgevoerd om de doelgebruikersinterface compatibel te maken met [Web Content Accessibility Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/) 2.0 Level A en AA Success Criteria (WCAG 2.0 AA). (TGT-34384 &amp; TGT-24679)
* Verbeterde CSP-functies (Content Security Policy). (TGT-37035)
* Introduceerde een manier om de cliëntcode als parameter voor klanten te specificeren die CNAME gebruiken. (TNT-38571)
* [!DNL Adobe Experience Cloud] de documentatie gaat verder naar  [!DNL Experience League]. In oktober worden alle opmerkingen bij de release, artikelen, video&#39;s en zelfstudies verplaatst van hun huidige locatie op `docs.adobe.com` naar [!DNL Experience League]. Deze beweging zorgt ervoor dat al het leren, zelfhulp, enablement, en communautaire inhoud van één enkele plaats wordt gediend. Wanneer deze wijziging optreedt, hoeft u niets te doen, aangezien alle koppelingen naar [!DNL Experience League] worden omgeleid. De opmerkingen bij de release worden bijgewerkt wanneer de cutover begint.

## Aanvullende opmerkingen bij de release en versiedetails

| Resource | Details |
|--- |--- |
| [details van de at.js-versie](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informatie over wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Documentatiewijzigingen, Opmerkingen bij de vorige release en Opmerkingen bij de release Experience Cloud

Naast de notities voor elke release bevatten de volgende bronnen aanvullende informatie:

| Resource | Details |
|--- |--- |
| Documentatiewijzigingen | Gedetailleerde informatie weergeven over updates van deze handleiding die mogelijk niet zijn opgenomen in deze releaseopmerkingen.<br>Zie  [Documentatiewijzigingen](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C) voor meer informatie. |
| Opmerkingen bij de release van vorige releases | Informatie weergeven over nieuwe functies en verbeteringen in eerdere versies van Target Standard en Target Premium.<br>Voor meer informatie, zie de nota&#39;s van de  [Versie voor vorige versies](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Opmerkingen bij de release van Adobe Experience Cloud | Bekijk de nieuwste releaseopmerkingen voor de Adobe Experience Cloud-oplossingen.<br>Zie Opmerkingen bij de release  [Experience Cloud voor meer informatie](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html). |

## Voorlopige-releasegegevens {#section_5D588F0415A2435B851A4D0113ACA3A0}

De volgende middelen laten u zien wat in de volgende versie van het Doel komt.

| Resource | Details |
|--- |--- |
| Adobe Priority-productupdatelijst | Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Opmerkingen bij de volgende release | Voor informatie over de versies van het Doel van de huidige maand, met inbegrip van prereleaseinformatie, zie [de Nota&#39;s van de Versie van het Doel - Prerelease](/help/r-release-notes/target-release-notes.md) pagina. |
