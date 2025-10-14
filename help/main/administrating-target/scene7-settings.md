---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Leer hoe te om Adobe  [!DNL Target]  met Adobe Dynamic Media Classic (vroeger Scene7) te integreren om het Digitale Beheer van Activa (DAM) in de Bibliotheek van de Inhoud te verstrekken.
title: Hoe vorm ik de integratie van Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
source-git-commit: 12831d6584acc482db415629d7e70a18e39c47c2
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Dynamic Media Classic (voorheen Scene7) configuratie

[!DNL Adobe Target] kan worden geïntegreerd met [!DNL Adobe Dynamic Media Classic] (voorheen [!DNL Scene7] ) voor DAM (Digital Asset Management) in de [!UICONTROL Content Library] .

{{permissions-update}}

>[!NOTE]
>
>Door [!DNL Target] te integreren met [!DNL Dynamic Media Classic] , kunnen elementen (als onderdeel van activiteiten) die naar de map [!DNL Adobe Experience Cloud] assets zijn geüpload, worden geleverd. Deze integratie maakt geen toegang mogelijk tot alle elementen die in [!DNL Dynamic Media Classic] zijn geüpload voor levering in [!DNL Target] -activiteiten.

Als u al een [!DNL Dynamic Media] -account hebt, kunt u uw bestaande referenties opgeven. Als u geen account hebt, kunt u gratis een [!DNL Dynamic Media Classic] -account voor beperkt gebruik aanvragen bij uw [!DNL Adobe] -vertegenwoordiger. Dit account kan alleen worden gebruikt voor doeleinden die zijn beperkt tot [!DNL Target] . Deze service wordt beschikbaar gesteld aan klanten voor workflows die functionaliteit voor het wisselen van afbeeldingen nodig hebben.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Als deze instelling niet is geconfigureerd, is de optie [!UICONTROL Swap Image offer] in de workflow voor het maken van activiteiten niet beschikbaar. Nadat dit plaatsen wordt gevormd, is de optie om beeldaanbiedingen te ruilen/veranderen beschikbaar in zowel [&#x200B; Visuele Composer van de Ervaring (VEC) als in de op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Vervolgens kunt u afbeeldingsaanbiedingen gebruiken met afbeeldingen die vanuit de [!DNL Adobe Experience Cloud] zijn geüpload voor gebruik in [!DNL Target] -activiteiten.

Als u tijdens het maken van activiteiten rechtstreeks in een aanbieding of aangepaste code wilt verwijzen naar een openbare afbeeldings-URL, moet u de afbeelding op uw eigen webservers implementeren en uw eigen URL in de code gebruiken. Het is niet mogelijk de gepubliceerde URL te verkrijgen van een afbeelding die in [!DNL Experience Cloud] is geüpload om direct of buiten doelworkflows met [!DNL Target] te gebruiken. Deze functionaliteit is niet toegestaan, zoals in een contract.

Merk op dat de opslag URL en definitief URLs van beelden van [!DNL Dynamic Media] verschillend zijn en men *NIET* moet aanbiedingen creëren gebruikend de opslagverbinding van beelden aangezien de levering in dergelijke gevallen niet zal werken. U moet het beeld gebruiken biedt mogelijkheden zoals die in onze hulpdocumentatie worden verklaard.

Als u wilt integreren met [!DNL Dynamic Media Classic] ([!DNL Scene7] ), moet u de volgende informatie opgeven.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]** .

1. Geef de volgende [!DNL Dynamic Media Classic] accountgegevens op:

   **Gebied:** het gebied voor uw [!DNL Dynamic Media] rekening: Noord Amerika, Europa, of Azië.

   **Adhoc omslag:** de plaats voor inhoud die buiten de doelomslag verblijft en manueel aan [!DNL Dynamic Media] wordt geupload.

   **E-mailadres:** Het e-mailadres dat aan login aan [!DNL Dynamic Media Classic] wordt gebruikt ([!DNL Scene7]).

   **Wachtwoord:** het wachtwoord dat aan login aan [!DNL Dynamic Media Classic] wordt gebruikt ([!DNL Scene7]).

1. Klik op **[!UICONTROL Submit]**.
