---
swagger: "2.0"
x-collection-name: PagerDuty
x-complete: 0
info:
  title: PagerDuty Delete or end a maintenance window
  version: 1.0.0
  description: Delete an existing maintenance window if it's in the future, or end
    it if it's currently on-going. If the maintenance window has already ended it
    cannot be deleted.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /maintenance_windows:
    get:
      summary: List maintenance windows
      description: List existing maintenance windows, optionally filtered by service
        and/or team, or whether they are from the past, present or future.
      operationId: list-existing-maintenance-windows-optionally-filtered-by-service-andor-team-or-whether-they-are-from
      x-api-path-slug: maintenance-windows-get
      parameters:
      - in: query
        name: filter
        description: Only return maintenance windows in a given state
      - in: query
        name: No Name
      - in: query
        name: query
        description: Filters the results, showing only the maintenance windows whose
          descriptions contain the query
      responses:
        200:
          description: OK
      tags:
      - Maintenance Windows
    post:
      summary: Create a maintenance window
      description: Create a new maintenance window for the specified services. No
        new incidents will be created for a service that is in maintenance.
      operationId: create-a-new-maintenance-window-for-the-specified-services-no-new-incidents-will-be-created-for-a-se
      x-api-path-slug: maintenance-windows-post
      parameters:
      - in: body
        name: maintenance_window
        description: The maintenance window object
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Maintenance Windows
  /maintenance_windows/{id}:
    get:
      summary: Get a maintenance window
      description: Get an existing maintenance window.
      operationId: get-an-existing-maintenance-window
      x-api-path-slug: maintenance-windowsid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Maintenance Windows
    delete:
      summary: Delete or end a maintenance window
      description: Delete an existing maintenance window if it's in the future, or
        end it if it's currently on-going. If the maintenance window has already ended
        it cannot be deleted.
      operationId: delete-an-existing-maintenance-window-if-its-in-the-future-or-end-it-if-its-currently-ongoing-if-the
      x-api-path-slug: maintenance-windowsid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Maintenance Windows
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