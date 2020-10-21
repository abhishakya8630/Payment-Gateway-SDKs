**SDK Payment Flow**
_Different steps as mentioned in the flow diagram._

-  On click of make payment/pay now button,order payload is passed to merchant server by the app.
- Order payload is used to generate checksum by Pine Labs server side utility and secret key(merchant key)on your server. Secret key is shared by Pine labs with merchant. Checksum is a signature used by Pine Labs to ensure the integrity of request.

- Merchant server pass the payload , Dia secret and Dia secret type back to app .Merchant apps pass all the details to 
               Pine Labs android sdk.
- Pine Labs sdk accepts and forward the payload to Pine Labs payment gateway.
- Pine Labs' payment gateway verifies the payload and accept/denied the request. If payload is valid payment options 
              will be displayed.
- Once the customer fill the payment details and complete the payment, then merchant app is notified via call back.
- Merchant verifies the transaction status with transaction status API via server to server call.
 
 **Flow Diagram**
_Step-by-step payment flow is described in below diagram :_
![image](https://user-images.githubusercontent.com/23396167/96772821-4e882480-1401-11eb-89a3-bc0386d98e19.png)
