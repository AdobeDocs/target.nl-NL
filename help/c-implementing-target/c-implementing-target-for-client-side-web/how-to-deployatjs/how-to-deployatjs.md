---
keywords: implement;at.js;javascript library
description: Informatie over hoe u de Adobe Target JavaScript-bibliotheek in.js kunt implementeren met behulp van Adobe Launch, zonder tagbeheer of met behulp van Adobe Dynamic Tag Management (DTM).
title: Hoe te opstellen bij.js
feature: Implement Server-side
translation-type: tm+mt
source-git-commit: 88f6e4c6ad168e4f9ce69aa6618d8641b466e28a
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---


# Hoe te opstellen bij.js

Informatie over hoe u de Adobe Target JavaScript-bibliotheek in.js kunt implementeren met behulp van Adobe Launch, zonder tagbeheer of met behulp van Adobe Dynamic Tag Management (DTM).

U kunt at.js opstellen gebruikend de volgende methodes:

* **[Doel implementeren met Adobe starten](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md)**: Starten is het platform voor tagbeheer van de volgende generatie van Adobe en is de voorkeursmethode voor het implementeren van Adobe Target. De lancering geeft klanten een eenvoudige manier om alle analytische, marketing, en reclame markeringen noodzakelijk om relevante klantenervaringen op te stellen en te beheren.
* **[Doel implementeren zonder tagbeheer](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)**: U kunt Doel implementeren zonder een tagbeheer te gebruiken (Adobe Launch of Dynamisch tagbeheer).
* **[Doel implementeren met dynamisch tagbeheer](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-using-dynamic-tag-management.md)**: U kunt Doel implementeren met DTM (Adobe Dynamic Tag Management), beheer van Adobe voor oude tags. De Lancering van de Adobe is de aangewezen, bijgewerkte methode om Doel en de at.js bibliotheek uit te voeren. Gebruik Starten voor nieuwe doelimplementaties.
* **Doel implementeren met tagbeheer** van derden:  [Adobe ](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) Launchis de aangewezen methode om Doel uit te voeren; u kunt Target echter ook implementeren met behulp van een externe tagmanager, zoals Tealium, Ensighten, Google Tag, enzovoort. Voor een lijst van voordelen om Lancering te gebruiken, zie [Voordelen om at.js uit te voeren gebruikend de uitbreiding van de Lancering van het Doel](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md#section_48B3F938B6F8491DAF798E0DB54EF304).

   Als u echter weet hoe u Doel kunt implementeren zonder tagbeheer, kunt u eenvoudig implementeren met een externe tagmanager in plaats van hard-coding bij.js in de sitecode.

   Hier zijn twee relevante onderwerpen die u zullen helpen Doel met een derde markeringsmanager uitvoeren:

   * [Voordat u implementeert](/help/c-implementing-target/c-considerations-before-you-implement-target/considerations-before-you-implement-target.md)
   * [Doel implementeren zonder tagbeheer](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md)

   Raadpleeg de documentatie bij de tagmanager van derden voor meer informatie.

Als u Doel wilt implementeren bij het gebruik van apps voor één pagina (SPA), raadpleegt u [Toepassing voor één pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/target-atjs-single-page-application.md).