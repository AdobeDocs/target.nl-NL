---
keywords: e-mail;adbox;e-mailafbeeldingsadbox
description: Leer hoe u Adobe Target kunt gebruiken om afbeeldingen dynamisch te testen in e-mail en deze afbeeldingen zelfs direct te wijzigen wanneer iemand de e-mail opent.
title: Hoe test ik een e-mailafbeeldingsadbox?
feature: Implement Email
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---


# Een e-mailafbeelding testen in een adbox{#test-an-email-image-adbox}

Test afbeeldingen dynamisch in een e-mailbericht en wijzig deze afbeeldingen zelfs als iemand het e-mailbericht opent.

Redirecteurs kunnen in e-mails worden gebruikt om kliks te volgen en dynamisch te controleren welke landende pagina mensen bereiken.

Het testen van afbeeldingen via e-mail wordt uitgevoerd met gewijzigde versies van bijschriften. Omdat e-mailclients het niet toestaan dat cookies worden ingesteld, moet voor elke e-mail een unieke id worden gegenereerd. Dit aantal wordt toegevoegd aan adbox URL en aan om het even welke redirecteurs die in e-mail worden gebruikt om kliks van e-mail te volgen.

>[!NOTE]
>
>Hoewel Target technisch gesproken optimalisatie van afbeeldingen kan bieden bij een open tijd, verwerkt elke e-mailclient caching anders, zodat het succes anders wordt. Ongeacht de e-mailserviceprovider die wordt gebruikt, bepaalt de e-mailclient die de eindgebruiker gebruikt om de e-mail te openen (Gmail-app, Outlook, Hotmail, enzovoort) of de afbeelding daadwerkelijk wordt opgehaald tijdens een open-time periode. Gmail plaatst bijvoorbeeld alles in cache, zodat de afbeelding die de eindgebruiker ziet, afhankelijk is van de vraag of Gmail de afbeelding wil aanroepen en in cache plaatst.

**Voorbeeldcode voor een e-mailafbeeldingsadbox:**

```
<img src="https://{clientcode}.tt.omtrdc.net/m2/​{clientcode}/ubox/​image?
mbox={email_header}&
mboxDefault=​{http%3A%2F%2Fwww.domain.com%2Fheader.jpg}&
mboxXDomain=disabled&
mboxSession={123456}&
mboxPC={123456}” border=:"0"/>
```

Waar de onderstaande waarden specifiek voor u zijn:

| Waarde | Beschrijving |
|--- |--- |
| clientcode | De clientcode van uw bedrijf. Zoek dit in uw bestand at.js of mbox.js dat als `clientCode='yourclientcode'` wordt vermeld. Dit is allemaal kleine letters en heeft geen speciale tekens. |
| image | Het type voorstel. Het is altijd &quot;beeld&quot;voor grafische advertenties en &quot;pagina&quot;voor bestuurders. |
| email_header | De naam van het selectievakje. |
| `mboxDefault=http%3A%2F%2Fwww.domain.com%2Fheader.jpg` | Vereist. Vervang de URL door de juiste standaardinhoud voor uw adbox. Dit moet een absolute verwijzing zijn en moet URL-gecodeerd zijn. |
| `mboxXDomain=disabled` | Hiermee wordt aan Doel doorgegeven dat er niet moet worden geprobeerd een cookie in te stellen. |
| `mboxSession=123456` en  `mboxPC=123456` | Twee waarden die door Doel worden vereist om het profiel van deze gebruiker samen te voegen met het bestaande profiel voor uw site. 123456 is de unieke id die per e-mail wordt gegenereerd. Voeg deze waarde dynamisch in elke adbox en redirector-URL in. Dit nummer moet uniek zijn voor elke e-mail die naar elke persoon wordt verzonden. Als een wekelijkse e-mail naar 1.000 mensen wordt verzonden, moeten er 1.000 unieke id&#39;s worden gegenereerd.<br>Het unieke herkenningsteken per e-mail moet aan mboxSession en mboxPC in elke adbox en redirector URL worden toegewezen. De aanbevolen notatie voor deze id is timestamp-NNNN waarbij NNNNN een willekeurig getal van 5 cijfers is, maar elke alfanumerieke notatie werkt. Sommige massa-e-maildiensten en om het even welke programmeertaal kunnen dit unieke herkenningsteken produceren. |
