{
  "info": {
    "name": "AWS EC2 API Cancel Bundle Task",
    "_postman_id": "abf020a1-b736-4a83-b7a7-c5627085fa1c",
    "description": "Cancels a bundling operation for an instance store-backed Windows instance.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Bundle Task",
      "item": [
        {
          "id": "94efe640-0e42-40a6-b3ab-dbd8368a25c4",
          "name": "cancelbundletask",
          "request": {
            "url": "http://example.com/api/?Action=CancelBundleTask?BundleId.N=BundleId.N&DryRun=DryRun&Filter.N=Filter.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Cancels a bundling operation for an instance store-backed Windows instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "123c8043-251e-4649-8904-11425ada4820"
            }
          ]
        }
      ]
    }
  ]
}