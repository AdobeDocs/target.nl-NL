---
keywords: Implementation;Mbox;mbox.js;download mbox.js;configure mbox.js
description: Target Standard en Premium gebruiken een gewijzigde versie van het bestand Adobe Target mbox.js.
title: mbox.js downloaden
subtopic: Getting Started
topic: Standard
uuid: b2a46321-cac7-4924-92dd-a80b50e27cee
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# mbox.js downloaden{#download-mbox-js}

Target Standard en Premium gebruiken een gewijzigde versie van het bestand Adobe Target mbox.js.

Als u het [!DNL Adobe Target] bestand wilt gebruiken, moet u een extra regel JavaScript in het [!UICONTROL Visual Experience Editor][!DNL mbox.js] bestand opnemen.

1. Klik **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** in [!DNL Target Standard].
1. Klik op **[!UICONTROL Download mbox.js]** en volg de aanwijzingen om het bestand op te slaan.
1. (Voorwaardelijk) Als u [!DNL mbox.js] versie 60 of later gebruikt, kunt u de bibliotheek zo configureren dat de pagina-inhoud standaard automatisch wordt verborgen totdat de vakken worden geladen, zodat er minder flikkering optreedt op responsieve sites.

   Zie &quot;Paginalaadflikkering onderdrukken&quot; in [mbox.js Advanced Settings](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/advanced-mboxjs-settings.md#reference_A9C8DAC6DF7743EDBCF1D71F8F20843C)voor meer informatie.

1. Maak de [!DNL mbox.js] verwijzing op de website.

   Vanaf [!DNL mbox.js] versie 57 kan de [!DNL mbox.js] verwijzing overal in de `<head>` sectie van de pagina worden geplaatst.

   >[!IMPORTANT]
   >
   >Als u een versie van [!DNL mbox.js] ouder dan versie 57 gebruikt, moet de verwijzing het laatste punt in de `<head>` sectie van uw pagina&#39;s zijn. Als de verwijzing niet het laatste item is, kunnen er ernstige weergave- of prestatieproblemen optreden. Zie [Wat mbox.js voor meer informatie doet](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-technical.md) .

1. Upload het opgeslagen [!DNL mbox.js] bestand naar de locatie in uw hostingomgeving die u in de code hebt opgegeven.
