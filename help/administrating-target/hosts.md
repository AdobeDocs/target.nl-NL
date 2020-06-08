---
keywords: host;hosts;host group;troubleshooting;best practices;ubox;redirects;redirect;whitelist;allowlist;blacklist;blocklist
description: Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.
title: Gastheren
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: cf69c1d8472088d5f6a6b7250bedd1048cac5c10
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 0%

---


# Gastheren{#hosts}

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u rapportgegevens door [milieu](/help/administrating-target/environments.md)ook scheiden.

Een host is een willekeurige webserver (of een webdomein) van waaruit u inhoud tijdens een van de fasen van uw project kunt leveren. Elke host die een box bedient, wordt herkend.

Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. U hebt bijvoorbeeld tientallen hosts gegroepeerd in twee of drie omgevingen. De vooraf ingestelde omgevingen omvatten [!UICONTROL Production], [!UICONTROL Staging]en [!UICONTROL Development]. U kunt nieuwe omgevingen toevoegen en desgewenst de naam van uw omgeving wijzigen.

Eén omgeving, de standaardomgeving, heeft een voornaam [!UICONTROL Production]. Deze standaardomgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. [!DNL Target] Hierbij gaat u ervan uit dat u de laatste, goedgekeurde activiteiten en tests zult uitvoeren.

Wanneer een mbox verzoek van nieuwe websites of domeinen wordt ontvangen, verschijnen deze nieuwe domeinen altijd in het [!UICONTROL Production] milieu. De instellingen van de [!UICONTROL Production] omgeving kunnen niet worden gewijzigd. Onbekende of nieuwe sites kunnen alleen inhoud zien die actief en gereed is. Het beheer van de gastheer laat u ook gemakkelijk de kwaliteit van nieuwe activiteiten en inhoud in uw test, het opvoeren, en ontwikkelmilieu&#39;s verzekeren alvorens u de activiteiten activeert.

[!DNL Target] beperkt een gastheer niet die dozen kan verzenden en ontvangen, zodat wanneer de nieuwe servers of domeinen verschijnen, werken zij automatisch (tenzij u opstelling een allowlist of blocklist). Dit laat ook toe en het testen op verschillende domeinen u niet kent of niet kan voorzien.

Als u hosts wilt beheren, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Hosts herkennen {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Als u een host wilt herkennen en toevoegen aan de [!UICONTROL Hosts] lijst, moet aan de volgende voorwaarden zijn voldaan:

* Er moet minstens één box op de host aanwezig zijn
* Een pagina op de host moet het volgende bevatten:

   * Een nauwkeurige verwijzing van at.js of mbox.js
   * Een mbox of een automatisch gegenereerde globale mbox-aanroep

* De pagina met de mbox moet in een browser worden weergegeven

Nadat de pagina is weergegeven, wordt de host vermeld in de [!UICONTROL Hosts] lijst, zodat u deze in een omgeving kunt beheren en activiteiten en tests kunt voorvertonen en starten.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Dit geldt ook voor persoonlijke ontwikkelservers.

Nadat een gastheer aan de [!UICONTROL Host] lijst wordt toegevoegd, zorg ervoor dat de gastheer wordt erkend.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]**.
1. Vernieuw de browser als uw host niet in de lijst staat.

   Standaard wordt een nieuw herkende host in de [!UICONTROL Production] omgeving geplaatst. Dit is het veiligste milieu omdat het inactieve activiteiten niet om van deze gastheren toelaat worden bekeken.

1. (Voorwaardelijk) klik het pictogram van de Beweging ( ![bewegingspictogram](/help/administrating-target/assets/icon-move.png) ) om de gastheer in het [!UICONTROL Development], [!UICONTROL Staging], of andere milieu te bewegen.

>[!NOTE]
>
>De [!UICONTROL Production] omgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. Men gaat ervan uit dat u hier de laatste, actieve activiteiten en tests zult bedienen. De standaardomgeving staat niet toe dat inactieve campagnes worden weergegeven.

## De lijst met gastheren sorteren of doorzoeken {#section_068B23C9D8224EB78BC3B7C8580251B0}

Als u de [!UICONTROL Hosts] lijst wilt sorteren, klikt u op een kolomkop ([!UICONTROL Name], [!UICONTROL Environment]of [!UICONTROL Last Requested]) om de lijst in oplopende of aflopende volgorde te sorteren.

Als u in de [!UICONTROL Hosts] lijst wilt zoeken, typt u een zoekterm in het [!UICONTROL Search Hosts] vak.

## Creeer allowlists die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel te verzenden. {#whitelist}

U kunt een allowlist tot stand brengen die gastheren (domeinen) specificeert die worden gemachtigd om mbox vraag naar te verzenden [!DNL Target]. Alle andere gastheren die vraag produceren zullen een commentarieert-uit de foutenreactie van de toestemmingsfout krijgen. Door gebrek, om het even welke gastheer die een mbox vraagregisters met [!DNL Target] in het milieu van de Productie bevat en toegang tot alle actieve en goedgekeurde activiteiten heeft. Als dit niet de gewenste benadering is, kunt u in plaats daarvan het allowlist gebruiken om specifieke gastheren te registreren die verkiesbaar zijn om mbox vraag te maken en [!DNL Target] inhoud te ontvangen. Alle gastheren zullen in de [!UICONTROL Hosts] lijst blijven tonen, en de milieu&#39;s kunnen nog worden gebruikt om deze gastheren te groeperen en verschillende niveaus aan elk toe te wijzen, zoals of de gastheer actieve en/of inactieve campagnes kan zien.

Een allowlist maken:

1. From the [!UICONTROL Hosts] list, click **[!UICONTROL Authorize Hosts]**.
1. Schakel de **[!UICONTROL Enable Authorized Hosts for content delivery]** schakeloptie in.
1. Voeg desgewenst de gewenste hosts in het **[!UICONTROL Host contains]** vak toe.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Voeg desgewenst de gewenste hosts in het **[!UICONTROL Host does not contains]** vak toe.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Klik op **[!UICONTROL Save]**.

Als een mbox vraag op een onbevoegde gastheer wordt gemaakt, zal de vraag met antwoorden `/* no display - unauthorized mbox host */`.

>[!IMPORTANT]
>
>**Aanbevolen werkwijzen** voor beveiliging: Als u ubox functionaliteit van gebruikt [!DNL Target], merk op dat deze allowlist ook de lijst van domeinen zal controleren waaraan uw [redirecteuren](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) kunnen navigeren. Zorg ervoor dat u alle domeinen toevoegt waarnaar u wilt omleiden wanneer u ubox als onderdeel van uw implementatie gebruikt. Als de allowlist niet is opgegeven, kan Adobe de omleiding van URL&#39;s niet controleren en beschermen tegen mogelijke kwaadaardige omleidingen.
>
>De allowlist heeft voorrang op omgevingen. U zou alle gastheren moeten ontruimen alvorens de allowlist eigenschap te gebruiken, dan verschijnen slechts de gastheren die door de allowlist worden toegestaan in uw gastheerlijst. Vervolgens kunt u de hosts naar de gewenste omgeving verplaatsen.

Soms verschijnen domeinen van andere plaatsen in uw milieu&#39;s. Een domein verschijnt in de lijst als het domein een vraag aan uw at.js of mbox.js maakt. Als iemand bijvoorbeeld een van uw webpagina&#39;s naar de server kopieert, wordt dat domein in uw omgeving weergegeven. U ziet wellicht ook domeinen van spintengines, vertaalsites of lokale schijfstations.

Wanneer een API-aanroep `mboxHost` wordt doorgegeven, wordt de conversie opgenomen voor de omgeving die wordt doorgegeven. Als geen milieu wordt overgegaan, blijft de gastheer in de vraag aan [!UICONTROL Production].

U kunt ook een zwarte lijst maken die hosts (domeinen) opgeeft dan geen aanroepen vanuit een box kan verzenden [!DNL Target] door de gewenste hosts in het [!UICONTROL Host Does Not Contain] vak toe te voegen.

>[!NOTE]
>
>Omdat de lijst met geautoriseerde hosts wordt gebruikt voor zowel mbox-hosts als standaard omleidingshosts, moet u alle bestaande domeinen toevoegen die zijn goedgekeurd voor het gebruik van de Adobe Target Javascript SDK (at.js) *EN* alle domeinen die worden gebruikt in standaardomleidingsURL&#39;s. U moet ook in de toekomst eventuele nieuwe, vergelijkbare domeinen aan de allowlist toevoegen.

## Een host verwijderen {#section_F56355BA4BC54B078A1A8179BC954632}

U kunt een host verwijderen als deze niet meer nodig is.

1. Klik in de [!UICONTROL Hosts] lijst op het **[!UICONTROL Delete]** pictogram.
1. Klik **[!UICONTROL Delete]** om de verwijdering te bevestigen.

>[!NOTE]
>
>De host wordt opnieuw weergegeven als iemand naar een pagina met een maffout op de host bladert.

## Problemen met hosts oplossen {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Aanbevolen procedures voor het beheren en oplossen van problemen van hosts in [!DNL Adobe Target].

Probeer de volgende tips voor het oplossen van problemen als u problemen ondervindt met uw hosts:

**De host wordt niet weergegeven in de keuzelijst voor uw account.**

* Vernieuw de [!UICONTROL Hosts] pagina in uw browser.
* Controleer of de code van het vak correct is, inclusief de verwijzing at.js of mbox.js.
* Blader naar een van de vakken op de host. Het is mogelijk dat geen mbox op de gastheer ooit in browser werd teruggegeven.

**Willekeurige of onbekende domeinen worden in de[!UICONTROL Host]lijst weergegeven.**

Een domein verschijnt in deze lijst als een vraag aan van het domein [!DNL Target] wordt gemaakt. Vaak kunt u domeinen zien van spintengines, vertaalsites of lokale schijfstations. Als het vermelde domein niet één uw teamgebruik is, kunt u klikken [!UICONTROL Delete] om het te verwijderen.

**Mijn mbox-aanroep retourneert /* geen weergave - onbevoegde mbox-host */.**

Als een mbox vraag op een onbevoegde gastheer wordt gemaakt, zal de vraag met /* geen vertoning - onbevoegde mbox gastheer */ antwoorden.
