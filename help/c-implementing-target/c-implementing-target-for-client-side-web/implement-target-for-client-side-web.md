---
keywords: implement;implementation;at.js;adobe experience platform web sdk;aep web sdk
description: Informatie over het implementeren van Adobe Target voor client-side web met at.js.
title: Adobe Target for client-side web implementeren
feature: at.js
translation-type: tm+mt
source-git-commit: a85a5c10c31fb0d7eb00c21ff03b2012d044de45
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Overzicht: Doel voor client-side web implementeren

In een client-side implementatie van [!DNL Adobe Target] levert [!DNL Target] de ervaringen die met een activiteit zijn gekoppeld rechtstreeks aan de clientbrowser. De browser bepaalt welke ervaring wordt weergegeven en geeft deze weer. Met een cliënt-zijimplementatie, kunt u een redacteur WYSIWYG, [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC), of een niet-visuele interface, [Op vorm-gebaseerde Composer van de Ervaring](/help/c-experiences/form-experience-composer.md), gebruiken om uw activiteit en verpersoonlijkingservaringen tot stand te brengen.

Als u [!DNL Adobe Target] client-side wilt implementeren, moet u een van de volgende JavaScript-bibliotheken gebruiken:

* [Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md)
* [Doel in JavaScript-bibliotheek.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md)

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd. We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen.
>
>* **Adobe Experience Platform Web SDK**: Met dit  [!UICONTROL Adobe Experience Platform Web SDK] programma kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in de  [!DNL Experience Cloud] (inclusief  [!DNL Target]). Als u ervoor kiest om naar [!DNL Adobe Experience Platform Web SDK] te migreren, zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Web SDK Guide*.
   >
   >
* **at.js**: De JavaScript-bibliotheek at.js biedt veel voordelen ten opzichte van mbox.js. Het bestand at.js verbetert onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert de beveiliging en biedt betere implementatieopties voor toepassingen op één pagina. Als u verkiest om aan at.js te migreren, zie [How At.js werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) en [Adobe Target Skill Builder: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Hoewel mbox.js momenteel wordt ondersteund (tot 31 maart 2021), hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Door alle klanten naar [!UICONTROL Adobe Experience Platform Web SDK] of at.js te verplaatsen, zullen onze technici en ondersteunend personeel u van nieuwe functionaliteit kunnen voorzien en de steun aanbieden u van Adobe bent gekomen te verwachten.
