---
name: Starred
x-slug: starred
description: 'Better feedback for everyone, on a human scale. At Starred we like to
  work smart: working smarter to build great software, and working with smart companies
  who listen. As the feedback solution which puts the respondent first, we&rsquo;re
  empowering conversations between companies and their customers and employees. What&rsquo;s
  more, we equip them with the actionable insights they need to make better decisions
  and boost loyalty. With leading lights like Deliveroo, Heineken and Spotify already
  working with us to bring feedback to life, the road ahead for better feedback is
  looking good.'
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
x-kinRank: "7"
x-alexaRank: "916588"
tags: Starred
created: "2018-08-31"
modified: "2018-08-31"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/apis.md
specificationVersion: "0.14"
apis:
- name: Starred API - Anonymous Invitation Link
  x-api-slug: invitationlinksanonymous-post
  description: "Generate a link to a Starred survey form of your choice. \nGenerate
    from 1 up to, and including 100 anonymous links. (Anonymous is for when the recipient's
    email is not known)\n\n**Request Parameters**\n\n| Parameter | Required | Description
    |\n| ------ | ------ | ------ |\n| `form` | Required | ID of the form that will
    be sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n|
    `amount` | Optional | Amount of invitation links desired. (Defaults to 1) |\n|
    `tags` | Optional | Any number of invitation tags can be listed. It is in key
    - value format, e.g. tag1=tag1 |"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/invitationlinksanonymous-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/invitationlinksanonymous-post-openapi.md
- name: Starred API - Webhook v1.0
  x-api-slug: post
  description: |-
    Webhook v1.0 is our standard webhook response. This version will be deprecated soon. We highly recommend migrating to Webhook v1.1

    Please get in touch with our support to migrate your account to Webhook v1.1
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/post-openapi.md
- name: Starred API - Single Invitation Link
  x-api-slug: invitationlinkssingle-post
  description: "It is possible to generate a link to a Starred survey form of your
    choice. \n\n**Request Parameters**\n\n| Parameter | Required | Description |\n|
    ------ | ------ | ------ |\n| `form` | Required | ID of the form that will be
    sent out |\n| `fromUserEmail` | Required | Email address of the sender |\n| `recipient`
    | Required | Email address of the recipient |\n| `firstName` | Optional | First
    name to address the recipient with |\n| `lastName` | Optional | Surname to address
    the recipient with |\n| `tags` | Optional | Any number of invitation tags can
    be listed. It is in key - value format, e.g. tag1=tag1 |"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/invitationlinkssingle-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/invitationlinkssingle-post-openapi.md
- name: Starred API - Send Invitation CSV
  x-api-slug: sendinvitationscsv-post
  description: "With the /sendinvitations call you can link your CRM system to Starred
    so invitations are sent automatically. This will no longer require any manual
    action. \n\nYou can also import additional characteristics directly from your
    CRM so you can start analyzing results for different client groups. \n\nThe parameters
    on the right are mandatory to make the request succeed.\n\n### Request Parameters\n\n|
    Parameter | Required | Description |\n| ------ | ------ | ------ |\n| `form` |
    Required | ID of the form that will be sent out |\n| `from` | Required | Email
    address of the sender, must be a registered email |\n| `template` | Required |
    Template ID |\n| `language` | Required | The language of the template. For example:
    nl, en or fr |\n| `file` | Required | A CSV file formatted as a regular invitation
    CSV added as a HTTP POST file. |\n| `reminder` | Optional | Whether or not to
    send a reminder (1 means On, 0 means Off). Defaults to 1 |\n\n### Example curl
    request\n```\ncurl -F \"file=@testCSV.csv\" https://api.starred.com/sendinvitations\\?company\\={{companyID}}\\&auth\\={{auth}}\\&form\\={{formId}}\\&from\\={{sender}}\\&template\\={{templateId}}\\&language\\={{language}}\n```"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/sendinvitationscsv-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/sendinvitationscsv-post-openapi.md
- name: Starred API - Invitation Link CSV
  x-api-slug: invitationlinkscsv-post
  description: |-
    Generate links for users from a CSV file.

    **Request Parameters**

    | Parameter | Required | Description |
    | ------ | ------ | ------ |
    | `form` | Required | ID of the form that will be sent out |
    | `fromUserEmail` | Required | Email address of the sender |
    | `file` | Required | A CSV file formatted as a regular invitation CSV added as a HTTP POST file. |
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/invitationlinkscsv-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/invitationlinkscsv-post-openapi.md
- name: Starred API - Send Single Invitation
  x-api-slug: sendinvitations-post
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/sendinvitations-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/sendinvitations-post-openapi.md
- name: Starred API - Dashboard Summary
  x-api-slug: segmentsummary-get
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/starred-logo.png
  humanURL: https://www.starred.com
  baseURL: https://example.com//
  tags: SaaS, Technology, internet, Relative Data, Service API, Feedback, Stars
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/segmentsummary-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/starred/master/_listings/starred/segmentsummary-get-openapi.md
x-common:
- type: x-github
  url: https://github.com/starred-com
- type: x-twitter
  url: https://twitter.com/starred_com
- type: x-api-gallery
  url: http://standard.chartered.api.gallery.streamdata.io
- type: x-api-stack
  url: http://starred.stack.network
- type: x-blog
  url: https://www.starred.com/blog/
- type: x-crunchbase
  url: https://crunchbase.com/organization/starred
- type: x-email
  url: support@starred.com
- type: x-email
  url: legal@starred.com
- type: x-integrations
  url: https://www.starred.com/integrations/
- type: x-pricing
  url: https://www.starred.com/#
- type: x-website
  url: https://www.starred.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---