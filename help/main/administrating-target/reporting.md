---
keywords: rapport;rapporten;rapportering;ervaring wolkenoplossing;tijdzone;tijdzone;valuta;uitsluiten IPs;geschatte opheffing van inkomsten;opbrengst;opheffing van inkomsten;fijnkorrelige prioriteiten;fijnkorrelige prioriteiten
description: Het gebruik  [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics]  als rapporterende bron, specificeert de standaardtijdzone en het muntformaat, voegt IP adressen toe om van rapportering uit te sluiten, en meer.
title: Hoe vorm ik Rapportering in  [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: 3e2682acdf8c7be86285c901ddcdae0f43b647f2
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# Rapportage configureren in [!DNL Target]

Configureer algemene instellingen die moeten worden gebruikt in [!DNL Adobe Target] -rapporten die van toepassing zijn op uw gehele [!DNL Target] -account.

{{permissions-update}}

Als u de configuratiepagina van [!UICONTROL Reporting] wilt openen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

U kunt de volgende instellingen opgeven op deze pagina:

* De Adobe Experience Cloud-oplossing voor rapportage
* De tijdzone die moet worden gebruikt voor rapportage
* De valuta die moet worden gebruikt voor rapportage
* IP adressen om van rapportering uit te sluiten
* Of een geraamde toename van de inkomsten in de rapportage moet worden weergegeven
* Of fijnkorrelige prioriteiten mogelijk moeten worden gemaakt

>[!NOTE]
>
>Houd er rekening mee dat de tijdzone-, valuta- en IP-adressen voor het uitsluiten van instellingen van toepassing zijn op activiteiten die [!DNL Target] -rapportage gebruiken. Deze montages zijn niet op activiteiten van toepassing die [&#x200B; Analytics voor Doel (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) of [!DNL Customer Journey Analytics] als rapporteringsbron gebruiken.

![&#x200B; Meldend pagina &#x200B;](/help/main/administrating-target/assets/reporting.png)

## Cloudoplossing rapporteren {#solution}

Stel opties in om te bepalen welke gegevens worden gebruikt voor de resultaten en rapporten.

Selecteer de rapportbron voor uw activiteiten, [!DNL Target], [!DNL Adobe Analytics] of [!DNL Adobe Customer Journey Analytics] . U kunt ook de rapportbron per activiteit selecteren als onderdeel van een driedelige geleide workflow terwijl u de activiteit maakt.

Houd rekening met de volgende informatie wanneer u uw rapportbron kiest:

* **[!DNL Adobe Target]**: Als de rapportbron op **[!DNL Target]** hier is ingesteld, kunt u geen activiteit maken of activeren die [!DNL Analytics] of [!DNL Customer Journey Analytics] als rapportbron gebruikt. U moet de rapportbron wijzigen in **[!UICONTROL Select per activity]** .
* **[!DNL Adobe Analytics]**: Als de rapportbron op **[!DNL Analytics]** hier is ingesteld, kunt u geen activiteit maken of activeren die [!DNL Target] of [!DNL Customer Journey Analytics] als rapportbron gebruikt. U moet de rapportbron wijzigen in **[!UICONTROL Select per activity]** .
* **[!DNL Adobe Customer Journey Analytics]**: Als de rapportbron op **[!DNL Customer Journey Analytics]** hier is ingesteld, kunt u geen activiteit maken of activeren die [!DNL Target] of [!DNL Analytics] als rapportbron gebruikt. U moet de rapportbron wijzigen in **[!UICONTROL Select per activity]** .
* **Uitgezocht per activiteit**: Als de rapporteringsbron aan **[!UICONTROL Select per activity]** hier wordt geplaatst, kunt u activiteiten tot stand brengen en activeren die door de geselecteerde rapporteringsbron worden gesteund.

Houd rekening met de volgende informatie wanneer u de rapportbron bepaalt:

* **[!DNL Analytics]**: Voor een matrijs van gesteunde activiteiten die [!DNL Analytics] als rapporteringsbron (A4T) gebruiken, zie [&#x200B; Gesteunde activiteitentypes &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als rapporteringsbron voor Adobe Target (A4t)*.

  [!UICONTROL Automated Personalization] (AP) het creëren en activeren van activiteit wordt toegestaan ongeacht de geselecteerde rapporteringsbron. [!UICONTROL Automated Personalization] de activiteiten worden niet gesteund wanneer u [&#x200B; Adobe Analytics als rapporteringsbron voor Adobe Target (A4T) &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md) kiest.

  Zelfs als u [!DNL Analytics] opgeeft als rapportagebron, wordt [!DNL Target] gebruikt als rapportagebron voor [!DNL Automated Personalization] -activiteiten.

* **[!DNL Customer Journey Analytics]**: Voor een matrijs van gesteunde activiteiten die [!DNL Target] gebruiken meldend in [!DNL Customer Journey Analytics], zie [&#x200B; Gesteunde activiteitentypes &#x200B;](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) in *[!DNL Target]rapporterend in[!DNL Adobe Customer Journey Analytics]*.

  [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] het creëren en activeren van activiteit zijn toegestaan, ongeacht de geselecteerde rapportbron. Deze activiteiten worden niet gesteund wanneer u [&#x200B; Adobe Customer Journey Analytics als rapporteringsbron &#x200B;](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) kiest.

  Zelfs als u [!DNL Customer Journey Analytics] opgeeft als rapportagebron, wordt [!DNL Target] gebruikt als rapportagebron voor [!DNL Automated Personalization] -activiteiten.

  Als u [!DNL Customer Journey Analytics] opgeeft als bron voor [!UICONTROL Auto-Allocate] - of [!UICONTROL Auto-Target] -activiteiten, kan [!DNL Target] of [!DNL Analytics] worden gebruikt als bron voor rapportage.

## Tijdzone voor rapportage

Geef de tijdzone op die moet worden gebruikt voor rapportage.

## Valuta voor rapportage

Geef de valuta op die moet worden gebruikt voor rapportage.

## IP&#39;s die moeten worden uitgesloten van [!DNL Target] -rapportage

Specificeer om het even welke IP adressen die u van het melden van gegevens wilt uitsluiten. Het uitsluiten van interne bedrijfsadressen is bijvoorbeeld een goede manier om ervoor te zorgen dat uw rapportgegevens de interactie van klanten op uw website weerspiegelen.

Ga elk IP adres op een nieuwe lijn in.

## Geraamde verhoging van de ontvangsten tonen

U kunt kiezen om de geschatte verhoging van opbrengst te tonen als u een monetaire waarde voor uw doel ingaat. [!DNL Target] kan een schatting maken van de inkomstenverhoging die u zou bereiken als alle gebruikers de winnende ervaring bekijken. De functie voor het schatten van de lift is standaard uitgeschakeld.

Alleen [!DNL Experience Cloud] Beheerders kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.

Voor gedetailleerde informatie, zie [&#x200B; Schatting Lift in Ontvangsten &#x200B;](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Geavanceerde prioriteiten inschakelen

Numerieke items toestaan voor een prioriteit tussen 0 en 999.

Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen van Laag, Medium of Hoog gebruiken, of u kunt fijnkorrelige prioriteiten van 0 tot 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.
