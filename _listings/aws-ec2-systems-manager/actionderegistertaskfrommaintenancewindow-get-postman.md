{
  "info": {
    "name": "Amazon EC2 Systems Manager API Deregister Task From Maintenance Window",
    "_postman_id": "6526244b-9cde-4a88-a3dd-ac3a990527b9",
    "description": "Removes a task from a Maintenance Window.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Deregister",
      "item": [
        {
          "id": "494ae1fb-1173-4b38-83cc-40090b2687d2",
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
              "id": "ac162ded-2524-406d-9715-20d6bcde45ba"
            }
          ]
        }
      ]
    }
  ]
}