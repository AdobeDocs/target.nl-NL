---
keywords: inkomstenlift;inkomsten;schatten van lift in inkomsten;berekenen van lift;geschatte waarde
description: Schatting van de lift die u kunt bereiken als elke bezoeker de winnende ervaring ziet, als de trends doorzetten zoals deze tijdens de test zijn.
title: Wat schat ik de opbrengst in?
feature: Administration & Configuration
role: Admin
exl-id: a3c5e20e-f5d5-4b6f-b169-59d5916584ab
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Schatting van de inkomsten

Gebruiken [!DNL Adobe Target] om de inkomstenverhoging te schatten u zou bereiken als alle gebruikers de winnende ervaring bekijken.

>[!NOTE]
>
>Geschatte lift is niet beschikbaar voor [!UICONTROL Experience Targeting] (XT) activiteiten op dit moment.

De functie voor het schatten van de lift is standaard uitgeschakeld. U kunt deze functie inschakelen in uw accountvoorkeuren. Alleen gebruikers van Experience Cloud Admin kunnen deze functie in- of uitschakelen. Als geschatte lift is uitgeschakeld, worden de bijbehorende velden niet weergegeven in de interface. Als u de functie uitschakelt, gaan er geen gegevens verloren, inclusief de gegevens die voor uw ramingen worden gebruikt. De schattingen zijn gebaseerd op gegevens die worden verzameld, ongeacht of de functie is ingeschakeld.

>[!IMPORTANT]
>
>De geschatte lift is slechts een schatting. De nauwkeurigheid ervan hangt af van een aantal factoren, waaronder de geprojecteerde cijfers als de huidige tendensen aanhouden. Deze waarden zijn schattingen op basis van de in het verleden behaalde resultaten en mogen niet worden gebruikt voor financiële richtsnoeren. Toekomstige resultaten kunnen afwijken.

In deze schatting wordt de hoeveelheid lift berekend die door de winnende ervaring wordt behaald en het totale aantal bezoekers gedurende de levensduur van de activiteit, en wordt de lift weergegeven die u kunt behalen als elke bezoeker de winnende ervaring ziet, als de trends doorzetten zoals ze tijdens de test hebben.

De geraamde toename van de inkomsten wordt berekend op basis van de inkomsten per bezoek (RPV) die zijn verkregen uit de primaire doelstelling.

De geschatte lift wordt berekend met behulp van de volgende formule: (&lt;winning experience=&quot;&quot; rpv=&quot;&quot;> - &lt;control experience=&quot;&quot; rpv=&quot;&quot; total=&quot;&quot; number=&quot;&quot; of=&quot;&quot; visitors=&quot;&quot; in=&quot;&quot; the=&quot;&quot; activity=&quot;&quot;>

Het resulterende getal wordt afgerond tot op één decimaal (maximaal) als het versmalde formulier slechts één cijfer voor het decimaalteken heeft. Bijvoorbeeld: $ 1,6 MB, $ 60.000, $ 8,5.000, $ 205.000

Als uw winnende ervaring bijvoorbeeld een lift van $0,59 weergeeft en uw ervaring met besturing een lift van $0,15 weergeeft, berekent de schatting een lift van $0,44 per bezoeker. Als je 75.000 bezoekers had, zou de resulterende lift in inkomsten $33.000 bedragen als alle bezoekers de winnende ervaring en de huidige trends zien voortduren.

En als je winnende ervaring een lift van $0,17 over de controle-ervaring laat zien, en je hebt 192.000 bezoekers gehad tijdens de duur van de test, dan kon je een inkomstenverhoging van $32.640 verwachten als de huidige trends zich voortzetten.

De geraamde lift in het inkomstenveld wordt als &quot;—&quot; weergegeven onder de volgende omstandigheden:

* Indien er onvoldoende bezoekers zijn om een redelijke schatting te berekenen
* Als de geschatte waarde van metrisch niet op de metrische opstellingspagina is verstrekt
* Als de best presterende ervaring de controle is

Bij het instellen van de doelen van een activiteit, biedt het veld Geraamde waarde een waarde voor uw doel. Met deze waarde kan Target de geschatte lift in de inkomsten berekenen. Dit veld is facultatief; de incrementele inkomsten voor elke metrische waarde die geen inkomsten oplevert, kunnen echter niet zonder deze methode worden berekend. Het gegevenstype is currency. Dit veld wordt progressief weergegeven nadat de gebruiker de actie aangeeft die is ondernomen om het doel te bereiken.

De geschatte inkomsten als 100% van de bezoekers de winnende ervaring zien verschijnen bij de bovenkant van uw rapporten van het Doel.
