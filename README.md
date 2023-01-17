These API docs cover v1.0 of the [Arbon](https://www.arbon.one/) API.

# Quick Start

## 1. Request access to Arbon
Contact us via email contact@arbon.one to get in touch.

## 2. Grab your API Key
We will share the Sandbox API Access Key with you uppn your request.

## 3. Make your first request to offset Carbon
Currently there is only one endpoint that supports Carbon offset functionality. See the request template and the required parameters eplained below:

### Request template
```
https://api.arbon.one/v1/offset/?access_token={access_token}&amount={amount}&reason={reason}
```

### Request parameters
- **{access_token}**

    `int` Arbon API key.

    Example: `access_token=8534060ab04240b88ebe8715b27ca1f1`

- **{amount}** `int`
    Amount of CO2 tokens to offset. Each token corresponds to 1kg of CO2.

    Example: `5`

- **{reason}** `string`
    Reason for CO2 tokens being offset.

    Example: `hosting`

## Response
### Status: **200 - OK**

Successful response will return a transaction hash on the respective network. The example below returns the hash of the transaction on the [Mumbai](https://mumbai.polygonscan.com/) test network. The link to see the transaction details will be: https://mumbai.polygonscan.com/tx/0x655ae3e81f07bce450e489f9ccad9ac995d5c45154b72260259f57bee02a2d10

```
{
  "hash": "https://mumbai.polygonscan.com/tx/0x655ae3e81f07bce450e489f9ccad9ac995d5c45154b72260259f57bee02a2d10"
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