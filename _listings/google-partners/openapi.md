---
swagger: "2.0"
x-collection-name: Google Partners
x-complete: 1
info:
  title: Google Partners
  description: searches-certified-companies-and-creates-contact-leads-with-them-and-also-audits-the-usage-of-clients-
  contact:
    name: Google
    url: https://google.com
  version: v2
host: partners.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/analytics:
    get:
      summary: Get Analytics
      description: |-
        Lists analytics data for a user's associated company.
        Should only be called within the context of an authorized logged in user.
      operationId: partners.analytics.list
      x-api-path-slug: v2analytics-get
      parameters:
      - in: query
        name: pageSize
        description: Requested page size
      - in: query
        name: pageToken
        description: A token identifying a page of results that the server returns
      - in: query
        name: requestMetadata.experimentIds
        description: Experiment IDs the current request belongs to
      - in: query
        name: requestMetadata.locale
        description: Locale to use for the current request
      - in: query
        name: requestMetadata.partnersSessionId
        description: Google Partners session ID
      - in: query
        name: requestMetadata.trafficSource.trafficSourceId
        description: Identifier to indicate where the traffic comes from
      - in: query
        name: requestMetadata.trafficSource.trafficSubId
        description: Second level identifier to indicate where the traffic comes from
      - in: query
        name: requestMetadata.userOverrides.ipAddress
        description: IP address to use instead of the users geo-located IP address
      - in: query
        name: requestMetadata.userOverrides.userId
        description: Logged-in user ID to impersonate instead of the users ID
      responses:
        200:
          description: OK
      tags:
      - Analytics
---