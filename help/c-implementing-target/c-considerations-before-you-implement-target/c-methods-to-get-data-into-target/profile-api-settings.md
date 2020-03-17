---
keywords: implementation;api;profile;profile api settings
description: Schakel verificatie voor batchupdates via API in of uit en genereer een profielverificatietoken.
title: Profiel-API-instellingen
subtopic: Getting Started
topic: Standard
uuid: 481b4a14-f10f-47cd-988d-9e6b8c4d5c00
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Profiel-API-instellingen{#profile-api-settings}

Schakel verificatie voor batchupdates via API in of uit en genereer een profielverificatietoken.

Adobe Target maakt en onderhoudt een profiel voor elke individuele gebruiker. Dit profiel wordt opgeslagen in de doelEdge-cluster en wordt na elk bezoek in realtime bijgewerkt. U kunt een profiel echter afzonderlijk of bulksgewijs bijwerken via de API.

Voor extra veiligheid, kunt u vereisen dat de Bulk API vraag van de Update een geldig toegangstoken wordt overgegaan in de kopbal van het verzoek. Gebruikers met de machtiging fiatteur kunnen tokens voor API-profielverificatie genereren en inschakelen.

**Om authentificatie te vereisen en een toegangstoken te produceren gebruikend het Doel UI:**

1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Implementation]**.
1. In **[!UICONTROL Profile API Settings]**, gebruik de **[!UICONTROL Require Authentication]** drop-down lijst om authentificatievereisten in of onbruikbaar te maken.

   ![](assets/profile_api_settings.png)

1. (Voorwaardelijk) Als u authentificatievereisten toeliet, klik **[!UICONTROL Generate Pofile Authentication Token]**.

   ![](assets/profile_api_settings_2.png)

   Het token verloopt volgens de tijd die in het [!UICONTROL Expires In] vak staat.

   >[!NOTE]
   >
   >U kunt ook een profielverificatietoken genereren via de API. Zie [Profielen](https://developers.adobetarget.com/api/#profiles) op de website [van](https://developers.adobetarget.com/)Adobe Target Developers voor meer informatie.

1. Kopieer het token en neem het op in de koptekst van het verzoek in de notatie: &quot;Toestemming&quot; : &quot;Teller&quot;

Klik [!UICONTROL Re-generate Profile Authentication Token] om het token zo nodig opnieuw te genereren.

>[!IMPORTANT]
>
>Als u dit token opnieuw instelt, mislukken API-aanroepen met het huidige token. Hiervoor moeten alle scripts of apps die deze token gebruiken, worden bijgewerkt.

