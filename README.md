# az-900
Study material for Az-900

# Cloud Computing
Usage of remote servers hosted on the internet for processing, storage, networking etc. for an application.

## On-premise
1. You are responsible for the services, IT people, real estate, risk etc.

## Cloud solution
1. Servers, IT people, real estate are taken care of by someone else.
2. You are responsible for configuration and code.

## Evolution
Dedicated server > Virtual Private Server > Shared Hosting > Cloud Hosting

## Common cloud services for IaaS
1.Compute
2.Storage
3.Networking
4.Databases

## Benefits
1.Cost-effective - No upfront cost. You pay-as-you-go.
2.Global - Anywhere in the world in the form of regions.
3.Secure - Secure by default, using principle of least privilege.
4.Reliable - back up, disaster recovery, fault tolerant and data replication.
5.Elastic - Auto scale up and scale down as per demand.
6.Current - Software patches.

## Types of cloud computing
1.Saas - Product is run and managed by service provider. Ex: Gmail, Office 365.
2.PaaS - Focus on deployment and management of your application. Ex: Heroku, Elastic Beanstalk, Google App Engine.
3.IaaS - Basic building block of cloud IT. Provides access to N/w, compute and storage.

## Responsibilities
![Image of cloud service responsibilities](cloud-computing-responsibilities.png)

## Azure Deployment Models:
![Image of cloud deployment models](cloud-deployment-configurations.png)

## Total Cost of Ownership ( TCO )
![Image of total cost of ownerships](total-cost-of-ownership.png)

## Capex vs Opex
Spending money ###upfront### on physical infrastructure
1. Server costs, harddrives, Routers, cables, switches.
2. Technical Personal
3. Datacenter costs ( Rent, cooling, phyisical security ).

With cloud, Capex is removed. With Operation Expenses, you can try a product or service without investing in equipment.

## Cloud Architecture Terminologies
Availability zone is the Azure Data Center.

1. Availability - ensure that a service remains available.
![Image of availability](availability.png)
2. Scalable - Grow rapidly
![Image of availability](scaling.png)
3. Elasticity - shrink or grow to meet a demand
![Image of availability](elasticity.png)
4. Fault Tolerant - ability to prevent a failure
![Image of availability](availability.png)
5. Disaster recovery - ability to recover from a failure
![Image of availability](disaster recovery.png)


Concepts:
High Availability: 99.99% ( 4 minutes per month ) Up time.
Scalability: Grow as the web users grow. Ability to add another server easily.
Elasticity: auto shrink and auto grow.
Agility: change rapidly based on changes / environment.
Fault Tolerance: handle faults // multiple copies // replication
Disaster Recovery: recover from a failure - how long and how much data is lost.
Economies of scale: cheaper for cloud to run a server than you do yourself.
CapEx & OpEx: CapEx is upfront cost. OpEx is cost of doing business. OpEx is preferred. CLoud eliminates CapEx and reduces OpEx.
Consumption Based Model: Pay as you go.

Paradigms:
IaaS: VMs, N/W, LB, Firewalls. You are reponsible for middleware, runtime, data, applications.
PaaS: Upload code packages without access to/ knowledge of the hardware. You are responsible for data and applications.
SaaS: Access to configuration only. You only use, no responsibility.

Deployment Models:
Public cloud: This is what you get when you sign up.
Private cloud: only to your company.
Hybrid: Combination.

Open questions: In a private cloud, can I have the infrstructure on premise?.

Core Azure Services:
Regions - Geographically different areas. Around 60. Places where you can get Azure services from. Each region has multiple data centers.
Availability Zone - For maximum availability. This is only available in few regions.
Resource Groups - Grouping of resources in Azure. Each Subscription holds more than on Resource Groups.
Azure Resource Manager (ARM) - Common API which interprets the messages coming from other users/interfaces and passes to VMs etc.

Core Azure Architectural Components:
	Compute
		Execute code in cloud
			VMs 
				A slice of a physical machine.
				A model of IaaS.
				VM scale set
				No limit on horizontal scale.
				Limit on vertical scale.
			App Services
				Code and configuration given to Azure and they will run it.
				Promise of performance, but no access to hardware.
				A model of PaaS.
			Functions
				Serverless
			Containers
				Container, images, and is faster way to deploy.
				Azure Container Instance - single instance, quickest way to deploy a container.
				Azure Kubernetes Service - runs on a cluster of server.			
	Networking
		Connectivity services
			Virtual Network - basic unit. Divided into Subnets. Software configuration.
			ExpressRoute - high speed private connection to Azure.
		Protection services
			DDos Protection
				Basic is free. Standard comes with a fee.
			Azure firewall
			Network Security Groups - free / traffice denied if the ACL is matched. 
			Private Links
		Delivery services
			Load Balancer
			CDN
			Application Gateway
			Azure Front Door Service
		Monitoring services
			Network Watcher
			ExressRoute Monitoring
			Azure Monitor
				Collects all the logs from various resources into a central dashboard
	Storage
		Unmanaged Storage
			General Purpose V2
				Blobs, Tables, Queues, Files 5PB
			Azure Data Lake Storage
				Big Data
			Other options
				Access tiers - Hot, cool, archive
				Performance - standard vs premium
				Location
				Redundancy / Replication - locally, globally redundancy
				Failover options
		Managed Storage
			Azure Virtual Machine Disks
			Managed Disks
			Reserve capacity in advance
			Optimized to virtual hard disks
		Backup, Replication and Recovery Storage
			Azure Site Recovery
			Backup storage
			Recovery Services Vault
			Retention policy
	Databases
		Cosmos DB ( NoSQL )
			Video games, social networks
			Multi-modal ( different types of data )
		Azure SQL Databases ( RDBMS )
			Easy to replicate, scale, migrate from SQL server on prem.
			DB as a service, runs on SQL server underneath.
		Azure DB for MYSQL
			Managed MySQL DB
			Migration is easier
		Azure DB for PostgreSQL
			Scaling for larger number of users is easier.
		Azure DB Migration Services
			Data from different sources like Oracle, SQL Server, AWS, MongoDB, Google Cloud can be migrated to one of the databases using this tool.
		Azure Synapse Analytics ( SQL DW )
			SQL Data Warehouse changed to Synapse Analytics, used for Big Data.
			This is an analytical database, not a transactional database.
	Core Azure Solutions
		IoT
			IoT Hub - to ingest data to Cloud
			IoT Central
		Big Data and Analytics
			Azyre Synapse Analytics
			HD Insight - Big Data Apache Hadoop tools
			Azure Databrics - centralized data to pull and manipulate data and generate reports to the business.
		AI
			Azure Machine Learning Services	
				Vision, Speech etc
		Serverless
			Azure Functions
			Logic Apps
			Event grid
	Azure Management Tools
		Azure CLI - Linux style
		PowerShell - Windows style
		Azure Portal
		Azure Cloud Shell - PowerShell interface or Batch file interface.
	Azure Advisor
		Cost recommendations based on usage
	
		
	Security:
		Firewalls
			Xss, SQL Injections are rejected by the firewall.
		Azure DDoS Security
		Network Security Group
			Prevent inbound traffic based on certain rules or outbound traffic basedon certain rules
			Traffic to a subnet has to pass through an NSG
			Determine what all security rules that are to be followed for an ip + port.
			Application Security Group - allow us to define fine-grained network security policies based on workloads, centralized on applications, instead of explicit IP addresses.
		User Defined Route
			Force traffic over a route - either in bound or out bound or both.
		Summary
			All VN subnets should have a NSG.
			DDoS - as needed should be used.
			Layered security
				Data - VN Endpoint
				Application - API Management
				Compute - Limit RDP Access, Windows update
				Network - NSG, usage of subnets, deny by default
				Perimeter - DDoS, firewalls
				Identifiy & Access - MFA, Azure ADPhyicai - Door locks and key cards
		Azure Identifity Sevices
			Authentication and Authorization
			Azure Active Directory
				Identity as a service (IDaaS)
				Grouping, roles
				Single sign-on
			Azure Multi-factor identification
				USer Id, Password and Phone.
		Seucrity tools and features
			Azure AD
			Multi Factor Authentication MFA
			RBAC - Role Based Access Control
			Azure Security Center
				Dashboard that analyzed and gives recommendations
			Azure Key Vault
				SSL certificate
				API keys
				Public and private keys
					Expiration date
					Value
					Cipher algorithm
			Azure Information Protection
				Apply labels to emails and documents
					Confidential, super confidental and top secret
			Advanced Threat Protections
				Outside office hours, present MFA.
				On Saturday, someone from Ukraine tried loggin in. Force password reset.
		Azure Policy
			Implements standards for all of Organization
				10/15 VMs are compliant others are not etc.
			Policy Initiatives
				Multiple policies grouped together.
			Roles
				To be given judiciously.
				READER - Cannot create resources.
				Owner - Owner can assign someone else as a Contributor.
				Contributor.
			Locks
				READ Only Lock
				Cannot delete lock
				Giving people perission to do something or prevent something
			Azure recommendations in Azure Security Tab
			Azure Blueprints
				Roles and policies pre-defined
		Help + Support > Azure Monitor
			Log files or Metrics ( CPU Utilization )
			Centralized collector of all logs and can send SMS, Email etc.
			Specific to you.
		Azure Service Health
			Any downtimes etc.
			For everyone - general downtimes.
		Azure Compliance
			GDPR, ISO, 9001:2015 - QMS ( Bug tracking ), ISO/IEC 20000-1:2011 is for Service Management etc.
			Compliance Manager
			Geography Specific services
				Azure Government Services
					DoD, US Specific Geometry
					Isolated data centers
				Azure Germany Account
					Data remains in Germany
					Strictest EU data protection
					German Data Trustee
				Azure China
					Seperate Account
					Data remains in China
				
		Pricing and Support
			Azure Subscriptions
				Fundamental subscription unit - HR, Finance, etc
				Billed to that specific subscription
				Used to organize resources
				Management Groups - Hierarchy
			Purchase
				Pay as you go
				Enterprise Agreement
				MS Cloud Solution Provider - HP
				Azure Free Account
				12 months of free services
				Always free
			Factors affecting bill
				Different resources as billed different
			Azure Functions	
				1 million executions free per month
				Cheaest VM is 20$ per month
		Pricing calculator
			Similar to shopping cart
			Region, Tier, Subscription type, Support Options
		Total Cost of Ownership
			Cost of the service is more than just hardware price
			Electricity, Cooling, Internet Connectivity, Rack space, labor and back up.
		Best Practices:
			Azure Advisor Cost Tab
			Auto shutdown dev/qa resources
			Utilize cool/archive storage where possible
			Reserved instances
			Alerts when billing exeeds an expected level
			Restrict access to certain expensive resources
			Auto scaling resources
			Each resource has to be tagged
			Azure Cost Management
		
		Service Level Agreement
			Financial guarantee is MS does not honor it.
			Composite SLAs
			Public and Private previews => General Availabiliy
			
			
		Updated content
		Cloud Concepts
			Cost Savings
				TCO
				Economies of scale
				Autoscaling
			Global Reach
			Shared Responsibility Model
			Serverless
				You just dont have to deal with the server anymore.
				Even less access to the server than PaaS.
				Compute - Azure Functions
				Compute - Serverless Kubernetes
				Database - Azure SQL database
				Database - Cosmos DB Serverless
		Core Azure Services
			Region Pair: Each region has another region called as pair.
			Data connection b/w them have the highest speed etc.
			Almost always in the same geography.
			Resources are instances of services - Networks, Subnets, VMs, Databases etc.
		SQL Managed Instance
		
		
		Planning and managing costs
			Spot Pricing / Spot VM: Ability to use VM when nobody is using it at a discout price. Last minute travel website.
			
		
		General and Network security features
			Azure Security Centre - Dashboard for security.
			Azure Sentinel - Centralizes all the log files and analyzes to detect threats.
			Azure Dedicated Hosts - Hardware that is dedicated to you and you only.
			NW Security
				
			
		Core Solutions
			Azure Sphere
				A secure chip, with Spehere OS, designed to work with connected devices.
			Azure Bot Services
			Azure DevOps
			Azure Mobile App
				Monitor the working and services of Azure resources.
			Azure ARM Templates
		

		Identity, Governance, Privacy, Compliance Features
			Conditional Access - Admin logging in via a different country.
			Azure AD works with Organizational Admin
			Resource Tags: Helps in keeping an eye on the resources
			Governance:
				Cloud adoption framework
			Privacy and Compliance
				Data encrypted at rest
				Data encrypted at motion.
			MS will never look at your data.
			50 international data protection standards.
			Protecting IP
			Online Servie Terms
			Data Protection Addendum
			
Questions:
ARM Templates vs Virtual Machine Scale Sets
	ARM Templates are used to deploy the Azure resources. These templates could be reused & automated.
The Azure Advisor tool can be used to provide recommendations for your Azure environment from different fronts such as Security and Cost.
Azure Application Insights can be used to monitor web applications on different platforms. This tool can also be used to diagnose issues that can occur within your web-based applications.
Azure Monitor - performance and availability of your applications
Azure Log Analytics - for analyzing the event.
Azure Traffic Manager is a DNS-based traffic load balancer that enables you to distribute traffic optimally to services across global Azure regions, while providing high availability and responsiveness.
Subscriptions cannot be merged.
Azure AD Free edition has an object limit of 5,00,000.
Azure site recovery provides Disaste Recovery.
Support plans
	Only standard offers 24 x 7 email and phone support.
				
