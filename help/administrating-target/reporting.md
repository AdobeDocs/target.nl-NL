---
keywords: report;reports;reporting;experience cloud solution;timezone;time zone;currency;exclude IPs;estimated lift in revenue;revenue;lift in revenue;fine-grained priorities;fine-grained
description: Configureer de Adobe Target Visual Experience Composer (VEC) door de algemene instellingen, de configuratie van de mobiele viewport en de CSS-kiezers op te geven.
title: Rapporten configureren in Adobe Target
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 9b57d5554884b06d278c3baef3b2c1d5f37bdeb5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---


# Rapportage in doel configureren

Configureer algemene instellingen die moeten worden gebruikt in [!DNL Adobe Target]-rapportage die van toepassing zijn op uw gehele [!DNL Target]-account.

Als u de configuratiepagina [!UICONTROL Reporting] wilt openen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

U kunt de volgende instellingen opgeven op deze pagina:

* De Adobe Experience Cloud-oplossing voor rapportage
* De tijdzone die moet worden gebruikt voor rapportage
* De valuta die moet worden gebruikt voor rapportage
* IP adressen om van rapportering uit te sluiten
* Of een geraamde toename van de inkomsten in de rapportage moet worden weergegeven
* Of fijnkorrelige prioriteiten mogelijk moeten worden gemaakt

>[!NOTE]
>
>Houd er rekening mee dat de tijdzone-, valuta- en IP-adressen voor het uitsluiten van instellingen van toepassing zijn op activiteiten die [!DNL Target]-rapportage gebruiken. Deze instellingen zijn niet van toepassing op activiteiten die [Analytics for Target (A4T)] als rapportagebron gebruiken (/help/c-integrating-target-with-mac/a4t/a4t.md).

![Pagina rapporteren](/help/administrating-target/assets/reporting.png)

## Cloudoplossing rapporteren

Stel opties in die bepalen welke gegevens worden gebruikt voor de resultaten en rapporten.

Selecteer de rapportbron voor uw activiteiten, of [!DNL Target] of [!DNL Adobe Analytics]. U kunt ook de rapportbron per activiteit selecteren.

Houd rekening met de volgende informatie wanneer u uw rapportbron kiest:

* Als de rapportbron hier op **[!DNL Target]** wordt geplaatst, wordt u niet toegestaan om een activiteit te activeren die [!DNL Analytics] als rapporteringsbron gebruikt. U moet de rapportbron in [!DNL Target] in uw activiteit veranderen of de rapportbron in **[!UICONTROL Select per activity]** in **[!UICONTROL Administration]>[!UICONTROL Reporting]** veranderen.
* Als de rapportbron hier op **[!DNL Analytics]** wordt geplaatst, wordt u niet toegestaan om een activiteit te activeren die [!DNL Target] als rapporteringsbron gebruikt (de rapporteringsbron wordt gespecificeerd als **[!UICONTROL Target per activity])**. U moet de rapportbron in [!DNL Analytics] in uw activiteit veranderen of de rapportmotor in **[!UICONTROL Select per activity]** in **[!UICONTROL Administration]>[!UICONTROL Reporting]** veranderen.
* Als de rapportbron hier op **[!UICONTROL Select per activity]** wordt geplaatst, kunt u tot stand brengen, activeren en activiteiten deactiveren die door de geselecteerde rapporteringsbron worden gesteund. Zie [Ondersteunde activiteitstypen](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als rapportagebron voor Adobe Target (A4t)* voor een matrix met ondersteunde activiteiten.
* [!UICONTROL Automated Personalization] (AP) het creëren van activiteit, activering, en deactivering worden toegestaan ongeacht de geselecteerde rapporteringsbron. Automated Personalization-activiteiten worden niet ondersteund wanneer u [Adobe Analytics als rapportagebron voor Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md) kiest. Zelfs als u [!DNL Analytics] als uw rapporteringsbron specificeert, [!DNL Target] wordt gebruikt als rapporteringsbron voor de activiteiten van Automated Personalization. Zie [Ondersteunde activiteitstypen](/help/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als rapportagebron voor Adobe Target (A4t)* voor meer informatie.

## Tijdzone voor rapportage

Geef de tijdzone op die moet worden gebruikt voor rapportage.

## Valuta voor rapportage

Geef de valuta op die moet worden gebruikt voor rapportage.

## IPs om van het Doel uit te sluiten rapporteringsgegevens

Specificeer om het even welke IP adressen die u van het melden van gegevens wilt uitsluiten. Het uitsluiten van interne bedrijfsadressen is bijvoorbeeld een goede manier om ervoor te zorgen dat uw rapportgegevens de interactie van klanten op uw website weerspiegelen.

Ga elk IP adres op een nieuwe lijn in.

## Geraamde verhoging van de ontvangsten tonen

U kunt kiezen om de geschatte verhoging van opbrengst te tonen als u een monetaire waarde voor uw doel ingaat. [!DNL Target] U kunt een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. De functie voor het schatten van de lift is standaard uitgeschakeld.

Alleen [!DNL Experience Cloud] Admin-gebruikers kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.

Zie [Lift in Revenue schatten](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) voor gedetailleerde informatie.

## Geavanceerde prioriteiten inschakelen

Numerieke items toestaan voor een prioriteit tussen 0 en 999.

Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.
