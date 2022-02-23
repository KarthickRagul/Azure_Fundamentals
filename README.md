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
       
       
