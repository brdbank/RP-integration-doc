# API Documentation

## Base URL

[https://educapi.brd.rw](https://educapi.brd.rw)

## Endpoint

`/api/auth/login`

## HTTP Method

POST

## Request Body
```json
{
  "username": "string",
  "password": "string"
}
```


This endpoint will allow allow you to receive an autentication tocken for each of your request if the usename and passowrd provided are correct

## Response body

```json
{
  "status": 200,
  "message": "Successfully loggedIn",
  "data": {
    "user": {
      "id": 5,
      "firstName": "xxxxxx",
      "lastName": "xxxxx",
      "username": "xxxxxxxxx",
      "roleId": 5,
      "isActive": true,
      "loggedInAt": "2023-04-24T12:20:30.316Z",
      "createdAt": "2023-04-24T10:04:21.289Z",
      "updatedAt": "2023-04-24T12:20:30.317Z"
    },
    "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
  }
}
```
---------------------------------------------------------------------------------------------------------------------------------------------

`/api/payments/rp/paid-list`

## HTTP Method

POST

## Request Body

The request requires a JSON object in the body with the following format:

Filters (registrationNumber, beneficiaryAccountNumber, names, paymentPeriod)


```json
{
    {{filter}} : {{value}}
}
```

The filster avavailable are : registrationNumber, beneficiaryAccountNumber, names, paymentPeriod

## Headers

The API now requires JWT authentication. Pass the JWT token received on login in the header as Authorization. The token will be provided separately by the API provider (Minuza). 

## Example Request

```bash
Authorization: Barea xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## Response Body

The response is a JSON object with the following format:

```json
{
  "page": 0,
  "limit": 10,
  "totalPages": 81,
  "totalCount": 801,
  "totalOnPage": 10,
  "row": [
    {
      "postName": "xxxxxx",
      "surName": "xxxxx",
      "registrationNumber": "xxxx",
      "accountNumber": "xxxx-xxxx",
      "amount":xxxxx,
      "paymentPeriod": "xx-xxx",
      "academicYear": "xxxx-xxxx",
      "paymentChannel": "xxxxx",
      "paymentStatus": "xxxxxx",
      "paidDate": "xxxxxxxxZ",
      "collegeName": "xxxx xxx Regional xx xxxxx",
      "collegeAccronym": "xxxx xxxx",
      "hliName": "xxxxxxxxx xxxxxx",
      "hliAccronym": "RP",
      "lastIntegrationReportDate": "2022-12-xxxxxx:26:xx.790Z"
    },
  ]
}
```


---------------------------------------------------------------------------------------------------------------------------------------------

`/api/payments/rp/nonpaid-list`

## HTTP Method

POST

## Request Body

The request requires a JSON object in the body with the following format:

Filters (registrationNumber, beneficiaryAccountNumber, names, paymentPeriod)


```json
{
    {{filter}} : {{value}}
}
```

The filster avavailable are : registrationNumber, beneficiaryAccountNumber, names, paymentPeriod

## Headers

The API now requires JWT authentication. Pass the JWT token received on login in the header as Authorization. The token will be provided separately by the API provider (Minuza). 

## Example Request

```bash
Authorization: Barea xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## Response Body

The response is a JSON object with the following format:

```json
{
  "page": 0,
  "limit": 10,
  "totalPages": 81,
  "totalCount": 801,
  "totalOnPage": 10,
  "row": [
    {
      "postName": "xxxxxx",
      "surName": "xxxxx",
      "registrationNumber": "xxxx",
      "accountNumber": "xxxx-xxxx",
      "amount":xxxxx,
      "paymentPeriod": "xx-xxx",
      "academicYear": "xxxx-xxxx",
      "paymentChannel": "xxxxx",
      "paymentStatus": "xxxxxx",
      "paidDate": "xxxxxxxxZ",
      "collegeName": "xxxx xxx Regional xx xxxxx",
      "collegeAccronym": "xxxx xxxx",
      "hliName": "xxxxxxxxx xxxxxx",
      "hliAccronym": "RP",
      "lastIntegrationReportDate": "2022-12-xxxxxx:26:xx.790Z"
    },
  ]
}
```
