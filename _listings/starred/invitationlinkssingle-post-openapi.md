---
swagger: "2.0"
x-collection-name: Starred
x-complete: 0
info:
  title: Starred Single Invitation Link
  description: "It is possible to generate a link to a Starred survey form of your
    choice. \n\n**Request Parameters**\n\n| Parameter | Required | Description |\n|
    ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be
    sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `recipient`
    | Required | Email address of the recipient |\n| `firstName` | Optional | First
    name to address the recipient with |\n| `lastName` | Optional | Surname to address
    the recipient with |\n| `tags` | Optional | Any number of invitation tags can
    be listed. It is in key - value format, e.g. tag1=tag1 |"
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /InvitationLinks/anonymous:
    post:
      summary: Anonymous Invitation Link
      description: "Generate a link to a Starred survey form of your choice. \nGenerate
        from 1 up to, and including 100 anonymous links. (Anonymous is for when the
        recipient's email is not known)\n\n**Request Parameters**\n\n| Parameter |
        Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required
        | ID of the form that will be sent out |\n| `fromUserEmail` | Required | Email
        address of the sender |\n| `amount` | Optional | Amount of invitation links
        desired. (Defaults to 1) |\n| `tags` | Optional | Any number of invitation
        tags can be listed. It is in key - value format, e.g. tag1=tag1 |"
      operationId: InvitationLinksAnonymousPost
      x-api-path-slug: invitationlinksanonymous-post
      responses:
        200:
          description: OK
      tags:
      - Anonymous
      - Invitation
      - Link
  /:
    post:
      summary: Webhook v1.0
      description: |-
        Webhook v1.0 is our standard webhook response. This version will be deprecated soon. We highly recommend migrating to Webhook v1.1

        Please get in touch with our support to migrate your account to Webhook v1.1
      operationId: UnnammedEndpointPost2
      x-api-path-slug: post
      responses:
        200:
          description: OK
      tags:
      - Webhook
      - V1
      - "0"
  /InvitationLinks/single:
    post:
      summary: Single Invitation Link
      description: "It is possible to generate a link to a Starred survey form of
        your choice. \n\n**Request Parameters**\n\n| Parameter | Required | Description
        |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that
        will be sent out |\n| `fromUserEmail` | Required | Email address of the sender
        |\n| `recipient` | Required | Email address of the recipient |\n| `firstName`
        | Optional | First name to address the recipient with |\n| `lastName` | Optional
        | Surname to address the recipient with |\n| `tags` | Optional | Any number
        of invitation tags can be listed. It is in key - value format, e.g. tag1=tag1
        |"
      operationId: InvitationLinksSinglePost
      x-api-path-slug: invitationlinkssingle-post
      responses:
        200:
          description: OK
      tags:
      - Single
      - Invitation
      - Link
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---