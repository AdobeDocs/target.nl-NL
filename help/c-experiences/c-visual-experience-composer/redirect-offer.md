---
description: Gebruik deze optie als u de bezoeker naar een andere pagina wilt sturen in plaats van de inhoud op dezelfde pagina weer te geven.
title: Omleiden naar een URL
feature: vec
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---


# Omleiden naar een URL{#redirect-to-a-url}

Gebruik deze optie als u de bezoeker naar een andere pagina wilt sturen in plaats van de inhoud op dezelfde pagina weer te geven.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testcampagne in met twee ervaringen: één die aan standaardpagina A richt, en andere die aan pagina B wordt opnieuw gericht. Kies **[!UICONTROL Redirect to URL]** in het menu Actie beleven door op het letterlabel voor de ervaring te klikken en geef de URL van pagina B op. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

De omleidingsaanbieding voert code JavaScript uit om browser om te leiden. De methode `window.location.replace();`wordt gebruikt, zodat de pagina waarvan de bezoeker is omgeleid niet in de browsergeschiedenis wordt opgeslagen. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

Aanbiedingen voor omleiding hebben een aantal beperkingen:

* Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie [Aanbiedingen omleiden - A4T veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905) voor meer informatie.
* Als u de op formulieren gebaseerde Experience Composer gebruikt, mogen omleidingsvoorstellen niet worden gebruikt in vakken die deel uitmaken van de pagina. Een omleidingsaanbieding mag alleen worden gebruikt vanuit een scripttag die deel uitmaakt van de HTML `<head>`. Gebruik altijd Automatisch maken en stel de omleidingsaanbieding voor de globale mbox in.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

Een omleidingsvoorstel maken:

1. Maak een ervaring.
1. Houd de muis boven een ervaring en klik vervolgens op het pictogram Omleiden naar URL (![](assets/icon_redirect_url.png)).

   ![](assets/exp_actions.png)

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
   De extra regels kunnen met EN of OF aan de Activiteit URL worden aangesloten. Alle regels die u toevoegt, worden tegen elkaar geëvalueerd met EN.
