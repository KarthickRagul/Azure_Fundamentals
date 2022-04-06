# Azure_Fundamentals
Key notes for Azure Fundamentals

What is Cloud computing :
   * Delivery of computing services such as servers, storage, database, networking, software, analytics, inteligence and etc. through internet
   * As Pay As You Go Pricing
Advantages :
    * Less Management
    * Less Investments
    * Less Operations
    * Focus on business

Services provided by Azure :![image](https://user-images.githubusercontent.com/62194896/150908995-74e7ade8-af19-42d3-b802-e857a58515c4.png)


**Compute**
Compute services are often one of the primary reasons why companies move to the Azure platform. Azure provides a range of options for hosting applications and services. Here are some examples of compute services in Azure.
    Some Compute Services :- Azure VM's, Azure kubernete, Azure Container Instances, Azure functions and etc.

**Networking**
Linking compute resources and providing access to applications is the key function of Azure networking. Networking functionality in Azure includes a range of options to connect the outside world to services and features in the global Azure datacenters.
    Some Networking services :- Azure VPN, Azure Load Balancer, Azure Firewall, Azure DNS and etc.

**Storage**
Azure provides four main types of storage services.
    1. Azure Blob Storage: Storage service for large obj (videos)
    2. Azure File Storage: Accessed and Managed like a file server
    3. Azure Queue storage: A data store for queuing and reliably delivering messages between applications.
    4. Azure Table storage: Table storage is a service that stores non-relational structured data (also known as structured NoSQL data) in the cloud, providing a key/attribute store with a schemaless design
    
    These services all share several common characteristics:
    1. **Durable** and highly available with redundancy and replication.
    2. **Secure** through automatic encryption and role-based access control.
    3. **Scalable** with virtually unlimited storage.
    4. **Managed** handling maintenance and any critical problems for you.
    5. **Accessible** from anywhere in the world over HTTP or HTTPS.

**Mobile**
With Azure, developers can create mobile back-end services for iOS, Android, and Windows apps quickly and easily. Features that used to take time and increase project risks, such as adding corporate sign-in and then connecting to on-premises resources such as SAP, Oracle, SQL Server, and SharePoint, are now simple to include.

    Other features of this service include:
    1. Offline data synchronization.
    2. Connectivity to on-premises data.
    3. Broadcasting push notifications.
    4. Autoscaling to match business needs.

**Databases**
Azure provides multiple database services to store a wide variety of data types and volumes. And with global connectivity, this data is available to users instantly.
    Some DB Services :Azure Cosmos DB(No-Sql), Azure SQL Database, SQL Server on Azure Virtual Machines and etc.

**Big data**
Data comes in all formats and sizes. When we talk about big data, we're referring to large volumes of data. Data from weather systems, communications systems, genomic research, imaging platforms, and many other scenarios generate hundreds of gigabytes of data. This amount of data makes it hard to analyze and make decisions. It's often so large that traditional forms of processing and analysis are no longer appropriate.

Open-source cluster technologies have been developed to deal with these large data sets. Azure supports a broad range of technologies and services to provide big data and analytic solutions.
     Some Services :- Azure Synapse Analytics, Azure HDInsight(Hadoop), Azure Databricks(Spark)

Fo more details about other services please refer this link : https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/tour-of-azure-services

# Different Cloud Service Models:

![image](https://user-images.githubusercontent.com/62194896/151186470-8b6de292-b02b-45ca-bb85-3b72458c544e.png)

# Shared Responsibility Model :

![image](https://user-images.githubusercontent.com/62194896/151197413-d7ed1be5-2ca2-4dbb-baff-267eb4e67b64.png)

# Top-down hierarchy of organization :

![image](https://user-images.githubusercontent.com/62194896/151199317-4a35d6f2-2671-4dba-8ad0-e71655652be9.png)

**Region Pairs :**

![image](https://user-images.githubusercontent.com/62194896/151201455-79c2befc-9995-4f4a-9d9d-a2cc48d47a85.png)

Additional advantages of region pairs:

* If an extensive Azure outage occurs, one region out of every pair is prioritized to make sure at least one is restored as quickly as possible for applications hosted in that region pair.
* Planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage.
* Data continues to reside within the same geography as its pair (except for Brazil South) for tax- and law-enforcement jurisdiction purposes.

**Azure Resource Manager**
Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features like access control, locks, and tags to secure and organize your resources after deployment.

  ![image](https://user-images.githubusercontent.com/62194896/151204806-7368fc40-fa1b-493d-bc25-f736088e542d.png)

**The benefits of using Resource Manager
With Resource Manager, you can:**

* Manage your infrastructure through declarative templates rather than scripts. A Resource Manager template is a JSON file that defines what you want to deploy to Azure.
* Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
* Redeploy your solution throughout the development life cycle and have confidence your resources are deployed in a consistent state.
* Define the dependencies between resources so they're deployed in the correct order.
* Apply access control to all services because RBAC is natively integrated into the management platform.
* Apply tags to resources to logically organize all the resources in your subscription.
* Clarify your organization's billing by viewing costs for a group of resources that share the same tag.


 # Azure Compute Core Concepts :
 
**1. Virtual Machine**
 
An Azure VM gives you the flexibility of virtualization without having to buy and maintain the physical hardware that runs the VM. You still need to configure, update, and maintain the software that runs on the VM.

Examples of when to use VM's:
1. During testing and development
2. When running applications in the cloud
3. When extending your datacenter to the cloud
4. During disaster recovery

Scale VM's in Azure:
Two features :
* Virtual machine scale sets(Auto increase or decrease of VM's based on the workloads for high availability)
* Azure Batch(Azure Batch enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs)
      
       * It is a **Compute Resource** and **IAAS**
       * Devices are launched along with VM in the backend are OS Disk, Data Disk, Virtual Network, Network Interface, Security group, Public IP
       * These all are should be part of Resource Group(for logical grouping purpose) and Subscription(for billing purpose)
       * IMAGE - Type of server (Windows server, windows 10 pro(License required), ubuntu)
       * SIZE - Size of the server (Cpus,GIB memeries)
       * Billing includes the license for windows server (We can mention and cut down the lincense cost if we have the license) called as **Azure Hybrid Benefit Pricing**
       * Username and password are needed for the user to login VM
       * DISK's :
         # Types of OS Disk's Available :
             * Premium SSD : Best for production (Better Performance)
             * Standard SSD : Best for Web server
             * Standard HDD : Best for Backup
       * Data Disk configuration is optional, We can add the data disk if we need 
       * Connection Types to VM 
                 * **RDP (Connection Protocal for windows machine)**
                 * **SSH (Connection Protocal for Linux machine)**
                 * **Bastion (Securely connect to the VM)**
       * Login to the VM and configure the IIS to host the web content into the server
       * We can host the simple HTML File that is saved at the wwwroot folder location in our computer
       * Different Types of VM's are available as Families or Series (for More details refer the Document)
       * Temporary Storage for VM is based on the size of VM
       * **Shut down from VM itself will not lead to deallocation of physical server but stopping the VM from Azure portal will**
       * Deallocation will erase the data present in the temporary storage and it changes the public ip address for VM
       * Stopped state of VM will be partially charged for compute
       * Deallocation of VM will not be charged for compute
       * Changing Dynamic ip address to Static ip address follow these steps:---
              * Disassociate the public Ip using VM->networking->network interface->ip configuration->inconfig->disassociate 
              * Choose Ip type as Static from the VM->public ip->static
              * And then Associate the static ip VM->networking->network interface->ip configuration->ip config-> associate 
       * We can check the limit for vm creation for a particular region by subcription->usage and quotas
       * **Azure Marketplace for VM** where you can install softwares for ur virtual machine
       * **Avaliablity Sets** are used to maintain the availability of VM's, If one goes down then another one back up's. It will be only in server level not app level
              * Fault domains (2-default, 3-max)      *Update domains (5-default, 20-max)  
       * Note: We can't make existing vm as part of availability sets
       * **Avaliablity Zone's** are used for backup of data center failure. It charges extra cost for bandwidth communication
       * **Note :** We can choose availability set or Avail Zone in the **Availability options** when creating VM's
       * **Azure Dedicated Host** 
              * Hardware Isolation - No other VM's will be placed on the host
              * You can control the maintenance events
              * Mostly used by the large org, (Min 91 vCpus should be utilized)
   
           
**2. Azure App Service**
  
  When to Use App Service :
   * App Service enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure. It offers automatic scaling and high availability. App Service supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.
   * This platform as a service (PaaS) environment allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications.
  
   
   Types of app services
     With App Service, you can host most common app service styles like:
       
        * Web apps
        * API apps
        * WebJobs
        * Mobile apps
 
 **3. Azure Container Instances or Azure Kubernetes Service**
 
  While virtual machines are an excellent way to reduce costs versus the investments that are necessary for physical hardware, they're still limited to a single operating system per virtual machine. If you want to run multiple instances of an application on a single host machine, containers are an excellent choice.
  
   What are containers : 
  **Containers are a virtualization environment**. 
  
  Much like running multiple virtual machines on a single physical host, you can run multiple containers on a single physical or virtual host. Unlike virtual machines, you don't manage the operating system for a container. While it's possible to create and deploy virtual machines as application demand increases, containers are designed to allow you to respond to changes on demand. With containers, you can quickly restart in case of a crash or hardware interruption. One of the most popular container engines is **Docker**, which is supported by Azure.
     
   **Major Difference between VM's and Containers**
       * VM virtualizes the Hardware's but Containers virtualizes the OS(Environments)
       * VM (Complete control over the environment), Containers(Portability and Performance)
  
  Containers are managed through a container orchestrator, which can start, stop, and scale out application instances as needed. There are two ways to manage both Docker and Microsoft-based containers in Azure: Azure Container Instances and Azure Kubernetes Service (AKS).    
   
   **Azure Container Instances**
       It offers the fastest and simplest way to run a container in Azure without having to manage any virtual machines or adopt any additional services. It's a platform as a service (PaaS).
  
   **Azure Kubernetes Service**
       The task of automating, managing, and interacting with a large number of containers is known as orchestration. Azure Kubernetes Service is a complete orchestration service for containers with distributed architectures and large volumes of containers.
  
   **What is Kubernetes**
       It Manages the containers with the Clustered Node. Scaling can be done by manual or automation. Updates are quick and if the updates are problematic then it will role back to the previous version. It also manages the storage and networking.      
       
**4. Azure Functions**
     Serverless computing is the abstraction of servers, infrastructure, and operating systems. With serverless computing, Azure takes care of managing the server infrastructure and the allocation and deallocation of resources based on demand. Serverless computing includes the **abstraction of servers, an event-driven scale, and micro-billing**.
     
    Azure has two implementations of serverless compute:

         **Azure Functions:** Functions can execute code in almost any modern language.
         **Azure Logic Apps:** Logic apps are designed in a web-based designer and can execute logic triggered by Azure services without writing any code.
         
    Refer this link for some of the common differences between Functions and Logic Apps https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-functions
         
    Refer this link for know about **Virtual Desktops** https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/windows-virtual-desktop
    
    
# Azure Virtual Network

   Azure virtual networks enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers. You can think of an Azure network as a set of resources that links other Azure resources.
   Azure virtual networks provide the following key networking capabilities:

       1. Isolation and segmentation
       2. Internet communications
       3. Communicate between Azure resources
       4. Communicate with on-premises resources
       5. Route network traffic
       6. Filter network traffic
       7. Connect virtual networks
         
  **Communicate with on-premises resources**
      
       1. Point-to-site virtual private networks The typical approach to a virtual private network (VPN) connection is from a computer outside your organization, back into your corporate network. In this case, the client computer initiates an encrypted VPN connection to connect that computer to the Azure virtual network.
       2. Site-to-site virtual private networks A site-to-site VPN links your on-premises VPN device or gateway to the Azure VPN gateway in a virtual network. In effect, the devices in Azure can appear as being on the local network. The connection is encrypted and works over the internet.
       3. Azure ExpressRoute For environments where you need greater bandwidth and even higher levels of security, Azure ExpressRoute is the best approach. ExpressRoute provides dedicated private connectivity to Azure that doesn't travel over the internet.
       
   ## Azure VPN Gateways
      
   1. Connect on-premises datacenters to virtual networks through a site-to-site connection.
   2. Connect individual devices to virtual networks through a point-to-site connection.
   3. Connect virtual networks to other virtual networks through a network-to-network connection.
      
   # Azure Virtual Network

   The Azure Virtual Network service is used to define an isolated network in Azure. The virtual network can then be used to host your resources such as Azure virtual machines. The Azure virtual network gets assigned an address space which you specify when you create an Azure virtual network. You can then add subnets to your Azure virtual network. This helps divide your network into more logical segments. An example is shown below of having multiple subnets. You could have one subnet named SubnetA in the virtual network to host your Web servers and another subnet to host the Database servers.
          ![image](https://user-images.githubusercontent.com/62194896/155876048-4b18adc3-a0a8-4e15-a57b-3c2eec7e9aa6.png)
          
   ## Network Security Groups
      
   These are used to filter network traffic to and from Azure resources in an Azure virtual network. A network security group is attached to the network interface attached to the virtual machine. A network security group consists of Inbound rules that are used to control the traffic inbound into a virtual machine. By default all traffic into a virtual machine is DENIED. You have explicitly add rules to allow traffic into a virtual machine. There are also outbound rules to control the traffic flowing out of the virtual machine. By default all traffic outbound onto the Internet is allowed.
          ![image](https://user-images.githubusercontent.com/62194896/155876102-7faeea43-35e0-4ed2-8a1f-98245794cd76.png)
          
   ## Virtual Network Peering
      
Virtual Network Peering is used to connect two Azure virtual networks together via the backbone network. Azure supports connecting two virtual networks located in the same region or networks located across regions. Once you enable virtual network peering between two virtual networks, the virtual machines can then communicate via their private IP addresses across the peering connection. You can also peer virtual networks that are located across different subscriptions. The virtual networks can't have overlapping CIDR blocks.

   ## Point-to-Site VPN Connection
      
A Point-to-Site VPN connection is used to establish a secure connection between multiple client machines and an Azure virtual network via the Internet. Below is a diagram from the Microsoft documentation on a sample scenario
         ![image](https://user-images.githubusercontent.com/62194896/155876267-fae490af-b48e-43ee-aec1-df5ec003850b.png)
         
   ## Site-to-Site VPN Connection
      
A Site-to-Site VPN connection is used to establish a secure connection between an on-premise network and an Azure network via the Internet. Below is a diagram from the Microsoft documentation on a sample scenario
         ![image](https://user-images.githubusercontent.com/62194896/155876340-1615f232-3369-4004-9b47-cef97b58aa27.png)
         
On the on-premise side, you need to have a VPN device that can route traffic via the Internet onto the VPN gateway in Azure. The VPN device can be a hardware device like a Cisco router or a software device ( e.g Windows Server 2016 running Routing and Remote services). The VPN device needs to have a publically routable IP address. The subnets in your on-premise network must not overlap with the subnets in your Azure virtual network. The Site-to-Site VPN connection uses an IPSec tunnel to encrypt the traffic. The VPN gateway resource you create in Azure is used to route encrypted traffic between your on-premise data center and your Azure virtual network.


# Azure Storage Accounts

* This service is used to store objects(Images, Videos, files, etc.) on the cloud.
* Here you can make use of different services - Blob, File shares, Queues, Table
   
## Types of different storage accounts
       
* Standard general purpose v2 (Gives access to blob, files, queue, table)
* Premium block blobs (This is the premium storage for your block blobs)
* Premium File Shares (This is the premium storage account for ur file shares)
* Premium page blobs (This is the premium storage account for ur page blobs)
       
## Blob Storage
   
* This service is for optimized for storing large amount of unstructured data
* Examples : Storing images, videos, log files, documents
* In this blob service, ucan create container. This is used to organize a set of blobs
* Block blobs - This is used to store text and binary data
* Page blobs - This is used to store virtual hard drive files that are used as disks for ur azure VM's
   
## File Service 
   
 * This is used for hosting file shares on the cloud
 * This shares can be accessed via the SMB - Server Message blob protocol
 * You can mount the files from windows, linux, macOS clients.
    
## Azure Queues
   
 * This is used for storing large amount of messages
 * These messages can be accessed from anywhere in the world by HTTP, HTTPS protocols
 * You can store millions of messages in queue
    
## Azure Table
    
 * This service is used for storing non-relational structured data
 * It is ideal for storing flexible data sets bacause it does not conform to any sort of schema
 * In the table, you can store an entity which is a set of properties
 * A property is nothing but a name-value pair
 * The partition key is used to split the data across various partitions. And the row key is used to identify an item within a partition.
    
## Active Tiers
      
 * Hot : This is optimized for data that is accessed frequently.
 * Cool : This is for data that is infrequently accessed ans stored for atleast 30 days.
 * Archive : This is for data that is rarely accessed ans stored for atleast 180 days.

## Data Redundancy 
  
 * **Locally Redundant Storage** : Data is copied synchronously three times within a single physical location in the primary region.
 * **Zone Redundant Storage** : Data is copied synchronously three availability zones in the primary region.
 * **Geo-Redundant Storage**: Data is copied synchronously three times within a single physical location in the primary region using LRS. It then copies your data asy to a single physical location in the secondary region.
 * **Geo-Zone-redundant storage** : Data is copied synchronously three availability zones in the primary region using ZRS. It then copies ur data asy to a single physical location in the secondary region 
 
 
## Azure SQL DataBase 
 
  * This is a PAAS Service, It's underlined infrastructure is managed for you. Backups are managed for you, gives high availability
      
  * Azure database for MySql :
      * Mysql is a open-source RDBMS
      * We can store the data in the form of tables
      * We can query using SQL
      * It is a fully managed database service
      * Underlying platform is managed by the service itself
      * High availability, backups, patching as well
      * Note : While connecting to mysql server from mysql workbench(Client tool) we need to enable client ip address option in 'Connection Security' in the resource
          
   * Azure database for PostgreSQL :
      * It is also open-source
      * It has support for transaction that follow the ACID concepts - Atomicity, Consistency, Isolation, Duralability
      * It also supports views, triggers, foreign keys, stored procedures
      * Fully managed database service
      * Underlying infra is managed by the service itself
      * High availability, backups and patching as well
          
   * Azure Pricing Tiers :
      1. Database Transaction Units
        * This is a blended measure of CPU, memory, input/output 
        * There are some different models available 
              * Basic   * Standard   * Premium
      2. vCore based purchasing model
        * we can independently scale compute and storage
        * WE can make use of the HYBRID benefit model if we have the license
      3. Managed Instance 
        * This is a deployment model that provides native integration with the azure virtual network service
        * It provides 100% Compatibility with the latest sql server features
        * Infra is managed for u
        * Easy Migration of on-premises databases to the managed instance
 
 ## Azure Datawarehouse Enterprise Architecture
 
   1. Ingest : Data Synapse Pipeline, Data Lake
   2. Store : Azure data lake gen 2 storage account 
   3. Prep and Train : Azure synapse apache spark, Azure synapse dedicated sql pool 
        
   (Note : while creating storage account need to select checkbox for enable hierarchical namespace for Data lake)
        
 ## Azure Cosmos DB
       
   * It is a No-sql database or Non-relational database
   * It is fully managed nosql database
   * The database provides fast response and is highly scalable
   * Infra is managed by service itself
   * Commonly used for web, mobile, gaming and IOT appplication that needs to be handled mssive amount of data
        
   ### CosmosDB API
   * Core SQL API : If u want to query for items using sql
   * MongoDB API : If u want to host a MongoDB compatible database
   * Cassandra API : If u want to host a Cassandra compatible database
   * Gremlin API : If u want to host a graph-based database
   * Table API :If u want to host a tables-based database
        
## Difference between Azure SQL database and Azure cosmosDB
 
   * Azure sql database : when u need to have relationship between tables, when u want to have a constraints like foreign key
   * Azure cosmosDB : No sql data store, flexible schema, no need to joins between data structures

## Azure Databricks
        
   * It is a platform as a service, underlying infra is managed by the service itself. 
   * It is fully managed, cloud based platform used for Big data and Machine Learning
   * Databricks itself as a tool that is used to analyzeyour data
   * It is based on **Apache Spark**
   * Apache spark is a processing engine that is used to analyze big data using SQL, machine learning, graph processing, or real time stream analysis
   * Azure Data bricks is a managed version of Databricks
        
## Complete Notes on Azure storage 
   
## Azure Storage Accounts

### Types of storage accounts

 * General-purpose v2 accounts – This is recommended for most scenarios. This storage account type provides the blob, file , queue and table service.

 * Premium block blobs – This is specifically when you want premium performance for storing block or append blobs.

 * Premium file shares – This is specifically when you want premium performance for file-only storage.

 * Premium page blobs – This is specifically when you want premium performance for page blobs.

 * The most common type of storage account is the General Purpose v2 storage account.

 * Use case scenarios for the different services in a General Purpose v2 storage account

##Blob service

 * This is object storage for the cloud.

 * Here you can store massive amounts of unstructured data on the cloud.

 * This is highly recommended when you want to store images, documents, video and audio files.

 * Within the blob service, you create a container that is used to store the blob objects.

## There are three different types of blobs

 1. Block blobs – This is used for storing text and binary data.

 2. Append blobs – This is ideal for logging data.

 3. Page blobs – This is used to store virtual hard disk files for Azure virtual machines.


Note : To use the Blob service you have to first create a container and then upload the blobs or objects into the container.
When you upload an object or blob to the service, each bob gets a unique URL which you can access if you are assigned the right permissions


## File service - Use this service if you need to store files that need to be accessed by machines using the SMB (Server Message Block) protocol

In the File service, you can first go ahead and create a file share.

You can then mount this file share from different machines. You can't mount drives with the Blob service.


## Table service - Use this if you want to store NoSQL data or table like data.

It's easy and simple to create a table and add data from the Azure portal itself.


## Queue service - Use this if you want to exchange messages between components of your application


## Azure Storage Accounts - Replication

There are different replication techniques available to make your data highly available.

The different replication techniques available

1. Locally-redundant storage (LRS) - Here data is replicated synchronously three times within a physical location in the primary region.

2. Zone-redundant storage (ZRS) - Here data is replicated synchronously across three Azure availability zones in the primary region. This is good when you want to have data present even in the event of a data center failure.

3. Geo-redundant storage (GRS) - Here data is replicated synchronously three times in the primary region, then replicated asynchronously to the secondary region.

4. Read access Geo-redundant storage (RA-GRS) - Here data is replicated synchronously three times in the primary region, then replicated asynchronously to the secondary region. Here the data in the secondary region is also available for read-only purposes.

## Azure Storage Accounts - Access tiers

Access tiers help you optimize the storage costs and access costs for your data. The different access tiers are

1. Hot – This is optimized for storing data that is accessed frequently. This can be set at the account level.

2. Cool – This is optimized for storing data that is infrequently accessed and stored for at least 30 days. This can be set at the account level.

Note:- For the Cool Access tier , the storage costs are lower than the Hot tier. But the access costs are higher than the Hot access tier.

3. Archive tier - This is optimized for storing data that is rarely accessed and stored for at least 180 days. This can be set only at the blob level.

Note:- When a blob is in the archive tier, you can’t access the blob. You have to rehydrate the blob first before it can be accessed.

Also the storage costs are the least when it comes to the Archive access tier. But the access costs are the highest.

## Azure SQL Database (Platform as a service)

* This is a service that allows you to create a managed Microsoft SQL Server database on the cloud. The advantages of using this service

* You don't have to manage the underlying infrastructure. This is managed by Azure.

* You have a variety of purchasing options

* You have automated backups. This reduces the burden of managing backups.

* It gives you a service level agreement of 99.99%

* If you need to have more control over the database engine, then consider installing the SQL Server engine on an Azure virtual machine.

## Azure Synapse Analytics

* This was formerly known as Azure SQL Data warehouse.

* This service is used for enterprise data warehousing and Big Data Analytics

* When you want to perform analysis on a large data set , consider using this service.

* Below is a snapshot from the Microsoft documentation on where this tool fits in the picture of Big Data


## Azure Cosmos DB

* This is a data store that companies can opt for , when they want to get low latency access to their data and they want high availability for their data.

* It is a multi-model database. This means you can choose from a variety of options when it comes to what type of data you want to store in the account.


## Azure Load Balancer 

* This is service is used to distribute the incoming network traffic across a group of backend resources of servers

* You can define TWO types of load balancers - Public or Private 

* You have 2 SKU's for the load balancer - Standard and Basic load balancer

### Features of Basic Load Balancer 

* Pricing : You are not charged for the running cost for the load balancer

* No SLA : There is no SLA (If u need SLA for critical app's then choose standard)

* Backend Machines : Here the machines needs to be part of scale set or availability set

* Support for Zones : There is no support for availability zones

### Features of Standard Load Balancer 

* Pricing : Charged per hour

* No SLA : There is an SLA of 99.99%

* Backend Machines : Here the machines can be part of scale set or availability set or individual machines 

* Support for Zones : Here you get support for availability zones

### Components of Load Balancer 

1. Frontend IP : Here you define the public IP address for the load balancer
2. Backend Pool : This contains the backend virtual machines 
3. Health Probes : This helps to check the status of the backend pool 
4. Rules : The load balacing rules define how to distribute the incoming traffic

## Azure Using Powershell - Notes

The following can be used as a reference for the previous chapter

1. You can get the installation notes from the following Microsoft documentation link

   https://docs.microsoft.com/en-us/powershell/azure/install-az-ps?view=azps-6.3.0

Just ensure to also add the following flag when installing Azure PowerShell ( -AllowClobber).

   Install-Module -Name Az -Scope CurrentUser -Repository PSGallery -Force -AllowClobber

2. To connect to your Azure account, you can use the following command

   Connect-AzAccount

3. To list down the resource groups in your Azure account, you can use the following command

   Get-AzResourceGroup
   
## Azure Using Azure CLI - Notes

The following can be used as a reference for the previous chapter

1. You can get the installation notes from the following Microsoft documentation link

   https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli

2. To connect to your Azure account, you can use the following command

   az login

3. To list down the resource groups in your Azure account, you can use the following command

   az group list
   
## Azure App Service

* This is an HTTP-based service that allows you to host web applications, REST API's and mobile back ends. You can develop a program in programming languages such as .NET, .NET Core, Java, Ruby, Node.js, PHP and Python.

* Here you don't need to manage the underlying infrastructure. It allows you to focus on code development.

* Each App service needs to be associated with an App Service Plan.

* Each App service plan has an associated cost per month and also has specific features based on the plan you choose.

## Virtual Machine Scale Sets

* This service allows you to create and manage a group of identical load balanced virtual machines.

* Here the number of Virtual Machine instances in the scale set can scale based on demand

* This is the best service if you want to add scalability to your application

## Azure Load Balancer

* The Azure Load balancer is used to distribute incoming network traffic to a backend group of servers.

* This service helps increase the availability of your entire application architecture

* Here the Load Balancer would take the incoming requests from the users and direct the requests to virtual machines running in an Azure virtual network.

* If you have a web application running on the backend virtual machines, the requests would be distributed across the virtual machines by the Azure Load Balancer.

## Other tools to access Azure resources

* You can use other tools to access and work with Azure resources

* You can use PowerShell which can work on Windows, macOS and Linux

* You can use the Azure command line interface which can work on Windows, macOS and Linux

* You can use Azure cloud shell from the browser, which can then work on any operating system which has browser support
   
## Azure Functions

* This service allows you to run small pieces of code as functions
* Here you just develop and upload the code to an azure function
* You get billed for the amount of time you code gets run
* You can use many languages like C#, Java, Python, Powershell

### Azure Function Triggers

* HTTP Trigger : Here an HTTP call can be made to the function
* Timer : Here the function can be run on a schedule
* Blob Storage : Whenever a blob event occurs 
* Azure services : Azure event hubs, Azure service bus

### Pricing plans

* Consumption Plan – Here you only pay for the time the code runs.
* App Service Plan – If you already have an App Service plan that runs a web application, you can reuse the same plan to run Azure Functions. This would save on cost if you already have an App Service Plan in place.
* Premium Plan – Here you get a number of pre-warmed instances that are always online and ready to run your functions. The plan also automatically adds more compute when required.

## Azure Logic Apps

* This is a cloud service that helps you schedule, automate and orchestrate tasks , business processes and workflows.

### How it works

* You first design a workflow in Azure Logic Apps

* Each workflow starts with a trigger.

* The trigger is fired via a specific event

* When the trigger is fired , the Logic App engine creates a logic app instance that runs the workflow.

### Connectors for Azure Logic Apps

* These connectors provide easy access to event, data and actions that are sent from external applications, services , systems or platforms.

* You have built-in connectors that can connect to Azure services such as Azure functions, Azure API Apps etc.

* You have Managed connectors that can connect to platforms such as Office 365, Microsoft Dynamics.

## Azure Traffic Manager

* The Azure Traffic Manager service is a DNS-based traffic load balancer that distributes traffic across services that are distributed across different Azure regions.

* The Traffic Manager service is used to direct client requests to the most appropriate service endpoint that is based on a traffic-routing method and the health of the endpoints.

### The different traffic routing methods available for the Azure Traffic Manager are

1. Priority – Route traffic to another endpoint in case the primary fails.

2. Weighted – Route traffic to different endpoints based on weight.

3. Performance - you want end users to use the "closest" endpoint in terms of the lowest network latency.

4. Geographic - geographic location their DNS query originates from.

5. Multivalue – Here different endpoints are sent to the client. The client then selects the endpoint to send the request to.

6. Subnet – This maps a set of end-user IP address ranges to a specific endpoint within a Traffic Manager profile.

* Below is an example of the Priority routing method that can be used with the Azure Traffic Manager service

      Here we are assuming that a company has similar web applications , both are running using the Azure Web App service. One web application is running in the East         US Region and the other is running in the West US Region.
      
      ![image](https://user-images.githubusercontent.com/62194896/161919715-a8ad1661-6400-4ac3-b869-3f3852c5706b.png)
      
      1. Here we create a Traffic Manager profile and create two endpoints. Each endpoint points to each Azure Web app respectively. We assign a priority of 1 to the         service endpoint attached to the Azure Web App running in the East US region and  a priority of 2 to the other service endpoint.

      1. Here users would make requests to the Traffic Manager service.

      2. The requests could be initially be directed to an Azure Web App located in the East US region , since there is a priority of 1 to the service endpoint               attached to this endpoint.

      ![image](https://user-images.githubusercontent.com/62194896/161919937-50608cbb-8e2b-48a9-84fa-0b0b7c4622eb.png)
      
* If you use the Weighted Routing method , you can actually load balance requests across multiple service endpoints

      ![image](https://user-images.githubusercontent.com/62194896/161920220-52a5b58a-9ea2-44a0-a170-3e0b4f11c8be.png)

      Over here , users requests would be directed or load balanced across both web applications running in different regions.
      
* In the Performance routing method as shown below, users will be directed based on the least latency of an endpoint.
      
      [image](https://user-images.githubusercontent.com/62194896/161920413-2c3e84e8-9681-4ed6-9532-cdfed02daa2b.png)
      
* And then we have the Geographic routing method wherein users would be directed to an endpoint based on their geographic location

      ![image](https://user-images.githubusercontent.com/62194896/161920516-48c594d5-7ac3-41a1-898f-fd8ded989d63.png)












