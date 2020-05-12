---
keywords: Implementation;mbox.js non javascript;redirector;costs per click;revenue per click
description: Gebruik een Redirector vergelijkbaar met hoe u een box in uw tests gebruikt.
title: Werken met directeuren
subtopic: Getting Started
topic: Standard
uuid: 79d7caf6-5693-4bb3-9131-8d1ae420fa5e
translation-type: tm+mt
source-git-commit: d8f059565ff44646c99b284ffb765377f5e9d19d
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---


# Werken met directeuren{#work-with-redirectors}

Gebruik een Redirector vergelijkbaar met hoe u een box in uw tests gebruikt.

Redirector wordt gemaakt met een speciale Redirector-URL waarmee een Redirector-box (Redirector) in uw account wordt geladen. Gebruik deze Redirector net zo als hoe u een box in uw tests gebruikt. Verzend de Redirector-URL naar uw advertentienetwerk als doelkoppeling van de advertentie.

Gebruik Redirector om het volgende te doen:

* Houd klikjes bij van uw weergaveadvertenties naar uw site
* Creeer één enkel gecentraliseerd rapport om kliks te volgen om advertenties op veelvoudige ad netwerken te tonen
* Verschillende weergave- en bestemmingen

   Dezelfde banner bijvoorbeeld landt op uw homepage, categoriepagina en productpagina.

* Zoeken naar welke landingspagina de meeste conversies tot gevolg hebben

Zie Niet-JavaScript-gebaseerde implementaties [](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4)voor informatie over de juiste instelling.

## Een redirector maken {#redirector}

Voordat u een redirector kunt gebruiken, moet u deze maken.

1. Bepaal de doelvariaties van de advertentie, inclusief het standaarddoel.
1. Maak de Redirector-URL.

   ```
   https://<your_testandtarget_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox
   /​page?mbox=redirectorlink_456
   &mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm
   ```

   * Waar `yourclientcode` is de cliëntcode van uw bedrijf. De clientcode van uw bedrijf is helemaal in kleine letters en heeft geen speciale tekens.

      * **at.js**: Uw clientcode is beschikbaar boven aan de [!UICONTROL Setup > Implementation > Edit at.js Settings] pagina van de [!DNL Target] interface.

      * **mbox.js**: De clientcode is beschikbaar boven aan de [!UICONTROL Setup > Implementation > Edit Mbox.js Settings] pagina.
   * `redirectorlink_456` Dit is de naam van de Redirector-box die in uw account wordt weergegeven voor gebruik in campagnes en tests.

      Regelaars functioneren anders dan andere vakken, maar worden net zo weergegeven als elke andere box in uw account. Geef de redirector een naam, zodat deze gemakkelijk kan worden onderscheiden van de standaardtekstvakken in uw account.  Als beste praktijken, begin de mbox naam met &quot;redirectorlink&quot;.

   * Waar `http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2Fusualdestination%2Ehtm` is het standaarddoel.

      Dit moet URL gecodeerd zijn en moet een absolute verwijzing zijn. U kunt de [HTML URL-coderingsverwijzing](https://www.w3schools.com/tags/ref_urlencode.asp) gebruiken om uw URL&#39;s snel te coderen.

      >[!IMPORTANT]
      >
      >Merk op dat u met Redirector aan een risico van Open Redirect Kwetsbaarheid kunt worden blootgesteld. Om het ongeoorloofde gebruik van verbindingen van Redirector door derden te vermijden, adviseren wij u &quot;erkende gastheren&quot;aan whitelist het gebrek opnieuw richt URL domeinen. Het doel gebruikt gastheren aan whitelist domeinen waaraan u redirects wilt toestaan. Voor meer informatie, zie [Create Whitelists die gastheren specificeren die worden gemachtigd om mbox vraag naar Doel](/help/administrating-target/hosts.md#whitelist) in *Gastheren* te verzenden.


1. Valideer Redirector.
   1. *Beste praktijken* op het gebied van beveiliging: Zorg ervoor dat het domein dat in Redirector wordt gebruikt, gewhitelliseerd is, zoals hierboven vermeld. Als u een domein gebruikt dat niet wordt gewhitelisteerd, zal Adobe om het even welke vraag aan dat domein blokkeren om kwaadwillige acteurs te verhinderen Redirector te gebruiken om aan potentieel kwaadwillige domeinen om te leiden.
   1. Voeg de Redirector-URL in een browser in en vernieuw deze.
   1. Meld u aan bij uw account, vernieuw de keuzelijst en controleer of de nieuwe Redirector als een box wordt weergegeven.
1. Als u verschillende bestemmingen voor één advertentie zult testen, creeer [Omleidingsvoorstellen](../../c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) voor elke versie.
1. Maak de campagne.

   Zie Implementaties [](../../c-implementing-target/c-non-javascript-based-implementation/non-javascript-based-implementation.md#concept_4799C58B081A43F6B3B8CC25A8D5D7C4) die niet op JavaScript zijn gebaseerd voor de juiste setup om uw doelen te bereiken.
1. Voltooi de kwaliteitscontrole op de campagne.

   Maak een dummypagina met een URL `<a href>` die de Redirector-URL bevat. Voorbeeld:

   ```
   <a href=https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=
   
   redirectorlink_456&mboxDefault=http%3A%2F%2Fwww%2Eyourcompany%2Ecom%2F​usualdestination%2Ehtm>
   ```

1. Verifieer dat alle ervaringen, standaardinhoud, en rapporten zoals verwacht op alle browser types, voor al uw milieu&#39;s handelen.

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >* Redirecteurs worden niet ondersteund door Voorvertoning van aanbieding of Bladeren naar box. Voorvertoning vindt direct in een browser plaats.
   >* `mboxDebug` werkt niet met Redirector.


1. Verzend de volledige Redirector-URL naar het advertentienetwerk van uw beeldscherm als de advertentiebestemming.

## Gebruik een redirector om kosten per klik en opbrengst per klik door te geven {#concept_3078EF48E9C44B34992D62AAB9628853}

Informatie over het gebruiken van redirector om kosten per klik en opbrengst per klik over te gaan.

### Kosten doorgeven per klik {#section_DEB889470F7D4360B5CEA85FD05DEDFA}

Gebruik een redirector om de kosten per klik door te geven.

>[!NOTE]
>
>De beste manier is om de kostenwaarde te bepalen met behulp van de **score per bezoek** -betrokkenheidsmaatstaf.

Voeg toe `&mboxPageValue=-value` aan URL. Noteer de negatieve waarde.

Voorbeeld: Voor een kosten van 0,10 cent per klik:

```
https://<your_clientcode>.tt.omtrdc.net/​m2/yourclientcode/ubox/​page?mbox=redirectorlink_456
&mboxPageValue=-0.1&mboxDefault=​https://www.yourcompany.com/usualdestination.htm
```

### Ontvangsten doorgeven per klik {#section_3E48AC465E7D42DAAC51B4BFF83F64B1}

Gebruik een redirector om de opbrengst per klik over te gaan.

>[!NOTE]
>
>De beste praktijk is om de opbrengstwaarde te bepalen gebruikend de metrisch van de **Score per bezoek** overeenkomst.

Voeg toe `&mboxPageValue=value` aan URL.

Voorbeeld: Voor een opbrengst van 0,10 cent per klik.

```
https://<​your_clientcode>​​​​.tt​​.omtrdc​.net/​​m2/​yourclientcode/​ubox/​​​page?mbox=redirectorlink_456
&mboxPageValue=0.1​&mbox​Default=​​http%3A%2F%2Fwww%2E​yourcompany%2Ecom​%2Fusualdestination%2Ehtm
```
