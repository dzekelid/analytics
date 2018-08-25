---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Analytics Framework Undeploy test analytics.
  version: 1.0.0
  description: This operation un-deploys the analytic app from the Cloud Foundry environment
    only if the analytic has been validated for testing purposes. This api will not
    un-deploy production analytics.
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/catalog/analytics/{id}/validation:
    delete:
      summary: Undeploy test analytics.
      description: This operation un-deploys the analytic app from the Cloud Foundry
        environment only if the analytic has been validated for testing purposes.
        This api will not un-deploy production analytics.
      operationId: invalidateAnalytic
      x-api-path-slug: apiv1cataloganalyticsidvalidation-delete
      parameters:
      - in: path
        name: id
        description: analytic catalog entry id
      responses:
        2:
          description: Successful response
      tags:
      - Undeploy
      - Test
      - Analytics
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