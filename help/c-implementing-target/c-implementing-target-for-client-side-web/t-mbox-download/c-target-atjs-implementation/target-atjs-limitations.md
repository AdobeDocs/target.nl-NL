---
keywords: visual experience composer limitations;browser support;integrations;plugins;asynchronous considerations
description: Er zijn enkele verschillen tussen at.js en mbox.js. Deze sectie maakt een lijst van enkele verschillen en beperkingen, om u te helpen met at.js succesvol zijn.
title: om.js Beperkingen
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---


# om.js Beperkingen{#at-js-limitations}

Er zijn enkele verschillen tussen at.js en mbox.js. Deze sectie maakt een lijst van enkele verschillen en beperkingen, om u te helpen met at.js succesvol zijn.

## Bekende beperkingen van composers voor visuele ervaring {#section_4B63C97169DE4C93B22944E880FD3DF1}

* De opties Element invoegen en Opnieuw rangschikken in Composer visuele ervaring moeten worden vermeden in apps van één pagina.

   Omdat het DOM niet wordt gewist bij gebeurtenissen voor het laden van pagina&#39;s in apps van één pagina, zoals bij traditionele websites, kunnen de bewerkingen Element invoegen en Opnieuw rangschikken meerdere malen worden toegepast, afhankelijk van de manier waarop de bezoeker door de SPA navigeert.

## Integraties en plug-ins {#section_D92E31170176406AAC7B5005F03D3425}

Sommige functies binnen [!DNL mbox.js] zijn niet beschikbaar in [!DNL at.js]. Interne [mbox.js-objecten en -methoden](/help/c-target/c-visitor-profile/variables-profiles-parameters-methods.md#section_8C78059D15D9452F95636A5640188537) (zoals `mbox`, `mboxCurrent`, `mboxFactoryDefault`, `mboxFactories`enzovoort) worden niet meer ondersteund door [!DNL at.js] (voorbeeld: `mboxFactoryDefault`). Dit is door ontwerp, bedoeld om u te ontmoedigen van &quot;hacking&quot; [!DNL at.js] om niet gestaafde functionaliteit te ontwikkelen die op lange termijn een implementatie kan verlammen en het onmogelijk maken om te bevorderen. De enige methoden die beschikbaar zijn, worden beschreven in de API-pagina&#39;s van deze documentatie. Daarom:

* Verouderde, op pagina&#39;s gebaseerde [integratie](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md#concept_C100BC4F073C4B57A608B309D0157B39) met andere oplossingen van de Adobe werkt en zou aan nieuwere, server-zijintegratie moeten worden bevorderd.
* [Aangepaste plug-ins die voor mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) zijn ontwikkeld, werken mogelijk alleen als deze zijn bijgewerkt voor [!DNL at.js].

   Zorg ervoor dat u eventuele [plug-ins](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-plugins.md#concept_F5D4C0A4DACF41409CC42FDD93B13FAF) opneemt als onderdeel van de test.

## Asynchrone overwegingen {#section_B586360A3DD34E2995AE25A18E3FB953}

Omdat alle vakken nu asynchroon zijn, blokkeren ze het weergeven van pagina&#39;s of retourneren ze niet in de volgorde waarin ze zijn gestart.

* Als u een globale mbox in de [Formulier-Gebaseerde Composer](/help/c-experiences/experiences.md#section_3643394BD424463C8768F2907DEBCC22)van de Ervaring gebruikt, me ervan bewust ben dat de aanbiedingen van HTML slechts `<script>`, `<style>`, en `<link>` markeringen zouden moeten bevatten.

   Bij levering worden alle andere HTML-tags [!DNL at.js] uitgefilterd wanneer algemene mbox-aanbiedingen worden toegepast. Algemene mbox-aanbiedingen worden toegepast op HTML HEAD, dat geen DIV, SPAN enzovoort toestaat. Kan bijvoorbeeld `<div>test</div>` niet toepassen omdat de `<div>` tag alleen binnen HTML BODY kan worden gebruikt.

* Verouderde op pagina&#39;s gebaseerde [!DNL Target] [!DNL Analytics] integratie werkt niet.

   Deze integratie vereist dat de [!DNL Target] vraag vóór de [!DNL Analytics] vraag wordt gemaakt.

* Houd rekening met de JavaScript-afhankelijkheden tussen uw aanbieding en de pagina.

   U mag niet aannemen dat de JavaScript in uw aanbieding wordt uitgevoerd vóór de gecodeerde JavaScript onder de box.

* Houd rekening met JavaScript-afhankelijkheden tussen meerdere aanbiedingen op de pagina.

   Je kunt er niet langer van uitgaan dat de aanbieding van de eerste box wordt uitgevoerd vóór de aanbieding van de tweede box.

* Aanbiedingen voor DOM Manipulation en Redirect moeten worden geleverd via de automatisch gemaakte globale mbox in [!DNL at.js] en geleverd in de `<head>`.

   Een `mboxCreate()` functie boven aan het scherm `<body>` zal waarschijnlijk de standaardinhoud flikkeren.

