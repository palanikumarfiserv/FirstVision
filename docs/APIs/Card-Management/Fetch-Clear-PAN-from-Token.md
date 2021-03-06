# Fetch Clear PAN from Token

This service is used to fetch the clear pan for the requested First Vision's Token PAN.

## Endpoint

`GET /v1/cards/{cardNumber}/clearPan`

## Payload Example

### Request Payload

>Shoud be empty.  
***The Business Unit and AccountNumber should be sent as query parameters.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/clearPan).

The below table identifies the required query parameters in the request payload.

| Variable | Type | Length | Description |
| -------- | :--: | :------------: | ------------------ |
| `businessUnit` | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

>Shoud be empty.
***The Business Unit and cardNumber should be sent as query parameters.***

### Error Response Payload

```json
{
  "errorCode": "V5CL4002AS",
  "errorMessage": "Token number not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CL4001EA` |Invalid Business Unit|
|`V5CL4002EA` |Invalid card number|
|`V5CL4001AS` |Business Unit not found|
|`V5CL4002AS` |Token number not found|
