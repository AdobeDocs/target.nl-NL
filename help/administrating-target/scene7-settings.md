---
description: De norm van het doel kan met de Klassieke van de Media van Adobe Dynamische (vroeger Scene7) worden geïntegreerd om Digital Asset Management (DAM) in de Inhoudsbibliotheek te verstrekken.
title: Dynamic Media Classic-integratie
subtopic: Getting Started
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Dynamic Media Classic-integratie{#scene-settings}

De norm van het doel kan met de Klassieke van de Media van Adobe Dynamische (vroeger Scene7) worden geïntegreerd om Digital Asset Management (DAM) in de Inhoudsbibliotheek te verstrekken.

>[!NOTE]
>
>Als u Target integreert met Dynamic Media Classic, kunt u elementen (als onderdeel van activiteiten) leveren die zijn geüpload naar de map met Adobe Experience Cloud-middelen. Deze integratie maakt geen toegang mogelijk tot alle elementen die in Dynamic Media Classic zijn geüpload voor levering in Target-activiteiten.

Als u al een Dynamic Media-account hebt, kunt u uw bestaande referenties opgeven. Als u geen account hebt, kunt u gratis een Dynamic Media Classic-account aanvragen bij uw Adobe-vertegenwoordiger. Deze account kan alleen worden gebruikt voor doeleinden die zijn beperkt voor gebruik in Target. Deze service wordt beschikbaar gesteld aan klanten voor workflows die functionaliteit voor het wisselen van afbeeldingen nodig hebben.

Als deze instelling niet is geconfigureerd, is de optie Afbeelding verwisselen in de workflow voor het maken van activiteiten niet beschikbaar. Nadat dit plaatsen wordt gevormd, is de optie om beeldaanbiedingen te ruilen/veranderen beschikbaar in zowel Composer van de [Visuele Ervaring (VEC) als in de vorm-Gebaseerde Composer](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)van de Ervaring. Vervolgens kunt u afbeeldingsaanbiedingen gebruiken met afbeeldingen die vanuit de Adobe Experience Cloud zijn geüpload voor gebruik in Target-activiteiten.

Als u tijdens het maken van activiteiten rechtstreeks in een aanbieding of aangepaste code wilt verwijzen naar een openbare afbeeldings-URL, moet u de afbeelding op uw eigen webservers implementeren en uw eigen URL in de code gebruiken. De gepubliceerde URL van een afbeelding die is geüpload naar de Experience Cloud kan niet worden opgehaald voor directe of externe doelgerichte workflows met Adobe Target. Deze functionaliteit is niet toegestaan, zoals in een contract.

De opslag-URL en de uiteindelijke publicatie-URL&#39;s van afbeeldingen van Dynamic Media verschillen en er mogen GEEN aanbiedingen worden gemaakt met behulp van de opslagkoppeling van afbeeldingen, aangezien de levering in dergelijke gevallen niet werkt. U moet gebruikmaken van de mogelijkheid om het image te maken, zoals wordt uitgelegd in de Help-documentatie.

Om met Dynamische Klassieke Media (Scene7) te integreren, moet u sommige volgende informatie specificeren.

1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Scene7 Settings]**.
1. Geef de volgende gegevens voor de Dynamic Media Classic-account op:

   **Regio:** Het gebied voor uw Dynamic Media-account: Noord-Amerika, Europa of Azië.

   **Ad-hocmap:** De locatie voor inhoud die zich buiten de doelmap bevindt en handmatig naar dynamische media wordt geüpload.

   **E-mailadres:** Het e-mailadres dat wordt gebruikt om zich aan te melden bij Dynamic Media Classic (Scene7).

   **Wachtwoord:** Het wachtwoord dat wordt gebruikt om aan login aan Dynamische Klassieke Media (Scene7).
1. Klik op **[!UICONTROL Submit]**.
