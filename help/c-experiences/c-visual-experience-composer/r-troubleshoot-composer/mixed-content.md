---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure;http;https;firefox;internet explorer
description: Sommige browsers blokkeren de weergave van een pagina als beveiligde inhoud wordt gemengd met onveilige inhoud.
title: Gemengde inhoud in uw browser inschakelen
topic: Advanced,Standard,Classic
uuid: 6944ce97-ff73-4b61-b006-35862ff83ef1
translation-type: tm+mt
source-git-commit: e4f69d6e5543ed022f3f4dc0c13614dd78812457
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---


# Gemengde inhoud in uw browser inschakelen{#enabling-mixed-content-in-your-browser}

Gemengde inhoud komt voor als zowel (veilige) HTTPS *als* (onveilige) inhoud HTTP wordt geladen om de zelfde Web-pagina te tonen en het aanvankelijke verzoek veilig over HTTPS was.

Moderne browsers kunnen de weergave van een pagina blokkeren of waarschuwingsberichten weergeven als beveiligde inhoud wordt gemengd met onveilige inhoud.

Als de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] probeert om een pagina te openen die gemengde inhoud bevat, toont een bericht dat hoe te om het blokkeren in uw browser onbruikbaar te maken zodat kunt u een plaats van HTTP of een plaats openen die gemengde vraag (HTTPS en HTTP) heeft.

![](assets/mixed_content_warning.gif)

Eerder, toen gemengde inhoud niet werd toegestaan, kon u sommige acties in Stap 1 van het drie-stap geleide werkschema nog uitvoeren wanneer het creëren van activiteiten. [!DNL Target] blokkeert nu handelingen in stap 1. Wanneer dit bericht wordt weergegeven, moet u gemengde inhoud inschakelen voordat u verdergaat met het maken van de activiteit.

De beveiligingsinstellingen van uw browser kunnen voorkomen dat gemengde inhoud of onveilige (HTTP-) inhoud wordt geladen in een beveiligde (HTTPS-) pagina of frame (zoals de VEC). Als u de beveiligingsinstellingen van uw browser niet wilt uitschakelen, hebt u een HTTPS-website nodig.

Als uw website op een onbeveiligd (HTTP) domein loopt, moet u VEC toestaan om actieve gemengde inhoud te laden.

>[!NOTE]
>
>Het toestaan van gemengde inhoud beïnvloedt slechts VEC en niet uw levende website.

Zie [Gemengde inhoud](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) op de website *Mozilla Developer Network* (MDN) voor meer informatie.

## Gemengde inhoud inschakelen in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Als u een site bezoekt via een beveiligde verbinding, controleert Chrome of de inhoud op de webpagina veilig is verzonden.

Zie [Deze pagina bevat onveilige inhoud](https://support.google.com/chrome/answer/1342714?hl=en) in de Help van Google Chrome.

Als u de VEC gebruikt met de nieuwste versie van Chrome (versie 79.0.3945.117 of hoger), moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Klik op het pictogram Vergrendelen of Voorzichtigheid en klik vervolgens op **[!UICONTROL Site settings]**.

   ![Site-instellingen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Blader naar **[!UICONTROL Insecure content]**, gebruik vervolgens de vervolgkeuzelijst om &quot;Blok (standaard)&quot; te wijzigen in &quot;Toestaan&quot;.

   ![Onveilige inhoud](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laad de VEC-pagina opnieuw.

## Gemengde inhoud inschakelen in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Standaard blokkeert Firebox pagina&#39;s die beveiligde en onveilige inhoud mengen. U wordt aangeraden deze instelling permanent te wijzigen in gebruik [!DNL Target]. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Typ in Firefox `about:config` de adresbalk.
1. Bevestig het waarschuwingsbericht dat door Firefox wordt weergegeven.

   ![Firefox-waarschuwing](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Typ in de zoekbalk `block_active`.

   ![Actieve instelling Firefox-blok](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Dubbelklik ` **[!UICONTROL security.mixed_content.block_active_content]**` .

   De waarde verandert van &quot;Waar&quot; in &quot;Onwaar&quot;. Wanneer de waarde &quot;False&quot; weergeeft, bent u klaar.

   ![Firefox-beveiliging](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

We raden u aan de computer opnieuw op te starten nadat u deze instelling hebt gewijzigd.

## Gemengde inhoud inschakelen in Microsoft Edge

Als u een site bezoekt via een beveiligde verbinding, controleert Edge of de inhoud op de webpagina veilig is verzonden.

Als u de VEC gebruikt met de nieuwste versie van Edge, moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Klik op het pictogram Vergrendelen of Voorzichtigheid en klik vervolgens op **[!UICONTROL Site Permissions]**.

   ![Siterechten in Microsoft Edge](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Blader naar **[!UICONTROL Insecure content]**, gebruik vervolgens de vervolgkeuzelijst om &quot;Blok (standaard)&quot; te wijzigen in &quot;Toestaan&quot;.

   ![Onveilige inhoud](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Laad de VEC-pagina opnieuw.