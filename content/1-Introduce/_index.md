---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 1. </b> "
---
#### Overview

AWS Application Migration Service (MGN) is an advanced automated rehosting solution that simplifies, accelerates, and reduces costs for migrating applications to AWS. It enables companies to lift and shift a large number of physical, virtual, or cloud servers without compatibility issues, performance disruptions, or lengthy migration times. MGN copies the source servers into your AWS account. When you are ready, it automatically converts and launches your servers on AWS so that you can quickly take advantage of the cost savings, productivity, sustainability, and flexibility benefits of the cloud. Once your application is running on AWS, you can leverage AWS services and capabilities to easily re-platform or modernize those applications – making migration and modernization a fast path forward.

AWS Application Migration Service needs to be initiated on the service interface by creating a replication template when using it for the first time.

- After you create a replication template, the initialization process will automatically take place.

- Only the Admin user of your AWS account can initiate the Application Migration Service.

#### Create IAM Roles

During the initialization process, the following IAM roles will be created:

- AWSServiceRoleForApplicationMigrationService
- AWSApplicationMigrationReplicationServerRole
- AWSApplicationMigrationConversionServerRole
- AWSApplicationMigrationMGHRole
- AWSApplicationMigrationLaunchInstanceWithDrsRole
- AWSApplicationMigrationLaunchInstanceWithSsmRole
- AWSApplicationMigrationAgentRole

#### Additional Policies

You can create roles with specific permissions for the Application Migration Service. The service comes with pre-defined IAM management policies, as follows:

- AWSApplicationMigrationFullAccess - This policy provides access to all the public APIs of AWS Application Migration Service (MGN), as well as access to read KMS key information.

- AWSApplicationMigrationEC2Access - This policy allows the necessary Amazon EC2 operations to use Application Migration Service (MGN) to launch migrated servers as EC2 instances.

- AWSApplicationMigrationSSMAccess - This policy allows the necessary Amazon SSM operations to use Application Migration Service (MGN) to run SSM documents after moving the source servers.

- AWSApplicationMigrationReadOnlyAccess - This policy only allows users to view all the data available in the Application Migration Service interface, but does not allow them to modify any data or perform any actions. The policy also includes some read-only EC2 permissions.

- AWSApplicationMigrationAgentPolicy - This policy allows users to install the AWS Replication Agent.

- AWSApplicationMigrationAgentInstallationPolicy - This policy allows users to install the AWS Replication Agent.