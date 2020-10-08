---
title: payg

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python
  - javascript


includes:
  - errors

search: true

code_clipboard: true
---

# PayGv2 Documentation


version : V1

baseUri : uatapi.payg.in/payment/api/order/

protocols : HTTPS

mediaType : application/json





> /create post:


```python
# PYTHON EXAMPLE

import requests

url = 'https://uatapi.payg.in/payment/api/order/create'
```

```shell
# CURL EXAMPLE

curl -X POST "uatapi.payg.in/payment/api/order/create" \
	-H "Authorization: key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"" \
	-d @request_body
```

```javascript
# JAVA EXAMPLE

const http = require('https');
const init = {
  host: 'uatapi.payg.in',
  path: '/payment/api/order/create',
  method: 'POST',
  headers: {
    'Authorization': 'key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"'
  }
};
```
# / Create

## /Create post

POST: /create

# Header Parameters

> REQUEST HEADERS

```python

headers = {'Authorization': 'key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"'}
```

```shell

Authorization: key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"
```

```javascript

const callback = function(response) {
  let result = Buffer.alloc(0);
  response.on('data', function(chunk) {
    result = Buffer.concat([result, chunk]);
  });
  
  response.on('end', function() {
    // result has response body buffer
    console.log(result.toString());
  });
};

const req = http.request(init, callback);
```

> REQUEST BODY:


### Authorization

Property | Value 
--------- | -------
required | true 
type | string 
example | key:"Authorization" value:"OTcwNDU0MTVkMzkyNDlhODk5NmM0MmUxYzk1OThlZDE6NDNiNDI1YTYxNDhiNGQ5NDk4YTQ5YmU2MTMyMThkYjc6TTo3ODc1"

```python

body = """{
  "OrderKeyId": "",
  "MerchantKeyId": 2,
  "ApiKey": "",
  "UniqueRequestId": "ae021dg",
  "OrderAmount": 5,
  "OrderType": "",
  "OrderId": "",
  "OrderStatus": "",
  "OrderAmountData": {
    "AmountDetail": [
      {
        "AmountTypeDesc": "",
        "Amount": 0
      }
    ]
  },
  "ProductData": "",
  "NextStepFlowData": "",
  "TransactionData": {
    "AcceptedPaymentTypes": "",
    "PaymentType": "",
    "SurchargeType": "",
    "SurchargeValue": 0,
    "Card": {
      "CardNo": "",
      "CardType": 0,
      "NameOnCard": "",
      "ExpiryDate": "",
      "Cvv": "",
      "TrackData": "",
      "ChipData": "",
      "PassCode": "",
      "Ksn": "",
      "PinBlock": "",
      "AdditionalData1": "",
      "AdditionalData2": ""
    },
    "Ach": {
      "BankCodeType": 0,
      "BankCode": "",
      "AccountNo": "",
      "BankAccountType": 0,
      "CheckNo": "",
      "SecCode": 1,
      "MicrData": "",
      "CheckFrontImage": "",
      "CheckBackImage": "",
      "NameOnCard": "",
      "First6Digit": "",
      "Last4Digit": ""
    },
    "Wallet": {
      "BarQrCode": "",
      "UserName": "",
      "WalletType": 1,
      "FirstName": "",
      "LastName": ""
    },
    "Upi": {
      "Vpa": "",
      "AccountNumber": "",
      "Ifsc": "",
      "AdhAadhaarNo": ""
    },
    "Card3DSecure": {
      "AuthenticateTransaction": true,
      "Secure3DAuthenticationRequest": {
        "MD": "",
        "PaRes": ""
      }
    },
    "RefTransactionId": "",
    "IndustrySpecicationCode": "",
    "PartialPaymentOption": ""
  },
  "CustomerData": {
    "CustomerId": "12",
    "CustomerNotes": "Sample",
    "FirstName": "First",
    "LastName": "Last",
    "MobileNo": "9011001100",
    "Email": "test@gmail.com",
    "EmailReceipt": true,
    "BillingAddress": "",
    "BillingCity": "",
    "BillingState": "",
    "BillingCountry": "",
    "BillingZipCode": "",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "IntegrationData": {
    "UserName": "",
    "Source": "",
    "IntegrationType": "",
    "HashData": "",
    "PlatformId": ""
  },
  "ShipmentData": "",
  "RequestDateTime": "",
  "RedirectUrl": ""
}"""

req = requests.post(url, headers=headers, data=body)

print(req.status_code)
print(req.headers)
print(req.text)
```

```shell

{
  "OrderKeyId": "",
  "MerchantKeyId": 2,
  "ApiKey": "",
  "UniqueRequestId": "ae021dg",
  "OrderAmount": 5,
  "OrderType": "",
  "OrderId": "",
  "OrderStatus": "",
  "OrderAmountData": {
    "AmountDetail": [
      {
        "AmountTypeDesc": "",
        "Amount": 0
      }
    ]
  },
  "ProductData": "",
  "NextStepFlowData": "",
  "TransactionData": {
    "AcceptedPaymentTypes": "",
    "PaymentType": "",
    "SurchargeType": "",
    "SurchargeValue": 0,
    "Card": {
      "CardNo": "",
      "CardType": 0,
      "NameOnCard": "",
      "ExpiryDate": "",
      "Cvv": "",
      "TrackData": "",
      "ChipData": "",
      "PassCode": "",
      "Ksn": "",
      "PinBlock": "",
      "AdditionalData1": "",
      "AdditionalData2": ""
    },
    "Ach": {
      "BankCodeType": 0,
      "BankCode": "",
      "AccountNo": "",
      "BankAccountType": 0,
      "CheckNo": "",
      "SecCode": 1,
      "MicrData": "",
      "CheckFrontImage": "",
      "CheckBackImage": "",
      "NameOnCard": "",
      "First6Digit": "",
      "Last4Digit": ""
    },
    "Wallet": {
      "BarQrCode": "",
      "UserName": "",
      "WalletType": 1,
      "FirstName": "",
      "LastName": ""
    },
    "Upi": {
      "Vpa": "",
      "AccountNumber": "",
      "Ifsc": "",
      "AdhAadhaarNo": ""
    },
    "Card3DSecure": {
      "AuthenticateTransaction": true,
      "Secure3DAuthenticationRequest": {
        "MD": "",
        "PaRes": ""
      }
    },
    "RefTransactionId": "",
    "IndustrySpecicationCode": "",
    "PartialPaymentOption": ""
  },
  "CustomerData": {
    "CustomerId": "12",
    "CustomerNotes": "Sample",
    "FirstName": "First",
    "LastName": "Last",
    "MobileNo": "9011001100",
    "Email": "test@gmail.com",
    "EmailReceipt": true,
    "BillingAddress": "",
    "BillingCity": "",
    "BillingState": "",
    "BillingCountry": "",
    "BillingZipCode": "",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "IntegrationData": {
    "UserName": "",
    "Source": "",
    "IntegrationType": "",
    "HashData": "",
    "PlatformId": ""
  },
  "ShipmentData": "",
  "RequestDateTime": "",
  "RedirectUrl": ""
}
```

```javascript

const body = `{
  "OrderKeyId": "",
  "MerchantKeyId": 2,
  "ApiKey": "",
  "UniqueRequestId": "ae021dg",
  "OrderAmount": 5,
  "OrderType": "",
  "OrderId": "",
  "OrderStatus": "",
  "OrderAmountData": {
    "AmountDetail": [
      {
        "AmountTypeDesc": "",
        "Amount": 0
      }
    ]
  },
  "ProductData": "",
  "NextStepFlowData": "",
  "TransactionData": {
    "AcceptedPaymentTypes": "",
    "PaymentType": "",
    "SurchargeType": "",
    "SurchargeValue": 0,
    "Card": {
      "CardNo": "",
      "CardType": 0,
      "NameOnCard": "",
      "ExpiryDate": "",
      "Cvv": "",
      "TrackData": "",
      "ChipData": "",
      "PassCode": "",
      "Ksn": "",
      "PinBlock": "",
      "AdditionalData1": "",
      "AdditionalData2": ""
    },
    "Ach": {
      "BankCodeType": 0,
      "BankCode": "",
      "AccountNo": "",
      "BankAccountType": 0,
      "CheckNo": "",
      "SecCode": 1,
      "MicrData": "",
      "CheckFrontImage": "",
      "CheckBackImage": "",
      "NameOnCard": "",
      "First6Digit": "",
      "Last4Digit": ""
    },
    "Wallet": {
      "BarQrCode": "",
      "UserName": "",
      "WalletType": 1,
      "FirstName": "",
      "LastName": ""
    },
    "Upi": {
      "Vpa": "",
      "AccountNumber": "",
      "Ifsc": "",
      "AdhAadhaarNo": ""
    },
    "Card3DSecure": {
      "AuthenticateTransaction": true,
      "Secure3DAuthenticationRequest": {
        "MD": "",
        "PaRes": ""
      }
    },
    "RefTransactionId": "",
    "IndustrySpecicationCode": "",
    "PartialPaymentOption": ""
  },
  "CustomerData": {
    "CustomerId": "12",
    "CustomerNotes": "Sample",
    "FirstName": "First",
    "LastName": "Last",
    "MobileNo": "9011001100",
    "Email": "test@gmail.com",
    "EmailReceipt": true,
    "BillingAddress": "",
    "BillingCity": "",
    "BillingState": "",
    "BillingCountry": "",
    "BillingZipCode": "",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  },
  "UserDefinedData": {
    "UserDefined1": "",
    "UserDefined2": "",
    "UserDefined3": "",
    "UserDefined4": "",
    "UserDefined5": "",
    "UserDefined6": "",
    "UserDefined7": "",
    "UserDefined8": "",
    "UserDefined9": "",
    "UserDefined10": "",
    "UserDefined11": "",
    "UserDefined12": "",
    "UserDefined13": "",
    "UserDefined14": "",
    "UserDefined15": "",
    "UserDefined16": "",
    "UserDefined17": "",
    "UserDefined18": "",
    "UserDefined19": "",
    "UserDefined20": ""
  },
  "IntegrationData": {
    "UserName": "",
    "Source": "",
    "IntegrationType": "",
    "HashData": "",
    "PlatformId": ""
  },
  "ShipmentData": "",
  "RequestDateTime": "",
  "RedirectUrl": ""
}`;
req.write(body);
req.end();
```

## Possible Responses

200

Status Success

400

Bad input parameter. Error message should indicate which one and why.

401

The client passed in the invalid Auth token. Client should refresh the token and then try again.

403

Merchant doesn’t exist. * Merchant not registered. * Application try to access to properties not belong to an App. * Application try to trash/purge root node. * Application try to update contentProperties. * Operation is blocked (for third-party apps). * Merchant account over quota.

404

Resource not found.

405

The resource doesn't support the specified HTTP verb.

409

Conflict

411

The Content-Length header was not specified.

412

Precondition failed.

429

Too many request for rate limiting.

500

Servers are not working as expected. The request is probably valid but needs to be requested again later.

503

Service Unavailable.

> Type 

> any


> RESPONSE BODY

>200

```python

"OrderKeyId": ""
"MerchantKeyId": 2
"ApiKey": ""
"UniqueRequestId": "ae021dg"
"OrderAmount": 5.0
"OrderType": ""
"OrderId": ""
"OrderStatus": ""
"OrderAmountData":
  "AmountDetail":
    -
      "AmountTypeDesc": ""
      "Amount": 0
"ProductData": ""
"NextStepFlowData": ""
"TransactionData":
  "AcceptedPaymentTypes": ""
  "PaymentType": ""
  "SurchargeType": ""
  "SurchargeValue": 0
  "Card":
    "CardNo": ""
    "CardType": 0
    "NameOnCard": ""
    "ExpiryDate": ""
    "Cvv": ""
    "TrackData": ""
    "ChipData": ""
    "PassCode": ""
    "Ksn": ""
    "PinBlock": ""
    "AdditionalData1": ""
    "AdditionalData2": ""
  "Ach":
    "BankCodeType": 0
    "BankCode": ""
    "AccountNo": ""
    "BankAccountType": 0
    "CheckNo": ""
    "SecCode": 1
    "MicrData": ""
    "CheckFrontImage": ""
    "CheckBackImage": ""
    "NameOnCard": ""
    "First6Digit": ""
    "Last4Digit": ""
  "Wallet":
    "BarQrCode": ""
    "UserName": ""
    "WalletType": 1
    "FirstName": ""
    "LastName": ""
  "Upi":
    "Vpa": ""
    "AccountNumber": ""
    "Ifsc": ""
    "AdhAadhaarNo": ""
  "Card3DSecure":
    "AuthenticateTransaction": true
    "Secure3DAuthenticationRequest":
      "MD": ""
      "PaRes": ""
  "RefTransactionId": ""
  "IndustrySpecicationCode": ""
  "PartialPaymentOption": ""
"CustomerData":
  "CustomerId": "12"
  "CustomerNotes": "Sample"
  "FirstName": "First"
  "LastName": "Last"
  "MobileNo": "9011001100"
  "Email": "test@gmail.com"
  "EmailReceipt": true
  "BillingAddress": ""
  "BillingCity": ""
  "BillingState": ""
  "BillingCountry": ""
  "BillingZipCode": ""
  "ShippingFirstName": ""
  "ShippingLastName": ""
  "ShippingAddress": ""
  "ShippingCity": ""
  "ShippingState": ""
  "ShippingCountry": ""
  "ShippingZipCode": ""
  "ShippingMobileNo": ""
"UserDefinedData":
  "UserDefined1": ""
  "UserDefined2": ""
  "UserDefined3": ""
  "UserDefined4": ""
  "UserDefined5": ""
  "UserDefined6": ""
  "UserDefined7": ""
  "UserDefined8": ""
  "UserDefined9": ""
  "UserDefined10": ""
  "UserDefined11": ""
  "UserDefined12": ""
  "UserDefined13": ""
  "UserDefined14": ""
  "UserDefined15": ""
  "UserDefined16": ""
  "UserDefined17": ""
  "UserDefined18": ""
  "UserDefined19": ""
  "UserDefined20": ""
"IntegrationData":
  "UserName": ""
  "Source": ""
  "IntegrationType": ""
  "HashData": ""
  "PlatformId": ""
"ShipmentData": ""
"RequestDateTime": ""
"RedirectUrl": ""
```

```shell
{
  "OrderKeyId": "200915M292UAA10030",
  "MerchantKeyId": 292,
  "UniqueRequestId": "AA10030",
  "OrderType": "PAYMENT",
  "OrderAmount": 15,
  "OrderId": "225",
  "OrderStatus": null,
  "OrderPaymentStatus": 0,
  "OrderPaymentStatusText": null,
  "PaymentStatus": 0,
  "PaymentTransactionId": null,
  "PaymentResponseCode": 0,
  "PaymentApprovalCode": null,
  "PaymentResponseText": null,
  "PaymentMethod": null,
  "PaymentAccount": null,
  "OrderNotes": null,
  "PaymentDateTime": null,
  "UpdatedDateTime": null,
  "PaymentProcessUrl": "https://uat.payg.in/payment/payment?orderid=200915M292UAA10030",
  "OrderPaymentCustomerData": {
    "FirstName": "test",
    "LastName": null,
    "Address": null,
    "City": null,
    "State": null,
    "ZipCode": null,
    "Country": null,
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "UserId": null,
    "IpAddress": null
  },
  "UpiLink": "&sign=",
  "CustomerData": {
    "CustomerId": "1",
    "CustomerNotes": null,
    "FirstName": "test",
    "LastName": "m",
    "MobileNo": "33333333333",
    "Email": "praveen@gmail.com",
    "EmailReceipt": false,
    "BillingAddress": "Telangana",
    "BillingCity": "test",
    "BillingState": "TS",
    "BillingCountry": "IN",
    "BillingZipCode": "TEST",
    "ShippingFirstName": "",
    "ShippingLastName": "",
    "ShippingAddress": "",
    "ShippingCity": "",
    "ShippingState": "",
    "ShippingCountry": "",
    "ShippingZipCode": "",
    "ShippingMobileNo": ""
  }
}
```

```javascript

"OrderKeyId": ""
"MerchantKeyId": 2
"ApiKey": ""
"UniqueRequestId": "ae021dg"
"OrderAmount": 5.0
"OrderType": ""
"OrderId": ""
"OrderStatus": ""
"OrderAmountData":
  "AmountDetail":
    -
      "AmountTypeDesc": ""
      "Amount": 0
"ProductData": ""
"NextStepFlowData": ""
"TransactionData":
  "AcceptedPaymentTypes": ""
  "PaymentType": ""
  "SurchargeType": ""
  "SurchargeValue": 0
  "Card":
    "CardNo": ""
    "CardType": 0
    "NameOnCard": ""
    "ExpiryDate": ""
    "Cvv": ""
    "TrackData": ""
    "ChipData": ""
    "PassCode": ""
    "Ksn": ""
    "PinBlock": ""
    "AdditionalData1": ""
    "AdditionalData2": ""
  "Ach":
    "BankCodeType": 0
    "BankCode": ""
    "AccountNo": ""
    "BankAccountType": 0
    "CheckNo": ""
    "SecCode": 1
    "MicrData": ""
    "CheckFrontImage": ""
    "CheckBackImage": ""
    "NameOnCard": ""
    "First6Digit": ""
    "Last4Digit": ""
  "Wallet":
    "BarQrCode": ""
    "UserName": ""
    "WalletType": 1
    "FirstName": ""
    "LastName": ""
  "Upi":
    "Vpa": ""
    "AccountNumber": ""
    "Ifsc": ""
    "AdhAadhaarNo": ""
  "Card3DSecure":
    "AuthenticateTransaction": true
    "Secure3DAuthenticationRequest":
      "MD": ""
      "PaRes": ""
  "RefTransactionId": ""
  "IndustrySpecicationCode": ""
  "PartialPaymentOption": ""
"CustomerData":
  "CustomerId": "12"
  "CustomerNotes": "Sample"
  "FirstName": "First"
  "LastName": "Last"
  "MobileNo": "9011001100"
  "Email": "test@gmail.com"
  "EmailReceipt": true
  "BillingAddress": ""
  "BillingCity": ""
  "BillingState": ""
  "BillingCountry": ""
  "BillingZipCode": ""
  "ShippingFirstName": ""
  "ShippingLastName": ""
  "ShippingAddress": ""
  "ShippingCity": ""
  "ShippingState": ""
  "ShippingCountry": ""
  "ShippingZipCode": ""
  "ShippingMobileNo": ""
"UserDefinedData":
  "UserDefined1": ""
  "UserDefined2": ""
  "UserDefined3": ""
  "UserDefined4": ""
  "UserDefined5": ""
  "UserDefined6": ""
  "UserDefined7": ""
  "UserDefined8": ""
  "UserDefined9": ""
  "UserDefined10": ""
  "UserDefined11": ""
  "UserDefined12": ""
  "UserDefined13": ""
  "UserDefined14": ""
  "UserDefined15": ""
  "UserDefined16": ""
  "UserDefined17": ""
  "UserDefined18": ""
  "UserDefined19": ""
  "UserDefined20": ""
"IntegrationData":
  "UserName": ""
  "Source": ""
  "IntegrationType": ""
  "HashData": ""
  "PlatformId": ""
"ShipmentData": ""
"RequestDateTime": ""
"RedirectUrl": ""
```

> Type:

> any
  