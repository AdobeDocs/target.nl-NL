---
kewords: redirect;redirect url;send to different page
description: Leer hoe u de optie Omleiden naar URL in Adobe gebruikt [!DNL Target] wanneer u de bezoeker naar een andere pagina wilt sturen in plaats van de inhoud op dezelfde pagina weer te geven.
title: Kan ik een pagina omleiden naar een andere URL?
feature: Visual Experience Composer (VEC)
exl-id: bd448482-0079-4689-aa24-65ecbb31b8ae
source-git-commit: b0bf54d47ac44afc3597f308ea38fd479c54026d
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Omleiden naar een URL

Gebruik de [!UICONTROL Redirect to URL] optie in [!DNL Adobe Target] wanneer u de bezoeker naar een andere pagina wilt sturen in plaats van de inhoud op dezelfde pagina weer te geven.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testcampagne in met twee ervaringen: één die aan standaardpagina A richt, en andere die aan pagina B wordt opnieuw gericht. Kies in het menu Actie beleven de optie **[!UICONTROL Redirect to URL]** en geeft u de URL van pagina B op. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

De omleidingsaanbieding voert code JavaScript uit om browser om te leiden. Het gebruikt de `window.location.replace();`methode, zodat de pagina waarvan de bezoeker wordt omgeleid niet in de browsergeschiedenis wordt opgeslagen. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

Aanbiedingen voor omleiding hebben een aantal beperkingen:

* Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie voor meer informatie [Omleidingsvoorstellen - Veelgestelde vragen A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
* Als u de op formulieren gebaseerde Experience Composer gebruikt, mogen omleidingsvoorstellen niet worden gebruikt in vakken die deel uitmaken van de pagina. Een omleidingsaanbod mag alleen worden gebruikt vanuit een scripttag die deel uitmaakt van de HTML `<head>`. Gebruik altijd Automatisch maken en stel de omleidingsaanbieding voor de globale mbox in.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

Een omleidingsvoorstel maken:

1. Maak een ervaring.
1. Houd de muis boven een ervaring en klik vervolgens op het pictogram Omleiden naar URL (![icon_redirect_url, afbeelding](assets/icon_redirect_url.png)).

   ![exp_actions, afbeelding](assets/exp_actions.png)

1. Typ de URL.
1. Selecteer desgewenst de optie om de huidige queryparameters op te nemen.

   Als deze optie wordt geselecteerd, om het even wat na ? in de URL van de bezoeker wordt toegevoegd aan de omleidings-URL op het moment van omleiding.

   Deze optie is standaard ingeschakeld.
1. (Optioneel) Maak aanvullende regels.

   De extra regels kunnen op om het even welke volgend worden gebaseerd:

   * URL
   * Domein
   * Pad
   * Hash-fragment (#)
   * Query
   * mbox-parameter

   De extra regels kunnen tot aan de Activiteit URL met EN of OF worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.

## Bekende problemen

* De omleiding van activiteiten in implementaties at.js zou de voorproef URL kunnen veroorzaken om in een lijn in te gaan (de aanbieding wordt herhaaldelijk geleverd). U kunt [QA-modus](/help/main/c-activities/c-activity-qa/activity-qa.md) om Voorvertoning en QA uit te voeren. Deze kwestie heeft geen invloed op de daadwerkelijke levering van het aanbod. (TGT-23019)
