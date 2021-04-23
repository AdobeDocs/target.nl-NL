---
keywords: Analyse als bron van rapportage;a4t;A4T;vereisten
description: Leer hoe u de vereisten voor gebruikersaccounts configureert die nodig zijn om een op Adobe Analytics gebaseerde activiteit te maken in Adobe [!DNL Target] using Analytics for [!DNL Target] (A4T).
title: Welke Vereisten van de Toestemming van de Gebruiker voor A4T worden vereist?
feature: Analyses voor doel (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Vereisten voor gebruikerstoegang

Informatie over de vereisten van de gebruikersrekening om een [!DNL Adobe Analytics]-gebaseerde activiteit in [!DNL Adobe Target] (A4T) tot stand te brengen.

Voordat een rapportsuite kan worden geselecteerd bij het definiëren van een [!DNL Analytics]-activiteit, hebt u zowel een [!DNL Analytics]-gebruikersaccount als een [!DNL Target]-gebruikersaccount nodig.

Uw gebruikersaccounts moeten zijn geconfigureerd zoals wordt beschreven in de volgende secties:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Voltooi de volgende taken in [!DNL Adobe Experience Cloud] [Admin Console](https://adminconsole.adobe.com):

### Accounts voor oplossingen koppelen aan uw Adobe ID

Uw [!DNL Analytics]- en [!DNL Target]-gebruikersaccounts moeten aan uw Adobe ID zijn gekoppeld.

Zie [Organisaties en account linking](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html) voor meer informatie.

### Experience Cloud-groepslidmaatschap configureren

U moet lid van één of meerdere [!DNL Experience Cloud] groepen zijn die toegang tot [!DNL Analytics] en [!DNL Target] hebben.

Zie [Gebruikers en producten van Experience Cloud beheren](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html) voor meer informatie.

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Om A4T op een bepaalde rapportreeks te gebruiken, moet u toegang tot die rapportreeks hebben en toegang tot [!DNL Web Services Access] groep verlenen.

1. Klik in **[!UICONTROL Admin Console]** op een [!DNL Analytics]-productprofiel en klik vervolgens op het tabblad **[!UICONTROL Permissions]**.

   Vervolgens kunt u zien tot welke rapportsuites het profiel toegang heeft.

1. Zorg ervoor dat de rapportenreeks u toegang tot in [!DNL Target] wilt hebben één van degenen die in het productprofiel wordt vermeld u een deel van bent.

   De volgende illustratie is een voorbeeld van een productprofiel dat toegang tot alle rapportsuites heeft:

   ![Tabblad Machtiging Admin Console](/help/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Vorm toegang tot [!UICONTROL Web Services Access] groep.

   Toegang tot de [!UICONTROL Web Services Access]-groep in [!DNL Analytics] is vereist om [!DNL Analytics] als rapportagebron voor [!DNL Target] te kunnen gebruiken.


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Er zijn geen aanvullende rechten vereist.
