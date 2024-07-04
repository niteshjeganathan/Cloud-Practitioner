# Cloud-Practitioner

## Module 1 - Cloud Concepts Overview
### Cloud Service Models
* IaaS - AWS EC2
* PaaS - AWS Elastic Beanstalk
* SaaS - Dropbox

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



