---
name: Instructure
x-slug: instructure
description: Instructure makes software that makes smarter people. Products include
  Canvas LMS, Bridge and Canvas Network.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
x-kinRank: "8"
x-alexaRank: "367"
tags: Analytics
created: "2018-06-17"
modified: "2018-06-17"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/apis.md
specificationVersion: "0.14"
apis:
- name: Instructure Canvas Courses API Get course-level participation data
  x-api-slug: instructure-canvas-courses-api
  description: Get course-level participation data.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//courses/{course_id}/analytics/activity
  tags: Courses,Course,Id,Analytics,Activity
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsactivity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsactivity-get-openapi.md
- name: Instructure Canvas Courses API Get course-level assignment data
  x-api-slug: instructure-canvas-courses-api
  description: Get course-level assignment data.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//courses/{course_id}/analytics/assignments
  tags: Courses,Course,Id,Analytics,Assignments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsassignments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsassignments-get-openapi.md
- name: Instructure Canvas Courses API Get course-level student summary data
  x-api-slug: instructure-canvas-courses-api
  description: Get course-level student summary data.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//courses/{course_id}/analytics/student_summaries
  tags: Courses,Course,Id,Analytics,Student,Summaries
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsstudent-summaries-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsstudent-summaries-get-openapi.md
- name: Instructure Canvas Courses API Get user-in-a-course-level participation data
  x-api-slug: instructure-canvas-courses-api
  description: Get user-in-a-course-level participation data.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//courses/{course_id}/analytics/users/student_id/activity
  tags: Courses,Course,Id,Analytics,Users,Student,Id,Activity
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsusersstudent-idactivity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsusersstudent-idactivity-get-openapi.md
- name: Instructure Canvas Courses API Get user-in-a-course-level assignment data
  x-api-slug: instructure-canvas-courses-api
  description: Get user-in-a-course-level assignment data.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//courses/{course_id}/analytics/users/student_id/assignments
  tags: Courses,Course,Id,Analytics,Users,Student,Id,Assignments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsusersstudent-idassignments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsusersstudent-idassignments-get-openapi.md
- name: Instructure Canvas Courses API Get user-in-a-course-level messaging data
  x-api-slug: instructure-canvas-courses-api
  description: Get user-in-a-course-level messaging data.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1//courses/{course_id}/analytics/users/student_id/communication
  tags: Courses,Course,Id,Analytics,Users,Student,Id,Communication
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsusersstudent-idcommunication-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/coursescourse-idanalyticsusersstudent-idcommunication-get-openapi.md
- name: Instructure Canvas Courses API
  x-api-slug: instructure-canvas-courses-api
  description: Instructure makes software that makes smarter people. Products include
    Canvas LMS, Bridge and Canvas Network.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/820-instructure.jpg
  humanURL: http://instructure.com
  baseURL: https://canvas.instructure.com//api/v1
  tags: Analytics
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/analytics/master/_listings/instructure/openapi.md
x-common:
- type: x-blog
  url: http://blog.instructure.com
- type: x-blog-rss
  url: http://voice.instructure.com/CMS/UI/Modules/BizBlogger/rss.aspx?tabid=772438&moduleid=1638884&maxcount=25&t=415c2e5d197a4d6f7cdcc81385b677f1
- type: x-crunchbase
  url: https://crunchbase.com/organization/instructure
- type: x-crunchbase
  url: http://www.crunchbase.com/company/instructure
- type: x-email
  url: info@instructure.com
- type: x-email
  url: jobs@instructure.com
- type: x-email
  url: privacy@instructure.com
- type: x-email
  url: legal@instructure.com
- type: x-github
  url: https://github.com/instructure
- type: x-twitter
  url: https://twitter.com/instructure
- type: x-website
  url: http://instructure.com
- type: x-website
  url: https://canvas.instructure.com/doc/api/index.html
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---