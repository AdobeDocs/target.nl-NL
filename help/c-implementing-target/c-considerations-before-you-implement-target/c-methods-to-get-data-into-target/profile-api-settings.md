---
keywords: implementation;api;profile;profile api settings;authentication token
description: Schakel verificatie voor batchupdates via Adobe Target API's in of uit en genereer een profielverificatietoken.
title: Profiel-API-instellingen in Adobe Target
feature: api
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# Profiel-API-instellingen

Schakel verificatie voor batchupdates via Adobe Target API&#39;s in of uit en genereer een profielverificatietoken.

[!DNL Adobe Target] maakt en onderhoudt een profiel voor elke individuele gebruiker. Dit profiel wordt opgeslagen in de [!DNL Target] Edge-cluster en wordt na elk bezoek in real-time bijgewerkt. echter, kunt u een profiel individueel of in bulk bijwerken via API.

Voor extra veiligheid, kunt u vereisen dat de Bulk API vraag van de Update een geldig toegangstoken wordt overgegaan in de kopbal van het verzoek.

**Om authentificatie te vereisen en een toegangstoken te produceren gebruikend het Doel UI:**

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. Onder **[!UICONTROL Profile API]** dia de **[!UICONTROL Require Authentication]** knevel aan toegelaten of gehandicapte positie.

   ![](assets/profile_api_settings.png)

1. (Voorwaardelijk) Als u authentificatievereisten toeliet, klik **[!UICONTROL Generate New Profile Authentication Token]**.

   ![](assets/profile_api_settings_2.png)

   Het token verloopt volgens de tijd die in het [!UICONTROL Expires In] vak staat.

   U moet een van de volgende gebruikersmachtigingen hebben om een verificatietoken te genereren:

   * Minstens [!UICONTROL Editor] toestemming (of [!UICONTROL Approver])

      Voor meer informatie voor [!DNL Target Standard] klanten, zie [Specificeer rollen en Toestemmingen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers*. Voor meer informatie voor [!DNL Target Premium] klanten, zie ondernemingstoestemmingen [](/help/administrating-target/c-user-management/property-channel/properties-overview.md)vormen.

   * Beheerdersrol op het niveau van de werkruimte/het productprofiel

      De werkruimten zijn alleen beschikbaar voor [!DNL Target Premium] klanten. Voor meer informatie, zie ondernemingstoestemmingen [](/help/administrating-target/c-user-management/property-channel/properties-overview.md)vormen.

   * Admin Rights (Sysadmin-machtiging) op [!DNL Adobe Target] productniveau
   >[!NOTE]
   >
   >U kunt ook een profielverificatietoken genereren via de API. Zie [Profielen](https://developers.adobetarget.com/api/#profiles) op de website [van](https://developers.adobetarget.com/)Adobe Target Developers voor meer informatie.

1. Kopieer het token en neem het op in de koptekst van het verzoek in de notatie: &quot;Toestemming&quot; : &quot;Teller&quot;

Klik [!UICONTROL Generate New Profile Authentication Token] om het token zo nodig opnieuw te genereren.

>[!IMPORTANT]
>
>Als u dit token opnieuw instelt, mislukken API-aanroepen met het huidige token. Hiervoor moeten alle scripts of apps die deze token gebruiken, worden bijgewerkt.
