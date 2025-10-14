---
kewords: redirect;redirect url;send to different page
description: Leer hoe te om Redirect aan optie URL in Adobe  [!DNL Target]  te gebruiken wanneer u de bezoeker naar een verschillende pagina eerder dan het tonen van inhoud op de zelfde pagina wilt verzenden.
title: Kan ik een pagina omleiden naar een andere URL?
feature: Visual Experience Composer (VEC)
exl-id: bd448482-0079-4689-aa24-65ecbb31b8ae
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# Omleiden naar een URL

Gebruik de optie [!UICONTROL Redirect to URL] in [!DNL Adobe Target] als u de bezoeker naar een andere pagina wilt sturen in plaats van de inhoud op dezelfde pagina weer te geven.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testcampagne in met twee ervaringen: een die verwijst naar de standaardpagina A en een andere die wordt doorgestuurd naar pagina B. Kies **[!UICONTROL Redirect to URL]** in het menu Actie beleven door op het letterlabel voor de beleving te klikken en geef de URL van pagina B op. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

De omleidingsaanbieding voert de code van JavaScript uit om browser om te leiden. Het gebruikt de `window.location.replace();` methode, zodat wordt de pagina de bezoeker van wordt opnieuw geleid niet opgeslagen in de browser geschiedenis. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

Aanbiedingen voor omleiding hebben een aantal beperkingen:

* Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Voor meer informatie, zie [&#x200B; Aanbiedingen opnieuw richten - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
* Als u de op formulieren gebaseerde Experience Composer gebruikt, mogen omleidingsvoorstellen niet worden gebruikt in vakken die deel uitmaken van de pagina. Een omleidingsaanbieding mag alleen worden gebruikt vanuit een scripttag die deel uitmaakt van de HTML `<head>` . Gebruik altijd Automatisch maken en stel de omleidingsaanbieding voor de globale mbox in.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

Een omleidingsvoorstel maken:

1. Maak een ervaring.
1. Van het [!UICONTROL Experiences] kader, klik het **[!UICONTROL More Actions]** pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallList.svg)) voor de gewenste ervaring.
1. Klik op **[!UICONTROL Redirect to URL]**.
1. Typ de URL in het dialoogvenster Omleiden naar URL.
1. Selecteer desgewenst de optie om de huidige queryparameters op te nemen.

   Als deze optie wordt geselecteerd, om het even wat na ? in de URL van de bezoeker wordt toegevoegd aan de omleidings-URL op het moment van omleiding.

1. (Optioneel) Maak aanvullende regels.

   De extra regels kunnen op om het even welk van het volgende worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

## Bekende problemen

* De omleiding van activiteiten in implementaties at.js zou de voorproef URL kunnen veroorzaken om in een lijn in te gaan (de aanbieding wordt herhaaldelijk geleverd). U kunt [&#x200B; Wijze QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md) gebruiken in plaats daarvan om Voorproef en QA uit te voeren. Deze kwestie heeft geen invloed op de daadwerkelijke levering van het aanbod. (TGT-23019)
