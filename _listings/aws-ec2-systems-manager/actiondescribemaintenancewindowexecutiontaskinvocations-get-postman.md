{
  "info": {
    "name": "Amazon EC2 Systems Manager API Describe Maintenance Window Execution Task Invocations",
    "_postman_id": "9c1223fe-ccf3-4053-924a-aacdbbaf7b0d",
    "description": "Retrieves the individual task executions (one per target) for a particular task executed\n   as part of a Maintenance Window execution.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Deregister",
      "item": [
        {
          "id": "f1e98f14-4875-45c6-8b92-fb425cac08f8",
          "name": "deregisterTaskFromMaintenanceWindow",
          "request": {
            "url": "http://example.com/api/?Action=DeregisterTaskFromMaintenanceWindow?WindowId=WindowId&WindowTaskId=WindowTaskId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes a task from a Maintenance Window."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "53962a3c-cabf-4c42-a8ae-c537edbdf47f"
            }
          ]
        }
      ]
    },
    {
      "name": "Maintenance",
      "item": [
        {
          "id": "520994ea-eec8-4ca0-a1ea-943eccb592bb",
          "name": "describeMaintenanceWindowExecutionTaskInvocations",
          "request": {
            "url": "http://example.com/api/?Action=DescribeMaintenanceWindowExecutionTaskInvocations?Filters=Filters&MaxResults=MaxResults&NextToken=NextToken&TaskId=TaskId&WindowExecutionId=WindowExecutionId",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the individual task executions (one per target) for a particular task executed\n   as part of a Maintenance Window execution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "38544620-de0f-453f-9e7d-3d400ca028b6"
            }
          ]
        }
      ]
    }
  ]
}