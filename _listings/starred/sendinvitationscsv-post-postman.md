{
  "info": {
    "name": "Starred Send Invitation CSV",
    "_postman_id": "cd74c0a3-7a58-4a30-85b9-7eb41755af16",
    "description": "With the /sendinvitations call you can link your CRM system to Starred so invitations are sent automatically. This will no longer require any manual action. \n\nYou can also import additional characteristics directly from your CRM so you can start analyzing results for different client groups. \n\nThe parameters on the right are mandatory to make the request succeed.\n\n### Request Parameters\n\n| Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be sent out |\n| `from` | Required | Email address of the sender, must be a registered email |\n| `template` | Required | Template ID |\n| `language` | Required | The language of the template. For example: nl, en or fr |\n| `file` | Required | A CSV file formatted as a regular invitation CSV added as a HTTP POST file. |\n| `reminder` | Optional | Whether or not to send a reminder (1 means On, 0 means Off). Defaults to 1 |\n\n### Example curl request\n```\ncurl -F \"file=@testCSV.csv\" https://api.starred.com/sendinvitations\\?company\\={{companyID}}\\&auth\\={{auth}}\\&form\\={{formId}}\\&from\\={{sender}}\\&template\\={{templateId}}\\&language\\={{language}}\n```",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "0475a8dd-bbe1-4beb-884b-f85d0553ad34",
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
              "id": "d1919e14-9a84-454d-9a3e-21c2ac2f2772"
            }
          ]
        }
      ]
    },
    {
      "name": "Single",
      "item": [
        {
          "id": "90e7abf6-bdce-4721-afdf-594f45dff317",
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
              "id": "8155571e-11c3-4e85-836d-609f89968335"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "02760f74-0f14-4f0c-a721-a785fdbee4e2",
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
              "id": "22cabdc2-a604-4387-b0ce-11969c8fd7ea"
            }
          ]
        },
        {
          "id": "1fea6394-3dcd-4037-b2e9-106526de5e42",
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
              "id": "efa63f90-72b7-443f-9041-994b669e2ae6"
            }
          ]
        }
      ]
    },
    {
      "name": "Invitation",
      "item": [
        {
          "id": "d26e98e1-21db-43e9-a71a-f0d402bdeefc",
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
              "id": "c1da4ec5-1614-4cd0-9e27-ec82aa3bc524"
            }
          ]
        }
      ]
    }
  ]
}