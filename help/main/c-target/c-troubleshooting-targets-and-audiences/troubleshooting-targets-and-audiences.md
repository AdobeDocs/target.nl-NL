---
keywords: problemen oplossen;veelgestelde vragen;veelgestelde vragen;veelgestelde vragen;veelgestelde vragen;doelen;doelgroepen
description: De mening vaak gestelde vragen (FAQs) over ervaring richtend en publiek dat in Adobe  [!DNL Target]  activiteiten wordt gebruikt.
title: Waar kan ik vragen en antwoorden vinden over doelen en publiek?
feature: Audiences
exl-id: f829bd4a-852a-4eb1-85d1-89e74c14b37e
source-git-commit: cf7f18b5fd9647bbecda2e6b6419c3a927708bd6
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 1%

---

# Veelgestelde vragen over doelen en doelgroepen

Lijst met veelgestelde vragen (FAQ&#39;s) over de ervaring die doelgericht en publiek is.

## Hoe evalueert [!DNL Target] URLs in het richten? {#url}

Het doel evalueert URLs verschillend afhankelijk van of u publiek URL het richten tijdens het creëren van een activiteit gebruikt of of gebruikt u URL het richten terwijl het creëren van een publiek.

Neem bijvoorbeeld de volgende URL:

`http://www.example.com/path1/path2/path3?queryStringParam1=test123&queryStringParam2=test7`

### URL-doelgroep

Om publiek URL toe te passen richtend, terwijl het creëren van een activiteit, op de **[!UICONTROL Experiences]** pagina (stap één van de drie-stap geleide werkschema), klik het **[!UICONTROL Configure]** pictogram ( ![&#x200B; vormt pictogram &#x200B;](/help/main/assets/icons/Setting.svg)), klik **[!UICONTROL Page Delivery]**, dan specificeer gewenste URL.

![&#x200B; URL van de Levering van de Pagina &#x200B;](/help/main/c-target/c-troubleshooting-targets-and-audiences/assets/activity-url.png)

URL van publiek zoekt naar een exacte URL-overeenkomst. Als de URL overeenkomt, overweegt Doel geen verdere logica. Als in de bovenstaande URL de activiteit is ingesteld op geactiveerd door `www.example.com` , komt de URL overeen met de volgende URL&#39;s, omdat de URL van het publiek niet specifiek is voor query&#39;s:

* `www.example.com?query=something`
* `www.example.com?query=anything`
* `www.example.com?query=nothing&qa=true&stuff=random&product=shoes&height=superTall`

Buiten het publiek dat op URL richt, kunt u specifieke waarden ook specificeren die in de vraag kunnen zijn.

URL-doel voor publiek en URL-doel toegevoegd via [!UICONTROL Template Rules] evalueren als URL-doel (zie hieronder voor URL-doel).

### URL-doel {#url-targeting}

Als u een doel voor de URL wilt toepassen, klikt u tijdens het maken van een publiek op slepen **[!UICONTROL Site Pages]** en zet u deze neer in het deelvenster [!UICONTROL Create Audiences] , klikt u op **[!UICONTROL Site Pages]** , selecteert u een optie in de eerste vervolgkeuzelijst ( [!UICONTROL Current Page] , [!UICONTROL Previous Page] of [!UICONTROL Landing Page] ), selecteert u [!UICONTROL URL] in de tweede vervolgkeuzelijst, geeft u een beoordelaar op en geeft u vervolgens de gewenste URL op.

![&#x200B; de Pagina&#39;s van de Plaats > Huidige Pagina > URL &#x200B;](/help/main/c-target/c-troubleshooting-targets-and-audiences/assets/site-url.png)

URL die richt transformeert URL in een reeks regels om te evalueren:

* URL = `example.com/path1/path2/path3?queryStringParam1=test123&queryStringParam2=test7`
* Domain = `example.com`
* Pad = `path1/path2/path3`
* Query = `queryStringParam1=test123&queryStringParam2=test7`

## Evalueert [!DNL Target] bij het maken van complexe URL-tekenreeksen de volledige URL?

Wanneer u dezelfde parameternaam meerdere keren gebruikt in een URL-tekenreeks, wordt door HTTP de naam van de eerste parameter beschouwd en worden de volgende parameters met dezelfde naam genegeerd.

Bijvoorbeeld in de volgende URL-tekenreeks:

`https://www.adobe.com/SearchResults.aspx?sc=BM&fi=1&fr=1&ps=0&av=0&Category=C0010438&Category=C000047`

De eerste instantie van de parameter `Category` wordt geëvalueerd en de tweede parameter `Category` wordt genegeerd.

De beste manier is om meerdere waarden aan één categorie te koppelen, zoals hieronder wordt getoond:

`https://www.adobe.com/SearchResults.aspx?sc=BM&fi=1&fr=1&ps=0&av=0&Category=C0010438,C000047`

## Waarom worden bij het maken van soorten publiek vooraf samengestelde soorten publiek onder [!DNL Target] Bibliotheek gevonden onder andere categorieën? {#section_9EBF5B0F9DF94168A15B92B905CCF7E0}

Het vooraf gebouwde publiek in de categorie Doelbibliotheek is verouderd publiek en bestaat in andere categorieën. Zo heeft het verouderde doelpubliek > Nieuwe bezoekers een bijgewerkte tegenhanger: Bezoekersprofiel > Nieuwe bezoeker.

De beste manier is om het nieuwere publiek te gebruiken omdat het betere prestaties heeft. Sommige klanten zouden erfenis kunnen gebruiken, prebuilt publiek, zodat zijn zij niet verwijderd uit de interface van het Doel.

## Hoe weet ik hoe verkeer verdeeld zal worden tussen het publiek? {#section_067EEFB956E7465CBF77EC86834470AB}

Door gebrek, is het verkeer gelijkmatig tussen ervaringen verdeeld. U kunt echter voor elke ervaring streefpercentages opgeven. In dit geval wordt een willekeurig getal gegenereerd en wordt dat nummer gebruikt om de ervaring te kiezen die moet worden weergegeven. De resulterende percentages zouden niet precies de gespecificeerde doelstellingen kunnen aanpassen, maar meer verkeer betekent dat de ervaringen dichter aan de doeldoelstellingen zouden moeten worden verdeeld.

## Welke ervaring toont als een gebruiker voor een activiteit kwalificeert die veelvoudige ervaringen met veelvoudige gekwalificeerde publiek bevat? {#section_94A60B11212D48FD8AB0803C6C7E7253}

De gebruiker komt in aanmerking voor de eerste ervaring/het eerste publiek dat wordt weergegeven op de pagina [!UICONTROL Target] van de activiteit.

Stel bijvoorbeeld dat de ervaring/het publiek Windows als Experience A, iOS als Experience B en Californië als Experience C opsomt. Een gebruiker uit Californië die een apparaat van Vensters gebruikt kwalificeert voor zowel Ervaring A (het publiek van Vensters) als Ervaring C (het publiek van Californië). Deze gebruiker krijgt Experience A te zien, omdat deze wordt weergegeven in de lijst hierboven Experience C op de pagina Target.

## Waarom verschillen namen voor hetzelfde publiek in [!DNL Target] , Adobe Audience Manager (AAM) en de Audience Library in core services? {#section_F67E61A607B6444C8DAA4F99C3E95AED}

De namen van het publiek in [!DNL Target] zijn uniek. In [!DNL AAM] en [!DNL Audience Library] kunt u echter dezelfde naam voor meerdere soorten publiek hebben (als ze zich in verschillende mappen bevinden). Wanneer [!DNL Target] een publieksnaam aantreft die overeenkomt met een [!DNL AAM] - of [!DNL Audience Library] -publiek, voegt [!DNL Target] &quot;#&lt;number>&quot; aan de naam toe.

U ziet bijvoorbeeld het volgende publiek: &quot;PC Users&quot; (in [!DNL AAM] ) en &quot;PC Users #1&quot; (in [!DNL Target] ).

## Waarom kan ik een publiek niet hernoemen? {#section_54E420556F534D20836E261E253D8B97}

Sommige doelgroepen zijn vooraf gedefinieerd, zoals &quot;Nieuwe bezoekers&quot; en &quot;Terugkerende bezoekers&quot;. Gebruikers kunnen de naam van dit vooraf gedefinieerde publiek niet wijzigen.

## Waarom worden niet alle profielparameters weergegeven in de gebruikersinterface van [!DNL Target] ? {#section_3CD947D15C984EE9AD19550220E0E8BD}

[!DNL Target] heeft een limiet van 50 unieke profielkenmerken per mbox-aanroep. Als u meer dan 50 profielkenmerken moet doorgeven aan [!DNL Target] , kunt u deze doorgeven met de API-methode [!UICONTROL Profile Update] . Voor meer informatie, zie [&#x200B; Update van het Profiel &#x200B;](https://developers.adobetarget.com/api/#authentication-tokens) in de documentatie van Adobe Target API.

## Waarom zien bezoekers ervaringen voor een AP-activiteit die ze niet zouden moeten zien? {#section_41CECEAE0881446A8D9F3B016857914B}

Automated Personalization-activiteiten worden één keer per sessie geëvalueerd. Als er actieve sessies waren die in aanmerking kwamen voor een bepaalde ervaring en er nu nieuwe aanbiedingen aan zijn toegevoegd, zien gebruikers de nieuwe inhoud samen met de eerder weergegeven aanbiedingen. Omdat ze eerder gekwalificeerd waren voor die ervaringen, zouden ze ze nog steeds zien gedurende de sessie. Als u dit bij elk paginabezoek wilt evalueren, kunt u beter overschakelen op het type activiteit Experience Targeting (XT).

## Waarom worden wijzigingen die zijn aangebracht in soorten publiek die zijn gemaakt via API, niet doorgevoerd in de gebruikersinterface van [!DNL Target] ? {#section_6BEB237CAC004A06A290F9644E5BF0FB}

In tegenstelling tot aanbiedingen en profielscripts, worden wijzigingen die door API worden aangebracht in publiek dat via Target Standard is gemaakt, momenteel niet opnieuw gesynchroniseerd naar de doelinterface.

## Tekenreeksen die getallen vertegenwoordigen (drijvende-kommagetallen worden ook ondersteund) worden als getallen vergeleken.{#strings-that-represent-numbers}

Als het linker- en rechtergedeelte van de gelijksoortige expressies op een getal kunnen worden geparseerd, worden de twee delen als getallen vergeleken, niet als tekenreeksen.

Bijvoorbeeld:

| Waarde | Doelcriteria | Resultaat |
| --- | --- | --- |
| 1,0 | is gelijk aan 1 | true |
| 1 | equalsIgnoreCase 1.0 | true |
| 1,230 | is gelijk aan 1 | true |
| 1,500 | is gelijk aan 1,5 | true |
| 1,200 | is kleiner dan 2 | true |
| 2 | is groter dan 3,0 | false |
| 045 | is gelijk aan 45 | true |

Getallen die in wetenschappelijke notatie zijn geschreven, worden altijd als tekenreeksen vergeleken.

Bijvoorbeeld:

&quot;4e-2&quot; is alleen gelijk aan &quot;4e-2&quot;. Het zal ** niet gelijk &quot;0.04&quot;.
