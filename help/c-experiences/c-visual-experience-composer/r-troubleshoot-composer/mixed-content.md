---
keywords: gemengde inhoud;veilig;onveilig;chroom;problemen;vec;visuele ervaringscomposer;onveilig;http;https;firefox;Internet Explorer
description: Sommige browsers blokkeren de weergave van een pagina als beveiligde inhoud wordt gemengd met onveilige inhoud. Leer hoe u gemengde inhoud inschakelt in Chrome, Firefox en Edge.
title: Hoe laat ik Gemengde Inhoud in Mijn Browser toe?
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 453106f7534f83c205722421bbf00044fde7da67
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---


# Gemengde inhoud in uw browser inschakelen

Gemengde inhoud komt voor als het aanvankelijke verzoek over HTTPS veilig is, maar de inhoud HTTPS *en* van HTTP wordt geladen om de Web-pagina te tonen. HTTPS-inhoud is beveiligd. HTTP-inhoud is onveilig.

Moderne browsers kunnen de weergave van een pagina blokkeren of waarschuwingsberichten weergeven als beveiligde inhoud wordt gemengd met onveilige inhoud.

Er wordt een waarschuwingsbericht weergegeven als de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Target] een pagina probeert te openen die gemengde inhoud bevat. Dit bericht geeft aan hoe u blokkering in uw browser kunt uitschakelen. Als u het blokkeren uitschakelt, kunt u een HTTP-site of een site met gemengde aanroepen (HTTPS en HTTP) openen.

![Waarschuwing gemengde inhoud](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Eerder, toen gemengde inhoud niet werd toegestaan, kon u sommige acties in Stap 1 van het drie-stap geleide werkschema nog uitvoeren wanneer het creëren van activiteiten. [!DNL Target] blokkeert nu handelingen in stap 1. Wanneer dit bericht wordt weergegeven, moet u gemengde inhoud inschakelen voordat u verdergaat met het maken van de activiteit.

De beveiligingsinstellingen van uw browser kunnen voorkomen dat gemengde inhoud of onveilige (HTTP-) inhoud wordt geladen in een beveiligde (HTTPS-) pagina of frame (zoals de VEC). Als u de beveiligingsinstellingen van uw browser niet wilt uitschakelen, hebt u een HTTPS-website nodig.

Als uw website op een onbeveiligd (HTTP) domein loopt, moet u VEC toestaan om actieve gemengde inhoud te laden.

>[!NOTE]
>
>Het toestaan van gemengde inhoud beïnvloedt slechts VEC en niet uw levende website.

Zie [Gemengde inhoud](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) op de website *Mozilla Developer Network* (MDN) voor meer informatie.

## Gemengde inhoud inschakelen in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Als u een site bezoekt via een beveiligde verbinding, controleert Chrome of de inhoud op de webpagina veilig is verzonden.

Zie &quot;[Deze pagina heeft onveilige inhoud](https://support.google.com/chrome/answer/1342714?hl=en)&quot; in de Help van Google Chrome.

Als u de VEC gebruikt met de nieuwste versie van Chrome (versie 79.0.3945.117 of hoger), moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Klik op het vergrendelingspictogram (voorzichtig) en klik op **[!UICONTROL Site settings]**.

   ![Site-instellingen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Blader naar **[!UICONTROL Insecure content]** en gebruik vervolgens de vervolgkeuzelijst om &quot;Blok (standaard)&quot; te wijzigen in &quot;Toestaan&quot;.

   ![Onveilige inhoud](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laad de VEC-pagina opnieuw.

## Gemengde inhoud inschakelen in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Standaard blokkeert Firebox pagina&#39;s die beveiligde en onveilige inhoud mengen. U wordt aangeraden deze instelling permanent te wijzigen in [!DNL Target]. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Typ `about:config` in de adresbalk van Firefox.
1. Bevestig het waarschuwingsbericht dat door Firefox wordt weergegeven.

   ![Firefox-waarschuwing](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Typ `block_active` in de zoekbalk.

   ![Firefox block_active setting](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Dubbelklik op ` **[!UICONTROL security.mixed_content.block_active_content]**`.

   De waarde verandert van &quot;Waar&quot; in &quot;Onwaar&quot;. Wanneer de waarde &quot;False&quot; weergeeft, bent u klaar.

   ![Firefox-beveiliging](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

Start de computer opnieuw nadat u deze instelling hebt gewijzigd.

## Gemengde inhoud inschakelen in Microsoft Edge

Als u een site bezoekt via een beveiligde verbinding, controleert Edge of de inhoud op de webpagina veilig is verzonden.

Als u de VEC gebruikt met de nieuwste versie van Edge, moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Klik op het vergrendelingspictogram (voorzichtig) en klik op **[!UICONTROL Site Permissions]**.

   ![Siterechten in Microsoft Edge](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge.png)

1. Blader naar **[!UICONTROL Insecure content]** en gebruik vervolgens de vervolgkeuzelijst om &quot;Blok (standaard)&quot; te wijzigen in &quot;Toestaan&quot;.

   ![Onveilige inhoud](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/ms-edge-2.png)

1. Laad de VEC-pagina opnieuw.