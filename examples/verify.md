##  VERIFY [VERIFY ACTOIN]

In other to verify the status of a transaction, you send `verify` action request.
 
Transactions are identified by a reference unique to the merchant.



**URL** : `/BaseURL/BaseEndpoint/`

**Method** : `POST`

## Parameters

M => Mandatory
O => Optional
 
       merchant_id (M)
       merchant_secrete (M)
       action (M)
       reference (M)
       method (M)
       amount (M)
       currency (M)
       customer_number (M)
       firstname (O)
       lastname (O)
       email (O)
    

**Available request method** : 

* orange
* airtel
* mpesa


**Available request currencies** : 

* USD
* CDF 

## Request
 
 
```json

    {
        "merchant_id": "qwertyuioiuytrew",
        "merchant_secrete": "qwertyuioiuytrew",
        "action":"verify",
        "reference":"asdfghjk123456890"
    }
```

## Success Responses
 

**Code** : `200 OK`
 
 
```json
{
    "Status": "Success",
    "Comment": "Transaction Found",
    "Trans_Status": "Failed",
    "Currency": "CDF",
    "Amount": "100",
    "Method": "mpesa",
    "Customer_Details": "08xxxxxxxx",
    "Reference": "asdfghjk123456890",
    "Action": "credit"
}
```


**other Informations** : 

FreshPay tries to keep track of all customers that make transactions on their platforms: So merchants who will have to on-board their customers to the FreshPay Platform
if it is a first time transactions of the customer with the FreshPay platform.
 