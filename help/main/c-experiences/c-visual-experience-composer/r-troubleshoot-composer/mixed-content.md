---
keywords: gemengde inhoud;veilig;onveilig;chroom;problemen;vec;visuele ervaringscomposer;onveilig;http;https;firefox;Internet Explorer
description: Leer hoe te om gemengde inhoud in  [!DNL Chrome] toe te laten,  [!DNL Firefox], en  [!DNL Edge].
title: Hoe te om Gemengde Inhoud in Mijn Browser toe te laten
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: c5b43faa2fc55c2c8737e586cfdfaa1444a05880
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Gemengde inhoud in uw browser inschakelen

De gemengde inhoud komt voor als het aanvankelijke verzoek over HTTPS veilig is, maar HTTPS *en* de inhoud van HTTP wordt geladen om de Web-pagina te tonen. HTTPS-inhoud is beveiligd. HTTP-inhoud is onveilig.

Moderne browsers kunnen de weergave van een pagina blokkeren of waarschuwingsberichten weergeven als beveiligde inhoud wordt gemengd met onveilige inhoud.

Er wordt een waarschuwingsbericht weergegeven als de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] een pagina probeert te openen die gemengde inhoud bevat. Dit bericht geeft aan hoe u blokkering in uw browser kunt uitschakelen. Als u het blokkeren uitschakelt, kunt u een HTTP-site of een site met gemengde inhoud (HTTPS en HTTP) openen.

![&#x200B; Gemengde inhoudswaarschuwing &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Eerder, toen gemengde inhoud niet werd toegestaan, kon u sommige acties in Stap 1 van het drie-stap geleide werkschema nog uitvoeren wanneer het creëren van activiteiten. [!DNL Target] blokkeert nu handelingen in stap 1. Wanneer dit bericht wordt weergegeven, moet u gemengde inhoud inschakelen voordat u verdergaat met het maken van de activiteit.

De beveiligingsinstellingen van uw browser kunnen voorkomen dat gemengde inhoud of onveilige (HTTP-) inhoud wordt geladen in een beveiligde (HTTPS-) pagina of frame (zoals de VEC). Als u de beveiligingsinstellingen van uw browser niet wilt uitschakelen, hebt u een HTTPS-website nodig.

Als uw website op een onbeveiligd (HTTP) domein loopt, moet u VEC toestaan om actieve gemengde inhoud te laden.

>[!IMPORTANT]
>
>Het toestaan van gemengde inhoud beïnvloedt slechts VEC en niet uw levende website.

Voor meer informatie, zie [&#x200B; Gemengde Inhoud &#x200B;](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) op de *Mozilla website van het Netwerk van de Ontwikkelaar van het Netwerk* (MDN).

## Gemengde inhoud inschakelen in [!DNL Google Chrome] {#task_FF297A08F66E47A588C14FD67C037B3A}

Als u een site bezoekt via een beveiligde verbinding, controleert [!DNL Chrome] of de inhoud op de webpagina veilig is verzonden.

Zie &quot;[&#x200B; waarschuwingen over onveilige plaatsen &#x200B;](https://support.google.com/chrome/answer/99020?hl=en)&quot;in de Hulp van Chrome van Google beheren.

Als u de VEC gebruikt met de nieuwste versie van [!DNL Chrome] (versie 79.0.3945.117 of hoger), moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Klik op het vergrendelingspictogram (voorzichtig) en klik vervolgens op **[!UICONTROL Site settings]** .

   ![&#x200B; Montages van de Plaats &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Blader naar **[!UICONTROL Insecure content]** en gebruik vervolgens de vervolgkeuzelijst om &quot;Blok (standaard)&quot; te wijzigen in &quot;Toestaan&quot;.

   ![&#x200B; Onveilige inhoud &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laad de VEC-pagina opnieuw.

## Gemengde inhoud inschakelen in [!DNL Mozilla Firefox] {#task_5448763B8DC941FD80F84041AEF0A14D}

Standaard blokkeert [!DNL Firebox] pagina&#39;s die beveiligde en onveilige inhoud mengen. U moet deze instelling permanent wijzigen om [!DNL Target] te gebruiken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Typ in Firefox `about:config` in de adresbalk.
1. Bevestig het waarschuwingsbericht dat door [!DNL Firefox] wordt weergegeven.

   ![&#x200B; waarschuwing Firefox &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Typ `block_active` in de zoekbalk.

   ![&#x200B; blok_active het plaatsen Firefox &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Dubbelklik op ` **[!UICONTROL security.mixed_content.block_active_content]**` .

   De waarde verandert van &quot;Waar&quot; in &quot;Onwaar&quot;. Wanneer de waarde &quot;False&quot; weergeeft, bent u klaar.

   ![&#x200B; veiligheid Firefox &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Start de computer opnieuw nadat u deze instelling hebt gewijzigd.

## Gemengde inhoud inschakelen in [!DNL Microsoft Edge]

Als u een site bezoekt via een beveiligde verbinding, controleert [!DNL Edge] of de inhoud op de webpagina veilig is verzonden.

Als u de VEC gebruikt met de nieuwste versie van [!DNL Edge] , moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. In [!DNL Edge], klik **[!DNL Microsoft Edge]** in de menubar, **[!UICONTROL Settings]**, dan klik **Cookies en de Toestemmingen van de Plaats**.

1. Schuif naar **[!UICONTROL Insecure content]** .

1. Klik op **[!UICONTROL Insecure content]** en klik vervolgens op **[!UICONTROL Add]** naast **[!UICONTROL Allow]** , voeg de site toe waarop u onveilige inhoud wilt toestaan en klik op **[!UICONTROL Add]** .

1. Laad de VEC-pagina opnieuw.
