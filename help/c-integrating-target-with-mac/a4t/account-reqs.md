---
keywords: Analytics as reporting source;a4t;A4T;requirements
description: Gebruikersaccountvereisten om een op Adobe Analytics gebaseerde activiteit te maken in Adobe Target (A4T).
title: Vereisten voor gebruikerstoegang
feature: a4t implementation
solution: Target,Analytics
topic: Reports and analytics
uuid: cf359bcd-547e-4f8f-bcf6-e646245bb9ce
translation-type: tm+mt
source-git-commit: a05d2a28b7bea3aa559cd0174930af10c6d94134
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Vereisten voor gebruikerstoegang

Informatie over de vereisten van de gebruikersrekening om een [!DNL Adobe Analytics]gebaseerde activiteit in [!DNL Adobe Target] (A4T) tot stand te brengen.

Voordat u een rapportsuite kunt selecteren wanneer u een [!DNL Analytics] activiteit definieert, hebt u zowel een [!DNL Analytics] gebruikersaccount als een [!DNL Target] gebruikersaccount nodig.

Uw gebruikersaccounts moeten zijn geconfigureerd zoals wordt beschreven in de volgende secties:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Voer de volgende taken uit in de [!DNL Adobe Experience Cloud][Admin Console](https://adminconsole.adobe.com):

### Accounts voor oplossingen koppelen aan uw Adobe ID

Je [!DNL Analytics] en [!DNL Target] gebruikersaccounts moeten aan je Adobe ID zijn gekoppeld.

Zie [Organisaties en accountkoppelingen](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html)voor meer informatie.

### Experience Cloud-groepslidmaatschap configureren

U moet lid zijn van een of meer [!DNL Experience Cloud] groepen die toegang hebben tot [!DNL Analytics] en [!DNL Target].

Zie Gebruikers en producten [van Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html)beheren voor meer informatie.

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Toegang tot de [!DNL Analytics] rapportsuite configureren:

Om A4T op een bepaalde rapportreeks te gebruiken, moet u toegang tot die rapportreeks hebben.

1. Klik **[!UICONTROL Admin Console]** in op een [!DNL Analytics] productprofiel en klik vervolgens op de **[!UICONTROL Permissions]** tab.

   Vervolgens kunt u zien tot welke rapportsuites het profiel toegang heeft.

1. Zorg ervoor dat de rapportsuite waartoe u toegang wilt hebben [!DNL Target] een van de servers is die worden vermeld in het productprofiel waarvan u deel uitmaakt.

   De volgende illustratie is een voorbeeld van een productprofiel dat toegang tot alle rapportsuites heeft:

   ![Tabblad Machtiging Admin Console](/help/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

Er zijn geen aanvullende rechten vereist.
