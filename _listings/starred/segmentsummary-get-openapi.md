---
swagger: "2.0"
x-collection-name: Starred
x-complete: 0
info:
  title: Starred Dashboard Summary
  description: "Retrieve segment summary from your account. This summary includes
    your NPS score and detailed breakdown.\n\n**Request Parameters**\n\n| Parameter
    | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required
    | ID of the form that will be sent out |\n| `segment` | Optional | Group ID to
    get summary data for (defaults to 0) |\n\nNote: Segment is an alias for Groups
    in Starred Platform. You can retrieve Segment ID on Groups page in Starred Platform.
    [Groups in Starred](https://app.starred.com/segments/overview)\n\n#### Steps to
    retrieve Segment ID\n1. Login to Starred Platform\n2. Go to Clients tab\n3. Click
    on a Group you want to get data for. \n4. In Group detail view copy the Segment
    ID from URL\n\n![Starred API Key][starred-segment-id]\n[See Full Image](http://www.starred.com/wp-content/uploads/2018/05/starred-segment-id.png)\n[starred-segment-id]:
    http://www.starred.com/wp-content/uploads/2018/05/starred-segment-id.png"
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
  /sendinvitations/csv:
    post:
      summary: Send Invitation CSV
      description: "With the /sendinvitations call you can link your CRM system to
        Starred so invitations are sent automatically. This will no longer require
        any manual action. \n\nYou can also import additional characteristics directly
        from your CRM so you can start analyzing results for different client groups.
        \n\nThe parameters on the right are mandatory to make the request succeed.\n\n###
        Request Parameters\n\n| Parameter | Required | Description |\n| ------ | ------
        | ------ |\n| `form` | Required | ID of the form that will be sent out |\n|
        `from` | Required | Email address of the sender, must be a registered email
        |\n| `template` | Required | Template ID |\n| `language` | Required | The
        language of the template. For example: nl, en or fr |\n| `file` | Required
        | A CSV file formatted as a regular invitation CSV added as a HTTP POST file.
        |\n| `reminder` | Optional | Whether or not to send a reminder (1 means On,
        0 means Off). Defaults to 1 |\n\n### Example curl request\n```\ncurl -F \"file=@testCSV.csv\"
        https://api.starred.com/sendinvitations\\?company\\={{companyID}}\\&auth\\={{auth}}\\&form\\={{formId}}\\&from\\={{sender}}\\&template\\={{templateId}}\\&language\\={{language}}\n```"
      operationId: SendinvitationsCsvPost
      x-api-path-slug: sendinvitationscsv-post
      responses:
        200:
          description: OK
      tags:
      - Send
      - Invitation
      - CSV
  /InvitationLinks/csv:
    post:
      summary: Invitation Link CSV
      description: |-
        Generate links for users from a CSV file.

        **Request Parameters**

        | Parameter | Required | Description |
        | ------ | ------ | ------ |
        | `form` | Required | ID of the form that will be sent out |
        | `fromUserEmail` | Required | Email address of the sender |
        | `file` | Required | A CSV file formatted as a regular invitation CSV added as a HTTP POST file. |
      operationId: InvitationLinksCsvPost
      x-api-path-slug: invitationlinkscsv-post
      responses:
        200:
          description: OK
      tags:
      - Invitation
      - Link
      - CSV
  /sendinvitations:
    post:
      summary: Send Single Invitation
      description: |-
        Instead of uploading a CSV file, you can also set one recipient per API call by using the following parameters to the URL.

        ### Request Parameters

        | Parameter | Required | Description |
        | ------ | ------ | ------ |
        | `form` | Required | ID of the form that will be sent out |
        | `from` | Required | Email address of the sender, must be a registered email |
        | `recipient` | Required | Email address of the recipient |
        | `firstName` | Required | First name to address the recipient with |
        | `lastName` | Required | Surname to address the recipient with |
        | `template` | Required | Template ID |
        | `language` | Required | The language of the template. For example: nl, en or fr |
        | `reminder` | Optional | Whether or not to send a reminder (1 or 0). Defaults to 1 |
      operationId: SendinvitationsPost
      x-api-path-slug: sendinvitations-post
      responses:
        200:
          description: OK
      tags:
      - Send
      - Single
      - Invitation
  /segment/summary:
    get:
      summary: Dashboard Summary
      description: "Retrieve segment summary from your account. This summary includes
        your NPS score and detailed breakdown.\n\n**Request Parameters**\n\n| Parameter
        | Required | Description |\n| ------ | ------ | ------ |\n| `form` | Required
        | ID of the form that will be sent out |\n| `segment` | Optional | Group ID
        to get summary data for (defaults to 0) |\n\nNote: Segment is an alias for
        Groups in Starred Platform. You can retrieve Segment ID on Groups page in
        Starred Platform. [Groups in Starred](https://app.starred.com/segments/overview)\n\n####
        Steps to retrieve Segment ID\n1. Login to Starred Platform\n2. Go to Clients
        tab\n3. Click on a Group you want to get data for. \n4. In Group detail view
        copy the Segment ID from URL\n\n![Starred API Key][starred-segment-id]\n[See
        Full Image](http://www.starred.com/wp-content/uploads/2018/05/starred-segment-id.png)\n[starred-segment-id]:
        http://www.starred.com/wp-content/uploads/2018/05/starred-segment-id.png"
      operationId: SegmentSummaryGet
      x-api-path-slug: segmentsummary-get
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Summary
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