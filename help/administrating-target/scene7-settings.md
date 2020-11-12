---
keywords: scene7;dynamic media classic;digital asset management;assets;dam;content library;swap image
description: De doelstandaard kan worden geïntegreerd met Adobe Dynamic Media Classic om DAM (Digital Asset Management) in de inhoudsbibliotheek te bieden.
title: Integratie van dynamische Media Classic-integratie
feature: administration general
translation-type: tm+mt
source-git-commit: 44c2a1dd1fa51cb7ea50a5e3d0125ba9abb1896c
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---


# Scene7-configuratie {#scene-settings}

[!DNL Target] kan worden geïntegreerd [!DNL Adobe Dynamic Media Classic] om Digital Asset Management (DAM) in de [!UICONTROL Content Library]website te bieden.

>[!NOTE]
>
>Door integratie [!DNL Target] met [!DNL Dynamic Media Classic] kunt u elementen (als onderdeel van activiteiten) uploaden naar de map [!DNL Adobe Experience Cloud] assets. Deze integratie maakt geen toegang mogelijk tot alle elementen die in [!DNL Dynamic Media Classic] de computer zijn geüpload voor levering in [!DNL Target] activiteiten.

Als u al een [!DNL Dynamic Media] account hebt, kunt u uw bestaande gegevens opgeven. Als u geen account hebt, kunt u gratis een account voor beperkt gebruik aanvragen bij uw [!DNL Dynamic Media Classic] [!DNL Adobe] vertegenwoordiger. Deze account kan [!DNL Target] alleen worden gebruikt voor doeleinden waarvoor beperkingen gelden. Deze service wordt beschikbaar gesteld aan klanten voor workflows die functionaliteit voor het wisselen van afbeeldingen nodig hebben.

<!-- 
>[!NOTE]
>
>A restricted-use, free [!DNL Dynamic Media Classic] account for [!DNL Adobe Target] is no longer supported for new customers or new users. Existing sign-in credentials work as usual. 
-->

Als deze instelling niet is geconfigureerd, is de [!UICONTROL Swap Image offer] optie in de workflow voor het maken van activiteiten niet beschikbaar. Nadat dit plaatsen wordt gevormd, is de optie om beeldaanbiedingen te ruilen/veranderen beschikbaar in zowel Composer van de [Visuele Ervaring (VEC) als in de vorm-Gebaseerde Composer](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)van de Ervaring. Vervolgens kunt u afbeeldingsaanbiedingen gebruiken met afbeeldingen die vanuit de toepassing zijn geüpload [!DNL Adobe Experience Cloud] voor gebruik in [!DNL Target] activiteiten.

Als u tijdens het maken van activiteiten rechtstreeks in een aanbieding of aangepaste code wilt verwijzen naar een openbare afbeeldings-URL, moet u de afbeelding op uw eigen webservers implementeren en uw eigen URL in de code gebruiken. Het is niet mogelijk om de gepubliceerde URL te verkrijgen van een afbeelding die naar de server is geüpload [!DNL Experience Cloud] om direct of buiten de doelworkflows voor gebruik [!DNL Target]te gebruiken. Deze functionaliteit is niet toegestaan, zoals in een contract.

De opslag-URL en de uiteindelijke publicatie-URL&#39;s van afbeeldingen van [!DNL Dynamic Media] elkaar verschillen en er mogen *GEEN* aanbiedingen worden gemaakt met behulp van de opslagkoppeling van afbeeldingen, aangezien de levering in dergelijke gevallen niet werkt. U moet het beeld gebruiken biedt mogelijkheden zoals die in onze hulpdocumentatie worden verklaard.

Om met [!DNL Dynamic Media Classic] ([!DNL Scene7]) te integreren, moet u de volgende informatie specificeren.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Scene7 Configuration]**.

   ![Scene7-pagina](/help/administrating-target/assets/scene7.png)

1. Geef de volgende [!DNL Dynamic Media Classic] accountgegevens op:

   **Regio:** De regio voor uw [!DNL Dynamic Media] account: Noord-Amerika, Europa of Azië.

   **Ad-hocmap:** De locatie voor inhoud die zich buiten de doelmap bevindt en waarnaar handmatig wordt geüpload. [!DNL Dynamic Media]

   **E-mailadres:** Het e-mailadres dat wordt gebruikt om u aan te melden bij [!DNL Dynamic Media Classic] ([!DNL Scene7]).

   **Wachtwoord:** Het wachtwoord dat wordt gebruikt om u aan te melden bij [!DNL Dynamic Media Classic] ([!DNL Scene7]).

1. Klik op **[!UICONTROL Submit]**.
