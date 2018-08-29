swagger: "2.0"
x-collection-name: AWS OpsWorks
x-complete: 1
info:
  title: AWS OpsWorks API
  version: 1.0.0
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