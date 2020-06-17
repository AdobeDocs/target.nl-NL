---
description: Target Standard kan worden geïntegreerd met Adobe Dynamic Media Classic (voorheen Scene7) voor Digital Asset Management (DAM) in de inhoudsbibliotheek.
title: Dynamic Media Klassieke integratie-integratie
subtopic: Getting Started
topic: Standard
uuid: 4b06a3ed-0e87-4e49-874f-2e479324f81c
translation-type: tm+mt
source-git-commit: 44d9024cb9c1f6a1e28845f9545fed0d56fe176a
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Dynamic Media Klassieke integratie{#scene-settings}

Target kan worden geïntegreerd met Adobe Dynamic Media Classic (voorheen Scene7) voor Digital Asset Management (DAM) in de inhoudsbibliotheek.

>[!NOTE]
>
>De informatie in dit onderwerp is bijgewerkt om u een sluimerpiek bij de veranderingen te geven UI die in Target Standard/Premium 20.6.1 versie (Juli 2020) komen. De meeste informatie die in dit onderwerp wordt voorgesteld is op huidige UI van toepassing; de opties kunnen zich echter op iets andere locaties bevinden .

>[!NOTE]
>
>Als u Target integreert met Dynamic Media Classic, kunt u elementen (als onderdeel van activiteiten) die zijn geüpload naar de map met Adobe Experience Cloud-middelen, leveren. Deze integratie maakt geen toegang mogelijk tot alle in Dynamic Media Classic geüploade middelen voor levering in Target-activiteiten.

Als u al een account voor Dynamic Media hebt, kunt u uw bestaande gegevens opgeven. Als u geen account hebt, kunt u zonder extra kosten een Classic-account voor beperkt gebruik aanvragen bij uw Adobe-vertegenwoordiger. Deze account kan alleen worden gebruikt voor doeleinden die beperkt zijn tot Target. Deze service wordt beschikbaar gesteld aan klanten voor workflows die functionaliteit voor het wisselen van afbeeldingen nodig hebben.

Als deze instelling niet is geconfigureerd, is de optie Afbeelding verwisselen in de workflow voor het maken van activiteiten niet beschikbaar. Nadat dit plaatsen wordt gevormd, is de optie om beeldaanbiedingen te ruilen/veranderen beschikbaar in zowel Composer van de [Visuele Ervaring (VEC) als in de vorm-Gebaseerde Composer](../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)van de Ervaring. Vervolgens kunt u afbeeldingsaanbiedingen gebruiken met afbeeldingen die vanuit de Adobe Experience Cloud zijn geüpload voor gebruik in Target-activiteiten.

Als u tijdens het maken van activiteiten rechtstreeks in een aanbieding of aangepaste code wilt verwijzen naar een openbare afbeeldings-URL, moet u de afbeelding op uw eigen webservers implementeren en uw eigen URL in de code gebruiken. Er is geen manier om de gepubliceerde URL te verkrijgen van een afbeelding die in de Experience Cloud is geüpload om direct of buiten de doelworkflows met Adobe Target te gebruiken. Deze functionaliteit is niet toegestaan, zoals in een contract.

De opslag-URL en de uiteindelijke publicatie-URL&#39;s van afbeeldingen van Dynamic Media verschillen en er mogen GEEN aanbiedingen worden gemaakt met de opslagkoppeling van afbeeldingen, omdat de levering in dergelijke gevallen niet werkt. U moet gebruikmaken van de mogelijkheid om het image te maken, zoals wordt uitgelegd in de Help-documentatie.

Om met Dynamic Media Klassiek (Scene7) te integreren, moet u de volgende informatie specificeren.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Settings]**.

   ![Pagina Scene7](/help/administrating-target/assets/scene7.png)

1. Geef de volgende klassieke accountgegevens voor Dynamic Media op:

   **Regio:** Het gebied voor uw account voor Dynamic Media: Noord-Amerika, Europa of Azië.

   **Ad-hocmap:** De locatie voor inhoud die zich buiten de doelmap bevindt en handmatig naar Dynamic Media wordt geüpload.

   **E-mailadres:** Het e-mailadres dat wordt gebruikt om zich aan te melden bij Dynamic Media Classic (Scene7).

   **Wachtwoord:** Het wachtwoord dat wordt gebruikt om aan login aan Dynamic Media Klassiek (Scene7).

1. Klik op **[!UICONTROL Submit]**.
