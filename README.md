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
* AWS Shield Advanced is available to everyone
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



