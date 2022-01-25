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

 # Azure Core Concepts :
 
 **1. Virtual Machine**
      
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
                 * **RDP (Connection using windows)**
                 * **SSH (Connection using Linux)**
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
           

       

