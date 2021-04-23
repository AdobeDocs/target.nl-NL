---
keywords: Doelstandaard;at.js;implementatie
description: Leer hoe u kunt migreren naar at.js, de nieuwe implementatiebibliotheek voor Adobe [!DNL Target] die is ontworpen voor zowel standaard webimplementaties als toepassingen voor één pagina (SPA).
title: Hoe kan ik migreren van mbox.js naar at.js?
feature: at.js
role: Developer
exl-id: 1d95faeb-7caa-44d6-b637-a06db393e50e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Migreren van mbox.js naar at.js

De bibliotheek at.js is een nieuwe implementatiebibliotheek voor [!DNL Adobe Target] die voor zowel typische Webimplementaties als enig-paginatoepassingen wordt ontworpen.

[!DNL at.js] verbetert onder andere de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina.

[!DNL at.js] vervangt  [!DNL mbox.js] voor  [!DNL Target] implementaties. De [!DNL at.js] bibliotheek omvat ook de componenten die in [!DNL target.js] inbegrepen waren, zodat is er niet meer een vraag aan [!DNL target.js].

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 met FP-11577 (of later) ondersteunt at.js-implementaties met de integratie van Adobe Target-Cloud Services. Zie [Feature Packs](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) en [Integrating with Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in de *Adobe Experience Manager 6.2 documentation* voor meer informatie.

## Voordelen van at.js {#benefits}

In de volgende tabel worden de verschillen tussen de twee bibliotheken uitgelegd:

| Bibliotheekreferentie | Beschrijving |
|--- |--- |
| at.js | at.js vervangt mbox.js voor [!DNL Target] implementaties.<br>Met at.js worden onder andere de laadtijden voor webimplementaties verbeterd, wordt de beveiliging verbeterd, wordt voorkomen dat documenten.write-waarschuwingen in Google Chrome verschijnen en worden betere implementatieopties geboden voor toepassingen van één pagina.<br>Zie  [at.js Implementation](#implement) voor meer informatie. |
| mbox.js | Vóór [!DNL Target] 16.3.1 (Maart 2016), vereiste [!DNL Target] een vraag aan mbox.js om globale mbox tot stand te brengen die voor [!DNL Target] wordt vereist om activiteiten te leveren, kliks te volgen, en de meeste succesmetriek te volgen. Dit bestand bevat de bibliotheken die nodig zijn voor al uw activiteiten. U hoeft geen verschillende activiteitspecifieke versies van het bestand te onderhouden.<br>Als u reeds het verpakken vakjes op uw pagina&#39;s van een oudere stijl van  [!DNL Target] implementatie hebt, kunnen deze vakjes nog in de nieuwe interface worden gebruikt. Het bijgewerkte bestand mbox.js is nog steeds vereist, maar deze vakken kunnen worden geselecteerd voor activiteiten en bewerkt met de Visual Experience Composer.<br>[!DNL Target] Standard- en Premium-update en -supplement mbox.js met een verwijzing naar het bestand target.js. Het bestand target.js wordt gehost door Adobe. Met het bestand Target.js kunt u inhoud op elke pagina bewerken met behulp van Visual Experience Composer, zelfs als de pagina geen vooraf gedefinieerde vakken bevat. U moet naar dit bestand verwijzen op elke pagina op uw site.<br>Zie  [mbox.js Implementation](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md) voor meer informatie.<br>**Belangrijk**: De bibliotheek mbox.js wordt nog steeds ondersteund, maar er zijn geen functie-updates. Alle klanten moeten naar om.js migreren. Zie [Migreren naar at.js vanuit mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md) voor meer informatie |

## Implementeren om.js {#implement}

Als u [!DNL at.js] wilt gebruiken, vervangt u de [!DNL mbox.js]-verwijzing op pagina&#39;s waar u deze wilt implementeren. U kunt niet zowel [!DNL mbox.js] als [!DNL at.js] op één pagina gebruiken. U kunt echter beide op elke pagina op uw site gebruiken.

De bibliotheek [!DNL at.js] werkt voor bestaande implementaties met behulp van de functies `mboxCreate()`, `mboxDefine()` en `mboxUpdate()` en ondersteunt nieuwe functionaliteit die is gericht op implementaties op basis van één pagina.

U kunt [!DNL at.js] overal gebruiken u momenteel [!DNL mbox.js] gebruikt.

De bibliotheek [!DNL at.js] biedt verschillende verbeteringen in vergelijking met de bibliotheek [!DNL mbox.js], waaronder:

* Volledig asynchrone communicatie via AJAX

   >[!IMPORTANT]
   >
   >Hoewel [!DNL at.js] asynchroon communiceert met de [!DNL Target] servers, moet het [!DNL at.js] dossier zelf synchroon in `<head>` sectie van uw pagina laden. In het ideale geval moet dit een van de eerste scripts zijn die worden geladen. Nadat [!DNL at.js] is geladen, wordt de box-aanroep asynchroon uitgevoerd via `XMLHttpRequest` en wordt de rendering van pagina&#39;s niet geblokkeerd.

* Geen blokkerende vraag meer
* Geen `document.write()` gebruikt
* Geen directe uitvoering van JavaScript in reacties [!DNL Target]
* Betere time-out en foutafhandeling

   * Aanpasbare [timeout](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) per oproep
   * Geen herladingen op onderbrekingen

* Functies die specifiek zijn ontworpen voor apps met één pagina/MVC-frameworks

## Trainingsvideo: at.js - Voordelen en Implementatie Beste praktijken ![Bekeken overzicht](/help/assets/overview.png)

Deze video is een opname van &quot; [Office Hours](/help/cmp-resources-and-contact-information.md)&quot;, een initiatief onder leiding van het team van de klantenservice van Adobe.

* Hoe de bibliotheek at.js werkt
* De voordelen van at.js ten opzichte van mbox.js
* Hoe at.js flikkering beheert
* Foutafhandeling in at.js
* Foutopsporingsmethoden
* Bekende problemen en toekomstig stappenplan

>[!VIDEO](https://video.tv.adobe.com/v/22223/)
