---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API Resolve path
  description: Resolve path.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/folders/by_path:
    get:
      summary: Resolve path
      description: Resolve path.
      operationId: resolve-path
      x-api-path-slug: coursescourse-idfoldersby-path-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Folders
      - By
      - Path
  /courses/{course_id}/folders/by_path/*full_path:
    get:
      summary: Resolve path
      description: Resolve path.
      operationId: resolve-path
      x-api-path-slug: coursescourse-idfoldersby-pathfull-path-get
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Folders
      - By
      - Path
      - '*full'
      - Path
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