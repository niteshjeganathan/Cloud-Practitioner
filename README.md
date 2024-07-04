# Cloud-Practitioner

## Module 1 - Cloud Concepts Overview
### Cloud Service Models
* IaaS - AWS EC2
* PaaS - AWS Elastic Beanstalk
* SaaS - AWS Trusted Advisor

### Cloud Deployment Models
* Cloud
* Hybrid
* On-Premises

### Advantages of Cloud
* Trade capital expenses for variable expenses
* Maintenance is reduced
* Massive economies of scale
* Stop guessing capacity
* Increase speed and agility - Faster procurement of resources
* No need to spend money on running and maintaining data centers
* Can go global in minutes

### Interacting with AWS
* AWS Management Console - GUI
* Command Line Interface - AWS CLI
* Software Development Kits - SDK's
> Note: All three options are built using REST like programming interface, serving as the foundation of AWS.

### AWS Cloud Adoption Framework ( AWS CAF )
* Provides guidance and support to accelerate cloud adoption
* Core Perspectives
  * Business Capabilities
    * Business - Ensure organisation's goals and business strategies align with IT strategies and goals.
    * People - Organisation's structure and roles, new skills and process requirements
    * Governance - Ensure skills and processes that align IT strategy and goals with business strategy and goals
  * Technical Capabilities
    * Platform - Understand and communicate the nature of IT systems and their relationships
    * Security - Organisation must meet it's security objectives
    * Operations - Align and support the operations of the business


## Module 2 - Cloud Economics and Billing
### Drivers of Cost 
* Compute - Charged per hour/second
* Storage - Charged per GB
* Data Transfer - Inbound free, Outbound is charged

### Pricing Policies 
* Pay for what you use
* Pay less by using more
* Pay less as AWS grows
* Custom pricing - for unique requirements
* AWS Free tier - gain hands-on experience

### Reserved Instances 
* AURI - All Upfront Reserved Instance
* PURI - Partial Upfront Reserved Instance
* NURI - No Upfront Reserved Instance

### TCO - Total Cost of Ownership
* Server costs - Hardware, Software and Physical costs
* Storage costs - Hardware, Administration and Facilities
* Network costs - Hardware, Administration and Facilities
* IT Labor Costs - Administer entire solution

### AWS Pricing Calculator
* Used to predict monthly expenses on AWS services
* Can be analysed and used for cost reduction
* Can be used for model your solutions
* Components
  * Total for first 12 months
  * Total upfront
  * Total Monthly

### Additional Benefits
* Hard Benefits
  * Reduced expenditure on hardware, software
  * Reduced operational costs
  * Reduced operational personnel
* Soft Benefits
  * Reuse of service and applications
  * Increased developer satisfaction
  * Increased customer satisfaction
  * Agile business processes
  * Increase in global reach

### AWS Organisations
* Free account management service
* Consolidate multiple AWS accounts into an organisational tree
* Root - Organisational Units ( OU's ). Each OU has AWS accounds under it
* Access through:
  * AWS Management Console
  * AWS CLI
  * SDK's
  * HTTP Query API's

### AWS Billing 
* AWS Billing and Cost Management - Pay bills, Monitor usage, budget and forecast costs
* AWS Cost and Usage Report Tool - Identify opportunities for optimisations by understanding your cost and usage data trends
* AWS Billing Dashboard - Status of month-to-date AWS expenditure, shows graphs ( Spend Summary, Month-to-Date Spend by Service )
* AWS Bills Page - Up-to-date infomration on your costs and usage, including the detailed breakdown of AWS services
* AWS Cost Explorer - View charts of costs, forecast costs, view metrics
* AWS Cost and Usage Report - Each service category used by an account and its costs. AWS can publish these reports to S3 buckets

### AWS Support
* Provided for:
  * Experimenting with AWS
  * Production Use with AWS
  * Business-critical use of AWS
* Supports:
  * Proactive guidance
  * Best Practices
  * Account Assistance
* Plans:
  * Basic Support
  * Developer Support
  * Business Support
  * Enterprise Support
* Case Severities:
  * Low
  * Normal
  * High
  * Urgent
  * Critical
    
### AWS Trusted Advisor
* Analyses your AWS environment
* Real-time guidance and recommendations to help you provision your resources
* Offered as part of AWS support plan

### AWS Shield
* DDoS Protection Service
* AWS Shield Standard is available to everyone
* AWS Shield Advanced is an optional paid service
* Contacting DDoS Response Team requires Enterprise Support or Business Support from AWS Support

### AWS Chime
* Communications Service
* Meet, chat, place business calls inside/outside of your organisation
* Pay as you go service

## Module 3 - AWS Global Infrastructure Overview 
### AWS Infrastructure
* Region
  * Physical geographical location
  * To achieve fault tolerance, AWS Regions are isolated from each other
  * Resources in one region aren't replicated automatically in another region
  * Contains one or more avalability zones
* Availability Zone
  * Includes multiple data centers
  * Physically separated from other availability zones
  * All availability zones are interconnected with high bandwidth and low latency networking
  * It is advised to replicate data in different availability zones
* Data Centers
  * Foundation of AWS infrastructure
  * Data centers can not be specified
* ODM's
  * Original Device Manufacturers design and manufacturer products based on specifications from a second company
  * Second company then rebrands it
* Points of Presence
  * Located among all major countries in the world
  * Delivers a better near real-time user experience
  * Edge locations are located througout the world
  * Regional edge caches have data that is not frequently accessed enough to remain in an edge location
 

 ## Module 4 - AWS Cloud Security
 ### AWS Shared Responsibility Model
 * Security and Compliance are a shared responbility between AWS and Customers
 * AWS Responsibilities ( Security of the cloud )
   * Physical security of data centers
   * Hardware Infrastructures
   * Software Infrastructures
   * Network Infrastructures
   * Virtual Infrastructures
 * Customer Responsibilities ( Security in the cloud )
   * Selecting and Securing any instance operating systems
   * Securing the applications launched on AWS resources
   * Security Group Configurations
   * Firewall Configurations
   * Network Configurations
   * Account Management

### AWS IAM 
* Define users, groups, roles and types of accesses they are allowed
* Free service
* Handles authorisation and authentication
* Components
  * IAM User - person/application that can authenticate the AWS account. Each user must have an unique name with no white spaces
  * IAM Group - Collection of users and are granted identical authorisation. Efficient mechanism to apply permissions. Can't have nested groups
  * IAM Policy - Document that defines which resource and the level of access. Policies can be attached to users/groups
  * IAM Role - Grant set of permissions for making AWS service requests. Provides temporary access.
* Authentication for IAM Users
  * Users/systems must prove their identity.
  * Types of Access:
    * Programmatic Access - Access Key ID and secret address key, when using API calls through AWS SDK, AWS CLI, or other tools
    * Management Console Access - 12 digit account ID or alias, user name, and password. Then may be prompted for MFA ( Multi-Factor Authentication )
* Authorisation for IAM Users
  * What permissions a user/service/application should be granted. Happens after authentication
  * By default, IAM users have no permissions to access any resource. Need to implicitly permit
  * Policies are documents in JSON, list of permissions that allow or deny access to resources

### IAM Policy
* Types:
  * Identity-Based Policies:
    * Managed Policies: Standalone policies than you can attach to users/groups/roles
    * Inline Policies: Policies embedded into an user group/role
  * Resource-Based Policies:
    * Attached to a resource
    * All of them are inline policies

### Root User
* Have and retain full access to all resources
* Create a user and an admin group with permissions that you require
* Store Root user credentials and use the new user just created instead
* AWS recommends not to use the root user

### Securing AWS Account
* Enable MFA
* Use AWS CloudTrail - logs all the accesses to your AWS resources for 90 days ( can be extended )
* Enable Billing Report 

### Security Features of AWS Organisations
* Groups
* Integration of AWS IAM
* Service Control Policies

### Service Control Policies ( SCP's )
* provides the maximum available control one user could have
* Also JSON documents
* Not a replacement for IAM, since it never grants permissions

### AWS Key Management Service ( KMS )
* Create and manage encryption keys to encrypt data
* Secure and resilient service that users hardware security modules ( HSM's ) approved by Federal Information Processing Standards ( FIPS )
* Integrates with CloudTrail to log all the accesses of the encryption keys
* Customer master keys ( CMK's ) are used to control access to the data encryption keys
* You can create new keys when you want and restrict their access
* Can import keys also

### AWS Incognito 
* Control access to AWS resources from the applications
* User sign-up, sign-up, log-in to your web and mobile applications
* Uses common identity management standards, like Security Assertion Markup Language 2.0 ( SAML )

### Encryption 
* Data at rest:
  * Data that is physically stored in a disk or a tape.
  * Using AWS KMS handles encryption and decryption transparently without modifying our application
* Data in transit:
  * Data that is moving in the internet is secured using Transport Layer Security ( TLS )
  * TLS was formerly called SSL
  * AWS Certificate Manager provisions, manages, deploys, renews SSL or TLS certificates for your AWS Services

### Securing Amazon S3
* By default, all S3 buckets are private and protected and can be accessed by users that are explicitly granted access
* Amazon S3 Block Public Access - Overrides any policy, avoids unintended access
* IAM Policy
* Bucket Policy - Policies applied to specific buckets
* ACL - applied on buckets or objects
* AWS Trusted Advisor - bucket permission check feature to check global checks

### AWS Config
* Assess, audit, evaluate the configurations of AWS resources
* Monitors and records AWS resouces configurations
* Detailed resource configuration histories, and determine overall compliance against internal guidelines
* Compliance auditing, Security Analysis, Change management, Operational Troubleshooting
* Non compliant resources are flagged
* AWS Config is a regional service, need to be enabled in every region manually

### AWS Artifact
* on-demand downloads of AWS Security and Compliance documents
* Can submit to security auditors directly

## Module 5 - Networking and Content Delivery
### OSI Model - Open Systems Interconnection Model
* Application Layer - Layer 7 - HTTP, FTP, DHCP
* Presentation Layer - Layer 6 - ASCI, ICA
* Session Layer - Layer 5 - NetBIOS, RPC
* Transport Layer - Layer 4 - TCP, UDP
* Network Layer - Layer 3 - IP
* Data Link Layer - Layer 2 - MAC
* Physical Layer - Layer 1 - Signal (1's and 0's)

### Amazon VPC
* Logically isolated section of AWS Cloud where we can launch our AWS resources
* Control over virtual networking resources - IP Addresses, subnets, route tables, gateways
* IPv4 and IPv6 can be used
* Multiple layers of security

### VPC
* Dedicated to one AWS account
* Belongs to one AWS Region and can span through multiple availability zones
* Can divide the VPC into several subnets

### Subnets
* Isolated range of VPC's
* Range of IP's addresses that are a subset of VPC IP addresses
* Belong to one availability zone
* Could be private or public

### IP Addressing in VPC
* IPv4 CIDR block is assigned to a VPC, can't be changed later
* Largest block is /28 and the smallest is /16
* Subnets divide the IP address pool and subnets cannot overlap
* For each CIDR block, AWS reserves IP addresses for: 
  * Network Address
  * VPC local router
  * Doman Name System resolution
  * Future use
  * Network brodcasting address
* Every instance gets a private IP address for internal networking
* Public IP Addresses can also be assigned using auto-assign at the subnet level
* Elastic IP Address:
  * static and public IPv4 address
  * Elastic IP address can be associated to an instance or a network interface
  * Can mask the failure of an instance by instantly remapping
  * All the attributes of the network interface can be moved from instance to instance
  * Additional costs are associated with elastic IP address

### Elastic Network Interface
* Can be attached/detached from an instance in VPC
* When the interface is moved, all the attributes and traffic follow the new instance
* Each instance in a VPC has a default primary network interface providing it private IPv4 address
* Primary network interface cannot be removed, but additional network interfaces can be added
* Number of network interfaces depend on the type of instance

### Route Tables
* Contains set of routes to direct traffic
* Each route specifies a destination ( CIDR Block ) and a target ( processing resource )
* By default, every route table has a local route for internal communication
* Local routes can not be deleted, but additional routes can be configured
* Each subnet can have only one route table, but multiple subnets can have the same route table

### Internet Gateway
* Scalable, Redundant, and highly available component that enables communication between instances and public internet
* Purpose:
  * Provide a target for internet traffic
  * Perform network address translation for instances that were assigned public IPv4 Address
* To make a subnet public, we add an internet gateway and add a route to send non-local traffic to the internet gateway

### NAT Gateway
* Enables instances in a private subnet to access the internet but prevents the public internet from initiating connection
* NAT gateway must exist inside a public subnet
* Elastic IP address must be associated to the NAT gateway
* Private subnets route tables should be updated to direct internet access through the NAT gateway
* NAT gateway is recommended over NAT instance, since it's a managed service

### VPC Sharing
* Can share subnets with other AWS accounts in the same organisation
* Advantages:
  * Separation of Duties
  * Ownership
  * Security Groups
  * Efficiencies
  * No Hard Limits
  * Optimised Costs

### VPC Peering
* privately routing traffic between two VPC
* Instances in either VPC can communicate with each other as if they are on the same VPC
* Has few restrictions:
  * IP addresses cannot overlap
  * Transitive Peering is not allowed
  * You can have only one peering resource between the same two VPC's ( can only have one connection )

### AWS Site-to-Site VPN
* enables access to your remote network from the VPC
* setup:
  * Create new virtual gateway device ( VPN Gateway )
  * Define configuration of VPN device or customer gateway
  * Create custom route table
  * Establish an AWS Site-to-Site connection
  * Configure routing

### AWS Direct Connect
* enables a dedicated private connection between the network and one of the DX ( AWS Direct Connect ) locations.
* Can reduce costs, provide a more consistent network connection
* It uses open standard VLAN's
* Direct Connect doesn't use encryption while AWS Site-to-Site VPN does

### VPC Endpoints
* enables you to privately connect to the VPC
* types:
  * Gateway
    * Specify as a target for a route destined to S3 or DynamoDB
  * Interface
    * AWS PrivateLink simplifies security of data shared in cloud-based applications
    * provides private connections between VPC's, AWS Services, and on-premises applications

### AWS Transit Gateway
* Network transit hub to interconnect VPC's instead of complicated peering connections
* Also can be used to connect on-premises network
* Requires only a single connection to the central gateway to VPC, on-premises data center, or remote office

### Security Groups
* Virtual firewall controlling inbound and outbound traffic
* Act at instance level
* By default, all inbound traffic is denied and all outbound traffic is allowed
* Security groups are stateful, state information is kept even after request is processed
* Only allow rules, no deny rules
* All rules are evaluated before the decision to allow traffic

### Network Access Control Lists
* Work at the subnet level
* Can specifiy rules that allow and deny, can specify ports and protocols
* Each subnet is associated with an ACL
* Default ACL's allow all inbound and outbound traffic
* Network ACL's are stateless
* Custom ACL's deny all inbound and outbound traffic unless specified
* All ACL rules are numbered and evaluated in order

### AWS Route 53
* translates an internal name to the corresponding IP address
* Can be used to check the health of your resources
* Features traffic flow
* Enables you to register domain names
* Routing Policies:
  * Simple Routing ( Round Robin ) - Single server environment
  * Weighted Round Robin Routing - Assign weights to resources - Used in A/B testing or blue/green deployment
  * Latency Routing
  * Geolocation Routing - Based on location of users
  * Geoproximity Routing - Based on location of resources
  * Failover Routing - if primary site unreachable, route to backup site
  * Multivalue answer Routing - Respond to DNS queries with up to eight healthy records selected at random

### Content Delivery Network 
* Globally distributed system of caching servers
* Caches copies of commonly requested files
* Delivers a local copy of requested content from a nearby cache edge or point of presence
* Accelerates delivery of dynamic content
* Improves application performance and scaling

### Amazon Cloudfront
* Relies on Route 53 Geolocation routing
* When user requests content, the user is routed to the edge location that provides the lowest latency
* When objects are less popular, they are moved from edge locations to regional edge caches

## Module 6 - Compute
### Compute Services
* EC2 - Virtual Machines
* EC2 Auto Scaling - automatically launch/terminate EC2 instances
* ECR - Store and retrieve docker images
* ECS - Container orchestration service
* VMWare Cloud on AWS - enables you to provision a hybrid cloud without custom hardware
* AWS Elastic Beanstalk - Run and manage web applications
* AWS Lambda - Serverless compute solution
* EKS - Kubernetes on AWS
* Lightsail - Building an application or website
* Batch - Running batch jobs at scale
* Fargate - Run containers without having to manage servers or clusters
* Outposts - run select AWS services in your on-premises data center
* Serverless Application Repository - discover, deploy, publish serverless applications

### Launching EC2
* AMI
  * Amazon Machine Image - template
  * Sources
    * QuickStart - prebuilt AMI - linux and windows
    * My AMI's
    * AWS MarketPlace
    * Community AMI
* Choosing an instance type
  * CPU, RAM, Storage, Networking Bandwidth Requirements
  * Placement groups to influcence the placement of interdependent instances
* Specifiying network settings
  * Region can not be changed once created
  * VPC and subnets can be chosen
  * If no VPC, default VPC is chosen and public IP is assigned
* Attaching an IAM Role
* Attaching User Data Script - Automate installations and configurations - Runs only the first time but can be configured
* Storage
  * AWS EBS - Retains data even after instance is stopped
  * EC2 Instance Store - Lost when instance is stopped
* Adding Tags
* Security Groups
* Identifying or Creating a key pair - Encrypting Login Information

### States of Instances
* Pending
* Running
* Rebooting
* Stopping
* Stopped
* Shutting Down
* Terminated

### Elastic IP Address
* Each instance that recieves a public IP address is also given an external DNS hostname
* For consistent IP address, need to use Elastic IP Address
* By default, 5 Elastic IP addresses per region are given ( Soft Limit )

### Amazon CloudWatch
* Monitor your instances
* Recorded for 15 months
* Basic Monitoring - 5 min periods
* Detailed Monitoring - 1 min periods

### Pricing Models
* On-Demand Instances
  * Pay by the hour
  * AWS Free Tier
  * No long term committments
  * Low cost and flexibility
  * Short term/Spiky Workloads
  * Application development/Testing
* Dedicated Hosts
  * Physical server with EC2 instance capacity fully dedicated to your use
  * Save money on licencing costs
  * Compliance and Regulatory Requirements
  * Bring your own Licence ( BYOL )
* Dedicated Instances
  * Instances that run in a VPC on hardware dedicated to single customer
* Reserved Instances
  * Full, partial or no upfront payments for discounted prices
  * 1-year or 3-year term
* Spot Instances
  * Instances run as long as they are available
  * 2 minute notification before it is interrupted
  * Interruptions can stop/hibernate/terminate
  * Large scale
  * Dynamic workload
  * Flexible start and end times
  * Application only feasible at very low cost
  * Users with urgent computing needs for large amounts of capacity
* Per second Billing
  * On-Demand Instances
  * Reserved Instances
  * Spot Instances

### Cost Optimisation
* Right Size
* Increase Elasticity
* Optimal Pricing Model
* Optimise Storage Choices

### Containers
* Operating System virtualisation
* Smaller than virtual machines
* Benefits
  * Repeatable
  * Self Contained Environment
  * Software runs the same in different enviroments
  * Faster to launch or terminate resources

### Docker
* Packages software into containers
* Containers are created using docker images

### Amazon ECS
* Scalable high-performance container management service, orchestration of docker container
* Using ECS:
  * Create task definition
    * Describes 1-10 docker containers
    * Blueprint of application
  * Task is instantiation of a task definition within a cluster. You can specify the number of tasks in your cluster
  * ECS Task Scheduler will place tasks in cluster
  * The cluster consists of a group of EC2 instances each of which is running a Amazon ECS Container Agent

### Amazon Cluster Options
* Networking only cluster - powered by Fargate - AWS Manages the cluster
* EC2 Linux + Networking Cluster
* EC2 Windows + Networking Cluster

### Kubernetes
* Container Orchestration
* Automates:
  * Container Provisioning
  * Networking
  * Load Distribution
  * Load Distribution
  * Scaling

### Amazon EKS
* Enables you to run Kubernetes on AWS
* Certified Kubernetes Comfortmant
* Supports Linux and Windows Containers
* Manage clusters of Amazon EC2 compute instances
* Run containers that are orchestrated on those instances

### Amazon ECR
* Fully managed docker container registry
* store, manage, deploy docker images

### AWS Lambda
* Lambda function contains the code we want to run
* Triggered either on schedule, or due to event
* Only paid for the compute time consumed
* Benefits:
  * Multiple programming languages
  * Automated Administration
  * Built-in Fault tolerance
  * Orchestration of mulitple functions
  * Pay-per-use pricing
* Event Sources
  * Some services publish events to invoke
  * Lambda can poll resources in other services
  * Some services can directly invoke
* Limits
  * Soft Limits
    * Concurrent executions: 1000
    * Function and Layer Storage: 75 GB
  * Hard Limits
    * Maximum function memory allocation: 10,240 MB
    * Function Timeout: 15 mins
    * Deployment package size: 250 MB
    * Container Image Code Package Size: 10 GB

### AWS Elastic Beanstalk
* Run and develop web applications
* Automatic Scaling
* Complete Resource Control


## Module 7 - Storage
### AWS EBS
* Persistant Block Storage Volume
* Each EBS volume is automatically replicated within it's availability zone
* Low latency since it is directly connected to EC2 instances
* Backed up automatically to Amazon S3 through snapshots
* First snapshot is called a baseline snapshot, and any other snapshot only saves the differences from the baseline
* Uses:
  * Boot Volume and Storage volume
  * Data storage with file system
  * Database hosts
  * Enterprise applications
* Types:
  * SSD - Can be used for Boot volumes
    * Provisioned IOPS - highest performance - large database workloads
    * General Purpose - most workloads
  * HDD - Cannot be used for Boot volumes
    * Throughput-Optimised - require consistent fast throughput - big data
    * Cold - Large volume of data that is not frequently accessed
* Cost Estimation
  * Volumes - Charged by the GB
  * IOPS - I/O is included in General SSD
  * Snapshots - Added cost is GB/month
  * Data Transfer - When you copy EBS snapshots through different regions then charged

### Amazon S3
* Object Level Storage
* Stores data as objects in buckets
* 11 9's of durability
* You can store as many objects in a bucket as you want
* Bucket names are universal and must be unique
* Objects can be up to 5 TB
* Data in S3 is redundantly stored across multiple facilities
* Fine-grained control over who can access
  * IAM policies
  * S3 bucket policites
  * Per-object access control lists
  * Can encrypt data in transit or at rest
* Includes event notifications when objects are uploaded, deleted

### Various Storage Classes 
* Amazon S3 Standard - low latency and high throughput
* Amazon S3 Intelligent Tiering - Automatically move data to the most cost effective access tier
* Amazon S3 Standard Infrequent Access - Data Accessed less frequently, but requires fast data access
* Amazon S3 One Zone Infrequent Access - Data replicated only in one availability zone. Good for secondary backups
* Amazon S3 Glacier - Low cost storage for data archiving
* Amazon S3 Glacier Deep Archive - Long term retention upto years. Accesses are usually only once or twice in a year

### Buckets
* Logical containers for objects
* Can have more than one bucket
* Can restrict who accesses, deletes, adds objects to our buckets
* URL Styles to access buckets:
  * Bucket path-style URL endpoint - When we need to access objects
  * Bucket virtual-style URL endpoint - as a website for static data
* Buckets belong to one region and are replicated in many availability zones
* Can access buckets through:
  * Console
  * AWS CLI
  * AWS SDK
  * REST based endpoints

### EBS Cost Estimation
* Costs vary with regions
* Factors:
  * Types of storage class
  * Amount of Storage
  * Requests - PUT, COPY, POST, LIST, GET
  * Data Transfer - Crossing boundary of Region

### Amazon EFS
* Multiple virtual machines can access at the same time
* Shared Filed system that uses NFS
* File Storage in AWS Cloud
* Big Data Analytics, Media Processing Workflows, Content Management
* Petabyte-scale, Low latency File System
* Shared Storage
* Elastic Capacity
* Each Availability zone has a mount target
* If there are more than one subnet in availability zone, only one mount is created
* Setup:
  * Create EC2 resources and launch your Amazon EC2 instance
  * Create your EFS file system
  * Create mount targets in appropriate subnets
  * Connect EC2 to mount targets
  * Verify resources and protection of your AWS account

### Amazon Glacier
* Secure, durable, extremely-low cost storage for data archiving
* Cannot retrieve data immediately
* Terms:
  * Archive - Any object
  * Vault - Container for storing archives
  * Vault Policy - Vault Access Policy and Vault Lock Policy
* Retrieving Data:
  * Expedited Retrievals - 1-5 mins ( highest cost )
  * Standard Retrievals - 3-5 hours
  * Bulk Retrievals - 5-12 hours ( lowest cost )

### Lifecyle Policies
* Delete or move objects according to their age
* Amazon S3 Standard -> Amazon S3 Standard Infrequent Access -> Amazon S3 Glacier -> Deleted


## Module 8 - Databases
### Amazon RDS
* Cost-efficient and resizable capacity while automating administrative tasks
* AWS manages installing, patching, automatic backups and high availability.
* AWS RDS Instance:
  * Isolated database environment that you can contain multiple user created databases
  * Instance class and Instance storage can be specified
  * Can choose database engine:
    * MySQL
    * Amazon Aurora
    * Microsoft SQL
    * Postgre SQL
    * MariaDB
    * Oracle

### Multi AZ deployment
* Generates a standby copy of database instance in another availability zone within the same VPC
* Every transaction is replicated
* In case of failure, the standby database is brought up as the new main instance
* Since DNS will be used, no changes are required in the application level

### Amazon Read Replicas
* MySQl, MariaDB, Postgre SQL, Amazon Aurora
* Updates made to the database are asynchronously copied to the read replica instance
* Reduce traffic to main instance by redirecting the read queries to the read replica instance
* Promoting to main instance is possible, but requires manual action since asynchronous updates are being made
* Read replicas can be created in different regions, so more fault-tolerant and lower latency

### When to use Amazon RDS
* Complex Transactions
* Medium to high queries or write rate
* No more than single worker node or shard
* High Durability

### When not to use Amazon RDS
* Massive read/write rates
* Sharding due to high data size or throughput demands
* Simple GET and PUT requests that a NoSQL database can handle
* Relational database management system customisation

### Billing Characteristics of RDS
* Clock Hour Billing
* Database Characteristics
* Database purchase type
* Number of database instances
* Provisioned Storage
* Requests

### Amazon DynamoDB
* Fast, flexible, NoSQL database
* Consistent, single digit millisecond latency at any scale
* System automatically adds paritions
* Flexible Schema
* Core components:
  * Table - collection of data
  * Items - Group of attributes
  * Attributes - Fundamental data element
  * Primary Key
    * Partition Key - Simple primary key, composed of one attribute called sort key
    * Partition Key and Sort key are also called as the composite primary key

### Amazon RedShift
* Fully managed data warehouse
* Analyse all data using standard SQL and existing business Intelligence tools
* Complex analytic queries against petabytes of structured data using sophisticated query optimisation, columnar storage on high performance local disks, parallel processing
* Parallel Processing Architecture
  * Cluster of leader and compute nodes
  * Leader node manages communication with client programs and all communication with compute nodes
  * Parses and develops plans for compute nodes
  * Compiles codes for individual elements of the plan
  * Compute nodes run compiled codes and returns back intermediate results
  * All data are aggregated
* Supports Standard SQL
* Also provides Java Database Connectivity ( JBDC ) and Open Database Connectivity ( OBDC ) connectors

### Amazon Aurora
* MySQL and Postgre SQL compatible RD built for cloud
* Reduce costs and are more reliable
* Fully managed service
  * Provisioning
  * Patching
  * Backup
  * Recovery
  * Failure Detection
  * Repair
* Multiple copies of data across Availability Zones with continous backups to S3
* Can use up to 15 read replicas
* Instant Crash Recovery
