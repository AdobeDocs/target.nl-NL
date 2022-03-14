---
keywords: Recommendations;intro;introductie;webinar;demo
description: Meer informatie over Recommendations-activiteiten in Adobe [!DNL Target] die automatisch inhoud weergeven die mogelijk van belang is voor uw klanten op basis van eerdere gebruikersactiviteiten of andere algoritmen.
title: Wat zijn Recommendations-activiteiten?
feature: Recommendations
exl-id: bc4d9a46-ea21-4687-b8a0-7f2e1dc33ebf
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '2106'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Inleiding tot Recommendations

De tekst in dit artikel is afkomstig uit de *Inleiding tot Recommendations* webinar, dat u hieronder in zijn geheel kunt bekijken.

De *Inleiding tot Recommendations* webinar bevat een diepgaande analyse van hoe u de waarde van [!DNL Adobe Target Recommendations]. Ontdek hoe dit [!DNL Target] De activiteit toont automatisch producten of inhoud die uw klanten zouden kunnen interesseren door suggesties in real time te optimaliseren die op vorige bezoeken worden gebaseerd. Verder duik in de [!DNL Target] UI voor een geleidelijke overzicht van hoe te om een [!DNL Recommendations] activiteit.

## Inleiding

We weten allemaal wat voor soort aanbevelingen we in de detailhandel zien. Klanten verwachten steeds vaker dit soort aanbevelingen en gebruiken deze als uitgangspunt om andere beschikbare opties te verkennen. Als je aan je eigen winkelgedrag denkt, werken dit soort aanbevelingen heel goed. Bijna iedereen onder ons heeft een product gekocht dat we eerst in een aanbeveling ergens hebben gezien, of dat nu in een winkel of op een digitaal eigendom was.

In de volgende afbeelding ziet u een aanbeveling voor accessoires die veel worden aangeschaft met een nieuwe telefoon, zoals oplaadstations, draagtassen en hoofdtelefoons.

![Aanbeveling waarin wordt aangegeven welke accessoires anderen met een nieuwe telefoon hebben gekocht.](/help/main/c-recommendations/assets/intro-1.png)

Maar waar we niet altijd aan denken, is hoe digitaal-eerste merken de verwachtingen van de klant doen toenemen. Steeds meer wordt de manier waarop we media en inhoud consumeren gedreven door gepersonaliseerde aanbevelingen. Denk aan het eerste ding dat je ziet wanneer je Netflix, Spotify of YouTube opent. Deze merken beginnen de klantenervaring met aanbevelingen. In een wereld waar meer alternatieven dan ooit beschikbaar zijn, is het kritiek dat u de meest relevante inhoud voor uw klant op het punt van interactie kunt identificeren.

![Aanbeveling voor de presentatie van digitale eerste merken](/help/main/c-recommendations/assets/intro-2.png)

Marketers gebruiken [!DNL Adobe Target] om gepersonaliseerde ervaringen over een grote verscheidenheid van industrieën, klantentypes, en kanalen te drijven.

[!DNL Adobe Target] levert overal gepersonaliseerde inhoud.

![Illustratie waarin wordt getoond hoe Target aanbevelingen op verschillende plaatsen levert](/help/main/c-recommendations/assets/intro-3.png)

* **Publiceren**: Webuitgevers gebruiken [!DNL Target Recommendations] om artikelen aan te bevelen aan bezoekers van de site en een grotere betrokkenheid te stimuleren.
* **Video-Tutorials**: [!DNL Adobe Creative Cloud] gebruik [!DNL Target] om videozelfstudies aan te bevelen aan Photoshop-gebruikers in de Photoshop-toepassing.
* **Games**: Games gebruiken [!DNL Target] om games en inhoud aan gebruikers op hun consoles aan te bevelen.
* **B2B-verkoop**: [Bedrijven van bedrijf tot bedrijf gebruiken Target om video&#39;s, whitepapers, en blogberichten aan B2B vooruitzichten aan te bevelen; downloads leveren; en hulp bieden aan bestaande klanten](https://theblog.adobe.com/testing-shifts-high-gear-intel).

* **Reizen**: [Een Duits reisboekje gebruikt Target om hotels en meer aan reizigers aan te bevelen](https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608).

* **Detailhandel**: [Een toonaangevende B2B-detailhandelaar gebruikt Target om topcategorieën en producten aan te bevelen om bezoekers in de browser en de mobiele app te retourneren](https://theblog.adobe.com/optimization-personalization-b2b-powerhouse-grainger/).

Dit zijn enkel een paar manieren de klanten Doel gebruiken om gepersonaliseerde aanbevelingen te leveren.

Wat is de reden voor grote aanbevelingen?

![Illustratie waarin de drie elementen worden getoond die belangrijke aanbevelingen doen](/help/main/c-recommendations/assets/intro-4.png)

Grote aanbevelingen moeten relevant en gepersonaliseerd zijn. Dit betekent dat u drie dingen nodig hebt om relevantie en personalisatie te stimuleren:

* **Besturingselementen voor markeertekens** om de relevantie van de aanbevolen items te helpen bepalen. Als markator, brengt u waardevolle context aan de lijst en u weet welke attributen van uw producten of inhoud relevant voor een te overwegen raadsmodel zijn. Als u een video-site uitvoert, weet u zeker dat gebruikers wellicht geïnteresseerd zijn in het bekijken van films van dezelfde directeur, maar het kan u waarschijnlijk niet schelen of u films wilt zien die door dezelfde studio zijn gemaakt. [!DNL Target] machtigt u met controles die u toestaan om uw algoritmen met deze domeinkennis te verbeteren.
* **Geavanceerde modellen** om de betekenis van miljoenen items in uw catalogus en interactiegebeurtenissen te begrijpen. [!DNL Target] beschikt over geavanceerde mogelijkheden voor machinaal leren die gedurende een decennium van ervaring zijn opgebouwd en we verwerken miljarden aanbevelingen per jaar.
* **Gebruikerscontext** om ervoor te zorgen dat aanbevelingen tijdig worden gedaan en relevant zijn voor uw gebruikers. U wilt de video die iemand net heeft bekeken of het shirt dat iemand net aan zijn winkelwagentje heeft toegevoegd, niet aanbevelen. Het rijke gebruikersprofiel van het doel kan in aanbevelingen worden gebruikt om verpersoonlijking te verzekeren.

## Implementeren [!DNL Target] Recommendations

Begin met een strategie.

![Illustratie met een strategie voor aanbevelingen](/help/main/c-recommendations/assets/intro-5.png)

* **Welke items wilt u aanbevelen?** Denk eerst na over de objecten die je wilt aanbevelen. Dit kunnen producten, video&#39;s of inhoud zijn.
* **Waar wilt u aanbevelingen tonen?** Denk vervolgens na over waar u aanbevelingen wilt doen. In grote lijnen welke kanalen (web, mobiel, in-store, kiosk, enzovoort). Welke delen van de klantenreis zullen aanbevelingen bevatten? Welke pagina&#39;s op uw site bevatten aanbevelingen?
* **Hoe gaat u bepalen als de aanbevelingen succesvol zijn?** Veronderstel dat u een ervaring zonder aanbevelingen en een ervaring met aanbevelingen hebt, of u hebt twee verschillende soorten aanbevelingen. Hoe zou u bepalen welke ervaring een betere ervaring voor uw klanten was? Sommige metriek is misschien moeilijker te meten dan andere. Bijvoorbeeld, is het effect van aanbevelingen op de Waarde van het Leven van de Klant vaak moeilijk om direct te krijgen. Het is dus vaak gemakkelijker om aan minder abstracte metrisch en te krijgen die concreter is, bijvoorbeeld opbrengst per bezoek, gemiddelde ordewaarde, of aantal kliks. In sommige gevallen zou u metrisch kunnen proberen te minimaliseren, bijvoorbeeld, het aantal steunvraag.

Nadat u met uw strategie komt, bent u bereid om de implementatie van te beginnen [!DNL Target Recommendations].

Er zijn drie brede stappen betrokken bij het creëren van uw aanbevelingen implementatie:

![Illustratie met de stappen voor het maken van de implementatie van uw aanbevelingen](/help/main/c-recommendations/assets/intro-6.png)

1. Teach [!DNL Target] over uw context of producten.
1. Leg gebruikersgedrag vast.
1. Krijg aanbevelingen met de juiste context.

### Teach [!DNL Target] over uw context of producten

Wanneer u begint met [!DNL Recommendations], geeft u informatie door over elk onderdeel dat u wilt aanbevelen. [!DNL Target] bevat verschillende integratieopties waarmee u uw catalogus kunt maken.

![Illustratie waarin wordt getoond hoe u Doel kunt onderwijzen over uw context of producten](/help/main/c-recommendations/assets/intro-7.png)

De eenvoudigste en meest gebruikte methode is het dagelijks of wekelijks verzenden van een CSV-bestand via uw systeem voor productinformatiebeheer of uw contentbeheersysteem. Maar u kunt ook informatie over de gegevenslaag van uw pagina doorgeven met behulp van de [!DNL Adobe Target] De bibliotheek van JavaScript, hefboomwerking onze APIs om informatie van uw bronsysteem direct over te gaan, of ons te gebruiken [!DNL Adobe Analytics] integratie als u al catalogusgegevens doorgeeft aan [!DNL Analytics].

Soms wilt u wellicht meerdere opties tegelijk gebruiken, bijvoorbeeld het doorgeven van de meeste gegevens per dag via een CSV-bestand en het vaker doorgeven van inventarisupdates via een API.

Uw IT-afdeling zal meestal betrokken zijn bij het instellen van deze stap.

Welke methode u ook kiest, u zou meta-gegevens over elk punt in drie categorieën moeten omvatten:

![Illustratie met metagegevens voor uw catalogus](/help/main/c-recommendations/assets/intro-8.png)

* Gegevens die u aan de gebruiker wilt tonen die de aanbeveling ontvangt. Bijvoorbeeld de naam van de film en een URL van een miniatuurafbeelding.
* Gegevens die nuttig zijn voor het toepassen van marketing- en verkoopbesturingselementen. Bijvoorbeeld, de classificatie van de film zodat u geen films NC-17 adviseert.
* Gegevens die nuttig zijn om de gelijkenis van items met andere items te bepalen. Bijvoorbeeld het genre van de film of de acteurs die in de film zijn.

### Gebruikersgedrag vastleggen

Vervolgens moet u tags toevoegen of gebruikmaken van uw bestaande tags [!DNL Analytics] implementatie om de conversiegebeurtenissen (zoals weergaven en aankopen) te volgen die [!DNL Target] algoritmen.

![Illustratie waarin wordt getoond hoe het gebruikersgedrag wordt vastgelegd](/help/main/c-recommendations/assets/intro-9.png)

U moet ervoor zorgen dat [!DNL Target] Houd rekening met de objecten die uw gebruikers bekijken en kopen. Als aankopen niet relevant zijn voor uw context, wilt u wellicht een ander type conversiegebeurtenis volgen, bijvoorbeeld het downloaden van een PDF, het voltooien van een enquête, het abonneren op een nieuwsbrief, het bekijken van een video enzovoort.

Als u al [!DNL Target] om A/B testactiviteiten op uw plaats in werking te stellen, zou u deze stap reeds kunnen voltooid hebben. Of als u al gebruikmaakt [!DNL Adobe Analytics] voor het melden van bezoeken ter plaatse en het conversiegedrag kunt u [!DNL Analytics] als uw gedragsgegevensbron. Als dat niet het geval is, kunt u dit het gemakkelijkst instellen met een tagbeheer, zoals tags in [[!DNL Adobe Experience Platform]](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). Het is ook mogelijk om offline- of in-app-interacties te verzenden naar [!DNL Target] via real-time API.

### Aanbevelingen ophalen met de juiste context

Geef informatie over de gebruiker en de context op het punt van interactie door aan [!DNL Target] relevante en gepersonaliseerde aanbevelingen terug te sturen.

![Illustratie waarin wordt getoond hoe u aanbevelingen kunt doen met de juiste context](/help/main/c-recommendations/assets/intro-10.png)

Naast het gedrag van gebruikers in het algemeen, moet u overgaan [!DNL Target] de specifieke context waarin aanbevelingen worden weergegeven. Dit omvat informatie over de pagina en informatie van het gebruikersprofiel. [!DNL Target] gebruikt deze informatie om gepersonaliseerde aanbevelingen te doen. Op een website in de detailhandel wilt u bijvoorbeeld weten welk product en welke productcategorie de bezoeker momenteel bekijkt. U wilt ook informatie over die gebruiker (favoriet merk, favoriete productcategorie, loyaliteitsrij, etc.) kennen. Deze informatie is belangrijk, zodat [!DNL Target] U kunt items filteren en de aanpassing van aanbevelingen verbeteren.

## Uw eerste Recommendations-activiteit samenstellen

Wat is een [!DNL Recommendations] activiteit?

![Illustratie waarin de onderdelen worden weergegeven die een goede aanbevolen activiteit uitvoeren](/help/main/c-recommendations/assets/intro-11.png)

A [!DNL Recommendations] de activiteit bestaat uit de volgende onderdelen :

* **Publiek**: Wie moet deze aanbevelingen zien?
* **Criteria**: Welke items moeten worden aanbevolen?
* **Ontwerp**: Hoe moeten de aanbevolen items worden weergegeven?

![Illustratie waarin wordt getoond wat een activiteit met aanbevelingen vormt: Soorten publiek, criteria en ontwerpen](/help/main/c-recommendations/assets/intro-12.png)

Uit de doos, [!DNL Target] omvat 14 ingebouwde doelgroepen, 42 ingebouwde criteria en 10 ingebouwde ontwerpsjablonen. U kunt elk van deze items aanpassen of uw eigen items toevoegen. We hebben eerder [webinars over het opbouwen van publiek](https://landing.adobe.com/acs/2018/na/adobe-target/registration.html) in [!DNL Target]. In dit gedeelte wordt de nadruk gelegd op het definiëren van criteria, die bepalen welke items worden aanbevolen.

Doel gebruikt het concept van de kaart met criteria. Een kaart met criteria is als een recept voor personalisatie.

![Criteria card illustratie](/help/main/c-recommendations/assets/intro-13.png)

Het is belangrijk om de juiste criteria te kiezen of te creëren om de personalisatieresultaten te bereiken u wenst. Een criterium is als een trechter die u van uw volledige catalogus aan uw definitieve reeks aanbevelingen neemt.

![Trechter-illustratie](/help/main/c-recommendations/assets/intro-14.png)

In de volgende secties worden de verschillende delen van deze trechter beschreven en wordt beschreven hoe deze werken in [!DNL Target]:

### Statische filters (verzamelingen en uitsluitingen)

Statische filters zijn globaal toepasbare regels met betrekking tot cataloguskenmerken die u niet verwacht vaak te wijzigen.

![Afbeelding van verzamelingen en uitsluitingen](/help/main/c-recommendations/assets/intro-16.png)

Bijvoorbeeld, in een inhoudscontext, zou u alle films in aanbevelingen kunnen willen omvatten, maar films die NC-17 worden beoordeeld uitsluiten. In een handelscontext, zou u veelvoudige merken in verschillende delen van de wereld kunnen hebben, maar u wilt slechts producten adviseren beschikbaar in de Verenigde Staten. U kunt ook producten van een regionaal privé-label uitsluiten.

Dit zijn alle catalogusattributen die globaal van toepassing zijn die u in veelvoudige aanbevelingen zou kunnen willen gebruiken en u verwacht niet hen om vaak te veranderen.

### Algorithm (advisesleutel en logica)

De volgende stap bestaat uit het kiezen van een aanbevolen sleutel en logica. Hier bepaalt u wat de basis voor uw aanbeveling is.

![Algorithm illustration](/help/main/c-recommendations/assets/intro-17.png)

Het eerste wat u moet kiezen is de raadssleutel. De sleutel van de aanbeveling is wat u &quot;omhoog&quot;kijkt om de aanbeveling te kiezen. Daar baseert u uw aanbeveling op.

U kunt uw aanbeveling baseren op:

* Het item dat de bezoeker momenteel bekijkt
* De categorie die de bezoeker momenteel bekijkt
* Het object dat de bezoeker voor het laatst heeft gekocht of aan het winkelwagentje heeft toegevoegd
* Een aangepast kenmerk dat is gekoppeld aan een bezoeker of een item

Op basis van deze toetsen kiest u vervolgens de gewenste logica voor de aanbeveling:

* Items met vergelijkbare kenmerken
* De meest bekeken items in een bepaalde categorie
* Klanten die dit object hebben gekocht, hebben deze objecten ook gekocht
* Een aangepast kenmerk

Uit de doos, [!DNL Target] bevat een portfolio met algoritmen.

![Portfolio van algoritmische illustratie](/help/main/c-recommendations/assets/intro-15.png)

* **Op populariteit gebaseerde algoritmen** Inclusief Meest bekeken verkopers en Topverkopers.
* **Op inhoud gebaseerde algoritmen** Inclusief gelijkenis met inhoud.
* **Op punten gebaseerde samenwerkende het filtreren algoritmen** Inclusief Bekeken/Weergegeven, Bekeken/Gekocht en Gekocht/Gekocht. Merk op dat &quot;gekocht&quot;om het even welke omzetting kan zijn.
* **Persoonlijke algoritmen** omvatten Recent Bekeken, de Aangesloten Plaats, en profiel-verbeterde samenwerkings het filtreren.
* **Uw eigen algoritmen gebruiken** laat u uw eigen douanealgoritmen gebruiken.

### Online bedrijfsregels

De laatste stap is het toepassen van online bedrijfsregels. Op deze manier kunt u algoritmen in staat stellen om domeinkennis en de huidige context te gebruiken op basis van wat de bezoeker doet voor uw digitale eigenschap.

![Online-business rules illustration](/help/main/c-recommendations/assets/intro-18.png)

In de context van de inhoud kunt u bijvoorbeeld films uitsluiten die de bezoeker eerder heeft bekeken, films van dezelfde regisseur aanbevelen of films in hetzelfde genre stimuleren. In de detailhandel, zou u uit-van-voorraad producten kunnen willen uitsluiten, punten in een prijswaaier van $5 tot $500 tonen, of voorwerpen van het zelfde merk verhogen.

## Demo

Nadat u de taken voltooit die in de hierboven beschreven aanbevelingen trechter worden geïllustreerd, wordt u verlaten met uw definitieve aanbeveling. Een demonstratie in het product bekijken binnen [!DNL Target], begint de demo om 21:00 in *Adobe Target Basics Webinar*, gekoppeld aan hieronder.

## Adobe [!DNL Target] Basics Webinar: Inleiding tot Recommendations {#intro-to-recs}

[Inleiding tot Recommendations](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)
