---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;pre-release
description: Leer meer over de nieuwe functies, verbeteringen en oplossingen in de komende release van Adobe Target, waaronder SDK's, API's en JavaScript-bibliotheken.
title: Welke nieuwe eigenschappen worden inbegrepen in de aanstaande Versie?
feature: Opmerkingen bij de release
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
translation-type: tm+mt
source-git-commit: 60c3dfe28f3618113d4d03da538e4d0e4ac2feb8
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Opmerkingen bij de release Doel (preRelease)

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 1 maart 2021**

Zie [Opmerkingen bij de doelversie](release-notes.md) voor informatie over de huidige versie. De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>Migreer vóór deze datum naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## Target Standard/Premium 21.2.1 (9 maart 2021)

Deze onderhoudsversie bevat de volgende verbeteringen, correcties en wijzigingen.

De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik [!DNL Adobe].

* De toegestane aanbiedingsgrootte is vergroot (TGT-38304):

   | Type | Vorige limiet | Nieuwe limiet |
   | --- | --- | --- |
   | HTML | 256 kB | 1024 kB |
   | Visuele aanbiedingen van het Doel UI | 64 kB | 1024 kB voor elke ervaring |
   | Via API | 512 kB | 1024 kB |

* [!UICONTROL Personalization Insights] Er worden nu dagelijks rapporten over  [!UICONTROL Auto-Target] (AT)- en  [!UICONTROL Automated Personalization] (AP)-activiteiten opgesteld. U kunt een rapport kiezen dat [!UICONTROL Automated Segments] of [!UICONTROL Important Attributes] voor de laatste 15, 30, en 60 dagen verstrekt. De opties voor 45 en 90 dagen zijn verwijderd om de andere instellingen voor terugzoekvensters dagelijks uit te voeren. (TGT-39472)
* Probleem verholpen waarbij de huidige afhankelijkheid niet werd weergegeven wanneer klanten [!UICONTROL Edit Dependency] op de pagina [!UICONTROL Goals & Settings] van een activiteit klikken. (TGT-39340)
* Probleem verholpen bij het vernieuwen van de [!UICONTROL Audience Library] van een werkruimte. Vóór verfrist zich, toont het publiek voor de momenteel geselecteerde werkruimte. Na verfrissen, [!UICONTROL Default Workspace] en zijn publiek getoond. De huidige werkruimte en het publiek blijven nu behouden na het vernieuwen. (TGT-38871)
* Probleem verholpen bij het kopiëren van een [!UICONTROL Recommendations]-activiteit en later het bewerken van de oorspronkelijke activiteit door de volgorde van criteria te wijzigen. De wijziging in de volgorde van criteria in de oorspronkelijke activiteit werd ook onjuist toegepast op de gekopieerde activiteit. (TGT-39155)
* Probleem verholpen waarbij het onjuiste aantal producten voor uitsluitingen [!UICONTROL Recommendations] werd weergegeven. (TGT-39599)

## Voorlopige-releasegegevens {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen, meldt u zich aan voor de Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
