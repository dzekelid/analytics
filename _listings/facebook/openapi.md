---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 1
info:
  title: Facebook Graph (Achievement Type) API
  description: api-for-managing-facebook-achievement-types
  termsOfService: https://www.facebook.com/policies/
  version: 1.0.0
host: graph.facebook.com
basePath: /v3.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /&#123;analytics-app-events-export-id&#125;:
    get:
      summary: Get Analytics App Events Export
      description: Analytics App Events Export
      operationId: getAnalyticsAppEventsExport
      x-api-path-slug: 123analyticsappeventsexportid125-get
      parameters:
      - in: query
        name: column_namesliststring
        description: Names of columns in the tableDefault
        type: string
      - in: query
        name: end_tsdatetime
        description: End time for the exportDefault
        type: string
      - in: query
        name: error_messagestring
        description: User error messageDefault
        type: string
      - in: query
        name: event_param_nameslistAnalyticsAppEventsExportEventParamNames
        description: Parameters names for each events that map to custom1-25 in data
          tableDefault
        type: string
      - in: query
        name: idnumeric string
        description: ID of the app events export jobDefault
        type: string
      - in: query
        name: recent_download_timestampslistdatetime
        description: Timestamps for recent downloads of the export
        type: string
      - in: query
        name: request_tsdatetime
        description: Time when the export was requested
        type: string
      - in: query
        name: start_tsdatetime
        description: Start time for the exportDefault
        type: string
      - in: query
        name: statusenum
        description: Status of the export jobDefault
        type: string
      responses:
        200:
          description: OK
      tags:
      - Analytics
      - App
      - Events
      - Export
  /&#123;user-id&#125;/adnetworkanalytics:
    get:
      summary: Get User Adnetworkanalytics
      description: User Adnetworkanalytics
      operationId: getUserAdnetworkanalytics
      x-api-path-slug: 123userid125adnetworkanalytics-get
      parameters:
      - in: query
        name: "100"
        description: Invalid parameter
        type: string
      - in: query
        name: "3001"
        description: Invalid query
        type: string
      - in: query
        name: "3011"
        description: Currently unavailable
        type: string
      responses:
        200:
          description: OK
      tags:
      - User
      - Adnetworkanalytics
---