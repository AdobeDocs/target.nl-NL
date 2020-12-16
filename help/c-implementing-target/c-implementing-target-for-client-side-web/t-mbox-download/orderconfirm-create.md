---
keywords: order confirmation;orderConfirmPage
description: In het vak Bevestiging van bestelling worden gegevens over bestellingen op uw site vastgelegd en wordt rapportage op basis van inkomsten en bestellingen toegestaan. Met het selectievakje Order Confirmation (Bevestiging bestellen) kunt u ook aanbevelingen uitvoeren, zoals "People that purchase product x also purchase product y." (Personen die het product hebben gekocht).
title: Een bevestigingsbox voor bestellingen maken - mbox.js
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 19%

---


# Een bevestigingsbox voor bestelling maken - mbox.js{#create-an-order-confirmation-mbox-mbox-js}

In het vak Bevestiging van bestelling worden gegevens over bestellingen op uw site vastgelegd en wordt rapportage op basis van inkomsten en bestellingen toegestaan. Met het selectievakje Order Confirmation (Bevestiging bestellen) kunt u ook aanbevelingen uitvoeren, zoals &quot;People that purchase product x also purchase product y.&quot; (Personen die het product hebben gekocht).

>[!NOTE]
>
>* Als gebruikers aankopen doen op uw website, raden we u aan een bevestigingsvak voor bestellingen te implementeren, zelfs als u Analytics for Target (A4T) gebruikt voor uw rapportage.
   >
   >
* U kunt ook een bevestigingsvak voor bestellingen maken voor at.js 1.*dezelfde* methode gebruiken; de  [!DNL at.js] methode heeft echter de voorkeur . Zie [Conversies bijhouden](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053) voor meer informatie.
   >
   >
* Als u at.js 2 gebruikt.*x*,  `mboxCreate` wordt niet meer ondersteund. Voor bevestiging van de bestelling met behulp van at.js 2.*x*, gebruik volgende het volgen-verwante APIs:  [trackEvent() ](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) en  [sendNotifications()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).


1. Voeg op de pagina met orderdetails het mbox-script in volgens het onderstaande model.
1. Vervang de WOORDEN IN KAPITAALLETTERS door dynamische of statische waarden uit de catalogus.

   >[!NOTE]
   >
   >Gebruik komma&#39;s als scheidingsteken om meerdere product-id&#39;s van elkaar te scheiden.

   **Tip:** U kunt ook ordergegevens in een willekeurige box doorgeven (hiervoor hoeft geen naam te worden gegeven  `orderConfirmPage`). U kunt ook ordergegevens in meerdere vakken in dezelfde campagne doorgeven.

   ```
   <div class="mboxDefault"> 
      <!-- CONTENT TO SHOW IF NO OFFERS AVAILABLE. --> 
   </div> 
   <script type="text/javascript">    
      mboxCreate('orderConfirmPage', 
      'productPurchasedId=PRODUCT ID FROM YOUR ORDER PAGE, PRODUCT ID2, PRODUCT ID3', 
      'orderTotal=ORDER TOTAL FROM YOUR ORDER PAGE', 
      'orderId=ORDER ID FROM YOUR ORDER PAGE'); 
   </script> 
   ```

In het bevestigingsvak Volgorde worden de volgende parameters gebruikt:

| Parameter | Beschrijving |
|--- |--- |
| `orderId` | Unieke waarde om een order voor het tellen van conversies te identificeren.<br>De `orderId` moet uniek zijn. Dubbele orders worden genegeerd in rapporten. |
| `orderTotal` | Monetaire waarde van de aankoop.<br>Geef het valutasymbool niet door. Gebruik een decimaalteken (geen komma) om decimale waarden aan te geven. |
| `productPurchasedId` (Optioneel) | Door komma&#39;s gescheiden lijst met product-id&#39;s die in de order zijn aangeschaft.<br>Deze product-id&#39;s worden in het auditrapport weergegeven ter ondersteuning van aanvullende rapportanalyse. |