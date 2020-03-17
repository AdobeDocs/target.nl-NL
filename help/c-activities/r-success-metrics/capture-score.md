---
keywords: capture score;score
description: De betrokkenheidsmetrische gegevens van de score vastleggen berekenen een geaggregeerde score op basis van de waarde die is toegewezen aan pagina's die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergavekader van de campagne voor de campagne voor ogen heeft.
title: Muziek vastleggen
subtopic: Getting Started
topic: Standard
uuid: 977454ad-da32-449a-a8c9-1f3c75220be6
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Muziek vastleggen{#capture-score}

De betrokkenheidsmetrische gegevens van de score vastleggen berekenen een geaggregeerde score op basis van de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergavekader van de campagne voor de campagne voor ogen heeft.

In het volgende voorbeeld wordt getoond hoe de betrokkenheid van de score wordt berekend in een campagne die twee ervaringen test, één met een kattenbeeld en één met een hondenbeeld.

![](assets/example_score.png)

In dit voorbeeld ervaart de eerste bezoeker de kattenervaring. Stel dat er een algemene mbox doorloopt in een paginascore op basis van de waarde van de pagina. Als de markering de betrokkenheid van het aantal pagina&#39;s heeft vastgelegd op een succesmetrische methode die is gekoppeld aan `**any mbox**`, accumuleert de bezoekscore voor elke aanvraag van een box die wordt weergegeven na de weergavemabox rondom de katafbeelding.

De eerste pagina voegt 1 aan de score toe, de tweede pagina 0.25, de derde 0.10 en de vierde 0.10 voor een totaal van 1.45. Dit kan worden geïnterpreteerd als een valuta of als punten. Tijdens een afzonderlijk bezoek ervaart een bezoeker de honden. Hoewel de bezoeker minder pagina&#39;s bekijkt, is de score 2,10 groter dan het andere bezoek, omdat de bezoeker waardevolle pagina&#39;s heeft bekeken.

U kunt aanschafkosten en partnerverbindingsopbrengsten in aanmerking nemen door adboxes en redirecteuren door te geven, zoals in de volgende paginastroom wordt getoond. Bericht dat, in dit voorbeeld, beide vakjes op de artikelpagina een score overgaan, misschien die een bekende CPM vertegenwoordigen.

![](assets/example_score2.png)

**Een paginascore toewijzen**

U kunt een waarde toewijzen aan elke pagina op uw site op basis van wat de pagina voor u waard is. Een kooksite kan bijvoorbeeld advertenties voor meer geld op artikelpagina&#39;s met functies verkopen dan in de sectie over ervaring. De functieartikelen zijn dus waardevoller dan de sectie Experience. Met de paginascore kunt u een algemene &#39;waarde&#39; van een bezoek ontwikkelen, zodat de persoon die meer functieartikelen leest, meer &#39;punten&#39; krijgt dan iemand die gewoon door de ervaringen bladert.

Er zijn twee methoden om een score toe te wijzen aan een pagina:

* Maak in de mbox-code een parameter mbox met de naam `mboxPageValue`.

   Voorbeeld: `('global_mbox', 'mboxPageValue=10');`

   Elke keer dat de pagina met dat vak wordt weergegeven, wordt de opgegeven waarde aan de score toegevoegd. Als meerdere vakken op de pagina score bevatten, is de score voor de pagina het totaal van alle mbox-waarden. `mboxPageValue` is een gereserveerde parameter die wordt gebruikt voor het doorgeven van waarden in een box om een betrokkenheidsscore vast te leggen. Positieve en negatieve waarden kunnen worden doorgegeven. De som wordt berekend aan het einde van het bezoek van elke bezoeker om de totale score voor het bezoek te berekenen.

* Geef de `?mboxPageValue=n` parameter in de URL voor de pagina door.

   Voorbeeld: `https://www.mydomain.com?mboxPageValue=5`

   Met deze methode wordt de opgegeven waarde toegevoegd aan de score voor elk vak op de pagina. Als u bijvoorbeeld de parameter doorgeeft `?mboxPageValue=10`en er drie vakken op de pagina staan, is de score voor de pagina 30.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Kaders boven het eerste weergavekader van de campagne worden niet in de score opgenomen.

U kunt het beste waarden toewijzen in de mbox-code. Hierdoor kunt u nauwkeurig aangeven welke waarden u meet, afhankelijk van de inhoud van elk vak.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>U kunt de waardetoewijzingen van de paginascore van uw site in het [!DNL at.js] of [!DNL mbox.js] bestand eenvoudig onderhouden met behulp van voorwaardelijke JavaScript-logica. Zo hoeft u niet meer code aan uw pagina&#39;s toe te voegen. Neem contact op met uw accountconsultant voor hulp.

U kunt de twee methoden combineren, maar dit kan resulteren in een hogere score dan u had verwacht. Als u bijvoorbeeld een waarde van 10 toewijst aan elk van drie vakken en geen score toewijst aan een vierde vak, geeft u de URL-parameter door `?mboxPageValue=5`, dan is de paginascore 50, 30 voor de drie vakken met toegewezen waarden en vervolgens 5 voor elk van de vier vakken op de pagina.

De teller begint met de eerste vertoningsmbox, niet de ingangsmbox. Als u bijvoorbeeld de campagne op de startpagina invoert die geen weergavekader heeft en vervolgens een koppeling naar de cataloguspagina met een weergavekader maakt, begint de teller wanneer u naar de cataloguspagina gaat.

U kunt ook negatieve waarden doorgeven op bepaalde pagina&#39;s die u geld kosten of die een bezoeker niet kan zien. De negatieve waarden beïnvloeden ook de algemene score. Deze techniek kan worden gebruikt op een pagina die bezoekers bereiken van een advertentie, zodat u weet hoeveel CPC was. Of u kunt het bijvoorbeeld gebruiken voor een ondersteuningspagina of contactpagina, waar bezoekers op deze pagina om hulp kunnen vragen.
