These API docs cover v1.0 of the [Arbon](https://www.arbon.one/) Receipt API.

# Quick Start

## 1. Request access to Arbon Sandbox
Contact us via email contact@arbon.one to get in touch.

## 2. Grab your API Key
We will share the Sandbox API Access Key with you upon your request.

## 3. Make your first request to offset Carbon
Currently there is only one endpoint that supports Carbon offset functionality. See the request template and the required parameters explained below:

### Request template
```
https://dev-api.arbon.one/v1/offset/?access_token={access_token}&amount={amount}&reason={reason}
```

### Request parameters
- **{access_token}**

    `int` Arbon API key.

    Example: `access_token=8534060ab04240b88ebe8715b27ca1f1`

- **{amount}** `int`
    Amount of CO2 to offset, in kilograms.

    Example: `500`

- **{reason}** `string`
    Reason for CO2 tokens being offset. This can be an account ID, a transaction ID or whatever you want.

    Example: `hosting account #1234`

## Response
### Status: **200 - OK**

Successful response will return a transaction hash on the respective network. The example below returns the hash of the transaction on the [Mumbai](https://mumbai.polygonscan.com/) test network. The link to see the transaction details will be: https://mumbai.polygonscan.com/tx/0x1246d8be97194f6846c8c92103211661a69900985c6936f30b578330fdd84b4a

```
{
  "hash": "0x1246d8be97194f6846c8c92103211661a69900985c6936f30b578330fdd84b4a",
  "receipt": "https://dev-api.arbon.one/v1/receipt/tx/0x1246d8be97194f6846c8c92103211661a69900985c6936f30b578330fdd84b4a"
}
```
### Status: 400 - Bad Request
```
{
  "statusCode": 400,
  "message": [
    "token should not be empty",
    "token must be a string",
    "amount must be a number conforming to the specified constraints"
  ],
  "error": "Bad Request"
}
```

### Status: 401 - Unauthorized
```
{
  "statusCode": 401,
  "message": "Unauthorized"
}
```

# Embed Receipt into your website

## Embed an interactive image (Recommended)
Receipt SVG image contains links to blockchain transaction and to some additional information to help better understand transaction details. To make sure the content of the receipt is interative and the links are clickable, use the following code to embed the receipt:

```html
<object type="image/svg+xml" data="https://dev-api.arbon.one/v1/receipt/tx/{transaction_hash}"></object>
```
NOTE: replace `{transaction_hash}` with the hash of the actual transaction.

## Embed a static image
In case, for some reason, you cannot embed receipt using an `<object>` tag, you can do it via an `<img>` tag as the following:

```html
<img src="https://dev-api.arbon.one/v1/receipt/tx/{transaction_hash}" />
```

NOTE: replace `{transaction_hash}` with the hash of the actual transaction.

# Sample receipt
<img src="https://dev-api.arbon.one/v1/receipt/tx/0x1246d8be97194f6846c8c92103211661a69900985c6936f30b578330fdd84b4a" />
