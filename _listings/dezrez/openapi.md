---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/sync/googleanalyticsoauthurl/{brandId}/{personId}:
    get:
      summary: Get the oauth url for the google analytics integration service
      description: Get the oauth url for the google analytics integration service.
      operationId: Sync_GoogleAnalyticsOauthUrlBybrandIdBypersonId
      x-api-path-slug: apisyncgoogleanalyticsoauthurlbrandidpersonid-get
      parameters:
      - in: path
        name: brandId
      - in: path
        name: personId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Oauth
      - Urlthe
      - Google
      - Analytics
      - Integration
      - Service
---