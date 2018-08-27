---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Analytics Framework Execute the analytic synchronously.
  version: 1.0.0
  description: Execute the analytic synchronously with the given execution payload.
host: predix-acs.run.aws-usw02-pr.ice.predix.io
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
    post:
      summary: Validate an analytic by analytic catalog entry id.
      description: This operation FORCE deploys the specified analytic into the Cloud
        Foundry environment, runs the analytic and responds with the validation request
        id (generated for the request), and the current request status.  The force
        deploy usually takes longer than the standard timeout, so the calling process
        should use the returned validation request id to monitor the request status
        and to retrieve the validation results.
      operationId: validateAnalytic
      x-api-path-slug: apiv1cataloganalyticsidvalidation-post
      parameters:
      - in: body
        name: body
        description: request payload containing analytic input data
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: analytic catalog entry id
      - in: query
        name: inputId
        description: test artifact id
      responses:
        2:
          description: Successful response
      tags:
      - Validate
      - Analytic
      - By
      - Analytic
      - Catalog
      - Entry
      - Id
  /api/v1/analytic/execution:
    post:
      summary: Execute the analytic synchronously.
      description: Execute the analytic synchronously with the given execution payload.
      operationId: synchronousExecution
      x-api-path-slug: apiv1analyticexecution-post
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: body
        name: body
        description: request payload containing analytic input data
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        2:
          description: Successful response
      tags:
      - Execute
      - Analytic
      - Synchronously
  /api/v1/analytic/execution/async:
    post:
      summary: Execute the analytic asynchronously using input data.
      description: Execute the analytic asynchronously with the given input data payload.
      operationId: asynchronousExecution
      x-api-path-slug: apiv1analyticexecutionasync-post
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: body
        name: body
        description: request payload containing analytic input data
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        2:
          description: Successful response
      tags:
      - Execute
      - Analytic
      - Asynchronously
      - Using
      - Input
      - Data
  /api/v1/analytic/execution/async/{requestId}:
    delete:
      summary: Cleanup analytic execution result by request id.
      description: Removes the analytic execution result from the cache. It is highly
        recommended to clean your old result data to have room for future result data.
      operationId: clearAnalyticExecutionResult
      x-api-path-slug: apiv1analyticexecutionasyncrequestid-delete
      parameters:
      - in: header
        name: Authorization
      - in: header
        name: Predix-Zone-Id
      - in: path
        name: requestId
      responses:
        2:
          description: Successful response
      tags:
      - Cleanup
      - Analytic
      - Execution
      - Result
      - By
      - Request
      - Id
  /api/v1/analytic/execution/async/{requestId}/result:
    get:
      summary: Get the analytic execution result by request id.
      description: Returns the analytic execution result.
      operationId: retrieveAnalyticExecutionResult
      x-api-path-slug: apiv1analyticexecutionasyncrequestidresult-get
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      - in: path
        name: requestId
        description: analytic execution request id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Execution
      - Result
      - By
      - Request
      - Id
  /api/v1/analytic/execution/async/{requestId}/status:
    get:
      summary: Get the analytic execution status by request id.
      description: Returns the analytic execution status (one of QUEUED, PROCESSING,
        COMPLETED, or FAILED).
      operationId: retrieveAnalyticExecutionStatus
      x-api-path-slug: apiv1analyticexecutionasyncrequestidstatus-get
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      - in: path
        name: requestId
        description: analytic execution request id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Execution
      - Status
      - By
      - Request
      - Id
  /api/v1/catalog/analytics:
    get:
      summary: Get all analytic catalog entries.
      description: Returns all analytic catalog entries as specified by page and sort
        criteria.
      operationId: retrieveAll
      x-api-path-slug: apiv1cataloganalytics-get
      parameters:
      - in: query
        name: page
        description: 'page index : zero-based page index'
      - in: query
        name: size
        description: 'page size : between 1 and 1000 inclusive'
      - in: query
        name: sortableFields
        description: 'sortable fields : name'
      - in: query
        name: sortOrder
        description: 'sort order : asc | desc'
      - in: query
        name: taxonomyPath
        description: 'taxonomy path : taxonomyPath'
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Catalog
      - Entries
    post:
      summary: Create an analytic catalog entry.
      description: Creates the analytic catalog entry with a generated id.
      operationId: createAnalyticCatalogEntry
      x-api-path-slug: apiv1cataloganalytics-post
      parameters:
      - in: body
        name: body
        description: analytic catalog entry
        schema:
          $ref: '#/definitions/holder'
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Catalog
      - Entry
  /api/v1/catalog/analytics/versions:
    get:
      summary: Get all versions of the analytic catalog entry with the given name.
      description: Returns all versions of the analytic catalog entry with the given
        name.
      operationId: retrieveByName
      x-api-path-slug: apiv1cataloganalyticsversions-get
      parameters:
      - in: query
        name: name
        description: analytic name
      responses:
        2:
          description: Successful response
      tags:
      - Versions
      - Of
      - Analytic
      - Catalog
      - Entry
      - Given
      - Name
  /api/v1/catalog/analytics/{id}:
    get:
      summary: Get an analytic catalog entry by id.
      description: Returns the analytic catalog entry with the given id.
      operationId: retrieveAnalyticCatalogEntryById
      x-api-path-slug: apiv1cataloganalyticsid-get
      parameters:
      - in: path
        name: id
        description: analytic catalog entry id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Catalog
      - Entry
      - By
      - Id
    put:
      summary: Update an analytic catalog entry by id.
      description: The analytic catalog entry with the given id will be updated.
      operationId: updateAnalyticCatalogEntry
      x-api-path-slug: apiv1cataloganalyticsid-put
      parameters:
      - in: body
        name: body
        description: analytic catalog entry
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: analytic catalog entry id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Catalog
      - Entry
      - By
      - Id
    delete:
      summary: Delete an analytic catalog entry by id.
      description: Deletes the analytic catalog entry with the given id.
      operationId: deleteAnalyticCatalogEntryById
      x-api-path-slug: apiv1cataloganalyticsid-delete
      parameters:
      - in: path
        name: id
        description: analytic catalog entry id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Catalog
      - Entry
      - By
      - Id
  /api/v1/catalog/analytics/{id}/artifacts:
    get:
      summary: Get the descriptive information of the artifacts corresponding to an
        analytic catalog entry.
      description: 'Returns the description information (type, description, etc.)
        for all artifacts associated with the given analytic catalog entry id. Note:
        it does not return the artifact file contents; use the download APIs to obtain
        an artifact file. An error is returned if the supplied analytic catalog entry
        id does not exist.'
      operationId: retrieveArtifactsByCatalogEntryId
      x-api-path-slug: apiv1cataloganalyticsidartifacts-get
      parameters:
      - in: path
        name: id
        description: analytic catalog entry id
      responses:
        2:
          description: Successful response
      tags:
      - Descriptive
      - Information
      - Of
      - Artifacts
      - Corresponding
      - To
      - Analytic
      - Catalog
      - Entry
  /api/v1/catalog/analytics/{id}/deployment:
    post:
      summary: Deploy an analytic with an optional deployment configuration by analytic
        catalog entry id.
      description: This operation FORCE deploys the specified analytic into the Cloud
        Foundry environment with an optional deployment configuration, responds with
        the request id (generated for the request), and the current request status.  The
        force deploy usually takes longer than the standard timeout, so the calling
        process should use the returned request id to monitor the request status and
        to retrieve the deployment results.
      operationId: deployAnalytic
      x-api-path-slug: apiv1cataloganalyticsiddeployment-post
      parameters:
      - in: body
        name: body
        description: deployment configuration
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: analytic catalog entry id
      responses:
        2:
          description: Successful response
      tags:
      - Deploy
      - Analytic
      - Optional
      - Deployment
      - Configuration
      - By
      - Analytic
      - Catalog
      - Entry
      - Id
  /api/v1/catalog/analytics/{id}/deployment/{requestId}:
    get:
      summary: Get the analytic deployment status by request id.
      description: Returns the analytic deployment status (one of 'queued,' 'processing,'
        or 'completed').
      operationId: retrieveAnalyticDeploymentResult
      x-api-path-slug: apiv1cataloganalyticsiddeploymentrequestid-get
      parameters:
      - in: path
        name: id
        description: analytic id
      - in: path
        name: requestId
        description: analytic deployment request id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Deployment
      - Status
      - By
      - Request
      - Id
  /api/v1/catalog/analytics/{id}/execution:
    post:
      summary: Execute an analytic by analytic catalog entry id.
      description: This operation executes the specified analytic and responds with
        the result produced by analytic.
      operationId: executeAnalytic
      x-api-path-slug: apiv1cataloganalyticsidexecution-post
      parameters:
      - in: body
        name: body
        description: request payload containing analytic input data
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: analytic catalog entry id
      - in: query
        name: inputId
        description: test artifact id
      responses:
        2:
          description: Successful response
      tags:
      - Execute
      - Analytic
      - By
      - Analytic
      - Catalog
      - Entry
      - Id
  /api/v1/catalog/analytics/{id}/logs:
    get:
      summary: Get the analytic recent logs
      description: Return the recent analytic logs
      operationId: retrieveAnalyticLog
      x-api-path-slug: apiv1cataloganalyticsidlogs-get
      parameters:
      - in: path
        name: id
        description: analytic id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Recent
      - Logs
  /api/v1/catalog/analytics/{id}/validation/{validationRequestId}:
    get:
      summary: Get the analytic validation status by validation request id.
      description: Returns the analytic validation status (one of 'queued,' 'processing,'
        or 'completed' and the result from running the analytic (when status is 'completed').
      operationId: retrieveAnalyticValidationResult
      x-api-path-slug: apiv1cataloganalyticsidvalidationvalidationrequestid-get
      parameters:
      - in: path
        name: id
        description: analytic id
      - in: path
        name: validationRequestId
        description: analytic validation request id
      responses:
        2:
          description: Successful response
      tags:
      - Analytic
      - Validation
      - Status
      - By
      - Validation
      - Request
      - Id
  /api/v1/catalog/analytics/{name}/versions:
    delete:
      summary: Delete all versions of the named analytic.
      description: Given the name of an analytic, this API deletes all its versions.
      operationId: deleteAllVersions
      x-api-path-slug: apiv1cataloganalyticsnameversions-delete
      parameters:
      - in: path
        name: name
        description: analytic name
      responses:
        2:
          description: Successful response
      tags:
      - Versions
      - Of
      - Named
      - Analytic
  /api/v1/catalog/artifacts:
    post:
      summary: Upload an artifact and attach it to an analytic catalog entry.
      description: Upload a single artifact file in a multipart MIME structure and
        attach it to an analytic catalog entry. The multipart MIME structure must
        have the catalog entry id tagged as 'catalogEntryId',  the file contents tagged
        as 'file',  the artifact type tagged as 'type', and  a description (under
        1024 characters) tagged as 'description'. Artifact types can be any string.  Artifacts
        with the type 'executable' must contain the executable for the analytic.   An
        analytic can only have 1 artifact labelled as 'executable'(See the documentation
        for more information regarding these files.)
      operationId: uploadAnalyticArtifact
      x-api-path-slug: apiv1catalogartifacts-post
      parameters:
      - in: formData
        name: catalogEntryId
        description: (Required) analytic catalog entry id
      - in: formData
        name: description
        description: artifact description
      - in: formData
        name: file
        description: (Required) artifact file
      - in: formData
        name: type
        description: (Required) artifact type
      responses:
        2:
          description: Successful response
      tags:
      - Upload
      - Artifact
      - Attach
      - It
      - To
      - Analytic
      - Catalog
      - Entry
  /api/v2/execution/validation:
    post:
      summary: Validate the specified orchestration and the health of all the analytics
        used in the orchestration.
      description: To successfully validate the orchestration, the BPMN XML file must
        reference analytics that are running. The validation will call a 'healthCheck'
        entry on each analytic.  Analytics in the platform automatically have this
        entry, analytics outside the platform must implement this APIfor their validation
        to pass.  The results contain the http status for each for the healthCheck
        call to each analytic.
      operationId: validate
      x-api-path-slug: apiv2executionvalidation-post
      parameters:
      - in: body
        name: file
        description: (Required) artifact file
        schema:
          $ref: '#/definitions/holder'
      responses:
        2:
          description: Successful response
      tags:
      - Validate
      - Specified
      - Orchestration
      - Health
      - Of
      - ""
      - Analytics
      - Used
      - In
      - Orchestration
  /api/v1/analytics/customdata/read:
    post:
      summary: Retrieve analytic input data from custom datasource.
      description: Returns the analytic input data used during runtime execution.
      operationId: readCustomProviderData
      x-api-path-slug: apiv1analyticscustomdataread-post
      parameters:
      - in: body
        name: body
        description: Analytic Input Data Read request
        schema:
          $ref: '#/definitions/holder'
      responses:
        2:
          description: Successful response
      tags:
      - Retrieve
      - Analytic
      - Input
      - Data
      - From
      - Custom
      - Datasource
  /api/v1/analytics/customdata/write:
    post:
      summary: Write analytic output data to custom datasource.
      description: Writes analytic output data generated during runtime execution.
      operationId: writeCustomProviderData
      x-api-path-slug: apiv1analyticscustomdatawrite-post
      parameters:
      - in: body
        name: body
        description: Analytic Output Data Write Request
        schema:
          $ref: '#/definitions/holder'
      responses:
        2:
          description: Successful response
      tags:
      - Write
      - Analytic
      - Output
      - Data
      - To
      - Custom
      - Datasource
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