---
keywords: Analyse als bron van rapportage;a4t;A4T;vereisten
description: Leer hoe te om de vereisten van de gebruikersrekening noodzakelijk te vormen om een op Adobe Analytics-Gebaseerde activiteit in Adobe  [!DNL Target]  tot stand te brengen gebruikend Analytics voor  [!DNL Target]  (A4T).
title: Welke Vereisten van de Toestemming van de Gebruiker voor A4T worden vereist?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Vereisten voor gebruikerstoegang

Informatie over de vereisten voor gebruikersaccounts om een op [!DNL Adobe Analytics] gebaseerde activiteit te maken in [!DNL Adobe Target] (A4T).

Voordat u een rapportsuite kunt selecteren wanneer u een [!DNL Analytics] -activiteit definieert, hebt u zowel een [!DNL Analytics] gebruikersaccount als een [!DNL Target] -gebruikersaccount nodig.

Uw gebruikersaccounts moeten zijn geconfigureerd zoals wordt beschreven in de volgende secties:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Voltooi de volgende taken in [!DNL Adobe Experience Cloud] [&#x200B; Admin Console &#x200B;](https://adminconsole.adobe.com):

### Accounts voor oplossingen koppelen aan uw Adobe ID

Uw [!DNL Analytics] - en [!DNL Target] -gebruikersaccounts moeten aan uw Adobe ID zijn gekoppeld.

Voor meer informatie, zie [&#x200B; Organisaties en rekening het verbinden &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl-NL).

### Experience Cloud-groepslidmaatschap configureren

U moet lid zijn van een of meer [!DNL Experience Cloud] -groepen die toegang hebben tot [!DNL Analytics] en [!DNL Target] .

Voor meer informatie, zie [&#x200B; de gebruikers en de producten van Experience Cloud beheren &#x200B;](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=nl-NL).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Als u A4T voor een bepaalde rapportsuite wilt gebruiken, moet u toegang hebben tot die rapportsuite en toegang verlenen tot de groep [!DNL Web Services Access] .

1. Klik in **[!UICONTROL Admin Console]** op een [!DNL Analytics] productprofiel en klik vervolgens op de tab **[!UICONTROL Permissions]** .

   Vervolgens kunt u zien tot welke rapportsuites het profiel toegang heeft.

1. Zorg ervoor dat de rapportsuite waartoe u toegang wilt hebben in [!DNL Target] een van de sets is die worden vermeld in het productprofiel waarvan u een deel bent.

   De volgende illustratie is een voorbeeld van een productprofiel dat toegang tot alle rapportsuites heeft:

   ![&#x200B; het lusje van de Toestemming van Admin Console &#x200B;](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Configureer toegang tot de groep [!UICONTROL Web Services Access] .

   U hebt toegang tot de [!UICONTROL Web Services Access] group in [!DNL Analytics] nodig om [!DNL Analytics] als rapportagebron voor [!DNL Target] te kunnen gebruiken.


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Er zijn geen aanvullende rechten vereist.
