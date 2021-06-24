---
keywords: beperkingen van composers voor visuele beleving;browserondersteuning;integratie;plug-ins;asynchrone overwegingen
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Wat zijn de verschillen tussen at.js en mbox.js?
feature: at.js
role: Developer
exl-id: 2fd0db66-0b47-41c0-86b6-44e711d70027
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# om.js Beperkingen

Er zijn enkele verschillen tussen at.js en mbox.js. Deze sectie maakt een lijst van enkele verschillen en beperkingen, om u te helpen met at.js succesvol zijn.

## Bekende beperkingen van composers voor visuele ervaring {#section_4B63C97169DE4C93B22944E880FD3DF1}

* De opties Element invoegen en Opnieuw rangschikken in Composer visuele ervaring moeten worden vermeden in apps van één pagina.

   Omdat het DOM niet wordt gewist bij gebeurtenissen voor het laden van pagina&#39;s in apps van één pagina, zoals bij traditionele websites, kunnen de bewerkingen Element invoegen en Opnieuw rangschikken meerdere malen worden toegepast, afhankelijk van de manier waarop de bezoeker door de SPA navigeert.

## Integraties en plug-ins {#section_D92E31170176406AAC7B5005F03D3425}

Sommige functies in [!DNL mbox.js] zijn niet beschikbaar in [!DNL at.js]. Interne [mbox.js-objecten en -methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (zoals `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories` en andere) worden niet meer ondersteund door [!DNL at.js] (voorbeeld: `mboxFactoryDefault`). Dit is door ontwerp, bedoeld om u te ontmoedigen om [!DNL at.js] te &quot;hacken&quot;om niet gestaafde functionaliteit te ontwikkelen die op lange termijn een implementatie kan verlammen en het onmogelijk maken om te bevorderen. De enige methoden die beschikbaar zijn, worden beschreven in de API-pagina&#39;s van deze documentatie. Daarom:

* Verouderde, op pagina&#39;s gebaseerde [integraties](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) met andere Adobe oplossingen werken mogelijk niet en zouden aan nieuwere, server-zijintegratie moeten worden bevorderd.

   Zorg ervoor dat u eventuele plug-ins opneemt als onderdeel van de test.

## Asynchrone overwegingen {#section_B586360A3DD34E2995AE25A18E3FB953}

Omdat alle vakken nu asynchroon zijn, blokkeren ze het weergeven van pagina&#39;s of retourneren ze niet in de volgorde waarin ze zijn gestart.

* Als u een globale box in [Form-Based Experience Composer](/help/c-experiences/experiences.md#section_3643394BD424463C8768F2907DEBCC22) gebruikt, moet u er rekening mee houden dat HTML-aanbiedingen alleen `<script>`-, `<style>`- en `<link>`-tags mogen bevatten.

   Tijdens levering, [!DNL at.js] filters uit alle andere markeringen van HTML wanneer het toepassen van globale mbox aanbiedingen. Algemene mbox-aanbiedingen worden toegepast op HTML HEAD, dat geen DIV, SPAN enzovoort toestaat. Kan bijvoorbeeld `<div>test</div>` niet toepassen, omdat de tag `<div>` alleen binnen de HTML-BODY kan worden gebruikt.

* Verouderde integratie op pagina&#39;s [!DNL Target] naar [!DNL Analytics] werkt niet.

   Deze integratie vereist dat [!DNL Target] vraag vóór [!DNL Analytics] vraag wordt gemaakt.

* Houd rekening met de JavaScript-afhankelijkheden tussen uw aanbieding en de pagina.

   U mag niet aannemen dat de JavaScript in uw aanbieding wordt uitgevoerd vóór de gecodeerde JavaScript onder de box.

* Houd rekening met JavaScript-afhankelijkheden tussen meerdere aanbiedingen op de pagina.

   Je kunt er niet langer van uitgaan dat de aanbieding van de eerste box wordt uitgevoerd vóór de aanbieding van de tweede box.

* Aanbiedingen voor DOM Manipulation en Redirect moeten worden geleverd via de automatisch gemaakte globale box in [!DNL at.js] en worden geleverd in `<head>`.

   Een functie `mboxCreate()` boven aan `<body>` zal waarschijnlijk in flikkering van standaardinhoud resulteren.
