---
keywords: Beheer;goedkeurende rol;fiatteur
description: Voer de eerste taken uit  [!DNL Adobe Target]  beheerders zouden na het ontvangen van de e-mailuitnodiging aan  [!DNL Adobe Experience Cloud] moeten nemen.
title: Waar wordt ik begonnen Administering  [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: b60236da-20ae-4bab-b261-6a33d2f70e23
source-git-commit: 614fd89c9746ce55f502debd5b689c34de400ae5
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Eerste stappen van beheerder

Dit artikel bevat de eerste stappen die [!DNL Adobe Target] -beheerders moeten uitvoeren nadat ze de e-mailuitnodiging voor de [!DNL Adobe Experience Cloud] hebben ontvangen.

## Welkom bij [!DNL Target] {#task_3E0817630774431983FAA3D2CB2E75BD}

Een systeembeheerder in [!DNL Adobe Admin Console] moet u als gebruiker in [!DNL Target] toevoegen door u uit te nodigen om zich aan te sluiten. De systeembeheerder zou u dan aan één of meerdere rol-specifieke productprofielen (groepen gebruikers) moeten toevoegen. Beide taken worden uitgevoerd in [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com).

Voor meer informatie, zie [&#x200B; gebruikersgroepen &#x200B;](https://helpx.adobe.com/nl/enterprise/using/users.html) leiden.

U ontvangt een uitnodigingse-mail nadat de systeembeheerder deze stappen heeft uitgevoerd.

## De uitnodiging accepteren {#task_24FE66659E634B24AB61DB8497772E17}

Nadat u de uitnodiging hebt ontvangen om deel te nemen aan de [!DNL Adobe Experience Cloud] , accepteert u de uitnodiging, meldt u zich aan en accepteert u de [!UICONTROL End User License Agreement] (EULA).

1. Accepteer de uitnodiging voor de [!DNL Adobe Experience Cloud] .
1. Als u nog geen Adobe ID hebt, wordt u gevraagd om er een te maken.

   Als u een Adobe ID hebt, wordt uw Adobe ID herkend en wordt u gevraagd u aan te melden.
1. Accepteer de [!UICONTROL Terms of Use] .
1. Bekijk de samenvatting van wat u tot nu toe hebt gedaan en klik vervolgens op **[!UICONTROL Continue to Experience Cloud]** .
1. Meld u aan bij de [!DNL Adobe Experience Cloud] en klik op **[!UICONTROL Link Account]** .

   >[!NOTE]
   >
   >Als u uw account niet koppelt, hebt u geen toegang tot [!DNL Target] .

   Alle [!UICONTROL Experience Cloud] -producten worden weergegeven op de koppelingspagina. Klik op `Link Target` en voer uw [!DNL Target] gebruikersnaam en wachtwoord in om toegang te krijgen tot [!DNL Target] .
1. Klik op **[!UICONTROL Continue to Experience Cloud]**.

   U hebt op dit moment nog geen groepen ingesteld met rechten die u kunt koppelen.
1. Bekijk desgewenst de video waarin u wordt geïntroduceerd op de [!DNL Adobe Experience Cloud] .
1. Als u de nieuwe rechten wilt zien en toegang wilt krijgen tot het product, meldt u zich af bij [!DNL Adobe Experience Cloud] en meldt u zich vervolgens weer aan.
1. Ga aan de volgende stap verder, [&#x200B; toewijzend zelf de rol Approver &#x200B;](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Wijs me de rol van fiatteur toe {#task_15CAA437A71444E2932B333D5E66A3C7}

Nadat u de uitnodiging om deel te nemen aan [!DNL Adobe Experience Cloud] hebt geaccepteerd en zich hebt aangemeld, bevestigt u dat [!DNL Target] is toegevoegd aan uw [!DNL Experience Cloud] -account en wijst u uzelf vervolgens de [!UICONTROL Approver] rol voor [!DNL Target] toe.

Als uw organisatie a [&#x200B; Target Standard &#x200B;](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) vergunning heeft, zie [&#x200B; rollen en toestemmingen &#x200B;](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers* specificeren.

Als uw organisatie a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) vergunning heeft, zie [&#x200B; Stap 6: Specificeer rollen en toestemmingen &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *vorm ondernemingstoestemmingen*.

In de volgende stap moeten gebruikers worden ingesteld in [!DNL Target Standard] en [!DNL Target Premium] . Voor meer informatie, zie [&#x200B; Gebruikersbeheer &#x200B;](/help/main/administrating-target/c-user-management/user-management.md).

## Machtigingen vereist voor het bewerken van [!UICONTROL Administration] -instellingen {#admin-permissions}

**vóór 22 April, 2025**: De gebruikers met [!UICONTROL Approvers] rechten in [!DNL Adobe Admin Console] kunnen alle montages op de [[!UICONTROL Administration] pagina &#x200B;](/help/main/administrating-target/administrating-target.md) pagina van [!DNL Target] uitgeven of veranderen, ongeacht hun [!DNL Target] rol.

**Ingetreden 22 April, 2025**: Slechts [!UICONTROL Product] en [!UICONTROL Solutions] admins zullen montages in de [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md) secties, ongeacht hun rollen in [!DNL Target] werkruimten kunnen bijwerken. Gebruikers zonder deze machtiging hebben alleen-lezen toegang tot de secties van [!UICONTROL Administration] .

Deze update verbetert de organisatorische controle over [!DNL Target] instantieconfiguraties, die toevallige updates verhinderen die activiteitenlevering over diverse test en verpersoonlijkingsteams zouden kunnen beïnvloeden.
