---
keywords: Profile script;profile script attributes;mutually exclusive activities
description: U kunt profielkenmerken gebruiken om tests in te stellen die twee of meer activiteiten vergelijken, maar niet toestaan dat dezelfde bezoekers aan elke activiteit deelnemen.
title: Profielscripts gebruiken om activiteiten te testen die elkaar uitsluiten
feature: null
topic: Advanced,Standard,Classic
uuid: a76ed523-32cb-46a2-a2a3-aba7f880248b
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# Profielscripts gebruiken om activiteiten te testen die elkaar uitsluiten {#section_FEFE50ACA6694DE7BF1893F2EFA96C01}

U kunt profielkenmerken gebruiken om tests in te stellen die twee of meer activiteiten vergelijken, maar niet toestaan dat dezelfde bezoekers aan elke activiteit deelnemen.

Het testen van activiteiten die elkaar uitsluiten, voorkomt dat een bezoeker in één activiteit de testresultaten voor de andere activiteiten beïnvloedt. Wanneer een bezoeker aan meerdere activiteiten deelneemt, kan het moeilijk zijn te bepalen of de positieve of negatieve lift het resultaat is van de ervaring van de bezoeker met één activiteit, of of de interacties tussen meerdere activiteiten van invloed waren op de resultaten van een of meer activiteiten.

Bijvoorbeeld, kunt u twee gebieden van uw e-commerce systeem testen. Misschien wilt u testen of de knop Toevoegen aan winkelwagentje rood wordt in plaats van blauw. U zou een nieuw controleproces ook kunnen testen dat het aantal stappen van vijf tot twee vermindert. Als beide activiteiten dezelfde succesgebeurtenis hebben (een voltooide aankoop), kan het moeilijk zijn om te bepalen of de rode knop conversies verbetert, of dat dezelfde conversies ook zijn verhoogd als gevolg van het verbeterde afrekenproces. Door de tests te scheiden in wederzijds uitsluitende activiteiten, kunt u elke verandering onafhankelijk testen.

Houd rekening met de volgende informatie wanneer u een van de volgende profielscripts gebruikt:

* Het profielscript moet worden uitgevoerd voordat de activiteit wordt gestart en het script moet tijdens de duur van de activiteit ongewijzigd blijven.
* Deze techniek vermindert de hoeveelheid verkeer in de activiteit, die de activiteit zou kunnen vereisen om langer te lopen. U moet hiermee rekening houden wanneer u de duur van de activiteit inschat.

## Twee activiteiten opzetten

Als u bezoekers wilt sorteren in groepen die elk een andere activiteit zien, moet u een profielkenmerk maken. Een profielkenmerk kan een bezoeker in een van twee of meer groepen sorteren. Als u een profielkenmerk met de naam &quot;twee groepen&quot; wilt instellen, maakt u het volgende script:

```
if (!user.get('twogroups')) { 
    var ran_number = Math.floor(Math.random() * 99); 
    if (ran_number <= 49) { 
        return 'GroupA'; 
    } else { 
        return 'GroupB'; 
    } 
}
```

* `if (!user.get('twogroups'))` Hiermee bepaalt u of het *twee-groepenprofielkenmerk* is ingesteld voor de huidige bezoeker. Als dat het geval is, is geen verdere actie vereist.

* `var ran_number=Math.floor(Math.random() *99)` declareert een nieuwe variabele met de naam ran_number, stelt de waarde ervan in op een willekeurige decimaal tussen 0 en 1, vermenigvuldigt deze vervolgens met 99 en rondt deze af om een bereik van 100 (0-99) te maken. Dit is handig voor het opgeven van een percentage bezoekers dat de activiteit ziet.

* `if (ran_number <= 49)` Hiermee wordt een routine gestart die bepaalt tot welke groep de bezoeker behoort. Als het teruggekeerde aantal 0-49 is, wordt de bezoeker toegewezen aan GroupA. Als het aantal 50-99 is, wordt de bezoeker toegewezen aan GroupB. De groep bepaalt welke activiteit de bezoeker ziet.

Nadat u de profielattributen creeert, opstelling de eerste activiteit om de gewenste bevolking te richten door te vereisen dat de parameter van het gebruikersprofiel de waarde aanpast die voor GroupA wordt gespecificeerd. `user.twogroups`

>[!NOTE]
>
>Kies een box vroeg op de pagina. Deze code bepaalt of een bezoeker de activiteit ervaart. Zolang een box eerst door browser wordt ontmoet, kan het worden gebruikt om deze waarde te plaatsen.

Opstelling de tweede campagne zodat de parameter van het gebruikersprofiel de waarde aanpast die voor GroupB wordt gespecificeerd. `user.twogroups`

## Het opzetten van drie of meer activiteiten

Het instellen van drie of meer activiteiten die elkaar uitsluiten, is vergelijkbaar met het instellen van twee, maar u moet het profielkenmerk van JavaScript wijzigen om een aparte groep voor elke activiteit te maken en bepalen wie elke activiteit ziet. Het genereren van willekeurige getallen is anders, afhankelijk van het feit of u een oneven of even aantal groepen maakt.

Als u bijvoorbeeld vier groepen wilt maken, gebruikt u de volgende JavaScript-code:

```
if (!user.get('fourgroups')) { 
    var ran_number = Math.floor​(Math.random() * 99); 
    if (ran_number <= 24) { 
        return 'GroupA'; 
    } else if (ran_number <= 49) { 
        return 'GroupB'; 
    } else if (ran_number <= 74) { 
        return 'GroupC'; 
    } else { 
        return 'GroupD'; 
    } 
}
```

In dit voorbeeld is de wiskunde die wordt gebruikt om het willekeurige aantal te produceren dat een bezoeker aan een groep toewijst het zelfde als het met slechts twee groepen is. Er wordt een willekeurig decimaal gegenereerd en vervolgens naar beneden afgerond om een geheel getal te maken.

Als u een oneven aantal groepen creeert, of om het even welk aantal dat 100 niet gelijkmatig in verdeelt, zou u decimaal niet aan een geheel moeten rond. Als u de decimale waarde niet afrondt, kunt u bereiken zonder gehele getallen opgeven. U doet dit door deze lijn te veranderen:

`var ran_number=Math.floor(Math.random()*99);`

tot:

`var ran_number=Math.random()*99;`

Als u bijvoorbeeld bezoekers in drie gelijke groepen wilt plaatsen, gebruikt u de volgende code:

```
if (!user.get('threegroups')) { 
    var ran_number = Math.random() * 99; 
    if (ran_number <= 32.33) { 
        return 'GroupA'; 
    } else if (ran_number <= 65.66) { 
        return 'GroupB'; 
    } else { 
        return 'GroupC'; 
    } 
}
```
