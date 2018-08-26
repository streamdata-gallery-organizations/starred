{
  "info": {
    "name": "Starred Anonymous Invitation Link",
    "_postman_id": "9154b4d6-b633-4ee6-be61-da5e938c6352",
    "description": "Generate a link to a Starred survey form of your choice. \nGenerate from 1 up to, and including 100 anonymous links. (Anonymous is for when the recipient's email is not known)\n\n**Request Parameters**\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `amount` | Optional | Amount of invitation links desired. (Defaults to 1) |\n| `tags` | Optional | Any number of invitation tags can be listed. It is in key - value format, e.g. tag1=tag1 |",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "e283a2a3-3328-41ac-bb78-59c649cb6ca5",
          "name": "InvitationLinksAnonymousPost",
          "request": {
            "url": "http://example.com/InvitationLinks/anonymous",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Generate a link to a Starred survey form of your choice. \nGenerate from 1 up to, and including 100 anonymous links. (Anonymous is for when the recipient's email is not known)\n\n**Request Parameters**\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `amount` | Optional | Amount of invitation links desired. (Defaults to 1) |\n| `tags` | Optional | Any number of invitation tags can be listed. It is in key - value format, e.g. tag1=tag1 |"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "abba35c2-825d-43c5-9d91-783116ed4aef"
            }
          ]
        }
      ]
    }
  ]
}