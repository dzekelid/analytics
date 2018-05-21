---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 1
info:
  title: SendGrid
  description: the-sendgrid-web-api-v3-documentation-this-is-the-entirety-of-the-documented-v3-endpoints-we-have-updated-all-the-descriptions-parameters-requests-and-responses-authentication-every-endpoint-requires-authentication-in-the-form-of-an-authorization-header-authorization-bearer-api-key
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tracking_settings/google_analytics:
    get:
      summary: Get Tracking Settings Google Analytics
      description: "**This endpoint allows you to retrieve your current setting for
        Google Analytics.**\n\nFor more information about using Google Analytics,
        please refer to [Google\u2019s URL Builder](https://support.google.com/analytics/answer/1033867?hl=en)
        and their article on [\"Best Practices for Campaign Building\"](https://support.google.com/analytics/answer/1037445).\n\nWe
        default the settings to Google\u2019s recommendations. For more information,
        see [Google Analytics Demystified](https://sendgrid.com/docs/Classroom/Track/Collecting_Data/google_analytics_demystified_ga_statistics_vs_sg_statistics.html).\n\nYou
        can track a variety of the actions your recipients may take when interacting
        with your emails including opening your emails, clicking on links in your
        emails, and subscribing to (or unsubscribing from) your emails.\n\nFor more
        information about tracking, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/tracking.html)."
      operationId: tracking_settings.google_analytics.get
      x-api-path-slug: tracking-settingsgoogle-analytics-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Tracking
      - Settings
      - Google
      - Analytics
    patch:
      summary: Patch Tracking Settings Google Analytics
      description: "**This endpoint allows you to update your current setting for
        Google Analytics.**\n\nFor more information about using Google Analytics,
        please refer to [Google\u2019s URL Builder](https://support.google.com/analytics/answer/1033867?hl=en)
        and their article on [\"Best Practices for Campaign Building\"](https://support.google.com/analytics/answer/1037445).\n\nWe
        default the settings to Google\u2019s recommendations. For more information,
        see [Google Analytics Demystified](https://sendgrid.com/docs/Classroom/Track/Collecting_Data/google_analytics_demystified_ga_statistics_vs_sg_statistics.html).\n\nYou
        can track a variety of the actions your recipients may take when interacting
        with your emails including opening your emails, clicking on links in your
        emails, and subscribing to (or unsubscribing from) your emails.\n\nFor more
        information about tracking, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/tracking.html)."
      operationId: tracking_settings.google_analytics.patch
      x-api-path-slug: tracking-settingsgoogle-analytics-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Tracking
      - Settings
      - Google
      - Analytics
---