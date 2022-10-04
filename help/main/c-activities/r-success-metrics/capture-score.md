---
keywords: vastlegscore;score
description: Meer informatie over de maatstaf voor de betrokkenheid van de opnamescore in Adobe [!DNL Target] Hiermee wordt een geaggregeerde score berekend op basis van de waarde die is toegewezen aan pagina's die op de site zijn bezocht.
title: Wat is de metrische score van de Score van de Vangst?
feature: Success Metrics
exl-id: 3446cdef-7ee0-40dd-bf17-27def56668d4
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Muziek vastleggen

De betrokkenheidsmetrische waarde van de opnamescore in [!DNL Adobe Target] berekent een geaggregeerde score op basis van de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergave van de campagne voor het eerst ziet [!DNL Target] verzoek.

In het volgende voorbeeld wordt getoond hoe de betrokkenheid van de score wordt berekend in een campagne die twee ervaringen test, één met een kattenbeeld en één met een hondenbeeld.

![example_score-afbeelding](assets/example_score.png)

In dit voorbeeld ervaart de eerste bezoeker de kattenervaring. Stel dat een globale [!DNL Target] Het verzoek gaat in een paginascore over die op de waarde van de pagina wordt gebaseerd. Als de markering de betrokkenheid van het aantal pagina&#39;s heeft vastgelegd op een succesmetrische methode die gekoppeld is aan `**any Target request**`, accumuleert de bezoekscore voor elk verzoek dat wordt gezien na het weergaveverzoek rond de katafbeelding.

De eerste pagina voegt 1 aan de score toe, de tweede pagina 0.25, de derde 0.10 en de vierde 0.10 voor een totaal van 1.45. Dit kan worden geïnterpreteerd als een valuta of als punten. Tijdens een afzonderlijk bezoek ervaart een bezoeker de honden. Hoewel de bezoeker minder pagina&#39;s bekijkt, is de score 2,10 groter dan het andere bezoek, omdat de bezoeker waardevolle pagina&#39;s heeft bekeken.

U kunt aanschafkosten en partnerverbindingsopbrengsten in aanmerking nemen door adboxes en redirecteuren door te geven, zoals in de volgende paginastroom wordt getoond. Let op: in dit voorbeeld beide [!DNL Target] De verzoeken op de artikelpagina gaan een score over, misschien die een bekende CPM vertegenwoordigen.

![example_score2-afbeelding](assets/example_score2.png)

## Een paginascore toewijzen

U kunt een waarde toewijzen aan elke pagina op uw site op basis van wat de pagina voor u waard is. Een kooksite kan bijvoorbeeld advertenties voor meer geld op artikelpagina&#39;s met functies verkopen dan in de sectie over ervaring. De functieartikelen zijn dus waardevoller dan de sectie Experience. Met de paginascore kunt u een algemene &#39;waarde&#39; van een bezoek ontwikkelen, zodat de persoon die meer functieartikelen leest, meer &#39;punten&#39; krijgt dan iemand die gewoon door de ervaringen bladert.

Er zijn twee methoden om een score toe te wijzen aan een pagina:

* In de [!DNL Target] verzoek, creeer een parameter genoemd `mboxPageValue`.

   Voorbeeld: `('global_mbox', 'mboxPageValue=10');`

   De opgegeven waarde wordt elke keer dat de pagina met die waarde wordt toegevoegd aan de score [!DNL Target] aanvraag wordt weergegeven. Als meerdere aanvragen op de pagina score bevatten, is de score voor de pagina het totaal van alle aanvraagwaarden. `mboxPageValue` is een gereserveerde parameter die wordt gebruikt voor het doorgeven van waarden in een doelaanvraag om een betrokkenheidsscore vast te leggen. Positieve en negatieve waarden kunnen worden doorgegeven. De som wordt berekend aan het einde van het bezoek van elke bezoeker om de totale score voor het bezoek te berekenen.

* Geef de `?mboxPageValue=n` in de URL voor de pagina.

   Voorbeeld: `https://www.mydomain.com?mboxPageValue=5`

   Met deze methode wordt de opgegeven waarde toegevoegd aan de score voor elke waarde [!DNL Target] op de pagina aanvragen. Wanneer u bijvoorbeeld de parameter doorgeeft `?mboxPageValue=10`en er zijn drie [!DNL Target] aanvragen op de pagina. De score voor de pagina is 30.

>[!NOTE]
>
>Doelverzoeken boven de eerste weergave van de activiteit [!DNL Target] aanvraag wordt niet in de score opgenomen.

U kunt het beste waarden toewijzen in het dialoogvenster [!DNL Target] verzoek. Hierdoor kunt u nauwkeurig aangeven welke waarden u meet, afhankelijk van de inhoud van elk verzoek.

>[!NOTE]
>
>Voor gemakkelijker onderhoud kunt u de pagina-score van uw site configureren in het dialoogvenster [!DNL at.js] bestand met bepaalde voorwaardelijke JavaScript-logica. Zo hoeft u niet meer code aan uw pagina&#39;s toe te voegen. Neem contact op met uw accountconsultant voor hulp.

U kunt de twee methoden combineren, maar dit kan resulteren in een hogere score dan u had verwacht. Als u bijvoorbeeld een waarde van 10 toewijst aan elk van drie [!DNL Target] aanvragen en geen score doorgeven aan een vierde aanvraag en vervolgens de URL-parameter doorgeven `?mboxPageValue=5`De paginascore is 50, 30 voor de drie aanvragen met toegewezen waarden en vervolgens 5 voor elk van de vier aanvragen op de pagina.

De teller begint met het eerste vertoningsverzoek, niet het ingangsverzoek. Als u bijvoorbeeld de activiteit op de startpagina invoert die geen weergaveverzoek heeft, en vervolgens een koppeling naar de cataloguspagina met een weergaveverzoek maakt, begint de teller wanneer u naar de cataloguspagina gaat.

U kunt ook negatieve waarden doorgeven op bepaalde pagina&#39;s die u geld kosten of die een bezoeker niet kan zien. De negatieve waarden beïnvloeden ook de algemene score. Deze techniek kan worden gebruikt op een pagina die bezoekers bereiken van een advertentie, zodat u weet hoeveel CPC was. Of u kunt het bijvoorbeeld gebruiken voor een ondersteuningspagina of contactpagina, waar bezoekers op deze pagina om hulp kunnen vragen.
