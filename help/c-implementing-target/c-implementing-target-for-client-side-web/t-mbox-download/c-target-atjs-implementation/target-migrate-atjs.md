---
keywords: Doel;at.js;migrate aan at.js;gereedheid;audit at.js;Integreren at.js
description: Leer hoe u kunt migreren naar at.js, de nieuwe implementatiebibliotheek voor Adobe Target die is ontworpen voor zowel standaard webimplementaties als toepassingen voor één pagina (SPA).
title: Migreren naar at.js vanuit mbox.js
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---


# Migreren naar at.js vanuit mbox.js

Het migreren van mbox.js aan at.js in [!DNL Adobe Target] is een ongecompliceerd proces.

Gebruik de volgende stappen om van [!DNL mbox.js] naar [!DNL at.js] te migreren en uw migratie te controleren:

1. Bepaal de [browserondersteuning](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100) vereisten van uw organisatie.
1. Controleer de huidige [!DNL mbox.js]-implementatie van uw website op mogelijkheden die niet worden ondersteund door [!DNL at.js].

   Wanneer het controleren van uw implementatie, zoek het volgende:

   **Welke typen vakken gebruikt u momenteel?**

   | Type | Details |
   |--- |--- |
   | Automatisch gemaakte globale mbox | Het automatisch gemaakte globale mbox wordt gemaakt wanneer de enige regel doelcode op uw site het bestand mbox.js is. Dat dossier produceert automatisch een mbox vraag. |
   | Globale, lege mboxCreate | U wordt aangeraden over te schakelen naar het automatisch gemaakte globale mbox. |
   | MboxCreate | De migratie moet eenvoudig zijn, zolang uw `mboxCreate()` wordt voorafgegaan door `<div class="mboxDefault"></div>`. |
   | mboxUpdate | Migratie moet eenvoudig zijn wanneer `mboxUpdate()` wordt gebruikt in combinatie met `mboxDefine()` of `mboxCreate()`. `mboxUpdate()` werkt automatisch gemaakte globale mbox of een mbox niet bij oorspronkelijk gecreeerd door  `getOffer()`. In deze omstandigheden moet een combinatie van `getOffer()` en `applyOffer()` worden gebruikt om `mboxUpdate()` te vervangen bij het migreren naar at.js. |
   | Aangepaste klikvolgvakjes, met inbegrip van mboxTrack | Wij adviseren dat u uw code aan gebruik `trackEvent()` bijwerkt. |

   >[!NOTE]
   >
   >Zie [at.js-functies](/help/c-implementing-target/c-implementing-target-for-client-side-web/cmp-atjs-functions.md) voor meer informatie over de verschillende functies die in de voorgaande tabel worden genoemd.

   **Hebt u aanpassingen aan uw  [!DNL mbox.js] bestand?**

   * mboxParameters()
   * mboxSupported()
   * mboxCookieDomain()
   * Extra JavaScript
   * Overige locaties

   De meeste [mbox.js-objecten en -methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (zoals `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` en andere) worden niet ondersteund. Alternatieve benaderingen kunnen mogelijk zijn om te bereiken wat u probeert te doen.

   **Hebt u  [!DNL mbox.js] op een van uw webpagina&#39;s?**

   U kunt niet zowel [!DNL at.js] als [!DNL mbox.js] op dezelfde webpagina gebruiken. U kunt de twee JavaScript-bibliotheken echter op twee verschillende pagina&#39;s van dezelfde website gebruiken.

   Het cookie van de box is de belangrijkste manier waarop Adobe de bezoeker van pagina tot pagina verbindt. Als onderdeel van uw kwaliteitscontrole moet u bevestigen dat het cookie wordt behouden en correct wordt gelezen terwijl de bezoeker heen en weer gaat tussen pagina&#39;s met [!DNL at.js] en pagina&#39;s met [!DNL mbox.js]. Zorg ervoor dat dezelfde `mboxPC`- en `mboxSession`-waarden worden doorgegeven in de mbox-aanroepen, ongeacht welk gedeelte van de site ( [!DNL at.js] of [!DNL mbox.js]) de bezoeker eerst landt en welke sectie de cookie oorspronkelijk instelt. Als u cookies van derden gebruikt in uw implementatie, moet u ervoor zorgen dat deze waarden gelijk blijven wanneer u door de site bladert.

   **Integreren  [!DNL Target] met andere Adobe-oplossingen?**

   * Analyse (A4T)
   * Analytics (legacy integration)
   * AAM (backend)
   * AAM (verouderde voorzijde)
   * AEM
   * Data Workbench

   Sommige verouderde integraties worden niet ondersteund door [!DNL at.js]. Zie de pagina [Integrations](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) voor meer informatie.

   **Integreert u  [!DNL Target] met andere hulpprogramma&#39;s van derden?**

   * Andere analysefuncties
   * Overige DMP&#39;s
   * Demandbase
   * Klikverhaal
   * Overige

   Deze integraties moeten mogelijk worden aangepast om met [!DNL at.js] te kunnen werken. Zie de pagina [Integrations](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) voor meer informatie.

   **Gebruikt u een tagbeheer?**

   * Dynamisch tagbeheer
   * Vergroten
   * Tealium
   * Signal/BrightTag

   Zie [at.js Integrations](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) voor meer informatie.

   >[!NOTE]
   >
   >Als u momenteel geen markeringsmanager gebruikt om [!DNL Target] op te stellen, zou nu een goede tijd kunnen zijn om het te overwegen. Dynamic Tag Management [Dynamic Tag Management is gratis voor [!DNL Target]-klanten en is de aanbevolen methode om [!DNL Target] te implementeren. ](https://dtm.adobe.com) Voor meer informatie, zie [Beste praktijken voor het Uitvoeren van Adobe Target gebruikend Dynamisch Beheer van de Markering](https://experienceleague.adobe.com/docs/dtm/implementing/overview.html).

1. Controleer of alle huidige activiteiten en integraties naar verwachting werken.

   Hier volgen enkele voorbeelden van wat u kunt doen tijdens het testen om te bevestigen dat [!DNL at.js] naar behoren werkt:

   * Zorg ervoor dat al uw huidige activiteiten werken met de nieuwe JavaScript-bibliotheek.
   * Bevestig dat alle [integraties](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) en [plugins](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) zoals verwacht werken.
   * Zorg ervoor dat u comfortabel [foutopsporing](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-debugging-atjs/target-debugging-atjs.md#concept_CAE591DA8C404C22917584ECD4F7494F) bent met de benaderingen die beschikbaar zijn bij [!DNL at.js].

**Mogelijke problemen bij het migreren naar at.** jsSommige klanten hebben na het uitvoeren van de migratie naar at.js de volgende problemen gemeld:

* Sommige VEC-activiteiten die op een pagina met [!DNL mbox.js] zijn gemaakt, moeten mogelijk worden bijgewerkt om met [!DNL at.js] te kunnen werken.

   Deze kwestie komt het vaakst op websites voor die vele identiteitskaart of klassenattributen in de elementen van HTML niet gebruiken. U kunt bevestigen of u dit probleem ervaart door de pagina te laden en te bepalen of de ervaring zoals verwacht wordt geleverd door de pagina met `?mboxDebug=true` te laden en de consoleverklaringen te herzien.

   ![](assets/mboxdebug.png)
In deze gevallen kunnen elementkiezers beginnen met iets als

   ```
   HTML > BODY > DIV:nth-of-type(2)
   ```

   en zijn gemaakt met de verwachting dat [!DNL mbox.js] een extra `<div>`-element aan de bovenkant van de pagina heeft toegevoegd. Omdat [!DNL at.js] geen `<div>` element aan de bovenkant van de pagina toevoegt, zou deze selecteur niet meer met [!DNL at.js] werken.

   Dit probleem kan worden opgelost door de activiteit in de VEC op de URL opnieuw te maken met behulp van [!DNL at.js] of door de kiezer handmatig bij te werken met de optie **[!UICONTROL </> Code]** > **[!UICONTROL Modifications]** in de VEC.

   U verhelpt dit probleem door 1 te verwijderen uit het nde-van-type getal in het eerste DIV-element na BODY. In het bovenstaande voorbeeld zou de bewerkte code als volgt zijn:

   ```
   HTML > BODY > DIV:nth-of-type(1)
   ```

   Voor meer informatie over hoe te om de coderedacteur te gebruiken om dit te doen, zie [de Redacteur van de Code](/help/c-experiences/c-visual-experience-composer/c-vec-code-editor/vec-code-editor.md#concept_B3A6E9EE3A60406DB640E205EA1745B5).

* Omdat alle vakken nu asynchroon zijn, blokkeren ze het weergeven van pagina&#39;s of retourneren ze niet in de volgorde waarin ze zijn gestart. Voor meer informatie, zie &quot;Asynchrone Overwegingen&quot;in [at.js Beperkingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md#concept_FA99E4D6EC274552BF45E01AFB76CCAE).
