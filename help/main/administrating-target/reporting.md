---
keywords: rapport;rapporten;rapportering;ervaring wolkenoplossing;tijdzone;tijdzone;valuta;uitsluiten IPs;geschatte opheffing van inkomsten;opbrengst;opheffing van inkomsten;fijnkorrelige prioriteiten;fijnkorrelige prioriteiten
description: Gebruiken [!DNL Target], [!DNL Adobe Analytics], or [!DNL Adobe Customer Journey Analytics] als rapporteringsbron, specificeer de standaardtijdzone en muntformaat, voeg IP adressen toe om van rapportering uit te sluiten, en meer.
title: Hoe ik Rapportering in Vorm [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: fd83e60e-64a6-4d0e-909f-480d13bac32b
source-git-commit: ea9513c4310d13e1e7899aa7e228b4d7ecdf0748
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# Rapportage configureren in [!DNL Target]

Algemene instellingen configureren voor gebruik in [!DNL Adobe Target] rapportage die van toepassing is op uw gehele [!DNL Target] account.

Als u toegang wilt krijgen tot [!UICONTROL Reporting] configuratiepagina, klik **[!UICONTROL Administration]** > **[!UICONTROL Reporting].**

U kunt de volgende instellingen opgeven op deze pagina:

* De Adobe Experience Cloud-oplossing voor rapportage
* De tijdzone die moet worden gebruikt voor rapportage
* De valuta die moet worden gebruikt voor rapportage
* IP adressen om van rapportering uit te sluiten
* Of een geraamde toename van de inkomsten in de rapportage moet worden weergegeven
* Of fijnkorrelige prioriteiten mogelijk moeten worden gemaakt

>[!NOTE]
>
>Houd er rekening mee dat de tijdzone, de valuta en IP-adressen waarop instellingen moeten worden uitgesloten van toepassing zijn op activiteiten die gebruikmaken [!DNL Target] rapportage. Deze instellingen zijn niet van toepassing op activiteiten die [Analyses voor doel (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md) of [!DNL Customer Journey Analytics] als de bron van de rapportage.

![Pagina rapporteren](/help/main/administrating-target/assets/reporting.png)

## Cloudoplossing rapporteren {#solution}

Stel opties in om te bepalen welke gegevens worden gebruikt voor de resultaten en rapporten.

Selecteer de rapporteringsbron voor uw activiteiten, of [!DNL Target], [!DNL Adobe Analytics], of [!DNL Adobe Customer Journey Analytics]. U kunt ook de rapportbron per activiteit selecteren als onderdeel van een driedelige geleide workflow terwijl u de activiteit maakt.

Houd rekening met de volgende informatie wanneer u uw rapportbron kiest:

* **[!DNL Adobe Target]**: Indien de bron van de rapportage is ingesteld op **[!DNL Target]** U mag hier geen activiteit maken of activeren die [!DNL Analytics] of [!DNL Customer Journey Analytics] als de bron van de rapportage. U moet de rapportbron wijzigen in **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Analytics]**: Indien de bron van de rapportage is ingesteld op **[!DNL Analytics]** U mag hier geen activiteit maken of activeren die [!DNL Target] of [!DNL Customer Journey Analytics] als de bron van de rapportage. U moet de rapportbron wijzigen in **[!UICONTROL Select per activity]**.
* **[!DNL Adobe Customer Journey Analytics]**: Indien de bron van de rapportage is ingesteld op **[!DNL Customer Journey Analytics]** U mag hier geen activiteit maken of activeren die [!DNL Target] of [!DNL Analytics] als de bron van de rapportage. U moet de rapportbron wijzigen in **[!UICONTROL Select per activity]**.
* **Selecteren per activiteit**: Indien de bron van de rapportage is ingesteld op **[!UICONTROL Select per activity]** Hier kunt u activiteiten maken en activeren die worden ondersteund door de geselecteerde rapportbron.

Houd rekening met de volgende informatie wanneer u de rapportbron bepaalt:

* **[!DNL Analytics]**: Voor een matrix van ondersteunde activiteiten die [!DNL Analytics] als rapportagebron (A4T), zie [Ondersteunde activiteitstypen](/help/main/c-integrating-target-with-mac/a4t/a4t.md#section_F487896214BF4803AF78C552EF1669AA) in *Adobe Analytics als bron van rapportage voor Adobe Target (A4t)*.

  [!UICONTROL Automated Personalization] (AP) het creëren en activeren van activiteiten is toegestaan ongeacht de geselecteerde bron van rapportage. [!UICONTROL Automated Personalization] activiteiten worden niet ondersteund wanneer u [Adobe Analytics als bron van rapportage voor Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

  Zelfs als u [!DNL Analytics] als bron voor de rapportage, [!DNL Target] wordt gebruikt als bron van rapportage voor [!DNL Automated Personalization] activiteiten.

* **[!DNL Customer Journey Analytics]**: Voor een matrix van ondersteunde activiteiten die [!DNL Target] rapporteren in [!DNL Customer Journey Analytics], zie [Ondersteunde activiteitstypen](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md#supported-activities) in *[!DNL Target]rapporteren in[!DNL Adobe Customer Journey Analytics]*.

  [!UICONTROL Automated Personalization] (AP), [!UICONTROL Auto-Allocate], en [!UICONTROL Auto-Target] het creëren en activeren van activiteiten is toegestaan, ongeacht de gekozen bron van rapportage. Deze activiteiten worden niet ondersteund wanneer u [Adobe Customer Journey Analytics als bron van rapportage](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

  Zelfs als u [!DNL Customer Journey Analytics] als bron voor de rapportage, [!DNL Target] wordt gebruikt als bron van rapportage voor [!DNL Automated Personalization] activiteiten.

  Als u [!DNL Customer Journey Analytics] als rapportagebron voor [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteiten, [!DNL Target] of [!DNL Analytics] kan worden gebruikt als bron van rapportage.

## Tijdzone voor rapportage

Geef de tijdzone op die moet worden gebruikt voor rapportage.

## Valuta voor rapportage

Geef de valuta op die moet worden gebruikt voor rapportage.

## IPs om van uit te sluiten [!DNL Target] rapportagegegevens

Specificeer om het even welke IP adressen die u van het melden van gegevens wilt uitsluiten. Het uitsluiten van interne bedrijfsadressen is bijvoorbeeld een goede manier om ervoor te zorgen dat uw rapportgegevens de interactie van klanten op uw website weerspiegelen.

Ga elk IP adres op een nieuwe lijn in.

## Geraamde verhoging van de ontvangsten tonen

U kunt kiezen om de geschatte verhoging van opbrengst te tonen als u een monetaire waarde voor uw doel ingaat. [!DNL Target] U kunt een schatting maken van de inkomstenbelasting die u kunt bereiken als alle gebruikers de winnende ervaring bekijken. De functie voor het schatten van de lift is standaard uitgeschakeld.

Alleen [!DNL Experience Cloud] Beheerders kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.

Zie voor meer informatie [Schatting van de opbrengst](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md).

## Geavanceerde prioriteiten inschakelen

Numerieke items toestaan voor een prioriteit tussen 0 en 999.

Afhankelijk van uw instellingen variëren de interface en opties voor prioriteit. U kunt de oudere instellingen Laag, Normaal of Hoog gebruiken of u kunt fijnkorrelige prioriteiten van 0 tot en met 999 inschakelen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.
