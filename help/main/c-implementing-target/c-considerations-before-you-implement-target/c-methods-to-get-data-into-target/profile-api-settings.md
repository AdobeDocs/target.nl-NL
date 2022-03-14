---
keywords: implementatie;api;profiel;profiel api-instellingen;verificatietoken
description: Leer hoe u verificatie voor batchupdates configureert via Adobe [!DNL Target] API's en genereren een profielverificatietoken.
title: Hoe gebruik ik profiel-API-instellingen om batchupdates in of uit te schakelen?
feature: APIs/SDKs
role: Developer
exl-id: 6346e11b-0853-47f1-9706-69e8635a6f25
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Profiel-API-instellingen

Verificatie voor batchupdates in- of uitschakelen via [!DNL Adobe Target] API&#39;s en genereren een profielverificatietoken.

[!DNL Adobe Target] maakt en onderhoudt een profiel voor elke individuele gebruiker. Dit profiel is opgeslagen op het tabblad [!DNL Target] Edge-cluster en wordt na elk bezoek in realtime bijgewerkt; echter, kunt u een profiel individueel of in bulk bijwerken via API.

Voor extra veiligheid, kunt u vereisen dat de Bulk API vraag van de Update een geldig toegangstoken wordt overgegaan in de kopbal van het verzoek.

**Om authentificatie te vereisen en een toegangstoken te produceren gebruikend het Doel UI:**

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.
1. Onder **[!UICONTROL Profile API]** schuiven **[!UICONTROL Require Authentication]** schakelen naar de in- of uitgeschakeld positie.

   ![](assets/profile_api_settings.png)

1. (Voorwaardelijk) Als u de verificatievereisten hebt ingeschakeld, klikt u op **[!UICONTROL Generate New Profile Authentication Token]**.

   ![](assets/profile_api_settings_2.png)

   Het token verloopt volgens de tijd die in het dialoogvenster [!UICONTROL Expires In] doos.

   U moet een van de volgende gebruikersmachtigingen hebben om een verificatietoken te genereren:

   * Minstens [!UICONTROL Editor] toestemming (of [!UICONTROL Approver])

      Voor meer informatie voor [!DNL Target Standard] klanten, zie [Rollen en machtigingen opgeven](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Gebruikers*. Voor meer informatie voor [!DNL Target Premium] klanten, zie [Bedrijfsmachtigingen configureren](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Beheerdersrol op het niveau van de werkruimte/het productprofiel

      Werkruimten zijn beschikbaar voor [!DNL Target Premium] alleen aan klanten. Zie voor meer informatie [Bedrijfsmachtigingen configureren](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Admin Rights (bevoegdheid Sysadmin) op de [!DNL Adobe Target] productniveau
   >[!NOTE]
   >
   >U kunt ook een profielverificatietoken genereren via de API. Zie voor meer informatie [Profielen](https://developers.adobetarget.com/api/#profiles) op de [Adobe Target Developers-website](https://developers.adobetarget.com/).

1. Kopieer het token en neem het op in de koptekst van het verzoek in de notatie: &quot;Toestemming&quot; : &quot;Teller&quot;

Klikken [!UICONTROL Generate New Profile Authentication Token] om het token zo nodig opnieuw te genereren.

>[!IMPORTANT]
>
>Als u dit token opnieuw instelt, mislukken API-aanroepen met het huidige token. Hiervoor moeten alle scripts of apps die deze token gebruiken, worden bijgewerkt.
