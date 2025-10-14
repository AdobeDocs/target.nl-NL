---
keywords: omgeving;problemen oplossen;aanbevolen procedures;ubox;omleiding;omleiding;whitelist;blacklist;lijst van gewezen personen;lijst van gewenste personen
description: Leer hoe te om milieu's in Adobe  [!DNL Target]  te gebruiken om uw plaatsen en pre-productiemilieu's voor gemakkelijk beheer en gescheiden rapportering te organiseren.
title: Wat zijn omgevingen en hoe gebruik ik deze?
feature: Administration & Configuration
role: Admin
exl-id: 820a116a-15f9-4ba0-94f3-8e35aa0f90da
source-git-commit: 12831d6584acc482db415629d7e70a18e39c47c2
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# Omgevingen

Organiseer uw sites en pre-productieomgevingen voor eenvoudig beheer en gescheiden rapportage.

Gastheren worden gebundeld in omgevingen voor eenvoudig beheer. U hebt bijvoorbeeld tientallen hosts gegroepeerd in twee of drie omgevingen. De vooraf ingestelde omgevingen zijn [!UICONTROL Production] , [!UICONTROL Staging] en [!UICONTROL Development] . U kunt nieuwe omgevingen toevoegen en desgewenst de naam van uw omgeving wijzigen.

Eén omgeving, de standaardomgeving, heeft de voornaam [!UICONTROL Production] . Deze standaardomgeving kan niet worden verwijderd, zelfs niet als u de naam ervan wijzigt. [!DNL Target] gaat ervan uit dat u hier de uiteindelijke, goedgekeurde activiteiten en tests kunt uitvoeren.

Wanneer een [!DNL Target] -aanvraag wordt ontvangen van nieuwe websites of domeinen, worden deze nieuwe domeinen altijd weergegeven in de [!UICONTROL Production] -omgeving. De instellingen van de [!UICONTROL Production] -omgeving kunnen niet worden gewijzigd, zodat onbekende of nieuwe sites altijd alleen inhoud kunnen zien die actief en gereed is. Het beheer van de gastheer laat u ook gemakkelijk de kwaliteit van nieuwe activiteiten en inhoud in uw test, het opvoeren, en ontwikkelmilieu&#39;s verzekeren alvorens u de activiteiten activeert.

{{permissions-update}}

Klik op **[!UICONTROL Administration]** > **[!UICONTROL Environments]** om omgevingen te beheren.

## Een omgeving toevoegen {#section_32097D0993724DF3A202D164D3F18674}

1. Klik in de lijst [!UICONTROL Environments] op **[!UICONTROL Add Environment]** .
1. Geef een beschrijvende naam voor de omgeving op.
1. Geef de gewenste actieve modus voor de omgeving op: [!UICONTROL Active Activities] of [!UICONTROL Active and Inactive Activities] .

   Als u [!UICONTROL Active and Inactive Activities] opgeeft, geven hosts vanuit deze omgeving ook inactieve activiteiten weer.

1. Klik op **[!UICONTROL Save]**.

## De standaardomgeving voor rapportage instellen {#section_4F8539B07C0C45E886E8525C344D5FB0}

U kunt de omgeving selecteren die u als standaard wilt gebruiken voor alle activiteitenrapporten.

Als u [!UICONTROL Production] als uw gebrek gebruikt, worden alle onbekende gastheren automatisch toegevoegd hier en rapportgegevens van daar zijn inbegrepen in de standaardrapportmening. In plaats daarvan zorgt het creëren van een &quot;schone&quot;milieu ervoor slechts uw kernplaatsen/domeinen inbegrepen zijn.

De standaardomgeving voor rapportage instellen:

1. Klik in de lijst [!UICONTROL Environments] op het pictogram Ster

>[!NOTE]
>
>[!DNL Recommendations] -gebruikers moeten hun gedragsdatabase en productdatabase opnieuw opbouwen als hosts van hostgroepen veranderen.
>
>Als u a [&#x200B; standaardmilieu in a  [!DNL Adobe Experience Platform]  datastream &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=nl-NL#target){target=_blank} specificeert, treedt dit het plaatsen in [!DNL Target] met voeten.

## De naam van een omgeving wijzigen {#section_9F5F94285F8E495E9CE69810CE94CA08}

1. Klik in de lijst [!UICONTROL Environment] op het pictogram **[!UICONTROL Edit]** .
1. Wijzig de naam van de omgeving.
1. Klik op **[!UICONTROL Save]**.

## Een omgeving verwijderen {#section_737F8869612047868D03FC755B1223D3}

U kunt een omgeving verwijderen wanneer deze niet meer nodig is.

1. Klik in de lijst [!UICONTROL Environment] op het pictogram **[!UICONTROL Delete]** .
1. Klik op **[!UICONTROL Delete]** om het verwijderen te bevestigen.

>[!NOTE]
>
>U kunt de [!UICONTROL Production] -omgeving niet verwijderen, maar u kunt de naam ervan wel wijzigen.

## [!BADGE &#x200B; Premium &#x200B;]{type=Positive url="/help/main/c-intro/intro.md#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."} Aanbevelingen: de inzamelingen en de uitsluitingen van de filter door milieu (gastheergroep)

U kunt de inhoud van de inzamelingen en de uitsluitingen van Aanbevelingen voor een geselecteerde milieu (gastheergroep) voorproef.

{{premium-note}}

U kunt een omgeving gebruiken om de beschikbare items in uw catalogus te scheiden voor verschillende toepassingen. U kunt bijvoorbeeld hostgroepen gebruiken voor [!UICONTROL Development] - en [!UICONTROL Production] -omgevingen, verschillende merken of verschillende geografische locaties. Standaard zijn de voorvertoningsresultaten in Cataloguszoekopdrachten, Verzamelingen en Uitsluitingen gebaseerd op de standaardhostgroep. (U kunt ook een andere hostgroep selecteren om een voorvertoning van de resultaten weer te geven met behulp van het filter Omgeving.) Nieuwe toegevoegde items zijn standaard beschikbaar in alle hostgroepen, tenzij een milieu-id is opgegeven bij het maken of bijwerken van het item.

>[!NOTE]
>
>De geleverde aanbevelingen hangen van de gastheergroep of milieu-id af die in het verzoek wordt gespecificeerd.


Als u uw producten niet ziet, zorg ervoor dat u de correcte gastheergroep gebruikt. Bijvoorbeeld, als u opstelling uw aanbeveling om een het opvoeren milieu te gebruiken en u uw gastheergroep aan het Opvoeren plaatst, zou u uw inzamelingen in het opvoeren milieu voor de te tonen producten kunnen moeten opnieuw creëren. Als u wilt zien welke producten in elke omgeving beschikbaar zijn, gebruikt u Cataloguszoekopdracht voor elke omgeving. U kunt ook een voorvertoning weergeven van de inhoud van verzamelingen en uitsluitingen met aanbevelingen voor een geselecteerde omgeving (hostgroep).

>[!NOTE]
>Nadat u de geselecteerde omgeving hebt gewijzigd, moet u op Zoeken klikken om de geretourneerde resultaten bij te werken.

Het filter [!UICONTROL Environment] is beschikbaar op de volgende plaatsen in het Doel UI:

* Catalogus zoeken ([!UICONTROL Recommendations > Catalog Search])
* Dialoogvenster Verzameling maken ([!UICONTROL Recommendations > Collections > Create New])
* Dialoogvenster Verzameling bijwerken ([!UICONTROL Recommendations > Collections > Edit])
* Dialoogvenster Uitsluiting maken ([!UICONTROL Recommendations > Exclusions > Create New])
* Dialoogvenster Uitsluiting bijwerken ([!UICONTROL Recommendations > Exclusions > Edit])
