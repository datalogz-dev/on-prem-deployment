# Datalogz On-Prem deployment using _docker compose_

Datalogz offers on-prem deployment using docker compose. Datalogz application follows microservice architecture, each service runs in a separate docker container. In this document, we will be looking at the important configurations required by each service to run the Datalogza app successfully. . We can configure each microservice in docker compose using the environment variables.

Datalogz contains the following microservices in the docker compose file:

1. Frontend
2. Search
3. Metadata
4. Databuilder
5. Utility

## Frontend

Frontend contains following configuration

**HOST**: the name of the host on which your users can access your deployed app. For example, if the users can access your deployed app on [https://mydatalogzapp.com](https://mydatalogzapp.com). Then the value for this variable will be **mydatalogzapp.com**

**PROTOCOL**: If you have enabled SSL in your domain. Then the value for this env variable will be “**https://**”. Otherwise, it will be “**http://**”

Google:

To enable your users to login using Google OAuth, You will need to create an OAuth for Google and provide the following

* **GOOGLE_CLIENT_ID**
* **GOOGLE_CLIENT_SECRET**

WorkOS:

To enable your users to login using MS/OKTA or any other authentication. You will need to create a WorkOS application and provide the following

* **WORKOS_API_KEY**
* **WORKOS_CLIENT_ID**

PowerBI:

To enable column lineage, diagnostic, and report catalog for PowerBI. You will need to register a PowerBI app in your Azure portal and provide the following

* **POWERBI_CLIENT_ID**
* **POWERBI_CLIENT_SECRET**

Sendgrid:

Datalogz uses Sendgrid to send notifications by email. You will need to create an Sendgrid account and provide the following variables

* **SEND_GRID_KEY**
* **SEND_GRID_TEMPLATE_URI**

## Metadata

This service does not require any environment variable to change.

## Search

This service does not require any environment variable to change.

## Databuilder

This service does not require any environment variable to change.

## Utility

This service does not require any environment variable to change.
