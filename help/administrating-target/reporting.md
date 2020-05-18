---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configureer de Adobe Target Visual Experience Composer (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.
title: Rapportage configureren in Adobe Target
topic: Standard
translation-type: tm+mt
source-git-commit: 34c4c48602df8550287e86c535ebc350fe2185f7
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---


# Rapportage in doel configureren

Configureer algemene instellingen die u wilt gebruiken in de rapportage van Target die van toepassing zijn op uw gehele [!DNL Target] account.

Klik op [!UICONTROL Reporting] > **[!UICONTROL Administration]** **[!UICONTROL Reporting].**

U kunt de volgende instellingen opgeven op deze pagina:

* De Adobe Experience Cloud-oplossing voor rapportage
* De tijdzone die moet worden gebruikt voor rapportage
* De valuta die moet worden gebruikt voor rapportage
* IP adressen om van rapportering uit te sluiten
* Of een geraamde toename van de inkomsten in de rapportage moet worden weergegeven
* Of fijnkorrelige prioriteiten mogelijk moeten worden gemaakt

![Pagina rapporteren](/help/administrating-target/assets/reporting.png)

## Cloudoplossing rapporteren

Stel opties in die bepalen welke gegevens worden gebruikt voor de resultaten en rapporten.

Selecteer de rapportbron voor uw activiteiten, of [!DNL Target] of Analytics van Adobe. U kunt ook de rapportbron per activiteit selecteren.

Houd rekening met de volgende informatie wanneer u uw rapportbron kiest:

* [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] (AP) het creëren van activiteit, activering, en deactivering worden toegestaan ongeacht de geselecteerde rapporteringsbron. Deze activiteitstypen worden niet ondersteund wanneer u [Adobe Analytics als rapportagebron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md)kiest. Zelfs als u Analytics als uw rapporteringsbron specificeert, [!DNL Target] wordt gebruikt als rapporteringsbron voor deze activiteitentypes.
* Als de rapporteringsbron hier aan Analytics wordt geplaatst, bent u niet toegestaan om een activiteit te activeren die als rapporteringsbron gebruikt (de rapporteringsbron wordt gespecificeerd als Doel per activiteit). [!DNL Target] U moet de rapportbron in Analytics in uw activiteit veranderen of de rapporteringsmotor veranderen om te selecteren per Activiteit in Opstelling > Voorkeur.
* Als de rapporteringsbron aan [!DNL Target] hier wordt geplaatst, wordt u niet toegestaan om een activiteit te activeren die Analytics als rapporteringsbron gebruikt. U moet de rapporteringsbron veranderen in [!DNL Target] in uw activiteit of de rapporteringsbron veranderen om te selecteren per Activiteit in Opstelling > Voorkeur.
* Als de rapportbron hier is ingesteld op Selecteren per activiteit, kunt u activiteiten maken, activeren en deactiveren die door de geselecteerde rapportbron worden ondersteund. Zie [Adobe Analytics als rapportbron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) voor een matrix met ondersteunde activiteiten.
* Wanneer u van Handleiding A/B aan [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target]schakelt, worden alle metriek en rapporteringspubliek verloren als de rapporteringsbron van de Handmatige activiteit A/B niet in [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteiten wordt gesteund.

## Tijdzone voor rapportage

Geef de tijdzone op die moet worden gebruikt voor rapportage.

## Valuta voor rapportage

Geef de valuta op die moet worden gebruikt voor rapportage.

## IPs om van het Doel uit te sluiten rapporteringsgegevens

Specificeer om het even welke IP adressen die u van het melden van gegevens wilt uitsluiten. Het uitsluiten van interne bedrijfsadressen is bijvoorbeeld een goede manier om ervoor te zorgen dat uw rapportgegevens de interactie van klanten op uw website weerspiegelen.

Ga elk IP adres op een nieuwe lijn in.

## Geraamde verhoging van de ontvangsten tonen

U kunt kiezen om de geschatte verhoging van opbrengst te tonen als u een monetaire waarde voor uw doel ingaat. [!DNL Target] U kunt een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. De functie voor het schatten van de lift is standaard uitgeschakeld.

Alleen Experience Cloud Admin-gebruikers kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.

Voor nadere informatie, zie [Schatting Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Geavanceerde prioriteiten inschakelen

Numerieke items toestaan voor een prioriteit tussen 0 en 999.

Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.
