swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 1
info:
  title: AWS EC2 API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=BundleInstance:
    get:
      summary: Bundle Instance
      description: Bundles an Amazon instance store-backed Windows instance.
      operationId: bundleinstance
      x-api-path-slug: actionbundleinstance-get
      parameters:
      - in: query
        name: BundleId
        description: The ID of the bundle task
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Bundle Instance
  /?Action=CancelBundleTask:
    get:
      summary: Cancel Bundle Task
      description: Cancels a bundling operation for an instance store-backed Windows
        instance.
      operationId: cancelbundletask
      x-api-path-slug: actioncancelbundletask-get
      parameters:
      - in: query
        name: BundleId.N
        description: One or more bundle task IDs
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      responses:
        200:
          description: OK
      tags:
      - Bundle Task
  /?Action=GetPasswordData:
    get:
      summary: Get Password Data
      description: Retrieves the encrypted administrator password for an instance
        running Windows.
      operationId: getpassworddata
      x-api-path-slug: actiongetpassworddata-get
      parameters:
      - in: query
        name: Attribute
        description: The name of the attribute
        type: string
      - in: query
        name: BlockDeviceMapping.N
        description: Modifies the DeleteOnTermination attribute for volumesthat are
          currently attached
        type: string
      - in: query
        name: DisableApiTermination
        description: If the value is true, you cant terminate the instance using the
          Amazon EC2      console, CLI, or API; otherwise, you can
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: EbsOptimized
        description: Specifies whether the instance is optimized for EBS I/O
        type: string
      - in: query
        name: EnaSupport
        description: Set to true to enable enhanced networking with ENA for the instance
        type: string
      - in: query
        name: GroupId.N
        description: '[EC2-VPC] Changes the security groups of the instance'
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: InstanceInitiatedShutdownBehavior
        description: Specifies whether an instance stops or terminates when you initiate
          shutdown from the instance (using the operating system command for system
          shutdown)
        type: string
      - in: query
        name: InstanceType
        description: Changes the instance type to the specified value
        type: string
      - in: query
        name: Kernel
        description: Changes the instances kernel to the specified value
        type: string
      - in: query
        name: Ramdisk
        description: Changes the instances RAM disk to the specified value
        type: string
      - in: query
        name: SourceDestCheck
        description: Specifies whether source/destination checking is enabled
        type: string
      - in: query
        name: SriovNetSupport
        description: Set to simple to enable enhanced networking with the Intel 82599
          Virtual Function interface for the instance
        type: string
      - in: query
        name: UserData
        description: Changes the instances user data to the specified value
        type: string
      - in: query
        name: Value
        description: A new value for the attribute
        type: string
      responses:
        200:
          description: OK
      tags:
      - Password Data