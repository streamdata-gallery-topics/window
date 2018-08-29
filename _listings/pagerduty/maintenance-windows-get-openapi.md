---
swagger: "2.0"
x-collection-name: PagerDuty
x-complete: 0
info:
  title: PagerDuty List maintenance windows
  version: 1.0.0
  description: List existing maintenance windows, optionally filtered by service and/or
    team, or whether they are from the past, present or future.
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