---
keywords: remote offer;remote offer selection matrix;cached content;dynamic content
description: Gebruik externe aanbiedingen om inhoud buiten Target te hosten die door Target naar websites van gebruikers wordt verwezen en aan hen wordt geleverd. Deze inhoud kan zich in een inhoudsbeheer of ander systeem bevinden, om redenen van gebruiksgemak of beveiliging.
title: Externe aanbiedingen maken
topic: Standard
uuid: 5aaff281-e96c-41a6-849e-2c3b0e35f161
translation-type: tm+mt
source-git-commit: c7664f9674234565a3657f453541095811fa5aa6
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 1%

---


# Externe aanbiedingen maken{#create-remote-offers}

Gebruik externe aanbiedingen om inhoud buiten Target te hosten die door Target naar websites van gebruikers wordt verwezen en aan hen wordt geleverd. Deze inhoud kan zich in een inhoudsbeheer of ander systeem bevinden, om redenen van gebruiksgemak of beveiliging.

>[!NOTE]
>
>Externe aanbiedingen kunnen alleen in de op formulieren gebaseerde composer worden gemaakt. De inhoud wordt op de [!DNL Target] aanvraaglocaties geïnjecteerd. Deze zijn dus hoogstwaarschijnlijk niet geschikt voor een algemeen [!DNL Target] verzoek.
>
>[!DNL Target Classic] meegeleverde vergelijkbare functies: [!UICONTROL Offer on Your Site] en [!UICONTROL Offer Outside Test&Target].

Voorbeelden van externe aanbiedingen zijn:

* Verschillende versies van je crosssells
* Dynamische boodschappen in winkelwagentjes
* Formulieren
* Rekenmachines
* Renteverhoging

**Een externe aanbieding maken:**

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.
1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![](assets/remote_offer_ui.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de [!UICONTROL Assets] bibliotheek.

1. Geef de externe URL voor de externe aanbieding op:

   | Option | Beschrijving |
   |--- |--- |
   | cachegeheugen | De inhoud voor een aanbieding op afstand in de cache wordt vanuit Target aangeboden.<br>Om de twee uur [!DNL Target] haalt u de inhoud op bij de externe URL en slaat u de inhoud vervolgens op in Target. Wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat, wordt de aanbieding geleverd door Target.<br>Externe aanbiedingen in cache bieden uitgebreide beveiliging omdat iemand die zich heeft aangemeld bijTarget de inhoud niet kan wijzigen. Als u de inhoud wilt wijzigen, moet iemand zich aanmelden bij het inhoudsbeheer of een ander systeem en de inhoud daar wijzigen.<br>U kunt een absolute of relatieve URL opgeven voor een externe aanbieding die in cache wordt geplaatst. |
   | Dynamisch | Een dynamische aanbieding op afstand wordt aangeboden door het contentbeheer of een ander systeem in plaats van door Target.<br>Mogelijk wilt u de inhoud niet periodiek in cache plaatsen en vervolgens door Target leveren wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat. In plaats daarvan, wilt u het systeem roepen dat de inhoud ontvangt, misschien in specifieke informatie overgaan zodat de teruggekeerde aanbieding dynamisch, of verschillend, voor elke gebruiker kan zijn.<br>Als een gebruiker zich bijvoorbeeld bij een website aanmeldt voor een creditcard die een ervaring met een dynamische externe aanbieding bevat, kunt u parameters aan de URL doorgeven voor de accountgegevens van de gebruiker. Vervolgens kan de website gebruikersspecifieke informatie verstrekken, zoals de accountbalans.<br>Klik [!UICONTROL Add Parameter] om een of meer [!DNL Target] aanvragen of aanvraagparameters toe te voegen. |

1. Klik op **[!UICONTROL Save]**.

## Beste praktijken voor het Gebruiken van Verre Aanbiedingen {#section_7718512D08E14121B6F6B8C38134F4BC}

Aanbevolen procedures voor het gebruik van externe aanbiedingen in uw activiteiten:

* Als uw aanbieding zich in hetzelfde domein bevindt als de [!DNL Target] aanvragen, kunt u met de [!UICONTROL Cached] optie relatieve URL&#39;s gebruiken om de locatie van uw aanbieding te beschrijven.

   Dit betekent dat wanneer u uw activiteit van uw testservers naar productie verplaatst, de inhoud automatisch toegankelijk zal zijn zonder het moeten URL manueel veranderen.

* Als de test gegevens bevat die dynamisch door de server worden gegenereerd, is de [!UICONTROL Dynamic] optie mogelijk de juiste keuze.
* Als u alleen de weergave van uw bestaande externe aanbiedingsinhoud wilt testen, gebruikt u de optie [!UICONTROL Visual Experience Composer] om de weergave van de inhoud die door het inhoudsbeheersysteem wordt geretourneerd, te wijzigen.
* Gebruik de Matrix van de Selectie van de Verre Aanbieding om u te helpen de aanbieding kiezen het best geschikt voor uw specifiek geval. Vraag uw accountvertegenwoordiger.

## Hoe dynamische externe aanbiedingen werken {#concept_CC2A969420B34364A9FA78C1CE251818}

Dynamische externe aanbiedingen gebruiken uw dynamische paginatechnologie om waarden aan de aanbieding door te geven.

De aanbieding wordt uitgevoerd nadat u de pagina teruggeeft. Een onzichtbaar iframe verzamelt de gegevens, kopieert het uit het frame en voegt in op de pagina en laadt de doorgegeven waarden.

![](assets/remote_offer_howitworks_2.jpeg)

## Selectiematrix externe aanbieding {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Met de Matrix Selectie voor externe aanbiedingen kunt u bepalen welk type externe aanbieding u wilt kiezen: [!UICONTROL Cached] of [!UICONTROL Dynamic].

| Functie | cachegeheugen | Dynamisch |
|--- |--- |--- |
| Wordt bijgewerkt wanneer een bezoeker een aanvraag indient | Nee | Ja |
| Inhoud bijwerken | Wordt elke 2 uur in de cache geplaatst | Onmiddellijk bijgewerkt na elk verzoek |
| Tijdstip van laden | Sneller | Langzamer vanwege verwerking van aanvragen |
| Kan JavaScript op pagina zien | Ja | Nee, maar kan wel via URL worden doorgegeven |
| Aanbiedingen kunnen JavaScript bevatten | Ja | Ja |
| Aanbiedings-URL | Absoluut of Relatief | Relatief |
| De computer aanvragen | Adobe-servers | De computer van de bezoeker, die de cookies van de bezoeker draagt |