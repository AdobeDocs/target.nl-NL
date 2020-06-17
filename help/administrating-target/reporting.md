---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configureer de Adobe Target Visual Experience Composer (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.
title: Rapporten configureren in Adobe Target
topic: Standard
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---


# Rapporten configureren in Target

Configureer algemene instellingen die u wilt gebruiken in Target-rapportage die van toepassing zijn op uw gehele [!DNL Target] account.

>[!NOTE]
>
>De informatie in dit onderwerp is bijgewerkt om u een sluimerpiek bij de veranderingen te geven UI die in Target Standard/Premium 20.6.1 versie (Juli 2020) komen. De meeste informatie die in dit onderwerp wordt voorgesteld is op huidige UI van toepassing; de opties kunnen zich echter op iets andere locaties bevinden .

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

Selecteer de rapportbron voor uw activiteiten, of [!DNL Target] of Adobe Analytics. U kunt ook de rapportbron per activiteit selecteren.

Houd rekening met de volgende informatie wanneer u uw rapportbron kiest:

* [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Automated Personalization] (AP) het creëren van activiteit, activering, en deactivering worden toegestaan ongeacht de geselecteerde rapporteringsbron. Deze activiteitstypen worden niet ondersteund wanneer u [Adobe Analytics kiest als rapportagebron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md). Zelfs als u Analytics opgeeft als rapportagebron, [!DNL Target] wordt dit gebruikt als rapportagebron voor deze typen activiteiten.
* Als de rapportbron hier op Analytics is ingesteld, kunt u geen activiteit activeren die als rapporteringsbron gebruikt (de rapporteringsbron wordt gespecificeerd als Target per activiteit). [!DNL Target] U moet de rapporteringsbron in Analytics in uw activiteit veranderen of de rapporteringsmotor in Uitgezochte per Activiteit in Opstelling > Voorkeur veranderen.
* Als de rapportbron [!DNL Target] hier is ingesteld, kunt u geen activiteit activeren die Analytics als rapportagebron gebruikt. U moet de rapporteringsbron veranderen in [!DNL Target] in uw activiteit of de rapporteringsbron veranderen om te selecteren per Activiteit in Opstelling > Voorkeur.
* Als de rapportbron hier is ingesteld op Selecteren per activiteit, kunt u activiteiten maken, activeren en deactiveren die door de geselecteerde rapportbron worden ondersteund. Voor een matrix met ondersteunde activiteiten raadpleegt u [Adobe Analytics als de rapportbron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Wanneer u van Handleiding A/B aan [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target]schakelt, worden alle metriek en rapporteringspubliek verloren als de rapporteringsbron van de Handmatige activiteit A/B niet in [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteiten wordt gesteund.

## Tijdzone voor rapportage

Geef de tijdzone op die moet worden gebruikt voor rapportage.

## Valuta voor rapportage

Geef de valuta op die moet worden gebruikt voor rapportage.

## IP&#39;s die moeten worden uitgesloten van Target-rapportagegegevens

Specificeer om het even welke IP adressen die u van het melden van gegevens wilt uitsluiten. Het uitsluiten van interne bedrijfsadressen is bijvoorbeeld een goede manier om ervoor te zorgen dat uw rapportgegevens de interactie van klanten op uw website weerspiegelen.

Ga elk IP adres op een nieuwe lijn in.

## Geraamde verhoging van de ontvangsten tonen

U kunt kiezen om de geschatte verhoging van opbrengst te tonen als u een monetaire waarde voor uw doel ingaat. [!DNL Target] U kunt een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. De functie voor het schatten van de lift is standaard uitgeschakeld.

Alleen gebruikers van Experience Cloud Admin kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.

Voor nadere informatie, zie [Schatting Lift in Revenue](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Geavanceerde prioriteiten inschakelen

Numerieke items toestaan voor een prioriteit tussen 0 en 999.

Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.
