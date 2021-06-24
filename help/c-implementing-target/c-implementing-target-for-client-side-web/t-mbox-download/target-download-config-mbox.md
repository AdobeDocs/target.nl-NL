---
keywords: Implementatie;Mbox;mbox.js;download mbox.js;configure mbox.js
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Hoe kan ik de bibliotheek [!DNL Target] mbox.js downloaden?
feature: at.js
role: Developer
exl-id: 92096b1b-a8a5-435b-8e62-24b5d15d392f
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# mbox.js downloaden

De Standaard en Premium van het doel gebruiken een gewijzigde versie van het Adobe Target mbox.js- dossier.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

Als u [!DNL Adobe Target] [!UICONTROL Visual Experience Editor] wilt gebruiken, moet u een extra regel JavaScript opnemen als onderdeel van uw [!DNL mbox.js]-bestand.

1. Klik **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** in [!DNL Target Standard].
1. Klik op **[!UICONTROL Download mbox.js]** en volg de aanwijzingen om het bestand op te slaan.
1. (Voorwaardelijk) Als u [!DNL mbox.js] versie 60 of later gebruikt, kunt u de bibliotheek zodanig configureren dat de pagina-inhoud standaard automatisch wordt verborgen totdat de vakken worden geladen, zodat er minder flikkering optreedt op responsieve sites.

1. Maak de [!DNL mbox.js] verwijzing op de website.

   Vanaf [!DNL mbox.js] versie 57 kan de [!DNL mbox.js] verwijzing overal binnen `<head>` sectie van de pagina worden geplaatst.

   >[!IMPORTANT]
   >
   >Als u een versie van [!DNL mbox.js] voorafgaand aan versie 57 gebruikt, moet de verwijzing het laatste punt in `<head>` sectie van uw pagina&#39;s zijn. Als de verwijzing niet het laatste item is, kunnen er ernstige weergave- of prestatieproblemen optreden.

1. Upload het opgeslagen [!DNL mbox.js]-bestand naar de locatie in uw hostingomgeving die u in de code hebt opgegeven.
