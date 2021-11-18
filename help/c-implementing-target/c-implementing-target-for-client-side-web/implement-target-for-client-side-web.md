---
keywords: implementeren;implementatie;at.js;adobe Experience platform web sdk;aep web sdk
description: Leer hoe u Adobe implementeert [!DNL Target] for client-side web using the Adobe Experience Platform Web SDK  (AEP Web SDK) or the [!DNL Target] at.js JavaScript-bibliotheek.
title: Hoe kan ik implementeren [!DNL Target] voor Client-Side Web
feature: at.js
role: Developer
exl-id: 34c1e39b-acae-4547-b67f-584bcd59913f
source-git-commit: bef2b493e8964f468d4f766c932a96d32e994a03
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Overzicht: uitvoeren [!DNL Target] voor client-side web

Bij een clientimplementatie van [!DNL Adobe Target], [!DNL Target] levert de ervaringen verbonden aan een activiteit rechtstreeks aan cliëntbrowser. De browser bepaalt welke ervaring wordt weergegeven en geeft deze weer. Met een cliënt-zijimplementatie, kunt u een redacteur gebruiken WYSIWYG, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) of een niet-visuele interface [Form-based Experience Composer](/help/c-experiences/form-experience-composer.md), om uw activiteiten en personalisatie-ervaringen te creëren.

Om [!DNL Adobe Target] aan clientzijde moet u een van de volgende JavaScript-bibliotheken gebruiken:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Doel in JavaScript-bibliotheek.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Vanaf 31 maart 2021, [!DNL Adobe Target] ondersteunt de bibliotheek niet meer. Na 31 maart 2021 mislukken alle aanroepen van mbox.js op elegante wijze en hebben deze invloed op uw pagina&#39;s die [!DNL Target] activiteiten die worden uitgevoerd door het bedienen van standaardinhoud. Adobe raadt alle klanten aan naar de meest recente versie van de nieuwe versie te migreren [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek op at.js vóór deze datum om mogelijke problemen met uw sites te voorkomen.
>
>* **Adobe Experience Platform Web SDK**: De [!UICONTROL Adobe Experience Platform Web SDK] kunt u de verschillende services van de [!DNL Experience Cloud] (inclusief [!DNL Target]) via Adobe Experience Edge Network. Als u naar de [!DNL Adobe Experience Platform Web SDK], zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in de *Web SDK Guide*.
>
>* **at.js**: De JavaScript-bibliotheek at.js verbetert de laadtijden van pagina&#39;s voor webimplementaties, verbetert de beveiliging en biedt betere implementatieopties voor toepassingen op één pagina. Als u naar at.js wilt migreren, raadpleegt u [Hoe werkt At.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) en [Adobe Target Skill Builder: Chat op ontwikkelaar, migrate Adobe Target mbox.js naar at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).


