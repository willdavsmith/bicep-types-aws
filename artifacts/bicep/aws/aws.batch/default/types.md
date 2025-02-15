# AWS.Batch @ default

## Resource AWS.Batch/ComputeEnvironment@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.Batch/ComputeEnvironmentProperties](#awsbatchcomputeenvironmentproperties) (Required): properties of the resource

## Resource AWS.Batch/JobQueue@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.Batch/JobQueueProperties](#awsbatchjobqueueproperties) (Required): properties of the resource

## Resource AWS.Batch/SchedulingPolicy@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.Batch/SchedulingPolicyProperties](#awsbatchschedulingpolicyproperties): properties of the resource

## AWS.Batch/ComputeEnvironmentProperties
### Properties
* **ComputeEnvironmentArn**: string (ReadOnly, Identifier)
* **ComputeEnvironmentName**: string
* **ComputeResources**: [ComputeResources](#computeresources)
* **EksConfiguration**: [EksConfiguration](#eksconfiguration)
* **ReplaceComputeEnvironment**: bool (WriteOnly)
* **ServiceRole**: string
* **State**: string
* **Tags**: [ComputeEnvironment_Tags](#computeenvironmenttags): A key-value pair to associate with a resource.
* **Type**: string (Required)
* **UnmanagedvCpus**: int
* **UpdatePolicy**: [UpdatePolicy](#updatepolicy) (WriteOnly)

## ComputeResources
### Properties
* **AllocationStrategy**: string
* **BidPercentage**: int
* **DesiredvCpus**: int
* **Ec2Configuration**: [Ec2ConfigurationObject](#ec2configurationobject)[]
* **Ec2KeyPair**: string
* **ImageId**: string
* **InstanceRole**: string
* **InstanceTypes**: string[]
* **LaunchTemplate**: [LaunchTemplateSpecification](#launchtemplatespecification)
* **MaxvCpus**: int (Required)
* **MinvCpus**: int
* **PlacementGroup**: string
* **SecurityGroupIds**: string[]
* **SpotIamFleetRole**: string
* **Subnets**: string[] (Required)
* **Tags**: [ComputeEnvironment_Tags](#computeenvironmenttags): A key-value pair to associate with a resource.
* **Type**: string (Required)
* **UpdateToLatestImageVersion**: bool (WriteOnly)

## Ec2ConfigurationObject
### Properties
* **ImageIdOverride**: string
* **ImageKubernetesVersion**: string
* **ImageType**: string (Required)

## LaunchTemplateSpecification
### Properties
* **LaunchTemplateId**: string
* **LaunchTemplateName**: string
* **Version**: string

## ComputeEnvironment_Tags
### Properties

## EksConfiguration
### Properties
* **EksClusterArn**: string (Required)
* **KubernetesNamespace**: string (Required)

## ComputeEnvironment_Tags
### Properties

## UpdatePolicy
### Properties
* **JobExecutionTimeoutMinutes**: int
* **TerminateJobsOnUpdate**: bool

## AWS.Batch/JobQueueProperties
### Properties
* **ComputeEnvironmentOrder**: [ComputeEnvironmentOrder](#computeenvironmentorder)[] (Required)
* **JobQueueArn**: string (ReadOnly, Identifier)
* **JobQueueName**: string
* **Priority**: int (Required)
* **SchedulingPolicyArn**: string
* **State**: string
* **Tags**: [JobQueue_Tags](#jobqueuetags): A key-value pair to associate with a resource.

## ComputeEnvironmentOrder
### Properties
* **ComputeEnvironment**: string (Required)
* **Order**: int (Required)

## JobQueue_Tags
### Properties

## AWS.Batch/SchedulingPolicyProperties
### Properties
* **Arn**: string (ReadOnly, Identifier)
* **FairsharePolicy**: [FairsharePolicy](#fairsharepolicy)
* **Name**: string: Name of Scheduling Policy.
* **Tags**: [SchedulingPolicy_Tags](#schedulingpolicytags): A key-value pair to associate with a resource.

## FairsharePolicy
### Properties
* **ComputeReservation**: int
* **ShareDecaySeconds**: int
* **ShareDistribution**: [ShareAttributes](#shareattributes)[]: List of Share Attributes

## ShareAttributes
### Properties
* **ShareIdentifier**: string
* **WeightFactor**: int

## SchedulingPolicy_Tags
### Properties

