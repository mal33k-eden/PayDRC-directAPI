## B2C [CREDIT ACTOIN]

In other to move money from a merchant's wallet to a customer's mobile money wallet, you send `credit` action request.
 
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
    	"action":"credit",
    	"reference":"asdfghjk123456890",
    	"method":"orange",
    	"amount":"10",
    	"currency":"CDF",
    	"customer_number":"08xxxxxxxx",
    	"firstname":"eden",
    	"lastname":"test",
    	"email":"etartey@yahoo.com"
    }
```

## Success Responses
 

**Code** : `200 OK`
 
 
```json
{
    "Status": "Success",
    "Comment": "Transaction Received Successfully",
    "Reference": "asdfghjk123456890",
    "Customer_Number": "08xxxxxxxx",
    "Amount": 10,
    "Currency": "CDF"
}
```


**other Informations** : 

FreshPay tries to keep track of all customers that make transactions on their platforms: So merchants who will have to on-board their customers to the FreshPay Platform
if it is a first time transactions of the customer with the FreshPay platform.
 