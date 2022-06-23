---
keywords: host;hosts;hostgroep;problemen oplossen;aanbevolen procedures;ubox;omleiding;omleiding;whitelist;lijst van gewenste personen;zwarte lijst;lijst van gewezen personen
description: Leer hoe u uw websites en pre-productieomgevingen kunt ordenen voor eenvoudig beheer en gescheiden rapportering in Adobe Target.
title: Wat zijn gastheren en hoe gebruik ik ze?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: a0a20b99a76ba0346f00e3841a345e916ffde8ea
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Gastheren

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportering in [!DNL Adobe Target].

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u ook rapportgegevens door scheiden [milieu](/help/main/administrating-target/environments.md).

Een host is elk domein waaruit een [!DNL Target] verzoek wordt ingediend. Op een website is het meestal de `location.hostname` eigenschap van de URL die de [!DNL Target] verzoek.

Standaard, [!DNL Target] beperkt geen host die [!DNL Target] verzoeken en ontvangen [!DNL Target] reacties. Wanneer nieuwe gastheren verzoeken indienen, werken zij automatisch. Met dit proces kunt u ook testen op verschillende domeinen die u niet kent of niet kunt voorzien. Als u dit standaardgedrag wilt met voeten treden, kunt u opstelling een lijst van gewenste personen of een lijst van gewezen personen om te beperken welke gastheren werken met [!DNL Target].

Als u hosts wilt beheren, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Hosts herkennen {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Een host herkennen en deze toevoegen aan de [!UICONTROL Hosts] lijst, moet aan de volgende voorwaarden worden voldaan:

* Ten minste één [!DNL Target] verzoek moet op de gastheer bestaan
* Een pagina op de host moet het volgende bevatten:

   * Een nauwkeurige verwijzing naar at.js
   * A [!DNL Target] verzoek of een automatisch gegenereerde globale [!DNL Target] verzoek

* De pagina met de [!DNL Target] verzoek moet in browser worden bekeken

Nadat de pagina is weergegeven, wordt de host weergegeven in het dialoogvenster [!UICONTROL Hosts] lijst, zodat u deze in een omgeving kunt beheren en activiteiten en tests kunt voorvertonen en starten.

>[!NOTE]
>
>Dit geldt ook voor persoonlijke ontwikkelservers.

Nadat een gastheer aan wordt toegevoegd [!UICONTROL Host] controleert u of de host wordt herkend.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Vernieuw de browser als uw host niet in de lijst staat.

   Standaard wordt een nieuw herkende host in het dialoogvenster [!UICONTROL Production] milieu. De [!UICONTROL Production] milieu is het veiligste milieu omdat het inactieve activiteiten om van deze gastheren niet toelaat worden bekeken.

1. (Voorwaardelijk) Klik op de knop **[!UICONTROL Move]** icon ( ![verplaatsingspictogram](/help/main/administrating-target/assets/icon-move.png) ) om de host naar de [!UICONTROL Development], [!UICONTROL Staging]of andere omgeving.

>[!NOTE]
>
>De [!UICONTROL Production] milieu kan niet worden geschrapt, zelfs als u het anders noemt. Men veronderstelt dat dit milieu is waar u definitieve, actieve activiteiten en tests dient. De standaardomgeving staat niet toe dat inactieve campagnes worden weergegeven.

## De lijst met gastheren sorteren of doorzoeken {#section_068B23C9D8224EB78BC3B7C8580251B0}

Als u de opdracht [!UICONTROL Hosts] lijst, klik om het even welke kolomkopbal ([!UICONTROL Name], [!UICONTROL Environment], of [!UICONTROL Last Requested]) om de lijst in oplopende of aflopende volgorde te sorteren.

Als u de opdracht [!UICONTROL Hosts] lijst, typt u een zoekterm in het dialoogvenster [!UICONTROL Search Hosts] doos.

## Creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om te verzenden [!DNL Target] verzoeken om [!DNL Target]. {#allowlist}

U kunt een lijst van gewenste personen tot stand brengen die gastheren (domeinen) specificeert die worden gemachtigd om te verzenden [!DNL Target] verzoeken om [!DNL Target]. Alle andere gastheren die verzoeken produceren krijgen een commentaar-uit reactie van de vergunningsfout. Standaard elke host die een [!DNL Target] om registers te verzoeken met [!DNL Target] in de [!UICONTROL Production] milieu en toegang heeft tot alle actieve en goedgekeurde activiteiten. Als deze benadering niet wordt gewenst, kunt u in plaats daarvan de lijst van gewenste personen gebruiken om specifieke gastheren te registreren die verkiesbaar zijn om te maken [!DNL Target] verzoeken en ontvangen [!DNL Target] inhoud. Alle hosts blijven in de [!UICONTROL Hosts] lijst, en de milieu&#39;s kunnen nog worden gebruikt om deze gastheren te groeperen en verschillende niveaus aan elk toe te wijzen, zoals of de gastheer actieve en/of inactieve activiteiten kan zien.

Een lijst van gewenste personen maken:

1. Van de [!UICONTROL Hosts] lijst, klikt u op **[!UICONTROL Authorize Hosts]**.
1. De optie **[!UICONTROL Enable Authorized Hosts for content delivery]** schakelen.
1. Voeg de gewenste hosts toe in het dialoogvenster **[!UICONTROL Host contains]** naar wens.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Voeg de gewenste hosts toe in het dialoogvenster **[!UICONTROL Host does not contains]** naar wens.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Klik op **[!UICONTROL Save]**.

Indien een [!DNL Target] het verzoek wordt gemaakt op een onbevoegde gastheer, beantwoordt de vraag met `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Aanbevolen werkwijzen voor beveiliging**: Als u de functionaliteit van het selectievakje [!DNL Target], controleert deze lijst van gewenste personen ook de lijst van domeinen waaraan uw [directeuren](https://developer.adobe.com/target/implement/email/working-with-redirectors/){target=_blank} kan navigeren. Zorg ervoor dat u alle domeinen toevoegt waarnaar u wilt omleiden wanneer u ubox als onderdeel van uw implementatie gebruikt. Als de lijst van gewenste personen niet gespecificeerd is, [!DNL Adobe] kan de omleidings-URL&#39;s niet controleren en beschermen tegen mogelijke omleiding door kwaadwillende gebruikers.
>
>De lijst van gewenste personen heeft voorrang op omgevingen. Wis uit alle gastheren alvorens de eigenschap van de lijst van gewenste personen te gebruiken, dan slechts verschijnen de gastheren die door de lijst van gewenste personen worden toegestaan in uw gastheerlijst. Vervolgens kunt u de hosts naar de gewenste omgeving verplaatsen.

Soms verschijnen domeinen van andere plaatsen in uw milieu&#39;s. Een domein verschijnt in de lijst als het domein at.js roept. Als iemand bijvoorbeeld een van uw webpagina&#39;s naar de server kopieert, wordt dat domein in uw omgeving weergegeven. U ziet wellicht ook domeinen van spintengines, vertaalsites of lokale schijfstations.

Wanneer `mboxHost` wordt doorgegeven in een API-aanroep, wordt de conversie opgenomen voor de omgeving die wordt doorgegeven. Als geen milieu wordt overgegaan, blijft de gastheer in de vraag in gebreke aan [!UICONTROL Production].

U kunt ook een lijst van gewezen personen maken die hosts (domeinen) opgeeft die niet kunnen worden verzonden [!DNL Target] verzoeken om [!DNL Target] door de gewenste hosts toe te voegen in het dialoogvenster [!UICONTROL Host Does Not Contain] doos.

>[!NOTE]
>
>De [!UICONTROL Authorized Hosts] list wordt gebruikt voor beide [!DNL Target] hosts en standaardomleidingshosts. Voeg alle bestaande domeinen toe die zijn goedgekeurd om de [!DNL Adobe Target] JavaScript SDK (at.js) *EN* alle domeinen die in ubox standaard worden gebruikt omleiden URLs. Voeg nieuwe gelijkaardige domeinen aan de lijst van gewenste personen in de toekomst toe.

## Een host verwijderen {#section_F56355BA4BC54B078A1A8179BC954632}

U kunt een host verwijderen wanneer deze niet meer nodig is.

1. Van de [!UICONTROL Hosts] lijst, klikt u op de knop **[!UICONTROL Delete]** pictogram.
1. Klikken **[!UICONTROL Delete]** om de schrapping te bevestigen.

>[!NOTE]
>
>De gastheer wordt opnieuw vermeld als iemand naar een pagina bladert die een [!DNL Target] verzoek aan de gastheer.

## Problemen met hosts oplossen {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probeer de volgende tips voor het oplossen van problemen als u problemen ondervindt met uw hosts:

**De host wordt niet weergegeven in de lijst voor uw account.**

* Vernieuw de [!UICONTROL Hosts] in uw browser.
* Bevestig dat de [!DNL Target] Het verzoek is correct, met inbegrip van de verwijzing at.js.
* Probeer te bladeren naar een van de [!DNL Target] verzoeken aan de gastheer. Het is mogelijk dat [!DNL Target] De aanvraag op de host is ooit in een browser weergegeven.

**Willekeurige of onbekende domeinen worden weergegeven in de [!UICONTROL Host] lijst.**

Een domein verschijnt in deze lijst als een verzoek om [!DNL Target] wordt gemaakt van het domein. Vaak kunt u domeinen zien van spintengines, vertaalsites of lokale schijfstations. Als het vermelde domein niet een domein is dat uw team gebruikt, kunt u op [!UICONTROL Delete] om het te verwijderen.

**Mijn [!DNL Target] request returns /&#42; geen weergave - ongeoorloofde mbox-host &#42;/.**

Indien een [!DNL Target] het verzoek wordt ingediend op een ongeoorloofde gastheer , het verzoek beantwoordt met /&#42; geen weergave - ongeoorloofde mbox-host &#42;/.
