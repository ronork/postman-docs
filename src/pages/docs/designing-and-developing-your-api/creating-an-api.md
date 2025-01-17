---
title: 'Creating an API'
order: 81.1
page_id: 'creating_an_api'
updated: 2022-02-16
warning: false
contextual_links:
  - type: section
    name: "Additional Resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "Postman Space Camp | Design and Prototype an API in Postman"
    url: "https://youtu.be/r4kb3jOSsmk"
  - type: link
    name: "API Builder | The Exploratory"
    url: "https://youtu.be/BUZiRtGRHj0"
  - type: link
    name: "API Fest 2022 | Workshop on Designing API Schemas"
    url: "https://youtu.be/gGOB3oM2cE4"
  - type: link
    name: "API Fest 2022 | Workshop on Coding an API using an API Schema"
    url: "https://youtu.be/RMiG9tzw5tg"
  - type: link
    name: "Getting Started with OpenAPI in Postman | Postman Space Camp"
    url: "https://youtu.be/YRzpziA35Mg"
  - type: section
    name: "Next Steps"
  - type: link
    name: "Managing APIs"
    url: "/docs/designing-and-developing-your-api/managing-apis/"
---

To start using the API Builder, you can create a new API in your workspace. You can also rename or delete existing APIs.

## Creating an API

1. From the sidebar, select __APIs__. You can open and edit any existing APIs from here.

   <img alt="Create API" src="https://assets.postman.com/postman-docs/v8-create-new-api2.jpg"/>

1. Select __New__, then select __API__ or select __+__.

   > You must be signed in to your Postman account to take this action.

1. Enter a name and a version, then select a schema type and format for your API. Postman will populate your API with a sample specification you can edit at any time.
   > Postman currently supports OpenAPI (versions 1.0, 2.0, 3.0, and 3.1), RAML (0.8 and 1.0), GraphQL, or WSDL (1.1 and 2.0) schemas. OpenAPI schemas can be defined in JSON or YAML. RAML schemas must be YAML. GraphQL schemas can be JSON or GraphQL SDL. WSDL schemas must be XML. Multi-file variants of schemas are currently not supported.

   ![New API](https://assets.postman.com/postman-docs/create-api-v9.jpg)

   You can instead select the **Import** tab to import an API specification directly from a local file, a GitHub or Bitbucket repo, or an Amazon API Gateway. For information on importing an API specification, see [Importing an API](/docs/designing-and-developing-your-api/importing-an-api/).

1. Select **Create API**.

## Renaming and deleting APIs

You can rename, delete, or remove the API from the workspace using the more actions icon <img alt="More actions icon" src="https://assets.postman.com/postman-docs/icon-more-actions-v9.jpg#icon" width="16px"> in the sidebar.

   > When you delete an API or remove it from a workspace, the collections, monitors, mocks, and environments linked to it won't be deleted or removed. Also, any configured integrations aren't deleted.

   <img alt="Edit API" src="https://assets.postman.com/postman-docs/v8-more-actions2.jpg"/>
