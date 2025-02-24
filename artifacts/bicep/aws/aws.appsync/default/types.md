# AWS.AppSync @ default

## Resource AWS.AppSync/DomainName@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.AppSync/DomainNameProperties](#awsappsyncdomainnameproperties) (Required): properties of the resource

## Resource AWS.AppSync/DomainNameApiAssociation@default
* **Valid Scope(s)**: Unknown
### Properties
* **alias**: string (Required): the resource alias
* **name**: string: the resource name
* **properties**: [AWS.AppSync/DomainNameApiAssociationProperties](#awsappsyncdomainnameapiassociationproperties) (Required): properties of the resource

## AWS.AppSync/DomainNameProperties
### Properties
* **AppSyncDomainName**: string (ReadOnly)
* **CertificateArn**: string (Required)
* **Description**: string
* **DomainName**: string (Required, Identifier)
* **HostedZoneId**: string (ReadOnly)

## AWS.AppSync/DomainNameApiAssociationProperties
### Properties
* **ApiAssociationIdentifier**: string (ReadOnly, Identifier)
* **ApiId**: string (Required)
* **DomainName**: string (Required)

