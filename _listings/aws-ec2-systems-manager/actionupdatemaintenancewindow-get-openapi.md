---
swagger: "2.0"
x-collection-name: AWS EC2 Systems Manager
x-complete: 0
info:
  title: Amazon EC2 Systems Manager API Update Maintenance Window
  version: 1.0.0
  description: Updates an existing Maintenance Window.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateMaintenanceWindow:
    get:
      summary: Create Maintenance Window
      description: Creates a new Maintenance Window.
      operationId: createMaintenanceWindow
      x-api-path-slug: actioncreatemaintenancewindow-get
      parameters:
      - in: query
        name: AllowUnassociatedTargets
        description: Whether targets must be registered with the Maintenance Window
          before tasks can be   defined for those targets
        type: string
      - in: query
        name: ClientToken
        description: User-provided idempotency token
        type: string
      - in: query
        name: Cutoff
        description: The number of hours before the end of the Maintenance Window
          that Systems Manager stops   scheduling new tasks for execution
        type: string
      - in: query
        name: Duration
        description: The duration of the Maintenance Window in hours
        type: string
      - in: query
        name: Name
        description: The name of the Maintenance Window
        type: string
      - in: query
        name: Schedule
        description: The schedule of the Maintenance Window in the form of a cron
          or rate   expression
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
  /?Action=DeleteMaintenanceWindow:
    get:
      summary: Delete Maintenance Window
      description: Deletes a Maintenance Window.
      operationId: deleteMaintenanceWindow
      x-api-path-slug: actiondeletemaintenancewindow-get
      parameters:
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
  /?Action=DeregisterTargetFromMaintenanceWindow:
    get:
      summary: Deregister Target From Maintenance Window
      description: Removes a target from a Maintenance Window.
      operationId: deregisterTargetFromMaintenanceWindow
      x-api-path-slug: actionderegistertargetfrommaintenancewindow-get
      parameters:
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window the target should be removed
          from
        type: string
      - in: query
        name: WindowTargetId
        description: The ID of the target definition to remove
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deregister
      - Target
      - From
      - Maintenance
      - Window
  /?Action=DeregisterTaskFromMaintenanceWindow:
    get:
      summary: Deregister Task From Maintenance Window
      description: Removes a task from a Maintenance Window.
      operationId: deregisterTaskFromMaintenanceWindow
      x-api-path-slug: actionderegistertaskfrommaintenancewindow-get
      parameters:
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window the task should be removed from
        type: string
      - in: query
        name: WindowTaskId
        description: The ID of the task to remove from the Maintenance Window
        type: string
      responses:
        200:
          description: OK
      tags:
      - Deregister
      - Task
      - From
      - Maintenance
      - Window
  /?Action=DescribeMaintenanceWindowExecutions:
    get:
      summary: Describe Maintenance Window Executions
      description: |-
        Lists the executions of a Maintenance Window (meaning, information about when the
           Maintenance Window was scheduled to be active and information about tasks registered and run with
           the Maintenance Window).
      operationId: describeMaintenanceWindowExecutions
      x-api-path-slug: actiondescribemaintenancewindowexecutions-get
      parameters:
      - in: query
        name: Filters
        description: 'Each entry in the array is a structure containing:'
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window whose executions should be retrieved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Executions
  /?Action=DescribeMaintenanceWindowExecutionTaskInvocations:
    get:
      summary: Describe Maintenance Window Execution Task Invocations
      description: |-
        Retrieves the individual task executions (one per target) for a particular task executed
           as part of a Maintenance Window execution.
      operationId: describeMaintenanceWindowExecutionTaskInvocations
      x-api-path-slug: actiondescribemaintenancewindowexecutiontaskinvocations-get
      parameters:
      - in: query
        name: Filters
        description: Optional filters used to scope down the returned task invocations
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: TaskId
        description: The ID of the specific task in the Maintenance Window task that
          should be   retrieved
        type: string
      - in: query
        name: WindowExecutionId
        description: The ID of the Maintenance Window execution the task is part of
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Execution
      - Task
      - Invocations
  /?Action=DescribeMaintenanceWindowExecutionTasks:
    get:
      summary: Describe Maintenance Window Execution Tasks
      description: For a given Maintenance Window execution, lists the tasks that
        were executed.
      operationId: describeMaintenanceWindowExecutionTasks
      x-api-path-slug: actiondescribemaintenancewindowexecutiontasks-get
      parameters:
      - in: query
        name: Filters
        description: Optional filters used to scope down the returned tasks
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: WindowExecutionId
        description: The ID of the Maintenance Window execution whose task executions
          should be   retrieved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Execution
      - Tasks
  /?Action=DescribeMaintenanceWindows:
    get:
      summary: Describe Maintenance Windows
      description: Retrieves the Maintenance Windows in an AWS account.
      operationId: describeMaintenanceWindows
      x-api-path-slug: actiondescribemaintenancewindows-get
      parameters:
      - in: query
        name: Filters
        description: Optional filters used to narrow down the scope of the returned
          Maintenance Windows
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Windows
  /?Action=DescribeMaintenanceWindowTargets:
    get:
      summary: Describe Maintenance Window Targets
      description: Lists the targets registered with the Maintenance Window.
      operationId: describeMaintenanceWindowTargets
      x-api-path-slug: actiondescribemaintenancewindowtargets-get
      parameters:
      - in: query
        name: Filters
        description: Optional filters that can be used to narrow down the scope of
          the returned window   targets
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window whose targets should be retrieved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Targets
  /?Action=DescribeMaintenanceWindowTasks:
    get:
      summary: Describe Maintenance Window Tasks
      description: Lists the tasks in a Maintenance Window.
      operationId: describeMaintenanceWindowTasks
      x-api-path-slug: actiondescribemaintenancewindowtasks-get
      parameters:
      - in: query
        name: Filters
        description: Optional filters used to narrow down the scope of the returned
          tasks
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of items to return for this call
        type: string
      - in: query
        name: NextToken
        description: The token for the next set of items to return
        type: string
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window whose tasks should be retrieved
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Tasks
  /?Action=GetMaintenanceWindow:
    get:
      summary: Get Maintenance Window
      description: Retrieves a Maintenance Window.
      operationId: getMaintenanceWindow
      x-api-path-slug: actiongetmaintenancewindow-get
      parameters:
      - in: query
        name: WindowId
        description: The ID of the desired Maintenance Window
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
  /?Action=GetMaintenanceWindowExecution:
    get:
      summary: Get Maintenance Window Execution
      description: |-
        Retrieves details about a specific task executed as part of a Maintenance Window
           execution.
      operationId: getMaintenanceWindowExecution
      x-api-path-slug: actiongetmaintenancewindowexecution-get
      parameters:
      - in: query
        name: WindowExecutionId
        description: The ID of the Maintenance Window execution that includes the
          task
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Execution
  /?Action=GetMaintenanceWindowExecutionTask:
    get:
      summary: Get Maintenance Window Execution Task
      description: |-
        Retrieves the details about a specific task executed as part of a Maintenance Window
           execution.
      operationId: getMaintenanceWindowExecutionTask
      x-api-path-slug: actiongetmaintenancewindowexecutiontask-get
      parameters:
      - in: query
        name: TaskId
        description: The ID of the specific task execution in the Maintenance Window
          task that should be   retrieved
        type: string
      - in: query
        name: WindowExecutionId
        description: The ID of the Maintenance Window execution that includes the
          task
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
      - Execution
      - Task
  /?Action=RegisterTargetWithMaintenanceWindow:
    get:
      summary: Register Target With Maintenance Window
      description: Registers a target with a Maintenance Window.
      operationId: registerTargetWithMaintenanceWindow
      x-api-path-slug: actionregistertargetwithmaintenancewindow-get
      parameters:
      - in: query
        name: ClientToken
        description: User-provided idempotency token
        type: string
      - in: query
        name: OwnerInformation
        description: User-provided value that will be included in any CloudWatch events
          raised while running   tasks for these targets in this Maintenance Window
        type: string
      - in: query
        name: ResourceType
        description: The type of target being registered with the Maintenance Window
        type: string
      - in: query
        name: Targets
        description: The targets (either instances or tags)
        type: string
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window the target should be registered
          with
        type: string
      responses:
        200:
          description: OK
      tags:
      - Register
      - TargetMaintenance
      - Window
  /?Action=RegisterTaskWithMaintenanceWindow:
    get:
      summary: Register Task With Maintenance Window
      description: Adds a new task to a Maintenance Window.
      operationId: registerTaskWithMaintenanceWindow
      x-api-path-slug: actionregistertaskwithmaintenancewindow-get
      parameters:
      - in: query
        name: ClientToken
        description: User-provided idempotency token
        type: string
      - in: query
        name: LoggingInfo
        description: A structure containing information about an Amazon S3 bucket
          to write instance-level logs to
        type: string
      - in: query
        name: MaxConcurrency
        description: The maximum number of targets this task can be run for in parallel
        type: string
      - in: query
        name: MaxErrors
        description: The maximum number of errors allowed before this task stops being
          scheduled
        type: string
      - in: query
        name: Priority
        description: The priority of the task in the Maintenance Window, the lower
          the number the higher the   priority
        type: string
      - in: query
        name: ServiceRoleArn
        description: The role that should be assumed when executing the task
        type: string
      - in: query
        name: Targets
        description: The targets (either instances or tags)
        type: string
      - in: query
        name: TaskArn
        description: The ARN of the task to execute
        type: string
      - in: query
        name: TaskParameters
        description: The parameters that should be passed to the task when it is executed
        type: string
      - in: query
        name: TaskType
        description: The type of task being registered
        type: string
      - in: query
        name: WindowId
        description: The id of the Maintenance Window the task should be added to
        type: string
      responses:
        200:
          description: OK
      tags:
      - Register
      - TaskMaintenance
      - Window
  /?Action=UpdateMaintenanceWindow:
    get:
      summary: Update Maintenance Window
      description: Updates an existing Maintenance Window.
      operationId: updateMaintenanceWindow
      x-api-path-slug: actionupdatemaintenancewindow-get
      parameters:
      - in: query
        name: AllowUnassociatedTargets
        description: Whether targets must be registered with the Maintenance Window
          before tasks can be   defined for those targets
        type: string
      - in: query
        name: Cutoff
        description: The number of hours before the end of the Maintenance Window
          that Systems Manager stops   scheduling new tasks for execution
        type: string
      - in: query
        name: Duration
        description: The duration of the Maintenance Window in hours
        type: string
      - in: query
        name: Enabled
        description: Whether the Maintenance Window is enabled
        type: string
      - in: query
        name: Name
        description: The name of the Maintenance Window
        type: string
      - in: query
        name: Schedule
        description: The schedule of the Maintenance Window in the form of a cron
          or rate   expression
        type: string
      - in: query
        name: WindowId
        description: The ID of the Maintenance Window to update
        type: string
      responses:
        200:
          description: OK
      tags:
      - Maintenance
      - Window
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