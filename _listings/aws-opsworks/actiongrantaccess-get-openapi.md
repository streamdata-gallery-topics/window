---
swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 0
info:
  title: AWS OpsWorks API Grant Access
  version: 1.0.0
  description: NoteThis action can be used only with Windows stacks.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GrantAccess:
    get:
      summary: Grant Access
      description: NoteThis action can be used only with Windows stacks.
      operationId: grantAccess
      x-api-path-slug: actiongrantaccess-get
      parameters:
      - in: query
        name: InstanceId
        description: The instances AWS OpsWorks Stacks ID
        type: string
      - in: query
        name: ValidForInMinutes
        description: The length of time (in minutes) that the grant is valid
        type: string
      responses:
        200:
          description: OK
      tags:
      - Grant
      - Access
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