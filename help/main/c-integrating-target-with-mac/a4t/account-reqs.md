---
keywords: Analyse als bron van rapportage;a4t;A4T;vereisten
description: Leer hoe u de vereisten voor gebruikersaccounts configureert die nodig zijn om een op Adobe Analytics gebaseerde activiteit in Adobe te maken [!DNL Target] Analyses gebruiken voor [!DNL Target] (A4T).
title: Welke Vereisten van de Toestemming van de Gebruiker voor A4T worden vereist?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Vereisten voor gebruikerstoegang

Informatie over de vereisten voor gebruikersaccounts om een [!DNL Adobe Analytics]-gebaseerde activiteit in [!DNL Adobe Target] (A4T).

Voordat een rapportsuite kan worden geselecteerd tijdens het definiëren van een [!DNL Analytics] activiteit, hebt u zowel [!DNL Analytics] gebruikersaccount en een [!DNL Target] gebruikersaccount.

Uw gebruikersaccounts moeten zijn geconfigureerd zoals wordt beschreven in de volgende secties:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Voltooi de volgende taken in de [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com):

### Accounts voor oplossingen koppelen aan uw Adobe ID

Uw [!DNL Analytics] en [!DNL Target] gebruikersaccounts moeten aan je Adobe ID zijn gekoppeld.

Zie voor meer informatie [Organisaties en accountkoppelingen](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).

### Experience Cloud-groepslidmaatschap configureren

U moet lid zijn van een of meer [!DNL Experience Cloud] groepen die toegang hebben tot [!DNL Analytics] en [!DNL Target].

Zie voor meer informatie [Gebruikers en producten van Experience Cloud beheren](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Om A4T op een bepaalde rapportreeks te gebruiken, moet u toegang tot die rapportreeks hebben en toegang verlenen tot [!DNL Web Services Access] groep.

1. In **[!UICONTROL Admin Console]**, klikt u op [!DNL Analytics] productprofiel en klik vervolgens op **[!UICONTROL Permissions]** tab.

   Vervolgens kunt u zien tot welke rapportsuites het profiel toegang heeft.

1. Zorg ervoor dat de rapportsuite waartoe u toegang wilt hebben in [!DNL Target] is een van de profielen die worden vermeld in het productprofiel waarvan u deel uitmaakt.

   De volgende illustratie is een voorbeeld van een productprofiel dat toegang tot alle rapportsuites heeft:

   ![Tabblad Machtiging Admin Console](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Toegang tot de [!UICONTROL Web Services Access] groep.

   Toegang tot de [!UICONTROL Web Services Access] groep in [!DNL Analytics] moet kunnen worden gebruikt [!DNL Analytics] als bron van rapportage voor [!DNL Target].


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Er zijn geen aanvullende rechten vereist.
