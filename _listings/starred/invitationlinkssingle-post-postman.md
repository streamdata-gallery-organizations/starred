{
  "info": {
    "name": "Starred Single Invitation Link",
    "_postman_id": "85e2f054-17d2-4a35-8835-f43fbfbc6b3d",
    "description": "It is possible to generate a link to a Starred survey form of your choice. \n\n**Request Parameters**\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `recipient` | Required | Email address of the recipient |\n| `firstName` | Optional | First name to address the recipient with |\n| `lastName` | Optional | Surname to address the recipient with |\n| `tags` | Optional | Any number of invitation tags can be listed. It is in key - value format, e.g. tag1=tag1 |",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "9cfbdc26-7111-4ecb-901f-46f6bb5c11bc",
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
              "id": "617aa42e-9ad3-473d-ba81-915638129a95"
            }
          ]
        }
      ]
    },
    {
      "name": "Single",
      "item": [
        {
          "id": "904482a4-19d8-48e2-8c05-0fe0750d6115",
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
              "id": "5ae09958-6c93-460a-9b04-ecbb1752d03b"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "03ddab30-162a-402c-994b-54dc2ad6f7ff",
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
              "id": "e7592fcd-c1cd-41f2-9163-f7b6970ae28f"
            }
          ]
        },
        {
          "id": "f6ecf0d4-60e6-4c39-968a-4303f65f2102",
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
              "id": "c1e7a182-4b61-4116-af01-70e0937da9ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Invitation",
      "item": [
        {
          "id": "86a283c1-b12c-4f1d-b3d6-e59a6aa2a553",
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
              "id": "004226aa-dbbd-40cb-9426-825593726816"
            }
          ]
        }
      ]
    }
  ]
}