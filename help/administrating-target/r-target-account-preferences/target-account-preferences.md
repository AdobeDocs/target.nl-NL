---
keywords: account preferences;preferences;site details;custom mbox name;Experience Cloud solution used for reporting;Show estimated lift in revenue;css selectors;use element classes;Default Visual Experience Composer URL;Enable Enhanced Experience Composer;Generate Experience Snapshots;mobile viewport configuration;Industry Vertical;Filter Incompatible Criteria
description: Stel uw accountvoorkeuren in om Adobe Target Standard of Target Premium zo te configureren dat deze correct werken met uw account.
title: Voorkeuren
subtopic: Getting Started
topic: Standard
uuid: ed3904c8-533b-4b9c-a3a1-079c61b1bf2a
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Voorkeuren{#preferences}

Stel uw accountvoorkeuren in om uw account te configureren [!DNL Target Standard] of correct met uw account [!DNL Target Premium] te werken.

Als u uw accountvoorkeuren wilt instellen, klikt u op **[!UICONTROL Setup]** > **[!UICONTROL Preferences]**, configureert u de voorkeuren naar wens en klikt u op **[!UICONTROL Submit]**.

In de volgende afbeelding ziet u de beschikbare instellingen op de [!UICONTROL Account Preferences] pagina.

![Voorkeurspagina](/help/administrating-target/r-target-account-preferences/assets/target-account-preferences.png)

>[!NOTE]
>
>Sommige van deze voorkeuren zijn alleen beschikbaar als u [Target Premium](/help/c-intro/intro.md#premium)hebt.

## Site-details {#section_04A3340FC29B46978DB77058259F4EE0}

Geef op hoe uw site is geconfigureerd.

### Aangepaste globale mabox

Selecteer de optionele aangepaste naam van het selectievakje die u gebruikt om [!DNL Target] activiteiten te leveren. Dit algemene selectievakje moet leeg zijn, wat betekent dat het geen standaardinhoud heeft. Sla deze instelling pas op nadat het bijgewerkte [!DNL at.js] of [!DNL mbox.js] bestand op uw site is geïnstalleerd.

>[!CAUTION]
>
>Het verkeerd vormen van dit het plaatsen zou in een stroomonderbreking voor bestaande activiteiten kunnen resulteren.

## Resultaten en rapportage {#section_47C887AABD704A96BCD1C00BEABF4BCE}

Stel opties in die bepalen welke gegevens worden gebruikt voor de resultaten en rapporten.

| Option | Beschrijving |
|--- |--- |
| Experience Cloud-oplossing voor rapportage | Selecteer de rapportbron voor uw activiteiten, of [!DNL Target] of Analytics van Adobe. U kunt ook de rapportbron per activiteit selecteren. Houd rekening met de volgende informatie wanneer u uw rapportbron kiest:<ul><li>[!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] (AP) het creëren van activiteit, activering, en deactivering worden toegestaan ongeacht de geselecteerde rapporteringsbron. Deze activiteitstypen worden niet ondersteund wanneer u [Adobe Analytics als rapportagebron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md)kiest. Zelfs als u Analytics als uw rapporteringsbron specificeert, [!DNL Target] wordt gebruikt als rapporteringsbron voor deze activiteitentypes.</li><li>Als de rapporteringsbron hier aan Analytics wordt geplaatst, bent u niet toegestaan om een activiteit te activeren die als rapporteringsbron gebruikt (de rapporteringsbron wordt gespecificeerd als Doel per activiteit). [!DNL Target] U moet de rapportbron in Analytics in uw activiteit veranderen of de rapporteringsmotor veranderen om te selecteren per Activiteit in Opstelling > Voorkeur.</li><li>Als de rapporteringsbron aan [!DNL Target] hier wordt geplaatst, wordt u niet toegestaan om een activiteit te activeren die Analytics als rapporteringsbron gebruikt. U moet de rapporteringsbron veranderen in [!DNL Target] in uw activiteit of de rapporteringsbron veranderen om te selecteren per Activiteit in Opstelling > Voorkeur.</li><li>Als de rapportbron hier is ingesteld op Selecteren per activiteit, kunt u activiteiten maken, activeren en deactiveren die door de geselecteerde rapportbron worden ondersteund. Zie [Adobe Analytics als rapportbron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) voor een matrix met ondersteunde activiteiten.</li><li>Wanneer u van Handleiding A/B aan [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target]schakelt, worden alle metriek en rapporteringspubliek verloren als de rapporteringsbron van de Handmatige activiteit A/B niet in [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteiten wordt gesteund.</li></ul> |
| Geraamde verhoging van de ontvangsten tonen | U kunt er ook voor kiezen om de geschatte verhoging van de inkomsten te laten zien als u een geldwaarde voor uw doel invoert. [!DNL Target] U kunt een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. De functie voor het schatten van de lift is standaard uitgeschakeld.<br>Alleen Experience Cloud Admin-gebruikers kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.<br>Voor nadere informatie, zie [Schatting Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md). |
| Geavanceerde prioriteiten inschakelen | Numerieke items toestaan voor een prioriteit tussen 0 en 999.<br>Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.<br>De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen. |

## CSS-kiezers {#section_8155EDBF449E4198863235F94D1EA872}

Geef op hoe CSS-kiezers moeten worden [!DNL Target] gegenereerd.

Met deze opties krijgt u inzicht in de structuur van uw site en kunt u betere CSS-kiezers voor de levering van inhoud genereren. [!DNL Target] Standaard worden kiezers [!DNL Target] gegenereerd op basis van element-id&#39;s op de pagina. Als uw site weinig id&#39;s gebruikt of ID&#39;s op dezelfde pagina dupliceert, kunt u beter klassen gebruiken.

U kunt een van de volgende opties of beide opties kiezen:

| Option | Beschrijving |
|--- |--- |
| Element-id&#39;s gebruiken | Schakel deze optie uit als dezelfde id wordt gebruikt voor meerdere elementen of als de element-id kan veranderen bij het laden van de pagina. |
| Elementklassen gebruiken | Standaard worden [!DNL Target] alleen element-id&#39;s gebruikt. Als uw pagina echter is ontworpen om klassen te gebruiken voor het identificeren van elementen, zoals een pagina die is gemaakt met [!DNL Adobe Experience Manager], moet u ook [!UICONTROL Use element classes]selecteren.<br>**Opmerking **: Hoewel alles is gedaan om nauwkeurigheid te verzekeren, houd er rekening mee dat het gebruik van klassen tot fouten kan leiden. Als u geen van beide opties selecteert, heeft dit ook invloed op de nauwkeurigheid. De nauwkeurigheidsvolgorde is ID&#39;s > klassen > geen van beide opties. Zorg altijd dat u de pagina test om te controleren of de kiezers correct zijn.<br>U kunt deze instelling per activiteit overschrijven (klik op het[!UICONTROL Settings]tandwielpictogram en selecteer[!UICONTROL CSS Selectors]). Dit is vooral nuttig als u veelvoudige plaatsen hebt die verschillend worden gevormd.<br>**Opmerking**: Het overschrijven van de instelling per activiteit is niet beschikbaar bij [!UICONTROL Automated Personalization] en [!UICONROL Multivariate testactiviteiten] .  Zie [Elementkiezers die in de Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/vec-selectors.md) worden gebruikt voor aanvullende informatie over kiezers. |

## Visual Experience Composer {#section_CD9BDD372CF54E678F88E8BA95757A5A}

| Option | Beschrijving |
|--- |--- |
| Standaard-URL voor composer visuele ervaring | Stel de standaard-URL in die door de [!UICONTROL Visual Experience Composer]URL wordt gebruikt. Dit is de standaardpagina, zoals uw homepage, die wordt gebruikt wanneer u opstelling een ervaring voor elke nieuwe activiteit. Als u geen standaard-URL instelt, moet u voor elke activiteit een URL invoeren wanneer u deze maakt. |
| Enhanced Experience Composer inschakelen | Hiermee kunt u iFrame-sites en sites met gemengde inhoud bewerken. Sommige sites zijn mogelijk niet compatibel met de verbeterde versie. Schakel deze optie uit om terug te keren naar de originele Experience Composer. Deze keuze heeft geen invloed op de levering van activiteiten op sites.<br>Voor meer informatie, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.<br>**Opmerking **: U kunt ook de Enhanced Experience Composer inschakelen op activiteitsniveau. |
| Gemengde inhoud laden | Schakel gemengde inhoud in terwijl u een website opent met de Enhanced Experience Composer (EEC). Als u deze optie inschakelt, voorkomt u de extra overhead van het laden van statische bronnen via doelproxyservers.<br>Deze optie is bijvoorbeeld handig als in de CSP-headers (Content Security Policy) het laden van gemengde inhoud is toegestaan zonder het gebruik van proxyservers waarvoor de EEC is ingeschakeld.<br>Deze optie is ook handig als uw HTTP-website te maken heeft met een langere laadtijd in de EEG, waarbij JavaScript, afbeeldingen enzovoort langer duurt om te laden via proxy. |
| Ervaar-momentopnamen genereren | Als u ervaringsmomentopnamen inschakelt, worden miniaturen voor uw ervaringen in het activiteitenwerkstroomdiagram gegenereerd. Het uitschakelen van momentopnamen kan voor sommige gebruikers tot snellere prestaties leiden. |

## Configuratie mobiele viewport {#section_42176D062BCE4A28ADBB784CC4BEF84D}

U kunt apparaten toevoegen om te gebruiken wanneer het previewing ervaringen. Elk apparaat heeft een bijbehorend publiek.

| Option | Beschrijving |
|--- |--- |
| ![Premium-badge](/help/assets/premium.png) Nieuwe toevoegen | Klik [!UICONTROL Add New], geef een beschrijvende naam op voor de mobiele viewport, geef de breedte en hoogte op, selecteer het gewenste besturingssysteem en klik op [!UICONTROL Save].  Voor informatie over hoe te om een mobiele viewport toe te voegen, zie de [Mobiele Configuratie](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md)van de Viewport. |

## Trainingsvideo: Accountvoorkeuren (7:33) - ![overzichtspagina](/help/assets/overview.png)

Deze video bevat informatie over accountvoorkeuren.

* Beschrijf de beschikbare accountinstellingen in [!DNL Target Standard]

>[!VIDEO](https://video.tv.adobe.com/v/17379)