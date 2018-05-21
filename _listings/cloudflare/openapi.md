---
swagger: "2.0"
x-collection-name: CloudFlare
x-complete: 1
info:
  title: CloudFlare
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /zones/:zone_identifier/analytics/colos:
    get:
      summary: This view provides a breakdown of analytics data by datacenter
      description: This view provides a breakdown of analytics data by datacenter
      operationId: cloudflare-zone-analytics-api
      x-api-path-slug: zoneszone-identifieranalyticscolos-get
      parameters:
      - in: query
        name: continuous
        description: When set to true, the range returned by the response acts like
          a sliding window to provide a contiguous time-window
      - in: query
        name: since
        description: The (inclusive) beginning of the requested time frame
      - in: query
        name: until
        description: The (exclusive) end of the requested time frame
      - in: header
        name: X-AUTH-EMAIL
        description: Email address associated with your account
      - in: header
        name: X-AUTH-KEY
        description: API key generated on the My Account page
      responses:
        200:
          description: OK
      tags:
      - Zones
      - Analytics
  /zones/:zone_identifier/analytics/dashboard:
    get:
      summary: The dashboard view provides both totals and timeseries data for the
        given zone and time period across the entire CloudFlare network
      description: The dashboard view provides both totals and timeseries data for
        the given zone and time period across the entire CloudFlare network
      operationId: cloudflare-zone-analytics-api
      x-api-path-slug: zoneszone-identifieranalyticsdashboard-get
      parameters:
      - in: query
        name: continuous
        description: When set to true, the range returned by the response acts like
          a sliding window to provide a contiguous time-window
      - in: query
        name: since
        description: The (inclusive) beginning of the requested time frame
      - in: query
        name: until
        description: The (exclusive) end of the requested time frame
      - in: header
        name: X-AUTH-EMAIL
        description: Email address associated with your account
      - in: header
        name: X-AUTH-KEY
        description: API key generated on the My Account page
      responses:
        200:
          description: OK
      tags:
      - Zones
      - Analytics
---