# AWS.MSK @ default

## Resource AWS.MSK/BatchScramSecret@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.MSK/BatchScramSecretProperties](#awsmskbatchscramsecretproperties) (Required): properties of the resource

## Resource AWS.MSK/Cluster@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.MSK/ClusterProperties](#awsmskclusterproperties) (Required): properties of the resource

## Resource AWS.MSK/Configuration@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.MSK/ConfigurationProperties](#awsmskconfigurationproperties) (Required): properties of the resource

## AWS.MSK/BatchScramSecretProperties
### Properties
* **ClusterArn**: string (Required, Identifier)
* **SecretArnList**: string[]

## AWS.MSK/ClusterProperties
### Properties
* **Arn**: string (ReadOnly, Identifier)
* **BrokerNodeGroupInfo**: [BrokerNodeGroupInfo](#brokernodegroupinfo) (Required)
* **ClientAuthentication**: [ClientAuthentication](#clientauthentication)
* **ClusterName**: string (Required)
* **ConfigurationInfo**: [ConfigurationInfo](#configurationinfo)
* **CurrentVersion**: string: The current version of the MSK cluster
* **EncryptionInfo**: [EncryptionInfo](#encryptioninfo)
* **EnhancedMonitoring**: string
* **KafkaVersion**: string (Required)
* **LoggingInfo**: [LoggingInfo](#logginginfo)
* **NumberOfBrokerNodes**: int (Required)
* **OpenMonitoring**: [OpenMonitoring](#openmonitoring)
* **StorageMode**: string
* **Tags**: [Cluster_Tags](#clustertags): A key-value pair to associate with a resource.

## BrokerNodeGroupInfo
### Properties
* **BrokerAZDistribution**: string
* **ClientSubnets**: string[] (Required)
* **ConnectivityInfo**: [ConnectivityInfo](#connectivityinfo)
* **InstanceType**: string (Required)
* **SecurityGroups**: string[]
* **StorageInfo**: [StorageInfo](#storageinfo)

## ConnectivityInfo
### Properties
* **PublicAccess**: [PublicAccess](#publicaccess)
* **VpcConnectivity**: [VpcConnectivity](#vpcconnectivity)

## PublicAccess
### Properties
* **Type**: string

## VpcConnectivity
### Properties
* **ClientAuthentication**: [VpcConnectivityClientAuthentication](#vpcconnectivityclientauthentication)

## VpcConnectivityClientAuthentication
### Properties
* **Sasl**: [VpcConnectivitySasl](#vpcconnectivitysasl)
* **Tls**: [VpcConnectivityTls](#vpcconnectivitytls)

## VpcConnectivitySasl
### Properties
* **Iam**: [VpcConnectivityIam](#vpcconnectivityiam)
* **Scram**: [VpcConnectivityScram](#vpcconnectivityscram)

## VpcConnectivityIam
### Properties
* **Enabled**: bool (Required)

## VpcConnectivityScram
### Properties
* **Enabled**: bool (Required)

## VpcConnectivityTls
### Properties
* **Enabled**: bool (Required)

## StorageInfo
### Properties
* **EBSStorageInfo**: [EBSStorageInfo](#ebsstorageinfo)

## EBSStorageInfo
### Properties
* **ProvisionedThroughput**: [ProvisionedThroughput](#provisionedthroughput)
* **VolumeSize**: int

## ProvisionedThroughput
### Properties
* **Enabled**: bool
* **VolumeThroughput**: int

## ClientAuthentication
### Properties
* **Sasl**: [Sasl](#sasl)
* **Tls**: [Tls](#tls)
* **Unauthenticated**: [Unauthenticated](#unauthenticated)

## Sasl
### Properties
* **Iam**: [Iam](#iam)
* **Scram**: [Scram](#scram)

## Iam
### Properties
* **Enabled**: bool (Required)

## Scram
### Properties
* **Enabled**: bool (Required)

## Tls
### Properties
* **CertificateAuthorityArnList**: string[]
* **Enabled**: bool

## Unauthenticated
### Properties
* **Enabled**: bool (Required)

## ConfigurationInfo
### Properties
* **Arn**: string (Required, Identifier)
* **Revision**: int (Required)

## EncryptionInfo
### Properties
* **EncryptionAtRest**: [EncryptionAtRest](#encryptionatrest)
* **EncryptionInTransit**: [EncryptionInTransit](#encryptionintransit)

## EncryptionAtRest
### Properties
* **DataVolumeKMSKeyId**: string (Required)

## EncryptionInTransit
### Properties
* **ClientBroker**: string
* **InCluster**: bool

## LoggingInfo
### Properties
* **BrokerLogs**: [BrokerLogs](#brokerlogs) (Required)

## BrokerLogs
### Properties
* **CloudWatchLogs**: [CloudWatchLogs](#cloudwatchlogs)
* **Firehose**: [Firehose](#firehose)
* **S3**: [S3](#s3)

## CloudWatchLogs
### Properties
* **Enabled**: bool (Required)
* **LogGroup**: string

## Firehose
### Properties
* **DeliveryStream**: string
* **Enabled**: bool (Required)

## S3
### Properties
* **Bucket**: string
* **Enabled**: bool (Required)
* **Prefix**: string

## OpenMonitoring
### Properties
* **Prometheus**: [Prometheus](#prometheus) (Required)

## Prometheus
### Properties
* **JmxExporter**: [JmxExporter](#jmxexporter)
* **NodeExporter**: [NodeExporter](#nodeexporter)

## JmxExporter
### Properties
* **EnabledInBroker**: bool (Required)

## NodeExporter
### Properties
* **EnabledInBroker**: bool (Required)

## Cluster_Tags
### Properties

## AWS.MSK/ConfigurationProperties
### Properties
* **Arn**: string (ReadOnly, Identifier)
* **Description**: string
* **KafkaVersionsList**: string[]
* **Name**: string (Required)
* **ServerProperties**: string (Required, WriteOnly)

