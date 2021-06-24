---
keywords: Doelstandaard;at.js;implementatie
description: Leer hoe u kunt migreren naar at.js, de nieuwe implementatiebibliotheek voor Adobe [!DNL Target] die is ontworpen voor zowel standaard webimplementaties als toepassingen voor één pagina (SPA).
title: Hoe kan ik migreren van mbox.js naar at.js?
feature: at.js
role: Developer
exl-id: 1d95faeb-7caa-44d6-b637-a06db393e50e
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Migreren van mbox.js naar at.js

De bibliotheek at.js is een nieuwe implementatiebibliotheek voor [!DNL Adobe Target] die voor zowel typische Webimplementaties als enig-paginatoepassingen wordt ontworpen.

[!DNL at.js] verbetert onder andere de laadtijden voor webimplementaties en biedt betere implementatieopties voor toepassingen van één pagina.

[!DNL at.js] vervangt  [!DNL mbox.js] voor  [!DNL Target] implementaties. De [!DNL at.js] bibliotheek omvat ook de componenten die in [!DNL target.js] inbegrepen waren, zodat is er niet meer een vraag aan [!DNL target.js].

>[!NOTE]
>
>Adobe Experience Manager (AEM) 6.2 met FP-11577 (of later) ondersteunt at.js-implementaties met de integratie van Adobe Target-Cloud Services. Zie [Feature Packs](https://docs.adobe.com/docs/en/aem/6-2/release-notes/feature-packs.html) en [Integrating with Adobe Target](https://docs.adobe.com/docs/en/aem/6-2/administer/integration/marketing-cloud/target.html) in de *Adobe Experience Manager 6.2 documentation* voor meer informatie.

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
