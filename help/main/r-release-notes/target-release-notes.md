---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8f7cdf94438763679273b3631e45b1b41899cda5
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**laatst bijgewerkt: 18 augustus, 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd. De informatie in dit artikel wordt regelmatig bijgewerkt, vooral vóór versies.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.8.3 (21 augustus 2025)

Deze release bevat de volgende updates en oplossingen:

**Aanbevelingen**

+++Zie details
* **Vaste kwestie in Recs UI waar de download van douanecriteria CSV 404 fout** terugkeerde: Vaste een kwestie waar de klanten de douanecriteria CSV in activiteit-creeer proces niet konden downloaden. (TGT-51966)
* **Vaste inconsistente beeld die in[!UICONTROL Catalog Search]** laadt: Vaste een kwestie waar de duimnagels en de beelden in [!UICONTROL  Catalog Search] niet constant in activiteit-creeer proces laadden. Afbeeldingen kunnen alleen worden weergegeven als de kolom &quot;URL miniatuur&quot; zichtbaar is en sommige productafbeeldingen geheel of gedeeltelijk zijn geladen na navigatie- of zoekacties. (TGT-52778)
* **Vaste een kwestie waar het uitgeven van een aanbeveling in een gedupliceerde ervaring beïnvloedde de originele ervaring**: De klanten rapporteerden dat het wijzigen van een aanbeveling in een gedupliceerde ervaring onbedoeld de originele ervaring veranderde. Na het dupliceren van Experience B in het activity-create proces en het bewerken van het ontwerp of de criteria, werden dezelfde wijzigingen weerspiegeld in de oorspronkelijke Experience B, hoewel ze afzonderlijke entiteiten waren. (TGT-53369)
* **Vaste een kwestie waar de veranderingen in een gedupliceerde ervaring onbedoeld de originele ervaring in een activiteit beïnvloedden:** de Klanten rapporteerden dat wanneer het dupliceren van een ervaring binnen een activiteit en het toewijzen van een nieuw publiek, om het even welke veranderingen die in het gedupliceerde ontwerp of de criteria van de ervaring werden aangebracht ook in de originele ervaring werden weerspiegeld. Dit gebeurde ook al werden er geen bewerkingen rechtstreeks in de oorspronkelijke versie aangebracht, wat invloed had op de mogelijkheid om onafhankelijke variaties binnen dezelfde activiteit te maken. (TGT-53361)
* **Vaste een kwestie waar [!UICONTROL Recommendation Catalog] periodiek om volledige gegevens van productattributen** te tonen er niet in slaagde: In bijgewerkte [!DNL Recommendations] UI, ervaren de klanten een kwestie waar bepaalde productattributen, zoals bericht, niet constant in de resultaten van het catalogusonderzoek werden getoond, alhoewel de gegevens in het voer bestonden. In dit geval moesten klanten de zichtbaarheid van de kolommen handmatig opnieuw configureren om de ontbrekende waarden op te halen. (TGT-52769)
+++

**[!UICONTROL Visual Experience Composer](VEC)**

+++Zie details
* **Vaste kwestie in activiteit-creeer proces dat vooruitgang aan [!UICONTROL Targeting] stap in AP activiteiten** blokkeerde: Vaste een kwestie in activiteit-creeert proces waar de klanten niet aan de [!UICONTROL Targeting] stap in [!UICONTROL Automated Personalization] (AP) activiteiten konden te werk gaan tenzij twee plaatsen werden toegevoegd. Dit gedrag verschilde van de vorige ervaring, waar één enkele plaats met veelvoudige aanbiedingen voldoende was. Deze vereiste is gecorrigeerd, zodat klanten de Single-location-instellingen kunnen blijven gebruiken in hun AP-workflows. (TGT-53426)

+++

**[!UICONTROL Workspaces]**

+++Zie details
* **Vaste een kwestie waar een klant tot één enkele werkruimte beperkt activiteiten van andere werkruimten** kon bekijken: De klanten met toegang die tot één werkruimte wordt beperkt waren onverwacht in staat om activiteiten over alle werkruimten te bekijken wanneer het selecteren [!UICONTROL All Workspaces] in activiteit-creeer proces. Deze zichtbaarheid vormde een risico op onbedoelde wijzigingen in de live activiteiten in andere werkruimten, hetgeen mogelijk van invloed was op de prestaties van de website. (TGT-53101)
* **Vaste een kwestie waar een klant activiteiten van [!UICONTROL Default Workspace] kon bekijken zonder toegang te hebben:** een klant met toegang die tot de het opvoeren werkruimte wordt beperkt kon activiteiten van [!UICONTROL Default Workspace] bekijken via het activiteit-creeer proces. Dit kwam ondanks correcte achtergrondconfiguratie en toegangsrechten voor. (TGT-53297)

+++

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
