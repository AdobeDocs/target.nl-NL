---
keywords: host;hosts;hostgroep;problemen oplossen;aanbevolen procedures;ubox;omleiding;omleiding;whitelist;lijst van gewenste personen;zwarte lijst;lijst van gewezen personen
description: Leer hoe u uw websites en pre-productieomgevingen kunt ordenen voor eenvoudig beheer en gescheiden rapportering in Adobe Target.
title: Wat zijn gastheren en hoe gebruik ik ze?
feature: Beheer en configuratie
role: Beheerder
translation-type: tm+mt
source-git-commit: 86102ed5b49d102660ed38fe0a71612cefcd2caf
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---


# Gastheren

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage in [!DNL Adobe Target].

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u rapportgegevens door [milieu](/help/administrating-target/environments.md) ook scheiden.

Een gastheer is om het even welk domein waarvan een [!DNL Target] verzoek wordt gemaakt. Op een website is het doorgaans de eigenschap `location.hostname` van de URL die de aanvraag [!DNL Target] indient.

[!DNL Target] beperkt standaard geen host die [!DNL Target]-aanvragen kan indienen en [!DNL Target]-reacties kan ontvangen. Wanneer nieuwe gastheren verzoeken indienen, werken zij automatisch. Met dit proces kunt u ook testen op verschillende domeinen die u niet kent of niet kunt voorzien. Als u dit standaardgedrag wilt met voeten treden, kunt u opstelling een lijst van gewenste personen of een lijst van gewezen personen om te beperken welke gastheren met [!DNL Target] werken.

Als u hosts wilt beheren, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Hosts {#concept_0D4B43E23AA9408F8B28A57ED754BF65} herkennen

Als u een host wilt herkennen en toevoegen aan de lijst [!UICONTROL Hosts], moet aan de volgende voorwaarden zijn voldaan:

* Er moet minstens één [!DNL Target]-verzoek op de host aanwezig zijn
* Een pagina op de host moet het volgende bevatten:

   * Een nauwkeurige verwijzing naar at.js
   * Een [!DNL Target] verzoek of een automatisch gegenereerde globale [!DNL Target] verzoek

* De pagina met het [!DNL Target] verzoek moet in browser worden bekeken

Nadat de pagina is weergegeven, wordt de host vermeld in de lijst [!UICONTROL Hosts], zodat u deze in een omgeving kunt beheren en activiteiten en tests kunt voorvertonen en starten.

>[!NOTE]
>
>Dit geldt ook voor persoonlijke ontwikkelservers.

Nadat een gastheer aan [!UICONTROL Host] lijst wordt toegevoegd, zorg ervoor dat de gastheer wordt erkend.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Vernieuw de browser als uw host niet in de lijst staat.

   Standaard wordt een nieuw herkende host in de [!UICONTROL Production]-omgeving geplaatst. De [!UICONTROL Production] omgeving is het veiligste milieu omdat het inactieve activiteiten niet toelaat om van deze gastheren worden bekeken.

1. (Voorwaardelijk) klik **[!UICONTROL Move]** pictogram ( ![verplaatsingspictogram](/help/administrating-target/assets/icon-move.png)) om de gastheer in [!UICONTROL Development], [!UICONTROL Staging], of andere milieu te bewegen.

>[!NOTE]
>
>De [!UICONTROL Production]-omgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. Men veronderstelt dat dit milieu is waar u definitieve, actieve activiteiten en tests dient. De standaardomgeving staat niet toe dat inactieve campagnes worden weergegeven.

## De lijst met hosts sorteren of doorzoeken {#section_068B23C9D8224EB78BC3B7C8580251B0}

Als u de lijst [!UICONTROL Hosts] wilt sorteren, klikt u op een kolomkop ([!UICONTROL Name], [!UICONTROL Environment] of [!UICONTROL Last Requested]) om de lijst in oplopende of aflopende volgorde te sorteren.

Als u in de lijst [!UICONTROL Hosts] wilt zoeken, typt u een zoekterm in het vak [!UICONTROL Search Hosts].

## Creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om de verzoeken van het Doel naar Doel te verzenden. {#allowlist}

U kunt een lijst van gewenste personen tot stand brengen die gastheren (domeinen) specificeert die [!DNL Target] verzoeken naar [!DNL Target] mogen verzenden. Alle andere gastheren die verzoeken produceren krijgen een commentaar-uit reactie van de vergunningsfout. Door gebrek, om het even welke gastheer die [!DNL Target] verzoek bevat registreert bij [!DNL Target] in het [!UICONTROL Production] milieu en heeft toegang tot alle actieve en goedgekeurde activiteiten. Als deze benadering niet wordt gewenst, kunt u in plaats daarvan de lijst van gewenste personen gebruiken om specifieke gastheren te registreren die geschikt zijn om [!DNL Target] verzoeken te maken en [!DNL Target] inhoud te ontvangen. Alle gastheren blijven in de [!UICONTROL Hosts] lijst tonen, en de milieu&#39;s kunnen nog worden gebruikt om deze gastheren te groeperen en verschillende niveaus aan elk toe te wijzen, zoals of de gastheer actieve en/of inactieve activiteiten kan zien.

Een lijst van gewenste personen maken:

1. Klik in de lijst [!UICONTROL Hosts] op **[!UICONTROL Authorize Hosts]**.
1. Schakel de schakeloptie **[!UICONTROL Enable Authorized Hosts for content delivery]** in.
1. Voeg desgewenst de gewenste hosts toe in het tekstvak **[!UICONTROL Host contains]**.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Voeg desgewenst de gewenste hosts toe in het tekstvak **[!UICONTROL Host does not contains]**.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Klik op **[!UICONTROL Save]**.

Als een [!DNL Target] verzoek op een onbevoegde gastheer wordt gemaakt, antwoordt de vraag met `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Aanbevolen werkwijzen** voor beveiliging: Als u ubox functionaliteit van gebruikt  [!DNL Target], controleert deze lijst van gewenste personen ook de lijst van domeinen waaraan uw redirectorcan  [](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) navigeert. Zorg ervoor dat u alle domeinen toevoegt waarnaar u wilt omleiden wanneer u ubox als onderdeel van uw implementatie gebruikt. Als de lijst van gewenste personen niet gespecificeerd wordt verlaten, [!DNL Adobe] kan niet redirect URLs verifiëren en tegen potentiële kwaadwillige omleidingen beschermen.
>
>De lijst van gewenste personen heeft voorrang op omgevingen. Wis uit alle gastheren alvorens de eigenschap van de lijst van gewenste personen te gebruiken, dan slechts verschijnen de gastheren die door de lijst van gewenste personen worden toegestaan in uw gastheerlijst. Vervolgens kunt u de hosts naar de gewenste omgeving verplaatsen.

Soms verschijnen domeinen van andere plaatsen in uw milieu&#39;s. Een domein verschijnt in de lijst als het domein at.js roept. Als iemand bijvoorbeeld een van uw webpagina&#39;s naar de server kopieert, wordt dat domein in uw omgeving weergegeven. U ziet wellicht ook domeinen van spintengines, vertaalsites of lokale schijfstations.

In gevallen waarin `mboxHost` in een API vraag wordt overgegaan, wordt de omzetting geregistreerd voor het milieu dat binnen wordt overgegaan. Als geen milieu wordt overgegaan, blijft de gastheer in de vraag aan [!UICONTROL Production] in gebreke.

U kunt een lijst van gewezen personen ook tot stand brengen die gastheren (domeinen) specificeert die [!DNL Target] verzoeken aan [!DNL Target] niet kunnen verzenden door de gewenste gastheren in [!UICONTROL Host Does Not Contain] doos toe te voegen.

>[!NOTE]
>
>De lijst [!UICONTROL Authorized Hosts] wordt gebruikt voor zowel [!DNL Target] gastheren als standaard opnieuw richten gastheren. Voeg alle bestaande domeinen toe die zijn goedgekeurd voor het gebruik van de [!DNL Adobe Target] JavaScript SDK (at.js) *AND* alle domeinen die in ubox standaard omleidings URLs worden gebruikt. Voeg nieuwe gelijkaardige domeinen aan de lijst van gewenste personen in de toekomst toe.

## Een host {#section_F56355BA4BC54B078A1A8179BC954632} verwijderen

U kunt een host verwijderen wanneer deze niet meer nodig is.

1. Klik in de lijst [!UICONTROL Hosts] op het pictogram **[!UICONTROL Delete]**.
1. Klik **[!UICONTROL Delete]** om de schrapping te bevestigen.

>[!NOTE]
>
>De gastheer wordt opnieuw vermeld als iedereen aan een pagina doorbladert die een [!DNL Target] verzoek op de gastheer bevat.

## Problemen met hosts {#concept_B3D7583FA4BB480382CC7453529FE1B7} oplossen

Probeer de volgende tips voor het oplossen van problemen als u problemen ondervindt met uw hosts:

**De host wordt niet weergegeven in de lijst voor uw account.**

* Vernieuw de pagina [!UICONTROL Hosts] in uw browser.
* Bevestig dat het [!DNL Target] verzoek correct is, met inbegrip van de verwijzing at.js.
* Blader naar een van de [!DNL Target] aanvragen op de host. Het is mogelijk dat geen [!DNL Target] verzoek op de gastheer ooit in browser werd teruggegeven.

**Willekeurige of onbekende domeinen worden in de  [!UICONTROL Host] lijst weergegeven.**

Een domein verschijnt in deze lijst als een verzoek aan [!DNL Target] van het domein wordt gemaakt. Vaak kunt u domeinen zien van spintengines, vertaalsites of lokale schijfstations. Als het vermelde domein niet één uw teamgebruik is, kunt u [!UICONTROL Delete] klikken om het te verwijderen.

**Mijn  [!DNL Target] verzoek retourneert /* geen weergave - ongeoorloofde mbox-host */.**

Als een [!DNL Target] verzoek op een onbevoegde gastheer wordt gemaakt, antwoordt het verzoek met /* geen vertoning - onbevoegde mbox gastheer */.
