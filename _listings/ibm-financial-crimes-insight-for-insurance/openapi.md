swagger: "2.0"
x-collection-name: IBM Financial Crimes Insight for Insurance
x-complete: 1
info:
  title: Financial Crimes Insight for Insurance public REST APIs
  description: these-are-the-financial-crimes-insight-for-insurance-public-rest-apis-used-by-clients-to-access-the-fcii-capabilities
  version: 1.0.0
host: fcihost.ibm.com:9443
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ibm/fci/platform/external_alert/analysis_result:
    post:
      summary: Submit assessments from monitored analytics
      description: This method is used to submit analysis results from monitored analysis
      operationId: postExternalAnalyticResult
      x-api-path-slug: ibmfciplatformexternal-alertanalysis-result-post
      parameters:
      - in: body
        name: AnalysisAssessedResults
        description: An XML object corresponding to the AnalysisAssessedResults
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: IBM-FCI-Role
        description: Userid / password for user with appropriate role
      - in: header
        name: IBM-FCI-Token
        description: Security token obtained for execution
      responses:
        200:
          description: OK
      tags:
      - Submit
      - Assessments
      - From
      - Monitored
      - Analytics