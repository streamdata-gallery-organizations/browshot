{
  "info": {
    "name": "Browshot Get information about your account",
    "_postman_id": "f6b1f4e2-8142-48f4-a499-10449ffec08c",
    "description": "Get information about your account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Account",
      "item": [
        {
          "id": "6fc25044-bd71-4eab-b005-3fb5077a79b9",
          "name": "GetAccountInfo",
          "request": {
            "url": "http://api.browshot.com/api/v1/account/info?details=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get information about your account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d7b283ee-6793-4d31-9b5e-908ff8afc370"
            }
          ]
        }
      ]
    }
  ]
}