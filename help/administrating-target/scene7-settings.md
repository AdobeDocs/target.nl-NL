---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: Adobe Target kan worden geïntegreerd met Adobe Dynamic Media Classic (voorheen Scene7) voor Digital Asset Management (DAM) in de inhoudsbibliotheek.
title: Integratie van Dynamic Media Classic-integratie
feature: Administration & Configuration
translation-type: tm+mt
source-git-commit: 2e80c972e432ce97596c856dd396b8f1be05a61a
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---


# Dynamic Media Classic-configuratie (voorheen Scene7)

[!DNL Adobe Target] kan worden geïntegreerd met  [!DNL Adobe Dynamic Media Classic] (voorheen  [!DNL Scene7]) Digital Asset Management (DAM) in de  [!UICONTROL Content Library].

>[!NOTE]
>
>Door [!DNL Target] te integreren met [!DNL Dynamic Media Classic], kunnen elementen (als onderdeel van activiteiten) worden geleverd die naar de map [!DNL Adobe Experience Cloud] assets zijn geüpload. Deze integratie maakt geen toegang mogelijk tot alle elementen die in [!DNL Dynamic Media Classic] zijn geüpload voor levering in [!DNL Target]-activiteiten.

Als u al een [!DNL Dynamic Media] account hebt, kunt u uw bestaande referenties opgeven. Als u geen account hebt, kunt u uw [!DNL Dynamic Media Classic]-vertegenwoordiger om een beperkte-gebruikaccount verzoeken zonder extra kosten. [!DNL Adobe] Deze account kan alleen worden gebruikt voor doeleinden die zijn beperkt tot [!DNL Target]. Deze service wordt beschikbaar gesteld aan klanten voor workflows die functionaliteit voor het wisselen van afbeeldingen nodig hebben.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Als deze instelling niet is geconfigureerd, is de optie [!UICONTROL Swap Image offer] in de workflow voor het maken van activiteiten niet beschikbaar. Nadat dit het plaatsen wordt gevormd, is de optie om beeldaanbiedingen te ruilen/veranderen beschikbaar in zowel [Visuele Composer van de Ervaring (VEC) als in Form-Based Composer van de Ervaring](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D). Vervolgens kunt u afbeeldingsaanbiedingen gebruiken met afbeeldingen die zijn geüpload van [!DNL Adobe Experience Cloud] voor gebruik in [!DNL Target]-activiteiten.

Als u tijdens het maken van activiteiten rechtstreeks in een aanbieding of aangepaste code wilt verwijzen naar een openbare afbeeldings-URL, moet u de afbeelding op uw eigen webservers implementeren en uw eigen URL in de code gebruiken. Er is geen manier om de gepubliceerde URL te verkrijgen van een afbeelding die is geüpload naar [!DNL Experience Cloud] om direct of buiten de doelworkflows te gebruiken met [!DNL Target]. Deze functionaliteit is niet toegestaan, zoals in een contract.

De opslag-URL en de uiteindelijke publicatie-URL&#39;s van afbeeldingen van [!DNL Dynamic Media] verschillen en *NOT* moet aanbiedingen maken met behulp van de opslagkoppeling van afbeeldingen, aangezien de levering in dergelijke gevallen niet werkt. U moet het beeld gebruiken biedt mogelijkheden zoals die in onze hulpdocumentatie worden verklaard.

Om met [!DNL Dynamic Media Classic] ([!DNL Scene7]) te integreren, moet u de volgende informatie specificeren.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

   ![Scene7-pagina](/help/administrating-target/assets/scene7.png)

1. Geef de volgende [!DNL Dynamic Media Classic] accountgegevens op:

   **Regio:** Het gebied voor uw  [!DNL Dynamic Media] account: Noord-Amerika, Europa of Azië.

   **Ad-hocmap:** de locatie voor inhoud die zich buiten de doelmap bevindt en handmatig wordt geüpload naar  [!DNL Dynamic Media].

   **E-mailadres:** Het e-mailadres dat wordt gebruikt voor aanmelding bij  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Wachtwoord:** het wachtwoord waarmee u zich aanmeldt bij  [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Klik op **[!UICONTROL Submit]**.
