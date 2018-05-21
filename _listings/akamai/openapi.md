---
swagger: "2.0"
x-collection-name: Akamai
x-complete: 1
info:
  title: Akamai API
  description: the-akamai-api-for-managing-your-akamai-service
  version: 1.0.0
host: developer.akamai.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /prolexic-analytics/v1/events/contract/{contract}:
    get:
      summary: List Events
      description: List Events
      operationId: prolexicanalyticsv1eventscontractcontract
      x-api-path-slug: prolexicanalyticsv1eventscontractcontract-get
      parameters:
      - in: query
        name: contract
        description: Name of contract events should be attached to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Prolexic
      - Analytics
      - Events
      - Contract
      - Contract
  /prolexic-analytics/v1/critical-events/contract/{contract}:
    get:
      summary: List Critical Events
      description: List Critical Events
      operationId: prolexicanalyticsv1criticaleventscontractcontract
      x-api-path-slug: prolexicanalyticsv1criticaleventscontractcontract-get
      parameters:
      - in: query
        name: contract
        description: Name of contract events should be attached to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Prolexic
      - Analytics
      - Critical
      - Events
      - Contract
      - Contract
  /prolexic-analytics/v1/metric-types:
    get:
      summary: List Metric Types
      description: List Metric Types
      operationId: prolexicanalyticsv1metrictypes
      x-api-path-slug: prolexicanalyticsv1metrictypes-get
      responses:
        200:
          description: OK
      tags:
      - Prolexic
      - Analytics
      - Metric
      - Types
  /prolexic-analytics/v1/attack-reports/contract/{contract}/start/{start}/end/{end}:
    get:
      summary: List Attack Reports
      description: List Attack Reports
      operationId: prolexicanalyticsv1attackreportscontractcontractstartstartendend
      x-api-path-slug: prolexicanalyticsv1attackreportscontractcontractstartstartendend-get
      parameters:
      - in: query
        name: contract
        description: Name of contract attack reports belong to
        type: string
      - in: query
        name: end
        description: Unix timestamp for end of attack report search
        type: string
      - in: query
        name: start
        description: Unix timestamp for beginning of attack report search
        type: string
      responses:
        200:
          description: OK
      tags:
      - Prolexic
      - Analytics
      - Attack
      - Reports
      - Contract
      - Contract
      - Start
      - Start
      - End
      - End
  /prolexic-analytics/v1/attack-report/contract/{contract}/attack-id/{attackId}:
    get:
      summary: Get an Attack Report
      description: Get an Attack Report
      operationId: prolexicanalyticsv1attackreportcontractcontractattackidattackid
      x-api-path-slug: prolexicanalyticsv1attackreportcontractcontractattackidattackid-get
      parameters:
      - in: query
        name: attackId
        description: Integer matching the attackId of the attack desired
        type: string
      - in: query
        name: contract
        description: Name of contract attack report belong to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Prolexic
      - Analytics
      - Attack
      - Report
      - Contract
      - Contract
      - Attack
      - ""
      - Attack
---