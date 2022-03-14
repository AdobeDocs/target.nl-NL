---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Leer hoe u Adobe kunt integreren [!DNL Target] met Adobe Dynamic Media Classic (voorheen Scene7) om Digital Asset Management (DAM) te leveren in de Content Library.
title: Hoe vorm ik de integratie van Dynamic Media Classic (Scene7)?
feature: Administration & Configuration
role: Admin
exl-id: 315670ca-a4d1-4808-b3ec-f2ac195c281a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Dynamic Media Classic-configuratie (voorheen Scene7)

[!DNL Adobe Target] kan worden geïntegreerd met [!DNL Adobe Dynamic Media Classic] (voorheen) [!DNL Scene7]) om Digital Asset Management (DAM) in de [!UICONTROL Content Library].

>[!NOTE]
>
>Integreren [!DNL Target] with [!DNL Dynamic Media Classic] de levering van activa (als onderdeel van activiteiten) die zijn geüpload naar de [!DNL Adobe Experience Cloud] map met middelen. Deze integratie maakt geen toegang mogelijk tot alle elementen die zijn geüpload in [!DNL Dynamic Media Classic] voor levering in [!DNL Target] activiteiten.

Als u al een [!DNL Dynamic Media] -account, kunt u uw bestaande gegevens opgeven. Als u geen account hebt, kunt u om een beperkt gebruik vragen [!DNL Dynamic Media Classic] gratis account van uw [!DNL Adobe] vertegenwoordiger. Deze account kan worden gebruikt voor doeleinden die zijn beperkt voor gebruik in [!DNL Target] alleen. Deze service wordt beschikbaar gesteld aan klanten voor workflows die functionaliteit voor het wisselen van afbeeldingen nodig hebben.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Als dit plaatsen niet wordt gevormd, [!UICONTROL Swap Image offer] is niet beschikbaar in de workflow voor het maken van activiteiten. Nadat deze instelling is geconfigureerd, is de optie voor het omwisselen/wijzigen van afbeeldingsaanbiedingen beschikbaar in beide [Visual Experience Composer (VEC) en in de Form-Based Experience Composer](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). U kunt dan afbeeldingsaanbiedingen gebruiken met afbeeldingen die zijn geüpload vanuit het [!DNL Adobe Experience Cloud] voor gebruik in [!DNL Target] activiteiten.

Als u tijdens het maken van activiteiten rechtstreeks in een aanbieding of aangepaste code wilt verwijzen naar een openbare afbeeldings-URL, moet u de afbeelding op uw eigen webservers implementeren en uw eigen URL in de code gebruiken. Er is geen manier om de gepubliceerde URL te verkrijgen van een afbeelding die is geüpload naar de [!DNL Experience Cloud] om direct of buiten doelworkflows te gebruiken [!DNL Target]. Deze functionaliteit is niet toegestaan, zoals in een contract.

De opslag-URL en de uiteindelijke publicatie-URL&#39;s van afbeeldingen vanuit [!DNL Dynamic Media] verschillen en moet *NOT* aanbiedingen maken met behulp van de opslagkoppeling van afbeeldingen, omdat de levering in dergelijke gevallen niet werkt. U moet het beeld gebruiken biedt mogelijkheden zoals die in onze hulpdocumentatie worden verklaard.

Om te integreren met [!DNL Dynamic Media Classic] ([!DNL Scene7]), moet u de volgende informatie opgeven.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

   ![Scene7-pagina](/help/main/administrating-target/assets/scene7.png)

1. Geef het volgende op [!DNL Dynamic Media Classic] accountgegevens:

   **Regio:** Het gebied voor uw [!DNL Dynamic Media] account: Noord-Amerika, Europa of Azië.

   **Ad-hocmap:** De locatie voor inhoud die zich buiten de doelmap bevindt en die handmatig wordt geüpload naar [!DNL Dynamic Media].

   **E-mailadres:** Het e-mailadres waarmee u zich aanmeldt bij [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Wachtwoord:** Het wachtwoord dat wordt gebruikt om u aan te melden bij [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Klik op **[!UICONTROL Submit]**.
