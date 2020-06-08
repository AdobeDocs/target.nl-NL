---
keywords: environment;troubleshooting;best practices;ubox;redirects;redirect;whitelist;blacklist;blocklist;allowlist
description: Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.
title: Omgevingen
topic: Standard
uuid: c7682269-4ec2-4a0f-b053-7e0ec77f4604
translation-type: tm+mt
source-git-commit: cf69c1d8472088d5f6a6b7250bedd1048cac5c10
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# Omgevingen

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.

Het primaire doel van hostbeheer is ervoor te zorgen dat er niet per ongeluk inactieve inhoud op websites wordt weergegeven. Het beheer van de gastheer laat u rapportgegevens door milieu ook scheiden.

Een [gastheer](/help/administrating-target/hosts.md) is om het even welke Webserver (of Webdomein) van waar u inhoud tijdens om het even welk stadium van uw project dient. Elke host die een box bedient, wordt herkend.

Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. U hebt bijvoorbeeld tientallen hosts gegroepeerd in twee of drie omgevingen. De vooraf ingestelde omgevingen omvatten [!UICONTROL Production], [!UICONTROL Staging]en [!UICONTROL Development]. U kunt nieuwe omgevingen toevoegen en desgewenst de naam van uw omgeving wijzigen.

Eén omgeving, de standaardomgeving, heeft een voornaam [!UICONTROL Production]. Deze standaardomgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. [!DNL Target] Hierbij gaat u ervan uit dat u de laatste, goedgekeurde activiteiten en tests zult uitvoeren.

Wanneer een mbox verzoek van nieuwe websites of domeinen wordt ontvangen, verschijnen deze nieuwe domeinen altijd in het [!UICONTROL Production] milieu. De instellingen van de [!UICONTROL Production] omgeving kunnen niet worden gewijzigd. Onbekende of nieuwe sites kunnen alleen inhoud zien die actief en gereed is. Het beheer van de gastheer laat u ook gemakkelijk de kwaliteit van nieuwe activiteiten en inhoud in uw test, het opvoeren, en ontwikkelmilieu&#39;s verzekeren alvorens u de activiteiten activeert.

[!DNL Target] beperkt een gastheer niet die dozen kan verzenden en ontvangen, zodat wanneer de nieuwe servers of domeinen verschijnen, werken zij automatisch (tenzij u opstelling een allowlist of blocklist). Dit laat ook toe en het testen op verschillende domeinen u niet kent of niet kan voorzien.

Klik op **[!UICONTROL Administration]** > **[!UICONTROL Environments]**.

![Lijst met omgevingen](/help/administrating-target/assets/environments.png)

## Een omgeving toevoegen {#section_32097D0993724DF3A202D164D3F18674}

1. From the [!UICONTROL Environments] list, click **[!UICONTROL Add Environment]**.
1. Geef een beschrijvende naam voor de omgeving op.
1. Geef de gewenste actieve modus voor de omgeving op: [!UICONTROL Active Activities] of [!UICONTROL Active and Inactive Activities].
1. Klik op **[!UICONTROL Save]**.

## De standaardomgeving voor rapportage instellen {#section_4F8539B07C0C45E886E8525C344D5FB0}

U kunt de omgeving selecteren die u als standaard wilt gebruiken voor alle activiteitenrapporten.

Als u [!UICONTROL Production] als uw gebrek gebruikt, worden alle onbekende gastheren automatisch toegevoegd hier en rapportgegevens van daar zijn inbegrepen in de standaardrapportmening. In plaats daarvan zorgt het creëren van een &quot;schone&quot;milieu ervoor slechts uw kernplaatsen/domeinen inbegrepen zijn.

De standaardomgeving voor rapportage instellen:

1. Klik in de [!UICONTROL Environments] lijst op het pictogram Ster

>[!NOTE]
>
>[!DNL Recommendations] gebruikers moeten hun gedragsgegevensbestand en productgegevensbestand opnieuw opbouwen als de gastheren gastheergroepen schakelen.

## De naam van een omgeving wijzigen {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klik in de [!UICONTROL Environment] lijst op de **[!UICONTROL Environments]** tab.
1. Klik op het **[!UICONTROL Edit]** pictogram.
1. Wijzig de naam van de omgeving.
1. Klik op **[!UICONTROL Save]**.

## Een omgeving verwijderen {#section_737F8869612047868D03FC755B1223D3}

U kunt een omgeving verwijderen wanneer deze niet meer nodig is.

1. Klik in de [!UICONTROL Environment] lijst op het **[!UICONTROL Delete]** pictogram.
1. Klik **[!UICONTROL Delete]** om de verwijdering te bevestigen.

>[!NOTE]
>
>U kunt de [!UICONTROL Production] omgeving niet verwijderen, maar u kunt de naam ervan wel wijzigen.

## Aanbevelingen: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep)

![Premium badge](/help/assets/premium.png)

U kunt de inhoud van de inzamelingen en de uitsluitingen van Aanbevelingen voor een geselecteerde milieu (gastheergroep) voorproef.

>[!NOTE]
>De activiteiten van aanbevelingen zijn beschikbaar als deel van de oplossing van de [!DNL Target] Premie. Ze zijn niet beschikbaar in [!DNL Target] Standard zonder een [!DNL Target] Premium-licentie.

U kunt een omgeving gebruiken om de beschikbare items in uw catalogus te scheiden voor verschillende toepassingen. U kunt bijvoorbeeld hostgroepen gebruiken voor [!UICONTROL Development] en [!UICONTROL Production] omgevingen, verschillende merken of verschillende geografische gebieden. Standaard zijn de voorvertoningsresultaten in Cataloguszoekopdrachten, Verzamelingen en Uitsluitingen gebaseerd op de standaardhostgroep. (U kunt ook een andere hostgroep selecteren om een voorvertoning van de resultaten weer te geven met behulp van het filter Omgeving.) Nieuwe toegevoegde items zijn standaard beschikbaar in alle hostgroepen, tenzij een milieu-id is opgegeven bij het maken of bijwerken van het item. De geleverde aanbevelingen hangen van de gastheergroep af die in het verzoek wordt gespecificeerd.

Als u uw producten niet ziet, zorg ervoor dat u de correcte gastheergroep gebruikt. Bijvoorbeeld, als u opstelling uw aanbeveling om een het opvoeren milieu te gebruiken en u uw gastheergroep aan het Opvoeren plaatst, zou u uw inzamelingen in het opvoeren milieu voor de te tonen producten kunnen moeten opnieuw creëren. Om te zien welke producten in elke milieu beschikbaar zijn, gebruik CatalogusOnderzoek met elke milieu. U kunt ook een voorvertoning weergeven van de inhoud van verzamelingen en uitsluitingen met aanbevelingen voor een geselecteerde omgeving (hostgroep).

>[!NOTE]
>Nadat u de geselecteerde omgeving hebt gewijzigd, moet u op Zoeken klikken om de geretourneerde resultaten bij te werken.

Het [!UICONTROL Environment] filter is beschikbaar op de volgende plaatsen in het Doel UI:

* Catalogus zoeken ([!UICONTROL Recommendations > Catalog Search])
* Verzameling maken, dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])
* Dialoogvenster Verzameling bijwerken ([!UICONTROL Recommendations > Collections > Edit])
* Dialoogvenster Uitsluiting maken ([!UICONTROL Recommendations > Exclusions > Create New])
* Dialoogvenster Uitsluiting bijwerken ([!UICONTROL Recommendations > Exclusions > Edit])