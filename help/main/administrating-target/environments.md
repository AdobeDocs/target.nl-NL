---
keywords: omgeving;problemen oplossen;aanbevolen procedures;ubox;omleiding;omleiding;whitelist;blacklist;lijst van gewezen personen;lijst van gewenste personen
description: Leer hoe u omgevingen in Adobe kunt gebruiken [!DNL Target] om uw sites en pre-productieomgevingen te organiseren voor eenvoudig beheer en gescheiden rapportering.
title: Wat zijn omgevingen en hoe gebruik ik deze?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Omgevingen

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.

Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. U hebt bijvoorbeeld tientallen hosts gegroepeerd in twee of drie omgevingen. De vooraf ingestelde omgevingen omvatten: [!UICONTROL Production], [!UICONTROL Staging], en [!UICONTROL Development]. U kunt nieuwe omgevingen toevoegen en desgewenst de naam van uw omgeving wijzigen.

Eén omgeving, de standaardomgeving, heeft een voornaam [!UICONTROL Production]. Deze standaardomgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. [!DNL Target] Hierbij gaat u ervan uit dat u de laatste, goedgekeurde activiteiten en tests zult uitvoeren.

Wanneer een [!DNL Target] verzoek wordt ontvangen van nieuwe websites of domeinen, verschijnen deze nieuwe domeinen altijd in [!UICONTROL Production] milieu. De [!UICONTROL Production] de instellingen van de omgeving kunnen niet worden gewijzigd, zodat onbekende of nieuwe sites gegarandeerd alleen inhoud zien die actief en gereed is. Het beheer van de gastheer laat u ook gemakkelijk de kwaliteit van nieuwe activiteiten en inhoud in uw test, het opvoeren, en ontwikkelmilieu&#39;s verzekeren alvorens u de activiteiten activeert.

Als u omgevingen wilt beheren, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Environments]**.

![Lijst met omgevingen](/help/main/administrating-target/assets/environments.png)

## Een omgeving toevoegen {#section_32097D0993724DF3A202D164D3F18674}

1. Van de [!UICONTROL Environments] lijst, klikt u op **[!UICONTROL Add Environment]**.
1. Geef een beschrijvende naam voor de omgeving op.
1. Geef de gewenste actieve modus voor de omgeving op: [!UICONTROL Active Activities] of [!UICONTROL Active and Inactive Activities].

   Als u [!UICONTROL Active and Inactive Activities], tonen de gastheren van deze milieu ook inactieve activiteiten.

1. Klik op **[!UICONTROL Save]**.

## De standaardomgeving voor rapportage instellen {#section_4F8539B07C0C45E886E8525C344D5FB0}

U kunt de omgeving selecteren die u als standaard wilt gebruiken voor alle activiteitenrapporten.

Als u [!UICONTROL Production] als uw gebrek, worden alle onbekende gastheren automatisch toegevoegd hier en rapportgegevens van daar zijn inbegrepen in de standaardrapportmening. In plaats daarvan zorgt het creëren van een &quot;schone&quot;milieu ervoor slechts uw kernplaatsen/domeinen inbegrepen zijn.

De standaardomgeving voor rapportage instellen:

1. Van de [!UICONTROL Environments] lijst, klik het pictogram van de Ster

>[!NOTE]
>
>[!DNL Recommendations] gebruikers moeten hun gedragsgegevensbestand en productgegevensbestand opnieuw opbouwen als de gastheren gastheergroepen schakelen.

## De naam van een omgeving wijzigen {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Van de [!UICONTROL Environment] lijst, klikt u op de knop **[!UICONTROL Edit]** pictogram.
1. Wijzig de naam van de omgeving.
1. Klik op **[!UICONTROL Save]**.

## Een omgeving verwijderen {#section_737F8869612047868D03FC755B1223D3}

U kunt een omgeving verwijderen wanneer deze niet meer nodig is.

1. Van de [!UICONTROL Environment] lijst, klikt u op de knop **[!UICONTROL Delete]** pictogram.
1. Klikken **[!UICONTROL Delete]** om de schrapping te bevestigen.

>[!NOTE]
>
>U kunt de [!UICONTROL Production] , maar u kunt de naam ervan wijzigen.

## Recommendations: filterverzamelingen en -uitsluitingen naar omgeving (hostgroep)

![Premium badge](/help/main/assets/premium.png)

U kunt een voorvertoning weergeven van de inhoud van Recommendations-verzamelingen en -uitsluitingen voor een geselecteerde omgeving (hostgroep).

{{premium-note}}

U kunt een omgeving gebruiken om de beschikbare items in uw catalogus te scheiden voor verschillende toepassingen. U kunt bijvoorbeeld hostgroepen gebruiken voor [!UICONTROL Development] en [!UICONTROL Production] omgevingen, verschillende merken of verschillende geografische locaties. Standaard zijn de voorvertoningsresultaten in Cataloguszoekopdrachten, Verzamelingen en Uitsluitingen gebaseerd op de standaardhostgroep. (U kunt ook een andere hostgroep selecteren om een voorvertoning van de resultaten weer te geven met behulp van het filter Omgeving.) Nieuwe toegevoegde items zijn standaard beschikbaar in alle hostgroepen, tenzij een milieu-id is opgegeven bij het maken of bijwerken van het item.

>[!NOTE]
>
>De geleverde aanbevelingen hangen van de gastheergroep of milieu-id af die in het verzoek wordt gespecificeerd.


Als u uw producten niet ziet, zorg ervoor dat u de correcte gastheergroep gebruikt. Bijvoorbeeld, als u opstelling uw aanbeveling om een het opvoeren milieu te gebruiken en u uw gastheergroep aan het Opvoeren plaatst, zou u uw inzamelingen in het opvoeren milieu voor de te tonen producten kunnen moeten opnieuw creëren. Om te zien welke producten in elke milieu beschikbaar zijn, gebruik CatalogusOnderzoek met elke milieu. U kunt ook een voorvertoning weergeven van de inhoud van Recommendations-verzamelingen en -uitsluitingen voor een geselecteerde omgeving (hostgroep).

>[!NOTE]
>Nadat u de geselecteerde omgeving hebt gewijzigd, moet u op Zoeken klikken om de geretourneerde resultaten bij te werken.

De [!UICONTROL Environment] is beschikbaar op de volgende plaatsen in het Doel UI:

* Catalogus zoeken ([!UICONTROL Recommendations > Catalog Search])
* Verzameling maken, dialoogvenster ([!UICONTROL Recommendations > Collections > Create New])
* Dialoogvenster Verzameling bijwerken ([!UICONTROL Recommendations > Collections > Edit])
* Dialoogvenster Uitsluiting maken ([!UICONTROL Recommendations > Exclusions > Create New])
* Dialoogvenster Uitsluiting bijwerken ([!UICONTROL Recommendations > Exclusions > Edit])
