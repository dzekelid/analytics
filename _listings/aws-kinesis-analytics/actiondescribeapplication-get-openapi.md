---
swagger: "2.0"
x-collection-name: AWS Kinesis Analytics
x-complete: 0
info:
  title: AWS Kinesis Analytics API Describe Application
  version: 1.0.0
  description: Returns information about a specific Amazon Kinesis Analytics application.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AddApplicationOutput:
    get:
      summary: Add Application Output
      description: Adds an external destination to your Amazon Kinesis Analytics application.
      operationId: addApplicationOutput
      x-api-path-slug: actionaddapplicationoutput-get
      parameters:
      - in: query
        name: ApplicationName
        description: Name of the application to which you want to add the output configuration
        type: string
      - in: query
        name: CurrentApplicationVersionId
        description: Version of the application to which you want add the             output
          configuration
        type: string
      - in: query
        name: Output
        description: An array of objects, each describing one output configuration
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=CreateApplication:
    get:
      summary: Create Application
      description: Creates an Amazon Kinesis Analytics application.
      operationId: createApplication
      x-api-path-slug: actioncreateapplication-get
      parameters:
      - in: query
        name: ApplicationCode
        description: One or more SQL statements that read input data, transform it,             and
          generate output
        type: string
      - in: query
        name: ApplicationDescription
        description: Summary description of the application
        type: string
      - in: query
        name: ApplicationName
        description: Name of your Amazon Kinesis Analytics application (for example,
          sample-app)
        type: string
      - in: query
        name: Inputs
        description: Use this parameter to configure the application input
        type: string
      - in: query
        name: Outputs
        description: You can configure application output to write data from any of
          the in-application streams to up to five destinations
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=DescribeApplication:
    get:
      summary: Describe Application
      description: Returns information about a specific Amazon Kinesis Analytics application.
      operationId: describeApplication
      x-api-path-slug: actiondescribeapplication-get
      parameters:
      - in: query
        name: ApplicationName
        description: Name of the application
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=ListApplications:
    get:
      summary: List Applications
      description: Returns a list of Amazon Kinesis Analytics applications in your
        account.
      operationId: listApplications
      x-api-path-slug: actionlistapplications-get
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=StartApplication:
    get:
      summary: Start Application
      description: Starts the specified Amazon Kinesis Analytics application.
      operationId: startApplication
      x-api-path-slug: actionstartapplication-get
      parameters:
      - in: query
        name: ApplicationName
        description: Name of the application
        type: string
      - in: query
        name: InputConfigurations
        description: Identifies the specific input, by ID, that the application starts
          consuming
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
  /?Action=UpdateApplication:
    get:
      summary: Update Application
      description: Updates an existing Amazon Kinesis Analytics application.
      operationId: updateApplication
      x-api-path-slug: actionupdateapplication-get
      parameters:
      - in: query
        name: ApplicationName
        description: Name of the Amazon Kinesis Analytics application to update
        type: string
      - in: query
        name: ApplicationUpdate
        description: Describes application updates
        type: string
      - in: query
        name: CurrentApplicationVersionId
        description: The current application version ID
        type: string
      responses:
        200:
          description: OK
      tags:
      - Applications
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