---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8f5e2c5025dc4b9caf31f51c03fb073ddd9ba756
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 6 oktober 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen.
>
>Migreer naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.10.1 (6 oktober 2021)

Deze release bevat de volgende nieuwe functies:

| Functie | Details |
| --- | --- |
| [!UICONTROL Audiences] UI vernieuwen | Als onderdeel van de voortdurende inspanningen van het [!DNL Adobe Target]-team om de gebruikerservaring voor [!DNL Target]-gebruikers te verbeteren, vernieuwt deze release de [!UICONTROL Audiences]- en [!UICONTROL Profile Scripts]-pagina&#39;s in de [!DNL Target]-interface. Deze update verenigt en normaliseert ontwerppatronen die eerder inconsistent waren, terwijl het toevoegen van nieuwe verhogingen, zoals:<ul><li>De mogelijkheid om meerdere soorten publiek tegelijk te selecteren en te verwijderen</li><li>Een vernieuwd [ontwerp voor publieksbuilder](/help/c-target/c-audiences/create-audience.md)</li><li>De regelsteun van de uitsluiting in [!UICONTROL Audience] de bouwer van de bibliotheekregel</li><li>Een nieuw filter &quot;Bron publiek&quot;, waarmee u sneller uw doelgroep kunt detecteren</li><li>Opties voor permanent zoeken en filteren tijdens sessies</li></ul>Zie [Soorten publiek](/help/c-target/target.md) voor meer informatie.<br>**Opmerking**: Deze interface wordt alleen aangepast aan klanten in de EMEA-regio. De klanten in andere delen van de wereld, met inbegrip van Noord-Amerika, zullen volgende week de vernieuwde UI zien. |
| [!UICONTROL Profile Scripts] UI vernieuwen | De bibliotheek [!UICONTROL Profile Scripts] is ook bijgewerkt en bevat een vernieuwde interface en diverse productiviteitsupdates:<ul><li>De mogelijkheid om meerdere profielscripts tegelijk te selecteren en te verwijderen</li><li>Een nieuwe code-editor voor profielscripts</li><li>Syntaxis markeren en fout controleren in de code-editor</li><li>Automatisch aanvullen van tokens (mbox of profiel) via sneltoetsen</li></ul>Zie [Bezoekersprofielen](/help/c-target/c-visitor-profile/visitor-profile.md) voor meer informatie.<br>**Opmerking**: Deze interface wordt alleen aangepast aan klanten in de EMEA-regio. De klanten in andere delen van de wereld, met inbegrip van Noord-Amerika, zullen volgende week de vernieuwde UI zien. |
| ![Criteria voor ](/help/assets/premium.png) het maken en bewerken van premiumbadgeRecommendations | De workflow voor het maken en bewerken van [!UICONTROL Recommendations Criteria] is gestroomlijnd en eenvoudiger om het juiste algoritme en de juiste instellingen voor aanbevelingen te kiezen om uw doelen te bereiken.<br>Zie  [Criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md) maken voor meer informatie. |
| ![Premium ](/help/assets/premium.png) badgeRecommendations lookback window en algoritme verfrissen tariefverbeteringen | U kunt de algoritmen &quot;Meest bekeken&quot; en &quot;Hoogste verkopers&quot; nu uitvoeren met een terugkijkvenster van zes uur om de inhoud vast te leggen die het laatst wordt doorzocht. Wanneer het terugkijkvenster van zes uur wordt geselecteerd, worden uw aanbevelingen resultaten bijgewerkt om de 3-6 uur door de dag.<br>Zie  [Gegevensbron in criteria](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source)   ** maken voor meer informatie. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
