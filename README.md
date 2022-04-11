

- [AzureFundamentals Introduction](#azurefundamentals-introduction)
  - [What is Azure?](#what-is-azure)
    - [Azure Portal](#azure-portal)
    - [Azure Marketplace](#azure-marketplace)
    - [Azure Services](#azure-services)
- [Azure Fundemental Concepts](#azure-fundemental-concepts)
  - [Public cloud, Private cloud and Hybrid cloud](#public-cloud-private-cloud-and-hybrid-cloud)
  - [Advantages of Cloud computing](#advantages-of-cloud-computing)
  - [Cloud Service Models](#cloud-service-models)
- [Azure Architectural Components](#azure-architectural-components)
  - [Hierarchy](#hierarchy)
  - [Azure Components](#azure-components)
    - [Resources](#resources)
    - [Resource groups](#resource-groups)
    - [Subscriptions](#subscriptions)
    - [Management groups](#management-groups)
    - [Regions](#regions)
    - [Region pair](#region-pair)
    - [Availability zones](#availability-zones)
- [Azure Services](#azure-services-1)
  - [Azure Compute Services](#azure-compute-services)
    - [Virtual machine scale sets](#virtual-machine-scale-sets)
    - [Azure Batch](#azure-batch)
    - [Azure App Service](#azure-app-service)
    - [Container and Kubernetes](#container-and-kubernetes)
    - [Azure Functions](#azure-functions)
      - [Serverless computing](#serverless-computing)
      - [Azure Functions](#azure-functions-1)
      - [Azure Logic Apps](#azure-logic-apps)
      - [Functions VS Logic Apps](#functions-vs-logic-apps)
    - [Azure Virtual Desktop](#azure-virtual-desktop)
- [Azure Networking Services](#azure-networking-services)
    - [What is Azure vitual networking](#what-is-azure-vitual-networking)
    - [Creating a virtual network](#creating-a-virtual-network)
    - [Azure VPN Gateways](#azure-vpn-gateways)
      - [VPNs](#vpns)
      - [Policy-based VPN](#policy-based-vpn)
      - [Route-based VPN](#route-based-vpn)
      - [Required resources for deploying a VPN gateway](#required-resources-for-deploying-a-vpn-gateway)
    - [Azure ExpressRoute](#azure-expressroute)
- [Azure Storage services](#azure-storage-services)
  - [Disk storage fundamentals](#disk-storage-fundamentals)
  - [Azure Blob storage fundamentals](#azure-blob-storage-fundamentals)
  - [Azure Files fundamentals](#azure-files-fundamentals)
  - [Understand Blob access tiers](#understand-blob-access-tiers)
- [Azure database and analytics services](#azure-database-and-analytics-services)
  - [Azure Cosmos DB](#azure-cosmos-db)
  - [Azure SQL Database](#azure-sql-database)
  - [Exercise](#exercise)
  - [Azure databse for MySQL](#azure-databse-for-mysql)
  - [Azure Databse for PostgreSQL](#azure-databse-for-postgresql)
    - [Single Server](#single-server)
    - [Hyperscale](#hyperscale)
  - [Azure SQL Managed Instance](#azure-sql-managed-instance)
  - [Big data and analytics](#big-data-and-analytics)
    - [Azure Synapse Analytics](#azure-synapse-analytics)
    - [Azure HDInsight](#azure-hdinsight)
    - [Azure Databricks](#azure-databricks)
    - [Azure Data Lake Analytics](#azure-data-lake-analytics)
- [Choose the best Azure IoT service for your application](#choose-the-best-azure-iot-service-for-your-application)
  - [Azure IoT Hub](#azure-iot-hub)
  - [Azure IoT Central](#azure-iot-central)
  - [Azure Sphere](#azure-sphere)
- [Choose the best AI service for your needs](#choose-the-best-ai-service-for-your-needs)

---

# AzureFundamentals Introduction


## What is Azure?

- Azure is Microsoft's Cloud Computing platform
- Provides over 100 services



### Azure Portal

The Azure portal is a web-based, unified console that provides an alternative to command-line tools


Alows you to:

- Build, manage, and monitor everything from simple web apps to complex cloud deployments
- Create custom dashboards for an organized view of resources
- Configure accessibility options for an optimal experience



### Azure Marketplace

Connects users with Microsoft partners, independent software vendors, and startups that are offering their solutions and services

Includes categories such as open-source container platforms, virtual machine images, databases, application build and deployment software, developer tools, threat detection, and blockchain



### Azure Services

![image](images/azure-services.png)
Most commonly used catagoies of services:

- Compute
- Networking
- Storage
- Mobile
- Databases
- Web
- Internet of Things (IoT)
- Big data
- AI
- DevOps

More detail on exact Azure services: https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/tour-of-azure-services

---
<br>

# Azure Fundemental Concepts

## Public cloud, Private cloud and Hybrid cloud

There are three deployment models for cloud computing:

Public cloud:
    
    Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources, such as servers and storage, are owned and operated by a third-party cloud service provider, and delivered over the internet.

    - No capital expenditures to scale up.
    - Applications can be quickly provisioned and deprovisioned.
    - Organizations pay only for what they use.
    
<br>

Private cloud:

    A private cloud consists of computing resources used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site (on-premises) datacenter, or it can be hosted by a third-party service provider.

    - Hardware must be purchased for start-up and maintenance.
    - Organizations have complete control over resources and security.
    - Organizations are responsible for hardware maintenance and updates.

<br>

Hybrid cloud:

    A hybrid cloud is a computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them.

    - Provides the most flexibility.
    - Organizations determine where to run their applications.
    - Organizations control security, compliance, or legal requirements.


## Advantages of Cloud computing

- High availability: Depending on the service-level agreement (SLA) that you choose, your cloud-based apps can provide a continuous user experience with no apparent downtime, even when things go wrong.

- Scalability: Apps in the cloud can scale vertically and horizontally:
  - Scale vertically to increase compute capacity by adding RAM or CPUs to a virtual machine.
  - Scaling horizontally increases compute capacity by adding instances of resources, such as adding VMs to the configuration.
  
- Elasticity: You can configure cloud-based apps to take advantage of autoscaling, so your apps always have the resources they need.

- Agility: Deploy and configure cloud-based resources quickly as your app requirements change.

- Geo-distribution: You can deploy apps and data to regional datacenters around the globe, thereby ensuring that your customers always have the best performance in their region.

- Disaster recovery: By taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your apps with the confidence that comes from knowing that your data is safe in the event of disaster.


## Cloud Service Models

IaaS:

    Infrastructure as a Service

    - This cloud service model is the closest to managing physical servers
    - A cloud provider will keep the hardware up-to-date, but operating system maintenance and network configuration is up to you


PaaS:

    Platform as a Service

    - This cloud service model is a managed hosting environment
    - The cloud provider manages the virtual machines and networking resources 
    - The cloud tenant deploys their applications into the managed hosting environment


SaaS:

    Software as a Service

    - The cloud provider manages all aspects of the application environment, such as virtual machines, networking resources, data storage, and applications
    - The cloud tenant provides their data to the application managed by the cloud provider

![image](images/iaas-paas-saas.png)
![image](images/cloud-service-responsibility.png)


---
<br>

# Azure Architectural Components

## Hierarchy

![image](images/azure-hierarchy.png)




## Azure Components

### Resources

- Resources are instances of services that you create, like virtual machines, storage, or SQL databases.

### Resource groups

- Resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.

### Subscriptions

- A subscription groups together user accounts and the resources that have been created by those user accounts. For each subscription, there are limits or quotas on the amount of resources that you can create and use. Organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects.

### Management groups

- These groups help you manage access, policy, and compliance for multiple subscriptions. All subscriptions in a management group automatically inherit the conditions applied to the management group.

### Regions

- A region is a geographical area on the planet that contains at least one but potentially multiple datacenters that are nearby and networked together with a low-latency network

### Region pair

- Regions in the same geography and al least 300 miles away from each other are paired together
- Resources are replicated accross the paired regions to help reduce the likelihood of interruptions because of events such as natural disasters, civil unrest or power outages

### Availability zones

- Availability zones are physically separate datacenters within an Azure region
- An availability zone is set up to be an isolation boundary, so If one zone goes down, the other continues working


---

# Azure Services

## Azure Compute Services

- Virtual machines
  - Software emulations of physical computers
  - Works just like a regular computer
- Virtual machine scale sets
  - Used to deply and manage a set of identical VMs
  - Designed to suppot true autoscale
  - No VM provisioning required
- Containers and Kubernetes
  - Used to deploy and manage containers
- App Service
  - Is a platform as a service (PaaS) offering
  - Quickly build, deploy and scale apps
- Functions
  - They are ideal when you're concerned only about the code running your service and not the underlying platform or infrastructure
  - Used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less

### Virtual machine scale sets

- Virtual machine scale sets allow you to create and manage a group of identical, load-balanced VMs
- If you duplicated the VM, you'd normally need to configure an additional service to route requests between multiple instances of the website. Virtual machine scale sets could do that work for you
- The number of VM instances can automatically increase or decrease in response to demand or a defined schedule

### Azure Batch

- Batch enables large-scale parallel and high-performance computing batch jobs with the ability to scale to tnes, hundreds or thousands of VMs
- When you run a job, Batch:
  - Starts a pool of compute VMs for you
  - Installs applications and staging data
  - Runs jobs with as many tasks as you have
  - Identifies failures
  - Requeues work
  - Scales down the pool as work completes
- Can provide supercomputer level compute power

### Azure App Service

- Allows you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs without managing infrastructure
- Offers automatic scaling and high availability
- Enables automated deployments from GitHub, Azure DevOps or any Git repo to support a continuous deployment model
- More information on apps with App Service: https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-app-services


### Container and Kubernetes

Containers

- Light weight virtualisation environment
- Managed through a container orchestrator

<br>
Azure Container Instances

- Fast and simple way to run a container without having to manage any virtual machines
- It is a PaaS offering

<br>
Azure Kubernetes Service

- Used to automate, manage and interact with a large number of containers
- It is a complete orchestration service for containers

### Azure Functions

#### Serverless computing

The abstraction of servers, infrastructure and operating systems. Azure manages allocation and deallocation of resources

- Abstraction of servers: Serverless computing abstracts the servers you run on. You never explicitly reserve server instances. The platform manages that for you. Each function execution can run on a different compute instance. This execution context is transparent to the code. With serverless architecture, you deploy your code, which then runs with high availability.

- Event-driven scale: Serverless computing is an excellent fit for workloads that respond to incoming events. Events include triggers by:
  - Timers, for example, if a function needs to run every day at 10:00 AM UTC
  - HTTP, for example, API and webhook scenarios
  - Queues, for example, with order processing

Azure has two implementations of serverless compute:

- Azure Functions: Functions can execute code in almost any modern language.
- Azure Logic Apps: Logic apps are designed in a web-based designer and can execute logic triggered by Azure services without writing any code.

#### Azure Functions

- Functions allow you to trigger logic based on an event


#### Azure Logic Apps

- Logic apps also allow you to trigger logic based on an event
- Logic apps execute workflows built from predefined logic blocks

#### Functions VS Logic Apps
![image](images/functionsVSlogicapps.jpg)


### Azure Virtual Desktop

- A desktop and application virtualisation service that runs on the cloud

---

# Azure Networking Services

### What is Azure vitual networking

- Enables resources (VMs, web apps, databases) to communicate with each other, users on the internet, and with on-premises client computers

Azure virtual networks provide the following key networking capabilities:

- Isolation and segmentation
  - Azure virtual network allows you to create multiple isolated virtual netwoks
- Internet communications
- Communicate between Azure resources
  - Virtual networks
    - They connect to VMs and other Azure resouces such as App Service, Kubernetes Service and virtual machine scale sets
  - Service endpoints
    - Used to connect to other Azure resouce types like Azure SQL databases and storage accounts
- Communicate with on-premises resources
  - Point-to-site VPN: From a computer outside your organisation to your corporate network
  - Site-to-site VPN: Links on-premises VPN to Azure VPN gateway
  - Azure ExpressRoute
- Route network traffic
  - Route tables
  - Border Gateway Protocol (BGP)
- Filter network traffic
  - Network security groups
  - Network virtual appliances
- Connect virtual networks
  - User-defined routes (UDR)

### Creating a virtual network

https://docs.microsoft.com/en-gb/learn/modules/azure-networking-fundamentals/azure-virtual-network-settings

### Azure VPN Gateways

More information on VPN gateways https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/azure-vpn-gateway-fundamentals

#### VPNs

- VPNs use an encrypted tunnel within another network
- They're typically deployed to connect two or more trusted private networks to one another over an untrusted network (typically the public internet)
- Traffic is encrypted while traveling over the untrusted network to prevent eavesdropping or other attacks

#### Policy-based VPN

- Used in specific cases that require them, such as for compatability with legacy on-premises VPN devices
- Policy-based VPN gateways specify statically the IP address of packets that should be encrypted through each tunnel. This type of device evaluates every data packet against those sets of IP addresses to choose the tunnel where that packet is going to be sent through

#### Route-based VPN

- With route-based gateways, IPSec tunnels are modeled as a network interface or virtual tunnel interface. IP routing (either static routes or dynamic routing protocols) decides which one of these tunnel interfaces to use when sending each packet. Route-based VPNs are the preferred connection method for on-premises devices. They're more resilient to topology changes such as the creation of new subnets

  Use a route-based VPN gateway if you need any of the following types of connectivity:
  - Connections between virtual networks
  - Point-to-site connections
  - Multisite connections
  - Coexistence with an Azure ExpressRoute gateway

#### Required resources for deploying a VPN gateway

- Virtual network
- Gateway Subnet
- Public IP address
- Local network gateway
- Vitual network gateway
- Connection

### Azure ExpressRoute

Lets you extend your on-premises networks into the Microsoft cloud over a private connection

More on ExpressRoute https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/express-route-fundamentals

---

# Azure Storage services

## Disk storage fundamentals

- Provides disks for Azure virtual machines
- Disks come in many different sizes and performance levels, from solid-state drives (SSDs) to traditional spinning hard disk drives (HDDs), with varying performance tiers

## Azure Blob storage fundamentals

- An object storage solution for the cloud
- It can store massive amounts of data, such as text or binary data
- Is unstructured, meaning that there are no restrictions on the kinds of data it can hold
- It can manage thousands of simultaneous uploads, massive amounts of video data, constantly growing log files, and can be reached from anywhere with an internet connection

<br>

- One advantage of blob storage over disk storage is that it does not require developers to think about or manage disks; data is uploaded as blobs, and Azure takes care of the physical storage needs

Blob storage is ideal for:

- Serving images or documents directly to a browser
- Storing files for distributed access
- Streaming video and audio
- Storing data for backup and restore, disaster recovery, and archiving
- Storing data for analysis by an on-premises or Azure-hosted service
- Storing up to 8 TB of data for virtual machines

You store blobs in containers, which helps you organize your blobs depending on your business needs

## Azure Files fundamentals

- Offers fully managed file shares in the cloud that are accessible via the industry standard Server Message Block (SMB) and Network File System (preview) protocols
- Azure file shares can be mounted concurrently by cloud or on-premises deployments of Windows, Linux, and macOS
- Applications running in Azure virtual machines or cloud services can mount a file storage share to access file data, just as a desktop application would mount a typical SMB share
- Any number of Azure virtual machines or roles can mount and access the file storage share simultaneously
- Typical usage scenarios would be to share files anywhere in the world, diagnostic data, or application data sharing

Use Azure Files for the following situations:

- Many on-premises applications use file shares. Azure Files makes it easier to migrate those applications that share data to Azure. If you mount the Azure file share to the same drive letter that the on-premises application uses, the part of your application that accesses the file share should work with minimal changes, if any.
- Store configuration files on a file share and access them from multiple VMs. Tools and utilities used by multiple developers in a group can be stored on a file share, ensuring that everybody can find them, and that they use the same version.
- Write data to a file share, and process or analyze the data later. For example, you might want to do this with diagnostic logs, metrics, and crash dumps.

## Understand Blob access tiers

Azure Storage offers different access tiers for your blob storage, helping you store object data in the most cost-effective manner. The available access tiers include:

- Hot access tier: Optimized for storing data that is accessed frequently (for example, images for your website)
- Cool access tier: Optimized for data that is infrequently accessed and stored for at least 30 days (for example, invoices for your customers)
- Archive access tier: Appropriate for data that is rarely accessed and stored for at least 180 days, with flexible latency requirements (for example, long-term backups)

The following considerations apply to the different access tiers:

- Only the hot and cool access tiers can be set at the account level. The archive access tier isn't available at the account level.
- Hot, cool, and archive tiers can be set at the blob level, during upload or after upload.
- Data in the cool access tier can tolerate slightly lower availability, but still requires high durability, retrieval latency, and throughput characteristics similar to hot data. For cool data, a slightly lower availability service-level agreement (SLA) and higher access costs compared to hot data are acceptable trade-offs for lower storage costs.
- Archive storage stores data offline and offers the lowest storage costs, but also the highest costs to rehydrate and access data.

---

# Azure database and analytics services

## Azure Cosmos DB

- A globally distributed, multi-model database service
- You can elastically and independently scale throughput and storage across any number of Azure regions worldwide
- You can take advantage of fast, single-digit-millisecond data access by using any one of several popular APIs
- Azure Cosmos DB provides comprehensive service level agreements for throughput, latency, availability, and consistency guarantees
- Azure Cosmos DB supports schema-less data, which lets you build highly responsive and "Always On" applications to support constantly changing data

Azure Cosmos DB is flexible. At the lowest level, Azure Cosmos DB stores data in atom-record-sequence (ARS) format. The data is then abstracted and projected as an API, which you specify when you're creating your database. Your choices include SQL, MongoDB, Cassandra, Tables, and Gremlin. This level of flexibility means that as you migrate your company's databases to Azure Cosmos DB, your developers can stick with the API that they're the most comfortable with.

## Azure SQL Database

- Azure SQL Database is a relational database based on the latest stable version of the Microsoft SQL Server database engine
- SQL Database is a high-performance, reliable, fully managed, and secure database

<br>
Features

- Azure SQL Database is a platform as a service (PaaS) database engine. It handles most of the database management functions, such as upgrading, patching, backups, and monitoring, without user involvement
- SQL Database provides 99.99 percent availability

Migration

- You can migrate your existing SQL Server databases with minimal downtime by using the Azure Database Migration Service
- The Microsoft Data Migration Assistant can generate assessment reports that provide recommendations to help guide you through required changes prior to performing a migration

## Exercise

https://docs.microsoft.com/en-gb/learn/modules/azure-database-fundamentals/exercise-create-sql-database

## Azure databse for MySQL

- Azure Database for MySQL is a relational database service in the cloud, and it's based on the MySQL Community Edition database engine, versions 5.6, 5.7, and 8.0
- With it, you have a 99.99 percent availability service level agreement from Azure
- With every Azure Database for MySQL server, you take advantage of built-in security, fault tolerance, and data protection that you would otherwise have to buy or design, build, and manage
- You can migrate your existing MySQL databases with minimal downtime by using the Azure Database Migration Service

Azure Database for MySQL delivers:

- Built-in high availability with no additional cost
- Predictable performance and inclusive, pay-as-you-go pricing
- Scale as needed, within seconds
- Ability to protect sensitive data at-rest and in-motion
- Automatic backups
- Enterprise-grade security and compliance

## Azure Databse for PostgreSQL

- Azure Database for PostgreSQL is a relational database service in the cloud
- The server software is based on the community version of the open-source PostgreSQL database engine

Azure Database for PostgreSQL delivers the following benefits:

- Built-in high availability compared to on-premises resources. There's no additional configuration, replication, or cost required to make sure your applications are always available.
- Simple and flexible pricing. You have predictable performance based on a selected pricing tier choice that includes software patching, automatic backups, monitoring, and security.
- Scale up or down as needed, within seconds. You can scale compute or storage independently as needed, to make sure you adapt your service to match usage.
- Adjustable automatic backups and point-in-time-restore for up to 35 days.
- Enterprise-grade security and compliance to protect sensitive data at-rest and in-motion. This security covers data encryption on disk and SSL encryption between client and server communication.

Azure Database for PostgreSQL is available in two deployment options: Single Server and Hyperscale (Citus)

### Single Server

The Single Server deployment option delivers:

- Built-in high availability with no additional cost (99.99 percent SLA).
- Predictable performance and inclusive, pay-as-you-go pricing.
- Vertical scale as needed, within seconds.
- Monitoring and alerting to assess your server.
- Enterprise-grade security and compliance.
- Ability to protect sensitive data at-rest and in-motion.
- Automatic backups and point-in-time-restore for up to 35 days.

### Hyperscale

- Horizontally scales queries across multiple machines by using sharding
- Its query engine parallelizes incoming SQL queries across these servers for faster responses on large datasets

## Azure SQL Managed Instance

- Azure SQL Managed Instance is a scalable cloud data service that provides the broadest SQL Server database engine compatibility with all the benefits of a fully managed platform as a service

Features

- Azure SQL Managed Instance is a platform as a service (PaaS) database engine
- Quick provisioning and service scaling
- Automated patching and version upgrades
- 99.99% uptime service level agreement

Azure SQL Managed Instance makes it easy to migrate your on-premises data on SQL Server to the cloud using the Azure Database Migration Service (DMS) or native backup and restore

## Big data and analytics

### Azure Synapse Analytics

Azure Synapse Analytics (formerly Azure SQL Data Warehouse) is a limitless analytics service that brings together enterprise data warehousing and big data analytics. You can query data on your terms by using either serverless or provisioned resources at scale. You have a unified experience to ingest, prepare, manage, and serve data for immediate business intelligence and machine learning needs.

### Azure HDInsight

Azure HDInsight is a fully managed, open-source analytics service for enterprises. It's a cloud service that makes it easier, faster, and more cost-effective to process massive amounts of data. You can run popular open-source frameworks and create cluster types such as Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services. HDInsight also supports a broad range of scenarios such as extraction, transformation, and loading (ETL), data warehousing, machine learning, and IoT.

### Azure Databricks

Azure Databricks helps you unlock insights from all your data and build artificial intelligence solutions. You can set up your Apache Spark environment in minutes, and then autoscale and collaborate on shared projects in an interactive workspace. Azure Databricks supports Python, Scala, R, Java, and SQL, as well as data science frameworks and libraries including TensorFlow, PyTorch, and scikit-learn.

### Azure Data Lake Analytics

Azure Data Lake Analytics is an on-demand analytics job service that simplifies big data. Instead of deploying, configuring, and tuning hardware, you write queries to transform your data and extract valuable insights. The analytics service can handle jobs of any scale instantly by setting the dial for how much power you need. You only pay for your job when it's running, making it more cost-effective.

---

# Choose the best Azure IoT service for your application

IoT enables devices to gather and then relay information for data analysis

Common IoT sensors:

- Environmental sensors that capture temperature and humidity levels
- Barcode, QR code, or optical character recognition (OCR) scanners
- Geo-location and proximity sensors
- Light, color, and infrared sensors
- Sound and ultrasonic sensors
- Motion and touch sensors
- Accelerometer and tilt sensors
- Smoke, gas, and alcohol sensors
- Error sensors to detect when there's a problem with the device
- Mechanical sensors that detect anomalies or deformations
- Flow, level, and pressure sensors for measuring gasses and liquids

By using Azure IoT services, devices that are equipped with these kinds of sensors and that can connect to the internet could send their sensor readings to a specific endpoint in Azure via a message. The message's data is then collected and aggregated, and it can be converted into reports and alerts.

The data that's collected from these devices could be combined with Azure AI services to help you predict:

- When machines need proactive maintenance.
- When inventories will need to be replenished and new product ordered from vendors.

## Azure IoT Hub

- A managed service that's hosted in the cloud and that acts as a central message hub for bi-directional communication between your IoT application and the devices it manages
- It also supports multiple messaging patterns, such as device-to-cloud telemetry, file upload from devices, and request-reply methods to control your devices from the cloud
- After an IoT hub receives messages from a device, it can route that message to other Azure services

## Azure IoT Central

- IoT Central builds on top of IoT Hub by adding a dashboard that allows you to connect, monitor, and manage your IoT devices
- You can watch the overall performance across all devices in aggregate
- You can set up alerts that send notifications when a specific device needs maintenance
- You can push firmware updates to a device
- You can use the UI to control your devices remotely and modify properties of a device

## Azure Sphere

Azure Sphere creates an end-to-end, highly secure IoT solution for customers that encompasses everything from the hardware and operating system on the device to the secure method of sending messages from the device to the message hub. Azure Sphere has built-in communication and security features for internet-connected devices.

- Azure Sphere micro-controller unit
- Custom Linux OS
- Azure Sphere Security Service (AS3)
  - Its job is to make sure that the device has not been maliciously compromised

---

# Choose the best AI service for your needs

