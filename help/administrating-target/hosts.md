---
keywords: host;hosts;host group;environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist
description: Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.
title: Gastheren
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: 81d6ce3e9c83fb4cce26644b45321e7492392bea
workflow-type: tm+mt
source-wordcount: '1741'
ht-degree: 0%

---


# Gastheren{#hosts}

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u rapportgegevens door milieu ook scheiden.

Een host is een willekeurige webserver (of een webdomein) van waaruit u inhoud tijdens een van de fasen van uw project kunt leveren. Elke host die een box bedient, wordt herkend.

Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. U hebt bijvoorbeeld tientallen hosts gegroepeerd in twee of drie omgevingen. De vooraf ingestelde omgevingen zijn onder andere Productie, Staging en Ontwikkeling. U kunt nieuwe omgevingen toevoegen en desgewenst de naam van uw omgeving wijzigen.

Één milieu, het gebrek, is pre-genoemde Productie. Deze standaardomgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. [!DNL Target] Hierbij gaat u ervan uit dat u de laatste, goedgekeurde activiteiten en tests zult uitvoeren.

Wanneer een mbox verzoek van nieuwe websites of domeinen wordt ontvangen, verschijnen deze nieuwe domeinen altijd in het milieu van de Productie. De instellingen van de productieomgeving kunnen niet worden gewijzigd. Onbekende of nieuwe sites kunnen alleen inhoud zien die actief en klaar is. Het beheer van de gastheer laat u ook gemakkelijk de kwaliteit van nieuwe activiteiten en inhoud in uw test, het opvoeren, en ontwikkelmilieu&#39;s verzekeren alvorens u de activiteiten activeert.

Het doel beperkt een host die dozen kan verzenden en ontvangen niet. Wanneer nieuwe servers of domeinen verschijnen, werken deze automatisch (tenzij u een whitelist of zwarte lijst hebt ingesteld). Dit laat ook toe en het testen op verschillende domeinen u niet kent of niet kan voorzien.

Als u hosts en omgevingen wilt beheren, klikt u op **[!UICONTROL Setup]** > **[!UICONTROL Hosts]**.

![](assets/hosts_list.png)

## Hosts herkennen {#concept_0D4B43E23AA9408F8B28A57ED754BF65}

Informatie over de voorwaarden waaraan moet worden voldaan om een gastheer te herkennen en toe te voegen aan de lijst met gastheren. [!DNL Target]

Om een gastheer te erkennen, moet aan de volgende voorwaarden worden voldaan:

* Er moet minstens één box op de host aanwezig zijn
* Een pagina op de host moet het volgende bevatten:

   * Een nauwkeurige [!DNL mbox.js] verwijzing
   * Een mbox of een automatisch gegenereerde globale mbox-aanroep

* De pagina met de mbox moet in een browser worden weergegeven

Nadat de pagina is weergegeven, wordt de host vermeld in de [!UICONTROL Hosts] lijst, zodat u deze in een omgeving kunt beheren en activiteiten en tests kunt voorvertonen en starten.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Dit geldt ook voor persoonlijke ontwikkelservers.

Nadat een gastheer aan de [!UICONTROL Host] lijst wordt toegevoegd, zorg ervoor dat de gastheer wordt erkend.

1. Klik op **[!UICONTROL Setup]** > **[!UICONTROL Hosts]**.
1. Vernieuw de browser als uw host niet in de lijst staat.
Standaard wordt een nieuw herkende host in de productieomgeving geplaatst. Dit is het veiligste milieu omdat het inactieve activiteiten niet om van deze gastheren toelaat worden bekeken.
1. (Voorwaardelijk) Beweeg de gastheer in de ontwikkelings of het Opvoeren milieu.

>[!NOTE]
>
>De productieomgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. Men gaat ervan uit dat u hier de laatste, actieve activiteiten en tests zult bedienen. De standaardomgeving staat niet toe dat inactieve campagnes worden weergegeven.

## Gastheren en omgevingen beheren {#concept_90573F5A52E04600A8C3C5897880C10F}

Informatie die u helpt gastheren en milieu&#39;s (gastheergroepen,) te beheren met inbegrip van het plaatsen van de standaardgastheer voor het melden, het creëren van whitelisten, het veranderen van de naam van een milieu, het bewegen van een gastheer aan een andere milieu, en het schrappen van een gastheer of een milieu.


Klik op [!UICONTROL Hosts] > om de **[!UICONTROL Setup]** **[!UICONTROL Hosts]** lijst te openen.

![](assets/hosts_list.png)

## De lijst Gastheren filteren, sorteren of doorzoeken {#section_068B23C9D8224EB78BC3B7C8580251B0}

Als u de [!UICONTROL Hosts] lijsten wilt filteren op omgeving, klikt u op de **[!UICONTROL All]** vervolgkeuzelijst en selecteert u de gewenste omgeving (Productie, Staging, Ontwikkeling of een aangepaste omgeving die u hebt gemaakt).

Als u de [!UICONTROL Hosts] lijst wilt sorteren, klikt u op een kolomkop (Naam, Omgeving of Laatst aangevraagd) om de lijst in oplopende of aflopende volgorde te sorteren.

Als u in de [!UICONTROL Hosts] lijst wilt zoeken, typt u een zoekterm in het vak Zoeken.

## Meerdere hosts selecteren {#section_EF3B458475184B7EA997C3559714397C}

Als u meerdere hosts wilt selecteren, schakelt u de selectievakjes naast de [!UICONTROL Name] kolom in voor de gewenste hosts. Vervolgens kunt u alle geselecteerde hosts verplaatsen of verwijderen.

## Een omgeving maken {#section_32097D0993724DF3A202D164D3F18674}

1. Klik in de [!UICONTROL Hosts] lijst op de **[!UICONTROL Environments]** tab.
1. Klik op **[!UICONTROL Create Environment]**.
1. Geef een beschrijvende naam voor de omgeving op.
1. Geef de gewenste actieve modus voor de omgeving op: [!UICONTROL Active Activities] of [!UICONTROL Active and Inactive Activities].
1. Klik op **[!UICONTROL Save]**.

## De standaardhost voor rapportage instellen {#section_4F8539B07C0C45E886E8525C344D5FB0}

U kunt de omgeving selecteren die u als standaard wilt gebruiken voor alle activiteitenrapporten.

Als u Productie als uw gebrek gebruikt, worden alle onbekende gastheren automatisch toegevoegd hier en rapportgegevens van daar zijn inbegrepen in de standaardrapportmening. In plaats daarvan zorgt het creëren van een &quot;schone&quot;milieu ervoor slechts uw kernplaatsen/domeinen inbegrepen zijn.

De standaardomgeving voor rapportage instellen:

1. Klik in de [!UICONTROL Hosts] lijst op de **[!UICONTROL Settings]** tab.
1. Selecteer de standaardhost in de **[!UICONTROL Environment Settings]** vervolgkeuzelijst.
1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>[!DNL Recommendations] gebruikers moeten hun gedragsgegevensbestand en productgegevensbestand opnieuw opbouwen als de gastheren gastheergroepen schakelen.

## Creeer whitelists die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel te verzenden. {#whitelist}

U kunt een whitelist creëren die gastheren (domeinen) specificeert die worden gemachtigd om mbox vraag naar te verzenden [!DNL Target]. Alle andere gastheren die vraag produceren zullen een commentarieert-uit de foutenreactie van de toestemmingsfout krijgen. Door gebrek, om het even welke gastheer die een mbox vraagregisters met [!DNL Target] in het milieu van de Productie bevat en toegang tot alle actieve en goedgekeurde activiteiten heeft. Als dit niet de gewenste benadering is, kunt u whitelist in plaats daarvan gebruiken om specifieke gastheren te registreren die verkiesbaar zijn om mbox vraag te maken en [!DNL Target] inhoud te ontvangen. Alle gastheren zullen in de [!UICONTROL Hosts] lijst blijven tonen, en de milieu&#39;s kunnen nog worden gebruikt om deze gastheren te groeperen en verschillende niveaus aan elk toe te wijzen, zoals of de gastheer actieve en/of inactieve campagnes kan zien.

Een whitelist maken:

1. Klik in de [!UICONTROL Hosts] lijst op de **[!UICONTROL Settings]** tab.
1. Schakel **[!UICONTROL Enable Authorized Hosts for Content Delivery]** het selectievakje in.
1. Voeg desgewenst de gewenste hosts in het **[!UICONTROL Host Contains]** vak toe.

   De veelvoudige gastheren kunnen, elk op zijn eigen lijn worden vermeld.

1. Klik op **[!UICONTROL Save]**.

Als een mbox vraag op een onbevoegde gastheer wordt gemaakt, zal de vraag met antwoorden `/* no display - unauthorized mbox host */`.

Als u ubox functionaliteit van gebruikt, merk op dat deze whitelist ook de lijst van domeinen zal controleren waaraan uw [!DNL Target]redirecteuren [](/help/c-implementing-target/c-non-javascript-based-implementation/working-with-redirectors.md) kunnen navigeren. Zorg ervoor dat u alle domeinen toevoegt waarnaar u wilt omleiden wanneer u ubox als onderdeel van uw implementatie gebruikt. Als de whitelist niet wordt opgegeven, kan Adobe de omleidings-URL&#39;s niet controleren en beschermen tegen mogelijke kwaadwillige omleidingen.

De whitelist heeft voorrang op omgevingen. U zou alle gastheren moeten ontruimen alvorens de whitelist eigenschap te gebruiken, dan slechts verschijnen de gastheren die door whitelist worden toegestaan in uw gastheerlijst. Vervolgens kunt u de hosts naar de gewenste omgeving verplaatsen.

Soms verschijnen domeinen van andere plaatsen in uw milieu&#39;s. Een domein verschijnt in de lijst als het domein een vraag aan uw mbox.js maakt. Als iemand bijvoorbeeld een van uw webpagina&#39;s naar de server kopieert, wordt dat domein in uw omgeving weergegeven. U ziet wellicht ook domeinen van spintengines, vertaalsites of lokale schijfstations.

Wanneer een API-aanroep `mboxHost` wordt doorgegeven, wordt de conversie opgenomen voor de omgeving die wordt doorgegeven. Als geen milieu wordt overgegaan, blijft de gastheer in de vraag aan Productie in gebreke.

U kunt ook een zwarte lijst maken die hosts (domeinen) opgeeft dan geen aanroepen vanuit een box kan verzenden [!DNL Target] door de gewenste hosts in het [!UICONTROL Host Does Not Contain] vak toe te voegen.

## De naam van een omgeving wijzigen {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klik in de [!UICONTROL Hosts] lijst op de **[!UICONTROL Environments]** tab.
1. Houd de cursor boven de gewenste omgeving en klik op het **[!UICONTROL Edit]** pictogram.
1. Wijzig de naam van de omgeving.
1. Klik op **[!UICONTROL Save]**.

## Een host verplaatsen naar een andere omgeving {#section_9F52549958BD485EB74FE78C32773D2A}

1. Houd de muisaanwijzer in de [!UICONTROL Hosts] lijst boven de gewenste host.
1. Klik op het **[!UICONTROL Move]** pictogram.
1. Selecteer de gewenste omgeving in de vervolgkeuzelijst en klik op het pictogram van het vinkje.

## Een host verwijderen {#section_F56355BA4BC54B078A1A8179BC954632}

U kunt een host verwijderen als deze niet meer nodig is.

1. Houd de muisaanwijzer in de [!UICONTROL Hosts] lijst boven de host die u wilt verwijderen.
1. Klik op het **[!UICONTROL Delete]** pictogram.
1. Klik **[!UICONTROL Delete]** om de verwijdering te bevestigen.

>[!NOTE]
>
>De host wordt opnieuw weergegeven als iemand naar een pagina met een maffout op de host bladert.

## Een omgeving verwijderen {#section_737F8869612047868D03FC755B1223D3}

U kunt een omgeving verwijderen wanneer deze niet meer nodig is.

1. Klik in de [!UICONTROL Hosts] lijst op de **[!UICONTROL Environments]** tab.
1. Houd de muis boven de omgeving die u wilt verwijderen.
1. Klik op het **[!UICONTROL Delete]** pictogram.
1. Klik **[!UICONTROL Delete]** om de verwijdering te bevestigen.

>[!NOTE]
>
>U kunt de productieomgeving niet verwijderen, maar u kunt de naam ervan wel wijzigen.

## Problemen met hosts oplossen {#concept_B3D7583FA4BB480382CC7453529FE1B7}

Aanbevolen procedures voor het beheren en oplossen van problemen van hosts in [!DNL Adobe Target].

Probeer de volgende tips voor het oplossen van problemen als u problemen ondervindt met uw hosts:

**De host wordt niet weergegeven in de keuzelijst voor uw account.**

* Vernieuw de [!UICONTROL Hosts] pagina in uw browser.
* Bevestig dat de code van het selectievakje correct is, inclusief de [!DNL mbox.js] verwijzing.
* Blader naar een van de vakken op de host. Het is mogelijk dat geen mbox op de gastheer ooit in browser werd teruggegeven.

**Willekeurige of onbekende domeinen worden in de[!UICONTROL Host]lijst weergegeven.**

Een domein verschijnt in deze lijst als een vraag aan van het domein [!DNL Target] wordt gemaakt. Vaak kunt u domeinen zien van spintengines, vertaalsites of lokale schijfstations. Als het vermelde domein niet één uw teamgebruik is, kunt u klikken [!UICONTROL Delete] om het te verwijderen.

**Mijn mbox-aanroep retourneert /* geen weergave - onbevoegde mbox-host */.**

Als een mbox vraag op een onbevoegde gastheer wordt gemaakt, zal de vraag met /* geen vertoning - onbevoegde mbox gastheer */ antwoorden.

## Aanbevelingen: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep)

![Premium badge](/help/assets/premium.png)

U kunt de inhoud van de inzamelingen en de uitsluitingen van Aanbevelingen voor een geselecteerde milieu (gastheergroep) voorproef.

>[!NOTE]
>De activiteiten van aanbevelingen zijn beschikbaar als deel van de oplossing van de Premie van het Doel. Ze zijn niet beschikbaar in Target Standard zonder een Target Premium-licentie.

U kunt de hostgroep gebruiken om de beschikbare items in uw catalogus te scheiden voor verschillende toepassingen. U kunt bijvoorbeeld hostgroepen gebruiken voor ontwikkelings- en productieomgevingen, verschillende merken of verschillende geografische locaties. Standaard zijn de voorvertoningsresultaten in Cataloguszoekopdrachten, Verzamelingen en Uitsluitingen gebaseerd op de standaardhostgroep. (U kunt ook een andere hostgroep selecteren om een voorvertoning van de resultaten weer te geven met behulp van het filter Omgeving.) Nieuwe toegevoegde items zijn standaard beschikbaar in alle hostgroepen, tenzij een milieu-id is opgegeven bij het maken of bijwerken van het item. De geleverde aanbevelingen hangen van de gastheergroep af die in het verzoek wordt gespecificeerd.

Als u uw producten niet ziet, zorg ervoor dat u de correcte gastheergroep gebruikt. Bijvoorbeeld, als u opstelling uw aanbeveling om een het opvoeren milieu te gebruiken en u uw gastheergroep aan het Opvoeren plaatst, zou u uw inzamelingen in het opvoeren milieu voor de te tonen producten kunnen moeten opnieuw creëren. Om te zien welke producten in elke milieu beschikbaar zijn, gebruik CatalogusOnderzoek met elke milieu. U kunt ook een voorvertoning weergeven van de inhoud van verzamelingen en uitsluitingen met aanbevelingen voor een geselecteerde omgeving (hostgroep).

>[!NOTE]
>Nadat u de geselecteerde omgeving hebt gewijzigd, moet u op Zoeken klikken om de geretourneerde resultaten bij te werken.

Het filter Omgeving is beschikbaar op de volgende plaatsen in de interface van het Doel:

* Catalogus zoeken ([!UICONTROL Recommendations > Catalog Search])
* Verzameling maken, dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])
* Dialoogvenster Verzameling bijwerken ([!UICONTROL Recommendations > Collections > Edit])
* Dialoogvenster Uitsluiting maken ([!UICONTROL Recommendations > Exclusions > Create New])
* Dialoogvenster Uitsluiting bijwerken ([!UICONTROL Recommendations > Exclusions > Edit])
