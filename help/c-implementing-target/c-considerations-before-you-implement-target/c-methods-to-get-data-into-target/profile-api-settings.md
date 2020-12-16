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
1. Schuif onder **[!UICONTROL Profile API]** de schakeloptie **[!UICONTROL Require Authentication]** naar de in- of uitgeschakeld positie.

   ![](assets/profile_api_settings.png)

1. (Voorwaardelijk) Als u authentificatievereisten toeliet, klik **[!UICONTROL Generate New Profile Authentication Token]**.

   ![](assets/profile_api_settings_2.png)

   Het teken verloopt volgens de tijd die in [!UICONTROL Expires In] doos wordt vermeld.

   U moet een van de volgende gebruikersmachtigingen hebben om een verificatietoken te genereren:

   * Minstens [!UICONTROL Editor] toestemming (of [!UICONTROL Approver])

      Voor meer informatie voor [!DNL Target Standard] klanten, zie [Specificeer rollen en Toestemmingen](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers*. Zie [Bedrijfsmachtigingen configureren](/help/administrating-target/c-user-management/property-channel/properties-overview.md) voor meer informatie voor [!DNL Target Premium]-klanten.

   * Beheerdersrol op het niveau van de werkruimte/het productprofiel

      Werkruimten zijn alleen beschikbaar voor klanten van [!DNL Target Premium]. Zie [Bedrijfsmachtigingen configureren](/help/administrating-target/c-user-management/property-channel/properties-overview.md) voor meer informatie.

   * Admin Rights (toestemming Sysadmin) op het [!DNL Adobe Target] productniveau
   >[!NOTE]
   >
   >U kunt ook een profielverificatietoken genereren via de API. Zie [Profielen](https://developers.adobetarget.com/api/#profiles) op de [Adobe Target-website voor ontwikkelaars](https://developers.adobetarget.com/) voor meer informatie.

1. Kopieer het token en neem het op in de koptekst van het verzoek in de notatie: &quot;Toestemming&quot; : &quot;Teller&quot;

Klik [!UICONTROL Generate New Profile Authentication Token] om het token opnieuw te genereren.

>[!IMPORTANT]
>
>Als u dit token opnieuw instelt, mislukken API-aanroepen met het huidige token. Hiervoor moeten alle scripts of apps die deze token gebruiken, worden bijgewerkt.
