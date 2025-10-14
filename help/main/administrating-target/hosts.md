---
keywords: host;hosts;hostgroep;problemen oplossen;aanbevolen procedures;ubox;omleiding;omleiding;whitelist;lijst van gewenste personen;zwarte lijst;lijst van gewezen personen
description: Leer hoe u uw websites en pre-productieomgevingen kunt ordenen voor eenvoudig beheer en gescheiden rapportering in Adobe Target.
title: Wat zijn gastheren en hoe gebruik ik ze?
feature: Administration & Configuration
role: Admin
exl-id: 31c661c0-686d-440e-ad58-864fb853b1c4
source-git-commit: 0ab5b7d7cbfaef86b9a045883f597900dba72416
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 0%

---

# Gastheren

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage in [!DNL Adobe Target] .

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u ook rapportgegevens door [&#x200B; milieu &#x200B;](/help/main/administrating-target/environments.md) scheiden.

Een host is elk domein waaruit een [!DNL Target] -aanvraag wordt gedaan. Op een website is dit doorgaans de eigenschap `location.hostname` van de URL die de [!DNL Target] request uitvoert.

Standaard beperkt [!DNL Target] een host die [!DNL Target] aanvragen kan indienen en reacties kan ontvangen [!DNL Target] , niet. Wanneer nieuwe gastheren verzoeken indienen, werken zij automatisch. Dit proces laat ook het testen op verschillende domeinen toe u niet kent of niet kan voorzien. Als u dit standaardgedrag wilt met voeten treden, kunt u opstelling een lijst van gewenste personen of een lijst van gewezen personen om te beperken welke gastheren met [!DNL Target] werken.

{{permissions-update}}

Klik op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]** om hosts te beheren.

## Hosts herkennen {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Als u een host wilt herkennen en toevoegen aan de lijst [!UICONTROL Hosts] , moet aan de volgende voorwaarden zijn voldaan:

* Er moet minstens één [!DNL Target] -aanvraag op de host aanwezig zijn
* Een pagina op de host moet het volgende bevatten:

   * Een nauwkeurige verwijzing naar at.js
   * Een [!DNL Target] -aanvraag of een automatisch gegenereerde algemene [!DNL Target] -aanvraag

* De pagina met de aanvraag [!DNL Target] moet in een browser worden weergegeven

Nadat de pagina is weergegeven, wordt de host vermeld in de lijst van [!UICONTROL Hosts] , zodat u deze in een omgeving kunt beheren en activiteiten en tests kunt voorvertonen en starten.

>[!NOTE]
>
>Dit geldt ook voor persoonlijke ontwikkelservers.

Nadat een host aan de lijst van [!UICONTROL Host] is toegevoegd, controleert u of de host wordt herkend.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Hosts]** .
1. Vernieuw de browser als uw host niet in de lijst staat.

   Standaard wordt een nieuw herkende host in de [!UICONTROL Production] -omgeving geplaatst. De [!UICONTROL Production] -omgeving is de veiligste omgeving omdat inactieve activiteiten niet van deze hosts kunnen worden bekeken.

1. (Voorwaardelijk) klik het **[!UICONTROL Move]** pictogram ( ![&#x200B; bewegingspictogram &#x200B;](/help/main/assets/icons/MoveTo.svg)) om de gastheer in [!UICONTROL Development], [!UICONTROL Staging], of ander milieu te bewegen.

>[!NOTE]
>
>De [!UICONTROL Production] -omgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. Men veronderstelt dat dit milieu is waar u definitieve, actieve activiteiten en tests dient. De standaardomgeving staat niet toe dat inactieve campagnes worden weergegeven.

## De lijst met gastheren sorteren of doorzoeken {#section_068B23C9D8224EB78BC3B7C8580251B0}

Als u de lijst [!UICONTROL Hosts] wilt sorteren, klikt u op een kolomkop ( [!UICONTROL Name] , [!UICONTROL Environment] of [!UICONTROL Last Requested] ) om de lijst in oplopende of aflopende volgorde te sorteren.

Als u in de lijst [!UICONTROL Hosts] wilt zoeken, typt u een zoekterm in het vak [!UICONTROL Search Hosts] .

## Maak lijsten van gewenste personen die hosts opgeven die [!DNL Target] -aanvragen mogen verzenden naar [!DNL Target] . {#allowlist}

U kunt een lijst van gewenste personen maken die hosts (domeinen) opgeeft die [!DNL Target] -aanvragen mogen verzenden naar [!DNL Target] . Alle andere gastheren die verzoeken produceren krijgen een commentaar-uit reactie van de vergunningsfout. Standaard registreert elke host die een [!DNL Target] -aanvraag bevat, zich bij [!DNL Target] in de [!UICONTROL Production] -omgeving en heeft deze toegang tot alle actieve en goedgekeurde activiteiten. Als u deze methode niet wilt gebruiken, kunt u in plaats daarvan de lijst van gewenste personen gebruiken om specifieke hosts op te nemen die in aanmerking komen voor het indienen van [!DNL Target] -aanvragen en het ontvangen van [!DNL Target] -inhoud. Alle gastheren blijven in de [!UICONTROL Hosts] lijst tonen, en de milieu&#39;s kunnen nog worden gebruikt om deze gastheren te groeperen en verschillende niveaus aan elk toe te wijzen, zoals of de gastheer actieve en/of inactieve activiteiten kan zien.

Een lijst van gewenste personen maken:

1. Klik in de lijst [!UICONTROL Hosts] op **[!UICONTROL Authorize Hosts]** .
1. Schakel de **[!UICONTROL Enable Authorized Hosts for content delivery]** -schakeloptie in.
1. Voeg naar wens de gewenste hosts toe in het vak **[!UICONTROL Host contains]** .

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Voeg naar wens de gewenste hosts toe in het vak **[!UICONTROL Host does not contains]** .

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Klik op **[!UICONTROL Save]**.

Als een [!DNL Target] -aanvraag wordt ingediend op een niet-geautoriseerde host, reageert de aanroep op `/* no display - unauthorized mbox host */` .

>[!IMPORTANT]
>
>**beste praktijken van de Veiligheid**: Als u ubox functionaliteit van [!DNL Target] gebruikt, controleert deze lijst van gewenste personen ook de lijst van domeinen waaraan uw [&#x200B; redirector &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/implement-email/working-with-redirectors.html?lang=nl-NL){target=_blank} kan navigeren. Zorg ervoor dat u alle domeinen toevoegt waarnaar u wilt omleiden wanneer u ubox als onderdeel van uw implementatie gebruikt. Als de lijst van gewenste personen niet is opgegeven, kan [!DNL Adobe] de omleidings-URL&#39;s niet controleren en beschermen tegen mogelijke kwaadwillige omleidingen.
>
>De lijst van gewenste personen heeft voorrang op omgevingen. Wis uit alle gastheren alvorens de eigenschap van de lijst van gewenste personen te gebruiken, dan slechts verschijnen de gastheren die door de lijst van gewenste personen worden toegestaan in uw gastheerlijst. Vervolgens kunt u de hosts naar de gewenste omgeving verplaatsen.

Soms verschijnen domeinen van andere plaatsen in uw milieu&#39;s. Een domein verschijnt in de lijst als het domein at.js roept. Als iemand bijvoorbeeld een van uw webpagina&#39;s naar de server kopieert, wordt dat domein in uw omgeving weergegeven. U ziet wellicht ook domeinen van spintengines, vertaalsites of lokale schijfstations.

Wanneer `mboxHost` wordt doorgegeven in een API-aanroep, wordt de conversie opgenomen voor de omgeving die wordt doorgegeven. Als geen milieu wordt overgegaan, blijft de gastheer in de vraag aan [!UICONTROL Production] in gebreke.

U kunt ook een lijst van gewezen personen maken die hosts (domeinen) opgeeft die [!DNL Target] -aanvragen niet naar [!DNL Target] kunnen verzenden door de gewenste hosts toe te voegen in het vak [!UICONTROL Host Does Not Contain] .

>[!NOTE]
>
>De lijst [!UICONTROL Authorized Hosts] wordt gebruikt voor zowel [!DNL Target] -hosts als standaardhosts voor omleiding. Voeg alle bestaande domeinen toe die worden goedgekeurd om [!DNL Adobe Target] JavaScript SDK (at.js) *EN* te gebruiken alle domeinen die in ubox standaard worden gebruikt opnieuw richt URLs. Voeg nieuwe gelijkaardige domeinen aan de lijst van gewenste personen in de toekomst toe.

## Een host verwijderen {#section_F56355BA4BC54B078A1A8179BC954632}

U kunt een host verwijderen als deze niet meer nodig is.

1. Van de [!UICONTROL Hosts] lijst, klik het **[!UICONTROL Delete]** pictogram ( ![&#x200B; pictogram van de Schrapping &#x200B;](/help/main/assets/icons/DeleteOutline.svg)).
1. Klik op **[!UICONTROL Delete]** om het verwijderen te bevestigen.

>[!NOTE]
>
>De gastheer wordt opnieuw vermeld als iemand naar een pagina bladert die een [!DNL Target] verzoek op de gastheer bevat.

## Problemen met hosts oplossen {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Probeer de volgende tips voor het oplossen van problemen als u problemen ondervindt met uw hosts:

**de Gastheer verschijnt niet in de lijst voor uw rekening.**

* Vernieuw de pagina [!UICONTROL Hosts] in uw browser.
* Controleer of de aanvraag [!DNL Target] correct is, inclusief de verwijzing at.js.
* Blader naar een van de [!DNL Target] -aanvragen op de host. Het is mogelijk dat geen [!DNL Target] aanvraag op de host ooit in een browser is weergegeven.

**Willekeurige of onbekende domeinen verschijnen in de [!UICONTROL Host] lijst.**

Er wordt een domein in deze lijst weergegeven als er een aanvraag naar [!DNL Target] wordt gedaan vanuit het domein. Vaak kunt u domeinen zien van spintengines, vertaalsites of lokale schijfstations. Als het vermelde domein niet een domein is dat uw team gebruikt, kunt u op [!UICONTROL Delete] klikken om het te verwijderen.

**Mijn [!DNL Target] verzoekwinst /&#42; geen vertoning - onbevoegde mbox gastheer &#42;/.**

Als een [!DNL Target] -aanvraag wordt ingediend op een niet-geautoriseerde host, reageert de aanvraag met /&#42; geen weergave - niet-geautoriseerde mbox-host &#42;/.
