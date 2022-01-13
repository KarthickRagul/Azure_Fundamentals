# Azure_Fundamentals
Key notes for Azure Fundamentals

What is Cloud computing :
   * Delivery of computing services such as servers, storage, database, networking, software and etc. through internet
   * As Pay As You Go Pricing
Advantages :
    * Less Management
    * Less Investments
    * Less Operations
    * Focus on business
 
 Azure Core Concepts :
 1. Virtual Machine 
       * It is a **Compute Resource** and **IAAS**
       * Devices are launched along with VM in the backend are OS Disk, Data Disk, Virtual Network, Network Interface, Security group, Public IP
       * These all are should be part of Resource Group(for logical grouping purpose) and Subscription(for billing purpose)
       * IMAGE - Type of server (Windows server, windows 10 pro(License required), ubuntu)
       * SIZE - Size of the server (Cpus,GIB memeries)
       * Billing includes the license for windows server (We can mention and cut down the lincense cost if we have the license) called as **Azure Hybrid Benefit Pricing**
       * Username and password are needed for the user to login VM
       * DISK's :
         * Types of OS Disk's Available :
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
           
       

