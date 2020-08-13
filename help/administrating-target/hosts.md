---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.
title: Gastheren
feature: hosts and environments
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---


# Gastheren{#hosts}

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u rapportgegevens door [milieu](/help/administrating-target/environments.md)ook scheiden.

Een host is elk domein waaruit een [!DNL Target] aanvraag wordt gedaan. Op een website is dit doorgaans de `location.hostname` eigenschap van de URL die de [!DNL Target] aanvraag doet.

Door gebrek, beperkt [!DNL Target] niet een gastheer die [!DNL Target] verzoeken kan indienen en [!DNL Target] reacties ontvangen. Wanneer nieuwe gastheren verzoeken indienen, werken zij automatisch. Hierdoor kunt u ook testen op verschillende domeinen die u niet kent of niet kunt voorzien. Als u dit standaardgedrag wilt met voeten treden, kunt u opstelling een lijst van gewenste personen of een lijst van afgewezen personen om te beperken welke gastheren zullen werken met [!DNL Target].

Als u hosts wilt beheren, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Hosts herkennen {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Als u een host wilt herkennen en toevoegen aan de [!UICONTROL Hosts] lijst, moet aan de volgende voorwaarden zijn voldaan:

* Er moet minstens één [!DNL Target] verzoek aanwezig zijn op de host
* Een pagina op de host moet het volgende bevatten:

   * Een nauwkeurige verwijzing van at.js of mbox.js
   * Een [!DNL Target] verzoek of een automatisch gegenereerd globaal [!DNL Target] verzoek

* De pagina met het [!DNL Target] verzoek moet in een browser worden weergegeven

Nadat de pagina is weergegeven, wordt de host vermeld in de [!UICONTROL Hosts] lijst, zodat u deze in een omgeving kunt beheren en activiteiten en tests kunt voorvertonen en starten.

>[!NOTE]
>
>Dit geldt ook voor persoonlijke ontwikkelservers.

Nadat een gastheer aan de [!UICONTROL Host] lijst wordt toegevoegd, zorg ervoor dat de gastheer wordt erkend.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Vernieuw de browser als uw host niet in de lijst staat.

   Standaard wordt een nieuw herkende host in de [!UICONTROL Production] omgeving geplaatst. Dit is het veiligste milieu omdat het inactieve activiteiten niet om van deze gastheren toelaat worden bekeken.

1. (Voorwaardelijk) Klik op het **[!UICONTROL Move]** pictogram ( ![verplaatsingspictogram](/help/administrating-target/assets/icon-move.png) ) om de host naar de [!UICONTROL Development], [!UICONTROL Staging]of andere omgeving te verplaatsen.

>[!NOTE]
>
>De [!UICONTROL Production] omgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. Men gaat ervan uit dat u hier de laatste, actieve activiteiten en tests zult bedienen. De standaardomgeving staat niet toe dat inactieve campagnes worden weergegeven.

## De lijst met gastheren sorteren of doorzoeken {#section_068B23C9D8224EB78BC3B7C8580251B0}

Als u de [!UICONTROL Hosts] lijst wilt sorteren, klikt u op een kolomkop ([!UICONTROL Name], [!UICONTROL Environment]of [!UICONTROL Last Requested]) om de lijst in oplopende of aflopende volgorde te sorteren.

Als u in de [!UICONTROL Hosts] lijst wilt zoeken, typt u een zoekterm in het [!UICONTROL Search Hosts] vak.

## Creeer lijsten van gewenste personen die gastheren specificeren die worden gemachtigd om de verzoeken van het Doel naar Doel te verzenden. {#allowlist}

U kunt een lijst van gewenste personen tot stand brengen die gastheren (domeinen) specificeert die worden gemachtigd om [!DNL Target] verzoeken naar te verzenden [!DNL Target]. Alle andere gastheren die verzoeken produceren zullen een commentaar-uit reactie van de vergunningsfout krijgen. Door gebrek, om het even welke gastheer die een [!DNL Target] verzoekregisters met [!DNL Target] in het [!UICONTROL Production] milieu bevat en toegang tot alle actieve en goedgekeurde activiteiten heeft. Als dit niet de gewenste benadering is, kunt u in plaats daarvan de lijst van gewenste personen gebruiken om specifieke gastheren te registreren die verkiesbaar zijn om [!DNL Target] verzoeken te doen en [!DNL Target] inhoud te ontvangen. Alle gastheren zullen in de [!UICONTROL Hosts] lijst blijven tonen, en de milieu&#39;s kunnen nog worden gebruikt om deze gastheren te groeperen en verschillende niveaus aan elk toe te wijzen, zoals of de gastheer actieve en/of inactieve activiteiten kan zien.

Een lijst van gewenste personen maken:

1. From the [!UICONTROL Hosts] list, click **[!UICONTROL Authorize Hosts]**.
1. Schakel de **[!UICONTROL Enable Authorized Hosts for content delivery]** schakeloptie in.
1. Voeg desgewenst de gewenste hosts in het **[!UICONTROL Host contains]** vak toe.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Voeg desgewenst de gewenste hosts in het **[!UICONTROL Host does not contains]** vak toe.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Klik op **[!UICONTROL Save]**.

Als een [!DNL Target] verzoek op een onbevoegde gastheer wordt ingediend, zal de vraag met antwoorden `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Aanbevolen werkwijzen** voor beveiliging: Als u ubox functionaliteit van gebruikt [!DNL Target], merk op dat deze lijst van gewenste personen ook de lijst van domeinen zal controleren waaraan uw [bestuurders](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) kunnen navigeren. Zorg ervoor dat u alle domeinen toevoegt waarnaar u wilt omleiden wanneer u ubox als onderdeel van uw implementatie gebruikt. Als de lijst van gewenste personen niet gespecificeerd wordt verlaten, [!DNL Adobe] zal niet omleidings URLs kunnen verifiëren en tegen potentiële kwaadwillige omleidingen beschermen.
>
>De lijst van gewenste personen heeft voorrang op omgevingen. U zou alle gastheren moeten ontruimen alvorens de eigenschap van de lijst van gewenste personen te gebruiken, dan slechts verschijnen de gastheren die door de lijst van gewenste personen worden toegestaan in uw gastheerlijst. Vervolgens kunt u de hosts naar de gewenste omgeving verplaatsen.

Soms verschijnen domeinen van andere plaatsen in uw milieu&#39;s. Een domein verschijnt in de lijst als het domein een vraag aan uw at.js of mbox.js maakt. Als iemand bijvoorbeeld een van uw webpagina&#39;s naar de server kopieert, wordt dat domein in uw omgeving weergegeven. U ziet wellicht ook domeinen van spintengines, vertaalsites of lokale schijfstations.

Wanneer een API-aanroep `mboxHost` wordt doorgegeven, wordt de conversie opgenomen voor de omgeving die wordt doorgegeven. Als geen milieu wordt overgegaan, blijft de gastheer in de vraag aan [!UICONTROL Production].

U kunt een lijst van afgewezen personen ook tot stand brengen die gastheren (domeinen) specificeert dan geen [!DNL Target] verzoeken naar kan verzenden [!DNL Target] door de gewenste gastheren in de [!UICONTROL Host Does Not Contain] doos toe te voegen.

>[!NOTE]
>
>Omdat de lijst met geautoriseerde hosts wordt gebruikt voor zowel [!DNL Target] hosts als standaardhosts voor omleiding, moet u alle bestaande domeinen toevoegen die zijn goedgekeurd voor het gebruik van de [!DNL Adobe Target] Javascript SDK (at.js) *EN* alle domeinen die worden gebruikt in standaard URL&#39;s voor omleiding. U moet ook nieuwe, vergelijkbare domeinen toevoegen aan de lijst van gewenste personen in de toekomst.

## Een host verwijderen {#section_F56355BA4BC54B078A1A8179BC954632}

U kunt een host verwijderen wanneer deze niet meer nodig is.

1. Klik in de [!UICONTROL Hosts] lijst op het **[!UICONTROL Delete]** pictogram.
1. Klik **[!UICONTROL Delete]** om de verwijdering te bevestigen.

>[!NOTE]
>
>De host wordt opnieuw weergegeven als iemand naar een pagina bladert die een [!DNL Target] aanvraag op de host bevat.

## Problemen met hosts oplossen {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probeer de volgende tips voor het oplossen van problemen als u problemen ondervindt met uw hosts:

**De host wordt niet weergegeven in de lijst voor uw account.**

* Vernieuw de [!UICONTROL Hosts] pagina in uw browser.
* Bevestig dat het [!DNL Target] verzoek juist is, inclusief de verwijzing at.js of mbox.js.
* Blader naar een van de [!DNL Target] aanvragen op de host. Het is mogelijk dat geen [!DNL Target] verzoek op de gastheer ooit in browser werd teruggegeven.

**Willekeurige of onbekende domeinen worden in de[!UICONTROL Host]lijst weergegeven.**

Er wordt een domein in deze lijst weergegeven als er een aanvraag is ingediend vanuit het domein. [!DNL Target] Vaak kunt u domeinen zien van spintengines, vertaalsites of lokale schijfstations. Als het vermelde domein niet één uw teamgebruik is, kunt u klikken [!UICONTROL Delete] om het te verwijderen.

**Mijn[!DNL Target]verzoek retourneert /* geen weergave - ongeoorloofde mbox-host */.**

Als een [!DNL Target] verzoek wordt ingediend op een niet-geautoriseerde host, reageert het verzoek op /* geen weergave - niet-geautoriseerde mbox-host */.
