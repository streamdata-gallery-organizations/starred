{
  "info": {
    "name": "Starred Send Single Invitation",
    "_postman_id": "e2178c94-8b56-4762-8ec7-72f6dda1339a",
    "description": "Instead of uploading a CSV file, you can also set one recipient per API call by using the following parameters to the URL.\n\n### Request Parameters\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `from` | Required | Email address of the sender, must be a registered email |\n| `recipient` | Required | Email address of the recipient |\n| `firstName` | Required | First name to address the recipient with |\n| `lastName` | Required | Surname to address the recipient with |\n| `template` | Required | Template ID |\n| `language` | Required | The language of the template. For example: nl, en or fr |\n| `reminder` | Optional | Whether or not to send a reminder (1 or 0). Defaults to 1 |",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "55d3ef63-4470-4764-a8d4-0fcad95a7fff",
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
              "id": "08d0413e-9312-4b21-b4f3-f77d674a0792"
            }
          ]
        }
      ]
    },
    {
      "name": "Single",
      "item": [
        {
          "id": "98e08cdb-a45a-41f2-9879-669d85119b52",
          "name": "InvitationLinksSinglePost",
          "request": {
            "url": "http://example.com/InvitationLinks/single",
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
            "description": "It is possible to generate a link to a Starred survey form of your choice. \n\n**Request Parameters**\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `recipient` | Required | Email address of the recipient |\n| `firstName` | Optional | First name to address the recipient with |\n| `lastName` | Optional | Surname to address the recipient with |\n| `tags` | Optional | Any number of invitation tags can be listed. It is in key - value format, e.g. tag1=tag1 |"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6ff2a03e-1be0-4853-b513-ef956f5628c2"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "7e5e7967-3cd5-4dc5-bddd-c35ba4d0f2b5",
          "name": "SendinvitationsCsvPost",
          "request": {
            "url": "http://example.com/sendinvitations/csv",
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
            "description": "With the /sendinvitations call you can link your CRM system to Starred so invitations are sent automatically. This will no longer require any manual action. \n\nYou can also import additional characteristics directly from your CRM so you can start analyzing results for different client groups. \n\nThe parameters on the right are mandatory to make the request succeed.\n\n### Request Parameters\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `from` | Required | Email address of the sender, must be a registered email |\n| `template` | Required | Template ID |\n| `language` | Required | The language of the template. For example: nl, en or fr |\n| `file` | Required | A CSV file formatted as a regular invitation CSV added as a HTTP POST file. |\n| `reminder` | Optional | Whether or not to send a reminder (1 means On, 0 means Off). Defaults to 1 |\n\n### Example curl request\n```\ncurl -F \"file=@testCSV.csv\" https://api.starred.com/sendinvitations\\?company\\={{companyID}}\\&auth\\={{auth}}\\&form\\={{formId}}\\&from\\={{sender}}\\&template\\={{templateId}}\\&language\\={{language}}\n```"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef9bd2d5-b0d5-42b1-b4be-4dd11a30539e"
            }
          ]
        },
        {
          "id": "720c7e7f-0a74-44be-8da0-2bfb8a3d14d0",
          "name": "SendinvitationsPost",
          "request": {
            "url": "http://example.com/sendinvitations",
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
            "description": "Instead of uploading a CSV file, you can also set one recipient per API call by using the following parameters to the URL.\n\n### Request Parameters\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `from` | Required | Email address of the sender, must be a registered email |\n| `recipient` | Required | Email address of the recipient |\n| `firstName` | Required | First name to address the recipient with |\n| `lastName` | Required | Surname to address the recipient with |\n| `template` | Required | Template ID |\n| `language` | Required | The language of the template. For example: nl, en or fr |\n| `reminder` | Optional | Whether or not to send a reminder (1 or 0). Defaults to 1 |"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4cacf09b-3826-404d-b126-834600be4b33"
            }
          ]
        }
      ]
    },
    {
      "name": "Invitation",
      "item": [
        {
          "id": "9ba9b11b-8d24-4e9d-9d46-764785366e79",
          "name": "InvitationLinksCsvPost",
          "request": {
            "url": "http://example.com/InvitationLinks/csv",
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
            "description": "Generate links for users from a CSV file.\n\n**Request Parameters**\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `file` | Required | A CSV file formatted as a regular invitation CSV added as a HTTP POST file. |"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "789fbb91-2960-48d3-8ced-a291a6bccce0"
            }
          ]
        }
      ]
    }
  ]
}