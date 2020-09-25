---
keywords: Target Standard;at.js;implementation
description: De bibliotheek at.js is een nieuwe implementatiebibliotheek voor Adobe Target die is ontworpen voor zowel gangbare webimplementaties als toepassingen die uit één pagina bestaan.
title: Migreren van mbox.js naar at.js
feature: null
topic: Standard
uuid: 10da01d7-d308-44e3-9c6e-ff4f713bd312
translation-type: tm+mt
source-git-commit: 6922b80c88cbd2947c3bfd0cc9d8409ff5dcdcd0
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---


# Migreren van mbox.js naar at.js{#migrate-from-mbox-js-to-at-js}

De bibliotheek at.js is een nieuwe implementatiebibliotheek voor zowel typische Web-implementaties als enig-paginatoepassingen [!DNL Adobe Target] ontworpen.

De laadtijden van pagina&#39;s voor webimplementaties worden [!DNL at.js] onder andere verbeterd en er zijn betere implementatieopties voor toepassingen van één pagina.

[!DNL at.js] vervangt [!DNL mbox.js] voor [!DNL Target] implementaties. De [!DNL at.js] bibliotheek omvat ook de componenten die in [!DNL target.js]inbegrepen waren, zodat is er niet meer een vraag aan [!DNL target.js].

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 met FP-11577 (of later) ondersteunt at.js-implementaties met de integratie van Adobe Target-Cloud Services. Zie [Feature Packs](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) en [Integrating with Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in de documentatie *van* Adobe Experience Manager 6.2 voor meer informatie.

## Voordelen van at.js {#benefits}

In de volgende tabel worden de verschillen tussen de twee bibliotheken uitgelegd:

| Bibliotheekreferentie | Beschrijving |
|--- |--- |
| at.js | bij.js vervangt mbox.js voor [!DNL Target] implementaties.<br>Met at.js worden onder andere de laadtijden voor webimplementaties verbeterd, wordt de beveiliging verbeterd, wordt voorkomen dat documenten.write-waarschuwingen in Google Chrome verschijnen en worden betere implementatieopties geboden voor toepassingen van één pagina.<br>Zie [at.js Implementation](#implement)voor meer informatie. |
| mbox.js | Voorafgaand aan [!DNL Target] 16.3.1 (Maart 2016), [!DNL Target] [!DNL Target] vereiste een vraag aan mbox.js om globale mbox tot stand te brengen die wordt vereist om activiteiten te leveren, kliks te volgen, en de meeste succesmetriek te volgen. Dit bestand bevat de bibliotheken die nodig zijn voor al uw activiteiten. U hoeft geen verschillende activiteitspecifieke versies van het bestand te onderhouden.<br>Als u reeds het verpakken vakjes op uw pagina&#39;s van een oudere stijl van [!DNL Target] implementatie hebt, kunnen deze vakjes nog in de nieuwe interface worden gebruikt. Het bijgewerkte bestand mbox.js is nog steeds vereist, maar deze vakken kunnen worden geselecteerd voor activiteiten en bewerkt met de Visual Experience Composer.<br>[!DNL Target] Standard- en Premium-update en -supplement mbox.js met een verwijzing naar het bestand target.js. Het bestand target.js wordt gehost door Adobe. Met het bestand Target.js kunt u inhoud op elke pagina bewerken met behulp van Visual Experience Composer, zelfs als de pagina geen vooraf gedefinieerde vakken bevat. U moet naar dit bestand verwijzen op elke pagina op uw site.<br>Zie [mbox.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md)voor meer informatie.<br>**Belangrijk**: De bibliotheek mbox.js wordt nog steeds ondersteund, maar er zijn geen functie-updates. Alle klanten moeten naar om.js migreren. Zie [Migreren naar at.js vanuit mbox.js voor meer informatie](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md) |

## Implementeren om.js {#implement}

Vervang de [!DNL at.js][!DNL mbox.js] verwijzing op pagina&#39;s waarop u deze wilt implementeren om deze te gebruiken. U kunt niet zowel [!DNL mbox.js] als [!DNL at.js] op één pagina gebruiken. U kunt echter beide op elke pagina op uw site gebruiken.

De [!DNL at.js] bibliotheek werkt voor bestaande implementaties met de functies `mboxCreate()`, `mboxDefine()`en `mboxUpdate()` en ondersteunt nieuwe functionaliteit die is gericht op implementaties op basis van één pagina-app.

U kunt overal gebruiken [!DNL at.js] u momenteel gebruikt [!DNL mbox.js].

De [!DNL at.js] bibliotheek bevat verschillende verbeteringen ten opzichte van de [!DNL mbox.js] bibliotheek, waaronder:

* Volledig asynchrone communicatie via AJAX

   >[!IMPORTANT]
   >
   >Hoewel het [!DNL at.js] asynchroon met de [!DNL Target] servers communiceert, moet het [!DNL at.js] dossier zelf synchroon in de `<head>` sectie van uw pagina laden. In het ideale geval moet dit een van de eerste scripts zijn die worden geladen. Nadat de box is geladen, wordt de [!DNL at.js] box-aanroep asynchroon `XMLHttpRequest`uitgevoerd en wordt de rendering van de pagina niet geblokkeerd.

* Geen blokkerende vraag meer
* Geen `document.write()` gebruik
* Geen directe uitvoering van JavaScript in [!DNL Target] reacties
* Betere time-out en foutafhandeling

   * Aanpasbare [time-out](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) per oproep
   * Geen herladingen op onderbrekingen

* Functies die specifiek zijn ontworpen voor apps met één pagina/MVC-frameworks

## Trainingsvideo: at.js - Voordelen en het ![Overzicht van de Praktijken van de Implementatie badge](/help/assets/overview.png)

Deze video is een opname van &quot; [Office Hours](../../../../cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7)&quot;, een initiatief van het team van de klantenservice van Adobe.

* Hoe de bibliotheek at.js werkt
* De voordelen van at.js ten opzichte van mbox.js
* Hoe at.js flikkering beheert
* Foutafhandeling in at.js
* Foutopsporingsmethoden
* Bekende problemen en toekomstig stappenplan

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
