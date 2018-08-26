{
  "info": {
    "name": "Starred Invitation Link CSV",
    "_postman_id": "c97d4cad-106a-4f78-b01a-929d431b12b3",
    "description": "Generate links for users from a CSV file.\n\n**Request Parameters**\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `file` | Required | A CSV file formatted as a regular invitation CSV added as a HTTP POST file. |",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "63003005-6f0b-4aaa-b712-e22d11163ce3",
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
              "id": "226ac808-4cb3-4a48-984b-aa82293e2259"
            }
          ]
        }
      ]
    },
    {
      "name": "Single",
      "item": [
        {
          "id": "67fc5bce-a092-4844-ac0b-f36688a5e204",
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
              "id": "46b46395-5b3f-4a3a-ba69-12f56e4259b2"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "aa69ede7-ba4a-4f56-ad8c-31f3841b7abd",
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
              "id": "ef47fd91-7433-46e9-8bc3-91d7239597ec"
            }
          ]
        },
        {
          "id": "29df987a-c829-4339-9fcd-18d63818ab16",
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
              "id": "731a87bb-c513-4d08-9509-11a7344c96c9"
            }
          ]
        }
      ]
    },
    {
      "name": "Invitation",
      "item": [
        {
          "id": "32e894af-018c-4edd-8513-1d6ab4932b8e",
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
              "id": "c83793f4-4301-425e-8200-7509b7499a0a"
            }
          ]
        }
      ]
    }
  ]
}