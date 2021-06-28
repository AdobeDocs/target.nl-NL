---
keywords: implementeren;implementatie;at.js;adobe Experience platform web sdk;aep web sdk
description: Leer hoe u de JavaScript-bibliotheek Adobe [!DNL Target] for client-side web using the Adobe Experience Platform Web SDK  (AEP Web SDK) or the [!DNL Target] at.js implementeert.
title: Hoe kan ik  [!DNL Target] implementeren voor web op de client
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Overzicht: [!DNL Target] implementeren voor client-side web

In een client-side implementatie van [!DNL Adobe Target] levert [!DNL Target] de ervaringen die met een activiteit zijn gekoppeld rechtstreeks aan de clientbrowser. De browser bepaalt welke ervaring wordt weergegeven en geeft deze weer. Met een cliënt-zijimplementatie, kunt u een redacteur WYSIWYG, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC), of een niet-visuele interface, [Op vorm-gebaseerde Composer van de Ervaring](/help/c-experiences/form-experience-composer.md), gebruiken om uw activiteit en verpersoonlijkingservaringen tot stand te brengen.

Als u [!DNL Adobe Target] client-side wilt implementeren, moet u een van de volgende JavaScript-bibliotheken gebruiken:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Doel in JavaScript-bibliotheek.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021 wordt de bibliotheek mbox.js  [!DNL Adobe Target] niet meer ondersteund. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en worden deze van invloed op uw pagina&#39;s die [!DNL Target] activiteiten hebben die worden uitgevoerd door standaardinhoud te bedienen. Adobe raadt alle klanten aan vóór deze datum naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js te migreren om mogelijke problemen met uw sites te voorkomen.
>
>* **Adobe Experience Platform Web SDK**: Met dit  [!UICONTROL Adobe Experience Platform Web SDK] programma kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in de  [!DNL Experience Cloud] (inclusief  [!DNL Target]). Als u ervoor kiest om naar [!DNL Adobe Experience Platform Web SDK] te migreren, zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Web SDK Guide*.
   >
   >
* **at.js**: De JavaScript-bibliotheek at.js verbetert de laadtijden van pagina&#39;s voor webimplementaties, verbetert de beveiliging en biedt betere implementatieopties voor toepassingen op één pagina. Als u verkiest om aan at.js te migreren, zie [How At.js werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) en [Adobe Target Skill Builder: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).


