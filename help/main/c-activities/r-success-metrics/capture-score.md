---
keywords: vastlegscore;score
description: Leer over de metrisch van de Overeenkomst van de Score van de Vangst in Adobe  [!DNL Target]  die een bijeengevoegde score berekent die op de waarde wordt gebaseerd aan bezochte pagina's op de plaats wordt toegewezen.
title: Wat is de metrische score van de Score van de Vangst?
feature: Success Metrics
exl-id: 3446cdef-7ee0-40dd-bf17-27def56668d4
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Muziek vastleggen

De betrokkenheidsmetrische waarde voor de vastlegging van de score in [!DNL Adobe Target] berekent een geaggregeerde score op basis van de waarde die is toegewezen aan pagina&#39;s die op de site zijn bezocht, vanaf het punt waarop de bezoeker de eerste weergave van de [!DNL Target] -aanvraag van de campagne ziet.

In het volgende voorbeeld wordt getoond hoe de betrokkenheid van de score wordt berekend in een campagne die twee ervaringen test, één met een kattenbeeld en één met een hondenbeeld.

![&#x200B; example_score beeld &#x200B;](assets/example_score.png)

In dit voorbeeld ervaart de eerste bezoeker de kattenervaring. Stel dat een algemene [!DNL Target] aanvraag wordt doorgestuurd in een paginascore op basis van de waarde van de pagina. Als de markering de betrokkenheid van het aantal pagina&#39;s heeft vastgelegd op een succesmetrische methode die is gekoppeld aan `**any Target request**` , wordt de bezoekscore verzameld voor elke aanvraag die wordt weergegeven na de weergaveaanvraag rond de katafbeelding.

De eerste pagina voegt 1 aan de score toe, de tweede pagina 0.25, de derde 0.10 en de vierde 0.10 voor een totaal van 1.45. Dit kan worden geïnterpreteerd als een valuta of als punten. Tijdens een afzonderlijk bezoek ervaart een bezoeker de honden. Hoewel de bezoeker minder pagina&#39;s bekijkt, is de score 2,10 groter dan het andere bezoek, omdat de bezoeker waardevolle pagina&#39;s heeft bekeken.

U kunt aanschafkosten en partnerverbindingsopbrengsten in aanmerking nemen door adboxes en redirecteuren door te geven, zoals in de volgende paginastroom wordt getoond. In dit voorbeeld geven beide [!DNL Target] -aanvragen op de artikelpagina een score door, die mogelijk een bekende CPM vertegenwoordigt.

![&#x200B; example_score2 beeld &#x200B;](assets/example_score2.png)

## Een paginascore toewijzen

U kunt een waarde toewijzen aan elke pagina op uw site op basis van wat de pagina voor u waard is. Een kooksite kan bijvoorbeeld advertenties voor meer geld op artikelpagina&#39;s met functies verkopen dan in de sectie over ervaring. De functieartikelen zijn dus waardevoller dan de sectie Experience. Met de paginascore kunt u een algemene &#39;waarde&#39; van een bezoek ontwikkelen, zodat de persoon die meer functieartikelen leest, meer &#39;punten&#39; krijgt dan iemand die gewoon door de ervaringen bladert.

Er zijn twee methoden om een score toe te wijzen aan een pagina:

* Maak in de aanvraag [!DNL Target] een parameter met de naam `mboxPageValue` .

  Voorbeeld: `('global_mbox', 'mboxPageValue=10');`

  Elke keer dat de pagina met die [!DNL Target] -aanvraag wordt weergegeven, wordt de opgegeven waarde aan de score toegevoegd. Als meerdere aanvragen op de pagina score bevatten, is de score voor de pagina het totaal van alle aanvraagwaarden. `mboxPageValue` is een gereserveerde parameter die wordt gebruikt voor het doorgeven van waarden in een doelaanvraag om een betrokkenheidsscore vast te leggen. Positieve en negatieve waarden kunnen worden doorgegeven. De som wordt berekend aan het einde van het bezoek van elke bezoeker om de totale score voor het bezoek te berekenen.

* Geef de parameter `?mboxPageValue=n` door in de URL voor de pagina.

  Voorbeeld: `https://www.mydomain.com?mboxPageValue=5`

  Met deze methode wordt de opgegeven waarde toegevoegd aan de score voor elke [!DNL Target] -aanvraag op de pagina. Als u bijvoorbeeld de parameter `?mboxPageValue=10` doorgeeft en er drie [!DNL Target] -aanvragen op de pagina staan, is de score voor de pagina 30.

>[!NOTE]
>
>Doelverzoeken die zich boven de eerste weergave [!DNL Target] -aanvraag van de activiteit bevinden, worden niet in de score opgenomen.

U kunt het beste waarden toewijzen in de aanvraag [!DNL Target] . Op deze manier kunt u nauwkeurig aangeven welke waarden u meet, afhankelijk van de inhoud van elk verzoek.

>[!NOTE]
>
>Voor een gemakkelijker onderhoud kunt u de waardetoewijzingen voor de pagina&#39;s van uw site in het [!DNL at.js] -bestand configureren met behulp van bepaalde voorwaardelijke JavaScript-logica. Zo hoeft u niet meer code aan uw pagina&#39;s toe te voegen. Neem contact op met uw accountconsultant voor hulp.

U kunt de twee methoden combineren, maar dit kan resulteren in een hogere score dan u had verwacht. Als u bijvoorbeeld een waarde van 10 toewijst aan elk van de drie [!DNL Target] -aanvragen en geen score toewijst aan een vierde aanvraag, geeft u de URL-parameter `?mboxPageValue=5` door. De paginascore is dan 50, 30 voor de drie aanvragen met toegewezen waarden en vervolgens 5 voor elk van de vier aanvragen op de pagina.

De teller begint met het eerste vertoningsverzoek, niet het ingangsverzoek. Als u bijvoorbeeld de activiteit op de startpagina invoert die geen weergaveverzoek heeft, en vervolgens een koppeling naar de cataloguspagina met een weergaveverzoek maakt, begint de teller wanneer u naar de cataloguspagina gaat.

U kunt ook negatieve waarden doorgeven op bepaalde pagina&#39;s die u geld kosten of die een bezoeker niet kan zien. De negatieve waarden beïnvloeden ook de algemene score. Deze techniek kan worden gebruikt op een pagina die bezoekers bereiken van een advertentie, zodat u weet hoeveel CPC was. Of u kunt het bijvoorbeeld gebruiken voor een ondersteuningspagina of contactpagina, waar bezoekers op deze pagina om hulp kunnen vragen.
